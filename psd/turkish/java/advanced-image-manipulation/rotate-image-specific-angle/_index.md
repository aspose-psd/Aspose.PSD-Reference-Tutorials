---
date: 2026-02-12
description: Aspose.PSD kullanarak Java’da belirli bir açıyla resmi nasıl döndüreceğinizi
  öğrenin. Bu kılavuz, resmi nasıl döndüreceğinizi, derece cinsinden nasıl döndüreceğinizi
  ve arka plan renklerini nasıl yöneteceğinizi gösterir.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Belirli Bir Açıda Görüntüyü Döndürme
url: /tr/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Belirli Bir Açıda Görüntüyü Döndürme

## Introduction

Eğer bir Java uygulamasında **görüntüyü nasıl döndürürsünüz** programlı olarak yapmanız gerekiyorsa, Aspose.PSD for Java ağır işleri halleden temiz ve yüksek‑performanslı bir API sunar. Bir fotoğraf düzenleyici oluşturuyor, küçük resimler üretiyor ya da bir web servisi için varlıklar hazırlıyor olun, görüntüyü tam bir dereceyle döndürmek yaygın bir gereksinimdir. Bu öğreticide, PSD dosyasını yüklemekten döndürülmüş sonucu kaydetmeye kadar tam süreci adım adım inceleyecek ve önbellekleme ve arka plan yönetimi gibi en iyi uygulamaları vurgulayacağız.

## Quick Answers
- **Java'da görüntüleri döndürmek için en iyi kütüphane hangisidir?** Aspose.PSD for Java.  
- **Herhangi bir dereceyle döndürebilir miyim?** Evet, `rotate` metodu bir `float` açı (pozitif veya negatif) kabul eder.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme testi için çalışır; üretim için lisans gereklidir.  
- **Hangi görüntü formatları destekleniyor?** PSD, JPEG, PNG, TIFF, GIF, BMP ve daha birçokları.  
- **Boş alan için arka plan rengini nasıl ayarlarım?** `rotate` metoduna bir `Color` örneği geçin.

## What is Image Rotation in Java?

Görüntü döndürme, piksel matrisini belirli bir açıyla (genellikle merkez) bir dönme noktasının etrafında çevirmek anlamına gelir. Java’da bunu `Graphics2D` ile manuel olarak yapabilirsiniz, ancak Aspose.PSD matematiği soyutlar, farklı renk derinliklerini yönetir ve PSD dosyalarıyla çalışırken katman bilgilerini korur.

## Why Use Aspose.PSD for Rotating Images?

- **Precision:** Kalite kaybı olmadan herhangi bir kesirli dereceyle döndürür.  
- **Performance:** Yerleşik önbellekleme (`image.cacheData()`) büyük dosyaları hızlandırır.  
- **Background Control:** Döndürme sonucu oluşan boşlukları doldurmak için bir arka plan rengi belirleyin.  
- **Format Flexibility:** PSD yükleyin, JPEG, PNG veya desteklenen herhangi bir formatta çıktı alın.

