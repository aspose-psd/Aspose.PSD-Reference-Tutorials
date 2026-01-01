---
date: 2026-01-01
description: Aspose.PSD for Java ile nasıl görüntü kırpılacağını öğrenerek Java görüntü
  işleme konusunda uzmanlaşın. Sorunsuz görüntü manipülasyonu için kapsamlı bir öğretici.
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: Java Görüntü İşleme – Aspose.PSD ile Kaydırmalarla Görüntüyü Kırpma
url: /tr/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Processing – Kaydırmalarla Görüntüyü Kırpma (Aspose.PSD)

## Introduction

Eğer **java image processing** ile çalışıyorsanız, kesin kırpmanın herhangi bir grafik iş akışının temel bir yapı taşı olduğunu çabucak fark edeceksiniz. Kenarları düzeltmek, istenmeyen arka planı kaldırmak veya varlıkları web teslimi için hazırlamak ister misiniz, **how to crop image** programlı olarak bilmek sayısız manuel saati tasarruf ettirir. Bu öğreticide, güçlü **Aspose.PSD for Java** kütüphanesini kullanarak her kenar için kaydırma değerleri belirleyerek bir raster görüntüyü nasıl kırpacağınızı adım adım göstereceğiz. Sonunda **use the crop method** konusunda kendinize güvenerek **optimize image cropping** yapabileceksiniz.

## Quick Answers
- **What library handles java image processing?** Aspose.PSD for Java  
- **Which method crops a raster image?** `RasterImage.crop(left, right, top, bottom)`  
- **Do I need to cache data first?** Yes – caching improves speed for large PSD files  
- **Can I set custom cropping margins?** Absolutely – specify left, right, top, and bottom shifts  
- **What output formats are supported?** JPEG, PNG, BMP, and many more via `ImageOptions`

## What is java image processing?
Java image processing, Java‑tabanlı API'ler kullanarak bitmap ve vektör grafiklerin işlenmesi anlamına gelir. Görevler arasında yeniden boyutlandırma, filtreleme, format dönüşümü ve **image cropping margins** ayarlamaları bulunur—tümü sunucu‑taraflı veya masaüstü uygulamalarda otomatikleştirilebilir.

## Why use Aspose.PSD for java image processing?
Aspose.PSD, Photoshop uyumlu PSD dosyalarını, katmanları, kanalları ve maskeleri anlayan saf‑Java bir çözüm sunar. Yerel kütüphanelere ihtiyaç duymaz, çapraz‑platform çalışır ve mevcut Java projeleriyle sorunsuz entegrasyon sağlayan **crop raster image** API'si sunar.

## Prerequisites

- **Java Development Kit (JDK)** – en son sürümü [here](https://www.oracle.com/java/technologies/javase-downloads.html) adresinden indirin.  
- **Aspose.PSD for Java Library** – en yeni sürümü [download page](https://releases.aspose.com/psd/java/) üzerinden edinin.  
- **Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA veya tercih ettiğiniz herhangi bir editör.

## Import Packages

Java projenizde kırpma iş akışına başlamak için gerekli sınıfları içe aktarın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

### Step 1: Load the Image (how to crop image)

Öncelikle kaynak PSD dosyasını bir `RasterImage` örneğine yükleyin. Bu, piksel düzeyinde doğrudan erişim sağlar.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Step 2: Cache Image Data (optimize image cropping)

Görüntü verilerini bellekte önbelleğe almak, kırpma gibi birden fazla işlem yaparken I/O yükünü azaltır.

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Step 3: Define Cropping Margins (image cropping margins)

Her bir kenardan kaç piksel kesmek istediğinizi belirtin. Bu değerleri istediğiniz **image cropping margins** ile eşleyecek şekilde ayarlayın.

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Step 4: Apply the Crop (use crop method)

Şimdi `crop` metodunu kaydırma değerleriyle çağırın. Bu **crop raster image** işlemi, temel bitmap'i değiştirir.

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### Step 5: Save the Results (how to crop image to a new format)

Son olarak kırpılmış görüntüyü diske yazın. Bu örnekte JPEG seçtik, ancak Aspose.PSD tarafından desteklenen herhangi bir format kullanılabilir.

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

Congratulations! You have successfully **cropped an image by shifts** using Aspose.PSD for Java, a core skill in any **java image processing** toolkit.

## Common Issues and Solutions

| Sorun | Çözüm |
|-------|----------|
| **`OutOfMemoryError` on large PSD files** | `cacheData()` metodunu (Adım 2) çağırdığınızdan emin olun ve JVM yığın boyutunu (`-Xmx`) artırmayı düşünün. |
| **Unexpected transparent borders** | Kaydırma değerlerinizin istenen kenar boşluklarını doğru yansıttığını doğrulayın; negatif değerler kesmek yerine genişletebilir. |
| **Saving in the wrong format** | `save` çağrısında uygun `ImageOptions` alt sınıfını (ör. `PngOptions`) kullandığınızdan emin olun. |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with all image formats?**  
A: Yes, Aspose.PSD supports a wide range of raster and vector formats, ensuring versatility in your projects.

**Q: Can I apply multiple cropping operations to the same image?**  
A: Absolutely. You can call `crop` repeatedly; each call works on the current state of the image.

**Q: Is there a community forum for Aspose.PSD support?**  
A: Yes, you can find support and engage with the community at [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: How can I obtain a temporary license for Aspose.PSD?**  
A: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain a temporary license.

**Q: Are there any sample projects showcasing Aspose.PSD functionalities?**  
A: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

## Conclusion

Bu rehberde, kaydırma değerleri belirleyerek **crop raster image** dosyalarını nasıl kırpacağınızı, **java image processing** için kritik bir teknik olduğunu öğrendiniz. Artık web için varlık hazırlama, küçük resim oluşturma veya taranmış belgeleri temizleme gibi daha büyük iş akışlarına kırpma işlevini entegre etmek için sağlam bir temele sahipsiniz.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}