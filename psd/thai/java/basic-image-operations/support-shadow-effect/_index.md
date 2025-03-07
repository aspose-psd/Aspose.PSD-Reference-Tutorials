---
title: รองรับ Shadow Effect ใน Aspose.PSD สำหรับ Java
linktitle: สนับสนุนเอฟเฟกต์เงา
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มเอฟเฟกต์เงาที่น่าดึงดูดให้กับรูปภาพโดยใช้ Aspose.PSD สำหรับ Java ยกระดับการออกแบบกราฟิกของคุณด้วยบทช่วยสอนทีละขั้นตอนนี้
weight: 13
url: /th/java/basic-image-operations/support-shadow-effect/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับ Shadow Effect ใน Aspose.PSD สำหรับ Java

## การแนะนำ

การปรับปรุงภาพด้วยเอฟเฟ็กต์เงาถือเป็นเรื่องปกติในการออกแบบกราฟิก โดยการเพิ่มความลึกและความสมจริง Aspose.PSD สำหรับ Java ให้การสนับสนุนเอฟเฟกต์เงาอย่างแข็งแกร่ง ช่วยให้นักพัฒนาสามารถรวมเอฟเฟกต์เหล่านี้เข้ากับแอปพลิเคชัน Java ของตนได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะสำรวจวิธีการรองรับเอฟเฟกต์เงาโดยใช้ Aspose.PSD ทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ติดตั้ง Aspose.PSD สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ตรวจสอบให้แน่ใจว่าคุณได้นำเข้าแพ็คเกจที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชัน Aspose.PSD ในแอปพลิเคชัน Java ของคุณ ใช้ข้อมูลโค้ดต่อไปนี้เป็นแนวทาง:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## ขั้นตอนที่ 2: ดึงเอฟเฟกต์เงา

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## ขั้นตอนที่ 3: ตรวจสอบการตั้งค่าเริ่มต้น

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## ขั้นตอนที่ 4: ปรับแต่งเอฟเฟกต์เงา

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## ขั้นตอนที่ 5: บันทึกรูปภาพที่แก้ไข

```java
im.save(psdPathAfterChange);
```

## บทสรุป

ด้วยขั้นตอนง่ายๆ เหล่านี้ คุณจะสามารถรองรับเอฟเฟกต์เงาใน Aspose.PSD สำหรับ Java ได้อย่างง่ายดาย ซึ่งช่วยเพิ่มความน่าดึงดูดให้กับรูปภาพของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ Java เหมาะสำหรับโครงการออกแบบกราฟิกระดับมืออาชีพหรือไม่

A1: แน่นอน! Aspose.PSD สำหรับ Java เป็นไลบรารีอันทรงพลังที่ออกแบบมาสำหรับงานออกแบบกราฟิกระดับมืออาชีพ

### คำถามที่ 2: ฉันสามารถใช้ Aspose.PSD สำหรับ Java ในแอปพลิเคชันเชิงพาณิชย์ได้หรือไม่

 ตอบ 2: ใช่ Aspose.PSD สำหรับ Java เป็นผลิตภัณฑ์เชิงพาณิชย์ คุณสามารถซื้อได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ได้ คุณสามารถทดลองใช้เวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### Q4: ฉันจะหาเอกสารโดยละเอียดได้จากที่ไหน?

 A4: โปรดดูเอกสารประกอบที่ครอบคลุม[ที่นี่](https://reference.aspose.com/psd/java/).

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A5: เข้าร่วมฟอรั่มชุมชน[ที่นี่](https://forum.aspose.com/c/psd/34) สำหรับข้อสงสัยการสนับสนุนใด ๆ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
