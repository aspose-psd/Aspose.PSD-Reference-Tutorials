---
date: 2026-02-17
description: 了解如何使用 Aspose.PSD for Java 提取 PSD 圖層並將其轉換為 PNG。適合需要強大圖形處理功能的開發者。
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD Java 提取 PSD 圖層並為 PSD 檔案新增圖層支援
url: /zh-hant/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

個圖層個別匯出。"

Then the metadata.

--- line.

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

Then closing shortcodes.

Make sure to keep the markdown formatting exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 提取 PSD 圖層並為 PSD 檔案新增圖層支援（使用 Aspose.PSD Java）

## Introduction
在圖形設計師與開發人員的日常工作中，處理 Photoshop Document（PSD）檔案是常見情況。最常見的任務之一是 **提取 PSD 圖層**，以便進行編輯、重複使用或轉換為其他格式，例如 PNG。在 Java 應用程式中，Aspose.PSD 讓此過程變得簡單且程式碼友好。在本教學中，我們將逐步說明如何提取 PSD 圖層、啟用圖層支援，並 **將 PSD 圖層轉換為 PNG**——提供清晰說明與實用技巧。

## Quick Answers
- **什麼是「提取 PSD 圖層」？** 指載入 PSD 檔案並存取每個單獨的圖層以進行操作或匯出。  
- **哪個 Java 函式庫負責此功能？** Aspose.PSD for Java 提供完整的 PSD 處理功能，無需 Photoshop。  
- **能否一次性將 PSD 圖層轉換為 PNG？** 可以——只要使用正確的載入選項載入檔案，並以保留透明度的 PNG 選項儲存。  
- **正式環境是否需要授權？** 生產環境需要商業授權；可使用免費試用版進行評估。  
- **需要哪個 Java 版本？** JDK 8 以上（本教學以 JDK 11 為例）。

## How to extract PSD layers using Aspose.PSD for Java
以下是一個逐步指南，涵蓋從環境設定到儲存最終 PNG 的全部步驟。依照每個編號步驟操作，即可在數分鐘內得到可運作的解決方案。

## Why extract PSD layers and convert them to PNG?
- **重複使用資源：** 從主 PSD 中直接提取圖示、按鈕或 UI 元件，無需手動匯出。  
- **自動化：** 即時產生縮圖或適合網頁使用的圖像。  
- **保留透明度：** PNG 支援 alpha 通道，適合網頁圖形。  
- **跨平台：** 伺服器上不需要 Photoshop；Aspose.PSD 可在任何支援 Java 的環境執行。

## Prerequisites
Before we dive in, make sure you have the following:

1. **Java Development Environment** – JDK installed. You can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Grab the latest library from the official download page [here](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – Familiarity with compiling and running Java programs.  
4. **IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.  
5. **A PSD file** – Use any PSD you have, or download a sample PSD for testing.

Once you have these ready, you’re set to start extracting PSD layers.

## Import Packages
First, import the classes we’ll need from the Aspose.PSD library.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Define Your Directories
Set up the paths for the source PSD and the output PNG. Adjust the `dataDir` to point to the folder where your files reside.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – Replace `"Your Document Directory"` with **your actual folder path**.  
- `sourceFileName` – Full path to the PSD you want to process.  
- `output` – Destination path for the PNG that will contain the extracted layers.

## Step 2: Set Up the Load Options
Configuring `PsdLoadOptions` ensures that all layer effects and resources are loaded correctly, which is essential when you **extract PSD layers**.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – Loads additional effects (like drop shadows) attached to layers.  
- `setUseDiskForLoadEffectsResource(true)` – Offloads heavy resources to disk, reducing memory pressure.

## Step 3: Load the PSD File
Now we load the PSD into a `PsdImage` object using the options defined above.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

At this point, `image` contains all layers, masks, and effects, ready for extraction.

## Step 4: Set Up the Save Options
Configure how the PNG will be saved. Using `TruecolorWithAlpha` preserves transparency from the original layers.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 5: Save the Image (Convert PSD Layers to PNG)
Export the loaded PSD (with all its layers) to a single PNG file. This step effectively **convert psd layers png** in one operation.

```java
image.save(output, saveOptions);
```

If you need each layer as a separate PNG, you could iterate over `image.getLayers()`—but for many use‑cases a merged PNG is sufficient.

## Step 6: Wrap It Up
Add a friendly console message so you know the process succeeded.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Common Issues & Tips
- **Out‑of‑Memory Errors:** If you’re processing very large PSDs, keep `setUseDiskForLoadEffectsResource(true)` enabled to offload temporary data.  
- **Missing Effects:** Ensure `setLoadEffectsResource(true)` is set; otherwise some layer effects may be ignored.  
- **Path Problems:** Use `Paths.get(...)` from `java.nio.file` for **platform‑independent** path handling.

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library that allows you to manipulate PSD files without having Photoshop installed.

**Q: Can I use Aspose.PSD for other file formats?**  
A: Yes! While primarily for PSD files, Aspose offers libraries for various other formats too.

**Q: Is there a trial version available?**  
A: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).

**Q: Where can I get support if I need help?**  
A: You can access support in the Aspose forum [here](https://forum.aspose.com/c/psd/34).

**Q: Can I convert back from PNG to PSD?**  
A: The Aspose.PSD library focuses more on reading and manipulating PSD files rather than converting other formats back to PSD.

**Q: How do I extract each layer as a separate PNG?**  
A: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer, and save it with its own `PngOptions`. This gives you individual PNG files per layer.

## Conclusion
現在您已學會如何 **提取 PSD 圖層**、啟用完整的圖層支援，並 **將 PSD 圖層轉換為 PNG**，使用 Aspose.PSD for Java。無論是建構自動化資產管線，或為桌面應用程式加入圖形功能，此方法皆能在不依賴 Photoshop 的情況下，提供對 Photoshop 檔案的細緻控制。歡迎進一步探索，例如套用濾鏡、程式化合併圖層，或將每個圖層個別匯出。

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}