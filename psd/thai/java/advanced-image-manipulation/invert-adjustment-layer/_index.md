---
date: 2026-02-07
description: เรียนรู้วิธีใช้ไลบรารีการประมวลผลภาพ Java Aspose.PSD เพื่อใช้หลายเลเยอร์การปรับค่า
  รวมถึงเลเยอร์การปรับค่า Invert เพื่อการจัดการไฟล์ PSD อย่างราบรื่น
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'ไลบรารี Java สำหรับการประมวลผลภาพ: กลับชั้นโดยใช้ Aspose.PSD'
url: /th/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ชั้นปรับค่า Invert ใน Aspose.PSD สำหรับ Java

## บทนำ

หากคุณกำลังมองหา **image processing java library** ที่แข็งแกร่ง Aspose.PSD สำหรับ Java เป็นหนึ่งในตัวเลือกที่หลากหลายที่สุดในตลาด ในบทเรียนนี้เราจะอธิบายขั้นตอนการเพิ่ม **Invert Adjustment Layer** ลงในไฟล์ PSD ซึ่งเป็นเทคนิคที่คุณสามารถผสานกับชั้นปรับค่าอื่น ๆ เพื่อสร้างเอฟเฟกต์ภาพที่ซับซ้อน ไม่ว่าคุณจะสร้างเครื่องมือประมวลผลแบบแบตช์หรือโปรแกรมแก้ไขภาพเดี่ยว คู่มือนี้จะให้เส้นทางที่ชัดเจนเป็นขั้นตอนเพื่อทำงานให้เสร็จเร็วขึ้น

## คำตอบอย่างรวดเร็ว
- **ชั้น Invert Adjustment Layer ทำอะไร?** มันจะกลับค่าของสีทั้งหมดในพื้นที่ที่เลือก ทำให้ได้เอฟเฟกต์ภาพลบ (negative)  
- **ไลบรารีใดให้ฟีเจอร์นี้?** Aspose.PSD ซึ่งเป็น **image processing java library** ชั้นนำ  
- **ฉันสามารถซ้อนกับการปรับค่าอื่นได้หรือไม่?** ได้ – คุณสามารถ **apply multiple adjustment layers** เช่น Brightness/Contrast, Hue/Saturation และอื่น ๆ  
- **ต้องมีลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** มีการทดลองใช้ฟรี; จำเป็นต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์จริง  
- **การทำงานนี้ใช้เวลานานแค่ไหน?** ปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับกรณีการใช้งานพื้นฐาน  

## ชั้นปรับค่า Invert คืออะไร?

ชั้น Invert Adjustment Layer เป็นการแก้ไขแบบไม่ทำลาย (non‑destructive) ที่สลับค่าของ RGB ของพิกเซลทุกพิกเซลที่มันส่งผล เนื่องจากอยู่บนสุดของสแตกเลเยอร์ คุณสามารถสลับการมองเห็นหรือจัดลำดับใหม่ได้โดยไม่ทำให้ข้อมูลภาพต้นฉบับเปลี่ยนแปลงอย่างถาวร

## วิธีการ invert ชั้นโดยใช้ Aspose.PSD

ด้านล่างนี้คุณจะเห็นขั้นตอนที่ชัดเจนเกี่ยวกับ **how to invert layer** ในไฟล์ PSD ขั้นตอนถูกออกแบบให้เรียบง่ายเพื่อให้คุณมุ่งเน้นที่แนวคิดมากกว่ารหัสโครงสร้าง

## ทำไมต้องใช้ Aspose.PSD เป็นไลบรารีการประมวลผลภาพ Java ของคุณ?

