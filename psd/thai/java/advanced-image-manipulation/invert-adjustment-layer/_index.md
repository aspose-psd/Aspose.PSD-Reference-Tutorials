---
date: 2025-12-02
description: เรียนรู้วิธีใช้ไลบรารีการประมวลผลภาพ Java Aspose.PSD เพื่อใช้หลายเลเยอร์การปรับค่า
  รวมถึงเลเยอร์ปรับค่า Invert สำหรับการจัดการ PSD อย่างราบรื่น
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'ไลบรารีการประมวลผลภาพ Java: กลับเลเยอร์ด้วย Aspose.PSD'
url: /th/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เลเยอร์การปรับค่า Invert ใน Aspose.PSD สำหรับ Java

## บทนำ

หากคุณกำลังมองหาหนังสือ​ไลบรารี **image processing java library** ที่แข็งแกร่ง Aspose.PSD สำหรับ Java เป็นหนึ่งในตัวเลือกที่หลากหลายที่สุดในตลาด ในบทเรียนนี้เราจะอธิบายวิธีเพิ่ม **Invert Adjustment Layer** ลงในไฟล์ PSD ซึ่งเป็นเทคนิคที่คุณสามารถผสานกับเลเยอร์การปรับค่าอื่น ๆ เพื่อสร้างเอฟเฟกต์ภาพที่ซับซ้อน ไม่ว่าคุณจะกำลังสร้างเครื่องมือประมวลผลแบบชุดหรือโปรแกรมแก้ไขภาพเดี่ยว คู่มือนี้จะให้เส้นทางที่ชัดเจนและเป็นขั้นตอนเพื่อทำงานให้เสร็จเร็วขึ้น

## คำตอบด่วน
- **เลเยอร์การปรับค่า Invert ทำอะไร?** มันจะสลับค่าของสีทั้งหมดในพื้นที่ที่เลือก ทำให้ได้เอฟเฟกต์ภาพลบ.  
- **ไลบรารีใดที่ให้คุณสมบัตินี้?** Aspose.PSD, ไลบรารี **image processing java library** ชั้นนำ.  
- **ฉันสามารถซ้อนกับการปรับค่าอื่น ๆ ได้หรือไม่?** ได้ – คุณสามารถ **apply multiple adjustment layers** เช่น Brightness/Contrast, Hue/Saturation และอื่น ๆ.  
- **ฉันต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** มีการทดลองใช้งานฟรี; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานในสภาพแวดล้อมการผลิต.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** โดยทั่วไปใช้เวลาน้อยกว่า 10 นาทีสำหรับกรณีการใช้งานพื้นฐาน.

## เลเยอร์การปรับค่า Invert คืออะไร?

เลเยอร์การปรับค่า Invert เป็นการแก้ไขแบบไม่ทำลายที่สลับค่าของ RGB ของพิกเซลทุกพิกเซลที่มันส่งผลกระทบ เนื่องจากมันอยู่บนสุดของสแตกเลเยอร์ คุณสามารถสลับการมองเห็นหรือจัดลำดับใหม่ได้โดยไม่ทำให้ข้อมูลภาพต้นฉบับเปลี่ยนแปลงอย่างถาวร

## ทำไมต้องใช้ Aspose.PSD เป็น Image Processing Java Library ของคุณ?

