---
date: 2026-01-01
description: เรียนรู้วิธีสร้างเมตาดาต้า XMP, เพิ่ม XMP ไปยังไฟล์ PSD, และอัปเดตเมตาดาต้าภาพด้วย
  Aspose.PSD สำหรับ Java. ติดตามคู่มือขั้นตอนต่อขั้นตอนนี้ทันที.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: สร้างเมตาดาต้า XMP ด้วย Aspose.PSD สำหรับ Java
url: /th/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง XMP Metadata ด้วย Aspose.PSD สำหรับ Java

## บทนำ

การจัดการเมตาดาต้าของภาพเป็นความต้องการทั่วไปสำหรับนักพัฒนา Java ที่ทำงานกับไฟล์ Photoshop (PSD) ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีสร้าง XMP metadata** ด้วยไลบรารี Aspose.PSD, เพิ่ม XMP ลงในภาพ PSD, และอัปเดตเมตาดาต้าของภาพโดยอัตโนมัติ เราจะเดินผ่านแต่ละขั้นตอน, อธิบายว่าทำไมแต่ละส่วนจึงสำคัญ, และให้เคล็ดลับที่คุณสามารถนำไปใช้ในโครงการจริงได้

## คำตอบสั้น
- **XMP metadata คืออะไร?** รูปแบบมาตรฐานสำหรับฝังข้อมูลอธิบาย (ผู้เขียน, คำสำคัญ ฯลฯ) ไว้ในไฟล์ภาพ  
- **ทำไมต้องใช้ Aspose.PSD?** มันให้ API แบบ pure‑Java สำหรับสร้าง, อ่าน, และแก้ไขไฟล์ PSD โดยไม่ต้องใช้ Photoshop  
- **ฉันสามารถเพิ่ม XMP ลงใน PSD ที่มีอยู่ได้หรือไม่?** ได้ – คุณสามารถอัปเดตเมตาดาต้าของภาพได้ทันทีด้วย `setXmpData`  
- **ขั้นตอนหลักมีอะไรบ้าง?** ตั้งค่าขนาดภาพ, สร้าง header/trailer, สร้างแพ็กเกจ XMP, แนบเข้าไป, แล้วบันทึก  
- **ต้องมีลิขสิทธิ์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง

## “สร้าง XMP metadata” ใน Java หมายถึงอะไร?

การสร้าง XMP metadata หมายถึงการประกอบแพ็กเกจ XMP (header, body, trailer) ที่อธิบายภาพและจากนั้นฝังแพ็กเกจนั้นลงในไฟล์ PSD ไลบรารี Aspose.PSD จะจัดการรายละเอียดระดับต่ำให้คุณโฟกัสที่เนื้อหาที่ต้องการจัดเก็บ

## ทำไมต้องเพิ่ม XMP ลงในไฟล์ PSD?

- **การค้นหา:** ทำให้สามารถค้นหาไฟล์ตามผู้เขียน, ชื่อเรื่อง หรือแท็กที่กำหนดเองได้อย่างมีประสิทธิภาพ  
- **ความเข้ากันได้:** XMP ถูกยอมรับโดยผลิตภัณฑ์ของ Adobe, Lightroom, และระบบ DAM จำนวนมาก  
- **การควบคุมเวอร์ชัน:** เก็บประวัติการประมวลผล (เช่น เมือง, โหมดสี) ไว้ในไฟล์โดยตรง

## ข้อกำหนดเบื้องต้น

