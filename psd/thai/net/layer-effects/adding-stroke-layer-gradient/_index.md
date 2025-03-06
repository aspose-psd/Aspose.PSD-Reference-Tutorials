---
title: การเพิ่มเลเยอร์ Stroke พร้อมการไล่ระดับสีใน Aspose.PSD สำหรับ .NET
linktitle: การเพิ่มเลเยอร์ Stroke ด้วยการไล่ระดับสี
second_title: Aspose.PSD .NET API
description: เรียนรู้วิธีเพิ่มเลเยอร์เส้นขีดไล่ระดับสีใน Aspose.PSD สำหรับ .NET ยกระดับทักษะการจัดการภาพของคุณด้วยบทช่วยสอนที่ครอบคลุมนี้
weight: 12
url: /th/net/layer-effects/adding-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเพิ่มเลเยอร์ Stroke พร้อมการไล่ระดับสีใน Aspose.PSD สำหรับ .NET

## การแนะนำ

หากคุณต้องการปรับปรุงแอปพลิเคชัน .NET ด้วยเอฟเฟกต์กราฟิกที่น่าทึ่ง Aspose.PSD สำหรับ .NET คือโซลูชันที่เหมาะกับคุณ ในบทช่วยสอนนี้ เราจะเจาะลึกกระบวนการเพิ่มเลเยอร์เส้นโครงร่างด้วยการไล่ระดับสีโดยใช้ Aspose.PSD สำหรับ .NET คำแนะนำทีละขั้นตอนนี้จะช่วยให้คุณยกระดับความน่าดึงดูดทางสายตาให้กับรูปภาพของคุณได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นการเดินทางครั้งนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความรู้ด้านการทำงานของการพัฒนา C# และ .NET
-  ติดตั้ง Aspose.PSD สำหรับไลบรารี .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/net/).
- โปรแกรมแก้ไขโค้ด เช่น Visual Studio เพื่อนำตัวอย่างที่ให้มาไปใช้

## นำเข้าเนมสเปซ

เพื่อเริ่มต้นสิ่งต่างๆ เรามานำเข้าเนมสเปซที่จำเป็นมาสู่โปรเจ็กต์ของเรากัน เนมสเปซเหล่านี้มีความสำคัญอย่างยิ่งในการใช้ประโยชน์จากฟังก์ชันการทำงานของ Aspose.PSD สำหรับ .NET

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

เริ่มต้นด้วยการกำหนดเส้นทางไปยังไดเร็กทอรีเอกสารของคุณในโค้ด เพื่อให้แน่ใจว่าไฟล์ที่จำเป็นจะถูกโหลดและบันทึกจากตำแหน่งที่ถูกต้อง

```csharp
string dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

โหลดไฟล์ PSD ต้นฉบับโดยใช้ Aspose.PSD สำหรับ .NET ตรวจสอบให้แน่ใจว่าโหลดทรัพยากรเอฟเฟกต์เพื่อจัดการเลเยอร์อย่างมีประสิทธิภาพ

```csharp
string sourceFileName = dataDir + "Stroke.psd";
string exportPath = dataDir + "StrokeGradientChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // รหัสสำหรับจัดการไฟล์ PSD อยู่ที่นี่
}
```

## ขั้นตอนที่ 3: ตรวจสอบการตั้งค่าเส้นโครงร่างไล่ระดับสี

ตรวจสอบให้แน่ใจว่าเลเยอร์เส้นโครงร่างที่มีการไล่ระดับสีได้รับการกำหนดค่าอย่างถูกต้องโดยตรวจสอบการตั้งค่าต่างๆ เช่น โหมดผสมผสาน ความทึบ และการมองเห็น

```csharp
var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

// ตรวจสอบการยืนยันสำหรับการตั้งค่าจังหวะการไล่ระดับสี
AssertIsTrue(gradientStroke.BlendMode == BlendMode.Normal);
AssertIsTrue(gradientStroke.Opacity == 255);
AssertIsTrue(gradientStroke.IsVisible);

// การตรวจสอบการยืนยันเพิ่มเติมสำหรับการตั้งค่าการเติม
// -
```

ใช้การตรวจสอบการยืนยันสำหรับการตั้งค่าการเติมอื่นๆ ต่อไป รวมถึงจุดสีและจุดโปร่งใส

## ขั้นตอนที่ 4: แก้ไขการตั้งค่าเส้นโครงร่างไล่ระดับสี

ตอนนี้ เรามาเปลี่ยนแปลงการตั้งค่าเส้นโครงร่างการไล่ระดับสีกัน แก้ไขพารามิเตอร์ เช่น สี ความทึบ โหมดผสมผสาน และประเภทการไล่ระดับสี เพื่อให้ได้เอฟเฟ็กต์ภาพที่ต้องการ

```csharp
// โค้ดสำหรับแก้ไขการตั้งค่าจังหวะการไล่ระดับสี
// -
```

## ขั้นตอนที่ 5: บันทึกไฟล์ PSD ที่แก้ไข

บันทึกไฟล์ PSD ที่แก้ไขไปยังเส้นทางการส่งออกที่ระบุ

```csharp
im.Save(exportPath);
```

## บทสรุป

ยินดีด้วย! คุณได้เพิ่มเลเยอร์เส้นขีดด้วยการไล่ระดับสีโดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ช่วยให้คุณมีความรู้ในการปรับปรุงรูปภาพของคุณโดยทางโปรแกรม

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD สำหรับ .NET กับเฟรมเวิร์ก .NET อื่นๆ ได้หรือไม่

A1: ใช่ Aspose.PSD สำหรับ .NET เข้ากันได้กับกรอบงาน .NET ต่างๆ

### คำถามที่ 2: Aspose.PSD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อสนับสนุนชุมชน

### คำถามที่ 4: ฉันจะหาเอกสารที่ครอบคลุมสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A4: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/psd/net/) สำหรับข้อมูลโดยละเอียด

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A5: คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
