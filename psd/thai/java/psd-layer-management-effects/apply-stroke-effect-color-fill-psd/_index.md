---
date: 2026-04-03
description: เรียนรู้วิธีบันทึกไฟล์ PSD เป็น PNG พร้อมเอฟเฟกต์เส้นขอบและการเติมสีโดยใช้
  Aspose.PSD สำหรับ Java คู่มือขั้นตอนต่อขั้นตอนนี้แสดงวิธีส่งออก PSD เป็น PNG อย่างรวดเร็ว.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: บันทึก PSD เป็น PNG พร้อมเอฟเฟกต์ Stroke – Java
second_title: Aspose.PSD Java API
title: บันทึก PSD เป็น PNG พร้อมเอฟเฟกต์เส้นขอบ – Java
url: /th/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก PSD เป็น PNG พร้อมเอฟเฟกต์ Stroke และการเติมสี – Java

## บทนำ

ในคู่มือนี้ คุณจะได้เรียนรู้วิธี **บันทึก PSD เป็น PNG** พร้อมใช้เอฟเฟกต์เส้นขอบ (stroke) พร้อมการเติมสีโดยใช้ Aspose.PSD for Java ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น คำแนะนำแบบขั้นตอนนี้จะทำให้คุณทำงานได้ง่าย เราจะครอบคลุมตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการส่งออกภาพขั้นสุดท้าย เพื่อให้คุณสามารถ **ส่งออก PSD เป็น PNG** ในโปรเจกต์ของคุณได้อย่างรวดเร็ว

## คำตอบสั้น

- **บทเรียนนี้ทำอะไรได้บ้าง?** แสดงวิธีบันทึกไฟล์ PSD เป็น PNG หลังจากใส่เอฟเฟกต์เส้นขอบที่ปรับแต่งได้  
- **ใช้ไลบรารีอะไร?** Aspose.PSD for Java  
- **ต้องมีไลเซนส์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; ต้องมีไลเซนส์สำหรับการใช้งานจริง  
- **เปลี่ยนสีเส้นขอบได้หรือไม่?** ได้ – สามารถตั้งค่าสีใดก็ได้ผ่าน `ColorFillSettings`  
- **สามารถประมวลผลเป็นชุดได้หรือไม่?** แน่นอน – เพียงห่อโค้ดในลูปเพื่อประมวลผลหลายไฟล์ PSD

## “บันทึก PSD เป็น PNG” คืออะไร?

การบันทึก PSD เป็น PNG หมายถึงการแปลงไฟล์ชั้นของ Photoshop ให้เป็นรูปแบบภาพแบนที่เป็นมิตรกับเว็บโดยคงความคมชัดของภาพไว้ การทำเช่นนี้มีประโยชน์เมื่อคุณต้องการแสดงเนื้อหา PSD บนเว็บไซต์, แอปมือถือ หรือแพลตฟอร์มใด ๆ ที่ไม่รองรับไฟล์ PSD โดยตรง

## ทำไมต้องใส่เอฟเฟกต์เส้นขอบพร้อมการเติมสี?

