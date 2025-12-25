---
date: 2025-12-25
description: เรียนการสอนการประมวลผลภาพด้วย Java เกี่ยวกับการบันทึกไฟล์ PSD เป็น JPG
  โดยใช้ worker threads คู่มือนี้แสดงวิธีการบันทึกภาพด้วยเธรดอย่างมีประสิทธิภาพ
linktitle: Save Images using Worker Threads
second_title: Aspose.PSD Java API
title: บทแนะนำการประมวลผลภาพด้วย Java – บันทึกรูปภาพด้วยเธรดทำงาน
url: /th/java/advanced-techniques/save-images-worker-threads/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บทเรียนการประมวลผลภาพด้วย Java – บันทึกรูปภาพด้วย Worker Threads

## Introduction

ยินดีต้อนรับสู่ **java image processing tutorial** นี้ ที่เราจะสาธิตวิธีบันทึกไฟล์ PSD เป็น JPG (หรือรูปแบบอื่น) ด้วย **worker threads** ใน Aspose.PSD for Java การประมวลผลภาพแบบหลายเธรดสามารถลดเวลาการทำงานได้อย่างมาก โดยเฉพาะเมื่อคุณต้องแปลงไฟล์จำนวนมากในชุดต่อเนื่อง ในไม่กี่นาทีต่อไป คุณจะได้เรียนรู้ว่าทำไมการใช้เธรดจึงสำคัญ วิธีตั้งค่าอย่างปลอดภัย และดูตัวอย่างโค้ดที่สมบูรณ์พร้อมรัน

## Quick Answers
- **บทเรียนนี้ครอบคลุมอะไร?** Saving images with worker threads using Aspose.PSD for Java.  
- **ทำไมต้องใช้เธรด?** To parallel‑process multiple images and improve throughput.  
- **ต้องการไลเซนส์หรือไม่?** A temporary license is required for production; a free trial works for testing.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 or higher.  
- **สามารถแปลง PSD เป็น JPG ได้หรือไม่?** Yes – the tutorial demonstrates saving as any supported format.  

## What is java image processing tutorial?

A *java image processing tutorial* สอนคุณวิธีจัดการ, แปลง, และส่งออกไฟล์ภาพโดยโปรแกรมใน Java ในคู่มือนี้เน้นที่ **saving images efficiently** โดยการย้ายงาน I/O ที่หนักไปยังเธรดพื้นหลัง.

## Why use worker threads for saving images?

- **ประสิทธิภาพ:** Parallel execution utilizes multiple CPU cores, reducing overall processing time.  
- **ความตอบสนอง:** Your main application stays responsive while large files are being saved.  
- **ความสามารถในการขยาย:** Easily extend the approach to handle thousands of files in a batch job.  

## Prerequisites

ก่อนที่เราจะเริ่ม โปรดตรวจสอบว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้พร้อมแล้ว:

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
- ไลบรารี Aspose.PSD for Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/).  
- สภาพแวดล้อมการพัฒนาตั้งค่าไว้ด้วย Java (JDK 8 หรือใหม่กว่า)  

## Import Packages

ในโครงการ Java ของคุณ ให้เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นสำหรับการทำงานกับ Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ImageOptionsBase;
import com.aspose.psd.coreexceptions.OperationInterruptedException;
import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.multithreading.InterruptMonitor;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

### Step 1: Initialize `SaveImageWorker`

สร้างคลาสชื่อ `SaveImageWorker` และกำหนดตัวแปรที่จำเป็น Worker นี้จะบรรจุข้อมูลทั้งหมดที่ต้องใช้สำหรับการบันทึกหนึ่งครั้ง

```java
public class SaveImageWorker {
    // ... (Refer to provided code for variable declarations)
    
    public SaveImageWorker(String inputPath, String outputPath, ImageOptionsBase saveOptions, InterruptMonitor monitor) {
        // Constructor logic
    }
    
    // ... (Refer to provided code for additional methods)
}
```

### Step 2: Define `ThreadProc` Method

ทำการ Implement เมธอด `ThreadProc` เพื่อแปลงภาพจากรูปแบบหนึ่งเป็นอีกรูปแบบหนึ่งพร้อมจัดการการขัดจังหวะอย่างราบรื่น

