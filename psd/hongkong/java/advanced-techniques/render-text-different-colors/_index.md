---
date: 2026-05-29
description: 了解如何使用 Aspose.PSD for Java 將 PSD 另存為帶彩色文字的 PNG。本分步指南將示範如何高效地將 PSD 轉換為
  PNG。
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: 在 Text Layer 中以不同顏色呈現文字
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 將 PSD 另存為帶彩色文字的 PNG
url: /zh-hant/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 將 PSD 儲存為 PNG 並套用彩色文字

歡迎閱讀我們的逐步指南，了解如何使用 Aspose.PSD for Java **將 PSD 儲存為 PNG** 並使用不同顏色的文字。Aspose.PSD 是一個功能強大的 Java 函式庫，可讓您以程式方式操作 Photoshop 檔案，提供廣泛的功能來處理 PSD 與 PSB 檔案格式。

在本教學中，我們將帶領您完成使用 Aspose.PSD 在文字圖層中以不同顏色呈現文字的過程。完成本指南後，您將清楚了解如何順利完成此任務。

## 快速解答
- **如何將 PSD 儲存為 PNG？** 使用 Aspose.PSD 的 `PsdImage` 類別載入 PSD，並以 `PngOptions` 呼叫 `save`。
- **我可以在同一文字圖層中渲染多種顏色嗎？** 可以，為文字的每個 `Portion` 指派不同的 `Color` 物件。
- **需要哪個 Java 版本？** 支援 Java 8 或更高版本。
- **生產環境是否需要授權？** 需要商業授權；亦提供免費試用版。
- **此函式庫對大型檔案的記憶體效能如何？** 可處理高達 2 GB 的檔案，且不需完整載入記憶體。

## 如何使用彩色文字將 PSD 儲存為 PNG？

載入 PSD 檔案，修改文字圖層的各個 Portion 以指派不同顏色，然後將影像儲存為 PNG——整個工作流程只需幾行 Java 程式碼。Aspose.PSD 會自動光柵化編輯過的圖層，保留透明度與色彩忠實度，使最終的 PNG 與原始設計相符。

## 什麼是 Aspose.PSD for Java？

Aspose.PSD for Java 是一個函式庫，可程式化建立、編輯與轉換 Photoshop (PSD/PSB) 檔案。它支援 **50 多種影像格式**，且能在不將整個檔案載入記憶體的情況下處理數百頁的文件，提供高效能的伺服器端自動化。

## 前置條件

- 具備 Java 程式設計的基本知識。
- 已安裝 Aspose.PSD for Java 函式庫。您可從 [Aspose.PSD for Java 文件](https://reference.aspose.com/psd/java/) 下載。

## 匯入套件

`Image` 為載入與儲存影像檔案的基底類別。`PsdImage` 代表 Photoshop 文件，而 `TextLayer` 提供存取文字圖層屬性的功能。`PngOptions` 定義 PNG 匯出的設定。  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定專案

建立一個新的 Java 專案並加入 Aspose.PSD 函式庫。確保您具備存取與修改專案目錄中檔案的必要權限。

## 步驟 2：定義來源與輸出目錄

指定 PSD 檔案所在的來源目錄以及最終影像要儲存的輸出目錄。相應地更新 `sourceDir` 與 `outputDir` 變數。  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## 步驟 3：載入 PSD 檔案並存取文字圖層

`PsdImage` 將 PSD 檔案載入記憶體，而 `TextLayer` 允許操作該圖層內的文字內容。  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## 步驟 4：設定 PNG 選項並儲存結果影像

`PngOptions` 設定 PNG 輸出的參數，例如顏色類型與壓縮方式。  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## 常見問題與解決方案

- **缺少授權例外錯誤：** 確保在呼叫任何儲存操作前已套用有效的授權檔案。
- **顏色未套用：** 確認文字圖層中的每個 `Portion` 的 `Color` 屬性已正確設定。
- **大型檔案記憶體使用量：** 使用 `PsdImage` 的 `load` 重載並搭配 `loadOptions` 以串流方式處理大型檔案。

## 常見問答

**Q: 我可以將 Aspose.PSD for Java 與其他程式語言一起使用嗎？**  
A: Aspose.PSD 主要設計給 Java 使用，但 Aspose 亦提供其他程式語言的類似函式庫。

**Q: 是否有 Aspose.PSD for Java 的試用版可供下載？**  
A: 有，您可從 [Aspose.PSD](https://releases.aspose.com/) 取得免費試用版。

**Q: 我可以在哪裡取得額外的支援或協助？**  
A: 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 獲得社群支援與討論。

**Q: 如何取得 Aspose.PSD for Java 的臨時授權？**  
A: 您可向 [Aspose.PSD](https://purchase.aspose.com/temporary-license/) 申請臨時授權。

**Q: 是否有其他 Aspose.PSD 的教學可供參考？**  
A: 有，請瀏覽 [Aspose.PSD 文件](https://reference.aspose.com/psd/java/) 以取得更多教學與範例。

**Q: 此函式庫是否支援將多個 PSD 檔案批次轉換為 PNG？**  
A: 有，您可以遍歷 PSD 檔案資料夾，套用相同的文字顏色邏輯，並使用迴圈將每個檔案儲存為 PNG。

**Q: 輸出的 PNG 是否為無損？**  
A: 透過 Aspose.PSD 儲存的 PNG 保持完整的無損品質，保留所有顏色與透明度資訊。

---

**最後更新:** 2026-05-29  
**測試環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.PSD for Java 匯出 PSD 為 PNG 並新增常規圖層](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [使用 Aspose.PSD for Java 將 PSD 儲存為 PNG 並套用渲染陰影](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [使用 Aspose.PSD for Java 以顏色覆蓋將 PSD 轉換為 PNG](/psd/java/advanced-image-manipulation/rendering-color-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}