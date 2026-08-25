---
date: 2026-08-01
description: Aspose.PSD kullanarak Java görüntü işleminde gamma ayarlamayı, PSD'yi
  TIFF'e dönüştürmeyi ve soluk görüntüleri düzeltmeyi kısa bir öğreticide öğrenin.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Bir Görüntünün Gamma'sını Ayarlama
og_description: Aspose.PSD kullanarak Java görüntü işleminde gamma ayarlamayı öğrenin
  – soluk görüntüleri düzelten ve PSD'yi birkaç satır kodla TIFF'e dönüştüren hızlı,
  sunucu‑taraflı bir kütüphane.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: gamma nasıl ayarlanır – Aspose.PSD ile Java işleme
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Aspose.PSD ile Java Görüntü İşleme'de Gamma Nasıl Ayarlanır
url: /tr/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD ile Java Görüntü İşleme'de Gamma Nasıl Ayarlanır

## Giriş

Eğer **java image processing** ile çalışıyorsanız, **gama nasıl ayarlanır** öğrenmek, ayrıntıyı kaybetmeden parlaklık ve kontrastı artırmak için temel bir tekniktir. Bu öğreticide **Aspose.PSD for Java** kullanarak bir PSD dosyasına gamma düzeltmesi uygulamayı, **convert PSD to TIFF** ve **soluk görüntü** oluşumunu önlemeyi adım adım göstereceğiz. Bu yaklaşımın hızlı, güvenilir ve **server‑side image processing** boru hatları için mükemmel olduğunu göreceksiniz.

## Hızlı Yanıtlar
- **Gamma düzeltmesi ne yapar?** Parlaklık değerlerini yeniden eşleyerek karanlık bölgeleri daha parlak, parlak bölgeleri daha karanlık hale getirir ve genel ayrıntıyı korur.  
- **İşlemeyi hangi kütüphane yönetir?** Aspose.PSD for Java, raster görüntüler için özel bir `adjustGamma` yöntemi sağlar.  
- **Aynı akışta PSD'yi TIFF'e dönüştürebilir miyim?** Evet – gamma ayarlamasından sonra görüntüyü doğrudan `TiffOptions` kullanarak TIFF olarak kaydedebilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme çalışır; üretim kullanımı için ticari bir lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Aspose.PSD, Java 8 ve üzerini destekler.

## Java Gamma Düzeltmesi Nedir?

Gamma düzeltmesi, kodlanmış piksel değerleri ile görüntülenen parlaklık arasındaki doğrusal olmayan ilişkiyi değiştirir. Gamma eğrisini ayarlayarak **soluk görüntü** sorunlarını düzeltebilir veya gölgelerdeki detayları artırabilirsiniz, vurguları aşırı aydınlatmadan. Her piksele bir güç‑kanunu fonksiyonu uygulayarak çalışır; bu, koyu tonları aydınlatır ve vurguları sıkıştırır, daha doğal bir görsel görünüm sağlar.

## Gamma Düzeltmesi için Aspose.PSD Neden Kullanılmalı?

Aspose.PSD, PSD formatının karmaşıklıklarını soyutlayan bir **java image processing library**'dir. 2 GB'a kadar dosyaları işleyebilir, 50'den fazla farklı görüntü formatını destekler ve basit bir `adjustGamma` çağrısı sağlar; bu da **java gamma correction** ve **convert PSD to TIFF** iş akışları için ideal kılar.

## Önkoşullar

1. **Java Development Environment** – Java 8 veya daha yeni bir sürüm yüklü.  
2. **Aspose.PSD Library** – JAR dosyasını indirip projenize ekleyin. Resmi [documentation](https://reference.aspose.com/psd/java/) sayfasına bakın.  
3. **Sample Image** – İşlemek istediğiniz bir PSD dosyası (örnek: `sample.psd`).  

## Paketleri İçe Aktarma

Başlamadan önce, raster işleme ve dosya‑format seçeneklerine erişim sağlayan temel ad alanlarını içe aktarın.

## Adım 1: Görüntüyü Yükle

`RasterImage` sınıfı, bir PSD katmanının bellekte rasterleştirilmiş piksel verilerini temsil eder. Görüntüyü bir kez yükleyip önbelleğe almak, sonraki ayarlamalar için bellek tüketimini azaltır.

## Adım 2: Gamma'yı Ayarla

`new RasterImage("sample.psd")` ile PSD'nizi yükleyin ve `rasterImage.adjustGamma(2.0f)` metodunu çağırın — bu tek satır, tüm renk kanallarında 2.0 gamma uygular, gölgeleri aydınlatır ve vurguları aynı tutar. Kanal‑spesifik ayarlamalar gerekiyorsa kırmızı, yeşil ve mavi için ayrı değerler de geçirebilirsiniz.

## Adım 3: TiffOptions Oluştur

`TiffOptions`, sıkıştırma, örnek başına bit ve diğer TIFF‑özel ayarları kontrol etmenizi sağlar. 8‑bit örnek (`{8,8,8}`) ayarlamak, TIFF dosya boyutunu makul tutar ve renk doğruluğunu korur.

## Adım 4: Sonuç Görüntüyü Kaydet

`rasterImage.save("output.tif", tiffOptions)` metodunu çağırarak işlenmiş görüntüyü diske yazın. Kaydettikten sonra, TIFF'i baskı hizmetleri veya web API'leri gibi sonraki sistemlere besleyebilirsiniz.

## Yaygın Kullanım Senaryoları

- **Otomatik grafik boru hatları** – Küçük resimler oluşturulmadan önce anlık olarak gamma ayarlayın.  
- **Toplu dönüşüm araçları** – Parlaklığı normalleştirirken büyük PSD arşivlerini TIFF'e dönüştürün.  
- **Web servisleri** – PSD alan, gamma düzeltmesi uygulayan ve istemci tüketimi için TIFF döndüren bir uç nokta sunun.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Olur | Nasıl Düzeltilir |
|-------|------------|-------------------|
| **Görüntü soluk görünüyor** | Gamma değeri çok yüksek (örnek: > 2.5) | Gamma faktörünü 1.8 ile 2.2 arasında bir değere düşürün. |
| **`rasterImage.isCached()` returns false** | Görüntü henüz belleğe yüklenmemiş | `rasterImage.cacheData()` metodunu gamma ayarlamadan önce çağırın. |
| **TIFF dosya boyutu büyük** | Örnek başına bit 16‑bit olarak ayarlanmış | Örnekte gösterildiği gibi 8‑bit örnek (`{8,8,8}`) kullanın. |

## Sıkça Sorulan Sorular

**Q: Her renk kanalına farklı gamma değerleri uygulayabilir miyim?**  
A: Evet – `adjustGamma` metodu, kırmızı, yeşil ve mavi kanallar için ayrı float değerleri kabul eder.

**Q: Kaydetmeden önce birden fazla görüntü ayarlamasını zincirleme yapmak mümkün mü?**  
A: Kesinlikle. Aynı `RasterImage` örneği üzerinde yeniden boyutlandırma, kırpma veya renk düzeltmeleri gibi işlemleri sıralı olarak yapabilirsiniz.

**Q: Aspose.PSD çok sayfalı PSD dosyalarını destekliyor mu?**  
A: Evet, her katmana ayrı ayrı erişilip işlenebilir.

**Q: TIFF dışında hangi formata dışa aktarabilirim?**  
A: Aspose.PSD, PNG, JPEG, BMP ve ilgili seçenek sınıfları aracılığıyla birçok diğer formatı destekler.

**Q: Gamma düzeltmesinden sonra soluk bir görüntüyü nasıl önleyebilirim?**  
A: Orta seviyede bir gamma (yaklaşık 2.0) ile başlayın ve sonucu önizleyin; görüntü çok parlak görünüyorsa gamma değerini azaltın.

## Sonuç

Tebrikler! **gama nasıl ayarlanır** konusunu **java image processing** iş akışında başarıyla öğrendiniz, bir PSD'yi TIFF'e dönüştürdünüz ve **soluk görüntü** gibi yaygın sorunlardan kaçındınız. Bu desen, parlaklık ve kontrast üzerinde ince ayar kontrolü sağlar ve otomatik grafik boru hatları, web servisleri veya masaüstü yardımcı programları için idealdir.

---

**Son Güncelleme:** 2026-08-01  
**Test Edilen:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Java Görüntü İşleme Öğreticisi - Aspose.PSD for Java ile Bir Görüntünün Parlaklığını Ayarlama](/psd/java/advanced-techniques/adjust-brightness/)
- [PSD'yi TIFF'e Dönüştürme ve Aspose.PSD for Java ile Kontrastı Ayarlama](/psd/java/advanced-techniques/adjust-contrast/)
- [Java'da PSD'yi Görüntüye Dönüştür – Aspose.PSD ile Ayar Katmanları Uygulama](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```