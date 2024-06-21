---
title: อ่านรายการแท็ก EXIF ทั้งหมดใน Java
linktitle: อ่านรายการแท็ก EXIF ทั้งหมดใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีแยกข้อมูลเมตา EXIF จากไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java พร้อมบทช่วยสอนและตัวอย่างโค้ดที่ครอบคลุมของเรา
type: docs
weight: 16
url: /th/java/java-jpeg-image-processing/read-all-exif-tag-list-java/
---
### การแนะนำ
ในขอบเขตของการพัฒนา Java การจัดการและการจัดการไฟล์ PSD ถือเป็นข้อกำหนดที่สำคัญสำหรับหลาย ๆ แอปพลิเคชัน Aspose.PSD สำหรับ Java มอบโซลูชันที่มีประสิทธิภาพสำหรับการจัดการไฟล์ Photoshop Document (PSD) โดยทางโปรแกรม ทำให้นักพัฒนามีชุดเครื่องมือในการอ่าน เขียน และแก้ไขไฟล์ PSD ได้อย่างราบรื่น บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการอ่านแท็ก EXIF ทั้งหมดจากไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ในตอนท้าย คุณจะมีความเข้าใจที่ชัดเจนเกี่ยวกับวิธีการแยกและใช้ข้อมูลเมตา EXIF ที่ฝังอยู่ในรูปภาพ PSD
### ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอนนี้ ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:
- ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE) เช่น IntelliJ IDEA หรือ Eclipse
-  ดาวน์โหลด Aspose.PSD สำหรับไลบรารี Java แล้ว คุณสามารถรับได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).
## แพ็คเกจนำเข้า
ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นจาก Aspose.PSD สำหรับ Java ในโปรเจ็กต์ของคุณ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import java.util.Properties;
```
## ขั้นตอนที่ 1: โหลดไฟล์ PSD
 ขั้นแรก ให้โหลดไฟล์ PSD ลงในไฟล์`PsdImage` วัตถุ:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "example.psd");
```
## ขั้นตอนที่ 2: ทำซ้ำทรัพยากรรูปภาพ
จากนั้นวนซ้ำทรัพยากรรูปภาพเพื่อค้นหาข้อมูล EXIF :
```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null) {
            // ประมวลผลคุณสมบัติข้อมูล EXIF
            for(int j = 0; j < exifData.getProperties().length; j++) {
                System.out.println(exifData.getProperties()[j].getId() + ": " + exifData.getProperties()[j].getValue());
            }
        }
    }
}
```

## บทสรุป
โดยสรุป การใช้ประโยชน์จาก Aspose.PSD สำหรับ Java ช่วยลดความยุ่งยากในการแยกข้อมูลเมตา EXIF จากไฟล์ PSD บทช่วยสอนนี้ได้จัดเตรียมขั้นตอนที่จำเป็นเพื่อรวมฟังก์ชันนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น
## คำถามที่พบบ่อย
### Aspose.PSD สำหรับ Java คืออะไร
Aspose.PSD สำหรับ Java เป็นไลบรารีที่ช่วยให้นักพัฒนา Java สามารถทำงานกับไฟล์ PSD ได้โดยไม่จำเป็นต้องติดตั้ง Photoshop
### ฉันจะหาเอกสารประกอบ Aspose.PSD สำหรับ Java ได้ที่ไหน
 คุณสามารถค้นหาเอกสาร[ที่นี่](https://reference.aspose.com/psd/java/).
### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร
 เยี่ยม[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับตัวเลือกใบอนุญาตชั่วคราว
### Aspose.PSD สำหรับ Java รองรับการเขียนไฟล์ PSD หรือไม่
ใช่ รองรับทั้งการอ่านและการเขียนไฟล์ PSD
### ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน
 สำหรับการสนับสนุนโปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).