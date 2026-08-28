---
date: 2026-08-28
description: เพิ่ม pattern ลงใน layer ด้วย Java ด้วย Aspose.PSD. ทำตามคำแนะนำขั้นตอนต่อขั้นตอนนี้เพื่อใช้
  stroke layer effect, ตั้งค่า pattern resources, และบันทึกไฟล์ PSD ของคุณอย่างมีประสิทธิภาพ.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: วิธีเพิ่ม Stroke Layer Pattern ใน Java
og_description: เพิ่ม pattern ลงใน layer ด้วย Java โดยใช้ Aspose.PSD. ทำตามคำแนะนำสั้นนี้เพื่อใช้
  stroke layer effect, ตั้งค่า pattern resources, และบันทึกไฟล์ PSD ของคุณอย่างมีประสิทธิภาพ.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: เพิ่ม pattern ลงใน layer ด้วย Java – บทแนะนำ Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: วิธีเพิ่ม pattern ลงใน layer ด้วย Java
url: /th/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มลายเส้นให้กับเลเยอร์ใน Java

## บทนำ
การเพิ่มลายเส้นให้กับเลเยอร์ใน Java เป็นความต้องการทั่วไปเมื่อคุณต้องการเสริมไฟล์ Photoshop PSD ด้วยเอฟเฟกต์เส้นขอบแบบกำหนดเอง ด้วย Aspose.PSD for Java งานนี้จะง่ายขึ้น แม้คุณจะใหม่กับไลบรารีนี้ ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีโหลด PSD, สร้างทรัพยากรลาย, แนบเข้ากับเอฟเฟกต์เส้นขอบ, และบันทึกผลลัพธ์—ทั้งหมดด้วยคำแนะนำที่ชัดเจนและเป็นขั้นตอน

## คำตอบสั้น
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD for Java.  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ประมาณ 10‑15 นาทีสำหรับลายพื้นฐาน.  
- **ต้องมีลิขสิทธิ์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **รองรับเวอร์ชัน Java ใด?** JDK 8 หรือใหม่กว่า.  
- **สามารถใช้ในเว็บเซอร์วิสได้หรือไม่?** ใช่, API ไม่จำกัดแพลตฟอร์มและทำงานได้ในสภาพแวดล้อม Java ใดก็ได้.

## การเพิ่มลายเส้นให้กับเลเยอร์คืออะไร?
การเพิ่มลายเส้นให้กับเลเยอร์หมายถึงการกำหนดบิตแมพแบบต่อเนื่องให้กับเอฟเฟกต์เส้นขอบหรือเติมสีเพื่อให้กราฟิกทำซ้ำทั่วขอบของรูปทรง เทคนิคนี้ใช้กันอย่างแพร่หลายสำหรับกรอบตกแต่ง, เนื้อพื้นผิว, และการวางโลโก้, ช่วยให้ผู้ออกแบบสร้างธีมภาพที่สอดคล้องกันโดยไม่ต้องวาดแต่ละองค์ประกอบด้วยตนเอง.

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?
Aspose.PSD รองรับ **รูปแบบภาพกว่า 30 ประเภท** และสามารถจัดการไฟล์ PSD ขนาด **ถึง 2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ, ให้ประสิทธิภาพสูงบนฮาร์ดแวร์เซิร์ฟเวอร์ทั่วไป API ที่ใช้งานง่ายทำให้คุณสามารถทำงานกับเอฟเฟกต์เลเยอร์โดยโปรแกรม, ไม่ต้องพึ่ง Photoshop ในกระบวนการอัตโนมัติ.

## ข้อกำหนดเบื้องต้น
ก่อนคุณเริ่ม, โปรดตรวจสอบว่าคุณมี:
- Java Development Kit (JDK) 8 หรือใหม่กว่า ติดตั้งแล้ว.
- Aspose.PSD for Java – ดาวน์โหลดจาก **หน้าดาวน์โหลด Aspose.PSD for Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) แล้วเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจคของคุณ.
- IDE เช่น IntelliJ IDEA หรือ Eclipse สำหรับแก้ไขและรันโค้ดตัวอย่าง.
- ไฟล์ PSD ตัวอย่างที่มีเลเยอร์รูปทรงที่คุณต้องการแก้ไข.

