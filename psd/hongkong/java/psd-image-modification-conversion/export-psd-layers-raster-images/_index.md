---
date: 2026-03-26
description: 學習使用 Aspose.PSD for Java 將 PSD 圖層匯出為 PNG。將 PSD 轉換為光柵圖像，並高效批量匯出 PSD 圖層。
linktitle: Export psd layers to png using Java
second_title: Aspose.PSD Java API
title: 使用 Java 匯出 PSD 圖層至 PNG
url: /zh-hant/java/psd-image-modification-conversion/export-psd-layers-raster-images/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 匯出 psd 圖層為 png

## 簡介

在數位設計的世界裡，處理多圖層影像既是福也是挑戰。想像一下，你已花了數小時在 Photoshop（PSD 格式）中打造出一幅精彩的圖像，包含多個讓設計栩栩如生的圖層。現在，你可能想要獨立 **export psd layers to png** 以供後續使用。這時 Aspose.PSD for Java 就顯現其價值，能自動化將 PSD 檔案中的每個圖層轉換為高品質的點陣圖（如 PNG）的繁瑣工作。在本完整指南中，我們將一步步帶領你完成整個流程，從環境設定到僅需幾行程式碼即可批次匯出 psd 圖層。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.PSD for Java 將每個 PSD 圖層匯出為 PNG 檔案。  
- **主要好處？** 相較於在 Photoshop 手動提取，可節省數小時時間。  
- **先決條件？** JDK 8 以上、Aspose.PSD 函式庫，以及範例 PSD 檔案。  
- **可以匯出至其他點陣格式嗎？** 可以——你也能將 psd 轉換為 BMP、TIFF 或 JPEG 等點陣格式。  
- **支援批次處理嗎？** 當然支援；程式碼中的迴圈可讓你一次執行批次匯出 psd 圖層。

## 什麼是「psd layers to png」？

匯出 **psd layers to png** 意味著將 Photoshop 文件中的每個單獨圖層保存為獨立的 PNG 圖像。PNG 能保留透明度，非常適合用於網頁圖形、UI 資源以及後續的影像處理。

## 為什麼使用 Aspose.PSD for Java？

- **不需 Photoshop** – 可在任何伺服器或 CI 環境中運行。  
- **高保真度** – 保留圖層效果、遮罩與 Alpha 通道。  
- **可擴充** – 非常適合在自動化流水線中批次匯出 psd 圖層。  

## 先決條件

在深入程式碼之前，請確保已具備以下項目：

1. **Java Development Kit (JDK)** – 8 版或以上。  
2. **Aspose.PSD for Java** – 從 [Aspose Releases](https://releases.aspose.com/psd/java/) 下載最新函式庫。  
3. **IDE** – IntelliJ IDEA、Eclipse，或任何你偏好的編輯器。  
4. **範例 PSD 檔案** – 例如 `sample.psd`，放置於專案資料夾中。  

現在一切就緒，讓我們開始編寫程式吧！

## 匯入套件

首先，從 Aspose.PSD 函式庫匯入所需的類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

這些匯入讓你能使用影像載入、PNG 選項以及圖層操作功能。

## 步驟 1：定義文件目錄

指定來源 PSD 與產生的 PNG 檔案所在的位置：

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為指向 `sample.psd` 的絕對或相對路徑。

## 步驟 2：載入 PSD 檔案

將 PSD 載入 `PsdImage` 物件，以便操作其圖層：

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

將其轉型為 `PsdImage` 後，即可使用圖層專屬功能。

## 步驟 3：設定 PNG 選項

設定 PNG 匯出參數。使用 `TruecolorWithAlpha` 可保留透明度：

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## 步驟 4：遍歷圖層並分別匯出

遍歷每個圖層並將其保存為單獨的 PNG 檔案。此迴圈可自動執行 **batch export psd layers**：

```java
for (int i = 0; i < psdImage.getLayers().length; i++) {
    // Convert and save the layer to PNG file format.
    psdImage.getLayers()[i].save(dataDir + String.format("layer_out%d.png", i + 1), pngOptions);
}
```

每次迭代會產生 `layer_out1.png`、`layer_out2.png` 等檔案。

## 常見問題與解決方案

- **FileNotFoundException** – 請確認 `dataDir` 指向正確的資料夾且 `sample.psd` 存在。  
- **OutOfMemoryError** – 若 PSD 檔案非常大，請考慮分批處理圖層或增大 JVM 堆積大小（`-Xmx`）。  
- **Missing Transparency** – 請確保已設定 `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)`；否則 PNG 會在沒有 Alpha 通道的情況下儲存。

## 常見問答

### 什麼是 Aspose.PSD for Java？

Aspose.PSD for Java 是一套功能強大的函式庫，讓開發人員能在不需要 Adobe Photoshop 的情況下，建立、修改、轉換與呈現 Photoshop 檔案。

### 我可以將圖層匯出為 PNG 以外的格式嗎？

可以，Aspose.PSD 支援 BMP、TIFF、JPEG 以及許多其他點陣格式。只需實例化相應的選項類別（例如 `JpegOptions`），並將其傳遞給 `save` 方法即可。

### 是否提供 Aspose.PSD 的免費試用？

當然！你可以從他們的 [free trial page](https://releases.aspose.com/) 下載並免費試用 Aspose.PSD。

### 使用 Aspose.PSD 時遇到問題該怎麼辦？

你可以向 Aspose 社群尋求協助與支援。請前往他們的支援論壇 [here](https://forum.aspose.com/c/psd/34)。

### 哪裡可以購買 Aspose.PSD 的授權？

你可以輕鬆在他們的購買頁面 [here](https://purchase.aspose.com/buy) 購買 Aspose.PSD 授權。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-26  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose