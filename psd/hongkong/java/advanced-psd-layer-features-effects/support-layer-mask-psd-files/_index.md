---
date: 2025-12-17
description: 學習如何使用 Aspose.PSD for Java 將 PSD 匯出為 PNG 並保留圖層遮罩——Java 圖像轉換的逐步指南。
linktitle: Export PSD to PNG with Layer Mask Support in Java
second_title: Aspose.PSD Java API
title: 在 Java 中將 PSD 匯出為支援圖層遮罩的 PNG
url: /zh-hant/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 PSD 為 PNG（支援圖層遮罩）於 Java

## 介紹
當您需要 **匯出 PSD 為 PNG** 並保留複雜的圖層遮罩時，可靠的 Java 函式庫可以為您節省大量手動操作時間。在本教學中，我們將使用 Aspose.PSD Java API，從載入 PSD 檔案到以完整 alpha‑channel 支援儲存為 PNG 圖像，逐步說明整個流程。無論您是建立批次處理工具、自動化資產管線，或只是需要快速轉換腳本，都能找到清晰、對話式的步驟，使任務變得簡單。

## 快速回答
- **「匯出 PSD 為 PNG」是什麼意思？** 將 Photoshop PSD 檔案轉換為 PNG 點陣圖，同時保留視覺忠實度。  
- **哪個函式庫支援圖層遮罩？** Aspose.PSD for Java 內建對遮罩與 alpha 通道的支援。  
- **需要授權嗎？** 免費試用可用於測試；商業使用需購買授權。  
- **可以在任何作業系統上執行嗎？** 可以 – Java API 與平台無關。  
- **轉換需要多長時間？** 標準尺寸檔案通常在一秒內完成。

## 什麼是「匯出 PSD 為 PNG」以及為何重要？
匯出 PSD 為 PNG 在您想要將 Photoshop 藝術作品分享至網路、嵌入應用程式，或產生縮圖時相當重要。PNG 能保留透明度，對於包含圖層遮罩的資產而言是理想選擇。透過 Java 自動化轉換，您可以省去手動匯出的步驟，並確保大量批次的結果一致。

## 前置條件
在開始編寫程式碼之前，請確保您具備以下條件：

- **Java Development Kit (JDK)** – 使用 `java -version` 檢查。若需下載，請前往 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)。  
- **Aspose.PSD 函式庫** – 從 [下載頁面](https://releases.aspose.com/psd/java/) 取得最新 JAR，或透過 Maven/Gradle 加入。  
- **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何 Java 開發編輯器。

### 1. Java 開發環境
使用近期的 JDK（11 或更新）可確保與 Aspose.PSD API 相容。

### 2. Aspose.PSD 函式庫
此函式庫處理 **java image conversion**、遮罩解析與 PNG 匯出選項。

### 3. IDE（整合開發環境）
使用 IDE 可簡化除錯與專案設定流程。

## 匯入套件
將必要的匯入語句加入您的 Java 類別。這些類別讓您能載入 PSD 檔案、操作遮罩，並設定 PNG 匯出參數。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## 匯出 PSD 為 PNG（支援圖層遮罩）
以下是完整的逐步工作流程，用於 **save psd as png** 同時保留遮罩。

### 步驟 1：設定專案目錄
定義包含來源 PSD 並將存放輸出 PNG 的資料夾。

```java
String dataDir = "Your Document Directory";
```

將 `Your Document Directory` 替換為您機器上的絕對路徑。

### 步驟 2：指定來源 PSD 檔案
指向您想要轉換的 PSD。此範例使用包含複雜遮罩的檔案。

```java
String sourceFileName = dataDir + "MaskComplex.psd";
```

### 步驟 3：定義 PNG 的匯出路徑
告訴程式將產生的 PNG 檔寫入何處。

```java
String exportPath = dataDir + "MaskComplex.png";
```

### 步驟 4：載入 PSD 檔案
這是 **how to load psd** 步驟。`Image.load` 方法會將檔案讀入 `PsdImage` 物件。

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 步驟 5：設定 PNG 匯出選項
設定 PNG 以保留 alpha 通道，這對圖層遮罩的透明度至關重要。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### 步驟 6：儲存 PNG 檔案
最後，執行 **convert psd to png** 操作。

```java
im.save(exportPath, saveOptions);
```

如果一切設定正確，您會在輸出資料夾中看到 `MaskComplex.png`，完美顯示原始 PSD 的遮罩區域。

## 常見問題與解決方案
- **檔案未找到錯誤** – 再次確認 `dataDir`，確保 PSD 檔名完全相符（含大小寫）。  
- **缺少透明度** – 確認已套用 `saveOptions.setColorType(PngColorType.TruecolorWithAlpha)`，否則 PNG 會在沒有 alpha 通道的情況下儲存。  
- **大型檔案記憶體不足** – 處理非常大的 PSD 時，可考慮增加 JVM 堆積大小（`-Xmx2g`）。

## 常見問與答

**Q: 什麼是 PSD 檔案中的圖層遮罩？**  
A: 圖層遮罩控制圖層的透明度，允許您在不永久刪除像素的情況下隱藏或顯示圖像的部分區域。

**Q: 沒有程式設計背景也能處理 PSD 檔案嗎？**  
A: 雖然 Aspose.PSD 需要撰寫程式碼，但平面設計師仍可使用 Photoshop 或其他 GUI 工具手動轉換。

**Q: Aspose.PSD 可以免費使用嗎？**  
A: 下載頁面提供免費試用；商業專案需購買授權。

**Q: 若我的 PSD 檔案沒有遮罩會怎樣？**  
A: 轉換仍會成功，產生的 PNG 只是不會有遮罩透明效果。

**Q: 若遇到問題該向哪裡尋求支援？**  
A: 前往 [support forum](https://forum.aspose.com/c/psd/34) 向 Aspose 專家與社群求助。

## 結論
您現在已學會如何使用 Aspose.PSD Java API **匯出 PSD 為 PNG**，同時保留圖層遮罩。此方法簡化了 **java image conversion**，支援批次處理，並確保您的視覺資產保持預期的透明度。歡迎嘗試不同的 PNG 選項，或將此工作流程整合至更大的自動化管線中。

---

**最後更新：** 2025-12-17  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}