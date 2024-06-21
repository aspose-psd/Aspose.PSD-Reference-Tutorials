---
title: การเพิ่มเลเยอร์ Stroke ด้วยสีทึบใน Aspose.PSD สำหรับ .NET
linktitle: การเพิ่มเลเยอร์ Stroke ด้วยสีทึบ
second_title: Aspose.PSD .NET API
description: เพิ่มทักษะการจัดการภาพ .NET ของคุณด้วย Aspose.PSD เรียนรู้การเพิ่มเลเยอร์เส้นโครงร่างด้วยสีทึบทีละขั้นตอน
type: docs
weight: 11
url: /th/net/layer-effects/adding-stroke-layer-solid-color/
---
## การแนะนำ

ในขอบเขตของการพัฒนา .NET การสร้างภาพที่ดึงดูดสายตาถือเป็นข้อกำหนดทั่วไป Aspose.PSD สำหรับ .NET มอบชุดเครื่องมืออันทรงพลังเพื่อจัดการและปรับปรุงรูปภาพได้อย่างราบรื่น หนึ่งในคุณสมบัติที่สำคัญคือการเพิ่มเลเยอร์เส้นโครงร่างด้วยสีทึบ ซึ่งเพิ่มความมีชีวิตชีวาและความลึกให้กับภาพของคุณ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอนโดยใช้ Aspose.PSD สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับการพัฒนา .NET
- ติดตั้ง Visual Studio บนเครื่องของคุณแล้ว
- Aspose.PSD สำหรับไลบรารี .NET คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/psd/net/).

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชันการทำงานของ Aspose.PSD สำหรับ .NET:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

เริ่มต้นด้วยการโหลดไฟล์ PSD ที่คุณต้องการปรับปรุงด้วยเลเยอร์เส้นขีด ตรวจสอบให้แน่ใจว่าคุณมีเส้นทางไฟล์ที่ถูกต้อง:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // รหัสสำหรับขั้นตอนต่อไปจะถูกเพิ่มที่นี่
}
```

## ขั้นตอนที่ 2: เข้าถึงคุณสมบัติเอฟเฟกต์จังหวะ

ดึงคุณสมบัติของเอฟเฟกต์จังหวะจากไฟล์ PSD:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## ขั้นตอนที่ 3: ปรับการตั้งค่าจังหวะ

ปรับเปลี่ยนการตั้งค่าจังหวะตามความต้องการของคุณ ในตัวอย่างนี้ เราเปลี่ยนสีเป็นสีเหลือง ตั้งค่าความทึบเป็น 127 และใช้โหมดผสมผสานสี:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## ขั้นตอนที่ 4: บันทึกภาพที่แก้ไข

บันทึกภาพหลังจากใช้การเปลี่ยนแปลงเลเยอร์จังหวะ:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## ขั้นตอนที่ 5: ตรวจสอบการเปลี่ยนแปลง

ตรวจสอบให้แน่ใจว่ามีการใช้การเปลี่ยนแปลงอย่างถูกต้องโดยการโหลดและตรวจสอบภาพที่แก้ไข:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // รหัสเพื่อยืนยันการเปลี่ยนแปลงจะถูกเพิ่มที่นี่
}
```

ทำซ้ำขั้นตอนเหล่านี้เพื่อปรับแต่งเพิ่มเติมหรือทดลองกับเอฟเฟ็กต์สโตรกต่างๆ เพื่อให้ได้เอฟเฟกต์ภาพที่ต้องการ

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มเลเยอร์เส้นขีดด้วยสีทึบโดยใช้ Aspose.PSD สำหรับ .NET เรียบร้อยแล้ว คุณสมบัติอันทรงพลังนี้เปิดโลกแห่งความเป็นไปได้ในการปรับปรุงภาพของคุณในสภาพแวดล้อม .NET

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ .NET เข้ากันได้กับเวอร์ชันเฟรมเวิร์ก .NET ล่าสุดหรือไม่

ตอบ 1: ใช่ Aspose.PSD สำหรับ .NET ได้รับการอัปเดตเป็นประจำเพื่อให้แน่ใจว่าเข้ากันได้กับเวอร์ชันเฟรมเวิร์ก .NET ล่าสุด

### คำถามที่ 2: ฉันสามารถใช้ Aspose.PSD สำหรับ .NET สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

A2: แน่นอน! Aspose.PSD สำหรับ .NET เป็นผลิตภัณฑ์เชิงพาณิชย์ และคุณสามารถใช้ในโครงการของคุณได้โดยการซื้อใบอนุญาต

### คำถามที่ 3: ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A3: สำรวจ[เอกสารประกอบ](https://reference.aspose.com/psd/net/) สำหรับตัวอย่างและคำแนะนำที่ครอบคลุม

### คำถามที่ 4: Aspose.PSD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถทดลองใช้ฟรีได้จาก[หน้าเผยแพร่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A5: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อขอความช่วยเหลือและเชื่อมต่อกับชุมชน