---
date: 2026-02-20
description: เรียนรู้วิธีสนับสนุนคุณสมบัติ length record และประมวลผลไฟล์ PSD เป็นชุดโดยใช้
  Aspose.PSD for Java คู่มือแบบขั้นตอนต่อขั้นตอนพร้อมตัวอย่างโค้ด
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: สนับสนุนคุณสมบัติ Length Record – แก้ไขรูปทรงเวกเตอร์ PSD (Java)
url: /th/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สนับสนุนคุณสมบัติ Length Record – แก้ไขรูปเวกเตอร์ PSD (Java)

## คำแนะนำ
หากคุณต้องการ **แก้ไขรูปเวกเตอร์ PSD** อย่างอัตโนมัติ ไลบรารี Aspose.PSD for Java จะให้คุณควบคุมไฟล์ Photoshop ได้โดยตรงจากโค้ด Java ของคุณ ในบทเรียนนี้เราจะอธิบายทุกอย่างที่คุณต้องรู้เพื่อ **สนับสนุนคุณสมบัติ Length Record** — ขั้นตอนสำคัญเมื่อคุณต้องการแก้ไขเลเยอร์รูปเวกเตอร์ เมื่อเสร็จแล้วคุณจะสามารถเปิดไฟล์ PSD ปรับคุณสมบัติรูปเวกเตอร์และบันทึกไฟล์ที่อัปเดตได้โดยไม่ต้องออกจาก IDE ของคุณ มาเริ่มกันเลย!

## คำตอบสั้น
- **“แก้ไขรูปเวกเตอร์ PSD” หมายถึงอะไร?** การปรับเปลี่ยนรูปทรง, การดำเนินการเส้นทาง, หรือคุณสมบัติเพิ่มเติมของเลเยอร์แบบเวกเตอร์ภายในไฟล์ PSD  
- **ไลบรารีใดรับผิดชอบ?** Aspose.PSD for Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการประเมินผล; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **ใช้เวลาพัฒนาเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับสคริปต์แก้ไขรูปแบบพื้นฐาน  
- **ข้อกำหนดหลักคืออะไร?** Java JDK, Aspose.PSD for Java, และไฟล์ PSD ตัวอย่าง

## “สนับสนุนคุณสมบัติ Length Record” คืออะไร?
การสนับสนุนคุณสมบัติ Length Record หมายถึงการเข้าถึงและอัปเดตอ็อบเจ็กต์ `LengthRecord` ที่อธิบายแต่ละเส้นทางเวกเตอร์ภายใน PSD การเปลี่ยนแปลงเรคคอร์ดเหล่านี้ทำให้คุณควบคุมวิธีที่รูปทรงรวมกัน, ตัดกัน, หรือหักลบกันได้

