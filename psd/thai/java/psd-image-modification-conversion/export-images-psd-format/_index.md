---
date: 2026-03-23
description: เรียนรู้วิธีบันทึกรูปภาพเป็นไฟล์ PSD ด้วย Aspose.PSD for Java คู่มือแบบขั้นตอนเพื่อกำหนดโหมดสีของ
  PSD แปลงบิตแมปเป็น PSD และส่งออกภาพโดยอัตโนมัติผ่านโปรแกรม.
linktitle: Export Images to PSD Format with Java
second_title: Aspose.PSD Java API
title: วิธีบันทึกภาพเป็น PSD ด้วย Java โดยใช้ Aspose.PSD
url: /th/java/psd-image-modification-conversion/export-images-psd-format/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีบันทึกรูปภาพเป็น PSD ด้วย Java โดยใช้ Aspose.PSD

## วิธีบันทึกรูปภาพเป็น PSD ด้วย Java

ในบทเรียนนี้ คุณจะได้เรียนรู้ **วิธีบันทึกรูปภาพเป็น PSD** ด้วย Java และไลบรารี Aspose.PSD การทำงานกับไฟล์ Photoshop แบบหลายเลเยอร์เป็นงานประจำวันของนักพัฒนาออกแบบกราฟิกหลายคน และการทำอัตโนมัติการสร้างไฟล์ PSD สามารถเร่งกระบวนการทำงานได้อย่างมหาศาล เราจะอธิบายการตั้งค่าโหมดสีของ PSD การสร้าง bitmap และการแปลง bitmap ให้เป็นไฟล์ PSD — ทุกอย่างที่คุณต้องการเพื่อเริ่มต้นอย่างรวดเร็ว มาเริ่มกันเลย!

## คำตอบสั้น
- **ต้องการไลบรารีอะไร?** Aspose.PSD for Java (downloadable from the official site).  
- **ฉันสามารถตั้งค่าโหมดสีได้หรือไม่?** ใช่ – use `PsdOptions.setColorMode()` to choose RGB, CMYK, etc.  
- **การแปลง bitmap เป็น PSD รองรับหรือไม่?** Absolutely; create a `PsdImage` from dimensions or an existing bitmap and save it.  
- **ฉันต้องการลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** A commercial license is required for non‑trial use.  
- **ต้องการเวอร์ชัน Java ใด?** Java 8 หรือสูงกว่า.

## อะไรคือ “save image as PSD”?

การบันทึกรูปภาพเป็น PSD หมายถึงการส่งออกกราฟิกแบบแรสเตอร์ไปยังรูปแบบเลเยอร์ของ Adobe Photoshop ซึ่งทำให้เครื่องมือที่ตามมาภายหลัง (Photoshop, GIMP ฯลฯ) สามารถเก็บเลเยอร์, แชนแนล, และความสามารถในการแก้ไขได้ ด้วย Aspose.PSD คุณสามารถสร้างไฟล์ PSD ด้วยโปรแกรมโดยไม่ต้องเปิด Photoshop

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java?

- **การควบคุมเต็มรูปแบบ** บนโหมดสี, การบีบอัด, และความเข้ากันได้กับเวอร์ชัน Photoshop  
- **ไม่มีการพึ่งพาภายนอก** – เป็น Java แท้, เหมาะสำหรับการเรนเดอร์ฝั่งเซิร์ฟเวอร์  
- **ประสิทธิภาพสูง** – เหมาะสำหรับการประมวลผลเป็นชุดของภาพหลายพันภาพ  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **ความรู้พื้นฐานของ Java** – คุณควรคุ้นเคยกับการคอมไพล์และรันโปรแกรม Java  
2. **Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).  
3. **Java Development Kit (JDK)** – JDK 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณแล้ว  
4. **IDE หรือ Text Editor** – IntelliJ IDEA, Eclipse, VS Code หรือโปรแกรมแก้ไขใด ๆ ที่คุณชอบ  
5. **ความเข้าใจพื้นฐานเกี่ยวกับภาพ** – โหมดสี, การบีบอัด, และพื้นฐานของ bitmap จะช่วยได้แต่ไม่จำเป็น  

พร้อมหรือยัง? ดีมาก, ไปต่อกันเลย

## นำเข้าชุดคำสั่ง

ก่อนอื่น, ให้ import คลาสที่เราต้องการจากไลบรารี Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

การ import เหล่านี้ทำให้เราสามารถใช้ยูทิลิตี้การวาด, การจัดการสี, และตัวเลือกเฉพาะของ PSD ได้

## ขั้นตอนที่ 1: เริ่มต้นไดเรกทอรีเอกสารของคุณ

กำหนดตำแหน่งที่ไฟล์ PSD ที่สร้างจะถูกบันทึก:

```java
String dataDir = "Your Document Directory";
```

เปลี่ยน `"Your Document Directory"` เป็นพาธเต็ม เช่น `"C:/Images/"` หรือพาธสัมพันธ์ภายในโปรเจกต์ของคุณ

## ขั้นตอนที่ 2: สร้างภาพใหม่ (แปลง Bitmap เป็น PSD)

ตอนนี้เราจะสร้าง bitmap ว่างเปล่าที่ต่อมาเราจะ **แปลง bitmap เป็น PSD** โดยบันทึกด้วยตัวเลือก PSD:

