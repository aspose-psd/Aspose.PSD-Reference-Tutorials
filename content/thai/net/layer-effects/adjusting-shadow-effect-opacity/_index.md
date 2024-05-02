---
title: การปรับความทึบของเอฟเฟกต์เงาใน Aspose.PSD สำหรับ .NET
linktitle: การปรับความทึบของเอฟเฟกต์เงา
second_title: Aspose.PSD .NET API
description: เรียนรู้วิธีปรับความทึบของเอฟเฟกต์เงาใน Aspose.PSD สำหรับ .NET ด้วยบทช่วยสอนที่ครอบคลุมนี้
type: docs
weight: 15
url: /th/net/layer-effects/adjusting-shadow-effect-opacity/
---
## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนในการปรับความทึบของเอฟเฟกต์เงาใน Aspose.PSD สำหรับ .NET! ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการใช้คุณสมบัติ Opacity ของ DropShadowEffect Aspose.PSD สำหรับ .NET เป็นไลบรารีอันทรงพลังที่ช่วยให้คุณทำงานกับไฟล์ PSD ในแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

-  Aspose.PSD สำหรับไลบรารี .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD สำหรับ .NET ในโปรเจ็กต์ของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/net/).

- ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีสำหรับไฟล์ PSD อินพุตของคุณ

- Output Directory: สร้างไดเร็กทอรีที่จะบันทึกภาพที่ได้

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

 เริ่มต้นด้วยการโหลดไฟล์ PSD ของคุณโดยใช้นามสกุล`Image.Load` วิธี:

```csharp
string inputFile = Path.Combine(baseDir, "input.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    // รหัสของคุณสำหรับการประมวลผลเพิ่มเติมอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: เข้าถึงเลเยอร์และเพิ่มเอฟเฟกต์ Drop Shadow

ดึงเลเยอร์ที่ต้องการจากไฟล์ PSD และเพิ่มเอฟเฟกต์เงา:

```csharp
Layer workLayer = psdImage.Layers[1];
DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
dropShadowEffect.Distance = 0;
dropShadowEffect.Size = 8;
```

## ขั้นตอนที่ 3: ปรับความทึบและบันทึกรูปภาพ

ตอนนี้ ให้ปรับคุณสมบัติความทึบและบันทึกภาพที่มีความทึบต่างกัน:

```csharp
// ตัวอย่างที่มีความทึบ = 20
dropShadowEffect.Opacity = 20;
psdImage.Save(outputImage20, new PngOptions());

// ตัวอย่างที่มีความทึบ = 200
dropShadowEffect.Opacity = 200;
psdImage.Save(outputImage200, new PngOptions());
```

## ขั้นตอนที่ 4: ทำความสะอาด

หลังจากบันทึกภาพแล้ว ให้ล้างข้อมูลโดยการลบไฟล์ชั่วคราว:

```csharp
File.Delete(outputImage20);
File.Delete(outputImage200);
```

## บทสรุป

ยินดีด้วย! คุณได้ปรับความทึบของเอฟเฟกต์เงาใน Aspose.PSD สำหรับ .NET เรียบร้อยแล้ว บทช่วยสอนนี้ให้คำแนะนำที่ตรงไปตรงมาในการปรับปรุงรูปภาพ PSD ของคุณด้วยความทึบของเงาที่แตกต่างกัน

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้บทช่วยสอนนี้กับรูปแบบภาพอื่นได้หรือไม่

A1: ไม่ บทช่วยสอนนี้ครอบคลุมถึงการปรับความทึบของเอฟเฟกต์เงาในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ .NET โดยเฉพาะ

### คำถามที่ 2: มีคุณสมบัติเงาเพิ่มเติมที่สามารถแก้ไขได้หรือไม่

A2: ใช่ Aspose.PSD สำหรับ .NET มีคุณสมบัติต่างๆ สำหรับการปรับแต่งเอฟเฟ็กต์เงาอย่างละเอียด

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A3: คุณสามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 4: Aspose.PSD สำหรับ .NET เข้ากันได้กับ .NET Core หรือไม่

A4: ใช่ Aspose.PSD สำหรับ .NET เข้ากันได้กับทั้ง .NET Framework และ .NET Core

### คำถามที่ 5: ฉันจะหาการสนับสนุนชุมชนสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A5: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการอภิปรายของชุมชน