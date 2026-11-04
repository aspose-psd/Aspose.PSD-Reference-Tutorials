---
date: 2026-11-04
description: 了解如何使用 Aspose.PSD for Java 將 PSD 另存為 PNG、匯出具備 alpha 透明度的 PNG，並新增 drop
  shadow 圖層——完整的逐步指南。
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- java image manipulation
lastmod: 2026-11-04
linktitle: 套用 Rendering Drop Shadow
og_description: 使用 Aspose.PSD for Java 將 PSD 另存為 PNG、匯出具備 alpha 透明度的 PNG，並新增 Rendering
  Drop Shadow——針對 Java 開發者的逐步指南。
og_image_alt: Developer guide showing how to convert PSD to PNG and apply drop shadow
  using Aspose.PSD Java
og_title: 在 Aspose.PSD for Java 中將 PSD 另存為 PNG 並套用 Rendering Drop Shadow
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  headline: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  name: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  steps:
  - name: define document directory
    text: Define the directory path where your PSD files are stored.
  - name: set psd and png file paths
    text: Specify the full file paths for the source PSD and the target PNG.
  - name: load psd file with effects
    text: '`PsdImage` loads the PSD and gives access to its layers and effects.'
  - name: access drop shadow effect
    text: '`DropShadowEffect` represents a drop‑shadow layer effect that can be read
      or modified.'
  - name: validate shadow effect properties
    text: '`shadowEffect` holds the properties of the drop‑shadow such as opacity,
      distance, and size. > **Pro tip:** Adjust `setSpread()` or `setNoise()` to create
      softer or more textured shadows.'
  - name: save as png – the “save psd as png” step
    text: '`PngOptions` configures PNG export settings, including color type and alpha
      channel handling. At this point you have successfully **converted psd to png**,
      **exported png with alpha**, and applied a rendering drop shadow in a single
      workflow.'
  type: HowTo
