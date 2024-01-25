---
title: Aspose.PSD for Java 中的反轉調整圖層
linktitle: 反轉調整圖層
second_title: Aspose.PSD Java API
description: 探索 Aspose.PSD for Java 中的反轉調整圖層。用於無縫 PSD 檔案操作的強大 Java 程式庫。
type: docs
weight: 14
url: /zh-hant/java/advanced-image-manipulation/invert-adjustment-layer/
---
## 介紹

歡迎來到我們關於在 Aspose.PSD for Java 中實作反轉調整層的逐步指南。在本教程中，我們將探索 Aspose.PSD 的強大功能，這是一個允許無縫操作 PSD 檔案的 Java 程式庫。無論您是經驗豐富的開發人員還是影像處理新手，本教學旨在幫助您有效地理解和實現反轉調整層。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

1. Aspose.PSD 庫：確保您已下載並安裝 Aspose.PSD 庫。你可以找到下載鏈接[這裡](https://releases.aspose.com/psd/java/).

2. Java 開發環境：確保您的系統上設定了 Java 開發環境。

現在，讓我們開始實作。

## 導入包

首先在 Java 應用程式中導入必要的套件。這些套件對於使用 Aspose.PSD 功能至關重要。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## 第 1 步：設定文檔目錄

初始化 PSD 檔案所在的目錄。

```java
String dataDir = "Your Document Directory";
```

## 第 2 步：載入 PSD 文件

使用 Aspose.PSD 庫載入 PSD 檔案。

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## 步驟3：新增反轉調整圖層

在載入的 PSD 映像上實作反轉調整圖層。

```java
im.addInvertAdjustmentLayer();
```

## 第 4 步：儲存輸出

使用套用的反轉調整圖層儲存修改後的 PSD 影像。

```java
im.save(outputPath);
```

恭喜！您已經使用 Aspose.PSD for Java 成功實現了反轉調整圖層。請隨意探索 Aspose.PSD 提供的更多特性和功能，以增強您的影像處理能力。

## 結論

在本教程中，我們介紹了使用 Aspose.PSD for Java 將反轉調整圖層合併到 PSD 檔案中的逐步過程。這個多功能庫使開發人員能夠輕鬆地操作圖像，為創意專案開啟了一個充滿可能性的世界。

## 常見問題解答

### Q1：Aspose.PSD 是否與所有 Java 版本相容？

A1：Aspose.PSD支援Java 6.0及更高版本。

### Q2：我可以在一次操作中套用多個調整圖層嗎？

A2：是的，您可以堆疊多個調整圖層來實現複雜的影像操作。

### Q3：在哪裡可以找到 Aspose.PSD 的附加文件？

 A3：參考文檔[這裡](https://reference.aspose.com/psd/java/)以獲得全面的資訊。

### Q4：Aspose.PSD 有免費試用版嗎？

 A4：是的，您可以探索免費試用[這裡](https://releases.aspose.com/).

### Q5：如何取得Aspose.PSD的臨時授權？

A5：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).