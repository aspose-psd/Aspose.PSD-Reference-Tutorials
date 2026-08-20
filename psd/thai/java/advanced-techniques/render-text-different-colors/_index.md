---
date: 2026-05-29
description: เรียนรู้วิธีบันทึก PSD เป็น PNG พร้อมข้อความสีโดยใช้ Aspose.PSD for Java
  คู่มือขั้นตอนต่อขั้นตอนนี้แสดงวิธีแปลง PSD เป็น PNG อย่างมีประสิทธิภาพ
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: เรนเดอร์ข้อความด้วยสีต่าง ๆ ในเลเยอร์ข้อความ
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: บันทึก PSD เป็น PNG พร้อมข้อความสีโดยใช้ Aspose.PSD for Java
url: /th/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก PSD เป็น PNG พร้อมข้อความสีโดยใช้ Aspose.PSD สำหรับ Java

ยินดีต้อนรับสู่คู่มือขั้นตอนโดยละเอียดของเราว่าจะ **save PSD as PNG** พร้อมข้อความสีต่าง ๆ โดยใช้ Aspose.PSD สำหรับ Java. Aspose.PSD เป็นไลบรารี Java ที่ทรงพลังซึ่งช่วยให้คุณสามารถจัดการไฟล์ Photoshop ผ่านโปรแกรมได้, มอบความสามารถที่กว้างขวางในการทำงานกับรูปแบบไฟล์ PSD และ PSB.

ในบทแนะนำนี้, เราจะพาคุณผ่านกระบวนการเรนเดอร์ข้อความด้วยสีต่าง ๆ ในเลเยอร์ข้อความโดยใช้ Aspose.PSD. เมื่อจบคู่มือคุณจะเข้าใจอย่างชัดเจนว่าจะแก้ไขงานนี้ได้อย่างราบรื่น.

## คำตอบด่วน
- **How to save PSD as PNG?** ใช้คลาส `PsdImage` ของ Aspose.PSD เพื่อโหลดไฟล์ PSD และเรียก `save` พร้อม `PngOptions`.
- **Can I render multiple colors in one text layer?** ใช่, กำหนดอ็อบเจ็กต์ `Color` ที่แตกต่างกันให้กับแต่ละ `Portion` ของข้อความ.
- **What Java version is required?** รองรับ Java 8 หรือสูงกว่า.
- **Do I need a license for production?** จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้.
- **Is the library memory‑efficient for large files?** สามารถจัดการไฟล์ขนาดสูงสุด 2 GB ได้โดยไม่ต้องโหลดเต็มในหน่วยความจำ.

## วิธีบันทึก PSD เป็น PNG พร้อมข้อความสี?
โหลดไฟล์ PSD ของคุณ, ปรับส่วนของเลเยอร์ข้อความเพื่อกำหนดสีที่แตกต่างกัน, แล้วบันทึกภาพเป็น PNG—กระบวนการทั้งหมดนี้ทำได้ด้วยไม่กี่บรรทัดของโค้ด Java. Aspose.PSD จะทำการแรสเตอร์เลเยอร์ที่แก้ไขโดยอัตโนมัติ, รักษาความโปร่งใสและความแม่นยำของสี, ทำให้ PNG ที่ได้ตรงกับการออกแบบต้นฉบับ.

## Aspose.PSD for Java คืออะไร?
Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้สามารถสร้าง, แก้ไข, และแปลงไฟล์ Photoshop (PSD/PSB) ผ่านโปรแกรมได้. รองรับ **50+ image formats** และสามารถประมวลผลเอกสารหลายร้อยหน้าโดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ, ให้ประสิทธิภาพสูงสำหรับการทำงานอัตโนมัติบนเซิร์ฟเวอร์.

## ข้อกำหนดเบื้องต้น
- ความรู้พื้นฐานของการเขียนโปรแกรม Java.
- ไลบรารี Aspose.PSD for Java ติดตั้งแล้ว. คุณสามารถดาวน์โหลดได้จาก [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## นำเข้าแพ็กเกจ
`Image` เป็นคลาสฐานสำหรับการโหลดและบันทึกไฟล์รูปภาพ. `PsdImage` แทนเอกสาร Photoshop, ส่วน `TextLayer` ให้การเข้าถึงคุณสมบัติของเลเยอร์ข้อความ. `PngOptions` กำหนดการตั้งค่าสำหรับการส่งออก PNG.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ
สร้างโครงการ Java ใหม่และเพิ่มไลบรารี Aspose.PSD เข้าไป. ตรวจสอบให้แน่ใจว่าคุณมีสิทธิ์ที่จำเป็นในการเข้าถึงและแก้ไขไฟล์ในไดเรกทอรีของโครงการ.

## ขั้นตอนที่ 2: กำหนดไดเรกทอรีต้นทางและไดเรกทอรีผลลัพธ์
ระบุไดเรกทอรีต้นทางและไดเรกทอรีผลลัพธ์ที่ไฟล์ PSD ของคุณอยู่และที่ภาพที่ได้จะถูกบันทึก. ปรับค่าแปร `sourceDir` และ `outputDir` ให้สอดคล้อง.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## ขั้นตอนที่ 3: โหลดไฟล์ PSD และเข้าถึงเลเยอร์ข้อความ
`PsdImage` โหลดไฟล์ PSD เข้าสู่หน่วยความจำ, และ `TextLayer` อนุญาตให้จัดการเนื้อหาข้อความภายในเลเยอร์นั้น.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## ขั้นตอนที่ 4: ตั้งค่า PNG Options และบันทึกภาพที่ได้
`PngOptions` กำหนดค่าพารามิเตอร์การส่งออก PNG เช่น ประเภทสีและการบีบอัด.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## ปัญหาทั่วไปและวิธีแก้ไข
- **Missing license exception:** ตรวจสอบว่าคุณได้ใช้ไฟล์ลิขสิทธิ์ที่ถูกต้องก่อนเรียกดำเนินการบันทึกใด ๆ.  
- **Color not applied:** ยืนยันว่าแต่ละ `Portion` ในเลเยอร์ข้อความมีคุณสมบัติ `Color` ตั้งค่าอย่างถูกต้อง.  
- **Large file memory usage:** ใช้ overload `load` ของ `PsdImage` พร้อม `loadOptions` เพื่อสตรีมไฟล์ขนาดใหญ่.

## คำถามที่พบบ่อย
**Q: Can I use Aspose.PSD for Java with other programming languages?**  
A: Aspose.PSD ถูกออกแบบมาสำหรับ Java เป็นหลัก, แต่ Aspose มีไลบรารีที่คล้ายกันสำหรับหลายภาษาโปรแกรมอื่น ๆ.

**Q: Is there a trial version available for Aspose.PSD for Java?**  
A: มี, คุณสามารถรับรุ่นทดลองฟรีจาก [Aspose.PSD](https://releases.aspose.com/).

**Q: Where can I find additional support or assistance?**  
A: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

**Q: How can I obtain a temporary license for Aspose.PSD for Java?**  
A: คุณสามารถขอรับลิขสิทธิ์ชั่วคราวจาก [Aspose.PSD](https://purchase.aspose.com/temporary-license/).

**Q: Are there other tutorials available for Aspose.PSD?**  
A: มี, สำรวจ [Aspose.PSD documentation](https://reference.aspose.com/psd/java/) เพื่อดูบทเรียนและตัวอย่างเพิ่มเติม.

**Q: Does the library support batch conversion of multiple PSD files to PNG?**  
A: มี, คุณสามารถวนลูปผ่านโฟลเดอร์ของไฟล์ PSD, ใช้ตรรกะสีข้อความเดียวกัน, และบันทึกแต่ละไฟล์เป็น PNG ด้วยลูป.

**Q: Is the output PNG lossless?**  
A: PNG ที่บันทึกโดย Aspose.PSD รักษาคุณภาพ lossless เต็มรูปแบบ, คงข้อมูลสีและความโปร่งใสทั้งหมด.

---

**อัปเดตล่าสุด:** 2026-05-29  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง
- [ส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ปกติใหม่โดยใช้ Aspose.PSD สำหรับ Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [บันทึก PSD เป็น PNG และใช้เงาตกของการเรนเดอร์ใน Aspose.PSD สำหรับ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [แปลง PSD เป็น PNG พร้อมการทับสี – Aspose.PSD สำหรับ Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}