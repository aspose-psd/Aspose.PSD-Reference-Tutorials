---
title: รองรับเอฟเฟกต์การซ้อนทับแบบไล่ระดับสีใน Aspose.PSD สำหรับ .NET
linktitle: รองรับเอฟเฟกต์การซ้อนทับแบบไล่ระดับสี
second_title: Aspose.PSD .NET API
description: ปรับปรุงกราฟิกใน .NET ด้วย Aspose.PSD บทช่วยสอนนี้จะแนะนำคุณตลอดการสนับสนุนเอฟเฟกต์การไล่ระดับสีแบบไล่สี
weight: 18
url: /th/net/image-manipulation/supporting-gradient-overlay-effect/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับเอฟเฟกต์การซ้อนทับแบบไล่ระดับสีใน Aspose.PSD สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการสนับสนุนเอฟเฟกต์การไล่ระดับสีใน Aspose.PSD สำหรับ .NET! หากคุณต้องการปรับปรุงความสามารถด้านกราฟิกของแอปพลิเคชัน .NET คำแนะนำทีละขั้นตอนนี้พร้อมช่วยเหลือคุณ เราจะเจาะลึกความซับซ้อนของการสร้างและแก้ไขเอฟเฟกต์การไล่ระดับสีในเลเยอร์โดยใช้ Aspose.PSD ซึ่งเป็นไลบรารีอันทรงพลังที่ทำให้การประมวลผลภาพง่ายขึ้น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มการเดินทางครั้งนี้ ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C# และ .NET
-  ติดตั้ง Aspose.PSD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/net/).
- สภาพแวดล้อมการพัฒนาที่ตั้งค่าด้วย IDE ที่คุณต้องการ

## นำเข้าเนมสเปซ

ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นในโค้ด C# ของคุณ:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
```

ตอนนี้เราได้พูดถึงข้อมูลเบื้องต้นแล้ว เรามาดูรายละเอียดแต่ละขั้นตอนกัน:

## ขั้นตอนที่ 1: โหลดรูปภาพ PSD

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFilePath = Path.Combine(SourceDir, "psdnet256.psd");
string outputFilePath = Path.Combine(OutputDir, "psdnet256.psd_output.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // รหัสสำหรับขั้นตอนต่อไปอยู่ที่นี่...
}
```

## ขั้นตอนที่ 2: เข้าถึงตัวเลือกการผสมเลเยอร์

```csharp
BlendingOptions layerBlendOptions = psdImage.Layers[1].BlendingOptions;
```

## ขั้นตอนที่ 3: ค้นหาหรือสร้างเอฟเฟกต์การไล่ระดับสีแบบไล่ระดับสี

```csharp
GradientOverlayEffect gradientOverlayEffect = null;

foreach (ILayerEffect effect in layerBlendOptions.Effects)
{
    gradientOverlayEffect = effect as GradientOverlayEffect;
    if (gradientOverlayEffect != null)
    {
        break;
    }
}

if (gradientOverlayEffect == null)
{
    gradientOverlayEffect = layerBlendOptions.AddGradientOverlay();
}
```

## ขั้นตอนที่ 4: กำหนดค่าเอฟเฟกต์การซ้อนทับแบบไล่ระดับสี

```csharp
gradientOverlayEffect.Opacity = 200;
gradientOverlayEffect.BlendMode = BlendMode.Hue;

GradientFillSettings settings = gradientOverlayEffect.Settings;

settings.ColorPoints = new IGradientColorPoint[]
{
    new GradientColorPoint(Color.GreenYellow, 0, 50),
    new GradientColorPoint(Color.BlueViolet, 4096, 50),
};

settings.Angle = 80;
settings.Scale = 150;
settings.GradientType = GradientType.Linear;

settings.TransparencyPoints[0].Opacity = 100;
settings.TransparencyPoints[1].Opacity = 100;
```

## ขั้นตอนที่ 5: บันทึกรูปภาพที่แก้ไข

```csharp
psdImage.Save(outputFilePath);
```

แค่นั้นแหละ! คุณได้เพิ่มเอฟเฟกต์การไล่ระดับสีแบบไล่ระดับสีลงในเลเยอร์โดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการสนับสนุนเอฟเฟกต์การไล่ระดับสีใน Aspose.PSD สำหรับ .NET ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถรวมคุณสมบัตินี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น ซึ่งจะช่วยเพิ่มความน่าดึงดูดให้กับรูปภาพของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับ .NET ทุกเวอร์ชันหรือไม่

A1: Aspose.PSD สำหรับ .NET เข้ากันได้กับ .NET Framework และ .NET Core

### คำถามที่ 2: ฉันสามารถใช้เอฟเฟ็กต์หลายรายการกับเลเยอร์เดียวได้หรือไม่

A2: ได้ คุณสามารถใช้เอฟเฟ็กต์ต่างๆ รวมถึงการไล่ระดับสีบนเลเยอร์เดียวได้

### คำถามที่ 3: ฉันจะหาตัวอย่างและเอกสารเพิ่มเติมได้จากที่ไหน

 A3: เยี่ยมชม[เอกสารประกอบ](https://reference.aspose.com/psd/net/) สำหรับตัวอย่างและแนวทางโดยละเอียด

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร

 A5: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อสนับสนุนชุมชน
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
