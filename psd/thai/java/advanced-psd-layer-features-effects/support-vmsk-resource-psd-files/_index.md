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

## Introduction
หากคุณต้องการ **สร้าง vector mask** (Vmsk) ภายในไฟล์ Photoshop (PSD) Aspose.PSD for Java จะมอบวิธีการที่สะอาดและเป็นโปรแกรมเมติกให้คุณ ไม่ว่าคุณจะกำลังสร้างเครื่องมือการออกแบบอัตโนมัติหรือเพิ่มการสนับสนุน mask แบบกำหนดเองให้กับ pipeline กราฟิกที่มีอยู่แล้ว บทเรียนนี้จะพาคุณผ่านทุกขั้นตอน—การโหลด PSD, การอ่าน Vmsk resource, การปรับแต่งคุณสมบัติ, และการบันทึกผลลัพธ์. เมื่อเสร็จสิ้น คุณจะคุ้นเคยกับการจัดการ vector mask, การแปลง PSD เป็น PNG, และการขยายไฟล์ด้วยข้อมูลเวกเตอร์เพิ่มเติม.

## Quick Answers
- **Vmsk resource คืออะไร?** เป็นข้อมูล vector mask ที่เก็บอยู่ในไฟล์ PSD, กำหนดรูปทรงเวกเตอร์ซับซ้อนสำหรับเลเยอร์.  
- **ไลบรารีใดรองรับ?** Aspose.PSD for Java ให้การเข้าถึงอ่าน/เขียน Vmsk resource อย่างเต็มรูปแบบ.  
- **ต้องมีลิขสิทธิ์หรือไม่?** มีรุ่นทดลองฟรี; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์.  
- **สามารถแปลง PSD ที่แก้ไขแล้วเป็น PNG ได้หรือไม่?** ได้—บันทึกแล้วคุณสามารถโหลด PSD อีกครั้งและส่งออกเป็น PNG ด้วย API เดียวกัน.  
- **รองรับ Maven หรือไม่?** แน่นอน; สามารถเพิ่ม Aspose.PSD เป็น dependency ของ Maven (ดูคีย์เวิร์ด “aspose psd maven”).

## What is a Vector Mask (Vmsk Resource)?
Vector mask (Vmsk) คือ mask ที่ไม่อิงพิกเซล ใช้เส้นโค้ง Bézier และบันทึกเส้นทางเพื่อกำหนดพื้นที่โปร่งใสและทึบบนเลเยอร์. เนื่องจากเป็นเวกเตอร์ มันสามารถขยายได้โดยไม่สูญเสียคุณภาพ—เหมาะสำหรับกราฟิกความละเอียดสูง.

## Why Create a Vector Mask with Aspose.PSD?
- **Automation:** เพิ่มหรือแก้ไข mask ผ่านโปรแกรมโดยไม่ต้องเปิด Photoshop.  
- **Consistency:** ทำให้ทุก PSD ที่คุณสร้างปฏิบัติตามกฎ mask เดียวกัน.  
- **Cross‑platform:** ทำงานบน OS ใดก็ได้ที่รองรับ Java.  
- **Integration:** ผสานกับ Aspose API อื่น (เช่น แปลง PSD → PNG) เพื่อสร้าง workflow ครบวงจร.

## Prerequisites
ก่อนที่เราจะลงลึกในโค้ด, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

