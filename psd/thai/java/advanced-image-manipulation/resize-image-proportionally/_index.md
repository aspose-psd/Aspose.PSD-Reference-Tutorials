---
date: 2025-12-08
description: เรียนรู้วิธีแปลงไฟล์ PSD เป็น PNG และปรับขนาดภาพให้สัดส่วนเท่าเดิมใน
  Java ด้วย Aspose.PSD บทเรียนทีละขั้นตอนนี้ครอบคลุมการแคชภาพ การปรับขนาด และการบันทึกเป็น
  PNG.
language: th
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: วิธีแปลง PSD เป็น PNG และปรับขนาดอย่างสัดส่วนด้วย Aspose.PSD สำหรับ Java
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง PSD เป็น PNG และปรับขนาดอย่างสัดส่วนด้วย Aspose.PSD for Java

## บทนำ

หากคุณต้องการ **แปลง PSD เป็น PNG** พร้อมคงอัตราส่วนเดิม คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะพาคุณผ่าน **Aspose.PSD tutorial** ที่สมบูรณ์ ซึ่งจะแสดงวิธี **ปรับขนาดภาพ** อย่างสัดส่วนใน Java, แคชภาพเพื่อประสิทธิภาพที่ดีที่สุด, และสุดท้ายบันทึกผลลัพธ์เป็น PNG. เมื่อเสร็จคุณจะสามารถนำกระบวนการนี้ไปใช้ใน pipeline การประมวลผลภาพที่ใช้ Java ใด ๆ ได้

## คำตอบสั้น
- **Aspose.PSD สามารถแปลง PSD เป็น PNG ได้หรือไม่?** ได้ – เพียงโหลด PSD แล้วบันทึกด้วย `PngOptions`.
- **ไลบรารีรองรับการปรับขนาดอย่างสัดส่วนหรือไม่?** แน่นอน; ใช้ `resizeWidthProportionally` และ `resizeHeightProportionally`.
- **ต้องแคชภาพก่อนหรือไม่?** การแคช (`image.cacheData()`) ช่วยเพิ่มประสิทธิภาพสำหรับไฟล์ PSD ขนาดใหญ่.
- **ต้องใช้ Java เวอร์ชันใด?** รองรับ Java 8 หรือใหม่กว่าอย่างเต็มที่.
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** ต้องมี – ลิขสิทธิ์เชิงพาณิชย์จะลบลายน้ำการประเมินผล.

## “แปลง PSD เป็น PNG” คืออะไรและทำไมจึงสำคัญ?

การแปลงไฟล์ Photoshop (PSD) เป็นไฟล์ Portable Network Graphics (PNG) ทำให้คุณสามารถแชร์การออกแบบแบบหลายเลเยอร์ในรูปแบบที่เบาและเป็นมิตรต่อเว็บ PNG รักษาความโปร่งใสและคุณภาพแบบไม่มีการสูญเสีย ทำให้เหมาะสำหรับ assets UI, thumbnails หรือสถานการณ์ใด ๆ ที่คุณภาพภาพเป็นสิ่งสำคัญ

## ทำไมต้องปรับขนาดภาพอย่างสัดส่วนใน Java?

