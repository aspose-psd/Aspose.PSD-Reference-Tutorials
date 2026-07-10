---
date: 2026-03-28
description: เรียนรู้วิธีปรับความสว่างของ PSD ด้วย Java โดยใช้ Aspose.PSD for Java
  รวมถึงวิธีเปลี่ยนความสว่างและคอนทราสต์ของเลเยอร์ PSD เหมาะสำหรับนักพัฒนาและนักออกแบบกราฟิก
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: ปรับความสว่าง PSD Java – จัดการความสว่างและคอนทราสต์
url: /th/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ปรับความสว่าง PSD Java – จัดการความสว่างและคอนทราสต์

## บทนำ

Are you a graphic designer or a developer who frequently works with PSD (Photoshop Document) files? Do you need to **adjust brightness psd java** quickly and reliably without leaving your Java environment? In this tutorial, we’ll show you exactly how to change PSD layer brightness and contrast using the Aspose.PSD library for Java. You’ll walk away with a reusable code snippet that can be integrated into any automated image‑processing pipeline. Let’s roll up our sleeves and get started!

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD for Java  
- **ฉันสามารถเปลี่ยนหลายเลเยอร์พร้อมกันได้หรือไม่?** ใช่ – ทำการวนซ้ำผ่านวัตถุ `BrightnessContrastLayer` ทั้งหมด.  
- **ต้องการเวอร์ชัน Java ใด?** JDK 8 หรือสูงกว่า.  
- **ต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** ใช่, จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่การประเมิน.  
- **โค้ดนี้เข้ากันได้กับโครงการ Maven/Gradle หรือไม่?** แน่นอน – เพียงเพิ่มการพึ่งพา Aspose.PSD.  

## “adjust brightness psd java” คืออะไร?

การปรับความสว่างในไฟล์ PSD ผ่าน Java หมายถึงการแก้ไขค่าของ `BrightnessContrastLayer` อย่างโปรแกรมเมติก, ซึ่งทำให้คุณสามารถอัตโนมัติการปรับแต่งภาพที่โดยปกติจะต้องทำด้วยมือใน Photoshop.

## ทำไมต้องปรับความสว่างและคอนทราสต์ในเลเยอร์ PSD?

- **เร่งการประมวลผลแบบกลุ่ม** – เหมาะสำหรับคลังงานออกแบบขนาดใหญ่.  
- **รักษาโครงสร้างเลเยอร์** – เฉพาะเลเยอร์การปรับที่ต้องการเท่านั้นที่ถูกแก้ไข, คงมาสก์และเอฟเฟกต์ไว้.  
- **รวมเข้ากับ pipeline CI/CD** – สร้างภาพตัวอย่างหรือภาพย่อโดยอัตโนมัติ.  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มการเดินทางที่น่าตื่นเต้นนี้ในการจัดการไฟล์ PSD ด้วย Java, จำเป็นต้องตรวจสอบว่าคุณได้เตรียมทุกอย่างอย่างถูกต้องแล้ว นี่คือสิ่งที่คุณต้องการเพื่อทำให้บทเรียนนี้สำเร็จ:

1. **Java Development Kit (JDK)** – ตรวจสอบว่าคุณมี JDK 8 หรือสูงกว่าติดตั้งบนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [เว็บไซต์ของ Oracle](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. **Aspose.PSD for Java Library** – เพื่อทำงานกับไฟล์ PSD, คุณจะต้องใช้ไลบรารี Aspose.PSD คุณสามารถดาวน์โหลดเวอร์ชันล่าสุดได้จาก [หน้ารีลีส](https://releases.aspose.com/psd/java/).

3. **IDE ที่คุณเลือก** – สภาพแวดล้อมการพัฒนาแบบบูรณาการ (IDE) เช่น IntelliJ IDEA, Eclipse หรือ NetBeans เป็นที่แนะนำสำหรับการเขียนและรันโค้ด Java ของคุณ.

4. **ความรู้พื้นฐานของ Java** – ความคุ้นเคยกับการเขียนโปรแกรม Java จะช่วยให้คุณเข้าใจโค้ดสแนปที่เราจะทำงานด้วย.

เมื่อคุณมีข้อกำหนดเบื้องต้นเหล่านี้ครบแล้ว, เราพร้อมที่จะดำเนินต่อไป ตอนนี้เปิดตัวแก้ไขโค้ดที่คุณชื่นชอบและเริ่มเขียนโค้ดกันเถอะ!

## นำเข้าแพ็กเกจ

ขั้นตอนแรกในเส้นทางการเขียนโค้ดของเราคือการนำเข้าแพ็กเกจที่จำเป็น ก่อนที่คุณจะใช้ฟังก์ชันที่ Aspose.PSD มีให้, คุณต้องแน่ใจว่าไลบรารีอยู่ใน classpath ของคุณ นี่คือวิธีทำ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

โดยการทำขั้นตอนเหล่านี้เสร็จ, คุณได้เตรียมพื้นฐานสำหรับการทำงานกับไฟล์ PSD อย่างมีประสิทธิภาพ!

เมื่อเราตั้งค่าทุกอย่างเรียบร้อยแล้ว, ถึงเวลาที่จะเข้าสู่หัวใจของบทเรียน: การปรับความสว่างและคอนทราสต์ในเลเยอร์ PSD เราจะแบ่งกระบวนการนี้เป็นขั้นตอนที่ชัดเจนเพื่อให้คุณสามารถทำตามได้ง่าย.

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสารของคุณ

เริ่มต้นโดยกำหนดไดเรกทอรีที่ไฟล์ PSD ของคุณอยู่ ขั้นตอนนี้ช่วยจัดระเบียบไฟล์ของคุณอย่างมีประสิทธิภาพ.

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธจริงของไดเรกทอรีไฟล์ PSD ของคุณ.

## ขั้นตอนที่ 2: ระบุชื่อไฟล์ต้นทางและปลายทาง

ต่อไป, คุณต้องระบุชื่อไฟล์ต้นทางของ PSD ของคุณและไฟล์ปลายทางที่ PSD ที่แก้ไขแล้วจะถูกบันทึก.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

ในตัวอย่างนี้, เรากำลังสมมติว่าคุณมีไฟล์ PSD ชื่อ `BrightnessContrastModern.psd` อยู่ในไดเรกทอรีของคุณ.

## ขั้นตอนที่ 3: โหลดไฟล์ PSD

ตอนนี้ถึงเวลาที่จะโหลดไฟล์ PSD เข้าสู่แอปพลิเคชันของคุณเพื่อให้คุณสามารถจัดการได้.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

บรรทัดโค้ดนี้สร้างอินสแตนซ์ของ `PsdImage` ที่แทนไฟล์ PSD ของคุณ ด้วยสิ่งนี้คุณสามารถเข้าถึงเลเยอร์ทั้งหมดของ PSD ได้แล้ว.

## ขั้นตอนที่ 4: วนซ้ำผ่านเลเยอร์

ขั้นตอนต่อไปคือการวนซ้ำผ่านแต่ละเลเยอร์ของไฟล์ PSD เพื่อค้นหาและจัดการการตั้งค่าความสว่างและคอนทราสต์.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

ลูป `for` จะวนผ่านแต่ละเลเยอร์ของ PSD เรากำลังตรวจสอบว่าเลเยอร์เป็นอินสแตนซ์ของ `BrightnessContrastLayer` หรือไม่ สิ่งนี้สำคัญเพื่อให้แน่ใจว่าคุณพยายามเปลี่ยนความสว่างของเลเยอร์ PSD เฉพาะที่ถูกต้อง.

## ขั้นตอนที่ 5: ปรับความสว่างและคอนทราสต์

ภายในลูป, คุณสามารถตั้งค่าความสว่างและคอนทราสต์สำหรับแต่ละ `BrightnessContrastLayer` ได้แล้ว.

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

ในตัวอย่างนี้, เราตั้งค่าความสว่างและคอนทราสต์เป็น `50` คุณสามารถปรับค่าตามความต้องการของคุณ ตัวเลขที่สูงขึ้นจะเพิ่มความสว่าง/คอนทราสต์, ส่วนตัวเลขที่ต่ำลงจะลดลง.

## ขั้นตอนที่ 6: บันทึกการเปลี่ยนแปลง

ขั้นตอนสุดท้ายคือการบันทึกการเปลี่ยนแปลงของคุณลงในไฟล์ PSD คุณต้องการเขียนภาพที่แก้ไขแล้วกลับไปยังปลายทางที่ระบุ.

```java
im.save(psdPathAfterChange);
```

บรรทัดโค้ดนี้บันทึกไฟล์ PSD ที่แก้ไขแล้วพร้อมการตั้งค่าความสว่างและคอนทราสต์ใหม่ของคุณ.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **ไม่พบ `BrightnessContrastLayer`** | PSD อาจใช้ประเภทการปรับอื่น (เช่น Levels). | ตรวจสอบประเภทของเลเยอร์หรือแปลงการปรับเป็น `BrightnessContrastLayer`. |
| **ไฟล์ที่บันทึกดูเหมือนเสียหาย** | ขาดไลเซนส์หรือใช้เวอร์ชัน Aspose.PSD ที่ล้าสมัย. | ใช้ไลเซนส์ที่ถูกต้องและตรวจสอบว่าคุณใช้เวอร์ชันไลบรารีล่าสุด. |
| **ค่านอกช่วง** | ค่าความสว่าง/คอนทราสต์ต้องอยู่ระหว่าง -100 ถึง 100. | จำกัดค่าก่อนเรียก `setBrightness`/`setContrast`. |

## คำถามที่พบบ่อย

**Q: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถจัดการไฟล์ PSD ด้วยโปรแกรม, ทำให้สามารถอัตโนมัติการทำงานที่เกี่ยวข้องกับ Photoshop ได้.

**Q: ฉันสามารถปรับความสว่างและคอนทราสต์ของหลายเลเยอร์พร้อมกันได้หรือไม่?**  
A: ได้, วิธีที่ใช้ในบทเรียนนี้จะวนซ้ำผ่านทุกเลเยอร์ใน PSD, ทำให้คุณสามารถปรับหลายอินสแตนซ์ของ `BrightnessContrastLayer` ได้.

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: คุณสามารถรับไลเซนส์ชั่วคราวโดยไปที่ [หน้าไลเซนส์ชั่วคราว](https://purchase.aspose.com/temporary-license/).

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.PSD หรือไม่?**  
A: มี, คุณสามารถดาวน์โหลดรุ่นทดลองฟรีของ Aspose.PSD จาก [หน้ารีลีส](https://releases.aspose.com/).

**Q: ฉันจะหาแนวทางสนับสนุนเพิ่มเติมสำหรับ Aspose.PSD ได้จากที่ไหน?**  
A: คุณสามารถรับการสนับสนุนสำหรับ Aspose.PSD ได้จาก [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/psd/34).

---

**อัปเดตล่าสุด:** 2026-03-28  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}