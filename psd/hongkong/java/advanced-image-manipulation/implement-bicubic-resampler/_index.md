---
date: 2025-12-01
description: 學習如何在 Java 中使用 Aspose.PSD 的雙三次重採樣器實現高品質圖像縮放。請遵循我們的逐步指南，以獲得卓越效果。
language: zh-hant
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: 在 Aspose.PSD for Java 中使用雙三次重取樣器進行高品質圖像縮放
url: /java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 高品質圖像縮放與 Aspose.PSD for Java 中的雙三次重採樣器

## 簡介

## 快速回答
- **Bicubic Resampler 的作用是什麼？** 它使用複雜的插值演算法，在調整圖像大小時保留細節。  
- **有哪些 ResizeType 值可用？** `CubicConvolution` 與 `Bell` 是 Aspose.PSD 提供的兩個雙三次選項。  
- **執行程式碼是否需要授權？** 臨時授權可用於評估；正式環境需要完整授權。  
- **需要哪個 Java 版本？** 任意 Java 8 以上的執行環境皆相容於最新的 Aspose.PSD 程式庫。  
- **可以使用相同 API 調整其他格式（PNG、JPEG）嗎？** 可以，Aspose.PSD 支援多種圖像類型，儘管範例以 PSD 為主。

## 什麼是高品質圖像縮放？

高品質圖像縮放是指在調整圖像尺寸的同時，保持邊緣銳利、漸層平滑以及色彩精確。雙三次重採樣器透過考慮周圍像素的數值（使用 cubic convolution 或 Bell 演算法）來計算每個新像素，與最近鄰或雙線性方法相比，能產生更自然的外觀。

## 為何在高品質圖像縮放中使用雙三次重採樣器？

- **保留細節：** 即使尺寸變化幅度較大，細緻的紋理與線條仍保持清晰。  
- **減少雜訊：** 最小化在較簡單演算法下常見的環形效應與模糊。  
- **易於整合：** 只需一行方法呼叫 (`image.resize`) 即可在演算法間切換，無需重寫程式碼。  

## 先決條件

在開始之前，請確保您已具備以下項目：

- **Aspose.PSD for Java** – 從 [Aspose.PSD for Java 文件](https://reference.aspose.com/psd/java/) 下載最新的 JAR。  
- **Java Development Kit** – 已安裝並設定 JDK 8 或更新版本。  
- **範例 PSD 檔案** – 測試圖像（例如 `sample_bicubic.psd`），放置於已知目錄中。

## 匯入套件

在 Java 類別中加入必要的匯入。這些匯入會載入 Aspose.PSD 的核心類別與 `ResizeType` 列舉。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 步驟 1：載入圖像

首先，載入您想要調整大小的來源 PSD 檔案。將 `Your Document Directory` 替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## 步驟 2：使用 Cubic Convolution 進行縮放（高品質）

現在套用 **Cubic Convolution** 演算法，這是兩個雙三次選項之一，可實現高品質圖像縮放。範例將圖像縮放至 300 × 300 像素。

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## 步驟 3：使用 Bell 演算法進行縮放（替代高品質）

如果您偏好 **Bell** 演算法，其提供稍有不同的平滑效果，您可以以相同方式使用。請注意，我們會重新載入原始圖像，以確保比較公平。

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

歡迎嘗試其他尺寸或檔案格式——只需相應調整參數即可。

## 常見問題與技巧

- **路徑錯誤：** 確認 `dataDir` 以符合作業系統的檔案分隔符（`/` 或 `\`）結尾。  
- **授權例外：** 未使用有效授權執行時，輸出圖像可能會加上浮水印。  
- **記憶體使用量：** 大型 PSD 檔案可能佔用大量記憶體；儲存後請考慮釋放圖像 (`image.dispose()`)。  

## 常見問與答

**Q: 我可以在 Aspose.PSD for Java 中使用其他圖像格式嗎？**  
A: 可以，程式庫支援 PSD、PNG、JPEG、TIFF、BMP 等多種格式。

**Q: 是否提供 Aspose.PSD for Java 的臨時授權？**  
A: 有，您可從 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 在哪裡可以取得 Aspose.PSD for Java 的支援？**  
A: 請前往 Aspose.PSD 論壇 [此處](https://forum.aspose.com/c/psd/34) 查詢相關支援問題。

**Q: 我可以下載 Aspose.PSD for Java 程式庫嗎？**  
A: 可以，請從發行頁面 [此處](https://releases.aspose.com/psd/java/) 下載。

**Q: 我要如何購買 Aspose.PSD for Java？**  
A: 您可從購買頁面 [此處](https://purchase.aspose.com/buy) 進行購買。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-01  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose