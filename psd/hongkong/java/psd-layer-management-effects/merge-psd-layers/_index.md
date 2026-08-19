---
date: 2026-04-05
description: 學習如何使用 Aspose.PSD for Java 將 PSD 匯出為 PNG 並合併 PSD 圖層。內容包括將 PSD 轉換為 JPEG、設定
  JPEG 品質，以及 PSD 轉 TIFF 的技巧。
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: 將 PSD 匯出為 PNG 並使用 Aspose.PSD for Java 合併圖層
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 匯出 PSD 為 PNG 並合併圖層
url: /zh-hant/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 PSD 為 PNG 並合併圖層 – 使用 Aspose.PSD for Java

## 簡介

有沒有想過平面設計師如何在 Photoshop 中製作那些錯綜複雜、分層的圖像？祕訣往往就在 **匯出 PSD 為 PNG** 並智慧地合併圖層。如果你在 Java 中處理 PSD 檔案，掌握這些技巧可以協助你建立合成圖像、減少檔案大小，並為 Web 或行動裝置部署準備資產。在本教學中，我們將一步步說明如何使用 Aspose.PSD for Java **合併 PSD** 圖層，並示範如何將結果匯出為 PNG（必要時亦可為 JPEG/TIFF）。完成後，你將能直接從 Java 應用程式自動化圖層管理與匯出工作流程。

## 快速答覆
- **什麼程式庫負責在 Java 中處理 PSD 檔案？** Aspose.PSD for Java。  
- **我可以將 PSD 匯出為 PNG 嗎？** 可以 – 只需設定相應的影像選項。  
- **如何合併多個圖層？** 載入 PSD，操作 `Layer` 集合，然後儲存。  
- **如果需要 JPEG 品質控制該怎麼辦？** 使用 `JpegOptions` 並設定品質 (0‑100)。  
- **需要 Photoshop 嗎？** 不需要，Aspose.PSD 可獨立於 Adobe 軟體運作。

## 什麼是匯出 PSD 為 PNG？
匯出 PSD 為 PNG 指的是將 Photoshop 文件（PSD）轉換為可攜式網路圖形（PNG）檔案，同時可選擇性地將圖層平面化或合併。PNG 能保留透明度，且在網路上廣受支援，是 UI 資產的常用格式。

## 為什麼要以程式方式合併 PSD 圖層？
- **自動化：** 批次處理數百個檔案，無需手動點擊。  
- **效能：** 合併圖層可減少下游應用程式的渲染時間。  
- **檔案大小：** 平面化不必要的圖層可縮小最終影像。  
- **一致性：** 確保在不同建置間圖層順序與混合模式保持一致。

## 先決條件

1. **Aspose.PSD for Java Library** – 下載自 [Aspose.PSD for Java download link](https://releases.aspose.com/psd/java/)。  
2. **Java Development Environment** – IntelliJ IDEA、Eclipse，或任何你偏好的 IDE。  
3. **Sample PSD File** – 含多個圖層的檔案（例如 `layers.psd`）。  
4. **Basic Java Knowledge** – 你應該對類別與方法相當熟悉。  
5. **Aspose Temporary License (Optional)** – 若需處理較大檔案或移除試用限制，請取得 [temporary license](https://purchase.aspose.com/temporary-license/)。

## 匯入套件

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## 逐步指南

### 步驟 1：載入 PSD 檔案

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> 這會將 `layers.psd` 載入 `PsdImage` 物件，讓您完整存取其圖層。

### 步驟 2：檢查圖層（如何合併 psd）

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> 檢視圖層名稱可協助您決定哪些圖層要合併或保持分離。

### 步驟 3：設定影像選項（設定 jpeg 品質）

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> 如果您偏好 PNG 或 TIFF，可將 `JpegOptions` 替換為 `PngOptions` 或 `TiffOptions` – 這裡會設定 **psd 轉 tiff 轉換**。

### 步驟 4：儲存合併後的影像（匯出 psd 為 png）

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> `save` 方法會將合併結果寫入 `MergePSDlayers_output.png`。  
> *提示：* 若要匯出為 PNG，只需將 `jpgOptions` 換成 `PngOptions` 實例；其餘程式碼保持不變。

## 常見問題與解決方案

- **File‑not‑found exception:** Verify `dataDir` ends with a path separator (`/` or `\\`) and that `layers.psd` exists.  
- **Unexpected colors after merge:** Ensure the layer blending modes are compatible; you can adjust them via `layer.setBlendMode(...)`.  
- **Large output file:** Lower JPEG quality or use PNG compression levels to reduce size.

## 常見問答

**Q: 是否可以將合併後的影像儲存為 JPEG 以外的格式？**  
A: 當然可以！Aspose.PSD 支援 PNG、BMP、TIFF 等多種格式。只需使用對應的選項類別（`PngOptions`、`BmpOptions`、`TiffOptions`）。

**Q: 如何調整不同輸出格式的影像品質？**  
A: 每個選項類別都有自己的品質/壓縮設定。對於 JPEG，使用 `setQuality(int)`；對於 PNG，則可控制 `CompressionLevel`。

**Q: 使用 Aspose.PSD for Java 是否需要安裝 Photoshop？**  
A: 不需要。Aspose.PSD 可獨立於 Adobe Photoshop 運作，因而可在任何伺服器或 CI 環境執行。

**Q: 若在儲存前未設定影像選項會發生什麼事？**  
A: 程式庫會套用預設設定（例如 JPEG 品質 75）。自行指定選項可讓您掌控最終輸出。

**Q: 能否一次性將 PSD 直接轉換為 TIFF？**  
A: 可以 – 只需實例化 `TiffOptions`，然後呼叫 `psdImage.save("output.tiff", tiffOptions);`。

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}