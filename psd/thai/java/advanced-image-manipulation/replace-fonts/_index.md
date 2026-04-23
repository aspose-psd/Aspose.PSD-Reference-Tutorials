---
date: 2026-02-09
description: เรียนรู้วิธีใช้การแทนที่ฟอนต์ของ Aspose PSD ใน Java เพื่อจัดการไฟล์ PSD
  ที่ขาดฟอนต์, แทนที่ฟอนต์ที่หายไปใน PSD อย่างรวดเร็ว, และส่งออกภาพ
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: การแทนที่ฟอนต์ใน Aspose PSD ด้วย Java – แทนที่ฟอนต์ที่หายไป
url: /th/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแทนที่ฟอนต์ Aspose PSD ใน Java

## บทนำ

หากคุณต้องการเปลี่ยนฟอนต์ที่หายไปหรือไม่ต้องการภายในไฟล์ Photoshop (PSD) **Aspose PSD font substitution** ทำให้เป็นเรื่องง่าย ในแอปพลิเคชัน Java คุณสามารถโหลด PSD, บอก Aspose ว่าจะใช้ฟอนต์สำรองใด, แล้วบันทึกผลลัพธ์ในรูปแบบใดก็ได้ตามต้องการ บทเรียนนี้จะพาคุณผ่านขั้นตอนการทำงาน **aspose psd font substitution** อย่างครบถ้วน ตั้งแต่การตั้งค่าโปรเจกต์จนถึงการส่งออกภาพที่อัปเดต เพื่อให้คุณจัดการกับสถานการณ์ฟอนต์หายใน PSD ได้อย่างเชื่อถือโดยไม่ต้องเปิด Photoshop.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่จัดการการแทนที่ฟอนต์คืออะไร?** Aspose.PSD for Java  
- **การดำเนินการใช้เวลานานเท่าไหร่?** About 5‑10 minutes for a basic scenario  
- **ฟอนต์ใดที่ใช้เป็นฟอนต์สำรองเริ่มต้น?** You can set any TrueType font, e.g., “Arial”  
- **ฉันสามารถบันทึกเป็นรูปแบบอื่นนอกจาก PNG ได้หรือไม่?** Yes – PSD, JPEG, BMP, etc., are supported  
- **ต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** A valid Aspose.PSD license is required for non‑trial use  

## Aspose PSD Font Substitution คืออะไร?

Aspose PSD font substitution คือกระบวนการระบุฟอนต์สำรองที่ไลบรารีจะใช้เมื่อพบฟอนต์ที่หายไปหรือไม่รองรับในไฟล์ PSD ซึ่งทำให้เลเยอร์ข้อความแสดงผลอย่างถูกต้องโดยไม่ต้องแก้ไขด้วยมือใน Photoshop และทำให้คุณ **handle missing fonts PSD** ไฟล์โดยอัตโนมัติ.

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java?

- **Full‑featured PSD handling** – ชั้น, มาสก์, เอฟเฟกต์, และข้อความทั้งหมดสามารถเข้าถึงได้ผ่าน API.  
- **Cross‑platform** – ทำงานบนระบบปฏิบัติการใดก็ได้ที่รองรับ Java.  
- **No external dependencies** – ไลบรารีจัดการการแทนที่ฟอนต์ภายใน, ดังนั้นคุณไม่จำเป็นต้องจัดส่งฟอนต์เพิ่มเติมกับแอปของคุณ.  

## วิธีการแทนที่ฟอนต์ที่หายไปใน PSD ด้วย Aspose PSD

ต่อไปนี้เป็นคู่มือขั้นตอนที่แสดง **how to replace missing fonts PSD** ไฟล์ด้วยฟอนต์สำรองที่กำหนดเอง.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม, ตรวจสอบให้แน่ใจว่าคุณมี:

