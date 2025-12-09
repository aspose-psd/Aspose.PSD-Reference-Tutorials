---
date: 2025-12-06
description: 學習如何使用 Aspose.PSD for Java 將圖像旋轉 270 度。本指南說明如何旋轉 PSD 檔案、翻轉圖像，以及將 PSD
  轉換為 JPEG。
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 將圖像旋轉 270 度
url: /zh-hant/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 旋轉圖像 270 度

## 介紹

在本 **java 圖像處理教學** 中，您將快速且可靠地學會使用 Aspose.PSD for Java **旋轉圖像 270 度**。無論您是構建照片編輯工具、自動化批次轉換，或僅需重新定位 PSD 圖層，該函式庫都能讓工作變得輕鬆。我們亦會簡介圖像翻轉以及將旋轉後的 PSD 轉換為 JPEG，讓您獲得完整的端對端工作流程。

## 快速解答
- **什麼函式庫負責旋轉？** Aspose.PSD for Java  
- **範例使用的旋轉角度為？** 270 degrees  
- **我也可以翻轉圖像嗎？** 是 – 使用 `RotateFlipType` 選項，例如 `Rotate90FlipX`  
- **如何儲存結果？** 在範例中，我們使用 `JpegOptions` 以 JPEG 格式儲存  
- **生產環境需要授權嗎？** 商業使用需擁有有效的 Aspose.PSD 授權  

## 什麼是「rotate image 270 degrees」？
將圖像旋轉 270 度表示將圖片順時針旋轉完整圓的四分之三（或逆時針旋轉 90 度）。在許多圖形編輯情境中，此方向在經過一系列變換後會與原始的直式版面相符。

## 為何使用 Aspose.PSD 完成此任務？
- **完整的 PSD 支援** – 可處理圖層、遮色片與調整物件。  
- **不需原生 Photoshop** – 可在任何 Java 執行環境上執行。  
- **簡易 API** – 單一方法呼叫（`rotateFlip`）即可處理旋轉與翻轉。  
- **輕鬆格式轉換** – 可直接匯出為 JPEG、PNG 或其他常見格式。  

## 前置條件

在開始之前，請確保您已具備：

- **Aspose.PSD for Java** 函式庫已安裝。您可下載並於 [此處](https://reference.aspose.com/psd/java/) 查看完整 API 參考。  
- Java 開發環境（JDK 8 或以上）。  
- 您想要旋轉的 PSD 範例檔案。請在程式碼中將 `sourceFile` 變數更新為檔案的正確路徑。  

## 匯入套件

首先從 Aspose.PSD 套件匯入所需的類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 如何旋轉 PSD – 步驟 1：載入圖像

建立指向來源 PSD 檔案的 `Image` 實例：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## 如何旋轉 PSD – 步驟 2：將圖像旋轉 270 度

使用 `rotateFlip` 方法搭配 `RotateFlipType.Rotate270FlipNone` 以在不進行翻轉的情況下完成 270 度旋轉：

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **專業提示：** 若您還需要水平或垂直翻轉圖像，請選擇其他 `RotateFlipType`，例如 `Rotate90FlipX` 或 `Rotate180FlipY`。

## 如何旋轉 PSD – 步驟 3：將 PSD 轉換為 JPEG 並儲存

旋轉完成後，您可以使用相應的選項類別 **將 PSD 轉換為 JPEG**（或其他支援的格式）：

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

檔案 `RotatedImage_out.jpg` 現在包含已旋轉 270 度的原始 PSD 內容，並以 JPEG 格式儲存。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **圖像顯示顛倒** | 請確認您使用了 `Rotate270FlipNone`。若要順時針旋轉 90 度，請使用 `Rotate90FlipNone`。 |
| **輸出檔案損毀** | 確保目標資料夾已存在且您具有寫入權限。 |
| **授權例外** | 在生產環境載入圖像前，請安裝臨時或永久的 Aspose.PSD 授權。 |

## 常見問答

**Q: Aspose.PSD 是否相容於不同的圖像格式？**  
A: 是，Aspose.PSD 支援 PSD、JPEG、PNG、BMP、GIF 以及許多其他點陣圖格式。

**Q: 我可以套用自訂旋轉，而非僅使用預定義的翻轉嗎？**  
A: 當然可以！雖然 `RotateFlipType` 提供常見角度，您仍可結合多次呼叫或使用變換矩陣來實現任意角度。

**Q: 如何將旋轉後的 PSD 轉換為其他格式，例如 PNG？**  
A: 在 `save` 方法中將 `JpegOptions` 換成 `PngOptions`（或相應的選項類別）。

**Q: 我可以在哪裡取得額外的支援或協助？**  
A: 可前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 取得社群協助。

**Q: 是否提供免費試用？**  
A: 有，您可透過 [免費試用](https://releases.aspose.com/) 來體驗 Aspose.PSD。

**Q: 如何取得臨時授權？**  
A: 若需要臨時授權，可於[此處](https://purchase.aspose.com/temporary-license/) 取得。

## 結論

您現在已學會如何使用 Aspose.PSD for Java **旋轉圖像 270 度**、在需要時翻轉圖像，並將結果匯出為 JPEG。這個簡潔的工作流程可整合至更大型的基於 Java 的圖像處理管線，讓您在不依賴 Photoshop 的情況下，完整掌控 PSD 的操作。

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}