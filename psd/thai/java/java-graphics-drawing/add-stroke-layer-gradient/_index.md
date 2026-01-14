---
date: 2026-01-14
description: เรียนรู้วิธีสร้างเลเยอร์เส้นขอบแบบไล่สีและปรับแต่งการไล่สีของเส้นขอบในไฟล์
  PSD ด้วย Aspose.PSD สำหรับ Java ผ่านบทเรียนขั้นตอนต่อขั้นตอนนี้.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: วิธีสร้างเลเยอร์เส้นขอบไล่สีใน Java
url: /th/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างเลเยอร์เส้นขอบไล่ระดับสีใน Java

## บทนำ
เคยสงสัยไหมว่า **จะสร้างเลเยอร์เส้นขอบไล่ระดับสี** ในไฟล์ PSD ของคุณโดยใช้ Java อย่างไร? คุณมาถูกที่แล้ว! วันนี้เราจะเจาะลึก Aspose.PSD for Java—ไลบรารีที่ทรงพลังซึ่งช่วยให้คุณจัดการไฟล์ PSD ได้อย่างง่ายดาย ไม่ว่าคุณจะเป็นมือใหม่ในการเขียนโปรแกรมกราฟิกหรือกำลังมองหาวิธีปรับแต่งการออกแบบที่มีอยู่แล้ว คู่มือนี้จะพาคุณผ่านขั้นตอนการเพิ่มและปรับแต่งเส้นขอบไล่ระดับสีอย่างเป็นขั้นเป็นตอน

## คำตอบอย่างรวดเร็ว
- **เป้าหมายหลักคืออะไร?** สร้างเลเยอร์เส้นขอบไล่ระดับสีบนไฟล์ PSD  
- **ต้องใช้ไลบรารีใด?** Aspose.PSD for Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** ใช่, จำเป็นต้องมีลิขสิทธิ์ที่ถูกต้อง (หรือชั่วคราว) สำหรับการใช้งานในโปรดักชัน  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 หรือสูงกว่า  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ประมาณ 10‑15 นาทีสำหรับเส้นขอบไล่ระดับสีพื้นฐาน

## เลเยอร์เส้นขอบไล่ระดับสีคืออะไร?
เลเยอร์เส้นขอบไล่ระดับสีคือเส้นขอบเวกเตอร์รอบรูปทรงหรือข้อความที่เปลี่ยนสีอย่างราบรื่นระหว่างสีต่าง ๆ โดยใช้ Aspose.PSD คุณสามารถกำหนดสี, ความทึบ, มุม, และประเภท (เช่น linear, radial ฯลฯ) ของเส้นขอบได้โดยโปรแกรม

