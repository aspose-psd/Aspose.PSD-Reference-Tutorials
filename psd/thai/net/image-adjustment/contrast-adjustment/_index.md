---
title: การใช้การปรับความคมชัดใน Aspose.PSD สำหรับ .NET
linktitle: การใช้การปรับคอนทราสต์
second_title: Aspose.PSD .NET API
description: เรียนรู้วิธีใช้งานการปรับคอนทราสต์ใน Aspose.PSD สำหรับ .NET พร้อมคำแนะนำทีละขั้นตอนนี้
weight: 11
url: /th/net/image-adjustment/contrast-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การใช้การปรับความคมชัดใน Aspose.PSD สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่คู่มือที่ครอบคลุมเกี่ยวกับการนำการปรับคอนทราสต์ไปใช้ใน Aspose.PSD สำหรับ .NET! ในบทช่วยสอนนี้ เราจะสำรวจกระบวนการเพิ่มคอนทราสต์ของรูปภาพโดยใช้ Aspose.PSD ซึ่งเป็นไลบรารีรูปภาพ .NET อันทรงพลัง ในตอนท้ายของคู่มือนี้ คุณจะมีความเข้าใจที่ชัดเจนเกี่ยวกับวิธีการใช้การปรับคอนทราสต์กับรูปภาพของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกกระบวนการทีละขั้นตอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.PSD สำหรับไลบรารี .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD สำหรับ .NET คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/psd/net/).

2. ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีที่จะจัดเก็บไฟล์ต้นทางและปลายทางของคุณ แทนที่ "Your Document Directory" ในโค้ดที่ให้มาด้วยเส้นทางไปยังไดเร็กทอรีนี้

ตอนนี้เรามีข้อกำหนดเบื้องต้นตามลำดับแล้ว เรามาดำเนินการดำเนินการต่อไป

## นำเข้าเนมสเปซ

ในขั้นตอนนี้ เราจะนำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานที่ได้รับจากไลบรารี Aspose.PSD

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ

โหลดอิมเมจต้นฉบับลงในอินสแตนซ์ของ`RasterImage` ระดับ.

```csharp
//ExStart:LoadImage
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // ไปยังขั้นตอนต่อไป...
}
//ตัวอย่าง: LoadImage
```

## ขั้นตอนที่ 2: ปรับคอนทราสต์

ในขั้นตอนนี้ เราจะปรับคอนทราสต์ของรูปภาพที่โหลด

```csharp
//ExStart:ปรับคอนทราสต์
rasterImage.AdjustContrast(50); // ปรับความคมชัด 50%
// ไปยังขั้นตอนต่อไป...
//ExEnd:ปรับคอนทราสต์
```

## ขั้นตอนที่ 3: สร้างตัวเลือก TIFF

 สร้างอินสแตนซ์ของ`TiffOptions` สำหรับรูปภาพที่ได้ ให้ตั้งค่าคุณสมบัติต่างๆ และบันทึกรูปภาพในรูปแบบ TIFF

```csharp
//ExStart:CreateTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd: CreateTiffOptions
```

ยินดีด้วย! คุณใช้งานการปรับคอนทราสต์โดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการเพิ่มคอนทราสต์ของภาพด้วย Aspose.PSD สำหรับ .NET ไลบรารีให้วิธีที่ตรงไปตรงมาในการจัดการคุณสมบัติของรูปภาพ ช่วยให้นักพัฒนาสามารถสร้างรูปภาพที่ดึงดูดสายตาได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ .NET เหมาะสำหรับผู้เริ่มต้นหรือไม่

คำตอบ 1: Aspose.PSD สำหรับ .NET ได้รับการออกแบบมาให้เป็นมิตรกับนักพัฒนา ทำให้เหมาะสำหรับทั้งผู้เริ่มต้นและนักพัฒนาที่มีประสบการณ์

### คำถามที่ 2: ฉันสามารถใช้ Aspose.PSD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 ตอบ 2: ได้ Aspose.PSD สำหรับ .NET สามารถใช้ในโครงการเชิงพาณิชย์ได้ สำหรับรายละเอียดใบอนุญาต โปรดไปที่[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ได้ คุณสามารถทดลองใช้ Aspose.PSD สำหรับ .NET ได้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A4: เยี่ยมชมฟอรั่มสนับสนุน Aspose.PSD สำหรับ .NET[ที่นี่](https://forum.aspose.com/c/psd/34) เพื่อขอความช่วยเหลือ

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A5: หากจำเป็น คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
