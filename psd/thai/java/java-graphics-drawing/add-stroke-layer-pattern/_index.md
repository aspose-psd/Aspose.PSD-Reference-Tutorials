---
date: 2026-01-17
description: เรียนรู้วิธีเพิ่มลายเส้นใน Java ด้วย Aspose.PSD for Java. ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อปรับปรุงภาพ
  PSD ของคุณอย่างรวดเร็ว.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: วิธีเพิ่มลายเส้นใน Java ด้วย Aspose.PSD
url: /th/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่ม Stroke Pattern Java ด้วย Aspose.PSD

## บทนำ
หากคุณต้องการ **add stroke pattern java** ลงในไฟล์ Photoshop, Aspose.PSD for Java ทำให้ขั้นตอนนี้ง่ายกว่าที่คิด ไม่ว่าคุณจะกำลังสร้างเครื่องมือออกแบบกราฟิก, ทำการแก้ไขเป็นชุดอัตโนมัติ, หรือแค่ทดลองกับเอฟเฟกต์เลเยอร์, บทเรียนนี้จะพาคุณผ่านทุกขั้นตอน—from การโหลด PSD ไปจนถึงการตรวจสอบ Pattern ใหม่. มาดูกันว่าคุณสามารถเพิ่มคุณค่าให้กับภาพของคุณได้เร็วแค่ไหน.

## คำตอบอย่างรวดเร็ว
- **ต้องการไลบรารีอะไร?** Aspose.PSD for Java  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** JDK 8 หรือใหม่กว่า  
- **ต้องมีลิขสิทธิ์สำหรับการทดสอบหรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา; จำเป็นต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ประมาณ 10‑15 นาทีสำหรับ Stroke Pattern พื้นฐาน  
- **สามารถใช้ Pattern ซ้ำบนหลายเลเยอร์ได้หรือไม่?** ได้, เพียงกำหนด `PattResource` เดียวกันให้กับเลเยอร์อื่น ๆ  

## add stroke pattern java คืออะไร?
การเพิ่ม Stroke Pattern ใน Java หมายถึงการใช้ Fill แบบกำหนดเอง (มักเป็น Bitmap ที่ทำซ้ำ) กับเอฟเฟกต์ Stroke ของเลเยอร์. เทคนิคนี้ช่วยให้คุณสร้างขอบเส้นสไตล์ต่าง ๆ — เช่น เส้นประ, พื้นผิวอิฐ, หรือกรอบกราฟิกที่กำหนดเอง — โดยตรงในไฟล์ PSD โดยไม่ต้องเปิด Photoshop.

## ทำไมต้องใช้ Aspose.PSD สำหรับ add stroke pattern java?
- **Full PSD fidelity** – ทุกเอฟเฟกต์เลเยอร์, resource, และโหมดการผสมจะถูกเก็บรักษาไว้ครบถ้วน.  
- **ไม่ต้องใช้ Photoshop ติดตั้ง** – ทำงานบนระบบปฏิบัติการใดก็ได้ที่มี JDK.  
- **ควบคุมแบบโปรแกรม** – สามารถทำการประมวลผลเป็นชุดหรือรวมเข้าในบริการฝั่งเซิร์ฟเวอร์ได้.  
- **Rich API** – เข้าถึง resource ทั้งหมด, pattern fill, และ blend mode ผ่านอินเทอร์เฟซเดียวที่ใช้งานง่าย.

