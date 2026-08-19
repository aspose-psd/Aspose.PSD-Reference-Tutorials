---
date: 2026-04-03
description: เรียนรู้วิธีการไฮไลท์สีของแผ่นในไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java.
  ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อพัฒนาทักษะการจัดการภาพของคุณใน Java.
keywords:
- highlight sheet color psd
- change psd layer color
- Aspose.PSD Java
linktitle: ไฮไลท์สีแผ่นในไฟล์ PSD โดยใช้ Aspise.PSD Java
second_title: Aspose.PSD Java API
title: ไฮไลท์สีแผ่นงานในไฟล์ PSD ด้วย Aspise.PSD Java
url: /th/java/psd-layer-management-effects/highlight-sheet-color-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ไฮไลท์สีแผ่นในไฟล์ PSD ด้วย Aspose.PSD Java

## บทนำ

หากคุณต้องการ **highlight sheet color psd** ไฟล์โดยอัตโนมัติ คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะพาคุณผ่านตัวอย่างเต็มรูปแบบที่ทำให้คุณเห็นวิธีการเปลี่ยนสีแผ่นของเลเยอร์แต่ละชั้นโดยใช้ Aspose.PSD for Java ไม่ว่าคุณจะกำลังสร้างเครื่องมือประมวลผลแบบกลุ่ม, ตัวแก้ไขแบบกำหนดเอง, หรือเพียงแค่ทำงานออกแบบที่ทำซ้ำอัตโนมัติ การเชี่ยวชาญเทคนิคนี้จะให้การควบคุมระดับละเอียดเหนือทรัพย์สิน PSD ของคุณ

## คำตอบอย่างรวดเร็ว
- **“highlight sheet color” หมายถึงอะไร?** เป็นสัญญาณภาพที่กำหนดให้กับเลเยอร์และปรากฏเป็นแถบสีในพาเนลเลเยอร์ของ Photoshop.  
- **ไลบรารีใดจัดการสิ่งนี้ใน Java?** Aspose.PSD for Java มี `SheetColorHighlightEnum` และ API ที่เกี่ยวข้อง.  
- **ฉันต้องการไลเซนส์เพื่อทดลองใช้งานหรือไม่?** มีการทดลองใช้งานฟรี; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานในสภาพแวดล้อมการผลิต.  
- **ฉันสามารถเปลี่ยนหลายเลเยอร์พร้อมกันได้หรือไม่?** ได้—ทำการวนลูปผ่านคอลเลกชัน `Layer[]` และตั้งค่าสีไฮไลท์ของแต่ละเลเยอร์.  
- **ต้องการเวอร์ชัน Java ใด?** JDK 8 หรือสูงกว่า.

## “highlight sheet color psd” คืออะไร?

การไฮไลท์สีแผ่นคือคุณลักษณะเมตาดาต้าที่เก็บอยู่ในไฟล์ PSD ซึ่งบอก Photoshop (และเครื่องมือที่เข้ากันได้) ให้วาดแถบสีข้างชื่อเลเยอร์ มันมีประโยชน์สำหรับการระบุกลุ่มเลเยอร์อย่างรวดเร็ว—คิดว่าเป็นแท็กภาพที่สามารถตั้งเป็นสีต่าง ๆ เช่น สีม่วง, สีส้ม, สีเหลือง ฯลฯ.

## ทำไมต้องเปลี่ยนสีเลเยอร์ PSD ด้วยโปรแกรม?

