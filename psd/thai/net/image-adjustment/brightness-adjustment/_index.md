---
title: การใช้การปรับความสว่างใน Aspose.PSD สำหรับ .NET
linktitle: การใช้การปรับความสว่าง
second_title: Aspose.PSD .NET API
description: สำรวจพลังของ Aspose.PSD สำหรับ .NET ในการปรับความสว่างของภาพ ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการใช้งานที่ราบรื่น
weight: 10
url: /th/net/image-adjustment/brightness-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การใช้การปรับความสว่างใน Aspose.PSD สำหรับ .NET

## การแนะนำ

การปรับปรุงและปรับคุณลักษณะของรูปภาพเป็นข้อกำหนดทั่วไปในแอปพลิเคชันต่างๆ และ Aspose.PSD สำหรับ .NET มอบโซลูชันที่มีประสิทธิภาพสำหรับการจัดการไฟล์ PSD ได้อย่างราบรื่น การปรับเปลี่ยนอย่างหนึ่งคือการปรับความสว่าง ซึ่งช่วยให้คุณปรับเปลี่ยนความสว่างของภาพได้อย่างง่ายดาย

ในบทช่วยสอนนี้ เราจะอธิบายขั้นตอนการปรับความสว่างโดยใช้ Aspose.PSD สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อทำความเข้าใจอย่างครอบคลุมเกี่ยวกับวิธีการรวมการปรับความสว่างลงในไฟล์ PSD ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับไลบรารี .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD สำหรับ .NET จากไฟล์[ลิงค์ดาวน์โหลด](https://releases.aspose.com/psd/net/).

-  ไดเรกทอรีเอกสาร: ตั้งค่าไดเรกทอรีเพื่อจัดเก็บไฟล์ PSD ของคุณและอัปเดตไฟล์`dataDir` ตัวแปรในข้อมูลโค้ดที่ให้มาพร้อมเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชัน Aspose.PSD เพิ่มเนมสเปซต่อไปนี้ลงในโค้ดของคุณ:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

ตอนนี้ เรามาแบ่งตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// โหลดไฟล์ PSD โดยใช้ Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: รับภาพแรสเตอร์

```csharp
// รับภาพแรสเตอร์จากไฟล์ PSD ที่โหลด
RasterCachedImage rasterImage = image;
```

## ขั้นตอนที่ 3: ปรับความสว่าง

```csharp
// ตั้งค่าความสว่าง ค่าความสว่างที่ยอมรับได้อยู่ในช่วง [-255, 255]
rasterImage.AdjustBrightness(-50);
```

## ขั้นตอนที่ 4: บันทึกรูปภาพที่แก้ไข

```csharp
// บันทึกภาพที่แก้ไขด้วยความสว่างที่ปรับแล้ว
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

ตอนนี้เราได้แจกแจงตัวอย่างออกเป็นขั้นตอนที่สามารถจัดการได้แล้ว คุณสามารถรวมการปรับความสว่างเข้ากับโปรเจ็กต์ .NET ของคุณโดยใช้ Aspose.PSD ได้อย่างราบรื่น

## บทสรุป

Aspose.PSD สำหรับ .NET ช่วยให้กระบวนการปรับใช้การปรับความสว่างในไฟล์ PSD ง่ายขึ้น ด้วยการทำตามคำแนะนำทีละขั้นตอนข้างต้น คุณสามารถเพิ่มความน่าดึงดูดให้กับภาพของคุณได้อย่างง่ายดาย ทดลองใช้ค่าความสว่างต่างๆ เพื่อให้ได้ผลลัพธ์ที่ต้องการ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสารสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A1: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/psd/net/).

### คำถามที่ 2: ฉันจะดาวน์โหลดไลบรารี Aspose.PSD สำหรับ .NET ได้อย่างไร

 A2: คุณสามารถดาวน์โหลดไลบรารีได้จากไฟล์[หน้าปล่อย](https://releases.aspose.com/psd/net/).

### คำถามที่ 3: Aspose.PSD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

 A4: สำหรับการสนับสนุน โปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A5: คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