## ข้อกำหนดเบื้องต้น
- **Java Development Kit (JDK)** – ตรวจสอบให้แน่ใจว่าติดตั้ง JDK 8 หรือใหม่กว่า.  
- **Aspose.PSD for Java** – ดาวน์โหลดไลบรารีจาก [here](https://releases.aspose.com/psd/java/) และเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจกต์.  
- **IDE** – IntelliJ IDEA, Eclipse, หรือเครื่องมือแก้ไขใดก็ได้ที่คุณชอบ.

## นำเข้าแพ็กเกจ
ก่อนอื่นให้ import คลาสที่จำเป็นสำหรับการจัดการไฟล์ PSD, สี, สี่เหลี่ยม, และเอฟเฟกต์ Stroke.

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

## ขั้นตอนที่ 1: โหลดไฟล์ PSD
โหลดไฟล์ PSD ต้นฉบับเพื่อให้คุณสามารถทำงานกับเลเยอร์และ resource ต่าง ๆ ได้.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## ขั้นตอนที่ 2: เตรียมข้อมูล Pattern ใหม่
สร้าง Pattern ขนาด 4 × 4 พิกเซลแบบง่ายที่จะใช้สำหรับ Stroke.

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

## ขั้นตอนที่ 3: เข้าถึง Stroke Effect
ค้นหา Stroke Effect บนเลเยอร์เป้าหมาย (ในตัวอย่างนี้คือเลเยอร์ที่สี่).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## ขั้นตอนที่ 4: แก้ไข Stroke Effect
### อัปเดตคุณสมบัติของ Stroke Effect
ปรับค่า opacity และ blend mode เพื่อดูผลลัพธ์ของ Pattern ใหม่.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### อัปเดต Pattern Resource
แทนที่ Pattern Resource ทั่วโลกที่มีอยู่ด้วย Pattern ที่คุณเพิ่งสร้าง.

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

## ขั้นตอนที่ 5: ใช้ Pattern ใหม่
ผูก Pattern Resource ที่อัปเดตแล้วกับ Stroke Effect และบันทึกไฟล์ PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## ขั้นตอนที่ 6: ตรวจสอบการเปลี่ยนแปลง
โหลดไฟล์ใหม่อีกครั้งและยืนยันว่า Pattern, opacity, และ blend mode ถูกนำไปใช้อย่างถูกต้อง.

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

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| Pattern ไม่แสดง | อ้างอิง `PatternId` ผิด | ตรวจสอบให้แน่ใจว่า `PatternId` ที่ตั้งบน `PattResource` ตรงกับที่ใช้ใน `PatternFillSettings`. |
| Stroke หายไปหลังบันทึก | Opacity ตั้งเป็น 0 หรือเอฟเฟกต์ถูกซ่อน | ตรวจสอบว่า `setOpacity` อยู่ระหว่าง 0‑255 และ `isVisible()` คืนค่า `true`. |
| สีที่ไม่คาดคิด | Blend mode ไม่ตรงกัน | ใช้ `BlendMode.Color` (หรือโหมดอื่น) ที่ตรงกับความต้องการออกแบบของคุณ. |

## คำถามที่พบบ่อย
### Aspose.PSD for Java คืออะไร?
Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสร้าง, แก้ไข, และแปลงไฟล์ PSD (Photoshop Document) ได้โดยโปรแกรม.

### ฉันสามารถใช้ Aspose.PSD for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?
ได้, คุณสามารถใช้ในโครงการเชิงพาณิชย์ได้. คุณสามารถซื้อไลเซนส์ได้จาก [here](https://purchase.aspose.com/buy).

### มีรุ่นทดลองฟรีสำหรับ Aspose.PSD for Java หรือไม่?
มี, คุณสามารถดาวน์โหลดรุ่นทดลองฟรีได้จาก [here](https://releases.aspose.com/).

### ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD for Java อย่างไร?
คุณสามารถรับการสนับสนุนจากฟอรั่มชุมชนของ Aspose [here](https://forum.aspose.com/c/psd/34).

### ความต้องการระบบสำหรับ Aspose.PSD for Java มีอะไรบ้าง?
คุณต้องมี JDK ติดตั้งและ IDE สำหรับการพัฒนา. ไลบรารีรองรับหลายระบบปฏิบัติการรวมถึง Windows, Linux, และ macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-17  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (ล่าสุดในขณะเขียน)  
**ผู้เขียน:** Aspose