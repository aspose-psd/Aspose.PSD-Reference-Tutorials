---
title: การใช้การปรับสมดุลสีใน Aspose.PSD สำหรับ .NET
linktitle: การใช้การปรับสมดุลสี
second_title: Aspose.PSD .NET API
description: ปรับปรุงสีของภาพ PSD ได้อย่างง่ายดายด้วย Aspose.PSD สำหรับคุณสมบัติการปรับสมดุลสีของ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อผลลัพธ์ที่น่าทึ่ง
weight: 14
url: /th/net/image-adjustment/color-balance-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การใช้การปรับสมดุลสีใน Aspose.PSD สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำที่ครอบคลุมเกี่ยวกับการใช้การปรับสมดุลสีใน Aspose.PSD สำหรับ .NET! Aspose.PSD เป็นไลบรารี .NET ที่ทรงพลังซึ่งช่วยให้นักพัฒนาทำงานกับไฟล์ PSD ได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะเน้นที่คุณสมบัติการปรับสมดุลสี ซึ่งช่วยให้คุณสามารถเพิ่มสมดุลสีของรูปภาพ PSD ได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจากไฟล์[เว็บไซต์ Aspose.PSD](https://releases.aspose.com/psd/net/).
- สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้บนเครื่องของคุณ
- ไฟล์ PSD: เตรียมไฟล์ PSD ที่คุณต้องการใช้การปรับสมดุลสี

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อใช้คุณสมบัติ Aspose.PSD เพิ่มบรรทัดต่อไปนี้ลงในโค้ดของคุณ:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

ตอนนี้ เราจะแบ่งกระบวนการปรับสมดุลสีออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // รหัสสำหรับการปรับสมดุลสีจะถูกเพิ่มในขั้นตอนต่อไปนี้
}
```

## ขั้นตอนที่ 2: เข้าถึงและปรับสมดุลสี

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## ขั้นตอนที่ 3: บันทึกภาพที่ปรับแล้ว

```csharp
im.Save(outputPath);
```

ตอนนี้ คุณได้ใช้การปรับสมดุลสีกับไฟล์ PSD ของคุณโดยใช้ Aspose.PSD สำหรับ .NET สำเร็จแล้ว!

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีปรับปรุงสมดุลสีของรูปภาพ PSD ของคุณด้วย Aspose.PSD สำหรับ .NET แล้ว ทดลองใช้ค่าสมดุลต่างๆ เพื่อให้ได้เอฟเฟ็กต์ภาพที่ต้องการ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้การปรับสมดุลสีกับหลายเลเยอร์ได้หรือไม่

A1: ได้ คุณสามารถวนซ้ำทุกเลเยอร์ในไฟล์ PSD ของคุณและปรับสมดุลสีได้ตามต้องการ

### คำถามที่ 2: Aspose.PSD สำหรับ .NET เหมาะสำหรับการประมวลผลไฟล์ PSD เป็นชุดหรือไม่

A2: แน่นอน! Aspose.PSD มอบความสามารถในการประมวลผลแบบแบตช์ที่มีประสิทธิภาพสำหรับไฟล์ PSD

### คำถามที่ 3: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ .NET ได้อย่างไร

 A3: เยี่ยมเลย[Aspose.PSD ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อขอรับใบอนุญาตชั่วคราว

### คำถามที่ 4: ฉันจะหาตัวอย่างและเอกสารเพิ่มเติมได้จากที่ไหน

 A4: สำรวจ[เอกสาร Aspose.PSD](https://reference.aspose.com/psd/net/) สำหรับตัวอย่างและคำแนะนำโดยละเอียด

### คำถามที่ 5: Aspose.PSD สำหรับ .NET มีตัวเลือกการสนับสนุนใดบ้าง

 A5: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการอภิปรายของชุมชน

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
