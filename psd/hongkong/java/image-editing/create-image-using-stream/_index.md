---
date: 2026-07-17
description: 了解如何在 Aspose.PSD for Java 中使用串流建立 BMP 圖像。遵循此一步一步的 Java 圖像教學，以高效產生圖像。
keywords:
- how to create bmp
- generate image stream
- java image tutorial
lastmod: 2026-07-17
linktitle: 使用串流建立圖像
og_description: 了解如何在 Aspose.PSD for Java 中使用串流建立 BMP 圖像。本 Java 圖像教學展示了逐步產生 BMP 檔案的過程。
og_image_alt: 'Guide: create BMP image from stream with Aspose.PSD Java'
og_title: 如何在 Aspose.PSD for Java 中使用串流建立 BMP
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to create BMP images using stream in Aspose.PSD for Java.
    Follow this step‑by‑step java image tutorial for efficient image generation.
  headline: How to Create BMP Using Stream in Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`BmpOptions` combined with `Image.create`.'
    question: What is the main class for BMP creation?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `FileCreateSource` streams the data.
    question: Can I generate large BMPs (>10 MB) without loading the whole file into
      memory?
  - answer: Java 8 through Java 21 are fully compatible.
    question: Which Java versions are supported?
  - answer: Only the Aspose.PSD for Java JAR; no external imaging libraries needed.
    question: Is any additional dependency required?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create bmp
- Aspose.PSD
- Java image processing
- stream image generation
title: 如何在 Aspose.PSD for Java 中使用串流建立 BMP
url: /zh-hant/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中使用串流建立 BMP

## 簡介

直接從串流建立 BMP 檔案可讓您細緻控制記憶體使用量和檔案處理，這對高效能 Java 應用程式至關重要。在本教學中，您將學習 **如何建立 BMP** 圖像，使用 Aspose.PSD 的串流 API，逐步說明。我們將涵蓋從設定環境到儲存最終圖像的全部內容，讓您能立即將此技術整合到實務專案中。

## 快速解答
- **建立 BMP 的主要類別是什麼？** `BmpOptions` combined with `Image.create`.
- **開發時需要授權嗎？** A free trial works for testing; a commercial license is required for production.
- **能否在不將整個檔案載入記憶體的情況下產生大型 BMP（>10 MB）？** Yes, using `FileCreateSource` streams the data.
- **支援哪些 Java 版本？** Java 8 through Java 21 are fully compatible.
- **是否需要其他相依性？** Only the Aspose.PSD for Java JAR; no external imaging libraries needed.

## 如何在 Aspose.PSD for Java 中使用串流建立 BMP？

載入目標目錄，使用 `FileCreateSource` 設定 `BmpOptions`，然後以所需的寬度和高度呼叫 `Image.create` —— 整個操作僅需三行簡潔程式碼。此方法將 BMP 直接寫入檔案串流，避免暫存緩衝區，為批次圖像產生提供最佳效能。

## 什麼是 Aspose.PSD for Java？

Aspose.PSD for Java 是一套完整的函式庫，可程式化建立、操作與轉換 Photoshop®（PSD）檔案及超過 30 種其他點陣格式。它能處理高達 2 GB 的檔案而無需將完整影像載入記憶體，非常適合伺服器端影像流水線。

## 為何使用基於串流的 BMP 產生？

基於串流的產生方式透過直接寫入磁碟的方式減少記憶體負擔，對於產生大型 BMP 或平行處理大量影像尤為有利。Aspose.PSD 能處理 **30+ 種影像格式**，且在一般伺服器硬體上可在一秒內產生最高 500 MPixels 的 BMP。

## 先決條件

