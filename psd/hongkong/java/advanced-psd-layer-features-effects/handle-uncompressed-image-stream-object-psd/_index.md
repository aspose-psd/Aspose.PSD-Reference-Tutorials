---
date: 2026-08-01
description: 了解如何使用 Aspose.PSD for Java 將 PSD 匯出為 PNG，並處理 uncompressed image streams。
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: 處理 PSD 中的 Uncompressed Image Stream Object - Java
og_description: 使用 Aspose.PSD for Java 將 PSD 匯出為 PNG。了解如何處理 uncompressed image streams、建立
  graphics objects，並儲存高品質 PNG。
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: 將 PSD 匯出為 PNG – Java 未壓縮 PSD 串流指南
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: 將 PSD 匯出為 PNG – 建立 PSD Graphics Object – Java 中的 Uncompressed Stream
url: /zh-hant/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 PSD 為 PNG – 建立 PSD 圖形物件 – Java 中未壓縮串流

## 介紹
在本步驟指南中，您將 **export PSD to PNG**，同時使用 Aspose.PSD for Java 處理未壓縮的影像串流。無論是自動化設計流程或打造自訂編輯器，能在不失真的情況下渲染 Photoshop 檔案都是關鍵。我們將從必備設定開始，逐步說明如何建立 `Graphics` 物件，最後完成無損 PNG 匯出。完成後，您將了解 Aspose.PSD 為何能有效處理原始串流，以及如何將其整合至任何 Java 專案。

## 快速回答
- **什麼是「create PSD graphics object」的意思？** 它指的是實例化一個 `Graphics` 內容，讓您能以程式方式在 PSD 圖像上繪圖或修改。  
- **哪個函式庫處理未壓縮的串流？** Aspose.PSD for Java 完全支援原始（未壓縮）影像資料。  
- **編輯後可以匯出 PSD 為 PNG 嗎？** 可以——只要取得 `Graphics` 物件，即可渲染 PSD 並一次呼叫保存為 PNG。  
- **開發階段需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **匯出是無損的嗎？** 匯出為 PNG 會保留原始像素資料，提供無損品質，同時檔案大小比原始 PSD 更小。

## 什麼是 export psd to png？
將 PSD 匯出為 PNG 會把多層的 Photoshop 文件轉換為單層、無損的點陣圖，任何瀏覽器或影像檢視器皆可顯示。此過程保留透明度、色深與圖層效果，同時捨棄 Photoshop 專屬的中繼資料，並保留原始色彩配置檔以確保色彩準確性。

## 為何在影像處理上使用 Aspose.PSD for Java？
Aspose.PSD 支援 **50+** 輸入與輸出格式——包括 PSD、PNG、JPEG、BMP、TIFF，且可處理 **200+** 圖層而無需一次將整個文件載入記憶體。其 `Raw` 壓縮選項以未壓縮方式儲存像素資料，確保下游編輯或存檔時的像素完美還原。

## 前置條件
在開始撰寫程式碼前，請確認您具備以下環境：

