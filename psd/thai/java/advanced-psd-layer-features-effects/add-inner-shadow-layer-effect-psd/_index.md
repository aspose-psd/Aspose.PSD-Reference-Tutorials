---
date: 2026-02-14
description: เรียนรู้วิธีเพิ่มเงาภายในใน PSD ด้วย Aspose.PSD for Java และประยุกต์ใช้เอฟเฟกต์เลเยอร์
  PSD ผ่านโปรแกรมด้วยบทแนะนำแบบขั้นตอนต่อขั้นตอนนี้ รวมถึงเคล็ดลับและแนวทางปฏิบัติที่ดีที่สุด
linktitle: Add Inner Shadow PSD Layer Effect in Java
second_title: Aspose.PSD Java API
title: วิธีเพิ่มเอฟเฟกต์เงาภายในให้กับเลเยอร์ PSD ใน Java
url: /th/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มเอฟเฟกต์เงาภายใน (Inner Shadow) ของเลเยอร์ PSD ใน Java

## บทนำ
หากคุณต้องการ **เพิ่มเงาภายใน PSD** อย่างอัตโนมัติ คุณมาถูกที่แล้ว ในคู่มือนี้ เราจะสาธิต **วิธีเพิ่มเงาภายใน** ให้กับเอกสาร Photoshop ใด ๆ ด้วย Aspose.PSD for Java ไม่ว่าคุณจะกำลังสร้างเครื่องมือประมวลผลแบบชุด, pipeline การออกแบบอัตโนมัติ, หรือแค่ทดลองกับเอฟเฟกต์ภาพ ขั้นตอนต่อไปนี้จะให้โซลูชันที่พร้อมใช้งานในระดับ production ที่คุณสามารถผสานเข้ากับแอปพลิเคชัน Java ของคุณได้

## คำตอบสั้น ๆ
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD for Java.  
- **ใช้เวลานานแค่ไหนในการทำงานนี้?** ประมาณ 10‑15 นาทีสำหรับการตั้งค่าเบื้องต้น.  
- **ต้องติดตั้ง Photoshop ไหม?** ไม่จำเป็น ไลบรารีทำงานอิสระจาก Photoshop.  
- **เปลี่ยนสีเงาได้ไหม?** ได้ – เมธอด `setColor` รับค่า `Color` ใดก็ได้.  
- **ต้องมีไลเซนส์สำหรับการใช้งานใน production ไหม?** ต้องมีไลเซนส์เชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้.

## “add inner shadow psd” คืออะไร?
การเพิ่มเงาภายในให้กับไฟล์ PSD หมายถึงการสร้างเอฟเฟกต์เงาแบบแทรกซึมที่ทำให้ดูมีความลึกภายในเลเยอร์ เอฟเฟกต์นี้มักใช้เพื่อทำให้ UI, ไอคอน หรือข้อความโดดเด่นโดยไม่ต้องเพิ่มแสงสว่างจากภายนอก

## ทำไมต้องใช้ Java เพื่อใช้เอฟเฟกต์เลเยอร์ PSD?
การใช้ Java เพื่อ **ใช้เอฟเฟกต์เลเยอร์ PSD** ช่วยให้คุณอัตโนมัติงานออกแบบที่ทำซ้ำได้, ผสานการประมวลผลภาพเข้ากับบริการ backend, และสร้างทรัพยากรบน fly โดยไม่ต้องทำงานใน Photoshop ด้วยตนเอง Aspose.PSD มี API แบบวัตถุ‑เชิงวัตถุที่ทำให้การจัดการรูปแบบไฟล์ PSD ง่ายขึ้น

