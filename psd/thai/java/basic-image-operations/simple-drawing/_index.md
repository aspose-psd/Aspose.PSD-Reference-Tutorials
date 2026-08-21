---
date: 2026-06-13
description: เรียนรู้วิธีวาดสี่เหลี่ยมในไฟล์ PSD ด้วย Aspose.PSD for Java คู่มือนี้แสดงโค้ดแบบขั้นตอนต่อขั้นตอน
  การเพิ่มเลเยอร์ การประมวลผลภาพบนเซิร์ฟเวอร์และการวาดรูปทรง
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: ทำการวาดอย่างง่าย
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: วิธีวาดสี่เหลี่ยมในไฟล์ PSD ด้วย Aspose.PSD for Java
url: /th/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดสี่เหลี่ยมผืนผ้าใน PSD ด้วย Aspose.PSD สำหรับ Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีวาดสี่เหลี่ยมผืนผ้า** ภายในไฟล์ Photoshop PSD โดยใช้ไลบรารี Aspose.PSD แบบ pure‑Java ไม่ว่าคุณจะสร้าง pipeline สินทรัพย์ฝั่งเซิร์ฟเวอร์, ทำการสร้าง thumbnail อัตโนมัติ, หรือเพิ่มกราฟิกแบบไดนามิกให้กับการออกแบบที่มีอยู่ ขั้นตอนต่อไปนี้จะให้โซลูชันที่ครบถ้วนและพร้อมใช้งานในสภาพแวดล้อมการผลิต เราจะครอบคลุมการสร้างเอกสาร PSD ใหม่, การเพิ่มเลเยอร์, การล้างพื้นหลัง, และสุดท้ายการวาดสี่เหลี่ยมสีแดงและสีน้ำเงิน—ทั้งหมดโดยไม่ต้องเปิด Photoshop

## คำตอบด่วน
- **คลาสหลักที่ใช้สร้างไฟล์ PSD คืออะไร?** `PsdImage`
- **เมธอดใดที่ใช้ล้างสีพื้นหลังของเลเยอร์?** `Graphics.clear(Color)`
- **วิธีวาดสี่เหลี่ยมสีแดงคืออะไร?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **ฉันต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** A free trial works for testing; a license is required for production.
- **ฉันสามารถจัดการไฟล์ PSD ที่มีอยู่ด้วย API เดียวกันได้หรือไม่?** Yes, Aspose.PSD supports full PSD editing.

## การวาดสี่เหลี่ยมสีแดงในไฟล์ PSD คืออะไร?

การวาดสี่เหลี่ยมสีแดงหมายถึงการใช้วัตถุ `Graphics` เพื่อเรนเดอร์รูปสี่เหลี่ยมที่เติมหรือขอบด้วยสีแดงลงบนเลเยอร์เฉพาะของภาพ PSD การดำเนินการนี้มักใช้เพื่อไฮไลท์พื้นที่, สร้างตำแหน่งเก็บชั่วคราว, หรือเพิ่มกราฟิกง่าย ๆ ผ่านโปรแกรม

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java เพื่อจัดการไฟล์ PSD?

Aspose.PSD สำหรับ Java รองรับ **รูปแบบการนำเข้าและส่งออกกว่า 50** รูปแบบ, สามารถประมวลผลไฟล์ PSD หลายร้อยหน้าโดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ, และทำงานบนแพลตฟอร์มใดก็ได้ที่รองรับ Java 8 หรือสูงกว่า เครื่องมือประมวลผลภาพฝั่งเซิร์ฟเวอร์ของมันช่วยขจัดความจำเป็นในการใช้ Photoshop, ลดค่าใช้จ่ายไลเซนส์, และเปิดใช้งานเวิร์กโฟลว์อัตโนมัติที่จัดการข้อมูลภาพได้ถึง **10 GB** ต่อชั่วโมงบน VM ที่มีสเปคปานกลาง

## ข้อกำหนดเบื้องต้น

