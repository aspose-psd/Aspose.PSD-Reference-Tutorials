---
date: 2026-03-13
description: เรียนรู้วิธีสร้างโครงการ Java สำหรับภาพ PSD พร้อมการจัดการการจัดสรรแคชด้วย
  Aspose.PSD for Java. ปรับเพิ่มประสิทธิภาพการใช้หน่วยความจำและการใช้ดิสก์อย่างมีประสิทธิภาพ.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: สร้างภาพ PSD ด้วย Java – ควบคุมการจัดสรรแคชใหม่
url: /th/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ควบคุมการจัดสรรแคชใหม่ในไฟล์ PSD

## บทนำ
If you need to **create PSD image java** projects efficiently, controlling cache reallocation is essential. When working with images and Photoshop files programmatically, efficiency is a key factor. Aspose.PSD for Java offers robust features to manage and manipulate PSD files seamlessly. One of the fundamental aspects of optimizing performance is controlling cache reallocation. Cache management helps in maintaining the balance between memory and disk usage, ensuring your application runs smoothly, without unexpected crashes or slowdowns. 

## คำตอบสั้น
- **การจัดสรรแคชใหม่ทำอะไร?** It balances memory and disk usage while processing large PSD files.  
- **ประเภทแคชใดที่เหมาะกับภาพขนาดใหญ่?** `CacheOnDiskOnly` keeps memory free by storing cache on disk.  
- **ฉันสามารถจัดสรรพื้นที่ดิสก์ได้เท่าไหร่?** Up to 1 GB (or any size you set with `setMaxDiskSpaceForCache`).  
- **ฉันต้องมีลิขสิทธิ์เพื่อใช้ฟีเจอร์เหล่านี้หรือไม่?** A license removes trial limitations; see the Aspose purchase page.  
- **ฉันสามารถตรวจสอบการใช้แคชขณะทำงานได้หรือไม่?** Yes, use `Cache.getAllocatedDiskBytesCount()` and `Cache.getAllocatedMemoryBytesCount()`.

## ทำไมต้องควบคุมการจัดสรรแคชใหม่?
Managing cache is crucial when you **create PSD image java** applications that handle high‑resolution or multi‑layer files. Proper cache settings prevent out‑of‑memory errors, reduce GC pauses, and give you predictable performance on servers or desktop apps.

