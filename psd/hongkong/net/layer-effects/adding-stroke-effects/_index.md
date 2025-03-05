---
title: 在 Aspose.PSD for .NET 中新增描邊效果
linktitle: 在圖層中加入描邊效果
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 增強影像美感。學習逐步加入描邊效果。立即下載、購買或嘗試免費試用。
type: docs
weight: 10
url: /zh-hant/net/layer-effects/adding-stroke-effects/
---
## 介紹

歡迎來到 Aspose.PSD for .NET 中向圖層新增描邊效果的逐步教學。使用描邊效果可以輕鬆增強影像的視覺吸引力，而 Aspose.PSD 使 .NET 開發人員能夠無縫實現這一點。在本指南中，我們將引導您完成整個過程，提供清晰的步驟和範例來幫助您掌握這項強大的功能。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

- Aspose.PSD for .NET：從下列位置下載並安裝 Aspose.PSD 函式庫：[網站](https://releases.aspose.com/psd/net/).

- 文件目錄：準備一個包含要套用描邊效果的 PSD 文件的目錄。

- 輸出目錄：有一個單獨的目錄用於儲存帶有描邊效果的輸出影像。

- Visual Studio：確保您已設定 Visual Studio 或任何其他首選的 .NET 開發環境。

## 導入命名空間

在您的 .NET 專案中，包含必要的命名空間以利用 Aspose.PSD 功能：

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## 第 1 步：載入 PSD 文檔

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    //您用於載入 PSD 文件的程式碼位於此處
}
```

## 步驟2：新增顏色描邊效果

```csharp
//在“內部”位置添加顏色填充
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## 第三步：外側位置

```csharp
//在外部位置添加顏色填充
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## 第四步：中心位置

```csharp
//在中心位置新增顏色填充
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

對漸層和圖案填滿重複類似的步驟，相應地調整設定。

## 結論

恭喜！您已經成功學習如何使用 Aspose.PSD for .NET 為圖層新增描邊效果。嘗試不同的設置，以獲得圖像所需的視覺效果。

## 常見問題解答

### Q1：我可以只對特定圖層套用描邊效果嗎？

A1：是的，您可以透過調整程式碼中的圖層索引來定位特定圖層。

### Q2：Aspose.PSD 與最新的.NET 框架相容嗎？

A2：當然！ Aspose.PSD 旨在與最新的 .NET 框架無縫整合。

### Q3：如何自訂描邊顏色？

 A3：只需修改`Color`程式碼中的屬性以實現所需的描邊顏色。

### Q4：Aspose.PSD支援批次處理多個PSD檔案嗎？

A4：是的，您可以循環瀏覽多個 PSD 檔案並使用類似的方法套用描邊效果。

### Q5: 在購買Aspose.PSD之前我可以使用試用版嗎？

 A5：當然！抓住[免費試用](https://releases.aspose.com/)在購買之前探索 Aspose.PSD 的功能。