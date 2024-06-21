---
title: การใช้การปรับแกมมาใน Aspose.PSD สำหรับ .NET
linktitle: การใช้การปรับแกมมา
second_title: Aspose.PSD .NET API
description: สำรวจพลังของ Aspose.PSD สำหรับ .NET ด้วยคำแนะนำทีละขั้นตอนเกี่ยวกับการนำการปรับแกมมาไปใช้ ปรับความสว่างและคอนทราสต์ของภาพอย่างละเอียดได้อย่างง่ายดาย
type: docs
weight: 12
url: /th/net/image-adjustment/gamma-adjustment/
---
## การแนะนำ

ยินดีต้อนรับสู่คู่มือที่ครอบคลุมเกี่ยวกับการนำการปรับแกมมาไปใช้ใน Aspose.PSD สำหรับ .NET! การปรับแกมม่าเป็นเทคนิคการประมวลผลภาพที่สำคัญซึ่งช่วยให้คุณปรับแต่งความสว่างและคอนทราสต์ของภาพได้ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการโดยใช้ไลบรารี Aspose.PSD อันทรงพลังสำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเริ่มใช้งาน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับ .NET Library: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/net/).

- .NET Framework: บทช่วยสอนนี้ถือว่าคุณมีความเข้าใจพื้นฐานเกี่ยวกับการพัฒนา .NET และติดตั้ง .NET Framework แล้ว

- สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก IDE ที่คุณต้องการสำหรับการพัฒนา .NET เช่น Visual Studio

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นสำหรับการทำงานกับ Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

สร้างโครงการ .NET ใหม่ใน IDE ที่คุณเลือก ตรวจสอบให้แน่ใจว่าได้เพิ่มการอ้างอิงไปยังไลบรารี Aspose.PSD

## ขั้นตอนที่ 2: กำหนดไดเร็กทอรีเอกสาร

```csharp
string dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 3: โหลดรูปภาพ

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // ขั้นตอนเพิ่มเติมจะดำเนินการภายในนี้โดยใช้บล็อก
}
```

## ขั้นตอนที่ 4: ส่งไปยัง RasterImage และ Cache Data

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## ขั้นตอนที่ 5: ปรับแกมมา

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## ขั้นตอนที่ 6: สร้าง TiffOptions และบันทึก

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## บทสรุป

ยินดีด้วย! คุณใช้งานการปรับแกมมาโดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว ไลบรารีอันทรงพลังนี้มอบความสามารถที่แข็งแกร่งสำหรับการประมวลผลภาพ ทำให้เป็นเครื่องมืออันมีค่าสำหรับนักพัฒนา .NET

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสาร Aspose.PSD ได้ที่ไหน

 A1:คุณสามารถดูเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/psd/net/).

### คำถามที่ 2: ฉันจะดาวน์โหลด Aspose.PSD สำหรับ .NET ได้อย่างไร

 A2: คุณสามารถดาวน์โหลดห้องสมุดได้[ที่นี่](https://releases.aspose.com/psd/net/).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้ที่ไหน

 A4: คุณสามารถเยี่ยมชมฟอรั่มการสนับสนุนได้[ที่นี่](https://forum.aspose.com/c/psd/34).

### คำถามที่ 5: ฉันจำเป็นต้องมีใบอนุญาตชั่วคราวหรือไม่

 A5: หากจำเป็น คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).