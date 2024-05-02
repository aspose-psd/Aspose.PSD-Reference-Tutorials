---
title: 在 Aspose.PSD for .NET 中透過移位裁剪影像
linktitle: 透過移位裁剪影像
second_title: Aspose.PSD .NET API
description: 學習使用 Aspose.PSD for .NET 輕鬆裁切影像。請按照我們的逐步指南進行精確的影像調整。
type: docs
weight: 12
url: /zh-hant/net/image-manipulation/crop-image-shifts/
---
## 介紹

在 .NET 開發領域，Aspose.PSD 作為影像處理任務的強大工具包脫穎而出。其顯著特點之一是能夠透過「按班次裁剪」功能精確裁剪影像。在本逐步指南中，我們將引導您完成使用 Aspose.PSD for .NET 無縫裁切影像的過程。

## 先決條件

在深入研究本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET Library：確保您已安裝該程式庫。如果沒有，您可以從以下位置下載[發布頁面](https://releases.aspose.com/psd/net/).

- .NET 環境：確保您的電腦上設定了 .NET 開發環境。

- 範例影像：準備您想要使用的 PSD 格式的範例影像。

## 導入命名空間

首先將必要的命名空間匯入到您的 .NET 專案中。這些命名空間提供對影像裁剪所需的 Aspose.PSD 類別和方法的存取。

```csharp
using Aspose.PSD.ImageOptions;
```

## 第 1 步：定義您的文件目錄

設定來源檔案和目標檔案所在文件目錄的路徑。

```csharp
string dataDir = "Your Document Directory";
```

## 步驟2：載入來源圖像

載入要裁剪的 PSD 映像。確保將“sample.psd”替換為原始檔案的名稱。

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## 步驟 3：快取影像資料以獲得更好的效能

在裁剪之前，建議快取圖像資料以提高效能。

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## 步驟 4：定義裁切的平移值

指定影像的左、右、上、下側的偏移值。根據您的裁切要求調整這些值。

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## 第 5 步：套用裁切並儲存結果

利用`Crop`方法套用指定的移位並將裁剪後的影像儲存到目標檔案。

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## 結論

恭喜！您已成功學習如何使用 Aspose.PSD for .NET 按班次裁切影像。這種強大的功能為您提供各種影像處理任務所需的精確度和控制。

## 常見問題解答

### Q1：我可以裁切不同格式的影像，而不僅僅是 PSD 嗎？

A1：是的，Aspose.PSD 支援各種圖片格式，讓您可以裁切 JPEG、PNG 等格式的圖片。

### Q2：購買 Aspose.PSD for .NET 之前有沒有試用版？

 A2：當然！您可以透過免費試用來探索該工具包[這裡](https://releases.aspose.com/).

### Q3：如何取得 Aspose.PSD for .NET 的臨時授權？

 A3：您可以獲得臨時許可證用於測試目的[這裡](https://purchase.aspose.com/temporary-license/).

### Q4：在哪裡可以找到與 Aspose.PSD 相關的其他支援和討論？

 A4：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得支持和參與討論。

### Q5：可以直接從網站購買Aspose.PSD for .NET嗎？

 A5：是的，您可以從[購買頁面](https://purchase.aspose.com/buy).
