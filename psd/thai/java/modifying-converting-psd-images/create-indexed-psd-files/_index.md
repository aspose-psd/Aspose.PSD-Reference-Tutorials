---
date: 2026-03-15
description: เรียนรู้วิธีสร้างไฟล์ PSD, สร้างพาเล็ตสี PSD และตั้งค่าโหมดสี PSD ด้วย
  Aspose.PSD for Java ในคู่มือขั้นตอนต่อขั้นตอนนี้.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: วิธีสร้างไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java
url: /th/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java

## บทนำ
หากคุณเคยสงสัย **วิธีสร้างไฟล์ PSD** ด้วยโปรแกรม คุณมาถูกที่แล้ว Aspose.PSD สำหรับ Java ให้คุณควบคุมเอกสาร Photoshop ได้อย่างเต็มที่ สามารถสร้าง แก้ไข และบันทึกไฟล์ PSD ได้โดยไม่ต้องเปิด Photoshop ในบทเรียนนี้เราจะอธิบายขั้นตอนการสร้างไฟล์ **indexed PSD** ตั้งค่าโหมดสีของ PSD และสร้างพาเลตสีแบบกำหนดเอง—ทั้งหมดด้วยโค้ด Java ที่ชัดเจนเป็นขั้นตอน ไม่ว่าคุณจะสร้างกราฟิกไพพ์ไลน์ อัตโนมัติการสร้างแอสเซ็ต หรือแค่ทดลองเล่น แนวคิดเหล่านี้จะช่วยให้คุณทำให้ไอเดียภาพของคุณเป็นจริง

## คำตอบสั้น ๆ
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD สำหรับ Java  
- **สามารถสร้าง indexed PSD ได้หรือไม่?** ได้ โดยตั้งค่าโหมดสีเป็น `Indexed`  
- **ต้องติดตั้ง Photoshop ไหม?** ไม่จำเป็น Aspose.PSD ทำงานอิสระจาก Photoshop  
- **ต้องใช้ Java เวอร์ชันใด?** JDK 8 หรือใหม่กว่า  
- **ขนาดแคนวาสสูงสุดเท่าไร?** ใด ๆ ก็ได้; ตัวอย่างนี้ใช้ 500 × 500 px  

## Indexed PSD คืออะไร?
Indexed PSD จะเก็บสีในพาเลตแทนการเก็บค่าระดับสีเต็มสำหรับแต่ละพิกเซล ซึ่งช่วยลดขนาดไฟล์และเหมาะกับกราฟิกที่มีสีจำกัด เช่น ไอคอนหรือแอสเซ็ต UI การสร้างพาเลตสีแบบกำหนดเองทำให้คุณควบคุมสีที่ปรากฏในภาพสุดท้ายได้อย่างแม่นยำ

## ทำไมต้องสร้างพาเลตสี PSD?
การสร้าง **พาเลตสี PSD** ช่วยให้คุณ:
- ลดขนาดไฟล์สำหรับการใช้งานบนเว็บหรือมือถือ  
- รักษาความสอดคล้องของแบรนด์โดยจำกัดสีให้ตรงกับพาเลตขององค์กร  
- เร่งความเร็วในการเรนเดอร์ในแอปพลิเคชันที่รองรับภาพแบบ indexed  

## สิ่งที่ต้องเตรียม
ก่อนจะลงมือเขียนโค้ด ตรวจสอบว่าคุณมีสิ่งต่อไปนี้แล้ว:

