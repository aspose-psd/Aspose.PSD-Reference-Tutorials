---
title: 在 Aspose.PSD for .NET 中新增漸層效果
linktitle: 為影像添加漸層效果
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 透過迷人的漸變效果增強影像。請按照我們的逐步教學進行創意視覺轉換。
type: docs
weight: 11
url: /zh-hant/net/image-manipulation/adding-gradient-effects/
---
## 介紹

使用漸變效果增強影像可以為您的視覺內容添加迷人的維度。 Aspose.PSD for .NET 提供了一個強大的平台，可以將漸層疊加合併到影像中。在本教學中，我們將引導您完成使用 Aspose.PSD for .NET 新增漸層效果的過程。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET Library：從以下位置下載並安裝該程式庫[Aspose.PSD for .NET 文檔](https://reference.aspose.com/psd/net/).
- .NET 環境：確保您的電腦上設定了有效的 .NET 環境。

## 導入命名空間

首先將必要的命名空間匯入到您的專案中：

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## 第 1 步：載入圖像並定義路徑

```csharp
//文檔目錄的路徑。
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFileName = Path.Combine(SourceDir, "GradientOverlay.psd");
string exportPath = Path.Combine(OutputDir, "GradientOverlayChanged.psd");

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};
```

## 第 2 步：斷言初始設置

確保漸層疊加的初始設定符合預期：

```csharp
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    //斷言檢查初始設置
    //……

    //色點
    //……

    //透明點
    //……
}
```

## 步驟 3：修改漸層疊加設置

依照您的喜好調整漸層疊加設定：

```csharp
//測試編輯
settings.Color = Color.Green;

gradientOverlay.Opacity = 193;
gradientOverlay.BlendMode = BlendMode.Lighten;

settings.AlignWithLayer = false;
settings.GradientType = GradientType.Radial;
settings.Angle = 45;
settings.Dither = true;
settings.HorizontalOffset = 15;
settings.VerticalOffset = 11;
settings.Reverse = true;

//新增色點
//……

//更改前一點的位置
//……

//增加新的透明點
//……

//更改先前透明點的位置
//……

im.Save(exportPath);
```

## 第 4 步：驗證編輯的文件

檢查修改是否成功應用：

```csharp
//編輯後測試文件
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];
    try
    {
        //斷言檢查修改的設定
        //……
    }
    catch (Exception e)
    {
        string ex = e.StackTrace;
    }
}
```

## 結論

使用 Aspose.PSD for .NET 為影像添加漸變效果開啟了創意可能性的世界。嘗試各種設定以獲得圖像所需的視覺效果。

## 常見問題解答

### Q1：我可以同時對多個圖層套用漸層效果嗎？

A1：是的，您可以透過迭代每個圖層並套用所需的設定來將漸層效果套用到多個圖層。

### Q2：Aspose.PSD for .NET 支援哪些檔案格式？

A2：Aspose.PSD for .NET支援各種圖片檔案格式，包括PSD、PNG、JPEG、BMP和GIF。

### Q3：Aspose.PSD for .NET 有試用版嗎？

A3：是的，您可以透過下載免費試用版來探索 Aspose.PSD for .NET 的功能[這裡](https://releases.aspose.com/).

### 問題 4：如何獲得 Aspose.PSD for .NET 支援？

 A4：如需任何協助或疑問，請訪問[Aspose.PSD for .NET 支援論壇](https://forum.aspose.com/c/psd/34).

### Q5：哪裡可以購買 Aspose.PSD for .NET？

A5：您可以從以下網站購買該庫：[Aspose.PSD for .NET 購買頁面](https://purchase.aspose.com/buy).