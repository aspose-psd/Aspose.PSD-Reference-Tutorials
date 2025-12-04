---
date: 2025-12-04
description: 了解如何使用 Aspose.PSD for Java 將 PSD 儲存為 PNG 並套用渲染陰影。本指南涵蓋如何添加陰影、將 PSD 轉換為
  PNG，以及在 Java 中套用陰影。
language: zh-hant
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: 將 PSD 另存為 PNG 並使用 Aspose.PSD Java 添加投影陰影
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 另存為 PNG 並使用 Aspose.PSD Java 添加投影

## 簡介

如果你在 Java 中處理 Photoshop 檔案，**將 PSD 另存為 PNG** 並加入專業外觀的投影是常見需求。Aspose.PSD 讓此工作變得簡單，只需幾行程式碼即可 **將 PSD 轉換為 PNG** 並 **在 Java 中套用投影**。本教學將逐步說明整個流程，從載入 PSD 檔案到匯出帶有渲染投影效果的最終 PNG。

## 快速解答
- **「將 PSD 另存為 PNG」是什麼意思？** 它會將具層次的 Photoshop 檔案轉換為平面 PNG 圖像，並保留透明度。  
- **轉換時可以加入投影嗎？** 可以——Aspose.PSD 允許你在匯出前修改圖層效果。  
- **執行程式碼需要授權嗎？** 免費試用可用於評估；正式環境需購買授權。  
- **支援哪個 Java 版本？** Java 8 或以上。  
- **投影效果可以自訂嗎？** 當然可以——你可以調整顏色、不透明度、距離、大小、角度等多項參數。

## 先決條件

在開始之前，請確保你已具備以下條件：

- **Java 開發環境** – 已安裝 JDK 8 或更新版本。  
- **Aspose.PSD 函式庫** – 從官方網站[此處](https://releases.aspose.com/psd/java/)下載最新 JAR。  
- **PSD 檔案** – 包含至少一個你想加入投影的圖層的檔案。  

## 如何在 Java 中將 PSD 另存為 PNG 並添加投影？

以下為逐步指南。每一步都包含簡短說明，並附上需要複製的完整程式碼。

### 步驟 1：匯入必要的套件

我們先匯入提供影像載入、效果處理與 PNG 匯出功能的類別。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### 步驟 2：定義文件目錄

設定來源 PSD 與最終 PNG 所在的資料夾。

```java
String dataDir = "Your Document Directory";
```

### 步驟 3：設定 PSD 與 PNG 檔案路徑

指定輸入 PSD 與輸出 PNG 的完整路徑。

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### 步驟 4：載入啟用效果的 PSD 檔案

啟用 **loadEffectsResource** 可確保圖層效果（如投影）可供操作。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 步驟 5：取得投影效果

此處取得套用於第二層（索引 1）的第一個效果。我們將在此讀取或修改投影參數。

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 步驟 6：驗證投影效果屬性（可選但有幫助）

檢查現有屬性可協助你判斷是否需要變更。以下斷言驗證預設值。

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

> **專業提示：** 若想以自訂設定 **如何添加投影**，請在儲存前修改 `shadowEffect` 的屬性（例如 `shadowEffect.setColor(Color.getRed());`）。

### 步驟 7：將修改後的影像儲存為 PNG

最後，我們將帶有渲染投影的 PSD 匯出為 PNG 檔案。`TruecolorWithAlpha` 選項可保留透明度。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

這樣就完成了一個完整的 **將 PSD 轉換為 PNG** 工作流程，同時在一次操作中 **在 Java 中套用投影**。

## 為什麼要使用 Aspose.PSD 來完成此任務？

- **不需原生 Photoshop** – 可在任何支援 Java 的平台上執行。  
- **完整的 PSD 相容性** – 所有圖層資訊、遮色片與效果皆會保留。  
- **細緻的控制** – 在匯出前可調整投影的每個參數。  
- **高效能** – 為大型檔案與批次處理進行最佳化。  

## 常見問題與疑難排解

| 症狀 | 可能原因 | 解決方案 |
|------|----------|----------|
| `shadowEffect` 上的 `NullPointerException` | 目標圖層沒有效果或索引錯誤。 | 驗證圖層索引 (`im.getLayers()[i]`) 並確保存在效果。 |
| 匯出的 PNG 為空白 | PNG 選項未正確設定或影像未儲存。 | 使用 `PngColorType.TruecolorWithAlpha`，並確認 `im.save()` 的路徑可寫入。 |
| 投影顏色不可見 | 投影不透明度設為 0 或顏色與背景相同。 | 設定 `shadowEffect.setOpacity(255);` 並選擇對比色。 |

## 常見問答

**問：我可以一次對多個圖層套用投影嗎？**  
答：可以。遍歷 `im.getLayers()`，根據需要修改每個圖層的 `DropShadowEffect`。

**問：‘Spread’ 參數的作用是什麼？**  
答：它控制投影從完全不透明到透明的過渡程度。較高的 Spread 會產生較硬的邊緣。

**問：Aspose.PSD 是否相容所有 Photoshop 版本？**  
答：它支援廣泛的 PSD 版本，從早期版本到最新的 Photoshop CC 檔案皆可。

**問：如果遇到問題，如何取得協助？**  
答：前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 獲得社群支援與官方協助。

**問：我可以在購買前試用 Aspose.PSD 嗎？**  
答：當然可以。從 [Aspose 官方網站](https://releases.aspose.com/) 下載免費試用版。

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**最後更新：** 2025-12-04  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose