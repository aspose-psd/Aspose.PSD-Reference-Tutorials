---
title: 使用 Aspose.PSD Java 展平 PSD 檔案中的圖層
linktitle: 使用 Aspose.PSD Java 展平 PSD 檔案中的圖層
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD for Java 輕鬆展平和合併 PSD 檔案中的圖層。請按照此逐步指南來簡化 PSD 檔案管理。
type: docs
weight: 13
url: /zh-hant/java/psd-layer-management-effects/flatten-layers-psd-files/
---
## 介紹

您是否曾經發現自己正在使用 Photoshop 檔案並希望有一種更簡單的方法來管理這些複雜的圖層？嗯，你很幸運！今天，我們將深入了解 Aspose.PSD for Java 的世界，這是一個功能強大的工具，可以讓以程式設計方式處理 PSD 檔案變得輕而易舉。我們將探索的便利功能之一是展平圖層。無論您想要拼合整個影像或選擇性地合併特定圖層，Aspose.PSD for Java 都能滿足您的需求。本教學將逐步引導您完成整個過程，確保您準備好自信地處理 PSD 檔案。

## 先決條件

在我們進入程式碼之前，讓我們確保您擁有所需的一切：

1. Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK 8 或更高版本。
2.  Aspose.PSD for Java：下載 Aspose.PSD 庫並將其新增至您的專案。你可以找到它[這裡](https://releases.aspose.com/psd/java/).
3. 整合開發環境 (IDE)：IntelliJ IDEA 或 Eclipse 等 IDE 將使您的編碼體驗更加流暢。
4. Java 基礎：雖然本教學適合初學者，但一些 Java 基礎知識將幫助您更輕鬆地學習。
5. 範例 PSD 檔案：準備一個 PSD 檔案以供試驗。我們將使用多層來示範展平過程。

現在我們已經掌握了要點，讓我們開始有趣的部分——使用程式碼！

## 導入包

首先，您需要將必要的套件匯入到您的 Java 專案中。這些套件將允許您使用 Aspose.PSD for Java 處理 PSD 檔案。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

這些導入將使我們能夠載入 PSD 檔案、操作圖層並儲存變更。現在，讓我們將扁平化圖層的流程分解為可管理的步驟。

## 第 1 步：展平整個 PSD 影像

第一個任務是展平整個 PSD 影像。當您想要將所有圖層合併為單一圖層時，這非常有用，使影像更易於管理和匯出。

### 1.1 載入PSD文件

首先，我們將 PSD 檔案載入到我們的程式中。該文件應放置在您的專案目錄中，我們稱之為`Your Document Directory`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

此程式碼片段載入名為的 PSD 文件`ThreeRegularLayersSemiTransparent.psd`從您指定的目錄。

### 1.2 扁平化影像

接下來，我們將展平整個影像。拼合將所有可見圖層合併為單一背景圖層。

```java
im.flattenImage();
```

透過這一行，PSD 檔案中的所有圖層都將合併為一個。

### 1.3 儲存拼合後的影像

最後，我們將拼合後的圖像儲存到一個新檔案中。

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

這會將拼合的 PSD 檔案保存在新名稱下`ThreeRegularLayersSemiTransparentFlattened.psd`。恭喜！您剛剛使用 Aspose.PSD for Java 展平了您的第一個 PSD 影像。

## 第 2 步：合併特定圖層

有時，您可能不想展平整個影像，而是只合併某些圖層。讓我們看看如何實現這一目標。

### 2.1 再次載入PSD文件

由於我們正在執行不同的操作，因此首先再次載入 PSD 檔案。

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

這將載入相同的 PSD 文件，為特定於圖層的操作做好準備。

### 2.2 識別和選擇層

若要合併特定圖層，首先，請識別並選擇要合併的圖層。

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

在這裡，我們選擇 PSD 檔案的第一、第二和第三層。這些層儲存在一個陣列中，您可以透過它們的索引存取它們。

### 2.3 合併圖層

現在，讓我們合併選定的圖層。我們將從合併底層和中間層開始，然後將結果與頂層合併。

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

此代碼依序合併各層，從而形成單一組合層。

### 2.4 用合併層取代現有層

合併後，您需要用新合併的圖層取代影像中現有的圖層。

```java
img.setLayers(new Layer[]{layer2});
```

此步驟可確保影像現在僅包含合併的圖層。

### 2.5 儲存更新的 PSD 文件

最後，儲存更新後的 PSD 檔案和合併的圖層。

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

這會將帶有合併圖層的 PSD 保存在新名稱下，從而使您可以保持原始檔案完整。

## 結論

使用 PSD 檔案中的圖層通常感覺就像在迷宮中導航，但使用 Aspose.PSD for Java，就像手中握有一張地圖。無論您需要拼合整個影像還是仔細合併選定的圖層，Aspose.PSD 都能簡化流程，將一項艱鉅的任務變成簡單的操作。透過學習本教程，您現在應該可以輕鬆地使用 Java 處理 PSD 檔案中的圖層操作。那麼為什麼不在自己的專案中嘗試一下，看看您節省了多少時間和精力呢？

## 常見問題解答

### 我可以撤銷 Aspose.PSD 中圖層的展平嗎？  
不，一旦使用 Aspose.PSD 拼裝圖層，此操作就不可逆轉。保留原始文件的備份始終是一個好習慣。

### 是否可以僅展平可見層？  
是的，您可以根據圖層的可見性來控制要展平的圖層。使用前確保只有要展平的圖層可見`flattenImage`方法。

### 拼合圖層會減少檔案大小嗎？  
拼合圖層可以減少檔案大小，尤其是在有許多複雜圖層的情況下。然而，確切的減少量取決於各層的含量。

### 我可以合併不同混合模式的圖層嗎？  
是的，您可以使用 Aspose.PSD 合併具有不同混合模式的圖層，並且產生的圖層將保持合併圖層的外觀。

### 如果我嘗試合併不相鄰的圖層會發生什麼情況？  
Aspose.PSD 可讓您合併任何圖層，無論其在圖層堆疊中的順序為何。合併過程將依指定組合所選圖層。