```java
PsdImage bmpImage = new PsdImage(300, 300);
```

คุณสามารถเปลี่ยน `300, 300` ให้ตรงกับขนาดที่ต้องการได้ตามสะดวก

## ขั้นตอนที่ 3: เติมข้อมูลภาพ

เพิ่มกราฟิกบางอย่างลงใน bitmap เพื่อให้ PSD ที่ได้ไม่ใช่แค่แคนวาสเปล่า:

```java
Graphics graphics = new Graphics(bmpImage);
graphics.clear(Color.getWhite());
Pen pen = new Pen(Color.getBrown());
graphics.drawRectangle(pen, bmpImage.getBounds());
```

- `graphics.clear(Color.getWhite())` ระบายแคนวาสทั้งหมดเป็นสีขาว  
- ปากกาสีสีน้ำตาลวาดสี่เหลี่ยมที่เป็นขอบของภาพ  

## ขั้นตอนที่ 4: ตั้งค่า PSD Options (ตั้งค่าโหมดสี PSD)

ที่นี่เราตั้งค่าการบันทึกไฟล์ ซึ่งเป็นจุดที่เราจะ **ตั้งค่าโหมดสี PSD** เป็น RGB, เลือกการบีบอัด, และระบุเวอร์ชัน Photoshop:

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setColorMode(ColorModes.Rgb);
psdOptions.setCompressionMethod(CompressionMethod.Raw);
psdOptions.setVersion(4);
```

- `ColorModes.Rgb` – โหมดที่ใช้กันมากที่สุดสำหรับกราฟิกบนเว็บและหน้าจอ  
- `CompressionMethod.Raw` – เก็บข้อมูลพิกเซลโดยไม่มีการบีบอัดเพื่อคุณภาพสูงสุด  
- `setVersion(4)` – บันทึกไฟล์ในรูปแบบ Photoshop 4.0 ซึ่งเข้ากันได้อย่างกว้างขวาง  

## ขั้นตอนที่ 5: บันทึกภาพ

สุดท้าย, ส่งออก bitmap เป็นไฟล์ PSD — นี่คือการดำเนินการ **บันทึกรูปภาพเป็น PSD** หลัก:

```java
bmpImage.save(dataDir + "ExportImageToPSD_output.psd", psdOptions);
```

ไฟล์ `ExportImageToPSD_output.psd` จะปรากฏในไดเรกทอรีที่คุณระบุไว้

## กรณีการใช้งานทั่วไป

- **การสร้างรายงานอัตโนมัติ** ที่ต้องการให้แผนภูมิสามารถแก้ไขได้ใน Photoshop  
- **การแปลงเป็นชุด** ของไฟล์ PNG/JPEG ไปเป็น PSD สำหรับนักออกแบบที่ต้องการเลเยอร์  
- **การประกอบภาพฝั่งเซิร์ฟเวอร์** สำหรับบริการเว็บที่ส่งเทมเพลต PSD ให้กับลูกค้า  

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ไฟล์ไม่พบ** error when saving | Verify that `dataDir` ends with a path separator (`/` or `\\`) and that the folder exists. |
| **ภาพเปล่า** after saving | Ensure you called `graphics.clear()` and drew something before saving. |
| **โหมดสีไม่รองรับ** | Use `ColorModes.Cmyk` if you need CMYK output; remember to adjust your graphics accordingly. |
| **LicenseException** at runtime | Install a valid Aspose.PSD license or run in trial mode (evaluation watermark may appear). |

## คำถามที่พบบ่อย

**Q: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java is a robust API that enables developers to create, edit, convert, and render Photoshop PSD files without using Adobe Photoshop.

**Q: ฉันสามารถแก้ไขไฟล์ PSD ที่มีอยู่ได้หรือไม่?**  
A: Yes, you can open an existing PSD with `new PsdImage("input.psd")`, make changes, and save it back.

**Q: มีรุ่นทดลองฟรีหรือไม่?**  
A: Absolutely! You can download a free trial of Aspose.PSD [here](https://releases.aspose.com/).

**Q: ฉันจะหาเอกสารเพิ่มเติมได้จากที่ไหน?**  
A: You can check out the comprehensive [documentation](https://reference.aspose.com/psd/java/) to learn more about using Aspose.PSD.

**Q: จะขอรับการสนับสนุนหากเจอปัญหาคืออะไร?**  
A: For support, you can visit the [Aspose forum](https://forum.aspose.com/c/psd/34).

## สรุป

คุณได้เรียนรู้วิธี **บันทึกรูปภาพเป็น PSD** ด้วย Java, วิธี **ตั้งค่าโหมดสี PSD**, และวิธี **แปลง bitmap เป็น PSD** ด้วย Aspose.PSD วิธีนี้ให้คุณควบคุมไฟล์ Photoshop อย่างเต็มที่ เปิดประตูสู่การทำงานอัตโนมัติของการออกแบบ, การสร้างภาพแบบไดนามิก, และการผสานรวมอย่างราบรื่นกับแอปพลิเคชัน Java ที่มีอยู่แล้ว ทดลองใช้โหมดสี, ขนาด, และการวาดต่าง ๆ เพื่อปรับไฟล์ PSD ให้ตรงตามความต้องการของคุณ

---

**Last Updated:** 2026-03-23  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}