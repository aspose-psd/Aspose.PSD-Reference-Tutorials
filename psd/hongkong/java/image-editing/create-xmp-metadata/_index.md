---
date: 2026-01-01
description: 學習如何建立 XMP 中繼資料、將 XMP 加入 PSD 檔案，並使用 Aspose.PSD for Java 更新影像中繼資料。立即跟隨此一步一步的指南。
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 建立 XMP 元資料
url: /zh-hant/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 建立 XMP 中繼資料

## Introduction

管理影像中繼資料是使用 Photoshop (PSD) 檔案的 Java 開發人員常見的需求。在本教學中，您將學習 **如何建立 XMP 中繼資料**，使用 Aspose.PSD 函式庫將 XMP 加入 PSD 圖像，並以程式方式更新影像中繼資料。我們將逐步說明每個步驟，解釋每個環節的重要性，並提供可在實際專案中應用的實用技巧。

## Quick Answers
- **XMP 中繼資料是什麼？** 一種標準化的格式，用於在影像檔案中嵌入描述性資訊（作者、關鍵字等）。  
- **為什麼使用 Aspose.PSD？** 它提供純 Java API，讓您在不使用 Photoshop 的情況下建立、讀取與編輯 PSD 檔案。  
- **我可以將 XMP 加入現有的 PSD 嗎？** 可以——您可以使用 `setXmpData` 即時更新影像中繼資料。  
- **主要步驟是什麼？** 設定影像尺寸、建立 header/trailer、建構 XMP 套件、附加套件，最後儲存。  
- **需要授權嗎？** 免費試用版可用於開發；正式上線需購買商業授權。

## What is “create XMP metadata” in Java?

建立 XMP 中繼資料表示組合一個 XMP 封包（包含 header、body、trailer），此封包描述影像內容，然後將其嵌入 PSD 檔案中。Aspose.PSD 函式庫會抽象化底層細節，讓您專注於要儲存的資訊本身。

## Why add XMP to PSD files?

- **可搜尋性：** 讓資產管理系統能依作者、標題或自訂標籤進行強大的搜尋。  
- **相容性：** XMP 被 Adobe 產品、Lightroom 以及多數 DAM 系統所識別。  
- **版本控制：** 可直接在檔案內儲存處理歷史（例如城市、色彩模式）。

## Prerequisites

- **Java 開發環境：** 已安裝 JDK 8 或以上，且具備基本的 Java 知識。  
- **Aspose.PSD 函式庫：** 下載並設定 Aspose.PSD for Java 函式庫。您可於 [此處](https://reference.aspose.com/psd/java/) 找到函式庫與詳細文件。  
- **文件目錄：** 決定在系統中讀寫 PSD 檔案的路徑。

## Import Packages

在您的 Java 專案中匯入必要的套件，以使用 Aspose.PSD 功能：

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

## Step 1: Specify Image Size

首先，為新建的 PSD 圖像定義畫布尺寸。

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Step 2: Create a New Image

建立一個空白的 PSD 圖像，稍後我們會為其加入 XMP 中繼資料。

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Step 3: Create XMP Header

Header 包含開頭的 XML 處理指令以及用於識別文件的 GUID。

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Step 4: Create XMP Trailer

Trailer 標示 XMP 封包的結尾。將 `true` 旗標設為 true 會寫入結束的處理指令。

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Step 5: Create XMP Metadata

為核心 XMP 中繼資料物件加入一般屬性，例如作者與說明。

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Step 6: Create XMP Packet Wrapper

將 header、trailer 與核心中繼資料封裝成單一封包，以便附加至影像。

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Step 7: Set Photoshop Attributes

填寫 Photoshop 專屬欄位（城市、國家、色彩模式），這些欄位是多數 Adobe 工具所期待的。

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Step 8: Add Photoshop Package to XMP Metadata

將 Photoshop 套件附加至 XMP 封包。

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Step 9: Set DublinCore Attributes

加入 Dublin Core 中繼資料，例如作者、標題，以及自訂的 movie 標籤。

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Step 10: Add DublinCore Package to XMP Metadata

將 Dublin Core 套件與現有的 XMP 封包合併。

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Step 11: Update XMP Metadata into Image

現在將完整的 XMP 封包嵌入 PSD 圖像中。

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Step 12: Save Image

最後，將 PSD 檔寫入磁碟（或記憶體串流），使中繼資料永久保存。

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Common Issues and Solutions

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **`NullPointerException` on `setXmpData`** | XMP 封包未完整建立（缺少 header/trailer）。 | 確認已建立 `XmpHeaderPi`、`XmpTrailerPi`，且在呼叫 `setXmpData` 前已加入所有套件。 |
| **Metadata not visible in Photoshop** | Photoshop 需要正確包裹的 XMP 封包。 | 確認使用 `XmpTrailerPi(true)`，且封包已隨影像一起儲存。 |
| **File path errors** | 使用相對路徑且權限不足。 | 改用絕對路徑或確保應用程式對目標資料夾具有寫入權限。 |

## Frequently Asked Questions

**Q: Aspose.PSD 是否相容於不同的影像格式？**  
A: 是的，Aspose.PSD 支援 PSD、PSB、BMP、GIF、JPEG、PNG、TIFF 等多種格式，提供跨格式的彈性。

**Q: 我可以使用 Aspose.PSD 操作既有的中繼資料嗎？**  
A: 當然可以。您可以載入現有的 PSD，使用 `getXmpData()` 取得 XMP 資料，修改封包後再儲存回去。

**Q: Aspose.PSD 在影像尺寸上有什麼限制嗎？**  
A: Aspose.PSD 設計可處理大型影像（最高可達數十億像素），唯一限制來自可用記憶體。

**Q: 有提供 Aspose.PSD 的試用版嗎？**  
A: 有，您可於 [此處](https://releases.aspose.com/) 取得免費試用版，體驗其功能。

**Q: 若有 Aspose.PSD 相關問題，該向哪裡尋求支援？**  
A: 歡迎前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 取得協助與解答。

## Conclusion

您現在已掌握 **如何建立 XMP 中繼資料**、將 XMP 加入 PSD，並使用 Aspose.PSD for Java 更新影像中繼資料。這些步驟讓您能完整控制嵌入影像的描述資訊，使其具備可搜尋性、相容性，並可順利進入後續工作流程。歡迎嘗試其他 XMP 架構，或將此程式碼整合至更大型的影像處理管線中。

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}