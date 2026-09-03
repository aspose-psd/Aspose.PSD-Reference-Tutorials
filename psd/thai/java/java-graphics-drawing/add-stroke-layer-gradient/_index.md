---
date: 2026-09-03
description: เรียนรู้วิธีสร้าง gradient stroke java และปรับแต่ง gradient ของ stroke
  ในไฟล์ PSD ด้วย Aspose.PSD for Java คู่มือขั้นตอนต่อขั้นสำหรับนักพัฒนา
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: วิธีสร้าง Gradient Stroke Layer ใน Java
og_description: สร้าง gradient stroke java ด้วย Aspose.PSD for Java ภายในไม่กี่นาที
  คู่มือการสอนนี้จะแสดงวิธีเพิ่มและปรับแต่ง gradient strokes ในไฟล์ PSD พร้อมตัวอย่างโค้ดและแนวปฏิบัติที่ดีที่สุด
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: สร้าง gradient stroke java – คู่มือการสอน Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: สร้าง gradient stroke java – คู่มือการสอน Aspose.PSD
url: /th/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้าง gradient stroke java ด้วย Aspose.PSD

## บทนำ
หากคุณต้องการสร้างเอฟเฟกต์ **create gradient stroke java** โดยไม่ต้องเปิด Photoshop คุณมาถูกที่แล้ว ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีใช้ Aspose.PSD for Java — ไลบรารี pure‑Java ที่ให้คุณควบคุมไฟล์ PSD ได้อย่างเต็มรูปแบบผ่านโปรแกรม เราจะอธิบายขั้นตอนการโหลด PSD, เข้าถึงเอฟเฟกต์ stroke ของเลเยอร์, กำหนดค่า gradient fill, และสุดท้ายบันทึกผลลัพธ์ เมื่อเสร็จคุณจะสามารถเพิ่มเส้นขอบ gradient ระดับมืออาชีพให้กับรูปทรงหรือข้อความได้ด้วยเพียงไม่กี่บรรทัดของโค้ด.

## คำตอบอย่างรวดเร็ว
- **What is the primary goal?** สร้างเลเยอร์ gradient stroke บนไฟล์ PSD ด้วย Java.  
- **Which library provides the API?** Aspose.PSD for Java (รองรับ Java 8 +).  
- **Do I need a license for production?** ใช่ – จำเป็นต้องมีใบอนุญาตที่ถูกต้องหรือใบอนุญาตชั่วคราว.  
- **How long does a basic implementation take?** ประมาณ 10‑15 นาทีสำหรับ stroke ง่าย.  
- **Can I customize the gradient type?** แน่นอน – รองรับ gradient แบบ linear, radial, และ angle‑based.

## เลเยอร์ gradient stroke คืออะไร?
เลเยอร์ gradient stroke คือเส้นขอบเวกเตอร์ที่สีเปลี่ยนอย่างราบรื่นระหว่างสองสีหรือมากกว่านั้น สามารถนำไปใช้กับรูปทรง, ข้อความ, หรือมาสก์เวกเตอร์ใด ๆ ภายในไฟล์ PSD ทำให้ผู้ออกแบบได้เอฟเฟกต์ภาพที่ไดนามิกโดยไม่ต้องแปลงเป็น raster.