## ทำไมต้องใช้ Aspose.PSD for Java เพื่อสนับสนุนคุณสมบัติ Length Record?
- **ไม่ต้องใช้ Photoshop** – ทำงานกับไฟล์ PSD โดยตรงบนเซิร์ฟเวอร์ใดก็ได้  
- **API ครบถ้วน** – เข้าถึงเลเยอร์, รีซอร์ส, และข้อมูลเวกเตอร์ด้วยคลาสที่มีประเภทชัดเจน  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux หรือ macOS กับ JDK ใดก็ได้  
- **เน้นประสิทธิภาพ** – จัดการหน่วยความจำอย่างมีประสิทธิภาพและบันทึกไฟล์ได้เร็ว  

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ดาวน์โหลดจาก [เว็บไซต์ของ Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) หรือใช้แพคเกจเมเนเจอร์ที่คุณชื่นชอบ  
2. **Aspose.PSD for Java** – รับไฟล์ JAR ล่าสุดจาก [หน้า releases ของ Aspose](https://releases.aspose.com/psd/java/)  
3. **IDE** – IntelliJ IDEA, Eclipse หรือเครื่องมือแก้ไข Java ใดก็ได้  
4. **ไฟล์ PSD** – สร้างไฟล์ใน Photoshop หรือใช้ไฟล์ PSD ตัวอย่างเพื่อทดลอง  
5. **ความรู้พื้นฐาน Java** – รู้จักคลาส, อ็อบเจ็กต์, และการจัดการข้อยกเว้น  

## นำเข้าแพ็กเกจ
ก่อนอื่นให้นำเข้าคลาสที่จำเป็นสำหรับทำงานกับไฟล์ PSD และรีซอร์สรูปเวกเตอร์

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์ต้นทางและปลายทาง
กำหนดตำแหน่งที่ไฟล์ PSD ต้นฉบับอยู่และที่ต้องการบันทึกไฟล์ที่แก้ไขแล้ว

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD
ใช้ `Image.load` เพื่อเปิดไฟล์และแคสต์เป็น `PsdImage` เพื่อใช้ฟีเจอร์เฉพาะของ PSD

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## ขั้นตอนที่ 3: ค้นหารีซอร์ส Vsms ในเลเยอร์
ข้อมูลรูปเวกเตอร์อยู่ใน `VsmsResource` ลูปผ่านรีซอร์สของเลเยอร์ที่สองเพื่อค้นหา

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## ขั้นตอนที่ 4: เข้าถึง Length Records
แต่ละ `LengthRecord` แทนเส้นทางเวกเตอร์ที่แตกต่างกัน ดึงเรคคอร์ดที่ต้องการแก้ไข

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## ขั้นตอนที่ 5: แก้ไขคุณสมบัติ Path Operation
ตอนนี้คุณสามารถ **แก้ไขรูปเวกเตอร์ PSD** โดยเปลี่ยน `PathOperations` ของมัน ซึ่งกำหนดว่ารูปทรงจะทำงานร่วมกันอย่างไร (เช่น การยกเว้น, การตัดกัน, การหักลบ)

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
บันทึกการเปลี่ยนแปลงของคุณลงในไฟล์ใหม่

```java
psdImage.save(outPsdFilePath);
```

## ขั้นตอนที่ 7: ทำความสะอาดรีซอร์ส
เรียก `dispose` กับ `PsdImage` เพื่อคืนหน่วยความจำ

```java
psdImage.dispose();
```

## วิธีประมวลผลไฟล์ PSD เป็นชุดพร้อมสนับสนุนคุณสมบัติ Length Record
หากต้องการปรับการตั้งค่ารูปเวกเตอร์เดียวกันกับหลายไฟล์ PSD ให้ใส่โค้ดข้างต้นไว้ในลูปที่วนผ่านโฟลเดอร์ของไฟล์ ปรับค่า `inPsdFilePath` และ `outPsdFilePath` สำหรับแต่ละรอบ และคุณจะสามารถ **ประมวลผลไฟล์ PSD เป็นชุด** ได้อย่างมีประสิทธิภาพ

## ข้อผิดพลาดทั่วไป & เคล็ดลับ
- **ตรวจสอบค่า null** – ตรวจสอบให้แน่ใจว่า `resource` ไม่เป็น `null` ก่อนเข้าถึงเส้นทาง  
- **ขอบเขตดัชนีของเส้นทาง** – ตรวจสอบว่าดัชนีที่คุณใช้ (`[2]`, `[7]`, `[11]`) มีอยู่ใน PSD ที่กำลังแก้ไข  
- **ลิขสิทธิ์** – หากรันโดยไม่มีลิขสิทธิ์ที่ถูกต้อง จะมีลายน้ำแทรกใน PSD ที่บันทึก  

## สรุป
คุณได้เห็นตัวอย่างครบวงจรว่าต้อง **แก้ไขรูปเวกเตอร์ PSD** อย่างไรโดยสนับสนุนคุณสมบัติ Length Record ด้วย Aspose.PSD for Java ไม่ว่าคุณจะทำอัตโนมัติใน pipeline ของสินทรัพย์หรือสร้างเครื่องมือออกแบบแบบกำหนดเอง API เหล่านี้ให้ความยืดหยุ่นในการจัดการเลเยอร์เวกเตอร์โดยไม่ต้องใช้ Photoshop ลองสำรวจต่อด้วยการทดลอง `PathOperations` อื่น ๆ หรือรวมการแก้ไข `LengthRecord` หลายรายการเพื่อสร้างรูปทรงที่ซับซ้อน

## คำถามที่พบบ่อย

**ถาม: จะจัดการกับ PSD ที่ไม่มีเลเยอร์รูปเวกเตอร์อย่างไร?**  
ตอบ: `VsmsResource` จะไม่มีอยู่ ดังนั้น `resource` จะเป็น `null` ให้เพิ่มการตรวจสอบและข้ามขั้นตอนการแก้ไขหรือแจ้งผู้ใช้

**ถาม: สามารถเปลี่ยนคุณสมบัติอื่น ๆ เช่น สีเติมหรือความกว้างของเส้นขอบได้หรือไม่?**  
ตอบ: ได้, `LengthRecord` มีเมธอด setter เพิ่มเติมสำหรับสีเติม, เส้นขอบ, และความทึบ โปรดดูเอกสาร API เพื่อรายละเอียดเต็ม

**ถาม: สามารถประมวลผลหลายไฟล์ PSD เป็นชุดได้หรือไม่?**  
ตอบ: แน่นอน. ใส่โค้ดไว้ในลูปที่วนผ่านโฟลเดอร์ของไฟล์ PSD แล้วปรับเส้นทางอินพุตและเอาต์พุตในแต่ละรอบ

**ถาม: จำเป็นต้องปิดสตรีมด้วยตนเองเมื่อโหลดจากเส้นทางไฟล์หรือไม่?**  
ตอบ: เมธอด `Image.load` จัดการสตรีมไฟล์โดยอัตโนมัติ แต่หากโหลดจาก `InputStream` ต้องปิดสตรีมด้วยตนเองหลังใช้งาน

**ถาม: ต้องใช้เวอร์ชัน Aspose.PSD ใดสำหรับ API เหล่านี้?**  
ตอบ: คลาส `LengthRecord` และ `PathOperations` มีตั้งแต่ Aspose.PSD 20.10 แนะนำให้ใช้เวอร์ชันล่าสุด

---

**อัปเดตล่าสุด:** 2026-02-20  
**ทดสอบกับ:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}