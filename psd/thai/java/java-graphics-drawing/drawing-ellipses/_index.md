---
title: การวาดวงรีใน Java
linktitle: การวาดวงรีใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีการวาดวงรีใน Java โดยใช้ Aspose.PSD เพื่อการออกแบบกราฟิกและการปรับแต่งรูปภาพที่แม่นยำ บทช่วยสอนแบบทีละขั้นตอน
weight: 15
url: /th/java/java-graphics-drawing/drawing-ellipses/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดวงรีใน Java

## การแนะนำ
ในบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีการวาดวงรีโดยใช้ Aspose.PSD สำหรับ Java Aspose.PSD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนา Java สามารถทำงานกับไฟล์ PSD และจัดการรูปภาพได้อย่างง่ายดาย การวาดรูปร่างเช่นวงรีเป็นงานพื้นฐานในการประมวลผลภาพและการออกแบบกราฟิก เมื่อปฏิบัติตามคู่มือนี้ คุณจะได้รับประสบการณ์ตรงในการสร้างจุดไข่ปลาโดยใช้โปรแกรม Aspose.PSD
## ข้อกำหนดเบื้องต้น
ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
- ติดตั้ง JDK (Java Development Kit) บนระบบของคุณ
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE) เช่น IntelliJ IDEA หรือ Eclipse
-  Aspose.PSD สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).
## แพ็คเกจนำเข้า
ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.PSD:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
## ขั้นตอนที่ 1: ตั้งค่าโปรเจ็กต์ Java ของคุณ
ก่อนที่คุณจะเริ่มเขียนโค้ด ตรวจสอบให้แน่ใจว่าโปรเจ็กต์ Java ของคุณได้รับการตั้งค่าอย่างถูกต้องโดยมี Aspose.PSD รวมอยู่ด้วยเป็นการขึ้นต่อกัน
## ขั้นตอนที่ 2: สร้างอินสแตนซ์ของ PsdImage
เริ่มต้นอินสแตนซ์ใหม่ของ PsdImage ด้วยความกว้างและความสูงที่ต้องการ
```java
Image image = new PsdImage(100, 100);
```
## ขั้นตอนที่ 3: เริ่มต้นวัตถุกราฟิก
สร้างและเริ่มต้นอินสแตนซ์ของกราฟิกเพื่อทำงานกับรูปภาพ
```java
Graphics graphics = new Graphics(image);
```
## ขั้นตอนที่ 4: ล้างพื้นผิวกราฟิก
ก่อนวาด ให้ล้างพื้นผิวกราฟิกด้วยสีเฉพาะ (ไม่จำเป็น)
```java
graphics.clear(Color.getYellow());
```
## ขั้นตอนที่ 5: วาดวงรีประ
ใช้วัตถุปากกาที่มีสีแดงและวาดวงรีประภายในสี่เหลี่ยมผืนผ้าที่ระบุ
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## ขั้นตอนที่ 6: วาดวงรีต่อเนื่อง
สร้างวัตถุปากกาด้วยแปรงสีน้ำเงินทึบ แล้ววาดวงรีต่อเนื่องภายในสี่เหลี่ยมผืนผ้าอื่น
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## ขั้นตอนที่ 7: บันทึกภาพ
สุดท้าย ให้บันทึกรูปภาพที่สร้างขึ้นในรูปแบบ BMP ไปยังเส้นทางที่ระบุ
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีการวาดวงรีโดยทางโปรแกรมโดยใช้ Aspose.PSD สำหรับ Java แล้ว บทช่วยสอนนี้ครอบคลุมถึงการตั้งค่าโปรเจ็กต์ของคุณ การเริ่มต้นกราฟิก การวาดเส้นประและจุดต่อเนื่อง และการบันทึกภาพที่ได้ ตอนนี้คุณสามารถรวมเทคนิคเหล่านี้เข้ากับแอปพลิเคชัน Java ของคุณสำหรับงานออกแบบกราฟิกและการจัดการรูปภาพต่างๆ
## คำถามที่พบบ่อย
### ฉันสามารถใช้ Aspose.PSD ได้ฟรีหรือไม่
Aspose.PSD มีเวอร์ชันทดลองใช้ฟรี ซึ่งช่วยให้คุณสามารถประเมินคุณสมบัติต่างๆ ได้ก่อนที่จะซื้อ
### ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมได้ที่ไหน
 เยี่ยม[เอกสาร Aspose.PSD](https://reference.aspose.com/psd/java/) สำหรับคำแนะนำและตัวอย่างที่ครอบคลุม
### ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร
 สามารถรับใบอนุญาตชั่วคราวได้จาก[Aspose.PSD ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD สามารถบันทึกรูปภาพเป็นรูปแบบใดได้บ้าง
Aspose.PSD รองรับการบันทึกรูปภาพในรูปแบบต่าง ๆ รวมถึง BMP, PNG, JPEG และ PSD
### Aspose.PSD เหมาะสำหรับการใช้งานระดับองค์กรหรือไม่
ใช่ Aspose.PSD ได้รับการออกแบบมาเพื่องานการประมวลผลภาพระดับมืออาชีพและระดับองค์กร
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