เส้นขอบ (stroke) เพิ่มขอบชัดเจนรอบเนื้อหาในเลเยอร์ ทำให้กราฟิกโดดเด่นขึ้นเมื่ออยู่บนพื้นหลังที่ซับซ้อน การผสานกับสีเติมที่กำหนดเองช่วยให้คุณสร้างแบรนด์ภาพ, เน้นส่วน UI, หรือทำให้รูปภาพตัวอย่างดูน่าสนใจโดยไม่ต้องเปิด Photoshop

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK) 8+** – ตรวจสอบให้ `java` อยู่ใน PATH  
2. **Aspose.PSD for Java** – ดาวน์โหลดจาก [website](https://releases.aspose.com/psd/java/)  
3. **IDE** – IntelliJ IDEA, Eclipse หรือเครื่องมือแก้ไขอื่นที่คุณชอบ  
4. **ตัวอย่าง PSD** – ไฟล์ที่มีเอฟเฟกต์เส้นขอบอยู่แล้ว (หรือเพิ่มใน Photoshop)  
5. **ความรู้พื้นฐาน Java** – คุณจะเขียนโค้ดไม่กี่บรรทัด, ไม่ต้องเป็นระดับสูง  

เมื่อคุณเตรียมสิ่งเหล่านี้เรียบร้อยแล้ว เราก็เริ่มเขียนโค้ดได้

## นำเข้าแพ็กเกจ

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

การนำเข้าดังกล่าวจะทำให้คุณเข้าถึงคลาสทั้งหมดที่จำเป็นสำหรับการโหลด PSD, แก้ไขเส้นขอบ, และบันทึกผลลัพธ์เป็น PSD และ PNG

## วิธีบันทึก PSD เป็น PNG พร้อมเอฟเฟกต์ Stroke

### ขั้นตอนที่ 1: โหลดไฟล์ PSD

แรกสุด ให้ระบุโฟลเดอร์ที่เก็บไฟล์ PSD ของคุณ

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธที่แท้จริงบนเครื่องของคุณ  

ต่อไปโหลดไฟล์โดยคงรักษาเอฟเฟกต์ที่มีอยู่ทั้งหมดไว้

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### ขั้นตอนที่ 2: ตั้งค่าสีเส้นขอบ (และปรับความกว้างตามต้องการ)

ลูปด้านล่างจะวนผ่านแต่ละเลเยอร์, ดึง `StrokeEffect` ตัวแรก, แล้วเปลี่ยนสีเติมของมัน คุณยังสามารถปรับ `setWidth` หรือ `setPosition` ของอ็อบเจกต์ `StrokeEffect` เพื่อ **ปรับความกว้างของเส้นขอบ** ได้ตามต้องการ

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **เคล็ดลับ:** `Color.getDeepPink()` เป็นเพียงตัวอย่าง ใช้ `new Color(r, g, b)` เพื่อกำหนดค่า RGB ที่ต้องการ

### ขั้นตอนที่ 3: บันทึก PSD ที่แก้ไขแล้ว (ไม่บังคับ)

หากต้องการเก็บไฟล์ PSD ที่มีเส้นขอบอัปเดตไว้ ให้บันทึกดังนี้

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### ขั้นตอนที่ 4: ส่งออกเป็น PNG (ขั้นตอนหลัก “บันทึก PSD เป็น PNG”)

สุดท้าย แปลง PSD ที่แก้ไขแล้วเป็นไฟล์ PNG พร้อมใช้งานบนเว็บ

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

ไฟล์ PNG จะคงเส้นขอบสีชมพูเข้มที่คุณตั้งไว้ และตัวเลือก `TruecolorWithAlpha` จะทำให้ความโปร่งใสถูกเก็บรักษาไว้

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | เลเยอร์ไม่มีเอฟเฟกต์หรือเอฟเฟกต์แรกไม่ใช่ `StrokeEffect` | ตรวจสอบว่าเลเยอร์มีเส้นขอบจริงหรือวนผ่าน `getEffects()` เพื่อหาเอฟเฟกต์ประเภทที่ต้องการ |
| **สีไม่เปลี่ยน** | คุณอาจแก้ไขสำเนาของการตั้งค่าแทนที่จะเป็นของต้นฉบับ | ให้ทำการแคสต์เป็น `ColorFillSettings` โดยตรงจาก `effect.getFillSettings()` |
| **PNG แสดงเป็นสีขาวเปล่า** | PSD ถูกโหลดโดยไม่ได้ทำการเรสเตอร์ไลซ์เลเยอร์ | เรียก `im.save(..., new PngOptions())` หลังจากทำการแก้ไขทั้งหมด; อย่าบันทึก `im` ดั้งเดิมก่อนทำการเปลี่ยนแปลง |

## คำถามที่พบบ่อย

**ถาม: สามารถใส่หลายเอฟเฟกต์ให้กับเลเยอร์เดียวด้วย Aspose.PSD for Java ได้หรือไม่?**  
ตอบ: ได้, คุณสามารถเข้าถึงตัวเลือกการผสมของเลเยอร์และเพิ่มเอฟเฟกต์ได้หลายแบบ รวมถึงเงา, แสงเรืองแสง, และเส้นขอบ  

**ถาม: สามารถทำอัตโนมัติสำหรับชุดไฟล์ PSD ได้หรือไม่?**  
ตอบ: แน่นอน. ห่อส่วนการโหลด, การใส่เอฟเฟกต์, และการบันทึกไว้ในลูป `for‑each` ที่วนผ่านไฟล์ในโฟลเดอร์  

**ถาม: จะย้อนกลับการเปลี่ยนแปลงในไฟล์ PSD ได้อย่างไร?**  
ตอบ: โหลดไฟล์ต้นฉบับใหม่ก่อนบันทึกการแก้ไข; Aspose.PSD ไม่มีระบบ undo  

**ถาม: สามารถปรับความกว้างและตำแหน่งของเส้นขอบได้หรือไม่?**  
ตอบ: ได้. ใช้ `effect.setWidth(float)` และ `effect.setPosition(StrokeEffect.Position)` เพื่อควบคุมความหนาและตำแหน่ง (ภายใน, ภายนอก, หรือกึ่งกลาง)  

**ถาม: ไลบรารี Aspose.PSD for Java ใช้ได้ฟรีหรือไม่?**  
ตอบ: มีรุ่นทดลองฟรีสำหรับการประเมินผล. การใช้งานเต็มรูปแบบต้องซื้อไลเซนส์. ดูรายละเอียดที่ [buy options](https://purchase.aspose.com/buy)

---

**อัปเดตล่าสุด:** 2026-04-03  
**ทดสอบกับ:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}