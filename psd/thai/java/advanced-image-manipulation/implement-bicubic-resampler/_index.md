---
date: 2026-04-12
description: เรียนรู้วิธีปรับขนาดภาพใน Java ด้วย Bicubic Resampler ของ Aspose.PSD.
  บทแนะนำการสเกลภาพนี้แสดงขั้นตอนทีละขั้นตอนเพื่อให้ได้ผลลัพธ์ที่เหนือกว่า.
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: ดำเนินการรีซแอมพลเลอร์แบบไบคิวบิก
second_title: Aspose.PSD Java API
title: ปรับขนาดภาพ Java – ตัวรีซามพลเลอร์แบบบิกิวบิกสำหรับการสเกลคุณภาพสูง
url: /th/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ปรับขนาดภาพ Java – Bicubic Resampler สำหรับการสเกลคุณภาพสูง

## บทนำ

หากคุณต้องการ **resize image java** โปรเจกต์โดยไม่สูญเสียความคมชัดหรือทำให้เกิดศิลปะบกพร่อง คุณมาถูกที่แล้ว ใน **image scaling tutorial** นี้เราจะอธิบายการใช้ Bicubic Resampler ของ Aspose.PSD — ฟีเจอร์ที่ทรงพลังของ **java image library** ที่ให้ผลลัพธ์ที่เรียบเนียนและคมชัดสำหรับไฟล์ PSD และรูปแบบอื่น ๆ มากมาย เมื่อจบคู่มือคุณจะสามารถผสานการสเกลคุณภาพสูงเข้าไปในแอปพลิเคชัน Java ใดก็ได้ด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบด่วน
- **What does the Bicubic Resampler do?** มันใช้ขั้นตอนการแทรกแซงที่ซับซ้อนซึ่งรักษารายละเอียดเมื่อปรับขนาดภาพ  
- **Which ResizeType values are available?** `CubicConvolution` และ `Bell` เป็นสองตัวเลือก Bicubic ที่ Aspose.PSD ให้มา  
- **Do I need a license to run the code?** ใบอนุญาต aspose ชั่วคราวทำงานสำหรับการประเมิน; จำเป็นต้องมีใบอนุญาตเต็มสำหรับการผลิต  
- **What Java version is required?** Runtime Java 8+ ใดก็เข้ากันได้กับไลบรารี Aspose.PSD เวอร์ชันล่าสุด  
- **Can I resize other formats (PNG, JPEG) with the same API?** ใช่, Aspose.PSD รองรับหลายประเภทของภาพ แม้ว่าตัวอย่างจะเน้นที่ PSD  

## การสเกลภาพคุณภาพสูงคืออะไร

การสเกลภาพคุณภาพสูงหมายถึงการปรับขนาดภาพโดยยังคงรักษาขอบที่คมชัด, การไล่สีที่เรียบเนียน, และการแสดงสีที่แม่นยำ. Bicubic Resampler ทำเช่นนี้โดยพิจารณาค่าของพิกเซลรอบข้าง (ใช้ cubic convolution หรืออัลกอริทึม Bell) เพื่อคำนวณพิกเซลใหม่แต่ละตัว, ส่งผลให้ได้ลักษณะที่เป็นธรรมชาติมากกว่าวิธี nearest‑neighbor หรือ bilinear.

## ทำไมต้องใช้ Bicubic Resampler สำหรับการสเกลภาพคุณภาพสูง

- **Preserves Detail:** เนื้อผิวละเอียดและเส้นงานยังคงชัดเจนแม้หลังจากการเปลี่ยนขนาดอย่างมาก  
- **Reduces Artifacts:** ลดการเกิด ringing และการเบลอที่มักพบกับอัลกอริทึมที่ง่ายกว่า  
- **Easy Integration:** การเรียกเมธอดแบบบรรทัดเดียว (`image.resize`) ทำให้คุณสลับอัลกอริทึมได้โดยไม่ต้องเขียนโค้ดใหม่  

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่ม, ตรวจสอบให้แน่ใจว่าคุณมี:

- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – JDK 8 หรือใหม่กว่า ติดตั้งและกำหนดค่าแล้ว  
- **Sample PSD file** – ภาพทดสอบ (เช่น `sample_bicubic.psd`) วางไว้ในไดเรกทอรีที่ทราบ  

