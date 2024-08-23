---
title: 在 Aspose.PSD for .NET 中應用 Bradley 閾值
linktitle: 應用布拉德利閾值
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 中的 Bradley Threshold 增強影像分割。有效二值化的逐步指南。
type: docs
weight: 15
url: /zh-hant/net/image-processing/apply-bradley-threshold/
---
## 介紹

歡迎來到我們關於在 Aspose.PSD for .NET 中應用 Bradley Threshold 的綜合教學。 Aspose.PSD for .NET 是一個功能強大的程式庫，可讓您在 .NET 應用程式中使用 Photoshop 檔案。 Bradley 閾值處理是一種用於影像二值化的技術，有助於有效地將物件與背景分開。

在本教程中，我們將引導您完成使用 Aspose.PSD for .NET 應用 Bradley Threshold 的過程。在我們深入了解這些步驟之前，請確保您具備必要的先決條件。

## 先決條件

在開始之前，請確保您已進行以下設定：

-  Aspose.PSD for .NET Library：從以下位置下載並安裝該程式庫：[Aspose.PSD for .NET 文檔](https://reference.aspose.com/psd/net/).
- 文件目錄：建立一個目錄來儲存來源 PSD 檔案和產生的二值化影像。

現在您已準備好先決條件，讓我們繼續執行逐步指南。

## 導入命名空間

在您的 .NET 專案中，請確保匯入所需的命名空間以存取 Aspose.PSD 功能：

```csharp
//導入 Aspose.PSD 命名空間
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## 第 1 步：載入有雜訊的影像

定義來源 PSD 檔案的路徑和二進位輸出的目標：

```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"binarized_out.png";
```

## 步驟 2：使用 Bradley 閾值對影像進行二值化

載入 PSD 影像，指定閾值，套用 Bradley 閾值，並將輸出儲存為 PNG 影像：

```csharp
//載入圖片
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //定義閾值
    double threshold = 0.15;

    //呼叫 BinarizeBradley 方法並將閾值作為參數傳遞
    image.BinarizeBradley(threshold);

    //儲存輸出影像
    image.Save(destName, new PngOptions());
}
```

## 結論

恭喜！您已成功在 Aspose.PSD for .NET 中套用 Bradley Threshold。該技術對於增強各種應用中的影像分割非常有價值。

請隨意探索 Aspose.PSD for .NET 提供的更多特性和功能來最佳化您的影像處理任務。

## 常見問題解答

### Q1：我可以將 Bradley 閾值套用到任何類型的影像嗎？

A1：是的，Bradley 閾值是一種適用於各種影像類型的多功能技術。

### Q2：在哪裡可以找到其他 Aspose.PSD 文件？

 A2：請參閱[文件](https://reference.aspose.com/psd/net/)有關 Aspose.PSD for .NET 的詳細資訊。

### Q3：有免費試用嗎？

A3：是的，您可以探索 Aspose.PSD for .NET 的免費試用版[這裡](https://releases.aspose.com/).

### Q4：如何獲得 Aspose.PSD 的支援？

 A4：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和討論。

### Q5: 哪裡可以購買 Aspose.PSD 的授權？

 A5：您可以購買許可證[這裡](https://purchase.aspose.com/buy).