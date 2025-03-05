---
title: 使用 Aspose.PSD for Java 中的調整大小類型枚舉調整大小
linktitle: 使用調整大小類型枚舉調整大小
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 在 Java 中掌握影像大小調整。使用調整大小類型枚舉的逐步指南。
type: docs
weight: 18
url: /zh-hant/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## 介紹

在不斷發展的 Java 開發環境中，高效能的影像處理是開發人員經常要解決的關鍵問題。 Aspose.PSD for Java 成為一個強大的解決方案，提供了調整影像大小的無縫體驗，並具有調整大小類型枚舉的附加優勢。在本教程中，我們將深入研究使用 Aspose.PSD for Java 調整圖像大小的複雜性，分解每個步驟以確保全面理解。

## 先決條件

在開始本教學之前，請確保您具備以下先決條件：

1. Java 開發環境：確保您的電腦上設定了 Java 開發環境。

2. Aspose.PSD 庫：從以下位置下載並安裝 Aspose.PSD 庫：[網站](https://releases.aspose.com/psd/java/).

3. 範例 PSD 檔案：準備好範例 PSD 檔案以供實驗。您可以使用[Sample.psd]（您的文件目錄/sample.psd）本教學的檔案。

## 導入包

首先，將必要的套件匯入您的 Java 專案：

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 第 1 步：載入圖像

首先將現有圖像載入到實例中`RasterImage`班級。使用以下程式碼片段：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//將現有映像載入到 RasterImage 類別的實例中
Image image = Image.load(sourceFile);
```

## 第 2 步：調整影像大小

現在，使用調整大小類型列舉調整載入的圖像的大小。在此範例中，我們使用 Lanczos Resample 方法：

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 第 3 步：儲存調整大小的影像

調整大小後，使用指定尺寸和所選調整大小類型儲存影像。在這裡，我們將其另存為 JPEG 檔案：

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

現在你就擁有了！您已使用 Aspose.PSD for Java 中的調整大小類型枚舉成功調整了圖片大小。

總之，Aspose.PSD for Java 為影像操作提供了一個強大的平台，並且調整大小類型枚舉為該過程增加了一層靈活性。無論您正在處理小型專案還是大型應用程序，掌握這些步驟都將使您能夠無縫地處理影像大小調整。

## 常見問題解答

### Q1：Aspose.PSD for Java 適合小型和大型專案嗎？

A1：當然！ Aspose.PSD for Java 旨在滿足各種規模的項目，提供可擴展性和效率。

### 問題 2：我可以使用 Lanczos Resample 以外的其他調整大小類型嗎？

A2：是的，Aspose.PSD for Java 提供了各種調整大小類型，例如最近鄰、雙三次等。瀏覽文件以取得完整清單。

### 問題 3：在哪裡可以找到 Aspose.PSD for Java 的其他支援？

 A3：如有任何疑問或幫助，請訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34).

### Q4：Aspose.PSD for Java 有免費試用版嗎？

 A4：是的，您可以存取免費試用版[這裡](https://releases.aspose.com/).

### Q5: 如何取得 Aspose.PSD for Java 的臨時授權？

 A5：若要取得臨時許可證，請訪問[這個連結](https://purchase.aspose.com/temporary-license/).