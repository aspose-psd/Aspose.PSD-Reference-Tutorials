---
date: 2025-12-15
description: 學習如何使用 Aspose.PSD 在 Java 中將 PSD 轉換為 PNG 並旋轉 PSD 圖層。一步一步的指南，附有程式碼範例。
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: 使用 Java 將 PSD 轉換為 PNG 並旋轉 PSD 檔案中的圖層
url: /zh-hant/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 轉換為 PNG 並旋轉 PSD 檔案中的圖層（使用 Java）

## 介紹
如果您需要 **將 PSD 轉換為 PNG** 並同時旋轉圖層，本指南正是為您而寫。無論您是在打造批次處理工具，或是將影像操作整合到 Web 服務中，透過程式碼自動化都能節省時間，且不再依賴 Adobe Photoshop。在本教學中，我們將示範如何 **旋轉 PSD** 圖層，並使用 Aspose.PSD for Java 將結果匯出為 PNG。讓我們捲起袖子，讓您的設計工作流程順暢運作！

## 快速答覆
- **可以使用哪個函式庫？** Aspose.PSD for Java  
- **能否一次同時旋轉與轉換？** 可以 – 先旋轉 PSD 再儲存為 PNG  
- **需要授權嗎？** 免費試用可用於測試；正式環境需購買授權  
- **支援哪個 Java 版本？** Java 8 及以上  
- **PNG 輸出會保留透明度嗎？** 會，只要設定 `PngColorType.TruecolorWithAlpha`

## 什麼是「將 PSD 轉換為 PNG」？
將 Photoshop 文件（PSD）轉換成 PNG 圖像，意指將視覺內容（包括所有圖層、遮色片與透明度）提取為一種廣受支援的點陣圖格式。PNG 能保留 Alpha 通道，非常適合用於網站圖形、縮圖以及後續的影像處理。

## 為什麼要使用 Aspose.PSD for Java 來將 PSD 轉換為 PNG 並旋轉 PSD 圖層？
- **不需要 Photoshop** – 可在任何伺服器或 CI 環境執行  
- **完整圖層支援** – 透明度與圖層效果保持不變  
- **簡易 API** – 只需幾行程式碼即可旋轉、翻轉並儲存  
- **跨平台** – 支援 Windows、Linux 與 macOS  

## 前置條件
在開始撰寫程式碼之前，請確保您已具備以下項目：

- **Java Development Kit (JDK)** – 從 [Oracle 官方網站](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
- **整合開發環境 (IDE)** – IntelliJ IDEA、Eclipse 或 NetBeans 都可以。  
- **Aspose.PSD for Java 函式庫** – 從 [發行頁面](https://releases.aspose.com/psd/java/) 取得最新的 JAR。  
- **基本的 Java 知識** – 熟悉類別、物件與例外處理。

## 步驟說明

### 步驟 1：設定 Java 專案
在您的 IDE 中建立新 Java 專案，並將 Aspose.PSD JAR 加入專案的建置路徑。

### 步驟 2：匯入必要類別
在 Java 原始檔的最上方加入以下匯入語句：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

這些類別讓您可以存取影像載入、旋轉以及 PNG 專屬的選項。

### 步驟 3：定義檔案路徑
指定來源 PSD 檔案的位置以及輸出檔案的寫入路徑。

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **專業提示：** 測試時使用絕對路徑，可避免「找不到檔案」的錯誤。

### 步驟 4：載入 PSD 檔案
將 PSD 載入可操作的物件。

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

此時 `im` 代表整個 Photoshop 文件，包含所有圖層。

### 步驟 5：旋轉影像（如何旋轉 PSD）
從 `RotateFlipType` 中選擇旋轉類型。本範例將圖像旋轉 270° 並同時翻轉兩個軸向。

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

您也可以嘗試其他值，例如 `Rotate90FlipNone` 或 `Rotate180FlipX`。

### 步驟 6：將旋轉後的影像儲存為 PNG（將 PSD 轉換為 PNG）
設定 PNG 選項以保留透明度，然後儲存。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

產生的 PNG 仍保有圖層透明度，適合直接用於網頁。

### 步驟 7：儲存已修改的 PSD（可選）
如果您同時需要一個已套用旋轉的 PSD，請將其另存回去。

```java
im.save(psdPath);
```

現在您同時擁有 PNG 預覽圖與更新後的 PSD 檔案。

## 常見問題與解決方案
- **找不到檔案：** 確認 `dataDir` 以路徑分隔符（`/` 或 `\`）結尾。  
- **大型 PSD 發生 OutOfMemoryError：** 增加 JVM 堆積大小（例如 `-Xmx2g`）。  
- **透明度遺失：** 必須設定 `PngColorType.TruecolorWithAlpha`，否則 PNG 會以不含 Alpha 的方式儲存。

## 常見問答

### 我可以只旋轉 PSD 中的特定圖層嗎？
可以，遍歷 `im.getLayers()` 後，對單一圖層呼叫 `Layer.rotateFlip()` 即可。

### Aspose.PSD for Java 有性能限制嗎？
函式庫對大多數檔案都能有效處理，但極大型 PSD（>500 MB）可能需要額外記憶體。

### Aspose.PSD 可以免費使用嗎？
Aspose 提供免費試用版，但正式環境必須購買授權。測試可參考 [temporary license](https://purchase.aspose.com/temporary-license/)。

### 哪裡可以找到完整文件說明？
請參閱 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)。

### 使用 Aspose.PSD 時遇到問題該怎麼辦？
可前往 [Aspose Support Forum](https://forum.aspose.com/c/psd/34) 尋求協助。

## 其他常見問答

**Q: 將 PSD 轉換為 PNG 時會保留圖層效果嗎？**  
A: 會，只要以 `PngColorType.TruecolorWithAlpha` 儲存，大部分視覺效果會被光柵化到 PNG 中。

**Q: 能否批次處理多個 PSD 檔案？**  
A: 完全可以。將程式碼包在迴圈中，遍歷資料夾內的 PSD 檔案即可。

**Q: 可以設定 PNG 的壓縮等級嗎？**  
A: `PngOptions` 類別提供 `setCompressionLevel(int)` 方法，可進行細部調整。

**Q: 必須手動關閉影像物件嗎？**  
A: `PsdImage` 實作 `Closeable` 介面；請在 `finally` 區塊中呼叫 `im.close()`，或使用 try‑with‑resources。

**Q: 旋轉後的 PNG 會保留原始尺寸嗎？**  
A: 旋轉 90° 或 270° 會交換寬高，PNG 會呈現新的方向尺寸。

## 結論
透過 Aspose.PSD for Java，您只需幾行程式碼即可 **將 PSD 轉換為 PNG** 並 **旋轉 PSD** 圖層。此方法免除 Photoshop 的需求，加速自動化工作流程，且讓您完整掌控影像輸出。立即在自己的專案中試試看，體驗節省的時間與效能！

---

**最後更新：** 2025-12-15  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}