---
title: 在 Aspose.PSD for .NET 中支援外發光效果
linktitle: 支持外發光效果
second_title: Aspose.PSD .NET API
description: 探索 Aspose.PSD for .NET 中外發光效果的強大功能。透過此逐步教學提升您的圖像設計。
type: docs
weight: 16
url: /zh-hant/net/image-manipulation/supporting-outer-glow-effect/
---
## 介紹

歡迎來到我們關於在 Aspose.PSD for .NET 中支援外發光效果的逐步指南。 Aspose.PSD 是一個功能強大的函式庫，可以在 .NET 應用程式中無縫操作 PSD 檔案。在本教程中，我們將探索外發光效果的實現，並提供將其整合到專案中的詳細演練。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET 函式庫：從下列位置下載函式庫：[Aspose.PSD .NET 文檔](https://reference.aspose.com/psd/net/).

- 開發環境：設定您首選的 .NET 開發環境。

- 文件和輸出目錄：在提供的程式碼中定義文件和輸出目錄。

## 導入命名空間

在本節中，我們將導入必要的命名空間來啟動我們的外發光效果實作。請依照下列步驟操作：

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

現在，讓我們將提供的範例分解為多個步驟來實現外發光效果。

## 步驟1：設定文檔和輸出路徑

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## 第 2 步：載入 PSD 映像

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    //下面將新增實施步驟。
}
```

## 第三步：增加外發光效果

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## 步驟 4：配置外發光參數

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## 第 5 步：儲存影像

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## 第 6 步：清理

```csharp
File.Delete(outputPng);
```

## 步驟7：顯示成功訊息

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## 結論

恭喜！您已使用 Aspose.PSD for .NET 成功實現了外發光效果。這項強大的功能增強了影像的視覺吸引力，為您的設計提供了獨特的觸感。

## 常見問題解答

### Q1：Aspose.PSD 與所有.NET 框架相容嗎？

A1：是的，Aspose.PSD支援廣泛的.NET框架，確保與各種開發環境的兼容性。

### Q2：在哪裡可以找到 Aspose.PSD 的附加文件？

 A2：請參閱[Aspose.PSD .NET 文檔](https://reference.aspose.com/psd/net/)獲取全面的資訊和範例。

### Q3：如何取得Aspose.PSD的臨時授權？

 A3：參觀[Aspose.PSD臨時許可證](https://purchase.aspose.com/temporary-license/)用於臨時許可選項。

### Q4：Aspose.PSD 用戶可以獲得哪些支援？

 A4：加入[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和討論。

### Q5：我可以購買 Aspose.PSD for .NET 嗎？

 A5：是的，探索授權選項並進行購買[這裡](https://purchase.aspose.com/buy).