---
date: 2025-12-22
description: 學習如何使用 Aspose.PSD for Java 將 PSD 另存為 PNG，並使用不同的文字顏色。請參考我們的逐步指南，將 PSD
  匯出為 PNG 並渲染文字。
linktitle: Render Text with Different Colors in Text Layer
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 將 PSD 儲存為帶彩色文字的 PNG
url: /zh-hant/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 將 PSD 另存為 PNG 並套用彩色文字

## 介紹

歡迎閱讀我們的逐步指南，說明如何使用 Aspose.PSD for Java **將 PSD 另存為 PNG**，同時在文字圖層中套用不同顏色的文字。Aspose.PSD 是一個功能強大的 Java 函式庫，可讓您以程式方式操作 Photoshop 檔案，全面掌控 PSD 與 PSB 格式。

## 快速解答
- **本教學涵蓋什麼內容？** 呈現彩色文字並將 PSD 另存為 PNG 圖片。  
- **需要哪個函式庫？** Aspose.PSD for Java。  
- **是否需要授權？** 免費試用版可用於開發；正式環境需購買商業授權。  
- **可以更改輸出格式嗎？** 可以，您可以將 PSD 匯出為 PNG 或其他支援的格式。  
- **程式碼是否相容於 Java 8 以上？** 完全相容，範例可在 Java 8 及更新版本執行。

## 什麼是 **將 PSD 另存為 PNG**？
將 PSD 另存為 PNG 會將具圖層的 Photoshop 檔案轉換為平面點陣圖，同時保留透明度與色彩精度。當您需要網頁使用的圖像，或想在不透露原始圖層的情況下分享視覺結果時，這非常有用。

## 為何使用 Aspose.PSD **將 PSD 匯出為 PNG**？
- **不需安裝 Photoshop** – 函式庫在內部處理 PSD 解析。  
- **保留文字樣式** – 您可在匯出前修改字型、顏色與效果。  
- **高效能** – 為大型檔案與批次處理進行最佳化。  

## 前置條件

- 具備 Java 程式設計的基礎知識。  
- 已安裝 Aspose.PSD for Java 函式庫。您可從 [Aspose.PSD for Java 文件](https://reference.aspose.com/psd/java/) 下載。

## 匯入套件

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 如何 **將 PSD 另存為 PNG** 並套用彩色文字

### 步驟 1：設定專案
建立一個新的 Java 專案，並將 Aspose.PSD JAR 加入 classpath。確保應用程式對將使用的目錄具有讀寫權限。

### 步驟 2：定義來源與輸出目錄
更新路徑，使其指向您的 PSD 檔案以及 PNG 將被儲存的資料夾。

```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

### 步驟 3：載入 PSD 檔案並存取文字圖層
我們載入目標 PSD，定位文字圖層，並刷新其資料，使顏色變更得以套用。

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

### 步驟 4：設定 PNG 選項並 **將 PSD 匯出為 PNG**
設定 PNG 以保留完整色深與 Alpha 通道，然後儲存影像。

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

## 常見問題與技巧
- **圖層索引：** 確認您參考的是正確的圖層索引（範例中為 `[1]`）。不同檔案的圖層順序可能不同。  
- **顏色更新：** 在修改文字屬性後務必呼叫 `updateLayerData()`；否則變更不會出現在匯出的 PNG 中。  
- **記憶體管理：** 在 `finally` 區塊中釋放 `PsdImage` 物件，以釋放本機資源。

## 結論

恭喜！您現在已了解如何使用 Aspose.PSD for Java **將 PSD 另存為 PNG**，同時以多種顏色呈現文字。此技術可讓您在不開啟 Photoshop 的情況下，實現自動化影像產生、批次處理與動態圖形製作。

## 常見問答

### Q1：我可以在其他程式語言中使用 Aspose.PSD for Java 嗎？
A1：Aspose.PSD 主要為 Java 設計，但 Aspose 亦提供其他程式語言的相似函式庫。

### Q2：是否有 Aspose.PSD for Java 的試用版？
A2：有，您可從 [Aspose.PSD](https://releases.aspose.com/) 取得免費試用版。

### Q3：我可以在哪裡取得其他支援或協助？
A3：請前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 獲得社群支援與討論。

### Q4：如何取得 Aspose.PSD for Java 的臨時授權？
A4：您可向 [Aspose.PSD](https://purchase.aspose.com/temporary-license/) 申請臨時授權。

### Q5：是否有其他 Aspose.PSD 教學？
A5：有，請參考 [Aspose.PSD 文件](https://reference.aspose.com/psd/java/) 取得更多教學與範例。

---

**最後更新：** 2025-12-22  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}