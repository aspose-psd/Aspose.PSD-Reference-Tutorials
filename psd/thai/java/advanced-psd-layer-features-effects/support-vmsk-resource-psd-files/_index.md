---
date: 2026-02-22
description: เรียนรู้วิธีสร้างเวกเตอร์มาสก์ใน Java ด้วย Aspose.PSD for Java, เพิ่มเวกเตอร์มาสก์ในไฟล์
  PSD, และจัดการทรัพยากร Vmsk อย่างโปรแกรมมิ่ง.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: สร้างมาสก์เวกเตอร์ Java – ทรัพยากร Vmsk ในไฟล์ PSD
url: /th/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง Vector Mask ด้วย Java – ทรัพยากร Vmsk ในไฟล์ PSD

## บทนำ
หากคุณต้องการ **สร้าง vector mask** (Vmsk) ภายในไฟล์ Photoshop (PSD) Aspose.PSD for Java จะมอบวิธีการที่สะอาดและเป็นโปรแกรมเมติกให้คุณ ไม่ว่าคุณจะกำลังสร้างเครื่องมือออกแบบอัตโนมัติหรือเพิ่มการสนับสนุน mask แบบกำหนดเองให้กับ pipeline กราฟิกที่มีอยู่แล้ว บทแนะนำนี้จะพาคุณผ่านทุกขั้นตอน—การโหลด PSD, การอ่านทรัพยากร Vmsk, การปรับคุณสมบัติ, และการบันทึกผลลัพธ์ สุดท้ายคุณจะคุ้นเคยกับการจัดการ vector mask, การแปลง PSD เป็น PNG, และการขยายไฟล์ด้วยข้อมูลเวกเตอร์เพิ่มเติม—ทั้งหมดด้วยเทคนิค **create vector mask java**.

## คำตอบสั้น
- **ทรัพยากร Vmsk คืออะไร?** เป็นข้อมูล vector mask ที่เก็บอยู่ในไฟล์ PSD กำหนดรูปร่างเวกเตอร์ที่ซับซ้อนสำหรับเลเยอร์หนึ่ง  
- **ไลบรารีใดสนับสนุน?** Aspose.PSD for Java ให้การเข้าถึงแบบอ่าน/เขียนเต็มรูปแบบต่อทรัพยากร Vmsk  
- **ต้องมีลิขสิทธิ์หรือไม่?** มีรุ่นทดลองฟรี; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์  
- **สามารถแปลง PSD ที่แก้ไขแล้วเป็น PNG ได้หรือไม่?** ได้—บันทึกแล้วคุณสามารถโหลด PSD อีกครั้งและส่งออกเป็น PNG ด้วย API เดียวกัน  
- **รองรับ Maven หรือไม่?** แน่นอน; สามารถเพิ่ม Aspose.PSD เป็น dependency ของ Maven (ดูคีย์เวิร์ด “aspose psd maven”)

## Vector Mask คืออะไร (ทรัพยากร Vmsk)?
Vector mask (Vmsk) คือ mask ที่ไม่อิงพิกเซล ใช้เส้นโค้ง Bézier และบันทึกเส้นทางเพื่อกำหนดพื้นที่โปร่งใสและทึบบนเลเยอร์ เนื่องจากเป็นแบบเวกเตอร์ จึงสามารถขยายโดยไม่สูญเสียคุณภาพ—เหมาะสำหรับกราฟิกความละเอียดสูง

## ทำไมต้องสร้าง Vector Mask ด้วย Aspose.PSD?
- **Automation:** เพิ่มหรือแก้ไข mask ผ่านโปรแกรมโดยไม่ต้องเปิด Photoshop  
- **Consistency:** ทำให้ทุก PSD ที่สร้างขึ้นปฏิบัติตามกฎ mask เดียวกัน  
- **Cross‑platform:** ทำงานบน OS ใดก็ได้ที่รองรับ Java  
- **Integration:** ผสานกับ API ของ Aspose อื่น ๆ (เช่น แปลง PSD → PNG) เพื่อสร้าง workflow ครบวงจร  
- **Scalability:** Vector mask คมชัดทุกขนาด เหมาะกับการออกแบบที่ตอบสนองต่ออุปกรณ์ต่าง ๆ  

## ทำไมเรื่องนี้ถึงสำคัญสำหรับนักพัฒนา Java
การใช้เทคนิค **create vector mask java** ทำให้คุณฝังตรรกะกราฟิกขั้นสูงลงในบริการ back‑end, pipeline CI, หรือยูทิลิตี้เดสก์ท็อปได้โดยตรง ไม่ต้องพึ่งนักออกแบบเพิ่ม mask ด้วยตนเอง โค้ดของคุณสามารถสร้างหรือปรับ mask ได้ทันที ช่วยประหยัดเวลาและลดข้อผิดพลาดจากมนุษย์

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงมือเขียนโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

