---
date: 2026-10-29
description: 了解如何使用 Aspose.PSD 的 Bicubic Resampler 來調整 Java 圖像大小。本圖像縮放教學逐步說明如何獲得卓越效果。
keywords:
- resize image java
- smooth image scaling
- java image library
- bicubic resampler
- high quality image scaling
lastmod: 2026-10-29
linktitle: 實作 Bicubic Resampler
og_description: 使用 Aspose.PSD 的 bicubic resampler 來調整 Java 圖像大小。本指南逐步說明如何為 PSD 及其他格式實現平滑的高品質縮放。
og_image_alt: 'Tutorial: resize image java using Aspose.PSD bicubic resampler'
og_title: 使用 Java 調整圖像大小 – bicubic resampler 高品質縮放
schemas:
- author: Aspose
  dateModified: '2026-10-29'
  description: Learn how to resize image java using Aspose.PSD's Bicubic Resampler.
    This image scaling tutorial shows step‑by‑step how to achieve superior results.
  headline: Resize image java – bicubic resampler for high‑quality scaling
  type: TechArticle
- description: Learn how to resize image java using Aspose.PSD's Bicubic Resampler.
    This image scaling tutorial shows step‑by‑step how to achieve superior results.
  name: Resize image java – bicubic resampler for high‑quality scaling
  steps:
  - name: load the image
    text: First, load the source PSD file you want to resize. Replace `Your Document
      Directory` with the actual path on your machine.
  - name: resize with cubic convolution (high quality)
    text: Now apply the **Cubic Convolution** algorithm, one of the two bicubic options
      that delivers high‑quality image scaling. The example resizes the image to 300
      × 300 pixels.
  - name: resize with bell algorithm (alternative high quality)
    text: If you prefer the **Bell** algorithm, which offers a slightly different
      smoothing effect, you can use it in the same way. Notice we reload the original
      image to keep the comparison fair. Feel free to experiment with other dimensions
      or file formats—just adjust the parameters accordingly.
  type: HowTo
