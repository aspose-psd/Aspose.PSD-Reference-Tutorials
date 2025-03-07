---
title: 使用 Aspose.PSD for Java 執行簡單繪圖
linktitle: 進行簡單繪圖
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 在 PSD 檔案中繪製形狀。本逐步指南涵蓋了建立、新增圖層以及使用程式碼範例進行繪圖的內容。
weight: 10
url: /zh-hant/java/basic-image-operations/simple-drawing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 執行簡單繪圖

## 介紹

歡迎閱讀有關使用 Aspose.PSD for Java 執行簡單繪圖的逐步指南！在本教程中，我們將探索建立新 PSD 文件、新增圖層以及使用不同顏色繪製形狀的基礎知識。 Aspose.PSD for Java 是一個功能強大的函式庫，可讓您以程式設計方式操作 PSD 文件，為圖形設計任務提供廣泛的功能。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- 您的電腦上安裝了 Java 開發工具包 (JDK)。
- Java 函式庫的 Aspose.PSD。您可以從[Aspose.PSD for Java 文檔](https://reference.aspose.com/psd/java/).

## 導入包

首先，將必要的套件匯入到您的 Java 專案中。在 Java 檔案的開頭包含以下程式碼：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 第 1 步：建立一個新文檔

讓我們先建立一個具有指定寬度和高度的新 PSD 文件：

```java
//ExStart:建立文檔
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd：建立文檔
```

## 第 2 步：新增圖層

現在，讓我們使用無參構造函數為文件新增一個圖層：

```java
//ExStart:新增圖層
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//結束：新增圖層
```

## 第三步：繪製形狀

在此步驟中，我們將使用 Graphics 類別在建立的圖層上繪製形狀：

### 畫一個黃色的矩形

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd：繪製矩形黃色
```

### 畫一個紅色矩形

```java
//ExStart：繪製紅色矩形
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd：繪製紅色矩形
```

### 畫一個藍色矩形

```java
//ExStart：繪製藍色矩形
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd：繪製藍色矩形
```

## 第 4 步：儲存更改

最後，儲存已載入 PSD 檔案的副本（包括變更）：

```java
//ExStart:儲存更改
image.save(outPsdFilePath);
//ExEnd：儲存更改
```

## 結論

恭喜！您已經使用 Aspose.PSD for Java 成功執行了簡單的繪圖。本教學介紹了建立新文件、新增圖層以及繪製不同顏色的矩形。請隨意探索該庫為您的圖形設計需求提供的更多高級功能。

## 常見問題解答

### Q1：我可以使用Aspose.PSD for Java來操作現有的PSD檔案嗎？

A1：是的，Aspose.PSD for Java 提供了廣泛的功能來編輯和操作現有的 PSD 檔案。

### Q2：在哪裡可以找到 Aspose.PSD for Java 的支援？

 A2：您可以訪問[Aspose.PSD for Java 論壇](https://forum.aspose.com/c/psd/34)任何與支援相關的查詢。

### Q3：Aspose.PSD for Java 有免費試用版嗎？

A3：是的，您可以存取免費試用版[這裡](https://releases.aspose.com/).

### Q4：如何購買 Aspose.PSD for Java 的授權？

 A4：您可以從[Aspose.PSD 購買頁面](https://purchase.aspose.com/buy).

### Q5：Aspose.PSD for Java 是否有臨時授權？

A5：是的，您可以從以下機構獲得臨時許可證：[這裡](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
