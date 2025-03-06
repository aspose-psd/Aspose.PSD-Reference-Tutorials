---
title: 支援 PSD 中的長度記錄資料屬性 - Java
linktitle: 支援 PSD 中的長度記錄資料屬性 - Java
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD 在 Java 中操作具有長度記錄資料屬性的 PSD 檔案。請按照此逐步指南了解所有詳細資訊。
weight: 14
url: /zh-hant/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 支援 PSD 中的長度記錄資料屬性 - Java

## 介紹
您是否曾經使用過 Photoshop 檔案並希望以程式設計方式操作圖層或形狀？如果是這樣，您已經偶然發現了 Aspose.PSD for Java 程式庫的魅力。這個強大的工具允許開發人員透過 Java 程式碼無縫地互動和修改 PSD 檔案。在今天的文章中，我們將深入探討如何使用此程式庫支援 PSD 檔案中的長度記錄資料屬性。 
無論您是經驗豐富的 Java 開發人員還是剛起步，本指南都將逐步引導您了解您需要了解的所有內容。最後，您將能夠開啟 PSD 檔案、修改其向量形狀屬性並儲存變更 — 所有這些都無需離開舒適的 Java 環境。讓我們捲起袖子，跳起來吧！
## 先決條件
在我們開始之前，您需要準備一些東西。確保一切就位可以讓過程更加順利，沒有人喜歡最後一刻的爭吵！這是您需要的：
1.  Java 開發工具包 (JDK)：確保您的電腦上安裝了 JDK。您可以從以下位置下載：[甲骨文網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)或使用套件管理器。
2.  Aspose.PSD for Java 程式庫：您需要下載 Aspose.PSD for Java 程式庫並將其包含在您的專案中。從[Aspose 發佈頁面](https://releases.aspose.com/psd/java/).
3. IDE：使用整合開發環境 (IDE)，例如 IntelliJ IDEA、Eclipse 或您選擇的任何 Java IDE，以便更好地處理程式碼。
4. PSD 檔案：對於本教學課程，您需要一個 PSD 檔案來處理。您可以在 Adobe Photoshop 中建立一個或下載範例 PSD。
5. 基本 Java 知識：熟悉 Java 語法將幫助您輕鬆掌握。
## 導入包
現在您已經設定了所有先決條件，下一步是匯入必要的套件。此步驟對於存取我們將使用的類別和方法至關重要。以下是如何在 Java 專案中匯入所需套件的範例：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```
透過這些匯入，您就可以開始操作 PSD 檔案了！

## 第 1 步：設定來源目錄和輸出目錄
在載入任何檔案之前，讓我們指定輸入 PSD 檔案的來源以及修改後的檔案的儲存位置。根據本機機器調整目錄路徑。
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```
## 第 2 步：載入 PSD 文件
是時候載入 PSD 檔案了！為此，我們將使用`Image.load`來自 Aspose.PSD 庫的方法。此方法允許我們開啟 PSD 檔案並存取其圖層和資源。
```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```
這就像打開一本書 - 您將能夠瀏覽其頁面（圖層和資源）。
## 步驟3：在層中找到Vsms資源
接下來，我們需要在 PSD 檔案中找到特定的 VsmsResource。這些資源保存向量形狀圖層的資料。這就是魔法發生的地方！在此程式碼片段中，我們循環遍歷圖層的資源來尋找該資源。
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```
就像尋寶一樣，您正在層層搜尋以找到有價值的向量資料！
## 步驟4：訪問長度記錄
一旦我們有了 VsmsResource，我們就可以提取 LengthRecord 物件。每個 LengthRecord 代表向量形狀內的一條路徑。在這裡，我們訪問三個 LengthRecord 來操作它們的屬性。
```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```
這就像是選擇要修飾一幅畫的哪些部分！
## 步驟5：修改路徑操作屬性
現在到了有趣的部分——修改路徑屬性！在這裡，setPathOperations 方法允許更改形狀之間的互動方式。我們可以設定排除重疊區域或從背面減去正面形狀等操作。
```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```
將其想像為調整蛋糕的層數 - 根據您切片的方式，每一層的相互作用都不同！
## 步驟6：儲存修改後的PSD文件
進行所需的變更後，下一步是儲存修改後的 PSD 檔案。這就是你所有的努力得到回報的地方。 
```java
psdImage.save(outPsdFilePath);
```
您的傑作現已包裝整齊，供全世界觀看！
## 第 7 步：清理資源
最後，處理您使用過的物件以釋放記憶體和資源至關重要。
```java
psdImage.dispose();
```
可以把它想像成在藝術項目結束後清理你的工作空間——確保一切都乾淨整潔！
## 結論
給你了！您剛剛完成了有關使用 Aspose.PSD for Java 支援 PSD 檔案中的長度記錄資料屬性的綜合教程。從載入檔案到修改形狀屬性和保存最終產品，每一步都揭示了該庫的強大功能。無論您是從事創意專案還是自動化圖形資源，Aspose.PSD 都開啟了一個充滿可能性的全新世界。準備好開始了嗎？深入研究您的 PSD 檔案並釋放您的創造力！
## 常見問題解答
### 什麼是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一個函式庫，允許開發人員使用 Java 以程式方式操作和使用 Photoshop PSD 檔案。
### 我可以在免費項目中使用 Aspose.PSD 嗎？
是的，您可以使用 Aspose 網站上提供的試用版免費試用庫。
### 我可以對 PSD 檔案進行哪些類型的修改？
您可以在 PSD 檔案中操縱圖層、形狀、文字、路徑操作等。
### Aspose.PSD 與其他程式語言相容嗎？
是的，Aspose 為不同的程式語言提供了各種函式庫，包括 .NET 和 Python。
### 在哪裡可以找到 Aspose.PSD 的文檔？
您可以存取完整的文檔[這裡](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
