---
date: 2026-03-15
description: เรียนรู้วิธีกรองภาพ PNG ด้วย Aspose.PSD สำหรับ Java คู่มือแบบขั้นตอนนี้ครอบคลุมการเพิ่มประสิทธิภาพ
  PNG ใน Java และการแปลง PSD เป็น PNG พร้อมประเภทของฟิลเตอร์
linktitle: How to Filter PNG Files in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: วิธีกรองไฟล์ PNG ใน Aspose.PSD สำหรับ Java
url: /th/java/optimizing-png-files/apply-filters-png-files/
weight: 10
---

Now produce final content.

Let's craft translation.

We'll keep code block placeholders as they are.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีกรองไฟล์ PNG ด้วย Aspose.PSD สำหรับ Java

## บทนำ
หากคุณกำลังสงสัย **วิธีกรอง PNG** ขณะทำงานกับ Java คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะพาคุณผ่านการใช้ประเภทฟิลเตอร์ PNG กับ Aspose.PSD สำหรับ Java ซึ่งเป็นไลบรารีที่ช่วยคุณ **แปลง PSD เป็น PNG** และทำ **java png optimization** ด้วย เมื่อจบคุณจะสามารถปรับการบีบอัดให้เหมาะสม ปรับคุณภาพภาพให้ดีขึ้น และนำกระบวนการนี้ไปใช้ในโปรเจกต์ Java ใดก็ได้

## คำตอบสั้น
- **ไลบรารีใดที่รองรับการกรอง PNG ใน Java?** Aspose.PSD for Java.  
- **ฟิลเตอร์ใดให้การบีบอัดที่ดีที่สุดสำหรับภาพส่วนใหญ่?** ฟิลเตอร์ Paeth (ใช้ในตัวอย่างนี้).  
- **ต้องใช้ไลเซนส์เพื่อรันโค้ดหรือไม่?** สามารถใช้รุ่นทดลองฟรีเพื่อประเมินได้; ต้องมีไลเซนส์สำหรับการใช้งานจริง.  
- **สามารถแปลง PSD เป็น PNG ในขั้นตอนเดียวกันได้หรือไม่?** ได้ – โหลด PSD แล้วบันทึกเป็น PNG พร้อมฟิลเตอร์ที่ต้องการ.  
- **ต้องการ Java เวอร์ชันใด?** Java 8 หรือใหม่กว่า.

## “วิธีกรอง png” คืออะไรในทางปฏิบัติ?
การกรองไฟล์ PNG หมายถึงการเลือกอัลกอริทึมการเตรียมข้อมูลพิกเซลก่อนการบีบอัด ฟิลเตอร์ที่เลือกจะมีผลต่อขนาดไฟล์และการรักษาสีหลังจากบันทึก PNG Aspose.PSD ให้คุณควบคุมขั้นตอนนี้โดยตรงผ่านเมธอด `PngOptions.setFilterType`.

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java เพื่อทำการปรับแต่ง PNG?
- **รองรับ PSD อย่างเต็มรูปแบบ:** เปิด, แก้ไข, และส่งออกเลเยอร์ PSD โดยไม่สูญเสียคุณภาพ.  
- **เลือกฟิลเตอร์ในตัว:** มีให้เลือกจาก Paeth, Sub, Up, Average หรือ None.  
- **ข้ามแพลตฟอร์ม:** ทำงานบน Windows, Linux, และ macOS กับ JDK มาตรฐานใดก็ได้.  
- **ไม่มีการพึ่งพาไลบรารีเนทีฟภายนอก:** การทำงานแบบ Pure Java ทำให้การปรับใช้ง่ายขึ้น.

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK) 8+** – ตรวจสอบว่า `java -version` แสดง 1.8 หรือสูงกว่า.  
2. **IDE (IntelliJ IDEA, Eclipse, หรือ VS Code)** – สภาพแวดล้อมใดก็ได้ที่คุณถนัด.  
3. **Aspose.PSD for Java library** – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/).  
4. **ความรู้พื้นฐาน Java** – คุ้นเคยกับคลาส, เมธอด, และการทำ I/O ของไฟล์.

## นำเข้าแพ็กเกจ
แรกเริ่มให้เพิ่มคลาส Aspose.PSD ที่จำเป็นลงในไฟล์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngFilterType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

> **เคล็ดลับ:** เพิ่ม JAR ของ Aspose.PSD ไปยัง build path ของโปรเจกต์หรือ dependencies ของ Maven/Gradle เพื่อให้การนำเข้าถูกต้องโดยไม่มีข้อผิดพลาด.

## ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์เอกสาร
กำหนดโฟลเดอร์ที่เก็บ PSD ต้นฉบับและที่ต้องการบันทึก PNG ที่ผ่านการกรอง

```java
String dataDir = "Your Document Directory"; // Adjust this path
```

