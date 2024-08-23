---
title: รองรับทรัพยากร Infx ในไฟล์ PSD ด้วย Java
linktitle: รองรับทรัพยากร Infx ในไฟล์ PSD ด้วย Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีจัดการทรัพยากร Infx ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ด้วยบทช่วยสอนแบบทีละขั้นตอนที่ครอบคลุมนี้ เหมาะสำหรับนักพัฒนาทุกระดับ
type: docs
weight: 13
url: /th/java/working-with-psd-files/support-infx-resource-psd-files/
---
## การแนะนำ

การทำงานกับไฟล์ PSD (เอกสาร Photoshop) ใน Java อาจดูยุ่งยาก แต่ก็ไม่จำเป็นต้องเป็นเช่นนั้น ลองนึกภาพคุณมีไฟล์ PSD หลายชั้นที่มีทรัพยากรต่างๆ และคุณจำเป็นต้องแก้ไขไฟล์ที่เฉพาะเจาะจง เช่น InfxResource ในขณะเดียวกันก็ตรวจสอบให้แน่ใจว่าไฟล์นั้นมีความสมบูรณ์ครบถ้วน นั่นคือจุดที่ Aspose.PSD สำหรับ Java เข้ามานำเสนอ API ที่ใช้งานง่ายเพื่อจัดการไฟล์ PSD ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะอธิบายวิธีการค้นหา แก้ไข และบันทึก InfxResource ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น คู่มือนี้จะทำให้การจัดการทรัพยากร PSD เป็นไปอย่างตรงไปตรงมาที่สุด

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทแนะนำ โปรดตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่คุณต้องการแล้ว นี่คือรายการตรวจสอบด่วน:

