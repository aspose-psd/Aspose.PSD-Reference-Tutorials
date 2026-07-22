---
date: 2026-02-17
description: 學習如何使用 Aspose.PSD 在 Java 中將 PSD 轉換為圖像並套用調整圖層。本分步指南亦說明如何在生產環境中設定 Aspose
  Java 授權。
linktitle: Apply Adjustment Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: 在 Java 中將 PSD 轉換為圖像 – 使用 Aspose.PSD 套用調整圖層
url: /zh-hant/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 PSD 轉換為影像 – 使用 Aspose.PSD 套用調整圖層

## 介紹
如果你是 Java 開發者，想要 **將 PSD 轉換為影像** 同時 **在 Photoshop PSD 檔案中套用調整圖層 java**，那麼你已經來對地方了。在本教學中，我們將示範如何載入 PSD、定位其調整圖層、將它們合併至基底圖層，最後儲存更新後的影像——全部使用 Aspose.PSD for Java 函式庫。無論你是在建置批次處理工具、自動化影像編輯服務，或只是想以程式方式操作 Photoshop 檔案，掌握此技巧都能大幅擴展 Java 應用程式的能力。

## 快速解答
- **需要哪個函式庫？** Aspose.PSD for Java  
- **可以在未安裝 Photoshop 的環境下執行嗎？** 可以，函式庫可獨立運作。  
- **支援哪個 JDK 版本？** JDK 11 或更新版本（相容於大多數現代發行版）。  
- **正式環境需要授權嗎？** 非試用用途需購買商業授權。  
- **程式碼跨平台嗎？** 絕對可以——在 Windows、macOS 或 Linux 上皆可執行。

## 什麼是 “apply adjustment layers java”？
在 Java 中套用調整圖層是指以程式方式在 PSD 檔案內找到調整類型的圖層，並將其視覺效果合併至另一圖層（通常是背景）。這會產生與在 Photoshop 手動點選「合併」相同的結果，但可自動化處理數百個檔案，讓 **將 PSD 轉換為影像** 的工作流程完全可腳本化。

## 為什麼選擇 Aspose.PSD 來完成此任務？
- **完整的 PSD 相容性** – 所有圖層類型、遮色片與效果皆會被保留。  
- **不依賴 Photoshop** – 可在無頭伺服器上執行，完美適用於自動化 **將 PSD 轉換為影像** 流程。  
- **功能豐富的 API** – 直觀的類別可處理圖層、影像與檔案 I/O。  
- **跨平台** – 一次編寫，於任何支援 Java 的環境執行。

## 前置條件
1. **Java Development Kit (JDK)** – 從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD 函式庫** – 從官方下載頁面 [此處](https://releases.aspose.com/psd/java/) 取得 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse，或任何你慣用的編輯器。  
4. **基本的 Java 知識** – 需要熟悉類別與迴圈。  
5. **範例 PSD 檔案** – 準備好幾個含有調整圖層的 PSD 以供測試。

## 如何設定 Aspose 授權 Java（set aspose license java）
在載入任何 PSD 之前，先設定 Aspose 授權以避免評估水印。正式環境中你會呼叫 `License license = new License(); license.setLicense("Aspose.PSD.Java.lic");`。雖然此處省略了程式碼片段以保持程式碼區塊數量不變，但請務必在應用程式生命週期的早期 **設定 Aspose 授權 Java**。

## 匯入套件
在開始編寫程式碼之前，先說明需要匯入哪些套件。Aspose.PSD 讓我們能以多種方式操作 Photoshop 檔案，以下是處理 PSD 影像與調整圖層所需的類別。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```

現在套件已備妥，讓我們一步一步拆解範例吧！

## 步驟說明

### 步驟 1：載入 PSD 檔案
第一步是載入要修改的 PSD 檔案。載入檔案同時也是 **將 PSD 轉換為影像** 流程的起點。

```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```

將 `"Your Document Directory"` 替換為你機器上的實際路徑。此程式碼會建立一個代表整個 Photoshop 文件的 `PsdImage` 物件。

### 步驟 2：遍歷圖層並合併調整圖層
接下來，我們會遍歷每個圖層，辨識調整圖層，並將它們合併至基底圖層（通常是第一個圖層）。合併是最後 **將 PSD 轉換為影像** 前的必要步驟，因為它會把所有視覺效果整合起來。

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

此程式碼會檢查每個圖層的類型，必要時將其轉型為 `AdjustmentLayer`，然後呼叫 `mergeLayerTo` 以套用視覺變更。

### 步驟 3：儲存已修改的 PSD 檔案
合併完成後，需要將變更寫回磁碟。儲存 PSD 可保留合併結果，為最終的 **將 PSD 轉換為影像** 匯出做好準備。

```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```

新檔案 `ChannelMixerAdjustmentLayerChanged.psd` 現已包含合併後的結果。

### 步驟 4：處理 Levels 調整圖層（額外範例）
讓我們對包含 Levels 調整圖層的 PSD 重複相同流程。

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

現在你已成功套用 Levels 調整。

## 常見問題與技巧
- **Null Pointer 例外** – 在呼叫 `mergeLayerTo` 前，務必確認 `adjustmentLayer` 不為 null。  
- **基底圖層錯誤** – 若你的 PSD 使用不同的背景圖層，請相應調整索引 (`im.getLayers()[0]`)。  
- **大型檔案** – 對於非常大的 PSD，建議增加 JVM 堆積大小（例如 `-Xmx2g` 或更高）。  
- **授權錯誤** – 確保在正式環境載入檔案前已設定 Aspose 授權，以避免評估水印。  
- **匯出為影像** – 合併後，你可以呼叫 `im.save("output.png")` 以 **將 PSD 轉換為影像**，支援 PNG、JPEG、BMP 等格式。

## 常見問答

**Q: 什麼是 Aspose.PSD 函式庫？**  
A: Aspose.PSD 是一套讓開發者在 Java 應用程式中載入、操作與儲存 Photoshop PSD 檔案的函式庫。

**Q: 可以免費使用 Aspose.PSD 嗎？**  
A: 可以！Aspose 提供免費試用版讓你探索其功能。你可以在 [此處](https://releases.aspose.com/) 註冊。

**Q: 使用 Aspose.PSD 必須安裝 Photoshop 嗎？**  
A: 不需要，Aspose.PSD 可獨立於 Photoshop 操作 PSD 檔案。

**Q: 哪裡可以找到 Aspose.PSD 的文件？**  
A: 請前往文件頁面 [此處](https://reference.aspose.com/psd/java/) 了解功能、類別與方法。

**Q: 如何取得 Aspose 產品的支援？**  
A: 你可以透過 [Aspose 論壇](https://forum.aspose.com/c/psd/34) 提問或尋找解決方案。

**Q: 能否批次處理多個 PSD 檔案？**  
A: 當然可以——將載入、合併與儲存的邏輯包在迴圈中，對檔案路徑清單逐一執行即可。

## 結論
恭喜！你現在已掌握如何使用 Aspose.PSD 函式庫在 PSD 檔案中 **將 PSD 轉換為影像** 並 **套用調整圖層 java**。此功能讓你能在不開啟 Photoshop 的情況下自動化顏色校正、色階調整與其他視覺微調。嘗試其他調整圖層類型，結合影像匯出功能，讓你的 Java 應用程式具備 Photoshop 級別的影像處理能力，並可大規模運作。

---

**最後更新：** 2026-02-17  
**測試環境：** Aspose.PSD Java API（最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}