## นำเข้าแพ็กเกจ
ก่อนอื่นให้ import namespaces ที่ให้การเข้าถึงออบเจ็กต์ PSD, ทรัพยากร, และเอฟเฟกต์.

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## วิธีเพิ่มลายเส้นให้กับเลเยอร์ใน Java?

โหลดไฟล์ PSD เป้าหมาย, สร้างทรัพยากรลาย, แนบเข้ากับเอฟเฟกต์เส้นขอบของเลเยอร์ที่ต้องการ, และสุดท้ายบันทึกไฟล์ กระบวนการครบวงจรนี้ใช้เพียงไม่กี่บรรทัดของโค้ดและทำงานกับ PSD มาตรฐานใด ๆ ที่มีเลเยอร์รูปทรงเวกเตอร์.

### ขั้นตอนที่ 1: โหลดไฟล์ PSD
การโหลดเอกสารทำให้คุณเข้าถึงโครงสร้างเลเยอร์และคอลเลกชันเอฟเฟกต์ของมัน  
`PsdLoadOptions` กำหนดวิธีการอ่าน PSD, ส่วน `PsdImage` แทนไฟล์ที่โหลดในหน่วยความจำ.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

โดยการโหลดไฟล์ PSD คุณสามารถเข้าถึงและจัดการเลเยอร์และเอฟเฟกต์ของมันได้แล้ว.

### ขั้นตอนที่ 2: เตรียมข้อมูลลายใหม่
สร้าง `PatternResource` ที่เก็บบิตแมพที่คุณต้องการทำเป็นลายเส้นขอบ `PatternResource` เป็นทรัพยากรระดับโลกของ PSD ที่เก็บลายบิตแมพที่ทำซ้ำ `Rectangle` กำหนดขอบเขตของลาย, และ `UUID` ให้ตัวระบุที่ไม่ซ้ำกัน.

```
// Placeholder for original code.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
```

ข้อมูลลายนี้จะถูกใช้เพื่อสร้างเอฟเฟกต์เส้นขอบใหม่.

### ขั้นตอนที่ 3: เข้าถึงเอฟเฟกต์เส้นขอบ
ระบุเลเยอร์รูปทรงที่มีเส้นขอบอยู่แล้ว, จากนั้นดึงออบเจ็กต์ `StrokeEffect` ของมัน `StrokeEffect` แสดงถึงเอฟเฟกต์เส้นขอบที่ใช้กับเลเยอร์รูปทรง.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

นี่ทำให้แน่ใจว่าคุณกำลังทำงานกับเลเยอร์และเอฟเฟกต์ที่ถูกต้อง.

### ขั้นตอนที่ 4: ปรับแก้เอฟเฟกต์เส้นขอบ
ตอนนี้อัปเดตคุณสมบัติของเส้นขอบให้อ้างอิงถึงทรัพยากรลายใหม่.

#### อัปเดตคุณสมบัติของเอฟเฟกต์เส้นขอบ
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### อัปเดตทรัพยากรลาย
`PattResource` เป็นทรัพยากรระดับโลกของ PSD ที่เก็บข้อมูลลาย.

```
// Placeholder for original code.
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
```

โค้ดเหล่านี้แทนที่ลายเดิมด้วยลายที่คุณกำหนด.

### ขั้นตอนที่ 5: ใช้ลายใหม่
`PatternFillSettings` เก็บการตั้งค่าการเติมสำหรับเอฟเฟกต์เส้นขอบแบบลาย. ทำการบันทึกการเปลี่ยนแปลงลงในเลเยอร์และเขียน PSD ที่อัปเดตกลับไปยังดิสก์.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

