---
title: 使用 Java 在 PSD 檔案中套用調整圖層
linktitle: 使用 Java 在 PSD 檔案中套用調整圖層
second_title: Aspose.PSD Java API
description: 在這份開發人員的完整逐步指南中，學習如何使用 Aspose.PSD for Java 在 PSD 檔案中套用調整圖層。
weight: 15
url: /zh-hant/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 在 PSD 檔案中套用調整圖層

## 介紹
您是一位希望增強 PSD 檔案中儲存的映像的 Java 開發人員嗎？如果是這樣，那麼您來對地方了！在本文中，我們將探討如何使用 Java 的 Aspose.PSD 函式庫在 PSD 檔案中套用調整圖層。無論您是在處理個人專案還是專業應用程序，了解如何操作 PSD 檔案都可以顯著提升軟體的功能。 

## 先決條件
在我們進入程式碼並開始應用這些調整圖層之前，您需要滿足一些先決條件：
1. Java 開發工具包 (JDK)：確保您的電腦上安裝了 JDK。您可以從以下位置下載：[甲骨文網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD 函式庫：如果您還沒有下載，則需要下載 Java 的 Aspose.PSD 函式庫。你可以找到它[這裡](https://releases.aspose.com/psd/java/).
3. 開發環境：設定一個 Java 整合開發環境 (IDE)，例如 IntelliJ IDEA 或 Eclipse，您將在其中編寫和執行程式碼。
4. 對 Java 的基本熟悉：對 Java 程式設計的一般了解將幫助您順利進行。
5. PSD 檔案：手邊有幾個 PSD 檔案用於測試目的。您可以使用 Adobe Photoshop 建立一些檔案或從 Internet 下載範例檔案。
## 導入包
在開始編碼之前，我們先澄清一下需要導入哪些套件。 Aspose.PSD 允許我們以多種方式處理 Photoshop 文件，因此讓我們取得必要的類別來處理 PSD 影像和調整圖層。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
現在我們已經有了我們的包，讓我們逐步分解這些範例！
## 第 1 步：載入 PSD 文件
我們旅程的第一步是載入 PSD 檔案。這是我們將用來套用調整圖層的檔案。
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
在此程式碼片段中，我們定義 PSD 檔案所在的目錄並載入我們要操作的特定檔案。確保更換`"Your Document Directory"`與您電腦上 PSD 檔案的實際路徑。
## 第 2 步：迭代層
現在我們已經加載了 PSD 文件，我們將要迭代其圖層以找到我們的調整圖層。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
在此步驟中，我們循環遍歷 PSD 檔案中的每一層，以識別屬於`AdjustmentLayer`類型。如果我們找到一個，我們將其與基礎層合併，基礎層通常是第一層（`im.getLayers()[0]`）。此合併過程有效地將調整應用於我們的影像。 
## 步驟3：儲存修改後的PSD文件
修改圖層後，儲存所做的變更至關重要。讓我們在下一步中執行此操作。
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
在這裡，我們指定修改後的 PSD 檔案的匯出路徑並調用`save()`將我們的更改寫入磁碟的方法。
## 第四步：色階調整圖層
讓我們對不同類型的調整圖層重複這個過程：色階調整圖層。 
### 載入等級調整圖層 PSD
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
和之前一樣，我們載入包含色階調整圖層的 PSD 檔案。 
### 迭代級別層
接下來，我們將再次循環遍歷各層，就像之前所做的那樣，但現在我們正在處理另一個 PSD 檔案。
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
此程式碼的行為與先前的迭代類似；它會在目前 PSD 檔案中搜尋調整圖層，使我們能夠套用任何可用的調整。
## 儲存等級調整圖層 PSD
最後，我們將在應用調整後儲存這個新檔案。
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
現在，我們已經成功處理了色階調整圖層！
## 結論
恭喜！您剛剛學習如何使用 Java 和 Aspose.PSD 函式庫在 PSD 檔案中套用調整圖層。無論您是調整顏色還是調整級別，您現在都具備以程式設計方式操作 PSD 檔案的基本技能。
使用 Aspose.PSD 可以顯著簡化影像編輯的工作流程，從而以傳統工具無法實現的方式實現自動化和自訂。不要猶豫，進一步探索該庫並嘗試不同類型的圖層，看看有哪些創造性的可能性。
## 常見問題解答
### 什麼是 Aspose.PSD 函式庫？
Aspose.PSD 是一個函式庫，可讓開發人員在 Java 應用程式中載入、操作和保存 Photoshop PSD 檔案。
### 我可以免費使用 Aspose.PSD 嗎？
是的！ Aspose 為您提供免費試用來探索他們的庫。您可以報名[這裡](https://releases.aspose.com/).
### 我需要安裝 Photoshop 才能使用 Aspose.PSD 嗎？
不，您不需要 Photoshop。 Aspose.PSD 獨立工作，以程式方式操作 PSD 檔案。
### 在哪裡可以找到 Aspose.PSD 的文檔？
您可以造訪文件頁面[這裡](https://reference.aspose.com/psd/java/)探索特性、類別和方法。
### 我如何獲得 Aspose 產品的支援？
您可以透過以下方式獲得支持[Aspose論壇](https://forum.aspose.com/c/psd/34)您可以在這裡提出問題並找到解決方案。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
