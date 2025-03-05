---
title: การเพิ่มเลเยอร์ Stroke ด้วยรูปแบบใน Aspose.PSD สำหรับ .NET
linktitle: การเพิ่มเลเยอร์ Stroke ด้วย Pattern
second_title: Aspose.PSD .NET API
description: ปรับปรุงไฟล์ PSD ของคุณด้วยเลเยอร์เส้นขีดและรูปแบบโดยใช้ Aspose.PSD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
type: docs
weight: 13
url: /th/net/layer-effects/adding-stroke-layer-pattern/
---
## การแนะนำ

การปรับปรุงไฟล์ PSD (เอกสาร Photoshop) ด้วยเลเยอร์เส้นขีดและรูปแบบจะช่วยเพิ่มไดนามิกให้กับการออกแบบของคุณได้ ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ประโยชน์จาก Aspose.PSD สำหรับ .NET เพื่อเพิ่มเลเยอร์เส้นขีดที่มีรูปแบบให้กับไฟล์ PSD ของคุณได้อย่างง่ายดาย Aspose.PSD เป็นไลบรารี .NET ที่ทรงพลังซึ่งให้การสนับสนุนที่ครอบคลุมสำหรับการจัดการไฟล์ PSD ทำให้เป็นเครื่องมืออันล้ำค่าสำหรับนักพัฒนาและนักออกแบบ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
- ติดตั้ง Visual Studio บนเครื่องของคุณแล้ว
-  Aspose.PSD สำหรับไลบรารี .NET ซึ่งคุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/net/).

## นำเข้าเนมสเปซ

ตรวจสอบให้แน่ใจว่าคุณนำเข้าเนมสเปซที่จำเป็นในรหัส C# ของคุณ:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อมของคุณ

เริ่มต้นด้วยการกำหนดไดเร็กทอรีต้นทางและเอาต์พุตในโค้ด C# ของคุณ:

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

โหลดไฟล์ PSD โดยใช้คลาส PsdImage ของ Aspose.PSD:

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // รหัสของคุณสำหรับการประมวลผลไฟล์ PSD อยู่ที่นี่
}
```

## ขั้นตอนที่ 3: เตรียมข้อมูลรูปแบบใหม่

กำหนดรูปแบบใหม่และขอบเขต:

```csharp
var newPattern = new int[]
{
    // สีลวดลายของคุณอยู่ที่นี่
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## ขั้นตอนที่ 4: แก้ไขเลเยอร์ Stroke

เข้าถึงเลเยอร์เส้นขีดและอัพเดตคุณสมบัติ:

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

// ตรวจสอบและอัพเดตคุณสมบัติของเส้นขีด
// -

// อัปเดตความทึบและโหมดผสมผสาน
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## ขั้นตอนที่ 5: อัปเดตข้อมูลรูปแบบ

อัปเดตข้อมูลรูปแบบในไฟล์ PSD:

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        // รหัสของคุณสำหรับการอัปเดตข้อมูลรูปแบบอยู่ที่นี่
    }
}

// บันทึกไฟล์ PSD ที่แก้ไข
im.Save(exportPath);
```

## ขั้นตอนที่ 6: ตรวจสอบการเปลี่ยนแปลง

โหลดไฟล์ PSD ที่แก้ไขแล้วและตรวจสอบการเปลี่ยนแปลง:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    // รหัสของคุณสำหรับการตรวจสอบการเปลี่ยนแปลงอยู่ที่นี่
}
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มเลเยอร์เส้นขีดด้วยรูปแบบใน Aspose.PSD สำหรับ .NET เรียบร้อยแล้ว ไลบรารีอเนกประสงค์นี้ช่วยให้นักพัฒนาสามารถสร้างการออกแบบที่ดึงดูดสายตาและเพิ่มความยืดหยุ่นของไฟล์ PSD

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD สำหรับ .NET กับ Visual Studio เวอร์ชันใดก็ได้ได้หรือไม่

A1: ใช่ Aspose.PSD สำหรับ .NET เข้ากันได้กับ Visual Studio เวอร์ชันต่างๆ

### คำถามที่ 2: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A2: เยี่ยมเลย[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อขอรับใบอนุญาตชั่วคราว

### คำถามที่ 3: มีไฟล์ PSD ตัวอย่างสำหรับการทดสอบหรือไม่

 A3: คุณสามารถค้นหาไฟล์ PSD ตัวอย่างได้ในเอกสารประกอบ[ที่นี่](https://reference.aspose.com/psd/net/).

### คำถามที่ 4: Aspose.PSD เหมาะสำหรับการประมวลผลไฟล์ PSD เป็นชุดหรือไม่

A4: แน่นอน Aspose.PSD สำหรับ .NET ให้การสนับสนุนที่มีประสิทธิภาพสำหรับการประมวลผลแบบแบตช์

### คำถามที่ 5: ฉันสามารถขอความช่วยเหลือหรือมีส่วนร่วมในการอภิปรายของชุมชนได้ที่ไหน?

 A5: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการมีปฏิสัมพันธ์กับชุมชน