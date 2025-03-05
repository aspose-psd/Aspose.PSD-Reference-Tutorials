---
title: 在 Aspose.PSD for .NET 中擴充和裁切影像
linktitle: 擴大和裁剪圖像
second_title: Aspose.PSD .NET API
description: 了解如何使用 Aspose.PSD for .NET 動態擴充和裁切影像。請按照我們的逐步指南進行無縫影像處理。
type: docs
weight: 13
url: /zh-hant/net/image-manipulation/expand-crop-images/
---
## 介紹

Aspose.PSD for .NET 是一個綜合圖像庫，允許開發人員在其 .NET 應用程式中使用各種圖像格式。其突出的功能之一是能夠輕鬆操縱影像。在本教程中，我們將重點放在擴展和裁剪圖像，為您提供使用 Aspose.PSD 完成這些任務的實踐指南。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET 函式庫：確保您已安裝 Aspose.PSD for .NET 函式庫。您可以從[Aspose.PSD for .NET 文檔](https://reference.aspose.com/psd/net/).

- 範例圖像：準備本教學將使用的範例圖像檔案（例如“example1.psd”）。

現在，讓我們開始使用逐步指南。

## 導入命名空間

首先匯入必要的命名空間以利用 Aspose.PSD for .NET 提供的功能。將以下命名空間加入您的程式碼：

```csharp
using Aspose.PSD.ImageOptions;
```

## 第 1 步：設定項目

確保您有一個整合了 Aspose.PSD for .NET 的專案。如果沒有，請按照[文件](https://reference.aspose.com/psd/net/)以獲得指導。

## 第 2 步：載入圖像

使用以下程式碼載入範例圖像：

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

//載入圖片
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    //圖像處理的附加程式碼將在此處
}
```

## 第三步：快取圖像數據

快取圖像資料以優化效能：

```csharp
rasterImage.CacheData();
```

## 第 4 步：定義目標矩形

建立 Rectangle 類別的實例並定義矩形的 X、Y、寬度和高度。這將是圖像將被擴展或裁剪的區域。

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## 第5步：儲存輸出影像

使用指定的選項和目標矩形儲存輸出影像：

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## 結論

恭喜！您已成功學習如何使用 Aspose.PSD for .NET 擴充和裁切影像。這個強大的程式庫為您的 .NET 應用程式中的圖像操作開啟了無限可能。

## 常見問題解答

### Q1：Aspose.PSD可以處理PSD以外的其他影像格式嗎？

A1：是的，Aspose.PSD 支援多種圖片格式，包括 JPEG、PNG、GIF 等。

### Q2：在哪裡可以找到對 Aspose.PSD 的支援？

 A2：您可以在以下位置找到支持並與社區互動：[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34).

### Q3 Aspose.PSD for .NET 有免費試用版嗎？

 A3：是的，您可以透過免費試用來探索這些功能，網址為[Aspose.PSD 免費試用](https://releases.aspose.com/).

### Q4：如何取得Aspose.PSD的臨時授權？

A4：您可以從以下地點獲得臨時許可證：[Aspose.PSD臨時許可證](https://purchase.aspose.com/temporary-license/).

### Q5：哪裡可以購買 Aspose.PSD for .NET？

 A5：您可以在以下位置購買圖書館：[Aspose.PSD 購買頁面](https://purchase.aspose.com/buy).