1. **ความรู้พื้นฐานของ Java** – ควรคุ้นเคยกับคลาส เมธอด และการสร้างอ็อบเจกต์  
2. **Java Development Kit (JDK) 8+** – ติดตั้งและตั้งค่าใน IDE ของคุณแล้ว  
3. **IDE (IntelliJ IDEA, Eclipse ฯลฯ)** – ไม่บังคับแต่แนะนำเพื่อการดีบักที่ง่ายขึ้น  
4. **Aspose.PSD สำหรับ Java Library** – ดาวน์โหลด **[ที่นี่](https://releases.aspose.com/psd/java/)** แล้วเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจกต์  
5. **ความเข้าใจพื้นฐานด้านการออกแบบกราฟิก** – รู้เรื่องโหมดสี พาเลต และรูปทรงพื้นฐานจะช่วยให้ตามได้ง่ายขึ้น  

## นำเข้าแพ็กเกจ
ก่อนจะเขียนโค้ด ให้แน่ใจว่าได้นำเข้าแพ็กเกจที่จำเป็นทั้งหมดเข้าสู่แอปพลิเคชัน Java ของคุณ ตัวอย่างดังนี้:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

การนำเข้าดังกล่าวทำให้คุณสามารถทำงานกับตัวเลือก PSD สีและการจัดการกราฟิกผ่าน Aspose.PSD ได้

ต่อไปเราจะอธิบายโค้ด **วิธีสร้างไฟล์ PSD** ด้วยโหมดสี indexed ทีละขั้นตอน

## ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์เอกสาร
กำหนดตำแหน่งที่ไฟล์ PSD ที่สร้างขึ้นจะถูกบันทึก

```java
String dataDir = "Your Document Directory";
```

เปลี่ยน `"Your Document Directory"` เป็นพาธแบบ absolute หรือ relative เช่น `"/Users/YourName/Documents/"`

## ขั้นตอนที่ 2: สร้างอินสแตนซ์ของ PsdOptions
`PsdOptions` เก็บการตั้งค่าต่าง ๆ ของไฟล์ที่คุณกำลังจะสร้าง

```java
PsdOptions createOptions = new PsdOptions();
```

## ขั้นตอนที่ 3: ตั้งค่าคุณสมบัติหลักของ PsdOptions
ที่นี่เรากำหนดตำแหน่งไฟล์ผลลัพธ์, **ตั้งค่าโหมดสีของ PSD** เป็น `Indexed` และเวอร์ชันของ PSD

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – พาธเต็มของไฟล์ใหม่  
- **Color Mode** – `Indexed` บอก Aspose.PSD ให้ใช้ภาพแบบพาเลต  
- **Version** – เวอร์ชันฟอร์แมต PSD (5 ทำงานได้กับ Photoshop รุ่นใหม่ส่วนใหญ่)  

## ขั้นตอนที่ 4: สร้างพาเลตสี (Generate PSD Color Palette)
กำหนดสีที่สามารถใช้ในภาพ indexed

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- อาร์เรย์ `palette` สามารถเก็บได้สูงสุด 256 อ็อบเจกต์ `Color`  
- `CompressionMethod.RLE` ให้การบีบอัดแบบ lossless ที่มีประสิทธิภาพสำหรับภาพ indexed  

## ขั้นตอนที่ 5: สร้างแคนวาสภาพ PSD
สร้าง PSD เปล่าที่มีขนาดตามที่ต้องการ

```java
Image psd = Image.create(createOptions, 500, 500);
```

โค้ดนี้สร้างแคนวาสขนาด 500 × 500 พิกเซลโดยใช้พาเลตที่กำหนดไว้ก่อนหน้า

## ขั้นตอนที่ 6: วาดกราฟิกบน PSD
เพิ่มเนื้อหาภาพ – ตัวอย่างนี้วาดวงรีสีแดงบนพื้นหลังสีขาว

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` เติมพื้นหลังด้วยสีขาว  
- `drawEllipse` วาดวงรีสีแดงด้วยเส้นกว้าง 6 พิกเซล  

## ขั้นตอนที่ 7: บันทึกไฟล์ PSD
สุดท้ายบันทึกภาพลงดิสก์

```java
psd.save();
```

ไฟล์ `Newsample_out.psd` จะปรากฏในโฟลเดอร์ที่คุณระบุไว้ข้างต้น

## ปัญหาที่พบบ่อยและเคล็ดลับ
- **ขนาดพาเลต** – หากต้องการสีมากกว่า 4 สี เพียงเพิ่มลงในอาร์เรย์ `palette` (สูงสุด 256)  
- **สิทธิ์การเขียนไฟล์** – ตรวจสอบให้แน่ใจว่าโปรเซส Java มีสิทธิ์เขียนไปยัง `dataDir`  
- **โหมดสีไม่ถูกต้อง** – หากลืมเรียก `createOptions.setColorMode(ColorModes.Indexed)` จะได้ไฟล์ PSD แบบ RGB แทนที่เป็น indexed  

## คำถามที่พบบ่อย

**Q: Aspose.PSD สำหรับ Java คืออะไร?**  
A: Aspose.PSD สำหรับ Java เป็นไลบรารีที่ช่วยให้คุณจัดการไฟล์ PSD (Photoshop) ด้วย Java อย่างโปรแกรมเมติก

**Q: สามารถใช้ Aspose.PSD ได้ฟรีหรือไม่?**  
A: ใช่ คุณสามารถเข้าถึงเวอร์ชันทดลองฟรีของ Aspose.PSD **[ที่นี่](https://releases.aspose.com/)**

**Q: จำเป็นต้องติดตั้ง Photoshop เพื่อใช้ Aspose.PSD หรือไม่?**  
A: ไม่จำเป็น คุณสามารถสร้างและแก้ไขไฟล์ PSD ได้โดยไม่ต้องมี Photoshop เนื่องจาก Aspose.PSD ทำงานอิสระทั้งหมด

**Q: จะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: คุณสามารถขอรับไลเซนส์ชั่วคราว **[ที่นี่](https://purchase.aspose.com/temporary-license/)**

**Q: จะขอรับการสนับสนุนสำหรับ Aspose.PSD ได้จากที่ไหน?**  
A: คุณสามารถรับการสนับสนุนจากฟอรั่มของ Aspose **[ที่นี่](https://forum.aspose.com/c/psd/34)**

## สรุป
คุณได้เรียนรู้ **วิธีสร้างไฟล์ PSD** ด้วยโหมดสี indexed สร้างพาเลตสีแบบกำหนดเอง และเพิ่มกราฟิกง่าย ๆ ทั้งหมดโดยใช้ Aspose.PSD สำหรับ Java ด้วยบล็อกพื้นฐานเหล่านี้ คุณสามารถต่อยอดไปสู่การวาดที่ซับซ้อนขึ้น การจัดการเลเยอร์ และการประมวลผลเป็นชุด สำหรับการสำรวจเพิ่มเติม ดูเอกสารอ้างอิง API อย่างเป็นทางการ **[ที่นี่](https://reference.aspose.com/psd/java/)** และทดลองกับพาเลตและ primitive การวาดต่าง ๆ

---

**อัปเดตล่าสุด:** 2026-03-15  
**ทดสอบกับ:** Aspose.PSD สำหรับ Java 24.12 (ล่าสุด)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}