- **Automation:** ประมวลผลหลายร้อยไฟล์โดยไม่ต้องคลิกด้วยมือ.  
- **Consistency:** บังคับใช้รูปแบบการตั้งชื่อ/สีทั่วทั้งระบบออกแบบ.  
- **Integration:** ผสานการจัดการ PSD กับกระบวนการทำงานอื่น ๆ ที่ใช้ Java (เช่น การสร้างทรัพยากรสำหรับแอปมือถือ).

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Java Development Kit (JDK) 8+** – ดาวน์โหลดจาก [Java website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **IDE** – IntelliJ IDEA, Eclipse, หรือ NetBeans (ตามที่คุณเลือก).  
- **Aspose.PSD for Java library** – รับได้จาก [Aspose's website](https://releases.aspose.com/psd/java/).  
- **Sample PSD file** – `SheetColorHighlightExample.psd` (สร้างของคุณเองหรือดาวน์โหลดตัวอย่างจากออนไลน์).  
- **Basic Java knowledge** – คุณควรคุ้นเคยกับคลาส, เมธอด, และการทำ I/O ของไฟล์อย่างง่าย.

## นำเข้าแพ็กเกจ

ก่อนอื่นให้ทำการนำเข้าคลาสที่เราต้องการ การนำเข้าต่าง ๆ นี้ทำให้เราสามารถเข้าถึงการจัดการภาพหลัก, การจัดการเลเยอร์, และ enumeration สำหรับการไฮไลท์สีแผ่น.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layerresources.SheetColorHighlightEnum;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดไฟล์ PSD

#### 1.1 กำหนดเส้นทางไฟล์

ตั้งค่าเส้นทางต้นทางและปลายทาง แทนที่ตัวแปรตำแหน่งที่เก็บด้วยโฟลเดอร์จริงที่มีไฟล์ PSD ของคุณ.

```java
String dataDir = "YOUR DOCUMENT DIRECTORY";

String sourceFileName = dataDir + "SheetColorHighlightExample.psd";
String exportPath = dataDir + "SheetColorHighlightExampleChanged.psd";
```

#### 1.2 โหลดไฟล์ PSD

ใช้ `Image.load()` และแคสต์ผลลัพธ์เป็น `PsdImage` เพื่อให้เราสามารถทำงานกับฟีเจอร์เฉพาะของ PSD.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### ขั้นตอนที่ 2: เข้าถึงและตรวจสอบเลเยอร์

เลเยอร์เก็บเนื้อหาภาพของ PSD เราจะอ่านการไฮไลท์สีแผ่นปัจจุบันเพื่อยืนยันสถานะเริ่มต้น.

#### 2.1 เข้าถึงเลเยอร์แรก

```java
Layer layer1 = im.getLayers()[0];
Assert.areEqual(SheetColorHighlightEnum.Violet, layer1.getSheetColorHighlight());
```

#### 2.2 เข้าถึงเลเยอร์ที่สอง

```java
Layer layer2 = im.getLayers()[1];
Assert.areEqual(SheetColorHighlightEnum.Orange, layer2.getSheetColorHighlight());
```

### ขั้นตอนที่ 3: แก้ไขการไฮไลท์สีแผ่น

ตอนนี้เราจะเปลี่ยนการไฮไลท์ของเลเยอร์แรกเป็นสีเหลือง เพื่อสาธิตวิธี **change psd layer color** ด้วยโปรแกรม.

```java
layer1.setSheetColorHighlight(SheetColorHighlightEnum.Yellow);
```

### ขั้นตอนที่ 4: บันทึกไฟล์ PSD ที่แก้ไขแล้ว

บันทึกการเปลี่ยนแปลงลงในไฟล์ใหม่เพื่อให้ไฟล์ต้นฉบับไม่ถูกแก้ไข.

```java
im.save(exportPath);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| `Assert` ล้มเหลว | การไฮไลท์ของเลเยอร์ที่มีอยู่ไม่ตรงกับที่โค้ดคาดหวัง (เช่น PSD ที่แตกต่าง) | เปิด PSD ใน Photoshop เพื่อตรวจสอบสี, หรือเอาการตรวจสอบ `Assert` ออกเพื่อสคริปต์ที่ยืดหยุ่นมากขึ้น. |
| `NullPointerException` บน `im.getLayers()` | ไฟล์ไม่โหลดอย่างถูกต้อง (เส้นทางผิดหรือไฟล์เสียหาย) | ตรวจสอบ `sourceFileName` อีกครั้งและให้แน่ใจว่า PSD ถูกต้อง. |
| การไฮไลท์ไม่ปรากฏใน Photoshop | Photoshop แคชข้อมูลเลเยอร์; คุณอาจต้องเปิดไฟล์ใหม่ | ปิดและเปิด PSD ใหม่หลังบันทึก, หรือใช้ `im.flush()` ก่อนบันทึก. |

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถอ่าน, แก้ไข, และบันทึกไฟล์ PSD ได้โดยไม่ต้องติดตั้ง Photoshop.

**ถาม: ฉันสามารถใช้ Aspose.PSD for Java กับรูปแบบไฟล์อื่นได้หรือไม่?**  
A: ได้—รองรับ BMP, PNG, JPEG, GIF, TIFF และอื่น ๆ ทำให้สามารถแปลงไฟล์ไปยังและจาก PSD ได้.

**ถาม: สามารถยกเลิกการเปลี่ยนแปลงไฟล์ PSD ที่ทำด้วย Aspose.PSD for Java ได้หรือไม่?**  
A: เมื่อบันทึกแล้ว การเปลี่ยนแปลงจะถาวร เก็บสำเนาสำรองของไฟล์ต้นฉบับไว้หากต้องการย้อนกลับ.

**ถาม: ฉันจะขอรับไลเซนส์สำหรับ Aspose.PSD for Java ได้อย่างไร?**  
A: ซื้อไลเซนส์จาก [Aspose website](https://purchase.aspose.com/buy). หากคุณกำลังประเมินผล คุณสามารถขอ [temporary license](https://purchase.aspose.com/temporary-license/) สำหรับระยะเวลาจำกัด.

**ถาม: ฉันสามารถไฮไลท์หลายเลเยอร์พร้อมกันในไฟล์ PSD ได้หรือไม่?**  
A: แน่นอน. ทำการวนลูปผ่าน `im.getLayers()` และเรียก `setSheetColorHighlight()` บนแต่ละเลเยอร์ตามต้องการ.

---

**อัปเดตล่าสุด:** 2026-04-03  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}