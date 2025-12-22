---
date: 2025-12-19
description: Aspose.PSD for Java kullanarak bir görüntünün parlaklığını nasıl ayarlayacağınızı
  öğrenin. Bu Java görüntü işleme öğreticisi adım adım bir rehber sunar.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Bir Görüntünün Parlaklığını Nasıl Ayarlarsınız
url: /tr/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Bir Görüntünün Parlaklığını Ayarlama

## Introduction

Eğer **parlaklığı nasıl ayarlayacağınızı** doğrudan Java kodundan öğrenmek istiyorsanız doğru yerdesiniz. Parlaklık ayarı, grafik tasarımcılar, fotoğrafçılar ve görüntü‑işleme hatları oluşturan herkes için sıkça yapılan bir görevdir. Bu **java image manipulation tutorial** içinde, PSD/TIFF yükleme, bir parlaklık ofseti uygulama ve sonucu kaydetme adımlarını Aspose.PSD for Java kütüphanesini kullanarak adım adım inceleyeceğiz.

## Quick Answers
- **What library handles brightness?** Aspose.PSD for Java  
- **Which method changes brightness?** `RasterImage.adjustBrightness()`  
- **Can I work with PSD and TIFF files?** Yes, the API supports both formats.  
- **Do I need a license for production?** A commercial license is required for non‑evaluation use.  
- **How long does the implementation take?** Typically under 10 minutes for a basic adjustment.

## What is Image Brightness Adjustment?

Görüntü parlaklığı ayarı, bir görüntünün tüm piksellerinin genel ışıklılığını değiştirir. Parlaklığı artırmak karanlık bölgeleri aydınlatırken, azaltmak tüm resmi karartır. Bu işlem, düşük pozlanmış fotoğrafları düzeltmek, baskı için varlıkları hazırlamak veya uygulamalarda görsel efektler oluşturmak için faydalıdır.

## Why Use Aspose.PSD for Java?

- **Full format support** – PSD, TIFF, JPEG, PNG, and more.  
- **No external native dependencies** – pure Java, easy to integrate.  
- **High‑performance caching** – raster data can be cached for faster repeated operations.  
- **Rich API** – methods for color correction, layers, masks, and other advanced edits.

## Prerequisites

Tutoriala başlamadan önce aşağıdaki ön koşulları karşıladığınızdan emin olun:

- Aspose.PSD for Java Library: Download and install the library from the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## Import Packages

Başlamak için gerekli paketleri Java projenize ekleyin. Bu örnekte aşağıdaki paketleri kullanacağız:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Şimdi, bir görüntünün parlaklığını ayarlama sürecini basit adımlara ayıralım:

## How to Adjust Brightness Using Aspose.PSD

### Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Bu adımda hedef görüntüyü yüklüyor ve daha sonraki işlemler için bir `RasterImage` nesnesine dönüştürüyoruz.

### Step 2: Adjust Brightness

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Burada, görüntünün parlaklığını değiştirmek için `adjustBrightness` metodunu kullanıyoruz. Bu örnekte parlaklığı 50 birim azaltıyoruz, ancak ihtiyacınıza göre bu değeri özelleştirebilirsiniz.

### Step 3: Set TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Ayarlanan görüntüyü kaydetmek için `TiffOptions` yapılandırmasını yapın. `bitsPerSample` ve `photometric` özelliklerini özel ihtiyaçlarınıza göre ayarlayın.

### Step 4: Save the Resultant Image

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Son olarak, belirtilen `TiffOptions` ile değiştirilmiş görüntüyü kaydedin.

## Common Issues and Solutions

| Issue | Reason | Solution |
|-------|--------|----------|
| **`ClassCastException` when casting Image** | The file is not a raster image (e.g., a vector PSD). | Verify the source file format or use `image instanceof RasterImage` before casting. |
| **Brightness change has no effect** | The image was not cached before adjustment. | Call `rasterImage.cacheData()` as shown in Step 1. |
| **Saved file appears corrupted** | Incorrect `TiffOptions` configuration. | Ensure `bitsPerSample` matches the source image depth (usually 8‑bit per channel). |

## Frequently Asked Questions

### Q1: Can I adjust brightness in other image formats besides PSD?

A1: Yes, Aspose.PSD for Java supports various image formats like JPEG, PNG, and TIFF.

### Q2: How can I handle errors during the image adjustment process?

A2: You can implement error handling using try‑catch blocks to manage exceptions that may occur.

### Q3: Is there a limit to the range of brightness adjustment?

A3: The range of adjustment depends on the image content and format, but Aspose.PSD provides flexibility in customization.

### Q4: Can I use Aspose.PSD for Java in commercial projects?

A4: Yes, Aspose.PSD for Java is a commercial library, and you can obtain a license from [here](https://purchase.aspose.com/buy).

### Q5: Is there a free trial available for Aspose.PSD for Java?

A5: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).

### Q6: Does the `adjustBrightness` method affect layer visibility?

A6: The method works on the rasterized composite image, so layer visibility is respected during rasterization.

### Q7: Can I chain multiple adjustments (e.g., contrast, saturation) together?

A7: Absolutely. After adjusting brightness, you can call `adjustContrast`, `adjustSaturation`, etc., on the same `RasterImage` instance.

---

**Last Updated:** 2025-12-19  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}