---
date: 2025-12-30
description: 學習如何使用 Aspose.PSD for Java 更改陰影顏色並自訂陰影效果。請跟隨此一步一步的陰影效果教學。
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 更改陰影顏色
url: /zh-hant/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 更改陰影顏色

## 介紹

為圖形添加層次感通常意味著 **更改陰影顏色** 以配合設計氛圍。使用 Aspose.PSD for Java，您可以輕鬆加入或修改投影陰影效果、控制不透明度，並微調其他參數——全部透過 Java 程式碼完成。在本 **陰影效果教學** 中，我們將示範如何載入 PSD、讀取現有陰影、客製化其顏色、不透明度、距離，最後儲存更新後的檔案。

## 快速答覆
- **「更改陰影顏色」是什麼意思？** 它會更新套用於 PSD 圖層的 DropShadowEffect 的 color 屬性。  
- **哪個函式庫支援此功能？** Aspose.PSD for Java 完整支援陰影效果。  
- **需要授權嗎？** 開發階段可使用試用版；正式上線需購買商業授權。  
- **可以設定陰影不透明度嗎？** 可以 – 使用 `setOpacity(byte)` 來定義透明度（0‑255）。  
- **程式碼相容於 Java 8+ 嗎？** 完全相容，API 目標為 Java 8 及以上版本。

## 在 PSD 檔案中「更改陰影顏色」是什麼？

更改陰影顏色會改變圖層背後投影的色調。這對於營造真實光影、配合品牌色或單純增添藝術感都非常有用。

## 為什麼使用 Aspose.PSD for Java 來自訂陰影效果？

- **完整 PSD 相容性** – 所有圖層效果（包括陰影）皆會被保留。  
- **不需 Photoshop** – 可在任何伺服器上以程式方式操作檔案。  
- **細緻控制** – 調整顏色、不透明度、距離、角度、擴散與噪點。  
- **跨平台** – 支援 Windows、Linux 與 macOS 的 JVM。

## 先決條件

- 具備 Java 程式設計基礎。  
- 已安裝 Aspose.PSD for Java。您可於 [此處](https://releases.aspose.com/psd/java/) 下載。

## 匯入套件

在開始之前，先匯入所需的類別，以便操作影像與陰影效果：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 逐步指南

### 步驟 1：載入 PSD 影像

先載入來源 PSD，並啟用效果資源的載入：

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 步驟 2：取得現有的投影陰影效果

在目標圖層（本例為第二層）上定位陰影效果：

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 步驟 3：驗證預設設定（可選）

執行這些斷言可讓您在修改前了解原始值：

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

現在我們實際 **更改陰影顏色** 為綠色，調整不透明度、距離、大小等屬性。此範例展示了 Aspose.PSD 的 **自訂陰影效果** 能力：

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

最後，將更新後的 PSD 寫回磁碟：

```java
im.save(psdPathAfterChange);
```

## 常見問題與技巧

- **取得效果時拋出 NullPointerException** – 請確認已呼叫 `setLoadEffectsResource(true)`，否則不會載入效果。  
- **顏色未變更** – 請確認您編輯的是正確的圖層索引（本例為 `im.getLayers()[1]`）。  
- **不透明度看起來未變** – 記得不透明度是 byte（0‑255），必須強制轉型為 `(byte)`。

## 結論

依循上述步驟，您即可 **更改陰影顏色**、**設定陰影不透明度**，並完整 **自訂陰影效果** 參數，使用 Aspose.PSD for Java 在任何 PSD 檔案中程式化地打造更豐富的圖形，無需手動操作 Photoshop。

## 常見問題

**Q: Aspose.PSD for Java 適合專業圖形設計專案嗎？**  
A: 絕對適合！Aspose.PSD for Java 是為專業圖形設計任務打造的強大函式庫。

**Q: 我可以在商業應用中使用 Aspose.PSD for Java 嗎？**  
A: 可以，Aspose.PSD for Java 為商業產品。您可於 [此處](https://purchase.aspose.com/buy) 購買。

**Q: 有免費試用版嗎？**  
A: 有，您可在 [此處](https://releases.aspose.com/) 取得免費試用版。

**Q: 哪裡可以找到詳細文件？**  
A: 請參考完整文件 [此處](https://reference.aspose.com/psd/java/)。

**Q: 如何取得 Aspose.PSD for Java 的支援？**  
A: 可前往社群論壇 [此處](https://forum.aspose.com/c/psd/34) 提問。

---

**最後更新：** 2025-12-30  
**測試環境：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}