---
date: 2025-12-18
description: เรียนรู้วิธีสร้างเวกเตอร์มาสก์ (ทรัพยากร Vmsk) ในไฟล์ PSD ด้วย Aspose.PSD
  สำหรับ Java บทเรียนทีละขั้นตอนนี้จะแสดงวิธีเพิ่มเวกเตอร์มาสก์, แปลง PSD เป็น PNG,
  และอื่น ๆ อีกมากมาย
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: สร้างมาสก์เวกเตอร์ (ทรัพยากร Vmsk) ในไฟล์ PSD ด้วย Java
url: /th/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง Vector Mask (Vmsk Resource) ในไฟล์ PSD ด้วย Java

## การแนะนำ
คุณสมบัติ ** สร้าง vector mask** (Vmsk) ภายในไฟล์ Photoshop (PSD) Aspose.PSD สำหรับ Java จะนำเสนอโปรแกรมสะอาดในโปรแกรมเมทัลลิก เทคโนโลยีกำลังสร้างการออกแบบเครื่องมืออัตโนมัติหรือเพิ่มประสิทธิภาพของมาส์ก ให้กับไปป์ไลน์การไหลของความร้อนแล้ว ให้คุณใช้พาคุณผ่านทุกขั้นตอน— จากนั้น PSD, ทรัพยากร Vmsk, คุณสมบัติ, และการวิจัยผลลัพธ์ หากต้องการทราบถึงการจัดการ vector mask, PSD เป็น PNG, และจะกล่าวถึงไฟล์ด้วยข้อมูลเพิ่มเติม

## คำตอบด่วน
- **ทรัพยากร Vmsk คืออะไร?** เป็นข้อมูลเวกเตอร์มาสก์ที่เก็บไว้ในไฟล์ PSD, กำหนดการของโปรแกรมสำหรับคืนนี้
- **ไลบรารีใดรองรับ?** Aspose.PSD สำหรับ Java ไม่ต้องอ่าน/เขียนทรัพยากร Vmsk ตามที่กล่าวไว้
- **ต้องมีลิขสิทธิ์หรือไม่?** มีรุ่นทดลองฟรี; จะต้องมีลิขสิทธิ์เพื่อการนี้ในผลิตภัณฑ์
- **สามารถแปลง PSD ที่แก้ไขแล้วเป็น PNG ได้หรือไม่** ได้— บันทึกแล้วโหลด PSD อีกครั้งและส่งออกเป็น PNG ด้วย API เดียวกัน
- ** รองรับ Maven อย่างเป็นทางการ?** รองรับ; คีย์บอร์ด Aspose.PSD เป็นการพึ่งพาของ Maven (ดูคีย์การเดินทาง “aspose psd maven”)

## Vector Mask (ทรัพยากร Vmsk) คืออะไร
Vector mask (Vmsk) คือหน้ากากที่ไม่ต้องใช้ส่วนประกอบ Bézier และบันทึกเส้นทางเพื่อกำหนดพื้นที่บางส่วนและทึบบนร่างกาย อาจเป็นสัญญาณการขยายได้โดยไม่ต้องใช้คุณภาพ—สำหรับกราฟิกความละเอียดสูง

## เหตุใดจึงต้องสร้าง Vector Mask ด้วย Aspose.PSD
- **ระบบอัตโนมัติ:**ไม่จำเป็นต้องหรือแก้ไขมาสก์ผ่านโปรแกรมก็สามารถเปิด Photoshop ได้
- **ความสม่ำเสมอ:** ไม่ต้องใช้ PSD ทุกอันที่คุณสร้างการปฏิบัติตามกฎหน้ากากเดียวกัน
- **ข้ามแพลตฟอร์ม:** ทำงานบน OS รองรับ Java
- **Integration:** เรากับ Aspose API (อื่นๆ เช่น ไฟล์ PSD→PNG) สร้างเวิร์กโฟลว์ครบวงจร

## ข้อกำหนดเบื้องต้น
ในที่สุดเราจะลงลึกในโค้ด, ภาพถ่ายที่คุณรู้เรื่องราวนี้:

