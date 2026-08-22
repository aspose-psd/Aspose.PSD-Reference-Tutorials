---
date: 2026-07-22
description: 了解如何使用 Aspose.PSD for Java 提取 PSD 圖層並將其轉換為 PNG。適合需要強大圖形處理的開發人員。
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: 使用 Aspose.PSD Java 提取 PSD 圖層並為 PSD 檔案新增圖層支援
og_description: 使用 Aspose.PSD for Java 提取 PSD 圖層並將其轉換為 PNG。請依照本步驟指南自動化圖層提取與影像轉換。
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: 提取 PSD 圖層 – 為 PSD 檔案新增圖層支援（使用 Aspose.PSD Java）
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: 使用 Aspose.PSD Java 提取 PSD 圖層並為 PSD 檔案新增圖層支援
url: /zh-hant/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD Java 提取 PSD 圖層並新增圖層支援

## 簡介
對於平面設計師和開發人員而言，處理 Photoshop Document（PSD）檔案是日常工作，而 **extract psd layers** 通常是重新使用資產或自動化影像流程的第一步。在本教學中，您將學習如何從 PSD 中提取單獨圖層、啟用完整圖層支援，並使用 Aspose.PSD for Java **convert PSD layers to PNG**。我們將涵蓋從環境設定到最佳實踐的所有內容，讓您能在幾分鐘內將此工作流程整合到任何 Java 應用程式中。

## 快速解答
- **What does “extract PSD layers” mean?** 它表示載入 PSD 檔案並存取每個單獨的圖層以進行操作或匯出。  
- **Which library handles this in Java?** Aspose.PSD for Java 提供完整功能的 PSD 處理，無需 Photoshop。  
- **Can I convert PSD layers to PNG in one go?** 可以——只要使用適當的選項載入檔案，並以保留透明度的 PNG 選項儲存即可。  
- **Do I need a license for production use?** 生產環境需要商業授權；亦提供免費試用版供評估。  
- **What Java version is required?** 需要 JDK 8 或更高版本（本教學示範使用 JDK 11）。

## 如何使用 Aspose.PSD for Java 提取 PSD 圖層？
只需幾行 Java 程式碼即可載入 PSD、啟用圖層效果，並將結果儲存為 PNG。此直接方法免除伺服器上安裝 Photoshop 的需求，且可在任何支援 Java 8+ 的平台上執行。  
您首先建立一個 `PsdLoadOptions` 物件，設定 `setLoadEffectsResource(true)` 與 `setUseDiskForLoadEffectsResource(true)`，然後使用 `PsdImage.load(path, options)` 載入檔案。載入後，您可以透過 `image.save(outputPath, new PngOptions())` 合併圖層，或遍歷 `image.getLayers()` 逐一匯出每個圖層，確保保留所有效果，同時降低記憶體使用量。

## 為何要提取 PSD 圖層並將其轉換為 PNG？
提取圖層可讓您 **reuse assets**、**automate thumbnail generation**，以及 **preserve transparency**，以製作適合網路的圖形。Aspose.PSD 支援 **50+ input and output formats**，且可在不將整個檔案載入記憶體的情況下處理多百頁的 PSD 檔案，這得益於其基於磁碟的資源處理機制。

