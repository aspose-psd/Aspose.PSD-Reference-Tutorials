---
date: 2026-07-22
description: 了解如何使用 Aspose.PSD 在 Java 中將 PSD 轉換為圖像並套用 Adjustment Layers。此一步一步指南亦說明如何為生產環境設定
  Aspose license Java。
keywords:
- convert psd to image
- save psd as image
- convert psd to png
- set aspose license java
- image editing without photoshop
lastmod: 2026-07-22
linktitle: 使用 Java 在 PSD 檔案中套用 Adjustment Layers
og_description: 使用 Aspose.PSD 在 Java 中將 PSD 轉換為圖像。了解如何套用 Adjustment Layers、將 PSD 儲存為圖像，以及為生產環境設定
  Aspose license Java。
og_image_alt: 'Guide: Convert PSD to Image and Apply Adjustment Layers using Java
  Aspose.PSD'
og_title: 將 PSD 轉換為圖像 – 在 Java 中使用 Aspose.PSD 套用 Adjustment Layers
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to convert PSD to image and apply adjustment layers in Java
    using Aspose.PSD. This step‑by‑step guide also shows how to set Aspose license
    Java for production.
  headline: Convert PSD to Image in Java – Apply Adjustment Layers with Aspose.PSD
  type: TechArticle
- description: Learn how to convert PSD to image and apply adjustment layers in Java
    using Aspose.PSD. This step‑by‑step guide also shows how to set Aspose license
    Java for production.
  name: Convert PSD to Image in Java – Apply Adjustment Layers with Aspose.PSD
  steps:
  - name: Load the PSD File
    text: The `PsdImage` class is Aspose.PSD's core object that represents a Photoshop
      document in memory. Loading the file is also the point where the **convert PSD
      to image** process begins. Replace `"Your Document Directory"` with the actual
      path on your machine. This snippet creates a `PsdImage` object th
  - name: Iterate Over Layers and Merge Adjustment Layers
    text: The `AdjustmentLayer` class encapsulates any adjustment‑type layer (e.g.,
      Levels, Curves, Color Balance). Loop through each layer, identify adjustment
      layers, and merge them into the base layer (usually the first layer). Merging
      is essential before you finally **convert PSD to image** because it con
  - name: Save the Modified PSD File
    text: After merging, you need to write the changes back to disk. Saving the PSD
      preserves the merged result, ready for the final **convert PSD to image** export.
      You can also **save psd as image** in PNG, JPEG, or BMP formats directly. The
      new file `ChannelMixerAdjustmentLayerChanged.psd` now contains the
  - name: Process a Levels Adjustment Layer (Additional Example)
    text: '#### Load the Levels Adjustment Layer PSD'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java API that lets developers load, manipulate, and save
      Photoshop PSD files without needing Photoshop installed.
    question: What is the Aspose.PSD library?
  - answer: Yes! Aspose offers a free trial for you to explore their library. You
      can sign up [here](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for free?
  - answer: No, you do not need Photoshop. Aspose.PSD works independently to manipulate
      PSD files programmatically.
    question: Do I need Photoshop installed to use Aspose.PSD?
  - answer: You can visit the documentation page [here](https://reference.aspose.com/psd/java/)
      to explore features, classes, and methods.
    question: Where can I find documentation for Aspose.PSD?
  - answer: You can access support via the [Aspose forum](https://forum.aspose.com/c/psd/34)
      where you can ask questions and find solutions.
    question: How do I get support for Aspose products?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
- adjustment layers
- PSD conversion
title: 在 Java 中將 PSD 轉換為圖像 – 使用 Aspose.PSD 套用 Adjustment Layers
url: /zh-hant/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 PSD 轉換為圖像 – 使用 Aspose.PSD 套用調整圖層

## 簡介
如果您是一位尋找 **convert PSD to image** 並且同時 **apply adjustment layers java** 於 Photoshop PSD 檔案的 Java 開發人員，您來對地方了。 在本教學中，我們將逐步說明如何載入 PSD、定位其調整圖層、將它們合併至基礎圖層，最後儲存更新後的圖像——全部使用 Aspose.PSD 的 Java 函式庫。 無論您是構建批次處理工具、自動化圖像編輯服務，或僅是以程式方式實驗 Photoshop 檔案，精通此技術都能大幅擴展您的 Java 應用程式的能力。

## 快速答案
- **需要哪個函式庫？** Aspose.PSD for Java  
- **可以在未安裝 Photoshop 的情況下執行嗎？** 是的，該函式庫可獨立運作，讓您在未安裝 Photoshop 的情況下進行圖像編輯。  
- **支援哪個 JDK 版本？** JDK 11 或更新版本（相容於大多數現代發行版）。  
- **在正式環境需要授權嗎？** 商業授權在非試用情況下是必須的；請在程式碼中盡早設定 aspose license java。  
- **此程式碼是否跨平台？** 絕對支援——可在 Windows、macOS 或 Linux 上執行。  

## 如何在 Java 中將 PSD 轉換為圖像並套用調整圖層？
`PsdImage` 類別代表已載入記憶體的 Photoshop 文件。 `AdjustmentLayer` 是一種圖層類型，用於儲存非破壞性的圖像調整，例如色階或曲線。 使用 `new PsdImage("file.psd")` 載入 PSD，遍歷其圖層，將任何 `AdjustmentLayer` 合併至基礎圖層，最後呼叫 `save("output.png")`（或任何支援的格式）——這就是完整的 **convert PSD to image** 工作流程，只需幾行程式碼。 此流程支援 PNG、JPEG、BMP 等多種格式，讓您 **save PSD as image** 而無需開啟 Photoshop。

## 什麼是 “apply adjustment layers java”？
在 Java 中套用調整圖層是指以程式方式定位 PSD 檔案內的調整類型圖層，並將其視覺效果合併至另一圖層（通常是背景）。 這會產生與在 Photoshop 手動點擊「Merge」相同的結果，但可在數百個檔案上自動化，讓 **convert PSD to image** 工作流程完全可腳本化。

## 為什麼在此任務中使用 Aspose.PSD？
Aspose.PSD 是專為 Java 設計的函式庫，提供 **full PSD fidelity**——保留所有圖層類型、遮色片與效果。 它 **supports over 100 image formats**，且可在不將整個文件載入記憶體的情況下處理高達 2 GB 的檔案，於無頭伺服器上提供高效能的 **convert PSD to png** 或其他點陣圖轉換。 此 API 直觀、跨平台，且 **no Photoshop installation**，非常適合 **image editing without photoshop**。

## 先決條件
1. **Java Development Kit (JDK)** – 從 [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD Library** – 從官方下載頁面取得 JAR 檔案 [here](https://releases.aspose.com/psd/java/)。 您也可以在此處瀏覽所有 Aspose 版本 [here](https://releases.aspose.com/)。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
4. **Basic Java knowledge** – 您應該熟悉類別與迴圈。  
5. **Sample PSD files** – 準備好幾個含有調整圖層的 PSD 檔案以供測試。

## 如何設定 Aspose 授權 Java（set aspose license java）
`License` 類別用於在執行時套用您購買的 Aspose.PSD 授權。於載入任何 PSD 前，設定 Aspose 授權以避免評估水印。 在正式環境中，您會呼叫 `License license = new License(); license.setLicense("Aspose.PSD.Java.lic");`。 雖然我們省略了程式碼片段以保持程式碼區塊數量不變，但請記得在應用程式生命週期早期 **set aspose license java**。

## 匯入套件
`PsdImage` 及相關類別位於 `com.aspose.psd` 命名空間。請在開始編寫程式碼前匯入必要的套件。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```

現在套件已就緒，讓我們一步一步拆解範例！

## 步驟指南

### 步驟 1：載入 PSD 檔案
`PsdImage` 類別是 Aspose.PSD 的核心物件，代表記憶體中的 Photoshop 文件。載入檔案也是 **convert PSD to image** 流程的起點。

```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```

將 `"Your Document Directory"` 替換為您機器上的實際路徑。此程式碼片段會建立一個代表整個 Photoshop 文件的 `PsdImage` 物件。

### 步驟 2：遍歷圖層並合併調整圖層
`AdjustmentLayer` 類別封裝任何調整類型的圖層（例如 Levels、Curves、Color Balance）。遍歷每個圖層，識別調整圖層，並將其合併至基礎圖層（通常是第一層）。在最終 **convert PSD to image** 前必須先合併，因為這會整合所有視覺效果。

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

此程式碼會檢查每個圖層的類型，適時將其轉型為 `AdjustmentLayer`，然後呼叫 `mergeLayerTo` 以套用視覺變更。

### 步驟 3：儲存已修改的 PSD 檔案
合併完成後，需要將變更寫回磁碟。儲存 PSD 可保留合併結果，為最終 **convert PSD to image** 匯出做好準備。您也可以直接 **save psd as image** 為 PNG、JPEG 或 BMP 格式。

```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```

新檔案 `ChannelMixerAdjustmentLayerChanged.psd` 現已包含合併結果。

### 步驟 4：處理 Levels 調整圖層（額外範例）

#### 載入 Levels 調整圖層 PSD
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```

#### 遍歷 Levels 圖層
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

#### 儲存 Levels 調整圖層 PSD
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```

現在您已成功套用 Levels 調整，亦可透過呼叫 `save("output.png")` **convert PSD to png** 或其他點陣格式。

## 常見問題與技巧
- **Null Pointer Exceptions** – 在呼叫 `mergeLayerTo` 前，務必確認 `adjustmentLayer` 不為 null。  
- **Incorrect Base Layer** – 若您的 PSD 使用不同的背景圖層，請相應調整索引 (`im.getLayers()[0]`)。  
- **Large Files** – 對於非常大的 PSD，建議增加 JVM 堆積大小 (`-Xmx2g` 或更高) 以避免記憶體不足錯誤。  
- **License Errors** – 請確保在正式環境載入檔案前已設定 Aspose 授權，以避免評估水印。  
- **Export to Image** – 合併後，您可以呼叫 `im.save("output.png")` 以 **convert PSD to image** 為 PNG、JPEG 或 BMP 等格式。

## 常見問答

**Q: 什麼是 Aspose.PSD 函式庫？**  
A: Aspose.PSD 是一套 Java API，讓開發人員能在不安裝 Photoshop 的情況下載入、操作與儲存 Photoshop PSD 檔案。

**Q: 可以免費使用 Aspose.PSD 嗎？**  
A: 可以！Aspose 提供免費試用版讓您探索此函式庫。您可在此註冊 [here](https://releases.aspose.com/).

**Q: 使用 Aspose.PSD 是否需要安裝 Photoshop？**  
A: 不需要。Aspose.PSD 可獨立運作，以程式方式操作 PSD 檔案。

**Q: 在哪裡可以找到 Aspose.PSD 的文件？**  
A: 您可前往文件頁面 [here](https://reference.aspose.com/psd/java/) 了解功能、類別與方法。

**Q: 如何取得 Aspose 產品的支援？**  
A: 您可透過 [Aspose forum](https://forum.aspose.com/c/psd/34) 獲得支援，提出問題並尋找解決方案。

**Q: 能否批次處理多個 PSD 檔案？**  
A: 當然可以——將載入、合併與儲存的邏輯包在迴圈中，對檔案路徑清單逐一處理。

## 結論
恭喜！您現在已了解如何使用 Aspose.PSD 函式庫在 PSD 檔案中 **convert PSD to image** 與 **apply adjustment layers java**。此功能讓您在不開啟 Photoshop 的情況下自動化顏色校正、色階調整及其他視覺微調。可嘗試其他調整圖層類型，結合此方法與圖像匯出功能，讓您的 Java 應用程式在大規模下處理 Photoshop 級別的圖像處理。

---

**最後更新：** 2026-07-22  
**測試環境：** Aspose.PSD Java API (latest version)  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.PSD for Java 轉換 PSD 為點陣圖格式](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [在 PSD 檔案中呈現曝光調整圖層 - Java](/psd/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/)
- [使用 Java 套用 PSD 檔案的圖層效果](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}