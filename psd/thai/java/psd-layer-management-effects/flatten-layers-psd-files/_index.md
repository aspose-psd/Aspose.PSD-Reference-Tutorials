---
date: 2026-04-03
description: เรียนรู้วิธีลดขนาดไฟล์ PSD โดยการทำให้เลเยอร์แบนด้วย Aspose.PSD สำหรับ
  Java คู่มือแบบขั้นตอนนี้จะแสดงวิธีทำให้ไฟล์ PSD แบนอย่างรวดเร็ว
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: ลดขนาดไฟล์ PSD ด้วยการทำให้เลเยอร์แบน – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: ลดขนาดไฟล์ PSD ด้วยการรวมเลเยอร์ – Aspose.PSD Java
url: /th/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ลดขนาดไฟล์ PSD ด้วยการทำให้ชั้นเป็นแบน – Aspose.PSD Java

## บทนำ

หากคุณเคยเปิดเอกสาร Photoshop แล้วสงสัยว่าจะ **reduce PSD file size** อย่างไร การทำให้ชั้นเป็นแบนเป็นหนึ่งในเทคนิคที่มีประสิทธิภาพที่สุด ด้วย Aspose.PSD for Java คุณสามารถทำให้ PSD ทั้งไฟล์เป็นแบนโดยอัตโนมัติหรือรวมเฉพาะชั้นที่คุณเลือกได้ ให้คุณควบคุมน้ำหนักไฟล์อย่างละเอียดโดยไม่เสียคุณภาพภาพ ในบทแนะนำนี้เราจะอธิบายทั้งสองวิธี—การทำให้ภาพทั้งหมดเป็นแบนและการรวมชั้นเฉพาะ—เพื่อให้คุณสามารถลดขนาดไฟล์ PSD ได้อย่างรวดเร็วและทำให้กระบวนการทำงานของคุณราบรื่น

## คำตอบสั้น
- **การทำให้เป็นแบนทำอะไร?** มันรวมชั้นที่มองเห็นได้เป็นชั้นพื้นหลังเดียว, ลบข้อมูลชั้นและมักจะลดขนาดไฟล์.  
- **ฉันสามารถทำให้เป็นแบนเฉพาะชั้นที่เลือกได้หรือไม่?** ได้, คุณสามารถรวมชั้นเฉพาะได้ในขณะที่ปล่อยให้ชั้นอื่นไม่ถูกเปลี่ยนแปลง.  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีทำงานสำหรับการพัฒนา; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการผลิต.  
- **ต้องการเวอร์ชัน Java ใด?** JDK 8 หรือสูงกว่า.  
- **การทำให้เป็นแบนจะส่งผลต่อคุณภาพภาพหรือไม่?** ไม่, ลักษณะภาพยังคงเหมือนเดิม; มีเพียงโครงสร้างชั้นที่เปลี่ยนแปลง.

## “reduce PSD file size” คืออะไร

การลดขนาดไฟล์ PSD หมายถึงการลบข้อมูลที่ไม่จำเป็น—เช่นชั้นเพิ่มเติม, ช่องที่ซ่อนอยู่, หรือเมตาดาต้ามากเกินไป—เพื่อให้ไฟล์เบาขึ้นและโหลด, แชร์, หรือประมวลผลได้เร็วขึ้น การทำให้ชั้นเป็นแบนเป็นเทคนิคทั่วไปเพราะมันกำจัดวัตถุชั้นแยกต่างหากในขณะที่ยังคงรักษาภาพรวมสุดท้าย

## ทำไมต้องทำให้ชั้นเป็นแบนด้วย Aspose.PSD for Java?

