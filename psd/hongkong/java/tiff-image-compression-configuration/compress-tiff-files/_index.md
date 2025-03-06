---
title: 使用 Aspose.PSD for Java 壓縮 TIFF 文件
linktitle: 使用 Aspose.PSD for Java 壓縮 TIFF 文件
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD for Java 高效壓縮 TIFF 文件，而不犧牲品質。請遵循我們的詳細指南來簡化您的工作流程。
weight: 10
url: /zh-hant/java/tiff-image-compression-configuration/compress-tiff-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 壓縮 TIFF 文件

## 介紹

想像一下，您正在從事一個大型圖形設計項目，而您的 PSD 檔案正在拖垮您的系統。您需要共享這些文件或儲存它們以供以後使用，但其大小太大而難以處理。這就是將 PSD 檔案壓縮為 TIFF 格式派上用場的地方。 TIFF 檔案在品質和大小之間取得了平衡，使其成為儲存和共享的理想選擇。在本教程中，我們將引導您完成使用 Aspose.PSD for Java 壓縮 TIFF 檔案的過程，確保您的影像緊湊但保持其品質。

## 先決條件

在深入研究程式碼之前，讓我們先做好準備。要學習本教程，您需要具備以下條件：

1.  Aspose.PSD for Java：確保您擁有 Aspose.PSD for Java 函式庫。您可以從[網站](https://releases.aspose.com/psd/java/).
2. Java 開發環境：確保已安裝 JDK。像 IntelliJ IDEA 或 Eclipse 這樣的 IDE 也會很有用。
3. 範例 PSD 檔案：您需要一個 PSD 檔案才能使用。如果沒有，您可以使用任何圖形設計軟體（例如 Adobe Photoshop）建立一個簡單的 PSD 檔案。

完成所有設定後，您就可以開始壓縮 TIFF 檔案了。

## 導入包

在開始實際編碼之前，我們需要將必要的套件匯入到 Java 專案中。這些套件將提供我們操作 PSD 和 TIFF 檔案所需的類別和方法。

```java
import com.aspose.psd.ColorPaletteHelper;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

現在我們已經匯入了必要的套件，讓我們深入了解將 PSD 檔案壓縮為 TIFF 格式的逐步指南。

## 第 1 步：載入 PSD 文件

我們旅程的第一步是載入要壓縮的 PSD 檔案。 Aspose.PSD for Java 讓這個過程變得異常簡單。
要載入 PSD 文件，您將使用`Image.load()`方法。此方法從您指定的目錄讀取 PSD 檔案。讓我們看看它是如何完成的：

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

在這裡，我們載入一個名為的 PSD 文件`layers.psd`從指定的目錄`dataDir`。這`Image.load()`方法傳回一個泛型`Image`對象，然後我們將其轉換為`PsdImage`目的。這種轉換使我們能夠存取 PSD 檔案的特定功能。

為什麼這很重要？載入 PSD 檔案是您執行其他操作的基礎。這就像在主要活動之前搭建舞台一樣。

## 第 2 步：建立 TIFF 選項

載入 PSD 檔案後，下一步是建立 TIFF 選項，該選項將決定最終 TIFF 影像的外觀。此步驟涉及設定壓縮、每個樣本的位數以及其他關鍵設定。

要壓縮映像，您需要建立一個實例`TiffOptions`班級。此類別可讓您配置 TIFF 檔案的各種設定。

```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
```

到這裡，我們已經初始化了`TiffOptions`使用預設格式。但這只是開始。讓我們分解一下您需要調整的設定。

## 步驟 3：設定 TIFF 壓縮

現在我們已經設定了 TIFF 選項，是時候注意壓縮了。壓縮可以減小檔案大小，使 TIFF 檔案更易於管理。

在此範例中，我們將使用 LZW 壓縮，這是一種無損壓縮方法。這意味著您的影像品質將保持不變，同時檔案大小會縮小。

```java
outputSettings.setCompression(TiffCompressions.Lzw);
```

透過將壓縮設定為`Lzw`，我們確保在不犧牲圖像品質的情況下減小文件大小。這就像兩全其美——文件小且質量高。

為什麼選擇LZW？ LZW 壓縮對於具有重複圖案的影像特別有效，這在圖形和設計檔案中很常見。

## 步驟 4：調整每個樣本的位元數和光度模式

壓縮至關重要，但還有其他因素會影響最終 TIFF 檔案的品質和大小。其中最重要的兩個是每個樣本的位元數和光度模式。

### 設定每個樣本的位數

每個樣本的數字決定影像的顏色深度。在本教程中，我們將使用 4 位元灰度調色板，它可以平衡圖像品質和檔案大小。

```java
int[] ushort = {4};  
outputSettings.setBitsPerSample(ushort);
```

在這裡，我們將每個樣本的位數設為 4。此設定非常適合不需要完整色彩範圍的影像。

### 設定測光模式

光度模式決定像素資料的解釋方式。在我們的例子中，我們將使用灰階調色板，它非常適合壓縮無顏色的影像。

```java
outputSettings.setPhotometric(TiffPhotometrics.Palette);
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(true));
```

透過將測光模式設定為`Palette`使用 4 位元灰階調色板，我們告訴程式將影像視為具有有限數量色調的灰階影像。這進一步減小了檔案大小，同時保持視覺完整性。

## 步驟 5：儲存壓縮的 TIFF 文件

所有設定完成後，最後一步是將 PSD 檔案另存為壓縮的 TIFF 檔案。這一步是您迄今為止所做的一切的頂峰。

以下是保存壓縮的 TIFF 檔案的方法：

```java
psdImage.save(dataDir + "SampleTiff_out.tiff", outputSettings);
```

這行程式碼將 PSD 檔案作為 TIFF 檔案保存在指定的目錄中`dataDir`。這`outputSettings`您之前配置的確保檔案根據您的規格進行壓縮。

現在你就擁有了！您的 PSD 檔案現在是一個緊湊、易於共享的 TIFF 檔案。

## 結論

使用 Aspose.PSD for Java 壓縮 TIFF 檔案是一個簡單的過程，可以節省大量儲存空間，同時保持影像品質。透過遵循本教學中概述的步驟，您可以有效地減少 PSD 檔案的大小並將其轉換為更易於管理的 TIFF 格式。無論您想要儲存、分享還是存檔影像，此方法都可以確保您不必在品質或效能上做出妥協。

## 常見問題解答

### 與其他格式相比，使用 TIFF 有何優點？

TIFF 檔案提供無損壓縮，這意味著它們可以在保持影像品質的同時減少檔案大小。它們也得到不同平台和軟體的廣泛支援。

### 我可以使用這種方法壓縮彩色影像嗎？

是的，你可以。但是，本教程重點介紹灰階圖像。您可以透過調整來修改設定以處理彩色影像`BitsPerSample`和`Photometric`模式。

### LZW 壓縮是所有影像的最佳選擇嗎？

LZW 壓縮非常適合具有重複圖案的圖像，例如標誌或簡單圖形。然而，對於照片，其他壓縮方法（例如 JPEG）可能更合適。

### 我可以使用 Aspose.PSD for Java 來壓縮其他檔案格式嗎？

Aspose.PSD for Java 主要處理 PSD 文件，但它提供了將這些文件轉換為各種格式的廣泛支持，包括 TIFF、JPEG、PNG 等。

### 灰階壓縮如何影響影像品質？

灰階壓縮會減少影像中的色彩數量，從而導致視覺細節減少。然而，對於某些類型的圖像，這種權衡是最小的，並且可能會導致檔案大小顯著減少。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
