---
title: 在 Aspose.PSD for .NET 中實現伽瑪調整
linktitle: 實施伽瑪調整
second_title: Aspose.PSD .NET API
description: 透過我們關於實作伽瑪調整的逐步指南來探索 Aspose.PSD for .NET 的強大功能。輕鬆微調影像亮度和對比度。
type: docs
weight: 12
url: /zh-hant/net/image-adjustment/gamma-adjustment/
---
## 介紹

歡迎閱讀這份關於在 Aspose.PSD for .NET 中實現 Gamma 調整的綜合指南！伽瑪調整是一項重要的影像處理技術，可讓您微調影像的亮度和對比。在本教程中，我們將引導您使用強大的 .NET Aspose.PSD 庫完成整個過程。

## 先決條件

在深入實施之前，請確保滿足以下先決條件：

-  Aspose.PSD for .NET 函式庫：確保您已安裝 Aspose.PSD for .NET 函式庫。你可以下載它[這裡](https://releases.aspose.com/psd/net/).

- .NET Framework：本教學假設您對 .NET 開發有基本的了解並且已安裝 .NET Framework。

- 整合開發環境 (IDE)：選擇用於 .NET 開發的首選 IDE，例如 Visual Studio。

## 導入命名空間

在您的 .NET 專案中，首先匯入使用 Aspose.PSD 所需的命名空間：

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 第 1 步：設定您的項目

在您選擇的 IDE 中建立一個新的 .NET 專案。確保新增對 Aspose.PSD 庫的引用。

## 第 2 步：定義文檔目錄

```csharp
string dataDir = "Your Document Directory";
```

## 第 3 步：載入圖像

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    //附加步驟將在此 using 區塊內執行。
}
```

## 第 4 步：轉換為 RasterImage 並快取數據

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## 第5步：調整伽瑪值

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## 第 6 步：建立 TiffOptions 並儲存

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## 結論

恭喜！您已使用 Aspose.PSD for .NET 成功實現了伽瑪調整。這個強大的程式庫提供了強大的影像處理功能，使其成為 .NET 開發人員的寶貴工具。

## 常見問題解答

### Q1：哪裡可以找到Aspose.PSD文件？

 A1：可以參考文檔[這裡](https://reference.aspose.com/psd/net/).

### Q2：如何下載 Aspose.PSD for .NET？

 A2：您可以下載該程式庫[這裡](https://releases.aspose.com/psd/net/).

### Q3：有免費試用嗎？

 A3：是的，您可以獲得免費試用[這裡](https://releases.aspose.com/).

### Q4：我可以在哪裡獲得 Aspose.PSD 的支援？

 A4：您可以造訪支援論壇[這裡](https://forum.aspose.com/c/psd/34).

### Q5: 我需要臨時許可證嗎？

 A5：如果需要，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).