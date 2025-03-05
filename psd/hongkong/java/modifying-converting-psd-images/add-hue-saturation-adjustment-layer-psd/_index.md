---
title: 加入色相飽和度調整圖層到PSD
linktitle: 加入色相飽和度調整圖層到PSD
second_title: Aspose.PSD Java API
description: 在這個全面的逐步教學中，了解如何使用 Aspose.PSD for Java 將色調飽和度調整圖層新增至 PSD。增強您的圖形設計工作流程。
type: docs
weight: 14
url: /zh-hant/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## 介紹
在圖形設計中，色彩處理起著至關重要的作用，具體來說，調整色調、飽和度和亮度可以極大地改變任何影像的情緒和品質。實現此目的的有效方法是使用 Photoshop 中的調整圖層（PSD 檔案）。如果您希望使用 Java 以程式設計方式增強 PSD 文件，Aspose.PSD 庫可以為您提供協助！本教學將引導您完成為 PSD 檔案新增色相飽和度調整圖層的步驟，讓您的工作流程更有效率。
在本指南中，我們將涵蓋從匯入必要的套件到程式碼範例的具體細節的所有內容。
## 先決條件
在我們開始編寫程式碼之前，請確保您已準備好以下內容：
1.  Java 開發工具包 (JDK)：確保您的電腦上安裝了 JDK 8 或更高版本。您可以從[Java SE 開發工具包下載](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Aspose.PSD for Java Library：您需要擁有 Aspose.PSD 函式庫，您可以[在這裡下載](https://releases.aspose.com/psd/java/). 
3. IDE：適合 Java 開發的整合開發環境 (IDE)，例如 IntelliJ IDEA 或 Eclipse。
4. 基本 Java 知識：熟悉 Java 程式設計是一個優勢，但不用擔心；我們將逐步引導您完成程式碼。
現在我們已經解決了先決條件，讓我們繼續有趣的部分——編碼！
## 導入包
要開始使用 Aspose.PSD 庫，第一步是匯入必要的類別。以下是在 Java 檔案中執行此操作的方法：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
確保您已將適當的庫新增至您的專案中，以便這些匯入能夠無縫運作。
## 第 1 步：設定您的文件目錄
每個專案都需要一個起點，我們也不例外。您需要指定儲存 PSD 檔案的目錄。這對於正確加載和保存圖像至關重要。
```java
String dataDir = "Your Document Directory"; //將此路徑更新為您的實際目錄
```
## 第 2 步：載入現有 PSD 文件
要操作現有的 PSD 文件，我們首先需要將其載入到我們的程式中。您可以按照以下方法執行此操作：
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
在此程式碼中，更新`"HueSaturationAdjustmentLayer.psd"`到您要編輯的現有 PSD 檔案的名稱。
## 第三步：編輯色相/飽和度圖層
接下來，我們將循環遍歷載入的 PSD 影像的圖層，以尋找並編輯任何現有的色相/飽和度圖層。此步驟涉及修改色調、飽和度和亮度值。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
在這個例子中：
- 我們將色調調整為 -25，飽和度調整為 -12，亮度調整為 +67。
- 這`getRange(2)`方法允許我們根據需要調整特定的顏色範圍。
## 步驟4：儲存修改後的PSD文件
進行調整後，下一步是儲存文件。這是我們流程的重要組成部分，確保我們所做的更改不會遺失。
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## 步驟5：新增新的色相/飽和度圖層
接下來，您可能想要將新的色相/飽和度調整圖層新增到另一個 PSD 檔案中。只需遵循您之前使用的相同方法，但使用不同的 PSD 檔案。
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## 步驟 6：為新圖層設定新的色相/飽和度值
現在您已經建立了這個新圖層，像以前一樣套用所需的色調、飽和度和亮度設定。
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## 第 7 步：儲存更新的 PSD 文件
最後，儲存新增了色相/飽和度圖層的 PSD 文件，以便您可以看到所做的變更。
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
恭喜！您已經使用 Aspose.PSD for Java 成功操作了 PSD 檔案。現在，您可以嘗試不同的圖像和更深層的更改，使您的圖形設計專案變得栩栩如生。
## 結論
以程式方式處理圖形開啟了一個充滿可能性的世界。使用 Aspose.PSD for Java 添加和修改色相飽和度調整圖層提供了靈活性和效率，可以簡化您的設計工作流程。無論您是要增強專案的照片還是創建令人驚嘆的視覺內容，掌握這些工具都可以大大提高您的輸出。
歡迎深入探索 Aspose.PSD 的更多功能[文件](https://reference.aspose.com/psd/java/)或考慮抓住一個[臨時執照](https://purchase.aspose.com/temporary-license/)測試庫的全部功能。
## 常見問題解答
### 什麼是色相飽和度調整圖層？
色相飽和度調整圖層可讓您修改影像的色彩屬性，而無需永久變更原始像素。
### 我需要安裝 Photoshop 才能使用 Aspose.PSD 嗎？
不，Aspose.PSD 是一個獨立於 Photoshop 運作的獨立函式庫。
### 我可以使用Aspose.PSD進行批次嗎？
是的，您可以使用 Aspose.PSD 自動執行和批次處理多個 PSD 檔案。
### Aspose.PSD 是免費的嗎？
Aspose.PSD提供免費試用，但長期使用需要授權。您可以查看定價[這裡](https://purchase.aspose.com/buy).