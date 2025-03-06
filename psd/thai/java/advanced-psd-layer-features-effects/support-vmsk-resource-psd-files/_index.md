---
title: รองรับทรัพยากร Vmsk ในไฟล์ PSD ด้วย Java
linktitle: รองรับทรัพยากร Vmsk ในไฟล์ PSD ด้วย Java
second_title: Aspose.PSD Java API
description: จัดการทรัพยากร Vmsk ในไฟล์ PSD ได้อย่างง่ายดายโดยใช้ Aspose.PSD สำหรับ Java บทช่วยสอนแบบทีละขั้นตอนที่ครอบคลุมซึ่งเหมาะสำหรับนักพัฒนาและนักออกแบบ
weight: 23
url: /th/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับทรัพยากร Vmsk ในไฟล์ PSD ด้วย Java

## การแนะนำ
เมื่อพูดถึงการทำงานกับไฟล์ PSD (เอกสาร Photoshop) การจัดการทรัพยากรเป็นสิ่งสำคัญ โดยเฉพาะอย่างยิ่งเมื่อรวมคุณสมบัติพิเศษ เช่น ทรัพยากร Vmsk (Vector Mask) ทรัพยากรของ Vmsk สามารถเสริมพลังให้กับนักออกแบบโดยการเพิ่มรูปร่างเวกเตอร์ที่ซับซ้อน ช่วยให้พวกเขาสร้างกราฟิกที่น่าทึ่งได้อย่างง่ายดาย ในคู่มือนี้ เราจะใช้แนวทางปฏิบัติจริงเพื่อแสดงวิธีสนับสนุนทรัพยากร Vmsk ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาที่ต้องการปรับปรุงแอปพลิเคชันของคุณ หรือนักออกแบบที่กำลังมองหาระบบอัตโนมัติ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอน ทำให้ง่ายต่อการปฏิบัติตามและนำไปใช้
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกรายละเอียดที่สำคัญในการจัดการทรัพยากร Vmsk เรามาตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่พร้อมสำหรับประสบการณ์ที่ราบรื่น
### สิ่งที่คุณต้องการ
-  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ออราเคิล](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD สำหรับไลบรารี Java: นี่คือไลบรารีที่มีประสิทธิภาพสำหรับการจัดการไฟล์ PSD คุณสามารถดาวน์โหลดได้จาก[กำหนดหน้าเผยแพร่](https://releases.aspose.com/psd/java/) - สำหรับผู้ที่ต้องการทดลองใช้ก่อนซื้อคุณสามารถเริ่มต้นด้วย[ทดลองใช้ฟรี](https://releases.aspose.com/).
- IDE: IDE ใดๆ สำหรับ Java (เช่น IntelliJ IDEA, Eclipse ฯลฯ) จะใช้ได้กับโปรเจ็กต์นี้
### การตั้งค่าพื้นที่ทำงานของคุณ
1. สร้างโปรเจ็กต์ Java ใหม่: เริ่ม IDE ที่คุณต้องการและสร้างโปรเจ็กต์ Java ใหม่ นี่คือสนามเด็กเล่นของคุณสำหรับการทำงานกับโค้ด
2. เพิ่มไลบรารี Aspose: หลังจากดาวน์โหลดไลบรารี Aspose แล้ว ให้เพิ่มไฟล์ jar ลงในไลบรารีของโปรเจ็กต์ของคุณ ขั้นตอนนี้มีความสำคัญเนื่องจากช่วยให้เราสามารถใช้ฟีเจอร์หวานๆ ทั้งหมดของ Aspose.PSD ได้
ด้วยข้อกำหนดเบื้องต้นเหล่านี้ คุณก็พร้อมที่จะเริ่มสร้าง แก้ไข และจัดการไฟล์ PSD ด้วยทรัพยากร Vmsk มาเข้าสู่การเขียนโปรแกรมกันเถอะ!
## แพ็คเกจนำเข้า
ก่อนที่เราจะสามารถทำงานกับไฟล์ PSD ได้ เราจำเป็นต้องนำเข้าแพ็คเกจที่จำเป็นก่อน นี่คือแกนหลักของโค้ดของเรา ทำให้เราสามารถเข้าถึงคลาสและวิธีการต่างๆ ที่ไลบรารี Aspose.PSD นำเสนอ
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
ตอนนี้เราได้เตรียมเวทีแล้ว ก็ถึงเวลาลงมือ! ในส่วนนี้ เราจะแบ่งโค้ดออกเป็นขั้นตอนที่สามารถจัดการได้ ขั้นตอนเหล่านี้จะแนะนำคุณในการอ่านไฟล์ PSD การจัดการทรัพยากร Vmsk และแม้กระทั่งการแก้ไข
## ขั้นตอนที่ 1: โหลดไฟล์ PSD ของคุณ
สิ่งแรกที่คุณต้องการทำคือโหลดไฟล์ PSD ของคุณ นี่คือจุดเริ่มต้นของความมหัศจรรย์ทั้งหมด
```java
String dataDir = "Your Document Directory"; // อัพเดตเส้นทางนี้
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  เราตั้งค่า`dataDir` ไปยังไดเร็กทอรีของไฟล์ PSD ของคุณ 
-  เราสร้างสตริงสำหรับ`sourceFileName`การรวมไดเรกทอรีเข้ากับชื่อไฟล์ PSD
-  ในที่สุด เราก็โหลดไฟล์ PSD ลงในไฟล์`PsdImage` วัตถุที่ใช้`Image.load()`.
## ขั้นตอนที่ 2: ดึงข้อมูลทรัพยากร Vmsk
ตอนนี้เราได้โหลดรูปภาพ PSD แล้ว เรามาเรียกทรัพยากร Vmsk กันดีกว่า
```java
VmskResource resource = getVmskResource(im);
```

-  เราเรียกว่า`getVmskResource()` วิธีการซึ่งจัดการการค้นหาและการดึงข้อมูลทรัพยากร Vmsk จากรูปภาพ
## ขั้นตอนที่ 3: ตรวจสอบคุณสมบัติทรัพยากร Vmsk
ก่อนดำเนินการแก้ไข จำเป็นต้องตรวจสอบว่าทรัพยากร Vmsk ของเราอยู่ในสถานะที่คาดไว้
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- ที่นี่ เรากำลังตรวจสอบคุณสมบัติต่างๆ ของทรัพยากร Vmsk เราต้องการให้แน่ใจว่าไม่ได้ปิดการใช้งาน กลับด้าน หรือไม่เชื่อมโยง และมีจำนวนเส้นทางที่ถูกต้อง
## ขั้นตอนที่ 4: เข้าถึงแต่ละเส้นทางและตรวจสอบ
มาเจาะลึกลงไปอีกหน่อยและตรวจสอบเส้นทางภายในทรัพยากร Vmsk
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

- เรากำลังแยกบันทึกเส้นทางเฉพาะสามรายการและตรวจสอบประเภทและคุณสมบัติเพื่อให้แน่ใจว่าตรงตามเกณฑ์ของเรา
## ขั้นตอนที่ 5: แก้ไขทรัพยากร Vmsk
ตอนนี้เรากำลังเข้าสู่ส่วนการปรับเปลี่ยน! คุณสามารถปรับแต่งคุณสมบัติของทรัพยากร Vmsk ได้ตามต้องการ
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- ในบล็อกนี้ เรากำลังสลับคุณสมบัติต่างๆ ของทรัพยากร Vmsk ด้วยการตั้งค่าให้เป็น "จริง" เราจึงสามารถควบคุมลักษณะการทำงานของมาสก์ในไฟล์ PSD ได้
## ขั้นตอนที่ 6: แก้ไขคะแนน Bezier Knot
ปม Bezier มีความสำคัญอย่างยิ่งต่อเส้นทางเวกเตอร์ ลองเปลี่ยนค่าบางอย่างที่นี่
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  เรากำลังเข้าถึงเฉพาะ`BezierKnotRecord` เส้นทางและการเปลี่ยนจุดเพื่อสร้างรูปแบบเวกเตอร์มาสก์ใหม่
## ขั้นตอนที่ 7: บันทึกไฟล์ PSD ที่แก้ไข
เมื่อการแก้ไขทั้งหมดเสร็จสิ้น ก็ถึงเวลาบันทึกไฟล์ PSD ที่แก้ไข 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  เรากำหนดเส้นทางสำหรับไฟล์ PSD ที่ส่งออกแล้วจึงโทร`im.save()` เพื่อเขียนการเปลี่ยนแปลงในไฟล์ใหม่นี้
## ขั้นตอนที่ 8: ทำความสะอาดทรัพยากร
สุดท้ายนี้ เราต้องแน่ใจว่าเรากำจัดรูปภาพอย่างเหมาะสมเพื่อเพิ่มพื้นที่ว่าง
```java
im.dispose();
```

- ถือเป็นแนวปฏิบัติที่ดีเสมอในการกำจัดทรัพยากรใดๆ เมื่อคุณดำเนินการเสร็จแล้ว ซึ่งจะช่วยหลีกเลี่ยงการรั่วไหลของหน่วยความจำในแอปพลิเคชันของคุณ
## บทสรุป
ยินดีด้วย! คุณเพิ่งทำตามขั้นตอนโดยละเอียดในการสนับสนุนทรัพยากร Vmsk ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ตั้งแต่การโหลดรูปภาพ การดึงข้อมูลและตรวจสอบความถูกต้องของทรัพยากร Vmsk การแก้ไขคุณสมบัติของทรัพยากร จากนั้นบันทึก PSD ที่แก้ไขแล้ว คุณได้ครอบคลุมสิ่งสำคัญต่างๆ แล้ว ด้วยทักษะเหล่านี้ คุณสามารถจัดการและใช้ทรัพยากรต่างๆ ภายในไฟล์ PSD ได้อย่างมีประสิทธิภาพ เพิ่มประสิทธิภาพโครงการออกแบบกราฟิกหรือสคริปต์อัตโนมัติของคุณ
## คำถามที่พบบ่อย
### ทรัพยากร Vmsk คืออะไร
ทรัพยากร Vmsk คือมาสก์เวกเตอร์ในไฟล์ PSD ที่ช่วยให้สามารถใช้รูปร่างเวกเตอร์ที่ซับซ้อนและคุณสมบัติการแก้ไขได้
### ฉันสามารถใช้ Aspose.PSD ในโปรเจ็กต์ Maven ได้หรือไม่
ได้ คุณสามารถรวม Aspose.PSD เป็นการขึ้นต่อกันในโปรเจ็กต์ Maven ของคุณได้โดยใช้พิกัดจากพื้นที่เก็บข้อมูล
### ฉันสามารถบันทึกไฟล์ PSD ที่แก้ไขแล้วในรูปแบบใดได้บ้าง
คุณสามารถบันทึกกลับเป็นไฟล์ PSD หรือส่งออกเป็นรูปแบบอื่น เช่น PNG, JPEG เป็นต้น
### มีการทดลองใช้ฟรีสำหรับ Aspose.PSD หรือไม่
 ใช่ คุณสามารถเข้าถึง Aspose.PSD รุ่นทดลองใช้ฟรีเพื่อทดสอบคุณสมบัติของมัน เยี่ยมชม[ลิงค์ทดลองใช้ฟรี](https://releases.aspose.com/).
### ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร
 คุณสามารถเข้าร่วม[ฟอรั่ม Aspose](https://forum.aspose.com/c/psd/34)สำหรับการสนับสนุนและความช่วยเหลือในการแก้ไขปัญหา
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