## ข้อกำหนดเบื้องต้น
1. Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. Aspose.PSD for Java: คุณต้องดาวน์โหลดไลบรารี Aspose.PSD คุณสามารถค้นหาเวอร์ชันล่าสุดได้ [ที่นี่](https://releases.aspose.com/psd/java/).  
3. การตั้งค่า IDE: สภาพแวดล้อมการพัฒนาแบบบูรณาการ (IDE) เช่น IntelliJ IDEA หรือ Eclipse จะทำให้การจัดการโค้ดของคุณง่ายขึ้น.  
4. ความเข้าใจพื้นฐานของ Java: ความคุ้นเคยกับการเขียนโปรแกรม Java จะช่วยให้คุณเข้าใจแนวคิดและโค้ดสแนปได้ดีขึ้น.  
5. ลิขสิทธิ์ Aspose (ไม่บังคับ): หากคุณต้องการลบลายน้ำและได้รับฟังก์ชันเต็มรูปแบบ, พิจารณาซื้อไลเซนส์ [ที่นี่](https://purchase.aspose.com/buy) หรือทดลองเวอร์ชันฟรี [ที่นี่](https://releases.aspose.com/).

## นำเข้าแพ็กเกจ
Before we start writing the code, let’s make sure we have the necessary packages imported. Below is a brief list of what to include at the beginning of your Java file:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## วิธีสร้าง PSD Image Java พร้อมการควบคุมแคช
Below is a step‑by‑step walkthrough that ties cache configuration directly to the process of creating a PSD image in Java.

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีข้อมูลของคุณ
First things first, you’ll need to set up a directory where you want your cache files to be stored. This is essential for managing the cache effectively.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: กำหนดไดเรกทอรีสำหรับแคชเอกสารของคุณ.  
- `Cache.setCacheFolder(dataDir)`: เมธอดนี้ตั้งค่าโฟลเดอร์แคชเป็นไดเรกทอรีที่ระบุ แคชใด ๆ ที่สร้างโดย Aspose จะถูกจัดเก็บที่นี่แทนไดเรกทอรีชั่วคราวเริ่มต้น.

### ขั้นตอนที่ 2: กำหนดค่าแคชให้เก็บบนดิสก์
Next, we’ll specify that we want our cache to be stored on disk only. This is particularly useful if your application uses large files and you want to ensure that memory remains free.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: ตัวเลือกนี้ทำให้แคชไม่ถูกเก็บในหน่วยความจำ ซึ่งเป็นประโยชน์สำหรับการจัดการไฟล์ PSD ขนาดใหญ่โดยไม่ใช้ RAM มากเกินไป.

### ขั้นตอนที่ 3: ตั้งค่าขนาดสูงสุดของแคชบนดิสก์และหน่วยความจำ
Now, let's restrict our cache sizes. This is crucial because unlimited cache can lead to performance issues.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: ตั้งขีดจำกัด 1 GB สำหรับแคชบนดิสก์ คุณสามารถปรับขนาดนี้ตามความต้องการของคุณ.  
- `Cache.setMaxMemoryForCache(1073741824)`: เช่นเดียวกัน, ตัวนี้จำกัดแคชในหน่วยความจำ เพื่อให้แอปของคุณไม่ใช้หน่วยความจำมากเกินไป.

### ขั้นตอนที่ 4: จัดการกลยุทธ์การจัดสรรแคชใหม่
Managing how cache is reallocated is essential for maintaining performance. Here’s how you can set it up.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: เมื่อกำหนดเป็น `false` จะทำให้ Aspose จัดการการจัดสรรแคชใหม่ได้อย่างยืดหยุ่นมากขึ้น ซึ่งอาจทำให้ประสิทธิภาพดีขึ้น.

### ขั้นตอนที่ 5: ตรวจสอบขนาดแคชที่จัดสรร
This step is about monitoring how many bytes are currently allocated for the cache in memory or on disk. Let’s implement that:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: เก็บจำนวนไบต์ที่จัดสรรบนดิสก์.  
- `long l2`: เก็บจำนวนไบต์ที่จัดสรรในหน่วยความจำ.  
You can check these values at any time to ensure your application is managing memory and disk usage as expected.

### ขั้นตอนที่ 6: สร้างภาพ PSD
Now that we have our cache configurations set up, let’s create a simple PSD image.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: อ็อบเจกต์นี้ให้คุณระบุตัวเลือกเมื่อสร้างภาพ Photoshop.  
- `Color[] color`: อาร์เรย์ที่บรรจุสีที่จะใช้ในพาเลตของภาพ.

### ขั้นตอนที่ 7: บันทึกข้อมูลพิกเซลลงในภาพ
Now, let’s populate our image with pixel data and save it.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: เป็นอาร์เรย์ของอ็อบเจกต์สี ที่นี่เรากำลังเติมด้วยพิกเซลสีขาว.  
- `image.savePixels(image.getBounds(), pixels)`: เมธอดนี้บันทึกข้อมูลพิกเซลลงในภาพ มันอัปเดตภาพด้วยสีที่เรากำหนด.

### ขั้นตอนที่ 8: ตรวจสอบแคชที่จัดสรรหลังจากสร้างภาพ
After creating the image, it’s a good practice to check how many bytes are allocated for the cache again.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: บันทึกการจัดสรรปัจจุบันบนดิสก์หลังจากสร้างภาพ.  
- `long memoryBytes`: บันทึกการจัดสรรปัจจุบันในหน่วยความจำ.  
This step will help you determine how much cache is being consumed after your operations.

### ขั้นตอนที่ 9: ตรวจสอบการทำลายที่เหมาะสม
Lastly, it's crucial to ensure that all Aspose.PSD objects were disposed of properly to avoid memory leaks.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` and `l2`: ตัวแปรเหล่านี้จะช่วยให้คุณตรวจสอบการจัดสรรสุดท้าย หากค่าไม่เป็นศูนย์ แสดงว่ามีอ็อบเจกต์บางส่วนที่ยังไม่ได้ทำลายอย่างเหมาะสม.

## ปัญหาที่พบบ่อยและวิธีแก้
- **โฟลเดอร์แคชไม่ถูกสร้าง** – Verify that the application has write permissions for the path you passed to `Cache.setCacheFolder`.  
- **ข้อผิดพลาด out‑of‑memory** – Double‑check that `Cache.setCacheType(CacheType.CacheOnDiskOnly)` is applied before loading large PSD files.  
- **ขนาดแคชที่ไม่คาดคิด** – Use the `Cache.getAllocated*BytesCount()` methods after each major operation to track growth.

## คำถามที่พบบ่อย

**Q: Aspose.PSD คืออะไร?**  
A: Aspose.PSD เป็นไลบรารีสำหรับนักพัฒนา .NET และ Java เพื่อสร้าง, ปรับแต่ง, และแปลงไฟล์ Photoshop (PSD) อย่างโปรแกรมเมติก.

**Q: ฉันจะตรวจสอบขนาดแคชที่จัดสรรได้อย่างไร?**  
A: ใช้เมธอดเช่น `Cache.getAllocatedDiskBytesCount()` และ `Cache.getAllocatedMemoryBytesCount()` เพื่อตรวจสอบการใช้แคชในปัจจุบัน.

**Q: ฉันสามารถตั้งค่าไดเรกทอรีที่กำหนดเองสำหรับแคชได้หรือไม่?**  
A: ได้, คุณสามารถระบุไดเรกทอรีอื่นโดยใช้ `Cache.setCacheFolder("Your Directory Path")`.

**Q: Aspose.PSD ใช้ได้ฟรีหรือไม่?**  
A: Aspose.PSD เป็นไลบรารีที่ต้องซื้อ, แต่คุณสามารถเริ่มต้นด้วยรุ่นทดลองฟรีที่มีบน [website](https://releases.aspose.com/).

**Q: จะเกิดอะไรขึ้นหากฉันไม่ทำลายอ็อบเจกต์?**  
A: การไม่ทำลายอ็อบเจกต์อาจทำให้เกิดการรั่วไหลของหน่วยความจำ, ทำให้แอปของคุณใช้ทรัพยากรมากเกินไป.

## สรุป
Controlling cache reallocation while you **create PSD image java** applications can make a significant difference in performance. By following the steps above, you’ll efficiently manage cache, minimize memory consumption, and generate high‑quality PSD files with Aspose.PSD for Java. Apply these techniques, and your projects will run smoother and scale better.

---

**อัปเดตล่าสุด:** 2026-03-13  
**ทดสอบด้วย:** Aspose.PSD for Java (latest release)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}