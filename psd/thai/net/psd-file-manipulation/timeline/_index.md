---
title: การทำงานกับไทม์ไลน์ใน Aspose.PSD สำหรับ .NET
linktitle: การทำงานกับไทม์ไลน์
second_title: Aspose.PSD .NET API
description: ปรับปรุงการจัดการภาพ PSD ด้วย Aspose.PSD สำหรับคลาส .NET Timeline ควบคุมคุณสมบัติของเฟรม สถานะของเลเยอร์ และปลดปล่อยความเป็นไปได้ที่สร้างสรรค์ได้อย่างง่ายดาย
weight: 16
url: /th/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การทำงานกับไทม์ไลน์ใน Aspose.PSD สำหรับ .NET

## การแนะนำ
ในโลกแบบไดนามิกของการออกแบบกราฟิกและการจัดการรูปภาพ ความสามารถในการควบคุมและจัดการไทม์ไลน์ของรูปภาพถือเป็นสิ่งสำคัญ Aspose.PSD สำหรับ .NET มอบโซลูชันอันทรงพลังด้วยคลาสไทม์ไลน์ คุณลักษณะระดับสูงนี้ช่วยให้ผู้ใช้สามารถเปลี่ยนแปลงไทม์ไลน์ของ PsdImage ได้ เช่น การแก้ไขการหน่วงเวลาของเฟรม การแก้ไขสถานะของเลเยอร์ในเฟรมที่ระบุ และอื่นๆ
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเจาะลึกความเป็นไปได้อันน่าตื่นเต้นที่คลาสไทม์ไลน์นำเสนอ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.PSD สำหรับไลบรารี .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[Aspose.PSD สำหรับเอกสาร .NET](https://reference.aspose.com/psd/net/).
-  ไดเร็กทอรีเอกสารและเอาต์พุต: กำหนดเส้นทางสำหรับเอกสารและไดเร็กทอรีเอาต์พุตของคุณในโค้ด ปรับ`baseDir` และ`outputDir` ตัวแปรตามโครงสร้างโครงการของคุณ
ตอนนี้ เรามาสำรวจวิธีการใช้คลาสไทม์ไลน์ทีละขั้นตอนกันดีกว่า
## นำเข้าเนมสเปซ
หากต้องการเริ่มทำงานกับคลาส Timeline ให้นำเข้าเนมสเปซที่จำเป็นในโค้ดของคุณ:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## ขั้นตอนที่ 1: โหลดรูปภาพ PSD
เริ่มต้นด้วยการโหลดรูปภาพ PSD จากไฟล์ต้นฉบับที่ระบุ ตรวจสอบให้แน่ใจว่าได้ตั้งค่าพาธของไฟล์ต้นฉบับอย่างถูกต้อง:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //รหัสของคุณสำหรับการดำเนินการเพิ่มเติมอยู่ที่นี่
}
```
## ขั้นตอนที่ 2: เข้าถึงไทม์ไลน์
เมื่อโหลดรูปภาพ PSD แล้ว ให้เข้าถึงไทม์ไลน์โดยใช้โค้ดต่อไปนี้:
```csharp
Timeline timeline = psdImage.Timeline;
```
## ขั้นตอนที่ 3: เปลี่ยนวิธีการกำจัด
จัดการวิธีการกำจัดของเฟรมเฉพาะ ในตัวอย่างนี้ เราเปลี่ยนวิธีการกำจัดของเฟรม 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## ขั้นตอนที่ 4: ปรับการหน่วงเวลาของเฟรม
แก้ไขการหน่วงเวลาของเฟรมใดเฟรมหนึ่ง ที่นี่เราเปลี่ยนการหน่วงเวลาของเฟรม 2 เป็น 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## ขั้นตอนที่ 5: แก้ไขสถานะเลเยอร์
เปลี่ยนความทึบของ 'เลเยอร์ 1' บนเฟรมที่ต้องการ ในกรณีนี้ เราตั้งค่าความทึบเป็น 50 ในเฟรมที่ 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## ขั้นตอนที่ 6: ย้ายเลเยอร์
ย้าย 'เลเยอร์ 1' ไปที่มุมล่างซ้ายบนเฟรมเฉพาะ (เฟรม 3 ในตัวอย่างนี้):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## ขั้นตอนที่ 7: เพิ่มเฟรมใหม่
เพิ่มเฟรมใหม่ให้กับไทม์ไลน์:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## ขั้นตอนที่ 8: เปลี่ยนโหมดการผสมผสาน
เปลี่ยนโหมดการผสมผสานของ 'เลเยอร์ 1' บนเฟรมเฉพาะ (เฟรม 4 ในกรณีนี้):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## ขั้นตอนที่ 9: บันทึกการเปลี่ยนแปลง
ใช้การเปลี่ยนแปลงกลับไปยังอินสแตนซ์ PsdImage และบันทึกรูปภาพ PSD ที่แก้ไข:
```csharp
psdImage.Save(outputPsd);
```
## ขั้นตอนที่ 10: ทำความสะอาด
สุดท้าย ให้ล้างข้อมูลโดยการลบไฟล์เอาต์พุตชั่วคราว:
```csharp
File.Delete(outputPsd);
```
## บทสรุป

โดยสรุป คลาสไทม์ไลน์ใน Aspose.PSD สำหรับ .NET ช่วยให้นักพัฒนาสามารถควบคุมไทม์ไลน์ของรูปภาพ PSD ได้อย่างละเอียด ด้วยขั้นตอนง่ายๆ หลายขั้นตอน คุณสามารถจัดการคุณสมบัติของเฟรม สถานะของเลเยอร์ และอื่นๆ อีกมากมาย เพื่อเปิดขอบเขตความเป็นไปได้ที่สร้างสรรค์

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ .NET เหมาะสำหรับผู้เริ่มต้นหรือไม่

A1: แน่นอน! Aspose.PSD สำหรับ .NET มีอินเทอร์เฟซที่เป็นมิตรต่อผู้ใช้และเอกสารประกอบที่ครอบคลุม ทำให้ทั้งผู้เริ่มต้นและนักพัฒนาที่มีประสบการณ์สามารถเข้าถึงได้

### คำถามที่ 2: ฉันสามารถใช้การเปลี่ยนแปลงไทม์ไลน์กับรูปภาพ GIF ได้หรือไม่

A2: คลาสไทม์ไลน์ได้รับการออกแบบมาโดยเฉพาะสำหรับรูปภาพ PSD สำหรับการปรับแต่ง GIF โปรดดูที่ Aspose.GIF สำหรับ .NET

### คำถามที่ 3: ฉันจะรับการสนับสนุนเพิ่มเติมหรือหารือเกี่ยวกับปัญหาได้จากที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนชุมชนและการอภิปรายประเด็นต่างๆ

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A4: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ประโยชน์หลักของการใช้ Aspose.PSD สำหรับ .NET คืออะไร

A5: Aspose.PSD สำหรับ .NET นำเสนอความสามารถในการประมวลผลภาพขั้นสูง การจัดการไฟล์ PSD และการเรนเดอร์ประสิทธิภาพสูง
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
