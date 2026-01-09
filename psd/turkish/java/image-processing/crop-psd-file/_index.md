---
date: 2026-01-09
description: Aspose.PSD kullanarak Java'da PSD'yi PNG'ye dönüştürmeyi ve PSD dosyalarını
  kırpmayı öğrenin. Hassas görüntü işleme artık kolay.
linktitle: Crop PSD File
second_title: Aspose.PSD Java API
title: PSD'yi PNG'ye Dönüştürün ve Aspose.PSD for Java ile Kırpın
url: /tr/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java kullanarak PSD'yi PNG'ye Dönüştürme ve PSD Dosyasını Kırpma

## Introduction

Eğer **PSD'yi PNG'ye dönüştürmeniz** ve aynı zamanda görüntüyü ihtiyacınız olan tam bölgeye kırpmanız gerekiyorsa, Aspose.PSD for Java bunu temiz ve programatik bir şekilde yapmanızı sağlar. Bu öğreticide, projenizi kurmaktan kırpılmış bir PSD ve PNG ihracatını kaydetmeye kadar tüm süreci adım adım göstereceğiz; böylece herhangi bir Java uygulamasına kesin görüntü işleme entegrasyonu ekleyebilirsiniz.

## Quick Answers
- **Aspose.PSD PSD'yi PNG'ye dönüştürebilir mi?** Evet, tam katman bütünlüğüyle doğrudan dönüşümü destekler.  
- **Kırpma için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri önerilir.  
- **PNG şeffaflığı korur mu?** Evet, `PngColorType.TruecolorWithAlpha` kullanılarak.  
- **Büyük dosyalar için işlem hızlı mı?** Aspose.PSD yüksek çözünürlüklü PSD'lerde performans için optimize edilmiştir.

## What is “convert PSD to PNG” and why crop it?

Photoshop Belgesi (PSD) dosyasını PNG'ye dönüştürmek, web için hazır bir görüntü veya tasarımın hafif bir sürümüne ihtiyaç duyduğunuzda yaygın bir adımdır. Kırpma, sadece ihtiyacınız olan tuval kısmını çıkarmanızı sağlar, dosya boyutunu azaltır ve ilgili içeriğe odaklanır. Her iki eylemi tek bir iş akışında birleştirmek zaman kazandırır ve kod tabanınızı basit tutar.

## Prerequisites

- **Java Geliştirme Ortamı** – JDK 8+ yüklü ve yapılandırılmış.  
- **Aspose.PSD for Java** – Kütüphaneyi indirin ve projenize ekleyin. Kütüphaneyi ve belgelerini [burada](https://reference.aspose.com/psd/java/) bulabilirsiniz.  
- **Örnek PSD Dosyası** – Proje dizininizde kırpıp dönüştürmek istediğiniz bir PSD dosyası.

## Import Packages

Java projenizde, Aspose.PSD işlevselliğinden yararlanmak için gerekli paketleri içe aktarın. Aşağıdaki import ifadelerini ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

## Step 1: Set Document Directory

```java
String dataDir = "Your Document Directory";
```

“Your Document Directory” ifadesini PSD dosyanızın bulunduğu gerçek yol ile değiştirin.

## Step 2: Load PSD File

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

Kırpmak istediğiniz PSD dosyasını bir `RasterImage` nesnesine yükleyin.

## Step 3: Define Crop Area

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

`Rectangle` sınıfını kullanarak kırpmak istediğiniz alanı belirtin; **x**, **y**, **width** ve **height** değerlerini sağlayın.

## Step 4: Save Cropped PSD

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

Kırpılmış görüntüyü belirtilen yol ile PSD formatında kaydedin.

## Step 5: Save Cropped Image as PNG

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

Ek olarak, kırpılmış görüntüyü şeffaflığı koruyarak bir PNG dosyası olarak dışa aktarın.

## Why use Aspose.PSD for Java to crop PSD files?

- **Tam PSD bütünlüğü** – Tüm katmanlar, maskeler ve efektler dönüşüm sırasında aynı kalır.  
- **Yerel Photoshop gerekmez** – Tamamen sunucu tarafında çalışır.  
- **Yüksek performans** – Büyük dosyalar ve toplu işleme için optimize edilmiştir.  
- **Basit API** – Birkaç satır kodla kırpma ve dönüşüm gerçekleştirilebilir.

## Common Issues and Solutions

| Sorun | Çözüm |
|-------|----------|
| **Dosya bulunamadı** | `dataDir`'in bir yol ayırıcı (`/` veya `\\`) ile bittiğini doğrulayın. |
| **Şeffaf arka plan kayboldu** | `PngOptions.setColorType(PngColorType.TruecolorWithAlpha)` ayarlandığından emin olun. |
| **Büyük PSD'lerde bellek yetersizliği** | Görüntüyü parçalar halinde işleyin veya JVM yığın boyutunu artırın (`-Xmx`). |
| **Lisans istisnası** | Görüntüyü yüklemeden önce Aspose lisansınızı uygulayın (`License license = new License(); license.setLicense("Aspose.PSD.lic");`). |

## Frequently Asked Questions

**S: Aspose.PSD for Java'yi diğer formatlardaki görüntüleri kırpmak için kullanabilir miyim?**  
C: Birincil odak PSD olsa da, kütüphane PNG, JPEG, BMP ve diğer raster formatlarını da destekler.

**S: Aspose.PSD büyük ölçekli görüntü işleme için uygun mu?**  
C: Evet, performans için optimize edilmiştir ve toplu işlemleri verimli bir şekilde yönetebilir.

**S: Üretim kullanımı için lisans konuları var mı?**  
C: Evet, detaylar için [Aspose.PSD for Java satın alma sayfasına](https://purchase.aspose.com/buy) bakın.

**S: Topluluk desteğini nereden alabilirim?**  
C: Diğer geliştiricilerden yardım almak için [Aspose.PSD for Java forumuna](https://forum.aspose.com/c/psd/34) ziyaret edin.

**S: Kütüphaneyi satın almadan önce deneyebilir miyim?**  
C: Kesinlikle—ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

## Conclusion

Artık **PSD'yi PNG'ye dönüştürürken** görüntüyü ihtiyacınız olan tam bölgeye kırpmak için eksiksiz, uçtan uca bir çözüme sahipsiniz. Bu kod parçacıklarını Java projelerinize entegre ederek Photoshop tarzı görüntü işleme işlemlerini Photoshop'un kendisi olmadan otomatikleştirebilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-09  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

---