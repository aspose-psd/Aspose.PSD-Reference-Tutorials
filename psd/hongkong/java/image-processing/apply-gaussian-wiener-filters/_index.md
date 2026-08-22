---
date: 2026-07-17
description: 使用 Aspose.PSD 的 Java 圖像處理教學，學習如何逐步套用 Gaussian 與 Wiener 濾鏡，打造驚艷的視覺效果。
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: 套用 Gaussian 與 Wiener 濾鏡
og_description: 此 Java 圖像處理教學示範如何使用 Aspose.PSD for Java 套用 Gaussian 與 Wiener 濾鏡，並支援匯出為
  PNG 及其他格式。
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: Java 圖像處理教學 – 套用 Gaussian 與 Wiener 濾鏡
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: Java 圖像處理教學 – 套用 Gaussian 與 Wiener 濾鏡
url: /zh-hant/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像處理教學 – 使用 Aspose.PSD 套用 Gaussian 與 Wiener 濾鏡

## 介紹

歡迎閱讀我們的 **java image processing tutorial**，本教學示範如何使用 Aspose.PSD for Java 套用 Gaussian 與 Wiener 濾鏡。無論是清理噪點照片或是為網路發佈準備圖形，這些濾鏡都能提供平滑、專業的效果。接下來的幾分鐘內，您將看到完整的工作流程——從載入 PSD 檔案到將過濾後的輸出儲存為 GIF。

## 快速解答
- **What does the Gaussian filter do?** 它透過對相鄰像素取平均來平滑影像，減少高頻噪聲。  
- **What is the Wiener filter?** 它執行自適應平滑，保留邊緣同時降低噪聲。  
- **Which library is used?** Aspose.PSD for Java 內建支援兩種濾鏡。  
- **Do I need a license?** 試用版可用於測試，但正式環境需購買商業授權。  
- **Can I output formats other than GIF?** 可以——Aspose.PSD 支援 PNG、JPEG、BMP 等多種格式。

## 什麼是 Java 圖像處理教學？

Java 圖像處理教學會引導開發者完成載入影像、套用轉換（如濾鏡或調整大小）以及最終以指定格式儲存結果的基本步驟。透過清晰的程式碼範例與說明，協助您將影像處理功能直接整合至 Java 應用程式，減少對外部工具的依賴。

## 為什麼使用 Gaussian 與 Wiener 濾鏡？

載入影像後套用結合的 Gaussian‑Wiener 濾鏡，您會看到顆粒感大幅降低，而關鍵邊緣仍保持銳利——非常適合用於網頁圖形或檔案掃描的前處理。Gaussian 部分去除高頻噪聲，Wiener 部分則根據局部變異自適應，保留最重要的細節。

## 前置條件

在開始之前，請確保您已具備：

- Java 開發環境（JDK 8 或更新版本）。  
- Aspose.PSD for Java 函式庫。您可於 **[here](https://releases.aspose.com/psd/java/)** 下載。  
- 基本的 Java 語法與物件導向概念。

## 匯入套件

匯入語句會將 Aspose.PSD 類別引入作用域，讓您能操作點陣圖、濾鏡選項與輸出格式。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

這些匯入讓您可以存取影像載入、點陣圖操作、濾鏡選項與輸出格式。

## 步驟 1：載入影像

`RasterImage` 類別代表可逐像素處理的點陣圖影像。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

我們從指定目錄載入 PSD 檔案，並將其轉型為 `RasterImage`，以便操作像素資料。

## 步驟 2：檢查 RasterImage

安全檢查會確認載入的檔案為點陣圖；若不是，程式會優雅地退出。

```java
if (rasterImage == null) {
    return;
}
```

## 步驟 3：設定濾鏡選項

`GaussWienerFilterOptions` 類別允許您在同一物件中微調 Gaussian 與 Wiener 參數。

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- 第一個參數（`12`）定義 Gaussian 核心的半徑大小。  
- 第二個參數（`3`）設定 Wiener 演算法使用的平滑值。  
- `setGrayscale(true)` 讓濾鏡以灰階模式運作，通常能在降噪時得到更乾淨的結果。

## 步驟 4：套用濾鏡並儲存

`filter` 方法會將設定好的 Gaussian‑Wiener 組合套用至整個影像範圍。最後，我們使用 `GifOptions` 將處理後的影像儲存為 GIF。您可以將 `GifOptions` 替換為 `PngOptions`、`JpegOptions` 等，以 **export PNG Java** 或其他格式。

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## 常見問題與技巧

- **Null RasterImage:** 請確認來源檔案為 PSD 或其他相容的點陣圖格式。  
- **Performance:** 大尺寸影像可能較慢；可考慮減小半徑或先處理縮小版的影像。  
- **Color vs. Grayscale:** 若需保留顏色，請設定 `options.setGrayscale(false)`。

## 常見問答

**Q1: Can I apply these filters to images in formats other than PSD?**  
A1: 是的，Aspose.PSD for Java 支援多種影像格式，除 PSD 外亦包括 PNG、JPEG、BMP 與 GIF。

**Q2: Are there any restrictions in the trial version of Aspose.PSD for Java?**  
A2: 試用版會限制輸出尺寸並加上浮水印。欲解鎖全部功能，請取得有效授權。

**Q3: How can I get support for Aspose.PSD for Java?**  
A3: 前往 **[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)** 取得社群協助與官方回覆。

**Q4: Is there a temporary license available for testing purposes?**  
A4: 可以，您可於 **[here](https://purchase.aspose.com/temporary-license/)** 取得臨時授權。

**Q5: Where can I find detailed documentation for Aspose.PSD for Java?**  
A5: 請參考 **[documentation](https://reference.aspose.com/psd/java/)** 取得深入的 API 參考與更多範例。

## 結論

您已完成完整的 **java image processing tutorial**，示範如何使用 Aspose.PSD for Java **apply Gaussian** 與 Wiener 濾鏡。可嘗試不同的半徑與平滑值、切換灰階模式，並嘗試 PNG 等其他輸出格式，觀察濾鏡對影像的影響。祝開發愉快！

---

**最後更新：** 2026-07-17  
**測試環境：** Aspose.PSD for Java 23.12 (latest at time of writing)  
**作者：** Aspose

## 相關教學

- [逐步濾鏡 - 使用 Aspose.PSD for Java 套用 Motion Wiener 濾鏡](/psd/java/image-processing/apply-motion-wiener-filters/)
- [逐步濾鏡 - 套用 Median 與 Wiener 濾鏡 (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [如何在 Aspose.PSD for Java 中濾鏡 PNG 檔案](/psd/java/optimizing-png-files/apply-filters-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}