1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าได้ติดตั้ง JDK เวอร์ชันล่าสุดบนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ออราเคิล](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
  
2.  Aspose.PSD สำหรับ Java Library: ดาวน์โหลด Aspose.PSD สำหรับ Java เวอร์ชันล่าสุดจาก[ลิงค์ดาวน์โหลด](https://releases.aspose.com/psd/java/) หากคุณยังไม่ได้ดำเนินการ คุณสามารถทดลองใช้ฟรีหรือซื้อใบอนุญาตได้จาก[ที่นี่](https://purchase.aspose.com/).

3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): Java IDE ใดๆ เช่น IntelliJ IDEA, Eclipse หรือ NetBeans จะทำงานนี้ได้

4. ความรู้ Java ขั้นพื้นฐาน: ความคุ้นเคยกับแนวคิดการเขียนโปรแกรม Java เป็นสิ่งสำคัญ หากคุณยังใหม่กับ Java ให้พิจารณาทบทวนพื้นฐาน Java ก่อนดำเนินการต่อ

5. ไฟล์ PSD ตัวอย่าง: จำเป็นต้องปฏิบัติตามไฟล์ PSD ตัวอย่างที่มี InfxResource พร้อมกับบทช่วยสอน คุณสามารถใช้ไฟล์ของคุณเองหรือดาวน์โหลดไฟล์ตัวอย่างก็ได้

## แพ็คเกจนำเข้า

ในการเริ่มต้นใช้งาน Aspose.PSD สำหรับ Java ขั้นตอนแรกคือการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ ขั้นตอนนี้มีความสำคัญเนื่องจากช่วยให้แอปพลิเคชัน Java ของคุณใช้คุณลักษณะของไลบรารี Aspose.PSD ได้

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layerresources.InfxResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.LayerResource;
import com.aspose.psd.systemexceptions.ArgumentNullException;
```

ตอนนี้ เรามาแบ่งโค้ดออกเป็นขั้นตอนง่ายๆ กัน

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางต้นทางและปลายทาง

ก่อนอื่น คุณต้องระบุไดเร็กทอรีต้นทางซึ่งเป็นที่ตั้งของไฟล์ PSD และไดเร็กทอรีปลายทางที่จะบันทึกไฟล์ที่แก้ไข

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFileName = sourceDir + "SampleForInfxResource.psd";
String destinationFileName = outputDir + "SampleForInfxResource_out.psd";
```

 ที่นี่,`sourceDir` คือเส้นทางไดเร็กทอรีที่มีไฟล์ PSD ต้นฉบับของคุณอยู่ และ`outputDir` คือตำแหน่งที่ไฟล์ PSD ที่แก้ไขจะถูกบันทึก ด้วยการตั้งค่าเส้นทางเหล่านี้ คุณแน่ใจได้ว่าแอปพลิเคชันของคุณรู้ว่าจะหาและจัดเก็บไฟล์ที่ต้องการใช้งานได้ที่ไหน

## ขั้นตอนที่ 2: โหลดรูปภาพ PSD

 จากนั้นให้โหลดไฟล์ PSD ลงในไฟล์`PsdImage` วัตถุ. วัตถุนี้จะช่วยให้คุณสามารถจัดการเลเยอร์และทรัพยากรภายในไฟล์ PSD

```java
PsdImage im = null;
try {
    im = (PsdImage) Image.load(sourceFileName);
} catch (ArgumentNullException e) {
    System.out.println("File not found: " + e.getMessage());
}
```

 ที่`Image.load` ใช้วิธีการที่นี่เพื่อโหลดไฟล์ PSD หากไม่พบไฟล์หรือเส้นทางไม่ถูกต้อง`ArgumentNullException` จะถูกจับได้และจะแสดงข้อความที่เหมาะสม

## ขั้นตอนที่ 3: วนซ้ำผ่านเลเยอร์และทรัพยากร

 เมื่อโหลดไฟล์ PSD แล้ว ขั้นตอนต่อไปคือการวนซ้ำผ่านเลเยอร์ต่างๆ เพื่อค้นหาไฟล์ที่เฉพาะเจาะจง`InfxResource` คุณกำลังมองหา

```java
boolean isRequiredResourceFound = false;

for (Layer layer : im.getLayers()) {
    for (LayerResource layerResource : layer.getResources()) {
        if (layerResource instanceof InfxResource) {
            InfxResource resource = (InfxResource) layerResource;
            isRequiredResourceFound = true;
            
            // ตรวจสอบและแก้ไขทรัพยากร
            if (!resource.getBlendInteriorElements()) {
                resource.setBlendInteriorElements(true);
                im.save(destinationFileName);
            }
            break;
        }
    }
}
```

 ที่นี่ เราวนซ้ำแต่ละเลเยอร์และทรัพยากรที่เกี่ยวข้อง ถ้าเป็น`InfxResource`พบแล้ว เราทำการตรวจสอบหรือแก้ไข โดยเฉพาะเราจะตรวจสอบว่า`BlendInteriorElements` เป็นเท็จ และหากเป็นเช่นนั้น ให้ตั้งค่าเป็นจริงและบันทึกไฟล์ที่แก้ไข

## ขั้นตอนที่ 4: บันทึกและกำจัดรูปภาพ

หลังจากแก้ไขทรัพยากรแล้ว จำเป็นต้องบันทึกการเปลี่ยนแปลงและกำจัดออบเจ็กต์รูปภาพเพื่อเพิ่มหน่วยความจำ

```java
finally {
    if (im != null) im.dispose();
}
```

 ที่`finally` บล็อกทำให้มั่นใจได้ว่า`PsdImage` วัตถุถูกกำจัดอย่างเหมาะสม ป้องกันการรั่วไหลของหน่วยความจำ และทำให้มั่นใจว่าแอปพลิเคชันของคุณยังคงมีประสิทธิภาพ

## ขั้นตอนที่ 5: โหลดและตรวจสอบไฟล์ PSD ที่ถูกแก้ไข

เมื่อคุณได้บันทึกไฟล์ PSD ที่แก้ไขแล้ว ขั้นตอนสุดท้ายคือโหลดอีกครั้งและตรวจสอบว่ามีการใช้การเปลี่ยนแปลงอย่างถูกต้อง

```java
PsdImage im2 = null;
try {
    im2 = (PsdImage) Image.load(destinationFileName);
    for (Layer layer : im2.getLayers()) {
        for (LayerResource layerResource : layer.getResources()) {
            if (layerResource instanceof InfxResource) {
                InfxResource resource = (InfxResource) layerResource;
                Assert.isTrue(resource.getBlendInteriorElements(), "The InfxResource.BlendInteriorElements should change to true");
                break;
            }
        }
    }
} finally {
    if (im2 != null) im2.dispose();
}
```

 ขั้นตอนนี้มีความสำคัญอย่างยิ่งในการตรวจสอบให้แน่ใจว่ามีการใช้การปรับเปลี่ยนตามที่คาดไว้ คุณโหลดไฟล์ที่แก้ไขและตรวจสอบไฟล์`BlendInteriorElements` คุณสมบัติเพื่อให้แน่ใจว่ามีการตั้งค่าเป็น`true`.

## บทสรุป

 ยินดีด้วย! คุณได้เรียนรู้วิธีจัดการกับมันเรียบร้อยแล้ว`InfxResource`ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะทำงานในโครงการขนาดเล็กหรือรวมฟังก์ชันนี้เข้ากับแอปพลิเคชันขนาดใหญ่ ขั้นตอนที่อธิบายไว้ในบทช่วยสอนนี้จะทำหน้าที่เป็นรากฐานที่มั่นคง ประสิทธิภาพของ Aspose.PSD สำหรับ Java อยู่ที่ความยืดหยุ่นและความสะดวกในการใช้งาน ทำให้เป็นเครื่องมือที่ขาดไม่ได้สำหรับนักพัฒนาที่ทำงานกับไฟล์ PSD ลองสำรวจคุณสมบัติเพิ่มเติม และดูว่ามีอะไรอีกบ้างที่คุณสามารถทำได้ด้วย Aspose.PSD สำหรับ Java!

## คำถามที่พบบ่อย

### ฉันสามารถใช้ Aspose.PSD สำหรับ Java เพื่อจัดการทรัพยากรอื่นๆ ในไฟล์ PSD ได้หรือไม่

 ใช่ Aspose.PSD สำหรับ Java ช่วยให้คุณสามารถจัดการทรัพยากรและคุณสมบัติต่างๆ ภายในไฟล์ PSD ได้ ไม่ใช่แค่เท่านั้น`InfxResource`.

###  จะเกิดอะไรขึ้นถ้า`InfxResource` is not found in the PSD file?

 ถ้า`InfxResource` ไม่พบ รหัสจะดำเนินการต่อไป แต่การดำเนินการที่ระบุจะไม่ถูกดำเนินการ และสามารถบันทึกข้อความเพื่อวัตถุประสงค์ในการแก้ไขจุดบกพร่อง

### ฉันจะจัดการไฟล์ PSD ขนาดใหญ่ที่มีหลายเลเยอร์ได้อย่างไร

การจัดการไฟล์ PSD ขนาดใหญ่ที่มีหลายเลเยอร์อาจต้องใช้หน่วยความจำและพลังการประมวลผลมากขึ้น ตรวจสอบให้แน่ใจว่าสภาพแวดล้อมของคุณได้รับการปรับให้เหมาะสม และพิจารณากำจัดอ็อบเจ็กต์เมื่อไม่จำเป็นอีกต่อไปเพื่อเพิ่มทรัพยากร

### เป็นไปได้หรือไม่ที่จะคืนค่าการเปลี่ยนแปลงที่ทำกับไฟล์ PSD?

เมื่อบันทึกการเปลี่ยนแปลงแล้ว การเปลี่ยนแปลงจะมีผลถาวร เว้นแต่คุณจะสำรองข้อมูลของไฟล์ต้นฉบับไว้ ทำงานกับสำเนาของไฟล์เสมอหากคุณต้องการเก็บต้นฉบับไว้ไม่เปลี่ยนแปลง

### ฉันสามารถทำการแก้ไขไฟล์ PSD หลายไฟล์โดยอัตโนมัติโดยใช้ Aspose.PSD สำหรับ Java ได้หรือไม่

ได้ คุณสามารถสร้างสคริปต์เพื่อประมวลผลไฟล์ PSD หลายไฟล์เป็นชุด โดยใช้การแก้ไขแบบเดียวกันในแต่ละไฟล์