- **Java Development Kit (JDK)** – เวอร์ชัน 8 หรือสูงกว่า ติดตั้งแล้ว.  
- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [release page](https://releases.aspose.com/psd/java/).  
- **An IDE** – IntelliJ IDEA, Eclipse, หรือโปรแกรมแก้ไขใด ๆ ที่คุณชอบ.  

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าคลาสที่คุณต้องการ ซึ่งจะทำให้คุณเข้าถึงการโหลดภาพ, ตัวเลือกการโหลด, และฟังก์ชันการบันทึก.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

กำหนดโฟลเดอร์ที่บรรจุไฟล์ PSD ต้นฉบับ. แทนที่ตัวแสดงตำแหน่งด้วยพาธจริงบนเครื่องของคุณ.

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดภาพพร้อมฟอนต์สำรอง

สร้างอินสแตนซ์ของ `PsdLoadOptions`, ระบุฟอนต์สำรองเริ่มต้น (เช่น **Arial**), และโหลด PSD. Aspose จะใช้ฟอนต์สำรองโดยอัตโนมัติเมื่อพบฟอนต์ที่หายไป.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## ขั้นตอนที่ 3: บันทึกภาพที่แทนที่แล้ว

หลังจากการแทนที่ฟอนต์, คุณสามารถส่งออกภาพในรูปแบบที่รองรับใดก็ได้ ที่นี่เราบันทึกเป็น PNG, แต่คุณก็สามารถเลือก JPEG, BMP, หรือแม้กระทั่งเขียนกลับเป็น PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| ข้อความแสดงผลเป็นอักขระผิดหลังการแทนที่ | ฟอนต์สำรองไม่มี glyph ที่จำเป็น | เลือกฟอนต์ที่รองรับช่วง Unicode ที่ต้องการ (เช่น “Arial Unicode MS”). |
| `OutOfMemoryError` บน PSD ขนาดใหญ่ | โหลดไฟล์ความละเอียดสูงมากโดยไม่มีหน่วยความจำ heap เพียงพอ | เพิ่มขนาด heap ของ JVM (`-Xmx2g`) หรือโหลดภาพในโหมดสตรีมมิ่งหากมีให้ใช้. |
| ข้อยกเว้นใบอนุญาต | ใช้เวอร์ชันทดลองในการผลิต | ใช้ใบอนุญาตถาวรหรือชั่วคราวที่ถูกต้องก่อนโหลดภาพ. |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถแทนที่ฟอนต์ในรูปแบบภาพอื่นนอกจาก PSD ได้หรือไม่?**  
A: ใช่. แม้ว่ากรณีการใช้งานหลักจะเป็น PSD, Aspose.PSD ยังรองรับ PNG, JPEG, BMP, และ TIFF, ทำให้สามารถแทนที่ฟอนต์ได้เมื่อมีเลเยอร์ข้อความ.

**ถาม: ฟอนต์สำรองเริ่มต้นเป็นสิ่งจำเป็นหรือไม่?**  
A: ไม่. คุณสามารถตั้งค่าฟอนต์ TrueType ใดก็ได้ที่ต้องการ, หรือไม่ตั้งค่าเพื่อให้ Aspose ใช้ค่าเริ่มต้นภายใน.

**ถาม: มีข้อกำหนดด้านใบอนุญาตสำหรับการใช้ Aspose.PSD หรือไม่?**  
A: จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมการผลิต. ดูรายละเอียดที่ [purchase page](https://purchase.aspose.com/buy).

**ถาม: ฉันสามารถขอใบอนุญาตชั่วคราวเพื่อทดสอบได้หรือไม่?**  
A: แน่นอน. Aspose มีใบอนุญาตชั่วคราวฟรีสำหรับการประเมิน – เยี่ยมชม [temporary license page](https://purchase.aspose.com/temporary-license/).

**ถาม: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมหรือหารือเกี่ยวกับปัญหา Aspose.PSD ได้จากที่ไหน?**  
A: ฟอรั่มชุมชนเป็นสถานที่ที่ดีสำหรับการถามคำถาม: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**ถาม: ฉันจะจัดการไฟล์ PSD ที่มีฟอนต์หายหลายตัวอย่างไร?**  
A: ตั้งค่าฟอนต์สำรองเริ่มต้นครั้งเดียว (ตามที่แสดง) – จะถูกนำไปใช้กับ *ฟอนต์ที่หายทั้งหมด* ระหว่างการโหลด.

**ถาม: สามารถแทนที่ฟอนต์หลังจากที่ภาพถูกบันทึกแล้วได้หรือไม่?**  
A: การแทนที่ฟอนต์ต้องทำในขั้นตอนการโหลด. หากต้องการเปลี่ยนฟอนต์ภายหลัง, ให้โหลด PSD ใหม่ด้วยฟอนต์สำรองที่ต่างกันและบันทึกใหม่.

## สรุป

คุณได้เห็นกระบวนการทำงาน **aspose psd font substitution** อย่างครบถ้วนใน Java—ตั้งแต่การนำเข้าคลาสที่ถูกต้อง, การกำหนดฟอนต์สำรอง, การโหลด PSD, จนถึงการส่งออกภาพที่แก้ไขแล้ว. นำรูปแบบนี้ไปใช้ใน pipeline การประมวลผลภาพของคุณเพื่อให้การจัดการตัวอักษรสอดคล้องกันในทุกทรัพยากร PSD และเพื่อ **handle missing fonts PSD** โดยอัตโนมัติ.

---

**อัปเดตล่าสุด:** 2026-02-09  
**ทดสอบกับ:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**ผู้เขียน:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
