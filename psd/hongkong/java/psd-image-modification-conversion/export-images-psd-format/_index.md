---
date: 2026-03-23
description: 了解如何使用 Aspose.PSD for Java 將圖像儲存為 PSD。一步一步的指南，設定 PSD 色彩模式，將位圖轉換為 PSD
  並以程式方式匯出圖像。
linktitle: Export Images to PSD Format with Java
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD 在 Java 中將圖像另存為 PSD
url: /zh-hant/java/psd-image-modification-conversion/export-images-psd-format/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 的 Java 將圖像儲存為 PSD

## 使用 Java 保存圖像為 PSD

在本教學中，您將學習 **如何將圖像儲存為 PSD**，使用 Java 以及 Aspose.PSD 函式庫。對許多平面設計開發者而言，處理具圖層的 Photoshop 檔案是日常工作，將 PSD 檔案的產生自動化可以大幅提升工作流程效率。我們將逐步說明設定 PSD 顏色模式、建立 bitmap，並將該 bitmap 轉換為 PSD 檔案——所有您快速入門所需的內容。讓我們開始吧！

## 快速解答
- **需要什麼函式庫？** Aspose.PSD for Java（可從官方網站下載）。  
- **可以設定顏色模式嗎？** 可以 – 使用 `PsdOptions.setColorMode()` 來選擇 RGB、CMYK 等。  
- **支援將 bitmap 轉換為 PSD 嗎？** 當然可以；從尺寸或現有 bitmap 建立 `PsdImage` 並儲存即可。  
- **生產環境需要授權嗎？** 非試用版需購買商業授權。  
- **需要哪個 Java 版本？** Java 8 或以上。

## 什麼是「將圖像儲存為 PSD」？

將圖像儲存為 PSD 意指將點陣圖匯出為 Adobe Photoshop 原生的具圖層格式。這讓後續工具（如 Photoshop、GIMP 等）能保留圖層、通道與可編輯性。使用 Aspose.PSD，您可以在不開啟 Photoshop 的情況下程式化產生 PSD 檔案。

## 為什麼使用 Aspose.PSD for Java？

- **完整控制** 顏色模式、壓縮方式以及 Photoshop 版本相容性。  
- **無外部相依性** – 純 Java，適合伺服器端渲染。  
- **高效能** – 適用於成千上萬圖像的批次處理。  

## 前置條件

在開始之前，請確保您具備以下條件：

1. **基本的 Java 知識** – 需要能編譯與執行 Java 程式。  
2. **Aspose.PSD for Java 函式庫** – 可於[此處下載](https://releases.aspose.com/psd/java/)。  
3. **Java Development Kit (JDK)** – 在機器上安裝 JDK 8 或更新版本。  
4. **IDE 或文字編輯器** – 如 IntelliJ IDEA、Eclipse、VS Code，或任何您喜歡的編輯器。  
5. **了解影像概念** – 顏色模式、壓縮與 bitmap 基礎有助於學習，但非必須。  

全部準備好了嗎？太好了，讓我們繼續。

## 匯入套件

首先，匯入我們將從 Aspose.PSD 函式庫中使用的類別：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

這些匯入讓我們能使用繪圖工具、顏色處理以及 PSD 專屬選項。

## 步驟 1：初始化文件目錄

定義產生的 PSD 檔案要儲存的位置：

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為絕對路徑（例如 `"C:/Images/"`）或專案內的相對路徑。

## 步驟 2：建立新圖像（將 Bitmap 轉換為 PSD）

現在我們建立一個空白 bitmap，稍後會透過 PSD 選項 **將 bitmap 轉換為 PSD** 並儲存：

```java
PsdImage bmpImage = new PsdImage(300, 300);
```

如有需要，可自行調整 `300, 300` 為您想要的尺寸。

## 步驟 3：填充圖像資料

為 bitmap 加入一些圖形，使最終的 PSD 不會只是空白畫布：

```java
Graphics graphics = new Graphics(bmpImage);
graphics.clear(Color.getWhite());
Pen pen = new Pen(Color.getBrown());
graphics.drawRectangle(pen, bmpImage.getBounds());
```

- `graphics.clear(Color.getWhite())` 會將整個畫布填成白色。  
- 棕色筆會繪製一個矩形，標示圖像邊界。

## 步驟 4：設定 PSD 選項（設定 PSD 顏色模式）

在此我們設定檔案的儲存方式。這裡會 **設定 PSD 顏色模式** 為 RGB，選擇壓縮方式，並指定 Photoshop 版本：

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setColorMode(ColorModes.Rgb);
psdOptions.setCompressionMethod(CompressionMethod.Raw);
psdOptions.setVersion(4);
```

- `ColorModes.Rgb` – 網頁與螢幕圖形最常用的顏色模式。  
- `CompressionMethod.Raw` – 不壓縮像素資料，保證最高品質。  
- `setVersion(4)` – 以 Photoshop 4.0 格式儲存，具廣泛相容性。

## 步驟 5：儲存圖像

最後，將 bitmap 匯出為 PSD 檔案——這就是核心的 **將圖像儲存為 PSD** 操作：

```java
bmpImage.save(dataDir + "ExportImageToPSD_output.psd", psdOptions);
```

檔案 `ExportImageToPSD_output.psd` 會出現在您先前指定的目錄中。

## 常見使用情境

- **自動化報告產生**，圖表需在 Photoshop 中可編輯。  
- **批次轉換** PNG/JPEG 資產為 PSD，供需要圖層的設計師使用。  
- **伺服器端影像合成**，為向客戶提供 PSD 模板的網路服務。

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| **File not found** 錯誤（儲存時找不到檔案） | 確認 `dataDir` 以路徑分隔符 (`/` 或 `\\`) 結尾，且資料夾已存在。 |
| **Blank image**（儲存後為空白圖像） | 確保已呼叫 `graphics.clear()` 並在儲存前繪製了內容。 |
| **Unsupported color mode**（不支援的顏色模式） | 若需 CMYK 輸出，請使用 `ColorModes.Cmyk`，並相應調整繪圖內容。 |
| **LicenseException**（執行時授權例外） | 安裝有效的 Aspose.PSD 授權，或以試用模式執行（可能會出現評估水印）。 |

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套功能強大的 API，讓開發者在不使用 Adobe Photoshop 的情況下，建立、編輯、轉換與渲染 Photoshop PSD 檔案。

**Q: 我可以修改既有的 PSD 檔案嗎？**  
A: 可以，您可以使用 `new PsdImage("input.psd")` 開啟既有 PSD，進行修改後再儲存。

**Q: 有免費試用版嗎？**  
A: 當然有！您可於[此處](https://releases.aspose.com/)下載 Aspose.PSD 的免費試用版。

**Q: 哪裡可以找到更多文件說明？**  
A: 您可以參考完整的[文件說明](https://reference.aspose.com/psd/java/)，了解更多 Aspose.PSD 的使用方式。

**Q: 若遇到問題該如何取得支援？**  
A: 您可前往[Aspose 論壇](https://forum.aspose.com/c/psd/34)取得協助。

## 結論

現在您已了解如何使用 Java **將圖像儲存為 PSD**、如何 **設定 PSD 顏色模式**，以及如何 **將 bitmap 轉換為 PSD**，全部透過 Aspose.PSD 完成。此方法賦予您對 Photoshop 檔案的完整程式化控制，為自動化設計流程、動態影像產生以及與現有 Java 應用程式的無縫整合開啟新可能。請嘗試不同的顏色模式、尺寸與繪圖操作，打造符合您需求的 PSD 檔案。

---

**最後更新：** 2026-03-23  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}