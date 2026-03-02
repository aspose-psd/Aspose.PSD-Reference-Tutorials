---
date: 2026-03-02
description: เรียนรู้วิธีเพิ่มการเติมสีโดยการสร้างเลเยอร์เติมสีในไฟล์ PSD ด้วย Java
  และ Aspose.PSD ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อกำหนดสีของเลเยอร์เติมอย่างรวดเร็ว.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'วิธีเพิ่มการเติมสี: เพิ่มเลเยอร์การเติมสีในไฟล์ PSD ด้วย Java'
url: /th/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มเลเยอร์สีเติมในไฟล์ PSD ด้วย Java

## บทนำ
เคยต้องการจัดการไฟล์ Photoshop ด้วยโปรแกรมบ้างไหม บางครั้งอาจต้องการเพิ่มสีสันให้กับการออกแบบ? หากคุณกำลังสงสัย **วิธีเพิ่มสีเติม** ในไฟล์ PSD คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายขั้นตอนการเพิ่มเลเยอร์สีเติมในไฟล์ PSD (Photoshop Document) ด้วย Java และไลบรารี Aspose.PSD คิดว่า PSD ของคุณเป็นผ้าใบดิจิทัล—เมื่อจบคุณจะรู้วิธีสร้างเลเยอร์สีเติม ตั้งค่าสีของเลเยอร์เติม และบันทึกไฟล์ที่อัปเดตด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD for Java  
- **กรณีการใช้งานหลัก?** เพิ่มหรือเปลี่ยนสีเติมใน PSD ด้วยโปรแกรม  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ประมาณ 10‑15 นาทีสำหรับสถานการณ์พื้นฐาน  
- **ต้องการไลเซนส์หรือไม่?** สามารถใช้รุ่นทดลองฟรีเพื่อประเมิน; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **เวอร์ชัน Java ที่รองรับ?** Java 8 ขึ้นไป  

## เลเยอร์สีเติมคืออะไร?
เลเยอร์สีเติมคือการวางซ้อนสีทึบที่อยู่บนเลเยอร์อื่น ๆ ในเอกสาร Photoshop มักใช้เพื่อเพิ่มสีพื้นหลัง สร้างมาสก์ หรือเปลี่ยนธีมภาพของการออกแบบอย่างรวดเร็วโดยไม่ต้องแก้ไขพิกเซลแต่ละจุด

## ทำไมต้องเพิ่มเลเยอร์สีเติมด้วยโค้ด?
- **อัตโนมัติ:** สร้างสินทรัพย์แบรนด์ที่สอดคล้องกันในหลายไฟล์  
- **การประมวลผลเป็นชุด:** อัปเดตหลายสิบไฟล์ PSD ภายในไม่กี่วินาที แทนการทำด้วยมือ  
- **การออกแบบแบบไดนามิก:** เปลี่ยนสีได้ทันทีตามข้อมูลหรือการป้อนของผู้ใช้  

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงลึกในโค้ด ให้แน่ใจว่าคุณมีทุกอย่างที่จำเป็น:

1. **Java Development Kit (JDK)** – ติดตั้ง JDK 8 หรือใหม่กว่า  
2. **Aspose.PSD Library** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose Releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans หรือเครื่องมือแก้ไขใด ๆ ที่คุณชอบ  
4. **ความรู้พื้นฐาน Java** – คุ้นเคยกับอ็อบเจ็กต์, ลูป, และการจัดการข้อยกเว้น  

## นำเข้าแพ็กเกจ
เมื่อเราครอบคลุมพื้นฐานแล้ว ให้ทำการนำเข้าคลาสที่จำเป็น การนำเข้าตัวนี้ทำให้เราสามารถจัดการ PSD และการจัดการเลเยอร์สีเติมได้

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## วิธีเพิ่มสีเติม – คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อมของคุณ
กำหนดตำแหน่งที่เก็บ PSD ต้นฉบับและที่ที่ไฟล์ที่แก้ไขจะถูกบันทึก จากนั้นโหลดเอกสาร

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` ชี้ไปยังโฟลเดอร์ที่มี PSD ของคุณ  
- `sourceFileName` คือไฟล์ต้นฉบับที่คุณจะทำการแก้ไข  
- `exportPath` คือที่ที่ไฟล์ใหม่พร้อม **เพิ่มเลเยอร์สีเติม** จะถูกเขียนออก  

### ขั้นตอนที่ 2: วนลูปผ่านเลเยอร์ทั้งหมด
เราต้องค้นหาเลเยอร์สีเติมที่มีอยู่เพื่อที่เราจะสามารถแก้ไขหรือสร้างใหม่ได้

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- ลูป `for` จะวนซ้ำผ่านทุกเลเยอร์ใน PSD  
- การตรวจสอบ `instanceof FillLayer` ทำให้แน่ใจว่าเราทำงานเฉพาะกับเลเยอร์สีเติมเท่านั้น  

### ขั้นตอนที่ 3: ตรวจสอบประเภทของสีเติม
ตรวจสอบให้แน่ใจว่าเลเยอร์ที่พบเป็น **เลเยอร์สีเติม** ก่อนที่จะพยายามเปลี่ยนสีของมัน

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

หากประเภทสีเติมไม่ใช่ `FillType.Color` เราจะหยุดการทำงานเพื่อหลีกเลี่ยงการเปลี่ยนแปลงสีไล่ระดับหรือแพทเทิร์นโดยไม่ได้ตั้งใจ  

### ขั้นตอนที่ 4: ตั้งค่าสีของสีเติม
นี่คือขั้นตอนที่เราจะ **ตั้งค่าสีของเลเยอร์สีเติม** ตัวอย่างจะเปลี่ยนเลเยอร์เป็นสีแดง แต่คุณสามารถแทนที่ `Color.getRed()` ด้วย `Color` ใดก็ได้ที่ต้องการ (เช่น `Color.getBlue()`, `new Color(255, 165, 0)` สำหรับสีส้ม)

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` จะเปลี่ยนสีเติมจริง  
- `fillLayer.update()` จะรีเฟรชเลเยอร์เพื่อให้สีใหม่ถูกนำไปใช้  

