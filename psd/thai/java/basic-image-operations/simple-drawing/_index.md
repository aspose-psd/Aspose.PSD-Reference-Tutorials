---
date: 2025-12-27
description: เรียนรู้วิธีวาดสี่เหลี่ยมสีแดงและรูปทรงอื่น ๆ ในไฟล์ PSD ด้วย Aspose.PSD
  for Java คู่มือขั้นตอนต่อขั้นตอนนี้ครอบคลุมการสร้างเอกสาร การเพิ่มเลเยอร์ และการวาดด้วยตัวอย่างโค้ด
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: วาดสี่เหลี่ยมสีแดงด้วย Aspose.PSD สำหรับ Java
url: /th/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วาดสี่เหลี่ยมสีแดงด้วย Aspose.PSD สำหรับ Java

## บทนำ

ยินดีต้อนรับสู่คู่มือแบบขั้นตอนนี้เกี่ยวกับการ **วาดสี่เหลี่ยมสีแดง** ด้วย Aspose.PSD สำหรับ Java! ในบทเรียนนี้ เราจะอธิบายการสร้างเอกสาร PSD ใหม่, การเพิ่มเลเยอร์, และการวาดรูปทรงด้วยสีที่กำหนดเอง ไม่ว่าคุณจะทำงานอัตโนมัติสำหรับสินทรัพย์กราฟิกหรือสร้างแบ็กเอนด์ของเครื่องมือออกแบบ บทเรียนนี้จะให้บล็อกการสร้างพื้นฐานที่จำเป็นแก่คุณ

## คำตอบสั้น
- **คลาสหลักที่ใช้สร้างไฟล์ PSD คืออะไร?** `PsdImage`
- **เมธอดใดที่ล้างสีพื้นหลังของเลเยอร์?** `Graphics.clear(Color)`
- **จะวาดสี่เหลี่ยมสีแดงอย่างไร?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **ต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์สำหรับการใช้งานจริง
- **สามารถจัดการไฟล์ PSD ที่มีอยู่ด้วย API เดียวกันได้หรือไม่?** ใช่, Aspose.PSD รองรับการแก้ไข PSD อย่างเต็มรูปแบบ

## การวาดสี่เหลี่ยมสีแดงในไฟล์ PSD คืออะไร?
การวาดสี่เหลี่ยมสีแดงหมายถึงการใช้วัตถุ `Graphics` เพื่อเรนเดอร์รูปสี่เหลี่ยมที่เติมสีหรือขอบสีแดงลงบนเลเยอร์เฉพาะของภาพ PSD การดำเนินการนี้มักใช้สำหรับไฮไลท์พื้นที่, สร้างตำแหน่งที่วางไว้, หรือเพิ่มกราฟิกอย่างง่ายโดยอัตโนมัติ

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java เพื่อจัดการไฟล์ PSD?
Aspose.PSD ให้ API แบบ pure‑Java ที่ทำให้คุณสามารถอ่าน, แก้ไข, และเขียนไฟล์ Photoshop PSD ได้โดยไม่ต้องติดตั้ง Photoshop รองรับการจัดการเลเยอร์, การจัดการสี, และการวาดเวกเตอร์ ทำให้เหมาะสำหรับการประมวลผลภาพบนเซิร์ฟเวอร์, สายงานอัตโนมัติของสินทรัพย์, และการสร้างกราฟิกแบบกำหนดเอง

## ข้อกำหนดเบื้องต้น

- ติดตั้ง Java Development Kit (JDK) บนเครื่องของคุณ  
- ไลบรารี Aspose.PSD สำหรับ Java คุณสามารถดาวน์โหลดได้จาก [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/)

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น ให้นำเข้าคลาสที่จำเป็นเข้าสู่โครงการ Java ของคุณ:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## ขั้นตอนที่ 1: สร้างเอกสารใหม่

แรกเริ่ม สร้างเอกสาร PSD ใหม่ด้วยขนาดแคนวาสที่ต้องการ เอกสารนี้จะเป็นโฮสต์ของเลเยอร์ที่เราจะวาดบนมัน

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## ขั้นตอนที่ 2: เพิ่มเลเยอร์

ต่อไป เพิ่มเลเยอร์เปล่าที่ครอบคลุมความกว้างและความสูงเต็มของภาพ เลเยอร์เป็นสิ่งสำคัญสำหรับการแยกการดำเนินการวาด

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## ขั้นตอนที่ 3: วาดรูปทรง