## 先決條件
1. **Java Development Environment** – 已安裝 JDK。您可從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 從官方下載頁面 [here](https://releases.aspose.com/psd/java/) 取得最新程式庫。  
3. **Basic Java knowledge** – 熟悉編譯與執行 Java 程式。  
4. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
5. **A PSD file** – 使用您手頭的任何 PSD，或下載範例 PSD 進行測試。

一旦您準備好上述項目，即可開始提取 PSD 圖層。

## 匯入套件
`PsdImage`、`PsdLoadOptions` 與 `PngOptions` 類別是工作流程的核心。  

`PsdImage` 是 Aspose.PSD 的頂層物件，代表記憶體中的單一 PSD 檔案。  

`PsdLoadOptions` 讓您控制諸如圖層效果等資源的載入方式。  

`PngOptions` 定義 PNG 檔案的輸出格式與透明度處理。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：定義目錄
設定來源 PSD 與輸出 PNG 的路徑。將 `dataDir` 調整為指向您檔案所在的資料夾。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – 將 `"Your Document Directory"` 替換為實際的資料夾路徑。  
- `sourceFileName` – 要處理的 PSD 完整路徑。  
- `output` – 將提取圖層的 PNG 輸出目的路徑。

## 步驟 2：設定載入選項
設定 `PsdLoadOptions` 可確保正確載入所有圖層效果與資源，這在您 **extract PSD layers** 時至關重要。

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – 載入附加於圖層的效果（例如投影）。  
- `setUseDiskForLoadEffectsResource(true)` – 將大量資源卸載至磁碟，降低記憶體壓力。

## 步驟 3：載入 PSD 檔案
現在使用上述選項將 PSD 載入 `PsdImage` 物件。

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

此時，`image` 已包含所有圖層、遮色片與效果，準備好進行提取。

## 步驟 4：設定儲存選項
設定 PNG 的儲存方式。使用 `TruecolorWithAlpha` 可保留原始圖層的透明度。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## 步驟 5：儲存影像（將 PSD 圖層轉換為 PNG）
將載入的 PSD（含所有圖層）匯出為單一 PNG 檔案。此步驟實際上一次性 **convert psd layers png**。

```java
image.save(output, saveOptions);
```

如果您需要將每個圖層分別儲存為 PNG，可遍歷 `image.getLayers()`——但對於多數使用情境，合併的 PNG 已足夠。

## 步驟 6：完成收尾
加入友善的主控台訊息，以確認流程已成功。

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## 常見問題與技巧
- **Out‑of‑Memory Errors:** 若處理非常大的 PSD，請保持 `setUseDiskForLoadEffectsResource(true)` 為啟用狀態，以將暫存資料卸載至磁碟。  
- **Missing Effects:** 確認已設定 `setLoadEffectsResource(true)`；否則某些圖層效果可能會被忽略。  
- **Path Problems:** 使用 `java.nio.file` 中的 `Paths.get(...)` 以取得跨平台的路徑處理方式。

## 常見問答

**Q: Aspose.PSD for Java 是什麼？**  
A: Aspose.PSD for Java 是一個讓您在未安裝 Photoshop 的情況下操作 PSD 檔案的程式庫。

**Q: 我可以將 Aspose.PSD 用於其他檔案格式嗎？**  
A: 可以！雖然主要針對 PSD 檔案，Aspose 亦提供支援多種格式的程式庫，包括 AI、PDF 與 SVG。

**Q: 是否提供試用版？**  
A: 當然！您可在此處下載免費試用版 [here](https://releases.aspose.com/)。

**Q: 若遇到問題，該向哪裡尋求支援？**  
A: 前往 Aspose 論壇的 PSD 相關問題區 [here](https://forum.aspose.com/c/psd/34)。

**Q: 我能將每個圖層轉換為單獨的 PNG 嗎？**  
A: 可遍歷 `image.getLayers()`，為每個圖層建立新的 `Bitmap`，並使用各自的 `PngOptions` 儲存。如此即可為每個圖層產生獨立的 PNG 檔案。

## 結論
您現在已學會如何 **extract PSD layers**、啟用完整圖層支援，並使用 Aspose.PSD for Java **convert PSD layers to PNG**。無論是建立自動化資產管線，或為桌面應用程式加入圖形功能，此方法皆能讓您在不需要 Photoshop 本身的情況下，對 Photoshop 檔案進行精細控制。您可進一步探索套用濾鏡、程式化合併圖層，或逐層匯出以符合工作流程需求。

---

**最後更新：** 2026-07-22  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 匯出 PSD 為 PNG 並新增常規圖層](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [在 Java 中匯出 PSD 為 PNG 並支援圖層遮罩](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [在 Java 中將 PSD 轉換為影像 – 使用 Aspose.PSD 套用調整圖層](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}