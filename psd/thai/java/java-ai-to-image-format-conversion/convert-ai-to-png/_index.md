---
title: แปลง AI เป็น PNG ใน Java
linktitle: แปลง AI เป็น PNG ใน Java
second_title: Aspose.PSD Java API
description: แปลง AI เป็น PNG ใน Java ได้อย่างง่ายดายโดยใช้ Aspose.PSD พร้อมคำแนะนำนี้ เรียนรู้วิธีโหลด ตั้งค่าตัวเลือก และบันทึกไฟล์ AI ของคุณเป็นภาพ PNG ได้อย่างง่ายดาย
type: docs
weight: 13
url: /th/java/java-ai-to-image-format-conversion/convert-ai-to-png/
---
## การแนะนำ
คุณต้องการแปลงไฟล์ Adobe Illustrator (.AI) เป็นภาพ PNG โดยใช้ Java หรือไม่? คุณมาถูกที่แล้ว! ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอนโดยใช้ Aspose.PSD อันทรงพลังสำหรับไลบรารี Java คู่มือนี้จะช่วยให้คุณเข้าใจวิธีแปลงไฟล์ AI ของคุณเป็น PNG คุณภาพสูงได้อย่างราบรื่นด้วยโค้ดเพียงไม่กี่บรรทัด มาดำดิ่งกันเถอะ!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม มีบางสิ่งที่คุณต้องมี:
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK 8 ขึ้นไปบนเครื่องของคุณ
2.  Aspose.PSD สำหรับ Java: คุณต้องมี Aspose.PSD สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[กำหนดหน้าการเผยแพร่](https://releases.aspose.com/psd/java/) หรือได้รับ[ทดลองใช้ฟรี](https://releases.aspose.com/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): Java IDE ใดๆ เช่น IntelliJ IDEA, Eclipse หรือ NetBeans
4. ความรู้พื้นฐานของ Java: ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java จะเป็นประโยชน์
## แพ็คเกจนำเข้า
ขั้นแรก คุณจะต้องนำเข้าแพ็คเกจ Aspose.PSD ที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ มาตั้งค่าสภาพแวดล้อมของคุณกันดีกว่า
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```
ตอนนี้เราได้ตั้งค่าสภาพแวดล้อมของเราแล้ว เรามาแบ่งกระบวนการแปลงเป็นขั้นตอนที่ง่ายต่อการปฏิบัติตามกัน
## ขั้นตอนที่ 1: โหลดไฟล์ AI
ขั้นตอนแรกในกระบวนการแปลงคือการโหลดไฟล์ AI ลงในแอปพลิเคชัน Java ของคุณโดยใช้ไลบรารี Aspose.PSD
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage)Image.load(sourceFileName);
```
## ขั้นตอนที่ 2: ตั้งค่าตัวเลือก PNG
ถัดไปคุณต้องตั้งค่าตัวเลือก PNG ซึ่งเกี่ยวข้องกับการกำหนดประเภทสีและการตั้งค่าอื่นๆ เฉพาะสำหรับไฟล์ PNG
```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
```
## ขั้นตอนที่ 3: บันทึกภาพเป็น PNG
สุดท้าย ให้บันทึกไฟล์ AI ที่โหลดเป็นรูปภาพ PNG โดยใช้ตัวเลือกที่ระบุ
```java
String outFileName = dataDir + "34992OStroke.png";
image.save(outFileName, options);
```
แค่นั้นแหละ! ไฟล์ AI ของคุณแปลงเป็น PNG เรียบร้อยแล้ว
## บทสรุป
การแปลงไฟล์ AI เป็น PNG ใน Java เป็นเรื่องง่ายด้วย Aspose.PSD ด้วยการทำตามขั้นตอนที่ระบุไว้ในคู่มือนี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย ไม่ว่าคุณจะทำงานกับแอปพลิเคชันกราฟิกหรือต้องการแปลงไฟล์เป็นชุด Aspose.PSD ก็มีเครื่องมือที่คุณต้องการเพื่อให้งานสำเร็จลุล่วงได้อย่างมีประสิทธิภาพ
## คำถามที่พบบ่อย
### Aspose.PSD คืออะไร
Aspose.PSD เป็นไลบรารี Java ที่ช่วยให้นักพัฒนาสามารถทำงานกับ PSD (Photoshop) และรูปแบบไฟล์ Adobe อื่น ๆ รองรับการดำเนินการต่างๆ เช่น การแก้ไข การแปลง และการเรนเดอร์
### ฉันสามารถใช้ Aspose.PSD ได้ฟรีหรือไม่
 คุณสามารถใช้ Aspose.PSD กับไฟล์[ทดลองใช้ฟรี](https://releases.aspose.com/) แต่หากต้องการฟังก์ชันการทำงานเต็มรูปแบบ คุณจะต้องซื้อใบอนุญาต คุณยังสามารถได้รับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการประเมินผล
### Aspose.PSD รองรับไฟล์รูปแบบใดบ้าง
Aspose.PSD รองรับไฟล์ PSD, PSB, AI และรูปแบบไฟล์ Adobe อื่นๆ ช่วยให้สามารถแปลงเป็นรูปแบบภาพต่างๆ เช่น PNG, JPEG, BMP และ TIFF
### Aspose.PSD เข้ากันได้กับ Java ทุกเวอร์ชันหรือไม่
Aspose.PSD เข้ากันได้กับ JDK 8 และสูงกว่า ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งเวอร์ชัน JDK ที่เหมาะสมแล้ว
### ฉันจะหาเอกสารเพิ่มเติมได้จากที่ไหน?
 คุณสามารถดูเอกสารรายละเอียดได้ที่[หน้าเอกสารประกอบของ Aspose.PSD](https://reference.aspose.com/psd/java/).