## ข้อกำหนดเบื้องต้น
ก่อนจะลงมือเขียนโค้ด ให้ตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK 11 หรือสูงกว่า)** – ดาวน์โหลดจาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – รับไฟล์ JAR ล่าสุดจาก [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse หรือ NetBeans (เลือกได้ตามสะดวก).  
4. **ความรู้พื้นฐาน Java** – ควรคุ้นเคยกับคลาส, อ็อบเจกต์, และการจัดการข้อยกเว้น.  
5. **ไฟล์ PSD ตัวอย่าง** – PSD อย่างง่ายที่มีอย่างน้อยหนึ่งเลเยอร์เพื่อทดสอบเอฟเฟกต์เงาภายใน.

## นำเข้าแพ็กเกจที่จำเป็น
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
การนำเข้าเหล่านี้ทำให้คุณเข้าถึงคลาสหลักที่ใช้ในการโหลด PSD, จัดการเลเยอร์, และตั้งค่าเอฟเฟกต์เงา

## วิธีเพิ่มเงาภายใน PSD ในไฟล์โดยใช้ Java
ต่อไปนี้เป็นคำแนะนำแบบขั้นตอนต่อขั้นตอน แต่ละขั้นมีคำอธิบายสั้น ๆ ตามด้วยโค้ดที่ต้องคัดลอก

### ขั้นตอนที่ 1: กำหนดโฟลเดอร์ต้นทางและปลายทาง
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
แทนที่พาธตัวอย่างด้วยตำแหน่งจริงบนเครื่องของคุณ

### ขั้นตอนที่ 2: โหลดไฟล์ PSD พร้อมทรัพยากรเอฟเฟกต์
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
`setLoadEffectsResource(true)` ทำให้โหลดเอฟเฟกต์ของเลเยอร์ที่มีอยู่แล้ว เพื่อให้เราสามารถแก้ไขได้

### ขั้นตอนที่ 3: เข้าถึงเลเยอร์เป้าหมาย
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
ที่นี่เราดึง **เลเยอร์สุดท้าย** ของเอกสาร ซึ่งมักเป็นเลเยอร์ที่ต้องการแก้ไข ปรับดัชนีหากต้องการเลเยอร์อื่น

### ขั้นตอนที่ 4: ตั้งค่าเอฟเฟกต์เงาภายใน
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
บล็อกนี้ **เพิ่มเงาภายใน** และปรับลักษณะการแสดง:
- **Color** – ตั้งเป็นสีเขียว (เปลี่ยนเป็น `Color` ใดก็ได้ที่คุณต้องการ).  
- **Opacity** – ความโปร่งใส 50 % (`128` จาก `255`).  
- **Distance, Size, Angle** – ควบคุมการเลื่อนและการกระจายของเงา.  
- **Spread & Noise** – เพิ่มความหลากหลายเชิงศิลปะ

### ขั้นตอนที่ 5: บันทึก PSD ที่แก้ไขแล้ว
```java
    image.save(destName, new PsdOptions(image));
```
ไฟล์ `sample_out.psd` ตอนนี้มีเอฟเฟกต์เงาภายในแล้ว

### ขั้นตอนที่ 6: ทำความสะอาดทรัพยากร
```java
} finally {
    image.dispose();
}
```
การทำลายอ็อบเจกต์ `image` จะปลดปล่อยหน่วยความจำและป้องกันการรั่วไหล ซึ่งสำคัญมากเมื่อประมวลผลไฟล์จำนวนมากในลูป

## กรณีการใช้งานทั่วไป
- **Pipeline การสร้างแบรนด์อัตโนมัติ** – เพิ่มเงาภายในที่สอดคล้องให้กับโลโก้ก่อนเผยแพร่.  
- **การสร้างทรัพยากร UI แบบไดนามิก** – สร้างสถานะปุ่มที่มีความลึกบน fly สำหรับเว็บหรือแอปมือถือ.  
- **การประมวลผลชุดของไลบรารี PSD เก่า** – ปรับปรุงการออกแบบเดิมให้มีเงาแบบสมัยใหม่โดยไม่ต้องเปิด Photoshop.

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| **`ArrayIndexOutOfBoundsException` ที่ `getEffects()[0]`** | เลเยอร์เป้าหมายยังไม่มีเอฟเฟกต์ใด ๆ แนบอยู่. | เพิ่ม `IShadowEffect` ใหม่โดยใช้ `layer.getBlendingOptions().addEffect(new ShadowEffect())` ก่อนทำการแคสท์. |
| **สีเงาไม่เปลี่ยน** | มีเอฟเฟกต์ประเภทอื่นที่ครอบคลุมเงาอยู่. | ตรวจสอบให้แน่ใจว่ากำลังแก้ไขดัชนีเอฟเฟกต์ที่ถูกต้อง หรือเคลียร์เอฟเฟกต์เดิมด้วย `layer.getBlendingOptions().clearEffects()`. |
| **ไฟล์ไม่ถูกบันทึก** | โฟลเดอร์ปลายทางไม่มีอยู่หรือไม่มีสิทธิ์เขียน. | สร้างโฟลเดอร์ล่วงหน้า (`new File(outputDir).mkdirs();`) หรือเลือกพาธที่เขียนได้. |

## คำถามที่พบบ่อย

**Q: Aspose.PSD คืออะไร?**  
A: Aspose.PSD เป็นไลบรารี Java สำหรับทำงานกับไฟล์ PSD ให้ผู้พัฒนาสามารถจัดการเอฟเฟกต์เลเยอร์, มาสก์, และคุณสมบัติต่าง ๆ ของภาพได้โดยโปรแกรม

**Q: ต้องใช้ Photoshop เพื่อใช้ Aspose.PSD หรือไม่?**  
A: ไม่จำเป็น Aspose.PSD ทำงานอิสระจาก Photoshop สำหรับการจัดการไฟล์ PSD

**Q: สามารถใช้หลายเอฟเฟกต์บนเลเยอร์เดียวได้หรือไม่?**  
A: สามารถ! คุณสามารถเพิ่มหลายเอฟเฟกต์โดยเข้าถึงแต่ละประเภทเอฟเฟกต์ในลักษณะเดียวกับที่ทำกับเงาภายใน

**Q: Aspose.PSD มีให้ใช้ฟรีหรือไม่?**  
A: Aspose.PSD เป็นผลิตภัณฑ์เชิงพาณิชย์; อย่างไรก็ตาม มีรุ่นทดลองฟรีให้ใช้ผ่าน Aspose

**Q: จะหาเอกสารเพิ่มเติมได้จากที่ไหน?**  
A: คุณสามารถดูเอกสารครบถ้วนสำหรับ Aspose.PSD ได้ [ที่นี่](https://reference.aspose.com/psd/java/).

## สรุป
คุณได้เรียนรู้วิธี **เพิ่มเงาภายใน PSD** และ **ใช้เอฟเฟกต์เลเยอร์ PSD** ด้วย Aspose.PSD for Java วิธีนี้ช่วยให้คุณอัตโนมัติกระบวนการปรับแต่งการออกแบบขั้นสูง, ผสานเข้ากับบริการ backend, หรือสร้างตัวประมวลผลชุดสำหรับไลบรารีภาพขนาดใหญ่ อย่าลังเลที่จะทดลองกับเอฟเฟกต์อื่น ๆ เช่น drop shadow, glow, bevel เพื่อขยายเครื่องมือของคุณ

---

**อัปเดตล่าสุด:** 2026-02-14  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}