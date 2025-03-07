---
title: การครอบตัดไฟล์ PSD เมื่อแปลงเป็น PNG ใน Aspose.PSD สำหรับ .NET
linktitle: การครอบตัดไฟล์ PSD เมื่อแปลงเป็น PNG
second_title: Aspose.PSD .NET API
description: เรียนรู้วิธีครอบตัดไฟล์ PSD ได้อย่างง่ายดายโดยใช้ Aspose.PSD สำหรับ .NET ทำตามคำแนะนำทีละขั้นตอนของเราเพื่อการแปลงเป็น PNG อย่างราบรื่น
weight: 18
url: /th/net/psd-file-manipulation/crop-psd-conversion-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การครอบตัดไฟล์ PSD เมื่อแปลงเป็น PNG ใน Aspose.PSD สำหรับ .NET

## การแนะนำ
ในขอบเขตของการพัฒนา .NET การจัดการและการแปลงรูปภาพถือเป็นงานทั่วไป Aspose.PSD สำหรับ .NET มอบชุดเครื่องมืออันทรงพลังเพื่อปรับปรุงกระบวนการนี้ ข้อกำหนดที่พบบ่อยประการหนึ่งคือการครอบตัดไฟล์ PSD ก่อนที่จะแปลงเป็น PNG ในบทช่วยสอนทีละขั้นตอนนี้ เราจะเจาะลึกกระบวนการโดยใช้ Aspose.PSD สำหรับ .NET
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มการเดินทางครั้งนี้ ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
-  Aspose.PSD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจากไฟล์[Aspose.PSD สำหรับเอกสาร .NET](https://reference.aspose.com/psd/net/).
- ไฟล์ PSD ตัวอย่าง: เตรียมไฟล์ PSD ให้พร้อมสำหรับการทดลอง หากคุณไม่มี คุณสามารถใช้ตัวอย่างที่ให้ไว้ในบทช่วยสอนได้
- สภาพแวดล้อม .NET: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้
- Document Directory: ระบุเส้นทางไปยังไดเร็กทอรีเอกสารของคุณในโค้ด
## นำเข้าเนมสเปซ
ในโปรเจ็กต์ .NET ของคุณ ให้รวมเนมสเปซที่จำเป็นสำหรับ Aspose.PSD สำหรับ .NET:
```csharp
using Aspose.PSD.ImageOptions;
```
## ขั้นตอนที่ 1: โหลดรูปภาพ PSD
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// โหลดรูปภาพ PSD ที่มีอยู่
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```
## ขั้นตอนที่ 2: กำหนดสี่เหลี่ยมการครอบตัด
```csharp
// สร้างอินสแตนซ์ของคลาสสี่เหลี่ยมผืนผ้าโดยส่ง x, y, ความกว้าง และความสูง
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## ขั้นตอนที่ 3: ครอบตัดรูปภาพ
```csharp
// เรียกวิธีการครอบตัดของคลาส Image และส่งอินสแตนซ์คลาสสี่เหลี่ยมผืนผ้า
image.Crop(cropRectangle);
```
## ขั้นตอนที่ 4: ระบุตัวเลือก PNG
```csharp
// สร้างอินสแตนซ์ของคลาส PngOptions
PngOptions pngOptions = new PngOptions();
```
## ขั้นตอนที่ 5: บันทึกภาพที่ครอบตัดเป็น PNG
```csharp
// เรียกวิธีการบันทึก ระบุเส้นทางเอาต์พุต และ PngOptions เพื่อแปลงไฟล์ PSD เป็น PNG และบันทึกเอาต์พุต
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีครอบตัดไฟล์ PSD เรียบร้อยแล้วเมื่อแปลงเป็น PNG โดยใช้ Aspose.PSD สำหรับ .NET ความสามารถนี้สามารถประเมินค่าได้ในสถานการณ์การประมวลผลภาพต่างๆ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ไลบรารีนี้ในโครงการเชิงพาณิชย์ได้หรือไม่

 A1: ใช่ Aspose.PSD สำหรับ .NET พร้อมให้ใช้งานเชิงพาณิชย์แล้ว อ้างถึง[Aspose.PSD ใบอนุญาต](https://purchase.aspose.com/buy) เพื่อดูรายละเอียด

### คำถามที่ 2: มีการทดลองใช้ฟรีหรือไม่?

A2: แน่นอน! คุณสามารถสำรวจเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับความช่วยเหลือหรือข้อสงสัยใด ๆ

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A4: หากคุณต้องการใบอนุญาตชั่วคราว คุณสามารถขอรับได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: มีตัวอย่างหรือบทช่วยสอนในเอกสารประกอบหรือไม่

 A5: ได้ คุณสามารถค้นหาเอกสารและตัวอย่างที่ครอบคลุมได้[ที่นี่](https://reference.aspose.com/psd/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
