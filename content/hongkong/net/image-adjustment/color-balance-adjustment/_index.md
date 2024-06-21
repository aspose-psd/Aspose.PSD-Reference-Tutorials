---
title: 在 Aspose.PSD for .NET 中套用色彩平衡調整
linktitle: 應用色彩平衡調整
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 的色彩平衡調整功能輕鬆增強 PSD 影像色彩。按照我們的逐步指南獲得令人驚嘆的結果。
type: docs
weight: 14
url: /zh-hant/net/image-adjustment/color-balance-adjustment/
---
## 介紹

歡迎閱讀這份關於在 Aspose.PSD for .NET 中應用色彩平衡調整的綜合指南！ Aspose.PSD 是一個功能強大的 .NET 程式庫，可讓開發人員有效率地處理 PSD 檔案。在本教學中，我們將重點介紹色彩平衡調整功能，讓您輕鬆增強 PSD 影像的色彩平衡。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET Library：從以下位置下載並安裝該程式庫：[Aspose.PSD 網站](https://releases.aspose.com/psd/net/).
- 開發環境：確保您的電腦上設定了有效的 .NET 開發環境。
- PSD 檔案：準備好要套用色彩平衡調整的 PSD 檔案。

## 導入命名空間

在您的 .NET 專案中，包含使用 Aspose.PSD 功能所需的命名空間。將以下行加入您的程式碼：

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

現在，讓我們將色彩平衡調整流程分解為多個步驟：

## 第 1 步：載入 PSD 文件

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    //色彩平衡調整的程式碼將在以下步驟中新增。
}
```

## 第 2 步：訪問並調整色彩平衡

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## 第三步：儲存調整後的影像

```csharp
im.Save(outputPath);
```

現在，您已經使用 Aspose.PSD for .NET 成功將色彩平衡調整套用到您的 PSD 檔案！

## 結論

恭喜！您已經了解如何使用 Aspose.PSD for .NET 來增強 PSD 影像的色彩平衡。嘗試不同的平衡值以達到所需的視覺效果。

## 常見問題解答

### Q1：我可以對多個圖層套用色彩平衡調整嗎？

A1：是的，您可以迭代 PSD 檔案中的所有圖層並根據需要調整色彩平衡。

### Q2：Aspose.PSD for .NET適合批次處理PSD檔案嗎？

A2：當然！ Aspose.PSD為PSD檔案提供高效率的批次功能。

### Q3：如何取得 Aspose.PSD for .NET 的臨時授權？

 A3：參觀[Aspose.PSD臨時許可證](https://purchase.aspose.com/temporary-license/)以獲得臨時許可證。

### Q4：在哪裡可以找到更多範例和文件？

 A4：探索[Aspose.PSD 文檔](https://reference.aspose.com/psd/net/)取得詳細範例和指南。

### 問題 5：Aspose.PSD for .NET 有哪些支援選項？

 A5：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和討論。
