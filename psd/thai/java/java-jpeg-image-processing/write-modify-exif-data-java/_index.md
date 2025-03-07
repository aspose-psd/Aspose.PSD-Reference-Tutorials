---
title: เขียนและแก้ไขข้อมูล EXIF ใน Java
linktitle: เขียนและแก้ไขข้อมูล EXIF ใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเขียนและแก้ไขข้อมูล EXIF ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java พร้อมคำแนะนำทีละขั้นตอนที่ครอบคลุมนี้
weight: 22
url: /th/java/java-jpeg-image-processing/write-modify-exif-data-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เขียนและแก้ไขข้อมูล EXIF ใน Java

## การแนะนำ
คุณต้องการจัดการข้อมูล EXIF ในไฟล์ PSD โดยใช้ Java หรือไม่? ถ้าใช่ แสดงว่าคุณมาถูกที่แล้ว! คู่มือที่ครอบคลุมนี้จะแนะนำคุณตลอดขั้นตอนในการเขียนและแก้ไขข้อมูล EXIF ใน Java โดยใช้ไลบรารี Aspose.PSD อันทรงพลัง 
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเจาะลึกโค้ด โปรดตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าทุกอย่างถูกต้องแล้ว
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว
2.  Aspose.PSD สำหรับ Java: ดาวน์โหลดไลบรารีจาก[ที่นี่](https://releases.aspose.com/psd/java/).
3. IDE: ใช้ IDE เช่น IntelliJ IDEA หรือ Eclipse เพื่อประสบการณ์การเขียนโค้ดที่ราบรื่น
4. ความรู้ Java ขั้นพื้นฐาน: จำเป็นต้องมีความคุ้นเคยกับการเขียนโปรแกรม Java
5.  กำหนดใบอนุญาตชั่วคราว: รับใบอนุญาตชั่วคราวจาก[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อปลดล็อกศักยภาพเต็มรูปแบบของ Aspose.PSD
## แพ็คเกจนำเข้า
ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณ ต่อไปนี้เป็นวิธีดำเนินการ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.exif.enums.ExifFlash;
import com.aspose.psd.exif.enums.ExifWhiteBalance;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
การนำเข้าเหล่านี้จะช่วยให้คุณสามารถทำงานกับไฟล์ PSD จัดการข้อมูล EXIF และใช้คุณสมบัติอันทรงพลังของ Aspose.PSD
ตอนนี้คุณได้ตั้งค่าทุกอย่างเรียบร้อยแล้ว เรามาแบ่งกระบวนการออกเป็นขั้นตอนง่ายๆ และปฏิบัติตามง่ายๆ กัน
## ขั้นตอนที่ 1: โหลดรูปภาพ PSD
ในการเริ่มต้น คุณต้องโหลดไฟล์ PSD ลงในโปรเจ็กต์ของคุณ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
ข้อมูลโค้ดนี้จะโหลดรูปภาพ PSD จากไดเรกทอรีที่คุณระบุ
## ขั้นตอนที่ 2: ทำซ้ำทรัพยากรรูปภาพ
ถัดไป คุณต้องวนซ้ำทรัพยากรรูปภาพเพื่อค้นหาทรัพยากรภาพขนาดย่อ นี่คือที่ที่ข้อมูล EXIF มักจะถูกจัดเก็บในรูปแบบ JPEG
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // ตรวจสอบทรัพยากรภาพขนาดย่อ
}
```
## ขั้นตอนที่ 3: ระบุทรัพยากรภาพขนาดย่อ
ในขั้นตอนนี้ คุณจะระบุทรัพยากรภาพขนาดย่อจากทรัพยากรภาพ
```java
if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
    // แยกข้อมูล EXIF จากทรัพยากรภาพขนาดย่อ
}
```
## ขั้นตอนที่ 4: แยกและพิมพ์ข้อมูล EXIF
เมื่อคุณระบุทรัพยากรภาพขนาดย่อแล้ว ขั้นตอนต่อไปคือการดึงข้อมูล EXIF และพิมพ์ลงในคอนโซล
```java
JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
if (exif != null) {
    // พิมพ์ข้อมูล EXIF
}
```
## ขั้นตอนที่ 5: แก้ไขข้อมูล EXIF
มาถึงส่วนที่สนุกแล้ว - การแก้ไขข้อมูล EXIF ต่อไปนี้คือวิธีที่คุณสามารถตั้งค่าข้อมูล LensMake, WhiteBalance และ Flash
```java
exif.setLensMake("Sony");
exif.setWhiteBalance(ExifWhiteBalance.Auto);
exif.setFlash(ExifFlash.Fired);
```
## ขั้นตอนที่ 6: บันทึกรูปภาพ
หลังจากทำการแก้ไขที่จำเป็นแล้ว ให้บันทึกรูปภาพเพื่อใช้การเปลี่ยนแปลง
```java
image.save(dataDir + "Modified_Zebras_Serengeti.psd");
```
## บทสรุป
และคุณก็ได้แล้ว! คุณได้เรียนรู้วิธีเขียนและแก้ไขข้อมูล EXIF ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้ทำให้การทำงานกับรูปแบบรูปภาพที่ซับซ้อนง่ายขึ้น ทำให้เป็นเครื่องมืออันมีค่าสำหรับนักพัฒนาที่ทำงานกับไฟล์กราฟิก 
 สำหรับข้อมูลโดยละเอียดเพิ่มเติม โปรดดูที่[เอกสาร Aspose.PSD](https://reference.aspose.com/psd/java/) - หากคุณพบปัญหาใดๆ[ฟอรั่มการสนับสนุน](https://forum.aspose.com/c/psd/34) เป็นสถานที่ที่ดีเยี่ยมในการขอความช่วยเหลือ อย่าลืมไปสำรวจ[ทดลองใช้ฟรี](https://releases.aspose.com/) และพิจารณาซื้อใบอนุญาต[ที่นี่](https://purchase.aspose.com/buy) เพื่อคุณสมบัติที่ครบครัน
## คำถามที่พบบ่อย
### ข้อมูล EXIF คืออะไร?
ข้อมูล EXIF (รูปแบบไฟล์ภาพที่แลกเปลี่ยนได้) คือข้อมูลเมตาที่ฝังอยู่ในไฟล์ภาพ ซึ่งมีข้อมูลต่างๆ เช่น การตั้งค่ากล้อง วันที่ เวลา และสถานที่
### Aspose.PSD สามารถจัดการรูปแบบรูปภาพอื่น ๆ ได้หรือไม่
ใช่ Aspose.PSD รองรับรูปแบบภาพที่หลากหลาย รวมถึง PNG, JPEG, BMP และ GIF
### Aspose.PSD สำหรับ Java ฟรีหรือไม่
คุณสามารถใช้รุ่นทดลองใช้ฟรีได้ แต่สำหรับฟีเจอร์ทั้งหมด คุณจะต้องซื้อใบอนุญาต
### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร
 คุณสามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
### ฉันสามารถใช้ Aspose.PSD สำหรับการประมวลผลภาพเป็นชุดได้หรือไม่
ได้ คุณสามารถประมวลผลภาพหลายภาพในชุดเดียวกันได้โดยใช้คุณสมบัติที่แข็งแกร่งของ Aspose.PSD
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
