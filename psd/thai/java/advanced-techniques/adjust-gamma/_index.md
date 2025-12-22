---
date: 2025-12-21
description: เรียนรู้วิธีทำการประมวลผลภาพด้วย Java โดยการปรับแกมมาของภาพด้วย Aspose.PSD
  คู่มือแบบขั้นตอนต่อขั้นตอนในการแปลง PSD เป็น TIFF และทำการปรับแกมมา
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: การประมวลผลภาพด้วย Java – ปรับค่าแกมม่าโดยใช้ Aspose.PSD
url: /th/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การประมวลผลภาพด้วย Java – ปรับค่า Gamma ด้วย Aspose.PSD

## บทนำ

หากคุณกำลังทำงานกับ **java image processing** การปรับค่า gamma ของภาพเป็นเทคนิคพื้นฐานเพื่อปรับปรุงความสว่างและความคอนทราสต์โดยไม่สูญเสียรายละเอียด ในบทเรียนนี้เราจะอธิบายวิธีใช้ **Aspose.PSD for Java** เพื่อทำการแก้ไข gamma ให้กับไฟล์ PSD แล้วส่งออกผลลัพธ์เป็นภาพ TIFF คุณจะเห็นว่าทำไมวิธีนี้จึงเร็ว เชื่อถือได้ และเหมาะอย่างยิ่งสำหรับ pipeline ภาพบนเซิร์ฟเวอร์

## คำตอบอย่างรวดเร็ว
- **การแก้ไขค่า gamma ทำอะไร?** มันทำการแมปค่าความสว่างใหม่เพื่อทำให้พื้นที่มืดสว่างขึ้นหรือพื้นที่สว่างมืดลงในขณะที่ยังคงรักษารายละเอียดโดยรวม  
- **ไลบรารีใดที่จัดการการประมวลผล?** Aspose.PSD for Java มีเมธอด `adjustGamma` เฉพาะสำหรับภาพแรสเตอร์  
- **ฉันสามารถแปลง PSD เป็น TIFF ในขั้นตอนเดียวกันได้หรือไม่?** ได้ – หลังจากปรับค่า gamma คุณสามารถบันทึกภาพโดยตรงเป็น TIFF ด้วยการใช้ `TiffOptions`  
- **ฉันต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมจริง  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Aspose.PSD รองรับ Java 8 ขึ้นไป  

## java image processing คืออะไร?

Java image processing หมายถึงการจัดการ, วิเคราะห์, และแปลงข้อมูลภาพโดยใช้ไลบรารีของ Java งานที่ทำได้รวมถึงการปรับขนาด, การกรอง, การแก้ไขสี, และการแปลงฟอร์แมต – ทั้งหมดนี้สามารถทำอัตโนมัติในแอปพลิเคชันเดสก์ท็อปหรือเว็บได้

## ทำไมต้องใช้ Aspose.PSD สำหรับการแก้ไขค่า gamma?

Aspose.PSD ให้ API ระดับสูงที่ซ่อนความซับซ้อนของฟอร์แมต PSD ไว้ ทำให้คุณโฟกัสที่การปรับภาพจริง ๆ มันจัดการแคช, โปรไฟล์สี, และมีเมธอด `adjustGamma` ที่เรียบง่าย ทำให้เหมาะอย่างยิ่งสำหรับ **image gamma correction** และ **convert psd to tiff** workflow  

## ข้อกำหนดเบื้องต้น

1. **Java Development Environment** – ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา Java ติดตั้งอยู่บนระบบของคุณ  
2. **Aspose.PSD Library** – ดาวน์โหลดและรวมไลบรารี Aspose.PSD เข้ากับโครงการ Java ของคุณ คุณสามารถค้นหาแหล่งข้อมูลที่จำเป็นได้ใน [documentation](https://reference.aspose.com/psd/java/)  
3. **Sample Image** – เตรียมภาพ PSD ตัวอย่างที่คุณจะใช้ในการปรับค่า gamma  

## นำเข้าแพ็กเกจ

เพื่อเริ่มกระบวนการ ให้นำเข้าแพ็กเกจที่จำเป็นในโครงการ Java ของคุณ ซึ่งจะทำให้คุณสามารถใช้ฟังก์ชันของ Aspose.PSD ได้อย่างราบรื่น  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: โหลดภาพ

เริ่มต้นด้วยการโหลดภาพ PSD ตัวอย่างเข้าสู่อินสแตนซ์ของคลาส `RasterImage` ซึ่งเป็นพื้นฐานสำหรับการปรับค่า gamma ต่อไป  

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

## ขั้นตอนที่ 2: ปรับค่า Gamma

จากนั้นปรับค่า gamma ของภาพที่โหลดแล้วโดยใช้เมธอด `adjustGamma` ปรับค่าตามความต้องการของคุณ  

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## ขั้นตอนที่ 3: สร้าง TiffOptions

สร้างอินสแตนซ์ของ `TiffOptions` สำหรับภาพผลลัพธ์ ตั้งค่าต่าง ๆ เช่น bits per sample และ photometric options เพื่อให้ได้ผลลัพธ์ตามที่ต้องการ  

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## ขั้นตอนที่ 4: บันทึกภาพผลลัพธ์

บันทึกภาพที่ปรับแต่งแล้วเป็นฟอร์แมต TIFF โดยใช้ `TiffOptions` ที่กำหนดไว้ก่อนหน้า  

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## ปัญหาทั่วไปและวิธีแก้ไข

| ปัญหา | สาเหตุ | วิธีแก้ไข |
|-------|--------|-----------|
| **ภาพดูซีด** | ค่ากามม่าสูงเกินไป (เช่น > 2.5) | ลดค่ากามม่าให้อยู่ระหว่าง 1.8 ถึง 2.2 |
| **`rasterImage.isCached()` คืนค่า false** | ภาพยังไม่ได้โหลดเข้าสู่หน่วยความจำ | เรียก `rasterImage.cacheData()` ก่อนปรับค่า gamma |
| **ขนาดไฟล์ TIFF ใหญ่** | บิตต่อตัวอย่างตั้งเป็น 16‑bit | ใช้ตัวอย่าง 8‑bit (`{8,8,8}`) ตามที่แสดงในตัวอย่าง |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถใช้ค่ากามม่าที่แตกต่างกันสำหรับแต่ละช่องสีได้หรือไม่?**  
**ตอบ:** ใช่ – เมธอด `adjustGamma` ยอมรับค่าจำนวนจริงแยกสำหรับช่องสีแดง เขียว และน้ำเงิน  

**ถาม: สามารถทำการปรับภาพหลายขั้นตอนต่อเนื่องก่อนบันทึกได้หรือไม่?**  
**ตอบ:** แน่นอน คุณสามารถทำการปรับขนาด การครอป หรือการแก้ไขสีต่อเนื่องกันบนอินสแตนซ์ `RasterImage` เดียว  

**ถาม: Aspose.PSD รองรับไฟล์ PSD แบบหลายหน้าไหม?**  
**ตอบ:** ใช่ แต่ละเลเยอร์สามารถเข้าถึงและประมวลผลได้แยกกัน  

**ถาม: ฉันสามารถส่งออกเป็นฟอร์แมตอะไรได้บ้างนอกจาก TIFF?**  
**ตอบ:** Aspose.PSD รองรับ PNG, JPEG, BMP และฟอร์แมตอื่น ๆ อีกหลายรูปแบบผ่านคลาส options ที่เกี่ยวข้อง  

## สรุป

ขอแสดงความยินดี! คุณได้ทำ **java image processing** สำเร็จโดยการปรับค่า gamma ของไฟล์ PSD และส่งออกเป็นภาพ TIFF ด้วย Aspose.PSD for Java Workflow นี้ให้การควบคุมความสว่างและคอนทราสต์อย่างละเอียด เหมาะสำหรับ pipeline กราฟิกอัตโนมัติ, บริการเว็บ หรือยูทิลิตี้เดสก์ท็อป  

**อัปเดตล่าสุด:** 2025-12-21  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