## ทำไมต้องใช้ Aspose.PSD for Java?
Aspose.PSD for Java ให้ **full PSD support** สำหรับคุณลักษณะกว่า 100 รายการ — รวมถึงเลเยอร์, มาสก์, เลเยอร์ปรับค่า, และเอฟเฟกต์ของเลเยอร์ – และสามารถประมวลผลไฟล์ขนาดถึง 2 GB โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ไลบรารีทำงานบนระบบปฏิบัติการใด ๆ ที่รองรับ Java, ไม่มีการพึ่งพา native ใด ๆ, และได้รับการอัปเดตทุกเดือนเพื่อให้สอดคล้องกับสเปคไฟล์ Photoshop ล่าสุด.

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ติดตั้ง JDK ล่าสุดจาก [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – ดาวน์โหลดไลบรารีจาก [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, หรือ NetBeans.  
4. **License** – รับ [temporary license](https://purchase.aspose.com/temporary-license/) หากคุณไม่มีใบอนุญาตเชิงพาณิชย์เต็มรูปแบบ.

## นำเข้าแพ็กเกจ
คำสั่ง `import` จะนำคลาสที่จำเป็นเข้าสู่สโคป.

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

ตอนนี้เราจะแบ่งกระบวนการเป็นขั้นตอนที่ชัดเจน

## ขั้นตอนที่ 1: โหลดไฟล์ PSD
การโหลดไฟล์ต้นทางเป็นขั้นตอนแรก; คุณต้องเปิดใช้งานทรัพยากรเอฟเฟกต์เพื่อให้ข้อมูล stroke สามารถแก้ไขได้ **PsdLoadOptions** กำหนดวิธีการโหลดไฟล์ PSD, ให้คุณเปิดหรือปิดทรัพยากรเฉพาะได้

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## ขั้นตอนที่ 2: เข้าถึงเอฟเฟกต์ stroke
**StrokeEffect** แสดงสไตล์เส้นขอบที่ใช้กับเลเยอร์, รวมถึงความกว้าง, สี, และ gradient fill.

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## ขั้นตอนที่ 3: ตรวจสอบคุณสมบัติของเอฟเฟกต์ stroke
ก่อนที่คุณจะทำการแก้ไขใด ๆ ควรอ่านคุณสมบัติที่มีอยู่ก่อน นี่ช่วยให้คุณเข้าใจการตั้งค่าปัจจุบันและหลีกเลี่ยงการเขียนทับการตั้งค่าที่สำคัญโดยไม่ได้ตั้งใจ **GradientFillSettings** เก็บการกำหนดค่า gradient fill สำหรับเอฟเฟกต์ stroke.

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## ขั้นตอนที่ 4: แก้ไขการตั้งค่า gradient fill
`GradientFill` กำหนดวิธีการเปลี่ยนสีผ่าน stroke คุณสามารถเปลี่ยนประเภท (linear, radial), มุม, และ blend mode, จากนั้นกำหนดจุดสีและความโปร่งใสใหม่.

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## ขั้นตอนที่ 5: เพิ่มและแก้ไขจุดสีและความโปร่งใส
gradient ถูกสร้างจากชุดของจุด color‑stop และ opacity‑stop **GradientColorPoint** กำหนดจุดสีใน gradient, ระบุตำแหน่งและสีของมัน **GradientTransparencyPoint** กำหนดจุดความโปร่งใสใน gradient, ระบุตำแหน่งและความโปร่งใส การเพิ่มหรือปรับจุดเหล่านี้ช่วยให้คุณกำหนดรูปแบบการไหลของสีใน stroke.

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่แก้ไข
หลังจากปรับแต่งทั้งหมดแล้ว ให้บันทึกเอกสารที่อัปเดตกลับไปยังดิสก์ Aspose.PSD จะรักษาเลเยอร์และทรัพยากรอื่น ๆ ทั้งหมดโดยอัตโนมัติ.

```text
```java
im.save(exportPath);
```
```

## ขั้นตอนที่ 7: ตรวจสอบการแก้ไข
โหลดไฟล์ที่บันทึกใหม่และตรวจสอบว่า คุณสมบัติ gradient ของ stroke ตรงกับค่าที่คุณตั้งไว้ ขั้นตอนการตรวจสอบนี้สำคัญสำหรับ pipeline อัตโนมัติ **Assert** ให้การตรวจสอบแบบง่ายเพื่อยืนยันเงื่อนไขในระหว่างการทำงาน.

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## ข้อผิดพลาดทั่วไปและเคล็ดลับการแก้ไขปัญหา
- **Missing license error** – หากคุณพบข้อยกเว้นเรื่องใบอนุญาต ตรวจสอบให้แน่ใจว่าไฟล์ใบอนุญาตชั่วคราวถูกโหลดอย่างถูกต้องก่อนเรียกใช้ API ใด ๆ  
- **Gradient not visible** – ตรวจสอบให้แน่ใจว่าแฟล็ก `strokeEnabled` ของเลเยอร์เป้าหมายตั้งเป็น `true`; มิฉะนั้นเอฟเฟกต์จะถูกละเว้นระหว่างการเรนเดอร์  
- **Performance on large files** – สำหรับ PSD ที่ใหญ่กว่า 500 MB พิจารณาใช้ `PsdImage.load(..., LoadOptions)` พร้อม `loadResources = false` และเปิดใช้งานเฉพาะทรัพยากรที่คุณต้องการเท่านั้น

## คำถามที่พบบ่อย

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java เป็นไลบรารี pure‑Java ที่ช่วยให้นักพัฒนาสามารถสร้าง, แก้ไข, แปลง, และเรนเดอร์ไฟล์ Photoshop PSD ได้โดยไม่ต้องใช้ Adobe Photoshop.

**Q: Do I need a license to use Aspose.PSD for Java?**  
A: ใช่, จำเป็นต้องมีใบอนุญาตที่ถูกต้องสำหรับการใช้งานในผลิตภัณฑ์ คุณสามารถรับ [temporary license](https://purchase.aspose.com/temporary-license/) เพื่อการประเมินผลได้.

**Q: Can I create PSD files from scratch with this library?**  
A: แน่นอน. Aspose.PSD มี API สำหรับสร้างเอกสาร PSD ใหม่, เพิ่มเลเยอร์, ใช้เอฟเฟกต์, และบันทึกไฟล์ทั้งหมดโดยโปรแกรม.

**Q: Is it possible to apply other effects besides gradient strokes?**  
A: ใช่, คุณสามารถใช้เงา, แสงเรืองแสง, bevels, และเอฟเฟกต์เลเยอร์อื่น ๆ อีกหลายอย่างโดยใช้ API ที่อิงเอฟเฟกต์เดียวกัน.

**Q: Where can I find the full reference documentation?**  
A: เอกสารอ้างอิงเต็มรูปแบบสามารถดูได้ใน [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

## สรุป
คุณมีวิธีแก้ไขแบบครบวงจรสำหรับการ **create gradient stroke java** ในไฟล์ PSD ด้วย Aspose.PSD โดยการโหลด PSD, เข้าถึงเอฟเฟกต์ stroke, กำหนดค่า gradient fill, และบันทึกไฟล์ คุณสามารถอัตโนมัติกระบวนการกราฟิกที่ซับซ้อนซึ่งโดยปกติจะต้องทำด้วยมือใน Photoshop ทดลองใช้ประเภท gradient, blend mode, และจุดความโปร่งใสต่าง ๆ เพื่อให้ได้ลุคที่ต้องการสำหรับแอปพลิเคชันของคุณ.

---

**อัปเดตล่าสุด:** 2026-09-03  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [สร้าง Gradient Fill PSD ด้วย Java โดยใช้ Aspose.PSD – เพิ่ม Gradient Fill Layer](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [วิธีสร้างเอฟเฟกต์ Radial Gradient ใน Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [วิธีเปลี่ยนสี Stroke ด้วย Java โดยใช้ Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}