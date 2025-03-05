---
title: 使用 Aspose.PSD for Java 調整影像的 Gamma
linktitle: 調整影像的伽瑪值
second_title: Aspose.PSD Java API
description: 學習使用 Aspose.PSD for Java 輕鬆調整圖像伽瑪。請遵循我們的逐步指南以獲得最佳結果。
type: docs
weight: 23
url: /zh-hant/java/advanced-techniques/adjust-gamma/
---
## 介紹

在影像處理領域，調整影像的伽瑪是增強其視覺吸引力的關鍵步驟。 Aspose.PSD for Java 為 Java 開發人員提供了一個強大的解決方案，可以輕鬆操縱映像伽瑪。在本教程中，我們將探索如何使用 Aspose.PSD 調整伽瑪，分解每個步驟以確保無縫實施。

## 先決條件

在深入學習本教學之前，請確保您已設定以下先決條件：

1. Java 開發環境：確保您的系統上安裝了 Java 開發環境。
2.  Aspose.PSD 庫：下載 Aspose.PSD 庫並將其整合到您的 Java 專案中。您可以在以下位置找到必要的資源[文件](https://reference.aspose.com/psd/java/).
3. 範例影像：準備用於應用伽馬調整的範例 PSD 影像。

## 導入包

若要開始流程，請在 Java 專案中匯入所需的套件。這為無縫利用 Aspose.PSD 功能奠定了基礎。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 第 1 步：載入圖像

首先將範例 PSD 映像載入到`RasterImage`班級。這是後續gamma調整的基礎。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//將現有映像載入到 RasterImage 類別的實例中
Image image = Image.load(sourceFile);

//將 Image 物件轉換為 RasterImage
RasterImage rasterImage = (RasterImage)image;

//檢查 RasterImage 是否已緩存以獲得更好的效能
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## 第 2 步：調整伽瑪值

現在，使用以下命令調整載入圖片的伽瑪值：`adjustGamma`方法。根據您的要求微調伽瑪值。

```java
//調整伽瑪值
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 第 3 步：建立 TiffOptions

建立一個實例`TiffOptions`對於結果圖像。設定各種屬性，例如每個樣本的位數和光度選項，以根據您的規格自訂輸出。

```java
//為產生的映像建立 TiffOptions 實例
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 第 4 步：儲存結果影像

使用先前定義的將處理後的影像儲存為 TIFF 格式`TiffOptions`.

```java
//將產生的影像儲存為 TIFF 格式
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 結論

恭喜！您已使用 Aspose.PSD for Java 成功調整了影像的伽瑪值。此過程使開發人員能夠輕鬆提高影像質量，從而打造具有視覺吸引力的用戶體驗。

## 常見問題解答

### Q1：哪裡可以找到Aspose.PSD文件？

 A1：您可以存取文件：[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: 如何下載 Aspose.PSD for Java？

 A2：從以下位置下載庫[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3：哪裡可以購買Aspose.PSD？

 A3：參觀[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy)購買Aspose.PSD。

### Q4：有免費試用嗎？

 A4：是的，您可以在以下位置探索免費試用：[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5：我可以在哪裡尋求Aspose.PSD的支援？

 A5：如需支持，請造訪 Aspose.PSD 論壇：[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).