---
title: ใช้ Adobe Deflate Compression กับ TIFF - Java
linktitle: ใช้ Adobe Deflate Compression กับ TIFF - Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีใช้การบีบอัด Adobe Deflate กับอิมเมจ TIFF โดยใช้ Aspose.PSD สำหรับ Java คำแนะนำทีละขั้นตอนเพื่อการประมวลผลภาพที่มีประสิทธิภาพ
type: docs
weight: 12
url: /th/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---
## การแนะนำ

เคยสงสัยบ้างไหมว่าจะบีบอัดภาพ TIFF ของคุณอย่างมีประสิทธิภาพโดยไม่ลดคุณภาพลงได้อย่างไร หากคุณกำลังจัดการกับไฟล์ภาพขนาดใหญ่ คุณอาจทราบถึงความเจ็บปวดจากเวลาในการโหลดที่ช้าและปัญหาการจัดเก็บ นั่นคือจุดที่การบีบอัด Adobe Deflate เข้ามามีบทบาท และด้วย Aspose.PSD สำหรับ Java คุณสามารถนำไปใช้ในโครงการของคุณได้อย่างง่ายดาย บทช่วยสอนนี้จะแนะนำคุณเกี่ยวกับการใช้การบีบอัด Adobe Deflate กับรูปภาพ TIFF ทีละขั้นตอน พร้อมที่จะดำน้ำแล้วหรือยัง? มาเริ่มกันเลย!

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะพูดถึงโค้ดจริง เรามาตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าทุกอย่างเรียบร้อยแล้ว นี่คือสิ่งที่คุณต้องการ:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK เวอร์ชันล่าสุดบนเครื่องของคุณ
2.  Aspose.PSD สำหรับ Java: ดาวน์โหลดและรวมไลบรารี Aspose.PSD สำหรับ Java เข้ากับโปรเจ็กต์ของคุณ คุณสามารถรับได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนา: IDE เช่น IntelliJ IDEA, Eclipse หรือ NetBeans
4.  ใบอนุญาตชั่วคราว (ไม่บังคับ): หากคุณไม่พร้อมที่จะซื้อ คุณสามารถรับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อลองใช้คุณสมบัติต่างๆ

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณ การนำเข้าเหล่านี้มีความสำคัญเนื่องจากช่วยให้คุณสามารถทำงานกับไลบรารี Aspose.PSD และยูทิลิตี้ Java ได้

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

ตอนนี้เราได้พูดถึงข้อมูลพื้นฐานแล้ว เรามาแบ่งกระบวนการออกเป็นขั้นตอนที่ง่ายต่อการปฏิบัติตามกัน

## ขั้นตอนที่ 1: ตั้งค่าตัวเลือก TIFF

 ก่อนอื่นคุณต้องสร้างอินสแตนซ์ของ`TiffOptions` และกำหนดค่าตามความต้องการของคุณ ตัวเลือกเหล่านี้จะกำหนดวิธีการประมวลผลไฟล์ TIFF รวมถึงความละเอียด รูปแบบสี และการบีบอัด

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

ที่นี่เรากำลังสร้าง`TiffOptions` วัตถุที่มีรูปแบบเริ่มต้น แต่นั่นเป็นเพียงจุดเริ่มต้น! 

## ขั้นตอนที่ 2: กำหนดค่าคุณสมบัติรูปภาพ

 ถัดไป คุณจะต้องตั้งค่าคุณสมบัติต่างๆ ของรูปภาพ TIFF เช่น`BitsPerSample`, `Photometric`, `Resolution` , และ`PlanarConfiguration`- การตั้งค่าเหล่านี้จะกำหนดวิธีการจัดเก็บและแสดงข้อมูลภาพ

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

แต่ละพร็อพเพอร์ตี้ทำดังนี้:
- BitsPerSample: ตั้งค่าจำนวนบิตต่อตัวอย่างสำหรับแต่ละช่องสี
- โฟโตเมตริก: กำหนดโมเดลสี (ในกรณีนี้คือ RGB)
- ความละเอียด: ระบุความละเอียดแนวนอนและแนวตั้งของภาพ
- PlanarConfiguration: กำหนดวิธีจัดเก็บข้อมูลพิกเซล

## ขั้นตอนที่ 3: ใช้ Adobe Deflate Compression

