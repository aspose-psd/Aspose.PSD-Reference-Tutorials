---
title: เพิ่มลายน้ำให้กับไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java
linktitle: เพิ่มลายน้ำให้กับไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มลายน้ำให้กับไฟล์ PSD ของคุณอย่างง่ายดายโดยใช้ Aspose.PSD สำหรับ Java ปกป้องภาพของคุณด้วยคำแนะนำง่ายๆ ทีละขั้นตอน
weight: 18
url: /th/java/modifying-converting-psd-images/add-watermark-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มลายน้ำให้กับไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java

## การแนะนำ
ลายน้ำเป็นวิธีที่ละเอียดอ่อนแต่มีประสิทธิภาพในการปกป้องภาพของคุณและสื่อสารถึงความเป็นเจ้าของ ไม่ว่าคุณจะเป็นช่างภาพที่แสดงผลงานของคุณหรือนักออกแบบที่นำเสนอผลงานล่าสุดของคุณ การเพิ่มลายน้ำอาจเป็นสิ่งสำคัญในการรักษาเอกลักษณ์ของแบรนด์ของคุณ ในบทช่วยสอนนี้ เราจะเจาะลึกวิธีการเพิ่มลายน้ำให้กับไฟล์ PSD ของคุณอย่างง่ายดายโดยใช้ Aspose.PSD สำหรับ Java คว้ากาแฟสักแก้ว ทำตัวให้สบาย แล้วมาเริ่มกันเลย!
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเจาะลึกโค้ด จำเป็นอย่างยิ่งที่จะต้องแน่ใจว่าคุณมีเครื่องมือและแพ็คเกจที่จำเป็นเพื่อใช้ลายน้ำในไฟล์ PSD ของคุณได้สำเร็จ นี่คือสิ่งที่คุณต้องเตรียม:
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว อาจจำเป็นต้องกำหนดค่าตัวแปร PATH ด้วย
2. Aspose.PSD สำหรับ Java Library: นี่คือหัวใจสำคัญของแอปพลิเคชันลายน้ำของเรา คุณต้องดาวน์โหลดไลบรารี่จากไฟล์[เว็บไซต์กำหนด](https://releases.aspose.com/psd/java/).
3. IDE: Java IDE ใดๆ ที่คุณเลือกจะทำได้ ไม่ว่าจะเป็น Eclipse, IntelliJ IDEA หรือแม้แต่โปรแกรมแก้ไขข้อความธรรมดา คุณสามารถเลือกได้อย่างอิสระ
4.  ไฟล์ PSD: เตรียมไฟล์ PSD ไว้ให้พร้อม คุณสามารถสร้างหรือค้นหาตัวอย่างทางออนไลน์ได้ เราจะเรียกมันว่า`layers.psd`.
5. ความรู้พื้นฐานของ Java: ความเข้าใจที่ดีเกี่ยวกับพื้นฐานของ Java จะช่วยคุณได้มากในการปฏิบัติตาม
## แพ็คเกจนำเข้า
ตอนนี้คุณได้ตั้งค่าทุกอย่างแล้ว เรามานำเข้าแพ็คเกจที่จำเป็นกันดีกว่า การนำเข้าใน Java ช่วยให้คุณสามารถนำเข้าคลาสและฟังก์ชันจากไลบรารีต่างๆ ได้ ทำให้โค้ดของคุณมีประสิทธิภาพมากขึ้น ด้านล่างนี้คือสิ่งที่คุณต้องการ:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีของคุณ
ก่อนอื่น เราต้องกำหนดเส้นทางสำหรับตำแหน่งที่ไฟล์ PSD ของคุณอยู่ นี่เป็นสิ่งสำคัญเนื่องจาก Java จำเป็นต้องรู้ว่าจะหาไฟล์ของคุณได้จากที่ไหน 
```java
String dataDir = "Your Document Directory";
```
 แทนที่`Your Document Directory` ด้วยไดเร็กทอรีจริงของคุณซึ่งมีไฟล์ PSD ของคุณอยู่
## ขั้นตอนที่ 2: โหลดไฟล์ PSD
 ต่อไป เราจะโหลดไฟล์ PSD และโยนมันลงในไฟล์`PsdImage`ขั้นตอนนี้จะแปลงไฟล์เป็นรูปแบบที่เราสามารถจัดการได้
```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```
 สิ่งที่บรรทัดนี้ใช้คือนำไฟล์ PSD ที่มีอยู่ของคุณไปโหลดลงในหน่วยความจำในรูปแบบ a`PsdImage`- ให้คิดว่ามันเหมือนกับการเปิดหนังสือเพื่อที่คุณจะได้เริ่มเขียนลงไปได้
## ขั้นตอนที่ 3: สร้างวัตถุกราฟิก
 เมื่อโหลดไฟล์ PSD ของเราแล้ว เราจำเป็นต้องสร้างไฟล์`Graphics` วัตถุ. สิ่งนี้ช่วยให้เราดำเนินการวาดภาพได้ โดยพื้นฐานแล้วเหมือนกับการใช้พู่กันเพื่อเพิ่มสีสันให้กับผืนผ้าใบของคุณ
```java
Graphics graphics = new Graphics(psdImage);
```
## ขั้นตอนที่ 4: กำหนดแบบอักษรสำหรับลายน้ำของคุณ
ตอนนี้ก็ถึงเวลาเลือกว่าลายน้ำของคุณจะมีลักษณะอย่างไร เราจะใช้ Arial ด้วยขนาดตัวอักษร 20 นี่คือที่ที่คุณจะได้อวดสไตล์ของคุณ!
```java
Font font = new Font("Arial", 20.0f);
```
## ขั้นตอนที่ 5: สร้างแปรงทึบสำหรับใส่ลายน้ำ
แปรงทึบคือสิ่งที่ทำให้ลายน้ำของคุณมีสีและความทึบ เราต้องการให้มองเห็นได้ชัดเจนแต่ไม่มากเกินไป ดังนั้นให้ตั้งค่าอัลฟ่าใกล้กับ 0 เพื่อให้ได้รูปลักษณ์ที่โปร่งใสบางส่วน
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 ที่นี่,`Color.fromArgb(50, 128, 128, 128)` สร้างสีเทาที่มีความทึบ 50% มันเหมือนกับเมฆที่บดบังท้องฟ้าที่สดใสอย่างนุ่มนวล
## ขั้นตอนที่ 6: ตั้งค่าการจัดแนวสตริงสำหรับลายน้ำของคุณ
เพื่อให้แน่ใจว่าลายน้ำของคุณปรากฏตรงกลางภาพ เราจะตั้งค่าตัวเลือกการจัดตำแหน่งสตริง ขั้นตอนนี้เน้นความแม่นยำ!
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```
## ขั้นตอนที่ 7: วาดลายน้ำ
เรากำลังเข้าสู่ส่วนที่น่าตื่นเต้นแล้ว! เมื่อตั้งค่าบริบทกราฟิกของเราแล้ว ก็ถึงเวลาวาดลายน้ำลงบนภาพ
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```
 นี่ครับ แทนที่`"Some watermark text"` พร้อมข้อความลายน้ำที่คุณต้องการ ขั้นตอนนี้เหมือนกับการลงลายเซ็นของคุณบนผลงานชิ้นเอก!
## ขั้นตอนที่ 8: ส่งออกรูปภาพเป็นรูปแบบ PNG
ตอนนี้อาร์ตเวิร์คของเราพร้อมแล้ว เราจำเป็นต้องบันทึกมันเป็นรูปแบบไฟล์ใหม่ ซึ่งในกรณีนี้คือ PNG 
```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```
ด้วยการดำเนินการบรรทัดนี้ คุณจะทำให้งานของคุณเป็นอมตะในรูปแบบใหม่ได้อย่างมีประสิทธิภาพ โดยรักษาลายน้ำให้โลกได้เห็น!
## บทสรุป
และคุณก็ได้แล้ว! คุณได้เพิ่มลายน้ำลงในไฟล์ PSD ของคุณสำเร็จแล้วโดยใช้ Aspose.PSD สำหรับ Java กระบวนการนี้ไม่เพียงแต่รักษาความปลอดภัยให้กับเนื้อหาของคุณ แต่ยังช่วยยกระดับการมองเห็นแบรนด์ของคุณอีกด้วย โปรดจำไว้ว่าขั้นตอนที่คุณทำเป็นเพียงจุดเริ่มต้นเท่านั้น รู้สึกอิสระที่จะสร้างสรรค์—ทดลองใช้แบบอักษร สไตล์ และสีที่แตกต่างกัน! ปกป้องงานของคุณและแสดงแบรนด์ของคุณด้วยความภาคภูมิใจ 
## คำถามที่พบบ่อย
### ฉันสามารถปรับแต่งข้อความลายน้ำได้หรือไม่?
 อย่างแน่นอน! เพียงแทนที่ข้อความใน`drawString` วิธีการที่มีลายน้ำที่คุณต้องการ
### จะทำอย่างไรถ้าฉันต้องการแบบอักษรอื่น
 คุณสามารถเปลี่ยนแบบอักษรได้อย่างง่ายดายโดยเลือกแบบอักษรอื่นใน`Font` การสร้างอินสแตนซ์
### มีวิธีปรับความทึบหรือไม่?
 ใช่! เปลี่ยนค่าอัลฟ่าเป็น`Color.fromArgb()` เพื่อเปลี่ยนความทึบของลายน้ำ
### ฉันสามารถใช้รูปแบบภาพอื่นได้หรือไม่?
 ได้ คุณสามารถบันทึกในรูปแบบต่างๆ เช่น JPEG หรือ BMP เพียงแค่แทนที่`PngOptions()` ด้วยตัวเลือกที่ต้องการ
### ฉันจะขอความช่วยเหลือเพิ่มเติมได้จากที่ไหน?
 สอบถามรายละเอียดเพิ่มเติมได้ที่[กำหนดฟอรั่ม](https://forum.aspose.com/c/psd/34) หรือตรวจสอบของพวกเขา[เอกสารประกอบ](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
