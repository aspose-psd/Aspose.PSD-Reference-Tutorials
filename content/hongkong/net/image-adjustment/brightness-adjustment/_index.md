---
title: 在 Aspose.PSD for .NET 中實現亮度調整
linktitle: 實施亮度調整
second_title: Aspose.PSD .NET API
description: 探索 Aspose.PSD for .NET 在調整影像亮度方面的強大功能。請遵循我們的逐步指南以實現無縫實施。
type: docs
weight: 10
url: /zh-hant/net/image-adjustment/brightness-adjustment/
---
## 介紹

增強和調整影像屬性是各種應用程式中的常見要求，Aspose.PSD for .NET 提供了無縫操作 PSD 檔案的強大解決方案。其中一種操作是亮度調整，可讓您輕鬆修改影像的亮度。

在本教學中，我們將逐步介紹使用 Aspose.PSD for .NET 實現亮度調整的過程。請依照以下步驟操作，全面了解如何將亮度調整合併到 PSD 檔案中。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET 函式庫：從下列位置下載並安裝 Aspose.PSD for .NET 函式庫：[下載連結](https://releases.aspose.com/psd/net/).

- 文件目錄：設定一個目錄來儲存您的 PSD 檔案並更新`dataDir`提供的程式碼片段中的變數以及文檔目錄的路徑。

## 導入命名空間

在您的 .NET 專案中，包含存取 Aspose.PSD 功能所需的命名空間。將以下命名空間加入您的程式碼：

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

現在，讓我們將範例分解為多個步驟：

## 第 1 步：載入 PSD 文件

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

//使用Aspose.PSD載入PSD文件
using (var image = (PsdImage)Image.Load(sourceFile))
{
    //您的進一步步驟的程式碼位於此處
}
```

## 步驟2：取得光柵影像

```csharp
//從載入的 PSD 檔案中取得光柵影像
RasterCachedImage rasterImage = image;
```

## 第三步：調整亮度

```csharp
//設定亮度值。可接受的亮度值在[-255, 255]範圍內。
rasterImage.AdjustBrightness(-50);
```

## 第四步：儲存修改後的影像

```csharp
//儲存修改後的影像並調整亮度
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

現在我們已將範例分解為可管理的步驟，您可以使用 Aspose.PSD 將亮度調整無縫整合到您的 .NET 專案中。

## 結論

Aspose.PSD for .NET 簡化了在 PSD 檔案中實現亮度調整的過程。透過遵循上面提供的逐步指南，您可以輕鬆增強影像的視覺吸引力。嘗試不同的亮度值以獲得所需的結果。

## 常見問題解答

### Q1：在哪裡可以找到 Aspose.PSD for .NET 的文件？

 A1：文檔可用。[這裡](https://reference.aspose.com/psd/net/).

### Q2: 如何下載 Aspose.PSD for .NET 函式庫？

 A2：您可以從以下位置下載該庫：[發布頁面](https://releases.aspose.com/psd/net/).

### Q3：Aspose.PSD for .NET 有沒有免費試用版？

 A3：是的，您可以免費試用。[這裡](https://releases.aspose.com/).

### 問題 4：在哪裡可以獲得 Aspose.PSD for .NET 支援？

 A4：如需支持，請訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34).

### Q5：如何取得 Aspose.PSD for .NET 的臨時授權？

 A5：您可以獲得臨時許可證。[這裡](https://purchase.aspose.com/temporary-license/).