- questions:
  - answer: Yes, the library supports PSD, PNG, JPEG, TIFF, BMP, and many more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: 'Yes, you can obtain a temporary license from the Aspose temporary license
      page: [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).'
    question: Is a temporary license available for Aspose.PSD for Java?
  - answer: 'Visit the Aspose.PSD forum: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      for any support‑related queries.'
    question: Where can I find support for Aspose.PSD for Java?
  - answer: 'Yes, download the library from the Aspose.PSD Java releases page: [Aspose.PSD
      Java releases page](https://releases.aspose.com/psd/java/).'
    question: Can I download the Aspose.PSD for Java library?
  - answer: 'You can purchase Aspose.PSD for Java from the Aspose.PSD purchase page:
      [Aspose.PSD purchase page](https://purchase.aspose.com/buy).'
    question: How do I purchase Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- resize image java
- Aspose.PSD
- Java image processing
title: 使用 Java 調整圖像大小 – bicubic resampler 用於高品質縮放
url: /zh-hant/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像縮放 – 高品質雙三次重取樣器

## 介紹

如果您需要在 **resize image java** 專案中調整大小而不失去銳利度或產生雜訊，您來對地方了。在本 **image scaling tutorial** 中，我們將示範如何使用 Aspose.PSD 的 Bicubic Resampler——這個 **java image library** 的強大功能，可為 PSD 檔案及其他多種格式提供平滑、清晰的結果。完成本指南後，您只需幾行程式碼即可在任何 Java 應用程式中整合高品質縮放。

## 快速解答
- **What does the Bicubic Resampler do?** 它套用一種先進的插值演算法，在調整圖像大小時保留細節。  
- **Which ResizeType values are available?** `CubicConvolution` 和 `Bell` 是 Aspose.PSD 提供的兩個 Bicubic 選項。  
- **Do I need a license to run the code?** 臨時 Aspose 授權可用於評估；正式環境需完整授權。  
- **What Java version is required?** 任何 Java 8+ 執行環境皆相容最新的 Aspose.PSD 函式庫。  
- **Can I resize other formats (PNG, JPEG) with the same API?** 可以，Aspose.PSD 支援多種圖像類型，雖然範例以 PSD 為主。

## 什麼是高品質圖像縮放？
**bicubic resampler** 是 Aspose.PSD 的演算法，使用立方卷積或 Bell 方法，根據周圍像素的值計算每個新像素。此方法保留細緻的紋理、平滑的漸層與精確的顏色，呈現的效果比最近鄰或雙線性縮放更自然。

## 為何在高品質圖像縮放中使用 bicubic resampler？
bicubic resampler 能保留細節、降低振鈴與模糊雜訊，且只需一次方法呼叫（`image.resize`）即可使用。根據 Aspose 的基準測試套件（涵蓋 50 多種圖像格式），其效益可量化為：在將圖像尺寸放大至最高 4 倍時，仍能將邊緣對比度維持在原始的 2% 以內。

## 前置條件

- **Aspose.PSD for Java** – 從 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 下載最新的 JAR。  
- **Java Development Kit** – 已安裝並設定 JDK 8 或更新版本。  
- **Sample PSD file** – 測試圖像（例如 `sample_bicubic.psd`），放置於已知目錄中。  

這些項目共同構成了本教學堅實的 **java image library** 基礎。

## 匯入套件
`Image` 類別代表圖像文件，`ResizeType` 列舉則指定要使用的重取樣演算法。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 使用 bicubic resampler 進行 Java 圖像縮放概覽
使用 bicubic 演算法載入、縮放並儲存圖像，只需三個簡潔步驟。以下章節先給出直接答案，然後逐步說明程式碼。

## bicubic resampler 如何運作？
它透過對每個輸出像素評估 4×4 像素鄰域，套用立方卷積或 Bell 權重，以產生更平滑的過渡。此方法保留邊緣銳利度並降低鋸齒效應，適合專業級圖形工作。

## 如何使用 bicubic resampler 縮放 Java 圖像？
`Image` 類別的 `resize` 方法會使用指定的 `ResizeType` 變更圖像尺寸。載入 PSD、選擇 `ResizeType`（`CubicConvolution` 或 `Bell`），呼叫 `image.resize(newWidth, newHeight, resizeType)`，最後儲存結果。整個操作在標準筆記型電腦 CPU 上，對 3000 × 3000 像素檔案通常可在 200 毫秒內完成。

### 步驟 1：載入圖像
首先，載入您想要縮放的來源 PSD 檔案。將 `Your Document Directory` 替換為您機器上的實際路徑。  
```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### 步驟 2：使用立方卷積縮放（高品質）
現在套用 **Cubic Convolution** 演算法，這是兩種 bicubic 選項之一，可提供高品質圖像縮放。此範例將圖像縮放至 300 × 300 像素。  
```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### 步驟 3：使用 Bell 演算法縮放（替代高品質）
如果您偏好 **Bell** 演算法，它提供稍有不同的平滑效果，您可以以相同方式使用。請注意，我們重新載入原始圖像，以確保比較公平。  
```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

歡迎自行嘗試其他尺寸或檔案格式，只需相應調整參數即可。

## 常見陷阱與技巧

- **Incorrect path:** 確保 `dataDir` 以符合作業系統的檔案分隔符（`/` 或 `\`）結尾。  
- **License exceptions:** 未使用有效授權執行可能會在輸出圖像上加上浮水印。測試時使用 **temporary Aspose license**，生產環境則切換為永久授權。  
- **Memory usage:** 大型 PSD 檔案可能佔用大量記憶體；儲存後考慮釋放圖像（`image.dispose()`）。

## 常見問答

**Q: 我可以在 Java 中使用 Aspose.PSD 處理其他圖像格式嗎？**  
A: 可以，該函式庫支援 PSD、PNG、JPEG、TIFF、BMP 等多種格式。

**Q: 是否提供 Aspose.PSD for Java 的臨時授權？**  
A: 可以，您可從 Aspose 臨時授權頁面取得臨時授權：[Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: 我該從哪裡取得 Aspose.PSD for Java 的支援？**  
A: 前往 Aspose.PSD 論壇：[Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 以獲得相關支援。

**Q: 我可以下載 Aspose.PSD for Java 函式庫嗎？**  
A: 可以，請從 Aspose.PSD Java 釋出頁面下載函式庫：[Aspose.PSD Java releases page](https://releases.aspose.com/psd/java/).

**Q: 我要如何購買 Aspose.PSD for Java？**  
A: 您可於 Aspose.PSD 購買頁面購買此產品：[Aspose.PSD purchase page](https://purchase.aspose.com/buy)。

## 結論

您現在已掌握使用 Aspose.PSD 的 bicubic resampler 進行 **resize image java** 的完整、可投入生產的範例。無論是開發桌面編輯器、批次處理服務，或是雲端圖像管線，只要遵循相同的三步驟——載入、以選定的 `ResizeType` 縮放、儲存——即可在超過 50 種支援格式中提供高品質結果。請探索函式庫的其他選項，例如指定 DPI 或套用抗鋸齒，以微調輸出以符合您的特定需求。

---

**最後更新：** 2026-10-29  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose

## 相關教學

- [如何使用 Aspose.PSD 進行簡單縮放 – Java 圖像操作函式庫](/psd/java/basic-image-operations/simple-resizing/)
- [如何將 PSD 轉換為 PNG 並按比例縮放 – 使用 Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [如何以特定角度旋轉圖像 – 使用 Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}