---
title: 在 Aspose.PSD for Java 中旋轉影像
linktitle: 旋轉影像
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 輕鬆探索 Java 中的影像旋轉。輕鬆旋轉、翻轉和儲存 PSD 檔案。
type: docs
weight: 19
url: /zh-hant/java/advanced-image-manipulation/rotate-image/
---
## 介紹

Aspose.PSD for Java 提供了一組強大的影像處理功能，使開發人員能夠有效地操作和處理 PSD 檔案。在本教程中，我們將重點放在一項特定任務：旋轉圖像。無論您是建立照片編輯應用程式還是僅需要調整影像的方向，Aspose.PSD 都能使過程變得簡單。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.PSD for Java 函式庫：確保您已下載並安裝 Aspose.PSD for Java 函式庫。您可以找到該庫和詳細文檔[這裡](https://reference.aspose.com/psd/java/).

- Java 開發環境：確保您的電腦上設定了 Java 開發環境。

- 範例 PSD 檔案：準備要旋轉的範例 PSD 檔案。調整`sourceFile`範例程式碼中的變數以及 PSD 檔案的路徑。

## 導入包

首先導入必要的套件以利用 Aspose.PSD 的功能：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 第 1 步：載入圖像

將現有映像載入到實例中`Image`班級：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## 第 2 步：旋轉影像

使用旋轉影像`rotateFlip`方法。在此範例中，我們將影像旋轉 270 度：

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 步驟 3：儲存旋轉影像

使用以下命令儲存旋轉後的影像`save`方法並指定輸出格式（在本例中為 JPEG）：

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## 結論

恭喜！您已使用 Aspose.PSD for Java 成功旋轉了影像。這個簡單但功能強大的程式庫為您的 Java 應用程式中的圖像操作開闢了一個可能性的世界。

## 常見問題解答

### Q1：Aspose.PSD 是否相容於不同的影像格式？

A1：是的，Aspose.PSD支援各種影像格式，包括PSD、JPEG、PNG等。

### 問題 2：我可以應用自訂旋轉，而不僅僅是預先定義的翻轉嗎？

A2：當然！ Aspose.PSD 提供了應用自訂旋轉的靈活性，以滿足您的特定要求。

### 問題 3：我可以在哪裡找到額外的支援或協助？

 A3：如有任何疑問或問題，請訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持。

### Q4：有免費試用嗎？

 A4：是的，您可以使用[免費試用](https://releases.aspose.com/).

### Q5：如何取得臨時駕照？

 A5：如果您需要臨時許可證，您可以獲得一個[這裡](https://purchase.aspose.com/temporary-license/).