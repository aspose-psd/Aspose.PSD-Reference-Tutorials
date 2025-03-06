---
title: เพิ่ม Curves Adjustment Layer ใน PSD โดยใช้ Java
linktitle: เพิ่ม Curves Adjustment Layer ใน PSD โดยใช้ Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มเลเยอร์การปรับเส้นโค้งลงในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ในบทช่วยสอนโดยละเอียดนี้ ปรับปรุงภาพของคุณได้อย่างง่ายดาย
weight: 11
url: /th/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่ม Curves Adjustment Layer ใน PSD โดยใช้ Java

## การแนะนำ
คุณเคยพบว่าตัวเองติดอยู่ในขณะที่พยายามจัดการรูปภาพในรูปแบบ PSD หรือไม่? ไม่ว่าคุณจะเป็นนักออกแบบกราฟิกหน้าใหม่หรือมือโปรผู้ช่ำชอง การทำงานกับไฟล์ Photoshop บางครั้งอาจรู้สึกเหมือนกำลังอยู่ในเขาวงกต โชคดีที่มีเครื่องมือที่ทำให้กระบวนการนี้ง่ายขึ้น - Aspose.PSD สำหรับ Java ในบทช่วยสอนนี้ เราจะเจาะลึกวิธีการเพิ่มเลเยอร์การปรับเส้นโค้งลงในไฟล์ PSD โดยใช้ Aspose.PSD ซึ่งจะทำให้งานแก้ไขภาพของคุณง่ายขึ้นและมีประสิทธิภาพมากขึ้น ด้วยคำแนะนำทีละขั้นตอน คุณจะสามารถปรับปรุงภาพของคุณอย่างมืออาชีพโดยไม่ต้องจมอยู่กับความซับซ้อนที่เกี่ยวข้องกับการจัดการภาพแบบดั้งเดิม
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกโค้ด เรามาตรวจสอบให้แน่ใจว่าคุณพร้อมแล้ว ต่อไปนี้เป็นข้อกำหนดเบื้องต้นที่คุณต้องการ:
1. Java Development Kit (JDK): คุณจะต้องติดตั้ง JDK บนคอมพิวเตอร์ของคุณ ตรวจสอบให้แน่ใจว่าเป็นเวอร์ชันล่าสุดเพื่อความเข้ากันได้ดีที่สุด
2. Aspose.PSD สำหรับไลบรารี Java: หากต้องการจัดการไฟล์ PSD คุณจะต้องดาวน์โหลดและรวมไลบรารี Aspose.PSD ในโปรเจ็กต์ของคุณ คุณสามารถคว้ามันได้[ที่นี่](https://releases.aspose.com/psd/java/).
3. IDE: ใช้ Java IDE ใดๆ เช่น IntelliJ IDEA, Eclipse หรือแม้แต่โปรแกรมแก้ไขข้อความธรรมดาเพื่อเขียนโค้ดของคุณ
4. ความเข้าใจพื้นฐานของ Java: ความคุ้นเคยกับการเขียนโปรแกรม Java จะช่วยให้คุณปฏิบัติตามได้อย่างราบรื่น
ได้ทุกอย่างแล้วเหรอ? สุดยอด! มาเข้าสู่ส่วนที่สนุกกันดีกว่า
## การนำเข้าแพ็คเกจ
ก่อนอื่น คุณต้องนำเข้าแพ็คเกจที่จำเป็นก่อน นี่คือวิธีที่คุณทำ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
```
ด้วยการนำเข้าแพ็คเกจเหล่านี้ คุณกำลังแจ้งให้แอปพลิเคชัน Java ของคุณทราบเกี่ยวกับคลาสที่จำเป็นในการจัดการไฟล์ PSD และเพื่อทำงานเฉพาะกับเลเยอร์ Curves Adjustment
ตอนนี้เราได้ตั้งค่าทุกอย่างเรียบร้อยแล้ว เรามาแจกแจงโค้ดและดูวิธีเพิ่มเลเยอร์ Curves Adjustment ทีละขั้นตอนกันดีกว่า
## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีข้อมูลของคุณ
ขั้นตอนแรกคือการพิจารณาว่าไฟล์ PSD ของคุณจะถูกจัดเก็บไว้ที่ใด ตั้งค่าไดเร็กทอรีเพื่อจัดระเบียบทุกอย่าง
```java
String dataDir = "Your Document Directory"; // อัพเดตเส้นทางนี้
```
 คิดถึง`dataDir`เป็นพื้นที่ทำงานของคุณ มันคือจุดที่ความมหัศจรรย์ทั้งหมดเกิดขึ้น! ตรวจสอบให้แน่ใจว่าได้เปลี่ยน`Your Document Directory` ด้วยเส้นทางจริงที่ไฟล์ PSD ของคุณอยู่หรือจะตั้งอยู่
## ขั้นตอนที่ 2: โหลดไฟล์ PSD ของคุณ
จากนั้น คุณจะต้องโหลดไฟล์ PSD ที่คุณต้องการแก้ไข ทำได้โดยใช้รหัสต่อไปนี้:
```java
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
```
 ในข้อมูลโค้ดนี้`sourceFileName` ชี้ไปที่ไฟล์ PSD ต้นฉบับในขณะที่`psdPathAfterChange` คือที่ที่คุณจะบันทึกไฟล์ที่คุณแก้ไข อย่าลืมต่อท้ายด้วย`.psd` ต่อมาในรหัส
## ขั้นตอนที่ 3: วนซ้ำเลเยอร์
ตอนนี้ได้เวลาเจาะลึกลงไปในเลเยอร์ของไฟล์ PSD ของคุณแล้ว เราจะวนซ้ำแต่ละเลเยอร์เพื่อค้นหาเลเยอร์การปรับเส้นโค้ง
```java
for (int j = 1; j < 2; j++) {
    String fileName = sourceFileName + ".psd";
    PsdImage im = (PsdImage) Image.load(fileName);
    
    for(int k = 0; k < im.getLayers().length; k++) {
        if (im.getLayers()[k] instanceof CurvesLayer) {
            // การประมวลผลเลเยอร์ Curves จะไปที่นี่
        }
    }
}
```
ต่อไปนี้คือรายละเอียดของสิ่งที่เกิดขึ้น:
-  เราเริ่มต้นด้วยการโหลดไฟล์ PSD ลงในไฟล์`PsdImage` วัตถุชื่อ`im`.
-  ต่อไป เราจะวนซ้ำเลเยอร์ทั้งหมดในรูปภาพโดยใช้`im.getLayers().length` - นี่ทำให้เราเข้าถึงแต่ละเลเยอร์ได้ ทำให้เราสามารถตรวจสอบได้ว่าใช่หรือไม่`CurvesLayer`.
## ขั้นตอนที่ 4: แก้ไขเลเยอร์ Curves
 ภายในวงที่ตรวจสอบ`CurvesLayer`คุณจะเพิ่มตรรกะเพื่อปรับเปลี่ยนเส้นโค้ง ต่อไปนี้เป็นวิธีดำเนินการ:
```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager) curvesLayer.getCurvesManager();
    for (int i = 10; i < 50; i++) {
        manager.setValueInPosition(0, (byte) i, (byte) (15 + (i * 2)));
    }
} else {
    CurvesContinuousManager manager = (CurvesContinuousManager) curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte) 0, (byte) 50, (byte) 100);
    manager.addCurvePoint((byte) 0, (byte) 150, (byte) 130);
}
```
ในส่วนนี้:
- เราตรวจสอบว่าเลเยอร์เส้นโค้งใช้ผู้จัดการแบบแยกหรือผู้จัดการแบบต่อเนื่องหรือไม่
- หากเป็นผู้จัดการแยก เราจะตั้งค่าใหม่สำหรับแต่ละตำแหน่งตั้งแต่ 10 ถึง 49
- ในทางกลับกัน ด้วยผู้จัดการที่ต่อเนื่อง เราจะเพิ่มจุดโค้งเพื่อปรับเส้นโค้งตามต้องการ
## ขั้นตอนที่ 5: บันทึก PSD ที่แก้ไขแล้ว
หลังจากทำการปรับเปลี่ยนแล้ว ขั้นตอนสุดท้ายคือการบันทึกไฟล์ PSD ที่แก้ไข
```java
im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
```
 บรรทัดนี้จะบันทึก PSD ที่ปรับแล้วลงในเส้นทางที่คุณกำหนดไว้ก่อนหน้านี้ แต่ละครั้งที่คุณแก้ไข ไฟล์จะสร้างไฟล์ใหม่โดยมีคำต่อท้ายที่แตกต่างกันตามตัวนับลูป`j`.
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มเลเยอร์การปรับเส้นโค้งให้กับไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java เรียบร้อยแล้ว ด้วยขั้นตอนเพียงไม่กี่ขั้นตอน คุณสามารถปรับปรุงรูปภาพของคุณและปรับแต่งตามความต้องการของคุณได้ ความยืดหยุ่นที่ได้รับจากไลบรารีนี้ทำให้เป็นเครื่องมืออันล้ำค่าสำหรับทุกคนที่ทำงานกับไฟล์ PSD ตอนนี้ลองทดลองกับเส้นโค้งต่างๆ และปล่อยให้ความคิดสร้างสรรค์ของคุณไหลลื่น
## คำถามที่พบบ่อย
### Aspose.PSD คืออะไร
Aspose.PSD เป็นไลบรารีสำหรับประมวลผลไฟล์ Photoshop PSD ในภาษาการเขียนโปรแกรมต่างๆ รวมถึง Java
### ฉันสามารถใช้ Aspose.PSD ได้ฟรีหรือไม่
 ใช่ Aspose เสนอการทดลองใช้ฟรีที่คุณสามารถสำรวจได้ก่อนซื้อ ตรวจสอบ[ดาวน์โหลดทดลองใช้ฟรี](https://releases.aspose.com/) ลิงค์
### จำเป็นต้องติดตั้ง Photoshop หรือไม่?
ไม่ คุณไม่จำเป็นต้องติดตั้ง Photoshop บนเครื่องของคุณเพื่อทำงานกับ Aspose.PSD
### ฉันสามารถจัดการเลเยอร์อื่นนอกเหนือจากเลเยอร์การปรับเส้นโค้งได้หรือไม่
อย่างแน่นอน! Aspose.PSD ช่วยให้สามารถจัดการเลเยอร์ประเภทต่างๆ ในไฟล์ PSD ได้
### ฉันจะหาเอกสารเพิ่มเติมได้จากที่ไหน?
 สำหรับเอกสารโดยละเอียด โปรดไปที่[Aspose.PSD สำหรับเอกสาร Java](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
