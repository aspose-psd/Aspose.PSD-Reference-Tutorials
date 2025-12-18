---
date: 2025-12-17
description: เรียนรู้วิธีแก้ไขรูปเวกเตอร์ PSD โดยสนับสนุนคุณสมบัติข้อมูลบันทึกความยาวด้วย
  Aspose.PSD for Java คู่มือขั้นตอนโดยละเอียดพร้อมตัวอย่างโค้ด
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: วิธีแก้ไขรูปทรงเวกเตอร์ PSD – รองรับคุณสมบัติข้อมูลบันทึกความยาวใน Java
url: /th/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สนับสนุนคุณสมบัติข้อมูลบันทึกความยาวใน PSD - Java

## บทนำ
หากคุณต้องการ **modify PSD vector shapes** อย่างอัตโนมัติ ไลบรารี Aspose.PSD for Java จะให้คุณควบคุมไฟล์ Photoshop ได้เต็มที่จากโค้ด Java ของคุณ ในบทแนะนำนี้เราจะพาคุณผ่านทุกอย่างที่ต้องรู้เพื่อสนับสนุนคุณสมบัติข้อมูลบันทึกความยาว — ขั้นตอนสำคัญเมื่อคุณต้องการแก้ไขเลเยอร์รูปเวกเตอร์ สุดท้ายคุณจะสามารถเปิดไฟล์ PSD ปรับเปลี่ยนคุณสมบัติรูปเวกเตอร์ แล้วบันทึกไฟล์ที่อัปเดตโดยไม่ต้องออกจาก IDE ของคุณ มาเริ่มกันเลย!

## คำตอบอย่างรวดเร็ว
- **การปรับเปลี่ยน “modify PSD vector shapes” หมายถึงอะไร?** การปรับเปลี่ยนรูปทรงเรขาคณิต, การดำเนินการเส้นทาง, หรือคุณสมบัติอื่น ๆ ของเลเยอร์ที่เป็นเวกเตอร์ภายในไฟล์ PSD  
- **ไลบรารีใดจัดการเรื่องนี้?** Aspose.PSD for Java  
- **ฉันต้องการไลเซนส์หรือไม่?** สามารถใช้รุ่นทดลองฟรีเพื่อประเมินผล; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **การดำเนินการใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับสคริปต์แก้ไขรูปแบบพื้นฐาน  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** Java JDK, Aspose.PSD for Java, และไฟล์ PSD ตัวอย่าง

## อะไรคือ “modify PSD vector shapes”?
การแก้ไข PSD vector shapes หมายถึงการเปลี่ยนแปลงข้อมูลเส้นทางเวกเตอร์พื้นฐาน — เช่นบันทึกความยาวและการดำเนินการเส้นทาง — เพื่อให้รูปลักษณ์ของรูปเปลี่ยนแปลงตาม ซึ่งมีประโยชน์อย่างยิ่งสำหรับกระบวนการกราฟิกอัตโนมัติ, การประมวลผลเป็นชุด, หรือเครื่องมือออกแบบแบบกำหนดเอง

