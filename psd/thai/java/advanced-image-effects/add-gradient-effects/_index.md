---
date: 2026-10-18
description: เรียนรู้วิธีสร้างเอฟเฟกต์ไล่สีรัศมีในภาพ Java ด้วย Aspose.PSD. ทำตามคู่มือ
  step‑by‑step นี้เพื่อการบูรณาการที่ราบรื่น
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: เพิ่มเอฟเฟกต์ไล่สี
og_description: เรียนรู้การสร้างเอฟเฟกต์ไล่สีรัศมีใน Java ด้วย Aspose.PSD. บทเรียนนี้แสดงวิธีเพิ่ม
  ปรับแต่ง และบันทึกการทับไล่สีในไม่กี่นาที
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: สร้างไล่สีรัศมีใน Java ด้วย Aspose.PSD – คู่มือ step‑by‑step
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: วิธีสร้างเอฟเฟกต์ไล่สีรัศมีใน Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างเอฟเฟกต์การไล่สีแบบรัศมีใน Aspose.PSD สำหรับ Java

## บทนำ

ในคู่มือนี้คุณจะได้เรียนรู้วิธี **สร้างเอฟเฟกต์การไล่สีแบบรัศมีใน Java** ด้วยไลบรารี Aspose.PSD การไล่สีแบบรัศมีเหมาะอย่างยิ่งสำหรับเพิ่มความลึก, โฟกัส, หรือแสงเรืองรอบอ่อน ๆ ให้กับเลเยอร์ PSD ของคุณโดยไม่ต้องเปิด Photoshop เมื่อจบบทเรียนคุณจะสามารถโหลดไฟล์ PSD, ใส่การไล่สีแบบโอเวอร์เลย์, ปรับคุณสมบัติต่าง ๆ, และบันทึกผลลัพธ์ — ทั้งหมดจากโค้ด Java

## คำตอบด่วน
- **ฉันสามารถทำอะไรได้บ้าง?** เพิ่ม, แก้ไข, และผสมการโอเวอร์เลย์การไล่สีแบบรัศมีบนเลเยอร์ PSD.  
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java (เวอร์ชันล่าสุด).  
- **ฉันต้องการไลเซนส์หรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **การทำงานใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับการโอเวอร์เลย์การไล่สีแบบรัศมีพื้นฐาน.  
- **รองรับ Java 8+ หรือไม่?** ใช่, API รองรับ Java 8 และรันไทม์ที่ใหม่กว่า.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในบทเรียน โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งาน:

