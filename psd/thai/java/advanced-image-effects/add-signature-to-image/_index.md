---
date: 2025-12-02
description: เรียนรู้วิธีวาดภาพบนแคนวาสและใส่ลายเซ็นทับใน Java ด้วย Aspose.PSD ทำตามบทเรียนการประมวลผลภาพ
  Java ทีละขั้นตอนนี้และบันทึกผลลัพธ์เป็น PNG.
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: วาดภาพบนแคนวาส – เพิ่มลายเซ็นด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วาดภาพบน Canvas – เพิ่มลายเซ็นด้วย Aspose.PSD สำหรับ Java

## บทนำ

การเพิ่มลายเซ็นมือหรือดิจิทัลลงในรูปภาพเป็นความต้องการที่พบบ่อยสำหรับสัญญา ใบแจ้งหนี้ หรือเอกสารใด ๆ ที่ต้องการหลักฐานความถูกต้อง ด้วย **Aspose.PSD for Java** คุณสามารถ **draw image on canvas** และถือว่าลายเซ็นเป็นเพียงเลเยอร์โอเวอร์เลย์อีกชั้นหนึ่ง ใน **java image processing tutorial** นี้เราจะพาคุณผ่านขั้นตอนทั้งหมด—from การโหลดรูปภาพฐานและไฟล์ลายเซ็น, การเริ่มต้น graphics, การวาดโอเวอร์เลย์, และสุดท้าย **save image png java**‑style

## คำตอบด่วน
- **What does “draw image on canvas” mean?** หมายถึงการเรนเดอร์ภาพหนึ่งลงบนอีกภาพหนึ่งโดยใช้คลาส `Graphics`  
- **How to add a signature in Java?** โหลดไฟล์ลายเซ็นเป็น `Image` แล้วใช้ `Graphics.drawImage`  
- **Which Aspose.PSD version is required?** เวอร์ชัน 24.x ล่าสุดใดก็ได้; โค้ดทำงานกับไลบรารีล่าสุด  
- **Can I overlay multiple images?** ได้—เรียก `drawImage` ซ้ำกับแหล่งที่มาที่ต่างกัน  
- **Do I need a license?** รุ่นทดลองใช้ได้สำหรับการพัฒนา; ต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง  

## “Draw Image on Canvas” คืออะไร?
ในคำศัพท์ของ Aspose.PSD การวาดภาพบน canvas หมายถึงการทาสีอ็อบเจ็กต์ `Image` หนึ่งลงบนอีกอ็อบเจ็กต์หนึ่งโดยใช้คอนเท็กซ์ `Graphics` การดำเนินการนี้เป็นหัวใจของเทคนิค **overlay images java** เช่น การเพิ่มลายน้ำ โลโก้ หรือ ลายเซ็น

## ทำไมต้องใช้ Aspose.PSD สำหรับการวางลายเซ็นทับ?
- **Full PSD support** – ทำงานกับเลเยอร์, มาสก์, และความโปร่งใส  
- **No native OS dependencies** – pure Java, เหมาะสำหรับการประมวลผลฝั่งเซิร์ฟเวอร์  
- **High‑performance rendering** – ปรับให้ทำงานได้อย่างมีประสิทธิภาพกับไฟล์ขนาดใหญ่และคอมโพสชันซับซ้อน  

## ข้อกำหนดเบื้องต้น
- Java Development Kit (JDK) 8 หรือสูงกว่า  
- Aspose.PSD for Java JAR ที่เพิ่มใน classpath ของโปรเจกต์  
- ไฟล์ภาพสองไฟล์: ภาพฐาน (เช่น `layers.psd`) และกราฟิกลายเซ็น (`sample.psd`)  

## นำเข้าแพ็กเกจ

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดภาพหลักและภาพรอง

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** เก็บภาพทั้งสองไว้ในโหมดสีเดียวกัน (RGB) เพื่อหลีกเลี่ยงการเปลี่ยนสีที่ไม่คาดคิดเมื่อวาด  

## ขั้นตอนที่ 2: เริ่มต้น Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

อ็อบเจ็กต์ `Graphics` ทำหน้าที่เหมือนแปรงสีที่ให้คุณ **draw image on canvas** การเริ่มต้นด้วย `Image` หลักทำให้คำสั่งการวาดทั้งหมดต่อมาถูกผูกกับ canvas นี้  

