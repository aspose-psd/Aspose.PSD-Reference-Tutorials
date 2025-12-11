---
date: 2025-12-10
description: 學習如何使用 Aspose.PSD for Java 提取 PSD 圖層並將 PSD 圖層轉換為 PNG。適合需要強大圖形操作的開發人員。
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD Java 提取 PSD 圖層並為 PSD 檔案新增圖層支援
url: /zh-hant/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD Java 提取 PSD 圖層並新增圖層支援

## 介紹
處理 Photoshop Document（PSD）檔案是平面設計師與開發人員的日常工作之一。最常見的任務之一是 **提取 PSD 圖層**，以便進行編輯、重複使用，或轉換為其他格式（例如 PNG）。在 Java 應用程式中，Aspose.PSD 讓這個過程變得直觀且程式碼友好。本教學將逐步說明如何提取 PSD 圖層、啟用圖層支援，並 **將 PSD 圖層轉換為 PNG**——提供清晰說明與實用技巧。

## 快速回答
- **「提取 PSD 圖層」是什麼意思？** 意指載入 PSD 檔案並存取每一個獨立圖層，以便進行操作或匯出。  
- **哪個程式庫在 Java 中處理此功能？** Aspose.PSD for Java 提供完整的 PSD 處理功能，無需 Photoshop。  
- **可以一次性將 PSD 圖層轉換為 PNG 嗎？** 可以——只要使用正確的載入選項，並以保留透明度的 PNG 選項儲存。  
- **生產環境需要授權嗎？** 生產環境需要商業可使用免費試用版進行評估。  
- **需要哪個 Java 版本？** JDK 8 以上（本教學以 JDK 11 為例）。

## 什麼是「提取 PSD 圖層」？
提取 PSD 圖層指的是讀取 PSD 檔案的內部結構，將每個圖層作為獨立的影像物件取出。這讓您能夠編輯、隱藏、重新排序或單獨匯出圖層——正如設計師在 Photoshop 中所做的，只是以程式方式實現。

## 為什麼要提取 PSD 圖層並轉換為 PNG？
- **重複使用資產：** 從主 PSD 中直接抽取圖示、按鈕或 UI 元件，省去手動匯出。  
- **自動化：** 即時產生縮圖或網頁用圖。  
- **保留透明度：** PNG 支援 Alpha 通道，適合網頁圖形。

## 前置需求
在開始之前，請確保您已具備以下項目：

1. **Java 開發環境** – 已安裝 JDK。可從 [Oracle 官方網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 從官方下載頁面 [此處](https://releases.aspose.com/psd/java/) 取得最新程式庫。  
3. **基本的 Java 知識** – 熟悉編譯與執行 Java 程式。  
4. **IDE** – IntelliJ IDEA、Eclipse 或您慣用的編輯器。  
5. **PSD 檔案** – 使用您手頭的 PSD，或下載範例 PSD 進行測試。

準備好以上項目後，即可開始提取 PSD 圖層。

## 匯入套件
首先，匯入 Aspose.PSD 程式庫中需要的類別。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：定義目錄
設定來源 PSD 與輸出 PNG 的路徑。將 `dataDir` 調整為您檔案所在的資料夾。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – 將 `"Your Document Directory"` 替換為實際的資料夾路徑。  
- `sourceFileName` – 要處理的 PSD 完整路徑。  
- `output` – 用於儲存包含提取圖層的 PNG 的目標路徑。

## 步驟 2：設定載入選項
配置 `PsdLoadOptions` 可確保所有圖層效果與資源正確載入，這對 **提取 PSD 圖層** 至關重要。

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – 載入附加於圖層的效果（如投影）。  
- `setUseDiskForLoadEffectsResource(true)` – 將大型資源寫入磁碟，降低記憶體壓力。

## 步驟 3：載入 PSD 檔案
使用上述選項將 PSD 載入 `PsdImage` 物件。

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

此時，`image` 已包含所有圖層、遮色片與效果，準備進行提取。

## 步驟 4：設定儲存選項
設定 PNG 的儲存方式。使用 `TruecolorWithAlpha` 可保留原始圖層的透明度。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## 步驟 5：儲存影像（將 PSD 圖層轉換為 PNG）
將載入的 PSD（含全部圖層）匯出為單一 PNG 檔案。此步驟即完成 **convert psd layers png** 的一次性操作。

```java
image.save(output, saveOptions);
```

若需要將每個圖層分別儲存為 PNG，可遍歷 `image.getLayers()`——但對多數情境而言，合併的 PNG 已足夠。

## 步驟 6：結束
加入友善的主控台訊息，讓您知道流程已成功完成。

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## 常見問題與技巧
- **記憶體不足錯誤：** 若處理極大尺寸的 PSD，請保持 `setUseDiskForLoadEffectsResource(true)` 開啟，以將暫存資料寫入磁碟。  
- **效果遺失：** 確認已設定 `setLoadEffectsResource(true)`，否則部分圖層效果可能被忽略。  
- **路徑問題：** 使用 `java.nio.file.Paths.get(...)` 以取得跨平台的路徑處理方式。

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套讓您在未安裝 Photoshop 的情況下操作 PSD 檔案的程式庫。

**Q: 我可以用 Aspose.PSD 處理其他檔案格式嗎？**  
A: 可以！雖然主要針對 PSD，Aspose 亦提供其他多種格式的程式庫。

**Q: 有試用版嗎？**  
A: 當然！您可以在 [此處](https://releases.aspose.com/) 下載免費試用版。

**Q: 若需要協助，該向哪裡尋求支援？**  
A: 可前往 Aspose 論壇的 PSD 版塊取得協助 [此處](https://forum.aspose.com/c/psd/34)。

**Q: 能否將 PNG 轉回 PSD？**  
A: Aspose.PSD 主要聚焦於讀取與操作 PSD，較少支援從其他格式轉回 PSD。

**Q: 如何將每個圖層分別匯出為 PNG？**  
A: 迭代 `image.getLayers()`，為每個圖層建立新的 `Bitmap`，並以各自的 `PngOptions` 儲存，即可得到每層獨立的 PNG 檔案。

## 結論
您現在已學會如何 **提取 PSD 圖層**、啟用完整圖層支援，並使用 Aspose.PSD for Java **將 PSD 圖層轉換為 PNG**。無論是建構自動化資產管線，或為桌面應用程式加入圖形功能，此方法皆能在不依賴 Photoshop 的前提下，提供對 Photoshop 檔案的細緻控制。歡迎進一步探索——例如套用濾鏡、程式化合併圖層，或個別匯出每層。

---

**最後更新：** 2025-12-10  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}