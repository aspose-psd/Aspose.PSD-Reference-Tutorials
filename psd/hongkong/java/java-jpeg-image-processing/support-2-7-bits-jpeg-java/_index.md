---
date: 2026-10-08
description: Java 圖像處理教學：學習如何使用 Aspose.PSD 操作 PSD 檔案並將其儲存為 JPEG。提供逐步指南與程式碼範例，適合新手與專業人士。
keywords:
- java image processing tutorial
- Aspose.PSD
- 2 bit JPEG
- 7 bit JPEG
lastmod: 2026-10-08
linktitle: 在 Java 中支援 2 位元與 7 位元 JPEG
og_description: Java 圖像處理教學：學習如何使用 Aspose.PSD 操作 PSD 檔案並將其儲存為 JPEG。提供詳細步驟、快速解答與開發人員除錯指南。
og_image_alt: Guide to processing 2‑ and 7‑bit JPEG images in Java with Aspose.PSD
og_title: Java 圖像處理教學：支援 2 位元與 7 位元 JPEG
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  headline: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  type: TechArticle
- description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  name: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  steps:
  - name: '**Java Development Kit (JDK)** – version 8 or higher.'
    text: '**Java Development Kit (JDK)** – version 8 or higher.'
  - name: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**Sample PSD file** – any PSD you wish to convert.'
    text: '**Sample PSD file** – any PSD you wish to convert.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables creation, manipulation,
      and conversion of Photoshop PSD files directly from Java applications.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [website](https://releases.aspose.com/psd/java/)
      and add the JAR to your project’s build path or Maven/Gradle dependencies.
    question: How do I install Aspose.PSD for Java?
  - answer: Yes, you can load custom RGB or CMYK ICC profiles and assign them to the
      `JpegOptions` before saving.
    question: Can I use custom color profiles with Aspose.PSD for Java?
  - answer: It supports PSD, JPEG, PNG, BMP, TIFF, GIF, and over 20 additional raster
      formats.
    question: What image formats does Aspose.PSD for Java support?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library before purchasing a license.
    question: Is there a free trial available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- JPEG conversion
title: Java 圖像處理教學：支援 2 位元與 7 位元 JPEG
url: /zh-hant/java/java-jpeg-image-processing/support-2-7-bits-jpeg-java/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像處理教學：支援 2‑ 位元與 7‑ 位元 JPEG

## 介紹
在本 **java 圖像處理教學** 中，您將了解如何使用 Aspose.PSD for Java 函式庫載入 PSD 檔案並匯出為 2‑ 或 7‑ 位元 JPEG。無論您是要建置批次轉換服務，或是需要對影像品質進行細緻控制，以下步驟都會從環境設定說明到最終 JPEG 儲存，帶您一步步完成。讓我們開始吧！

## 快速答案
- **哪個函式庫支援 2‑ 與 7‑ 位元 JPEG？** Aspose.PSD for Java。  
- **最低 Java 版本？** JDK 8 或更新版本。  
- **開發時需要授權嗎？** 免費試用可用於評估；正式上線需購買商業授權。  
- **可以變更色彩模式嗎？** 可以 – 透過 `JpegCompressionColorMode` 支援 CMYK、YCCK 及其他模式。  
- **預期可減少多少檔案大小？** 使用每通道 2 位元可比 8 位元輸出縮小最高 80 % 左右。

## 什麼是 java 圖像處理教學？
java 圖像處理教學是一套逐步說明，教導開發者如何以 Java 程式化操作影像資料。內容涵蓋載入各種格式、套用轉換、調整色彩與壓縮設定，並儲存結果，讓您能建立自訂的影像處理工作流程。

## 為何使用 Aspose.PSD for Java？
Aspose.PSD for Java 提供完整的 API，讓您在不安裝 Photoshop 的情況下操作 Photoshop 檔案。支援超過 30 種影像格式，透過串流方式處理最高 2 GB 的檔案，並提供對圖層、通道與色彩描述檔的細緻控制，是高效能伺服器端處理的理想選擇。

## 前置條件
在開始之前，請確認您具備以下項目：

1. **Java Development Kit (JDK)** – 版本 8 以上。  
2. **Aspose.PSD for Java 函式庫** – 您可於[此處下載](https://releases.aspose.com/psd/java/)。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 NetBeans。  
4. **範例 PSD 檔案** – 任意您想要轉換的 PSD。  
5. **基本的 Java 知識** – 熟悉類別、物件與例外處理。

## 匯入套件
首先，將 Aspose.PSD JAR 加入專案的 classpath，然後匯入所需的命名空間：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.jpeg.JpegCompressionMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## 如何在 Java 中載入 PSD 影像？
要載入 PSD 檔案，呼叫 `Image` 類別的靜態 `load` 方法，並將結果轉型為 `PsdImage`。這會在記憶體中建立 Photoshop 文件的表示，讓您存取其圖層、通道、遮色片與中繼資料，進而進行操作或匯出為其他格式。

`PsdImage` 是 Aspose.PSD 的核心類別，代表記憶體中的 Photoshop 文件，支援對其內容的讀寫操作。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "PsdImage.psd");
```

## 如何設定 2‑ 或 7‑ 位元 JPEG 的選項？
建立新的 `JpegOptions` 實例，並設定其屬性以符合目標輸出。使用 `setColorType` 選擇適當的 `JpegCompressionColorMode`（例如 CMYK 或 YCCK），再以 `setCompressionType` 指定壓縮演算法。最後，將 `bitsPerChannel` 設為 2 或 7，以控制每個色彩通道的位元深度。

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Cmyk);
options.setCompressionType(JpegCompressionMode.JpegLs);
```

## 如何為低位元 JPEG 設定每通道位元數？
`bitsPerChannel` 定義輸出 JPEG 每個色彩通道使用的位元數。將此屬性設為 2 會將每個通道縮減至兩位元，產生高度壓縮且會出現明顯色帶的影像；設為 7 則保留較多細節，檔案大小介於極低位元與標準 8‑ 位元之間。請依您的品質與尺寸需求選擇合適的值。

```java
byte bpp = 2;
options.setBitsPerChannel(bpp);
```

## 如何套用色彩描述檔（可選）？
`ICCProfile` 代表國際色彩聯盟（International Color Consortium）描述檔，用於說明裝置或工作空間的色彩特性。若您有自訂的 ICC 檔案，可使用 `ICCProfile.getInstance(path)` 載入，並指派給 `jpegOptions` 物件的 `iccProfile` 屬性。若屬性為 null，Aspose.PSD 會使用系統預設描述檔，足以應付大多數情境。

```java
options.setRgbColorProfile(null);
options.setCmykColorProfile(null);
```

## 如何將處理後的影像儲存為 JPEG？
`save` 方法會依據提供的選項將影像寫入檔案。對 `PsdImage` 實例呼叫 `save`，傳入目標檔名（含 .jpg 副檔名）與已配置好的 `JpegOptions`。函式庫會負責編碼、套用選定的每通道位元與色彩描述檔，產生符合規格的 JPEG。

```java
image.save(dataDir + "2_7BitsJPEG_output.jpg", options);
```

## 常見問題與解決方案
- **檔案過大錯誤** – 確認使用最新的 Aspose.PSD 版本，該版本會串流資料，避免一次將整個檔案載入記憶體。  
- **顏色異常** – 請確認所選的 `JpegCompressionColorMode` 與來源影像的色彩空間相符。  
- **缺少 ICC 描述檔** – 若需特定描述檔，請使用 `ICCProfile.getInstance(path)` 載入，並指派給 `JpegOptions`。

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套商業函式庫，讓 Java 應用程式直接建立、操作與轉換 Photoshop PSD 檔案。

**Q: 如何安裝 Aspose.PSD for Java？**  
A: 您可從[官方網站](https://releases.aspose.com/psd/java/)下載函式庫，然後將 JAR 加入專案的建置路徑，或透過 Maven/Gradle 依賴管理。

**Q: 可以在 Aspose.PSD for Java 中使用自訂色彩描述檔嗎？**  
A: 可以，您可載入自訂的 RGB 或 CMYK ICC 描述檔，並在儲存前指派給 `JpegOptions`。

**Q: Aspose.PSD for Java 支援哪些影像格式？**  
A: 支援 PSD、JPEG、PNG、BMP、TIFF、GIF，以及超過 20 種其他點陣圖格式。

**Q: 有免費試用版嗎？**  
A: 有，您可下載[免費試用版](https://releases.aspose.com/)以評估函式庫功能，之後再購買授權。

---

**最後更新：** 2026-10-08  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose

## 相關教學

- [Image Processing Java – Support for JPEG-LS with CMYK](/psd/java/java-jpeg-image-processing/support-jpeg-ls-cmyk-java/)
- [Save PSD as JPEG and Support RGB Color with Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [How to Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}