การปรับขนาด **how to resize image** โดยไม่บิดเบือนอัตราส่วนช่วยให้กราฟิกดูเป็นธรรมชาติบนหน้าจอที่หลากหลาย API ของ `Aspose.PSD` มีเมธอดเฉพาะสำหรับการสเกลแบบสัดส่วน ซึ่งคำนวณความสูงหรือความกว้างที่สอดคล้องโดยอัตโนมัติ ลดความผิดพลาดจากการคำนวณด้วยตนเอง

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK)** – ติดตั้ง Java 8 หรือใหม่กว่า
2. **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์อย่างเป็นทางการ [ที่นี่](https://releases.aspose.com/psd/java/)
3. ไฟล์ PSD ตัวอย่าง (`sample.psd`) ที่วางไว้ในโฟลเดอร์ที่คุณสามารถอ้างอิงจากโปรเจกต์ได้

## นำเข้าแพ็กเกจ

เพิ่มการนำเข้าที่จำเป็นในคลาส Java ของคุณ คลาสเหล่านี้ให้คุณเข้าถึงการโหลดภาพ, แคช, ปรับขนาด, และตัวเลือกการส่งออก PNG

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดภาพ PSD

แรกสุดให้โหลดไฟล์ PSD ต้นฉบับ หากไฟล์มีขนาดใหญ่ การแคชข้อมูลภาพจะช่วยลดการใช้หน่วยความจำเมื่อทำการดำเนินการต่อ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## ขั้นตอนที่ 2: ปรับขนาดภาพอย่างสัดส่วน (Java)

ต่อไปให้กำหนดขนาดใหม่ ในตัวอย่างนี้เราจะลดขนาดภาพลงเหลือ **ครึ่ง** ของขนาดเดิมโดยคงอัตราส่วน คุณสามารถปรับความกว้างหรือความสูงเป้าหมายตามต้องการ

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **เคล็ดลับ:** ใช้ `resizeWidthProportionally` *หรือ* `resizeHeightProportionally` — ไลบรารีจะคำนวณมิติอื่นโดยอัตโนมัติเพื่อให้ภาพคงสัดส่วน

## ขั้นตอนที่ 3: บันทึกภาพที่ปรับขนาดเป็น PNG

สุดท้ายให้ส่งออกภาพที่ปรับขนาดเป็นรูปแบบ PNG ขั้นตอนนี้จะสรุป workflow **แปลง PSD เป็น PNG** ของเรา

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

เมื่อโค้ดทำงาน คุณจะพบไฟล์ PNG ที่มีขนาดครึ่งหนึ่งของ PSD ต้นฉบับ โดยยังคงคุณภาพภาพเดิมและไม่มีการบิดเบือน

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **OutOfMemoryError** | PSD ขนาดใหญ่ไม่ได้แคช | เรียก `image.cacheData()` ก่อนปรับขนาด |
| **PNG ผลลัพธ์เป็นสีขาว** | เส้นทางไฟล์ไม่ถูกต้อง | ตรวจสอบ `dataDir` และสิทธิ์การเขียน |
| **อัตราส่วนภาพผิด** | ใช้ความกว้างและความสูงพร้อมกันแบบแมนนวล | ใช้เมธอดสัดส่วนที่ Aspose.PSD ให้มา |

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD รองรับฟอร์แมตภาพทั้งหมดหรือไม่?**  
ตอบ: Aspose.PSD รองรับ PSD, PNG, JPEG, BMP, GIF และอื่น ๆ อีกมาก ดูรายการเต็มใน [เอกสาร](https://reference.aspose.com/psd/java/)

**ถาม: สามารถใช้ Aspose.PSD ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
ตอบ: ได้. ซื้อไลเซนส์เชิงพาณิชย์ได้ที่ [Aspose store](https://purchase.aspose.com/buy)

**ถาม: มีไลเซนส์ชั่วคราวสำหรับการทดสอบหรือไม่?**  
ตอบ: มี – ขอรับไลเซนส์ชั่วคราว [ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับการประเมินผล

**ถาม: จะหาแหล่งสนับสนุนจากชุมชนได้จากที่ไหน?**  
ตอบ: ฟอรั่ม [Aspose.PSD](https://forum.aspose.com/c/psd/34) เป็นที่ดีสำหรับถามคำถามและแบ่งปันวิธีแก้

**ถาม: จะเข้าถึงเอกสาร API เต็มรูปแบบได้อย่างไร?**  
ตอบ: ดูเอกสาร API รายละเอียดได้ [ที่นี่](https://reference.aspose.com/psd/java/)

## สรุป

คุณได้เรียนรู้วิธี **แปลง PSD เป็น PNG**, ปรับขนาดภาพอย่างสัดส่วน, และจัดการแคชอย่างมีประสิทธิภาพด้วย Aspose.PSD for Java. นำขั้นตอนเหล่านี้ไปใช้ในแอปพลิเคชันของคุณเพื่อให้การประมวลผลภาพเร็วขึ้น, คุณภาพสูงโดยไม่ต้องพึ่งพาการติดตั้ง Photoshop ดั้งเดิม

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2025-12-08  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose