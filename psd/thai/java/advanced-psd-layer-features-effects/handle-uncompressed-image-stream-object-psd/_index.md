---
date: 2026-08-01
description: เรียนรู้วิธีส่งออก PSD เป็น PNG และจัดการสตรีมภาพที่ไม่ได้บีบอัดด้วย
  Aspose.PSD for Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: จัดการวัตถุสตรีมภาพที่ไม่ได้บีบอัดใน PSD - Java
og_description: ส่งออก psd เป็น png ด้วย Aspose.PSD for Java. เรียนรู้การจัดการสตรีมภาพที่ไม่ได้บีบอัด,
  สร้างวัตถุกราฟิก, และบันทึก PNG คุณภาพสูง.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: ส่งออก psd เป็น png – คู่มือ Java สำหรับสตรีม PSD ที่ไม่ได้บีบอัด
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: ส่งออก PSD เป็น PNG – สร้างวัตถุกราฟิก PSD – สตรีมที่ไม่ได้บีบอัดใน Java
url: /th/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก PSD เป็น PNG – สร้างอ็อบเจ็กต์กราฟิก PSD – สตรีมที่ไม่ได้บีบอัดใน Java

## บทนำ
ในคู่มือแบบขั้นตอนนี้คุณจะ **ส่งออก PSD เป็น PNG** ขณะทำงานกับสตรีมภาพที่ไม่ได้บีบอัดโดยใช้ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะทำอัตโนมัติขั้นตอนการออกแบบหรือสร้างโปรแกรมแก้ไขแบบกำหนดเอง ความสามารถในการเรนเดอร์ไฟล์ Photoshop โดยไม่สูญเสียคุณภาพเป็นสิ่งสำคัญ เราจะเริ่มด้วยการตั้งค่าที่จำเป็น, เดินผ่านการสร้างอ็อบเจ็กต์ `Graphics`, และสรุปด้วยการส่งออก PNG แบบไม่สูญเสียข้อมูล เมื่อเสร็จสิ้นคุณจะเข้าใจว่าทำไม Aspose.PSD จึงจัดการสตรีมดิบได้อย่างมีประสิทธิภาพและวิธีการผสานรวมเข้ากับโครงการ Java ใด ๆ

## คำตอบอย่างรวดเร็ว
- **What does “create PSD graphics object” mean?** It means instantiating a `Graphics` context that lets you draw on or modify a PSD image programmatically.  
- **Which library handles uncompressed streams?** Aspose.PSD for Java provides full support for raw (uncompressed) image data.  
- **Can I export PSD to PNG after editing?** Yes—once you have a `Graphics` object you can render the PSD and save it as PNG in a single call.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production deployments.  
- **Is the export lossless?** Exporting to PNG preserves the original pixel data, offering lossless quality with a smaller file size than the raw PSD.

## การส่งออก PSD เป็น PNG คืออะไร?
การส่งออก PSD เป็น PNG แปลงเอกสาร Photoshop แบบหลายเลเยอร์ให้เป็นภาพเรสเตอร์แบบชั้นเดียวที่ไม่มีการสูญเสียข้อมูล ซึ่งสามารถแสดงผลได้ในเว็บเบราว์เซอร์หรือโปรแกรมดูภาพใด ๆ กระบวนการนี้รักษาความโปร่งใส, ความลึกสี, และเอฟเฟกต์ของเลเยอร์ไว้ขณะละทิ้งเมตาดาต้าเฉพาะของ Photoshop นอกจากนี้ยังคงโปรไฟล์สีเดิมเพื่อการทำสำเนาสีที่แม่นยำ

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java ในการจัดการภาพ?
Aspose.PSD รองรับ **50+** รูปแบบไฟล์เข้าและออก รวมถึง PSD, PNG, JPEG, BMP, และ TIFF และสามารถประมวลผลไฟล์ที่มี **200+** เลเยอร์โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ตัวเลือกการบีบอัด `Raw` จะเก็บข้อมูลพิกเซลโดยไม่บีบอัด ทำให้ได้ความแม่นยำระดับพิกเซลสำหรับการแก้ไขต่อไปหรือการเก็บรักษา

