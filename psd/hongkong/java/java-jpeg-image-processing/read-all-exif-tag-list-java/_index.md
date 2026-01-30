---
date: 2026-01-30
description: 學習如何使用 Aspose.PSD for Java 從 PSD 檔案讀取 EXIF 標籤。本分步指南將向您展示如何在 Java 中提取圖像
  EXIF 元資料。
linktitle: Read All EXIF Tag List in Java
second_title: Aspose.PSD Java API
title: 在 Java 中讀取 EXIF 標籤 – 讀取全部 EXIF 標籤清單
url: /zh-hant/java/java-jpeg-image-processing/read-all-exif-tag-list-java/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中讀取 EXIF 標籤 – 讀取全部 EXIF 標籤清單

### 簡介
如果您需要在 Java 應用程式中 **read EXIF tags** Photoshop (PSD) 檔案，Aspose.PSD for Java 能讓此工作變得簡單。在本教學中，我們將逐步說明如何載入 PSD、定位內嵌的 EXIF 中繼資料，並列印每一個標籤‑值對。完成後，您將了解如何 **read all EXIF** 資訊，這對於影像目錄管理、鑑識分析或自動化資產管理等任務至關重要。

### 快速解答
- **What does “read EXIF tags” mean?** 從影像檔案中提取嵌入的中繼資料（相機設定、時間戳記等）。  
- **Which library handles this in Java?** Aspose.PSD for Java。  
- **Do I need a license to try it?** 提供免費試用；正式使用時需購買授權。  
- **How many lines of code are needed?** 少於 30 行，如下例所示。  
- **Can I use this with other image formats?** 相同方法亦適用於 JPEG 的 EXIF 資料；PSD 檔案則將 EXIF 存於縮圖資源中。

## 在 PSD 檔案的情境下，什麼是「read EXIF tags」？
EXIF（Exchangeable Image File Format）標籤儲存相機特定資訊與其他中繼資料。雖然 PSD 主要是分層影像格式，但它可以包含一個縮圖資源，內部保存 JPEG EXIF 資料。讀取這些標籤即可在不開啟完整影像的情況下取得曝光、ISO、建立日期等細節。

## 為什麼使用 Aspose.PSD for Java 讀取 EXIF 標籤？
- **無需 Photoshop** – 可程式化操作 PSD 檔案。  
- **完整控制** – 直接存取縮圖及其 EXIF 區塊等低階資源。  
- **跨平台** – 可在任何相容 Java 的環境執行。  
- **效能佳** – 僅解析縮圖資源，降低記憶體使用。

### 前置條件
在開始之前，請確保您已具備：
- 已安裝 Java Development Kit (JDK)。  
- 如 IntelliJ IDEA 或 Eclipse 等 IDE。  
- 下載 Aspose.PSD for Java 程式庫，可從 [here](https://releases.aspose.com/psd/java/) 取得。

## 匯入套件
首先，從 Aspose.PSD for Java 匯入必要的類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import java.util.Properties;
```

## Step 1: Load the PSD File
載入檔案是任何 **load PSD file** 操作的第一步。請將佔位路徑替換為您的 PSD 文件所在位置。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "example.psd");
```

## Step 2: Iterate Over Image Resources to **read EXIF tags**
PSD 可能包含多個資源。我們會尋找縮圖資源，因為它們保存 JPEG EXIF 區塊。

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null) {
            // Process EXIF data properties
            for(int j = 0; j < exifData.getProperties().length; j++) {
                System.out.println(exifData.getProperties()[j].getId() + ": " + exifData.getProperties()[j].getValue());
            }
        }
    }
}
```

### 程式碼說明
1. **Loop through all resources** attached to the PSD.  
2. **Identify thumbnail resources** (`ThumbnailResource` or `Thumbnail4Resource`).  
3. **Extract the `JpegExifData`** object from the thumbnail’s JPEG options.  
4. **Iterate over each EXIF property**, printing the tag ID and its value – this is the core of **java extract exif** functionality.

## 常見問題與技巧
- **Null 檢查** – 必須確認 `exifData` 不為 null；某些 PSD 可能沒有 EXIF 資訊。  
- **資源類型** – 只有縮圖資源包含 EXIF，其他資源（例如圖層資訊）應忽略。  
- **效能** – 若只需少數標籤，可在找到目標後即中斷內層迴圈。

## 結論
依照上述步驟，您即可使用 Aspose.PSD for Java **read EXIF tags** 任意 PSD 檔案。此功能讓您能構建更完整的影像處理流程、自動化中繼資料擷取，並在不安裝 Photoshop 的情況下將 Photoshop 資產整合至 Java 系統。

## 常見問題
### What is Aspose.PSD for Java?
Aspose.PSD for Java 是一套讓 Java 開發者在不安裝 Photoshop 的前提下，操作 PSD 檔案的程式庫。

### Where can I find the Aspose.PSD for Java documentation?
您可以在 [here](https://reference.aspose.com/psd/java/) 找到相關文件。

### How can I obtain a temporary license for Aspose.PSD for Java?
請前往 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權方案。

### Does Aspose.PSD for Java support writing PSD files?
是的，該程式庫同時支援讀取與寫入 PSD 檔案。

### Where can I get support for Aspose.PSD for Java?
如需協助，請造訪 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)。

## Frequently Asked Questions

**Q: Can I extract EXIF data from a PSD that has no thumbnail?**  
A: No. EXIF information is stored only in thumbnail resources, so a PSD without a thumbnail won’t contain EXIF tags.

**Q: Is it possible to modify EXIF tags and save them back to the PSD?**  
A: Aspose.PSD allows you to edit the `JpegExifData` object and then save the PSD, but be aware that changing EXIF may affect the thumbnail’s integrity.

**Q: Does this approach work with large PSD files?**  
A: Yes, because we only read the thumbnail resource, memory consumption stays low even for multi‑megabyte PSDs.

**Q: Which version of Aspose.PSD is required?**  
A: Any recent version that includes the `com.aspose.psd.exif` package; the tutorial was tested with the latest release at the time of writing.

**Q: Can I use this code in a web application?**  
A: Absolutely. Just ensure the server has access to the PSD files and the Aspose.PSD JAR is on the classpath.

---

**Last Updated:** 2026-01-30  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}