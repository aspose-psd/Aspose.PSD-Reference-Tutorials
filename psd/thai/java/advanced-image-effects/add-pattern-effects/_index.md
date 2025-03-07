---
title: เพิ่มเอฟเฟกต์รูปแบบใน Aspose.PSD สำหรับ Java
linktitle: เพิ่มเอฟเฟ็กต์รูปแบบ
second_title: Aspose.PSD Java API
description: ปรับปรุงรูปแบบภาพ Java ของคุณได้อย่างง่ายดายด้วย Aspose.PSD สำหรับ Java ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเราเพื่อเพิ่มเอฟเฟกต์รูปแบบที่น่าดึงดูด
weight: 12
url: /th/java/advanced-image-effects/add-pattern-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มเอฟเฟกต์รูปแบบใน Aspose.PSD สำหรับ Java

## การแนะนำ

ในโลกของการพัฒนา Java การปรับปรุงรูปแบบภาพเป็นงานทั่วไป และ Aspose.PSD สำหรับ Java มอบโซลูชันที่มีประสิทธิภาพสำหรับสิ่งนี้ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการเพิ่มเอฟเฟกต์รูปแบบโดยใช้ Aspose.PSD เพื่อให้มั่นใจว่ารูปภาพของคุณโดดเด่นด้วยการซ้อนทับและการปรับปรุงที่เป็นเอกลักษณ์

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
-  Aspose.PSD สำหรับไลบรารี Java ที่ดาวน์โหลดและเพิ่มลงในโปรเจ็กต์ของคุณ คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ Aspose.PSD](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นสำหรับการทำงานกับ Aspose.PSD รวมโค้ดต่อไปนี้ไว้ที่จุดเริ่มต้นของคลาส Java ของคุณ:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ

```java
// โหลดรูปภาพ PSD
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "YourImagePath" และ "YourExportPath" ด้วยเส้นทางจริงในโครงการของคุณ

## ขั้นตอนที่ 2: แยกข้อมูลการซ้อนทับรูปแบบ

```java
// แยกข้อมูลเกี่ยวกับการซ้อนทับรูปแบบ
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## ขั้นตอนที่ 3: แก้ไขการตั้งค่าการซ้อนทับรูปแบบ

```java
// แก้ไขการตั้งค่าการซ้อนทับรูปแบบ
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## ขั้นตอนที่ 4: แก้ไขข้อมูลรูปแบบ

```java
// แก้ไขข้อมูลรูปแบบ
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## ขั้นตอนที่ 5: บันทึกรูปภาพที่แก้ไข

```java
// บันทึกภาพที่แก้ไข
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## ขั้นตอนที่ 6: ตรวจสอบการเปลี่ยนแปลง

```java
// ตรวจสอบการเปลี่ยนแปลงในไฟล์ที่แก้ไข
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// เพิ่มการยืนยันเพื่อให้แน่ใจว่าการเปลี่ยนแปลงมีผลสำเร็จ
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มเอฟเฟกต์รูปแบบโดยใช้ Aspose.PSD สำหรับ Java เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้ช่วยให้คุณสร้างรูปภาพที่ดึงดูดสายตาด้วยรูปแบบที่กำหนดเอง มอบความเป็นไปได้ที่ไม่มีที่สิ้นสุดสำหรับโปรเจ็กต์ที่ใช้ Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD สำหรับ Java กับไลบรารีการประมวลผลรูปภาพ Java อื่นๆ ได้หรือไม่

คำตอบ 1: Aspose.PSD สำหรับ Java ได้รับการออกแบบมาให้ทำงานแยกจากกัน แต่คุณสามารถรวมเข้ากับไลบรารี Java อื่นๆ ได้หากจำเป็น

### คำถามที่ 2: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A2: โปรดดูที่[Aspose.PSD สำหรับเอกสาร Java](https://reference.aspose.com/psd/java/) เพื่อข้อมูลที่ครบถ้วน

### คำถามที่ 3: Aspose.PSD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A4: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนจากชุมชนหรือพิจารณาซื้อแผนการสนับสนุน

### คำถามที่ 5: ฉันสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ Java ได้หรือไม่

A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
