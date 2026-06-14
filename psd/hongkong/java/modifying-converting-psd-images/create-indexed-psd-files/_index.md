---
date: 2026-03-15
description: 在本分步指南中，學習如何使用 Aspose.PSD for Java 建立 PSD 檔案、產生 PSD 色盤以及設定 PSD 色彩模式。
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 建立 PSD 檔案
url: /zh-hant/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 建立 PSD 檔案

## Introduction
如果你曾經想過 **如何以程式方式建立 PSD** 檔案，你來對地方了。Aspose.PSD for Java 為你提供對 Photoshop 文件的完整控制，讓你在不開啟 Photoshop 的情況下產生、編輯與儲存 PSD 檔案。在本教學中，我們將逐步說明如何建立 **索引式 PSD** 檔案、設定 PSD 顏色模式，並產生自訂顏色調色盤——全部以清晰的 Java 程式碼示範。無論你是在建構圖形管線、自動化資產產生，或只是試驗，這裡的概念都能幫助你將視覺構想付諸實現。

## Quick Answers
- **需要的函式庫是什麼？** Aspose.PSD for Java  
- **我可以建立索引式 PSD 嗎？** 可以，將顏色模式設為 `Indexed`  
- **需要安裝 Photoshop 嗎？** 不需要，Aspose.PSD 可獨立運作  
- **需要哪個 Java 版本？** JDK 8 或更新版本  
- **畫布大小上限是多少？** 任意尺寸；本範例使用 500 × 500 px  

## What is an Indexed PSD File?
索引式 PSD 以調色盤儲存顏色，而非每個像素的完整顏色值。這可減少檔案大小，且非常適合顏色受限的圖形，如圖示或 UI 資產。透過產生自訂調色盤，你可以精確控制最終影像中出現的顏色。

## Why Generate a PSD Color Palette?
建立 **PSD 調色盤** 可讓你：
- 保持檔案尺寸小，適用於網頁或行動裝置  
- 透過限制於企業調色盤，確保品牌色彩一致性  
- 加速支援索引圖像的應用程式之渲染速度  

## Prerequisites
在深入程式碼之前，請確保你已具備以下條件：

1. **基本的 Java 知識** – 你應該熟悉類別、方法與物件建立。  
2. **Java Development Kit (JDK) 8+** – 已在 IDE 中安裝並設定。  
3. **IDE（IntelliJ IDEA、Eclipse 等）** – 雖非必須，但強烈建議使用以便除錯。  
4. **Aspose.PSD for Java 函式庫** – 前往 **[此處](https://releases.aspose.com/psd/java/)** 下載，並將 JAR 加入專案的 classpath。  
5. **基礎平面設計概念** – 了解顏色模式、調色盤與基本形狀將有助於跟隨本教學。  

## Import Packages
在開始撰寫程式碼之前，先確保已在 Java 應用程式中匯入所有必要的套件。以下是你需要的內容：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

這些匯入讓你能透過 Aspose.PSD 操作 PSD 選項、顏色與圖形。

現在，讓我們一步步拆解程式碼，說明 **如何建立 PSD** 檔案並使用索引色彩模式。

## Step 1: Set Up Your Document Directory
首先，定義產生的 PSD 要儲存的位置。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為絕對或相對路徑，例如 `"/Users/YourName/Documents/"`。

## Step 2: Create an Instance of PsdOptions
`PsdOptions` 包含即將產生檔案的所有設定。

```java
PsdOptions createOptions = new PsdOptions();
```

## Step 3: Set Core Properties of PsdOptions
在此我們指定輸出位置、將 **psd 顏色模式** 設為 `Indexed`，以及 PSD 版本。

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – 新檔案的完整路徑。  
- **Color Mode** – `Indexed` 告訴 Aspose.PSD 使用基於調色盤的影像。  
- **Version** – PSD 格式版本（5 可適用於大多數現代 Photoshop 版本）。  

## Step 4: Create a Color Palette (Generate PSD Color Palette)
定義索引影像中可使用的顏色。

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette` 陣列可容納最多 256 個 `Color` 物件。  
- `CompressionMethod.RLE` 為索引影像提供高效的無損壓縮。  

## Step 5: Create the PSD Image Canvas
現在我們建立一個空白 PSD，尺寸為所需的大小。

```java
Image psd = Image.create(createOptions, 500, 500);
```

此程式碼會建立一個 500 × 500 像素的畫布，使用先前定義的調色盤。

## Step 6: Draw Graphics on the PSD
加入視覺內容——此處在白色背景上繪製一個簡單的紅色橢圓。

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` 以白色填滿背景。  
- `drawEllipse` 繪製一個紅色橢圓，筆畫寬度為 6 像素。  

## Step 7: Save the PSD File
最後，將影像寫入磁碟。

```java
psd.save();
```

檔案 `Newsample_out.psd` 會出現在先前指定的目錄中。

## Common Issues & Tips
- **調色盤大小** – 若需要超過 4 種顏色，只需將它們加入 `palette` 陣列（上限 256）。  
- **檔案權限** – 確認 Java 程序對 `dataDir` 具有寫入權限。  
- **顏色模式錯誤** – 若遺漏 `createOptions.setColorMode(ColorModes.Indexed)`，將產生 RGB PSD 而非索引式 PSD。  

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library that enables manipulation of PSD (Photoshop) files programmatically using Java.  

**Q: Can I use Aspose.PSD for free?**  
A: Yes, you can access a free trial version of Aspose.PSD **[here](https://releases.aspose.com/)**.  

**Q: Do I need to have Photoshop installed to work with Aspose.PSD?**  
A: No, you can create and manipulate PSD files without Photoshop, as Aspose.PSD handles all operations independently.  

**Q: How do I obtain a temporary license for Aspose.PSD?**  
A: You can request a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.  

**Q: Where can I get support for Aspose.PSD?**  
A: You can get support from the Aspose forum **[here](https://forum.aspose.com/c/psd/34)**.  

## Conclusion
你剛剛學會 **如何建立 PSD** 檔案並使用索引色彩模式、產生自訂調色盤，以及加入簡單圖形——全部透過 Aspose.PSD for Java 完成。利用這些基礎，你可以擴展到更複雜的繪圖、圖層管理與批次處理。欲深入探索，請參考官方 API 參考 **[here](https://reference.aspose.com/psd/java/)**，並持續嘗試不同的調色盤與繪圖基元。

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}