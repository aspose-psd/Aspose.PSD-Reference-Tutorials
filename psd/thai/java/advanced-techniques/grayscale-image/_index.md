---
date: 2026-05-24
description: เรียนรู้วิธีทำให้ภาพเป็นสีเทาโดยใช้ Aspose.PSD for Java ซึ่งเป็นโซลูชันแปลงสีเป็นสีเทาอย่างรวดเร็วที่รองรับรูปแบบกว่า
  30 แบบและไฟล์ขนาดใหญ่
keywords:
- how to grayscale image
- convert color to grayscale
- java image processing tutorial
- convert psd to grayscale
- grayscale image java
linktitle: ทำให้ภาพเป็นสีเทา
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to grayscale image using Aspose.PSD for Java, a fast convert
    color to grayscale solution that works with 30+ formats and large files.
  headline: How to Grayscale Image using Aspose.PSD for Java
  type: TechArticle
- description: Learn how to grayscale image using Aspose.PSD for Java, a fast convert
    color to grayscale solution that works with 30+ formats and large files.
  name: How to Grayscale Image using Aspose.PSD for Java
  steps:
  - name: Set Up Your Document Directory
    text: 'Define where the original PSD resides and where the grayscale JPEG will
      be written:'
  - name: Load the Source Image
    text: '`PsdImage` is the Aspose.PSD class that represents a Photoshop document
      and provides methods to access its raster data.'
  - name: Check and Cache Image
    text: '`RasterCachedImage` is a subclass that allows caching of raster data to
      improve performance.'
  - name: Transform to Grayscale
    text: '`toGrayscale()` converts the image’s color channels to a single luminance
      channel using the ITU‑R BT.709 formula.'
  - name: Save the Resultant Image
    text: '`JpegOptions` lets you specify JPEG encoding parameters such as quality
      before saving. Repeat the above steps for any additional PSD files you need
      to process.'
  type: HowTo