- questions:
  - answer: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect`
      for each target layer, which also lets you perform a batch psd to png conversion.
    question: Can I apply drop shadows to multiple layers simultaneously?
  - answer: '`Spread` determines how abruptly the shadow transitions from full opacity
      to transparent. A higher value creates a harder edge.'
    question: What does the ‘Spread’ parameter control?
  - answer: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release,
      handling most layer types and effects.
    question: Is Aspose.PSD compatible with all Photoshop versions?
  - answer: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/)
      and run the sample without a license key.
    question: How can I test the code before purchasing a license?
  - answer: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      where the community and Aspose engineers can assist.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd as png
- aspose psd java
- java image manipulation
- png transparency
- rendering drop shadow
title: 在 Aspose.PSD for Java 中將 PSD 另存為 PNG 並套用 Rendering Drop Shadow
url: /zh-hant/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 儲存為 PNG 並在 Aspose.PSD for Java 中套用渲染投影

## 介紹

如果你在 Java 中處理 Photoshop 檔案，**saving psd as png** 是最常見的任務之一。在許多專案中，你需要**save psd as png** 以將資產發佈到網站或行動應用程式，同時保留透明度和視覺效果。使用 Aspose.PSD，你不僅可以**convert psd to png**，還能透過**adding a drop shadow layer** 來增強圖像。在本教學中，我們將完整示範整個流程——載入 PSD、套用渲染投影，最後**saving the PSD as a PNG** 檔案——讓你能自信地將此工作流程整合到自己的專案中。

## 快速回答
- **哪個函式庫負責 PSD 轉 PNG 轉換？** Aspose.PSD for Java.  
- **實作投影需要多久？** 基本範例大約需要 10‑15 分鐘。  
- **執行程式碼是否需要授權？** 免費試用可用於評估；正式環境需購買授權。  
- **可以將投影套用到多個圖層嗎？** 可以——只要在迴圈中處理目標圖層，即可同時完成批次 psd to png 轉換。  
- **需要哪個版本的 Java？** Java 8 或更高版本。

## 什麼是 “save psd as png” 以及為何重要？
**Saving a PSD as PNG creates a widely‑supported, lossless image that retains transparency.** 此格式在需要在網頁、行動應用或更大型的影像處理流程中顯示 Photoshop 資產時相當重要。同步加入投影可在不開啟 Photoshop 的情況下產生精緻的視覺效果。

## 為何在此工作流程中使用 Aspose.PSD？
載入時即支援圖層效果的即時渲染，無需 Photoshop。Aspose.PSD 支援超過 50 種輸入與輸出格式（PSD、PNG、JPEG、TIFF、BMP），且可在不將整個檔案載入記憶體的情況下處理大型文件。它能完整保留投影與發光等效果，並自動以帶 Alpha 透明度的 PNG 匯出。

## 前置條件
- **Java Development Environment** – 已安裝 JDK 8 或更新版本。  
- **Aspose.PSD for Java** – 從 [Aspose.PSD 下載頁面](https://releases.aspose.com/psd/java/) 下載最新 JAR。  
- **A PSD file** – 檔案需至少包含一個欲套用投影的圖層（例如 *Shadow.psd*）。

## 匯入套件
`com.aspose.psd` 命名空間提供載入影像、操作圖層與匯出 PNG 檔案的核心類別。  
`PsdImage` 是用來載入與操作 PSD 檔案的主要類別。  

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟指南

### 步驟 1：定義文件目錄
Define the directory path where your PSD files are stored.  

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：設定 PSD 與 PNG 檔案路徑
Specify the full file paths for the source PSD and the target PNG.  

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### 步驟 3：載入含效果的 PSD 檔案
`PsdImage` loads the PSD and gives access to its layers and effects.  

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 步驟 4：存取投影效果
`DropShadowEffect` represents a drop‑shadow layer effect that can be read or modified.  

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 步驟 5：驗證投影效果屬性
`shadowEffect` holds the properties of the drop‑shadow such as opacity, distance, and size.  

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

> **專業提示：** 調整 `setSpread()` 或 `setNoise()` 以產生較柔和或更具紋理的投影。

### 步驟 6：儲存為 PNG – “save psd as png” 步驟
`PngOptions` configures PNG export settings, including color type and alpha channel handling.  

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

此時你已成功 **converted psd to png**、**exported png with alpha**，並在單一工作流程中套用渲染投影。

## 匯出帶 Alpha 透明度的 PNG
當需要 PNG 輸出保留透明背景（特別是 UI 疊層或網頁圖形）時，請務必如上一步使用 `PngColorType.TruecolorWithAlpha`。此設定可確保投影位於透明畫布上，而非實心背景，協助你 **preserve png transparency**。

## 使用 Java 新增投影圖層
如果你的 PSD 包含多個需要投影的圖層，只需在迴圈中重複 **Step 4** 與 **Step 5**，遍歷 `im.getLayers()`。每次迭代皆可建立或修改 `DropShadowEffect` 實例，讓你對每個圖層的透明度、距離、大小與角度進行精細控制。此方式亦能實現 **batch psd to png** 轉換，讓每個檔案皆得到相同的投影處理。

## 常見的 save psd as png 使用情境
* **Web asset pipelines** – 將設計師提供的 PSD 轉換為具備內建投影的 Web‑ready PNG。  
* **Mobile app resources** – 即時產生透明 PNG 圖示，免除手動匯出。  
* **Batch processing** – 在伺服器端工作自動化轉換數百個 PSD 檔，確保每個 PNG 保留 Alpha 通道與視覺效果。  

## 常見問題與解決方案

| 問題 | 可能原因 | 解決方法 |
|------|----------|----------|
| **陰影未顯示** | `Opacity` 設為 0 或圖層被隱藏 | 確認 `shadowEffect.getOpacity()` > 0 且圖層可見。 |
| **PNG 看起來平坦（沒有透明度）** | 使用了錯誤的 `PngColorType` | 使用如上所示的 `PngColorType.TruecolorWithAlpha`。 |
| **載入時發生例外** | 未載入效果 | 確保已呼叫 `loadOptions.setLoadEffectsResource(true)`。 |
| **圖層索引不正確** | PSD 結構不同 | 檢查 `im.getLayers()` 並選擇正確的索引。 |

## 常見問答

**Q: 可以同時將投影套用到多個圖層嗎？**  
A: 可以。遍歷 `im.getLayers()`，為每個目標圖層新增或修改 `DropShadowEffect`，同時也能執行 batch psd to png 轉換。

**Q: ‘Spread’ 參數控制什麼？**  
A: `Spread` 決定投影從完全不透明過渡到透明的突變程度。數值越高，邊緣越硬。

**Q: Aspose.PSD 是否相容所有 Photoshop 版本？**  
A: Aspose.PSD 支援從 Photoshop 3.0 到最新版本的 PSD 檔，能處理大多數圖層類型與效果。

**Q: 如何在購買授權前測試程式碼？**  
A: 從 [Aspose.PSD 下載頁面](https://releases.aspose.com/psd/java/) 下載免費試用版，並在未輸入授權金鑰的情況下執行範例。

**Q: 若遇到問題該向哪裡求助？**  
A: 可在 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 發問，社群與 Aspose 工程師會提供協助。

## 結論

你現在已掌握如何使用 Aspose.PSD for Java **save psd as png**、**export png with alpha**、**convert psd to png**，以及 **apply a drop shadow layer**。此組合讓你能自動化高品質的影像前處理，適用於 Web、行動或桌面應用程式，且無需開啟 Photoshop。

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## 相關教學

- [將 PSD 轉換為 PNG 並套用顏色覆蓋 – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [如何在 PSD 中使用 Java 新增陰影 – 進階圖層效果](/psd/java/advanced-psd-layer-features-effects/)
- [如何使用 Aspose.PSD for Java 將 PSD 轉換為點陣圖格式](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}