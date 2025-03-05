---
title: การแสดงเอฟเฟกต์ Drop Shadow ใน Aspose.PSD สำหรับ .NET
linktitle: การเรนเดอร์เอฟเฟกต์เงาหล่น
second_title: Aspose.PSD .NET API
description: สำรวจพลังของ Aspose.PSD สำหรับ .NET ในบทช่วยสอนนี้ ฝึกฝนศิลปะแห่งการเรนเดอร์เอฟเฟกต์เงาตกกระทบที่น่าหลงใหล
type: docs
weight: 12
url: /th/net/image-effects/render-drop-shadow/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนทีละขั้นตอนเกี่ยวกับการแสดงเอฟเฟกต์เงาตกหล่นใน Aspose.PSD สำหรับ .NET! หากคุณต้องการพัฒนาทักษะการจัดการภาพโดยใช้ Aspose.PSD คุณมาถูกที่แล้ว ในคู่มือนี้ เราจะแนะนำคุณตลอดขั้นตอนการใช้เอฟเฟกต์เงาตกกระทบกับภาพของคุณอย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับไลบรารี .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/net/).

- ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีที่เก็บเอกสารและรูปภาพของคุณ คุณจะต้องระบุไดเร็กทอรีนี้ในโค้ด

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
using System;
```

ตอนนี้ เรามาแบ่งตัวอย่างโค้ดออกเป็นหลายขั้นตอนเพื่อความเข้าใจที่ชัดเจน:

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

```csharp
string dataDir = "Your Document Directory";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางจริงที่ใช้จัดเก็บรูปภาพของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ PSD พร้อมทรัพยากรเอฟเฟกต์

```csharp
string sourceFileName = dataDir + "Shadow.psd";
string pngExportPath = dataDir + "Shadowchanged1.png";
var loadOptions = new PsdLoadOptions()
{
	LoadEffectsResource = true
};
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

โหลดไฟล์ PSD ของคุณ ทำให้สามารถโหลดทรัพยากรเอฟเฟกต์ได้

## ขั้นตอนที่ 3: ดึงและตรวจสอบคุณสมบัติของเอฟเฟกต์ Drop Shadow

```csharp
var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);
if ((shadowEffect.Color != Color.Black) ||
	(shadowEffect.Opacity != 255) ||
	(shadowEffect.Distance != 3) ||
	(shadowEffect.Size != 7) ||
	(shadowEffect.UseGlobalLight != true) ||
	(shadowEffect.Angle != 90) ||
	(shadowEffect.Spread != 0) ||
	(shadowEffect.Noise != 0))
{
	throw new Exception("Shadow Effect properties were read wrong");
}
```

รับคุณสมบัติเอฟเฟกต์เงาตกกระทบและตรวจสอบตามความคาดหวังของคุณ

## ขั้นตอนที่ 4: บันทึกภาพด้วยเอฟเฟกต์เงาที่ใช้

```csharp
var saveOptions = new PngOptions();
saveOptions.ColorType = PngColorType.TruecolorWithAlpha;
im.Save(pngExportPath, saveOptions);
```

บันทึกภาพที่แก้ไขโดยใช้เอฟเฟกต์เงาแบบวางในรูปแบบ PNG

แค่นั้นแหละ! คุณได้แสดงผลเอฟเฟกต์เงาโดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการเรนเดอร์เอฟเฟกต์เงาใน Aspose.PSD สำหรับ .NET ด้วยการทำตามขั้นตอนง่ายๆ เหล่านี้ คุณจะสามารถเพิ่มความลึกและมิติให้กับภาพของคุณ สร้างผลลัพธ์ที่สวยงามน่าทึ่งได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ .NET เข้ากันได้กับรูปแบบภาพทุกรูปแบบหรือไม่

A1: Aspose.PSD รองรับรูปแบบ PSD เป็นหลัก แต่ยังมีตัวเลือกการแปลงสำหรับรูปแบบอื่นๆ มากมายอีกด้วย

### คำถามที่ 2: ฉันสามารถปรับแต่งคุณสมบัติเงาตกกระทบเพิ่มเติมได้หรือไม่

A2: แน่นอน! อย่าลังเลที่จะปรับโค้ดให้ตรงตามความต้องการเฉพาะของคุณและบรรลุเอฟเฟกต์ภาพที่ต้องการ

### คำถามที่ 3: ฉันจะหาเอกสารเพิ่มเติมสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/psd/net/) สำหรับข้อมูลเชิงลึกโดยละเอียดเกี่ยวกับฟังก์ชัน Aspose.PSD

### คำถามที่ 4: Aspose.PSD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือขอความช่วยเหลือจาก Aspose.PSD สำหรับ .NET ได้อย่างไร

 A5: ไปที่ฟอรัม Aspose.PSD[ที่นี่](https://forum.aspose.com/c/psd/34) เพื่อมีส่วนร่วมกับชุมชนและขอคำแนะนำจากผู้เชี่ยวชาญ