มาถึงความมหัศจรรย์แล้ว! คุณจะใช้การบีบอัด Adobe Deflate กับภาพ TIFF ซึ่งช่วยลดขนาดไฟล์โดยไม่สูญเสียคุณภาพของภาพ

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

Adobe Deflate เป็นวิธีการบีบอัดแบบไม่สูญเสียข้อมูลซึ่งเหมาะสำหรับรูปภาพที่คุณต้องการรักษาคุณภาพสูงในขณะที่ลดขนาดไฟล์

## ขั้นตอนที่ 4: สร้างและแก้ไขภาพ TIFF

เมื่อตั้งค่าตัวเลือกแล้ว ก็ถึงเวลาสร้างภาพ TIFF ใหม่และปรับแต่งภาพ ในขั้นตอนนี้ เราจะสร้างรูปภาพธรรมดาขนาด 100x100 แล้วเติมด้วยพิกเซลสีแดง

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

ที่นี่ เรากำลังวนซ้ำแต่ละพิกเซลของภาพและตั้งค่าสีของภาพให้เป็นสีแดง แน่นอนคุณสามารถปรับแต่งส่วนนี้เพื่อสร้างภาพที่ซับซ้อนมากขึ้นได้

## ขั้นตอนที่ 5: บันทึกภาพ TIFF ที่บีบอัด

สุดท้าย หลังจากกำหนดค่าและสร้างอิมเมจแล้ว ขั้นตอนสุดท้ายคือบันทึกด้วยการบีบอัดที่ใช้ ตรวจสอบให้แน่ใจว่าคุณระบุเส้นทางไดเรกทอรีที่ถูกต้อง

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

แค่นั้นแหละ! คุณใช้การบีบอัด Adobe Deflate กับอิมเมจ TIFF โดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว

## บทสรุป

และคุณก็ได้แล้ว! การใช้การบีบอัด Adobe Deflate กับอิมเมจ TIFF เป็นกระบวนการที่ไม่ซับซ้อนกับ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะจัดการกับภาพขนาดใหญ่สำหรับเว็บไซต์ สื่อดิจิทัล หรือโครงการอื่น ๆ วิธีนี้ช่วยให้มั่นใจได้ว่าไฟล์ของคุณยังคงมีคุณภาพสูงในขณะที่ยังสามารถจัดการขนาดได้มากขึ้น พลังของ Aspose.PSD สำหรับ Java อยู่ที่ความเรียบง่ายและมีประสิทธิภาพ ทำให้เป็นเครื่องมือที่นำไปใช้ได้ง่ายสำหรับนักพัฒนาที่ทำงานกับรูปแบบภาพที่ซับซ้อน

## คำถามที่พบบ่อย

### การบีบอัด Adobe Deflate คืออะไร
Adobe Deflate เป็นวิธีการบีบอัดแบบไม่สูญเสียข้อมูลซึ่งใช้เพื่อลดขนาดของภาพ TIFF โดยไม่สูญเสียคุณภาพ

### ฉันสามารถใช้วิธีการบีบอัดอื่นกับ Aspose.PSD สำหรับ Java ได้หรือไม่
ใช่ Aspose.PSD รองรับวิธีการบีบอัดที่หลากหลาย เช่น LZW, CCITT และ JPEG

### ไลบรารี Aspose.PSD ฟรีหรือไม่
 Aspose.PSD ให้ทดลองใช้ฟรี แต่จำเป็นต้องมีใบอนุญาตเพื่อการใช้งานเต็มรูปแบบ คุณจะได้รับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อลองดู

### การตั้งค่าความละเอียดส่งผลต่อภาพ TIFF อย่างไร
ความละเอียดจะกำหนดความชัดเจนของภาพเมื่อพิมพ์หรือแสดง ความละเอียดที่สูงขึ้นจะให้คุณภาพที่ดีขึ้น แต่ส่งผลให้ขนาดไฟล์ใหญ่ขึ้น

### ฉันสามารถจัดการรูปแบบรูปภาพอื่นด้วย Aspose.PSD สำหรับ Java ได้หรือไม่
อย่างแน่นอน! Aspose.PSD รองรับรูปแบบต่างๆ เช่น PSD, PNG, JPEG และอื่นๆ