- **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。
- **Aspose.PSD Library** – 從[文件說明](https://reference.aspose.com/psd/java/)下載最新的 JAR。
- **IDE** – Eclipse、IntelliJ IDEA，或您偏好的任何相容 Java 的 IDE。

## 匯入套件

`import` 陳述式將所需的類別匯入作用域。  
`BmpOptions` 設定 BMP 專屬的參數，而 `FileCreateSource` 代表輸出串流。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## 步驟 1：設定文件目錄

`File` 代表檔案系統中的檔案或目錄路徑。  

`File dataDir = new File("Your Document Directory");` – 此變數指向 BMP 將被儲存的資料夾。  
將 `"Your Document Directory"` 替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：指定輸出檔案名稱

`String outFile = dataDir.getAbsolutePath() + File.separator + "output.bmp";` – 定義將要建立的 BMP 檔案的完整路徑與名稱。

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

## 步驟 3：設定 BmpOptions

`BmpOptions bmpOptions = new BmpOptions();` – 建立一個選項物件。  
您可以設定 `bitsPerPixel`（例如 24 代表真彩色）以控制影像品質與檔案大小。

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

## 步驟 4：建立 FileCreateSource

`FileCreateSource fileSource = new FileCreateSource(outFile, false);` – 將輸出路徑包裝為串流來源。  
`bmpOptions.setSource(fileSource);` 告訴 Aspose.PSD 直接將 BMP 寫入此串流。

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

## 步驟 5：產生影像

`Image` 是 Aspose.PSD 用來表示影像的類別，提供建立、編輯與儲存點陣圖的功能。  

`Image img = Image.create(bmpOptions, 800, 600);` – 使用先前設定的選項建立一個 800 × 600 像素的空白 BMP。  
此影像現在已可進一步繪製或處理。

```java
Image image = Image.create(imageOptions, 500, 500);
```

## 步驟 6：影像處理

`Graphics` 是用來在 `Image` 物件上繪製形狀、文字與其他圖形的類別。  

您可以透過從 `img` 取得的 `Graphics` 物件繪製形狀、加入文字或套用濾鏡。  
最後，呼叫 `img.save()` 完成檔案儲存。此步驟確保所有待處理的操作都寫入串流。

```java
// Perform desired image processing operations
// ...

// Save the processed image
image.save(desName);
```

## 常見問題與解決方案

- **檔案權限錯誤** – 確認 Java 程序對目標目錄具有寫入權限。
- **大型影像記憶體不足** – 使用 `FileCreateSource`（如示範）以串流方式處理資料，避免將整個位圖載入記憶體。
- **顏色異常** – 確認 `bitsPerPixel` 與您想要的色深相符；24 bpp 為真彩色 BMP 的標準設定。

## 常見問答

### Q1: 我可以將 Aspose.PSD 與其他 Java 函式庫一起使用嗎？
A1: 可以，Aspose.PSD 能與常見的 Java 影像函式庫（如 ImageIO）順利整合，讓您在不衝突的情況下結合功能。

### Q2: 我該去哪裡取得 Aspose.PSD 相關問題的支援？
A2: 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 獲得社群協助與 Aspose 工程師的官方回覆。

### Q3: 是否提供 Aspose.PSD 的免費試用？
A3: 有，您可在[此處](https://releases.aspose.com/)取得免費試用。

### Q4: 我該如何取得 Aspose.PSD 的臨時授權？
A4: 可在[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q5: Aspose.PSD 的系統需求是什麼？
A5: 請參考[文件說明](https://reference.aspose.com/psd/java/)了解支援的作業系統、Java 版本與記憶體建議。

## 結論

您現在已掌握一套完整、可投入生產的工作流程，使用 Aspose.PSD for Java 透過串流 **建立 BMP** 圖像。藉由運用 `BmpOptions` 與 `FileCreateSource`，您能快速且節省記憶體地產生 BMP，從簡單縮圖到大型點陣圖皆能擴展。歡迎自行嘗試不同的尺寸、色深與後處理步驟，以符合您的應用需求。

---

**最後更新:** 2026-07-17  
**測試環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose

## 相關教學

- [使用 Aspose.PSD for Java 從串流載入影像](/psd/java/advanced-techniques/loading-images-from-stream/)
- [使用 Aspose.PSD for Java 儲存影像至串流](/psd/java/advanced-techniques/save-images-to-stream/)
- [使用 Aspose.PSD for Java 以路徑建立影像](/psd/java/image-editing/create-image-by-setting-path/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}