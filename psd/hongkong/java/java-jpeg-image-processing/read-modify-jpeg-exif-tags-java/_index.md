---
date: 2026-10-03
description: 了解如何在 Java 中使用 Aspose.PSD for Java 讀取圖像元資料並修改 JPEG EXIF 標籤，本分步指南適合高效處理圖像元資料的開發人員。
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: 在 Java 中讀取與修改 JPEG EXIF 標籤
og_description: 了解如何在 Java 中使用 Aspose.PSD for Java 讀取圖像元資料並修改 JPEG EXIF 標籤。本指南提供逐步程式碼示例，說明如何提取與更新
  EXIF 資訊。
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: 如何在 Java 中讀取圖像元資料並修改 JPEG EXIF 標籤
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: 如何在 Java 中讀取圖像元資料並修改 JPEG EXIF 標籤
url: /zh-hant/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中讀取與修改 JPEG EXIF 標籤

## 簡介
如果您需要從 JPEG 檔案 **java read image metadata** 並以程式方式更改它，您已來對地方。在本教學中，我們將示範如何使用 Aspose.PSD for Java 來提取與更新 EXIF 標籤。完成後，您將能取得相機資訊、方向以及自訂欄位，並將它們寫回檔案——全部不需圖形編輯器。

## 快速回答
- **哪個函式庫在 Java 中處理 JPEG EXIF？** Aspose.PSD for Java.
- **讀取 EXIF 需要多少行程式碼？** 約三行（在載入影像後）。
- **可以修改 EXIF 標籤嗎？** 可以，您可以變更任何標準或自訂標籤並儲存結果。
- **支援的影像格式？** 超過 150 種格式，包括 PSD、JPEG、PNG、TIFF 與 BMP。
- **最低 Java 版本？** Java 7 或以上。

## 為何使用 Aspose.PSD for Java？
Aspose.PSD 支援 **150+ image formats**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案，為大型相片集提供快速、低記憶體的中繼資料操作。它亦提供簡易的 API 以讀寫 EXIF、IPTC 與 XMP 資料，使成千上萬張影像的批次處理既高效又可靠。

## 先決條件
1. **Java Development Kit (JDK)** – 確保您已安裝 JDK 11 或更新版本。您可從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java library** – 從 [Aspose releases page](https://releases.aspose.com/psd/java/) 取得最新的 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
4. **Basic Java knowledge** – 您應熟悉建立專案與加入外部 JAR。

## 什麼是 Java 讀取影像中繼資料？
Java read image metadata 指的是使用 Java 程式碼以程式方式存取嵌入於影像檔案中的資訊，如 EXIF、IPTC 與 XMP。此類中繼資料可能包含相機設定、時間戳記、GPS 座標、版權聲明與使用者評論，使應用程式能根據描述性資料來組織、搜尋與操作影像。

## 匯入套件
首先，將 Aspose.PSD JAR 加入專案的 classpath，並匯入所需的類別。

`com.aspose.psd` 套件提供載入影像與存取其資源的核心 API。

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 如何在 Java 中讀取 JPEG 檔案的影像中繼資料？
使用 `PsdImage.load("image.jpg")` 載入 JPEG，找到包含 EXIF 資料的縮圖資源，然後呼叫 `ExifData.read()` 取得填充好的 `ExifData` 物件。此一步驟方法讓您完整存取所有標準 EXIF 欄位以及任何自訂標籤。

## 步驟 1：載入 PSD 影像
PsdImage 是 Aspose.PSD 用來表示 PSD 檔案的類別，提供存取其資源與中繼資料的方法。  
在此步驟中，我們將載入欲讀取 EXIF 資料的 PSD 影像。請確保您的影像位於正確的目錄。

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## 步驟 2：遍歷影像資源
ThumbnailResource 代表儲存在 PSD 檔案中的縮圖影像，通常包含嵌入的 EXIF 資料。  
影像載入後，下一步是遍歷其資源以尋找縮圖資源，該資源通常包含 EXIF 資料。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## 步驟 3：提取 EXIF 資料
JpegExifData 是用來保存從 JPEG 影像提取之 EXIF 資訊的類別，讓您能讀取與修改個別標籤。  
現在我們已取得縮圖資源，可以從中提取 EXIF 資料。EXIF 資料包含相機擁有者名稱、光圈值、方向等寶貴資訊。

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## 步驟 4：修改 EXIF 資料
讀取 EXIF 資料後，您可能想修改其中的某些欄位。以下示範如何操作：

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## 步驟 5：儲存變更
最後，於修改 EXIF 資料後，將變更儲存為新的 PSD 檔案。

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## 常見問題與解決方案
- **Missing thumbnail resource** – 某些 JPEG 會將 EXIF 直接儲存在主影像標頭中。若缺少縮圖資源，請改用 `image.getExifData()`。  
- **Large files cause OutOfMemoryError** – 確保 JVM 具有足夠的堆記憶體（`-Xmx2g`），或使用 `PsdImage.load(inputStream, loadOptions)` 以串流模式處理影像。  
- **Unsupported tag types** – Aspose.PSD 支援所有標準 EXIF 標籤；自訂標籤可能需要手動的位元組層級處理。

## 常見問答

**Q: 什麼是 EXIF 資料？**  
A: EXIF（可交換影像檔案格式）中繼資料儲存相機設定、時間戳記、GPS 座標以及嵌入於 JPEG 與其他影像檔案中的其他資訊。

**Q: 我可以免費使用 Aspose.PSD for Java 嗎？**  
A: 您可從 [Aspose releases page](https://releases.aspose.com/) 取得免費試用版。

**Q: Aspose.PSD for Java 是否相容所有 Java 版本？**  
A: Aspose.PSD for Java 支援 Java SE 7 及以上版本。

**Q: 在哪裡可以找到更多 Aspose.PSD for Java 的文件？**  
A: 請參閱 [documentation](https://reference.aspose.com/psd/java/) 以取得更多細節。

**Q: 如何取得 Aspose.PSD for Java 的支援？**  
A: 您可從 [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/) 獲得支援。

## 結論
依照上述步驟，您即可從任何 JPEG **java read image metadata**，調整所需的 EXIF 欄位，並將更新後的資料寫回檔案——僅需幾行簡潔的 Java 程式碼。Aspose.PSD 豐富的 API 使中繼資料處理可靠且效能卓越，您可將其整合至批次處理管線、相片管理工具或任何需要操作影像資訊的應用程式中。

---

**最後更新：** 2026-10-03  
**測試環境：** Aspose.PSD for Java 24.5  
**作者：** Aspose

## 相關教學

- [在 Java 中使用 Aspose 讀取特定 EXIF 標籤資訊 (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [使用 Aspose.PSD for Java 在 PSD 檔案中建立 XMP 中繼資料](/psd/java/image-editing/create-xmp-metadata/)
- [使用 Aspose.PSD for Java 調整影像大小 – 繪製形狀與基本影像操作](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}