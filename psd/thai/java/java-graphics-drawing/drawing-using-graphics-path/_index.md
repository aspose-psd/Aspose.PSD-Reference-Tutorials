---
title: การวาดภาพโดยใช้เส้นทางกราฟิกใน Java
linktitle: การวาดภาพโดยใช้เส้นทางกราฟิกใน Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีสร้างกราฟิกที่ซับซ้อนใน Java โดยใช้คลาส Graphics Path ของ Aspose.PSD บทช่วยสอนนี้จะแนะนำคุณตลอดแต่ละขั้นตอนในการสร้างภาพที่น่าทึ่ง
weight: 19
url: /th/java/java-graphics-drawing/drawing-using-graphics-path/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดภาพโดยใช้เส้นทางกราฟิกใน Java

## การแนะนำ
การสร้างและจัดการรูปภาพโดยทางโปรแกรมอาจเป็นงานที่น่าตื่นเต้นสำหรับนักพัฒนา Java โดยเฉพาะอย่างยิ่งเมื่อใช้ไลบรารีเช่น Aspose.PSD ในบทช่วยสอนนี้ เราจะเจาะลึกขั้นตอนการวาดภาพกราฟิกที่ซับซ้อนโดยใช้คลาส Graphics Path ใน Java ด้วย Aspose.PSD
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะพูดถึงส่วนการเขียนโค้ด ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
1.  Java Development Kit (JDK): JDK เวอร์ชันเสถียรที่ติดตั้งบนเครื่องของคุณ คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ของออราเคิล](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD สำหรับไลบรารี Java: ดาวน์โหลด Aspose.PSD สำหรับไลบรารี Java จาก[ที่นี่](https://releases.aspose.com/psd/java/)- หลังจากดาวน์โหลด ให้เพิ่มไฟล์ JAR ลงใน classpath ของโปรเจ็กต์ของคุณ
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): ไม่ว่าจะเป็น Eclipse, IntelliJ IDEA หรืออื่นๆ คุณต้องมี IDE เพื่อเขียนและรันโค้ด Java
ด้วยข้อกำหนดเบื้องต้นเหล่านี้ เรามาดูวิธีสร้างภาพที่น่าดึงดูดใจโดยใช้คลาสเส้นทางกราฟิกกันดีกว่า
## แพ็คเกจนำเข้า
ในการเริ่มต้น คุณต้องนำเข้าแพ็คเกจที่จำเป็น:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```
การนำเข้าเหล่านี้ให้การเข้าถึงฟังก์ชันหลักที่จำเป็นในการสร้างและจัดการรูปภาพโดยใช้ Aspose.PSD
## ขั้นตอนที่ 1: เริ่มต้นรูปภาพและกราฟิก
ในการเริ่มต้น เรามาตั้งค่ารูปภาพใหม่และเริ่มต้นวัตถุกราฟิก:
```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```
ที่นี่ เราสร้างรูปภาพขนาด 500x500 พิกเซลและวัตถุกราฟิกสำหรับวาดภาพ
## ขั้นตอนที่ 2: สร้างและกำหนดค่าเส้นทางกราฟิก
 ต่อไปเราจะสร้าง a`GraphicsPath` วัตถุเพื่อกำหนดเส้นทางการวาด:
```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```
ในขั้นตอนนี้ เราจะเพิ่มวงกลม สี่เหลี่ยม และป้ายกำกับข้อความให้กับรูปภาพของเรา จากนั้นจึงเพิ่มรูปภาพนี้ในเส้นทางกราฟิกของเรา
## ขั้นตอนที่ 3: วาดและเติมเส้นทาง
ตอนนี้เราได้กำหนดเส้นทางของเราแล้ว เราสามารถวาดและเติมมันได้:
```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```
ในขั้นตอนนี้ เราวาดเส้นทางโดยใช้ปากกาสีน้ำเงิน และเติมด้วยรูปแบบฟักแนวตั้งโดยใช้แปรงฟัก
## ขั้นตอนที่ 4: บันทึกรูปภาพ
สุดท้าย ให้บันทึกรูปภาพลงในไฟล์:
```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```
ในขั้นตอนสุดท้ายนี้ การสร้างภาพของคุณโดยใช้เส้นทางกราฟิกจะเสร็จสมบูรณ์
## บทสรุป
การสร้างภาพที่ซับซ้อนโดยใช้คลาส Graphics Path ด้วย Aspose.PSD นั้นทั้งทรงพลังและน่าดึงดูด โดยการปฏิบัติตามคู่มือนี้ คุณสามารถขยายความสามารถของแอปพลิเคชัน Java ในการออกแบบกราฟิกได้
## คำถามที่พบบ่อย
### Aspose.PSD คืออะไร
Aspose.PSD เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Photoshop และจัดการเลเยอร์รูปภาพโดยทางโปรแกรม
### ฉันสามารถใช้ Aspose.PSD สำหรับรูปแบบอื่นที่ไม่ใช่ PSD ได้หรือไม่
ในคู่มือนี้ Aspose.PSD เกี่ยวข้องกับไฟล์ PSD โดยเฉพาะ แต่มีส่วนขยายเพื่อรองรับรูปแบบรูปภาพที่แตกต่างกัน
### มีเวอร์ชันทดลองใช้งานสำหรับ Aspose.PSD หรือไม่
 ใช่ คุณสามารถเข้าถึง Aspose.PSD รุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ฉันจะซื้อ Aspose.PSD ได้อย่างไร
 คุณสามารถซื้อ Aspose.PSD ได้จาก[ที่นี่](https://purchase.aspose.com/buy).
### ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้ที่ไหน
คุณสามารถขอการสนับสนุนและการสนทนาได้ที่[ฟอรั่มของ Aspose](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
