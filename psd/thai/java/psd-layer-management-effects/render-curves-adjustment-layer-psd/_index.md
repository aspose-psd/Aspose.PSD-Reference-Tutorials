---
date: 2026-04-05
description: เรียนรู้วิธีเรนเดอร์เลเยอร์ Curves ใน Java และปรับแต่ง Curves Adjustment
  Layers ในไฟล์ PSD ด้วย Aspose.PSD for Java คู่มือขั้นตอนโดยละเอียดพร้อมตัวอย่างโค้ด
keywords:
- render curves layer java
- curves adjustment layer java
- aspose psd java
linktitle: เรนเดอร์เลเยอร์การปรับโค้งในไฟล์ PSD - Java
second_title: Aspose.PSD Java API
title: เรนเดอร์เลเยอร์โค้ง Java – ปรับเลเยอร์การปรับโค้งในไฟล์ PSD
url: /th/java/psd-layer-management-effects/render-curves-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เรนเดอร์เลเยอร์ Curves ใน Java – ปรับเลเยอร์ Curves Adjustment ในไฟล์ PSD

## บทนำ

หากคุณต้องการ **render curves layer java** อย่างโปรแกรมมิ่ง, เลเยอร์ Curves Adjustment ใน Photoshop คือเพื่อนที่ดีที่สุดสำหรับการปรับโทนและสีอย่างละเอียด คิดว่าเป็นพาเลตศิลปินดิจิทัลที่แต่ละจุดโค้งจะเปลี่ยนแปลงความสว่างและคอนทราสต์ของภาพ ในบทแนะนำนี้เราจะอธิบายขั้นตอนการโหลดไฟล์ PSD, ค้นหาเลเยอร์ Curves Adjustment, ปรับจุดโค้ง, และสุดท้ายส่งออกผลลัพธ์—ทั้งหมดด้วย Aspose.PSD for Java. เมื่อเสร็จคุณจะมั่นใจในการเรนเดอร์เลเยอร์ Curves ด้วย Java และผสานการทำงานนี้เข้ากับ pipeline การประมวลผลภาพของคุณเอง.

## คำตอบสั้น
- **What does “render curves layer java” mean?** การเรนเดอร์เลเยอร์ Curves Adjustment ในไฟล์ PSD ด้วยโค้ด Java.  
- **Which library handles this?** Aspose.PSD for Java.  
- **Do I need Photoshop installed?** No, the API works independently.  
- **Can I export the result as PNG?** Yes, using `PngOptions`.  
- **Is a license required for production?** A commercial license is needed for non‑trial use.

## เลเยอร์ Curves Adjustment คืออะไร?

เลเยอร์ Curves Adjustment ช่วยให้คุณแก้ไขโค้งโทน RGB ของภาพ, ให้คุณควบคุมเงา, โทนกลาง, และไฮไลท์อย่างแม่นยำในระดับพิกเซล ในโค้ด, เลเยอร์นี้แสดงด้วยคลาส `CurvesLayer` ซึ่งสามารถแก้ไขได้ผ่านผู้จัดการโค้งแบบแยกส่วนหรือแบบต่อเนื่อง.

## ทำไมต้องใช้ Aspose.PSD for Java เพื่อเรนเดอร์เลเยอร์ Curves?