### สิ่งที่คุณต้องการ
- Java Development Kit (JDK): ตรวจสอบว่ามี JDK ติดตั้งบนเครื่องของคุณ หากยังไม่มีสามารถดาวน์โหลดได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html)  
- Aspose.PSD for Java Library: ไลบรารีที่ทรงพลังสำหรับจัดการไฟล์ PSD ดาวน์โหลดได้จาก [Aspose release page](https://releases.aspose.com/psd/java/) สำหรับผู้ที่ต้องการทดลองก่อนซื้อ สามารถเริ่มต้นด้วย [free trial](https://releases.aspose.com/)  
- IDE: IDE ใดก็ได้สำหรับ Java (เช่น IntelliJ IDEA, Eclipse ฯลฯ) จะทำงานได้กับโปรเจกต์นี้  

### การตั้งค่าพื้นที่ทำงานของคุณ
1. **Create a New Java Project** – เปิด IDE ที่คุณชื่นชอบและสร้างโปรเจกต์ใหม่  
2. **Add the Aspose Library** – หลังจากดาวน์โหลดไฟล์ JAR ของ Aspose ให้เพิ่มเข้าไปใน build path ของโปรเจกต์เพื่อให้เข้าถึงคลาสที่เกี่ยวกับ PSD ได้  

เมื่อพร้อมแล้ว เรามาเริ่มการทำงานจริงกัน

## วิธีสร้าง vector mask ในไฟล์ PSD ด้วย Java
ต่อไปนี้เป็นคำแนะนำแบบขั้นตอนต่อขั้นตอน โค้ดบล็อกจะคงไว้ตามต้นฉบับ; เราเพียงเพิ่มข้อความอธิบายเพื่อให้แต่ละขั้นชัดเจนยิ่งขึ้น

### นำเข้าแพ็กเกจ
ก่อนที่เราจะทำงานกับไฟล์ PSD เราต้องนำเข้าคลาสที่จำเป็นจากไลบรารี Aspose.PSD

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

ตอนนี้เราพร้อมแล้ว ไปดำเนินการแต่ละขั้นตอนต่อไป

### ขั้นตอนที่ 1: โหลดไฟล์ PSD ของคุณ
สิ่งแรกที่ต้องทำคือโหลดไฟล์ PSD ของคุณ ซึ่งเป็นจุดเริ่มต้นของทุกอย่าง

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- เรากำหนด `dataDir` ให้เป็นไดเรกทอรีของไฟล์ PSD  
- สร้างสตริง `sourceFileName` โดยรวมไดเรกทอรีกับชื่อไฟล์ PSD  
- สุดท้ายโหลดไฟล์ PSD เข้าออบเจ็กต์ `PsdImage` ด้วย `Image.load()`

### ขั้นตอนที่ 2: ดึงทรัพยากร Vmsk
เมื่อโหลดภาพ PSD แล้ว ให้ดึงทรัพยากร Vmsk ออกมา

```java
VmskResource resource = getVmskResource(im);
```

- เรียกเมธอด `getVmskResource()` เพื่อค้นหาและดึงทรัพยากร Vmsk จากภาพ

### ขั้นตอนที่ 3: ตรวจสอบคุณสมบัติของทรัพยากร Vmsk
ก่อนทำการแก้ไข ควรตรวจสอบว่าทรัพยากร Vmsk อยู่ในสถานะที่คาดหวังหรือไม่

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- ตรวจสอบคุณสมบัติต่าง ๆ ของ Vmsk เช่น ไม่ได้ถูกปิดใช้งาน, ไม่ได้กลับด้าน, ไม่ได้เชื่อมโยง, และมีจำนวนเส้นทางที่ถูกต้อง

### ขั้นตอนที่ 4: เข้าถึงแต่ละ Path และตรวจสอบ
สำรวจลึกลงไปใน Path ภายในทรัพยากร Vmsk

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- ดึงบันทึก Path สามรายการที่ระบุและตรวจสอบประเภทและคุณสมบัติเพื่อให้แน่ใจว่าตรงตามเกณฑ์ของเรา

### ขั้นตอนที่ 5: แก้ไขทรัพยากร Vmsk
เข้าสู่ส่วนการปรับแก้! สามารถเปลี่ยนแปลงคุณสมบัติของ Vmsk ได้ตามต้องการ

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- ในบล็อกนี้ เราเปิด/ปิดคุณสมบัติต่าง ๆ ของ Vmsk โดยตั้งค่าเป็น `true` เพื่อควบคุมการทำงานของ mask ในไฟล์ PSD

### ขั้นตอนที่ 6: ปรับจุด Bezier Knot
จุด Knot ของ Bézier มีความสำคัญต่อเส้นทางเวกเตอร์ ให้เปลี่ยนค่าบางส่วน

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- เข้าถึง `BezierKnotRecord` เฉพาะและเปลี่ยนจุดเพื่อปรับรูปร่างของ vector mask

### ขั้นตอนที่ 7: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
เมื่อแก้ไขครบทุกอย่างแล้ว ให้บันทึกไฟล์ PSD ใหม่

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- กำหนดเส้นทางสำหรับไฟล์ PSD ที่ส่งออก แล้วเรียก `im.save()` เพื่อเขียนการเปลี่ยนแปลงลงไฟล์ใหม่

### ขั้นตอนที่ 8: ทำความสะอาดทรัพยากร
สุดท้ายต้องแน่ใจว่าได้ทำการปล่อยทรัพยากรของภาพอย่างถูกต้อง

```java
im.dispose();
```

- การเรียก `dispose()` เสมอเป็นแนวปฏิบัติที่ดีเพื่อป้องกันการรั่วไหลของหน่วยความจำในแอปพลิเคชันของคุณ

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ไข |
|-------|--------|-----------|
| **ไม่พบ `VmskResource`** | ไฟล์ PSD ไม่มีเลเยอร์ vector mask | ตรวจสอบให้แน่ใจว่า PSD ต้นฉบับมี vector mask หรือเพิ่ม mask ด้วย Photoshop ก่อนรันโค้ด |
| **`ArrayIndexOutOfBoundsException` ขณะเข้าถึง path** | จำนวนบันทึก Path ที่คาดไม่ตรง | ตรวจสอบ `resource.getPaths().length` แล้วปรับการใช้ดัชนีให้สอดคล้อง |
| **License exception** | รันโดยไม่มีลิขสิทธิ์ Aspose.PSD ที่ถูกต้อง | ใช้ลิขสิทธิ์ทดลองหรือซื้อโดยเพิ่มโค้ด `License license = new License(); license.setLicense("Aspose.PSD.lic");` |
| **Memory leak** | ไม่ได้ทำ `dispose()` ในกระบวนการที่ทำงานต่อเนื่อง | เรียก `im.dispose()` ในบล็อก `finally` หรือใช้ try‑with‑resources หากรองรับ |

## คำถามที่พบบ่อย

**ถาม: จะเพิ่ม vector mask ใหม่ให้กับเลเยอร์ที่มีอยู่ได้อย่างไร?**  
ตอบ: สร้าง `VmskResource` เติมบันทึก Path ที่ต้องการ (เช่น `BezierKnotRecord`) แล้วแนบลงในคอลเลกชัน resources ของเลเยอร์

**ถาม: สามารถแปลง PSD ที่แก้ไขแล้วเป็น PNG ได้โดยไม่ต้องเปิด Photoshop หรือไม่?**  
ตอบ: ได้—บันทึก PSD แล้วโหลดอีกครั้งด้วย `Image.load()` และเรียก `im.save("output.png")` พร้อมระบุฟอร์แมต PNG

**ถาม: มีวิธีทำอัตโนมัติใน pipeline CI/CD หรือไม่?**  
ตอบ: แน่นอน เนื่องจากกระบวนการเป็น Java เพียว ๆ สามารถฝังลงใน build ของ Maven/Gradle, Docker container หรือระบบ CI ใด ๆ ที่รองรับ Java

**ถาม: เวอร์ชันของ Aspose.PSD ใดที่เข้ากันได้กับ Java 11+?**  
ตอบ: ทุกเวอร์ชันล่าสุด (2024‑2025) รองรับ Java 8 ขึ้นไป รวมถึง Java 11, 17 และ LTS เวอร์ชันใหม่ ๆ

**ถาม: จำเป็นต้องมีลิขสิทธิ์สำหรับการพัฒนาแบบ build‑dev หรือไม่?**  
ตอบ: ลิขสิทธิ์ประเมินฟรีใช้ได้สำหรับการพัฒนาและทดสอบ ส่วนการใช้งานในผลิตภัณฑ์ต้องมีลิขสิทธิ์เชิงพาณิชย์

---

**อัปเดตล่าสุด:** 2026-02-22  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}