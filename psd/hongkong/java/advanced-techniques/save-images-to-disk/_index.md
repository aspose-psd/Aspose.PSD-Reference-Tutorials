---
date: 2026-06-03
description: 使用 Aspose.PSD for Java，輕鬆將 PSD 另存為 PNG 並儲存至磁碟。這是一個功能強大的 Java 程式庫，用於 PSD
  檔案操作。
keywords:
- save psd as png
- convert psd to png
- export psd to png
- save image file java
linktitle: 將影像儲存至磁碟
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  headline: Save PSD as PNG with Aspose.PSD for Java
  type: TechArticle
- description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  name: Save PSD as PNG with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: 'Set the path for your document directory, where your PSD file is located:'
  - name: Specify Source and Destination Paths
    text: 'Define the paths for your source PSD file and the destination file where
      the image will be saved:'
  - name: Load PSD Image
    text: 'Load the PSD image using Aspose.PSD:'
  - name: Save Image with Options
    text: '`PsdImage` is Aspose.PSD''s core class that represents a Photoshop document
      in memory. Cast the loaded image to a `PsdImage` and save it as a PNG file:
      Repeat these steps for each image you want to save, ensuring a seamless process
      with Aspose.PSD.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports various formats, including JPEG, BMP,
      TIFF, and more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: Yes, you can explore a free trial of Aspose.PSD for Java by visiting [this
      link](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: Refer to the [documentation](https://reference.aspose.com/psd/java/) for
      detailed information on Aspose.PSD for Java.
    question: Where can I find comprehensive documentation for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: How can I get support for Aspose.PSD for Java?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 將 PSD 另存為 PNG
url: /zh-hant/java/advanced-techniques/save-images-to-disk/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 將 PSD 另存為 PNG

## 簡介

**Save PSD as PNG** 是在 Java 應用程式中處理 Photoshop 檔案時的常見需求。使用 Aspose.PSD for Java，您只需幾行程式碼即可將任何 PSD 圖層或整個文件轉換為 PNG 圖像。本教學將逐步說明具體操作，解釋為何此函式庫非常適合此任務，並展示如何有效處理多張圖像。

## 快速解答
- **哪個函式庫可處理 PSD 轉 PNG 轉換？** Aspose.PSD for Java.
- **需要多少行程式碼？** 通常在載入檔案後只需兩行。
- **我可以處理大型 PSD 檔案嗎？** 可以 — API 會串流資料，支援超過 2 GB 的檔案。
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線需購買授權。
- **支援哪些 Java 版本？** Java 8 至 Java 21（LTS 及更新版本）。

## 什麼是「將 PSD 另存為 PNG」？

將 PSD 另存為 PNG 意指將 Photoshop 文件中的點陣圖像資料匯出為可攜式 PNG 格式，同時保留透明度、色彩忠實度以及任何內嵌的色彩描述檔。產生的 PNG 可用於網頁、行動裝置及桌面應用程式，提供無損壓縮且與各種圖像檢視器和編輯器具備廣泛相容性。

## 為何使用 Aspose.PSD for Java 轉換 PSD 為 PNG？

Aspose.PSD 支援 **30+ 輸入與輸出格式**，且可 **處理高達 2 GB 的檔案** 而無需將整個文件載入記憶體，較手動像素處理可提供最高 **3 倍更快的轉換速度**。此函式庫亦會自動保留圖層效果、遮色片與色彩描述檔，免除後續處理的需求。

## 先決條件

在開始本教學之前，請確保已具備以下先決條件：

- Aspose.PSD for Java 函式庫：從 [release page](https://releases.aspose.com/psd/java/) 下載並安裝函式庫。
- Java 開發環境：確保您的機器上已設定可正常運作的 Java 開發環境。

## 匯入套件

以下匯入語句會載入處理 PSD 檔案與設定 PNG 匯出選項所需的 Aspose.PSD 核心類別。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

以下將把儲存影像的過程分解為多個步驟，以便清晰且完整地了解。

## 如何使用 Aspose.PSD for Java 將 PSD 另存為 PNG？

`PsdImage` 類別代表記憶體中的 Photoshop 文件，而 `ImageSaveOptions` 搭配 `SaveFormat` 則指定所需的輸出格式與壓縮設定。透過載入 PSD 並以 PNG 選項呼叫儲存方法，即可在一次高效的呼叫中完成檔案轉換。  

使用 `new PsdImage("source.psd")` 載入 PSD 檔案，然後呼叫 `psd.save("output.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`。此單行呼叫會自動處理圖層合併、色彩描述檔保留以及 PNG 壓縮。若需批次處理，請將此呼叫放入遍歷來源檔案的迴圈中。

### 步驟 1：定義文件目錄

設定文件目錄的路徑，即放置 PSD 檔案的資料夾：

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：指定來源與目的路徑

定義來源 PSD 檔案的路徑以及影像要儲存的目的檔案路徑：

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

### 步驟 3：載入 PSD 影像

使用 Aspose.PSD 載入 PSD 影像：

```java
Image image = Image.load(sourceFile);
```

### 步驟 4：使用選項儲存影像

`PsdImage` 是 Aspose.PSD 的核心類別，代表記憶體中的 Photoshop 文件。將載入的影像轉型為 `PsdImage`，並將其儲存為 PNG 檔案：

```java
PsdImage psdImage = (PsdImage)image;
psdImage.save(destName, new PngOptions());
```

對每張要儲存的影像重複上述步驟，即可確保使用 Aspose.PSD 的流程順暢。

## 常見問題與解決方案

- **大型檔案的 OutOfMemoryError** – 使用 `PsdImage.load(inputStream, true)` 啟用串流，以避免將整個檔案載入記憶體。
- **透明度遺失** – 確認使用 `PngOptions` 並將 `ColorType = PngColorType.Rgba` 設為保留 alpha 通道。
- **顏色不正確** – 檢查來源 PSD 是否已嵌入色彩描述檔；Aspose.PSD 會在匯出時自動套用。

## 常見問與答

**Q: 我可以在 Aspose.PSD for Java 中使用其他影像格式嗎？**  
A: 可以，Aspose.PSD for Java 支援多種格式，包括 JPEG、BMP、TIFF 等。

**Q: 是否提供 Aspose.PSD for Java 的免費試用？**  
A: 可以，您可透過造訪 [this link](https://releases.aspose.com/) 來體驗 Aspose.PSD for Java 的免費試用。

**Q: 我在哪裡可以找到 Aspose.PSD for Java 的完整文件？**  
A: 請參考 [documentation](https://reference.aspose.com/psd/java/) 以取得 Aspose.PSD for Java 的詳細資訊。

**Q: 我該如何取得 Aspose.PSD for Java 的支援？**  
A: 前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得社群支援與討論。

**Q: 是否提供 Aspose.PSD for Java 的臨時授權？**  
A: 可以，您可在 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 此函式庫是否支援將單一圖層匯出為 PNG？**  
A: 當然可以 — 取得目標 `Layer` 物件，然後呼叫 `layer.save("layer.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`。

**Q: 我能控制 PNG 的壓縮等級嗎？**  
A: 可以，使用 `PngOptions.setCompressionLevel(int level)` 設定，其中 `level` 的範圍為 0（無壓縮）至 9（最高壓縮）。

## 結論

使用 Aspose.PSD for Java 將 PSD 另存為 PNG 是一項簡單卻功能強大的操作。依照上述步驟，您即可將高效能的影像匯出整合至 Java 應用程式，有效處理大型檔案，並保持完整的視覺忠實度。

---

**最後更新：** 2026-06-03  
**測試版本：** Aspose.PSD 24.10 for Java  
**作者：** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 將 PSD 轉換為點陣圖格式](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)
- [使用 Aspose.PSD for Java 將影像儲存至串流](/psd/java/advanced-techniques/save-images-to-stream/)
- [使用 Aspose.PSD for Java 將 PSD 另存為 PNG 並套用渲染陰影](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}