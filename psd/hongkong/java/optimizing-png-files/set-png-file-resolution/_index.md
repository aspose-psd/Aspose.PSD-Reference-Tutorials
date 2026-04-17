---
date: 2026-03-18
description: 學習如何使用 Aspose.PSD for Java 更改 PNG 解析度及設定影像解析度。按照此一步一步的指南，即可快速優化您的圖片。
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD 在 Java 中更改 PNG 解析度
url: /zh-hant/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 更改 PNG 解析度（Java）

## 簡介
如果你需要快速且可靠地 **change PNG resolution java**，你來對地方了。在本教學中，我們將逐步說明如何使用 Aspose.PSD for Java 調整 PNG 檔案的解析度。無論你是在建立批次處理工具、Web 服務，或只是微調少量資產，同樣的方法都適用。打開你喜愛的 IDE，讓我們開始吧！

## 快速答覆
- **什麼函式庫處理 PNG 解析度？** Aspose.PSD for Java  
- **主要方法？** `PngOptions.setResolutionSettings`  
- **典型 DPI 值？** 72 × 96 for web‑ready images  
- **需要授權嗎？** A trial works for testing; a license is required for production  
- **支援的 JDK？** Java 8 or higher  

## 什麼是「change PNG resolution java」？
在 Java 中更改 PNG 解析度是指修改 DPI（每英吋點數）之中繼資料，該資料告訴瀏覽器與印表機圖像應顯示的大小。像素資料保持不變，但解析度標籤會被更新，這可能會影響列印尺寸與品質。

## 為什麼在此任務中使用 Aspose.PSD？
Aspose.PSD 提供高階 API，抽象化低階的 PNG 處理，讓你專注於業務邏輯而非檔案格式的細節。它支援數百項 PSD 功能，可在任何執行 Java 的平台上運作，且不需要本機函式庫。

## 先決條件
在開始之前，請確保你已擁有：

1. **Java Development Kit (JDK) 8+** – 程式碼可在任何近期的 JDK 上執行。  
2. **Aspose.PSD for Java** – 從 [download link](https://releases.aspose.com/psd/java/) 下載。  
3. **IDE** – IntelliJ IDEA、Eclipse 或具 Java 支援的 VS Code。  
4. **範例 PSD 檔案** – 我們將把它轉換為 PNG 並更改其解析度。  
5. **基本的 Java 知識** – 你能在不需額外說明的情況下理解程式碼片段。  

## 匯入套件
現在所有設定已完成，匯入你需要的類別。這些匯入讓你能使用影像載入、解析度設定與 PNG 匯出選項。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定你的 Java 專案
建立一個新的 Java 專案（或 Maven/Gradle 模組），並將 Aspose.PSD JAR 加入建置路徑。若使用 Maven，請從 Aspose 套件庫加入相應的相依性。

## 步驟 2：定義文件目錄
告訴程式來源 PSD 檔案所在位置以及輸出 PNG 應寫入的目錄。

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

將 `"Your Document Directory"` 替換為包含 `sample.psd` 的絕對或相對路徑。

## 步驟 3：載入 PSD 影像
使用 `PsdImage` 類別從磁碟讀取 PSD 檔案。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

確保檔名與你要處理的實際 PSD 相符。

## 步驟 4：建立與設定 PNG 選項
這裡就是實際 **change PNG resolution java** 的地方。我們實例化 `PngOptions`，並透過 `ResolutionSetting` 設定水平與垂直 DPI 值。

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

隨意將 `72` 與 `96` 替換為符合目標裝置的任意值。這就是 **set image resolution java** 操作的核心。

## 步驟 5：儲存產生的 PNG
最後，將 PSD 匯出為帶有新解析度中繼資料的 PNG。

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

檔案 `SettingResolution_output.png` 會出現在相同資料夾中，現在已帶有你指定的 DPI 值。

## 常見陷阱與技巧
- **路徑不正確** – 請再次確認 `dataDir` 以檔案分隔符號（`/` 或 `\`）結尾。  
- **不支援的 DPI** – 大多數瀏覽器會忽略 300 以上的 DPI 值；請保持在合理範圍。  
- **記憶體使用** – 大型 PSD 可能佔用大量 RAM；儲存後考慮釋放 `psdImage`（`psdImage.dispose()`）。  

## 結論
你剛剛學會如何使用 Aspose.PSD **change PNG resolution java**。透過調整 `ResolutionSetting`，你可以在不改變像素資料的情況下，控制印表機與設計工具對 PNG 的解讀方式。探索其他選項，如壓縮等級、色彩深度或批次處理，以進一步自動化工作流程。

欲深入了解，請參閱官方的 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

## 常見問答
### 使用 Aspose.PSD for Java 我可以將 PSD 檔案轉換為哪些格式？
你可以將 PSD 檔案轉換為 PNG、JPEG、BMP 與 TIFF 等格式。  
### 使用 Aspose.PSD for Java 是否需要授權？
是的，雖然提供免費試用版，但評估後若要持續使用必須擁有有效授權。  
### 我可以在同一程式中多次更改解析度嗎？
當然可以！你可以在同一應用程式中建立不同的 `PngOptions` 實例，以設定各種匯出設定。  
### 如果我的 PSD 檔案損毀該怎麼辦？
Aspose.PSD 能處理許多常見問題，但若檔案嚴重損毀，可能無法載入。請務必保留備份。  
### Aspose.PSD 適用於高效能應用程式嗎？
是的，它設計用於有效處理大型檔案，適合對效能有高要求的影像處理任務。

## 常見問題
**Q: 我該如何以程式方式為水平與垂直軸設定不同的 DPI？**  
A: 使用 `new ResolutionSetting(horizontalDpi, verticalDpi)`，如 PNG 選項範例所示。  

**Q: 我可以在一次執行中批次處理多個 PSD 檔案嗎？**  
A: 可以——將載入、選項設定與儲存步驟包在迴圈中，對你的檔案集合逐一處理。  

**Q: 更改 DPI 會影響檔案大小嗎？**  
A: 通常不會；DPI 只是中繼資料。只有在修改壓縮或像素尺寸時檔案大小才會變化。  

**Q: 有沒有方法讀取現有 PNG 的目前 DPI？**  
A: 使用 `Image.load()` 載入 PNG，然後檢查 `image.getResolutionSettings()`（適用於 PNG 檔案）。  

**Q: 官方支援哪些 JDK 版本？**  
A: Aspose.PSD for Java 支援 JDK 8 至 JDK 21。  

**最後更新：** 2026-03-18  
**測試版本：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}