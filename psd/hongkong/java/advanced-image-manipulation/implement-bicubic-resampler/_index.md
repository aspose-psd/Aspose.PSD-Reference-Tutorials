---
date: 2026-04-12
description: 學習如何在 Java 中使用 Aspose.PSD 的雙三次重採樣器調整圖像大小。此圖像縮放教學將一步步說明如何獲得卓越的效果。
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: 實作雙立方重取樣器
second_title: Aspose.PSD Java API
title: Java 圖像縮放 – 高品質縮放的雙三次重採樣器
url: /zh-hant/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 調整圖像大小（Java） – 雙三次重採樣器 用於高品質縮放

## 介紹

如果您需要在 **resize image java** 專案中調整圖像大小而不失去銳利度或產生雜訊，您來對地方了。在本 **image scaling tutorial** 中，我們將示範如何使用 Aspose.PSD 的雙三次重採樣器——這是一項強大的 **java image library** 功能，可為 PSD 檔案及其他多種格式提供平滑、清晰的結果。閱讀完本指南後，您只需幾行程式碼即可在任何 Java 應用程式中整合高品質縮放功能。

## 快速回答
- **Bicubic Resampler 的作用是什麼？** 它使用複雜的插值演算法，在調整圖像大小時保留細節。  
- **有哪些 ResizeType 值可用？** `CubicConvolution` 與 `Bell` 為 Aspose.PSD 提供的兩種雙三次選項。  
- **執行程式碼是否需要授權？** 臨時的 aspose 授權可用於評估；正式環境需使用完整授權。  
- **需要哪個 Java 版本？** 任意 Java 8 以上的執行環境皆相容最新的 Aspose.PSD 函式庫。  
- **可以使用相同 API 調整其他格式（PNG、JPEG）嗎？** 可以，Aspose.PSD 支援多種圖像類型，雖然範例以 PSD 為主。

## 什麼是高品質圖像縮放？

高品質圖像縮放指在調整圖像尺寸的同時，保持邊緣銳利、漸層平滑以及色彩精準。雙三次重採樣器透過考慮周圍像素的數值（使用 cubic convolution 或 Bell 演算法）來計算每個新像素，較之最近鄰或雙線性方法可呈現更自然的效果。

## 為何在高品質圖像縮放中使用雙三次重採樣器？

- **保留細節：** 即使尺寸變化幅度較大，細緻的紋理與線條仍保持清晰。  
- **減少雜訊：** 可減少較簡單演算法常見的振鈴與模糊現象。  
- **易於整合：** 只需一行方法呼叫（`image.resize`）即可在演算法間切換，無需重寫程式碼。  

## 前置條件

- **Aspose.PSD for Java** – 從 [Aspose.PSD for Java 文檔](https://reference.aspose.com/psd/java/) 下載最新的 JAR。  
- **Java Development Kit** – 已安裝並設定 JDK 8 或更新版本。  
- **Sample PSD file** – 測試圖像（例如 `sample_bicubic.psd`），放置於已知目錄中。  

上述項目共同構成本教學的堅實 **java image library** 基礎。

## 匯入套件

在 Java 類別中加入所需的匯入語句。這些語句會載入 Aspose.PSD 的核心類別以及 `ResizeType` 列舉。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 如何使用雙三次重採樣器在 Java 中調整圖像大小

### 步驟 1：載入圖像

首先，載入您想要調整大小的來源 PSD 檔案。將 `Your Document Directory` 替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### 步驟 2：使用 Cubic Convolution（高品質）進行縮放

現在套用 **Cubic Convolution** 演算法，這是兩種雙三次選項之一，可提供高品質的圖像縮放。範例將圖像縮放至 300 × 300 像素。

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### 步驟 3：使用 Bell 演算法（替代高品質）進行縮放

如果您偏好 **Bell** 演算法，它提供稍微不同的平滑效果，您可以以相同方式使用。請注意，我們會重新載入原始圖像，以確保比較公平。

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

歡迎自行嘗試其他尺寸或檔案格式——只需相應調整參數即可。

## 常見陷阱與技巧

- **路徑錯誤：** 確認 `dataDir` 以符合作業系統的檔案分隔符（`/` 或 `\`）結尾。  
- **授權例外：** 未使用有效授權執行時，輸出圖像可能會加上浮水印。測試時可使用 **temporary aspose license**，正式環境請改為永久授權。  
- **記憶體使用量：** 大型 PSD 檔案可能佔用大量記憶體；儲存後建議釋放圖像（`image.dispose()`）。  

## 常見問答

**Q: 我可以在 Java 中使用 Aspose.PSD 處理其他圖像格式嗎？**  
A: 可以，該函式庫支援 PSD、PNG、JPEG、TIFF、BMP 等多種格式。

**Q: Aspose.PSD for Java 是否提供臨時授權？**  
A: 可以，您可從 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 我可以在哪裡取得 Aspose.PSD for Java 的支援？**  
A: 請前往 Aspose.PSD 論壇 [此處](https://forum.aspose.com/c/psd/34) 取得相關支援。

**Q: 我可以下載 Aspose.PSD for Java 函式庫嗎？**  
A: 可以，請從發行頁面 [此處](https://releases.aspose.com/psd/java/) 下載。

**Q: 我要如何購買 Aspose.PSD for Java？**  
A: 您可於購買頁面 [此處](https://purchase.aspose.com/buy) 進行購買。

---

**最後更新：** 2026-04-12  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}