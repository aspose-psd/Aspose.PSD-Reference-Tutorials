---
date: 2025-12-17
description: 學習如何使用 Aspose.PSD for Java 匯出 PSD 為 PNG 並支援剪裁遮罩。跟隨我們的逐步指南，快速將 PSD 儲存為
  PNG。
linktitle: Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: 將 PSD 匯出為 PNG（含剪裁遮色片）– Aspose.PSD Java
url: /zh-hant/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 支援 PSD 檔案的 Clipping Mask 與 Aspose.PSD Java

## 介紹
如果您需要在保留裁剪遮罩資訊的同時 **export PSD as PNG**，Aspose.PSD for Java 可讓您輕鬆完成。在本教學中，我們將逐步說明如何以程式方式處理 PSD 檔案、套用裁剪遮罩，並 **save PSD to PNG**，完整支援透明度。完成後，您將擁有一段可直接嵌入 Java 專案的可重用程式碼。

## 快速解答
- **此函式庫的功能是什麼？** 它在 Java 中讀取、編輯並匯出 Photoshop PSD 檔案。  
- **能保留裁剪遮罩嗎？** 能——在匯出為 PNG 時遮罩會被保留。  
- **使用哪種格式進行無損匯出？** 使用帶 TruecolorWithAlpha 的 PNG。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。  
- **需要哪個版本的 Java？** JDK 8 或更高版本。

## 什麼是「export psd as png」？
將 PSD 檔案匯出為 PNG 會將多層的 Photoshop 文件轉換為平面點陣圖，同時保留透明度。這在需要 Web 用圖或想在不安裝 Photoshop 的情況下分享設計時特別有用。

## 為什麼要使用 Aspose.PSD 來完成此任務？
Aspose.PSD 能處理 Photoshop 的複雜功能——如裁剪遮罩、調整圖層與混合模式——而不需安裝 Photoshop。非常適合自動化工作流程、批次處理，或將設計資產整合至伺服器端應用程式。

## 前置條件
在開始撰寫程式碼前，請確保您已具備以下項目：

1. **Java Development Kit (JDK)** – 至少 JDK 8。從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) 下載。  
2. **Aspose.PSD for Java Library** – 從 [download page](https://releases.aspose.com/psd/java/) 取得最新 JAR。您也可以試用 [free trial](https://releases.aspose.com/)。  
3. **IDE** – IntelliJ IDEA、Eclipse，或任何您偏好的編輯器。  
4. **Basic Java Knowledge** – 熟悉檔案 I/O 與物件導向概念會更有幫助。

## 匯出 PSD 為 PNG – 步驟指南

### 步驟 1：定義文件目錄
首先，告訴程式您的來源 PSD 位於何處，以及 PNG 要寫入的目標路徑。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為您機器上包含 PSD 檔案的絕對路徑。

### 步驟 2：載入 PSD 檔案
接著，將 PSD 載入 `PsdImage` 物件，以便操作其圖層與遮罩。

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 步驟 3：設定匯出選項
設定 PNG 匯出參數。使用 `TruecolorWithAlpha` 可確保裁剪遮罩產生的透明區域得以保留。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### 步驟 4：匯出影像
現在將帶有裁剪遮罩的 PSD 儲存為 PNG 檔案。

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

產生的 PNG 可直接用於網頁、行動應用程式，或任何接受點陣圖的地方。

### 步驟 5：清理資源
完成後務必釋放 `PsdImage`，以釋放本機記憶體。

```java
im.dispose();
```

### 如何在單行程式碼中將 PSD 儲存為 PNG
如果您偏好簡潔寫法，整個流程可縮減為：

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*（上方顯示的展開版本是為了清晰說明與除錯方便而提供的。）*

## 常見問題與解決方案
- **Missing Transparency:** 請確認已設定 `PngColorType.TruecolorWithAlpha`，否則 PNG 會變成不透明。  
- **File Not Found:** 請檢查 `dataDir` 是否以正確的路徑分隔符（`/` 或 `\\`）結尾。  
- **OutOfMemoryError:** 請及時釋放 `PsdImage`，特別是在處理大型檔案或批次時。

## 常見問答

**Q: 什麼是 PSD 檔案中的裁剪遮罩？**  
A: 裁剪遮罩利用一個圖層的透明度限制另一圖層的可見範圍，讓複雜合成在不永久改變圖層的前提下完成。

**Q: 我可以使用 Aspose.PSD 編輯 PSD 檔案嗎？**  
A: 可以，您可以編輯圖層、套用效果，並匯出為 PNG、JPEG 等格式。

**Q: 哪裡可以找到 Aspose.PSD 的文件說明？**  
A: 您可以在此處取得完整的 Aspose.PSD for Java 文件說明 [here](https://reference.aspose.com/psd/java/)。

**Q: 是否提供 Aspose.PSD 的試用版？**  
A: 有！您可在此取得免費試用版 [here](https://releases.aspose.com/)。

**Q: 若遇到 Aspose.PSD 的問題，該如何取得支援？**  
A: 您可透過 Aspose 論壇取得支援，連結如下 [here](https://forum.aspose.com/c/psd/34)。

## 結論
您現在已學會如何使用 Aspose.PSD for Java **export PSD as PNG**，同時保留裁剪遮罩。此方法可讓您自動化設計流程、將 Photoshop 資產整合至後端服務，且不需手動匯出步驟。探索 Aspose.PSD 的其他功能——如圖層合併、顏色調整與批次處理——以進一步簡化工作流程。

---

**最後更新：** 2025-12-17  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}