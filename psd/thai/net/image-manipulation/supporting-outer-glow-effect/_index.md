---
title: รองรับเอฟเฟกต์เรืองแสงภายนอกใน Aspose.PSD สำหรับ .NET
linktitle: รองรับเอฟเฟกต์เรืองแสงด้านนอก
second_title: Aspose.PSD .NET API
description: สำรวจพลังของเอฟเฟกต์เรืองแสงภายนอกใน Aspose.PSD สำหรับ .NET ยกระดับการออกแบบภาพของคุณด้วยบทช่วยสอนทีละขั้นตอนนี้
weight: 16
url: /th/net/image-manipulation/supporting-outer-glow-effect/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับเอฟเฟกต์เรืองแสงภายนอกใน Aspose.PSD สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนของเราในการสนับสนุน Outer Glow Effect ใน Aspose.PSD สำหรับ .NET Aspose.PSD เป็นไลบรารีอันทรงพลังที่ช่วยให้จัดการไฟล์ PSD ในแอปพลิเคชัน .NET ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะสำรวจการใช้งาน Outer Glow Effect และให้คำแนะนำโดยละเอียดเพื่อรวมเข้ากับโปรเจ็กต์ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับ .NET Library: ดาวน์โหลดไลบรารีจากไฟล์[เอกสาร Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่คุณต้องการ

- ไดเร็กทอรีเอกสารและเอาท์พุต: กำหนดไดเร็กทอรีเอกสารและเอาท์พุตของคุณในโค้ดที่ให้มา

## นำเข้าเนมสเปซ

ในส่วนนี้ เราจะนำเข้าเนมสเปซที่จำเป็นเพื่อเริ่มต้นใช้งาน Outer Glow Effect ทำตามขั้นตอนเหล่านี้:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

ตอนนี้ เรามาแบ่งตัวอย่างที่ให้ไว้ออกเป็นหลายขั้นตอนเพื่อให้ได้เอฟเฟกต์แสงด้านนอก

## ขั้นตอนที่ 1: ตั้งค่าเอกสารและเส้นทางเอาท์พุต

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## ขั้นตอนที่ 2: โหลดรูปภาพ PSD

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    // ขั้นตอนการดำเนินการจะถูกเพิ่มด้านล่าง
}
```

## ขั้นตอนที่ 3: เพิ่มเอฟเฟกต์เรืองแสงด้านนอก

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## ขั้นตอนที่ 4: กำหนดค่าพารามิเตอร์การเรืองแสงภายนอก

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## ขั้นตอนที่ 5: บันทึกรูปภาพ

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## ขั้นตอนที่ 6: ทำความสะอาด

```csharp
File.Delete(outputPng);
```

## ขั้นตอนที่ 7: แสดงข้อความแสดงความสำเร็จ

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## บทสรุป

ยินดีด้วย! คุณใช้งาน Outer Glow Effect โดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว คุณสมบัติอันทรงพลังนี้ช่วยเพิ่มความน่าดึงดูดทางสายตาให้กับรูปภาพของคุณ โดยมอบสัมผัสอันเป็นเอกลักษณ์ให้กับการออกแบบของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับเฟรมเวิร์ก .NET ทั้งหมดหรือไม่

ตอบ 1: ใช่ Aspose.PSD รองรับเฟรมเวิร์ก .NET ที่หลากหลาย ทำให้มั่นใจได้ถึงความเข้ากันได้กับสภาพแวดล้อมการพัฒนาที่หลากหลาย

### คำถามที่ 2: ฉันจะหาเอกสารเพิ่มเติมสำหรับ Aspose.PSD ได้ที่ไหน

 A2: โปรดดูที่[เอกสาร Aspose.PSD .NET](https://reference.aspose.com/psd/net/) สำหรับข้อมูลและตัวอย่างที่ครอบคลุม

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A3: เยี่ยมเลย[Aspose.PSD ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) สำหรับตัวเลือกการออกใบอนุญาตชั่วคราว

### คำถามที่ 4: ผู้ใช้ Aspose.PSD รองรับอะไรบ้าง

 A4: เข้าร่วม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 5: ฉันสามารถซื้อ Aspose.PSD สำหรับ .NET ได้หรือไม่

 A5: ใช่ สำรวจตัวเลือกใบอนุญาตและทำการซื้อของคุณ[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
