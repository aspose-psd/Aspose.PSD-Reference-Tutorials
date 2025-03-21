---
title: การวาดส่วนโค้งด้วย Aspose.PSD สำหรับ .NET
linktitle: การวาดส่วนโค้งด้วย Aspose.PSD สำหรับ .NET
second_title: Aspose.PSD .NET API
description: สำรวจพลังของ Aspose.PSD สำหรับ .NET ในการวาดส่วนโค้งได้อย่างง่ายดาย ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเราเพื่อดูกราฟิกที่น่าทึ่งในแอปพลิเคชันของคุณ
weight: 11
url: /th/net/psd-drawing-techniques/drawing-arcs/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดส่วนโค้งด้วย Aspose.PSD สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมของเราเกี่ยวกับการวาดส่วนโค้งโดยใช้ Aspose.PSD สำหรับ .NET! Aspose.PSD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Adobe Photoshop (.psd) ในแอปพลิเคชัน .NET ของตนได้ ในบทช่วยสอนนี้ เราจะเน้นไปที่การสร้างส่วนโค้งที่ดึงดูดสายตาโดยใช้ไลบรารี Aspose.PSD

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำดิ่งสู่โลกแห่งการวาดส่วนโค้งที่น่าตื่นเต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Aspose.PSD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD จากไฟล์[ลิงค์ดาวน์โหลด](https://releases.aspose.com/psd/net/).

-  ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีเพื่อจัดเก็บเอกสารของคุณและแทนที่`"Your Document Directory"` ในรหัสที่ให้มาพร้อมกับเส้นทางจริง

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ตรวจสอบให้แน่ใจว่าได้รวมเนมสเปซที่จำเป็นสำหรับการทำงานกับ Aspose.PSD เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของไฟล์โค้ดของคุณ:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

ตอนนี้ เรามาแบ่งตัวอย่างออกเป็นหลายขั้นตอนกัน

## ขั้นตอนที่ 1: การตั้งค่าไดเร็กทอรีเอกสาร

 แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงไปยังไดเร็กทอรีเอกสารของคุณที่คุณต้องการบันทึกรูปภาพที่สร้างขึ้น

```csharp
string dataDir = "Your Actual Document Directory";
```

## ขั้นตอนที่ 2: การวาดส่วนโค้ง

 สร้างอินสแตนซ์ของ`BmpOptions` และกำหนดคุณสมบัติได้แก่`BitsPerPixel`.

```csharp
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## ขั้นตอนที่ 3: การเริ่มต้นรูปภาพและกราฟิก

 สร้างอินสแตนซ์ของ`PsdImage` และ`Graphics`จากนั้นล้างพื้นผิวกราฟิกด้วยสีที่ระบุ (ในกรณีนี้คือสีเหลือง)

```csharp
using (Image image = new PsdImage(100, 100))
{
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## ขั้นตอนที่ 4: การกำหนดพารามิเตอร์ส่วนโค้ง

ตั้งค่าพารามิเตอร์สำหรับส่วนโค้ง เช่น ความกว้าง ความสูง มุมเริ่มต้น และมุมกวาด

```csharp
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

## ขั้นตอนที่ 5: การวาดส่วนโค้ง

วาดส่วนโค้งบนพื้นผิวกราฟิกโดยใช้พารามิเตอร์ที่ระบุและปากกาสีดำ

```csharp
graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);
```

## ขั้นตอนที่ 6: บันทึกรูปภาพ

บันทึกรูปภาพเป็นรูปแบบไฟล์ BMP โดยใช้ตัวเลือกที่ระบุ

```csharp
image.Save(outpath, saveOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีการวาดส่วนโค้งโดยใช้ Aspose.PSD สำหรับ .NET เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้เปิดโอกาสให้สร้างกราฟิกที่น่าทึ่งในแอปพลิเคชันของคุณได้อย่างไม่มีที่สิ้นสุด

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสารสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A1: สามารถดูเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/psd/net/).

### คำถามที่ 2: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A2: คุณสามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 3: มีฟอรัมชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่

 A3: ใช่ คุณสามารถเยี่ยมชมได้[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อสนับสนุนชุมชน

### คำถามที่ 4: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.PSD ได้ที่ไหน

 A4: คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 5: ฉันสามารถลองใช้ Aspose.PSD สำหรับ .NET ฟรีก่อนซื้อได้หรือไม่

 A5: ได้ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
