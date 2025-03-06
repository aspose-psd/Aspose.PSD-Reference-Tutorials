---
title: Java 中自動更正 JPEG 影像方向
linktitle: Java 中自動更正 JPEG 影像方向
second_title: Aspose.PSD Java API
description: 學習使用 Aspose.PSD 在 Java 中自動校正 JPEG 影像方向。輕鬆提升您的影像處理技能。
weight: 12
url: /zh-hant/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 中自動更正 JPEG 影像方向

## 介紹
在當今的數位時代，以程式設計方式操作和優化影像已成為各個領域的開發人員的關鍵任務。 Aspose.PSD for Java 為開發人員提供了強大的工具來有效地處理 PSD、JPEG 和其他影像格式。本教學深入探討一項特定任務：使用 Aspose.PSD for Java 自動校正 JPEG 影像方向。無論您是建立照片編輯應用程式、管理內容管理系統中的影像資源，還是自動化影像處理工作流程，本指南都將為您提供必要的知識，以便將此功能無縫整合到您的Java 應用程式中。
## 先決條件
在深入學習本教學之前，請確保您已設定以下先決條件：
- Java 開發環境：確保您的系統上安裝了 Java 開發工具包 (JDK)。
-  Aspose.PSD for Java JAR：從下列位置下載 Aspose.PSD for Java 函式庫[這裡](https://releases.aspose.com/psd/java/).
- 整合開發環境 (IDE)：使用 IntelliJ IDEA、Eclipse 或您選擇的任何 IDE 進行 Java 開發。
- 對 Java 和影像處理的基本了解：熟悉 Java 程式設計和影像處理的基本概念將很有幫助。

## 導入包
在開始範例之前，請確保從 Aspose.PSD for Java 匯入必要的套件：
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## 第 1 步：載入 PSD 映像
首先，載入包含方向需要校正的 JPEG 縮圖的 PSD 影像：
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
代替`"Your Document Directory"`與 PSD 檔案所在的實際目錄路徑。
## 第 2 步：迭代圖像資源
接下來，迭代圖像資源以尋找 JPEG 縮圖資源：
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    //尋找縮圖資源。通常它們採用 Jpeg 檔案格式。
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        //調整縮圖數據。
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            //如果儲存了縮圖，則自動旋轉它。
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## 第 3 步：儲存影像
最後，套用自動旋轉後儲存校正後的影像：
```java
image.save();
```
此步驟可確保影像所做的變更得以保留。

## 結論
總之，使用 Aspose.PSD for Java 提供了一個強大的解決方案，可以自動校正 PSD 檔案中的 JPEG 影像方向。透過遵循本教程中概述的步驟，開發人員可以增強其影像處理工作流程，確保影像在各種平台和裝置上正確顯示。
## 常見問題解答
### 什麼是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一個功能強大的函式庫，可讓 Java 開發人員以程式設計方式處理 PSD、JPEG 和其他影像格式。
### 如何下載 Java 版 Aspose.PSD？
您可以從以下位置下載該程式庫[這裡](https://releases.aspose.com/psd/java/).
### Aspose.PSD for Java 支援影像處理嗎？
是的，它支援各種影像處理任務，例如調整大小、裁剪和調整方向。
### 在哪裡可以找到 Aspose.PSD for Java 的文檔？
提供全面的文檔[這裡](https://reference.aspose.com/psd/java/).
### 我可以免費試用 Aspose.PSD for Java 嗎？
是的，您可以從以下位置獲得免費試用[這裡](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
