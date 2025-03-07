---
title: รองรับทรัพยากรสีพื้นหลังใน Aspose.PSD สำหรับ .NET
linktitle: สนับสนุนทรัพยากรสีพื้นหลัง
second_title: Aspose.PSD .NET API
description: Master Aspose.PSD สำหรับ .NET พร้อมคำแนะนำทีละขั้นตอนของเรา จัดการภาพ PSD ได้อย่างง่ายดาย ดาวน์โหลดทดลองใช้ฟรีตอนนี้!
weight: 10
url: /th/net/psd-file-resources/supporting-background-color-resource/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับทรัพยากรสีพื้นหลังใน Aspose.PSD สำหรับ .NET

## การแนะนำ
ปลดล็อกศักยภาพทั้งหมดของ Aspose.PSD สำหรับ .NET ในขณะที่เราเจาะลึกบทช่วยสอนที่ครอบคลุม คู่มือนี้จะช่วยให้คุณมีความรู้ในการใช้ประโยชน์จากความสามารถของ Aspose.PSD ได้อย่างมีประสิทธิภาพ ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเป็นมือใหม่ โปรดปฏิบัติตามในขณะที่เราแบ่งแต่ละแง่มุมออกเป็นขั้นตอนที่สามารถจัดการได้ เพื่อให้การเดินทางของคุณกับ Aspose.PSD ราบรื่น
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มต้นการเดินทางครั้งนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- Visual Studio: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Visual Studio บนเครื่องของคุณแล้ว
-  Aspose.PSD สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD สำหรับ .NET จาก[เผยแพร่](https://releases.aspose.com/psd/net/).
## นำเข้าเนมสเปซ
ในโครงการ Visual Studio ของคุณ ให้เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็น:
```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Resources;
using System;
using System.IO;
```
## 1. ตั้งค่าโครงการของคุณ
สร้างโครงการใหม่ใน Visual Studio และอ้างอิงไลบรารี Aspose.PSD ตั้งค่าไดเรกทอรีเอกสารและเอาต์พุตของคุณ:
```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```
## 2. โหลดรูปภาพ PSD
โหลดภาพ PSD ของคุณโดยใช้รหัสต่อไปนี้:
```csharp
string sourceFilePath = Path.Combine(SourceDir, "YourInputFile.psd");
string outputFilePath = Path.Combine(OutputDir, "YourOutputFile.psd");
using (var image = (PsdImage)Image.Load(sourceFilePath))
{
    // รหัสของคุณที่นี่
}
```
## 3. การสนับสนุน BackgroundColorResource
ในตัวอย่างนี้ เราจะเน้นที่การสนับสนุนของ BackgroundColorResource ทรัพยากรนี้ช่วยให้คุณสามารถปรับแต่งสีพื้นหลังได้ 
```csharp
//ExStart: SupportOfBackgroundColorResource
string sourceFilePath = Path.Combine(SourceDir, "BackgroundColorResourceInput.psd");
string outputFilePath = Path.Combine(OutputDir, "BackgroundColorResourceOutput.psd");
using (var image = (PsdImage)Image.Load(sourceFilePath))
{
    ResourceBlock[] imageResources = image.ImageResources;
    BackgroundColorResource backgroundColorResource = null;
    
    // ทำซ้ำผ่านแหล่งข้อมูลรูปภาพ
    foreach (var imageResource in imageResources)
    {
        if (imageResource is BackgroundColorResource)
        {
            backgroundColorResource = (BackgroundColorResource)imageResource;
            break;
        }
    }
    // อัปเดต BackgroundColorResource
    backgroundColorResource.Color = Color.DarkRed;
    // บันทึกภาพที่แก้ไข
    image.Save(outputFilePath);
}
//ตัวอย่าง: SupportOfBackgroundColorResource
Console.WriteLine("SupportOfBackgroundColorResource executed successfully");
```
## บทสรุป
ยินดีด้วย! คุณจัดการ BackgroundColorResource ในภาพ PSD ของคุณสำเร็จแล้วโดยใช้ Aspose.PSD สำหรับ .NET นี่เป็นเพียงจุดเริ่มต้นของสิ่งที่คุณสามารถทำได้ด้วยไลบรารีอันทรงพลังนี้

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับ PSD เวอร์ชันทั้งหมดหรือไม่

คำตอบ 1: Aspose.PSD รองรับ PSD เวอร์ชันต่างๆ มากมาย จึงรับประกันความเข้ากันได้กับไฟล์ส่วนใหญ่

### คำถามที่ 2: ฉันสามารถใช้ Aspose.PSD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

A2: ได้ คุณสามารถใช้ Aspose.PSD ได้ทั้งในโครงการเชิงพาณิชย์และไม่ใช่เชิงพาณิชย์ ตรวจสอบ[หน้าซื้อ](https://purchase.aspose.com/buy) สำหรับรายละเอียดใบอนุญาต

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนจากชุมชนหรือสำรวจตัวเลือกการสนับสนุนระดับพรีเมียม

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถทดลองใช้งานฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: จะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A5: ทำตามขั้นตอนใน[หน้าใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
