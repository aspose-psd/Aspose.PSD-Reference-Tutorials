---
title: 在 Aspose.PSD for .NET 中建立 XMP 元數據
linktitle: 建立 XMP 元數據
second_title: Aspose.PSD .NET API
description: 探索 Aspose.PSD for .NET 中的 XMP 元資料建立。透過無縫操作增強影像組織。
type: docs
weight: 10
url: /zh-hant/net/file-and-font-handling/create-xmp-metadata/
---
## 介紹

在 .NET 開發的動態世界中，精確操作影像是許多應用程式的重要方面。本教學探討了在 Aspose.PSD for .NET 中建立 XMP 元數據，這是一個可以簡化影像處理任務的強大函式庫。 XMP（可擴展元資料平台）可讓您將元資料嵌入影像檔案中，從而促進高效組織和檢索與影像相關的資訊。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for .NET Library：從以下位置下載並安裝該程式庫：[Aspose.PSD 文檔](https://reference.aspose.com/psd/net/).

- 開發環境：使用 Visual Studio 或您首選的 IDE 設定 .NET 開發環境。

- 基本 .NET 知識：熟悉基本 .NET 概念，因為本教學假設您對 .NET 開發有基本的了解。

## 導入命名空間

在您的 .NET 專案中，包含存取 Aspose.PSD 功能所需的命名空間：

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

現在，讓我們將建立 XMP 元資料的過程分解為一系列綜合步驟。

## 第 1 步：指定圖像大小和矩形

```csharp
//文檔目錄的路徑。
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//透過定義矩形指定影像的大小
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## 第 2 步：建立新映像

```csharp
//建立全新影像以供樣品使用
using (var image = new PsdImage(rect.Width, rect.Height))
{
    //圖像處理程式碼在這裡...
}
```

## 步驟 3： 建立 XMP 標頭和 XMP 尾部

```csharp
//建立 XMP-Header 的實例
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

//建立XMP-TrailerPi、XMPmeta類別的實例來設定不同的屬性
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## 步驟 4：設定 XMP 屬性

```csharp
//設定XMP屬性，例如：
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## 第 5 步：建立 XMP 封包包裝器

```csharp
//建立包含所有元資料的 XmpPacketWrapper 實例
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## 步驟6：建立Photoshop套件並設定屬性

```csharp
//建立 Photoshop 套件實例並設定 Photoshop 屬性
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## 步驟 7：將 Photoshop 套件新增至 XMP 元數據

```csharp
//將 Photoshop 套件加入 XMP 元資料中
xmpData.AddPackage(photoshopPackage);
```

## 步驟8：建立DublinCore套件並設定屬性

```csharp
//建立 DublinCore 套件的實例並設定 dublinCore 屬性
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## 第 9 步：將 DublinCore 套件加入 XMP 元數據

```csharp
//將 dublinCore 套件加入 XMP 元資料中
xmpData.AddPackage(dublinCorePackage);
```

## 步驟 10：更新 XMP 元資料並儲存影像

```csharp
using (var ms = new MemoryStream())
{
    //將 XMP 元資料更新到影像中並將影像保存在磁碟或記憶體流中
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## 第11步：載入圖像並讀取元數據

```csharp
//從內存流或磁碟加載圖像以讀取/獲取元數據
using (var img = (PsdImage)Image.Load(ms))
{
    //取得 XMP 元數據
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        //使用套件資料...
    }
}
```

## 結論

恭喜！您已在 Aspose.PSD for .NET 中成功建立了 XMP 元資料。這種強大的功能增強了您的影像處理能力，從而可以有效地組織和檢索重要資訊。

## 常見問題解答

### Q1：Aspose.PSD for .NET 是否相容於所有影像格式？

A1：Aspose.PSD 主要專注於 PSD (Adobe Photoshop) 檔案格式，但支援各種其他格式。

### 問題 2：我可以使用 Aspose.PSD for .NET 操作現有的 XMP 元資料嗎？

A2：是的，Aspose.PSD 可讓您讀取和修改現有的 XMP 元資料。

### Q3：使用 Aspose.PSD for .NET 時圖片大小有限制嗎？

A3：Aspose.PSD 可以處理不同尺寸的影像，但超大影像可能需要額外考慮。

### Q4：Aspose.PSD for .NET 多久更新一次？

A4：定期發布更新，以確保與最新的 .NET 框架版本和行業標準相容。

### Q5：有 Aspose.PSD 支援的社群論壇嗎？

答：是的，您可以在以下位置找到支援和討論：[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34).