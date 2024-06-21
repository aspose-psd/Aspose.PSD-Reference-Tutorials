---
title: 使用 Aspose.PSD for .NET 建立橢圓形狀
linktitle: 使用 Aspose.PSD for .NET 建立橢圓形狀
second_title: Aspose.PSD .NET API
description: 了解如何使用 Aspose.PSD 在 .NET 中繪製橢圓形。帶有程式碼範例的分步指南。輕鬆創建令人驚嘆的圖形。
type: docs
weight: 13
url: /zh-hant/net/psd-drawing-techniques/creating-elliptical-shapes/
---
## 介紹

歡迎閱讀我們有關使用 Aspose.PSD for .NET 建立橢圓形狀的綜合指南。 Aspose.PSD 是一個功能強大的.NET 程式庫，可讓開發人員操作和轉換 Photoshop 文件，而無需 Adobe Photoshop。在本教程中，我們將引導您完成使用該庫繪製橢圓形狀的過程。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

- Aspose.PSD for .NET 函式庫：確保您的 .NET 專案中安裝了 Aspose.PSD 函式庫。您可以從[Aspose.PSD for .NET 文檔](https://reference.aspose.com/psd/net/).

- .NET 環境：本教學假設您具有 .NET 架構的應用知識。

## 導入命名空間

首先，將必要的命名空間匯入到您的專案中。這可確保您可以存取繪製橢圓形狀所需的類別和方法。這是一個例子：

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

現在，讓我們將建立橢圓形狀的過程分解為多個步驟：

## 第 1 步：設定文檔目錄

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";
```

## 第 2 步：建立 BmpOptions 實例

```csharp
//建立 BmpOptions 的實例並設定其各種屬性
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## 第 3 步：建立映像實例

```csharp
//建立圖像實例
using (Image image = new PsdImage(100, 100))
{
    //建立並初始化 Graphics 類別的實例和 Clear Graphics 表面
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## 第四步：畫一個虛線橢圓形狀

```csharp
    //透過指定紅色的 Pen 物件和周圍的矩形來繪製虛線橢圓形狀
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## 第五步：畫一個連續的橢圓形

```csharp
    //透過指定具有藍色實心畫筆和周圍矩形的 Pen 物件來繪製連續的橢圓形狀
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    //將影像匯出為 bmp 檔案格式。
    image.Save(outpath, saveOptions);
}
```

## 結論

恭喜！您已使用 Aspose.PSD for .NET 成功建立了橢圓形。本教學涵蓋了從設定環境到繪製點狀和連續橢圓形狀的基本步驟。

## 常見問題解答

### Q1：在哪裡可以找到 Aspose.PSD for .NET 的文件？

 A1：文檔可用。[這裡](https://reference.aspose.com/psd/net/).

### Q2：如何下載 Aspose.PSD for .NET？

 A2：您可以從發布頁面下載它。[這裡](https://releases.aspose.com/psd/net/).

### Q3：有免費試用嗎？

 A3：是的，您可以免費試用。[這裡](https://releases.aspose.com/).

### 問題 4：如何獲得 Aspose.PSD for .NET 支援？

 A4：造訪支援論壇[這裡](https://forum.aspose.com/c/psd/34).

### Q5：測試需要臨時許可證嗎？

 A5: 是的，您可以獲得臨時許可證。[這裡](https://purchase.aspose.com/temporary-license/).