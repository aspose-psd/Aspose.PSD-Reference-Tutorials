---
date: 2025-12-01
description: เรียนรู้วิธีทำให้การปรับขนาดภาพคุณภาพสูงใน Java ด้วย Bicubic Resampler
  ของ Aspose.PSD. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อผลลัพธ์ที่เหนือกว่า.
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: การปรับขนาดภาพคุณภาพสูงด้วย Bicubic Resampler ใน Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การปรับขนาดภาพคุณภาพสูงด้วย Bicubic Resampler ใน Aspose.PSD for Java

## บทนำ

การปรับขนาดภาพคุณภาพสูงเป็นความต้องการที่พบบ่อยเมื่อคุณต้องการเปลี่ยนขนาดกราฟิกโดยไม่สูญเสียความคมชัดของภาพ Aspose.PSD for Java มี **Bicubic Resampler** ที่ให้ผลลัพธ์ที่เรียบและคมชัดสำหรับไฟล์ PSD และรูปแบบที่รองรับอื่น ๆ ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีการใช้ Bicubic Resampler อย่างละเอียดขั้นตอนต่อขั้นตอน เพื่อให้คุณสามารถนำการปรับขนาดภาพคุณภาพสูงไปใช้ในแอปพลิเคชัน Java ของคุณได้ทันที

## คำตอบสั้น
- **Bicubic Resampler ทำอะไร?** มันใช้ขั้นตอนการประมาณค่าที่ซับซ้อนเพื่อรักษารายละเอียดเมื่อปรับขนาดภาพ  
- **ค่า ResizeType ที่มีให้เลือกมีอะไรบ้าง?** `CubicConvolution` และ `Bell` คือสองตัวเลือก Bicubic ที่ Aspose.PSD มีให้  
- **ต้องมีลิขสิทธิ์เพื่อรันโค้ดหรือไม่?** ลิขสิทธิ์ชั่วคราวใช้ได้สำหรับการประเมินผล; ต้องมีลิขสิทธิ์เต็มสำหรับการใช้งานจริง  
- **ต้องใช้ Java เวอร์ชันใด?** ทุก Runtime Java 8 ขึ้นไปเข้ากันได้กับไลบรารี Aspose.PSD เวอร์ชันล่าสุด  
- **สามารถปรับขนาดรูปแบบอื่น (PNG, JPEG) ด้วย API เดียวกันได้หรือไม่?** ได้, Aspose.PSD รองรับหลายรูปแบบภาพ แม้ว่าตัวอย่างจะเน้นที่ PSD  

## การปรับขนาดภาพคุณภาพสูงคืออะไร?

การปรับขนาดภาพคุณภาพสูงหมายถึงการเปลี่ยนขนาดภาพโดยยังคงรักษาขอบที่คม, การไล่สีที่เรียบ, และการแสดงสีที่แม่นยำ Bicubic Resampler ทำได้โดยพิจารณาค่าของพิกเซลรอบข้าง (โดยใช้ cubic convolution หรืออัลกอริทึม Bell) เพื่อคำนวณพิกเซลใหม่แต่ละจุด ทำให้ได้ภาพที่ดูเป็นธรรมชาติมากกว่าวิธี nearest‑neighbor หรือ bilinear

## ทำไมต้องใช้ Bicubic Resampler สำหรับการปรับขนาดภาพคุณภาพสูง?

- **รักษารายละเอียด:** เนื้อผิวและเส้นที่ละเอียดยังคงชัดเจนแม้หลังจากการเปลี่ยนขนาดอย่างมาก  
- **ลดอาการบิดเบือน:** ลดการเกิด ringing และการเบลอที่มักพบกับอัลกอริทึมที่ง่ายกว่า  
- **ผสานรวมง่าย:** การเรียกเมธอดแบบบรรทัดเดียว (`image.resize`) ทำให้คุณสลับอัลกอริทึมได้โดยไม่ต้องเขียนโค้ดใหม่  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน ตรวจสอบให้แน่ใจว่าคุณมี:

- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)  
- **Java Development Kit** – JDK 8 หรือใหม่กว่า ที่ติดตั้งและกำหนดค่าเรียบร้อย  
- **ไฟล์ PSD ตัวอย่าง** – ภาพทดสอบ (เช่น `sample_bicubic.psd`) ที่วางไว้ในไดเรกทอรีที่รู้จัก  

## นำเข้าแพ็กเกจ

เพิ่มการนำเข้าที่จำเป็นลงในคลาส Java ของคุณ เพื่อดึงคลาสหลักของ Aspose.PSD และ enumeration `ResizeType`

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## ขั้นตอนที่ 1: โหลดภาพ

แรกสุดให้โหลดไฟล์ PSD ต้นฉบับที่คุณต้องการปรับขนาด แทนที่ `Your Document Directory` ด้วยพาธจริงบนเครื่องของคุณ

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## ขั้นตอนที่ 2: ปรับขนาดด้วย Cubic Convolution (คุณภาพสูง)

ต่อไปให้ใช้ **Cubic Convolution** ซึ่งเป็นหนึ่งในสองตัวเลือก Bicubic ที่ให้การปรับขนาดภาพคุณภาพสูง ตัวอย่างนี้ปรับขนาดภาพเป็น 300 × 300 พิกเซล

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## ขั้นตอนที่ 3: ปรับขนาดด้วย Bell Algorithm (คุณภาพสูงแบบทางเลือก)

หากคุณต้องการใช้ **Bell** algorithm ซึ่งให้เอฟเฟกต์การทำให้เรียบที่แตกต่างเล็กน้อย คุณสามารถใช้ได้ในลักษณะเดียวกัน โปรดสังเกตว่าเราจะโหลดภาพต้นฉบับใหม่เพื่อให้การเปรียบเทียบเป็นธรรม

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

คุณสามารถทดลองกับมิติอื่นหรือรูปแบบไฟล์อื่นได้—เพียงปรับพารามิเตอร์ตามต้องการ

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **พาธไม่ถูกต้อง:** ตรวจสอบให้ `dataDir` ลงท้ายด้วยเครื่องหมายแยกไฟล์ (`/` หรือ `\`) ที่เหมาะกับระบบปฏิบัติการของคุณ  
- **ข้อยกเว้นลิขสิทธิ์:** การรันโดยไม่มีลิขสิทธิ์ที่ถูกต้องอาจทำให้ภาพผลลัพธ์มีลายน้ำ  
- **การใช้หน่วยความจำ:** ไฟล์ PSD ขนาดใหญ่ใช้หน่วยความจำมาก; ควรทำลายอ็อบเจ็กต์ภาพ (`image.dispose()`) หลังจากบันทึกเสร็จ  

## คำถามที่พบบ่อย

**ถาม: สามารถใช้ Aspose.PSD for Java กับรูปแบบภาพอื่นได้หรือไม่?**  
ตอบ: ได้, ไลบรารีรองรับ PSD, PNG, JPEG, TIFF, BMP และรูปแบบอื่น ๆ อีกหลายประเภท  

**ถาม: มีลิขสิทธิ์ชั่วคราวสำหรับ Aspose.PSD for Java หรือไม่?**  
ตอบ: มี, คุณสามารถรับลิขสิทธิ์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/)  

**ถาม: จะหาแหล่งสนับสนุนสำหรับ Aspose.PSD for Java ได้ที่ไหน?**  
ตอบ: เยี่ยมชมฟอรั่ม Aspose.PSD [ที่นี่](https://forum.aspose.com/c/psd/34) สำหรับคำถามเกี่ยวกับการสนับสนุน  

**ถาม: สามารถดาวน์โหลดไลบรารี Aspose.PSD for Java ได้หรือไม่?**  
ตอบ: ได้, ดาวน์โหลดไลบรารีจากหน้าปล่อยเวอร์ชัน [ที่นี่](https://releases.aspose.com/psd/java/)  

**ถาม: จะซื้อ Aspose.PSD for Java อย่างไร?**  
ตอบ: คุณสามารถซื้อ Aspose.PSD for Java ได้จากหน้าซื้อ [ที่นี่](https://purchase.aspose.com/buy)  

---

**Last Updated:** 2025-12-01  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}