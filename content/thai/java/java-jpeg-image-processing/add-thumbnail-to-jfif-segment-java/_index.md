---
title: เพิ่มรูปขนาดย่อให้กับกลุ่ม JFIF ใน Java
linktitle: เพิ่มรูปขนาดย่อให้กับกลุ่ม JFIF ใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มภาพขนาดย่อให้กับรูปภาพ PSD ใน Java โดยใช้ Aspose.PSD ทีละขั้นตอน เหมาะสำหรับนักพัฒนา Java ที่ต้องการเพิ่มความสามารถในการประมวลผลภาพ
type: docs
weight: 11
url: /th/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
---
## การแนะนำ
ในขอบเขตของการพัฒนา Java การบูรณาการความสามารถในการประมวลผลภาพเป็นสิ่งสำคัญสำหรับแอปพลิเคชันต่างๆ ตั้งแต่การปรับแต่งรูปภาพอย่างง่ายไปจนถึงงานออกแบบกราฟิกที่ซับซ้อน Aspose.PSD สำหรับ Java โดดเด่นในฐานะไลบรารีอันทรงพลังที่ออกแบบมาเพื่อจัดการไฟล์ PSD (เอกสาร Photoshop) ได้อย่างง่ายดาย บทช่วยสอนนี้มุ่งเน้นไปที่งานเฉพาะ: การเพิ่มภาพขนาดย่อให้กับส่วน JFIF ของรูปภาพโดยใช้ Aspose.PSD สำหรับ Java ในตอนท้ายของคู่มือนี้ คุณจะได้เรียนรู้วิธีดำเนินการทีละขั้นตอนนี้ เพื่อให้มั่นใจว่าคุณเข้าใจแต่ละส่วนได้อย่างละเอียด
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอนนี้ ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:
-  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ JDK ของออราเคิล](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
-  Aspose.PSD สำหรับ Java: คุณต้องมี Aspose.PSD สำหรับไลบรารี Java คุณสามารถรับได้จาก[หน้าดาวน์โหลด Java ของ Aspose.PSD](https://releases.aspose.com/psd/java/).
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE): ใช้ IDE เช่น IntelliJ IDEA หรือ Eclipse สำหรับการพัฒนา Java
- ความเข้าใจพื้นฐานของ Java: ความคุ้นเคยกับภาษาและแนวคิดการเขียนโปรแกรม Java
## แพ็คเกจนำเข้า
ก่อนที่คุณจะเริ่มเขียนโค้ด ให้นำเข้าแพ็คเกจที่จำเป็นเพื่อใช้ฟังก์ชัน Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## ขั้นตอนที่ 1: โหลดรูปภาพ PSD
ขั้นแรก โหลดรูปภาพ PSD ที่คุณต้องการเพิ่มภาพขนาดย่อ:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```
## ขั้นตอนที่ 2: ทำซ้ำทรัพยากรรูปภาพ
วนซ้ำทรัพยากรรูปภาพเพื่อค้นหาส่วน JFIF:
```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // ดำเนินการต่อด้วยการประมวลผลภาพขนาดย่อ
    }
}
```
## ขั้นตอนที่ 3: ปรับข้อมูลภาพขนาดย่อ
สร้างภาพขนาดย่อใหม่และเติมข้อมูลด้วย:
```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // กรอกข้อมูลภาพขนาดย่อ (ตัวอย่าง: สร้างอาร์เรย์พิกเซลแบบง่าย)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    //บันทึกข้อมูลภาพขนาดย่อ
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // ตั้งค่าข้อมูลภาพขนาดย่อเป็นตัวเลือก Jpeg
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // ตั้งค่าตัวเลือกให้กับทรัพยากรภาพขนาดย่อ
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // จัดการกับข้อยกเว้น
} finally {
    // กำจัดทรัพยากร
}
```
## ขั้นตอนที่ 4: บันทึกรูปภาพที่แก้ไข
สุดท้าย ให้บันทึกรูปภาพ PSD ที่แก้ไขแล้ว:
```java
image.save(dataDir + "output.psd");
```

## บทสรุป
โดยสรุป บทช่วยสอนนี้ได้แนะนำคุณตลอดขั้นตอนการเพิ่มภาพขนาดย่อไปยังส่วน JFIF ของรูปภาพ PSD โดยใช้ Aspose.PSD สำหรับ Java ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถปรับปรุงแอปพลิเคชัน Java ของคุณด้วยความสามารถในการประมวลผลภาพอันทรงพลังที่นำเสนอโดย Aspose.PSD
## คำถามที่พบบ่อย
### Aspose.PSD สำหรับ Java คืออะไร
Aspose.PSD สำหรับ Java เป็นไลบรารีที่ช่วยให้นักพัฒนา Java สามารถจัดการไฟล์ PSD โดยทางโปรแกรม
### ฉันจะหาเอกสารเพิ่มเติมเกี่ยวกับ Aspose.PSD สำหรับ Java ได้ที่ไหน
 เอกสารรายละเอียดสามารถดูได้ที่[Aspose.PSD สำหรับหน้าเอกสารประกอบ Java](https://reference.aspose.com/psd/java/).
### Aspose.PSD สำหรับ Java เหมาะสำหรับการใช้งานเชิงพาณิชย์หรือไม่
 ใช่ Aspose.PSD สำหรับ Java สามารถใช้ในเชิงพาณิชย์ได้ คุณสามารถซื้อใบอนุญาตได้จาก[หน้าการซื้อของ Aspose.PSD](https://purchase.aspose.com/buy).
### ฉันสามารถลองใช้ Aspose.PSD สำหรับ Java ก่อนซื้อได้หรือไม่
 ใช่ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้จาก[หน้าดาวน์โหลดรุ่นทดลองของ Aspose.PSD](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุน Aspose.PSD สำหรับ Java ได้อย่างไร
 สำหรับการสนับสนุนโปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).