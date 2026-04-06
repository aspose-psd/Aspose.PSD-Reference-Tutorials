---
date: 2026-01-14
description: 學習如何使用 Aspose.PSD 在 Java 中將 AI 轉換為 TIFF。包括逐步指南、TIFF 壓縮選項及程式碼片段。
linktitle: Convert AI to TIFF in Java
second_title: Aspose.PSD Java API
title: 在 Java 中將 AI 轉換為 TIFF
url: /zh-hant/java/java-ai-to-image-format-conversion/convert-ai-to-tiff/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 AI 轉換為 TIFF

## 簡介
如果您需要 **將 AI 轉換為 TIFF** 並快速保留原始視覺忠實度，您來對地方了。無論是為列印準備藝術作品、歸檔設計，或是將點陣圖輸入後續工作流程，Aspose.PSD for Java 都能讓整個過程變得輕鬆無痛。本指南將帶您走完整個流程——從載入 Adobe Illustrator (.ai) 檔案到以您需要的壓縮設定儲存高品質 TIFF。

## 快速解答
- **哪個函式庫負責轉換？** Aspose.PSD for Java  
- **輸出使用哪種格式？** TIFF (Tagged Image File Format)  
- **我可以控制壓縮嗎？** 是—使用如 DeflateRgba 的 TIFF 壓縮選項  
- **需要安裝 Adobe Illustrator 嗎？** 不需要，轉換完全由 Aspose.PSD 執行  
- **一般轉換需要多久？** 大多數檔案只需幾秒，視檔案大小而定  

## 什麼是「將 AI 轉換為 TIFF」？
將 AI 檔案（Adobe Illustrator 向量格式）轉換為 TIFF 點陣圖意味著將可縮放的向量資料翻譯成以像素為基礎的表現形式。這通常稱為 **ai to raster conversion**，使圖像能在不支援向量的環境中使用。

## 為什麼選擇 Aspose.PSD for Java？
- **完整功能的 API** – 支援除 AI 與 TIFF 之外的多種影像格式。  
- **無外部相依性** – 可在不安裝 Adobe Illustrator 或其他本機函式庫的情況下運作。  
- **細緻的控制** – 讓您指定 **tiff compression options** 以及其他輸出參數。  
- **跨平台** – 可在任何 JVM（Windows、Linux、macOS）上執行。  

## 先決條件
在開始之前，請確保您已具備：

1. **Java Development Kit (JDK)** – 版本 8 或更新。  
2. **Aspose.PSD for Java** – 下載 [Aspose.PSD for Java library](https://releases.aspose.com/psd/java/)。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
4. **來源 AI 檔案** – 您想要轉換的 Adobe Illustrator (.ai) 檔案。  
5. **TiffOptions** – 用於定義所需的 TIFF 格式與壓縮。  

## 匯入套件
首先，匯入 Aspose.PSD 所需的類別，這些類別提供載入 AI 檔案與設定 TIFF 輸出的核心功能。

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

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "34992OStroke.ai";
AiImage image = (AiImage) Image.load(sourceFileName);
```

> **提示：** 調整 `dataDir` 以指向 `.ai` 檔案所在的資料夾。

## 步驟 3：定義輸出檔案
指定最終 TIFF 應儲存的位置。

```java
String outFileName = dataDir + "34992OStroke.tiff";
```

## 步驟 4：設定 TIFF 選項
Aspose.PSD 提供豐富的 **tiff compression options**。本範例使用 `TiffDeflateRgba`，在保留色彩深度的同時提供良好壓縮。

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateRgba);
```

## 步驟 5：將 AI 檔案儲存為 TIFF
最後，呼叫 `save` 方法執行 **convert ai to tiff** 操作。

```java
image.save(outFileName, tiffOptions);
```

程式執行完畢後，您會在先前指定的位置找到已點陣化的 TIFF 檔案。

## 常見問題與解決方案
| Issue | Reason | Fix |
|-------|--------|-----|
| **空白 TIFF 輸出** | 來源 AI 檔案使用了不支援的功能 | 確保您使用支援該 AI 版本的最新 Aspose.PSD 版本。 |
| **檔案過大** | 預設壓縮不足 | 改用其他 `TiffExpectedFormat`（例如 `TiffLzw`）或在儲存前調整影像解析度。 |
| **OutOfMemoryError** | 在低記憶體 JVM 上的極大 AI 檔案 | 增加 JVM 堆積大小（`-Xmx`）或盡可能分塊處理影像。 |

## 常見問答

**Q: 我可以使用 Aspose.PSD for Java 轉換其他格式嗎？**  
A: 可以，函式庫支援 PSD、PNG、JPEG、BMP 等多種點陣與向量格式。

**Q: 轉換 AI 檔案需要安裝 Adobe Illustrator 嗎？**  
A: 不需要，Aspose.PSD 可獨立處理 AI 檔案。

**Q: 我可以為 TIFF 檔案套用自訂壓縮選項嗎？**  
A: 當然可以。您可以從多個 `TiffExpectedFormat`（如 `TiffLzw`、`TiffCcittFax4`、`TiffDeflateRgba`）中選擇，以符合需求。

**Q: 有提供 Aspose.PSD for Java 的免費試用嗎？**  
A: 有，您可以下載 [free trial](https://releases.aspose.com/) 以測試功能。

**Q: 我該向哪裡取得 Aspose.PSD for Java 的支援？**  
A: 您可以在 [Aspose.PSD Support Forum](https://forum.aspose.com/c/psd/34) 上取得支援。

## 結論
使用 **Aspose.PSD for Java** 將 AI 檔案轉換為 TIFF 非常簡單。依照上述步驟，您即可完成可靠的 **ai to raster conversion**，並完整掌控 **tiff compression options**。歡迎自行嘗試其他格式與壓縮設定，以符合您的工作流程。

---

**最後更新：** 2026-01-14  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}