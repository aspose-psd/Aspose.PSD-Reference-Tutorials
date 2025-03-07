---
title: 在 Aspose.PSD for .NET 中旋轉影像
linktitle: 旋轉影像
second_title: Aspose.PSD .NET API
description: 學習使用 Aspose.PSD 在 .NET 中輕鬆旋轉影像。請按照我們的逐步教學進行操作。
weight: 15
url: /zh-hant/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for .NET 中旋轉影像

## 介紹

如果您正在使用 .NET 深入研究影像處理世界，Aspose.PSD 是您無縫、高效影像處理的首選工具。在本教程中，我們將重點放在一項基本任務 - 使用 Aspose.PSD for .NET 旋轉圖像。請跟隨我們將流程分解為簡單、可操作的步驟。

## 先決條件

在我們開始之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET Library：從以下位置下載並安裝該程式庫：[Aspose.PSD .NET 文檔](https://reference.aspose.com/psd/net/).

- 您的文件目錄：設定儲存影像的目錄。將程式碼片段中的「您的文件目錄」替換為該目錄的路徑。

## 導入命名空間

確保包含存取 Aspose.PSD 功能所需的命名空間。在 .NET 專案的開頭新增以下行：

```csharp
using Aspose.PSD.ImageOptions;
```

## 第 1 步：載入圖像

```csharp
string sourceFile = dataDir + @"sample.psd";

//將現有映像載入到 RasterImage 類別的實例中
using (Image image = Image.Load(sourceFile))
{
```

## 第 2 步：旋轉影像

```csharp
    //將影像順時針旋轉 270 度
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 步驟 3：儲存旋轉影像

```csharp
    //將旋轉後的影像儲存為 JPEG 文件
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

就是這樣！只需幾行程式碼，您就可以使用 Aspose.PSD for .NET 成功旋轉影像。

## 結論

在本教程中，我們探索了使用 Aspose.PSD for .NET 旋轉影像的基礎知識。 Aspose.PSD 提供了一組強大的影像處理工具，使其成為 .NET 開發人員的必備函式庫。嘗試不同的旋轉並探索進一步的功能來增強您的影像處理工作流程。

## 常見問題解答

### Q1：我可以使用 Aspose.PSD 將影像旋轉自訂角度嗎？

是的，Aspose.PSD 可讓您指定自訂旋轉角度。只需更換`RotateFlipType.Rotate270FlipNone`與您想要的旋轉角度一致。

### Q2：Aspose.PSD 是否相容於各種影像格式？

絕對地。 Aspose.PSD支援多種影像格式，包括PSD、JPEG、PNG等。檢查[文件](https://reference.aspose.com/psd/net/)取得完整清單。

### Q3：如何取得 Aspose.PSD 的臨時授權？

參觀[臨時許可證頁面](https://purchase.aspose.com/temporary-license/)在 Aspose 網站上取得用於評估目的的臨時許可證。

### Q4：哪裡可以找到對 Aspose.PSD 的支援？

如有任何疑問或幫助，請訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)並與社區建立聯繫。

### Q5：我可以購買Aspose.PSD用於商業用途嗎？

當然。探索[購買頁面](https://purchase.aspose.com/buy)取得適合您需求的許可證。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