### What You Need
- Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว. หากยังไม่มี, คุณสามารถดาวน์โหลดได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- Aspose.PSD for Java Library: ไลบรารีที่ทรงพลังสำหรับจัดการไฟล์ PSD. ดาวน์โหลดได้จาก [Aspose release page](https://releases.aspose.com/psd/java/). สำหรับผู้ที่ต้องการลองก่อนซื้อ, สามารถเริ่มต้นด้วย [free trial](https://releases.aspose.com/).  
- An IDE: IDE ใดก็ได้สำหรับ Java (เช่น IntelliJ IDEA, Eclipse, ฯลฯ) จะทำงานกับโปรเจกต์นี้ได้.

### Setting Up Your Workspace
1. **Create a New Java Project** – เปิด IDE ที่คุณชื่นชอบและสร้างโปรเจกต์ใหม่.  
2. **Add the Aspose Library** – หลังจากดาวน์โหลดไฟล์ JAR ของ Aspose, เพิ่มเข้าไปใน build path ของโปรเจกต์เพื่อให้เข้าถึงคลาสที่เกี่ยวกับ PSD ได้.

เมื่อเตรียมสภาพแวดล้อมเรียบร้อย, ไปต่อที่การทำงานจริงกัน.

## How to create vector mask in PSD files with Java
ต่อไปนี้เป็นคำแนะนำแบบขั้นตอน. โค้ดบล็อกจะคงไว้ตามต้นฉบับ; เราเพียงเพิ่มข้อความอธิบายเพื่อทำให้แต่ละขั้นตอนชัดเจนยิ่งขึ้น.

## Import Packages
ก่อนที่เราจะทำงานกับไฟล์ PSD, เราต้องนำเข้าคลาสที่จำเป็นจากไลบรารี Aspose.PSD.

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

## Step 1: Load Your PSD File
สิ่งแรกที่คุณต้องทำคือโหลดไฟล์ PSD ของคุณ. นี่คือจุดเริ่มต้นของทุกอย่าง.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- เรากำหนด `dataDir` ให้เป็นไดเรกทอรีของไฟล์ PSD.  
- เราสร้างสตริง `sourceFileName` โดยรวมไดเรกทอรีกับชื่อไฟล์ PSD.  
- สุดท้ายเราจะโหลดไฟล์ PSD เข้าไปในอ็อบเจกต์ `PsdImage` ด้วย `Image.load()`.

## Step 2: Retrieve the Vmsk Resource
เมื่อเราโหลดภาพ PSD แล้ว, ให้ดึง Vmsk resource ออกมา.

```java
VmskResource resource = getVmskResource(im);
```

- เราเรียกเมธอด `getVmskResource()` ซึ่งทำหน้าที่ค้นหาและดึง Vmsk resource จากภาพ.

## Step 3: Validate Vmsk Resource Properties
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

## Step 4: Access Each Path and Validate
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

## Step 5: Edit the Vmsk Resource
ตอนนี้เราจะเข้าสู่ขั้นตอนการแก้ไข! คุณสามารถปรับคุณสมบัติของ Vmsk resource ตามต้องการ.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- ในบล็อกนี้เราจะสลับคุณสมบัติต่าง ๆ ของ Vmsk resource. การตั้งค่าเป็น `true` จะควบคุมพฤติกรรมของ mask ในไฟล์ PSD.

## Step 6: Modify the Bezier Knot Points
จุด Knot ของ Bézier มีความสำคัญต่อเส้นทางเวกเตอร์. เรามาเปลี่ยนค่าบางส่วนกัน.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- เราเข้าถึง `BezierKnotRecord` เฉพาะและเปลี่ยนจุดของมันเพื่อปรับรูปร่างของ vector mask.

## Step 7: Save the Modified PSD File
เมื่อแก้ไขทั้งหมดเสร็จ, ถึงเวลาบันทึกไฟล์ PSD ที่แก้ไขแล้ว.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- เรากำหนดเส้นทางสำหรับไฟล์ PSD ที่ส่งออกแล้วและเรียก `im.save()` เพื่อเขียนการเปลี่ยนแปลงลงไฟล์ใหม่.

## Step 8: Clean Up Resources
สุดท้าย, เราต้องแน่ใจว่าได้ทำการกำจัดอ็อบเจกต์ภาพเพื่อคืนทรัพยากร.

```java
im.dispose();
```

- การกำจัดทรัพยากรหลังการใช้งานเป็นแนวปฏิบัติที่ดีเพื่อหลีกเลี่ยงการรั่วของหน่วยความจำในแอปพลิเคชันของคุณ.

## Conclusion
ขอแสดงความยินดี! คุณเพิ่งผ่านกระบวนการโดยละเอียดของการ **สร้าง vector mask** (Vmsk) ในไฟล์ PSD ด้วย Aspose.PSD for Java. ตั้งแต่การโหลดภาพ, ดึงและตรวจสอบ Vmsk resource, แก้ไขคุณสมบัติ, จนถึงการบันทึก PSD ที่แก้ไขแล้ว, คุณมีพื้นฐานที่มั่นคงสำหรับการทำงานอัตโนมัติของ vector mask. ใช้เทคนิคเหล่านี้เพื่อเสริม pipeline การออกแบบของคุณ, ผสานกับ Aspose API อื่น (เช่น การแปลง PSD เป็น PNG), หรือสร้างเครื่องมือกราฟิกแบบกำหนดเอง.

## FAQ's
### What is a Vmsk resource?
Vmsk resource คือ vector mask ในไฟล์ PSD ที่อนุญาตให้สร้างรูปทรงเวกเตอร์ซับซ้อนและคุณสมบัติการแก้ไขได้.

### Can I use Aspose.PSD in a Maven project?
ได้, คุณสามารถเพิ่ม Aspose.PSD เป็น dependency ในโปรเจกต์ Maven ของคุณโดยใช้พิกัดจาก repository.

### What format can I save my modified PSD files in?
คุณสามารถบันทึกเป็นไฟล์ PSD อีกครั้งหรือส่งออกเป็นฟอร์แมตอื่น ๆ เช่น PNG, JPEG ฯลฯ.

### Is there a free trial available for Aspose.PSD?
ใช่, คุณสามารถเข้าถึงรุ่นทดลองฟรีของ Aspose.PSD เพื่อทดสอบฟีเจอร์ต่าง ๆ. เยี่ยมชม [free trial link](https://releases.aspose.com/).

### How can I get support for Aspose.PSD?
คุณสามารถเข้าร่วม [Aspose forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนและความช่วยเหลือในการแก้ปัญหา.

## Frequently Asked Questions
**Q: How do I add a new vector mask to an existing layer?**  
A: สร้าง `VmskResource`, เติมข้อมูลบันทึกเส้นทางที่ต้องการ (เช่น `BezierKnotRecord`), แล้วแนบเข้ากับคอลเลกชัน resources ของเลเยอร์.

**Q: Can I convert the edited PSD directly to PNG without opening Photoshop?**  
A: ได้—หลังจากบันทึก PSD, โหลดอีกครั้งด้วย `Image.load()` และเรียก `im.save("output.png")` พร้อมระบุฟอร์แมต PNG.

**Q: Is there a way to automate this in a CI/CD pipeline?**  
A: แน่นอน. เนื่องจากกระบวนการเป็น Java ธรรมดา, คุณสามารถฝังไว้ในการสร้าง Maven/Gradle, คอนเทนเนอร์ Docker, หรือระบบ CI ใด ๆ ที่รองรับ Java.

**Q: What versions of Aspose.PSD are compatible with Java 11+?**  
A: รุ่นล่าสุดทั้งหมด (2024‑2025) รองรับ Java 8 ขึ้นไป, รวมถึง Java 11, 17, และ LTS เวอร์ชันใหม่ ๆ.

**Q: Do I need a license for development builds?**  
A: ใบอนุญาตประเมินฟรีใช้ได้สำหรับการพัฒนาและทดสอบ. สำหรับการใช้งานในผลิตภัณฑ์จริง, จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

---