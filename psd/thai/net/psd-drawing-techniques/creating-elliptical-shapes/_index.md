---
title: การสร้างรูปทรงวงรีด้วย Aspose.PSD สำหรับ .NET
linktitle: การสร้างรูปทรงวงรีด้วย Aspose.PSD สำหรับ .NET
second_title: Aspose.PSD .NET API
description: เรียนรู้วิธีการวาดรูปทรงวงรีใน .NET โดยใช้ Aspose.PSD คำแนะนำทีละขั้นตอนพร้อมตัวอย่างโค้ด สร้างกราฟิกที่น่าทึ่งได้อย่างง่ายดาย
weight: 13
url: /th/net/psd-drawing-techniques/creating-elliptical-shapes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การสร้างรูปทรงวงรีด้วย Aspose.PSD สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่คู่มือที่ครอบคลุมของเราเกี่ยวกับการสร้างรูปทรงวงรีโดยใช้ Aspose.PSD สำหรับ .NET Aspose.PSD เป็นไลบรารี .NET อันทรงพลังที่ช่วยให้นักพัฒนาสามารถจัดการและแปลงไฟล์ Photoshop ได้โดยไม่ต้องใช้ Adobe Photoshop ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการวาดรูปทรงวงรีโดยใช้ไลบรารี

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Aspose.PSD สำหรับไลบรารี .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD ในโปรเจ็กต์ .NET ของคุณ คุณสามารถดาวน์โหลดได้จาก[Aspose.PSD สำหรับเอกสาร .NET](https://reference.aspose.com/psd/net/).

- สภาพแวดล้อม .NET: บทช่วยสอนนี้ถือว่าคุณมีความรู้เกี่ยวกับการทำงานของ .NET framework

## นำเข้าเนมสเปซ

ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ เพื่อให้แน่ใจว่าคุณจะสามารถเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับการวาดรูปทรงวงรี นี่คือตัวอย่าง:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

ตอนนี้ เรามาแบ่งกระบวนการสร้างรูปทรงวงรีออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: สร้างอินสแตนซ์ของ BmpOptions

```csharp
// สร้างอินสแตนซ์ของ BmpOptions และตั้งค่าคุณสมบัติต่างๆ
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## ขั้นตอนที่ 3: สร้างอินสแตนซ์ของรูปภาพ

```csharp
// สร้างอินสแตนซ์ของรูปภาพ
using (Image image = new PsdImage(100, 100))
{
    // สร้างและเริ่มต้นอินสแตนซ์ของคลาสกราฟิกและพื้นผิวกราฟิกที่ชัดเจน
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## ขั้นตอนที่ 4: วาดรูปวงรีประ

```csharp
    // วาดรูปวงรีประโดยระบุวัตถุปากกาที่มีสีแดงและมีสี่เหลี่ยมผืนผ้าล้อมรอบ
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## ขั้นตอนที่ 5: วาดรูปร่างวงรีต่อเนื่อง

```csharp
    //วาดรูปวงรีต่อเนื่องโดยระบุวัตถุปากกาด้วยแปรงทึบที่มีสีน้ำเงินและมีสี่เหลี่ยมผืนผ้าล้อมรอบ
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // ส่งออกรูปภาพเป็นรูปแบบไฟล์ bmp
    image.Save(outpath, saveOptions);
}
```

## บทสรุป

ยินดีด้วย! คุณสร้างรูปทรงวงรีโดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนที่สำคัญ ตั้งแต่การตั้งค่าสภาพแวดล้อมไปจนถึงการวาดวงรีทั้งแบบจุดและแบบต่อเนื่อง

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสารสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A1: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/psd/net/).

### คำถามที่ 2: ฉันจะดาวน์โหลด Aspose.PSD สำหรับ .NET ได้อย่างไร

 A2: คุณสามารถดาวน์โหลดได้จากหน้าวางจำหน่าย[ที่นี่](https://releases.aspose.com/psd/net/).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A4: เยี่ยมชมฟอรั่มการสนับสนุน[ที่นี่](https://forum.aspose.com/c/psd/34).

### คำถามที่ 5: ฉันจำเป็นต้องมีใบอนุญาตชั่วคราวในการทดสอบหรือไม่

 A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