```java
public String ThreadProc() {
    Image image = Image.load(this.inputPath);

    InterruptMonitor.setThreadLocalInstance(this.monitor);

    try {
        image.save(this.outputPath, this.saveOptions);
    } catch (OperationInterruptedException e) {
        System.out.println("The save thread #" + Thread.currentThread().getId() + " finishes at " + getDateTime().toString());
        System.out.println(e);
    } catch (Exception e) {
        System.out.println(e);
    } finally {
        InterruptMonitor.setThreadLocalInstance(null);
    }

    return "Hello Aspose";
}
```

### Step 3: Utilize `SaveImageWorker` in Your Application

ในแอปพลิเคชันหลักของคุณ สร้างอินสแตนซ์ของ `SaveImageWorker` และเรียก `ThreadProc` เพื่อดำเนินการบันทึกบนเธรดพื้นหลัง

```java
public class MainApplication {
    public static void main(String[] args) {
        // ... (Initialize inputPath, outputPath, saveOptions, and monitor)
        
        SaveImageWorker saveImageWorker = new SaveImageWorker(inputPath, outputPath, saveOptions, monitor);
        String result = saveImageWorker.ThreadProc();
        
        // ... (Handle the result as needed)
    }
}
```

## Common Issues and Solutions

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **เธรดค้าง** | `InterruptMonitor` not cleared | Ensure `InterruptMonitor.setThreadLocalInstance(null)` runs in `finally`. |
| **รูปแบบที่ไม่รองรับ** | Wrong `ImageOptionsBase` subclass | Use `JpegOptions`, `PngOptions`, etc., matching the desired output. |
| **หน่วยความจำไม่พอ** | Large PSD loaded on UI thread | Load and save inside the worker thread; consider streaming for huge files. |

## Frequently Asked Questions

### Q1: Aspose.PSD for Java เหมาะสำหรับการประมวลผลภาพแบบหลายเธรดหรือไม่?

A1: ใช่, Aspose.PSD for Java มีการสนับสนุนการทำงานหลายเธรดในตัว ทำให้คุณสามารถเพิ่มประสิทธิภาพในการประมวลผลภาพได้

### Q2: จะหาเอกสารรายละเอียดของ Aspose.PSD for Java ได้จากที่ไหน?

A2: คุณสามารถอ้างอิงเอกสารได้ที่ [here](https://reference.aspose.com/psd/java/) เพื่อรับข้อมูลที่ครอบคลุมเกี่ยวกับ Aspose.PSD for Java.

### Q3: จะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD for Java ได้อย่างไร?

A3: คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/) เพื่อสำรวจความสามารถทั้งหมดของ Aspose.PSD for Java.

### Q4: มีตัวเลือกการสนับสนุนอะไรบ้างสำหรับ Aspose.PSD for Java?

A4: หากต้องการความช่วยเหลือหรือสอบถามใด ๆ โปรดเยี่ยมชม [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) เพื่อเชื่อมต่อกับชุมชนและผู้เชี่ยวชาญ

### Q5: จะซื้อ Aspose.PSD for Java ได้จากที่ไหน?

A5: เพื่อซื้อ Aspose.PSD for Java ให้ไปที่ [purchase page](https://purchase.aspose.com/buy).

### Q6: สามารถแปลง PSD เป็น JPG ด้วยวิธีนี้ได้หรือไม่?

A6: แน่นอน ใช้ `JpegOptions` เป็นอาร์กิวเมนต์ `saveOptions` เมื่อเรียก `image.save(...)`.

### Q7: ควรสร้างเธรดกี่ตัวเพื่อประสิทธิภาพที่ดีที่สุด?

A7: กฎทั่วไปคือให้จำนวนเธรดเท่ากับจำนวนคอร์ CPU ที่พร้อมใช้งาน (`Runtime.getRuntime().availableProcessors()`), แต่ควรทดสอบกับภาระงานของคุณเสมอ.

## Conclusion

คุณได้เชี่ยวชาญ **java image processing tutorial** ที่แสดงวิธี **save images with threads** ด้วย Aspose.PSD for Java แล้ว โดยการบรรจุตรรกะการบันทึกไว้ในคลาส worker และใช้ `InterruptMonitor` คุณจะได้ความเร็วและความทนทานพร้อมกัน อย่าลังเลที่จะขยายรูปแบบนี้เพื่อประมวลผลโฟลเดอร์เป็นชุด, เพิ่มการรายงานความคืบหน้า, หรือรวมเข้ากับ pipeline การประมวลผลภาพที่ใหญ่ขึ้น.

---

**Last Updated:** 2025-12-25  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}