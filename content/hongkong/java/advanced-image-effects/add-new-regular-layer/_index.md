---
title: 使用 Aspose.PSD for Java 將新的常規圖層新增至 PSD
linktitle: 為 PSD 新增的常規圖層
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 為 PSD 檔案新增新的常規圖層。請按照我們的逐步指南進行無縫 PSD 操作。
type: docs
weight: 11
url: /zh-hant/java/advanced-image-effects/add-new-regular-layer/
---
## 介紹

歡迎來到這個關於使用 Aspose.PSD for Java 為 PSD 檔案新增新的常規圖層的綜合教學。 Aspose.PSD 是一個功能強大的 Java 程式庫，可讓開發人員有效地操作和使用 PSD 檔案。在本教程中，我們將指導您完成向 PSD 檔案添加新的常規圖層的過程，並提供詳細的步驟和程式碼範例。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- Java 開發環境：確保您的系統上設定了 Java 開發環境。
-  Aspose.PSD 函式庫：下載並安裝 Aspose.PSD for Java 函式庫。你可以找到圖書館[這裡](https://releases.aspose.com/psd/java/).

## 導入包

首先，將必要的套件匯入到您的 Java 專案中。這些套件對於使用 Aspose.PSD 功能至關重要。在 Java 檔案的開頭包含以下行：

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 第 1 步：載入 PSD 文件

使用以下程式碼載入要編輯的 PSD 檔案：

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 第 2 步：準備資料數組和矩形

準備兩個 int 陣列和兩個 Rectangle 對象，如下圖所示：

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## 第三步：初始化圖層數據

使用預設值初始化資料數組：

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## 第四步：新增常規圖層

將兩個常規圖層新增至 PSD 影像：

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## 第5步：保存PSD和PNG

儲存修改後的 PSD 和附加 PNG 檔案：

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

恭喜！您已使用 Aspose.PSD for Java 成功將新的常規圖層新增至 PSD 檔案。

## 結論

在本教程中，我們介紹了使用 Aspose.PSD for Java 為 PSD 檔案新增新的常規圖層的過程。這個強大的程式庫簡化了 PSD 操作，使其可供 Java 開發人員使用。嘗試不同的參數和功能，探索 Aspose.PSD 的全部潛力。

## 常見問題解答

### Q1：Aspose.PSD 與 Java 8 相容嗎？

A1：是的，Aspose.PSD 支援 Java 8 及更高版本。

### Q2：我可以對新增的圖層套用變換嗎？

A2：當然！ Aspose.PSD 提供了一系列圖層轉換選項。

### Q3：在哪裡可以找到額外的 Aspose.PSD 文件？

 A3：您可以參考文件。[這裡](https://reference.aspose.com/psd/java/).

### Q4：如何取得Aspose.PSD的臨時授權？

 A4：參觀[這個連結](https://purchase.aspose.com/temporary-license/)用於臨時許可證選項。

### Q5：是否有支援 Aspose.PSD 的社群論壇？

 A5：是的，您可以找到支持和討論。[這裡](https://forum.aspose.com/c/psd/34).