แทนที่ `"Your Document Directory"` ด้วยพาธแบบ absolute หรือ relative บนเครื่องของคุณ.

## ขั้นตอนที่ 2: โหลดภาพ PSD
เปิดไฟล์ PSD ที่ต้องการประมวลผล การแคสท์เป็น `PsdImage` จะให้ความสามารถเฉพาะของ PSD

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

หากไฟล์ไม่พบ `Image.load` จะโยนข้อยกเว้น – ตรวจสอบให้แน่ใจว่าพาธถูกต้อง.

## ขั้นตอนที่ 3: สร้าง PNG Options (Java PNG Optimization)
กำหนดค่าการส่งออก PNG รวมถึงประเภทฟิลเตอร์ที่ตอบโจทย์ **วิธีกรอง png** โดยตรง

```java
PngOptions options = new PngOptions();
options.setFilterType(PngFilterType.Paeth);
```

คุณสามารถทดลองใช้ฟิลเตอร์อื่น (`Sub`, `Up`, `Average`, `None`) เพื่อดูผลต่อขนาดและคุณภาพ ขั้นตอนนี้ยังแสดง **java png optimization** เนื่องจากฟิลเตอร์ที่เลือกมีผลต่อประสิทธิภาพการบีบอัด.

## ขั้นตอนที่ 4: บันทึกภาพ PNG
สุดท้ายให้เขียนภาพที่ประมวลผลแล้วกลับไปยังดิสก์โดยใช้ตัวเลือกที่กำหนดไว้

```java
psdImage.save(dataDir + "ApplyFilterMethod_out.png", options);
```

ไฟล์ผลลัพธ์ `ApplyFilterMethod_out.png` จะเป็น PNG ที่ผ่านการกรองพร้อมใช้บนเว็บหรือเดสก์ท็อป.

## ปัญหาที่พบบ่อยและวิธีแก้
| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| `FileNotFoundException` | เส้นทาง `dataDir` ไม่ถูกต้อง | ตรวจสอบให้แน่ใจว่า string ของไดเรกทอรีลงท้ายด้วยตัวคั่น (`/` หรือ `\\`). |
| ไม่มีผลของฟิลเตอร์ที่สังเกตเห็น | ใช้ `PngFilterType.None` | เปลี่ยนเป็น `Paeth` หรือฟิลเตอร์อื่น. |
| ข้อผิดพลาดหน่วยความจำไม่พอบน PSD ขนาดใหญ่ | โหลดไฟล์ขนาดใหญ่โดยไม่มีการสตรีม | ใช้ `PsdImage` พร้อม `loadOptions` เพื่อลดการใช้หน่วยความจำ. |

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD for Java คืออะไร?**  
ตอบ: Aspose.PSD for Java เป็น API ที่แข็งแกร่ง ช่วยให้นักพัฒนาสามารถอ่าน, แก้ไข, และแปลงไฟล์ PSD, ใช้ฟิลเตอร์, และทำการปรับแต่งภาพโดยไม่ต้องใช้ Adobe Photoshop.

**ถาม: จะดาวน์โหลด Aspose.PSD for Java ได้จากไหน?**  
ตอบ: คุณสามารถดาวน์โหลดได้จากหน้า releases ของ Aspose [here](https://releases.aspose.com/psd/java/).

**ถาม: สามารถทดลองใช้ Aspose.PSD ได้ฟรีหรือไม่?**  
ตอบ: ได้, มีรุ่นทดลองฟรีให้ใช้ [here](https://releases.aspose.com/).

**ถาม: ฟิลเตอร์ประเภทใดบ้างที่สามารถใช้กับภาพ PNG?**  
ตอบ: Aspose.PSD รองรับ Paeth, Sub, Up, Average, และ None. เลือกฟิลเตอร์ที่ให้สมดุลระหว่างขนาดและคุณภาพภาพที่ดีที่สุด.

**ถาม: จะหาการสนับสนุนสำหรับปัญหา Aspose.PSD ได้จากที่ไหน?**  
ตอบ: คุณสามารถขอความช่วยเหลือได้โดยไปที่ Aspose Forum [here](https://forum.aspose.com/c/psd/34).

## สรุป
คุณได้เรียนรู้ **วิธีกรองไฟล์ PNG** ด้วย Aspose.PSD for Java, **วิธีแปลง PSD เป็น PNG**, และ **java png optimization** ด้วยฟิลเตอร์ประเภทต่าง ๆ ทดลองใช้ฟิลเตอร์หลายแบบ, ผสานกระบวนการนี้เข้ากับ pipeline การประมวลผลภาพของคุณ, และเพลิดเพลินกับ PNG ที่มีขนาดเล็กแต่คุณภาพสูง.

---

**อัปเดตล่าสุด:** 2026-03-15  
**ทดสอบกับ:** Aspose.PSD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}