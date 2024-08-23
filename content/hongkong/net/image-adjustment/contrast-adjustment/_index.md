---
title: 在 Aspose.PSD for .NET 中實現對比調整
linktitle: 實施對比調整
second_title: Aspose.PSD .NET API
description: 透過此逐步指南了解如何在 Aspose.PSD for .NET 中實現對比度調整。
type: docs
weight: 11
url: /zh-hant/net/image-adjustment/contrast-adjustment/
---
## 介紹

歡迎閱讀這份關於在 Aspose.PSD for .NET 中實現對比調整的綜合指南！在本教程中，我們將探索使用 Aspose.PSD（強大的 .NET 影像庫）來增強影像對比度的過程。閱讀本指南後，您將對如何無縫地對影像應用對比度調整有深入的了解。

## 先決條件

在我們深入了解逐步流程之前，請確保您具備以下先決條件：

1.  Aspose.PSD for .NET 函式庫：下載並安裝 Aspose.PSD for .NET 函式庫。你可以找到下載鏈接[這裡](https://releases.aspose.com/psd/net/).

2. 文件目錄：設定儲存來源檔案和目標檔案的目錄。將提供的程式碼中的「您的文件目錄」替換為該目錄的路徑。

現在我們已經具備了先決條件，讓我們繼續實施。

## 導入命名空間

在此步驟中，我們將匯入必要的命名空間來存取 Aspose.PSD 庫提供的功能。

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 第 1 步：載入圖像

將來源圖像載入到實例中`RasterImage`班級。

```csharp
//ExStart：載入圖片
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    //繼續下一步...
}
//執行結束：載入映像
```

## 第 2 步：調整對比度

在此步驟中，我們將調整載入影像的對比度。

```csharp
//ExStart：調整對比度
rasterImage.AdjustContrast(50); //將對比度調整 50%
//繼續下一步...
//ExEnd：調整對比度
```

## 步驟 3：建立 TIFF 選項

建立一個實例`TiffOptions`對於產生的影像，設定各種屬性，並將影像儲存為 TIFF 格式。

```csharp
//ExStart:CreateTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

恭喜！您已使用 Aspose.PSD for .NET 成功實現了對比調整。

## 結論

在本教程中，我們探索了使用 Aspose.PSD for .NET 增強影像對比度的過程。該庫提供了一種操作圖像屬性的簡單方法，使開發人員能夠輕鬆創建具有視覺吸引力的圖像。

## 常見問題解答

### Q1：Aspose.PSD for .NET 適合初學者嗎？

A1：Aspose.PSD for .NET 被設計為對開發人員友好，使其適合初學者和經驗豐富的開發人員。

### Q2：我可以將Aspose.PSD用於商業項目嗎？

 A2：是的，Aspose.PSD for .NET可以用於商業專案。有關許可詳細信息，請訪問[這裡](https://purchase.aspose.com/buy).

### Q3：有免費試用嗎？

A3：是的，您可以探索 Aspose.PSD for .NET 的免費試用版[這裡](https://releases.aspose.com/).

### 問題 4：在哪裡可以找到 Aspose.PSD for .NET 支援？

 A4：造訪 Aspose.PSD for .NET 支援論壇[這裡](https://forum.aspose.com/c/psd/34)尋求幫助。

### Q5：如何取得臨時駕照？

A5：如果需要，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).