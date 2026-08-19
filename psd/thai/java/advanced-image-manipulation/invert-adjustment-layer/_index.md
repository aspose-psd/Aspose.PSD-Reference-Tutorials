---
date: 2026-04-22
description: เรียนรู้วิธีใช้ไลบรารีการประมวลผลภาพ Java Aspose.PSD เพื่อใช้หลายเลเยอร์ปรับแต่ง
  รวมถึงเลเยอร์ปรับแต่ง Invert สำหรับการจัดการไฟล์ PSD อย่างราบรื่น
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: เลเยอร์ปรับค่ากลับสี
second_title: Aspose.PSD Java API
title: 'ไลบรารี Java สำหรับการประมวลผลภาพ: กลับสีเลเยอร์ด้วย Aspose.PSD'
url: /th/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ชั้นปรับค่า Invert ใน Aspose.PSD สำหรับ Java

## บทนำ

หากคุณกำลังมองหา **image processing java library** ที่แข็งแกร่ง Aspose.PSD for Java เป็นหนึ่งในตัวเลือกที่หลากหลายที่สุดในตลาด ในบทเรียนนี้เราจะอธิบายวิธีเพิ่ม **Invert Adjustment Layer** ลงในไฟล์ PSD ซึ่งเป็นเทคนิคที่คุณสามารถผสานกับชั้นปรับค่าอื่น ๆ เพื่อสร้างเอฟเฟกต์ภาพที่ซับซ้อน ไม่ว่าคุณจะสร้างเครื่องมือประมวลผลเป็นชุด, บริการภาพฝั่งเซิร์ฟเวอร์, หรือโปรแกรมแก้ไขภาพเดี่ยว คู่มือนี้จะให้เส้นทางที่ชัดเจนและเป็นขั้นตอนเพื่อทำงานให้เสร็จเร็วและเชื่อถือได้

## คำตอบอย่างรวดเร็ว
- **What does the Invert Adjustment Layer do?** มันกลับค่าสีทั้งหมดในพื้นที่ที่เลือก, สร้างเอฟเฟกต์ภาพลบ (เช่น, มัน **converts PSD to negative**).  
- **Which library provides this feature?** Aspose.PSD, a leading **image processing java library**.  
- **Can I stack it with other adjustments?** Yes – you can **apply multiple adjustment layers** such as Brightness/Contrast, Hue/Saturation, and more.  
- **Do I need a license for development?** A free trial is available; a license is required for production use.  
- **How long does the implementation take?** Typically under 10 minutes for a basic use‑case.

## ชั้นปรับค่า Invert คืออะไร?

ชั้นปรับค่า Invert เป็นการแก้ไขแบบไม่ทำลายที่สลับค่ารหัสสี RGB ของพิกเซลทุกพิกเซลที่มันส่งผลกระทบ เนื่องจากมันอยู่บนสุดของสแตกชั้น, คุณสามารถสลับการมองเห็นหรือจัดลำดับใหม่ได้โดยไม่ทำให้ข้อมูลภาพต้นฉบับเปลี่ยนแปลงอย่างถาวร นี่เป็นวิธีที่ง่ายที่สุดในการ **invert colors PSD** ไฟล์หรือสร้างภาพลบแบบถ่ายภาพ

## ทำไมต้องใช้ Aspose.PSD เป็นไลบรารีการประมวลผลภาพ Java ของคุณ?

- **Full PSD support** – อ่าน, แก้ไข, และเขียนไฟล์ Photoshop โดยไม่ต้องติดตั้ง Photoshop.  
- **Cross‑platform** – ทำงานบน Java runtime ใดก็ได้ (Java 6+).  
- **Rich adjustment features** – มีเมธอดในตัวสำหรับการแก้ไขทั่วไปหลายอย่าง ทำให้ง่ายต่อการ **apply multiple adjustment layers** ในเวิร์กโฟลเดียว.  
- **Performance‑optimized** – จัดการไฟล์ขนาดใหญ่ได้อย่างมีประสิทธิภาพ ซึ่งจำเป็นสำหรับ **batch process psd images**.

## ข้อกำหนดเบื้องต้น

1. **Aspose.PSD Library** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – ติดตั้งและกำหนดค่า JDK 6.0 หรือใหม่กว่า.  

ตอนนี้, เรามาเจาะลึกโค้ดกัน

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็น การนำเข้าต่าง ๆ นี้ให้คุณเข้าถึง API การจัดการภาพหลักและฟังก์ชันเฉพาะของ PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

กำหนดโฟลเดอร์ที่บรรจุไฟล์ PSD ต้นฉบับของคุณและที่ที่ผลลัพธ์จะถูกบันทึก.

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