## ทำไมต้องใช้ Aspose.PSD for Java?
- **รองรับ PSD อย่างเต็มรูปแบบ** – อ่าน, แก้ไข, และเขียนไฟล์ PSD ได้โดยไม่ต้องใช้ Photoshop  
- **API เอฟเฟกต์ที่หลากหลาย** – เข้าถึงเส้นขอบ, เงา, แสงเรืองแสง, และเอฟเฟกต์เลเยอร์อื่น ๆ มากมาย  
- **ข้ามแพลตฟอร์ม** – ทำงานบนระบบปฏิบัติการใดก็ได้ที่รองรับ Java  
- **ไม่มีการพึ่งพาเนทีฟ** – เป็น Java แท้ ๆ, ง่ายต่อการรวมเข้ากับ pipeline CI

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ติดตั้ง JDK ล่าสุดจาก [เว็บไซต์ของ Oracle](https://www.oracle.com/java/technologies/javase-downloads.html)  
2. **Aspose.PSD for Java** – ดาวน์โหลดไลบรารีจาก [หน้าดาวน์โหลด Aspose.PSD](https://releases.aspose.com/psd/java/)  
3. **IDE** – IntelliJ IDEA, Eclipse หรือ NetBeans  
4. **License** – รับ [ลิขสิทธิ์ชั่วคราว](https://purchase.aspose.com/temporary-license/) หากคุณยังไม่มีลิขสิทธิ์เต็มรูปแบบ

## นำเข้าชุดแพ็กเกจ
ก่อนอื่นให้ทำการนำเข้าคลาสที่จำเป็นสำหรับการโหลด PSD, เข้าถึงเอฟเฟกต์, และกำหนดการเติมสีไล่ระดับ

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

ตอนนี้เรามาแบ่งกระบวนการเป็นขั้นตอนที่ชัดเจนกัน

## ขั้นตอนที่ 1: โหลดไฟล์ PSD
เราจะโหลดไฟล์ PSD ต้นฉบับและเปิดใช้งานทรัพยากรเอฟเฟกต์เพื่อให้เส้นขอบพร้อมใช้งาน

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## ขั้นตอนที่ 2: เข้าถึงเอฟเฟกต์เส้นขอบ
สมมติว่าเส้นขอบที่ต้องการแก้ไขอยู่ในเลเยอร์ที่สาม (ดัชนี 2) เราจะดึง `StrokeEffect` ของมันออกมา

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## ขั้นตอนที่ 3: ตรวจสอบคุณสมบัติของเอฟเฟกต์เส้นขอบ
ก่อนทำการเปลี่ยนแปลง เราจะตรวจสอบการตั้งค่าปัจจุบันเพื่อให้ทราบว่าต้องอัปเดตอะไรบ้าง

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

## ขั้นตอนที่ 4: แก้ไขการตั้งค่าการเติมสีไล่ระดับ
ที่นี่เราจะเปลี่ยนสี, ความทึบ, โหมดผสม, และคุณสมบัติอื่น ๆ เพื่อให้ได้ลุคที่ต้องการ

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

## ขั้นตอนที่ 5: เพิ่มและแก้ไขจุดสีและความโปร่งใส
เราจะเพิ่มจุดสีและความโปร่งใสใหม่ แล้วปรับจุดที่มีอยู่เพื่อกำหนดรูปแบบของไล่ระดับสี

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

## ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
หลังจากปรับแต่งทั้งหมดเสร็จ เราจะเขียนไฟล์ที่อัปเดตกลับไปยังดิสก์

```java
im.save(exportPath);
```

## ขั้นตอนที่ 7: ตรวจสอบการแก้ไข
โหลดไฟล์ที่บันทึกไว้และตรวจสอบว่าทุกคุณสมบัติตรงกับการเปลี่ยนแปลงที่เราได้ทำ

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
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## สรุป
คุณได้เรียนรู้วิธี **สร้างเลเยอร์เส้นขอบไล่ระดับสี** ในไฟล์ PSD ด้วย Aspose.PSD for Java แล้ว โดยการโหลด PSD, เข้าถึงเอฟเฟกต์เส้นขอบ, ปรับการตั้งค่าการเติมสีไล่ระดับ, และบันทึกผลลัพธ์ คุณสามารถสร้างกราฟิกระดับมืออาชีพโดยไม่ต้องเปิด Photoshop

## คำถามที่พบบ่อย
### Aspose.PSD for Java คืออะไร?
Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ PSD ในแอปพลิเคชัน Java ได้, ให้ฟีเจอร์ในการสร้าง, แก้ไข, และแปลงไฟล์ PSD

### จำเป็นต้องมีลิขสิทธิ์เพื่อใช้ Aspose.PSD for Java หรือไม่?
ใช่, คุณต้องมีลิขสิทธิ์ที่ถูกต้องเพื่อใช้ Aspose.PSD for Java คุณสามารถรับ [ลิขสิทธิ์ชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อการประเมินผลได้

### สามารถใช้ Aspose.PSD for Java เพื่อสร้างไฟล์ PSD ตั้งแต่เริ่มต้นได้หรือไม่?
ได้เลย! Aspose.PSD for Java มี API ครบวงจรสำหรับสร้างและจัดการไฟล์ PSD ด้วยโปรแกรม

### สามารถใช้ Aspose.PSD for Java เพื่อใช้เอฟเฟกต์อื่น ๆ ได้หรือไม่?
ได้, คุณสามารถใช้เอฟเฟกต์ต่าง ๆ เช่น เงา, แสงเรืองแสง, และอื่น ๆ ด้วย Aspose.PSD for Java

### จะหาเอกสารประกอบการใช้งาน Aspose.PSD for Java ได้จากที่ไหน?
คุณสามารถดูเอกสารได้ [ที่นี่](https://reference.aspose.com/psd/java/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-14  
**ทดสอบกับ:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose