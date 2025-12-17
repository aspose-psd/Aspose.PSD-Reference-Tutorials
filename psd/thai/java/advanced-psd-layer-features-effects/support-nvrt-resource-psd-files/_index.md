---
date: 2025-12-17
description: Learn how to load PSD files in Java and read PSD layers while supporting
  the Nvrt resource using Aspose.PSD.
linktitle: Support Nvrt Resource in PSD Files using Java
second_title: Aspose.PSD Java API
title: How to Load PSD Files and Support Nvrt Resource using Java
url: /th/java/advanced-psd-layer-features-effects/support-nvrt-resource-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สนับสนุนทรัพยากร Nvrt ในไฟล์ PSD ด้วย Java

## วิธีโหลดไฟล์ PSD ด้วย Java
เมื่อคุณต้องการ **how to load psd** ไฟล์โดยโปรแกรม, Java มีระบบนิเวศที่แข็งแกร่ง—โดยเฉพาะกับไลบรารี Aspose.PSD ไม่ว่าคุณจะกำลังสร้างโปรแกรมแก้ไขกราฟิก, ทำอัตโนมัติขั้นตอนการออกแบบ, หรือสกัดทรัพยากรจากเอกสาร Photoshop, การเชี่ยวชาญการจัดการ PSD เป็นสิ่งสำคัญ ในบทแนะนำนี้เราจะอธิบายขั้นตอนการโหลด PSD, อ่านเยอร์ของมัน, และสนับสนุนทรัพยากร Nvrt (Invert Adjustment) อย่างเฉพาะเจาะจง

## คำตอบสั้น
- **ไลบรารีใดจัดการไฟล์ PSD ใน Java?** Aspose.PSD for Java  
- **ฉันสามารถอ่านเลเยอร์ของ PSD ได้หรือไม่?** Yes, the API provides full access to layer structures  
- **ต้องใช้ใบอนุญาตสำหรับการผลิตหรือไม่?** Yes, a commercial license is needed  
- **เวอร์ชัน JDK ที่รองรับคืออะไร?** Java 8 and higher  
- **สามารถดาวน์โหลดไลบรารีได้จากที่ไหน?** From the official Aspose download page  

## ข้อกำหนดเบื้องต้น
ก่อนที่คุณจะเริ่มเขียนโค้ด, ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- **Java Development Kit (JDK)** ติดตั้งแล้ว (แนะนำ Java 8+ )  
- **An IDE** เช่น IntelliJ IDEA, Eclipse หรือ VS Code  
- **Aspose.PSD for Java** library – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ: [Download Aspose.PSD for Java](https://releases.aspose.com/psd/java/)  
- **Basic Java knowledge** (คลาส, อ็อบเจ็กต์, การจัดการข้อยกเว้น)  

## นำเข้าแพ็กเกจ
เมื่อสภาพแวดล้อมของคุณพร้อม, ให้นำเข้าคลาสที่จำเป็น. สิ่งเหล่านี้จะให้คุณเข้าถึงการจัดการ PSD, การเดินทางผ่านเลเยอร์, และทรัพยากร Nvrt

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.InvertAdjustmentLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.NvrtResource;
```

## ทำไมต้องอ่านเลเยอร์ของ PSD?
การอ่านเลเยอร์ของ PSD ทำให้คุณสามารถ:

- สกัดทรัพยากรแต่ละชิ้น (เช่น ไอคอน, มาสก์) เพื่อใช้งานซ้ำ  
- วิเคราะห์เลเยอร์ปรับค่า (เช่น **Nvrt**) เพื่อเข้าใจการแก้ไขภาพ  
- ทำอัตโนมัติการประมวลผลแบบกลุ่มของไฟล์ออกแบบ  

## ขั้นตอนที่ 1: ระบุไดเรกทอรีต้นทางของคุณ
กำหนดโฟลเดอร์ที่มีไฟล์ PSD ที่คุณต้องการทำงาน

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "InvertAdjustmentLayer.psd";
```

แทนที่ `"Your Source Directory"` ด้วยพาธจริงบนเครื่องของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ PSD
ตอนนี้เราจะทำการ **how to load psd** ไฟล์โดยใช้ Aspose API

```java
PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

เมธอด `Image.load()` จะเปิดไฟล์และเตรียมพร้อมสำหรับการตรวจสอบ

## ขั้นตอนที่ 3: เริ่มต้นตัวแปรทรัพยากร Nvrt
เราจะเก็บทรัพยากร Nvrt ที่พบไว้ที่

```java
NvrtResource nvrtResource = null;
```

## ขั้นตอนที่ 4: ค้นหาเลเยอร์ปรับค่า Invert
วนซ้ำผ่านแต่ละเลเยอร์, ค้นหา `InvertAdjustmentLayer`, แล้วมองหา `NvrtResource`

```java
try {
    for (Layer layer : psdImage.getLayers()) {
        if (layer instanceof InvertAdjustmentLayer) {
            for (LayerResource layerResource : layer.getResources()) {
                if (layerResource instanceof NvrtResource) {
                    // The NvrtResource is found
                    nvrtResource = (NvrtResource)layerResource;
                    break;
                }
            }
        }
    }
} finally {
    psdImage.dispose();
}
```

บล็อก `finally` รับประกันว่าภาพ PSD จะถูกปล่อยทรัพยากร, ทำให้การใช้หน่วยความจำสะอาด

## ขั้นตอนที่ 5: ตรวจสอบทรัพยากร Nvrt
ยืนยันว่าทรัพยากรถูกค้นพบอย่างสำเร็จ

```java
Assert.isNotNull(nvrtResource);
```

หากการตรวจสอบสำเร็จ, คุณได้อ่านเลเยอร์ของ PSD และสกัดทรัพยากร Nvrt อย่างสำเร็จแล้ว

## ข้อผิดพลาดทั่วไปและเคล็ดลับ
- **Null checks:** ตรวจสอบเสมอว่า `psdImage` และอ็อบเจ็กต์ของเลเยอร์ไม่เป็น null ก่อนเข้าถึง  
- **Resource disposal:** การลืมเรียก `psdImage.dispose()` อาจทำให้เกิดการรั่วของหน่วยความจำในแอปพลิเคชันที่ทำงานต่อเนื่องเป็นเวลานาน  
- **File path issues:** ใช้พาธแบบ absolute หรือให้แน่ใจว่าไดเรกทอรีทำงานตั้งค่าอย่างถูกต้องเพื่อหลีกเลี่ยง `FileNotFoundException`  

## สรุป
ตอนนี้คุณรู้แล้วว่า **how to load psd** ไฟล์, อ่านเลเยอร์ของมัน, และสกัดทรัพยากรการปรับค่า Nvrt ด้วย Java และ Aspose.PSD พื้นฐานนี้ทำให้คุณสามารถสร้างเครื่องมืออัตโนมัติกราฟิกที่ทรงพลัง, ประมวลผลแบบกลุ่มของทรัพยากรการออกแบบ, หรือรวมข้อมูล Photoshop เข้ากับกระบวนการทำงานที่ใหญ่ขึ้น

## คำถามที่พบบ่อย

**Q: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถสร้าง, แก้ไข, แปลง, และเรนเดอร์ไฟล์ PSD โดยตรงจากโค้ด Java  

**Q: ฉันสามารถใช้ Aspose.PSD ในผลิตภัณฑ์เชิงพาณิชย์ได้หรือไม่?**  
A: ใช่, จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์จริง คุณสามารถสำรวจตัวเลือกการซื้อได้ [here](https://purchase.aspose.com/buy)  

**Q: ฉันจะหาเอกสารประกอบของ Aspose.PSD ได้จากที่ไหน?**  
A: เอกสารฉบับเต็มพร้อมให้บริการที่นี่: [ose.PSD Documentation](https://reference.aspose.com/psd/java/)  

**Q: มีรุ่นทดลองใช้ฟรีหรือไม่?**  
A: แน่นอน! คุณสามารถรับรุ่นทดลองใช้ฟรีของ Aspose.PSD for Java [here](https://releases.aspose.com/)  

**Q: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร?**  
A: คุณสามารถตั้งคำถามและรับการสนับสนุนได้ในฟอรั่มของ Aspose: [Aspose Support](https://forum.aspose.com/c/psd/34)  

---

**อัปเดตล่าสุด:** 2025-12-17  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}