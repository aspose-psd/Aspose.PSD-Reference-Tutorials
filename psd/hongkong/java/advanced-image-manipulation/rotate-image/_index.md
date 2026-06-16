---
date: 2026-05-19
description: 了解如何使用 Aspose.PSD for Java 將 PSD 轉換為 JPEG 並將圖像旋轉 270 度。本指南說明如何旋轉 PSD
  檔案、翻轉圖像以及將 PSD 轉換為 JPEG。
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: 旋轉圖像 270 度
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 將 PSD 轉換為 JPEG 並旋轉 270°
url: /zh-hant/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 轉換為 JPEG 並將圖像旋轉 270 度（使用 Aspose.PSD for Java）

## 簡介

在本 **Java 圖像處理教學** 中，您將學習如何 **將 PSD 轉換為 JPEG**，同時使用 Aspose.PSD for Java 將圖像旋轉 270 度。無論您是構建批次處理管線、網頁編輯器，或是桌面工具，該函式庫都能讓您在不安裝 Photoshop 的情況下操作 PSD 層。我們還會介紹可選的翻轉功能，並展示從載入 PSD 檔案到儲存 JPEG 的完整端到端流程。

## 快速解答
- **哪個函式庫負責旋轉？** Aspose.PSD for Java  
- **範例使用哪個旋轉角度？** 270 度  
- **我也可以翻轉圖像嗎？** 可以 – 使用 `RotateFlipType` 選項，例如 `Rotate90FlipX`  
- **如何儲存結果？** 在範例中我們使用 `JpegOptions` 以 JPEG 格式儲存  
- **商業使用是否需要授權？** 商業用途需擁有有效的 Aspose.PSD 授權  

## 什麼是「將圖像旋轉 270 度」？
將圖像旋轉 270 度即將圖片順時針旋轉三分之三圈（或逆時針旋轉 90 度）。此方向常用於在先前的變換後恢復原始的直向版面，尤其是當圖像最初以橫向模式拍攝但需要以直向顯示時。結果是視覺上正確定位且不會損失畫質。

## 為什麼要使用 Aspose.PSD 完成此任務？
Aspose.PSD 支援 **超過 50 種輸入與輸出格式**——包括 PSD、JPEG、PNG、BMP、GIF 與 TIFF，且可處理高達 **2 GB** 的檔案而無需將整個文件載入記憶體。API 可在任何 Java 執行環境（JDK 8+）上運行，無需本機 Photoshop 安裝，並提供單一的 `rotateFlip` 呼叫，同時處理旋轉與翻轉。

## 先決條件

在開始之前，請確保您已具備：

- 已安裝 **Aspose.PSD for Java** 函式庫。您可以下載並在此處查看完整 API 參考 [此處](https://reference.aspose.com/psd/java/)。  
- Java 開發環境（JDK 8 或以上）。  
- 一個您想要旋轉的範例 PSD 檔案。請在程式碼中將 `sourceFile` 變數更新為檔案的正確路徑。

## 匯入套件

載入、轉換與儲存檔案時需要 `Image`、`RotateFlipType` 與 `JpegOptions` 類別。  
`Image` 是代表 PSD 文件於記憶體中的核心類別。  
`RotateFlipType` 列舉了支援的旋轉與翻轉操作。  
`JpegOptions` 用於設定 JPEG 輸出的品質等參數。  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 如何在旋轉後將 PSD 轉換為 JPEG？

載入來源 PSD，套用 270 度旋轉，然後立即儲存為 JPEG。此三步流程在現代 CPU 上對一般 10 MP 圖像的處理時間不足一秒，非常適合高吞吐量的批次作業。僅處理必要的圖像資料即可保持低記憶體使用量，且產生的 JPEG 在降低檔案大小的同時仍保有視覺忠實度。

### 步驟 1：載入 PSD 檔案

`Image` 是 Aspose.PSD 的核心類別，代表記憶體中的單一 PSD 文件。實例化時僅讀取標頭資訊，保持記憶體使用量低。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### 步驟 2：將圖像旋轉 270 度

`rotateFlip` 會對圖像執行指定的旋轉與可選的翻轉。`RotateFlipType.Rotate270FlipNone` 會將畫布順時針旋轉 270 度，同時保持圖像方向不變。

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **專業提示：** 若您還需要水平或垂直翻轉圖像，可選擇其他 `RotateFlipType`，例如 `Rotate90FlipX` 或 `Rotate180FlipY`。

### 步驟 3：將 PSD 轉換為 JPEG 並儲存

`JpegOptions` 定義 JPEG 專屬的參數，如壓縮品質。`save` 方法會將轉換後的圖像以指定格式寫入磁碟。

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

檔案 `RotatedImage_out.jpg` 現在包含已旋轉 270 度的原始 PSD 內容，並以 JPEG 格式儲存。

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| **圖像顯示顛倒** | 確認您使用的是 `Rotate270FlipNone`。若要順時針旋轉 90 度，請使用 `Rotate90FlipNone`。 |
| **輸出檔案損壞** | 確保目標資料夾已存在且您具有寫入權限。 |
| **授權例外** | 在生產環境載入圖像前，請安裝臨時或永久的 Aspose.PSD 授權。 |

## 常見問答

**Q: Aspose.PSD 是否相容於不同的圖像格式？**  
A: 是的，Aspose.PSD 支援 PSD、JPEG、PNG、BMP、GIF、TIFF 以及許多其他點陣圖格式。

**Q: 我可以套用自訂旋轉角度，而不僅限於預設的翻轉嗎？**  
A: 當然可以！雖然 `RotateFlipType` 提供常用角度，您仍可串接多次呼叫或使用變換矩陣來實現任意角度。

**Q: 如何將已旋轉的 PSD 轉換為其他格式，例如 PNG？**  
A: 在 `save` 方法中將 `JpegOptions` 替換為 `PngOptions`（或相應的選項類別）即可。

**Q: 我可以在哪裡取得更多支援或協助？**  
A: 如需社群協助，請造訪 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)。

**Q: 是否提供免費試用？**  
A: 有的，您可以透過 [免費試用](https://releases.aspose.com/) 來體驗 Aspose.PSD。

**Q: 如何取得臨時授權？**  
A: 若需要臨時授權，請在此處取得 [此處](https://purchase.aspose.com/temporary-license/)。

**最後更新：** 2026-05-19  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.PSD for Java 將 PSD 轉換為點陣圖格式](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [使用 Java 將 PSD 轉換為 PNG 並旋轉 PSD 檔案中的圖層](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [如何在 Java 中使用 Aspose.PSD 旋轉圖像](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}