## ทำไมต้องใช้ Aspose.PSD for Java เพื่อปรับเปลี่ยน PSD vector shapes?
- **ไม่ต้องใช้ Photoshop** – ทำงานกับไฟล์ PSD โดยตรงบนเซิร์ฟเวอร์ใดก็ได้  
- **Rich API** – เข้าถึงเลเยอร์, รีซอร์ส, และข้อมูลเวกเตอร์ด้วยคลาสที่มีประเภทชัดเจน  
- **Cross‑platform** – ทำงานบน Windows, Linux, หรือ macOS กับ JDK ใดก็ได้  
- **Performance‑focused** – จัดการหน่วยความจำอย่างมีประสิทธิภาพและบันทึกไฟล์ได้เร็ว

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ดาวน์โหลดจาก [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) หรือใช้ตัวจัดการแพ็กเกจที่คุณชอบ  
2. **Aspose.PSD for Java** – รับ JAR ล่าสุดจาก [Aspose releases page](https://releases.aspose.com/psd/java/)  
3. **IDE** – IntelliJ IDEA, Eclipse, หรือเครื่องมือแก้ไข Java ใดก็ได้  
4. **ไฟล์ PSD** – สร้างไฟล์ใน Photoshop หรือใช้ไฟล์ PSD ตัวอย่างเพื่อทดลอง  
5. **ความรู้พื้นฐาน Java** – คุ้นเคยกับคลาส, อ็อบเจ็กต์, และการจัดการข้อยกเว้น

## นำเข้าแพ็กเกจ
ก่อนอื่นให้ import คลาสที่จำเป็นสำหรับทำงานกับไฟล์ PSD และรีซอร์สรูปเวกเตอร์

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีต้นทางและปลายทาง
กำหนดตำแหน่งที่ไฟล์ PSD ต้นฉบับอยู่และที่ต้องการบันทึกไฟล์ที่แก้ไขแล้ว

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD
ใช้ `Image.load` เพื่อเปิดไฟล์และแคสต์เป็น `PsdImage` เพื่อเข้าถึงฟีเจอร์เฉพาะของ PSD

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## ขั้นตอนที่ 3: ค้นหา Vsms Resource ในเลเยอร์
ข้อมูลรูปเวกเตอร์อยู่ใน `VsmsResource` ลูปผ่านรีซอร์สของเลเยอร์ที่สองเพื่อหารีซอร์สนี้

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
แต่ละ `LengthRecord` แทนเส้นทางเวกเตอร์ที่แตกต่างกัน ดึงรายการที่คุณต้องการแก้ไข

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## ขั้นตอนที่ 5: แก้ไขคุณสมบัติ Path Operation
ตอนนี้คุณสามารถ **modify PSD vector shapes** โดยเปลี่ยน `PathOperations` ของแต่ละบันทึก ซึ่งกำหนดวิธีที่รูปโต้ตอบกัน (เช่น exclusion, intersection, subtraction)

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

## ขั้นตอนที่ 7: ทำความสะอาดทรัพยากร
Dispose `PsdImage` เพื่อคืนหน่วยความจำ

```java
psdImage.dispose();
```

## ข้อผิดพลาดทั่วไปและเคล็ดลับ
- **ตรวจสอบค่า null** – ตรวจสอบให้แน่ใจว่า `resource` ไม่เป็น `null` ก่อนเข้าถึงเส้นทาง  
- **ขอบเขตดัชนีของเส้นทาง** – ตรวจสอบว่าดัชนีที่ใช้ (`[2]`, `[7]`, `[11]`) มีอยู่ใน PSD ที่กำลังแก้ไข  
- **ไลเซนส์** – การรันโดยไม่มีไลเซนส์ที่ถูกต้องจะทำให้ไฟล์ PSD ที่บันทึกมีลายน้ำ

## สรุป
คุณมีตัวอย่างครบวงจรจากต้นจนจบสำหรับการ **modify PSD vector shapes** โดยสนับสนุนคุณสมบัติข้อมูลบันทึกความยาวด้วย Aspose.PSD for Java ไม่ว่าคุณจะทำอัตโนมัติไหลงานสินทรัพย์หรือสร้างเครื่องมือออกแบบแบบกำหนดเอง API เหล่านี้ให้ความยืดหยุ่นในการจัดการเลเยอร์เวกเตอร์โดยไม่ต้องใช้ Photoshop ลองสำรวจต่อด้วยการทดลอง `PathOperations` อื่น ๆ หรือรวมการแก้ไข `LengthRecord` หลายรายการเพื่อสร้างรูปทรงที่ซับซ้อน

## คำถามที่พบบ่อย

**Q: ฉันจะจัดการกับ PSD ที่ไม่มีเลเยอร์เวกเตอร์เชปไหม?**  
A: `VsmsResource` จะไม่มีอยู่ ดังนั้น `resource` จะเป็น `null` ให้เพิ่มการตรวจสอบและข้ามขั้นตอนการแก้ไขหรือแจ้งผู้ใช้

**Q: ฉันสามารถเปลี่ยนคุณสมบัติอื่น ๆ เช่นสีเติมหรือความกว้างของเส้นขอบได้หรือไม่?**  
A: ได้ `LengthRecord` มีเมธอด setter เพิ่มเติมสำหรับสีเติม, เส้นขอบ, และความทึบ โปรดดูเอกสาร API สำหรับรายละเอียดเต็ม

**Q: สามารถประมวลผลหลายไฟล์ PSD เป็นชุดได้หรือไม่?**  
A: แน่นอน เพียงห่อโค้ดไว้ในลูปที่วนผ่านไดเรกทอรีของไฟล์ PSD และปรับพาธอินพุตและเอาต์พุตในแต่ละครั้ง

**Q: จำเป็นต้องปิดสตรีมด้วยตนเองเมื่อโหลดจากพาธไฟล์หรือไม่?**  
A: เมธอด `Image.load` จัดการสตรีมไฟล์โดยอัตโนมัติ แต่หากคุณโหลดจาก `InputStream` ต้องปิดสตรีมนั้นหลังการใช้งาน

**Q: ต้องใช้เวอร์ชัน Aspose.PSD ใดสำหรับ API เหล่านี้?**  
A: คลาส `LengthRecord` และ `PathOperations` มีตั้งแต่ Aspose.PSD 20.10 แนะนำให้ใช้เวอร์ชันล่าสุด

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}