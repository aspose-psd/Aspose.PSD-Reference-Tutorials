---
title: 在 Aspose.PSD for .NET 中調整陰影效果不透明度
linktitle: 調整陰影效果不透明度
second_title: Aspose.PSD .NET API
description: 透過這個綜合教程，了解如何在 Aspose.PSD for .NET 中調整陰影效果不透明度。
weight: 15
url: /zh-hant/net/layer-effects/adjusting-shadow-effect-opacity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for .NET 中調整陰影效果不透明度

## 介紹

歡迎來到我們在 Aspose.PSD for .NET 中調整陰影效果不透明度的逐步指南！在本教學中，我們將引導您完成使用 DropShadowEffect 的 Opacity 屬性的過程。 Aspose.PSD for .NET 是一個功能強大的程式庫，可讓您在 .NET 應用程式中無縫地使用 PSD 檔案。

## 先決條件

在我們深入學習本教學之前，請確保您具備以下條件：

-  Aspose.PSD for .NET 函式庫：確保您的專案中安裝了 Aspose.PSD for .NET 函式庫。你可以下載它[這裡](https://releases.aspose.com/psd/net/).

- 文檔目錄：為輸入 PSD 檔案設定目錄。

- 輸出目錄：建立一個用於保存生成影像的目錄。

## 導入命名空間

在您的 .NET 專案中，確保導入必要的命名空間：

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

## 第 1 步：載入 PSD 文件

首先使用以下命令載入 PSD 文件`Image.Load`方法：

```csharp
string inputFile = Path.Combine(baseDir, "input.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    //您用於進一步處理的程式碼位於此處
}
```

## 步驟2：存取圖層並新增陰影效果

從 PSD 檔案中檢索所需的圖層並新增投影效果：

```csharp
Layer workLayer = psdImage.Layers[1];
DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
dropShadowEffect.Distance = 0;
dropShadowEffect.Size = 8;
```

## 第 3 步：調整不透明度並儲存影像

現在，調整不透明度屬性並儲存具有不同不透明度的影像：

```csharp
//不透明度 = 20 的範例
dropShadowEffect.Opacity = 20;
psdImage.Save(outputImage20, new PngOptions());

//不透明度 = 200 的範例
dropShadowEffect.Opacity = 200;
psdImage.Save(outputImage200, new PngOptions());
```

## 第四步：清理

儲存影像後，透過刪除臨時檔案進行清理：

```csharp
File.Delete(outputImage20);
File.Delete(outputImage200);
```

## 結論

恭喜！您已成功調整 Aspose.PSD for .NET 中的陰影效果不透明度。本教學提供了使用不同陰影不透明度增強 PSD 影像的簡單指南。

## 常見問題解答

### Q1：我可以將本教學套用到其他圖像格式嗎？

A1：不，本教學專門介紹使用 Aspose.PSD for .NET 調整 PSD 檔案中的陰影效果不透明度。

### Q2：是否有其他可以修改的陰影屬性？

A2：是的，Aspose.PSD for .NET 提供了各種微調陰影效果的特性。

### Q3：如何取得 Aspose.PSD for .NET 的臨時授權？

 A3：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q4：Aspose.PSD for .NET 與 .NET Core 相容嗎？

A4：是的，Aspose.PSD for .NET 與 .NET Framework 和 .NET Core 相容。

### 問題 5：在哪裡可以找到 Aspose.PSD for .NET 的社群支援？

 A5：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和討論。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