### ขั้นตอนที่ 5: บันทึกการเปลี่ยนแปลง
สุดท้าย ให้เขียน PSD ที่แก้ไขแล้วกลับไปยังดิสก์

```java
im.save(exportPath);
break;
```

- คำสั่ง `break` จะหยุดลูปหลังจากอัปเดตเลเยอร์สีเติมที่ตรงกันครั้งแรก ซึ่งเป็นพฤติกรรมที่ต้องการเมื่อคุณต้องการ **เปลี่ยนสีเติมของ PSD** เพียงครั้งเดียว  

## ปัญหาที่พบบ่อยและเคล็ดลับ
- **ไม่พบ FillLayer:** หาก PSD ของคุณไม่มีเลเยอร์สีเติม คุณต้องสร้างใหม่โดยใช้ `new FillLayer(im)` และเพิ่มเข้าไปใน `im.getLayers()`  
- **สีไม่อัปเดต:** ตรวจสอบว่าคุณเรียก `fillLayer.update()` หลังจากตั้งค่าสี  
- **ไฟล์ไม่บันทึก:** ตรวจสอบว่า `exportPath` ชี้ไปยังไดเรกทอรีที่สามารถเขียนได้และคุณมีสิทธิ์เขียนไฟล์ในนั้น  

## คำถามที่พบบ่อย

**Q: Aspose.PSD คืออะไร?**  
A: Aspose.PSD เป็นไลบรารี Java ที่แข็งแกร่ง ช่วยให้คุณสร้าง แก้ไข และแปลงไฟล์ Photoshop PSD ได้โดยไม่ต้องใช้ Adobe Photoshop  

**Q: ฉันสามารถใช้ Aspose.PSD ฟรีได้หรือไม่?**  
A: ได้, มีรุ่นทดลองฟรีที่พร้อมใช้งานบน [Aspose Releases page](https://releases.aspose.com/).  

**Q: ฉันสามารถทำงานกับรูปแบบไฟล์ใดได้บ้างนอกจาก PSD?**  
A: Aspose.PSD รองรับ PSD, PSB, BMP, JPEG, PNG, GIF, TIFF และอื่น ๆ  

**Q: ฉันจะรับการสนับสนุนอย่างไรหากเจอปัญหา?**  
A: คุณสามารถถามคำถามได้ที่ [Aspose Support Forum](https://forum.aspose.com/c/psd/34).  

**Q: ฉันจะซื้อไลเซนส์เต็มได้จากที่ไหน?**  
A: ไลเซนส์จำหน่ายผ่าน [Aspose Purchase page](https://purchase.aspose.com/buy).  

## สรุป
ตอนนี้คุณรู้ **วิธีเพิ่มสีเติม** ในเอกสาร Photoshop ด้วยโปรแกรม Java แล้ว โดยการสร้างหรือค้นหาเลเยอร์สีเติม ตั้งค่าสีของมัน และบันทึกผลลัพธ์ คุณสามารถอัตโนมัติงานออกแบบที่ทำซ้ำ ๆ สร้างสินทรัพย์แบบไดนามิก หรือรวมการจัดการ PSD เข้าไปในแอปพลิเคชัน Java ขนาดใหญ่ ลองดู—ทดลองกับสีต่าง ๆ เพิ่มหลายเลเยอร์สีเติม หรือผสานเทคนิคนี้กับฟีเจอร์อื่นของ Aspose.PSD เพื่อสร้างกระบวนการประมวลผลภาพที่ทรงพลัง

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-03-02  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose