---
date: 2025-12-25
description: เรียนรู้วิธีแปลง PSD เป็น PNG ด้วย Aspose.PSD สำหรับ Java พร้อมการสนับสนุนการตรวจสอบการขัดจังหวะ
  รวมถึงตัวอย่างการขัดจังหวะของเธรด Java และเคล็ดลับการบันทึก PSD เป็น PNG
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: วิธีแปลง PSD เป็น PNG พร้อมการสนับสนุน Interrupt Monitor ใน Aspose.PSD สำหรับ
  Java
url: /th/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น PNG ด้วย Interrupt Monitor ใน Aspose.PSD for Java

## บทนำ

หากคุณต้องการ **แปลง PSD เป็น PNG** พร้อมการควบคุมเต็มรูปแบบสำหรับการแปลงภาพที่ใช้เวลานาน Aspose.PSD for Java’s Interrupt Monitor** คือเครื่องมือที่คุณกำลังมองหา** ในบทแนะนำนี้เราจะพาคุณผ่าน **ตัวอย่างการขัดจังหวะเธรดใน Java** ที่ทำให้คุณหยุดการแปลงระหว่างกระบวนการได้ ให้คุณมีความยืดหยุ่นในการจัดการทรัพยากร, กำหนดเวลา, หรือรับมือกับการยกเลิกของผู้ใช้

## คำตอบสั้น
- **Interrupt Monitor ทำหน้าที่อะไร?** มันช่วยให้คุณส่งสัญญาณให้การแปลงภาพที่กำลังทำงานหยุดอย่างปลอดภัย  
- **ฉันสามารถแปลง PSD เป็น PNG ด้วยมันได้หรือไม่?** ได้ – monitor ทำงานกับการบันทึกใด ๆ รวมถึง PNG  
- **ต้องใช้เธรดแยกหรือไม่?** โดยทั่วไปคุณจะรันการแปลงในเธรดแยกเพื่อให้สามารถขัดจังหวะได้  
- **ต้องใช้เวอร์ชัน Aspose.PSD ใด?** เวอร์ชันล่าสุดที่มี `com.aspose.psd.multithreading.InterruptMonitor`  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** ต้องมี – ต้องใช้ลิขสิทธิ์ Aspose.PSD ที่ถูกต้องสำหรับการใช้งานที่ไม่ใช่ trial

## “แปลง PSD เป็น PNG” ด้วย Interrupt Monitor คืออะไร?

การแปลงไฟล์ Photoshop ขนาดใหญ่ (PSD/PSB) เป็นภาพ PNG อาจใช้ CPU มาก การแนบ **Interrupt Monitor** ไปกับงานแปลงทำให้คุณสามารถหยุดกระบวนการได้โดยโปรแกรม – เหมาะสำหรับเว็บเซอร์วิส, งานแบตช์, หรือแอปพลิเคชัน UI ที่ผู้ใช้อาจยกเลิกการทำงาน

## ทำไมต้องใช้ Interrupt Monitor?

- **UI ตอบสนองเร็ว:** ป้องกันแอปพลิเคชันของคุณจากการค้างขณะไฟล์ใหญ่กำลังประมวลผล  
- **การจัดการทรัพยากร:** หยุดการแปลงที่ใช้เวลา หรือหน่วยความจำเกินขอบเขต  
- **การจัดการข้อผิดพลาด:** ทำความสะอาดไฟล์ผลลัพธ์บางส่วนอย่างราบรื่นเมื่อเกิดการขัดจังหวะ

## ข้อกำหนดเบื้องต้น

