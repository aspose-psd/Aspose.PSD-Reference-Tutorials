---
date: 2025-12-06
description: Aspose.PSD for Java kullanarak görüntüyü 270 derece döndürmeyi öğrenin.
  Bu kılavuz, PSD dosyalarını nasıl döndüreceğinizi, görüntüleri nasıl çevirip ters
  çevireceğinizi ve PSD'yi JPEG'e nasıl dönüştüreceğinizi gösterir.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Görüntüyü 270 Derece Döndürme
url: /tr/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotate Image 270 Degrees with Aspose.PSD for Java

## Introduction

Bu **java image processing tutorial**'da, Aspose.PSD for Java kullanarak **rotate image 270 degrees** işlemini hızlı ve güvenilir bir şekilde nasıl yapacağınızı keşfedeceksiniz. İster bir fotoğraf düzenleme aracı geliştiriyor olun, toplu dönüşümleri otomatikleştiriyor olun ya da sadece bir PSD katmanını yeniden yönlendirmek istiyor olun, kütüphane bu görevi zahmetsizce halleder. Ayrıca görüntüleri döndürüp çevirme ve döndürülmüş PSD'yi JPEG'e dönüştürme konularına da değineceğiz, böylece tam bir uçtan uca iş akışı elde edeceksiniz.

## Quick Answers
- **What library handles the rotation?** Aspose.PSD for Java  
- **Which rotation angle does the example use?** 270 degrees  
- **Can I also flip the image?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **How do I save the result?** In the example we save as JPEG using `JpegOptions`  
- **Do I need a license for production?** A valid Aspose.PSD license is required for commercial use  

## What is “rotate image 270 degrees”?
Bir resmi 270 derece döndürmek, resmi saat yönünde tam bir çemberin üçte ikisini (veya saat yönünün tersine 90 derece) çevirmek anlamına gelir. Birçok grafik düzenleme senaryosunda bu yönlendirme, bir dizi dönüşümden sonra orijinal portre düzeniyle eşleşir.

## Why use Aspose.PSD for this task?
- **Full PSD support** – works with layers, masks, and adjustment objects.  
- **No native Photoshop required** – run on any Java runtime.  
- **Simple API** – a single method call (`rotateFlip`) handles rotation and flipping.  
- **Easy format conversion** – export directly to JPEG, PNG, or other common formats.

## Prerequisites

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.PSD for Java** kütüphanesi yüklü. Tam API referansını [buradan](https://reference.aspose.com/psd/java/) indirebilir ve görüntüleyebilirsiniz.  
- Java geliştirme ortamı (JDK 8 veya üzeri).  
- Döndürmek istediğiniz örnek PSD dosyası. Kod içindeki `sourceFile` değişkenini dosyanızın doğru yolu ile güncelleyin.

## Import Packages

Aspose.PSD paketinden gerekli sınıfları içe aktararak başlayın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## How to Rotate PSD – Step 1: Load the Image

Kaynak PSD dosyanıza işaret eden bir `Image` örneği oluşturun:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## How to Rotate PSD – Step 2: Rotate the Image 270 Degrees

Döndürme işlemi için `rotateFlip` metodunu `RotateFlipType.Rotate270FlipNone` ile kullanarak 270 derece döndürme ve herhangi bir çevirme yapmadan elde edin:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Görüntüyü yatay veya dikey olarak da çevirmek isterseniz, `Rotate90FlipX` veya `Rotate180FlipY` gibi farklı bir `RotateFlipType` seçin.

## How to Rotate PSD – Step 3: Convert PSD to JPEG and Save

Döndürmeden sonra, uygun seçenek sınıfını kullanarak **convert PSD to JPEG** (veya başka bir desteklenen format) yapabilirsiniz:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

`RotatedImage_out.jpg` dosyası artık orijinal PSD içeriğini 270 derece döndürülmüş olarak JPEG formatında içerir.

## Common Issues and Solutions

| Sorun | Çözüm |
|-------|----------|
| **Image appears upside‑down** | `Rotate270FlipNone` kullandığınızdan emin olun. Saat yönünde 90 derece döndürme için `Rotate90FlipNone` kullanın. |
| **Output file is corrupted** | Hedef klasörün var olduğundan ve yazma izinlerinizin bulunduğundan emin olun. |
| **License exception** | Üretimde görüntüyü yüklemeden önce geçici veya kalıcı bir Aspose.PSD lisansı kurun. |

## Frequently Asked Questions

**S: Is Aspose.PSD compatible with different image formats?**  
C: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, and many other raster formats.

**S: Can I apply custom rotations, not just predefined flips?**  
C: Absolutely! While `RotateFlipType` provides common angles, you can combine multiple calls or use transformation matrices for arbitrary angles.

**S: How do I convert the rotated PSD to another format, such as PNG?**  
C: Replace `JpegOptions` with `PngOptions` (or the appropriate options class) in the `save` method.

**S: Where can I find additional support or assistance?**  
C: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**S: Is there a free trial available?**  
C: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).

**S: How do I obtain a temporary license?**  
C: If you need a temporary license, you can obtain one [here](https://purchase.aspose.com/temporary-license/).

## Conclusion

Artık **rotate image 270 degrees** işlemini Aspose.PSD for Java kullanarak nasıl yapacağınızı, gerektiğinde görüntüleri nasıl çevireceğinizi ve sonucu JPEG olarak nasıl dışa aktaracağınızı öğrendiniz. Bu basit iş akışı, Photoshop'a ihtiyaç duymadan PSD manipülasyonu üzerinde tam kontrol sağlayarak daha büyük Java‑tabanlı görüntü‑işleme hatlarına entegre edilebilir.

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}