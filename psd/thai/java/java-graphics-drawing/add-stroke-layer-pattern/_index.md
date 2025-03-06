---
title: วิธีเพิ่มรูปแบบเลเยอร์ Stroke ใน Java
linktitle: วิธีเพิ่มรูปแบบเลเยอร์ Stroke ใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มรูปแบบเลเยอร์สโตรกให้กับไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนนี้เพื่อปรับปรุงภาพของคุณอย่างง่ายดาย
weight: 11
url: /th/java/java-graphics-drawing/add-stroke-layer-pattern/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มรูปแบบเลเยอร์ Stroke ใน Java

## การแนะนำ
การเพิ่มรูปแบบเลเยอร์สโตรกให้กับรูปภาพใน Java อาจฟังดูเป็นงานที่น่ากังวล แต่ด้วย Aspose.PSD สำหรับ Java มันง่ายกว่าที่คุณคิด ไม่ว่าคุณจะออกแบบกราฟิกหรือใช้งานแอพพลิเคชั่นแก้ไขภาพ คู่มือนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอน พร้อมที่จะเริ่มต้นหรือยัง? มาดำน้ำกันเถอะ!
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเริ่ม คุณจะต้องมีสิ่งต่อไปนี้:
- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
-  Aspose.PSD สำหรับ Java: ดาวน์โหลดไลบรารีจาก[ที่นี่](https://releases.aspose.com/psd/java/) และรวมไว้ในโครงการของคุณ
- IDE: ใช้ Integrated Development Environment (IDE) ที่คุณชื่นชอบ เช่น IntelliJ IDEA หรือ Eclipse
## แพ็คเกจนำเข้า
ก่อนอื่น คุณต้องนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ แพ็คเกจเหล่านี้จำเป็นสำหรับการทำงานกับ Aspose.PSD
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
ขั้นตอนแรกในการเพิ่มรูปแบบเลเยอร์สโตรคคือการโหลดไฟล์ PSD ที่คุณต้องการแก้ไข
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
เมื่อโหลดไฟล์ PSD คุณจะสามารถเข้าถึงและจัดการเลเยอร์และเอฟเฟ็กต์ของไฟล์ได้
## ขั้นตอนที่ 2: เตรียมข้อมูลรูปแบบใหม่
ถัดไป คุณต้องเตรียมข้อมูลรูปแบบใหม่ที่คุณจะนำไปใช้กับเลเยอร์เส้นโครงร่าง
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
ข้อมูลรูปแบบนี้จะถูกนำมาใช้เพื่อสร้างเอฟเฟกต์เส้นโครงร่างใหม่
## ขั้นตอนที่ 3: เข้าถึงเอฟเฟกต์ Stroke
หากต้องการแก้ไขเอฟเฟกต์เส้นโครงร่าง คุณต้องเข้าถึงเลเยอร์ที่ต้องการและตัวเลือกการผสม
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
เพื่อให้แน่ใจว่าคุณกำลังทำงานกับเลเยอร์และเอฟเฟกต์ที่ถูกต้อง
## ขั้นตอนที่ 4: แก้ไขเอฟเฟ็กต์โรคหลอดเลือดสมอง
ตอนนี้ เรามาแก้ไขเอฟเฟกต์เส้นโครงร่างด้วยข้อมูลรูปแบบใหม่กัน
### อัปเดตคุณสมบัติเอฟเฟกต์จังหวะ
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### อัปเดตทรัพยากรรูปแบบ
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
ข้อมูลโค้ดนี้จะอัปเดตทรัพยากรรูปแบบด้วยข้อมูลรูปแบบใหม่
## ขั้นตอนที่ 5: ใช้รูปแบบใหม่
สุดท้าย ใช้รูปแบบใหม่กับเอฟเฟกต์เส้นโครงร่างและบันทึกการเปลี่ยนแปลง
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
เพื่อให้แน่ใจว่ารูปแบบใหม่จะถูกนำไปใช้อย่างถูกต้อง และไฟล์จะถูกบันทึกพร้อมกับการเปลี่ยนแปลง
## ขั้นตอนที่ 6: ตรวจสอบการเปลี่ยนแปลง
เพื่อให้แน่ใจว่าทุกอย่างทำงานได้อย่างถูกต้อง ให้โหลดไฟล์อีกครั้งและตรวจสอบการเปลี่ยนแปลง
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
ขั้นตอนนี้จะตรวจสอบว่าข้อมูลรูปแบบถูกนำไปใช้กับเอฟเฟกต์เส้นโครงร่างอย่างถูกต้อง
## บทสรุป
และคุณก็ได้แล้ว! คุณได้เพิ่มรูปแบบเลเยอร์สโตรกลงในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถปรับแต่งและปรับปรุงรูปภาพของคุณได้อย่างง่ายดาย ขอให้มีความสุขในการเขียนโค้ด!
## คำถามที่พบบ่อย
### Aspose.PSD สำหรับ Java คืออะไร
Aspose.PSD สำหรับ Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถสร้าง แก้ไข และแปลงไฟล์ PSD (เอกสาร Photoshop) โดยทางโปรแกรม
### ฉันสามารถใช้ Aspose.PSD สำหรับ Java ในโปรเจ็กต์เชิงพาณิชย์ได้หรือไม่
 ใช่ คุณสามารถใช้มันในโครงการเชิงพาณิชย์ได้ คุณสามารถซื้อใบอนุญาตได้จาก[ที่นี่](https://purchase.aspose.com/buy).
### มีการทดลองใช้ฟรีสำหรับ Aspose.PSD สำหรับ Java หรือไม่
 ใช่ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุน Aspose.PSD สำหรับ Java ได้อย่างไร
 คุณสามารถรับการสนับสนุนจากฟอรัมชุมชน Aspose[ที่นี่](https://forum.aspose.com/c/psd/34).
### ความต้องการของระบบสำหรับ Aspose.PSD สำหรับ Java คืออะไร
คุณต้องติดตั้ง JDK และ IDE เพื่อการพัฒนา ไลบรารีรองรับระบบปฏิบัติการหลายระบบรวมถึง Windows, Linux และ macOS
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
