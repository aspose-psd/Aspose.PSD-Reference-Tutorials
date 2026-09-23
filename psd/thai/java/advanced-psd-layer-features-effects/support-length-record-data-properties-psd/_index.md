---
date: 2026-09-23
description: เรียนรู้วิธีแก้ไขรูปแบบเวกเตอร์ PSD และประมวลผลไฟล์ PSD เป็นชุดโดยใช้
  Aspose.PSD for Java รายละเอียดขั้นตอนอย่างละเอียด เคล็ดลับ และโค้ดตัวอย่างสำหรับโซลูชันที่ครบถ้วน
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: สนับสนุนคุณสมบัติข้อมูล Length Record ใน PSD - Java
og_description: เรียนรู้วิธีแก้ไขรูปแบบเวกเตอร์ PSD และประมวลผลไฟล์ PSD เป็นชุดโดยใช้
  Aspose.PSD for Java คู่มือขั้นตอนต่อขั้นตอนพร้อมโค้ดตัวอย่างและเคล็ดลับจากผู้เชี่ยวชาญ
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: แก้ไขรูปแบบเวกเตอร์ PSD ด้วย Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: แก้ไขรูปแบบเวกเตอร์ PSD ด้วย Aspose.PSD for Java
url: /th/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แก้ไขรูปเวกเตอร์ PSD ด้วย Aspose.PSD สำหรับ Java

## บทนำ
หากคุณต้องการ **แก้ไขรูปเวกเตอร์ PSD** อย่างโปรแกรมมิ่ง, Aspose.PSD สำหรับ Java จะให้คุณควบคุมไฟล์ Photoshop ได้โดยตรงจากโค้ด Java ของคุณ บทเรียนนี้จะพาคุณผ่านการสนับสนุนคุณสมบัติ length record — ขั้นตอนสำคัญเมื่อแก้ไขเลเยอร์รูปเวกเตอร์ เมื่อเสร็จคุณจะสามารถเปิดไฟล์ PSD, ปรับข้อมูลรูปเวกเตอร์, และบันทึกไฟล์ที่อัปเดตโดยไม่ต้องเปิด Photoshop.

## คำตอบสั้น
- **อะไรหมายถึง “แก้ไขรูปเวกเตอร์ PSD”?** การปรับเรขาคณิต, การดำเนินการเส้นทาง, หรือคุณลักษณะอื่นของเลเยอร์ที่เป็นเวกเตอร์ภายในไฟล์ PSD.  
- **ไลบรารีใดจัดการเรื่องนี้?** Aspose.PSD for Java.  
- **ฉันต้องการไลเซนส์หรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการประเมิน; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับสคริปต์แก้ไขรูปพื้นฐาน.  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** Java JDK, Aspose.PSD for Java, และไฟล์ PSD ตัวอย่าง.

## “สนับสนุนคุณสมบัติ length record” คืออะไร
การสนับสนุนคุณสมบัติ length record หมายถึงการเข้าถึงและอัปเดตอ็อบเจ็กต์ `LengthRecord` ที่อธิบายแต่ละเส้นทางเวกเตอร์ภายใน PSD รายการเหล่านี้เก็บข้อมูลเช่น ความยาวของเส้นทาง, ประเภท, และวิธีการเชื่อมต่อกับเส้นทางอื่น การเปลี่ยนแปลงเหล่านี้ทำให้คุณควบคุมว่ารูปทรงรวมกัน, ตัดกัน, หรือหักลบกันอย่างไร ทำให้การแก้ไขเวกเตอร์มีความแม่นยำ

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java เพื่อสนับสนุนคุณสมบัติ length record
โหลด PSD ของคุณ, แก้ไขข้อมูลเวกเตอร์, และบันทึก — ทั้งหมดโดยไม่ต้องใช้ Photoshop Aspose.PSD ประมวลผล PSD หลายร้อยหน้าในเวลาไม่ถึง 2 วินาทีบนเซิร์ฟเวอร์ทั่วไป, มีคลาสมากกว่า 150 คลาส (รวมถึงประเภทเวกเตอร์กว่า 30 ประเภท), และทำงานบน Windows, Linux, หรือ macOS กับ JDK 11+ ใดก็ได้ ไลบรารีที่เน้นประสิทธิภาพนี้ช่วยขจัดความจำเป็นในการใช้ซอฟต์แวร์เดสก์ท็อปที่มีค่าใช้จ่ายสูง

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ดาวน์โหลดจาก [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) หรือใช้ผู้จัดการแพ็กเกจที่คุณชื่นชอบ.  
2. **Aspose.PSD for Java** – รับไฟล์ JAR ล่าสุดจาก [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse หรือเครื่องมือแก้ไขที่เข้ากันได้กับ Java ใดก็ได้.  
4. **ไฟล์ PSD** – สร้างไฟล์ใน Photoshop หรือดึงไฟล์ PSD ตัวอย่างมาทดลอง.  
5. **ความรู้พื้นฐาน Java** – ความคุ้นเคยกับคลาส, อ็อบเจ็กต์, และการจัดการข้อยกเว้น.

## นำเข้าแพ็กเกจ
คำสั่ง import จะนำคลาสหลักของ Aspose.PSD เข้ามาในสโคป เช่น `PsdImage`, `VsmsResource`, และ `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีต้นทางและไดเรกทอรีผลลัพธ์ของคุณ
กำหนดตำแหน่งที่ไฟล์ PSD ต้นฉบับอยู่และตำแหน่งที่ไฟล์ที่แก้ไขแล้วจะถูกเขียนออกไป.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD
ใช้ `Image.load` เพื่อเปิดไฟล์และแคสต์เป็น `PsdImage` เพื่อใช้คุณลักษณะเฉพาะของ PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## ขั้นตอนที่ 3: ค้นหาแหล่งข้อมูล Vsms ในเลเยอร์
`VsmsResource` คือคอนเทนเนอร์ที่เก็บข้อมูลรูปเวกเตอร์ของเลเยอร์ ทำการวนลูปผ่านทรัพยากรของเลเยอร์ที่สองเพื่อค้นหา.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## ขั้นตอนที่ 4: เข้าถึง length records
`LengthRecord` แทนเส้นทางเวกเตอร์ที่แยกจากกัน ดึงรายการที่คุณต้องการแก้ไข.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## ขั้นตอนที่ 5: แก้ไขคุณสมบัติการดำเนินการเส้นทาง
`PathOperations` กำหนดว่ารูปทรงแต่ละรูปทำงานร่วมกันอย่างไร (เช่น การแยก, การตัดกัน, การลบ) การเปลี่ยนค่าต่าง ๆ จะอัปเดตการจัดวางภาพของเลเยอร์เวกเตอร์.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
บันทึกการเปลี่ยนแปลงของคุณลงในไฟล์ใหม่.

```java
psdImage.save(outPsdFilePath);
```

## ขั้นตอนที่ 7: ทำความสะอาดทรัพยากร
ทำการ dispose อินสแตนซ์ `PsdImage` เพื่อคืนหน่วยความจำและหลีกเลี่ยงการรั่วของทรัพยากร.

```java
psdImage.dispose();
```

## วิธีการประมวลผลไฟล์ PSD แบบกลุ่มด้วยการสนับสนุนคุณสมบัติ length record
ห่อหุ้มกระบวนการทำงานไฟล์เดียวในลูปที่วนผ่านไดเรกทอรีของ PSDs, ปรับค่า `inPsdFilePath` และ `outPsdFilePath` สำหรับแต่ละไฟล์ วิธีนี้ทำให้คุณสามารถปรับรูปเวกเตอร์เดียวกันให้กับหลายสิบหรือหลายร้อยไฟล์ในเวลาไม่กี่นาที เหมาะสำหรับสายงานอัตโนมัติของทรัพยากร.

## ข้อผิดพลาดทั่วไปและเคล็ดลับ
- **ตรวจสอบค่า null** – ตรวจสอบเสมอว่า `resource` ไม่เป็น `null` ก่อนเข้าถึงสมาชิกของมัน.  
- **ขอบเขตดัชนีเส้นทาง** – ตรวจสอบว่าดัชนีที่คุณใช้ (เช่น `[2]`, `[7]`, `[11]`) มีอยู่ใน PSD ที่กำลังแก้ไข.  
- **ไลเซนส์** – การทำงานโดยไม่มีไลเซนส์ที่ถูกต้องจะฝังลายน้ำใน PSD ที่บันทึก.  

## สรุป
ตอนนี้คุณมีตัวอย่างครบวงจรจากต้นจนจบว่า **แก้ไขรูปเวกเตอร์ PSD** อย่างไรโดยการสนับสนุนคุณสมบัติ length record ด้วย Aspose.PSD สำหรับ Java ไม่ว่าคุณจะทำอัตโนมัติในสายงานทรัพยากรหรือสร้างเครื่องมือออกแบบแบบกำหนดเอง API เหล่านี้ให้ความยืดหยุ่นในการจัดการเลเยอร์เวกเตอร์โดยไม่ต้องทำงานใน Photoshop ทดลองเปลี่ยนค่า `PathOperations` อื่น ๆ หรือรวมการแก้ไข `LengthRecord` หลายรายการเพื่อสร้างรูปทรงซับซ้อน.

## คำถามที่พบบ่อย

**Q: ฉันจะจัดการกับ PSD ที่ไม่มีเลเยอร์รูปเวกเตอร์อย่างไร?**  
**A:** `VsmsResource` จะไม่มีอยู่, ดังนั้น `resource` จะเป็น `null`. เพิ่มการตรวจสอบและข้ามขั้นตอนการแก้ไขหรือแจ้งผู้ใช้.

**Q: ฉันสามารถเปลี่ยนคุณสมบัติอื่น ๆ เช่น สีเติมหรือความกว้างของเส้นขอบได้หรือไม่?**  
**A:** ใช่, `LengthRecord` มีเมธอด setter สำหรับการเติม, เส้นขอบ, และความทึบแสง. ดูเอกสาร API สำหรับรายการทั้งหมด.

**Q: สามารถประมวลผลหลายไฟล์ PSD พร้อมกันได้หรือไม่?**  
**A:** แน่นอน. ห่อโค้ดภายในลูปที่วนผ่านไดเรกทอรีของไฟล์ PSD, ปรับพาธอินพุตและเอาต์พุตในแต่ละครั้ง.

**Q: จำเป็นต้องปิดสตรีมด้วยตนเองเมื่อโหลดจากพาธไฟล์หรือไม่?**  
**A:** `Image.load` จัดการสตรีมไฟล์โดยอัตโนมัติ, แต่หากคุณโหลดจาก `InputStream` จำเป็นต้องปิดหลังการใช้.

**Q: ต้องใช้เวอร์ชันของ Aspose.PSD ใดสำหรับ API เหล่านี้?**  
**A:** คลาส `LengthRecord` และ `PathOperations` มีตั้งแต่ Aspose.PSD 20.10. แนะนำให้ใช้เวอร์ชันล่าสุด (24.11 ณ เวลาที่เขียน) .

---

**อัปเดตล่าสุด:** 2026-09-23  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [แปลง PSD เป็น PNG และสร้าง Vector Mask ด้วย Java – แหล่งข้อมูล Vmsk ในไฟล์ PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [แปลง PSD เป็น PNG พร้อมการสนับสนุน Layer Mask ด้วย Aspose.PSD for Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [เพิ่มการสนับสนุน Layer ในไฟล์ PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}