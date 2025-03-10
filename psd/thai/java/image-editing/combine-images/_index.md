---
title: รวมรูปภาพโดยใช้ Aspose.PSD สำหรับ Java
linktitle: รวมรูปภาพ
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีผสานรูปภาพใน Java ด้วย Aspose.PSD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการผสมภาพที่ราบรื่น
weight: 11
url: /th/java/image-editing/combine-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รวมรูปภาพโดยใช้ Aspose.PSD สำหรับ Java

## การแนะนำ

ในขอบเขตของการเขียนโปรแกรม Java Aspose.PSD มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับจัดการและประมวลผลรูปภาพ หนึ่งในคุณสมบัติเด่นของมันคือความสามารถในการรวมภาพหลาย ๆ ภาพเข้าด้วยกันได้อย่างลงตัว บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการรวมรูปภาพสองรูปให้เป็นไฟล์ PSD ไฟล์เดียวโดยใช้ Aspose.PSD สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  ไลบรารี Aspose.PSD: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.PSD ในสภาพแวดล้อม Java ของคุณ คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).

2. Java Development Kit (JDK): Aspose.PSD ต้องใช้ Java เพื่อทำงาน ติดตั้ง JDK ล่าสุดบนเครื่องของคุณ

3. ไดเรกทอรีเอกสาร: ตั้งค่าไดเรกทอรีที่จะจัดเก็บรูปภาพและไฟล์ PSD ที่เป็นผลลัพธ์

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นสำหรับโปรเจ็กต์ Java ของคุณ รวมไลบรารี Aspose.PSD ไว้ในโปรเจ็กต์ของคุณ ดังที่แสดงด้านล่าง:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## ขั้นตอนที่ 1: สร้างตัวเลือก PSD

เริ่มต้นด้วยการสร้างอินสแตนซ์ของ PsdOptions และตั้งค่าคุณสมบัติต่างๆ:

```java
PsdOptions imageOptions = new PsdOptions();
```

## ขั้นตอนที่ 2: ตั้งค่า FileCreateSource

สร้างอินสแตนซ์ของ FileCreateSource และกำหนดให้กับคุณสมบัติ Source:

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

## ขั้นตอนที่ 3: สร้างอินสแตนซ์รูปภาพ

สร้างอินสแตนซ์วัตถุรูปภาพด้วยตัวเลือกและขนาดที่ระบุ:

```java
Image image = Image.create(imageOptions, 600, 600);
```

## ขั้นตอนที่ 4: เริ่มต้นกราฟิก

สร้างและเริ่มต้นอินสแตนซ์กราฟิก ล้างพื้นผิวรูปภาพด้วยสีขาว และวาดภาพแรก:

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

## ขั้นตอนที่ 5: วาดภาพที่สอง

วาดภาพที่สองบนผืนผ้าใบ PSD ที่สร้างขึ้น:

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

## ขั้นตอนที่ 6: บันทึกรูปภาพผลลัพธ์

บันทึกภาพที่รวมสุดท้าย:

```java
image.save();
```

ยินดีด้วย! คุณได้รวมรูปภาพสองรูปเป็นไฟล์ PSD ไฟล์เดียวสำเร็จโดยใช้ Aspose.PSD สำหรับ Java

## บทสรุป

Aspose.PSD ทำให้การจัดการรูปภาพใน Java ง่ายขึ้น โดยนำเสนอโซลูชันที่มีประสิทธิภาพสำหรับการรวมรูปภาพได้อย่างง่ายดาย ด้วยการทำตามบทช่วยสอนนี้ คุณได้ใช้ประโยชน์จากพลังของ Aspose.PSD เพื่อสร้างองค์ประกอบภาพที่ดึงดูดสายตา

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับรูปแบบภาพทุกรูปแบบหรือไม่

A1: Aspose.PSD เน้นที่รูปแบบไฟล์ PSD เป็นหลัก อย่างไรก็ตาม รองรับรูปแบบอื่น ๆ สำหรับอินพุตและเอาต์พุต

### คำถามที่ 2: ฉันสามารถทำการแก้ไขเพิ่มเติมกับภาพที่รวมกันได้หรือไม่

A2: แน่นอน! หลังจากรวมรูปภาพแล้ว คุณสามารถปรับแต่ง PSD ที่เป็นผลลัพธ์เพิ่มเติมได้โดยใช้ฟีเจอร์ที่ครอบคลุมของ Aspose.PSD

### คำถามที่ 3: มีข้อกำหนดสิทธิ์การใช้งานสำหรับการใช้ Aspose.PSD หรือไม่

 A3: ใช่ จำเป็นต้องมีใบอนุญาตที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์ รับได้จาก[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 4: Aspose.PSD มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถสำรวจ Aspose.PSD ได้ด้วยการทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับแบบสอบถามที่เกี่ยวข้องกับ Aspose.PSD ได้ที่ไหน

 A5: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการอภิปรายของชุมชน
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
