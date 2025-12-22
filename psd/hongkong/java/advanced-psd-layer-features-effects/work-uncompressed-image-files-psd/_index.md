---
date: 2025-12-22
description: 學習如何使用 Aspose.PSD Java 函式庫匯出未壓縮的 PSD。此步驟指南說明在 Java 中處理 PSD 中未壓縮影像檔案的方法。
linktitle: Work with Uncompressed Image Files in PSD using Java
second_title: Aspose.PSD Java API
title: Aspose PSD Java：在 PSD 中處理未壓縮的圖像檔案
url: /zh-hant/java/advanced-psd-layer-features-effects/work-uncompressed-image-files-psd/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 處理未壓縮的 PSD 圖像檔案

## 介紹
當在 Java 中處理 Photoshop 文件（PSD）時，**aspose psd java** 函式庫讓我們必須了解如何有效地操作與儲存這些豐富的圖像檔案。在本教學中，我們將深入探討 Aspose.PSD，這是一套簡化 PSD 檔案管理的強大 API，亦支援未壓縮圖像的處理。無論您是想為應用程式加入豐富圖形的開發者，或是僅想在 Java 中輕鬆處理 PSD 檔案，本指南都會一步步帶領您完成。準備好了嗎？讓我們馬上開始吧！

## 快速回答
- **如何在不壓縮的情況下匯出 PSD？** 使用 `CompressionMethod.Raw` 在 `PsdOptions` 中儲存檔案時。  
- **哪個函式庫支援在 Java 中處理未壓縮的 PSD？** **aspose psd java** 函式庫提供完整支援。  
- **生產環境需要授權嗎？** 是的，生產部署需要商業授權。  
- **需要哪個 Java 版本？** JDK 8 或以上即可。  
- **儲存後可以操作圖層嗎？** 當然可以 – 重新載入已儲存的檔案，並使用 `Graphics` 物件繪製或編輯圖層。

## 使用 aspose psd java 匯出未壓縮的 PSD
在不使用任何壓縮方式儲存 PSD，可保留原始像素資料，這對於高保真編輯流程、檔案保存或需要像素完美結果的後續處理至關重要。以下步驟說明如何使用 **aspose psd java** API 完成此操作。

## 前置條件
在動手寫程式碼之前，我們需要先確認以下前置條件。別擔心，這些都相當簡單！

### Java Development Kit (JDK)
- 確保您的系統已安裝 JDK 8 或以上版本。若尚未安裝，請前往 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載最新版本。

### Integrated Development Environment (IDE)
- 使用 IntelliJ IDEA、Eclipse 或 NetBeans 等好用的 IDE 能讓開發更順暢。若尚未安裝，請先設定好一個環境。

