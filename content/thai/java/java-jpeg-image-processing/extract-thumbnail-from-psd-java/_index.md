---
title: แยกรูปขนาดย่อจาก PSD ใน Java
linktitle: แยกรูปขนาดย่อจาก PSD ใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีแยกภาพขนาดย่อจากไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java คำแนะนำทีละขั้นตอนนี้ครอบคลุมทุกอย่างตั้งแต่การตั้งค่าไปจนถึงการบันทึกภาพที่แยกออกมา
type: docs
weight: 15
url: /th/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## การแนะนำ
ในบทช่วยสอนนี้ เราจะสำรวจวิธีแยกภาพขนาดย่อจากไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ภาพขนาดย่อมีประโยชน์สำหรับการดูตัวอย่างอย่างรวดเร็วหรือสำหรับการสร้างรูปภาพขนาดเล็กที่ฝังอยู่ในเอกสาร PSD มาดูรายละเอียดขั้นตอนที่จำเป็นเพื่อให้บรรลุเป้าหมายนี้โดยใช้ Aspose.PSD กันดีกว่า
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าต่อไปนี้:
- ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
-  Aspose.PSD สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
## แพ็คเกจนำเข้า
ในการเริ่มต้น ให้รวมแพ็คเกจ Aspose.PSD ที่จำเป็นในคลาส Java ของคุณ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## ขั้นตอนที่ 1: โหลดไฟล์ PSD
ขั้นแรก ให้โหลดไฟล์ PSD ที่มีภาพขนาดย่อที่คุณต้องการแยก
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 แทนที่`"Your_Document_Directory/"` ด้วยเส้นทางไดเรกทอรีที่มีไฟล์ PSD ของคุณอยู่ และ`"your_file.psd"` พร้อมชื่อไฟล์ PSD ของคุณ
## ขั้นตอนที่ 2: ทำซ้ำทรัพยากรรูปภาพ
วนซ้ำทรัพยากรรูปภาพเพื่อค้นหาทรัพยากรภาพขนาดย่อ
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // แยกข้อมูลภาพขนาดย่อ
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // สร้างภาพใหม่ด้วยข้อมูลภาพขนาดย่อที่แยกออกมา
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // บันทึกภาพขนาดย่อที่แยกออกมาเป็นไฟล์ JPEG แยกต่างหาก
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // ข้อความแสดงความสำเร็จเอาท์พุต
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // ออกจากลูปเมื่อพบและประมวลผลภาพขนาดย่อแล้ว
    }
}
```
## ขั้นตอนที่ 3: บันทึกภาพขนาดย่อที่แยกออกมา
บันทึกภาพขนาดย่อที่แยกออกมาเป็นไฟล์ภาพแยกต่างหาก (ในกรณีนี้คือไฟล์ JPEG)
## ขั้นตอนที่ 4: การจัดการภาพขนาดย่อประเภทต่างๆ
 หากไฟล์ PSD ของคุณอาจมีภาพขนาดย่อหลายประเภท เช่น`Thumbnail4Resource`คุณสามารถขยายตรรกะเพื่อจัดการกับกรณีเหล่านั้นในทำนองเดียวกันได้

## บทสรุป
ในบทช่วยสอนนี้ เราได้สำรวจวิธีแยกภาพย่อจากไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ด้วยการทำตามขั้นตอนที่อธิบายไว้ข้างต้น คุณสามารถดึงและบันทึกภาพขนาดย่อที่ฝังอยู่ในเอกสาร PSD ของคุณได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย
### Aspose.PSD คืออะไร
Aspose.PSD เป็นไลบรารี Java ที่ช่วยให้นักพัฒนาสามารถทำงานกับ PSD และรูปแบบไฟล์ภาพอื่น ๆ โดยทางโปรแกรม
### ฉันจะหาเอกสารเพิ่มเติมเกี่ยวกับ Aspose.PSD สำหรับ Java ได้ที่ไหน
 คุณสามารถอ้างถึง[เอกสารประกอบ](https://reference.aspose.com/psd/java/) สำหรับการอ้างอิงและตัวอย่าง API โดยละเอียด
### ฉันสามารถทดลองใช้ Aspose.PSD ฟรีก่อนซื้อได้หรือไม่
 ใช่ คุณสามารถดาวน์โหลด[ทดลองฟรี](https://releases.aspose.com/) เพื่อประเมินความสามารถของห้องสมุด
### ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร
 สามารถรับใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD เหมาะสำหรับการใช้งานเชิงพาณิชย์หรือไม่
ใช่ Aspose.PSD สามารถใช้กับทั้งโครงการส่วนบุคคลและเชิงพาณิชย์ภายใต้เงื่อนไขสิทธิ์การใช้งาน