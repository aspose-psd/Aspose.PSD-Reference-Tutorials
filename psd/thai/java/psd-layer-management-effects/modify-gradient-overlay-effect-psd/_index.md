---
title: แก้ไขเอฟเฟกต์การไล่ระดับสีแบบไล่ระดับสีใน PSD โดยใช้ Java
linktitle: แก้ไขเอฟเฟกต์การไล่ระดับสีแบบไล่ระดับสีใน PSD โดยใช้ Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีแก้ไขเอฟเฟกต์การไล่ระดับสีในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ปฏิบัติตามคำแนะนำของเราเพื่อทำให้ไฟล์ PSD ของคุณเป็นอัตโนมัติและปรับแต่งได้อย่างมีประสิทธิภาพ
weight: 12
url: /th/java/psd-layer-management-effects/modify-gradient-overlay-effect-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แก้ไขเอฟเฟกต์การไล่ระดับสีแบบไล่ระดับสีใน PSD โดยใช้ Java

## การแนะนำ

คุณพร้อมที่จะดำดิ่งสู่โลกแห่งศิลปะดิจิทัลด้วย Java แล้วหรือยัง? หากคุณกำลังทำงานกับไฟล์ Photoshop (PSD) และต้องการจัดการไฟล์เหล่านั้นโดยทางโปรแกรม คุณก็ยินดีเป็นอย่างยิ่ง วันนี้เราจะมาสำรวจวิธีการปรับเปลี่ยนเอฟเฟกต์การไล่ระดับสีในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาซอฟต์แวร์ที่ต้องการทำงานออกแบบกราฟิกแบบอัตโนมัติหรือแค่อยากรู้เกี่ยวกับกระบวนการนี้ บทช่วยสอนนี้จะแนะนำคุณทีละขั้นตอน ในตอนท้าย คุณจะมีความรู้ในการเพิ่มสัมผัสแบบมืออาชีพให้กับรูปภาพของคุณโดยไม่ต้องเปิด Photoshop

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม เรามาตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่คุณต้องการแล้ว นี่คือรายการตรวจสอบด่วน:

-  Aspose.PSD สำหรับไลบรารี Java: คุณจะต้องมี Aspose.PSD สำหรับไลบรารี Java หากยังไม่มีก็สามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).
- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK 1.8 หรือใหม่กว่าบนเครื่องของคุณ
- สภาพแวดล้อมการพัฒนาแบบผสมผสาน (IDE): Java IDE ใดๆ เช่น IntelliJ IDEA หรือ Eclipse จะทำงานได้อย่างสมบูรณ์แบบ
- ไฟล์ PSD ตัวอย่าง: เลือกไฟล์ PSD ตัวอย่างที่มีเลเยอร์ซึ่งคุณสามารถใช้การซ้อนทับแบบไล่ระดับสีได้ คุณสามารถใช้ไฟล์ของคุณเองหรือดาวน์โหลด PSD ทดสอบจากเว็บ
- ความรู้พื้นฐานของ Java: แม้ว่าฉันจะแนะนำคุณในแต่ละขั้นตอน แต่ความเข้าใจพื้นฐานเกี่ยวกับ Java จะช่วยให้คุณปฏิบัติตามได้ง่ายขึ้น

เมื่อคุณเตรียมทุกอย่างเรียบร้อยแล้ว เราก็พร้อมที่จะเข้าสู่โค้ดทันที!

## แพ็คเกจนำเข้า

ก่อนอื่น เราต้องแน่ใจว่าเราได้นำเข้าแพ็คเกจที่จำเป็นทั้งหมดแล้ว การนำเข้าเหล่านี้จะช่วยให้คุณสามารถทำงานกับไฟล์ PSD ใช้เอฟเฟกต์ และบันทึกไฟล์ที่คุณแก้ไข

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layereffects.ILayerEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

ขั้นตอนแรกในการปรับเปลี่ยนเอฟเฟกต์การไล่ระดับสีคือการโหลดไฟล์ PSD นี่คือจุดที่ Aspose.PSD สำหรับ Java เข้ามามีบทบาท คุณจะโหลดไฟล์ โดยต้องเปิดใช้งานการรองรับเอฟเฟกต์เลเยอร์ที่มีอยู่

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "psdnet256.psd";

//เปิดใช้งานการรองรับเอฟเฟกต์เลเยอร์ที่มีอยู่
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);

