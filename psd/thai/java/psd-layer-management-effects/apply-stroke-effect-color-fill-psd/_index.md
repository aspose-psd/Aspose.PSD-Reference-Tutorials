---
title: ใช้เอฟเฟกต์ Stroke พร้อมเติมสีใน PSD - Java
linktitle: ใช้เอฟเฟกต์ Stroke พร้อมเติมสีใน PSD - Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีใช้เอฟเฟกต์เส้นโครงร่างด้วยการเติมสีลงในไฟล์ PSD ของคุณโดยใช้ Aspose.PSD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนนี้เพื่อปรับปรุงภาพของคุณได้อย่างง่ายดาย
weight: 21
url: /th/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ใช้เอฟเฟกต์ Stroke พร้อมเติมสีใน PSD - Java

## การแนะนำ

ในคู่มือนี้ เราจะแนะนำคุณตลอดขั้นตอนการใช้เอฟเฟกต์เส้นขีดพร้อมการเติมสีให้กับไฟล์ PSD ของคุณโดยใช้ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น บทช่วยสอนทีละขั้นตอนนี้จะช่วยให้คุณทำงานให้สำเร็จได้อย่างง่ายดาย เราจะครอบคลุมทุกอย่างตั้งแต่การตั้งค่าสภาพแวดล้อมของคุณไปจนถึงการบันทึกภาพสุดท้ายด้วยเอฟเฟกต์ที่ใช้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่จำเป็นในการปฏิบัติตามพร้อมกับบทช่วยสอนนี้:

1. ติดตั้ง Java Development Kit (JDK) แล้ว: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK 8 หรือสูงกว่าในระบบของคุณ
2.  Aspose.PSD สำหรับไลบรารี Java: คุณจะต้องมี Aspose.PSD สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): IDE เช่น IntelliJ IDEA, Eclipse หรืออื่นๆ ที่คุณเลือก
4. ไฟล์ PSD ตัวอย่าง: ไฟล์ PSD ตัวอย่างที่คุณสามารถใช้เอฟเฟกต์เส้นขีดได้ หากคุณยังไม่มี คุณสามารถสร้างไฟล์ PSD ง่ายๆ ใน Photoshop หรือดาวน์โหลดไฟล์จากอินเทอร์เน็ต
5. ความรู้พื้นฐานของ Java: แม้ว่าบทช่วยสอนนี้เหมาะสำหรับผู้เริ่มต้น แต่การมีความรู้พื้นฐานเกี่ยวกับ Java บ้างก็จะเป็นประโยชน์

เมื่อคุณมีข้อกำหนดเบื้องต้นเหล่านี้แล้ว คุณก็พร้อมที่จะเริ่มใช้เอฟเฟกต์เส้นขีดพร้อมสีเติมลงในไฟล์ PSD ของคุณ

## แพ็คเกจนำเข้า

หากต้องการเริ่มทำงานกับ Aspose.PSD สำหรับ Java คุณจะต้องนำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

การนำเข้าเหล่านี้นำคลาสที่จำเป็นทั้งหมดที่คุณต้องใช้เพื่อทำงานกับไฟล์ PSD ใส่เอฟเฟกต์ และบันทึกรูปภาพในรูปแบบที่คุณต้องการ

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

 ขั้นตอนแรกในกระบวนการของเราคือการโหลดไฟล์ PSD ที่คุณต้องการแก้ไข Aspose.PSD สำหรับ Java ทำให้สิ่งนี้ง่ายอย่างเหลือเชื่อด้วย`PsdImage` ระดับ. ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

### 1.1 กำหนดเส้นทางไดเรกทอรี

ขั้นแรก ให้กำหนดเส้นทางไดเร็กทอรีที่เก็บไฟล์ PSD ของคุณ:

```java
String dataDir = "Your Document Directory";
```

 แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงที่มีไฟล์ PSD ของคุณอยู่

### 1.2 โหลดรูปภาพ PSD

 ตอนนี้ให้โหลดไฟล์ PSD โดยใช้นามสกุล`PsdLoadOptions` และ`PsdImage` ชั้นเรียน:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 นี่.`PsdLoadOptions`ได้รับการกำหนดค่าให้โหลดทรัพยากรเอฟเฟกต์ เพื่อให้มั่นใจว่าสามารถเข้าถึงเอฟเฟกต์ที่มีอยู่ใน PSD ได้

## ขั้นตอนที่ 2: ใช้เอฟเฟกต์เส้นขีดด้วยการเติมสี

เมื่อโหลดไฟล์ PSD แล้ว ขั้นตอนต่อไปคือการใช้เอฟเฟกต์เส้นขีดกับเลเยอร์ของรูปภาพ นี่คือจุดที่ความมหัศจรรย์ที่แท้จริงเกิดขึ้น

ไฟล์ PSD แต่ละไฟล์อาจมีหลายเลเยอร์ และคุณจะต้องใส่เอฟเฟกต์กับแต่ละเลเยอร์ ต่อไปนี้เป็นวิธีดำเนินการ:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

ในวงนี้:

