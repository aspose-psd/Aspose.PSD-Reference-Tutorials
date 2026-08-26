---
date: 2026-08-22
description: 了解如何使用 Aspose.PSD 在 Java 中將 AI 轉換為 TIFF。內容包括逐步指南、TIFF 壓縮選項以及程式碼片段。
keywords:
- convert ai to tiff
- tiff compression options
- aspose psd java
lastmod: 2026-08-22
linktitle: 在 Java 中將 AI 轉換為 TIFF
og_description: 使用 Aspose.PSD 在 Java 中將 AI 轉換為 TIFF。遵循逐步指南，學習設定 TIFF 壓縮選項，並避免常見問題，以確保可靠的點陣圖轉換。
og_image_alt: Guide showing Java code converting Adobe Illustrator files to TIFF format
og_title: 使用 Aspose.PSD 在 Java 中將 AI 轉換為 TIFF
schemas:
- author: Aspose
  dateModified: '2026-08-22'
  description: Learn how to convert AI to TIFF in Java using Aspose.PSD. Includes
    step‑by‑step guide, TIFF compression options, and code snippets.
  headline: Convert AI to TIFF in Java
  type: TechArticle
- description: Learn how to convert AI to TIFF in Java using Aspose.PSD. Includes
    step‑by‑step guide, TIFF compression options, and code snippets.
  name: Convert AI to TIFF in Java
  steps:
  - name: '**Java Development Kit (JDK)** – version 8 or newer.'
    text: '**Java Development Kit (JDK)** – version 8 or newer.'
  - name: '**Aspose.PSD for Java** – download the [Aspose.PSD for Java library](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – download the [Aspose.PSD for Java library](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Source AI file** – the Adobe Illustrator (.ai) file you want to convert.'
    text: '**Source AI file** – the Adobe Illustrator (.ai) file you want to convert.'
  - name: '**TiffOptions** – to define the desired TIFF format and compression.'
    text: '**TiffOptions** – to define the desired TIFF format and compression.'
  type: HowTo
