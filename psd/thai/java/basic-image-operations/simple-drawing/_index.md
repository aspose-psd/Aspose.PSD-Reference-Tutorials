---
title: ดำเนินการวาดภาพอย่างง่ายด้วย Aspose.PSD สำหรับ Java
linktitle: ดำเนินการวาดภาพอย่างง่าย
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีการวาดรูปทรงในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java คำแนะนำทีละขั้นตอนนี้ครอบคลุมถึงการสร้าง การเพิ่มเลเยอร์ และการวาดภาพพร้อมตัวอย่างโค้ด
weight: 10
url: /th/java/basic-image-operations/simple-drawing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดำเนินการวาดภาพอย่างง่ายด้วย Aspose.PSD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนในการวาดภาพอย่างง่ายโดยใช้ Aspose.PSD สำหรับ Java! ในบทช่วยสอนนี้ เราจะสำรวจพื้นฐานของการสร้างเอกสาร PSD ใหม่ การเพิ่มเลเยอร์ และการวาดรูปร่างด้วยสีที่ต่างกัน Aspose.PSD สำหรับ Java เป็นไลบรารีอันทรงพลังที่ช่วยให้คุณสามารถจัดการไฟล์ PSD โดยทางโปรแกรม โดยมีฟังก์ชันการทำงานที่ครอบคลุมสำหรับงานออกแบบกราฟิก

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ติดตั้ง Java Development Kit (JDK) บนเครื่องของคุณแล้ว
- Aspose.PSD สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[Aspose.PSD สำหรับเอกสาร Java](https://reference.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ รวมรหัสต่อไปนี้ไว้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

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

เริ่มต้นด้วยการสร้างเอกสาร PSD ใหม่โดยระบุความกว้างและความสูง:

```java
//ExStart:สร้างเอกสาร
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ตัวอย่าง:สร้างเอกสาร
```

## ขั้นตอนที่ 2: เพิ่มเลเยอร์

ตอนนี้ เรามาเพิ่มเลเยอร์ให้กับเอกสารโดยใช้ตัวสร้างแบบไม่มีอาร์กิวเมนต์:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## ขั้นตอนที่ 3: วาดรูปร่าง

ในขั้นตอนนี้ เราจะใช้คลาส Graphics เพื่อวาดรูปร่างบนเลเยอร์ที่สร้างขึ้น:

### วาดรูปสี่เหลี่ยมผืนผ้าด้วยสีเหลือง

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ตัวอย่างสิ้นสุด:DrawRectangleYellow
```

### วาดรูปสี่เหลี่ยมสีแดง

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ตัวอย่างEnd:DrawRedRectangle
```

### วาดรูปสี่เหลี่ยมผืนผ้าสีน้ำเงิน

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ตัวอย่างEnd:DrawBlueRectangle
```

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลง

สุดท้าย ให้บันทึกสำเนาของไฟล์ PSD ที่โหลด รวมถึงการเปลี่ยนแปลง:

```java
//ExStart:บันทึกการเปลี่ยนแปลง
image.save(outPsdFilePath);
//ExEnd:บันทึกการเปลี่ยนแปลง
```

## บทสรุป

ยินดีด้วย! คุณวาดภาพอย่างง่ายโดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว บทช่วยสอนนี้ครอบคลุมถึงการสร้างเอกสารใหม่ การเพิ่มเลเยอร์ และการวาดสี่เหลี่ยมด้วยสีต่างๆ สำรวจคุณสมบัติขั้นสูงเพิ่มเติมที่ห้องสมุดนำเสนอตามความต้องการด้านการออกแบบกราฟิกของคุณได้อย่างอิสระ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD สำหรับ Java เพื่อจัดการไฟล์ PSD ที่มีอยู่ได้หรือไม่

ตอบ 1: ใช่ Aspose.PSD สำหรับ Java มีฟังก์ชันการทำงานที่ครอบคลุมในการแก้ไขและจัดการไฟล์ PSD ที่มีอยู่

### คำถามที่ 2: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A2: คุณสามารถเยี่ยมชม[Aspose.PSD สำหรับฟอรัม Java](https://forum.aspose.com/c/psd/34) สำหรับคำถามที่เกี่ยวข้องกับการสนับสนุน

### คำถามที่ 3: Aspose.PSD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถเข้าถึงเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A4: คุณสามารถซื้อใบอนุญาตได้จาก[หน้าการซื้อ Aspose.PSD](https://purchase.aspose.com/buy).

### คำถามที่ 5: Aspose.PSD สำหรับ Java มีใบอนุญาตชั่วคราวหรือไม่

 A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