เราจะใช้คลาส `Graphics` เพื่อจัดการข้อมูลพิกเซลของเลเยอร์ ด้านล่างเป็นตัวอย่างสามกรณีที่แการล้างพื้นหลังและการวาดสี่เหลี่ยมด้วยสีต่าง ๆ

### ล้างสีเลเยอร์ (ตั้งค่าพื้นหลังเป็นสีเหลือง```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### วาดสี่เหลี่ยมสีแดง (จุดโฟกัสหลัก)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### วาดสี่เหลี่ยมสีน้ำเงิน (ตัวอย่างเพิ่มเติม)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลง

สุดท้าย ให้เขียนภาพ PSD ที่แก้ไขแล้วลงดิสก์ ไฟล์จะประกอบด้วยเลเยอร์ใหม่และรูปทรงที่วาดไว้

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## ปัญหาที่พบบ่อยและวิธีแก้

- **เลเยอร์ไม่แสดงหลังการวาด:** ตรวจสอบว่าได้เพิ่มเลเยอร์ลงในภาพ **ก่อน** สร้างอ็อบเจกต์ `Graphics`
- **สีแสดงไม่ถูกต้อง:** ยืนยันว่าคุณใช้ `Color.getRed()` (หรือเมธอดสเตติกอื่น) แทนค่ารหัส RGB ที่อาจอยู่นอกช่วง
- **ไฟล์ไม่ถูกบันทึก:** ยืนยันว่าเส้นทาง `outputDir` มีอยู่และแอปพลิเคชันมีสิทธิ์เขียน

## คำถามที่พบบ่อย

### Q1: สามารถใช้ Aspose.PSD สำหรับ Java เพื่อจัดการไฟล์ PSD ที่มีอยู่ได้หรือไม่?

A1: ใช่, Aspose.PSD สำหรับ Java มีฟังก์ชันการทำงานอย่างครอบคลุมสำหรับการแก้ไขและจัดการไฟล์ PSD ที่มีอยู่

### Q2: จะหาการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้จากที่ไหน?

A2: คุณสามารถเยี่ยมชม [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) สำหรับคำถามที่เกี่ยวกับการสนับสนุน

### Q3: มีเวอร์ชันทดลองฟรีสำหรับ Aspose.PSD สำหรับ Java หรือไม่?

A3: มี, คุณสามารถเข้าถึงเวอร์ชันทดลองฟรีได้ [ที่นี่](https://releases.aspose.com/)

### Q4: จะซื้อไลเซนส์สำหรับ Aspose.PSD สำหรับ Java อย่างไร?

A4: คุณสามารถซื้อไลเซนส์ได้จาก [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy)

### Q5: มีไลเซนส์ชั่วคราวสำหรับ Aspose.PSD สำหรับ Java หรือไม่?

A5: มี, คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/)

## คำถามที่พบบ่อยเพิ่มเติม

**Q: สามารถวาดรูปทรงอื่น ๆ นอกจากสี่เหลี่ยมได้หรือไม่?**  
A: ใช่, คลาส `Graphics` ยังรองรับการวาดวงรี, เส้น, และพาธที่กำหนดเอง

**Q: Aspose.PSD รองรับความโปร่งใสในรูปทรงที่วาดหรือไม่?**  
A: แน่นอน; คุณสามารถใช้ `SolidBrush` พร้อมสี ARGB เพื่อรวมค่าอัลฟ่าโปร่งใสได้

**Q: สามารถแก้ไขความทึบของเลเยอร์ได้หรือไม่?**  
A: ใช่, แต่ละอ็อบเจกต์ `Layer` มีเมธอด `setOpacity` ที่รับค่าตั้งแต่ 0 ถึง 255

**Q: จะโหลดไฟล์ PSD ที่มีอยู่แทนการสร้างใหม่อย่างไร?**  
A: ใช้ `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` ก่อนทำการจัดการเลเยอร์

## สรุป

คุณได้เรียนรู้วิธี **วาดสี่เหลี่ยมสีแดง** และรูปทรงพื้นฐานอื่น ๆ ในไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java แล้ว โดยการสร้างเอกสาร, เพิ่มเลเยอร์, ล้างพื้นหลังของเลเยอร์, และวาดด้วย API `Graphics` คุณสามารถทำงานอัตโนมัติหลายอย่างในงานออกแบบกราฟิกได้ ลองทดลองต่อด้วยการใช้แปรงต่าง ๆ, เอฟเฟกต์ของเลเยอร์, และรูปแบบไฟล์อื่น ๆ

---

**อัปเดตล่าสุด:** 2025-12-27  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}