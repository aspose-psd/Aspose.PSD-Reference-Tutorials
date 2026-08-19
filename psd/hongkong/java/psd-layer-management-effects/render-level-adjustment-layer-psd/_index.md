---
date: 2026-04-05
description: 學習如何使用 Aspose.PSD for Java 將 PSD 匯出為 PNG，並輕鬆提升圖像對比度。透過本分步指南，精通色階調整圖層。
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: 在 Java 中將 PSD 匯出為 PNG 並渲染色階調整圖層
second_title: Aspose.PSD Java API
title: 在 Java 中將 PSD 匯出為 PNG 並渲染色階調整圖層
url: /zh-hant/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 PSD 為 PNG 並在 Java 中渲染色階調整圖層

## 介紹

有沒有曾經打開 PSD 檔案後發現顏色顯得平淡或對比不足？您可以使用 Aspose.PSD for Java 快速 **export PSD to PNG**，同時透過色階調整圖層微調影像。本教學將逐步說明整個流程——從載入 PSD、調整色階，到將結果儲存為 PNG——讓您在數分鐘內提升飽和度並準備好可供網頁使用的資產。

## 快速解答
- **What does “export PSD to PNG” mean?** 它會將 Photoshop 文件轉換為無損的 PNG 圖像，同時保留透明度。  
- **Can I adjust levels before exporting?** 可以，Aspose.PSD 允許您以程式方式修改輸入與輸出色階。  
- **Do I need a license?** 免費試用可用於開發；商業授權則需於正式環境使用。  
- **Is batch processing possible?** 完全支援——您可以將程式碼放入迴圈中處理多個 PSD 檔案。  
- **Which Java version is required?** 建議使用 Java 8 或更新版本。

## 「export PSD to PNG」是什麼？
將 PSD 匯出為 PNG 意指將具多圖層的 Photoshop 檔案平面化為 Portable Network Graphics 圖像。PNG 支援無損壓縮與 alpha 通道，非常適合用於網頁圖形與 UI 資產。

## 為什麼在匯出前要調整色階？
調整色階可讓您控制陰影、中間調與高光，提升整體對比度與色彩平衡。此步驟確保最終的 PNG 看起來更為精緻，無需在 Photoshop 中手動編輯。

## 前置條件

- **Java Development Kit (JDK)** – 從 Oracle 官方網站下載最新版本 ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html))。  
- **Aspose.PSD for Java Library** – 從官方下載頁面取得 ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/))。亦提供免費試用版 ([https://releases.aspose.com/](https://releases.aspose.com/))。  

## 匯入套件

在深入程式碼之前，先匯入可讓我們操作 PSD 與匯出 PNG 的類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟指南

### 步驟 1：定義檔案路徑（如何自動化 PSD 處理）

為來源 PSD、已修改 PSD 以及最終 PNG 匯出位置設定清晰且具描述性的變數。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### 步驟 2：載入 PSD 影像

使用 `Image.load` 讀取 PSD 檔案至 `PsdImage` 物件。Aspose.PSD 會自動偵測格式。

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### 步驟 3：遍歷圖層（如何調整色階）

遍歷每一個圖層以定位色階調整圖層。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### 步驟 4：識別色階圖層

使用 `instanceof LevelsLayer` 檢查每個圖層。找到後將其轉型，以便修改其屬性。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### 步驟 5：微調色階（如何調整色階）

為第一通道（通常為合成通道）調整輸入與輸出色階。以下數值僅為示例，您可自行實驗調整。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### 步驟 6：儲存已修改的 PSD（如何自動化 PSD）

將變更持久化為新的 PSD 檔案。

```java
im.save(psdPathAfterChange);
```

### 步驟 7：匯出為 PNG（Export PSD to PNG）

若需要 PNG 版本，設定 `PngOptions` 後儲存影像。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## 常見使用情境

- **Web 資產準備：** 將設計師提供的 PSD 模型轉換為可直接在瀏覽器使用的 PNG。  
- **批次處理：** 在 CI 流程中自動轉換數十個 PSD 檔案。  
- **動態影像產生：** 在匯出前根據使用者輸入即時調整色階。

## 疑難排解與技巧

- **Null pointer when accessing layers:** 確認 PSD 確實包含色階調整圖層；若沒有，請加入 null 檢查。  
- **Unexpected colors after export:** 確認 PNG 色彩類型設定為 `TruecolorWithAlpha` 以保留透明度。  
- **Performance with many files:** 批次處理時重複使用同一個 `PsdImage` 實例，以減少記憶體開銷。

## 常見問題

**Q: Can I adjust individual color channels (RGB) separately?**  
A: 可以。使用 `levelsLayer.getChannel(index)`，其中 `index` = 0 (紅)、1 (綠)、2 (藍) 以分別調整各通道。

**Q: How do I handle multiple Levels Adjustment Layers in one PSD?**  
A: 迴圈會處理每一個圖層；每個找到的 `LevelsLayer` 都會依照 `if` 區塊內的程式碼進行調整。

**Q: Are there other ways to improve contrast besides Levels?**  
A: Aspose.PSD 亦提供曲線、亮度/對比度以及直方圖均衡化等調整功能。

**Q: Can I automate this for a folder of PSD files?**  
A: 可將整個工作流程包裹在 `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` 迴圈中，依序處理每個檔案。

**Q: Where can I find more documentation and support?**  
A: 請造訪官方參考文件 ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) 與社群論壇 ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34))。

## 結論

透過掌握 **export PSD to PNG** 工作流程與 **how to adjust levels** 程式化調整，您即可在不離開 Java 環境的情況下完整控制影像品質。無論是為網站準備資產、自動化設計管線，或是建置批次處理器，Aspose.PSD for Java 都能讓工作變得簡單且可靠。

---

**最後更新：** 2026-04-05  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}