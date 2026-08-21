---
date: 2026-06-13
description: 了解如何使用 Aspose.PSD for Java 替換 PSD 檔案中的字型、將 PSD 轉換為 PNG，並有效處理缺失的字型。
keywords:
- how to replace fonts
- convert psd to png
- handle missing fonts psd
linktitle: 缺失字型替換設定
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to replace fonts in PSD files using Aspose.PSD for Java,
    convert PSD to PNG, and handle missing fonts efficiently.
  headline: How to Replace Fonts in PSD Files with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`PsdImage` is the core class that represents a PSD document in memory.'
    question: What is the primary class for loading PSD files?
  - answer: Use `PsdLoadOptions.setDefaultFontName("Arial")`.
    question: Which option sets a default replacement font?
  - answer: Yes—call `psdImage.save("output.png", new PngOptions())`.
    question: Can I save the result as PNG?
  - answer: A temporary license works for testing; a full license is required for
      production.
    question: Do I need a license for development?
  - answer: Aspose.PSD for Java supports Java 8 and later.
    question: What Java version is supported?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 替換 PSD 檔案中的字型
url: /zh-hant/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 替換 PSD 檔案中的字型

在現代 Java 開發中，**如何替換字型**於 Photoshop (PSD) 檔案是一項常見挑戰，若處理不當會破壞設計的視覺版面。Aspose.PSD for Java 提供強大的 API 來自動化字型替換，讓您的圖像保持原本的外觀。本指南將逐步說明從環境設定到最終 PNG 儲存的每個步驟，讓您自信地處理 PSD 檔案中的缺失字型。

## 快速解答
- **什麼是載入 PSD 檔案的主要類別？** `PsdImage` 是代表記憶體中 PSD 文件的核心類別。  
- **哪個選項可設定預設替換字型？** 使用 `PsdLoadOptions.setDefaultFontName("Arial")`。  
- **我可以將結果儲存為 PNG 嗎？** 可以——呼叫 `psdImage.save("output.png", new PngOptions())`。  
- **開發時需要授權嗎？** 臨時授權可用於測試；正式環境需要完整授權。  
- **支援哪個 Java 版本？** Aspose.PSD for Java 支援 Java 8 及以上版本。

## 如何使用 Aspose.PSD for Java 替換 PSD 檔案中的字型？

使用 `PsdLoadOptions` 載入來源 PSD，指定備用字型，然後將圖像儲存為所需格式。API 會自動將任何缺失的字形以您提供的預設字型替代，免除手動編輯的錯誤。此一步驟方法適用於任何大小的檔案，且保留圖層、遮色片與效果。

## 什麼是 `PsdLoadOptions`？

`PsdLoadOptions` 是一個設定物件，控制 Aspose.PSD 解析 PSD 檔案的方式。它允許您指定預設替換字型、控制圖層載入行為，並設定缺失資源的處理選項。透過調整其屬性，開發者可確保在不同環境下文字與其他元素的渲染一致，避免因字型不可用而產生的執行時錯誤。

## 為什麼要替換 PSD 檔案中缺失的字型？

Aspose.PSD 支援 **50+ 輸入與輸出格式**，且可在不將整個文件載入記憶體的情況下處理上百頁的 PSD 檔案。替換缺失字型可防止文字圖層破碎，將手動校正時間縮減最高 **80%**，並確保匯出的 PNG 保持原始設計的忠實度。

## 前置條件

1. **Aspose.PSD Library** – 從[發佈頁面](https://releases.aspose.com/psd/java/)下載並安裝 Aspose.PSD for Java 函式庫。  
2. **Java 開發環境** – Java 8+ JDK 以及您偏好的 IDE（Eclipse、IntelliJ IDEA 等）。  

現在一切就緒，讓我們深入實作。

## 匯入套件

匯入必要的命名空間，以便編譯器能找到 Aspose.PSD 類別。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定文件目錄

定義包含來源 PSD 以及輸出檔案寫入位置的資料夾。此路徑會被載入器與儲存器使用。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：指定來源與目標檔案

提供原始 PSD 與目標 PNG 的絕對或相對路徑。使用清晰的命名規則可避免檔案被覆寫。

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## 步驟 3：設定字型替換

建立 `PsdLoadOptions` 實例，並將預設替換字型設定為 **Arial**（或系統中安裝的任何字型）。此設定告訴引擎在找不到原始字型時使用哪個字型。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## 步驟 4：載入 PSD 圖像並替換字型

使用先前設定的選項載入 PSD。Aspose.PSD 會在載入過程中自動替換缺失的字型，無需額外程式碼。

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## 步驟 5：儲存已修改的圖像

選擇 `PngOptions` 以真彩 PNG（含 Alpha 通道）匯出圖像。最終檔案將正確顯示已替換的字型。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|------|------|----------|
| 文字顯示亂碼 | 替換字型缺少必要的字形 | 選擇 Unicode 範圍更廣的字型（例如 **Arial Unicode MS**）。 |
| 找不到檔案錯誤 | 第 1 步或第 2 步的路徑不正確 | 檢查目錄字串，並使用 `File.separator` 以確保跨平台相容性。 |
| 授權例外 | 未使用有效授權執行 | 在測試時套用臨時授權，正式環境則購買完整授權。 |

## 常見問答

### Q1：Aspose.PSD 是否相容所有 PSD 檔案版本？

A1：Aspose.PSD 支援從 **4.0** 到最新 Photoshop 版本的 PSD，確保對舊版與新版設計皆具廣泛相容性。

### Q2：我可以在 Aspose.PSD 中使用自訂字型作為替換嗎？

A2：可以，您只要將伺服器上已安裝的任何 TrueType 或 OpenType 字型名稱傳給 `setDefaultFontName` 即可。這讓您完整掌控視覺效果。

### Q3：Aspose.PSD 有哪些授權方案可供選擇？

A3：請前往[此處](https://purchase.aspose.com/buy)了解授權方案，選擇最適合貴公司的方案，包含開發者、站點與 OEM 授權。

### Q4：是否有 Aspose.PSD 社群論壇可供支援？

A4：有，請造訪 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)取得社群協助、程式碼片段與其他開發者的除錯技巧。

### Q5：如何取得 Aspose.PSD 的臨時授權？

A5：可於[此處](https://purchase.aspose.com/temporary-license/)取得免費的臨時授權，用於評估、測試或概念驗證專案。

---

**最後更新：** 2026-06-13  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [將 PSD 轉換為帶顏色疊加的 PNG – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並等比例調整大小](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [將 PSD 轉換為點陣圖像格式 – Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}