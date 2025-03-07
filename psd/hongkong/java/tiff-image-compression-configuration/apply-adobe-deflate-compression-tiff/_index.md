---
title: 將 Adobe Deflate 壓縮套用至 TIFF - Java
linktitle: 將 Adobe Deflate 壓縮套用至 TIFF - Java
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 將 Adobe Deflate 壓縮套用至 TIFF 影像。高效影像處理的分步指南。
weight: 12
url: /zh-hant/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 Adobe Deflate 壓縮套用至 TIFF - Java

## 介紹

有沒有想過如何在不影響品質的情況下有效壓縮 TIFF 影像？如果您正在處理大型圖像文件，您可能知道加載時間緩慢和存儲問題帶來的痛苦。這就是 Adobe Deflate 壓縮發揮作用的地方，借助 Aspose.PSD for Java，您可以輕鬆地在專案中實現它。本教學將引導您逐步將 Adobe Deflate 壓縮套用至 TIFF 映像。準備好潛入了嗎？讓我們開始吧！

## 先決條件

在我們進入實際程式碼之前，讓我們確保您已完成所有設定。這是您需要的：

1. Java 開發工具包 (JDK)：確保您的電腦上安裝了最新版本的 JDK。
2.  Aspose.PSD for Java：下載 Aspose.PSD for Java 程式庫並將其整合到您的專案中。你可以從[這裡](https://releases.aspose.com/psd/java/).
3. 開發環境：IntelliJ IDEA、Eclipse 或 NetBeans 等 IDE。
4. 臨時許可證（可選）：如果您還沒有準備好購買，您可以獲得[臨時執照](https://purchase.aspose.com/temporary-license/)嘗試這些功能。

## 導入包

讓我們先在 Java 專案中匯入必要的套件。這些匯入至關重要，因為它們允許您使用 Aspose.PSD 庫和 Java 實用程式。

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

現在我們已經介紹了基礎知識，讓我們將流程分解為易於遵循的步驟。

## 第 1 步：設定 TIFF 選項

首先，您需要建立一個實例`TiffOptions`並根據您的需求進行配置。這些選項定義 TIFF 檔案的處理方式，包括其解析度、配色方案和壓縮。

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

在這裡，我們正在創建一個`TiffOptions`具有預設格式的物件。但這只是開始！ 

## 步驟 2：配置影像屬性

接下來，您需要設定 TIFF 影像的各種屬性，例如`BitsPerSample`, `Photometric`, `Resolution`， 和`PlanarConfiguration`。這些設定決定影像資料的儲存和顯示方式。

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

以下是每個屬性的作用：
- BitsPerSample：設定每個顏色通道的每個樣本的位數。
- 光度學：定義色彩模型（在本例中為 RGB）。
- 解析度：指定影像的水平和垂直解析度。
- PlanarConfiguration：決定像素資料的儲存方式。

## 第 3 步：套用 Adobe Deflate 壓縮

現在魔法來了！您將對 TIFF 影像套用 Adobe Deflate 壓縮，這有助於在不損失影像品質的情況下減少檔案大小。

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

Adobe Deflate 是一種無損壓縮方法，非常適合需要在縮小檔案大小的同時保持高品質的圖片。

## 步驟 4：建立並編輯 TIFF 影像

設定選項後，就可以建立新的 TIFF 影像並對其進行操作了。在此步驟中，我們將建立一個簡單的 100x100 影像並用紅色像素填滿它。

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

在這裡，我們循環遍歷圖像的每個像素並將其顏色設為紅色。當然，您可以自訂這部分以建立更複雜的圖像。

## 步驟 5：儲存壓縮的 TIFF 影像

最後，在配置和建立圖像之後，最後一步是使用應用的壓縮來保存它。確保指定正確的目錄路徑。

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

就是這樣！您已使用 Aspose.PSD for Java 成功將 Adobe Deflate 壓縮套用到 TIFF 映像。

## 結論

現在你就擁有了！使用 Aspose.PSD for Java 將 Adobe Deflate 壓縮套用至 TIFF 映像是一個簡單的過程。無論您是為網站、數位媒體還是任何其他項目處理大圖像，此方法都可以確保您的文件保持高質量，同時在大小上更易於管理。 Aspose.PSD for Java 的強大之處在於其簡單性和效率，使其成為處理複雜影像格式的開發人員的首選工具。

## 常見問題解答

### 什麼是 Adobe Deflate 壓縮？
Adobe Deflate 是一種無損壓縮方法，用於在不損失品質的情況下減少 TIFF 影像的大小。

### 我可以在 Aspose.PSD for Java 中使用其他壓縮方法嗎？
是的，Aspose.PSD 支援各種壓縮方法，如 LZW、CCITT 和 JPEG。

### Aspose.PSD 庫是免費的嗎？
 Aspose.PSD 提供免費試用版，但需要授權才能使用完整功能。你可以獲得一個[臨時執照](https://purchase.aspose.com/temporary-license/)嘗試一下。

### 解析度設定如何影響 TIFF 影像？
解析度決定了列印或顯示時影像的清晰度。解析度越高，品質越好，但檔案大小也越大。

### 我可以使用 Aspose.PSD for Java 操作其他影像格式嗎？
絕對地！ Aspose.PSD 支援各種格式，如 PSD、PNG、JPEG 等。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