- **Full PSD support** – อ่าน, แก้ไข, และเขียนไฟล์ Photoshop ได้โดยไม่ต้องติดตั้ง Photoshop  
- **Cross‑platform** – ทำงานบน Java runtime ใดก็ได้ (Java 6+)  
- **Rich adjustment features** – มีเมธอดในตัวสำหรับการแก้ไขทั่วไปหลายอย่าง ทำให้ง่ายต่อการ **apply multiple adjustment layers** ในเวิร์กโฟลเดียว  
- **Performance‑optimized** – จัดการไฟล์ขนาดใหญ่ได้อย่างมีประสิทธิภาพ ซึ่งจำเป็นสำหรับการประมวลผลแบบแบตช์  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.PSD Library** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ [here](https://releases.aspose.com/psd/java/)  
2. **Java Development Environment** – ติดตั้งและกำหนดค่า JDK 6.0 หรือใหม่กว่า  

ตอนนี้มาดูโค้ดกันเลย

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็น การนำเข้าตัวนี้จะให้คุณเข้าถึง API การจัดการภาพหลักและฟังก์ชันเฉพาะของ PSD

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

กำหนดโฟลเดอร์ที่เก็บไฟล์ PSD ต้นฉบับและที่ที่ผลลัพธ์จะถูกบันทึก

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

โหลดไฟล์ต้นฉบับเข้าสู่วัตถุ `PsdImage` ซึ่งเป็นตัวแทนของเอกสาร PSD ทั้งหมดในหน่วยความจำ

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## ขั้นตอนที่ 3: เพิ่มชั้นปรับค่า Invert

เรียกเมธอดในตัวเพื่อแทรก Invert Adjustment Layer ที่ด้านบนของสแตกเลเยอร์ปัจจุบัน คุณสามารถเพิ่มเลเยอร์อื่น ๆ (เช่น Brightness, Hue) ต่อไปเพื่อ **apply multiple adjustment layers**

```java
im.addInvertAdjustmentLayer();
```

## ขั้นตอนที่ 4: บันทึกผลลัพธ์

บันทึก PSD ที่แก้ไขแล้วลงดิสก์ ไฟล์ที่บันทึกจะมี Invert Adjustment Layer อยู่และสามารถเปิดใน Photoshop หรือโปรแกรมดู PSD ใดก็ได้

```java
im.save(outputPath);
```

### สิ่งที่เกิดขึ้นคืออะไร?

- โหลด PSD เข้าไปในหน่วยความจำ  
- เพิ่ม Invert Adjustment Layer เป็นเลเยอร์บนสุด  
- บันทึกภาพโดยคงการแก้ไขแบบไม่ทำลายไว้  

คุณได้ใช้ Aspose.PSD, **image processing java library**, เพื่อจัดการไฟล์ PSD อย่างสำเร็จแล้ว

## ปัญหาและเคล็ดลับทั่วไป

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | เส้นทางไฟล์ไม่ถูกต้องหรือไฟล์หาย | ตรวจสอบ `dataDir` และชื่อไฟล์; ใช้เส้นทางเต็มสำหรับการทดสอบ |
| **Layer order not as expected** | การเพิ่มเลเยอร์หลังจากที่มีอยู่ทำให้ลำดับเปลี่ยน | ใช้ `im.addInvertAdjustmentLayer()` ก่อนเพิ่มการปรับค่าอื่น ๆ หรือจัดลำดับเลเยอร์ใหม่ผ่าน `im.getLayers()` |
| **Performance slowdown on large PSDs** | โหลดไฟล์ขนาดใหญ่มากเข้าสู่หน่วยความจำ | พิจารณาประมวลผลหน้าเป็นชิ้น ๆ หรือเพิ่มขนาด heap ของ JVM (`-Xmx2g`) |

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD รองรับทุกเวอร์ชันของ Java หรือไม่?**  
ตอบ: Aspose.PSD รองรับ Java 6.0 และเวอร์ชันที่ใหม่กว่า

**ถาม: ฉันสามารถใช้หลายชั้นปรับค่าในหนึ่งการดำเนินการได้หรือไม่?**  
ตอบ: ได้, คุณสามารถซ้อนหลายชั้นปรับค่า เช่น Invert, Brightness, และ Hue/Saturation เพื่อสร้างเอฟเฟกต์ที่ซับซ้อนได้

**ถาม: ฉันจะหาเอกสารเพิ่มเติมสำหรับ Aspose.PSD ได้จากที่ไหน?**  
ตอบ: ดูเอกสาร [here](https://reference.aspose.com/psd/java/) สำหรับคู่มือและอ้างอิง API อย่างครบถ้วน

**ถาม: มีการทดลองใช้ฟรีสำหรับ Aspose.PSD หรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจการทดลองใช้ฟรี [here](https://releases.aspose.com/)  

**ถาม: ฉันจะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
ตอบ: คุณสามารถขอรับลิขสิทธิ์ชั่วคราว [here](https://purchase.aspose.com/temporary-license/)  

**อัปเดตล่าสุด:** 2026-02-07  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}