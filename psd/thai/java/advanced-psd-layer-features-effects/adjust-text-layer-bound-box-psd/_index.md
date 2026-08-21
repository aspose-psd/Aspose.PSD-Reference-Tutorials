---
date: 2026-06-28
description: เรียนรู้วิธีแก้ไขไฟล์ PSD ด้วย Aspose.PSD for Java – ดึงและปรับกล่องขอบเขตข้อความใน
  PSD. คู่มือขั้นตอนโดยละเอียดสำหรับการแก้ไข psd ด้วยโปรแกรม
keywords:
- how to edit psd
- change photoshop text layer
- adjust text bound box
- retrieve text bound box
- update text bound box
linktitle: ปรับกล่องขอบเขตเลเยอร์ข้อความใน PSD ด้วย Java
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to edit PSD files with Aspose.PSD for Java – retrieve and
    adjust a text bound box in a PSD. Step‑by‑step guide for how to edit psd programmatically.
  headline: 'how to edit psd: Adjust Text Layer Bound Box in Java'
  type: TechArticle
- description: Learn how to edit PSD files with Aspose.PSD for Java – retrieve and
    adjust a text bound box in a PSD. Step‑by‑step guide for how to edit psd programmatically.
  name: 'how to edit psd: Adjust Text Layer Bound Box in Java'
  steps:
  - name: '**Java Development Kit (JDK)** – download from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – download from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA,
      or NetBeans.'
    text: '**Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA,
      or NetBeans.'
  - name: '**Aspose.PSD for Java Library** – obtain the latest version from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java Library** – obtain the latest version from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and arrays.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and arrays.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a robust library that lets developers create, edit, and
      convert Adobe Photoshop PSD files without needing Photoshop installed.
    question: What is Aspose.PSD?
  - answer: No, Aspose.PSD operates completely independently of Adobe Photoshop, making
      it ideal for server‑side automation.
    question: Do I need Photoshop installed to use Aspose.PSD?
  - answer: Yes, Aspose.PSD is available for .NET, Java, and Python, providing a consistent
      API across platforms.
    question: Can I use Aspose.PSD with other programming languages?
  - answer: You can get help on the official [Aspose Forum](https://forum.aspose.com/c/psd/34)
      where both staff and community members answer questions.
    question: Where can I find support for Aspose.PSD?
  - answer: Yes! Download a free trial from the [Aspose website](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 'วิธีแก้ไข psd: ปรับกล่องขอบเขตเลเยอร์ข้อความใน Java'
url: /th/java/advanced-psd-layer-features-effects/adjust-text-layer-bound-box-psd/
weight: 25
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแก้ไข PSD: ปรับขอบเขตของเลเยอร์ข้อความใน Java

## บทนำ
หากคุณกำลังสงสัย **how to edit PSD** อย่างโปรแกรมเมติก—โดยเฉพาะเมื่อคุณต้องการ **edit Photoshop text layer**—ไลบรารี Aspose.PSD สำหรับ Java จะส่องแสงสว่างอย่างโดดเด่น บทแนะนำนี้จะพาคุณผ่านขั้นตอนที่แม่นยำเพื่อ **adjust text bound box** และ **retrieve text bound box** ด้วยการใช้ **aspose psd java** ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้นกับ Java คุณจะพบคำแนะนำที่ชัดเจนและเป็นกันเองที่ทำให้การจัดการ PSD รู้สึกง่ายและเข้าถึงได้ มาเริ่มกันเลย!

## คำตอบสั้น
- **ไลบรารีใดที่ช่วยแก้ไขไฟล์ PSD ใน Java?** Aspose.PSD for Java.  
- **ฉันสามารถปรับขอบเขตของเลเยอร์ข้อความได้หรือไม่?** ใช่—ใช้ `getTextBoundBox()` และ `setSize()` เพื่อแก้ไขมัน.  
- **ต้องติดตั้ง Photoshop หรือไม่?** ไม่จำเป็น, Aspose.PSD ทำงานโดยอิสระจาก Adobe Photoshop.  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** JDK, IDE, และไลบรารี Aspose.PSD for Java.  
- **การทำงานพื้นฐานใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีเพื่อรันโค้ดตัวอย่าง.

## “how to edit psd” กับ Aspose.PSD คืออะไร?
การแก้ไข PSD อย่างโปรแกรมเมติกหมายถึงการเปิดไฟล์, เข้าถึงเลเยอร์ต่าง ๆ, และแก้ไขคุณสมบัติเช่น ขนาด, ตำแหน่ง, หรือเนื้อหาข้อความ—ทั้งหมดนี้โดยไม่ต้องเปิด Photoshop. Aspose.PSD มี API ที่ครอบคลุมซึ่งทำให้ซับซ้อนของรูปแบบ PSD ถูกแยกออก, ให้คุณมุ่งเน้นที่ตรรกะที่ต้องการ.

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java?
Aspose.PSD สำหรับ Java มีชุดคุณสมบัติที่ครบถ้วนทำให้การจัดการ PSD ง่ายและมีประสิทธิภาพ มันขจัดความจำเป็นต้องใช้ Photoshop, รองรับประเภทเลเยอร์หลักทั้งหมด, ให้การประมวลผลที่รวดเร็วแม้ไฟล์ขนาดใหญ่, และทำงานสม่ำเสมอบนสภาพแวดล้อม Windows, Linux, และ macOS.

- **No Photoshop required** – ทำงานบนเซิร์ฟเวอร์หรือเดสก์ท็อปใดก็ได้.  
- **Full layer support** – สามารถอ่านหรือแก้ไขเลเยอร์ raster, vector, และ text.  
- **High‑performance engine** – ประมวลผลไฟล์ขนาดถึง 500 MB ภายในต่ำกว่า 2 วินาทีและจัดการงานแบชของ 1,000 ไฟล์โดยใช้หน่วยความจำสูงสุดต่ำกว่า 200 MB.  
- **Cross‑platform** – รันบน Windows, Linux, หรือ macOS ด้วยโค้ดเดียวกัน.

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ดาวน์โหลดจาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA, หรือ NetBeans.  
3. **Aspose.PSD for Java Library** – รับเวอร์ชันล่าสุดจาก [Aspose releases page](https://releases.aspose.com/psd/java/).  
4. **Basic Java knowledge** – ความคุ้นเคยกับคลาส, อ็อบเจกต์, และอาเรย์.

ยอดเยี่ยม! เมื่อมีทั้งหมดแล้ว, มาเริ่มเขียนโค้ดกัน.

## นำเข้าแพ็กเกจ
ขั้นตอนแรกคือการนำเข้าคลาสที่คุณต้องการ ใช้เปรียบเทียบเป็นการรวบรวมเครื่องมือทั้งหมดก่อนเริ่มโครงการ DIY.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Size;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

การนำเข้าดังกล่าวทำให้คุณเข้าถึงการจัดการภาพ, การปรับขนาด, และคลาส `TextLayer` ที่เราจะทำงานด้วย.

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไฟล์ของคุณ
ระบุที่ตั้งของไฟล์ PSD ของคุณ เหมือนการตั้งเวทีก่อนการแสดงเริ่มต้น.

`File` objects ให้ Java ค้นหาแหล่งข้อมูลบนดิสก์.  
`String` variables เก็บเส้นทางแบบ absolute หรือ relative ไปยัง PSD ต้นฉบับและโฟลเดอร์ผลลัพธ์.

```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "LayerWithText.psd";
```

แทนที่ `"Your Document Directory"` ด้วยเส้นทางโฟลเดอร์จริงบนเครื่องของคุณ.

## ขั้นตอนที่ 2: โหลดไฟล์ PSD
ตอนนี้เราจะเปิดไฟล์ PSD เพื่อให้สามารถโต้ตอบกับเลเยอร์ต่าง ๆ ได้.

`Image.load` อ่านไฟล์และคืนค่าเป็นอ็อบเจกต์ `PsdImage` ที่พร้อมสำหรับการจัดการ.  
`PsdImage` มีเมธอดสำหรับเรียกดูเลเยอร์, เข้าถึงเมตาดาต้า, และบันทึกการเปลี่ยนแปลง.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

เมธอด `Image.load` อ่านไฟล์และคืนค่าอ็อบเจกต์ `PsdImage` ที่พร้อมสำหรับการจัดการ.

## ขั้นตอนที่ 3: ดึงเลเยอร์ข้อความ
ระบุเลเยอร์ข้อความที่ต้องการปรับ ข้อมูลเลเยอร์เริ่มจากศูนย์, ดังนั้น `[1]` หมายถึงเลเยอร์ที่สอง.

`TextLayer` เป็นคลาสเฉพาะสำหรับเลเยอร์ประเภทข้อความ; มันเปิดเผยคุณสมบัติเฉพาะของข้อความเช่น ฟอนต์, สี, และ bounding box.

```java
TextLayer textLayer = (TextLayer) im.getLayers()[1];
```

ตรวจสอบให้แน่ใจว่าคุณเลือกเลเยอร์ที่ถูกต้อง; มิฉะนั้นอาจแก้ไขเนื้อหาผิด.

## ขั้นตอนที่ 4: ตรวจสอบขนาดของเลเยอร์
ก่อนทำการเปลี่ยนแปลงใด ๆ ควรตรวจสอบขนาดปัจจุบันเพื่อความมั่นใจ.

`Size` objects มีความกว้างและความสูงเป็นพิกเซล.  
`Assert` (หรือ `if` ธรรมดา) ช่วยให้คุณตรวจสอบความคาดหวังระหว่างการพัฒนา.

```java
Size correctOpticalSize = new Size(127, 45);
Size opticalSize = textLayer.getSize();
Assert.areEqual(correctOpticalSize, opticalSize);
```

หากขนาดไม่ตรงกัน, `Assert` จะส่งการแจ้งเตือนให้คุณทราบว่ามีบางอย่างผิดพลาด.

## ขั้นตอนที่ 5: รับขนาด Bound Box
ตอนนี้เราจะดึง **text bound box**—สี่เหลี่ยมที่ล้อมรอบข้อความที่เรนเดอร์.

`getTextBoundBox()` คืนค่าอ็อบเจ็กต์ `Size` ที่อธิบายสี่เหลี่ยมที่ข้อความครอบครองหลังการเรนเดอร์, พิจารณาเมตริกของฟอนต์และระยะห่างบรรทัด.

```java
Size correctBoundBox = new Size(172, 62);
Size boundBox = textLayer.getTextBoundBox();
Assert.areEqual(correctBoundBox, boundBox);
```

คุณสามารถเปรียบเทียบขนาดนี้กับมิติที่คาดหวังหรือใช้เพื่อคำนวณการปรับเพิ่มเติม.

## วิธีดึง text bound box ด้วย Aspose.PSD Java?
เพื่อดึง text bound box, เริ่มต้นด้วยการโหลดไฟล์ PSD ด้วย `Image.load` และรับอินสแตนซ์ `PsdImage`. จากนั้นค้นหา `TextLayer` ที่ต้องการโดยวนผ่าน `psdImage.getLayers()` หรือโดยใช้ดัชนี. เรียกเมธอด `getTextBoundBox()` บนเลเยอร์นั้น; มันจะคืนค่าอ็อบเจ็กต์ `Size` ที่มีความกว้างและความสูงเป็นพิกเซลที่แม่นยำ, ซึ่งคุณสามารถบันทึกหรือใช้สำหรับการคำนวณต่อไป.

## วิธีปรับ text bound box ด้วย Aspose.PSD Java?
หลังจากที่คุณมี bound box ปัจจุบัน, คุณสามารถแก้ไขได้โดยเรียก `setSize(new Size(width, height))` โดยตรงบน `TextLayer`, โดยระบุค่าความกว้างและความสูงที่ต้องการ. อีกทางเลือกหนึ่งคือใช้เมทริกซ์การแปลงด้วยเมธอด `transform()` เพื่อสเกลหรือย้ายตำแหน่งข้อความก่อนทำ rasterizing เลเยอร์. ทั้งสองวิธีจะอัปเดตการจัดวางภาพให้ตรงตามความต้องการออกแบบของคุณ.

## กรณีการใช้งานทั่วไป
- **Dynamic thumbnail generation** – ปรับขอบเขตข้อความก่อนทำ rasterizing ตัวอย่างภาพ.  
- **Automated branding** – แทนที่ข้อความโลโก้โดยอัตโนมัติและตรวจสอบให้พอดีกับข้อจำกัดการออกแบบ.  
- **Batch processing** – วนผ่านไฟล์ PSD จำนวนมากเพื่อทำให้ขนาดเลเยอร์ข้อความสอดคล้องกันทั่วทั้งสายผลิตภัณฑ์.

## การแก้ไขปัญหาและเคล็ดลับ
- **Incorrect layer index** – ตรวจสอบลำดับของเลเยอร์ใน Photoshop อีกครั้ง; ดัชนีอาจแตกต่างจากที่คุณคาดคิด.  
- **License issues** – เวอร์ชันทดลองอาจจำกัดบางการดำเนินการ; ตรวจสอบว่าคุณมีไลเซนส์ที่ถูกต้องสำหรับการผลิต.  
- **Unexpected sizes** – การตั้งค่า DPI สามารถส่งผลต่อการคำนวณขนาด; ตรวจสอบความละเอียดของ PSD หากตัวเลขดูแปลก.  
- **Performance tip** – ใช้อ็อบเจ็กต์ `PsdImage` เดียวกันเมื่อประมวลผลหลายเลเยอร์เพื่อลดการจัดสรรหน่วยความจำ.

## สรุป
คุณได้เรียนรู้ **how to edit PSD** ด้วยการดึงและปรับขอบเขตของเลเยอร์ข้อความโดยใช้ **aspose psd java** แล้ว. ด้วยเพียงไม่กี่บรรทัดของโค้ดคุณสามารถโหลด PSD, เลือกเลเยอร์เฉพาะ, ตรวจสอบมิติของมัน, และทำให้ข้อความพอดีอย่างสมบูรณ์. สำหรับการสำรวจเพิ่มเติม—เช่นการแก้ไขเนื้อหาข้อความ, การใช้เอฟเฟกต์, หรือการส่งออกเป็นรูปแบบอื่น—ดูเอกสาร Aspose.PSD เต็มรูปแบบ [here](https://reference.aspose.com/psd/java/).

## คำถามที่พบบ่อย
**Q: Aspose.PSD คืออะไร?**  
A: Aspose.PSD เป็นไลบรารีที่แข็งแกร่งซึ่งช่วยให้นักพัฒนาสร้าง, แก้ไข, และแปลงไฟล์ Adobe Photoshop PSD ได้โดยไม่ต้องติดตั้ง Photoshop.

**Q: จำเป็นต้องติดตั้ง Photoshop เพื่อใช้ Aspose.PSD หรือไม่?**  
A: ไม่จำเป็น, Aspose.PSD ทำงานอย่างอิสระจาก Adobe Photoshop อย่างสมบูรณ์, ทำให้เหมาะสำหรับการทำงานอัตโนมัติบนเซิร์ฟเวอร์.

**Q: สามารถใช้ Aspose.PSD กับภาษาโปรแกรมอื่นได้หรือไม่?**  
A: ได้, Aspose.PSD มีให้สำหรับ .NET, Java, และ Python, ให้ API ที่สอดคล้องกันบนหลายแพลตฟอร์ม.

**Q: จะหาแหล่งสนับสนุนสำหรับ Aspose.PSD ได้จากที่ไหน?**  
A: คุณสามารถรับความช่วยเหลือได้ใน [Aspose Forum](https://forum.aspose.com/c/psd/34) อย่างเป็นทางการ, ที่ซึ่งทั้งทีมงานและสมาชิกชุมชนตอบคำถาม.

**Q: มีเวอร์ชันทดลองสำหรับ Aspose.PSD หรือไม่?**  
A: มี! ดาวน์โหลดเวอร์ชันทดลองฟรีจาก [Aspose website](https://releases.aspose.com/).

**อัปเดตล่าสุด:** 2026-06-28  
**ทดสอบด้วย:** Aspose.PSD for Java (latest)  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีแก้ไขเลเยอร์ข้อความ PSD ด้วย Aspose.PSD for Java](/psd/java/advanced-psd-layer-features-effects/update-text-layer-psd-files/)
- [เพิ่มเลเยอร์ข้อความใน Runtime ในไฟล์ PSD ด้วย Java](/psd/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/)
- [เรนเดอร์เลเยอร์ข้อความที่หมุนในไฟล์ PSD ด้วย Java](/psd/java/psd-layer-management-effects/render-rotated-text-layer-psd/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}