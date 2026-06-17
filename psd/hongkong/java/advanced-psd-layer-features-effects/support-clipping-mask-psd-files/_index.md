---
date: 2026-02-20
description: 學習如何使用 Aspose.PSD for Java 將 PSD 匯出為 PNG，同時保留透明度與剪裁遮罩支援。本分步指南展示如何快速將
  PSD 儲存為 PNG。
linktitle: How to Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: 如何將 PSD 匯出為 PNG 並保留剪裁遮色片 – Aspose.PSD Java
url: /zh-hant/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 支援 PSD 檔案的 Clipping Mask 於 Aspose.PSD Java

## 簡介
如果您正在尋找 **如何匯出 PSD** 為 PNG 同時保留剪裁遮罩資訊，Aspose.PSD for Java 讓這個過程變得輕鬆。於本教學中，我們將逐步說明如何以程式方式處理 PSD 檔案、套用剪裁遮罩，並 **將 PSD 儲存為 PNG**，完整支援透明度。完成後，您將擁有一段可直接嵌入 Java 專案的可重用程式碼片段。

## 快速解答
- **此函式庫的功能是什麼？** 它能在 Java 中讀取、編輯與匯出 Photoshop PSD 檔案。  
- **它能保留剪裁遮罩嗎？** 可以——在匯出為 PNG 時遮罩會被保留。  
- **使用哪種格式進行無損匯出？** PNG 搭配 TruecolorWithAlpha。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。  
- **需要哪個 Java 版本？** JDK 8 或更高版本。

## 如何將 PSD 匯出為 PNG 並保留剪裁遮罩
將 PSD 檔案匯出為 PNG 會將多層的 Photoshop 文件轉換為平面點陣圖，同時保留透明度。當您需要適用於網頁的圖像、想要 **保留透明 PNG**，或在自動化流程中批次將 PSD 轉換為 PNG 時，這特別有用。

## 為何在此任務中使用 Aspose.PSD？
Aspose.PSD 能處理複雜的 Photoshop 功能——如剪裁遮罩、調整圖層與混合模式——且不需安裝 Photoshop。它非常適合自動化工作流程、批次處理，或將設計資產整合至伺服器端應用程式，確保可靠地 **將 PSD 匯出為 PNG**。

## 前置條件
在深入程式碼之前，請確保您已具備以下項目：

1. **Java Development Kit (JDK)** – 至少 JDK 8。從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) 下載。  
2. **Aspose.PSD for Java Library** – 從 [download page](https://releases.aspose.com/psd/java/) 取得最新 JAR。您亦可試用 [free trial](https://releases.aspose.com/)。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
4. **Basic Java Knowledge** – 熟悉檔案 I/O 與物件導向概念將有助於開發。

## 匯出 PSD 為 PNG – 步驟指南

### 步驟 1：定義文件目錄
首先，告訴程式您的來源 PSD 所在位置以及 PNG 要寫入的目錄。

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
設定 PNG 匯出參數。使用 `TruecolorWithAlpha` 可確保由剪裁遮罩產生的任何透明區域得以保留，從而 **保留透明 PNG**。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### 步驟 4：匯出影像
現在將 PSD（含剪裁遮罩）儲存為 PNG 檔案。

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

產生的 PNG 可直接用於網頁、行動應用程式或任何接受點陣圖的地方。

### 步驟 5：清理資源
完成後務必釋放 `PsdImage`，以釋放本機記憶體。

```java
im.dispose();
```

### 如何以單行程式碼將 PSD 儲存為 PNG
如果您偏好簡潔寫法，整個流程可縮減為：

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*（上方為展開版，便於閱讀與除錯。）*

## 常見問題與解決方案
- **缺少透明度：** 確認已設定 `PngColorType.TruecolorWithAlpha`；否則 PNG 會變成不透明。  
- **找不到檔案：** 確認 `dataDir` 以正確的路徑分隔符結尾（`/` 或 `\\`）。  
- **OutOfMemoryError：** 及時釋放 `PsdImage`，特別是在處理大型檔案或批次時。  
- **批次轉換 PSD 為 PNG：** 轉換多個檔案時，將步驟放入迴圈並重複使用 `PngOptions` 以提升效能。

## 常見問答

**Q: PSD 檔案中的剪裁遮罩是什麼？**  
A: 剪裁遮罩利用一個圖層的透明度來限制另一個圖層的可見範圍，允許在不永久改變圖層的情況下建立複雜的合成。

**Q: 我可以使用 Aspose.PSD 編輯 PSD 檔案嗎？**  
A: 可以，您可以編輯圖層、套用效果，並匯出為 PNG 或 JPEG 等格式。

**Q: 我在哪裡可以找到 Aspose.PSD 的文件說明？**  
A: 您可於此處取得 Aspose.PSD for Java 的完整文件說明 [here](https://reference.aspose.com/psd/java/)。

**Q: 是否提供 Aspose.PSD 的試用版？**  
A: 有！您可在此取得 Aspose.PSD 的免費試用版 [here](https://releases.aspose.com/)。

**Q: 我該如何取得 Aspose.PSD 的支援？**  
A: 如有任何問題或疑問，您可透過 Aspose 論壇取得支援 [here](https://forum.aspose.com/c/psd/34)。

## 結論
您現在已學會 **如何將 PSD 匯出為 PNG**，同時保留剪裁遮罩，使用 Aspose.PSD for Java。此方法可讓您自動化設計流程、將 Photoshop 資產整合至後端服務，且在不需手動匯出的情況下維持視覺完整性。探索 Aspose.PSD 的其他功能——如圖層合併、色彩調整與批次處理——以進一步簡化工作流程。

---

**最後更新：** 2026-02-20  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}