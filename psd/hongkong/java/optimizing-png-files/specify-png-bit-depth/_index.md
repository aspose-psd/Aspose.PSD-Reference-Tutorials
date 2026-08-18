---
date: 2026-03-18
description: 學習如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並更改 PNG 位深度 – 步驟說明與程式碼範例
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 將 PSD 轉換為具指定位元深度的 PNG
url: /zh-hant/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並指定位元深度

## Introduction
如果你需要 **convert psd to png** 並且想要精確控制 PNG 的位元深度，這裡就是你的最佳去處。在本教學中，我們將示範如何在使用 Aspose.PSD for Java 將 PSD 檔案儲存為 PNG 時變更 png 位元深度。無論你是在開發批次處理工具、網路服務或桌面應用程式，能夠 **save png with options**（例如灰階色彩類型與自訂位元深度）都能讓你對影像品質與檔案大小進行細緻的掌控。

## Quick Answers
- **Can I change the PNG bit depth?** 可以 – 使用 `PngOptions.setBitDepth()` 來指定 1、2、4、8 或 16 位元。  
- **Which color types are supported?** 支援 Grayscale、TrueColor、Indexed 等，透過 `PngColorType` 設定。  
- **Do I need a license for Aspose.PSD?** 開發階段可使用免費試用版；正式上線則需購買商業授權。  
- **What Java version is required?** 需要 Java 8 以上（函式庫相容於更新的 JDK）。  
- **Is the code runnable as‑is?** 可以直接執行，只要將佔位路徑換成你自己的資料夾即可。

## What is “convert psd to png” with custom bit depth?
將 Photoshop PSD 檔案轉換成 PNG 是在需要網頁友好格式時的常見需求。透過設定位元深度來 **adjust png quality**，可以在視覺保真度與檔案大小之間取得平衡，特別適用於縮圖、圖示或頻寬受限的情境。

## Why use Aspose.PSD for Java?
Aspose.PSD for Java 提供高階 API，將 PSD 格式的複雜性抽象化。它讓你能 **create grayscale png**、**save png with options**，並在不必處理低階位元操作的情況下管理色彩配置檔。此函式庫為全託管、跨平台，且會定期更新。

## Prerequisites
在進入程式碼之前，請先確認以下項目已備妥：

1. **Java Development Kit (JDK)** – 從 [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 從 [this link](https://releases.aspose.com/psd/java/) 取得最新 JAR。  
3. **Basic Java knowledge** – 需要熟悉類別、方法與例外處理。  
4. **An IDE** 如 IntelliJ IDEA 或 Eclipse（非必須但建議使用）。  
5. **A sample PSD file** – 將檔案放在程式碼中會引用的資料夾內。

全部準備好了嗎？太好了，接下來匯入必要的套件。

## Import Packages
現在先把環境設定好，於 Java 檔案的最上方加入以下匯入語句：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

上述語句會匯入本教學中會用到的類別，讓我們能載入 PSD 檔並以指定的位元深度儲存為 PNG 圖像。

## Step 1: Set Up Your Document Directory
在開始影像處理之前，先定義一個用來存放圖檔的目錄。這就像在手工藝專案開始前先準備好工具箱。

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the PSD Image
接下來，我們要載入要轉換的 PSD 圖檔。這相當於打開一塊畫布，準備開始作畫。

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

此處使用 `Image.load()` 方法讀取範例 PSD，並將其轉型為 `PsdImage` 以存取 PSD 專屬屬性。

## Step 3: Create PNG Options
畫布打開後，我們需要設定一組儲存影像的選項。這就像在繪畫前先挑選顏色與筆刷樣式。

```java
PngOptions options = new PngOptions();
```

此步驟會建立 `PngOptions` 實例，讓我們能指定 PNG 輸出的各項參數。

## Step 4: Set the Desired Color Type
現在決定最終 PNG 圖像要使用哪種色彩類型。是要豐富的調色盤，還是單色風格？讓我們來選擇！

```java
options.setColorType(PngColorType.Grayscale);
```

此範例將色彩類型設定為灰階。若想要全彩圖像，也可以改用 `PngColorType.TrueColor`。這就是 **create grayscale png** 的部分。

## Step 5: Specify the Bit Depth
接著指定位元深度。這就像告訴印表機要多細緻地列印圖像——位元越多，細節越豐富！

```java
options.setBitDepth((byte)1);
```

此處將位元深度設定為 **1 bit**，適合簡單的灰階圖像。你可以依需求改為 2、4、8 或 16 位元——這正是 **change png bit depth** 的典型範例。

## Step 6: Save the PNG Image
最後，將你的傑作儲存下來！這一步完成了整個流程，等於把畫布上的作品搬到展覽牆上。

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

透過 `PsdImage` 的 `save()` 方法，我們將轉換後的檔案依照先前定義的選項寫入。完成！現在的圖像已經以自訂位元深度儲存。

## Common Issues and Solutions
- **`NullPointerException` when loading the PSD** – 請再次確認 `dataDir` 指向正確的資料夾，且 `sample.psd` 確實存在。  
- **Unsupported bit depth** – Aspose.PSD 只支援 1、2、4、8 與 16 位元的 PNG。使用其他值會拋出 `IllegalArgumentException`。  
- **Color type mismatch** – 若設定的位元深度與所選 `PngColorType` 不相容，函式庫會自動調整為最近的支援設定。

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java 是一套用於 Java 應用程式中操作 PSD 檔的函式庫，提供影像的讀寫與轉換功能。

**Q: How do I specify different bit depths?**  
A: 只要使用 `options.setBitDepth((byte)n)` 方法，將 `n` 替換成你想要的位元深度即可。

**Q: Can I use Aspose.PSD for free?**  
A: 可以，你可以透過免費試用版體驗此函式庫，下載連結請見 [here](https://releases.aspose.com/)。

**Q: Where can I get a support license for Aspose?**  
A: 若需臨時授權，可前往 [here](https://purchase.aspose.com/temporary-license/) 申請。

**Q: What type of images can I convert?**  
A: Aspose.PSD 主要處理 PSD 檔，但也支援轉換為 PNG、JPEG、TIFF 等多種格式。

## Conclusion
現在你已學會如何使用 Aspose.PSD for Java **convert psd to png**，同時掌控 PNG 的位元深度。透過調整 `PngOptions`，你可以 **adjust png quality**、**create grayscale png**，並依需求微調檔案大小。建議多嘗試不同的色彩類型與位元深度，找出最適合你應用場景的平衡點。

---

**Last Updated:** 2026-03-18  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}