- **Java Development Kit (JDK)** – 已安裝 JDK 8 或更新版本。  
- **Aspose.PSD for Java** – 從官方發佈頁面下載最新 JAR：[Aspose.PSD Java download](https://releases.aspose.com/psd/java/)。您亦可透過 [此連結](https://releases.aspose.com/psd/java/) 或 [發佈頁面](https://releases.aspose.com/psd/java/) 取得。其他 Aspose 產品請點選 [此處](https://releases.aspose.com/)。  
- **IDE** – IntelliJ IDEA、Eclipse，或任何相容 Java 的編輯器。  
- **Basic Java knowledge** – 熟悉類別、方法與例外處理。

具備上述條件後，即可開始撰寫程式碼。

## 匯入套件
`Graphics` 類別是 Aspose.PSD 的繪圖表面，允許您直接對像素資料進行渲染或編輯。`PsdImage` 類別代表記憶體中的 PSD 檔案，而 `PsdOptions` 則控制影像的保存方式。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

現在，我們將程式碼拆解為易於理解的步驟，說明環境設定、載入 PSD、操作影像，最後儲存輸出。

## 步驟 1：定義文件目錄
在執行任何檔案操作前，必須告訴程式您的 PSD 資源所在的目錄路徑。此路徑會在整個教學中使用。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為包含 `layers.psd` 的絕對路徑。將路徑設為可配置，可提升程式在不同專案間的可重用性。

## 步驟 2：建立 ByteArrayOutputStream
`ByteArrayOutputStream` 是 Java 中的串流，會在記憶體中以位元組陣列形式保存資料。它充當未壓縮影像的記憶體緩衝區，讓您在寫入磁碟或傳輸前先取得原始位元組。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

變數 `ms` 會在 `save` 操作後保存未壓縮的影像資料。

## 步驟 3：載入 PSD 檔案
`PsdImage` 類別會將 PSD 檔案載入記憶體以供後續操作。載入過程會將磁碟上的 PSD 轉換為 `PsdImage` 物件，供您進行編輯。此步驟會讓 Aspose.PSD 讀取檔案標頭、圖層與資源。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

若路徑錯誤，Aspose.PSD 會拋出 `FileNotFoundException`，建議在正式環境中捕獲此例外。

## 步驟 4：設定 PsdOptions 以儲存
`PsdOptions` 定義 PSD 檔案的保存參數。將壓縮方式設定為 `Raw` 表示像素資料將不經壓縮直接儲存，確保每個像素與記憶體中的狀態完全相同。

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

`CompressionMethod.Raw` 選項在您計畫之後仍需進一步編輯時特別適用。

## 步驟 5：將影像儲存至輸出串流
現在將（可能已修改的）PSD 寫入先前建立的 `ByteArrayOutputStream`。`save` 方法會遵循先前設定的 `PsdOptions`。

```java
psdImage.save(ms, saveOptions);
```

此時，`ms` 已包含未壓縮 PSD 的完整二進位表示。

## 步驟 6：重設輸出串流
寫入完成後，串流的內部指標位於結尾。重設它可將指標回撥至開頭，以便後續讀取。

```java
ms.reset();
```

可將其想像為在播放磁帶前先把磁頭移回起始位置。

## 步驟 7：載入新建立的影像
現在可以直接從位元組陣列建立全新的 `PsdImage` 實例。此步驟驗證已保存的資料能在不損毀的情況下重新載入。

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

若影像成功載入，即代表未壓縮串流寫入正確。

## 步驟 8：建立 Graphics 物件
`Graphics` 類別是 Aspose.PSD 的繪圖畫布，提供在 `PsdImage` 的像素矩陣上直接繪製形狀、文字與套用濾鏡的方法。

```java
Graphics graphics = new Graphics(psdImage);
```

有了這個 `Graphics` 實例，您可以繪製新內容、擦除區域，或合成額外圖層。

## 如何使用 Aspose.PSD for Java 匯出 PSD 為 PNG？
使用 `new PsdImage(dataDir + "layers.psd")` 載入 PSD，建立 `Graphics` 物件，完成所需繪圖後，呼叫 `psdImage.save("output.png", new PngOptions())`。此流程會渲染已編輯的 PSD，並以單一步驟寫入無損 PNG，利用 Aspose.PSD 內建的轉換引擎完成。

## 使用 Graphics 物件操作 PSD 圖層
擁有 `Graphics` 實例即意味著您可對每個圖層進行像素層級的控制。您可以繪製幾何圖形、渲染文字或套用自訂濾鏡。因為圖形上下文作用於圖層的光柵化視圖，變更會即時在儲存影像時顯現。

## 常見問題與解決方案
- **NullPointerException 發生於載入檔案時** – 請再次確認 `dataDir` 路徑，並確保檔名完全相符，包含大小寫。  
- **Compressed output despite using Raw** – 請確認在呼叫 `save` 之前已呼叫 `saveOptions.setCompressionMethod(CompressionMethod.Raw);`。  
- **Graphics object appears blank** – 請確保您在正確的 `PsdImage` 實例上繪圖（即已載入的，而非新建立的空白影像）。  
- **OutOfMemoryError 發生於大型檔案** – 使用 `PsdImage.load(dataDir, LoadOptions)` 並設定 `loadOptions.setLoadMode(LoadMode.Memory)` 以串流大型檔案，避免一次載入整個文件至記憶體。

## 常見問答

### 什麼是 Aspose.PSD？
Aspose.PSD 是一套 Java 函式庫，讓開發者能在不安裝 Adobe Photoshop 的情況下，以程式方式建立、編輯與轉換 Photoshop PSD 檔案。它支援讀寫 PSD、處理圖層、遮色片、通道與各種影像資源，並提供光柵與向量操作 API，適合用於伺服器端影像處理與自動化工作流程。

### 如何下載 Aspose.PSD for Java？
您可從官方發佈頁面下載：[Aspose.PSD Java download](https://releases.aspose.com/psd/java/)。

### Aspose.PSD 有免費試用版嗎？
有，官方下載頁面提供完整功能的免費試用版，可用於開發與評估。

### 我可以取得 Aspose.PSD 的支援嗎？
當然！Aspose 支援論壇提供產品團隊與社群的即時回應：[Aspose support forum](https://forum.aspose.com/c/psd/34)。

### 如何取得 Aspose.PSD 的臨時授權？
您可直接於 Aspose 授權入口申請臨時授權，系統會產生有效期 30 天的金鑰，讓您在不購買正式授權的情況下完整評估功能。試用期結束後，請以永久授權取代臨時金鑰以持續在生產環境使用。前往臨時授權頁面產生金鑰：[temporary license page](https://purchase.aspose.com/temporary-license/)。

## 常見問題

**Q: 我可以使用 graphics 物件僅編輯特定圖層嗎？**  
A: 可以。載入 PSD 後，透過 `psdImage.getLayers().get_Item(index)` 取得目標圖層，並將該圖層傳入 `Graphics` 建構子即可。

**Q: Raw 壓縮方式會影響檔案大小嗎？**  
A: Raw 會以未壓縮方式儲存像素資料，檔案大小會大於使用壓縮的 PSD，但可保證 100 % 的像素忠實度。

**Q: 是否能將編輯後的 PSD 匯出為其他格式（例如 PNG）？**  
A: 完全可以。編輯完成後，呼叫 `psdImage.save("output.png", new PngOptions())`——這是 **export PSD to PNG** 的標準做法，且可確保無損品質。

**Q: 需要哪個 Java 版本？**  
A: Aspose.PSD for Java 支援 JDK 8 及以上版本，涵蓋所有長期支援（LTS）版本至 JDK 21。

**Q: 處理完畢後如何釋放資源？**  
A: 呼叫 `psdImage.dispose()`，並關閉任何串流（例如 `ms.close()`），以釋放本機記憶體並避免記憶體洩漏。

**最後更新：** 2026-08-01  
**測試環境：** Aspose.PSD for Java（最新版本）  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.PSD for Java 將影像儲存至串流](/psd/java/advanced-techniques/save-images-to-stream/)
- [使用 Java 匯出 PSD 圖層群組為影像](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [使用 Aspose.PSD for Java 以串流建立影像](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}