- สภาพแวดล้อมการพัฒนา Java (JDK 8 หรือใหม่กว่า)  
- ไลบรารี Aspose.PSD for Java – ดาวน์โหลด **[ที่นี่](https://releases.aspose.com/psd/java/)**  
- โฟลเดอร์ที่มีไฟล์ PSD/PSB ที่คุณต้องการทำงาน

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็น ซึ่งจะทำให้คุณเข้าถึงตัวเลือกภาพ, interrupt monitor, และยูทิลิตี้เธรดได้

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## คู่มือขั้นตอน‑โดย‑ขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธเต็มที่ไฟล์ PSD ของคุณอยู่

### ขั้นตอนที่ 2: กำหนด Image Options และ Output Path

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

ที่นี่เราจะ **บันทึก PSD เป็น PNG** ด้วย `PngOptions` ปรับชื่อไฟล์ตามต้องการ

### ขั้นตอนที่ 3: เริ่มต้น Interrupt Monitor และ SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

อินสแตนซ์ `InterruptMonitor` จะถูกใช้ต่อไปเพื่อหยุดการแปลง `SaveImageWorker` เชื่อม monitor กับงานแปลง

### ขั้นตอนที่ 4: เริ่มการแปลงภาพในเธรดแยก

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

เราจะรันการแปลงบนเธรดพื้นหลังเพื่อให้เธรดหลักยังคงตอบสนอง คำสั่ง `Thread.sleep(3000)` จำลองสถานการณ์ timeout

### ขั้นตอนที่ 5: ขัดจังหวะกระบวนการ (ตัวอย่างการขัดจังหวะเธรด Java)

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

การเรียก `monitor.interrupt()` จะกระตุ้นโลจิก **วิธีขัดจังหวะ monitor** หลังจากขัดจังหวะเราจะทำความสะอาดไฟล์ PNG ที่เขียนบางส่วน

## ปัญหาที่พบบ่อยและวิธีแก้

| Issue | Reason | Fix |
|-------|--------|-----|
| การแปลงไม่หยุด | Monitor ไม่ได้เชื่อมกับ worker | ตรวจสอบให้ `SaveImageWorker` ได้รับอินสแตนซ์ `InterruptMonitor` เดียวกัน |
| ไฟล์ผลลัพธ์ยังคงอยู่หลังขัดจังหวะ | โค้ดทำความสะอาดไม่ทำงาน | ยืนยันว่า `finally` block ทำงานและพาธไฟล์ถูกต้อง |
| `OutOfMemoryError` กับไฟล์ PSB ขนาดใหญ่ | ไม่ได้ใช้ตัวเลือกสตรีมมิ่ง | ใช้ `PsdImage` กับ `LoadOptions` ที่เปิดใช้งานการโหลดแบบประหยัดหน่วยความจำ |

## คำถามที่พบบ่อย

### Q1: Interrupt Monitor ใน Aspose.PSD for Java คืออะไร?

A1: Interrupt Monitor ช่วยให้ผู้พัฒนาสามารถ **จัดการและขัดจังหวะกระบวนการแปลงภาพ** ได้ ให้คุณควบคุมงานที่ใช้เวลานานอย่างละเอียด

### Q2: จะได้ไลบรารี Aspose.PSD สำหรับ Java อย่างไร?

A2: คุณสามารถดาวน์โหลดไลบรารี Aspose.PSD for Java **[ที่นี่](https://releases.aspose.com/psd/java/)**

### Q3: มีรุ่นทดลองฟรีสำหรับ Aspose.PSD for Java หรือไม่?

A3: มี – คุณสามารถลองรุ่นทดลองของ Aspose.PSD **[ที่นี่](https://releases.aspose.com/)**

### Q4: จะหา support สำหรับ Aspose.PSD for Java ได้จากที่ไหน?

A4: เยี่ยมชมฟอรั่มสนับสนุน Aspose.PSD for Java **[ที่นี่](https://forum.aspose.com/c/psd/34)**

### Q5: จะซื้อไลเซนส์สำหรับ Aspose.PSD for Java ได้อย่างไร?

A5: คุณสามารถซื้อไลเซนส์สำหรับ Aspose.PSD for Java **[ที่นี่](https://purchase.aspose.com/buy)**

---

**Last Updated:** 2025-12-25  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}