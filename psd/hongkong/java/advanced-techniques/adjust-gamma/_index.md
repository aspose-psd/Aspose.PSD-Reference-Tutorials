---
date: 2026-08-01
description: 學習如何在 Java 圖像處理中使用 Aspose.PSD 調整 Gamma、將 PSD 轉換為 TIFF，並在簡潔的教學中修復顏色黯淡的圖像。
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: 調整圖像的 Gamma
og_description: 學習如何在 Java 圖像處理中使用 Aspose.PSD 調整 Gamma – 這是一個快速的伺服器端函式庫，可修正顏色黯淡的圖像，並僅用幾行程式碼將
  PSD 轉換為 TIFF。
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: 如何調整 Gamma – Java 處理與 Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: 如何在 Java 圖像處理中使用 Aspose.PSD 調整 Gamma
url: /zh-hant/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 圖像處理中使用 Aspose.PSD 調整 Gamma

## 介紹

如果您正在從事 **java image processing**，學習 **how to adjust gamma** 是一項基本技術，可在不失去細節的情況下提升亮度與對比度。在本教學中，我們將示範如何使用 **Aspose.PSD for Java** 對 PSD 檔案套用 gamma 校正、**convert PSD to TIFF**，以及避免 **washed‑out image**。您將了解此方法為何快速、可靠，且非常適合 **server‑side image processing** 流程。

## 快速答覆
- **Gamma 校正的作用是什麼？** 它會重新映射亮度值，使暗部變亮或亮部變暗，同時保留整體細節。  
- **哪個函式庫負責處理？** Aspose.PSD for Java 提供專用的 `adjustGamma` 方法來處理光柵圖像。  
- **我可以在同一流程中將 PSD 轉為 TIFF 嗎？** 可以 — 在 gamma 調整後，直接使用 `TiffOptions` 將圖像儲存為 TIFF。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線需購買商業授權。  
- **支援哪個 Java 版本？** Aspose.PSD 支援 Java 8 及以上版本。

## 什麼是 Java Gamma 校正？

Gamma 校正會改變編碼像素值與顯示亮度之間的非線性關係。透過微調 gamma 曲線，您可以 **fix washed out image** 問題，或在不過度曝光高光的情況下增強陰影細節。它透過對每個像素套用冪律函數，使暗部變亮、亮部壓縮，從而產生更自然的視覺效果。

## 為何使用 Aspose.PSD 進行 Gamma 校正？

Aspose.PSD 是一套 **java image processing library**，可抽象化 PSD 格式的複雜性。它支援處理高達 2 GB 的檔案，支援超過 50 種不同的圖像格式，並提供簡單的 `adjustGamma` 呼叫，使其成為 **java gamma correction** 與 **convert PSD to TIFF** 工作流程的理想選擇。

## 前置條件

1. **Java 開發環境** – 已安裝 Java 8 或更新版本。  
2. **Aspose.PSD 函式庫** – 下載並將 JAR 加入專案。請參閱官方 [documentation](https://reference.aspose.com/psd/java/)。  
3. **範例圖像** – 您想要處理的 PSD 檔案（例如 `sample.psd`）。  

## 匯入套件

在開始之前，匯入必要的命名空間，以取得光柵處理與檔案格式選項的存取權。

## 步驟 1：載入圖像

`RasterImage` 類別代表 PSD 圖層在記憶體中的光柵化像素資料。一次載入圖像並快取，可減少後續調整時的記憶體開銷。

## 步驟 2：調整 Gamma

使用 `new RasterImage("sample.psd")` 載入 PSD，然後呼叫 `rasterImage.adjustGamma(2.0f)` — 這行程式碼會在所有顏色通道上套用 2.0 的 gamma，讓陰影變亮且保持高光完整。若需要對紅、綠、藍通道分別調整，可傳入各自的值。

## 步驟 3：建立 TiffOptions

`TiffOptions` 讓您控制壓縮方式、每樣本位元數等 TIFF 專屬設定。設定 8 位樣本 (`{8,8,8}`) 可在保持色彩忠實度的同時，讓 TIFF 檔案大小保持合理。

## 步驟 4：儲存結果圖像

呼叫 `rasterImage.save("output.tif", tiffOptions)` 即可將處理後的圖像寫入磁碟。儲存完成後，您可以將 TIFF 送入後續系統，例如列印服務或 Web API。

## 常見使用情境

- **自動化圖形流水線** – 在產生縮圖前即時調整 gamma。  
- **批次轉換工具** – 在將大量 PSD 檔案轉為 TIFF 時，同步正規化亮度。  
- **Web 服務** – 提供端點接收 PSD、套用 gamma 校正，並回傳 TIFF 給客戶端使用。

## 常見問題與解決方案

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Image appears washed out** | Gamma value too high (e.g., > 2.5) | Lower the gamma factor to a value between 1.8 and 2.2. |
| **`rasterImage.isCached()` returns false** | Image not yet loaded into memory | Call `rasterImage.cacheData()` before adjusting gamma. |
| **TIFF file size is large** | Bits per sample set to 16‑bit | Use an 8‑bit sample (`{8,8,8}`) as shown in the example. |

## 常見問答

**Q: 可以對每個顏色通道套用不同的 gamma 值嗎？**  
A: 可以 — `adjustGamma` 方法接受紅、綠、藍三個獨立的 float 值。

**Q: 能否在儲存前鏈接多個圖像調整操作？**  
A: 完全可以。您可以在同一個 `RasterImage` 實例上依序執行調整大小、裁切或顏色校正等操作。

**Q: Aspose.PSD 支援多頁 PSD 檔案嗎？**  
A: 支援，每個圖層皆可單獨存取與處理。

**Q: 除了 TIFF，還能匯出哪些格式？**  
A: Aspose.PSD 支援 PNG、JPEG、BMP 等多種格式，皆可透過對應的 Options 類別設定。

**Q: 如何避免 gamma 校正後出現 washed‑out image？**  
A: 從適中的 gamma（約 2.0）開始，預覽結果後若圖像過亮，請降低 gamma 值。

## 結論

恭喜您！您已成功學會在 **java image processing** 工作流程中 **how to adjust gamma**，並將 PSD 轉為 TIFF，同時避免常見的 **washed‑out image** 問題。此模式讓您對亮度與對比度擁有精細的控制，十分適合自動化圖形流水線、Web 服務或桌面工具使用。

---

**Last Updated:** 2026-08-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [Java Image Processing Tutorial - Adjust Brightness of an Image with Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [How to Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Convert PSD to Image in Java – Apply Adjustment Layers with Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```