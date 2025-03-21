---
title: การวาดเส้นโค้ง Bezier ใน Java
linktitle: การวาดเส้นโค้ง Bezier ใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีการวาดเส้นโค้ง Bezier ใน Java โดยใช้ Aspose.PSD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนพร้อมตัวอย่างโค้ด
weight: 14
url: /th/java/java-graphics-drawing/drawing-bezier-curves/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดเส้นโค้ง Bezier ใน Java

## การแนะนำ
ในการเขียนโปรแกรม Java การวาดรูปทรงที่ซับซ้อน เช่น เส้นโค้ง Bezier สามารถเพิ่มความดึงดูดสายตาของแอปพลิเคชันได้อย่างมาก Aspose.PSD สำหรับ Java มีฟังก์ชันการทำงานที่มีประสิทธิภาพเพื่ออำนวยความสะดวกในงานดังกล่าวได้อย่างมีประสิทธิภาพ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการวาดเส้นโค้ง Bezier ทีละขั้นตอนโดยใช้ Aspose.PSD สำหรับ Java ช่วยให้คุณสร้างกราฟิกที่ดึงดูดสายตาได้อย่างง่ายดาย
## ข้อกำหนดเบื้องต้น
ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าได้ติดตั้ง JDK บนระบบของคุณแล้ว
2.  Aspose.PSD สำหรับ Java JAR: ดาวน์โหลด Aspose.PSD สำหรับไลบรารี Java จาก[ที่นี่](https://releases.aspose.com/psd/java/) และรวมไว้ในโครงการของคุณ
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): ใช้ IDE ที่คุณเลือก (Eclipse, IntelliJ IDEA ฯลฯ) ที่กำหนดค่าด้วย JDK.z
## แพ็คเกจนำเข้า
ก่อนที่จะเริ่มดำเนินการ ให้นำเข้าคลาส Aspose.PSD ที่จำเป็น:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
## ขั้นตอนที่ 1: สร้างอินสแตนซ์รูปภาพ
 ขั้นแรก คุณต้องสร้างอินสแตนซ์ของ`PsdImage` คลาสซึ่งแสดงถึงรูปภาพ PSD ในหน่วยความจำ
```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
คำอธิบาย:
- `PsdImage` ถูกสร้างอินสแตนซ์ด้วยพารามิเตอร์ความกว้างและความสูง (100x100 พิกเซลในตัวอย่างนี้)
## ขั้นตอนที่ 2: เริ่มต้นบริบทกราฟิก
 ถัดไป เริ่มต้นอินสแตนซ์ของ`Graphics` คลาสเพื่อดำเนินการวาดภาพบนรูปภาพ
```java
Graphics graphics = new Graphics(image);
```
คำอธิบาย:
- `Graphics` วัตถุเริ่มต้นด้วย`image` เช่น ช่วยให้สามารถดำเนินการวาดภาพได้
## ขั้นตอนที่ 3: ล้างพื้นผิวกราฟิก
ล้างพื้นผิวกราฟิกโดยใช้สีพื้นหลังเฉพาะที่นี่`Color.getYellow()`.
```java
graphics.clear(Color.getYellow());
```
คำอธิบาย:
- `clear()` วิธีการกำหนดสีพื้นหลังของพื้นผิวกราฟิก
## ขั้นตอนที่ 4: เริ่มต้นปากกาสำหรับการวาดภาพ
 ตั้งค่าก`Pen` วัตถุที่มีคุณสมบัติเช่นสีและความกว้างเพื่อกำหนดวิธีการวาดเส้นโค้ง
```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
คำอธิบาย:
- `Pen` เริ่มต้นด้วยสีดำและความกว้าง 3 พิกเซล
## ขั้นตอนที่ 5: กำหนดพารามิเตอร์ Bezier Curve
ระบุจุดควบคุมและจุดสิ้นสุดสำหรับเส้นโค้ง Bezier
```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
คำอธิบาย:
- `startX`, `startY`: จุดเริ่มต้นของเส้นโค้ง
- `controlX1`, `controlY1`: จุดควบคุมแรก
- `controlX2`, `controlY2`: จุดควบคุมที่สอง
- `endX`, `endY`: จุดสิ้นสุดของเส้นโค้ง
## ขั้นตอนที่ 6: วาดเส้นโค้งเบซิเยร์
 ใช้`drawBezier()` วิธีการวาดเส้นโค้ง Bezier ลงบนภาพโดยใช้ค่าที่กำหนดไว้ก่อนหน้านี้`Pen` และจุดควบคุม
```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
คำอธิบาย:
- `drawBezier()` วิธีการวาดเส้นโค้งด้วยพารามิเตอร์ที่ระบุโดยใช้`blackPen`.
## ขั้นตอนที่ 7: บันทึกรูปภาพ
บันทึกภาพที่วาดเป็นรูปแบบไฟล์ BMP
```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```
## บทสรุป
การวาดเส้นโค้ง Bezier ใน Java โดยใช้ Aspose.PSD สำหรับ Java นั้นตรงไปตรงมาด้วยฟังก์ชันที่ให้มา เมื่อทำตามบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีตั้งค่าสภาพแวดล้อม นำเข้าแพ็คเกจที่จำเป็น และวาดเส้นโค้ง Bezier ทีละขั้นตอน ทดลองใช้จุดควบคุมและการตั้งค่าปากกาที่แตกต่างกันเพื่อสร้างเส้นโค้งที่หลากหลายและปรับปรุงแอปพลิเคชัน Java ของคุณให้มองเห็นได้
## คำถามที่พบบ่อย
### ฉันสามารถวาดเส้นโค้ง Bezier หลายเส้นในภาพเดียวกันได้หรือไม่
ได้ คุณสามารถวาดเส้นโค้งได้หลายเส้นโดยทำซ้ำขั้นตอนภายในลูป เปลี่ยนจุดควบคุมและจุดสิ้นสุดตามต้องการ
### ฉันจะเปลี่ยนสีของเส้นโค้ง Bezier ได้อย่างไร?
 ปรับเปลี่ยน`Pen` คุณสมบัติสีของวัตถุ (`Color.getBlack()` ในตัวอย่าง) ก่อนโทร`drawBezier()`.
### Aspose.PSD สำหรับ Java เหมาะสำหรับภาพที่มีความละเอียดสูงหรือไม่
ใช่ Aspose.PSD สำหรับ Java รองรับภาพความละเอียดสูงพร้อมการจัดการหน่วยความจำที่มีประสิทธิภาพ
### ฉันสามารถส่งออกรูปภาพเป็นรูปแบบอื่นที่ไม่ใช่ BMP ได้หรือไม่
ใช่ Aspose.PSD สำหรับ Java รองรับการส่งออกรูปภาพเป็นรูปแบบต่างๆ เช่น PNG, JPEG, TIFF เป็นต้น
### ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมได้ที่ไหน
 เยี่ยมชม[Aspose.PSD สำหรับเอกสาร Java](https://reference.aspose.com/psd/java/) สำหรับคำแนะนำและตัวอย่างโค้ดที่ครอบคลุม## ซอร์สโค้ดที่สมบูรณ์
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
