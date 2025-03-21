---
title: เพิ่มเลเยอร์ข้อความบนรันไทม์ในไฟล์ PSD โดยใช้ Java
linktitle: เพิ่มเลเยอร์ข้อความบนรันไทม์ในไฟล์ PSD โดยใช้ Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มเลเยอร์ข้อความแบบไดนามิกลงในไฟล์ PSD โดยใช้ Java กับ Aspose.PSD ปฏิบัติตามบทช่วยสอนทีละขั้นตอนนี้เพื่อความเป็นไปได้ของระบบอัตโนมัติที่น่าตื่นเต้น
weight: 17
url: /th/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มเลเยอร์ข้อความบนรันไทม์ในไฟล์ PSD โดยใช้ Java

## การแนะนำ
หากคุณเคยทำงานกับ Photoshop คุณจะรู้ว่าการแก้ไขภาพมีประสิทธิภาพเพียงใด แต่จะเกิดอะไรขึ้นถ้าฉันบอกคุณว่าคุณสามารถทำงานบางอย่างโดยอัตโนมัติโดยใช้ Java ได้? ลองนึกภาพการเพิ่มเลเยอร์ข้อความลงในไฟล์ PSD ของคุณแบบไดนามิกโดยทางโปรแกรม ค่อนข้างเท่ห์ใช่มั้ย? ในบทช่วยสอนนี้ เรากำลังเจาะลึกเกี่ยวกับวิธีการเพิ่มเลเยอร์ข้อความลงในไฟล์ PSD ได้ทันทีโดยใช้ไลบรารี Aspose.PSD สำหรับ Java ดังนั้น พับแขนเสื้อขึ้นแล้วเริ่มกันเลย!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกเรื่องโค้ด เรามาตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่จำเป็นในการเริ่มต้นแล้ว นี่คือสิ่งที่คุณต้องการ:
1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถ[ดาวน์โหลดได้ที่นี่](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD สำหรับแพ็คเกจ Java: คุณจะต้องดาวน์โหลดและรวมไลบรารี Aspose.PSD เข้ากับโปรเจ็กต์ของคุณ คุณสามารถคว้ามันได้จาก[กำหนดหน้าการเผยแพร่](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): แม้ว่าคุณจะสามารถใช้โปรแกรมแก้ไขข้อความใดก็ได้ แต่ IDE เช่น IntelliJ IDEA หรือ Eclipse จะทำให้ชีวิตของคุณง่ายขึ้นมากโดยการจัดหาเครื่องมือสำหรับจัดการโครงการของคุณ
4. ความรู้พื้นฐานของ Java: การทำความเข้าใจแนวคิดหลักของ Java เป็นสิ่งจำเป็นเพื่อศึกษาบทช่วยสอนนี้ได้อย่างราบรื่น
5.  ไฟล์ PSD: เตรียมไฟล์ PSD พื้นฐานให้พร้อมสำหรับการเล่น เราจะใช้ชื่อหนึ่ง`OneLayer.psd` เป็นจุดเริ่มต้นของเรา
## แพ็คเกจนำเข้า
เมื่อคุณมีทุกอย่างแล้ว ขั้นตอนแรกในกระบวนการของเราคือการนำเข้าแพ็คเกจที่จำเป็นในไฟล์ Java ของคุณ นี่คือสิ่งที่คุณจะต้องมี:
```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```
การนำเข้าเหล่านี้นำคลาสที่สำคัญทั้งหมดที่คุณต้องการในการจัดการไฟล์ PSD โดยใช้ไลบรารี Aspose.PSD
เอาล่ะ มาดูสาระสำคัญของการเพิ่มเลเยอร์ข้อความลงในไฟล์ PSD ของคุณกันดีกว่า เราจะแบ่งขั้นตอนนี้ออกเป็นขั้นตอนที่สามารถจัดการได้เพื่อให้แน่ใจว่าคุณจะเข้าใจแต่ละขั้นตอนได้อย่างถี่ถ้วน
## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ
ขั้นแรก คุณต้องตั้งค่าพื้นที่ทำงานของคุณซึ่งมีไฟล์ Adobe Photoshop Document (PSD) อยู่ กำหนดตำแหน่งที่ไฟล์ PSD ของคุณอาศัยอยู่ด้วยสตริงง่ายๆ
```java
String dataDir = "Your Document Directory"; 
```
 ที่นี่คุณจะแทนที่`"Your Document Directory"` ด้วยเส้นทางจริงที่เก็บไฟล์ PSD ของคุณ
## ขั้นตอนที่ 2: โหลดไฟล์ PSD ต้นฉบับของคุณ
ถัดไป คุณต้องโหลดไฟล์ PSD ลงในแอปพลิเคชันของคุณ นี่คือจุดเริ่มต้นของความมหัศจรรย์ ใช้`Image.load()` วิธีการนำไฟล์ของคุณมาเล่น
```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```
 ข้อมูลโค้ดนี้จะโหลดของคุณ`OneLayer.psd` ไฟล์ลงใน`img` วัตถุ. หากเส้นทางถูกต้อง คุณจะต้องโหลด PSD ของคุณและพร้อมที่จะจัดการ
## ขั้นตอนที่ 3: ส่งไปที่ PsdImage
 เมื่อโหลดภาพของคุณแล้ว คุณจะต้องส่งภาพไปที่`PsdImage` เนื่องจากเรากำลังจัดการกับไฟล์ Photoshop โดยเฉพาะ
```java
PsdImage im = (PsdImage)img;
```
เมื่อทำการแคสต์ คุณจะสามารถเข้าถึงวิธีการทั้งหมดที่เกี่ยวข้องกับการจัดการ PSD ที่คุณต้องการในบทช่วยสอนนี้
## ขั้นตอนที่ 4: กำหนดสี่เหลี่ยมผืนผ้าสำหรับเลเยอร์ข้อความ
ตอนนี้ได้เวลาระบุตำแหน่งที่คุณต้องการให้เลเยอร์ข้อความของคุณปรากฏ คุณจะต้องกำหนดสี่เหลี่ยมเพื่อกำหนดตำแหน่งและขนาดของข้อความ
```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```
ในตัวอย่างนี้ สี่เหลี่ยมผืนผ้าถูกตั้งค่าให้ใช้ความกว้างครึ่งหนึ่งและความสูงครึ่งหนึ่งของรูปภาพ โดยอยู่ที่หนึ่งในสี่ของทางด้านล่างและทางขวาง คุณสามารถปรับแต่งค่าเหล่านี้เพื่อวางตำแหน่งข้อความของคุณได้ตามที่คุณต้องการ!
## ขั้นตอนที่ 5: เพิ่มเลเยอร์ข้อความ
 ตอนนี้ถึง pièce de résistance — เพิ่มข้อความของคุณ! ใช้`addTextLayer()` วิธีการทำให้ข้อความที่คุณต้องการมีชีวิตชีวาในสี่เหลี่ยมที่ระบุ
```java
TextLayer layer = im.addTextLayer("Added text", rect);
```
ในกรณีนี้ เราเพียงแต่เพิ่มเลเยอร์ข้อความที่ระบุว่า "ข้อความที่เพิ่ม" คุณสามารถแทนที่สิ่งนี้ด้วยสตริงใดก็ได้ที่คุณต้องการ
## ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่อัปเดตของคุณ
ขั้นตอนสุดท้ายคือบันทึกการเปลี่ยนแปลงของคุณกลับไปเป็นไฟล์ PSD ใหม่ นี่คือวิธีที่คุณทำ:
```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```
 ตรวจสอบให้แน่ใจว่าได้ระบุชื่อไฟล์ใหม่เพื่อไม่ให้คุณเขียนทับไฟล์ PSD ต้นฉบับของคุณ ตอนนี้ เมื่อคุณตรวจสอบไดเร็กทอรีที่ระบุ คุณจะเห็น`ImageWithTextLayer.psd` พร้อมข้อความที่เพิ่มเข้ามาใหม่!
## บทสรุป
และนั่นคือการปิดท้าย! คุณเพิ่งเรียนรู้วิธีเพิ่มเลเยอร์ข้อความลงในไฟล์ PSD แบบไดนามิกโดยใช้ Java กับไลบรารี Aspose.PSD มันเป็นตัวเปลี่ยนเกมสำหรับนักพัฒนาที่ต้องการรวมความสามารถของ Photoshop เข้ากับแอพพลิเคชั่นของพวกเขา ไม่ว่าคุณจะทำงานเป็นผู้จัดการโครงการสำหรับนักออกแบบหรือทำงานกราฟิกอัตโนมัติ เทคนิคนี้สามารถช่วยคุณประหยัดเวลาได้มาก
รู้สึกอยากสำรวจเพิ่มเติมไหม? อย่าลืมตรวจสอบเอกสาร Aspose.PSD สำหรับ Java เพื่อดูฟังก์ชันเพิ่มเติมและคุณสมบัติขั้นสูง
## คำถามที่พบบ่อย
### ฉันสามารถเพิ่มเลเยอร์ข้อความหลายชั้นได้หรือไม่
อย่างแน่นอน! เพียงทำซ้ำขั้นตอนที่ 4 และ 5 สำหรับแต่ละเลเยอร์ข้อความที่คุณต้องการเพิ่ม
### จะเกิดอะไรขึ้นหากไฟล์ PSD ของฉันมีหลายเลเยอร์
Aspose.PSD สามารถจัดการไฟล์ PSD ที่มีเลเยอร์ที่ซับซ้อนได้ เพียงให้แน่ใจว่าคุณอ้างอิงเลเยอร์ที่ถูกต้องเมื่อจัดการกับมัน
### มีวิธีจัดรูปแบบข้อความหรือไม่?
 ใช่! คุณสามารถสำรวจความสามารถของ`TextLayer` คลาสเพื่อเปลี่ยนขนาดตัวอักษร สี และอื่นๆ โดยการเข้าไปดูเอกสารประกอบของ Aspose.PSD
### ฉันสามารถใช้สิ่งนี้ในแอปพลิเคชันบนเว็บได้หรือไม่?
ได้ ตราบใดที่คุณมีแบ็กเอนด์ Java คุณสามารถใช้แนวทางนี้ในเว็บแอปพลิเคชันได้
### ฉันจะรับการสนับสนุนได้ที่ไหนหากฉันประสบปัญหา
 ตรวจสอบ[กำหนดฟอรัมสนับสนุน](https://forum.aspose.com/c/psd/34) ซึ่งชุมชนและทีม Aspose สามารถช่วยเหลือคุณได้
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
