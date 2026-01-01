---
date: 2026-01-01
description: เรียนรู้วิธีสร้างบิตแมพใน Java โดยใช้สตรีมใน Aspose.PSD, บันทึกไฟล์ภาพใน
  Java, และตั้งค่าบิตต่อพิกเซลอย่างมีประสิทธิภาพ.
linktitle: Create Image using Stream
second_title: Aspose.PSD Java API
title: สร้างบิตแมป Java ด้วย Stream ใน Aspose.PSD
url: /th/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง bitmap java ด้วย Stream ใน Aspose.PSD

## Introduction

หากคุณต้องการ **create bitmap java** ภาพแบบเรียลไทม์ Aspose.PSD for Java จะมอบวิธีการที่สะอาดและใช้ Stream ซึ่งเร็วและประหยัดหน่วยความจำ ในบทแนะนำนี้เราจะอธิบายขั้นตอนการสร้างภาพ bitmap จาก Stream, การกำหนดบิตต่อพิกเซล, และสุดท้าย **save image file java** ไปยังดิสก์ เมื่อเสร็จคุณจะเข้าใจว่าทำไมวิธีนี้เหมาะสำหรับการประมวลผลภาพบนเซิร์ฟเวอร์, งานแบช, หรือสถานการณ์ใด ๆ ที่ต้องการหลีกเลี่ยงไฟล์ชั่วคราว

## Quick Answers
- **“create bitmap java” หมายถึงอะไร?** It refers to programmatically generating a BMP image using Java code.  
- **ไลบรารีใดจัดการกับ stream?** Aspose.PSD’s `StreamSource` and `FileCreateSource` classes.  
- **ฉันสามารถตั้งค่าความลึกสีได้หรือไม่?** Yes – use `BmpOptions.setBitsPerPixel(int)` (e.g., 24 bpp).  
- **ฉันจะบันทึกผลลัพธ์อย่างไร?** Call `image.save(outputPath)` to **save image file java**.  
- **ต้องใช้ใบอนุญาตสำหรับการผลิตหรือไม่?** A valid Aspose.PSD license is needed for commercial use.

## ข้อกำหนดเบื้องต้นสำหรับการสร้าง bitmap java

ก่อนเริ่มต้น โปรดตรวจสอบว่าคุณมี:

- **Java Development Kit (JDK)** – เวอร์ชันล่าสุดใดก็ได้ (8 หรือสูงกว่า).  
- **Aspose.PSD for Java** – ดาวน์โหลด JAR เวอร์ชันล่าสุดจาก [documentation](https://reference.aspose.com/psd/java/).  
- **IDE** – Eclipse, IntelliJ IDEA หรือเครื่องมือแก้ไขที่รองรับ Java ที่คุณต้องการ.

## นำเข้าแพ็กเกจสำหรับการสร้าง bitmap

เริ่มต้นด้วยการนำเข้า namespace ที่จำเป็น ซึ่งจะให้คุณเข้าถึงการสร้างภาพ, ตัวเลือก BMP, และการจัดการ stream.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

แทนที่ `"Your Document Directory"` ด้วยเส้นทางเต็มที่คุณเก็บไฟล์ต้นฉบับและไฟล์ผลลัพธ์ของคุณ.

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: กำหนดชื่อไฟล์ผลลัพธ์

นี่คือเส้นทางที่การดำเนินการ **save image file java** จะเขียน bitmap ไปยัง.

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

## ขั้นตอนที่ 3: กำหนดค่า BmpOptions (ตั้งค่าบิตต่อพิกเซล)

ที่นี่เราจะ **set bits per pixel** เป็น 24 bpp ซึ่งจะได้ bitmap แบบสีจริง ปรับค่าตามที่คุณต้องการความลึกสีที่แตกต่าง.

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

## ขั้นตอนที่ 4: สร้าง FileCreateSource (แหล่ง stream)

`FileCreateSource` ห่อหุ้มไฟล์ stream เพื่อให้ Aspose.PSD สามารถเขียนโดยตรงไปยังปลายทางโดยไม่ต้องใช้บัฟเฟอร์กลาง.

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

## ขั้นตอนที่ 5: สร้างภาพ Bitmap

บรรทัดนี้ **generates a bitmap java** ภาพขนาด 500 × 500 พิกเซลโดยใช้ตัวเลือกที่เรากำหนดไว้ก่อนหน้า.

```java
Image image = Image.create(imageOptions, 500, 500);
```

## ขั้นตอนที่ 6: ดำเนินการประมวลผลภาพและบันทึก

หลังจากการปรับแต่งเพิ่มเติมใด ๆ การเรียก `image.save` จะ **saves the image file java** ไปยังตำแหน่งที่ระบุใน `desName`.

```java
// Perform desired image processing operations here
// For example, you could draw shapes, apply filters, etc.

// Save the processed bitmap to disk
image.save(desName);
```

## สรุป

คุณได้เรียนรู้วิธี **create bitmap java** ภาพโดยใช้ stream ใน Aspose.PSD, ควบคุมความลึกสีด้วย **set bits per pixel**, และ **save image file java** อย่างมีประสิทธิภาพแล้ว ลองทดลองกับขนาดต่าง ๆ, รูปแบบพิกเซล, หรือขั้นตอนการประมวลผลเพิ่มเติมเพื่อให้ตรงกับความต้องการของโครงการของคุณ.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.PSD กับไลบรารี Java อื่น ๆ ได้หรือไม่?

A1: ใช่, Aspose.PSD ถูกออกแบบให้ผสานรวมกับไลบรารี Java อื่น ๆ อย่างราบรื่น ทำให้คุณมีความยืดหยุ่นในโครงการของคุณ.

### Q2: ฉันจะหาแหล่งสนับสนุนสำหรับคำถามที่เกี่ยวกับ Aspose.PSD ได้จากที่ไหน?

A2: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

### Q3: มีการทดลองใช้ฟรีสำหรับ Aspose.PSD หรือไม่?

A3: มี, คุณสามารถเข้าถึงการทดลองใช้ฟรีได้ [ที่นี่](https://releases.aspose.com/).

### Q4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD อย่างไร?

A4: รับใบอนุญาตชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ความต้องการระบบสำหรับ Aspose.PSD มีอะไรบ้าง?

A5: ดูที่ [documentation](https://reference.aspose.com/psd/java/) เพื่อดูความต้องการระบบโดยละเอียด.

---

**อัปเดตล่าสุด:** 2026-01-01  
**ทดสอบด้วย:** Aspose.PSD Java latest release  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}