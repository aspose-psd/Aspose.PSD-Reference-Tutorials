---
title: การเพิ่มเอฟเฟกต์การไล่ระดับสีให้กับรูปภาพใน Aspose.PSD สำหรับ .NET
linktitle: การเพิ่มเอฟเฟกต์การไล่ระดับสีให้กับรูปภาพ
second_title: Aspose.PSD .NET API
description: ปรับปรุงภาพของคุณด้วยเอฟเฟกต์การไล่ระดับสีที่น่าหลงใหลโดยใช้ Aspose.PSD สำหรับ .NET ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเราสำหรับการแปลงภาพที่สร้างสรรค์
type: docs
weight: 11
url: /th/net/image-manipulation/adding-gradient-effects/
---
## การแนะนำ

การปรับปรุงรูปภาพด้วยเอฟเฟกต์การไล่ระดับสีสามารถเพิ่มมิติที่น่าดึงดูดให้กับเนื้อหาภาพของคุณได้ Aspose.PSD สำหรับ .NET มอบแพลตฟอร์มอันทรงพลังสำหรับการรวมการซ้อนทับแบบไล่ระดับสีลงในรูปภาพของคุณ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการเพิ่มเอฟเฟกต์การไล่ระดับสีโดยใช้ Aspose.PSD สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจาก[Aspose.PSD สำหรับเอกสาร .NET](https://reference.aspose.com/psd/net/).
- สภาพแวดล้อม .NET: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อม .NET ที่ใช้งานได้บนเครื่องของคุณ

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นในโครงการของคุณ:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## ขั้นตอนที่ 1: โหลดรูปภาพและกำหนดเส้นทาง

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFileName = Path.Combine(SourceDir, "GradientOverlay.psd");
string exportPath = Path.Combine(OutputDir, "GradientOverlayChanged.psd");

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};
```

## ขั้นตอนที่ 2: ยืนยันการตั้งค่าเริ่มต้น

ตรวจสอบให้แน่ใจว่าการตั้งค่าเริ่มต้นของการซ้อนทับแบบไล่ระดับสีเป็นไปตามที่คาดไว้:

```csharp
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    // ตรวจสอบการยืนยันสำหรับการตั้งค่าเริ่มต้น
    // -

    // จุดสี
    // -

    //จุดโปร่งใส
    // -
}
```

## ขั้นตอนที่ 3: แก้ไขการตั้งค่าการซ้อนทับแบบไล่ระดับสี

ปรับการตั้งค่าการซ้อนทับแบบไล่ระดับสีตามความต้องการของคุณ:

```csharp
// ทดสอบการแก้ไข
settings.Color = Color.Green;

gradientOverlay.Opacity = 193;
gradientOverlay.BlendMode = BlendMode.Lighten;

settings.AlignWithLayer = false;
settings.GradientType = GradientType.Radial;
settings.Angle = 45;
settings.Dither = true;
settings.HorizontalOffset = 15;
settings.VerticalOffset = 11;
settings.Reverse = true;

// เพิ่มจุดสีใหม่
// -

// เปลี่ยนตำแหน่งของจุดก่อนหน้า
// -

// เพิ่มจุดโปร่งใสใหม่
// -

// เปลี่ยนตำแหน่งของจุดโปร่งใสก่อนหน้า
// -

im.Save(exportPath);
```

## ขั้นตอนที่ 4: ตรวจสอบไฟล์ที่แก้ไข

ตรวจสอบว่ามีการใช้การแก้ไขสำเร็จหรือไม่:

```csharp
// ทดสอบไฟล์หลังแก้ไข
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];
    try
    {
        // ตรวจสอบการยืนยันสำหรับการตั้งค่าที่แก้ไข
        // -
    }
    catch (Exception e)
    {
        string ex = e.StackTrace;
    }
}
```

## บทสรุป

การเพิ่มเอฟเฟ็กต์การไล่ระดับสีให้กับรูปภาพโดยใช้ Aspose.PSD สำหรับ .NET จะเปิดโลกแห่งความเป็นไปได้ที่สร้างสรรค์ ทดลองใช้การตั้งค่าต่างๆ เพื่อให้ได้ภาพที่ต้องการในภาพของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้เอฟเฟกต์การไล่ระดับสีกับหลายเลเยอร์พร้อมกันได้หรือไม่

A1: ได้ คุณสามารถใช้เอฟเฟกต์การไล่ระดับสีกับหลายเลเยอร์ได้โดยการวนซ้ำแต่ละเลเยอร์และใช้การตั้งค่าที่ต้องการ

### คำถามที่ 2: Aspose.PSD สำหรับ .NET รองรับรูปแบบไฟล์ใดบ้าง

A2: Aspose.PSD สำหรับ .NET รองรับไฟล์ภาพหลากหลายรูปแบบ รวมถึง PSD, PNG, JPEG, BMP และ GIF

### คำถามที่ 3: มีเวอร์ชันทดลองใช้งานสำหรับ Aspose.PSD สำหรับ .NET หรือไม่

A3: ได้ คุณสามารถสำรวจความสามารถของ Aspose.PSD สำหรับ .NET ได้ด้วยการดาวน์โหลดรุ่นทดลองใช้ฟรีจาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A4: สำหรับความช่วยเหลือหรือข้อสงสัยใด ๆ โปรดไปที่[Aspose.PSD สำหรับฟอรัมสนับสนุน .NET](https://forum.aspose.com/c/psd/34).

### คำถามที่ 5: ฉันจะซื้อ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถซื้อห้องสมุดได้จาก[Aspose.PSD สำหรับหน้าการซื้อ .NET](https://purchase.aspose.com/buy).