### สิ่งที่คุณต้องการ
- Java Development Kit (JDK): ฟังการติดตั้ง JDK บนเครื่องของคุณแล้ว. ดาวน์โหลดได้ฟรีจาก [เว็บไซต์ Oracle](https://www.oracle.com/java/technologies/javase-downloads.html)
- Aspose.PSD สำหรับ Java Library: ไลบรารีสำหรับจัดการไฟล์ PSD ดาวน์โหลดได้จาก [หน้าเผยแพร่ Aspose](https://releases.aspose.com/psd/java/) สำหรับผู้ที่ต้องการลองก่อนซื้อก็สามารถทำได้ [ทดลองใช้ฟรี](https://releases.aspose.com/)
- IDE: IDE สำหรับ Java สำหรับ Java (เช่น IntelliJ IDEA, Eclipse, ฯลฯ) จะสามารถโปรเจกต์ได้

### การตั้งค่าพื้นที่ทำงานของคุณ
1. **Create a New Java Project** – เปิด IDE โปรดดูโปรเจกต์ใหม่
2. **Add the Aspose Library** – หลังจากนั้นไม่นาน JAR ของ Aspose, และต่อเนื่อง build path ของโปรเจกต์เพื่อให้เข้าถึงคลาสคลาสได้ PSD ได้.

ในการเตรียมการเตรียมการ, ไปต่อที่การทำงานจริงกัน.

## วิธีสร้างเวกเตอร์มาสก์ในไฟล์ PSD ด้วย Java
ต่อไปเป็นคำแนะนำแบบขั้นตอน โค้ดบล็อกจะคงไว้ตามต้นฉบับ; เราเพียงเพิ่มข้อความอธิบายในแต่ละขั้นตอนที่ชัดเจนยิ่งขึ้น

## แพคเกจนำเข้า
เราจะมาพร้อมกับไฟล์ PSD, เราต้องนำเข้าคลาสจากไลบรารี Aspose.PSD.

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

ตอนนี้เราได้เตรียมพื้นฐานแล้ว, ไปสำรวจแต่ละการดำเนินการกัน.

## ขั้นตอนที่ 1: โหลดไฟล์ PSD ของคุณ
สิ่งแรกที่คุณต้องทำคือโหลดไฟล์ PSD ของคุณ. นี่คือจุดเริ่มต้นของทุกอย่าง.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- เรากำหนด `dataDir` ให้เป็นไดเรกทอรีของไฟล์ PSD.  
- เราสร้างสตริง `sourceFileName` โดยรวมไดเรกทอรีกับชื่อไฟล์ PSD.  
- สุดท้ายเราจะโหลดไฟล์ PSD เข้าไปในอ็อบเจกต์ `PsdImage` ด้วย `Image.load()`.

## ขั้นตอนที่ 2: ดึงข้อมูลทรัพยากร Vmsk
เมื่อเราโหลดภาพ PSD แล้ว, ให้ดึง Vmsk resource ออกมา.

```java
VmskResource resource = getVmskResource(im);
```

- เราเรียกเมธอด `getVmskResource()` ซึ่งทำหน้าที่ค้นหาและดึง Vmsk resource จากภาพ.

## ขั้นตอนที่ 3: ตรวจสอบความถูกต้องของคุณสมบัติทรัพยากร Vmsk
ก่อนดำเนินการแก้ไข, จำเป็นต้องตรวจสอบว่า Vmsk resource อยู่ในสถานะที่คาดหวังหรือไม่.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- ที่นี่เราตรวจสอบคุณสมบัติต่าง ๆ ของ Vmsk resource เพื่อให้แน่ใจว่าไม่ได้ถูกปิดใช้งาน, กลับด้าน, หรือไม่ได้เชื่อมโยง, และมีจำนวนเส้นทางที่ถูกต้อง.

## ขั้นตอนที่ 4: เข้าถึงแต่ละเส้นทางและตรวจสอบความถูกต้อง
ให้เราลงลึกและตรวจสอบเส้นทางภายใน Vmsk resource.

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

- เราดึงบันทึกเส้นทางสามรายการที่เฉพาะเจาะจงและตรวจสอบประเภทและคุณสมบัติของพวกมันเพื่อให้ตรงตามเกณฑ์ของเรา.

## ขั้นตอนที่ 5: แก้ไขทรัพยากร Vmsk
ตอนนี้เราจะเข้าสู่ขั้นตอนการแก้ไข! คุณสามารถปรับคุณสมบัติของ Vmsk resource ตามต้องการ.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- ในบล็อกนี้เราจะสลับคุณสมบัติต่าง ๆ ของ Vmsk resource. การตั้งค่าเป็น `true` จะควบคุมพฤติกรรมของ mask ในไฟล์ PSD.

## ขั้นตอนที่ 6: ปรับเปลี่ยนจุดปมเบซิเยร์
จุด Knot ของ Bézier มีความสำคัญต่อเส้นทางเวกเตอร์. เรามาเปลี่ยนค่าบางส่วนกัน.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- เราเข้าถึง `BezierKnotRecord` เฉพาะและเปลี่ยนจุดของมันเพื่อปรับรูปร่างของ vector mask.

## ขั้นตอนที่ 7: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
เมื่อแก้ไขทั้งหมดเสร็จ, ถึงเวลาบันทึกไฟล์ PSD ที่แก้ไขแล้ว.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- เรากำหนดเส้นทางสำหรับไฟล์ PSD ที่ส่งออกแล้วและเรียก `im.save()` เพื่อเขียนการเปลี่ยนแปลงลงไฟล์ใหม่.

## ขั้นตอนที่ 8: จัดเก็บและจัดการทรัพยากรให้เรียบร้อย
สุดท้าย, เราต้องแน่ใจว่าได้ทำการกำจัดอ็อบเจกต์ภาพเพื่อคืนทรัพยากร.

```java
im.dispose();
```

- การกำจัดทรัพยากรหลังการใช้งานเป็นแนวปฏิบัติที่ดีเพื่อหลีกเลี่ยงการรั่วของหน่วยความจำในแอปพลิเคชันของคุณ.

## บทสรุป
ขอแสดงความยินดี! คุณเพิ่งผ่านกระบวนการโดยละเอียดของการ **สร้าง vector mask** (Vmsk) ในไฟล์ PSD ด้วย Aspose.PSD for Java. ตั้งแต่การโหลดภาพ, ดึงและตรวจสอบ Vmsk resource, แก้ไขคุณสมบัติ, จนถึงการบันทึก PSD ที่แก้ไขแล้ว, คุณมีพื้นฐานที่มั่นคงสำหรับการทำงานอัตโนมัติของ vector mask. ใช้เทคนิคเหล่านี้เพื่อเสริม pipeline การออกแบบของคุณ, ผสานกับ Aspose API อื่น (เช่น การแปลง PSD เป็น PNG), หรือสร้างเครื่องมือกราฟิกแบบกำหนดเอง.

## คำถามที่พบบ่อย
**ถาม: ฉันจะเพิ่มเวกเตอร์มาสก์ใหม่ลงในเลเยอร์ที่มีอยู่ได้อย่างไร**
ตอบ: สร้าง `VmskResource`, เติมข้อมูลบันทึกเส้นทางที่ต้องการ (เช่น `BezierKnotRecord`), จากนั้นแนบมาเบาๆ ทรัพยากรของฮ่องกง

**ถาม: ฉันสามารถแปลง PSD ที่แก้ไขแล้วเป็น PNG โดยตรงโดยไม่ต้องเปิด Photoshop ได้หรือไม่**
ตอบ: ได้หลังจากบันทึก PSD อ่านอีกครั้งด้วย `Image.load()` และเรียก `im.save("output.png")` พร้อมระบุฟอร์แมต PNG

**ถาม: มีวิธีดำเนินการอัตโนมัติในไปป์ไลน์ CI/CD หรือไม่**
A: แน่นอน. ไม่จำเป็นต้องเป็น Java ธรรมดา, ไม่เคยฝังไว้อย่างนั้น Maven/Gradle, คอนเทนเนอร์ Docker, หรือระบบ CI ใด ๆ ที่เข้ากันได้กับ Java

**ถาม: Aspose.PSD เวอร์ชันใดบ้างที่เข้ากันได้กับ Java 11+**
A: และทั้งหมด (2024-2025) กับ Java 8 ขึ้นไป, และ Java 11, 17, และ LTS และอีกมากมาย.

**ถาม: ฉันต้องมีใบอนุญาตสำหรับรุ่นพัฒนาหรือไม่**
ตอบ: ตรวจประเมินฟรีสามารถใช้ได้สำหรับการพัฒนาและทดสอบ ในผลิตภัณฑ์ที่แท้จริง, ตลอดเวลานั้น.

---

**อัปเดตล่าสุด:** 18-12-2568
**ทดสอบด้วย:** Aspose.PSD 24.11 สำหรับ Java
**ผู้เขียน:** สมมติ 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