- questions:
  - answer: Yes, the library supports PSD, PNG, JPEG, BMP, GIF, and many more raster
      and vector formats.
    question: Can I convert other formats using Aspose.PSD for Java?
  - answer: No, Aspose.PSD handles AI files independently of Adobe Illustrator.
    question: Do I need Adobe Illustrator installed to convert AI files?
  - answer: Absolutely. Choose from `TiffLzw`, `TiffCcittFax4`, `TiffDeflateRgba`,
      or `TiffRle` to match your size‑quality trade‑off.
    question: Can I apply custom compression options to the TIFF file?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate all features.
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD Support Forum](https://forum.aspose.com/c/psd/34)
      for community help and official assistance.
    question: Where can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert ai
- tiff conversion
- java image processing
title: 在 Java 中將 AI 轉換為 TIFF
url: /zh-hant/java/java-ai-to-image-format-conversion/convert-ai-to-tiff/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 AI 轉換為 TIFF

## 簡介
如果您需要 **convert AI to TIFF** 並快速保留原始視覺忠實度，您來對地方了。無論是為列印準備藝術作品、存檔設計，或是將點陣圖輸入下游工作流程，Aspose.PSD for Java 都能讓整個過程變得輕鬆。在本教學中，我們將逐步說明完整流程——從載入 Adobe Illustrator (.ai) 檔案到使用您需要的壓縮設定儲存高品質 TIFF。

## 快速解答
- **哪個函式庫負責轉換？** Aspose.PSD for Java  
- **輸出使用哪種格式？** TIFF（Tagged Image File Format）  
- **我可以控制壓縮嗎？** 可以—使用 TIFF 壓縮選項，例如 `TiffDeflateRgba`  
- **需要安裝 Adobe Illustrator 嗎？** 不需要，轉換完全在 Java 執行環境內執行  
- **一般轉換需要多長時間？** 大多數檔案只需幾秒鐘，視檔案大小與解析度而定  

## 什麼是「將 AI 轉換為 TIFF」？
將 AI 轉換為 TIFF 意指將 Adobe Illustrator 向量檔案轉換為點陣圖 TIFF 影像，同時保留視覺忠實度，並能在僅接受點陣圖格式的環境中使用。此操作通常稱為 **ai to raster conversion**，在需要像素完美的列印或存檔時相當重要。

## 為什麼選擇 Aspose.PSD for Java？
Aspose.PSD 支援 **100+ 圖像格式**，且可在不將整個檔案載入記憶體的情況下處理多百頁文件。此函式庫可在任何 JVM（Windows、Linux、macOS）上執行，且 **不需外部相依**——您不必安裝 Adobe Illustrator 或本機編解碼器。透過對 **tiff compression options** 的細緻控制，您可以在檔案大小與影像品質之間取得精確的平衡，以符合生產需求。

## 先決條件
在開始之前，請確保您已具備：

1. **Java Development Kit (JDK)** – 版本 8 或更新。  
2. **Aspose.PSD for Java** – 下載 [Aspose.PSD for Java library](https://releases.aspose.com/psd/java/)。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
4. **Source AI file** – 您想要轉換的 Adobe Illustrator (.ai) 檔案。  
5. **TiffOptions** – 用於定義所需的 TIFF 格式與壓縮。  

## 匯入套件
以下類別提供載入 AI 檔案與設定 TIFF 輸出的核心功能。

`AiImage` 是代表 Adobe Illustrator 檔案於記憶體中的類別。  
`TiffOptions` 包含寫入 TIFF 檔案所需的所有設定，包括壓縮類型。  

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 步驟 1：設定專案
將 Aspose.PSD JAR 加入專案的 classpath，或透過 Maven/Gradle 參考函式庫。此步驟確保編譯器能找到程式碼片段中使用的類別。

## 步驟 2：載入 AI 檔案
載入 AI 檔案會建立一個 `AiImage` 物件，該物件在記憶體中代表向量藝術作品。

`AiImage` 封裝了原始 Illustrator 文件的所有圖層、路徑與色彩資訊，讓它可隨時進行點陣化。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "34992OStroke.ai";
AiImage image = (AiImage) Image.load(sourceFileName);
```

> **提示：** 調整 `dataDir` 以指向 `.ai` 檔案所在的資料夾。

## 步驟 3：定義輸出檔案
指定最終 TIFF 應儲存的位置。

`TiffOptions` 讓您在點陣化發生前設定輸出檔名、壓縮方式與像素格式。

```java
String outFileName = dataDir + "34992OStroke.tiff";
```

## 步驟 4：設定 TIFF 選項
Aspose.PSD 提供豐富的 **tiff compression options**。本例使用 `TiffDeflateRgba`，它在保留完整 32 位元色深的同時提供良好壓縮。

`TiffDeflateRgba` 會使用 DEFLATE 演算法分別壓縮每個通道，通常可將檔案大小減少 30‑50 %，且不會有明顯的品質損失。

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateRgba);
```

## 步驟 5：將 AI 檔案儲存為 TIFF
載入您的 AI，設定選項，然後呼叫 `save`。`save` 會使用提供的選項將影像寫入指定檔案。函式庫在單一步驟中處理點陣化、色彩轉換與壓縮。

```java
image.save(outFileName, tiffOptions);
```

程式碼執行完畢後，您會在先前指定的位置找到已點陣化的 TIFF 檔案，即可用於列印或進一步的影像處理流程。

## 常見問題與解決方案
| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **空白 TIFF 輸出** | 來源 AI 檔案使用不支援的功能 | 確保使用支援您要轉換之 AI 版本的最新 Aspose.PSD 版本。 |
| **檔案過大** | 預設壓縮不足 | 切換至其他 `TiffExpectedFormat`（例如 `TiffLzw`）或在儲存前降低影像解析度。 |
| **OutOfMemoryError** | 在低記憶體 JVM 上的非常大的 AI 檔案 | 增加 JVM 堆積大小 (`-Xmx`) 或在可能的情況下分塊處理影像。 |

## 常見問答

**問：我可以使用 Aspose.PSD for Java 轉換其他格式嗎？**  
答：可以，該函式庫支援 PSD、PNG、JPEG、BMP、GIF 以及許多其他點陣圖與向量格式。

**問：需要安裝 Adobe Illustrator 才能轉換 AI 檔案嗎？**  
答：不需要，Aspose.PSD 可獨立處理 AI 檔案，無需 Adobe Illustrator。

**問：我可以為 TIFF 檔案套用自訂壓縮選項嗎？**  
答：當然可以。可從 `TiffLzw`、`TiffCcittFax4`、`TiffDeflateRgba` 或 `TiffRle` 中選擇，以符合您的大小‑品質取捨。

**問：Aspose.PSD for Java 有免費試用嗎？**  
答：有，您可以下載 [free trial](https://releases.aspose.com/) 以評估所有功能。

**問：在哪裡可以取得 Aspose.PSD for Java 的支援？**  
答：請前往 [Aspose.PSD Support Forum](https://forum.aspose.com/c/psd/34) 取得社群協助與官方支援。

## 結論
使用 **Aspose.PSD for Java** 將 AI 檔案轉換為 TIFF 簡單且可靠。依照上述步驟，您即可取得具備完整 **tiff compression options** 控制的高品質點陣圖，適用於列印、存檔或下游影像處理工作流程。也可嘗試其他輸出格式與壓縮設定，以符合您的特定管線需求。

---

**最後更新:** 2026-08-22  
**測試環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose

## 相關教學

- [在 Java 中將 Illustrator 轉換為 PNG – Aspose.PSD 指南](/psd/java/java-ai-to-image-format-conversion/convert-ai-to-png/)
- [在 Aspose.PSD for Java 中設定 TIFF 選項](/psd/java/tiff-image-compression-configuration/configure-tiff-options/)
- [如何使用 Aspose.PSD for Java 將 PSD 轉換為 TIFF](/psd/java/psd-conversion/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}