// โหลดไฟล์ PSD
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath, psdLoadOptions);
```

 คำอธิบาย: เราเริ่มต้นด้วยการตั้งค่าเส้นทางของไฟล์และโหลดไฟล์ PSD ที่`PsdLoadOptions` object มีความสำคัญที่นี่เพราะช่วยให้คุณสามารถโหลดไฟล์ PSD พร้อมเอฟเฟกต์เลเยอร์ที่มีอยู่ทั้งหมดได้ เพื่อให้แน่ใจว่าการแก้ไขใดๆ ที่คุณทำจะถูกนำไปใช้กับเลเยอร์ที่ถูกต้องอย่างถูกต้อง

## ขั้นตอนที่ 2: ค้นหาเลเยอร์เป้าหมาย

เมื่อคุณโหลดไฟล์ PSD แล้ว ขั้นตอนต่อไปคือการค้นหาเลเยอร์เฉพาะที่คุณต้องการใช้หรือแก้ไขเอฟเฟกต์การซ้อนทับแบบไล่ระดับสี ขั้นตอนนี้มีความสำคัญเนื่องจากเลเยอร์ในไฟล์ Photoshop สามารถมีเนื้อหาได้หลายประเภท และคุณต้องการให้แน่ใจว่าคุณกำหนดเป้าหมายที่ถูกต้อง

```java
BlendingOptions layerBlendOptions = psdImage.getLayers()[1].getBlendingOptions();
```

คำอธิบาย: ในตัวอย่างนี้ เรากำลังเข้าถึงเลเยอร์ที่สองในไฟล์ PSD (`psdImage.getLayers()[1]` - ที่`BlendingOptions` วัตถุช่วยให้คุณเข้าถึงตัวเลือกการผสมของเลเยอร์ ซึ่งมีการจัดการเอฟเฟกต์เช่นการซ้อนทับแบบไล่ระดับสี หากคุณต้องการทำงานกับเลเยอร์อื่น เพียงปรับดัชนี`[1]`ให้ได้จำนวนชั้นที่เหมาะสม

## ขั้นตอนที่ 3: ค้นหาเอฟเฟกต์การซ้อนทับไล่ระดับสีที่มีอยู่

เมื่อคุณระบุเลเยอร์เป้าหมายแล้ว ก็ถึงเวลาตรวจสอบว่ามีการใช้เอฟเฟกต์การไล่ระดับสีซ้อนทับแล้วหรือไม่ หากมีคุณจะแก้ไขมัน ถ้าไม่เช่นนั้น คุณจะสร้างอันใหม่

```java
GradientOverlayEffect gradientOverlayEffect = null;
for (ILayerEffect effect : layerBlendOptions.getEffects()) {
    if (effect instanceof GradientOverlayEffect) {
        gradientOverlayEffect = (GradientOverlayEffect) effect;
        break;
    }
}

if (gradientOverlayEffect == null) {
    // สร้าง GradientOverlayEffect ใหม่หากไม่มีอยู่
    gradientOverlayEffect = layerBlendOptions.addGradientOverlay();
}
```

 คำอธิบาย: บล็อกของโค้ดนี้จะวนซ้ำเอฟเฟกต์ทั้งหมดที่ใช้กับเลเยอร์ โดยค้นหา a`GradientOverlayEffect` - ถ้าเจอก็เยี่ยมเลย! คุณสามารถดำเนินการแก้ไขต่อไปได้ ถ้าไม่เช่นนั้น คุณจะสร้างเอฟเฟกต์การไล่ระดับสีใหม่โดยใช้`addGradientOverlay()` วิธี. ความยืดหยุ่นนี้ช่วยให้มั่นใจได้ว่าโค้ดของคุณสามารถจัดการกับทั้งสองสถานการณ์ได้ ไม่ว่าจะเป็นการแก้ไขเอฟเฟกต์ที่มีอยู่หรือเพิ่มเอฟเฟกต์ใหม่

## ขั้นตอนที่ 4: แก้ไขเอฟเฟกต์การไล่ระดับสีแบบไล่ระดับสี

ตอนนี้มาถึงส่วนที่สนุกแล้ว—การปรับแต่งเอฟเฟกต์การซ้อนทับแบบไล่ระดับสี ขั้นตอนนี้เป็นขั้นตอนที่คุณสามารถใช้สร้างสรรค์ เปลี่ยนความทึบ โหมดผสมผสาน สีไล่ระดับสี และอื่นๆ อีกมากมาย

### ตั้งค่าความทึบและโหมดผสมผสาน

```java
gradientOverlayEffect.setOpacity((byte) 200);
gradientOverlayEffect.setBlendMode(BlendMode.Hue);
```

คำอธิบาย: ที่นี่ เรากำลังตั้งค่าความทึบของการซ้อนทับแบบไล่ระดับสีเป็น 200 (ในระดับตั้งแต่ 0 ถึง 255) และเปลี่ยนโหมดการผสมผสานเป็น`Hue`- โหมดผสมผสานจะกำหนดว่าการไล่ระดับสีจะโต้ตอบกับเนื้อหาที่มีอยู่ของเลเยอร์อย่างไร

### ปรับแต่งสีและการตั้งค่าการไล่ระดับสี

```java
GradientFillSettings settings = gradientOverlayEffect.getSettings();
settings.setColorPoints(new IGradientColorPoint[]{
        new GradientColorPoint(Color.getGreenYellow(), 0, 50),
        new GradientColorPoint(Color.getBlueViolet(), 4096, 50),
});
settings.setAngle(80);
settings.setScale(150);
settings.setGradientType(GradientType.Linear);
settings.getTransparencyPoints()[0].setOpacity(100);
settings.getTransparencyPoints()[1].setOpacity(100);
```

 คำอธิบาย :`GradientFillSettings` วัตถุช่วยให้คุณสามารถกำหนดค่าเฉพาะของการไล่ระดับสีได้ เรากำลังตั้งค่าจุดสีสองจุดสำหรับการไล่ระดับสี ได้แก่ สีเขียว-เหลืองที่จุดเริ่มต้น และสีน้ำเงิน-ม่วงที่จุดสิ้นสุด การไล่ระดับสีถูกกำหนดให้เป็นประเภทเส้นตรงที่มีสเกล 150% และมุม 80 องศา ซึ่งกำหนดทิศทางของการไล่ระดับสี นอกจากนี้ เรายังรับประกันว่าการไล่ระดับสีมีความทึบโดยการตั้งค่าความทึบของแต่ละจุดโปร่งใสเป็น 100%

## ขั้นตอนที่ 5: บันทึกไฟล์ PSD ที่แก้ไข

เมื่อแก้ไขเรียบร้อยแล้ว ขั้นตอนสุดท้ายคือบันทึกงานของคุณ เพื่อให้แน่ใจว่าการเปลี่ยนแปลงของคุณจะถูกเขียนลงในไฟล์ และคุณสามารถใช้หรือแชร์ PSD ที่คุณกำหนดเองใหม่ได้

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "psdnet256.psd_output.psd";

psdImage.save(outPsdFilePath);
psdImage.dispose();
```