- **Full PSD support** – อ่าน, แก้ไข, และเขียนไฟล์ Photoshop โดยไม่ต้องติดตั้ง Photoshop.  
- **Cross‑platform** – ทำงานบน Java runtime ใดก็ได้ (Java 6+).  
- **Rich adjustment features** – มีเมธอดในตัวสำหรับการแก้ไขทั่วไปหลายอย่าง ทำให้ง่ายต่อการ **apply multiple adjustment layers** ในกระบวนการทำงานเดียว.  
- **Performance‑optimized** – จัดการไฟล์ขนาดใหญ่ได้อย่างมีประสิทธิภาพ ซึ่งสำคัญสำหรับการประมวลผลแบบชุด.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มต้น, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.PSD Library** – ดาวน์โหลดจากเว็บไซต์ทางการ [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – ติดตั้งและกำหนดค่า JDK 6.0 หรือใหม่กว่า  

ตอนนี้, เรามาเริ่มดูโค้ดกัน

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

โหลดไฟล์ต้นฉบับเข้าสู่วัตถุ `PsdImage` วัตถุนี้แสดงถึงเอกสาร PSD ทั้งหมดในหน่วยความจำ.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## ขั้นตอนที่ 3: เพิ่มเลเยอร์การปรับค่า Invert

เรียกเมธอดในตัวเพื่อแทรกเลเยอร์การปรับค่า Invert ไว้บนสุดของสแตกเลเยอร์ปัจจุบัน คุณสามารถเพิ่มเลเยอร์อื่น ๆ ต่อไป (เช่น Brightness, Hue) เพื่อ **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## ขั้นตอนที่ 4: บันทึกผลลัพธ์

บันทึก PSD ที่แก้ไขแล้วลงดิสก์ ไฟล์ที่บันทึกไว้ตอนนี้มีเลเยอร์การปรับค่า Invert อยู่และสามารถเปิดใน Photoshop หรือโปรแกรมดู PSD ที่รองรับได้.

```java
im.save(outputPath);
```

### เกิดอะไรขึ้นบ้าง?

- PSD ถูกโหลดเข้าสู่หน่วยความจำ.  
- เลเยอร์การปรับค่า Invert ถูกเพิ่มเป็นเลเยอร์บนสุด.  
- ภาพถูกบันทึก, รักษาการแก้ไขแบบไม่ทำลาย.  

คุณได้ใช้ Aspose.PSD, **image processing java library** ที่ประสบความสำเร็จในการจัดการไฟล์ PSD.

## ปัญหาที่พบบ่อยและเคล็ดลับ

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| **NullPointerException บน `Image.load`** | เส้นทางไฟล์ไม่ถูกต้องหรือไฟล์หายไป | ตรวจสอบ `dataDir` และชื่อไฟล์; ใช้เส้นทางแบบเต็มสำหรับการทดสอบ |
| **ลำดับเลเยอร์ไม่เป็นตามที่คาดหวัง** | การเพิ่มเลเยอร์หลังจากที่มีอยู่แล้วทำให้การเรียงซ้อนเปลี่ยนแปลง | ใช้ `im.addInvertAdjustmentLayer()` ก่อนเพิ่มการปรับค่าอื่น ๆ, หรือจัดลำดับเลเยอร์ใหม่ผ่าน `im.getLayers()` |
| **ประสิทธิภาพช้าลงบน PSD ขนาดใหญ่** | โหลดไฟล์ขนาดใหญ่มากเข้าสู่หน่วยความจำ | พิจารณาประมวลผลหน้าเป็นส่วน ๆ หรือเพิ่มขนาด heap ของ JVM (`-Xmx2g`) |

## คำถามที่พบบ่อย

**Q: Aspose.PSD รองรับเวอร์ชัน Java ทั้งหมดหรือไม่?**  
A: Aspose.PSD รองรับ Java 6.0 และเวอร์ชันต่อ ๆ ไป  

**Q: ฉันสามารถใช้หลายเลเยอร์การปรับค่าในหนึ่งการดำเนินการได้หรือไม่?**  
A: ได้, คุณสามารถซ้อนหลายเลเยอร์การปรับค่า—เช่น Invert, Brightness, และ Hue/Saturation—to achieve complex effects.  

**Q: ฉันสามารถหาเอกสารเพิ่มเติมสำหรับ Aspose.PSD ได้จากที่ไหน?**  
A: ดูเอกสาร [here](https://reference.aspose.com/psd/java/) สำหรับคู่มือและอ้างอิง API อย่างครอบคลุม.  

**Q: มีการทดลองใช้ฟรีสำหรับ Aspose.PSD หรือไม่?**  
A: มี, คุณสามารถสำรวจการทดลองใช้ฟรี [here](https://releases.aspose.com/).  

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: คุณสามารถขอรับไลเซนส์ชั่วคราว [here](https://purchase.aspose.com/temporary-license/).  

---

**อัปเดตล่าสุด:** 2025-12-02  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}