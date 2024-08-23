---
title: 在 PSD 中新增等級調整圖層
linktitle: 在 PSD 中新增等級調整圖層
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 在 PSD 檔案中有效新增等級調整圖層。提高您的影像編輯技能。
type: docs
weight: 16
url: /zh-hant/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## 介紹
在影像編輯方面，管理層級可以使照片的活力和清晰度發生巨大變化。 Photoshop 工具庫中的一個方便工具是“色階調整圖層”，它可讓您調整影像的色調範圍和色彩平衡。在本指南中，我們將引導您了解如何使用 Aspose.PSD for Java 在 PSD 檔案中實作等級調整圖層。所以，拿起你的 Java IDE。
## 先決條件
在進入等級調整世界之前，您需要設定一些內容以確保平穩運行：
1.  Java 開發工具包 (JDK)：確保您的電腦上安裝了 JDK。如果沒有，您可以從[甲骨文網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)或者使用 OpenJDK。
2. Aspose.PSD for Java Library：要操作 PSD 文件，您需要下載 Aspose.PSD 函式庫。您可以從中取得最新版本[下載連結](https://releases.aspose.com/psd/java/)並確保您已將 JAR 包含在專案庫中。
3. Java 基礎知識：對 Java 程式設計有基本的了解將會有所幫助，因為我們將在本教程中深入研究程式碼片段。
4. IDE 設定：您可以使用任何您喜歡的 Java IDE（例如 IntelliJ IDEA、Eclipse 或 NetBeans）來編寫和執行程式碼。只需確保您已經設定了 Java 專案並新增了 Aspose.PSD 庫。

## 導入包
在開始編寫程式碼之前，我們需要從 Aspose.PSD 庫匯入必要的套件。您可以這樣做：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
透過匯入這些包，我們將可以存取載入、修改和保存 PSD 檔案所需的類別。

現在，讓我們將這個過程分解為易於理解的步驟。請跟隨我們一起載入 PSD 檔案、調整級別，然後儲存變更。 
## 第 1 步：設定檔案路徑
第一步是定義 PSD 檔案所在的位置以及我們要儲存修改後的輸出的位置。您可以自訂目錄路徑以滿足您的需求。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
在這裡，替換`"Your Document Directory"`與系統上儲存 PSD 檔案的實際路徑。這為我們接下來要做的一切奠定了基礎。
## 第 2 步：載入 PSD 文件
現在，讓我們使用以下命令來載入 PSD 文件`PsdImage`班級。此步驟至關重要，因為它允許我們存取和操作圖層。
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
當你打電話時`Image.load()`，它將讀取 PSD 檔案並建立一個實例`PsdImage`您可以使用。
## 第 3 步：迭代各層
由於我們想要調整等級調整圖層，因此我們需要循環遍歷 PSD 檔案中的每個圖層。這有助於我們找到要修改的特定層。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        //進一步的操縱將在這裡...
    }
}
```
在這個循環中，`instanceof LevelsLayer`檢查目前圖層是否為色階調整圖層。如果是，我們可以繼續調整它的屬性。
## 步驟 4：調整電平通道設定
一旦我們確定了正確的層，我們就可以修改其輸入和輸出等級。這就是魔法發生的地方！調整不同的參數以查看它們如何影響影像。
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
以下是每個參數的作用：
- 輸入中間色調等級：調整中間色調。
- 輸入陰影等級：調整影像的較暗區域。
- 輸入高光等級：改變影像的明亮區域。
- 輸出陰影等級：設定暗陰影的顯示方式。
- 輸出高光等級：設定高光的顯示方式。
請隨意嘗試不同的數值！
## 第5步：儲存修改後的PSD文件
現在我們已經完成了調整，是時候儲存修改過的 PSD 檔案了。此步驟對於確保應用和儲存您的變更至關重要。
```java
im.save(psdPathAfterChange);
```
現在您可以在指定的位置找到調整後的 PSD 文件`psdPathAfterChange`. 
## 結論
您剛剛學習如何使用 Aspose.PSD for Java 將等級調整圖層新增到 PSD 檔案！遵循本指南，您可以輕鬆調整影像的色調質量，為更生動、更具視覺吸引力的輸出鋪平道路。請記住，熟能生巧，因此請隨意調整並探索不同的 PSD 檔案以查看更改的效果。
## 常見問題解答
### 什麼是水平調整圖層？
等級調整圖層可讓您校正影像中的色調範圍，平衡陰影、中間色調和高光。
### 我可以在不購買的情況下使用 Aspose.PSD 嗎？
是的！ Aspose 提供免費試用，以便在購買前測試該庫。
### 在哪裡可以找到 Aspose.PSD 的文檔？
你可以找到文檔[這裡](https://reference.aspose.com/psd/java/).
### Aspose 產品有社區支持嗎？
絕對地！您可以在以下位置提出問題並獲得支持[Aspose論壇](https://forum.aspose.com/c/psd/34).
### 我如何獲得 Aspose.PSD 的臨時授權？
您可以申請臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).