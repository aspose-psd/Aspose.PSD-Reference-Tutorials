---
title: 在 Aspose.PSD for .NET 中加入有圖案的描邊圖層
linktitle: 添加帶有圖案的描邊圖層
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 透過描邊圖層和圖案增強 PSD 檔案。請按照我們的逐步指南進行無縫整合。
weight: 13
url: /zh-hant/net/layer-effects/adding-stroke-layer-pattern/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for .NET 中加入有圖案的描邊圖層

## 介紹

使用描邊圖層和圖案增強 PSD（Photoshop 文件）檔案可以為您的設計增添動態感。在本教學中，我們將探索如何利用 Aspose.PSD for .NET 輕鬆地在 PSD 檔案中新增帶有圖案的描邊圖層。 Aspose.PSD 是一個功能強大的 .NET 程式庫，可為操作 PSD 檔案提供全面支持，使其成為開發人員和設計人員的寶貴工具。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- C# 程式語言的基礎知識。
- Visual Studio 安裝在您的電腦上。
-  Aspose.PSD for .NET 函式庫，您可以下載[這裡](https://releases.aspose.com/psd/net/).

## 導入命名空間

確保在 C# 程式碼中導入必要的命名空間：

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## 第 1 步：設定您的環境

首先在 C# 程式碼中定義來源目錄和輸出目錄：

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## 第 2 步：載入 PSD 文件

使用 Aspose.PSD 的 PsdImage 類別載入 PSD 檔案：

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    //您處理 PSD 檔案的程式碼位於此處
}
```

## 第 3 步：準備新模式數據

定義一個新模式及其邊界：

```csharp
var newPattern = new int[]
{
    //您的圖案顏色放在這裡
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## 第四步：修改描邊圖層

存取描邊圖層並更新其屬性：

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

//檢查並更新筆劃屬性
//……

//更新不透明度和混合模式
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## 第5步：更新模式訊息

更新PSD檔案中的圖案資訊：

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        //您用於更新模式資訊的程式碼位於此處
    }
}

//儲存修改後的PSD文件
im.Save(exportPath);
```

## 第 6 步：驗證更改

載入修改後的 PSD 檔案並驗證變更：

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    //用於驗證更改的程式碼位於此處
}
```

## 結論

恭喜！您已成功學習如何在 Aspose.PSD for .NET 中新增帶有圖案的描邊圖層。這個多功能庫使開發人員能夠創建具有視覺吸引力的設計並增強 PSD 檔案的靈活性。

## 常見問題解答

### Q1：我可以在任何版本的 Visual Studio 中使用 Aspose.PSD for .NET 嗎？

A1：是的，Aspose.PSD for .NET 與各種版本的 Visual Studio 相容。

### Q2：如何取得Aspose.PSD的臨時授權？

 A2：參觀[這裡](https://purchase.aspose.com/temporary-license/)獲得臨時許可證。

### Q3：是否有可供測試的範例 PSD 檔案？

 A3：您可以在文件中找到範例 PSD 文件[這裡](https://reference.aspose.com/psd/net/).

### Q4：Aspose.PSD適合批次處理PSD檔案嗎？

A4：當然，Aspose.PSD for .NET 為批次提供了強大的支援。

### Q5：我可以在哪裡尋求協助或參與社區討論？

 A5：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)用於支持和社區互動。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
