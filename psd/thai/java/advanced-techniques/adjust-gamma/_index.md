---
date: 2026-02-27
description: เรียนรู้วิธีปรับค่าแกมม่าในการประมวลผลภาพด้วย Java และ Aspose.PSD, แปลงไฟล์
  PSD เป็น TIFF, และแก้ไขภาพที่ซีดจางในบทแนะนำสั้น.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: วิธีปรับค่าแกมม่าในการประมวลผลภาพด้วย Java และ Aspose.PSD
url: /th/java/advanced-techniques/adjust-gamma/
weight: 23
---

 block placeholders as is.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีปรับค่า Gamma ในการประมวลผลภาพ Java ด้วย Aspose.PSD

## บทนำ

หากคุณกำลังทำงานกับ **java image processing** การเรียนรู้ **วิธีปรับค่า gamma** เป็นเทคนิคพื้นฐานที่ช่วยปรับความสว่างและคอนทราสต์โดยไม่สูญเสียรายละเอียด ในบทแนะนำนี้เราจะพาคุณผ่านการใช้ **Aspose.PSD for Java** เพื่อทำการแก้ไข gamma ในไฟล์ PSD, **แปลง PSD เป็น TIFF**, และหลีกเลี่ยง **ภาพที่สีจาง** คุณจะเห็นว่าการทำเช่นนี้เร็ว, น่าเชื่อถือ, และเหมาะสำหรับ pipeline การประมวลผลภาพบนเซิร์ฟเวอร์

## คำตอบสั้น
- **Gamma correction ทำอะไร?** จะทำการแมปค่าความสว่างใหม่เพื่อทำให้พื้นที่มืดสว่างขึ้นหรือพื้นที่สว่างมืดลงโดยคงรายละเอียดโดยรวมไว้  
- **ไลบรารีใดรับผิดชอบการประมวลผล?** Aspose.PSD for Java มีเมธอด `adjustGamma` เฉพาะสำหรับภาพแรสเตอร์  
- **ฉันสามารถแปลง PSD เป็น TIFF ในขั้นตอนเดียวกันได้หรือไม่?** ได้ – หลังจากปรับค่า gamma แล้วคุณสามารถบันทึกภาพโดยตรงเป็น TIFF ด้วย `TiffOptions`  
- **ต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รองรับเวอร์ชัน Java ใด?** Aspose.PSD รองรับ Java 8 ขึ้นไป

## วิธีปรับค่า Gamma ในการประมวลผลภาพ Java
การปรับ gamma เป็นส่วนสำคัญของ **java image processing tutorial** ใด ๆ ที่เกี่ยวกับความสว่างหรือคอนทราสต์ ด้านล่างเราจะแบ่งขั้นตอน, อธิบายเหตุผลของแต่ละบรรทัด, และแสดงวิธีรวมกระบวนการนี้เข้าไปในโค้ดของคุณ

## Gamma Correction ใน Java คืออะไร?
Gamma correction เปลี่ยนความสัมพันธ์แบบไม่เชิงเส้นระหว่างค่าพิกเซลที่เข้ารหัสกับความสว่างที่แสดงผล โดยการปรับโค้ง gamma คุณสามารถ **แก้ปัญหาภาพสีจาง** หรือเพิ่มรายละเอียดในเงาโดยไม่ทำให้ไฮไลท์สว่างเกินไป

## ทำไมต้องใช้ Aspose.PSD สำหรับ Gamma Correction?
Aspose.PSD ทำหน้าที่เป็น **java image processing library** ที่ทำให้การจัดการรูปแบบ PSD ง่ายขึ้น มันจัดการโปรไฟล์สี, แคช, และให้เมธอด `adjustGamma` ที่เรียบง่าย ทำให้เหมาะสำหรับ **java gamma correction** และ workflow **convert PSD to TIFF**

## สิ่งที่ต้องเตรียม

1. **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง Java 8 หรือใหม่กว่า  
2. **ไลบรารี Aspose.PSD** – ดาวน์โหลดและเพิ่ม JAR ไปยังโปรเจกต์ของคุณ ดูที่ [documentation](https://reference.aspose.com/psd/java/) อย่างเป็นทางการ  
3. **ภาพตัวอย่าง** – ไฟล์ PSD ที่ต้องการประมวลผล (เช่น `sample.psd`)  

## นำเข้าแพ็กเกจ

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: โหลดภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

**เคล็ดลับ:** การแคชข้อมูลแรสเตอร์ครั้งเดียวจะช่วยลดการใช้หน่วยความจำเมื่อทำการปรับหลายครั้งต่อเนื่อง

## ขั้นตอนที่ 2: ปรับ Gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

คุณสามารถส่งค่าต่าง ๆ สำหรับช่องสีแดง, เขียว, และน้ำเงินได้หากต้องการปรับแต่ละช่องแยกกัน

## ขั้นตอนที่ 3: สร้าง TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

การตั้งค่า 8‑bit sample (`{8,8,8}`) จะทำให้ขนาดไฟล์ TIFF อยู่ในระดับที่เหมาะสมพร้อมคงความแม่นยำของสี

## ขั้นตอนที่ 4: บันทึกภาพผลลัพธ์

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

หลังจากบันทึกแล้ว คุณสามารถส่งไฟล์ TIFF ไปยังระบบต่อเนื่อง เช่น บริการพิมพ์หรือ API เว็บ

## กรณีการใช้งานทั่วไป

- **Pipeline กราฟิกอัตโนมัติ** – ปรับ gamma แบบเรียลไทม์ก่อนสร้างภาพย่อ  
- **เครื่องมือแปลงแบบแบตช์** – แปลงคลัง PSD ขนาดใหญ่เป็น TIFF พร้อมทำให้ความสว่างเป็นมาตรฐาน  
- **เว็บเซอร์วิส** – เปิด endpoint ที่รับ PSD, ทำ gamma correction, และคืนค่า TIFF ให้กับไคลเอนต์  

## ปัญหาที่พบบ่อยและวิธีแก้

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Image appears washed out** | ค่า Gamma สูงเกินไป (เช่น > 2.5) | ลดค่า gamma ให้อยู่ระหว่าง 1.8‑2.2 |
| **`rasterImage.isCached()` returns false** | ภาพยังไม่ได้โหลดเข้าสู่หน่วยความจำ | เรียก `rasterImage.cacheData()` ก่อนปรับ gamma |
| **TIFF file size is large** | Bits per sample ตั้งเป็น 16‑bit | ใช้ 8‑bit sample (`{8,8,8}`) ตามตัวอย่าง |

## คำถามที่พบบ่อย

**Q: สามารถใช้ค่า gamma ต่างกันสำหรับแต่ละช่องสีได้หรือไม่?**  
A: ได้ – เมธอด `adjustGamma` รับค่า float แยกสำหรับช่องสีแดง, เขียว, และน้ำเงิน

**Q: สามารถเชื่อมต่อการปรับภาพหลายขั้นตอนก่อนบันทึกได้หรือไม่?**  
A: แน่นอน คุณสามารถทำการปรับขนาด, ครอบ, หรือแก้ไขสีต่อเนื่องบนอ็อบเจ็กต์ `RasterImage` เดียวกัน

**Q: Aspose.PSD รองรับไฟล์ PSD แบบหลายหน้าไหม?**  
A: รองรับ, สามารถเข้าถึงและประมวลผลแต่ละเลเยอร์ได้แยกกัน

**Q: นอกจาก TIFF แล้วสามารถส่งออกเป็นฟอร์แมตอะไรได้บ้าง?**  
A: Aspose.PSD รองรับ PNG, JPEG, BMP และฟอร์แมตอื่น ๆ อีกหลายรูปแบบผ่านคลาส options ที่สอดคล้อง

**Q: จะหลีกเลี่ยงภาพสีจางหลังการปรับ gamma อย่างไร?**  
A: เริ่มต้นด้วยค่า gamma ปานกลาง (ประมาณ 2.0) แล้วดูตัวอย่างผลลัพธ์; ปรับค่าลงหากภาพดูสว่างเกินไป

## สรุป

ขอแสดงความยินดี! คุณได้เรียนรู้ **วิธีปรับค่า gamma** ใน workflow **java image processing**, แปลง PSD เป็น TIFF, และหลีกเลี่ยงปัญหาภาพ **สีจาง** แบบทั่วไปแล้ว รูปแบบนี้ให้การควบคุมความสว่างและคอนทราสต์อย่างละเอียด เหมาะสำหรับ pipeline กราฟิกอัตโนมัติ, เว็บเซอร์วิส, หรือยูทิลิตี้บนเดสก์ท็อป

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}