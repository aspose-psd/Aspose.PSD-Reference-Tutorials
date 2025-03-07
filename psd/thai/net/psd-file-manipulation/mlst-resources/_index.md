---
title: การเรียนรู้การจัดการทรัพยากร MLST ใน Aspose.PSD สำหรับ .NET
linktitle: การจัดการทรัพยากร MLST
second_title: Aspose.PSD .NET API
description: เรียนรู้วิธีจัดการสถานะของเลเยอร์ในไฟล์ Photoshop ด้วย Aspose.PSD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการจัดการทรัพยากร MLST อย่างมีประสิทธิภาพ
weight: 14
url: /th/net/psd-file-manipulation/mlst-resources/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเรียนรู้การจัดการทรัพยากร MLST ใน Aspose.PSD สำหรับ .NET

## การแนะนำ
ยินดีต้อนรับสู่บทช่วยสอนเชิงลึกเกี่ยวกับการจัดการทรัพยากร MLST (สถานะหลายเลเยอร์) ใน Aspose.PSD สำหรับ .NET Aspose.PSD สำหรับ .NET เป็นไลบรารีอันทรงพลังที่ให้ความสามารถมากมายสำหรับการทำงานกับไฟล์ Photoshop ในบทช่วยสอนนี้ เราจะมุ่งเน้นไปที่การสนับสนุนทรัพยากร MLST โดยเสนอกลไกระดับต่ำเพื่อจัดการสถานะของเลเยอร์อย่างมีประสิทธิภาพ
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.PSD สำหรับ .NET Library: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีแล้ว ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[Aspose.PSD สำหรับหน้าดาวน์โหลด .NET](https://releases.aspose.com/psd/net/).
- ไดเร็กทอรีเอกสารและเอาท์พุต: ตั้งค่าไดเร็กทอรีเอกสารของคุณ (`baseDir`) และไดเรกทอรีผลลัพธ์ (`outputDir`) ในโค้ดที่ให้มา
## นำเข้าเนมสเปซ
ในโปรเจ็กต์ .NET ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose.PSD:
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures;
```
## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไดเรกทอรี
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" และ "Your Output Directory" ด้วยเส้นทางจริงในโครงการของคุณ
## ขั้นตอนที่ 2: โหลดรูปภาพ PSD
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
string outputPsd = Path.Combine(outputDir, "output_image1219.psd");
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    // รหัสสำหรับการจัดการจะถูกเพิ่มในขั้นตอนต่อไป
}
```
## ขั้นตอนที่ 3: เข้าถึงทรัพยากร MLST
```csharp
Layer layer1 = image.Layers[1];
ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
```
## ขั้นตอนที่ 4: จัดการสถานะเลเยอร์
```csharp
ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
// ปิดการใช้งานเลเยอร์ 1 บนเฟรม 1
layerEnabled.Value = false;
```
## ขั้นตอนที่ 5: บันทึกรูปภาพที่แก้ไข
```csharp
image.Save(outputPsd);
```
## ขั้นตอนที่ 6: ทำความสะอาด
```csharp
File.Delete(outputPsd);
Console.WriteLine("SupportOfMlstResource executed successfully");
```
## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีจัดการทรัพยากร MLST ใน Aspose.PSD สำหรับ .NET เรียบร้อยแล้ว คุณลักษณะนี้มีกลไกที่มีประสิทธิภาพในการจัดการสถานะของเลเยอร์ในไฟล์ Photoshop โดยทางโปรแกรม

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD สำหรับ .NET เพื่อทำงานกับไฟล์ PSD ที่สร้างใน Photoshop เวอร์ชันต่างๆ ได้หรือไม่

ตอบ 1: ใช่ Aspose.PSD สำหรับ .NET รองรับไฟล์ PSD ที่สร้างใน Photoshop เวอร์ชันต่างๆ

### คำถามที่ 2: Aspose.PSD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้จาก[หน้าเผยแพร่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.PSD สำหรับ .NET ได้ที่ไหน

A3: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/psd/net/).

### คำถามที่ 4: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A4: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อสนับสนุนชุมชน

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A5: คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