- Java Development Kit (JDK) 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณ.  
- ไลบรารี Aspose.PSD สำหรับ Java คุณสามารถดาวน์โหลดได้จาก [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## นำเข้าแพ็กเกจ

คำสั่ง `import` จะนำเข้าคลาสที่จำเป็นเข้าสู่สโคปเพื่อให้คุณสามารถทำงานกับภาพ PSD, เลเยอร์, สีและกราฟิกได้

`PsdImage` เป็นอ็อบเจ็กต์ระดับบนของ Aspose.PSD ที่แทนไฟล์ PSD เดียวในหน่วยความจำ.  
`Graphics` ให้ primitive การวาดเช่น เส้น, สี่เหลี่ยมและวงรี.  
`Color` และ `Pen` ให้คุณกำหนดสีและความหนาของเส้น.  
คลาส `Layer` แทนเลเยอร์ภาพแต่ละชิ้นภายในเอกสาร PSD.  
คลาส `Rectangle` กำหนดตำแหน่งและขนาดของพื้นที่สี่เหลี่ยมที่ใช้สำหรับการวาด.  
คลาส `SolidBrush` เติมรูปด้วยสีทึบ.

## ขั้นตอนแรกในการสร้างเอกสาร PSD คืออะไร?

คุณสร้างอินสแตนซ์ของ `PsdImage` โดยระบุความกว้างและความสูงของแคนวาสเป็นพิกเซล ซึ่งจะสร้างโครงสร้างไฟล์ PSD ว่าง หลังจากตั้งค่าเลเยอร์หรือพื้นหลังเริ่มต้นแล้ว ให้เรียกเมธอด `save` พร้อมเส้นทางไฟล์เพื่อบันทึกเอกสารลงดิสก์ การทำเช่นนี้เตรียมภาพสำหรับการแก้ไขต่อไป

## ขั้นตอนที่ 1: สร้างเอกสารใหม่

แรกเริ่ม, สร้างเอกสาร PSD ใหม่ด้วยขนาดแคนวาสที่ต้องการ เอกสารนี้จะเป็นโฮสต์ของเลเยอร์ที่เราจะวาด

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## วิธีการเพิ่มเลเยอร์ว่างใหม่ลงในภาพ PSD คืออะไร?

แรกเริ่ม, สร้างอินสแตนซ์ `Layer` ใหม่ที่มีความกว้างและความสูงเท่ากับ `PsdImage` พาเรนท์ จากนั้นเพิ่มเลเยอร์นี้เข้าไปในคอลเลกชัน `Layers` ของภาพโดยใช้เมธอด `add` เมื่อเลเยอร์เป็นส่วนหนึ่งของภาพแล้ว ให้ดึงอ็อบเจ็กต์ `Graphics` ของมันเพื่อทำการวาด; หากข้ามขั้นตอนนี้ การวาดจะไม่ปรากฏ

## ขั้นตอนที่ 2: เพิ่มเลเยอร์

ต่อไป, เพิ่มเลเยอร์ว่างใหม่ที่ครอบคลุมความกว้างและความสูงทั้งหมดของภาพ เลเยอร์เป็นสิ่งสำคัญสำหรับการแยกการดำเนินการวาด

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## วัตถุประสงค์ของการล้างสีพื้นหลังของเลเยอร์คืออะไร?

การเรียก `Graphics.clear` พร้อม `Color` เฉพาะจะเติมสีนั้นลงบนเลเยอร์ทั้งหมด ทำให้รีเซ็ตข้อมูลพิกเซลทั้งหมด การทำเช่นนี้รับประกันว่าข้อมูลก่อนหน้าถูกลบและเลเยอร์เริ่มจากพื้นหลังที่กำหนดไว้ ซึ่งช่วยหลีกเลี่ยงความโปร่งใสหรือการผสมสีที่ไม่คาดคิดเมื่อเปิดหรือแก้ไข PSD ใน Photoshop ภายหลัง

## ขั้นตอนที่ 3: วาดรูปทรง

เราจะใช้คลาส `Graphics` เพื่อจัดการข้อมูลพิกเซลของเลเยอร์ ด้านล่างเป็นตัวอย่างสามกรณีที่แสดงการล้างพื้นหลังและการวาดสี่เหลี่ยมด้วยสีต่าง ๆ

### ล้างสีเลเยอร์ (ตั้งพื้นหลังเป็นสีเหลือง)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### วาดสี่เหลี่ยมสีแดง (จุดโฟกัสหลัก)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### วาดสี่เหลี่ยมสีน้ำเงิน (ตัวอย่างเพิ่มเติม)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## วิธีบันทึกไฟล์ PSD ที่แก้ไขแล้วลงดิสก์คืออะไร?

ใช้เมธอด `save` บนวัตถุ `PsdImage` โดยส่งเส้นทางไฟล์เต็มและอาจระบุรูปแบบภาพที่ต้องการ (โดยค่าเริ่มต้นคือ PSD) วิธีนี้จะเขียนเลเยอร์, มาสก์, และคำสั่งวาดทั้งหมดลงในไฟล์ PSD เดียวที่สอดคล้องกับสเปคของ Photoshop ทำให้สามารถเปิดได้โดยไม่มีคำเตือน

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลง

สุดท้าย, เขียนภาพ PSD ที่แก้ไขแล้วลงดิสก์ ไฟล์จะประกอบด้วยเลเยอร์ใหม่และรูปทรงที่วาด

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## ปัญหาที่พบบ่อยและวิธีแก้

- **เลเยอร์ไม่แสดงหลังการวาด:** ตรวจสอบว่าได้เพิ่มเลเยอร์ลงในภาพ **ก่อน** สร้างอ็อบเจ็กต์ `Graphics` พื้นผิวการวาดต้องเชื่อมต่อกับเลเยอร์ที่ถูกต้อง
- **สีแสดงผลไม่ถูกต้อง:** ตรวจสอบว่าคุณใช้ `Color.getRed()` (หรือ `Color.getBlue()`) แทนการสร้างค่า RGB แบบกำหนดเองที่เกินช่วง 0‑255
- **ไฟล์ไม่ถูกบันทึก:** ยืนยันว่าเส้นทาง `outputDir` มีอยู่และแอปพลิเคชันมีสิทธิ์เขียนบนระบบ ใน Linux คุณอาจต้องปรับสิทธิ์ของโฟลเดอร์หรือใช้ `Files.createDirectories`
- **ประสิทธิภาพช้าลงเมื่อไฟล์ขนาดใหญ่:** ใช้ `setLoadOptions` ของ `PsdImage` เพื่อโหลดเฉพาะช่องที่ต้องการ ลดการใช้หน่วยความจำสำหรับ PSD ที่ใหญ่กว่า 200 MB

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.PSD สำหรับ Java เพื่อจัดการไฟล์ PSD ที่มีอยู่ได้หรือไม่?**  
A1: ใช่, Aspose.PSD สำหรับ Java มีฟังก์ชันการทำงานที่ครอบคลุมเพื่อแก้ไขและจัดการไฟล์ PSD ที่มีอยู่ รวมถึงการจัดลำดับเลเยอร์, การปรับมาสก์และการวาดเวกเตอร์.

**Q2: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้จากที่ไหน?**  
A2: คุณสามารถเยี่ยมชม [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) เพื่อรับความช่วยเหลือจากชุมชนและการตอบกลับอย่างเป็นทางการจาก Aspose.

**Q3: มีรุ่นทดลองฟรีสำหรับ Aspose.PSD สำหรับ Java หรือไม่?**  
A3: ใช่, คุณสามารถเข้าถึงรุ่นทดลองฟรีได้ [ที่นี่](https://releases.aspose.com/). รุ่นทดลองมีคุณสมบัติทั้งหมดแต่จะใส่ลายน้ำลงในไฟล์ที่บันทึก

**Q4: ฉันจะซื้อไลเซนส์สำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร?**  
A4: คุณสามารถซื้อไลเซนส์ได้จาก [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). ตัวเลือกไลเซนส์รวมถึงแบบถาวร, แบบสมัครสมาชิกและแบบไซต์.

**Q5: มีไลเซนส์ชั่วคราวสำหรับ Aspose.PSD สำหรับ Java หรือไม่?**  
A5: ใช่, คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/).

## คำถามที่พบบ่อยเพิ่มเติม

**Q: ฉันสามารถวาดรูปร่างอื่นนอกจากสี่เหลี่ยมได้หรือไม่?**  
A: ได้, คลาส `Graphics` ยังรองรับการวาดวงรี, เส้น, และเส้นทางกำหนดเองผ่านเมธอด `drawPath`.

**Q: Aspose.PSD รองรับความโปร่งใสในรูปที่วาดหรือไม่?**  
A: แน่นอน; คุณสามารถใช้ `SolidBrush` กับสี ARGB เพื่อรวมความโปร่งใสของอัลฟ่า ทำให้สามารถสร้างโอเวอร์เลย์กึ่งโปร่งใสได้.

**Q: สามารถแก้ไขความทึบของเลเยอร์ได้หรือไม่?**  
A: ได้, แต่ละอ็อบเจ็กต์ `Layer` มีเมธอด `setOpacity` ที่รับค่าตั้งแต่ 0 ถึง 255 เพื่อควบคุมความโปร่งใสของเลเยอร์อย่างละเอียด.

**Q: ฉันจะโหลดไฟล์ PSD ที่มีอยู่แทนการสร้างใหม่ได้อย่างไร?**  
A: ใช้ `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` ก่อนทำการจัดการเลเยอร์ ภาพที่โหลดจะคงเลเยอร์และมาสก์เดิมทั้งหมด.

## สรุป

คุณได้เรียนรู้ **วิธีวาดสี่เหลี่ยมผืนผ้า** และการจัดการเลเยอร์ภายในไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java แล้ว ด้วยการสร้างเอกสาร, เพิ่มเลเยอร์, ล้างพื้นหลัง, และวาดด้วย API `Graphics` คุณสามารถทำงานอัตโนมัติหลายงานด้านการออกแบบกราฟิกบนเซิร์ฟเวอร์ได้ ลองทดลองใช้ปากกา, แปรง, และเอฟเฟกต์เลเยอร์ต่าง ๆ เพื่อขยายพื้นฐานนี้ให้เป็นไพพ์ไลน์การสร้างภาพที่ครบวงจร

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [วิธีวาดรูปทรง Java – การดำเนินการภาพพื้นฐาน](/psd/java/basic-image-operations/)
- [การปรับขนาดอย่างง่ายด้วย Aspose.PSD – ไลบรารีการจัดการภาพ Java](/psd/java/basic-image-operations/simple-resizing/)
- [ตัดภาพด้วยสี่เหลี่ยมใน Aspose.PSD สำหรับ Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**อัปเดตล่าสุด:** 2026-06-13  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**ผู้เขียน:** Aspose