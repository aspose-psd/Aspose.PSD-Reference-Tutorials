---
title: วิธีเพิ่มการไล่ระดับสี Stroke Layer ใน Java
linktitle: วิธีเพิ่มการไล่ระดับสี Stroke Layer ใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มและปรับแต่งการไล่ระดับสีเลเยอร์สโตรกในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java พร้อมบทช่วยสอนทีละขั้นตอนที่ครอบคลุมนี้
type: docs
weight: 10
url: /th/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## การแนะนำ
เคยสงสัยบ้างไหมว่าจะเพิ่มการไล่ระดับสีเลเยอร์สโตรกให้กับรูปภาพของคุณโดยใช้ Java ได้อย่างไร? คุณอยู่ในสถานที่ที่เหมาะสม! วันนี้ เรากำลังดำดิ่งสู่โลกของ Aspose.PSD สำหรับ Java ซึ่งเป็นไลบรารีอันทรงพลังที่ช่วยให้คุณจัดการไฟล์ PSD ได้อย่างง่ายดาย ไม่ว่าคุณจะเป็นมือใหม่หรือนักพัฒนาที่มีประสบการณ์ คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดขั้นตอนการเพิ่มการไล่ระดับสีเลเยอร์เส้นขีดให้กับไฟล์ PSD ของคุณ ดังนั้น รัดเข็มขัดให้พร้อมและเตรียมพร้อมที่จะพัฒนาทักษะการแก้ไขกราฟิกของคุณ!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม มีบางสิ่งที่คุณต้องมี ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณ คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ของออราเคิล](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD สำหรับ Java Library: คุณสามารถดาวน์โหลดได้จากไฟล์[หน้าดาวน์โหลด Aspose.PSD](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): IDE ใดๆ เช่น IntelliJ IDEA, Eclipse หรือ NetBeans จะใช้งานได้
4.  ใบอนุญาตที่ถูกต้อง: คุณสามารถรับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) ถ้าคุณไม่มีอันเต็ม
## แพ็คเกจนำเข้า
ก่อนอื่น เรามานำเข้าแพ็คเกจที่จำเป็นกันก่อน สิ่งเหล่านี้จะช่วยให้เราสามารถใช้คลาสและวิธีการที่จำเป็นสำหรับการจัดการไฟล์ PSD
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
ตอนนี้ เรามาแบ่งตัวอย่างออกเป็นหลายขั้นตอนเพื่อความเข้าใจที่ดีขึ้น
## ขั้นตอนที่ 1: โหลดไฟล์ PSD
 ขั้นแรก เราต้องโหลดไฟล์ PSD ที่เราต้องการแก้ไข เราจะใช้`PsdLoadOptions` เพื่อระบุว่าเราต้องการโหลดทรัพยากรเอฟเฟกต์
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## ขั้นตอนที่ 2: เข้าถึงเอฟเฟกต์ Stroke
ต่อไป เราต้องเข้าถึงเอฟเฟ็กต์เส้นขีดของเลเยอร์ที่เราสนใจ ในกรณีนี้ เราถือว่าเป็นเลเยอร์ที่สาม (ดัชนี 2) ในไฟล์ PSD
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## ขั้นตอนที่ 3: ตรวจสอบคุณสมบัติเอฟเฟกต์โรคหลอดเลือดสมอง
ก่อนที่จะทำการเปลี่ยนแปลงใดๆ มาตรวจสอบคุณสมบัติของเอฟเฟกต์เส้นโครงร่างเพื่อให้แน่ใจว่าเราได้แก้ไขการตั้งค่าที่ถูกต้อง
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
## ขั้นตอนที่ 4: แก้ไขการตั้งค่าการเติมไล่ระดับสี
ตอนนี้ได้เวลาแก้ไขการตั้งค่าการเติมไล่ระดับสีตามความต้องการของเรา เราจะเปลี่ยนสี ความทึบ โหมดผสมผสาน และคุณสมบัติอื่นๆ
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
## ขั้นตอนที่ 5: เพิ่มและแก้ไขสีและจุดโปร่งใส
มาเพิ่มจุดสีและความโปร่งใสใหม่และแก้ไขจุดที่มีอยู่เพื่อให้ได้เอฟเฟกต์การไล่ระดับสีที่ต้องการ
```java
// เพิ่มจุดสีใหม่
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// เปลี่ยนตำแหน่งของจุดก่อนหน้า
fillSettings.getColorPoints()[1].setLocation(1899);
// เพิ่มจุดโปร่งใสใหม่
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// เปลี่ยนตำแหน่งของจุดโปร่งใสก่อนหน้า
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่แก้ไข
หลังจากทำการแก้ไขที่จำเป็นทั้งหมดแล้ว เราจำเป็นต้องบันทึกไฟล์ PSD
```java
im.save(exportPath);
```
## ขั้นตอนที่ 7: ตรวจสอบการแก้ไข
สุดท้ายนี้ ให้โหลดไฟล์ PSD ที่บันทึกไว้และตรวจสอบว่าการเปลี่ยนแปลงของเรานำไปใช้อย่างถูกต้อง
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// ตรวจสอบจุดสี
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
// ตรวจสอบจุดโปร่งใส
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## บทสรุป
และคุณก็ได้แล้ว! ตอนนี้คุณรู้วิธีเพิ่มและจัดการการไล่ระดับสีเลเยอร์เส้นขีดในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java แล้ว บทช่วยสอนนี้ครอบคลุมถึงการโหลดไฟล์ PSD การเข้าถึงและแก้ไขเอฟเฟกต์เส้นขีด และบันทึกการเปลี่ยนแปลง ด้วยทักษะเหล่านี้ คุณสามารถสร้างการไล่ระดับสีที่ดึงดูดสายตาและปรับแต่งไฟล์ PSD ของคุณให้เหมาะกับความต้องการของคุณ
## คำถามที่พบบ่อย
### Aspose.PSD สำหรับ Java คืออะไร
Aspose.PSD สำหรับ Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ PSD ในแอปพลิเคชัน Java ได้ โดยมีคุณสมบัติในการสร้าง จัดการ และแปลงไฟล์ PSD
### ฉันต้องมีใบอนุญาตเพื่อใช้ Aspose.PSD สำหรับ Java หรือไม่
 ใช่ คุณต้องมีใบอนุญาตที่ถูกต้องเพื่อใช้ Aspose.PSD สำหรับ Java คุณจะได้รับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการประเมินผล
### ฉันสามารถใช้ Aspose.PSD สำหรับ Java เพื่อสร้างไฟล์ PSD ตั้งแต่เริ่มต้นได้หรือไม่
อย่างแน่นอน! Aspose.PSD สำหรับ Java มี API ที่ครอบคลุมเพื่อสร้างและจัดการไฟล์ PSD โดยทางโปรแกรม
### เป็นไปได้ไหมที่จะใช้เอฟเฟกต์อื่นโดยใช้ Aspose.PSD สำหรับ Java
ใช่ คุณสามารถใช้เอฟเฟ็กต์ต่างๆ เช่น เงา เรืองแสง และอื่นๆ โดยใช้ Aspose.PSD สำหรับ Java
### ฉันจะหาเอกสารสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน
 คุณสามารถค้นหาเอกสาร[ที่นี่](https://reference.aspose.com/psd/java/).