- questions:
  - answer: Yes, a purchased license permits commercial deployment; a free trial is
      available for evaluation.
    question: Can I use Aspose.PSD for Java for commercial projects?
  - answer: Yes, you can explore all features with a time‑limited trial. Download
      it [here](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.PSD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/psd/java/).
    question: Where can I find documentation for Aspose.PSD for Java?
  - answer: Temporary licenses are provided [here](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for testing?
  - answer: Visit the Aspose.PSD forum [here](https://forum.aspose.com/c/psd/34).
    question: Need support or have questions?
  type: FAQPage
second_title: Aspose.PSD Java API
title: วิธีทำให้ภาพเป็นสีเทาโดยใช้ Aspose.PSD for Java
url: /th/java/advanced-techniques/grayscale-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีทำให้ภาพเป็นสีเทาโดยใช้ Aspose.PSD for Java

## บทนำ

หากคุณกำลังมองหา **how to grayscale image** อย่างรวดเร็วในแอปพลิเคชัน Java คุณมาถูกที่แล้ว การแปลงภาพสีให้เป็นสีเทาเป็นหนึ่งในงานประมวลผลภาพที่พบบ่อยที่สุด และ Aspose.PSD for Java ทำให้เรื่องนี้ง่ายดาย ในบทแนะนำนี้เราจะพาคุณผ่านทุกขั้นตอนจากการตั้งค่าโปรเจกต์จนถึงการบันทึกไฟล์ JPEG สุดท้าย เพื่อให้คุณสามารถรวมการแปลงเป็นสีเทาเข้าไปในโซลูชัน Java ใดก็ได้อย่างมั่นใจ

## คำตอบอย่างรวดเร็ว
- **สีเทาหมายถึงอะไร?** It removes color information, leaving only shades of gray that represent luminance.
- **ไลบรารีใดที่จัดการการแปลง?** Aspose.PSD for Java ให้ API เฉพาะสำหรับไฟล์ PSD และภาพแรสเตอร์.
- **ฉันต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** Yes, a commercial license is required for non‑trial use.
- **ฉันสามารถประมวลผลไฟล์ขนาดใหญ่ได้หรือไม่?** ไลบรารีสามารถจัดการไฟล์ได้ถึง 2 GB โดยไม่ต้องโหลดภาพทั้งหมดเข้าสู่หน่วยความจำ.
- **โค้ดใช้เวลานานเท่าไหร่ในการเขียน?** Roughly 10 minutes to copy the snippets and run them.

## Aspose.PSD for Java คืออะไร?

Aspose.PSD for Java เป็น API ที่ไม่ขึ้นกับ .NET ซึ่งช่วยให้สร้าง, แก้ไข, และแปลงไฟล์ Adobe Photoshop® PSD ใน Java แท้ รองรับรูปแบบภาพกว่า 30 รูปแบบและให้การประมวลผลความเร็วสูงสำหรับไฟล์ที่มีขนาดหลายร้อยเมกะไบต์ ทำให้เหมาะสำหรับยูทิลิตี้ขนาดเล็กและงานแบตช์ขนาดใหญ่

## ทำไมต้องใช้ Aspose.PSD for Java เพื่อแปลงสีเป็นสีเทา?

Aspose.PSD มีการสนับสนุนรูปแบบที่หลากหลาย, การสตรีมที่ใช้หน่วยความจำน้อย, และการแปลงสีเป็นสีเทาที่แม่นยำโดยคำนึงถึงเอฟเฟกต์และมาสก์ของเลเยอร์ วิธี `toGrayscale()` ที่มาพร้อมกับไลบรารีใช้สูตรความสว่าง ITU‑R BT.709 เพื่อให้ผลลัพธ์ที่สอดคล้องกันบนอุปกรณ์ต่างๆ นอกจากนี้ไลบรารีทำงานบน Windows, Linux, และ macOS พร้อมกับ runtime JDK 8+ ใดก็ได้ ทำให้คุณมีความยืดหยุ่นในการปรับใช้

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK)** 8 หรือใหม่กว่า ติดตั้งแล้ว.
2. ไลบรารี **Aspose.PSD for Java** ดาวน์โหลดจาก [here](https://releases.aspose.com/psd/java/).
3. **Aspose.PSD license** ที่ถูกต้อง หากคุณวางแผนจะรันโค้ดหลังช่วงทดลอง คุณสามารถซื้อไลเซนส์ได้ที่ [here](https://purchase.aspose.com/buy).

## วิธีทำให้ภาพเป็นสีเทาโดยใช้ Aspose.PSD for Java?

โหลดไฟล์ PSD ต้นฉบับ, เปิดใช้งานการแคชเพื่อความเร็ว, แปลงภาพแรสเตอร์เป็นสีเทา, และสุดท้ายบันทึกเป็น JPEG—ทั้งหมดในห้าขั้นตอนสั้นๆ ส่วนต่อไปนี้จะแบ่งแต่ละขั้นตอนพร้อมคำอธิบายที่ชัดเจนและโค้ดตัวอย่างที่คุณต้องคัดลอก

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

Define where the original PSD resides and where the grayscale JPEG will be written:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
import java.io.FileNotFoundException;
```

### ขั้นตอนที่ 2: โหลดภาพต้นฉบับ

`PsdImage` is the Aspose.PSD class that represents a Photoshop document and provides methods to access its raster data.

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 3: ตรวจสอบและแคชภาพ

`RasterCachedImage` is a subclass that allows caching of raster data to improve performance.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "Grayscaling_out.jpg";

Image image = Image.load(sourceFile);
```

### ขั้นตอนที่ 4: แปลงเป็นสีเทา

`toGrayscale()` converts the image’s color channels to a single luminance channel using the ITU‑R BT.709 formula.

```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;
if (!rasterCachedImage.isCached())
{
    rasterCachedImage.cacheData();
}
```

### ขั้นตอนที่ 5: บันทึกภาพที่ได้

`JpegOptions` lets you specify JPEG encoding parameters such as quality before saving.

```java
rasterCachedImage.grayscale();
```

ทำซ้ำขั้นตอนข้างต้นสำหรับไฟล์ PSD เพิ่มเติมที่คุณต้องการประมวลผล

## ปัญหาที่พบบ่อยและวิธีแก้

- **OutOfMemoryError บน PSD ขนาดใหญ่มาก** – ตรวจสอบให้แน่ใจว่าเปิดการแคช (ขั้นตอน 3) และรัน JVM ด้วย heap ที่เพิ่มขึ้น (`-Xmx2g` หรือสูงกว่า).
- **สีเปลี่ยนหลังการแปลง** – ตรวจสอบว่าคุณใช้เมธอด `toGrayscale()` แทนการปรับช่องสีด้วยตนเอง; เมธอดในตัวใช้สูตรความสว่าง ITU‑R BT.709 เพื่อผลลัพธ์ที่แม่นยำ.
- **รูปแบบภาพที่ไม่รองรับ** – Aspose.PSD รองรับมากกว่า 30 รูปแบบ; หากพบส่วนขยายที่ไม่รู้จัก ให้เปลี่ยนชื่อเป็นรูปแบบที่รองรับ (เช่น `.psd` หรือ `.png`) ก่อนโหลด.

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.PSD for Java สำหรับโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ใช่, ไลเซนส์ที่ซื้อไว้อนุญาตให้ใช้งานเชิงพาณิชย์; มีรุ่นทดลองฟรีสำหรับการประเมิน.

**Q: มีเวอร์ชันทดลองฟรีของ Aspose.PSD for Java หรือไม่?**  
A: มี, คุณสามารถสำรวจคุณสมบัติทั้งหมดด้วยการทดลองแบบจำกัดเวลา ดาวน์โหลดได้ที่ [here](https://releases.aspose.com/).

**Q: ฉันจะหาเอกสารสำหรับ Aspose.PSD for Java ได้จากที่ไหน?**  
A: ดูเอกสารอย่างเป็นทางการที่ [here](https://reference.aspose.com/psd/java/).

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับการทดสอบได้อย่างไร?**  
A: ไลเซนส์ชั่วคราวมีให้ที่ [here](https://purchase.aspose.com/temporary-license/).

**Q: ต้องการสนับสนุนหรือมีคำถาม?**  
A: เยี่ยมชมฟอรั่ม Aspose.PSD ที่ [here](https://forum.aspose.com/c/psd/34).

## สรุป

ตอนนี้คุณมีเวิร์กโฟลว์ที่ครบถ้วนและพร้อมใช้งานในระดับผลิตสำหรับ **how to grayscale image** โดยใช้ Aspose.PSD for Java ด้วยการทำตามรูปแบบห้าขั้นตอน—ตั้งค่าไดเรกทอรี, โหลด PSD, เปิดการแคช, แปลงเป็นสีเทา, และบันทึก—คุณสามารถฝังความสามารถนี้เข้าไปในโปรเซสเซอร์แบบแบตช์, บริการเว็บ, หรือยูทิลิตี้เดสก์ท็อป ทดลองใช้รูปแบบเอาต์พุตและการตั้งค่าคุณภาพต่างๆ เพื่อปรับผลลัพธ์ให้เหมาะกับกรณีการใช้งานของคุณ

---

**อัปเดตล่าสุด:** 2026-05-24  
**ทดสอบด้วย:** Aspose.PSD for Java 23.12 (latest at time of writing)  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [แปลง PSD เป็นรูปแบบภาพแรสเตอร์ด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [วิธีปรับค่า Gamma ในการประมวลผลภาพ Java ด้วย Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [ไลบรารีการประมวลผลภาพ Java: กลับด้านเลเยอร์โดยใช้ Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
rasterCachedImage.save(destName, new JpegOptions());
```