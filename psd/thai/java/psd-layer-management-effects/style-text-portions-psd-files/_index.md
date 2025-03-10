---
title: ส่วนข้อความสไตล์ในไฟล์ PSD โดยใช้ Java
linktitle: ส่วนข้อความสไตล์ในไฟล์ PSD โดยใช้ Java
second_title: Aspose.PSD Java API
description: การจัดรูปแบบข้อความ PSD ต้นแบบด้วย Aspose.PSD สำหรับ Java เรียนรู้วิธีแก้ไข สร้าง และจัดสไตล์ส่วนข้อความได้อย่างง่ายดาย ปรับปรุงการออกแบบ PSD ของคุณ
weight: 22
url: /th/java/psd-layer-management-effects/style-text-portions-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่วนข้อความสไตล์ในไฟล์ PSD โดยใช้ Java

## การแนะนำ

เคยต้องการที่จะเพิ่มอุ้บพิเศษนั้นให้กับเลเยอร์ข้อความของคุณในไฟล์ PSD หรือไม่? Aspose.PSD สำหรับ Java ไม่เพียงแต่ให้พลังแก่คุณในการไม่เพียงแค่จัดการข้อความ แต่ยังจัดสไตล์แต่ละส่วนได้อย่างแม่นยำอย่างเหลือเชื่อ คู่มือที่ครอบคลุมนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอน ตั้งแต่การตั้งค่าสภาพแวดล้อมไปจนถึงการสร้างองค์ประกอบข้อความที่มีสไตล์สวยงามภายใน PSD ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำน้ำ ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- Java Development Kit (JDK): คุณจะต้องติดตั้ง JDK บนระบบของคุณเพื่อรันโค้ดที่เราจะสำรวจ ตรวจสอบเว็บไซต์ Java ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)) สำหรับคำแนะนำการดาวน์โหลดและการติดตั้ง
- Aspose.PSD สำหรับไลบรารี Java: ไลบรารีนี้ช่วยให้คุณสามารถโต้ตอบกับไฟล์ PSD โดยทางโปรแกรม ตรงไปที่เว็บไซต์ Aspose ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)เพื่อดาวน์โหลดไลบรารี โปรดจำไว้ว่า คุณจะต้องมีใบอนุญาตเพื่อใช้ฟังก์ชันการทำงานเต็มรูปแบบ แต่คุณสามารถทดลองใช้งานฟรีเพื่อเริ่มต้นใช้งานได้

## แพ็คเกจนำเข้า

เมื่อคุณตั้งค่าทุกอย่างเรียบร้อยแล้ว ให้เปิด Java IDE ที่คุณชื่นชอบและเริ่มเขียนโค้ด ขั้นตอนแรกคือการนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.PSD สำหรับ Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.fileformats.psd.layers.text.IText;
import com.aspose.psd.fileformats.psd.layers.text.ITextParagraph;
import com.aspose.psd.fileformats.psd.layers.text.ITextPortion;
import com.aspose.psd.fileformats.psd.layers.text.ITextStyle;
import com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline;
import com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps;
```

การนำเข้าเหล่านี้ทำให้เราสามารถเข้าถึงคลาสและฟังก์ชันการทำงานที่จำเป็นในการทำงานกับไฟล์ PSD

เอาล่ะ มาดูความมหัศจรรย์ของจริงกันดีกว่า! ต่อไปนี้เป็นรายละเอียดขั้นตอนที่เกี่ยวข้องกับการจัดสไตล์ส่วนข้อความภายในไฟล์ PSD:

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

ก่อนอื่น เราต้องโหลดไฟล์ PSD ที่มีเลเยอร์ข้อความที่เราต้องการแก้ไข ต่อไปนี้เป็นวิธีดำเนินการ:

```java
String sourceDir = "yourSourceDirectory";
String inPsdFilePath = sourceDir + "text212.psd";

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

ข้อมูลโค้ดนี้กำหนดเส้นทางไปยังไฟล์ PSD ต้นฉบับของคุณ (`inPsdFilePath` ) จากนั้นใช้`Image.load` วิธีโหลดไฟล์เป็น`PsdImage` วัตถุ.

## ขั้นตอนที่ 2: การเข้าถึงเลเยอร์ข้อความ

ไฟล์ PSD สามารถมีเลเยอร์ประเภทต่างๆ ได้ ในการทำงานกับข้อความโดยเฉพาะ เราจำเป็นต้องเข้าถึงออบเจ็กต์เลเยอร์ข้อความ มีวิธีดังนี้:

```java
TextLayer textLayer = (TextLayer)psdImage.getLayers()[1];
```

รหัสนี้ถือว่าคุณต้องการแก้ไขข้อความในเลเยอร์แรก (`psdImage.getLayers()[1]`- โปรดจำไว้ว่าลำดับเลเยอร์ในไฟล์ PSD อาจแตกต่างกัน ดังนั้นให้ปรับดัชนีให้เหมาะสมหากเลเยอร์ข้อความของคุณอยู่ในตำแหน่งอื่น

## ขั้นตอนที่ 3: การทำงานกับข้อมูลข้อความ

 ที่`TextLayer` วัตถุเก็บข้อมูลทั้งหมดเกี่ยวกับเนื้อหาข้อความและการจัดรูปแบบ เราสามารถเข้าถึงข้อมูลนี้ผ่านทาง`getTextData` วิธี:

```java
IText textData = textLayer.getTextData();
```

 ที่`IText`วัตถุ (`textData`) แสดงถึงเนื้อหาต้นฉบับของเลเยอร์ มีฟังก์ชันการทำงานเพื่อจัดการข้อความและสไตล์ของข้อความ

## ขั้นตอนที่ 4: การกำหนดสไตล์เริ่มต้น (ไม่บังคับ)

แม้ว่าจะไม่จำเป็นอย่างเคร่งครัด แต่การกำหนดสไตล์เริ่มต้นสำหรับข้อความและย่อหน้าสามารถปรับปรุงเวิร์กโฟลว์ของคุณได้ วิธีนี้ช่วยให้คุณกำหนดสไตล์พื้นฐานที่คุณสามารถแทนที่ส่วนที่ต้องการได้อย่างง่ายดาย:

```java
ITextStyle defaultStyle = textData.producePortion().getStyle();
defaultStyle.setFillColor(Color.getDimGray());
defaultStyle.setFontSize(51);

ITextParagraph defaultParagraph = textData.producePortion().getParagraph();
```

 รหัสนี้จะสร้างรหัสใหม่`ITextStyle`วัตถุ (`defaultStyle` ) และตั้งค่าคุณสมบัติ เช่น สีเติม และขนาดตัวอักษร ในทำนองเดียวกันใหม่`ITextParagraph`วัตถุ (`defaultParagraph`) ถูกสร้างขึ้นเพื่อกำหนดการตั้งค่าย่อหน้าเริ่มต้น

## ขั้นตอนที่ 5: จัดสไตล์ส่วนข้อความที่มีอยู่

สมมติว่าคุณต้องการเพิ่มเอฟเฟกต์ขีดทับให้กับส่วนเฉพาะของข้อความที่มีอยู่ในเลเยอร์ ต่อไปนี้คือวิธีการบรรลุเป้าหมายดังกล่าว:

```java
textData.getItems()[1].getStyle().setStrikethrough(true);
```

รหัสนี้ดึงส่วนข้อความที่สอง (`textData.getItems()[1]` ) และตั้งค่าของมัน`strikethrough`ทรัพย์สินเพื่อ`true` - คุณสามารถเข้าถึงส่วนอื่นๆ ในทำนองเดียวกันและแก้ไขสไตล์โดยใช้วิธีการต่างๆ ที่จัดทำโดย`ITextStyle` อินเตอร์เฟซ

## ขั้นตอนที่ 6: การสร้างส่วนข้อความใหม่ด้วยสไตล์

ต้องการเพิ่มองค์ประกอบข้อความใหม่โดยใช้สไตล์เฉพาะตั้งแต่เริ่มต้นหรือไม่ Aspose.PSD สำหรับ Java ให้คุณทำเช่นนั้นได้เช่นกัน!

```java
String[] newTextStrings = {"E=mc2", "Bold", "Italic", "Lowercasetext"};
ITextPortion[] newTextPortions = textData.producePortions(newTextStrings, defaultStyle, defaultParagraph);
```

รหัสนี้สร้างอาร์เรย์ของสตริง (`newTextStrings` ) ที่มีเนื้อหาข้อความสำหรับส่วนใหม่ แล้วมันก็ใช้`textData.producePortions` เพื่อสร้างอาร์เรย์ของ`ITextPortion` วัตถุการประยุกต์ใช้`defaultStyle` และ`defaultParagraph` ในแต่ละส่วน

## ขั้นตอนที่ 7: การปรับแต่งส่วนข้อความใหม่

เมื่อคุณมีส่วนข้อความใหม่แล้ว คุณสามารถใช้สไตล์เฉพาะกับแต่ละส่วนได้:

```java
newTextPortions[0].getStyle().setUnderline(true); // ขีดเส้นใต้สำหรับ "E=mc2"
newTextPortions[1].getStyle().setFauxBold(true); // ตัวหนาสำหรับ "ตัวหนา"
newTextPortions[2].getStyle().setFauxItalic(true); // ตัวเอียงสำหรับ "ตัวเอียง"
newTextPortions[3].getStyle().setFontCaps(FontCaps.SmallCaps); //ตัวพิมพ์เล็กสำหรับ "ข้อความตัวพิมพ์เล็ก"
```

ที่นี่ เรากำลังปรับแต่งสไตล์ของส่วนข้อความใหม่สามส่วนแรก คุณสามารถใช้ตัวเลือกสไตล์ต่างๆ ได้ตามความต้องการของคุณ

## ขั้นตอนที่ 8: การเพิ่มส่วนข้อความใหม่ลงในเลเยอร์

หลังจากปรับแต่งส่วนข้อความใหม่แล้ว คุณต้องเพิ่มส่วนเหล่านั้นลงในเลเยอร์ข้อความ:

```java
for (ITextPortion newTextPortion : newTextPortions) {
    textData.addPortion(newTextPortion);
}
```

 รหัสนี้วนซ้ำผ่าน`newTextPortions` อาร์เรย์และเพิ่มแต่ละส่วนใน`textData` วัตถุ.

## ขั้นตอนที่ 9: การใช้การเปลี่ยนแปลงกับเลเยอร์

เพื่อให้สอดคล้องกับการแก้ไขข้อมูลข้อความในเลเยอร์ PSD คุณต้องอัปเดตเลเยอร์:

```java
textData.updateLayerData();
```

 การโทรนี้จะอัปเดตไฟล์`textLayer` กับการเปลี่ยนแปลงที่เกิดขึ้นกับ`textData`.

## ขั้นตอนที่ 10: บันทึกไฟล์ PSD ที่แก้ไข

สุดท้าย ให้บันทึกไฟล์ PSD ที่แก้ไขไปยังตำแหน่งใหม่:

```java
String outputDir = "yourOutputDirectory";
String outPsdFilePath = outputDir + "Output_text212.psd";

psdImage.save(outPsdFilePath);
```

 รหัสนี้สร้างเส้นทางไฟล์เอาต์พุตและบันทึกไฟล์`psdImage` คัดค้านไปยังตำแหน่งที่ระบุ

## บทสรุป

และคุณก็ได้แล้ว! คุณจัดสไตล์ส่วนข้อความภายในไฟล์ PSD ได้สำเร็จโดยใช้ Aspose.PSD สำหรับ Java ด้วยการทำตามขั้นตอนเหล่านี้และสำรวจตัวเลือกสไตล์ต่างๆ ที่มี คุณสามารถสร้างองค์ประกอบข้อความที่ปรับแต่งและดึงดูดสายตาใน PSD ของคุณได้

จำไว้ว่านี่เป็นเพียงจุดเริ่มต้นเท่านั้น Aspose.PSD สำหรับ Java มีฟังก์ชันการทำงานที่หลากหลายสำหรับการจัดการข้อความ รวมถึงการจัดรูปแบบขั้นสูง การควบคุมย่อหน้า และอื่นๆ อีกมากมาย ทดลองและปลดปล่อยความคิดสร้างสรรค์ของคุณเพื่อให้ได้ผลลัพธ์ตามที่ต้องการ!

## คำถามที่พบบ่อย

### ฉันสามารถเปลี่ยนแบบอักษรของส่วนข้อความเฉพาะได้หรือไม่
 ใช่ คุณสามารถเปลี่ยนแบบอักษรของส่วนข้อความได้โดยใช้`setFontName` วิธีการของ`ITextStyle` วัตถุ.

### ฉันจะปรับการจัดแนวข้อความภายในย่อหน้าได้อย่างไร
 ที่`ITextParagraph` วัตถุมีคุณสมบัติเช่น`setAlignment` เพื่อควบคุมการจัดแนวข้อความภายในย่อหน้า

### เป็นไปได้ไหมที่จะแก้ไขระยะห่างอักขระของข้อความ?
 ใช่ คุณสามารถปรับระยะห่างระหว่างอักขระได้โดยใช้`setCharacterSpacing` วิธีการของ`ITextStyle` วัตถุ.

### ฉันสามารถใช้สไตล์ที่แตกต่างกันกับส่วนต่างๆ ของส่วนข้อความเดียวได้หรือไม่
แม้ว่าจะไม่รองรับโดยตรง แต่คุณสามารถสร้างเอฟเฟกต์ที่คล้ายกันได้โดยการสร้างส่วนข้อความหลายส่วนภายในส่วนโดยรวมเดียวกัน

### มีข้อจำกัดเกี่ยวกับจำนวนส่วนข้อความหรืออักขระที่สามารถจัดการได้หรือไม่?
ข้อจำกัดในทางปฏิบัติขึ้นอยู่กับทรัพยากรระบบและความซับซ้อนของไฟล์ PSD อย่างไรก็ตาม Aspose.PSD สำหรับ Java ได้รับการออกแบบมาเพื่อจัดการไฟล์ PSD ขนาดใหญ่ได้อย่างมีประสิทธิภาพ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
