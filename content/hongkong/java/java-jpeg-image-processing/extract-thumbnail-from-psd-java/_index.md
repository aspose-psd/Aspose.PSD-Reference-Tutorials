---
title: 在 Java 中從 PSD 中提取縮圖
linktitle: 在 Java 中從 PSD 中提取縮圖
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 從 PSD 檔案中提取縮圖。本逐步指南涵蓋了從設定到保存提取的圖像的所有內容。
type: docs
weight: 15
url: /zh-hant/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## 介紹
在本教學中，我們將探討如何使用 Aspose.PSD for Java 從 PSD 檔案中擷取縮圖。縮圖對於快速預覽或建立嵌入 PSD 文件中的影像的較小版本非常有用。讓我們深入了解使用 Aspose.PSD 實現此目的所需的步驟。
## 先決條件
在開始之前，請確保您已進行以下設定：
- 您的系統上安裝了 Java 開發工具包 (JDK)。
-  Java 函式庫的 Aspose.PSD。您可以從以下位置下載：[這裡](https://releases.aspose.com/psd/java/).
- Java 程式設計的基礎知識。
## 導入包
首先，在您的 Java 類別中包含必要的 Aspose.PSD 套件：
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## 第 1 步：載入 PSD 文件
首先，載入包含要擷取的縮圖的 PSD 檔案。
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
代替`"Your_Document_Directory/"`與 PSD 檔案所在的目錄路徑，以及`"your_file.psd"`與您的 PSD 檔案的名稱。
## 第 2 步：迭代圖像資源
迭代圖像資源以尋找縮圖資源。
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        //提取縮圖數據
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        //使用提取的縮圖資料建立新影像
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        //將提取的縮圖另存為單獨的 JPEG 文件
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        //輸出成功訊息
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; //找到並處理縮圖後退出循環
    }
}
```
## 第 3 步：保存提取的縮圖
將提取的縮圖另存為單獨的圖像檔案（在本例中為 JPEG 檔案）。
## 步驟 4：處理不同的縮圖類型
如果您的 PSD 檔案可能包含多種類型的縮圖，例如`Thumbnail4Resource`，您可以擴展邏輯以類似地處理這些情況。

## 結論
在本教學中，我們探討如何使用 Aspose.PSD for Java 從 PSD 檔案中擷取縮圖。透過執行上述步驟，您可以有效地檢索和儲存 PSD 文件中嵌入的縮圖。

## 常見問題解答
### 什麼是 Aspose.PSD？
Aspose.PSD 是一個 Java 函式庫，允許開發人員以程式設計方式使用 PSD 和其他映像檔格式。
### 在哪裡可以找到有關 Aspose.PSD for Java 的更多文件？
您可以參考[文件](https://reference.aspose.com/psd/java/)取得詳細的 API 參考和範例。
### 我可以在購買前免費試用 Aspose.PSD 嗎？
是的，您可以下載一個[免費試用](https://releases.aspose.com/)評估圖書館的能力。
### 我如何獲得 Aspose.PSD 的臨時授權？
臨時許可證可以從[這裡](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD適合商業用途嗎？
是的，根據其授權條款，Aspose.PSD 可用於個人和商業專案。