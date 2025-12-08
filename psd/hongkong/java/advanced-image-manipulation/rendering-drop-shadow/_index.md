---
date: 2025-12-05
description: 學習如何將 PSD 存成 PNG、將 PSD 轉換為 PNG，並使用 Aspose.PSD for Java 為圖層套用投影效果——完整的逐步指南。
language: zh-hant
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: 將 PSD 另存為 PNG 並在 Aspose.PSD for Java 中套用渲染投影
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 儲存為 PNG 並在 Aspose.PSD for Java 中套用渲染陰影

## 簡介

如果你在 Java 中處理 Photoshop 檔案，**saving PSD as PNG** 是你最常會遇到的工作之一。使用 Aspose.PSD，你不僅可以 **convert PSD to PNG**，還能透過 **adding a drop shadow layer** 來增強影像。在本教學中，我們將逐步說明整個流程——載入 PSD、套用渲染陰影，最後 **saving the PSD as a PNG** 檔案——讓你能自信地將此工作流程整合到自己的專案中。

## 快速回答
- **什麼函式庫負責 PSD 轉 PNG 轉換？** Aspose.PSD for Java。  
- **實作 drop‑shadow 需要多久？** 基本範例大約 10‑15 分鐘。  
- **執行程式碼是否需要授權？** 免費試用版可用於評估；正式環境需購買授權。  
- **可以將陰影套用到多個圖層嗎？** 可以——只要遍歷目標圖層即可。  
- **需要哪個版本的 Java？** Java 8 或更高版本。

## 什麼是「save PSD as PNG」以及為何重要？

將 PSD 儲存為 PNG 可產生一種廣受支援、無失真的影像，且保留透明度。當你需要在網站、行動應用程式或更大型的影像處理流程中顯示 Photoshop 資產時，這是必不可少的。同時加入陰影，讓你無需開啟 Photoshop 即可產生精緻的視覺效果。

## 先決條件

- **Java 開發環境** – 已安裝 JDK 8 或更新版本。  
- **Aspose.PSD for Java** – 從 [Aspose.PSD 下載頁面](https://releases.aspose.com/psd/java/) 下載最新的 JAR。  
- **PSD 檔案** – 檔案需至少包含一個你想套用 drop shadow 的圖層（例如 *Shadow.psd*）。  

## 匯入套件

首先，匯入我們需要的類別。這讓我們能存取影像載入、圖層效果以及 PNG 匯出選項。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## 逐步指南

### 步驟 1：定義文件目錄  
告訴程式你的來源 PSD 檔案所在的目錄。

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：設定 PSD 與 PNG 檔案路徑  
指定輸入的 PSD 檔案以及將包含渲染陰影的輸出 PNG 檔案。

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### 步驟 3：載入含效果的 PSD 檔案  
啟用載入效果資源，以便我們能操作 drop‑shadow 效果。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 步驟 4：取得 Drop Shadow 效果  
從第二個圖層（索引 1）取得第一個 drop‑shadow 效果。這裡我們會驗證或修改參數。

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 步驟 5：驗證陰影效果屬性  
在儲存前，確保效果的屬性符合預期。你也可以微調這些數值以獲得不同的外觀。

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

> **專業提示：** 調整 `setSpread()` 或 `setNoise()` 以產生較柔和或更具紋理的陰影。

### 步驟 6：儲存為 PNG – 「save PSD as PNG」步驟  
將修改後的影像匯出為 PNG，保留 alpha 通道，使陰影能正確混合。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

此時，你已成功 **converted PSD to PNG**，並在單一工作流程中套用了渲染陰影。

## 常見問題與解決方案

| 問題 | 可能原因 | 解決方法 |
|------|----------|----------|
| **陰影未顯示** | `Opacity` 設為 0 或圖層被隱藏 | 確認 `shadowEffect.getOpacity()` > 0 且圖層可見。 |
| **PNG 看起來平坦（無透明度）** | 使用了錯誤的 `PngColorType` | 如範例所示，使用 `PngColorType.TruecolorWithAlpha`。 |
| **載入時例外** | 未載入效果 | 確保已呼叫 `loadOptions.setLoadEffectsResource(true)`。 |
| **圖層索引不正確** | PSD 結構不同 | 檢查 `im.getLayers()` 並選擇正確的索引。 |

## 常見問答

**Q: 我可以同時將 drop shadows 套用到多個圖層嗎？**  
A: 可以。遍歷 `im.getLayers()`，為每個目標圖層新增或修改 `DropShadowEffect`。

**Q: ‘Spread’ 參數控制什麼？**  
A: `Spread` 決定陰影從完全不透明過渡到透明的突變程度。較高的數值會產生較硬的邊緣。

**Q: Aspose.PSD 是否相容所有 Photoshop 版本？**  
A: Aspose.PSD 支援從 Photoshop 3.0 到最新版本的 PSD 檔案，能處理大多數圖層類型與效果。

**Q: 我該如何在購買授權前測試程式碼？**  
A: 從 [Aspose.PSD 下載頁面](https://releases.aspose.com/psd/java/) 下載免費試用版，並在未提供授權金鑰的情況下執行範例。

**Q: 若遇到問題，我可以在哪裡取得協助？**  
A: 在 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 發問，社群與 Aspose 工程師會提供協助。

## 結論

現在你已了解如何使用 Aspose.PSD for Java **save PSD as PNG**、**convert PSD to PNG**，以及 **apply a drop shadow layer**。此組合讓你能自動化高品質的影像準備，適用於網站、行動或桌面應用程式——無需開啟 Photoshop。

---

**最後更新：** 2025-12-05  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}