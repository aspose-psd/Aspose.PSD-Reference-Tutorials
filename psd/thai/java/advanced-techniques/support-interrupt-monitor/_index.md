---
date: 2026-06-08
description: เรียนรู้วิธีบันทึกไฟล์ PSD เป็น PNG ด้วย Aspose.PSD for Java และหยุดการแปลงเมื่อจำเป็น
  จัดการกระบวนการทำงานของภาพอย่างมีประสิทธิภาพ
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: การสนับสนุนสำหรับ Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: วิธีบันทึกไฟล์ PSD เป็น PNG ด้วย Interrupt Monitor ใน Aspose.PSD for Java
url: /th/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก PSD เป็น PNG ด้วย Interrupt Monitor ใน Aspose.PSD สำหรับ Java

## บทนำ

หากคุณต้องการ **บันทึก PSD เป็น PNG** พร้อมการควบคุมเต็มที่สำหรับการแปลงที่ใช้เวลานาน, Interrupt Monitor ของ Aspose.PSD สำหรับ Java จะมอบสิ่งนั้นให้คุณ ในบทเรียนนี้เราจะอธิบายการตั้งค่า monitor, การแปลงไฟล์ PSD เป็น PNG, และการยกเลิกการทำงานอย่างปลอดภัยเมื่อจำเป็น คุณยังจะได้เห็นว่ามันเข้ากับกระบวนการประมวลผลภาพทั่วไปอย่างไรและทำไมจึงเป็นสิ่งจำเป็นสำหรับแอปพลิเคชันที่แข็งแรง

## คำตอบสั้น
- **ฉันสามารถขัดจังหวะการแปลง PSD‑to‑PNG ได้หรือไม่?** ใช่, ใช้ `InterruptMonitor` เพื่อหยุดกระบวนการตามต้องการ.  
- **เมธอดใดที่บันทึก PSD เป็น PNG?** เรียก `save(outputPath, new PngOptions())`.  
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์; มีการทดลองใช้ฟรี.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** รองรับ Java 8 และรุ่นต่อ ๆ ไปอย่างเต็มที่.  
- **ไลบรารีนี้ปลอดภัยต่อการทำงานหลายเธรดหรือไม่?** การแปลงสามารถทำงานในเธรดแยกต่างหาก; monitor จัดการการขัดจังหวะได้อย่างปลอดภัย.

## ข้อกำหนดเบื้องต้น

ก่อนจะลงลึกในรายละเอียดการใช้ Interrupt Monitor, โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งาน:

- **สภาพแวดล้อมการพัฒนา Java:** ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ.  
- **ไลบรารี Aspose.PSD:** รับไลบรารี Aspose.PSD สำหรับ Java คุณสามารถดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/psd/java/). คุณยังสามารถเยี่ยมชมเว็บไซต์หลักของ Aspose ได้ [ที่นี่](https://releases.aspose.com/).  
- **ไดเรกทอรีเอกสาร:** มีไดเรกทอรีที่กำหนดไว้สำหรับเอกสาร PSD ของคุณ.

## นำเข้าแพ็กเกจ

เริ่มต้นโดยการนำเข้าแพ็กเกจที่จำเป็นเข้าสู่โครงการ Java ของคุณ ซึ่งจะทำให้คุณเข้าถึงฟังก์ชันของ Aspose.PSD ได้

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

ตอนนี้เราจะทำการแยกโค้ดตัวอย่างเป็นขั้นตอนเพื่อรวม Interrupt Monitor เข้าในโครงการ Aspose.PSD สำหรับ Java ของคุณ

## วิธีบันทึก PSD เป็น PNG ด้วย Interrupt Monitor?

`PsdImage` แสดงถึงเอกสาร PSD ที่โหลดเข้าสู่หน่วยความจำ.  
`SaveImageWorker` ทำการแปลงภาพในเธรดแยกต่างหาก.  

โหลดไฟล์ PSD ของคุณด้วย `new PsdImage("source.psd")`, แนบ `InterruptMonitor` ไปยัง `SaveImageWorker`, แล้วเรียก `save("output.png", new PngOptions())`. Monitor จะตรวจสอบคำขอการยกเลิกและยุติการแปลงอย่างสะอาด, ส่งการควบคุมกลับไปยังแอปพลิเคชันของคุณภายในไม่กี่มิลลิวินาที.

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ “Your Document Directory” ด้วยเส้นทางจริงที่เก็บเอกสาร PSD ของคุณ.

### ขั้นตอนที่ 2: กำหนดตัวเลือกภาพและเส้นทางเอาต์พุต

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

กำหนดตัวเลือกภาพ, ไฟล์ PSD ต้นทาง, และเส้นทางเอาต์พุตที่ต้องการสำหรับภาพที่แปลงแล้ว.

### ขั้นตอนที่ 3: เริ่มต้น Interrupt Monitor และ SaveImageWorker

คลาส `InterruptMonitor` ตรวจสอบการแปลงที่กำลังทำงานและสามารถขัดจังหวะได้เมื่อเรียก `requestInterrupt()`.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

สร้างอินสแตนซ์ของ `InterruptMonitor` และ `SaveImageWorker`, เชื่อมต่อ monitor กับ worker ที่ทำการแปลงภาพ.

### ขั้นตอนที่ 4: เริ่มเธรดการแปลงภาพ

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

เริ่มเธรดใหม่สำหรับกระบวนการแปลงภาพและกำหนดช่วงเวลา timeout เพื่อคาดการณ์การขัดจังหวะ.

### ขั้นตอนที่ 5: ขัดจังหวะกระบวนการ

การเรียก `monitor.requestInterrupt()` จะสั่งให้ monitor ยกเลิกการแปลงที่กำลังดำเนินอยู่.

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

ขัดจังหวะกระบวนการแปลงภาพโดยใช้ `InterruptMonitor` และรอให้การขัดจังหวะเสร็จสมบูรณ์. สุดท้ายทำความสะอาดโดยการลบไฟล์เอาต์พุต.

## ทำไมต้องใช้ Interrupt Monitor สำหรับการแปลง PSD‑to‑PNG

Aspose.PSD รองรับ **รูปแบบเอาต์พุตกว่า 30** ประเภท, รวมถึง PNG, JPEG, BMP, และ TIFF, และสามารถประมวลผลไฟล์ขนาดถึง **500 MB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ. การเพิ่ม interrupt monitor จะช่วยลดการใช้ CPU ที่สูญเปล่าและเพิ่มความตอบสนองในสายงานประมวลผลแบบแบตช์, โดยเฉพาะเมื่อการแปลงใช้เวลานานเกินกว่าที่คาดไว้.

## ปัญหาทั่วไปและวิธีแก้

- **การแปลงค้างโดยไม่มีที่สิ้นสุด:** ตรวจสอบให้แน่ใจว่า monitor ถูกแนบ **ก่อน** เรียก `save`.  
- **ไฟล์เอาต์พุตเสียหายหลังจากการขัดจังหวะ:** monitor จะยกเลิกอย่างสะอาด; อย่างไรก็ตาม ควรตรวจสอบว่าไฟล์มีอยู่ก่อนใช้งานเสมอ.  
- **ข้อกังวลเรื่องความปลอดภัยของเธรด:** รันการแปลงแต่ละรายการในเธรดของตนเอง; monitor มีผลต่อ worker ที่เชื่อมโยงเท่านั้น.

## คำถามที่พบบ่อย

**Q1: Interrupt Monitor ใน Aspose.PSD สำหรับ Java คืออะไร?**  
A: Interrupt Monitor ช่วยให้นักพัฒนาสามารถหยุดหรือยกเลิกการแปลงภาพที่ใช้เวลานาน, ให้การควบคุมแบบเรียลไทม์ต่อการใช้ทรัพยากร.

**Q2: จะรับไลบรารี Aspose.PSD สำหรับ Java ได้อย่างไร?**  
A: คุณสามารถดาวน์โหลดไลบรารี Aspose.PSD สำหรับ Java ได้จาก [ที่นี่](https://releases.aspose.com/psd/java/).

**Q3: มีการทดลองใช้ฟรีสำหรับ Aspose.PSD สำหรับ Java หรือไม่?**  
A: มี, คุณสามารถสำรวจการทดลองใช้ฟรีของ Aspose.PSD ได้จาก [ที่นี่](https://releases.aspose.com/).

**Q4: จะหาแหล่งสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน?**  
A: เยี่ยมชมฟอรั่มสนับสนุน Aspose.PSD สำหรับ Java ได้จาก [ที่นี่](https://forum.aspose.com/c/psd/34).

**Q5: จะซื้อใบอนุญาตสำหรับ Aspose.PSD สำหรับ Java อย่างไร?**  
A: คุณสามารถซื้อใบอนุญาตสำหรับ Aspose.PSD สำหรับ Java ได้จาก [ที่นี่](https://purchase.aspose.com/buy).

**Q6: สามารถแปลงไฟล์ PSD หลายไฟล์เป็น PNG พร้อมกันได้หรือไม่?**  
A: ได้, สร้างเธรดแยกสำหรับแต่ละไฟล์และแนบ `InterruptMonitor` แยกต่างหากให้กับ worker ของการแปลงแต่ละรายการ.

**Q7: ไลบรารีนี้จัดการโปรไฟล์สีระหว่างการแปลง PSD‑to‑PNG หรือไม่?**  
A: แน่นอน; Aspose.PSD จะรักษา ICC profile ที่ฝังอยู่และนำไปใช้กับ PNG เอาต์พุตโดยอัตโนมัติ.

**Last Updated:** 2026-06-08  
**Tested With:** Aspose.PSD 23.12 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [บันทึก PSD เป็น PNG และใช้ Rendering Drop Shadow ใน Aspose.PSD สำหรับ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [ส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ปกติใหม่โดยใช้ Aspose.PSD สำหรับ Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [การสนับสนุน Interrupt Monitor ในไฟล์ PSD - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}