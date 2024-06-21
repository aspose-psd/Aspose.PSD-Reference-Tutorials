---
title: แปลง PSB เป็น PSD ใน Java
linktitle: แปลง PSB เป็น PSD ใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีแปลง PSB เป็น PSD ใน Java ได้อย่างราบรื่นโดยใช้ Aspose.PSD ซึ่งช่วยเพิ่มการจัดการไฟล์กราฟิกในแอปพลิเคชันของคุณ
type: docs
weight: 12
url: /th/java/java-psb-to-image-format-conversion/convert-psb-to-psd-java/
---
## การแนะนำ
ในขอบเขตของการพัฒนา Java การจัดการไฟล์กราฟิกอย่างมีประสิทธิภาพเป็นสิ่งสำคัญ บทช่วยสอนนี้มุ่งเน้นไปที่การใช้ประโยชน์จาก Aspose.PSD สำหรับ Java เพื่อแปลงไฟล์ PSB (Photoshop Big) เป็นรูปแบบ PSD (เอกสาร Photoshop) ได้อย่างราบรื่น ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถรวมความสามารถนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่กระบวนการแปลง ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:
- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าได้ติดตั้ง JDK 8 ขึ้นไปบนระบบของคุณ
-  Aspose.PSD สำหรับไลบรารี Java: ดาวน์โหลดและกำหนดค่า Aspose.PSD สำหรับไลบรารี Java คุณสามารถรับได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE): ใช้ IntelliJ IDEA, Eclipse หรือ Java IDE อื่นที่คุณเลือก
- ความคุ้นเคยขั้นพื้นฐานกับ Java: ความเข้าใจพื้นฐานการเขียนโปรแกรม Java จะเป็นประโยชน์
## แพ็คเกจนำเข้า
ขั้นแรก นำเข้าคลาส Aspose.PSD ที่จำเป็นในไฟล์ Java ของคุณ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.FileFormatVersion;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
## ขั้นตอนที่ 1: เริ่มต้นตัวแปรและโหลดไฟล์ PSB
เริ่มต้นด้วยการกำหนดตัวแปรและโหลดไฟล์ PSB:
```java
String dataDir = "Your_Document_Directory/";
String sourceFileName = dataDir + "2layers.psb";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```
 ให้แน่ใจว่าจะเปลี่ยน`"Your_Document_Directory/"` พร้อมเส้นทางไปยังไดเร็กทอรีเอกสารจริงของคุณที่มีไฟล์ PSB
## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแปลง PSD
ถัดไป กำหนดค่าตัวเลือกการแปลง PSD:
```java
PsdOptions options = new PsdOptions();
options.setFileFormatVersion(FileFormatVersion.Psd);
```
 ที่นี่,`FileFormatVersion.Psd` ตรวจสอบให้แน่ใจว่าไฟล์เอาต์พุตอยู่ในรูปแบบ PSD
## ขั้นตอนที่ 3: บันทึกไฟล์ PSD ที่แปลงแล้ว
บันทึกไฟล์ PSD ที่แปลงแล้วโดยใช้อิมเมจ PSB ที่โหลดและตัวเลือก:
```java
image.save(dataDir + "ConvertFromPsb_out.psd", options);
```
 แทนที่`"ConvertFromPsb_out.psd"` ด้วยชื่อไฟล์เอาต์พุตและเส้นทางที่คุณต้องการ

## บทสรุป
การทำตามขั้นตอนเหล่านี้ แสดงว่าคุณแปลงไฟล์ PSB เป็นรูปแบบ PSD ได้สำเร็จโดยใช้ Aspose.PSD สำหรับ Java ความสามารถนี้ช่วยปรับปรุงแอปพลิเคชัน Java ของคุณโดยให้การผสานรวมกับรูปแบบไฟล์ Photoshop ได้อย่างราบรื่น
## คำถามที่พบบ่อย
### Aspose.PSD สำหรับ Java สามารถจัดการไฟล์ PSB ที่ซับซ้อนที่มีหลายเลเยอร์ได้หรือไม่
ใช่ Aspose.PSD สำหรับ Java รองรับไฟล์ PSB ที่มีหลายเลเยอร์ โดยคงโครงสร้างไว้ระหว่างการแปลง
### Aspose.PSD สำหรับ Java เหมาะสำหรับการประมวลผลการแปลง PSB เป็น PSD เป็นชุดหรือไม่
แน่นอน คุณสามารถประมวลผลการแปลง PSB เป็น PSD ได้อย่างมีประสิทธิภาพโดยใช้ Aspose.PSD สำหรับ Java
### Aspose.PSD สำหรับ Java จะรักษาคุณภาพของภาพในระหว่างการแปลงหรือไม่
ใช่ ไลบรารีรับประกันการแปลงที่มีความเที่ยงตรงสูง โดยรักษาคุณภาพของภาพและรายละเอียด
### ฉันสามารถรวม Aspose.PSD สำหรับ Java เข้ากับเว็บแอปพลิเคชันได้หรือไม่
ใช่ Aspose.PSD สำหรับ Java สามารถผสานรวมเข้ากับแอปพลิเคชัน Java ทั้งบนเดสก์ท็อปและบนเว็บได้อย่างราบรื่น
### ฉันจะรับการสนับสนุนหรือความช่วยเหลือเพิ่มเติมสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน
 หากต้องการความช่วยเหลือเพิ่มเติม โปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).