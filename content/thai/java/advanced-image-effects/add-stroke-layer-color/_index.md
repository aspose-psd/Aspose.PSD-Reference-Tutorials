---
title: เพิ่มสีเลเยอร์ Stroke ใน Aspose.PSD สำหรับ Java
linktitle: เพิ่มสีเลเยอร์เส้นขีด
second_title: Aspose.PSD Java API
description: สำรวจพลังของ Aspose.PSD สำหรับ Java ด้วยคำแนะนำทีละขั้นตอนในการเพิ่มสีเลเยอร์เส้นโครงร่าง ยกระดับการออกแบบกราฟิกของคุณได้อย่างง่ายดาย
type: docs
weight: 14
url: /th/java/advanced-image-effects/add-stroke-layer-color/
---
## การแนะนำ

ปลดล็อกศักยภาพของการออกแบบกราฟิกของแอปพลิเคชัน Java ของคุณด้วย Aspose.PSD ในบทช่วยสอนนี้ เราจะเจาะลึกโลกอันน่าทึ่งของการเพิ่มสีเลเยอร์เส้นโครงร่างโดยใช้ Aspose.PSD สำหรับ Java ปรับปรุงกราฟิกของคุณด้วยลายเส้นที่โดดเด่น สร้างการออกแบบที่ดึงดูดสายตาได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเริ่มต้นการเดินทางที่สร้างสรรค์นี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose.PSD: ดาวน์โหลดและตั้งค่าไลบรารี Aspose.PSD โดยทำตาม[เอกสารประกอบ](https://reference.aspose.com/psd/java/).

- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว

- สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก IDE ตามที่คุณต้องการ Eclipse หรือ IntelliJ เป็นตัวเลือกยอดนิยม

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นเพื่อทำให้ความมหัศจรรย์ของ Aspose.PSD เกิดขึ้น

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

เริ่มต้นด้วยการสร้างโปรเจ็กต์ Java ใหม่ใน IDE ที่คุณต้องการ ตรวจสอบให้แน่ใจว่าได้เพิ่มไลบรารี Aspose.PSD ให้กับโปรเจ็กต์ของคุณแล้ว

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

โหลดไฟล์ PSD โดยใช้ Aspose.PSD เพื่อให้สามารถโหลดทรัพยากรเอฟเฟกต์ได้

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## ขั้นตอนที่ 3: เข้าถึงเลเยอร์ Stroke

เข้าถึงเลเยอร์เอฟเฟกต์เส้นขีดภายในไฟล์ PSD

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## ขั้นตอนที่ 4: ตรวจสอบคุณสมบัติของโรคหลอดเลือดสมอง

ตรวจสอบให้แน่ใจว่าคุณสมบัติของสโตรคเป็นไปตามที่คาดไว้

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## ขั้นตอนที่ 5: ตั้งค่าสีและความทึบ

แก้ไขสีและความทึบของเลเยอร์เส้นขีด

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## ขั้นตอนที่ 6: บันทึก PSD ที่แก้ไขแล้ว

บันทึกไฟล์ PSD ที่แก้ไขด้วยสีเลเยอร์เส้นขีดที่เพิ่มใหม่

```java
im.save(exportPath);
```

## บทสรุป

ยินดีด้วย! คุณได้เพิ่มสีเลเยอร์เส้นขีดลงในไฟล์ PSD ของคุณสำเร็จแล้วโดยใช้ Aspose.PSD สำหรับ Java ทดลองใช้สีและการตั้งค่าต่างๆ เพื่อทำให้การออกแบบกราฟิกของคุณมีชีวิตชีวา

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD กับไลบรารีกราฟิก Java อื่นๆ ได้หรือไม่

ตอบ 1: ได้ Aspose.PSD สามารถรวมเข้ากับไลบรารีกราฟิก Java อื่นๆ ได้เพื่อเพิ่มฟังก์ชันการทำงาน

### คำถามที่ 2: Aspose.PSD เข้ากันได้กับรูปแบบไฟล์ PSD ล่าสุดหรือไม่

A2: แน่นอน! Aspose.PSD ก้าวตามข้อกำหนดรูปแบบไฟล์ PSD ล่าสุด จึงมั่นใจได้ถึงความเข้ากันได้

### คำถามที่ 3: ฉันจะจัดการข้อยกเว้นขณะใช้ Aspose.PSD ได้อย่างไร

 A3: โปรดดูที่[ฟอรั่มการสนับสนุน](https://forum.aspose.com/c/psd/34) เพื่อขอความช่วยเหลือในการจัดการข้อยกเว้นและการแก้ไขปัญหา

### คำถามที่ 4: ฉันสามารถลองใช้ Aspose.PSD ก่อนซื้อได้หรือไม่

 A4: แน่นอน! คว้าก[ทดลองฟรี](https://releases.aspose.com/) เพื่อสำรวจคุณสมบัติของ Aspose.PSD ก่อนตัดสินใจ

### คำถามที่ 5: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้ที่ไหน

 A5: ได้รับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) สำหรับ Aspose.PSD เพื่อประเมินความสามารถในโครงการของคุณ