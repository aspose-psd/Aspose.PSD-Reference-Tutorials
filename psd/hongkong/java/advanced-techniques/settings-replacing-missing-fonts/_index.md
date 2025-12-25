---
date: 2025-12-25
description: 學習如何使用 Aspose.PSD for Java 替換 PSD 檔案中的字型——一步一步的指南，同時展示如何將 PSD 儲存為 PNG
  以及處理缺失的字型。
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中替換字型
url: /zh-hant/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中替換字型

## 介紹

如果您在 Java 應用程式中處理 Photoshop (PSD) 檔案，缺少字型會破壞視覺版面並導致渲染錯誤。**如何快速且可靠地替換字型**對於維持設計忠實度至關重要。在本教學中，您將學習如何使用 Aspose.PSD for Java 替換缺失的字型、將結果轉換為 PNG，並保持影像轉換工作流程順暢。完成後，您將能在影像中替換字型、將 PSD 儲存為 PNG，並避免開發人員常見的陷阱。

## 快速解答
- **「替換字型」在 PSD 處理中是什麼意思？** 它會將缺失或無法使用的字型以您指定的備用字型取代。  
- **哪個函式庫會自動處理此功能？** Aspose.PSD for Java 提供 `PsdLoadOptions.setDefaultReplacementFont`。  
- **替換後我也可以將 PSD 轉換為 PNG 嗎？** 可以 – 使用 `PngOptions` 並呼叫 `psdImage.save`。  
- **正式環境需要授權嗎？** 非評估版建置必須使用有效的 Aspose.PSD 授權。  
- **支援哪個 Java 版本？** 任何 Java 8 以上的執行環境皆可與目前的 Aspose.PSD 版本相容。

## 什麼是 PSD 檔案中的字型替換？

當 PSD 參考的字型未安裝於主機上時，渲染引擎會退回使用通用字型，往往導致文字對齊錯位。字型替換允許您定義預設字型（例如 Arial），讓函式庫在遇到缺失字型時使用該字型，確保輸出視覺效果一致。

## 為什麼要使用 Aspose.PSD 替換缺失的字型？

- **Zero‑dependency solution** – 無需原生 Photoshop 或外部工具。  
- **Batch‑ready** – 可在迴圈中一次處理數十個檔案，使用相同設定。  
- **Image conversion ready** – 替換後即可直接 **save PSD as PNG** 或 **convert PSD to PNG**，不需額外步驟。  
- **Cross‑platform** – 可在 Windows、Linux 與 macOS 的 Java 執行環境上運作。

## 前置條件

1. **Aspose.PSD Library** – 從 [releases page](https://releases.aspose.com/psd/java/) 下載並安裝 Aspose.PSD for Java 函式庫。  
2. **Java Development Environment** – 已安裝並設定 JDK 8 或更新版本。  

現在我們已具備必要條件，讓我們深入程式碼。

## 匯入套件

先匯入必要的 Aspose.PSD 類別。這樣即可使用影像載入、字型替換選項與 PNG 匯出功能。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定文件目錄

定義包含來源 PSD 以及最終 PNG 要儲存位置的資料夾。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：指定來源與目的檔案

提供輸入 PSD 與輸出 PNG 的完整路徑。此做法讓工作流程更清晰，也方便維護程式碼。

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## 步驟 3：設定字型替換選項

建立 `PsdLoadOptions` 實例，告訴 Aspose.PSD 在遇到缺失字型時使用哪個字型。本例使用 **Arial**，您亦可替換為系統中任何已安裝的字型。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## 步驟 4：載入 PSD 圖像並替換字型

使用上述設定載入 PSD。函式庫會自動將所有缺失的字型換成您指定的預設字型。

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## 步驟 5：儲存已修改的圖像

設定 PNG 匯出選項 – 真彩色加上 Alpha 通道，以保留透明度。此步驟同時示範 **image conversion PSD to PNG** 在字型替換後的操作。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### 發生了什麼？

- PSD 以備用字型（Arial）開啟。  
- 原本參考缺失字型的所有文字圖層現在改用 Arial 渲染。  
- 最終圖像以 PNG 儲存，等同於 **saving PSD as PNG**，同時保留視覺忠實度。

## 常見問題與故障排除

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 文字仍然顯示不正確 | 字型度量不同（大小、粗細） | 以程式方式調整替換字型的大小，或選擇度量相近的字型。 |
| PNG 檔案比預期大 | 預設 PNG 選項使用 32 位元顏色 | 如果不需要 alpha，將 `PngColorType` 改為 `Truecolor`。 |
| 授權例外 | 未使用有效授權執行 | 在載入圖像前套用臨時或永久的 Aspose.PSD 授權。 |

## 常見問答

**Q: Aspose.PSD 是否相容所有 PSD 檔案版本？**  
A: Aspose.PSD 支援廣泛的 PSD 版本，從早期的 Photoshop 版本到最新功能皆可處理。

**Q: 我可以在 Aspose.PSD 中使用自訂字型作為替換嗎？**  
A: 可以，只需將自訂字型名稱傳入 `setDefaultReplacementFont`。請確保該字型對 JVM 可存取。

**Q: Aspose.PSD 有哪些授權方案可供選擇？**  
A: 請前往 [here](https://purchase.aspose.com/buy) 探索授權方案，選擇最適合您需求的方案。

**Q: 有 Aspose.PSD 的社群論壇可以取得支援嗎？**  
A: 有，請造訪 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得社群支援與討論。

**Q: 我要如何取得 Aspose.PSD 的臨時授權？**  
A: 前往 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權，用於測試與評估目的。

---

**最後更新：** 2025-12-25  
**測試版本：** Aspose.PSD 24.11 for Java (latest at time of writing)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}