- **Full PSD fidelity** – ทุกประเภทเลเยอร์, มาสก์, และเอฟเฟกต์จะถูกเก็บรักษาไว้ครบถ้วน.  
- **No Photoshop dependency** – เหมาะสำหรับการทำงานอัตโนมัติบนเซิร์ฟเวอร์.  
- **Rich export options** – สามารถบันทึกเป็น PSD, PNG, TIFF, ฯลฯ.  
- **Cross‑platform** – ทำงานบนระบบปฏิบัติการใดก็ได้ที่รองรับ Java 8+.

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK) 8 หรือสูงกว่า** – จำเป็นสำหรับรัน Aspose.PSD.  
2. **Aspose.PSD for Java library** – ดาวน์โหลดจาก [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, หรือเครื่องมือแก้ไขที่รองรับ Java ใดก็ได้.  
4. **Basic Java knowledge** – ความคุ้นเคยกับคลาส, อ็อบเจ็กต์, และลูป.  
5. **ไฟล์ PSD** ที่มีเลเยอร์ Curves Adjustment ที่คุณต้องการแก้ไข.

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น, ให้นำเข้าคลาส Aspose.PSD ที่จำเป็น.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

โหลดไฟล์ PSD ต้นฉบับของคุณเข้าสู่วัตถุ `PsdImage`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
PsdImage im = (PsdImage)Image.load(sourceFileName + ".psd");
```

> **เคล็ดลับ:** ใช้เส้นทางแบบเต็ม (absolute paths) ระหว่างการดีบักเพื่อหลีกเลี่ยง `FileNotFoundException`.

## ขั้นตอนที่ 2: วนลูปผ่านเลเยอร์

ค้นหาเลเยอร์ Curves Adjustment โดยสแกนคอลเลกชันของเลเยอร์.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof CurvesLayer) {
        CurvesLayer curvesLayer = (CurvesLayer)im.getLayers()[i];
        // Additional operations will be handled here
    }
}
```

## ขั้นตอนที่ 3: แก้ไขเลเยอร์ Curves

เมื่อคุณได้ `CurvesLayer` แล้ว, ให้ตัดสินใจว่าใช้ผู้จัดการแบบแยกส่วน (discrete) หรือแบบต่อเนื่อง (continuous) และปรับตามนั้น.

### การแก้ไข Discrete Curves Manager

```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();
    
    for (int k = 10; k < 50; k++) {
        manager.setValueInPosition(0, (byte)k, (byte)(15 + (k * 2)));
    }
}
```

### การแก้ไข Continuous Curves Manager

```java
else {
    CurvesContinuousManager manager = (CurvesContinuousManager)curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte)0, (byte)50, (byte)100);
    manager.addCurvePoint((byte)0, (byte)150, (byte)130);
}
```

## ขั้นตอนที่ 4: บันทึก PSD ที่แก้ไขแล้ว

บันทึกการเปลี่ยนแปลงของคุณกลับไปยังไฟล์ PSD.

```java
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
im.save(psdPathAfterChange + ".psd");
```

## ขั้นตอนที่ 5: ส่งออกเป็น PNG

หากคุณต้องการภาพพร้อมใช้งานบนเว็บ, ให้ส่งออก PSD ที่แก้ไขเป็น PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
String pngExportPath = dataDir + "CurvesAdjustmentLayerChanged";
im.save(pngExportPath + ".png", saveOptions);
```

## ปัญหาทั่วไป & วิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **ไม่มีการเปลี่ยนแปลงของโค้งที่เห็นได้** | ใช้ประเภทผู้จัดการผิด | ตรวจสอบ `isDiscreteManagerUsed()` และทำการแคสตามนั้น. |
| **ไม่พบไฟล์** | เส้นทาง `dataDir` ไม่ถูกต้อง | ใช้ `System.getProperty("user.dir")` เพื่อสร้างเส้นทางแบบเต็ม. |
| **PNG ที่ส่งออกเป็นภาพว่าง** | PSD ไม่ได้เรนเดอร์เต็มก่อนบันทึก | เรียก `im.save(..., saveOptions)` หลังจากการแก้ไขทั้งหมดเสร็จสมบูรณ์. |

## คำถามที่พบบ่อย

**Q: เลเยอร์ Curves Adjustment คืออะไร?**  
A: เป็นการปรับใน Photoshop ที่ให้คุณแก้ไขโค้งโทน RGB เพื่อควบคุมสีและความสว่างอย่างแม่นยำ.

**Q: สามารถใช้ Aspose.PSD for Java กับรูปแบบภาพอื่นได้หรือไม่?**  
A: ได้, คุณสามารถส่งออก PSD ที่แก้ไขเป็น PNG, TIFF, JPEG, และอื่น ๆ.

**Q: จำเป็นต้องติดตั้ง Photoshop เพื่อใช้ Aspose.PSD for Java หรือไม่?**  
A: ไม่จำเป็น, ไลบรารีทำงานแยกจาก Photoshop.

**Q: ฉันจะรับการทดลองใช้ฟรีของ Aspose.PSD for Java ได้อย่างไร?**  
A: ดาวน์โหลดรุ่นทดลองจาก [Aspose releases page](https://releases.aspose.com/psd/java/).

**Q: จะหาแหล่งสนับสนุนสำหรับ Aspose.PSD for Java ได้จากที่ไหน?**  
A: เยี่ยมชม [Aspose support forum](https://forum.aspose.com/c/psd/34/).

**Q: สามารถประมวลผลหลายไฟล์ PSD พร้อมกันได้หรือไม่?**  
A: แน่นอน—ใส่ตรรกะการโหลดและแก้ไขไว้ในลูปที่วนผ่านรายการไฟล์ของคุณ.

---

**อัปเดตล่าสุด:** 2026-04-05  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}