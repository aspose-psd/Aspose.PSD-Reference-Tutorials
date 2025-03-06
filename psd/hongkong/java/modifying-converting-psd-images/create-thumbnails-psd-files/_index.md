---
title: 使用 Java 從 PSD 檔案建立縮圖
linktitle: 使用 Java 從 PSD 檔案建立縮圖
second_title: Aspose.PSD Java API
description: 了解如何使用 Java 和 Aspose.PSD 輕鬆地從 PSD 檔案建立縮圖。請遵循我們的無縫影像處理逐步指南。
weight: 24
url: /zh-hant/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 從 PSD 檔案建立縮圖

## 介紹
在圖形設計領域，使用 PSD（Photoshop 文件）檔案是很常見的。無論您是經驗豐富的開發人員、圖形設計師，還是只是想深入研究影像處理，從 PSD 檔案建立縮圖都可以節省您的時間並簡化您的工作流程。本教學將引導您完成使用 Aspose.PSD for Java 的整個過程。 Aspose.PSD 不僅是一個用於管理 Photoshop 檔案的強大庫，而且還使手頭上的任務直觀且易於管理。您準備好學習如何有效率地從 PSD 檔案建立縮圖了嗎？
## 先決條件
在我們深入了解縮圖創建的細節之前，讓我們先介紹一下開始時需要做什麼。
### Java開發環境
-  Java JDK：確保您的電腦上安裝了 Java 開發工具包 (JDK)。你可以下載它[這裡](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE：像 IntelliJ IDEA、Eclipse 或 NetBeans 這樣的整合開發環境 (IDE) 將使編碼變得更加容易。
### Aspose.PSD庫
- 您需要在專案中包含 Aspose.PSD 庫。你可以[在這裡下載最新版本](https://releases.aspose.com/psd/java/).
### Java基礎知識
- 熟悉 Java 基礎知識將幫助您更有效地瀏覽範例程式碼。諸如類、物件和循環之類的概念將被頻繁使用。
## 導入包
首先從 Aspose.PSD 庫導入必要的類別。此步驟至關重要，因為它使您能夠在程式碼中利用該庫的功能。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
滿足了先決條件後，讓我們進入主要活動吧！從 PSD 檔案建立縮圖涉及幾個簡單的步驟，我將為您詳細介紹。
## 第 1 步：設定您的環境
以下是如何啟動專案並準備縮圖生成。
1. 建立一個Java專案：
   - 開啟 IDE 並建立新的 Java 專案。
   - 將其命名為“PsdThumbnailGenerator”。
2. 包括Aspose.PSD庫：
   - 將 Aspose.PSD JAR 檔案加入到專案的建置路徑中。如果您使用 Maven，請將其包含在您的`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## 第 2 步：載入 PSD 文件
接下來，我們需要載入要從中建立縮圖的 PSD 檔案。 
1. 指定您的文件目錄：
   定義 PSD 檔案所在的目錄。
   ```java
   String dataDir = "Your Document Directory"; //替換為你的路徑
   ```
2. 載入 PSD 檔案：
   使用`PsdImage`類別來載入 PSD 檔案。
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
這裡，`sample.psd`是 PSD 檔案的名稱。根據您的檔案名稱進行調整。
## 第 3 步：迭代 PSD 資源
現在我們已經載入了 PSD 映像，下一步是檢查其資源。
1. 獲取資源數量：
   我們將循環存取 PSD 檔案中的所有資源。
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       //加工資源
   }
   ```
   
2. 識別縮圖資源：
   在循環內，檢查資源是否為縮圖。
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       //處理縮圖
   }
   ```
## 第 4 步：處理縮圖
一旦我們識別出縮圖資源，我們就需要對其進行相應的處理。
1. 檢索並檢查縮圖格式：
   如果資源確實是縮圖，則檢索它並檢查其格式。
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       //建立並儲存縮圖
   }
   ```
## 第 5 步：建立並儲存縮圖
這就是魔法發生的地方！我們將從縮圖資料創建一個新圖像並保存它。
1. 建立一個新映像：
   我們將使用縮圖資源的寬度和高度來建立新的點陣圖影像。
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. 將像素儲存在新圖像中：
   將縮圖資料傳輸到新建立的影像。
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. 儲存縮圖：
   最後，使用唯一的名稱將縮圖儲存到文件目錄中。
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## 結論
一旦將其分解為可管理的步驟，使用 Java 和 Aspose.PSD 從 PSD 檔案建立縮圖可以是一項簡單的任務。透過本教學課程，您現在可以輕鬆地從 PSD 檔案中提取縮圖，為您提供了一個增強工作流程的實用工具。那麼是什麼阻止了你呢？獲取一些 PSD 檔案並嘗試！
## 常見問題解答
### 什麼是 Aspose.PSD？
Aspose.PSD 是一個 Java 程式庫，可讓開發人員使用 Photoshop 文件，從而更輕鬆地以程式設計方式操作和管理 PSD 文件。
### 我可以免費使用 Aspose.PSD 嗎？
是的，Aspose 提供免費試用版，您可以在購買許可證之前使用它來測試庫。
### 我可以將縮圖儲存為哪些格式？
在此範例中，我們以 BMP 格式儲存縮圖，但 Aspose.PSD 也支援各種其他格式。
### 我需要安裝 Photoshop 才能使用 Aspose.PSD 嗎？
不，Aspose.PSD 獨立於 Photoshop 工作。
### 在哪裡可以找到有關 Aspose.PSD 的更多資訊？
您可以查看[Aspose.PSD 文檔](https://reference.aspose.com/psd/java/)了解更多詳細資訊、教學和資源。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
