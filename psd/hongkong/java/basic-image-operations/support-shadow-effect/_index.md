---
date: 2026-06-18
description: 了解如何使用 Aspose.PSD for Java 更改 shadow color（Java）並自訂 shadow effects。請跟隨此
  step‑by‑step shadow effect 教學。
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: 支援 Shadow Effect
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 更改 Shadow Color（Java）
url: /zh-hant/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 更改陰影顏色（Java）

## 介紹

為圖形增添層次感通常意味著 **更改陰影顏色** 以符合設計氛圍。使用 Aspose.PSD for Java，您可以輕鬆新增或修改投影效果、控制不透明度，並微調其他參數——全部透過 Java 程式碼完成。在本 **陰影效果教學** 中，我們將示範如何載入 PSD、讀取現有陰影、客製化其顏色、不透明度、距離，最後儲存更新後的檔案。本指南精確說明如何 **在 Java 中更改陰影顏色**，並可重現執行。

## 快速解答
- **「更改陰影顏色」是什麼意思？** 它會更新套用於 PSD 圖層的 DropShadowEffect 的顏色屬性。  
- **哪個函式庫支援此功能？** Aspose.PSD for Java 完全支援陰影效果。  
- **我需要授權嗎？** 試用版可用於開發；正式環境需購買商業授權。  
- **可以設定陰影不透明度嗎？** 可以 – 使用 `setOpacity(byte)` 來定義透明度（0‑255）。  
- **此程式碼相容於 Java 8 以上嗎？** 當然，API 以 Java 8 及以上版本為目標。

## 在 PSD 檔案中「更改陰影顏色」是什麼？

更改陰影顏色會修改圖層後方投影的色調。此調整讓設計師能模擬不同光源條件、將陰影與品牌色彩相匹配，或為構圖增添藝術感。透過改變色相，您可以讓陰影呈現更暖或更冷的感覺，甚至完全符合特定配色方案，提升整體視覺衝擊力。

## 為何使用 Aspose.PSD for Java 來自訂陰影效果？

Aspose.PSD for Java 支援 **100 多種影像格式**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的 PSD 檔案，提供企業級效能。此函式庫讓您完整掌控每項陰影屬性——顏色、不透明度、距離、角度、擴散與噪點——無需安裝 Photoshop。它可在 Windows、Linux 與 macOS 的 JVM 上執行，是自動化圖形流水線最可靠的選擇。

## 前置條件

- 具備 Java 程式設計的基礎知識。  
- 已安裝 Aspose.PSD for Java。您可於[此處](https://releases.aspose.com/psd/java/)下載。

## 匯入套件

在開始之前，匯入所需的類別以便操作影像與陰影效果：

`Color` 類別代表 API 中使用的顏色值。  
`Image` 類別是所有影像物件的基礎類型。  
`PsdImage` 類別提供針對 PSD 檔案的功能。  
`PsdLoadOptions` 類別允許您為載入 PSD 檔案指定選項，例如啟用效果資源。  
`DropShadowEffect` 類別代表套用於 PSD 圖層的投影濾鏡，並讓您存取其所有可調整屬性。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 步驟指南

### 步驟 1：載入 PSD 影像

首先，在載入來源 PSD 時啟用效果資源的載入：

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 步驟 2：取得現有的投影效果

在目標圖層上定位陰影效果（本例中為第二層）：

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 步驟 3：驗證預設設定（可選）

執行這些斷言可協助您了解在修改前的原始數值：

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

### 步驟 4：**更改陰影顏色** 並自訂其他屬性

現在我們實際將陰影顏色 **更改為綠色**，並調整不透明度、距離、大小及其他屬性。此示範了 Aspose.PSD 的 **自訂陰影效果** 功能。`setOpacity(byte)` 方法設定陰影的不透明度等級（0‑255）。

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### 步驟 5：儲存已修改的影像

最後，使用 `PsdImage` 的 `save` 方法將更新後的 PSD 寫回磁碟：

```java
im.save(psdPathAfterChange);
```

## 常見問題與技巧

- **取得效果時發生 NullPointerException** – 請確保已呼叫 `setLoadEffectsResource(true)`，否則不會載入效果。  
- **顏色未變更** – 請確認您編輯的是正確的圖層索引（本例為 `im.getLayers()[1]`）。  
- **不透明度看似未變** – 請記得不透明度是 byte（0‑255），需要轉型為 `(byte)`。

## 結論

依照上述步驟，您即可 **更改陰影顏色**、**設定陰影不透明度**，以及完整 **自訂陰影效果** 參數，無論是哪個 PSD 檔案，都能透過 Aspose.PSD for Java 以程式方式產生更豐富的圖形，免除手動 Photoshop 操作，非常適合自動化設計流水線與批次處理。

## 常見問答

**問：Aspose.PSD for Java 是否適合專業圖形設計專案？**  
**答：** 絕對適合！Aspose.PSD for Java 是為專業圖形設計任務打造的強大函式庫。

**問：我可以在商業應用程式中使用 Aspose.PSD for Java 嗎？**  
**答：** 是的，Aspose.PSD for Java 為商業產品。您可於[此處](https://purchase.aspose.com/buy)購買。

**問：是否提供免費試用版？**  
**答：** 是的，您可於[此處](https://releases.aspose.com/)體驗免費試用版。

**問：在哪裡可以找到詳細文件？**  
**答：** 請參考完整文件[此處](https://reference.aspose.com/psd/java/)。

**問：如何取得 Aspose.PSD for Java 的支援？**  
**答：** 加入社群論壇[此處](https://forum.aspose.com/c/psd/34)以獲得支援。

---

**最後更新：** 2026-06-18  
**測試版本：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [Java 圖像操作 - 使用 Aspose.PSD for Java 在執行時新增效果](/psd/java/advanced-techniques/add-effects-runtime/)
- [將 PSD 儲存為 PNG 並在 Aspose.PSD for Java 中套用渲染投影](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Java 影像模糊 - 使用 Aspose.PSD 添加模糊效果](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}