นี่ทำให้แน่ใจว่าลายใหม่ถูกนำไปใช้ถูกต้องและไฟล์ถูกบันทึกพร้อมการเปลี่ยนแปลง.

### ขั้นตอนที่ 6: ตรวจสอบการเปลี่ยนแปลง
โหลดไฟล์ใหม่และตรวจสอบเส้นขอบเพื่อยืนยันว่าลายปรากฏตามที่คาดหวัง.

```
// Placeholder for original code.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
```

ขั้นตอนนี้ตรวจสอบว่าข้อมูลลายได้ถูกนำไปใช้กับเอฟเฟกต์เส้นขอบอย่างถูกต้อง.

## ปัญหาทั่วไปและการแก้ไข
- **ลายไม่แสดง:** ตรวจสอบให้แน่ใจว่า DPI ของภาพลายตรงกับความละเอียดของ PSD, และฟลัก `Enabled` ของเส้นขอบตั้งเป็น `true`.  
- **ไฟล์ PSD ขนาดใหญ่ทำให้เกิด OutOfMemoryError:** ใช้ `PsdImage.load(..., LoadOptions)` พร้อม `LoadOptions.setLoadAllLayers(false)` เพื่อโหลดเลเยอร์ตามความต้องการ.  
- **เลือกเลเยอร์ผิด:** ตรวจสอบดัชนีหรือชื่อของเลเยอร์ก่อนเข้าถึงเอฟเฟกต์; คุณสามารถ enumerate `psdImage.getLayers()` เพื่อแสดงรายการเลเยอร์ที่มี.

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้ผู้พัฒนาสามารถสร้าง, แก้ไข, และแปลงไฟล์ PSD (Photoshop Document) ได้โดยโปรแกรม.

**ถาม: ฉันสามารถใช้ Aspose.PSD for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ได้, คุณสามารถใช้ในโครงการเชิงพาณิชย์ได้ คุณสามารถซื้อไลเซนส์จาก **หน้าซื้อของ Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**ถาม: มีเวอร์ชันทดลองฟรีสำหรับ Aspose.PSD for Java หรือไม่?**  
A: มี, คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีจาก **หน้า releases ของ Aspose**([Aspose releases page](https://releases.aspose.com/)).

**ถาม: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.PSD for Java ได้อย่างไร?**  
A: คุณสามารถรับการสนับสนุนจากฟอรั่มชุมชนของ Aspose **ที่นี่**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**ถาม: ความต้องการระบบสำหรับ Aspose.PSD for Java มีอะไรบ้าง?**  
A: คุณต้องมี JDK ติดตั้งและ IDE สำหรับการพัฒนา ไลบรารีรองรับ Windows, Linux, และ macOS.

## สรุป
คุณได้เรียนรู้วิธีเพิ่มลายเส้นให้กับเลเยอร์ใน Java ด้วย Aspose.PSD แล้ว ด้วยการทำตามขั้นตอนข้างต้นคุณสามารถเสริมไฟล์ PSD ด้วยลายเส้นขอบแบบกำหนดเองโดยอัตโนมัติ, ทำงานกระบวนการแบรนด์ดิ้งอัตโนมัติ, และรวมการประมวลผลกราฟิกเข้าไปในแอปพลิเคชันที่ใช้ Java สำรวจคุณสมบัติอื่นของ Aspose.PSD เช่น การรวมเลเยอร์, การปรับสี, และการส่งออกเป็น PNG หรือ JPEG เพื่อขยายเครื่องมือการประมวลผลภาพของคุณต่อไป.

---

**อัปเดตล่าสุด:** 2026-08-28  
**ทดสอบกับ:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [เรนเดอร์เลเยอร์เติมลายในไฟล์ PSD](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Pattern Overlay PSD: เพิ่มเอฟเฟกต์ด้วย Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [วิธีเปลี่ยนสีเส้นขอบใน Java ด้วย Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}