รายการเหล่านี้ร่วมกันสร้างพื้นฐาน **java image library** ที่แข็งแกร่งสำหรับบทเรียน

## นำเข้าแพ็กเกจ

เพิ่มการนำเข้า (import) ที่จำเป็นไปยังคลาส Java ของคุณ. สิ่งเหล่านี้จะนำเข้าคลาสหลักของ Aspose.PSD และ enumeration `ResizeType`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## วิธีปรับขนาดภาพ Java ด้วย Bicubic Resampler

### ขั้นตอนที่ 1: โหลดภาพ

แรก, โหลดไฟล์ PSD ต้นฉบับที่คุณต้องการปรับขนาด. แทนที่ `Your Document Directory` ด้วยเส้นทางจริงบนเครื่องของคุณ.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### ขั้นตอนที่ 2: ปรับขนาดด้วย Cubic Convolution (คุณภาพสูง)

ตอนนี้ใช้ขั้นตอนอัลกอริธึม **Cubic Convolution**, หนึ่งในสองตัวเลือก Bicubic ที่ให้การสเกลภาพคุณภาพสูง. ตัวอย่างนี้ปรับขนาดภาพเป็น 300 × 300 พิกเซล.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### ขั้นตอนที่ 3: ปรับขนาดด้วย Bell Algorithm (คุณภาพสูงทางเลือก)

หากคุณต้องการอัลกอริธึม **Bell**, ซึ่งให้ผลการทำให้เรียบที่แตกต่างเล็กน้อย, คุณสามารถใช้ได้ในลักษณะเดียวกัน. โปรดสังเกตว่าเราจะโหลดภาพต้นฉบับใหม่เพื่อให้การเปรียบเทียบเป็นธรรม.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

คุณสามารถทดลองกับมิติหรือรูปแบบไฟล์อื่น ๆ ได้ตามต้องการ — เพียงปรับพารามิเตอร์ให้เหมาะสม.

## ข้อผิดพลาดทั่วไปและเคล็ดลับ

- **Incorrect Path:** ตรวจสอบให้แน่ใจว่า `dataDir` ลงท้ายด้วยตัวคั่นไฟล์ (`/` หรือ `\`) ที่เหมาะสมกับ OS ของคุณ.  
- **License Exceptions:** การทำงานโดยไม่มีใบอนุญาตที่ถูกต้องอาจเพิ่มลายน้ำลงในภาพผลลัพธ์. ใช้ **temporary aspose license** สำหรับการทดสอบ, แล้วเปลี่ยนเป็นใบอนุญาตถาวรสำหรับการผลิต.  
- **Memory Usage:** ไฟล์ PSD ขนาดใหญ่สามารถใช้หน่วยความจำมาก; พิจารณาปล่อยภาพ (`image.dispose()`) หลังจากบันทึก.  

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.PSD for Java กับรูปแบบภาพอื่นได้หรือไม่?**  
A: ใช่, ไลบรารีนี้รองรับ PSD, PNG, JPEG, TIFF, BMP, และอื่น ๆ อีกมากมาย.  

**Q: มีใบอนุญาตชั่วคราวสำหรับ Aspose.PSD for Java หรือไม่?**  
A: ใช่, คุณสามารถรับใบอนุญาตชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).  

**Q: ฉันสามารถหาแหล่งสนับสนุนสำหรับ Aspose.PSD for Java ได้ที่ไหน?**  
A: เยี่ยมชมฟอรั่ม Aspose.PSD [here](https://forum.aspose.com/c/psd/34) สำหรับคำถามที่เกี่ยวกับการสนับสนุน.  

**Q: ฉันสามารถดาวน์โหลดไลบรารี Aspose.PSD for Java ได้หรือไม่?**  
A: ใช่, ดาวน์โหลดไลบรารีจากหน้าปล่อยเวอร์ชัน [here](https://releases.aspose.com/psd/java/).  

**Q: ฉันจะซื้อ Aspose.PSD for Java ได้อย่างไร?**  
A: คุณสามารถซื้อ Aspose.PSD for Java ได้จากหน้าซื้อ [here](https://purchase.aspose.com/buy).  

---

**อัปเดตล่าสุด:** 2026-04-12  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}