คำอธิบาย: ไฟล์ PSD ที่แก้ไขจะถูกบันทึกด้วยชื่อใหม่ไปยังไดเร็กทอรีเอาต์พุตที่ระบุ ในที่สุด.`dispose()` วิธีการนี้ถูกเรียกให้ปล่อยทรัพยากรใด ๆ ที่ใช้โดย`PsdImage` วัตถุ. นี่เป็นแนวปฏิบัติที่ดีเพื่อให้แน่ใจว่าแอปพลิเคชันของคุณทำงานอย่างมีประสิทธิภาพและไม่กินทรัพยากรที่ไม่จำเป็น

## บทสรุป

และคุณก็ได้แล้ว! คุณได้แก้ไขเอฟเฟกต์การไล่ระดับสีแบบไล่ระดับสีในไฟล์ PSD สำเร็จแล้วโดยใช้ Aspose.PSD สำหรับ Java บทช่วยสอนนี้จะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การโหลดไฟล์ PSD ไปจนถึงการใช้การไล่ระดับสีใหม่และบันทึกงานของคุณ ด้วยการทำตามขั้นตอนเหล่านี้ คุณได้ปลดล็อกวิธีที่มีประสิทธิภาพในการทำงานและปรับแต่งงานการออกแบบกราฟิกของคุณโดยอัตโนมัติโดยทางโปรแกรม

## คำถามที่พบบ่อย

### ฉันสามารถใช้การซ้อนทับแบบไล่ระดับสีหลายชั้นกับเลเยอร์เดียวได้หรือไม่  
 ได้ คุณสามารถใช้การซ้อนทับแบบไล่ระดับสีหลายรายการในเลเยอร์เดียวได้โดยการเพิ่มใหม่`GradientOverlayEffect` อินสแตนซ์ของตัวเลือกการผสมของเลเยอร์

### เป็นไปได้ไหมที่จะลบเอฟเฟกต์การไล่ระดับสีออกจากเลเยอร์?  
อย่างแน่นอน! คุณสามารถลบเอฟเฟกต์การไล่ระดับสีที่มีอยู่ได้โดยการลบเอฟเฟกต์ที่เกี่ยวข้องออกจากตัวเลือกการผสมของเลเยอร์

### ฉันสามารถใช้เอฟเฟกต์อื่นใดอีกได้บ้างโดยใช้ Aspose.PSD สำหรับ Java  
Aspose.PSD สำหรับ Java ช่วยให้คุณสามารถใช้เอฟเฟ็กต์ต่างๆ ได้ เช่น เงาตกกระทบ แสงด้านใน แสงด้านนอก และอื่นๆ อีกมากมาย คุณสามารถปรับแต่งเอฟเฟ็กต์แต่ละอย่างให้เหมาะกับความต้องการของคุณได้

### ฉันจะคืนค่าการเปลี่ยนแปลงที่ทำกับไฟล์ PSD ได้อย่างไร  
หากคุณยังไม่ได้บันทึกไฟล์ คุณสามารถโหลดไฟล์ PSD ต้นฉบับซ้ำได้ หากคุณได้บันทึกไว้แล้ว คุณจะต้องกู้คืนจากข้อมูลสำรองหรือเลิกทำการเปลี่ยนแปลงโดยทางโปรแกรม
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
