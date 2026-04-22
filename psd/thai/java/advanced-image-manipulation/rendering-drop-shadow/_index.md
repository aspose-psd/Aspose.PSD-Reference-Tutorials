---
date: 2026-02-07
description: เรียนรู้วิธีบันทึกไฟล์ PSD เป็น PNG, ส่งออก PNG พร้อมแอลฟา, และเพิ่มเลเยอร์เงาตกโดยใช้
  Aspose.PSD สำหรับ Java – คู่มือเต็มขั้นตอนแบบละเอียด.
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: บันทึก PSD เป็น PNG และใช้การเรนเดอร์เงาตกใน Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก PSD เป็น PNG และใช้ Rendering Drop Shadow ใน Aspose.PSD สำหรับ Java

## บทนำ

หากคุณทำงานกับไฟล์ Photoshop ใน Java, **การบันทึก PSD เป็น PNG** เป็นหนึ่งในงานที่พบบ่อยที่สุดที่คุณจะเจอ ด้วย Aspose.PSD คุณไม่เพียงแต่ **แปลง PSD เป็น PNG** แต่ยังสามารถปรับปรุงภาพโดย **เพิ่มเลเยอร์เงาตก** ได้อีกด้วย ในบทเรียนนี้เราจะพาคุณผ่านกระบวนการทั้งหมด—การโหลด PSD, การใช้ Rendering Drop Shadow, และสุดท้าย **การบันทึก PSD เป็นไฟล์ PNG**—เพื่อให้คุณสามารถผสานการทำงานนี้เข้าไปในโปรเจกต์ของคุณได้อย่างมั่นใจ

## คำตอบสั้น

- **ไลบรารีที่จัดการการแปลง PSD เป็น PNG คืออะไร?** Aspose.PSD for Java.  
- **การทำ Drop‑Shadow ใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับตัวอย่างพื้นฐาน.  
- **ต้องมีลิขสิทธิ์เพื่อรันโค้ดหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการประเมิน; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง.  
- **สามารถใช้เงาตกกับหลายเลเยอร์ได้หรือไม่?** ได้—แค่วนลูปผ่านเลเยอร์ที่ต้องการ.  
- **ต้องใช้ Java เวอร์ชันใด?** Java 8 หรือสูงกว่า.

## “บันทึก PSD เป็น PNG” คืออะไรและทำไมจึงสำคัญ?

การบันทึก PSD เป็น PNG สร้างภาพที่รองรับอย่างกว้างขวางและไม่มีการสูญเสียคุณภาพซึ่งยังคงรักษาความโปร่งใสไว้ได้ สิ่งนี้สำคัญเมื่อคุณต้องการแสดงสินทรัพย์ Photoshop บนเว็บ, ในแอปมือถือ, หรือเป็นส่วนหนึ่งของสายงานการประมวลผลภาพที่ใหญ่ขึ้น การเพิ่มเงาตกในเวลาเดียวกันทำให้คุณสร้างเอฟเฟกต์ที่ดูเป็นมืออาชีพโดยไม่ต้องเปิด Photoshop

## ทำไมต้องใช้ Aspose.PSD สำหรับกระบวนการนี้?

* **ควบคุมเต็มจากโค้ด** – ไม่ต้องเปิด Photoshop หรือพึ่งพาเครื่องมือภายนอก.  
* **รักษาเอฟเฟกต์ของเลเยอร์** – เงาตก, แสงเรืองแสง, และเอฟเฟกต์อื่น ๆ จะถูกเรนเดอร์เหมือนเดิมตามที่ปรากฏในไฟล์ต้นฉบับ.  
* **ส่งออก PNG พร้อม Alpha** – ผลลัพธ์ PNG จะคงพื้นหลังโปร่งใส ทำให้พร้อมใช้บนเว็บหรือ UI.  
* **ข้ามแพลตฟอร์ม** – ทำงานบน OS ใด ๆ ที่รองรับ Java 8+.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึก, โปรดตรวจสอบว่าคุณมี:

- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า.  
- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [หน้าดาวน์โหลด Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **ไฟล์ PSD** – ไฟล์ควรมีอย่างน้อยหนึ่งเลเยอร์ที่คุณต้องการเพิ่มเงาตก (เช่น *Shadow.psd*).  

## นำเข้าแพ็กเกจ

ก่อนอื่นให้นำเข้าคลาสที่เราต้องการ นี่จะทำให้เราสามารถโหลดภาพ, จัดการเอฟเฟกต์ของเลเยอร์, และตั้งค่าการส่งออก PNG ได้

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสาร  
บอกโปรแกรมว่าที่ใดที่ไฟล์ PSD ต้นฉบับของคุณอยู่

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: ตั้งค่าเส้นทางไฟล์ PSD และ PNG  
ระบุทั้งไฟล์ PSD เข้าและไฟล์ PNG ออกที่จะบรรจุ Rendering Drop Shadow

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### ขั้นตอนที่ 3: โหลดไฟล์ PSD พร้อมเอฟเฟกต์  
เปิดการโหลดทรัพยากรเอฟเฟกต์เพื่อให้เราสามารถจัดการกับเอฟเฟกต์เงาตกได้

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### ขั้นตอนที่ 4: เข้าถึงเอฟเฟกต์ Drop Shadow  
ดึงเอฟเฟกต์เงาตกแรกจากเลเยอร์ที่สอง (ดัชนี 1). ที่นี่เราจะตรวจสอบหรือแก้ไขพารามิเตอร์

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### ขั้นตอนที่ 5: ตรวจสอบคุณสมบัติของเอฟเฟกต์เงา  
ตรวจให้แน่ใจว่าคุณสมบัติของเอฟเฟกต์ตรงกับที่คุณคาดหวังก่อนบันทึก คุณยังสามารถปรับค่าเหล่านี้เพื่อให้ได้ลุคที่แตกต่างได้อีกด้วย

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **เคล็ดลับ:** ปรับ `setSpread()` หรือ `setNoise()` เพื่อสร้างเงาที่นุ่มหรือมีลักษณะเท็กซ์เจอร์มากขึ้น

### ขั้นตอนที่ 6: บันทึกเป็น PNG – ขั้นตอน “บันทึก PSD เป็น PNG”  
ส่งออกภาพที่แก้ไขเป็น PNG, รักษาชาแนล Alpha ไว้เพื่อให้เงาผสมอย่างถูกต้อง

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

ในตอนนี้คุณได้ **แปลง PSD เป็น PNG** อย่างสำเร็จ, **ส่งออก PNG พร้อม Alpha**, และ **ใช้ Rendering Drop Shadow** ในกระบวนการเดียวกันแล้ว

## ส่งออก PNG พร้อมความโปร่งใส Alpha

เมื่อคุณต้องการให้ผลลัพธ์ PNG คงพื้นหลังโปร่งใส—โดยเฉพาะสำหรับการโอเวอร์เลย์ UI หรือกราฟิกเว็บ—ให้ใช้ `PngColorType.TruecolorWithAlpha` ตามที่แสดงในขั้นตอนการบันทึกด้านบน สิ่งนี้รับประกันว่าเงาตกจะอยู่บนแคนวาสโปร่งใสแทนพื้นหลังสีทึบ

## เพิ่มเลเยอร์ Drop Shadow ด้วย Java

หาก PSD ของคุณมีหลายเลเยอร์ที่ต้องการเงา เพียงทำซ้ำ **ขั้นตอน 4** และ **ขั้นตอน 5** ภายในลูปที่วนผ่าน `im.getLayers()` แต่ละรอบสามารถสร้างหรือแก้ไขอินสแตนซ์ `DropShadowEffect` ได้, ให้คุณควบคุมความทึบ, ระยะ, ขนาด, และมุมของเงาแต่ละเลเยอร์ได้อย่างละเอียด

## การแปลง Photoshop PNG ด้วย Java – กรณีใช้งานทั่วไป

* **สายงานสินทรัพย์เว็บ** – แปลง PSD ที่ออกแบบโดยนักออกแบบเป็น PNG พร้อมเงาที่สร้างไว้ล่วงหน้า.  
* **ทรัพยากรแอปมือถือ** – สร้างไอคอน PNG โปร่งใสแบบไดนามิก, หลีกเลี่ยงการส่งออกด้วยมือ.  
* **การประมวลผลเป็นชุด** – อัตโนมัติการแปลงหลายร้อยไฟล์ PSD ในงานฝั่งเซิร์ฟเวอร์.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|-------|-------------------|--------|
| **เงาไม่ปรากฏ** | `Opacity` ตั้งเป็น 0 หรือเลเยอร์ถูกซ่อน | ตรวจสอบว่า `shadowEffect.getOpacity()` > 0 และเลเยอร์มองเห็นได้. |
| **PNG ปรากฏเป็นสีเดียว (ไม่มีความโปร่งใส)** | ใช้ `PngColorType` ไม่ถูกต้อง | ใช้ `PngColorType.TruecolorWithAlpha` ตามที่แสดง. |
| **เกิดข้อยกเว้นขณะโหลด** | ไม่ได้โหลดเอฟเฟกต์ | ตรวจสอบว่าได้เรียก `loadOptions.setLoadEffectsResource(true)` แล้ว. |
| **ดัชนีเลเยอร์ไม่ถูกต้อง** | โครงสร้าง PSD แตกต่าง | ตรวจสอบ `im.getLayers()` แล้วเลือกดัชนีที่ถูกต้อง. |

## คำถามที่พบบ่อย

**ถาม: สามารถใช้เงาตกกับหลายเลเยอร์พร้อมกันได้หรือไม่?**  
ตอบ: ได้. วนลูปผ่าน `im.getLayers()` แล้วเพิ่มหรือแก้ไข `DropShadowEffect` สำหรับแต่ละเลเยอร์ที่ต้องการ.

**ถาม: พารามิเตอร์ ‘Spread’ ควบคุมอะไร?**  
ตอบ: `Spread` กำหนดว่าการเปลี่ยนจากความทึบเต็มไปเป็นโปร่งใสจะเกิดขึ้นอย่างกะทันหันแค่ไหน ค่าเพิ่มทำให้ขอบเงาแข็งขึ้น.

**ถาม: Aspose.PSD รองรับเวอร์ชัน Photoshop ทั้งหมดหรือไม่?**  
ตอบ: Aspose.PSD รองรับไฟล์ PSD ตั้งแต่ Photoshop 3.0 จนถึงเวอร์ชันล่าสุด, รองรับประเภทเลเยอร์และเอฟเฟกต์ส่วนใหญ่.

**ถาม: จะทดสอบโค้ดก่อนซื้อไลเซนส์ได้อย่างไร?**  
ตอบ: ดาวน์โหลดเวอร์ชันทดลองฟรีจาก [หน้าดาวน์โหลด Aspose.PSD](https://releases.aspose.com/psd/java/) แล้วรันตัวอย่างโดยไม่ต้องใส่คีย์ไลเซนส์.

**ถาม: หากเจอปัญหาจะขอความช่วยเหลือได้จากที่ไหน?**  
ตอบ: โพสต์คำถามของคุณบน [ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) ที่ชุมชนและวิศวกรของ Aspose พร้อมให้ความช่วยเหลือ.

## สรุป

คุณได้เรียนรู้วิธี **บันทึก PSD เป็น PNG**, **ส่งออก PNG พร้อม Alpha**, **แปลง Photoshop PNG**, และ **เพิ่มเลเยอร์ Drop Shadow** ด้วย Aspose.PSD for Java การผสานรวมนี้ทำให้คุณสามารถอัตโนมัติการเตรียมภาพคุณภาพสูงสำหรับเว็บ, มือถือ, หรือแอปเดสก์ท็อป—โดยไม่ต้องเปิด Photoshop

---

**อัปเดตล่าสุด:** 2026-02-07  
**ทดสอบกับ:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}