โหลดไฟล์ต้นฉบับเข้าสู่วัตถุ `PsdImage` วัตถุนี้แทนเอกสาร PSD ทั้งหมดในหน่วยความจำ.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## ขั้นตอนที่ 3: เพิ่มชั้นปรับค่า Invert

เรียกเมธอดในตัวเพื่อแทรก Invert Adjustment Layer บนสุดของสแตกชั้นปัจจุบัน คุณสามารถเพิ่มชั้นอื่น ๆ ต่อไป (เช่น Brightness, Hue) เพื่อ **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## ขั้นตอนที่ 4: บันทึกผลลัพธ์

บันทึก PSD ที่แก้ไขแล้วลงดิสก์ ไฟล์ที่บันทึกแล้วจะมี Invert Adjustment Layer อยู่และสามารถเปิดใน Photoshop หรือโปรแกรมดู PSD ที่รองรับได้.

```java
im.save(outputPath);
```

### เกิดอะไรขึ้น?

- PSD ถูกโหลดเข้าสู่หน่วยความจำ.  
- Invert Adjustment Layer ถูกเพิ่มเป็นชั้นบนสุด.  
- ภาพถูกบันทึก, รักษาการแก้ไขแบบไม่ทำลาย.

คุณได้ใช้ Aspose.PSD, **image processing java library** ที่ประสบความสำเร็จในการจัดการไฟล์ PSD.

## การประมวลผลชุดไฟล์ PSD ด้วยการปรับค่า invert

หากคุณต้องการใช้เอฟเฟกต์ invert เดียวกันกับไฟล์หลายสิบหรือหลายร้อยไฟล์, คุณสามารถใส่โค้ดข้างต้นในลูปง่าย ๆ ที่วนผ่านไดเรกทอรีของ PSDs เนื่องจากไลบรารีนี้ **performance‑optimized**, การประมวลผลชุดขนาดใหญ่ยังคงเร็ว, และคุณสามารถรวมขั้นตอน invert กับการปรับค่าอื่น ๆ (เช่น brightness, hue) ในลูปเดียวกัน.

## การแปลง PSD เป็นภาพลบ

Invert Adjustment Layer โดยพื้นฐานคือการทำงาน **convert PSD to negative** โดยการเพิ่มชั้นนี้เป็นรายการบนสุด, คุณจะได้เอฟเฟกต์ลบเต็มรูปแบบโดยไม่ทำให้ข้อมูลพิกเซลต้นฉบับเปลี่ยนแปลงอย่างถาวร คุณสามารถลบหรือปิดการใช้งานชั้นนี้ในภายหลังเพื่อกลับสู่ลักษณะเดิม.

## ปัญหาและเคล็ดลับทั่วไป

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | เส้นทางไฟล์ไม่ถูกต้องหรือไฟล์หาย | ตรวจสอบ `dataDir` และชื่อไฟล์; ใช้เส้นทางเต็มสำหรับการทดสอบ |
| **Layer order not as expected** | การเพิ่มชั้นหลังจากที่มีอยู่แล้วทำให้การจัดเรียงเปลี่ยน | ใช้ `im.addInvertAdjustmentLayer()` ก่อนเพิ่มการปรับค่าอื่น ๆ, หรือจัดลำดับชั้นใหม่ผ่าน `im.getLayers()` |
| **Performance slowdown on large PSDs** | โหลดไฟล์ขนาดใหญ่มากเข้าสู่หน่วยความจำ | พิจารณาประมวลผลหน้าเป็นส่วน ๆ หรือเพิ่มขนาด heap ของ JVM (`-Xmx2g`) |

## คำถามที่พบบ่อย

**Q: Aspose.PSD รองรับเวอร์ชัน Java ทั้งหมดหรือไม่?**  
A: Aspose.PSD รองรับ Java 6.0 ขึ้นไป.

**Q: ฉันสามารถใช้หลายชั้นปรับค่าในหนึ่งการดำเนินการได้หรือไม่?**  
A: ได้, คุณสามารถสแต็กหลายชั้นปรับค่า เช่น Invert, Brightness, และ Hue/Saturation เพื่อสร้างเอฟเฟกต์ซับซ้อนได้.

**Q: ฉันสามารถหาเอกสารเพิ่มเติมสำหรับ Aspose.PSD ได้ที่ไหน?**  
A: ดูเอกสาร [here](https://reference.aspose.com/psd/java/) สำหรับคู่มือและอ้างอิง API อย่างครบถ้วน.

**Q: มีการทดลองใช้ฟรีสำหรับ Aspose.PSD หรือไม่?**  
A: มี, คุณสามารถสำรวจการทดลองใช้ฟรี [here](https://releases.aspose.com/).

**Q: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: คุณสามารถขอรับใบอนุญาตชั่วคราว [here](https://purchase.aspose.com/temporary-license/).

**อัปเดตล่าสุด:** 2026-04-22  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}