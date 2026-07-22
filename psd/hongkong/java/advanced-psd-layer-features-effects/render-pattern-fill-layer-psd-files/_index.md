---
date: 2026-07-22
description: 在本全面逐步教學中，學習如何使用 Java 與 Aspose.PSD 建立圖案填充 PSD 檔案，並在 PSD 中渲染圖案填充圖層。
keywords:
- create pattern fill psd
- generate tiled texture psd
- Aspose.PSD Java
lastmod: 2026-07-22
linktitle: 使用 Java 在 PSD 檔案中渲染圖案填充圖層
og_description: 學習如何使用 Java 與 Aspose.PSD 建立圖案填充 PSD 檔案。本指南將帶領您載入 PSD、設定 FillLayer
  圖案，並儲存結果以進行自動紋理生成。
og_image_alt: 'Developer guide: Create pattern fill PSD files using Aspose.PSD Java
  API'
og_title: 使用 Java 建立圖案填充 PSD 檔案 – Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to create pattern fill PSD files and render pattern fill
    layers in PSD using Java with Aspose.PSD in this comprehensive step-by-step tutorial.
  headline: Create pattern fill PSD Files Using Java
  type: TechArticle
- description: Learn how to create pattern fill PSD files and render pattern fill
    layers in PSD using Java with Aspose.PSD in this comprehensive step-by-step tutorial.
  name: Create pattern fill PSD Files Using Java
  steps:
  - name: Define Your Source and Output Directories
    text: To kick things off, you need to establish where your source PSD file is
      located and where you want to save the output file. Replace `"Your Source Directory"`
      and `"Your Document Directory"` with actual paths on your machine.
  - name: Load the PSD File
    text: Load your PSD into memory so you can start editing it. The `PsdImage` class
      represents a Photoshop document and provides access to its layers and resources.
      Casting the loaded image to `PsdImage` gives you access to PSD‑specific properties
      and methods.
  - name: Loop Through Layers
    text: Identify the fill layers that need pattern configuration. The `FillLayer`
      class models a Photoshop fill layer that can hold solid colors, gradients, or
      patterns. The `instanceof` check ensures we only work with `FillLayer` objects.
  - name: Configure Fill Layer Settings
    text: Adjust offsets, scale, and other visual parameters for the selected fill
      layer. `IPatternFillSettings` holds all pattern‑related options such as offset,
      scale, and the actual pattern data. Each property influences how the pattern
      will be rendered. For example, adjusting the offsets shifts the patter
  - name: Define Pattern Data
    text: Now it’s time to configure the actual pattern itself by defining the colors
      that will comprise your fill pattern. `PatternFillSettings` lets you supply
      a list of `Color` objects that define the tiled pattern. Feel free to replace
      any of the colors with your own choices to create a unique visual styl
  - name: Set Pattern Dimensions and Name
    text: Further customizing the fill layer involves defining its width and height,
      as well as assigning it a name and a unique ID. `PatternFillSettings.setPatternSize(int
      width, int height)` controls the tile size, while `setName` and `setId` help
      you identify the pattern later on. The dimensions control th
  - name: Update the Fill Layer
    text: After configuring all the desired properties, you need to push the changes
      back into the layer. Calling `update()` applies all modifications to the underlying
      PSD structure.
  - name: Save the Changes
    text: Finally, save the updated PSD file using the `save()` method. `PsdImage.save(String
      path)` persists the modified document to disk. Your new file now contains the
      customized pattern fill layer.
  - name: Dispose of the Image Object
    text: To free up resources, it’s a good practice to dispose of the image once
      you’re done. `PsdImage.dispose()` releases native memory and file handles, which
      is essential when processing large batches.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to work with
      Photoshop PSD files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can access a [free trial](https://releases.aspose.com/) to explore
      its functionalities.
    question: Can I try Aspose.PSD for free?
  - answer: You can purchase a license from the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: Where can I buy Aspose.PSD?
  - answer: Absolutely! You can get help from the [Aspose support forum](https://forum.aspose.com/c/psd/34).
    question: Is there any support available for Aspose.PSD?
  - answer: Check the documentation for troubleshooting tips or seek help in the [support
      forum](https://forum.aspose.com/c/psd/34).
    question: What should I do if I encounter issues when using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create pattern fill psd
- Aspose.PSD
- Java PSD manipulation
- pattern fill layer
- automated graphics
title: 使用 Java 建立圖案填充 PSD 檔案
url: /zh-hant/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Java 建立圖案填充 PSD 檔案

## 簡介
如果您希望以程式方式 **create pattern fill PSD** 檔案，您已來對地方。使用 Aspose.PSD for Java，您可以自動化在 Photoshop 文件中建立、操作與渲染圖案填充圖層，為您節省大量手動時間。在本教學中，我們將示範如何載入 PSD、定位填充圖層、設定圖案，最後儲存更新後的檔案。完成後，您將能熟練使用 Java **create pattern fill PSD** 檔案，並可在不同專案中重複使用或整合至自動化流程。

## 快速解答
- **需要的函式庫是什麼？** Aspose.PSD for Java  
- **我可以在任何作業系統上執行嗎？** 是的，任何支援 Java 8+ 的平台皆可  
- **測試是否需要授權？** 免費試用版足以用於開發  
- **實作需要多長時間？** 基本範例大約 10‑15 分鐘  
- **程式碼是否相容於 Maven/Gradle？** 當然，只要加入 Aspose.PSD 相依性即可  

## 什麼是「create pattern fill PSD」？
建立 pattern fill PSD 意指以程式方式定義一個平鋪的顏色圖案，並將其套用至 Photoshop 檔案中的填充圖層。當您需要可重複使用的紋理、品牌元素或即時產生的動態圖形時，此技術非常實用。

## 為何使用 Aspose.PSD 來建立 pattern fill PSD？
Aspose.PSD 為直接在 Java 中操作 PSD 檔案提供完整工具集。它免除對 Photoshop 的依賴，支援批次作業，並能處理複雜的圖層類型、遮色片與特效。函式庫針對效能進行最佳化，能有效處理大型檔案，同時保留高保真度。

- **完整自動化** – 無需手動 Photoshop 步驟。  
- **跨平台** – 可於 Windows、macOS 與 Linux 上執行。  
- **不需安裝 Photoshop** – 函式庫在內部處理 PSD 結構。  
- **豐富 API** – 可存取圖層屬性、填充設定與匯出選項。  
- **效能** – Aspose.PSD 支援超過 100 種影像格式，且可在不將整個檔案載入記憶體的情況下處理高達 2 GB 的 PSD 檔案，較傳統腳本解決方案提升約 30 % 的速度。  

## 前置條件
在開始之前，請確保以下項目已備妥，以免卡關：
1. **Java Development Kit (JDK)** – 確保您的機器已安裝 JDK。您可從 [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 若要操作 PSD 檔案，您需要 Aspose.PSD 函式庫。可從 [Aspose releases page](https://releases.aspose.com/psd/java/) 下載。  
3. **整合式開發環境 (IDE)** – 如 IntelliJ IDEA、Eclipse 或 NetBeans 等 IDE 可讓編碼更方便。挑選您喜愛的即可！  
4. **基本 Java 知識** – 熟悉 Java 語法有助於順利跟隨本教學。  
5. **範例 PSD 檔案** – 準備好測試用的 PSD 檔案。您可自行於 Photoshop 建立，或從網路下載範例檔案。  

一旦上述條件皆已就緒，您就可以開始動手寫程式了！

## 匯入套件
要在 Java 中使用 Aspose.PSD，您需要匯入相應的套件。以下示範如何在專案中設定：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.UUID;
```  
這些匯入提供了操作 PSD 圖像、存取圖層以及調整填充圖層各種屬性的功能。接下來，我們將一步步說明如何 **render pattern** 填充圖層於 PSD 檔案中。

## 如何使用 Aspose.PSD 建立 pattern fill PSD
以下提供實作指南，您可以將程式碼片段直接複製到 IDE 中，並對您的範例 PSD 執行。

### 步驟 1：定義來源與輸出目錄
首先，需要設定來源 PSD 檔案所在位置以及輸出檔案的儲存路徑。  

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String outputFile = outputDir + "sample_out.psd";
```  
將 `"Your Source Directory"` 與 `"Your Document Directory"` 替換為您機器上的實際路徑。

### 步驟 2：載入 PSD 檔案
將 PSD 載入記憶體，以便開始編輯。

`PsdImage` 類別代表 Photoshop 文件，提供對其圖層與資源的存取。  

```java
PsdImage image = (PsdImage) Image.load(sourceFile);
```  
將載入的影像轉型為 `PsdImage` 後，即可使用 PSD 專屬的屬性與方法。

### 步驟 3：遍歷圖層
找出需要設定圖案的填充圖層。

`FillLayer` 類別模型化 Photoshop 的填充圖層，可容納純色、漸層或圖案。  

```java
try {
    for (Layer layer : image.getLayers()) {
        if (layer instanceof FillLayer) {
            FillLayer fillLayer = (FillLayer)layer;
            // Additional code will go here.
        }
    }
}
```  
`instanceof` 檢查確保我們僅處理 `FillLayer` 物件。

### 步驟 4：設定填充圖層屬性
調整選取圖層的偏移、縮放及其他視覺參數。

`IPatternFillSettings` 包含所有與圖案相關的選項，如偏移、縮放與實際圖案資料。  

```java
IPatternFillSettings settings = (IPatternFillSettings) fillLayer.getFillSettings();
settings.setHorizontalOffset(-5);
settings.setVerticalOffset(12);
settings.setScale(300);
settings.setLinked(true);
```  
每個屬性皆會影響圖案的呈現方式。例如，調整偏移會使圖案相對於圖層移動。

### 步驟 5：定義圖案資料
現在開始設定圖案本身，定義組成填充圖案的顏色。

`PatternFillSettings` 允許您提供一系列 `Color` 物件，以定義平鋪圖案。  

```java
settings.setPatternData(new int[]{
    Color.getBlack().toArgb(), 
    Color.getRed().toArgb(),
    Color.getGreen().toArgb(), 
    Color.getBlue().toArgb(),
    Color.getWhite().toArgb(), 
    Color.getAliceBlue().toArgb(),
    Color.getViolet().toArgb(), 
    Color.getChocolate().toArgb(),
    Color.getIndianRed().toArgb(), 
    Color.getDarkOliveGreen().toArgb(),
    Color.getCadetBlue().toArgb(), 
    Color.getYellowGreen().toArgb(),
    Color.getBlack().toArgb(), 
    Color.getAzure().toArgb(),
    Color.getForestGreen().toArgb(), 
    Color.getSienna().toArgb(),
});
```  
您可以自行替換顏色，以創造獨特的視覺風格。

### 步驟 6：設定圖案尺寸與名稱
進一步自訂填充圖層，設定其寬高、名稱與唯一 ID。

`PatternFillSettings.setPatternSize(int width, int height)` 控制瓦片大小，`setName` 與 `setId` 則協助日後辨識圖案。  

```java
settings.setPatternHeight(4);
settings.setPatternWidth(4);
settings.setPatternName("$$$/Presets/Patterns/ColorfulSquare=Colorful Square New\0");
settings.setPatternId(UUID.randomUUID() + "\0");
```  
尺寸決定圖案的瓦片大小，名稱與 ID 有助於後續辨識。

### 步驟 7：更新填充圖層
完成所有屬性設定後，需要將變更寫回圖層。

呼叫 `update()` 會將所有修改套用至底層 PSD 結構。  

```java
fillLayer.update();
```  

### 步驟 8：儲存變更
最後，使用 `save()` 方法將更新後的 PSD 檔案寫入磁碟。`PsdImage.save(String path)` 會將修改後的文件持久化。  

```java
image.save(outputFile, new PsdOptions(image));
```  
您的新檔案現在已包含自訂的圖案填充圖層。

### 步驟 9：釋放影像物件
為釋放資源，建議在完成後處置影像物件。`PsdImage.dispose()` 會釋放原生記憶體與檔案句柄，對於大量批次處理尤為重要。  

```java
finally {
    image.dispose();
}
```  

## 常見使用情境
- **自動化品牌化** – 為行銷素材產生一致的品牌圖案填充。  
- **動態紋理** – 為遊戲或模擬產生程序化紋理，免除手動設計。  
- **批次處理** – 一次執行即可將標準圖案填充套用至數百個 PSD 檔案。  

## 常見問題與解決方案
- **儲存後圖案未顯示** – 確認您編輯的圖層未被隱藏 (`layer.setVisible(true)`) 且圖案尺寸符合預期的瓦片大小。  
- **`ClassCastException`** – 請確保在確認 `instanceof FillLayer` 後才將物件轉型為 `FillLayer`。  
- **檔案路徑錯誤** – 使用絕對路徑或在 Windows 上使用雙反斜線跳脫 (`C:\\\\Images\\\\sample.psd`)。  

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套讓開發者能以程式方式操作 Photoshop PSD 檔案的函式庫。

**Q: 可以免費試用 Aspose.PSD 嗎？**  
A: 是的，您可透過 [free trial](https://releases.aspose.com/) 取得免費試用版以探索其功能。

**Q: 在哪裡可以購買 Aspose.PSD？**  
A: 您可於 [Aspose purchase page](https://purchase.aspose.com/buy) 購買授權。

**Q: 是否提供 Aspose.PSD 的支援？**  
A: 當然！您可在 [Aspose support forum](https://forum.aspose.com/c/psd/34) 取得協助。

**Q: 使用 Aspose.PSD 時若遇到問題該怎麼辦？**  
A: 請參考文件中的故障排除提示，或於 [support forum](https://forum.aspose.com/c/psd/34) 尋求協助。

**Q: 我可以使用此程式碼在同一個 PSD 中建立多個 pattern fill 圖層嗎？**  
A: 可以。只需對每個想要自訂的 `FillLayer` 重複迴圈邏輯，並依需求調整設定。

**Q: 此函式庫是否支援套用圖層效果的 PSD 檔案？**  
A: Aspose.PSD 能保留大多數圖層效果，但圖案填充僅適用於 `FillLayer` 物件。

**Q: 有沒有方法從 PSD 中讀取現有圖案並重複使用？**  
A: 您可以從 `FillLayer` 取得目前的 `IPatternFillSettings`，在套用修改前先複製其屬性。

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose

## 相關教學

- [在 Aspose.PSD for Java 中新增填充圖層至 PSD 檔案](/psd/java/modifying-converting-psd-images/add-fill-layers-psd-files/)
- [在 Aspose.PSD for Java 中新增圖案覆疊效果](/psd/java/advanced-image-effects/add-pattern-effects/)
- [使用 Java 為 PSD 檔案新增顏色填充圖層](/psd/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}