### Aspose.PSD for Java Library
- 下載 Aspose.PSD for Java 函式庫。您可以在 [here](https://releases.aspose.com/psd/java/) 取得最新發行版。

### Basic Knowledge of Java 
- 需要具備基本的 Java 程式設計與物件導向概念，以便順利跟隨教學內容。

### A PSD File
- 準備一個測試用的 PSD 檔案。您可以在 Photoshop 中自行建立，或從線上下載免費樣本。

現在一切就緒，讓我們深入程式碼吧！

## 匯入套件
要開始，我們需要匯入程式碼所需的套件。以下是您需要的匯入清單：
```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
這些匯入會將必要的類別與方法帶入專案，讓我們能順暢地操作 PSD 檔案。接下來，我們將把流程拆解成易於管理的步驟。

## 步驟 1：設定檔案目錄
首先，需要指定 PSD 檔案所在位置以及輸出檔案的儲存路徑。以下範例程式會建立一個變數來保存目錄路徑。
```java
String dataDir = "Your Document Directory";
```
將 `"Your Document Directory"` 替換為實際存放 PSD 檔案（`layers.psd`）的路徑。如此一來，程式才能正確找到檔案。

## 步驟 2：載入 PSD 檔案
現在，使用 `Image.load()` 方法載入 PSD 檔案，並將其轉型為 `PsdImage`。
```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```
此行呼叫 `Image` 類別的 `load` 方法，將 PSD 檔案載入記憶體。透過轉型為 `PsdImage`，我們告訴 Java 這是一個具備 PSD 專屬功能的影像。

## 步驟 3：設定儲存選項
接著，我們需要為儲存檔案設定選項，特別是指定輸出為未壓縮。
```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```
`PsdOptions` 類別允許我們為儲存 PSD 檔案指定各種參數。將 `setCompressionMethod` 設為 `CompressionMethod.Raw`，即可確保儲存的檔案不會被壓縮，保持高品質。

## 步驟 4：儲存未壓縮的 PSD 檔案
現在是時候將新設定好的 PSD 影像儲存下來。
```java
psdImage.save(dataDir + "uncompressed_out.psd", saveOptions);
```
此行對 `PsdImage` 實例（`psdImage`）執行儲存功能，將檔案以 `uncompressed_out.psd` 名稱儲存在先前指定的目錄，並套用先前設定的選項。

## 步驟 5：重新開啟新建立的影像
儲存完成後，重新載入輸出影像以驗證一切如預期運作。
```java
PsdImage img = (PsdImage) Image.load(dataDir + "uncompressed_out.psd");
```
再次呼叫 `load`，即可建立對應於已儲存檔案的 `PsdImage` 新實例。若您想在儲存後繼續操作或顯示影像，這一步相當重要。

## 步驟 6：繪製或操作影像
最後，您可能想在新開啟的影像上進行繪製或其他操作。
```java
Graphics graphics = new Graphics(img);
```
此處我們初始化一個 `Graphics` 物件，讓您能對 `img` 執行各種圖形操作。您可以繪製形狀、加入文字，甚至修改圖層！

## 常見問題與解決方案
- **FileNotFoundException** – 請再次確認 `dataDir` 路徑，並確保 PSD 檔名完全相符。  
- **UnsupportedCompressionException** – 請確保使用支援 `CompressionMethod.Raw` 的最新 Aspose.PSD 版本。  
- **License Not Found** – 生產環境使用時，請在呼叫任何 API 方法前載入 Aspose 授權，以避免評估水印。

## 常見問答

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java 是一套讓開發者能以程式方式操作 Photoshop PSD 檔案的 Java 函式庫。

**Q: Can I manipulate layers in a PSD file using Aspose.PSD?**  
A: 可以！Aspose.PSD 允許您存取與操作圖層，輕鬆執行複雜的處理。

**Q: Is Aspose.PSD free to use?**  
A: 提供免費試用版，但若需大量使用或取得進階功能，仍需購買授權。

**Q: How can I contact support if I encounter issues?**  
A: 您可透過 [Aspose support forum](https://forum.aspose.com/c/psd/34) 尋求協助。

**Q: Does Aspose.PSD support saving in formats other than PSD?**  
A: 支援。Aspose.PSD 可依需求儲存為 PNG、JPEG 等多種格式。

**Q: Can I export a PSD without compression using this library?**  
A: 當然可以 – 如教學所示，於 `PsdOptions` 中設定 `CompressionMethod.Raw` 即可。

## 結論
恭喜！您已學會如何使用 Java 及 **aspose psd java** 函式庫處理未壓縮的 PSD 圖像檔案。此強大 API 讓您能輕鬆載入、操作與以不同格式儲存 PSD，無論是載入、編輯或保存都相當便利。現在就試試看吧！變更屬性、玩弄圖形，看看能創造出什麼令人驚豔的作品。

別忘了查閱 [documentation](https://reference.aspose.com/psd/java/) 以取得更多進階功能與設定說明。若想直接體驗，可於 [here](https://releases.aspose.com/psd/java/) 下載函式庫或開始免費試用。如有任何問題，歡迎前往 [support forum](https://forum.aspose.com/c/psd/34) 向社群尋求協助。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新:** 2025-12-22  
**測試環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose