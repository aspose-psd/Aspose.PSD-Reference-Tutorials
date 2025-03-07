---
title: 在 Aspose.PSD for Java 中以矩形裁切影像
linktitle: 按矩形裁切影像
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 探索 Java 中的無縫影像裁切功能。按照我們的逐步指南，使用 Aspose.PSD for Java 輕鬆裁切影像。
weight: 15
url: /zh-hant/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for Java 中以矩形裁切影像

## 介紹

在Java開發領域，操作影像是一項常見的任務，Aspose.PSD for Java為影像處理提供了強大的解決方案。在本教學中，我們將引導您完成使用 Aspose.PSD for Java 將影像裁切為矩形的過程。請按照以下步驟輕鬆實現此目的。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- 您的電腦上安裝了 Java 開發工具包 (JDK)。
- Java 函式庫的 Aspose.PSD。您可以從[網站](https://releases.aspose.com/psd/java/).

## 導入包

確保在您的 Java 專案中包含必要的套件，以利用 Aspose.PSD for Java 的功能。在 Java 檔案的開頭加入以下導入語句：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

現在，讓我們將流程分解為多個步驟，引導您使用 Aspose.PSD for Java 將影像裁切為矩形。

## 第 1 步：設定您的文件目錄

```java
String dataDir = "Your Document Directory";
```

代替`"Your Document Directory"`與 PSD 檔案所在的實際路徑。

## 第 2 步：指定來源文件和目標文件

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

定義來源 PSD 檔案和目標 JPEG 檔案的路徑。

## 第 3 步：載入並快取圖像

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

將 PSD 映像載入到`RasterImage`實例並快取其資料。

## 第 4 步：建立並定義裁剪矩形

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

建立一個實例`Rectangle`具有所需裁剪尺寸的類別。

## 第 5 步：裁剪並儲存影像

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

使用指定的矩形執行裁剪操作並將結果儲存為 JPEG 檔案。

根據需要重複這些步驟，並根據您的特定要求調整參數。

## 結論

在本教學中，我們示範了使用 Aspose.PSD for Java 將影像裁切為矩形的過程。透過執行這些步驟，您可以輕鬆地將強大的影像處理功能整合到您的 Java 應用程式中。

## 常見問題解答

### Q1：我可以將 Aspose.PSD for Java 與其他 Java 框架一起使用嗎？

A1：是的，Aspose.PSD for Java 可以與各種 Java 框架集成，為您的開發專案提供靈活性。

### Q2：Aspose.PSD for Java 有免費試用版嗎？

 A2：是的，您可以存取免費試用版[這裡](https://releases.aspose.com/).

### 問題 3：我可以在哪裡找到額外的支援或協助？

 A3：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和討論。

### Q4：如何取得 Aspose.PSD for Java 的臨時授權？

 A4：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：Aspose.PSD for Java 支援哪些影像格式進行裁切？

A5：Aspose.PSD for Java支援多種影像格式，包括PSD、PNG、JPEG等。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
