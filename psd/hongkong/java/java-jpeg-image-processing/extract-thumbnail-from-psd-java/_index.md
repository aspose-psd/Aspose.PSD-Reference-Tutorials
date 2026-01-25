---
date: 2026-01-25
description: 學習如何使用 Aspose.PSD for Java 從 PSD 檔案提取縮圖。跟隨此一步一步的指南，快速載入、提取並儲存縮圖。
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: 在 Java 中從 PSD 提取縮圖
url: /zh-hant/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 PSD 中提取縮圖（Java）

## 簡介
在本教學中，您將學習 **如何從 PSD 中提取縮圖**，使用 Aspose.PSD for Java 函式庫。縮圖是嵌入於 PSD 文件內的微型預覽圖像，提取它們可協助您快速產生預覽、建立圖庫，或在僅需原始作品的小尺寸表示時減少儲存空間。我們將從專案設定一路說明至將提取的縮圖儲存為標準圖像檔案。

## 快速解答
- **本教學涵蓋什麼內容？** 使用 Aspose.PSD for Java 從 PSD 文件中提取並儲存縮圖。  
- **需要哪個函式庫？** Aspose.PSD for Java（可從官方 Aspose 網站下載）。  
- **是否需要授權？** 生產環境需要臨時或完整授權；亦提供免費試用版。  
- **使用什麼輸出格式？** 範例將縮圖儲存為 JPEG 檔案，但可選擇任何支援的格式。  
- **實作需要多久？** 對於熟悉基本 Java 概念的開發者，大約 5‑10 分鐘。

## 什麼是「從 PSD 中提取縮圖」？
從 PSD 中提取縮圖是指讀取 Photoshop 在檔案資源區段中儲存的小型預覽圖像。此預覽通常是完整畫布的低解析度版本，適合在檔案總管或網站圖庫中快速載入。

## 為什麼使用 Aspose.PSD 提取縮圖？
- **速度：** 無需在圖形編輯器中開啟完整 PSD；縮圖已內嵌。  
- **自動化：** 非常適合批次處理大型影像庫。  
- **跨平台：** 可在任何支援 Java 的作業系統上執行，無需 Photoshop。  
- **格式彈性：** 可將縮圖轉換為 JPEG、PNG 或 Aspose.PSD 支援的任何格式。

## 前置條件
在開始之前，請確保已完成以下設定：
- 已在系統上安裝 Java Development Kit for Java 函式庫。可從 [here](https://releases.aspose.com/psd/java/) 下載。  
- 具備基本的 Java 程式設計知識。

## 匯入套件
要開始使用，請在 Java 類別中加入必要的 Aspose.PSD 套件：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## 如何使用 Aspose.PSD for Java 從 PSD 中提取縮圖
以下為逐步指南。每一步都包含簡要說明，並附上您需要複製的完整程式碼。

### 步驟 1：載入 PSD 檔案
首先，載入包含您想提取之縮圖的 PSD 檔案。
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
將 `"Your_Document_Directory/"` 替換為 PSD 檔案所在的目錄路徑，將 `"your_file.psd"` 替換為 PSD 檔案名稱。

### 步驟 2：遍歷影像資源
遍歷影像資源以尋找縮圖資源。
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```

### 步驟 3：儲存提取的縮圖
前一步的程式碼已將縮圖儲存為同一目錄下名為 `extracted_thumbnail.jpg` 的 JPEG 檔案。您可透過調整 `save` 方法的參數來變更檔名或格式。

### 步驟 4：處理不同的縮圖類型
如果您的 PSD 檔案可能包含多種縮圖，例如 `Thumbnail4Resource`，您可以以相同方式擴充邏輯來處理這些情況。只需在迴圈內加入 `instanceof Thumbnail4Resource` 檢查，並依相同模式處理即可。

## 常見問題與解決方案
- **未找到縮圖：** 並非所有 PSD 檔案都包含縮圖資源。請在 Photoshop 中確認來源檔案（檔案 → 匯出 → 縮圖），或使用包含預覽的其他 PSD。  
- **不支援的影像格式錯誤：** 請確認您使用的 Aspose.PSD 為支援目標格式的最新版本。  
- **儲存時的權限錯誤：** 確認應用程式對輸出目錄具有寫入權限。

## 常見問答

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一個 Java 函式庫，允許開發人員以程式方式處理 PSD 及其他影像檔案格式。

**Q: 在哪裡可以找到 Aspose.PSD for Java 的更多文件？**  
A: 您可參考 [documentation](https://reference.aspose.com/psd/java/) 以取得詳細的 API 參考與範例。

**Q: 購買前可以免費試用 Aspose.PSD 嗎？**  
A: 可以，您可下載 [free trial](https://releases.aspose.com/) 以評估此函式庫的功能。

**Q: 如何取得 Aspose.PSD 的臨時授權？**  
A: 可從 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: Aspose.PSD 適用於商業用途嗎？**  
A: 可以，Aspose.PSD 可依其授權條款用於個人與商業專案。

## 結論
在本教學中，我們探討了如何使用 Aspose.PSD for Java **從 PSD 中提取縮圖**。依照上述步驟，您即可有效取得並儲存嵌入於 PSD 文件中的縮圖，實現更快速的預覽與精簡的影像工作流程。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-01-25  
**測試環境：** Aspose.PSD for Java (latest release)  
**作者：** Aspose