- **สภาพแวดล้อมการพัฒนา Java:** ติดตั้ง JDK 8 หรือสูงกว่าและมีความเข้าใจพื้นฐานของ Java  
- **ไลบรารี Aspose.PSD:** ดาวน์โหลดและตั้งค่า Aspose.PSD for Java คุณสามารถหาไลบรารีและเอกสารรายละเอียดได้ [ที่นี่](https://reference.aspose.com/psd/java/)  
- **ไดเรกทอรีเอกสารของคุณ:** กำหนดตำแหน่งที่คุณจะอ่าน/เขียนไฟล์ PSD บนระบบของคุณ

## นำเข้าแพ็กเกจ

ในโปรเจกต์ Java ของคุณ ให้นำเข้าแพ็กเกจที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.PSD:

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

กำหนดมิติของแคนวาสสำหรับภาพ PSD ใหม่

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## ขั้นตอนที่ 2: สร้างภาพใหม่

สร้างภาพ PSD ว่างเปล่าที่เราจะเติมข้อมูล XMP ลงในภายหลัง

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## ขั้นตอนที่ 3: สร้าง XMP Header

Header จะประกอบด้วยคำสั่งประมวลผล XML เปิดและ GUID ที่ระบุเอกสาร

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## ขั้นตอนที่ 4: สร้าง XMP Trailer

Trailer ทำเครื่องหมายจบแพ็กเกจ XMP การตั้งค่า `true` จะเขียนคำสั่งประมวลผลปิด

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## ขั้นตอนที่ 5: สร้าง XMP Metadata

เพิ่มแอตทริบิวต์ทั่วไปเช่นผู้เขียนและคำอธิบายลงในอ็อบเจ็กต์ XMP metadata หลัก

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## ขั้นตอนที่ 6: สร้าง XMP Packet Wrapper

ห่อ Header, Trailer, และเมตาดาต้าแกนไว้ในแพ็กเกจเดียวที่สามารถแนบเข้ากับภาพได้

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## ขั้นตอนที่ 7: ตั้งค่า Photoshop Attributes

เติมฟิลด์เฉพาะของ Photoshop (เมือง, ประเทศ, โหมดสี) ที่เครื่องมือ Adobe หลายตัวคาดหวัง

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## ขั้นตอนที่ 8: เพิ่ม Photoshop Package ลงใน XMP Metadata

แนบแพ็กเกจ Photoshop เข้าไปในแพ็กเกจ XMP

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## ขั้นตอนที่ 9: ตั้งค่า DublinCore Attributes

เพิ่มเมตาดาต้า Dublin Core เช่นผู้เขียน, ชื่อเรื่อง, และแท็กภาพยนตร์ที่กำหนดเอง

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## ขั้นตอนที่ 10: เพิ่ม DublinCore Package ลงใน XMP Metadata

รวมแพ็กเกจ Dublin Core กับแพ็กเกจ XMP ที่มีอยู่

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## ขั้นตอนที่ 11: อัปเดต XMP Metadata ลงในภาพ

ตอนนี้ให้ฝังแพ็กเกจ XMP ที่สมบูรณ์ลงในภาพ PSD

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## ขั้นตอนที่ 12: บันทึกภาพ

สุดท้ายให้เขียนไฟล์ PSD ลงดิสก์ (หรือสตรีมหน่วยความจำ) เพื่อให้เมตาดาต้าถูกบันทึก

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| **`NullPointerException` ที่ `setXmpData`** | แพ็กเกจ XMP ไม่ได้สร้างครบ (ขาด Header/Trailer) | ตรวจสอบให้แน่ใจว่าคุณสร้าง `XmpHeaderPi`, `XmpTrailerPi` และเพิ่มทุกแพ็กเกจก่อนเรียก `setXmpData` |
| **เมตาดาต้าไม่แสดงใน Photoshop** | Photoshop คาดหวังให้แพ็กเกจ XMP ถูกห่ออย่างถูกต้อง | ยืนยันว่าใช้ `XmpTrailerPi(true)` และแพ็กเกจถูกบันทึกพร้อมกับภาพ |
| **ข้อผิดพลาดเส้นทางไฟล์** | ใช้เส้นทางสัมพันธ์โดยไม่มีสิทธิ์ที่เหมาะสม | ใช้เส้นทางเต็มหรือให้แน่ใจว่าแอปมีสิทธิ์เขียนในโฟลเดอร์เป้าหมาย |

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD รองรับรูปแบบไฟล์ภาพต่าง ๆ หรือไม่?**  
ตอบ: ใช่, Aspose.PSD รองรับ PSD, PSB, BMP, GIF, JPEG, PNG, TIFF และอื่น ๆ ทำให้คุณมีความยืดหยุ่นในการทำงานกับหลายรูปแบบ

**ถาม: สามารถจัดการเมตาดาต้าที่มีอยู่แล้วด้วย Aspose.PSD ได้หรือไม่?**  
ตอบ: แน่นอน. คุณสามารถโหลด PSD ที่มีอยู่, ดึงข้อมูล XMP ด้วย `getXmpData()`, แก้ไขแพ็กเกจ, แล้วบันทึกกลับได้

**ถาม: มีข้อจำกัดเรื่องขนาดภาพที่ Aspose.PSD สามารถจัดการได้หรือไม่?**  
ตอบ: Aspose.PSD ถูกออกแบบให้ทำงานกับภาพขนาดใหญ่ (ถึงหลายกิกะพิกเซล) โดยจำกัดเพียงหน่วยความจำที่มีอยู่

**ถาม: มีเวอร์ชันทดลองของ Aspose.PSD หรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจความสามารถของ Aspose.PSD ได้โดยรับเวอร์ชันทดลองฟรี [ที่นี่](https://releases.aspose.com/)

**ถาม: จะขอรับการสนับสนุนสำหรับคำถามเกี่ยวกับ Aspose.PSD ได้จากที่ไหน?**  
ตอบ: สำหรับความช่วยเหลือหรือคำถามใด ๆ ให้เยี่ยมชม [ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34)

## สรุป

คุณได้เรียนรู้ **วิธีสร้าง XMP metadata**, เพิ่ม XMP ลงใน PSD, และอัปเดตเมตาดาต้าของภาพด้วย Aspose.PSD for Java ขั้นตอนเหล่านี้ให้คุณควบคุมข้อมูลอธิบายที่ฝังอยู่ในภาพได้อย่างเต็มที่ ทำให้ภาพของคุณค้นหาได้ง่ายและพร้อมสำหรับกระบวนการทำงานต่อไป อย่าลังเลที่จะทดลองใช้สคีม่า XMP เพิ่มเติมหรือผสานโค้ดนี้เข้ากับไพป์ไลน์การประมวลผลภาพขนาดใหญ่ของคุณ

---

**อัปเดตล่าสุด:** 2026-01-01  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}