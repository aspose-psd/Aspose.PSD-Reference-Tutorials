---
date: 2026-02-12
description: 學習如何使用 Aspose.PSD for Java 旋轉圖像以及將圖像旋轉 270 度。本指南涵蓋旋轉 PSD 檔案、翻轉圖像，以及在不使用
  Photoshop 的情況下將 PSD 轉換為 JPEG。
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 將圖像旋轉 270 度
url: /zh-hant/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將圖像旋轉 270 度（使用 Aspose.PSD for Java）

## 簡介

在本 **java 圖像處理教學** 中，您將快速且可靠地學會使用 Aspose.PSD for Java **將圖像旋轉** 270 度。無論您是在構建照片編輯工具、自動化批次轉換，或僅需重新定位 PSD 圖層，這個函式庫都能讓工作變得輕鬆。我們亦會介紹 **flip image java** 技術以及將旋轉後的 PSD 轉換為 JPEG 的方法，讓您在不使用 Photoshop 的情況下完成完整的端對端工作流程。

## 快速解答
- **哪個函式庫負責旋轉？** Aspose.PSD for Java  
- **範例使用的旋轉角度為多少？** 270 degrees  
- **我也可以翻轉圖像嗎？** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **如何儲存結果？** In the example we save as JPEG using `JpegOptions`  
- **在正式環境需要授權嗎？** A valid Aspose.PSD license is required for commercial use  

## 什麼是「將圖像旋轉 270 度」？

將圖像旋轉 270 度表示將圖片順時針旋轉整個圓的四分之三（或逆時針旋轉 90 度）。在許多圖形編輯情境中，這種方向與經過一系列變換後的原始直式版面相符。

## 為何使用 Aspose.PSD 完成此任務？

- **完整的 PSD 支援** – 可處理圖層、遮色片與調整物件。  
- **不需原生 Photoshop** – 可在任何 Java 執行環境上執行。  
- **簡易 API** – 只需一次方法呼叫（`rotateFlip`）即可完成旋轉與翻轉。  
- **輕鬆格式轉換** – 可直接匯出為 JPEG、PNG 或其他常見格式。  

## 如何使用 Aspose.PSD for Java 旋轉圖像

以下是一個逐步指南，帶您完成載入 PSD、套用 270° 旋轉、（可選）翻轉圖像，最後將結果儲存為 JPEG 的全過程。

### 先決條件

在開始之前，請確保您已具備：

- **Aspose.PSD for Java** 函式庫已安裝。您可在此下載並查看完整 API 參考 [here](https://reference.aspose.com/psd/java/)。  
- Java 開發環境（JDK 8 或以上）。  
- 一個您想要旋轉的 PSD 範例檔案。請在程式碼中將 `sourceFile` 變數更新為正確的檔案路徑。

### 匯入套件

首先從 Aspose.PSD 套件匯入必要的類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 步驟 1：載入圖像

建立指向來源 PSD 檔案的 `Image` 實例：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### 步驟 2：將圖像旋轉 270 度

使用 `rotateFlip` 方法搭配 `RotateFlipType.Rotate270FlipNone` 以在不進行翻轉的情況下完成 270 度旋轉：

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **專業提示：**如果您還需要水平或垂直翻轉圖像，可選擇其他 `RotateFlipType`，例如 `Rotate90FlipX` 或 `Rotate180FlipY`。這是執行 **flip image java** 操作最常見的方式。

### 步驟 3：將 PSD 轉換為 JPEG 並儲存

旋轉完成後，您可以使用相應的選項類別 **將 PSD 轉換為 JPEG**（或其他支援的格式）：

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

檔案 `RotatedImage_out.jpg` 現在包含已旋轉 270 度的原始 PSD 內容，並已儲存為 JPEG。

## 為何重要 – 真實案例

- **批次處理產品目錄** – 在發佈前將數十個 PSD 資產旋轉至統一方向。  
- **自動縮圖產生** – 無需開啟 Photoshop，即可為網站畫廊建立正確方向的預覽圖。  
- **行動應用程式後端** – 使用純 Java 在伺服器端重新定位使用者上傳的 PSD 檔案。  

## 常見問題與故障排除

| 問題 | 解決方案 |
|-------|----------|
| **圖像顯示顛倒** | 確認您使用了 `Rotate270FlipNone`。若要順時針旋轉 90 度，請使用 `Rotate90FlipNone`。 |
| **輸出檔案損壞** | 確保目標資料夾已存在且您具有寫入權限。 |
| **授權例外** | 在正式環境載入圖像前，安裝臨時或永久的 Aspose.PSD 授權。 |
| **需要在無 Photoshop 的情況下旋轉圖像** | 此 API 完全在程式碼中執行旋轉，免除對 Photoshop 的依賴。 |
| **想在同一次操作中翻轉圖像** | 使用其他 `RotateFlipType` 值，例如 `Rotate90FlipX`（涵蓋 **how to flip image**）。 |

## 常見問答

**Q: Aspose.PSD 是否相容於不同的圖像格式？**  
A: 是的，Aspose.PSD 支援 PSD、JPEG、PNG、BMP、GIF 以及許多其他點陣圖格式。

**Q: 我可以套用自訂旋轉，而不僅是預定義的翻轉嗎？**  
A: 當然可以！雖然 `RotateFlipType` 提供常見角度，您仍可結合多次呼叫或使用變換矩陣來實作任意角度的旋轉。

**Q: 如何將旋轉後的 PSD 轉換為其他格式，例如 PNG？**  
A: 在 `save` 方法中將 `JpegOptions` 換成 `PngOptions`（或相應的選項類別）。

**Q: 我可以在哪裡取得額外的支援或協助？**  
A: 如需社群協助，請造訪 [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)。

**Q: 是否提供免費試用？**  
A: 是的，您可透過 [free trial](https://releases.aspose.com/) 體驗 Aspose.PSD。

**Q: 如何取得臨時授權？**  
A: 若需要臨時授權，您可於 [here](https://purchase.aspose.com/temporary-license/) 取得。

**Q: 此方法能在無頭伺服器上運作嗎？**  
A: 是的，Aspose.PSD for Java 可在任何標準 JVM 環境執行，適合 CI/CD 流水線或雲端函式使用。

## 結論

您現在已學會使用 Aspose.PSD for Java **將圖像旋轉** 270 度、在需要時 **翻轉圖像**，以及如何將結果匯出為 JPEG。這個簡單的工作流程可整合至更大的 Java 圖像處理管線，讓您在不依賴 Photoshop 的情況下完整掌控 PSD 操作。

---

**最後更新：** 2026-02-12  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}