- `im.getLayers()`: ดึงเลเยอร์ทั้งหมดในไฟล์ PSD
- `StrokeEffect effect`: แยกเอฟเฟกต์เส้นขีดที่ใช้กับเลเยอร์
- `ColorFillSettings settings`: แก้ไขการตั้งค่าการเติมสำหรับเอฟเฟ็กต์เส้นขีด
- `settings.setColor(Color.getDeepPink())`: ตั้งค่าสีเส้นโครงร่างเป็นสีชมพูเข้ม คุณสามารถเปลี่ยนเป็นสีใดก็ได้ที่คุณต้องการ

## ขั้นตอนที่ 3: บันทึก PSD ที่แก้ไขแล้วส่งออกเป็น PNG

เมื่อคุณใช้เอฟเฟกต์เส้นโครงร่างแล้ว ก็ถึงเวลาบันทึกการเปลี่ยนแปลงและส่งออกรูปภาพ

### 3.1 บันทึกไฟล์ PSD

หากต้องการบันทึกไฟล์ PSD ที่แก้ไข ให้ใช้รหัสต่อไปนี้:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

วิธีนี้จะบันทึกไฟล์โดยใช้เอฟเฟกต์เส้นขีดที่นำไปใช้กับเส้นทางที่ระบุ

### 3.2 ส่งออกเป็น PNG

เพื่อให้เข้าถึงรูปภาพได้มากขึ้น คุณอาจต้องการส่งออกเป็นไฟล์ PNG มีวิธีดังนี้:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

ข้อมูลโค้ดนี้จะบันทึกรูปภาพเป็น PNG โดยมีสีจริงและความโปร่งใสของอัลฟ่า ทำให้พร้อมสำหรับการใช้งานในแอปพลิเคชันบนเว็บหรือแพลตฟอร์มอื่นๆ

## บทสรุป

การใช้เอฟเฟกต์เส้นโครงร่างด้วยการเติมสีลงในไฟล์ PSD ของคุณโดยใช้ Aspose.PSD สำหรับ Java ไม่เพียงตรงไปตรงมา แต่ยังทรงพลังอย่างเหลือเชื่ออีกด้วย ด้วยโค้ดเพียงไม่กี่บรรทัด คุณสามารถทำงานประมวลผลภาพที่ซับซ้อนได้โดยอัตโนมัติ ซึ่งช่วยประหยัดทั้งเวลาและความพยายาม

ไม่ว่าคุณจะทำงานกับรูปภาพจำนวนมากหรือเพียงแค่ต้องปรับแต่งไฟล์เพียงไม่กี่ไฟล์ วิธีการนี้ก็มอบโซลูชันที่ยืดหยุ่นและมีประสิทธิภาพ เมื่อคุณมีพื้นฐานแล้ว คุณสามารถเริ่มทดลองใช้เอฟเฟกต์และการปรับแต่งต่างๆ เพื่อทำให้ภาพของคุณโดดเด่นอย่างแท้จริง

พร้อมที่จะลองหรือยัง? หยิบไฟล์ PSD ตัวอย่างของคุณแล้วเริ่มเพิ่มเอฟเฟกต์อันน่าทึ่งได้แล้ววันนี้!

## คำถามที่พบบ่อย

### ฉันสามารถใช้เอฟเฟกต์หลายรายการกับเลเยอร์เดียวโดยใช้ Aspose.PSD สำหรับ Java ได้หรือไม่
ใช่ คุณสามารถใช้เอฟเฟ็กต์หลายรายการในเลเยอร์เดียวได้โดยเข้าถึงตัวเลือกการผสมของเลเยอร์และเพิ่มเอฟเฟกต์ที่ต้องการ

### เป็นไปได้ไหมที่จะทำให้กระบวนการสำหรับไฟล์ PSD ชุดหนึ่งเป็นแบบอัตโนมัติ?
อย่างแน่นอน! คุณสามารถวนซ้ำไดเร็กทอรีของไฟล์ PSD ใช้เอฟเฟกต์เส้นขีด และบันทึกผลลัพธ์โดยอัตโนมัติ

### ฉันจะคืนค่าการเปลี่ยนแปลงที่ทำกับไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ได้อย่างไร
หากต้องการคืนค่าการเปลี่ยนแปลง คุณจะต้องโหลดไฟล์ PSD ต้นฉบับซ้ำก่อนที่จะบันทึกการแก้ไขใดๆ ไม่มีคุณลักษณะการเลิกทำโดยตรงใน Aspose.PSD

### ฉันสามารถปรับแต่งความกว้างและตำแหน่งของเส้นขีดได้หรือไม่?
 ใช่ Aspose.PSD สำหรับ Java อนุญาตให้คุณปรับแต่งความกว้างของเส้นขีด ตำแหน่ง และคุณสมบัติอื่นๆ ผ่านทาง`StrokeEffect` ระดับ.

### Aspose.PSD สำหรับไลบรารี Java ใช้งานได้ฟรีหรือไม่
 Aspose.PSD สำหรับ Java ให้ทดลองใช้ฟรี แต่หากต้องการเข้าถึงคุณสมบัติทั้งหมดอย่างเต็มรูปแบบ คุณจะต้องซื้อใบอนุญาต คุณสามารถสำรวจ[ซื้อตัวเลือก](https://purchase.aspose.com/buy)บนเว็บไซต์ของพวกเขา
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
