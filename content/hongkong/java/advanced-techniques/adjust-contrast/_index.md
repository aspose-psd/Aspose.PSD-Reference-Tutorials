---
title: 使用 Aspose.PSD for Java 調整影像的對比度
linktitle: 調整影像的對比度
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 探索 Java 中影像對比度調整的世界。請按照我們的逐步指南進行無縫影像處理。
type: docs
weight: 22
url: /zh-hant/java/advanced-techniques/adjust-contrast/
---
## 介紹

在使用 Java 進行影像處理的領域中，Aspose.PSD 是一款脫穎而出的強大工具。在其眾多功能中，調整影像對比度是常見的要求。本教學將引導您完成使用 Aspose.PSD for Java 調整影像對比度的過程。無論您是經驗豐富的開發人員還是新手，本指南都將幫助您掌握影像處理的這一重要方面。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- 對 Java 程式設計有基本的了解。
- 安裝了 Java 函式庫的 Aspose.PSD。你可以下載它[這裡](https://releases.aspose.com/psd/java/).

## 導入包

首先，您需要將必要的套件匯入到您的 Java 專案中。將以下行加入您的程式碼：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 第 1 步：載入圖像

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//將現有映像載入到 RasterImage 類別的實例中
Image image = Image.load(sourceFile);
```

在此步驟中，我們使用以下命令載入範例映像（“sample.psd”）`Image.load`方法。

## 第 2 步：轉換為 RasterImage 並快取數據

```java
//將 Image 物件轉換為 RasterImage
RasterImage rasterImage = (RasterImage)image;

//檢查 RasterImage 是否已快取並快取 RasterImage 以獲得更好的效能
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

在這裡，我們投射泛型`Image`反對`RasterImage`進行具體處理。快取圖像資料可以提高效能。

## 第 3 步：調整對比度

```java
//調整對比度
rasterImage.adjustContrast(50);
```

這`adjustContrast`方法用於修改影像的對比度。在此範例中，對比度增加了 50%。

## 第 4 步：建立 TiffOptions 並儲存

```java
//為產生的映像建立 TiffOptions 實例
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

//將產生的影像儲存為 TIFF 格式
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

在這裡，我們設定了`TiffOptions`對於輸出影像，指定格式和其他屬性。最終影像將儲存為 TIFF 檔案。

## 結論

恭喜！您已經使用 Aspose.PSD for Java 成功調整了影像的對比度。本教程涵蓋了從導入包到保存處理後的圖像的基本步驟。

## 常見問題解答

### Q1：Aspose.PSD 是否相容於不同的影像格式？

A1：是的，Aspose.PSD 支援各種圖像格式，為您的專案提供靈活性。

### Q2：如何取得Aspose.PSD的臨時授權？

 A2：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q3：哪裡可以找到Aspose.PSD文件？

A3：文檔可用[這裡](https://reference.aspose.com/psd/java/).

### 問題 4：Aspose.PSD 有哪些支援選項？

 A4：如需支持，請訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34).

### Q5: 我可以購買Aspose.PSD嗎？

 A5：是的，你可以購買Aspose.PSD[這裡](https://purchase.aspose.com/buy).