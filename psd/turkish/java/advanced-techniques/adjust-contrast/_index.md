---
date: 2026-07-27
description: Aspose.PSD for Java, önde gelen bir Java görüntü işleme kütüphanesi kullanarak
  PSD'yi TIFF'e dönüştürmeyi ve görüntü kontrastını ayarlamayı öğrenin.
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: PSD'yi TIFF'e Dönüştürün ve Kontrastı Ayarlayın
og_description: Aspose.PSD for Java kullanarak kontrast ayarıyla PSD'yi TIFF'e dönüştürün.
  Bu kılavuz adım adım kod, performans ipuçları ve yüksek kaliteli TIFF çıktısı için
  dışa aktarma seçeneklerini gösterir.
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: PSD'yi TIFF'e Dönüştür & Kontrastı Ayarla – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: Aspose.PSD for Java ile PSD'yi TIFF'e Dönüştürün ve Kontrastı Ayarlayın
url: /tr/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi TIFF'e Dönüştürme ve Aspose.PSD for Java ile Kontrastı Ayarlama

## Giriş

Grafiklerinizin görsel kalitesini ince ayar yaparken **PSD'yi TIFF'e dönüştürmeniz** gerekiyorsa, doğru yerdesiniz. Bu öğreticide Aspose.PSD for Java—güçlü bir **java image manipulation** kütüphanesini kullanarak tam iş akışını adım adım göstereceğiz. **Görüntü kontrast ayarını** artırmayı, performans için büyük raster verileri önbelleğe almayı ve sonunda **görüntüyü TIFF olarak kaydetmeyi** öğreneceksiniz. Hadi başlayalım!

## Hızlı Yanıtlar
- **‘adjust contrast’ ne anlama gelir?** En karanlık ve en parlak pikseller arasındaki farkı değiştirir, detayların ortaya çıkmasını sağlar.  
- **Bu işlemi hangi kütüphane gerçekleştirir?** Aspose.PSD for Java – tam özellikli bir görüntü işleme araç seti.  
- **Bir lisansa ihtiyacım var mı?** **Geçici bir Aspose lisansı** test için yeterlidir; üretim için tam lisans gereklidir.  
- **PSD'yi TIFF'e dönüştürebilir miyim?** Kesinlikle – işlenmiş görüntüyü dışa aktarmak için `TiffOptions` kullanacağız.  
- **Dönüşüm ne kadar hızlı?** Tipik bir 30 MB PSD için tüm işlem hattı modern bir CPU'da bir saniyenin altında çalışır.

## Görüntü Kontrast Ayarı Nedir?
Kontrast ayarı, bir görüntünün ton aralığını değiştirerek ışık ve karanlık bölgeler arasındaki farkı artırır. Bu, tarama sonrası görüntüler düz göründüğünde veya baskı için grafik hazırlarken özellikle faydalıdır. Piksel yoğunluklarının histogramını genişleterek veya sıkıştırarak çalışır, gölgeleri daha derin ve vurguları daha parlak hâle getirir, bu da algılanan derinlik ve detayı artırır.

## Neden Aspose.PSD for Java Kullanılmalı?
Aspose.PSD, **50+ raster ve vektör formatını** işleyebilen, dosyaları tam bellek yüklemesi yapmadan 500 MB'a kadar işleyebilen ve TIFF'e bit‑per‑sample ve fotometrik yorumlama üzerinde hassas kontrol sağlayan yüksek performanslı, özellik‑zengin bir motor sunar. Bu ölçülebilir yetenekler, onu kurumsal düzeydeki görüntü iş akışları için birincil tercih yapar.

## Ön Koşullar

Başlamadan önce şunlara sahip olduğunuzdan emin olun:

- Java programlamaya temel bilgi.  
- Aspose.PSD for Java kütüphanesi yüklü. Bunu [buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.

## Paketleri İçe Aktarma

Java sınıfınıza gerekli içe aktarmaları ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Adım 1: Görüntüyü Yükleme

`Image` sınıfı, Aspose.PSD’nin bellekte herhangi bir desteklenen raster görüntüyü temsil eden giriş noktasıdır.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Kaynak PSD dosyasını (`sample.psd`) bir `Image` nesnesine yüklüyoruz; bu nesne sonraki tüm işlemler için giriş noktası görevi görür.

## Adım 2: RasterImage'ye Dönüştürme ve Veriyi Önbelleğe Alma

`RasterImage` doğrudan piksel‑seviyesinde erişim sağlar ve büyük dosyalar için önbelleğe almayı etkinleştirir.  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage`'e dönüştürmek, piksel‑seviyesinde işlemlere erişim sağlar. Önbelleğe alma, özellikle büyük dosyalarda performansı artırır.

## Görüntünün Kontrastını Nasıl Ayarlarsınız

`adjustContrast` yöntemi, görüntü kontrastını yüzde değeriyle değiştiren basit bir API çağrısıdır.  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` yöntemi, yüzde değişimini temsil eden bir tam sayı alır. Bu örnekte kontrastı **%50** artırıyoruz.

## Aspose.PSD Kullanarak PSD'yi TIFF'e Dönüştürme

`TiffOptions`, örnek başına bit, sıkıştırma türü ve fotometrik yorumlama gibi TIFF'e özgü ayarları belirlemenizi sağlar.  
```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Burada `TiffOptions`'ı (örnek başına bit, fotometrik yorumlama) yapılandırıyor ve **görüntüyü TIFF olarak kaydediyoruz**. Bu adım **PSD'yi TIFF'e dönüştürme** iş akışını tamamlar.

## Yaygın Sorunlar ve Çözümleri
- **Görüntü önbelleğe alınmadı:** Büyük PSD'lerde `OutOfMemoryError` almamak için her zaman `cacheData()` çağırın.  
- **Beklenmeyen renk kayması:** `setPhotometric`'in hedef renk uzayınızla (RGB vs. CMYK) eşleştiğini doğrulayın.  
- **Dosya bulunamadı:** `dataDir`'in doğru klasöre işaret ettiğinden ve dosya adının doğru yazıldığından emin olun.

## Sıkça Sorulan Sorular

### Q1: Aspose.PSD farklı görüntü formatlarıyla uyumlu mu?

A1: Evet, Aspose.PSD **50+ giriş ve çıkış formatını** destekler; PSD, TIFF, PNG, JPEG, BMP ve GIF dahil, projeler arasında esneklik sağlar.

### Q2: Aspose.PSD için geçici bir lisans nasıl alabilirim?

A2: Geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

### Q3: Aspose.PSD belgelerini nerede bulabilirim?

A3: Belgeler [burada](https://reference.aspose.com/psd/java/) mevcuttur.

### Q4: Aspose.PSD için hangi destek seçenekleri mevcuttur?

A4: Destek için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

### Q5: Aspose.PSD satın alabilir miyim?

A5: Evet, Aspose.PSD'yi [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

## Sonuç

Artık **PSD'yi TIFF'e nasıl dönüştüreceğinizi** ve Aspose.PSD for Java kullanarak **görüntü kontrast ayarını** nasıl yapacağınızı biliyorsunuz. Bu adımlar, kodu temiz ve sürdürülebilir tutarken görüntü kalitesi üzerinde ayrıntılı kontrol sağlar. İhtiyacınıza göre `adjustBrightness` veya `adjustGamma` gibi diğer ayar yöntemlerini denemekten çekinmeyin.

---

**Son Güncelleme:** 2026-07-27  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Java Görüntü İşleme Öğreticisi - Aspose.PSD for Java ile Bir Görüntünün Parlaklığını Ayarlama](/psd/java/advanced-techniques/adjust-brightness/)
- [Aspose.PSD ile Java Görüntü İşlemede Gamma Nasıl Ayarlanır](/psd/java/advanced-techniques/adjust-gamma/)
- [Aspose.PSD for Java ile PSD'yi Raster Görüntü Formatlarına Dönüştürme](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}