## ข้อกำหนดเบื้องต้น
ก่อนเราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Java Development Kit (JDK)** – JDK 8 หรือใหม่กว่า  
- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจากหน้าปล่อยอย่างเป็นทางการ: [ดาวน์โหลด Aspose.PSD Java](https://releases.aspose.com/psd/java/). คุณสามารถเข้าถึงได้ผ่าน [ลิงก์นี้](https://releases.aspose.com/psd/java/) หรือ [หน้าปล่อย](https://releases.aspose.com/psd/java/). สำหรับผลิตภัณฑ์ Aspose อื่น ๆ ให้คลิก [ที่นี่](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse หรือโปรแกรมแก้ไขที่รองรับ Java ใด ๆ  
- **Basic Java knowledge** – ความคุ้นเคยกับคลาส, เมธอด, และการจัดการข้อยกเว้น  

เมื่อมีทั้งหมดนี้ คุณพร้อมที่จะเริ่มเขียนโค้ดแล้ว

## นำเข้าแพ็กเกจ
คลาส `Graphics` เป็นพื้นผิวการวาดของ Aspose.PSD ที่ให้คุณเรนเดอร์หรือแก้ไขข้อมูลพิกเซลโดยตรง คลาส `PsdImage` แทนไฟล์ PSD ในหน่วยความจำ ส่วน `PsdOptions` ควบคุมวิธีการบันทึกภาพ

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

ตอนนี้เราจะทำการแยกโค้ดเป็นขั้นตอนย่อยเพื่อให้คุณตามได้ง่าย เราจะตั้งค่าสภาพแวดล้อม, โหลดไฟล์ PSD, ปรับแต่ง, และสุดท้ายบันทึกผลลัพธ์

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสารของคุณ
ก่อนทำการใด ๆ กับไฟล์ คุณต้องบอกโปรแกรมว่าควรมองหาแอสเซ็ต PSD ที่ไหน เส้นทางไดเรกทอรีนี้จะถูกใช้ตลอดบทเรียน

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยเส้นทางเต็มที่มีไฟล์ `layers.psd` การทำให้เส้นทางเป็นค่าที่กำหนดได้ทำให้โค้ดสามารถใช้ซ้ำได้ในหลายโครงการ

## ขั้นตอนที่ 2: สร้าง Byte Array Output Stream
`ByteArrayOutputStream` เป็นสตรีมของ Java ที่เก็บข้อมูลในหน่วยความจำเป็นอาเรย์ไบต์ ทำหน้าที่เป็นบัฟเฟอร์ในหน่วยความจำสำหรับภาพที่แก้ไขแล้ว ช่วยให้คุณจับไบต์ดิบก่อนเขียนลงดิสก์หรือส่งผ่านเครือข่าย

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

ตัวแปร `ms` จะเก็บข้อมูลภาพที่ไม่ได้บีบอัดหลังจากดำเนินการ `save`

## ขั้นตอนที่ 3: โหลดไฟล์ PSD
คลาส `PsdImage` โหลดไฟล์ PSD เข้าไปในหน่วยความจำเพื่อทำการปรับแต่ง การโหลดไฟล์จะแปลง PSD บนดิสก์เป็นอ็อบเจ็กต์ `PsdImage` ที่คุณสามารถจัดการได้ ขั้นตอนนี้คือจุดที่ Aspose.PSD อ่านส่วนหัวไฟล์, เลเยอร์, และทรัพยากรต่าง ๆ

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

หากเส้นทางไม่ถูกต้อง Aspose.PSD จะโยน `FileNotFoundException` ซึ่งคุณควรจับไว้ในโค้ดสำหรับการใช้งานจริง

## ขั้นตอนที่ 4: ตั้งค่า PsdOptions สำหรับการบันทึก
`PsdOptions` ระบุพารามิเตอร์การบันทึกสำหรับไฟล์ PSD การตั้งค่าวิธีบีบอัดเป็น `Raw` หมายความว่าข้อมูลพิกเซลจะถูกเก็บโดยไม่มีการบีบอัด ทำให้คงพิกเซลทุกตัวอย่างที่ปรากฏในหน่วยความจำได้อย่างแม่นยำ

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

ตัวเลือก `CompressionMethod.Raw` จะเก็บข้อมูลพิกเซลโดยไม่มีการบีบอัด ซึ่งเหมาะอย่างยิ่งเมื่อคุณวางแผนจะทำการแก้ไขต่อไปในภายหลัง

## ขั้นตอนที่ 5: บันทึกภาพลงใน Output Stream
ตอนนี้คุณจะบันทึก PSD (พร้อมการแก้ไขใด ๆ) ลงใน `ByteArrayOutputStream` ที่สร้างไว้ก่อนหน้านี้ เมธอด `save` จะเคารพ `PsdOptions` ที่คุณกำหนดไว้

```java
psdImage.save(ms, saveOptions);
```

ในขณะนี้ `ms` มีการแสดงผลไบนารีเต็มของ PSD ที่ไม่ได้บีบอัด

## ขั้นตอนที่ 6: รีเซ็ต Output Stream
หลังจากเขียนเสร็จ ตัวชี้ภายในสตรีมจะอยู่ที่ตำแหน่งสุดท้าย การรีเซ็ตจะทำให้สตรีมกลับไปที่จุดเริ่มต้นเพื่อให้คุณอ่านจากต้นไฟล์ได้

```java
ms.reset();
```

คิดว่าเป็นการย้ายหัวเทปกลับไปที่จุดเริ่มต้นก่อนการเล่น

## ขั้นตอนที่ 7: โหลดภาพที่สร้างใหม่
ตอนนี้คุณสามารถสร้างอินสแตนซ์ `PsdImage` ใหม่โดยตรงจากอาเรย์ไบต์ ขั้นตอนนี้ตรวจสอบว่าข้อมูลที่บันทึกสามารถโหลดใหม่ได้โดยไม่มีความเสียหาย

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

หากภาพโหลดสำเร็จ คุณจะรู้ว่าสตรีมที่ไม่ได้บีบอัดถูกเขียนอย่างถูกต้อง

## ขั้นตอนที่ 8: สร้างอ็อบเจ็กต์ Graphics
คลาส `Graphics` เป็นแคนวาสการวาดของ Aspose.PSD ให้เมธอดสำหรับวาดรูปทรง, ข้อความ, และใช้ฟิลเตอร์โดยตรงบนเมทริกซ์พิกเซลของ `PsdImage`

```java
Graphics graphics = new Graphics(psdImage);
```

ด้วยอินสแตนซ์ `Graphics` นี้คุณสามารถวาดเนื้อหาใหม่, ลบส่วน, หรือรวมเลเยอร์เพิ่มเติมได้

## ฉันจะส่งออก PSD เป็น PNG ด้วย Aspose.PSD สำหรับ Java อย่างไร?
โหลด PSD ด้วย `new PsdImage(dataDir + "layers.psd")`, สร้างอ็อบเจ็กต์ `Graphics`, ทำการวาดตามต้องการ, แล้วเรียก `psdImage.save("output.png", new PngOptions())` ลำดับนี้จะเรนเดอร์ PSD ที่แก้ไขแล้วและเขียน PNG แบบไม่สูญเสียข้อมูลในขั้นตอนเดียว โดยใช้เอนจินการแปลงในตัวของ Aspose.PSD

## จัดการเลเยอร์ PSD ด้วยอ็อบเจ็กต์ Graphics
การมีอินสแตนซ์ `Graphics` ให้คุณควบคุมระดับพิกเซลของแต่ละเลเยอร์ คุณสามารถวาดรูปทรงเรขาคณิต, เรนเดอร์ข้อความ, หรือใช้ฟิลเตอร์แบบกำหนดเอง เนื่องจากคอนเท็กซ์กราฟิกทำงานบนมุมมองเรสเตอร์ของเลเยอร์ การเปลี่ยนแปลงจะแสดงผลทันทีเมื่อบันทึกภาพ

## ปัญหาที่พบบ่อยและวิธีแก้ไข
- **NullPointerException when loading the file** – ตรวจสอบเส้นทาง `dataDir` อีกครั้งและให้แน่ใจว่าชื่อไฟล์ตรงกันอย่างแม่นยำ รวมถึงความแตกต่างของตัวอักษรใหญ่‑เล็ก  
- **Compressed output despite using Raw** – ตรวจสอบว่าได้เรียก `saveOptions.setCompressionMethod(CompressionMethod.Raw);` **ก่อน** เรียก `save`  
- **Graphics object appears blank** – ตรวจสอบว่าคุณกำลังวาดบนอินสแตนซ์ `PsdImage` ที่ถูกต้อง (อันที่โหลดมา ไม่ใช่อ็อบเจ็กต์ว่างใหม่)  
- **OutOfMemoryError on large files** – ใช้ `PsdImage.load(dataDir, LoadOptions)` พร้อม `loadOptions.setLoadMode(LoadMode.Memory)` เพื่อสตรีมไฟล์ขนาดใหญ่โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่ RAM

## คำถามที่พบบ่อย
### Aspose.PSD คืออะไร
Aspose.PSD เป็นไลบรารี Java ที่ช่วยให้นักพัฒนาสร้าง, แก้ไข, และแปลงไฟล์ Photoshop PSD ได้โดยไม่ต้องใช้ Adobe Photoshop รองรับการอ่านและเขียนไฟล์ PSD, จัดการเลเยอร์, มาสก์, ช่องสี, และทรัพยากรภาพต่าง ๆ พร้อม API สำหรับการทำงานแบบเรสเตอร์และเวกเตอร์ เหมาะสำหรับการประมวลผลภาพฝั่งเซิร์ฟเวอร์และงานอัตโนมัติ

### ฉันจะดาวน์โหลด Aspose.PSD สำหรับ Java ได้อย่างไร
คุณสามารถดาวน์โหลดได้จากหน้าปล่อยอย่างเป็นทางการ: [ดาวน์โหลด Aspose.PSD Java](https://releases.aspose.com/psd/java/)

### มีรุ่นทดลองฟรีสำหรับ Aspose.PSD หรือไม่
มี รุ่นทดลองเต็มรูปแบบที่พร้อมใช้งานบนหน้าดาวน์โหลดเดียวกัน ใช้สำหรับการพัฒนาและการประเมินผล

### ฉันสามารถรับการสนับสนุนสำหรับ Aspose.PSD ได้หรือไม่
แน่นอน! ฟอรั่มสนับสนุนของ Aspose มีคำตอบจากทีมผลิตภัณฑ์และชุมชน: [Aspose support forum](https://forum.aspose.com/c/psd/34)

### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร
คุณสามารถขอใบอนุญาตชั่วคราวได้โดยตรงจากพอร์ทัลการออกใบอนุญาตของ Aspose ซึ่งจะให้คีย์ที่มีอายุจำกัด 30 วัน เพื่อประเมินฟังก์ชันทั้งหมดของ Aspose.PSD หลังระยะทดลองคุณต้องเปลี่ยนคีย์ชั่วคราวเป็นใบอนุญาตถาวรเพื่อใช้งานต่อในสภาพแวดล้อมการผลิต เยี่ยมชมพอร์ทัลใบอนุญาตชั่วคราวเพื่อสร้างคีย์ที่มีระยะเวลาจำกัด: [temporary license page](https://purchase.aspose.com/temporary-license/)

## คำถามที่พบบ่อย

**Q: Can I use the graphics object to edit only one specific layer?**  
A: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)` and pass that layer to the `Graphics` constructor.

**Q: Does the Raw compression method affect file size?**  
A: Raw stores pixel data without any compression, so the resulting file is larger than a compressed PSD, but it guarantees 100 % pixel fidelity.

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this is the standard way to **export PSD to PNG** with lossless quality.

**Q: What Java version is required?**  
A: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases up to JDK 21.

**Q: How do I release resources after processing?**  
A: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`) to free native memory and avoid leaks.

**อัปเดตล่าสุด:** 2026-08-01  
**ทดสอบกับ:** Aspose.PSD for Java (latest release)  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [Save Images to Stream with Aspose.PSD for Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Export PSD Layer Group to Image using Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Create Image using Stream in Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}