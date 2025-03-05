---
title: 在 Aspose.PSD for .NET 中簡單調整圖片大小
linktitle: 簡單調整影像大小
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 調整影像大小。高效、無縫且強大。輕鬆提升您的 .NET 專案。
type: docs
weight: 17
url: /zh-hant/net/image-manipulation/simple-resizing/
---
## 介紹

在 .NET 開發的動態領域中，操作影像是常見的需要。 Aspose.PSD for .NET 以其強大的功能來救援，為影像調整大小提供無縫體驗。在本教程中，我們將深入研究使用 Aspose.PSD for .NET 調整圖像大小的簡單但關鍵的過程。請繫好安全帶，我們將踏上增強您的影像處理技能的旅程。

## 先決條件

在我們深入學習本教學之前，讓我們確保您已完成一切設定以獲得流暢的體驗：

## 導入命名空間

確保您已匯入必要的命名空間來存取 Aspose.PSD for .NET 的功能：

```csharp
using Aspose.PSD.ImageOptions;
```

現在，讓我們將調整影像大小的過程分解為多個步驟：

## 第 1 步：設定您的文件目錄

首先設定文檔目錄的路徑：

```csharp
string dataDir = "Your Document Directory";
```

## 第 2 步：載入圖像

將現有映像載入到 RasterImage 類別的實例中：

```csharp
string sourceFile = dataDir + @"sample.psd";
using (Image image = Image.Load(sourceFile))
{
    //你的程式碼在這裡
}
```

## 第 3 步：調整影像大小

調整圖像大小就像調用`Resize`影像物件上的方法：

```csharp
image.Resize(300, 300);
```

## 第 4 步：儲存調整大小的影像

使用您喜歡的格式和選項儲存調整大小的影像。在此範例中，我們將其另存為 JPEG：

```csharp
string destName = dataDir + @"SimpleResizing_out.jpg";
image.Save(destName, new JpegOptions());
```

就是這樣！您已成功使用 Aspose.PSD for .NET 調整圖片大小。

## 結論

掌握影像大小調整是任何 .NET 開發人員工具包中的基本技能。借助 Aspose.PSD for .NET，過程不僅變得高效而且令人愉快。現在，掌握了這些知識，就可以繼續提升您在 .NET 專案中的影像處理能力。

## 常見問題解答

### 問題 1：我可以使用 Aspose.PSD for .NET 將圖片大小調整為特定的寬高比嗎？

A1：是的，您可以在調整影像大小時透過相應調整寬度或高度來保持特定的寬高比。

### Q2：Aspose.PSD for .NET 是否支援 JPEG 以外的其他影像格式？

A2：當然！ Aspose.PSD for .NET 支援多種圖片格式，包括 PNG、GIF、BMP 等。

### Q3：Aspose.PSD for .NET 是否有臨時授權？

A3：是的，您可以獲得 Aspose.PSD for .NET 的臨時許可證，以便在購買之前評估其功能。

### 問題 4：在哪裡可以找到 Aspose.PSD for .NET 的綜合文件？

 A4：查看詳細文檔[Aspose.PSD for .NET 文檔](https://reference.aspose.com/psd/net/).

### 問題 5：如何獲得 Aspose.PSD for .NET 的支援或與社群連結？

 A5：訪問[Aspose.PSD for .NET 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和討論。