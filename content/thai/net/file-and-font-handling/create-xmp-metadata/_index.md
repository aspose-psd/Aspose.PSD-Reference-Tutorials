---
title: การสร้างข้อมูลเมตา XMP ใน Aspose.PSD สำหรับ .NET
linktitle: การสร้างข้อมูลเมตา XMP
second_title: Aspose.PSD .NET API
description: สำรวจการสร้างข้อมูลเมตา XMP ใน Aspose.PSD สำหรับ .NET ปรับปรุงการจัดระเบียบรูปภาพด้วยการจัดการที่ราบรื่น
type: docs
weight: 10
url: /th/net/file-and-font-handling/create-xmp-metadata/
---
## การแนะนำ

ในโลกแบบไดนามิกของการพัฒนา .NET การจัดการรูปภาพด้วยความแม่นยำเป็นส่วนสำคัญของแอปพลิเคชันจำนวนมาก บทช่วยสอนนี้จะสำรวจการสร้างข้อมูลเมตา XMP ใน Aspose.PSD สำหรับ .NET ซึ่งเป็นไลบรารีอันทรงพลังที่ทำให้งานการประมวลผลภาพง่ายขึ้น XMP (Extensible Metadata Platform) ช่วยให้คุณสามารถฝังข้อมูลเมตาภายในไฟล์ภาพ อำนวยความสะดวกในการจัดระเบียบที่มีประสิทธิภาพ และการดึงข้อมูลที่เกี่ยวข้องกับภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจากไฟล์[เอกสาร Aspose.PSD](https://reference.aspose.com/psd/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ด้วย Visual Studio หรือ IDE ที่คุณต้องการ

- ความรู้พื้นฐานเกี่ยวกับ .NET: ทำความคุ้นเคยกับแนวคิดพื้นฐานของ .NET เนื่องจากบทช่วยสอนนี้ถือว่ามีความเข้าใจพื้นฐานของการพัฒนา .NET

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานของ Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

ตอนนี้ เรามาแจกแจงกระบวนการสร้างข้อมูลเมตา XMP ออกเป็นขั้นตอนที่ครอบคลุมต่างๆ

## ขั้นตอนที่ 1: ระบุขนาดภาพและสี่เหลี่ยมผืนผ้า

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//ระบุขนาดของภาพโดยการกำหนดสี่เหลี่ยมผืนผ้า
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## ขั้นตอนที่ 2: สร้างภาพใหม่

```csharp
// สร้างภาพใหม่เพื่อวัตถุประสงค์ในการเป็นตัวอย่าง
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // รหัสการจัดการรูปภาพอยู่ที่นี่...
}
```

## ขั้นตอนที่ 3: สร้าง XMP-Header และ XMP-Trailer

```csharp
// สร้างอินสแตนซ์ของ XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// สร้างอินสแตนซ์ของคลาส XMP-TrailerPi, XMPmeta เพื่อตั้งค่าแอตทริบิวต์ที่แตกต่างกัน
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## ขั้นตอนที่ 4: ตั้งค่าคุณสมบัติ XMP

```csharp
// ตั้งค่าแอ็ตทริบิวต์ XMP เช่น:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## ขั้นตอนที่ 5: สร้าง XMP Packet Wrapper

```csharp
// สร้างอินสแตนซ์ของ XmpPacketWrapper ที่มีข้อมูลเมตาทั้งหมด
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## ขั้นตอนที่ 6: สร้างแพ็คเกจ Photoshop และตั้งค่าคุณสมบัติ

```csharp
// สร้างอินสแตนซ์ของแพ็คเกจ Photoshop และตั้งค่าคุณสมบัติของ Photoshop
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## ขั้นตอนที่ 7: เพิ่มแพ็คเกจ Photoshop ลงในข้อมูลเมตา XMP

```csharp
// เพิ่มแพ็คเกจ Photoshop ลงในข้อมูลเมตา XMP
xmpData.AddPackage(photoshopPackage);
```

## ขั้นตอนที่ 8: สร้างแพ็คเกจ DublinCore และตั้งค่าคุณสมบัติ

```csharp
// สร้างอินสแตนซ์ของแพ็คเกจ DublinCore และตั้งค่าแอตทริบิวต์ dublinCore
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## ขั้นตอนที่ 9: เพิ่มแพ็คเกจ DublinCore ไปยังข้อมูลเมตา XMP

```csharp
// เพิ่มแพ็คเกจ dublinCore ลงในข้อมูลเมตา XMP
xmpData.AddPackage(dublinCorePackage);
```

## ขั้นตอนที่ 10: อัปเดตข้อมูลเมตา XMP และบันทึกรูปภาพ

```csharp
using (var ms = new MemoryStream())
{
    // อัปเดตข้อมูลเมตา XMP ลงในรูปภาพและบันทึกรูปภาพบนดิสก์หรือในสตรีมหน่วยความจำ
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## ขั้นตอนที่ 11: โหลดรูปภาพและอ่านข้อมูลเมตา

```csharp
// โหลดรูปภาพจากสตรีมหน่วยความจำหรือจากดิสก์เพื่ออ่าน/รับข้อมูลเมตา
using (var img = (PsdImage)Image.Load(ms))
{
    // รับข้อมูลเมตา XMP
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // ใช้ข้อมูลแพ็กเกจ...
    }
}
```

## บทสรุป

ยินดีด้วย! คุณสร้างข้อมูลเมตา XMP ใน Aspose.PSD สำหรับ .NET สำเร็จแล้ว ความสามารถอันทรงพลังนี้ช่วยเพิ่มความสามารถในการประมวลผลภาพของคุณ ทำให้สามารถจัดระเบียบและดึงข้อมูลสำคัญได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ .NET เข้ากันได้กับรูปแบบภาพทุกรูปแบบหรือไม่

A1: Aspose.PSD เน้นที่รูปแบบไฟล์ PSD (Adobe Photoshop) เป็นหลัก แต่รองรับรูปแบบอื่นๆ มากมาย

### คำถามที่ 2: ฉันสามารถจัดการข้อมูลเมตา XMP ที่มีอยู่โดยใช้ Aspose.PSD สำหรับ .NET ได้หรือไม่

ตอบ 2: ได้ Aspose.PSD ช่วยให้คุณสามารถอ่านและแก้ไขข้อมูลเมตา XMP ที่มีอยู่ได้

### คำถามที่ 3: มีข้อจำกัดเกี่ยวกับขนาดรูปภาพเมื่อใช้ Aspose.PSD สำหรับ .NET หรือไม่

A3: Aspose.PSD สามารถรองรับรูปภาพขนาดต่างๆ ได้ แต่รูปภาพที่มีขนาดใหญ่มากอาจต้องมีการพิจารณาเพิ่มเติม

### คำถามที่ 4: Aspose.PSD สำหรับ .NET อัปเดตบ่อยแค่ไหน

ตอบ 4: มีการเผยแพร่การอัปเดตเป็นประจำเพื่อให้มั่นใจว่าเข้ากันได้กับเวอร์ชันเฟรมเวิร์ก .NET ล่าสุดและมาตรฐานอุตสาหกรรม

### คำถามที่ 5: มีฟอรัมชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่

 ตอบ: ได้ คุณสามารถค้นหาการสนับสนุนและการสนทนาได้จากเว็บไซต์[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).