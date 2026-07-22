---
date: 2026-02-17
description: 學習如何使用 Aspose.PSD 在 Java 中將 PSD 轉換為 PNG、保留 PNG 透明度，並旋轉 PSD 圖層。逐步指南，附程式碼範例。
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: 使用 Java 將 PSD 轉換為 PNG 並旋轉 PSD 檔案中的圖層
url: /zh-hant/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 轉換 PSD 為 PNG 並旋轉 PSD 檔案中的圖層

## 介紹
如果你需要 **將 PSD 轉換為 PNG** 同時又要旋轉圖層，這篇指南適合你。無論你是在打造批次處理工具、需要即時影像處理的 Web 服務，或只是想自動化設計工作流程，程式化操作都能節省時間，且不再依賴 Adobe Photoshop。本教學將示範如何使用 Aspose.PSD for Java  **旋轉 PSD** 圖層並將結果匯出為 PNG。讓我們捲起袖子，讓你的設計工作流程順暢運作！

## 快速答覆
- **可以使用哪個函式庫？** Aspose.PSD for Java  
- **可以一次同時旋轉與轉換嗎？** 可以 – 先旋轉 PSD 再儲存為 PNG  
- **需要授權嗎？** 測試可使用免費試用版，正式環境需購買授權  
- **支援哪個 Java 版本？** Java 8 及以上  
- **PNG 輸出會保留透明度嗎？** 會，只要設定 `PngColorType.TruecolorWithAlpha`

## 什麼是「將 PSD 轉換為 PNG」？
將 Photoshop 文件（PSD）轉換成 PNG 圖像，意指把視覺內容（包括所有圖層、遮色片與透明度）抽取成一種廣受支援的點陣圖格式。PNG 能保留 Alpha 通道，非常適合用於網頁圖形、縮圖以及後續的影像處理。

## 為什麼使用 Aspose.PSD for Java 來轉換 PSD 為 PNG 並旋轉 PSD 圖層？
- **不需要 Photoshop** – 可在任何伺服器或 CI 環境執行  
- **完整圖層支援** – 透明度與圖層效果保持不變  
- **簡易 API** – 只需幾行程式碼即可旋轉、翻轉並儲存  
- **跨平台** – 支援 Windows、Linux 與 macOS  
- **Java 影像轉換** 只需一個函式庫即可輕鬆完成  

## 前置條件
在開始撰寫程式碼前，請先確認已具備以下項目：

- **Java Development Kit (JDK)** – 從 [Oracle 官方網站](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
- **整合開發環境 (IDE)** – IntelliJ IDEA、Eclipse 或 NetBeans 都可以。  
- **Aspose.PSD for Java 函式庫** – 從 [發行頁面](https://releases.aspose.com/psd/java/) 取得最新 JAR。  
- **基本的 Java 知識** – 了解類別、物件與例外處理。

## 步驟說明

### 步驟 1：建立 Java 專案
在 IDE 中建立新專案，並將 Aspose.PSD JAR 加入專案的建置路徑。

### 步驟 2：匯入必要類別
在 Java 原始檔的最上方加入以下匯入語句：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

這些類別提供載入影像、旋轉以及 PNG 專屬選項的功能。

### 步驟 3：定義檔案路徑
指定來源 PSD 的位置以及輸出檔案的寫入路徑。

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **小技巧：** 測試時使用絕對路徑，可避免「找不到檔案」的錯誤。

### 步驟 4：載入 PSD 檔案
將 PSD 載入可操作的物件。

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

此時 `im` 代表整個 Photoshop 文件，包含所有圖層。

### 步驟 5：旋轉影像（如何旋轉 PSD）
從 `RotateFlipType` 中選擇旋轉類型。本範例將影像旋轉 270° 並同時翻轉兩個軸向。

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

你也可以嘗試其他值，例如 `Rotate90FlipNone` 或 `Rotate180FlipX`。這就是本教學的 **如何旋轉 PSD** 部分。

### 步驟 6：將旋轉後的影像儲存為 PNG（將 PSD 轉換為 PNG）
設定 PNG 選項以保留透明度，然後儲存。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

產生的 PNG 會保留圖層透明度，確保 **保留 PNG 透明度** 供後續使用。

### 步驟 7：儲存已修改的 PSD（可選）
如果你也需要一個已套用旋轉的 PSD，請將其另存回去。

```java
im.save(psdPath);
```

現在你同時擁有 PNG 預覽檔與更新後的 PSD 檔案。

## 常見問題與解決方案
- **找不到檔案：** 確認 `dataDir` 以路徑分隔符 (`/` 或 `\`) 結尾。  
- **大型 PSD 發生 OutOfMemoryError：** 增加 JVM 堆積大小（例如 `-Xmx2g`）。  
- **透明度遺失：** 必須設定 `PngColorType.TruecolorWithAlpha`，否則 PNG 會以不含 Alpha 的方式儲存。  
- **翻轉 PSD 影像行為異常：** 再次檢查所選的 `RotateFlipType` 常數，有些常數會同時執行旋轉與翻轉。

## 常見問答

**Q: 可以只旋轉 PSD 中的特定圖層嗎？**  
A: 可以，使用 `Layer.rotateFlip()` 於遍歷 `im.getLayers()` 後對單一圖層操作。

**Q: Aspose.PSD for Java 有性能限制嗎？**  
A: 大多數檔案都能有效處理，但超大型 PSD（>500 MB）可能需要額外記憶體。

**Q: Aspose.PSD 可以免費使用嗎？**  
A: 提供免費試用版，正式環境需購買授權。可參考 [temporary license](https://purchase.aspose.com/temporary-license/) 進行測試。

**Q: 哪裡可以找到完整文件？**  
A: 請前往 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) 查看。

**Q: 使用 Aspose.PSD 時遇到問題該怎麼辦？**  
A: 可在 [Aspose Support Forum](https://forum.aspose.com/c/psd/34) 尋求協助。

**Q: 轉換 PSD 為 PNG 時會保留圖層效果嗎？**  
A: 會，只要使用 `PngColorType.TruecolorWithAlpha`，大部分視覺效果都會被光柵化到 PNG 中。

**Q: 可以批次處理多個 PSD 檔案嗎？**  
A: 完全可以，將程式碼包在迴圈中，遍歷資料夾內的 PSD 即可。

**Q: 能設定 PNG 的壓縮等級嗎？**  
A: `PngOptions` 類別提供 `setCompressionLevel(int)` 方法，可進行細部調整。

**Q: 必須手動關閉影像物件嗎？**  
A: `PsdImage` 實作 `Closeable`，請在 `finally` 區塊中呼叫 `im.close()`，或使用 try‑with‑resources。

**Q: 旋轉後的 PNG 會保留原始尺寸嗎？**  
A: 旋轉 90° 或 270° 時會交換寬高，PNG 會呈現新的方向尺寸。

## 結論
透過 Aspose.PSD for Java，你可以 **將 PSD 轉換為 PNG**、**保留 PNG 透明度**，並 **旋轉 PSD 圖層**，只需幾行程式碼。此方式省去 Photoshop 的需求，加速自動化工作流程，且讓你完整掌控影像輸出。快在自己的專案中試試看，體驗節省的時間與效能！

---

**最後更新：** 2026-02-17  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}