## ขั้นตอนที่ 3: เพิ่มลายเซ็นลงในภาพ (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

ในโค้ดสแนปนี้เราจะ **overlay images java** โดยวางลายเซ็นที่มุมล่าง‑ขวา ปรับค่า `Point` หากต้องการตำแหน่งอื่น  

## ปัญหาทั่วไปและวิธีแก้ไข
| อาการ | สาเหตุ | วิธีแก้ |
|---------|-------|-----|
| ลายเซ็นปรากฏบิดเบี้ยว | DPI ไม่ตรงกันระหว่าง canvas กับลายเซ็น | ใช้ `signature.resize` ก่อนวาดหรือให้ไฟล์ทั้งสองมี DPI เดียวกัน |
| ไฟล์ผลลัพธ์มีขนาดใหญ่ | บันทึกโดยไม่มีการบีบอัด | ส่ง `PngOptions` ที่กำหนด `CompressionLevel` ให้สูงขึ้น |
| ไม่มีอะไรถูกวาด | Graphics ไม่ได้ถูกทำลาย | เรียก `graphics.dispose()` หลังการวาด (เป็นทางเลือกแต่เป็นแนวปฏิบัติที่ดี) |

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณได้เรียนรู้ **how to draw image on canvas** และเพิ่ม **ลายเซ็น** อย่างราบรื่นด้วย Aspose.PSD for Java เทคนิคนี้สามารถต่อยอดเป็นลายน้ำ โลโก้ หรือกราฟิกโอเวอร์เลย์ใด ๆ ทำให้แอปพลิเคชัน Java ของคุณมีความสามารถ **java image processing** ที่แข็งแกร่ง

## คำถามที่พบบ่อย

### คำถาม 1: ฉันสามารถเพิ่มลายเซ็นหลายรายการลงในภาพได้หรือไม่?
**ตอบ:** ได้ คุณสามารถเพิ่มลายเซ็นหลายรายการโดยทำซ้ำขั้นตอนด้วยไฟล์ลายเซ็นที่ต่างกัน

### คำถาม 2: Aspose.PSD รองรับรูปแบบภาพอื่น ๆ หรือไม่?
**ตอบ:** รองรับรูปแบบภาพหลากหลาย ช่วยให้การประมวลผลภาพมีความยืดหยุ่น

### คำถาม 3: จำเป็นต้องมีใบอนุญาตสำหรับการใช้ Aspose.PSD สำหรับ Java หรือไม่?
**ตอบ:** ใช่ คุณต้องมีใบอนุญาตที่ถูกต้องสำหรับการใช้ Aspose.PSD เยี่ยมชม [Purchase Aspose.PSD](https://purchase.aspose.com/buy) เพื่อดูรายละเอียดการให้ใบอนุญาต

### คำถาม 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร?
**ตอบ:** เยี่ยมชม [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา

### คำถาม 5: ฉันสามารถทดลองใช้ Aspose.PSD สำหรับ Java ก่อนซื้อได้หรือไม่?
**ตอบ:** ได้ คุณสามารถรับ [free trial](https://releases.aspose.com/) เพื่อสำรวจคุณสมบัติก่อนตัดสินใจซื้อ

## คำถามที่พบบ่อยเพิ่มเติม

**ถาม: ฉันจะเปลี่ยนความทึบของลายเซ็นได้อย่างไร?**  
**ตอบ:** ใช้ `graphics.setOpacity(float opacity)` ก่อนเรียก `drawImage` ค่าอยู่ระหว่าง 0.0 (โปร่งใส) ถึง 1.0 (ทึบ)

**ถาม: สามารถหมุนลายเซ็นได้หรือไม่?**  
**ตอบ:** ได้—ใช้เมทริกซ์การแปลงโดยเรียก `graphics.rotateTransform(angle)` ก่อนวาด

**ถาม: ฉันสามารถวาดลายเซ็นลงบน JPEG แทน PNG ได้หรือไม่?**  
**ตอบ:** แน่นอน แทนที่ `PngOptions` ด้วย `JpegOptions` แล้วกำหนดระดับคุณภาพที่ต้องการ

---

**อัปเดตล่าสุด:** 2025-12-02  
**ทดสอบกับ:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}