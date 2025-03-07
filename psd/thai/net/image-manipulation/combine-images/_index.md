---
title: การรวมรูปภาพใน Aspose.PSD สำหรับ .NET
linktitle: การรวมรูปภาพ
second_title: Aspose.PSD .NET API
description: รวมรูปภาพได้อย่างง่ายดายใน .NET ด้วย Aspose.PSD ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเราเพื่อการปรับแต่งภาพที่ราบรื่น
weight: 10
url: /th/net/image-manipulation/combine-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การรวมรูปภาพใน Aspose.PSD สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนทีละขั้นตอนเกี่ยวกับการรวมรูปภาพโดยใช้ Aspose.PSD สำหรับ .NET! Aspose.PSD เป็นไลบรารี .NET อันทรงพลังที่ช่วยให้นักพัฒนาทำงานกับไฟล์ Adobe Photoshop ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการรวมรูปภาพโดยใช้ Aspose.PSD โดยให้ตัวอย่างที่เป็นประโยชน์และขั้นตอนโดยละเอียดแก่คุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose.PSD: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/psd/net/).

ตอนนี้ เรามาเจาะลึกบทช่วยสอนกันดีกว่า!

## นำเข้าเนมสเปซ

ขั้นแรก คุณต้องนำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose.PSD เพิ่มข้อมูลโค้ดต่อไปนี้ที่จุดเริ่มต้นของไฟล์ .NET ของคุณ:

```csharp
using Aspose.PSD.ImageOptions;
using Aspose.PSD.Sources;
```

## ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อม

เริ่มต้นด้วยการตั้งค่าสภาพแวดล้อมและระบุไดเร็กทอรีสำหรับรูปภาพของคุณ

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
```

## ขั้นตอนที่ 2: สร้างอินสแตนซ์ PsdOptions

สร้างอินสแตนซ์ของ PsdOptions โดยตั้งค่าคุณสมบัติตามต้องการ

```csharp
PsdOptions imageOptions = new PsdOptions();
```

## ขั้นตอนที่ 3: สร้าง FileCreateSource

สร้างอินสแตนซ์ของ FileCreateSource และกำหนดให้กับคุณสมบัติ Source ของ imageOptions

```csharp
imageOptions.Source = new FileCreateSource(dataDir + "Two_images_result_out.psd", false);
```

## ขั้นตอนที่ 4: สร้างอินสแตนซ์รูปภาพ

สร้างอินสแตนซ์ของรูปภาพและกำหนดขนาดแคนวาส

```csharp
using (var image = Image.Create(imageOptions, 600, 600))
```

## ขั้นตอนที่ 5: เริ่มต้นกราฟิกและวาดภาพ

เริ่มต้นอินสแตนซ์ของกราฟิก ล้างพื้นผิวของภาพด้วยสีขาว และวาดภาพลงบนผืนผ้าใบ

```csharp
var graphics = new Graphics(image);
graphics.Clear(Color.White);
graphics.DrawImage(Image.Load(dataDir + "example1.psd"), 0, 0, 300, 600);
graphics.DrawImage(Image.Load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

## ขั้นตอนที่ 6: บันทึกภาพที่รวม

บันทึกภาพรวมสุดท้าย

```csharp
image.Save();
```

ยินดีด้วย! คุณได้รวมสองภาพโดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้แนะนำคุณตลอดกระบวนการรวมรูปภาพโดยใช้ Aspose.PSD ด้วย API ที่ใช้งานง่าย Aspose.PSD ช่วยให้นักพัฒนาจัดการไฟล์ Photoshop ได้อย่างราบรื่นในแอปพลิเคชัน .NET

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับ .NET ทุกเวอร์ชันหรือไม่

ตอบ 1: ใช่ Aspose.PSD เข้ากันได้กับ .NET ทุกเวอร์ชัน จึงรับประกันความคล่องตัวในโครงการพัฒนาของคุณ

### คำถามที่ 2: ฉันสามารถใช้ Aspose.PSD เพื่อวัตถุประสงค์ทางการค้าได้หรือไม่

ตอบ 2: ได้ Aspose.PSD สามารถใช้เพื่อวัตถุประสงค์ส่วนตัวและเชิงพาณิชย์ได้ ตรวจสอบรายละเอียดใบอนุญาต[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนจากชุมชนหรือพิจารณาซื้อแผนการสนับสนุน

### คำถามที่ 4: Aspose.PSD มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้หรือไม่

A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
