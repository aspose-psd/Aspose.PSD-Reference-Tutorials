---
title: แปลง AI เป็น PSD ใน Java
linktitle: แปลง AI เป็น PSD ใน Java
second_title: Aspose.PSD Java API
description: แปลง AI เป็น PSD ใน Java โดยใช้ Aspose.PSD พร้อมคำแนะนำทีละขั้นตอนง่ายๆ ของเรา เหมาะสำหรับนักพัฒนาที่ต้องการการแปลงไฟล์ที่รวดเร็วและราบรื่น
weight: 14
url: /th/java/java-ai-to-image-format-conversion/convert-ai-to-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง AI เป็น PSD ใน Java

## การแนะนำ
คุณต้องการแปลงไฟล์ AI (Adobe Illustrator) เป็นไฟล์ PSD (Adobe Photoshop) โดยใช้ Java หรือไม่? คุณอยู่ในสถานที่ที่เหมาะสม! วันนี้ เราจะมาสำรวจวิธีการทำงานนี้ให้สำเร็จโดยใช้ไลบรารี Aspose.PSD สำหรับ Java อันทรงพลัง คู่มือนี้จะอธิบายทุกสิ่งที่คุณจำเป็นต้องรู้ ตั้งแต่ข้อกำหนดเบื้องต้นไปจนถึงคำแนะนำทีละขั้นตอนโดยละเอียด มาเจาะลึกและแปลงไฟล์การออกแบบของคุณได้อย่างราบรื่น
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม มีบางสิ่งที่คุณต้องมี:
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK 8 หรือสูงกว่าบนระบบของคุณ
2.  Aspose.PSD สำหรับ Java: ดาวน์โหลดไลบรารี Aspose.PSD สำหรับ Java จาก[หน้าดาวน์โหลด](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): IDE เช่น IntelliJ IDEA หรือ Eclipse เพื่อเขียนและรันโค้ด Java ของคุณ
4. ไฟล์ AI: ไฟล์ Adobe Illustrator ที่คุณต้องการแปลง
5.  Aspose Temporary License (ทางเลือก): สำหรับการใช้งานเต็มรูปแบบโดยไม่มีข้อจำกัด คุณสามารถขอรับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).
## แพ็คเกจนำเข้า
ขั้นแรก มาตั้งค่าโครงการของเราโดยการนำเข้าแพ็คเกจที่จำเป็น คุณจะต้องรวม Aspose.PSD สำหรับ Java ไว้ใน classpath ของโปรเจ็กต์ของคุณ ต่อไปนี้เป็นวิธีดำเนินการ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
 หรือคุณสามารถดาวน์โหลดไฟล์ JAR ได้จากไฟล์[Aspose.PSD สำหรับหน้าดาวน์โหลด Java](https://releases.aspose.com/psd/java/) และเพิ่มลงในโครงการของคุณด้วยตนเอง
มาแบ่งกระบวนการออกเป็นขั้นตอนง่ายๆ ที่จัดการได้
## ขั้นตอนที่ 1: การตั้งค่าโครงการของคุณ
ขั้นแรก ให้ตั้งค่าโปรเจ็กต์ของคุณใน IDE ที่คุณต้องการ
### สร้างโครงการใหม่
1. เปิด IDE ของคุณและสร้างโครงการ Java ใหม่
2. ตั้งชื่อโปรเจ็กต์ของคุณให้มีความหมาย เช่น "AItoPSDConverter"
### เพิ่มไลบรารี Aspose.PSD
1. หากคุณดาวน์โหลดไฟล์ JAR ให้เพิ่มลงในพาธการ build ของโปรเจ็กต์ของคุณ
2.  หากใช้ Maven ตรวจสอบให้แน่ใจว่าได้เพิ่มการพึ่งพาของคุณอย่างถูกต้อง`pom.xml`.
## ขั้นตอนที่ 2: กำลังโหลดไฟล์ AI
ตอนนี้โปรเจ็กต์ของคุณได้รับการตั้งค่าแล้ว มาโหลดไฟล์ AI ที่คุณต้องการแปลงกัน
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage) Image.load(sourceFileName);
```
## ขั้นตอนที่ 3: การตั้งค่าตัวเลือก PSD
ต่อไป เราต้องตั้งค่าตัวเลือกสำหรับเอาต์พุต PSD ของเรา
```java
PsdOptions options = new PsdOptions();
```
## ขั้นตอนที่ 4: บันทึกไฟล์ AI เป็น PSD
เมื่อโหลดไฟล์ AI และตั้งค่าตัวเลือกแล้ว เราก็สามารถบันทึกเป็นไฟล์ PSD ได้แล้ว
```java
String outFileName = dataDir + "34992OStroke.psd";
image.save(outFileName, options);
```
## บทสรุป
และคุณก็ได้แล้ว! คุณได้แปลงไฟล์ AI เป็นไฟล์ PSD สำเร็จโดยใช้ Aspose.PSD สำหรับ Java ไลบรารีอันทรงพลังนี้ทำให้การจัดการการแปลงไฟล์ที่ซับซ้อนในแอปพลิเคชัน Java ของคุณเป็นเรื่องง่าย ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น คู่มือนี้จะช่วยให้คุณรวมฟังก์ชันการแปลง AI เป็น PSD เข้ากับโปรเจ็กต์ของคุณได้อย่างง่ายดาย
## คำถามที่พบบ่อย
### Aspose.PSD สำหรับ Java คืออะไร
Aspose.PSD สำหรับ Java เป็นไลบรารีที่มีประสิทธิภาพซึ่งช่วยให้นักพัฒนาสามารถสร้าง แก้ไข และแปลงไฟล์ Photoshop (PSD และ PSB) ภายในแอปพลิเคชัน Java โดยไม่ต้องใช้ Adobe Photoshop
### ฉันสามารถใช้ Aspose.PSD สำหรับ Java ได้ฟรีหรือไม่
 Aspose.PSD สำหรับ Java ให้ทดลองใช้ฟรี ซึ่งคุณสามารถดาวน์โหลดได้จาก[หน้าทดลองใช้ฟรี](https://releases.aspose.com/) - เพื่อคุณสมบัติครบถ้วน ก[ใบอนุญาต](https://purchase.aspose.com/buy) เป็นสิ่งจำเป็น
### ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร
 คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[หน้าใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).
### เป็นไปได้ไหมที่จะแปลงไฟล์ PSD กลับเป็นไฟล์ AI
ปัจจุบัน Aspose.PSD สำหรับ Java ไม่รองรับการแปลงไฟล์ PSD กลับเป็นไฟล์ AI มุ่งเน้นไปที่การจัดการไฟล์ PSD และ PSB
### ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมได้ที่ไหน
 คุณสามารถค้นหาเอกสารและตัวอย่างที่ครอบคลุมได้ที่[Aspose.PSD สำหรับหน้าเอกสารประกอบ Java](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
