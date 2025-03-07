---
title: ครอบตัดรูปภาพตามกะใน Aspose.PSD สำหรับ Java
linktitle: ครอบตัดรูปภาพตามกะ
second_title: Aspose.PSD Java API
description: ต้นแบบการครอบตัดรูปภาพด้วย Aspose.PSD สำหรับ Java บทช่วยสอนที่ครอบคลุมสำหรับการปรับแต่งภาพที่ราบรื่น
weight: 16
url: /th/java/image-editing/crop-image-by-shifts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ครอบตัดรูปภาพตามกะใน Aspose.PSD สำหรับ Java

## การแนะนำ

ในขอบเขตของการประมวลผลภาพบน Java Aspose.PSD มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับจัดการและปรับปรุงรูปภาพด้วยความแม่นยำสูงสุด หนึ่งในคุณสมบัติหลักที่ทำให้ Aspose.PSD แตกต่างคือความสามารถในการครอบตัดรูปภาพได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะเจาะลึกศิลปะของการครอบตัดรูปภาพโดยใช้ Aspose.PSD สำหรับ Java ในตอนท้าย คุณจะมีทักษะในการครอบตัดรูปภาพตามข้อกำหนดของคุณได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นการเดินทางอันน่าตื่นเต้นนี้ โปรดตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นที่จำเป็น:

### ชุดพัฒนาจาวา (JDK)

 ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK เวอร์ชันล่าสุดบนระบบของคุณ คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD สำหรับไลบรารี Java

 ในการเริ่มต้น คุณจะต้องมี Aspose.PSD สำหรับไลบรารี Java มุ่งหน้าไปที่[หน้าดาวน์โหลด](https://releases.aspose.com/psd/java/) และคว้าเวอร์ชันล่าสุด

### สภาพแวดล้อมการพัฒนาแบบบูรณาการ (IDE)

เลือก Java IDE ที่คุณชื่นชอบ เช่น Eclipse หรือ IntelliJ เพื่อประสบการณ์การเขียนโค้ดที่ราบรื่น

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นเพื่อเริ่มกระบวนการครอบตัดรูปภาพ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการครอบตัดรูปภาพโดยใช้ Aspose.PSD สำหรับ Java ออกเป็นขั้นตอนง่ายๆ ดังต่อไปนี้:

## ขั้นตอนที่ 1: โหลดรูปภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของคลาส RasterImage
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

## ขั้นตอนที่ 2: ข้อมูลรูปภาพแคช

ก่อนที่จะครอบตัด ขอแนะนำให้แคชข้อมูลรูปภาพเพื่อประสิทธิภาพที่ดีขึ้น:

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

## ขั้นตอนที่ 3: กำหนดค่า Shift

ระบุค่าการเปลี่ยนแปลงสำหรับทั้งสี่ด้านของรูปภาพ:

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## ขั้นตอนที่ 4: ใช้การครอบตัด

 ขึ้นอยู่กับค่าการเปลี่ยนแปลงที่กำหนดไว้ ให้ใช้การครอบตัดบนรูปภาพโดยใช้`crop` วิธี:

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

บันทึกภาพที่ครอบตัดลงดิสก์ด้วยรูปแบบที่ต้องการ ในกรณีนี้คือ JPEG:

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

ยินดีด้วย! คุณครอบตัดรูปภาพโดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจความซับซ้อนของการครอบตัดรูปภาพด้วย Aspose.PSD สำหรับ Java ด้วยความรู้นี้ คุณสามารถผสานรวมการครอบตัดรูปภาพเข้ากับโปรเจ็กต์ Java ของคุณได้อย่างราบรื่น เพิ่มความประณีตให้กับความสามารถในการประมวลผลรูปภาพของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับรูปแบบภาพทุกรูปแบบหรือไม่

ตอบ 1: ใช่ Aspose.PSD รองรับรูปแบบภาพที่หลากหลาย ช่วยให้มั่นใจได้ถึงความคล่องตัวในโครงการของคุณ

### คำถามที่ 2: ฉันสามารถใช้การครอบตัดหลายรายการกับรูปภาพเดียวกันได้หรือไม่

คำตอบ 2: แน่นอน คุณสามารถทำการครอบตัดหลายรายการตามลำดับบนรูปภาพเดียวกันได้

### คำถามที่ 3: มีฟอรัมชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่

 A3: ได้ คุณสามารถรับการสนับสนุนและมีส่วนร่วมกับชุมชนได้ที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A4: เยี่ยมเลย[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อขอรับใบอนุญาตชั่วคราว

### คำถามที่ 5: มีโปรเจ็กต์ตัวอย่างที่แสดงฟังก์ชัน Aspose.PSD หรือไม่

 A5: สำรวจเอกสารและตัวอย่างได้ที่[เอกสาร Java Aspose.PSD](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
