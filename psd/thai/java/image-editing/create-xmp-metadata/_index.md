---
title: สร้างข้อมูลเมตา XMP ด้วย Aspose.PSD สำหรับ Java
linktitle: สร้างข้อมูลเมตา XMP
second_title: Aspose.PSD Java API
description: ปรับปรุงแอปพลิเคชัน Java ของคุณด้วย Aspose.PSD เรียนรู้การสร้างข้อมูลเมตา XMP ได้อย่างง่ายดาย ทำตามคำแนะนำทีละขั้นตอนของเราทันที
weight: 12
url: /th/java/image-editing/create-xmp-metadata/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างข้อมูลเมตา XMP ด้วย Aspose.PSD สำหรับ Java

## การแนะนำ

ในขอบเขตของการพัฒนา Java การจัดการและการจัดการข้อมูลเมตาของรูปภาพถือเป็นสิ่งสำคัญสำหรับแอปพลิเคชันต่างๆ Aspose.PSD สำหรับ Java โดดเด่นในฐานะเครื่องมืออันทรงพลังในการจัดการไฟล์ PSD และในบทช่วยสอนนี้ เราจะเจาะลึกในการสร้างข้อมูลเมตา XMP โดยใช้ไลบรารีที่มีประสิทธิภาพนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มบทช่วยสอนนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ติดตั้ง Java บนระบบของคุณ และมีความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ไลบรารี Aspose.PSD: ดาวน์โหลดและตั้งค่าไลบรารี Aspose.PSD สำหรับ Java คุณสามารถค้นหาห้องสมุดและเอกสารรายละเอียดได้[ที่นี่](https://reference.aspose.com/psd/java/).
- Your Document Directory: กำหนดไดเร็กทอรีที่เก็บไฟล์เอกสารของคุณ

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชัน Aspose.PSD:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## ขั้นตอนที่ 1: ระบุขนาดภาพ

```java
//ระบุขนาดของภาพโดยการกำหนดสี่เหลี่ยมผืนผ้า
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## ขั้นตอนที่ 2: สร้างภาพใหม่

```java
// สร้างภาพใหม่เพื่อจุดประสงค์ตัวอย่าง
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## ขั้นตอนที่ 3: สร้างส่วนหัว XMP

```java
// สร้างอินสแตนซ์ของ XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## ขั้นตอนที่ 4: สร้างตัวอย่าง XMP

```java
// สร้างอินสแตนซ์ของ Xmp-TrailerPi
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## ขั้นตอนที่ 5: สร้างข้อมูลเมตา XMP

```java
// สร้างอินสแตนซ์ของคลาส XMPmeta เพื่อตั้งค่าแอตทริบิวต์ที่แตกต่างกัน
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## ขั้นตอนที่ 6: สร้าง XMP Packet Wrapper

```java
// สร้างอินสแตนซ์ของ XmpPacketWrapper ที่มีข้อมูลเมตาทั้งหมด
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## ขั้นตอนที่ 7: ตั้งค่าคุณสมบัติ Photoshop

```java
// สร้างอินสแตนซ์ของแพ็คเกจ Photoshop และตั้งค่าคุณสมบัติ Photoshop
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## ขั้นตอนที่ 8: เพิ่มแพ็คเกจ Photoshop ลงในข้อมูลเมตา XMP

```java
// เพิ่มแพ็คเกจ Photoshop ลงในข้อมูลเมตา XMP
xmpData.addPackage(photoshopPackage);
```

## ขั้นตอนที่ 9: ตั้งค่าคุณสมบัติ DublinCore

```java
// สร้างอินสแตนซ์ของแพ็คเกจ DublinCore และตั้งค่าแอตทริบิวต์ DublinCore
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## ขั้นตอนที่ 10: เพิ่มแพ็คเกจ DublinCore ไปยังข้อมูลเมตา XMP

```java
// เพิ่มแพ็คเกจ DublinCore ลงในข้อมูลเมตา XMP
xmpData.addPackage(dublinCorePackage);
```

## ขั้นตอนที่ 11: อัปเดตข้อมูลเมตา XMP ลงในรูปภาพ

```java
//อัปเดตข้อมูลเมตา XMP ลงในรูปภาพ
image.setXmpData(xmpData);
```

## ขั้นตอนที่ 12: บันทึกรูปภาพ

```java
// บันทึกภาพบนดิสก์หรือในสตรีมหน่วยความจำ
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## บทสรุป

ยินดีด้วย! คุณสร้างข้อมูลเมตา XMP สำหรับรูปภาพโดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว บทช่วยสอนนี้ได้จัดเตรียมขั้นตอนที่จำเป็นในการปรับปรุงและจัดการข้อมูลเมตาในแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับรูปแบบรูปภาพที่แตกต่างกันหรือไม่

ตอบ 1: ใช่ Aspose.PSD รองรับรูปแบบรูปภาพที่หลากหลาย ซึ่งให้ความคล่องตัวในการจัดการไฟล์ประเภทต่างๆ

### คำถามที่ 2: ฉันสามารถจัดการข้อมูลเมตาที่มีอยู่โดยใช้ Aspose.PSD ได้หรือไม่

ตอบ 2: แน่นอน Aspose.PSD ช่วยให้คุณสามารถแก้ไขและอัปเดตข้อมูลเมตาที่มีอยู่ภายในรูปภาพได้

### คำถามที่ 3: มีข้อจำกัดเกี่ยวกับขนาดรูปภาพที่ Aspose.PSD สามารถรองรับได้หรือไม่

A3: Aspose.PSD ได้รับการออกแบบมาเพื่อจัดการรูปภาพขนาดต่างๆ ทำให้มั่นใจได้ถึงความสามารถในการปรับขนาดสำหรับโปรเจ็กต์ของคุณ

### คำถามที่ 4: Aspose.PSD มีเวอร์ชันทดลองใช้งานหรือไม่

 A4: ได้ คุณสามารถสำรวจความสามารถของ Aspose.PSD ได้โดยการทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับการสนับสนุนสำหรับการสอบถามที่เกี่ยวข้องกับ Aspose.PSD ได้ที่ไหน

 A5: สำหรับความช่วยเหลือหรือข้อสงสัยใดๆ โปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
