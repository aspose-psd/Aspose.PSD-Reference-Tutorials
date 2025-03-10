---
title: การเบลอภาพใน Aspose.PSD สำหรับ .NET
linktitle: การเบลอภาพ
second_title: Aspose.PSD .NET API
description: เรียนรู้วิธีเบลอภาพอย่างง่ายดายด้วย Aspose.PSD สำหรับ .NET คำแนะนำทีละขั้นตอนสำหรับการปรับแต่งภาพที่ราบรื่นในโปรเจ็กต์ C# ของคุณ
weight: 13
url: /th/net/image-adjustment/blur-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเบลอภาพใน Aspose.PSD สำหรับ .NET

## การแนะนำ

ในขอบเขตของการพัฒนา .NET นั้น Aspose.PSD พิสูจน์ให้เห็นแล้วว่าเป็นพันธมิตรที่ทรงพลังสำหรับการปรับแต่งภาพ บทช่วยสอนนี้มุ่งเน้นไปที่งานเฉพาะ: การทำภาพเบลอโดยใช้ Aspose.PSD สำหรับ .NET หากคุณกระตือรือร้นที่จะพัฒนาทักษะการประมวลผลภาพของคุณ หรือเพียงแค่มองหาวิธีที่มีประสิทธิภาพในการเบลอภาพโดยทางโปรแกรม แสดงว่าคุณมาถูกที่แล้ว

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/psd/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET และมีความเข้าใจพื้นฐานเกี่ยวกับ C#

- รูปภาพตัวอย่าง: เตรียมรูปภาพตัวอย่างในรูปแบบ PSD คุณสามารถใช้ของคุณเองหรือดาวน์โหลดเพื่อทดสอบ

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นในโค้ด C# ของคุณ:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีเอกสารของคุณ

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดรูปภาพ

```csharp
//ExStart: BluranImage

string sourceFile = dataDir + @"sample.psd";

// โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของคลาส RasterImage
using (var image = Image.Load(sourceFile))
{
    // ทำตามขั้นตอนถัดไปโดยใช้บล็อกนี้
}
```

## ขั้นตอนที่ 3: แปลงรูปภาพเป็น RasterImage

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## ขั้นตอนที่ 4: ใช้ตัวกรอง Gaussian Blur

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

 นี่.`GaussianBlurFilterOptions` คลาสใช้กับรัศมีที่ระบุ 15 สำหรับการเบลอทั้งแนวนอนและแนวตั้ง

## ขั้นตอนที่ 5: บันทึกภาพเบลอ

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## บทสรุป

ยินดีด้วย! คุณเบลอภาพโดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ให้ข้อมูลเชิงลึกเกี่ยวกับความสามารถของ Aspose.PSD และเปิดประตูสู่ความเป็นไปได้มากมายในการจัดการรูปภาพในแอปพลิเคชัน .NET ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ความเข้มของการเบลอที่แตกต่างกันกับส่วนต่างๆ ของภาพได้หรือไม่

ตอบ 1: ได้ Aspose.PSD อนุญาตให้คุณใช้ฟิลเตอร์ที่มีพารามิเตอร์ที่แตกต่างกันไปในพื้นที่เฉพาะของภาพ โดยให้การควบคุมกระบวนการเบลอได้อย่างละเอียด

### คำถามที่ 2: Aspose.PSD เข้ากันได้กับรูปแบบภาพทุกรูปแบบหรือไม่

ตอบ 2: แม้ว่า Aspose.PSD จะรองรับรูปแบบรูปภาพที่หลากหลาย แต่ขอแนะนำให้ตรวจสอบเอกสารประกอบเพื่อดูรายการทั้งหมดและข้อควรพิจารณาเฉพาะรูปแบบ

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A3: คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการทดสอบและประเมินผล

### คำถามที่ 4: มีคุณสมบัติการจัดการรูปภาพอื่นๆ ใน Aspose.PSD หรือไม่

A4: แน่นอน! Aspose.PSD นำเสนอชุดคุณสมบัติที่ครอบคลุม รวมถึงการปรับขนาด การครอบตัด และการปรับสี สำรวจเอกสารเพื่อดูรายการทั้งหมด

### คำถามที่ 5: ฉันจะขอความช่วยเหลือหรือติดต่อกับชุมชน Aspose.PSD ได้ที่ไหน

 A5: หากมีข้อสงสัยหรือข้อหารือใดๆ โปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