## Prerequisites

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK 8 veya daha yeni)** – çalışan bir Java IDE’si veya komut‑satırı ortamı.  
2. **Aspose.PSD for Java** – en son JAR dosyasını [Aspose.PSD Java sayfasından](https://reference.aspose.com/psd/java/) indirin.  
3. **Örnek PSD dosyası** – örneğin, kodunuzdan referans verebileceğiniz bir klasöre yerleştirilmiş `sample.psd`.

## Import Packages

İhtiyacımız olan sınıfları ilk olarak içe aktarın. Bu içe aktarmalar, seçtiğiniz döndürme açısına bakılmaksızın aynı kalır.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Your Document Directory

Kaynak PSD’nin bulunduğu ve çıktının yazılacağı klasörü ayarlayın.

```java
String dataDir = "Your Document Directory";
```

> **Pro tip:** Göreli‑yol sürprizlerinden kaçınmak için mutlak bir yol veya `System.getProperty("user.dir")` kullanın.

### Step 2: Specify Source and Destination File Paths

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

`destName` değerini, çıktı ihtiyacınıza göre (`.png`, `.tiff` vb.) desteklenen herhangi bir uzantıya değiştirebilirsiniz.

### Step 3: Load the Image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` dosya formatını otomatik olarak algılar ve raster‑tabanlı işlemler için somut bir `RasterImage` döndürür.

### Step 4: Cache Image Data (Optional but Recommended)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Önbellekleme, görüntü piksellerini bellekte saklar; bu da sonraki dönüşümleri hızlandırır—özellikle büyük PSD dosyaları için faydalıdır.

### Step 5: Rotate the Image

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – derece cinsinden döndürme açısı (float). Bu değeri, örneğin `-45f` gibi bir açıyla döndürmek için değiştirin.  
- **true** – döndürülmüş görüntüyü sığdırmak için tuvali genişletirken orijinal en‑boy oranını korur.  
- **Color.getRed()** – döndürme sonucu oluşan boş köşeleri dolduran arka plan rengi. İhtiyaca göre `Color.getWhite()` veya başka bir özel renk ile değiştirin.

#### Rotate Image by Degrees in Java

`rotate` metodu herhangi bir kayan‑nokta değeri kabul eder, böylece `30f`, `90f` veya `-15f` gibi **görüntüyü dereceyle döndür**ebilirsiniz. Pozitif değerler saat yönünde, negatif değerler saat yönünün tersine döndürür.

#### Rotate Image Specific Angle Using Aspose.PSD

Metot bir `float` ile çalıştığı için, grafik‑tasarım iş akışlarında hassas kontrol sağlamak amacıyla **görüntüyü belirli bir açıyla döndür** gibi `22.5f` gibi bir değer belirtebilirsiniz.

#### Rotate Image Java Example Summary

Yukarıdaki tüm adımlar, **rotate image java** iş akışını—dosyanın yüklenmesinden döndürülmüş çıktının kaydedilmesine kadar—tamamen göstermektedir.

### Step 6: Save the Result

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` kalite, sıkıştırma ve diğer JPEG‑özel ayarları kontrol etmenizi sağlar. Kayıpsız çıktı için `PngOptions` ile değiştirin.

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Döndürme sonrası boş köşeler** | Arka plan rengi belirtilmemiş | `rotate` metoduna bir `Color` (ör. `Color.getWhite()`) geçin. |
| **Büyük PSD’lerde bellek yetersizliği hatası** | Görüntü önbelleğe alınmamış | İşleme başlamadan önce `image.cacheData()` çağırın. |
| **Yanlış açı yönü** | Negatif ve pozitif açı karışıklığı | Saat yönünde döndürmek için negatif değer (veya koordinat sisteminize göre ters) kullanın. |
| **Değişiklikler kaydedilmedi** | `save` çağrısının unutulması | Döndürmeden sonra `image.save(...)` komutunun çalıştığından emin olun. |

## Frequently Asked Questions

**S: Aspose.PSD for Java kullanarak şeffaflık içeren görüntüleri döndürebilir miyim?**  
C: Evet. Kütüphane alfa kanallarını korur; şeffaf köşeler istiyorsanız opak bir arka plan rengi belirtmekten kaçının.

**S: Döndürme için desteklenen görüntü dosya formatlarıyla ilgili herhangi bir sınırlama var mı?**  
C: Hayır. Aspose.PSD PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF ve daha birçok formatı destekler.

**S: Görüntüleri negatif bir açıyla döndürebilir miyim?**  
C: Kesinlikle. Saat yönünde döndürmek için `rotate` metoduna negatif bir float (ör. `-30f`) geçin.

**S: Aspose.PSD döndürme sırasında gerçek‑zamanlı görüntü önizlemesi sağlar mı?**  
C: API yalnızca sunucu tarafıdır. Canlı önizlemeler için döndürülmüş bitmap’i bir UI çerçevesine (Swing, JavaFX) entegre edip görünümü yenileyin.

**S: Aspose.PSD için sorular sorabileceğim bir topluluk forumu var mı?**  
C: Evet, sorularınızı sormak ve deneyimlerinizi paylaşmak için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

## Conclusion

Artık Aspose.PSD for Java kullanarak belirli bir açıyla **görüntüyü nasıl döndürürsünüz** dosyalarını biliyorsunuz. Önbellekleme, arka plan rengi kontrolü ve esnek çıktı seçeneklerinden yararlanarak, herhangi bir Java‑tabanlı görüntü iş akışına kesin döndürme işlevselliği entegre edebilirsiniz.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}