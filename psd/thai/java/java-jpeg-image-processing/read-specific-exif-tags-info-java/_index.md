---
title: อ่านข้อมูลแท็ก EXIF เฉพาะใน Java
linktitle: อ่านข้อมูลแท็ก EXIF เฉพาะใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีอ่านแท็ก EXIF เฉพาะจากรูปภาพ PSD โดยใช้ Aspose.PSD สำหรับ Java พร้อมบทช่วยสอนทีละขั้นตอนของเรา เสริมทักษะการประมวลผลภาพของคุณ
weight: 19
url: /th/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# อ่านข้อมูลแท็ก EXIF เฉพาะใน Java

## การแนะนำ
คุณกำลังมองหาที่จะดำดิ่งสู่โลกแห่งการจัดการไฟล์ PSD ด้วย Java หรือไม่? หากคุณต้องการเข้าใจวิธีอ่านแท็ก EXIF เฉพาะจากรูปภาพ PSD คุณมาถูกที่แล้ว บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทั้งหมดโดยใช้ Aspose.PSD สำหรับ Java ตั้งแต่การตั้งค่าสภาพแวดล้อมของคุณไปจนถึงการแยกข้อมูล EXIF โดยละเอียด มาเริ่มกันเลย!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกโค้ด มีบางสิ่งที่คุณต้องเตรียม:
1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ออราเคิล JDK](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD สำหรับ Java: ดาวน์โหลดไลบรารีจาก[ที่นี่](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): IDE เช่น IntelliJ IDEA, Eclipse หรือ NetBeans จะทำให้การเขียนโค้ดสะดวกยิ่งขึ้น
4. ไฟล์ PSD: ไฟล์ PSD ที่มีข้อมูล EXIF คุณสามารถใช้ตัวอย่างที่ให้ไว้ในบทช่วยสอนนี้หรือไฟล์ PSD อื่นที่มีแท็ก EXIF
## แพ็คเกจนำเข้า
ขั้นแรก คุณจะต้องนำเข้าแพ็คเกจ Aspose.PSD ที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ ต่อไปนี้เป็นวิธีการตั้งค่า
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## ขั้นตอนที่ 1: โหลดรูปภาพ PSD
ในการเริ่มต้น คุณต้องโหลดไฟล์ PSD ของคุณลงในแอปพลิเคชัน ตรวจสอบให้แน่ใจว่าระบุเส้นทางไฟล์ของคุณอย่างถูกต้อง
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 ในขั้นตอนนี้ เราจะโหลดไฟล์ PSD โดยใช้นามสกุล`Image.load()` วิธี. ที่`PsdImage` คลาสใช้เพื่อแสดงรูปภาพ PSD และเราส่งรูปภาพที่โหลดไปยังคลาสนี้เพื่อเข้าถึงฟังก์ชันเฉพาะของ PSD
## ขั้นตอนที่ 2: ทำซ้ำทรัพยากรรูปภาพ
ตอนนี้ เราต้องวนซ้ำทรัพยากรรูปภาพเพื่อค้นหาทรัพยากรภาพขนาดย่อ ซึ่งโดยทั่วไปจะมีข้อมูล EXIF
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // การประมวลผลเพิ่มเติมจะดำเนินการที่นี่
    }
}
```
 เราวนซ้ำทรัพยากรรูปภาพโดยใช้`for` วนซ้ำ เป้าหมายคือการระบุทรัพยากรที่เป็นกรณีของ`ThumbnailResource` หรือ`Thumbnail4Resource`เนื่องจากเป็นประเภทที่เก็บข้อมูล EXIF
## ขั้นตอนที่ 3: แยกข้อมูล EXIF
เมื่อเราระบุทรัพยากรภาพขนาดย่อแล้ว เราจะแยกข้อมูล EXIF และพิมพ์ลงในคอนโซล
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```
 เราใช้อัน`if` คำสั่งเพื่อตรวจสอบว่าทรัพยากรเป็นอินสแตนซ์ของหรือไม่`ThumbnailResource` - หากเป็นเช่นนั้น เราก็โยนมันและดึงมันกลับมา`JpegOptions` เพื่อเข้าถึง`ExifData`สุดท้ายนี้ เราจะพิมพ์แท็ก EXIF ต่างๆ เช่น WhiteBalance, Pixel Dimensions, ISOSpeed และ FocalLength

## บทสรุป
เมื่อทำตามขั้นตอนเหล่านี้ คุณได้เรียนรู้วิธีอ่านแท็ก EXIF เฉพาะจากรูปภาพ PSD โดยใช้ Aspose.PSD สำหรับ Java กระบวนการนี้เกี่ยวข้องกับการโหลดรูปภาพ วนซ้ำทรัพยากร ระบุทรัพยากรภาพย่อ และแยกข้อมูล EXIF ด้วยความรู้นี้ คุณสามารถสำรวจและจัดการข้อมูล EXIF ในไฟล์ PSD ของคุณได้ ทำให้สามารถประมวลผลภาพที่ซับซ้อนมากขึ้นได้
## คำถามที่พบบ่อย
### ข้อมูล EXIF คืออะไร?
ข้อมูล EXIF (รูปแบบไฟล์ภาพที่แลกเปลี่ยนได้) คือข้อมูลเมตาที่ฝังอยู่ในไฟล์ภาพ ซึ่งมีข้อมูลต่างๆ เช่น การตั้งค่ากล้อง วันที่และเวลา และขนาดของภาพ
### ฉันสามารถแก้ไขข้อมูล EXIF โดยใช้ Aspose.PSD ได้หรือไม่
ใช่ Aspose.PSD ช่วยให้คุณสามารถอ่านและแก้ไขข้อมูล EXIF ได้ คุณสามารถอัปเดตแท็กและบันทึกการเปลี่ยนแปลงกลับไปยังไฟล์รูปภาพได้
### Aspose.PSD สำหรับ Java ฟรีหรือไม่
 Aspose.PSD มีเวอร์ชันทดลองใช้ฟรีซึ่งคุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/)- หากต้องการคุณสมบัติครบถ้วน คุณต้องซื้อใบอนุญาต
### Aspose.PSD รองรับรูปแบบอื่นใดบ้าง
Aspose.PSD รองรับรูปแบบ Adobe Photoshop หลากหลาย รวมถึง PSD, PSB และอื่นๆ นอกจากนี้ยังมีตัวเลือกในการแปลงรูปแบบเหล่านี้เป็นรูปแบบอื่น เช่น PNG, JPEG, TIFF เป็นต้น
### ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร
 คุณสามารถรับการสนับสนุนผ่าน Aspose.PSD[ฟอรั่ม](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