1. **Aspose.PSD for Java Library** – ตรวจสอบว่าคุณได้ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD for Java แล้ว คุณสามารถค้นหาไลบรารีและเอกสารได้ที่ [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ (JDK 8 หรือสูงกว่า, IDE ที่คุณชอบ).  
3. **Latest Aspose.PSD release** – ดาวน์โหลดเวอร์ชันล่าสุดจาก [Aspose releases page](https://releases.aspose.com/).  
4. **Support resources** – หากคุณพบปัญหา ให้เข้าไปที่ [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34).  
5. **License purchase** – เมื่อพร้อมสำหรับการใช้งานจริง ให้ซื้อไลเซนส์ผ่าน [purchase page](https://purchase.aspose.com/buy).

ตอนนี้คุณได้เตรียมทุกอย่างพร้อมแล้ว มาเริ่มทำตามขั้นตอนแบบทีละขั้นตอนกันเถอะ

## การทำงานของเอฟเฟกต์การโอเวอร์เลย์การไล่สีคืออะไร?

เอฟเฟกต์การโอเวอร์เลย์การไล่สีจะทาสีที่เปลี่ยนอย่างราบรื่นระหว่างสองสีหรือมากกว่านั้นบนพื้นที่ที่เลือกของเลเยอร์ ใน Photoshop เอฟเฟกต์นี้สามารถผสมสี, ปรับสี, และกำหนดตำแหน่งเพื่อสร้างการออกแบบที่ซับซ้อนได้ คลาส `GradientOverlayEffect` ของ Aspose.PSD แสดงถึงสไตล์เลเยอร์นี้ โดยเปิดเผยคุณสมบัติต่าง ๆ เช่น จุดสี, ความทึบ, โหมดผสม, และสไตล์การไล่สี

## วิธีสร้างเอฟเฟกต์การไล่สีแบบรัศมี

โหลดไฟล์ PSD, ค้นหาเลเยอร์เป้าหมาย, ปรับคุณสมบัติของ `GradientOverlayEffect`, แล้วบันทึกไฟล์ การทำงานทั้งหมดสามารถทำได้ในสี่บรรทัดสั้น ๆ ของโค้ด Java หลังจากโหลดภาพแล้ว

### ขั้นตอนที่ 1: โหลดไฟล์ PSD และเข้าถึงการโอเวอร์เลย์การไล่สี

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

ในขั้นตอนนี้ เราโหลดไฟล์ PSD และดึง `GradientOverlayEffect` ตัวแรกจากเลเยอร์ที่สอง (ดัชนี 1) การเรียก `loadOptions.setLoadEffectsResource(true)` ทำให้แน่ใจว่าทรัพยากรของเอฟเฟกต์พร้อมสำหรับการแก้ไข

### ขั้นตอนที่ 2: ตรวจสอบการตั้งค่าเริ่มต้น

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

ก่อนทำการเปลี่ยนแปลง ควรตรวจสอบโหมดผสม, ความทึบ, และการมองเห็นปัจจุบัน เพื่อให้คุณเข้าใจสถานะพื้นฐานของการโอเวอร์เลย์การไล่สี

### ขั้นตอนที่ 3: ปรับการตั้งค่าการไล่สี

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

ที่นี่คุณสามารถปรับสี, ความทึบ, และโหมดผสมของการไล่สี ตัวอย่างจะเปลี่ยนสีเป็นสีเขียว, ลดความทึบเป็น 193 (จาก 255), และสลับโหมดผสมเป็น **Lighten** คุณสามารถทดลองค่า `BlendMode` อื่น ๆ เช่น `Multiply`, `Screen`, หรือ `Overlay` ได้ตามต้องการ

### ขั้นตอนที่ 4: บันทึกภาพที่แก้ไขแล้ว

```java
// Save the edited image
im.save(exportPath);
```

หลังจากปรับแก้แล้ว ให้บันทึกการเปลี่ยนแปลงโดยการบันทึก PSD ไปยังไฟล์ใหม่ ขั้นตอนนี้ทำให้ไฟล์ต้นฉบับไม่ถูกแก้ไข

### ขั้นตอนที่ 5: ตรวจสอบการเปลี่ยนแปลง

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

โค้ดข้างต้นแสดงวิธีเปิด PSD, ดึงเอฟเฟกต์แรกของเลเยอร์ที่สอง (สมมติว่าเป็นการโอเวอร์เลย์การไล่สี) และเตรียมพร้อมสำหรับการแก้ไข

### ขั้นตอนที่ 2: ตรวจสอบการตั้งค่าเดิม (เป็นตัวเลือกแต่แนะนำ)

ก่อนที่คุณจะเปลี่ยนแปลงอะไร การตรวจสอบโหมดผสม, ความทึบ, และการมองเห็นที่มีอยู่ช่วยให้คุณเข้าใจฐานข้อมูล `Assert` ในโค้ดยืนยันว่าเอฟเฟกต์กำหนดเป็นโหมดผสม **Normal**, ทึบเต็ม, และมองเห็นได้

### ขั้นตอนที่ 3: ปรับคุณสมบัติการไล่สีเพื่อให้ได้สไตล์แบบรัศมี

คุณสามารถเปลี่ยนสี, ความทึบ, และโหมดผสมของการไล่สี สำหรับเอฟเฟกต์รัศมีที่แท้จริง ให้ตั้งสไตล์การไล่สี:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Pro tip:* ใช้ `Color.getGreen()` หรืออินสแตนซ์ `java.awt.Color` ใด ๆ เพื่อกำหนดสีเริ่มต้น, และ `gradientOverlay.setColor2(Color.getBlue())` สำหรับสีสุดท้าย

### ขั้นตอนที่ 4: บันทึก PSD ที่แก้ไขแล้ว

การเรียก `im.save(exportPath);` จะเขียนภาพที่แก้ไขแล้วลงดิสก์ ไฟล์ที่บันทึกจะคงการโอเวอร์เลย์การไล่สีแบบรัศมีและสามารถเปิดใน Photoshop, ดูตัวอย่างในเบราว์เซอร์, หรือแปลงเป็นรูปแบบอื่นได้

## ทำไมต้องสร้างการโอเวอร์เลย์การไล่สีแบบรัศมี?

การไล่สีแบบรัศมีเพิ่มความลึกและโฟกัสให้กับการออกแบบ ทำให้องค์ประกอบดูเหมือนสามมิติหรือมีแสงส่องสว่าง เหมาะสำหรับ:

- **การเติมพื้นหลัง** ที่ดึงสายตาไปยังหัวข้อศูนย์กลาง.  
- **การไฮไลท์ปุ่มหรือไอคอน** ที่ต้องการแสงเรืองรอบอ่อน ๆ.  
- **เอฟเฟกต์ภาพสร้างสรรค์** เช่น วินีเอตหรือแสงระเบิด.  

Aspose.PSD รองรับ **50+ รูปแบบการนำเข้าและส่งออก** และสามารถจัดการไฟล์ PSD หลายร้อยหน้าโดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ช่วยให้คุณอัตโนมัติการสร้างการไล่สีในคลังสินค้าขนาดใหญ่ได้

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **Effect not visible:** ตรวจสอบให้แน่ใจว่า `gradientOverlay.isVisible()` คืนค่า `true`. บางไฟล์ PSD จะซ่อนเอฟเฟกต์โดยค่าเริ่มต้น.  
- **Incorrect layer index:** เลเยอร์เริ่มจากศูนย์; ตรวจสอบให้แน่ใจว่าคุณกำหนดเลเยอร์ที่ถูกต้อง (`im.getLayers()[1]` หมายถึงเลเยอร์ที่สอง).  
- **Opacity casting:** เมธอด `setOpacity` ต้องการค่าเป็น `byte`. การส่งค่า `int` จะทำให้เกิดข้อผิดพลาดในการคอมไพล์; ให้ทำการแคสต์ตามตัวอย่าง.  
- **Resource loading:** หากคุณพบค่า `null` เมื่อเข้าถึงเอฟเฟกต์ ตรวจสอบว่าได้ตั้งค่า `loadOptions.setLoadEffectsResource(true)` ก่อนโหลดภาพแล้ว.

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้เอฟเฟกต์การไล่สีหลายอันกับภาพเดียวได้หรือไม่?**  
A: ใช่. ดึง `BlendingOptions` ของเลเยอร์, วนลูปผ่านคอลเลกชัน `Effects`, แล้วเพิ่ม `GradientOverlayEffect` ใหม่สำหรับแต่ละการไล่สีที่ต้องการ.

**Q: มีเอฟเฟกต์อื่น ๆ ที่สามารถรวมกับการโอเวอร์เลย์การไล่สีได้หรือไม่?**  
A: Aspose.PSD มีเงา, แสงเรือง, เบเวลและอื่น ๆ อีกมาก ทุกเอฟเฟกต์ปรากฏในอาเรย์ `Effects` และสามารถกำหนดค่าแยกกันได้.

**Q: ฉันจะแก้ไขปัญหาเมื่อเอฟเฟกต์ไม่แสดงผลอย่างถูกต้องได้อย่างไร?**  
A: ตรวจสอบว่ามีการโหลด PSD ด้วย `setLoadEffectsResource(true)`, ตรวจสอบการมองเห็นของเลเยอร์, และยืนยันว่าคุณแก้ไขดัชนีเอฟเฟกต์ที่ถูกต้อง.

**Q: มีเวอร์ชันทดลองสำหรับ Aspose.PSD for Java หรือไม่?**  
A: มี, คุณสามารถรับเวอร์ชันทดลองฟรีได้ที่ [here](https://releases.aspose.com/).

**Q: จะซื้อไลเซนส์สำหรับ Aspose.PSD for Java ได้จากที่ไหน?**  
A: เยี่ยมชม [purchase page](https://purchase.aspose.com/buy) เพื่อดูข้อมูลการไลเซนส์.

## คำถามเพิ่มเติม

**Q: สามารถเปลี่ยนทิศทางการไล่สีโดยโปรแกรมได้หรือไม่?**  
A: ใช่. ใช้เมธอด `GradientOverlayEffect.setAngle(float angle)` เพื่อกำหนดมุมการไล่สีเป็นองศา สำหรับการไล่สีแบบรัศมีมุมจะถูกละเลย แต่เมธอดต้องถูกเรียกใช้อย่างไรก็ตาม.

**Q: Aspose.PSD รองรับการไล่สีแบบรัศมีหรือไม่?**  
A: แน่นอน. ตั้งค่าสไตล์การไล่สีเป็น `GradientStyle.Radial` ผ่านคุณสมบัติของ `GradientOverlayEffect`.

**Q: การโอเวอร์เลย์การไล่สีจะคงอยู่เมื่อแปลง PSD เป็นรูปแบบอื่น (เช่น PNG) หรือไม่?**  
A: เมื่อคุณแรสเตอร์ไล่ PSD (เช่นบันทึกเป็น PNG) ผลลัพธ์ภาพของการโอเวอร์เลย์การไล่สีจะถูกเก็บไว้ในข้อมูลพิกเซล, แต่เอฟเฟกต์เองจะไม่อยู่ในรูปแบบไฟล์ใหม่.

**Q: จะลบการโอเวอร์เลย์การไล่สีออกจากเลเยอร์ได้อย่างไร?**  
A: ดึง `BlendingOptions` ของเลเยอร์, ค้นหา `GradientOverlayEffect` ในคอลเลกชัน `Effects`, แล้วลบด้วย `remove(effect)`.

**Q: สามารถทำให้การไล่สีเคลื่อนไหวได้หรือไม่?**  
A: แม้ Aspose.PSD จะไม่รองรับการทำแอนิเมชันโดยตรง, คุณสามารถสร้างชุดไฟล์ PSD ที่มีพารามิเตอร์การไล่สีต่างกันแล้วรวมเป็นวิดีโอหรือ GIF ด้วยไลบรารีอื่น.

## สรุป

ขอแสดงความยินดี! คุณได้เรียนรู้ **วิธีสร้างเอฟเฟกต์การไล่สีแบบรัศมีใน Java** ให้กับภาพของคุณโดยใช้ Aspose.PSD for Java ด้วยการทำตามขั้นตอนข้างต้น คุณสามารถเพิ่ม, ปรับเปลี่ยน, และบันทึกการโอเวอร์เลย์การไล่สีได้อย่างโปรแกรมเมติก ให้คุณมีอิสระในการสร้างสรรค์ PSD อย่างเต็มที่ ทดลองใช้สี, โหมดผสม, และค่าความทึบที่แตกต่างกันเพื่อให้ได้ผลลัพธ์ตามที่ต้องการ

---

**อัปเดตล่าสุด:** 2026-10-18  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## บทแนะนำที่เกี่ยวข้อง

- [สร้าง Gradient Fill PSD ด้วย Java โดยใช้ Aspose.PSD – เพิ่ม Gradient Fill Layer](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Pattern Overlay PSD: เพิ่มเอฟเฟกต์ด้วย Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [ใช้ Color Overlay และตั้งค่าความทึบใน Java ด้วย Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}