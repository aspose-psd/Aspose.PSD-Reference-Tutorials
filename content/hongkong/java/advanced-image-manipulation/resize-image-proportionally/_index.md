---
title: 使用 Aspose.PSD for Java 按比例調整影像大小
linktitle: 按比例調整影像大小
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 增強您的 Java 應用程式。按照我們的指南輕鬆按比例調整圖像大小。立即提高您的影像處理能力。
type: docs
weight: 17
url: /zh-hant/java/advanced-image-manipulation/resize-image-proportionally/
---
## 介紹

歡迎來到我們關於使用 Aspose.PSD for Java 按比例調整圖片大小的逐步指南。如果您希望透過高效的圖像調整功能來增強 Java 應用程序，那麼您來對地方了。在本教程中，我們將使用清晰簡潔的步驟來引導您完成整個過程。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

1. Java 環境：確保您的系統上安裝了 Java。
2.  Aspose.PSD 庫：下載並安裝 Aspose.PSD 庫。你可以找到需要的資源[這裡](https://releases.aspose.com/psd/java/).

## 導入包

整理好先決條件後，將所需的套件匯入到您的 Java 專案中。確保您的專案中正確引用了 Aspose.PSD 庫。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## 第 1 步：載入圖像

首先將要調整大小的圖像載入到 Java 應用程式中。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## 第 2 步：指定寬度和高度

確定調整後的影像的新寬度和高度。在此範例中，我們將影像大小調整為其原始尺寸的一半。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## 第 3 步：儲存調整大小的影像

將調整大小的影像儲存到所需位置，並指定格式選項（在本例中為 PNG）。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

現在你就擁有了！您已成功使用 Aspose.PSD for Java 按比例調整圖片大小。

## 結論

在本教程中，我們介紹了使用 Java 的 Aspose.PSD 庫按比例調整圖像大小的基本步驟。現在，您可以輕鬆地將此功能整合到您的 Java 應用程式中，以改進影像處理。

## 常見問題解答

### Q1：Aspose.PSD 是否相容於所有影像格式？

 A1：Aspose.PSD支援多種影像格式，包括PSD、PNG、JPEG等。檢查[文件](https://reference.aspose.com/psd/java/)以獲得完整的清單。

### Q2：我可以將Aspose.PSD用於商業項目嗎？

 A2: 是的，可以。參觀[購買頁面](https://purchase.aspose.com/buy)了解許可詳細資訊。

### Q3：臨時許可證是否可用於測試目的？

 A3：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)進行評估。

### Q4：哪裡可以找到對 Aspose.PSD 的支援？

 A4：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區的支持和幫助。

### Q5：如何存取Aspose.PSD文件？

 A5：參考詳細文檔[這裡](https://reference.aspose.com/psd/java/).
`