- **Automation:** ไม่จำเป็นต้องเปิด Photoshop ด้วยตนเอง; สามารถรวมเข้ากับแอปพลิเคชัน Java ของคุณโดยตรง.  
- **Precision:** เลือกทำให้เป็นแบนทั้งเอกสารหรือเฉพาะชั้นที่มองเห็น (`flattenImage`) หรือรวมชั้นที่เลือก (`mergeLayers`).  
- **Performance:** ไฟล์ที่เล็กลงโหลดได้เร็วขึ้นและใช้หน่วยความจำน้อยลงในกระบวนการต่อไป.  
- **Cross‑platform:** ทำงานบนระบบปฏิบัติการใดก็ได้ที่รองรับ Java.

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK):** ติดตั้ง JDK 8 หรือใหม่กว่า.  
2. **Aspose.PSD for Java:** ดาวน์โหลดไลบรารีจาก [here](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA, Eclipse หรือ IDE ที่รองรับ Java ใดก็ได้.  
4. **Basic Java knowledge:** มีประโยชน์แต่ไม่จำเป็นสำหรับการทำตามขั้นตอน.  
5. **Sample PSD:** ไฟล์ที่มีหลายชั้น (เราจะใช้ `ThreeRegularLayersSemiTransparent.psd`).

ตอนนี้เรามีทุกอย่างพร้อมแล้ว, มาเริ่มดูโค้ดกัน.

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น, ให้ import คลาส Aspose.PSD ที่จำเป็น:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

การ import เหล่านี้ทำให้เราสามารถโหลดไฟล์ PSD, ทำงานกับชั้นของมัน, และบันทึกผลลัพธ์ได้.

## ขั้นตอนที่ 1: ทำให้ภาพ PSD ทั้งหมดเป็นแบน

การทำให้ภาพทั้งหมดเป็นแบนเป็นวิธีที่เร็วที่สุดเพื่อ **reduce PSD file size** เพราะมันลบข้อมูลชั้นแต่ละชั้นทั้งหมด.

### 1.1 โหลดไฟล์ PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 ทำให้ภาพเป็นแบน

```java
im.flattenImage();
```

### 1.3 บันทึกภาพที่ทำให้เป็นแบน

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

ไฟล์ใหม่ของคุณตอนนี้มีเพียงชั้นพื้นหลังเดียว, ซึ่งโดยทั่วไปจะทำให้ขนาด PSD เล็กลง.

## ขั้นตอนที่ 2: รวมชั้นเฉพาะ (วิธีทำให้ PSD เป็นแบนแบบเลือกส่วน)

บางครั้งคุณอาจต้องการ **flatten visible layers** หรือรวมชุดย่อยของชั้นในขณะที่ยังคงให้ชั้นอื่นแก้ไขได้.

### 2.1 โหลดไฟล์ PSD อีกครั้ง

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 ระบุและเลือกชั้น

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 รวมชั้น

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 แทนที่ชั้นที่มีอยู่ด้วยชั้นที่รวมแล้ว

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 บันทึกไฟล์ PSD ที่อัปเดต

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

ตอนนี้ PSD มีเพียงชั้นที่รวมแล้ว, ทำให้ขนาดไฟล์ลดลงในขณะที่ยังคงรักษาชั้นที่คุณต้องการเก็บไว้.

## ปัญหาทั่วไปและเคล็ดลับ

- **Backup before flattening:** เมื่อชั้นถูกทำให้เป็นแบนแล้ว การดำเนินการไม่สามารถย้อนกลับได้. เก็บสำเนาไฟล์ PSD ดั้งเดิมไว้.  
- **Visibility matters:** `flattenImage()` จะรวมเฉพาะชั้นที่ *visible* เท่านั้น. ซ่อนชั้นใดที่คุณไม่ต้องการรวม.  
- **Memory usage:** PSD ขนาดใหญ่สามารถใช้ RAM มาก; พิจารณาประมวลผลบนเครื่องที่มีหน่วยความจำเพียงพอ.  
- **Blending modes:** การรวมจะเคารพโหมดการผสมของแต่ละชั้น, ดังนั้นผลลัพธ์ภาพจะตรงกับที่คุณเห็นใน Photoshop.

## คำถามที่พบบ่อย

**Q: ฉันสามารถย้อนกลับการทำให้ชั้นเป็นแบนใน Aspose.PSD ได้หรือไม่?**  
A: ไม่, การทำให้เป็นแบนไม่สามารถย้อนกลับได้. ควรเก็บสำเนาไฟล์ต้นฉบับไว้เสมอ.

**Q: สามารถทำให้เป็นแบนเฉพาะชั้นที่มองเห็นได้หรือไม่?**  
A: ได้. `flattenImage()` เคารพการมองเห็นของชั้น, ดังนั้นซ่อนชั้นที่คุณไม่ต้องการทำให้เป็นแบนก่อนเรียกเมธอด.

**Q: การทำให้ชั้นเป็นแบนทำให้ขนาดไฟล์ลดลงหรือไม่?**  
A: โดยทั่วไปแล้ว, ใช่. การลบข้อมูลชั้นและเมตาดาต้ามักทำให้ PSD เล็กลง, แม้ว่าการลดขนาดที่แน่นอนจะขึ้นอยู่กับเนื้อหา.

**Q: ฉันสามารถรวมชั้นที่มีโหมดการผสมต่างกันได้หรือไม่?**  
A: แน่นอน. Aspose.PSD จะรวมชั้นโดยยังคงลักษณะภาพที่สร้างโดยโหมดการผสมของพวกมัน.

**Q: จะเกิดอะไรขึ้นหากฉันพยายามรวมชั้นที่ไม่ต่อเนื่องกัน?**  
A: Aspose.PSD อนุญาตให้รวมชั้นใดก็ได้โดยไม่คำนึงถึงลำดับในสแตก; ผลลัพธ์จะสะท้อนลักษณะการรวมกัน.

---

**อัปเดตล่าสุด:** 2026-04-03  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}