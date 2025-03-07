---
title: 使用 Aspose.PSD for Java 調整影像的亮度
linktitle: 調整影像的亮度
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 在 Java 中增強影像亮度。以程式方式調整影像亮度的逐步指南。
weight: 21
url: /zh-hant/java/advanced-techniques/adjust-brightness/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 調整影像的亮度

## 介紹

增強影像是平面設計和數位攝影中的常見要求。 Aspose.PSD for Java 提供了一個強大的解決方案，可以程式方式調整影像亮度。在本教程中，我們將逐步探索如何利用 Aspose.PSD for Java 函式庫來調整影像的亮度。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for Java Library：從以下位置下載並安裝該程式庫：[Aspose.PSD for Java 文檔](https://reference.aspose.com/psd/java/).

## 導入包

首先，將必要的套件匯入到您的 Java 專案中。在此範例中，我們將使用以下內容：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

現在，讓我們將調整影像亮度的過程分解為簡單的步驟：

## 第 1 步：載入圖像

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

//將現有映像載入到 RasterImage 類別的實例中
Image image = Image.load(sourceFile);
//將 Image 物件轉換為 RasterImage
RasterImage rasterImage = (RasterImage) image;

//檢查 RasterImage 是否已快取並快取 RasterImage 以獲得更好的效能
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

在此步驟中，我們載入目標圖像並將其投射到`RasterImage`以便進一步加工。

## 第 2 步：調整亮度

```java
//調整亮度
rasterImage.adjustBrightness(-50);
```

在這裡，我們使用`adjustBrightness`修改影像亮度的方法。在此範例中，我們將亮度降低 50 個單位，但您可以根據您的要求自訂該值。

## 第 3 步：設定 TiffOptions

```java
int[] ushort = {8, 8, 8};
//為產生的映像建立 TiffOptions 實例
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

配置`TiffOptions`用於儲存調整後的影像。調整`bitsPerSample`和`photometric`根據您的具體需求的屬性。

## 第 4 步：儲存結果影像

```java
//儲存結果影像
rasterImage.save(destName, tiffOptions);
```

最後使用指定的保存修改後的圖像`TiffOptions`.

## 結論

使用 Aspose.PSD for Java 以程式方式調整影像的亮度變得很容易。本教程提供了有關在 Java 應用程式中實現此功能的全面指南。

## 常見問題解答

### Q1：除了PSD之外，我可以調整其他影像格式的亮度嗎？

A1：是的，Aspose.PSD for Java 支援各種影像格式，如 JPEG、PNG 和 TIFF。

### Q2：影像調整過程中出現錯誤如何處理？

A2：您可以使用 try-catch 區塊來實現錯誤處理，以管理可能發生的異常。

### Q3：亮度調整範圍有限制嗎？

A3：調整的範圍取決於圖像內容和格式，但Aspose.PSD提供了客製化的靈活性。

### Q4：我可以在商業專案中使用Aspose.PSD for Java嗎？

 A4：是的，Aspose.PSD for Java是一個商業庫，您可以從以下地址取得許可證[這裡](https://purchase.aspose.com/buy).

### Q5：Aspose.PSD for Java 有免費試用版嗎？

A5：是的，您可以透過免費試用來探索該庫[這裡](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
