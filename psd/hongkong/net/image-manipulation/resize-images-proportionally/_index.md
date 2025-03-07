---
title: 在 Aspose.PSD for .NET 中按比例調整影像大小
linktitle: 按比例調整影像大小
second_title: Aspose.PSD .NET API
description: 探索使用 Aspose.PSD for .NET 無縫調整圖片大小。下載該庫，按照我們的教程進行操作，並增強您的圖像處理能力。
weight: 14
url: /zh-hant/net/image-manipulation/resize-images-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for .NET 中按比例調整影像大小

在影像處理領域，Aspose.PSD for .NET 作為一個強大的工具包脫穎而出，為開發人員提供了輕鬆按比例調整影像大小的功能。在本逐步指南中，我們將引導您完成使用 Aspose.PSD for .NET 調整影像大小的過程，確保您的影像完美地保持其比例。

## 介紹

按比例調整圖像大小是許多應用程式中的常見任務，Aspose.PSD for .NET 為開發人員簡化了此過程。無論您是在開發 Web 應用程式、桌面軟體還是行動應用程序，了解如何在保持圖像寬高比的同時調整圖像大小對於保持視覺吸引力和一致性至關重要。

## 先決條件

在深入了解使用 Aspose.PSD for .NET 調整大小的魔力之前，請確保滿足以下先決條件：

1.  Aspose.PSD for .NET 函式庫：確保您已安裝 Aspose.PSD for .NET 函式庫。您可以從[Aspose.PSD for .NET 版本](https://releases.aspose.com/psd/net/)頁。

2. 文檔目錄：建立一個目錄來儲存您的文檔，並將提供的程式碼中的「您的文檔目錄」替換為該目錄的實際路徑。

現在您已經設定了先決條件，讓我們進入逐步指南。

## 導入命名空間

```csharp
using Aspose.PSD.ImageOptions;
```

導入必要的命名空間以存取所需的類別和方法。

## 第 1 步：載入圖像

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

//將現有映像載入到 RasterImage 類別的實例中
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	//其餘步驟請移至此處
}
```

使用載入來源圖像`Image.Load`方法。

## 第 2 步：指定寬度和高度

```csharp
//指定寬度和高度
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

確定調整後的影像的新寬度和高度。在此範例中，寬度和高度減半，但您可以根據您的要求調整這些值。

## 第 3 步：儲存調整大小的影像

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

使用以下命令儲存調整大小的圖像`Save`具有指定選項的方法。在本例中，我們將其另存為 PNG 檔案。

## 結論

在 Aspose.PSD for .NET 中按比例調整圖像大小是一個簡單的過程，可以為您的圖像處理工作流程增加價值。本指南為您提供了將此功能無縫整合到您的應用程式中的知識。

## 常見問題解答

### Q1：我可以將影像調整為特定尺寸嗎？

A1: 是的，您可以根據程式碼中的要求自訂新的寬度和高度。

### Q2：Aspose.PSD for .NET 適合批次調整影像大小嗎？

A2：當然！您可以將這些步驟合併到一個循環中以批次處理多個影像。

### Q3：Aspose.PSD for .NET 中還有其他影像處理功能嗎？

A3：是的，Aspose.PSD for .NET 提供了廣泛的功能，包括裁剪、旋轉以及對影像套用濾鏡。

### 問題 4：Aspose.PSD for .NET 是否有免費試用版？

 A4：是的，您可以透過免費試用來探索 Aspose.PSD for .NET 的功能。訪問[這裡](https://releases.aspose.com/)開始吧。

### Q5：在哪裡可以找到 Aspose.PSD for .NET 支援？

 A5：訪問[Aspose.PSD for .NET 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和討論。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
