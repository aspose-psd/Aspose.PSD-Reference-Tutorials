---
title: 使用 Aspose.PSD for Java 建立 XMP 元數據
linktitle: 建立 XMP 元數據
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 增強您的 Java 應用程式。了解輕鬆建立 XMP 元資料。現在就按照我們的逐步指南進行操作。
weight: 12
url: /zh-hant/java/image-editing/create-xmp-metadata/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 建立 XMP 元數據

## 介紹

在 Java 開發領域，管理和操作圖像元資料對於各種應用程式至關重要。 Aspose.PSD for Java 是處理 PSD 檔案的強大工具，在本教程中，我們將深入研究使用這個強大的程式庫建立 XMP 元資料。

## 先決條件

在開始本教學之前，請確保您具備以下先決條件：

- Java 開發環境：系統上安裝了 Java，並且對 Java 程式設計有基本的了解。
-  Aspose.PSD 函式庫：下載並設定適用於 Java 的 Aspose.PSD 函式庫。您可以找到該庫和詳細文檔[這裡](https://reference.aspose.com/psd/java/).
- 您的文件目錄：定義儲存文件檔案的目錄。

## 導入包

在您的 Java 專案中，匯入必要的套件以利用 Aspose.PSD 功能：

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## 第 1 步：指定圖像尺寸

```java
//透過定義矩形指定影像的大小
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## 第 2 步：建立新映像

```java
//創建一個全新的圖像用於範例目的
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## 第 3 步：建立 XMP 標頭

```java
//建立 XMP-Header 的實例
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## 第 4 步：建立 XMP 預告片

```java
//建立 Xmp-TrailerPi 的實例
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 第 5 步：建立 XMP 元數據

```java
//建立XMPmeta類別的實例來設定不同的屬性
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## 第 6 步：建立 XMP 封包包裝器

```java
//建立包含所有元資料的 XmpPacketWrapper 實例
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## 步驟7：設定Photoshop屬性

```java
//建立 Photoshop 套件的實例並設定 Photoshop 屬性
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## 步驟 8：將 Photoshop 套件新增至 XMP 元數據

```java
//將 Photoshop 套件加入 XMP 元資料中
xmpData.addPackage(photoshopPackage);
```

## 步驟 9：設定 DublinCore 屬性

```java
//建立 DublinCore 套件的實例並設定 DublinCore 屬性
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## 步驟 10：將 DublinCore 套件加入 XMP 元數據

```java
//將 DublinCore 套件加入 XMP 元資料中
xmpData.addPackage(dublinCorePackage);
```

## 步驟 11：將 XMP 元資料更新到影像中

```java
//將 XMP 元資料更新到影像中
image.setXmpData(xmpData);
```

## 第12步：儲存影像

```java
//將影像保存在磁碟或記憶體流中
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## 結論

恭喜！您已使用 Aspose.PSD for Java 成功為映像建立了 XMP 元資料。本教學為您提供了無縫增強和管理 Java 應用程式中的元資料的基本步驟。

## 常見問題解答

### Q1：Aspose.PSD是否相容於不同的影像格式？

A1：是的，Aspose.PSD 支援各種影像格式，提供處理不同檔案類型的多功能性。

### Q2：我可以使用 Aspose.PSD 操作現有元資料嗎？

A2：當然，Aspose.PSD 允許您修改和更新圖像中的現有元資料。

### Q3：Aspose.PSD 可以處理的圖片大小有限制嗎？

A3：Aspose.PSD 旨在處理各種尺寸的影像，確保您的專案的可擴展性。

### Q4：Aspose.PSD 有試用版嗎？

 A4：是的，您可以透過免費試用來探索 Aspose.PSD 的功能[這裡](https://releases.aspose.com/).

### Q5：我可以在哪裡尋求 Aspose.PSD 相關查詢的支援？

 A5：如需任何協助或疑問，請訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
