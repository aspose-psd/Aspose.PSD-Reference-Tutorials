---
title: การใช้ Bradley Threshold ใน Aspose.PSD สำหรับ .NET
linktitle: การใช้เกณฑ์แบรดลีย์
second_title: Aspose.PSD .NET API
description: ปรับปรุงการแบ่งส่วนภาพโดยใช้ Bradley Threshold ใน Aspose.PSD สำหรับ .NET คำแนะนำทีละขั้นตอนสำหรับไบนาไรเซชันที่มีประสิทธิภาพ
type: docs
weight: 15
url: /th/net/image-processing/apply-bradley-threshold/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมของเราเกี่ยวกับการใช้ Bradley Threshold ใน Aspose.PSD สำหรับ .NET Aspose.PSD สำหรับ .NET เป็นไลบรารีที่มีประสิทธิภาพซึ่งช่วยให้คุณสามารถทำงานกับไฟล์ Photoshop ในแอปพลิเคชัน .NET ของคุณได้ Bradley Thresholding เป็นเทคนิคที่ใช้สำหรับการสร้างภาพแบบไบนาไรซ์ ซึ่งช่วยแยกวัตถุออกจากพื้นหลังได้อย่างมีประสิทธิภาพ

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการใช้ Bradley Threshold โดยใช้ Aspose.PSD สำหรับ .NET ก่อนที่เราจะเจาะลึกขั้นตอนต่างๆ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นที่จำเป็นอยู่แล้ว

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าต่อไปนี้:

-  Aspose.PSD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจากไฟล์[Aspose.PSD สำหรับเอกสาร .NET](https://reference.aspose.com/psd/net/).
- ไดเร็กทอรีเอกสาร: สร้างไดเร็กทอรีเพื่อจัดเก็บไฟล์ PSD ต้นฉบับและรูปภาพไบนารี่ที่ได้

เมื่อคุณมีข้อกำหนดเบื้องต้นพร้อมแล้ว เรามาดำเนินการตามคำแนะนำทีละขั้นตอนกันดีกว่า

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชัน Aspose.PSD:

```csharp
// นำเข้าเนมสเปซ Aspose.PSD
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพที่มีสัญญาณรบกวน

กำหนดเส้นทางไปยังไฟล์ PSD ต้นทางของคุณและปลายทางสำหรับเอาต์พุตแบบไบนารี:

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"binarized_out.png";
```

## ขั้นตอนที่ 2: ไบนารีรูปภาพโดยใช้ Bradley Threshold

โหลดรูปภาพ PSD ระบุค่าเกณฑ์ ใช้เกณฑ์ของ Bradley และบันทึกเอาต์พุตเป็นรูปภาพ PNG:

```csharp
// โหลดรูปภาพ
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //กำหนดค่าเกณฑ์
    double threshold = 0.15;

    // เรียกวิธี BinarizeBradley และส่งค่าเกณฑ์เป็นพารามิเตอร์
    image.BinarizeBradley(threshold);

    // บันทึกภาพที่ส่งออก
    image.Save(destName, new PngOptions());
}
```

## บทสรุป

ยินดีด้วย! คุณใช้ Bradley Threshold ใน Aspose.PSD สำหรับ .NET สำเร็จแล้ว เทคนิคนี้มีคุณค่าอย่างยิ่งในการปรับปรุงการแบ่งส่วนภาพในการใช้งานต่างๆ

รู้สึกอิสระที่จะสำรวจคุณสมบัติและฟังก์ชันการทำงานเพิ่มเติมที่ Aspose.PSD สำหรับ .NET มอบให้เพื่อเพิ่มประสิทธิภาพงานการประมวลผลภาพของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Bradley Threshold กับรูปภาพประเภทใดก็ได้หรือไม่

ตอบ 1: ใช่ Bradley Thresholding เป็นเทคนิคอเนกประสงค์ที่เหมาะกับภาพประเภทต่างๆ

### คำถามที่ 2: ฉันจะหาเอกสารประกอบ Aspose.PSD เพิ่มเติมได้จากที่ไหน

 A2: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/psd/net/) สำหรับข้อมูลโดยละเอียดเกี่ยวกับ Aspose.PSD สำหรับ .NET

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ได้ คุณสามารถทดลองใช้ Aspose.PSD สำหรับ .NET ได้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร

 A4: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.PSD ได้ที่ไหน

 A5: คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).