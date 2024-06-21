---
title: การเพิ่มเอฟเฟกต์เส้นขีดให้กับเลเยอร์ใน Aspose.PSD สำหรับ .NET
linktitle: การเพิ่มเอฟเฟกต์เส้นขีดให้กับเลเยอร์
second_title: Aspose.PSD .NET API
description: ปรับปรุงความสวยงามของภาพด้วย Aspose.PSD สำหรับ .NET เรียนรู้การเพิ่มเอฟเฟ็กต์จังหวะทีละขั้นตอน ดาวน์โหลด ซื้อ หรือทดลองใช้งานฟรีทันที
type: docs
weight: 10
url: /th/net/layer-effects/adding-stroke-effects/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนทีละขั้นตอนเกี่ยวกับการเพิ่มเอฟเฟกต์เส้นโครงร่างให้กับเลเยอร์ใน Aspose.PSD สำหรับ .NET การเพิ่มความน่าดึงดูดทางสายตาให้กับรูปภาพของคุณเป็นเรื่องง่ายด้วยเอฟเฟกต์เส้นขีด และ Aspose.PSD ทำให้นักพัฒนา .NET กลายเป็นเรื่องราบรื่น ในคู่มือนี้ เราจะแนะนำคุณตลอดกระบวนการ โดยให้ขั้นตอนและตัวอย่างที่ชัดเจนเพื่อช่วยให้คุณเชี่ยวชาญคุณลักษณะอันทรงพลังนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Aspose.PSD สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD จากไฟล์[เว็บไซต์](https://releases.aspose.com/psd/net/).

- ไดเร็กทอรีเอกสาร: เตรียมไดเร็กทอรีที่มีเอกสาร PSD ที่คุณต้องการใช้เอฟเฟกต์เส้นขีด

- ไดเร็กทอรีเอาต์พุต: มีไดเร็กทอรีแยกต่างหากสำหรับจัดเก็บรูปภาพเอาต์พุตพร้อมเอฟเฟกต์เส้นโครงร่าง

- Visual Studio: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่า Visual Studio หรือสภาพแวดล้อมการพัฒนา .NET ที่ต้องการอื่นๆ แล้ว

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชันการทำงานของ Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดเอกสาร PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // รหัสของคุณสำหรับการโหลดเอกสาร PSD อยู่ที่นี่
}
```

## ขั้นตอนที่ 2: เพิ่มเอฟเฟกต์เส้นสี

```csharp
// เพิ่มการเติมสี ที่ตำแหน่งด้านใน
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## ขั้นตอนที่ 3: ตำแหน่งภายนอก

```csharp
// เพิ่มการเติมสีที่ตำแหน่งด้านนอก
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## ขั้นตอนที่ 4: ตำแหน่งกึ่งกลาง

```csharp
// เพิ่มการเติมสีที่ตำแหน่งกึ่งกลาง
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

ทำซ้ำขั้นตอนที่คล้ายกันสำหรับการเติมไล่ระดับสีและลวดลาย โดยปรับการตั้งค่าให้เหมาะสม

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มเอฟเฟกต์เส้นขีดให้กับเลเยอร์โดยใช้ Aspose.PSD สำหรับ .NET เรียบร้อยแล้ว ทดลองใช้การตั้งค่าต่างๆ เพื่อให้ได้ภาพที่ต้องการในภาพของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้เอฟเฟ็กต์สโตรคกับเลเยอร์ที่ต้องการเท่านั้นได้หรือไม่

A1: ได้ คุณสามารถกำหนดเป้าหมายเลเยอร์ที่ต้องการได้โดยการปรับดัชนีเลเยอร์ในโค้ด

### คำถามที่ 2: Aspose.PSD เข้ากันได้กับเฟรมเวิร์ก .NET ล่าสุดหรือไม่

A2: แน่นอน! Aspose.PSD ได้รับการออกแบบมาเพื่อผสานรวมกับเฟรมเวิร์ก .NET ล่าสุดได้อย่างราบรื่น

### คำถามที่ 3: ฉันจะปรับแต่งสีของเส้นขีดได้อย่างไร

 A3: เพียงแก้ไขไฟล์`Color` คุณสมบัติในโค้ดเพื่อให้ได้สีเส้นขีดที่ต้องการ

### คำถามที่ 4: Aspose.PSD รองรับการประมวลผลเป็นชุดสำหรับไฟล์ PSD หลายไฟล์หรือไม่

A4: ได้ คุณสามารถวนซ้ำไฟล์ PSD หลายไฟล์ และใช้เอฟเฟกต์เส้นขีดโดยใช้วิธีที่คล้ายกัน

### คำถามที่ 5: ฉันสามารถใช้เวอร์ชันทดลองก่อนซื้อ Aspose.PSD ได้หรือไม่

 A5: แน่นอน! คว้า[ทดลองฟรี](https://releases.aspose.com/) เพื่อสำรวจความสามารถของ Aspose.PSD ก่อนตัดสินใจซื้อ