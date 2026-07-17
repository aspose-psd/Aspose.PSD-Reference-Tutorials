---
date: 2026-07-17
description: Aspose.PSD for Java kullanarak Medyan ve Wiener filtrelerini uygulama
  adım adım filtre tekniklerini öğrenin ve PSD'yi GIF'e verimli bir şekilde dönüştürün.
keywords:
- convert psd to gif
- remove salt pepper noise
- median filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Medyan ve Wiener Filtrelerini Uygula
og_description: Aspose.PSD for Java kullanarak PSD'yi GIF'e dönüştürün. Medyan ve
  Wiener filtrelerini nasıl uygulayacağınızı, salt‑pepper noise'ı nasıl kaldıracağınızı
  öğrenin ve high‑quality GIF'leri dışa aktarın.
og_image_alt: 'Developer guide: Convert PSD to GIF with Median and Wiener filters
  in Java using Aspose.PSD'
og_title: PSD'yi GIF'e Dönüştür – Medyan ve Wiener Filtrelerini Uygula (Java)
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  headline: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  type: TechArticle
- description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  name: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  steps:
  - name: Load the Image
    text: '`Image` is Aspose.PSD''s base class representing any supported image file.'
  - name: Cast Image into RasterImage
    text: '`RasterImage` extends `Image` and provides pixel‑level access for raster‑based
      operations.'
  - name: Create MedianFilterOptions Instance
    text: '`MedianFilterOptions` configures the median filter, allowing you to set
      the kernel size.'
  - name: Save the Resultant Image (Convert PSD to GIF)
    text: '`GifOptions` specifies settings for saving an image in GIF format, such
      as color depth and compression. `ExportFormat.Gif` is the enum value used to
      save an image as a GIF file. By following these steps you have successfully
      applied a Median filter and exported the cleaned image as a GIF.'
  type: HowTo
- questions:
  - answer: It reduces salt‑and‑pepper noise while preserving edges.
    question: What does the Median filter do?
  - answer: For adaptive noise reduction that considers local image variance.
    question: When should I use the Wiener filter?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the code?
  - answer: Yes—Aspose.PSD lets you **convert PSD to GIF** in a single step.
    question: Can I save the output as GIF?
  - answer: Typically under 10 minutes for a basic setup.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
- median filter
- wiener filter
title: PSD'yi GIF'e Dönüştür – Adım Adım Medyan ve Wiener Filtreleri (Java)
url: /tr/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi GIF'e Dönüştür: Median ve Wiener Filtrelerini Uygula (Java)

Eğer Java'da gürültülü görüntüleri temizlemek için **adım‑adım filtre** iş akışı arıyorsanız, doğru yerdesiniz. Aspose.PSD for Java, hem Median hem de Wiener filtrelerini uygulamayı basitleştirir ve işleme sonrasında **PSD'yi GIF'e dönüştürmenize** bile izin verir. Bu rehberde kütüphane kurulumundan son GIF'in kaydedilmesine kadar her aşamayı adım adım göstereceğiz—böylece uygulamalarınıza yüksek kaliteli görüntü gürültü azaltma işlevi ekleyebilirsiniz.

## Hızlı Yanıtlar
- **Median filtresi ne yapar?** Tuz‑ve‑biber gürültüsünü azaltır ve kenarları korur.  
- **Wiener filtresini ne zaman kullanmalıyım?** Yerel görüntü varyansını dikkate alan uyarlamalı gürültü azaltma için.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme yeterlidir; üretim için ticari lisans gereklidir.  
- **Çıktıyı GIF olarak kaydedebilir miyim?** Evet—Aspose.PSD, **PSD'yi GIF'e dönüştürmenizi** tek adımda sağlar.  
- **Uygulama ne kadar sürer?** Temel kurulum için genellikle 10 dakikadan az.

## Adım Adım Filtre Nedir?
*Adım‑adım filtre* yaklaşımı, görüntü işleme sürecini net, yönetilebilir aşamalara ayırır—görüntüyü yükleme, filtre seçeneklerini yapılandırma, filtreyi uygulama ve sonunda sonucu kaydetme. Bu metodik akış, her bölümü hata ayıklamanıza, kodu yeniden kullanmanıza ve süreci farklı görüntü formatlarına uyarlamanıza yardımcı olur.

## Neden Aspose.PSD for Java Kullanmalısınız?
Aspose.PSD for Java, **30+ görüntü formatını** destekler; PSD, PNG, JPEG, GIF, BMP ve TIFF dahil ve tüm dosyayı belleğe yüklemeden çok sayfalı belgeleri işleyebilir. Kütüphanenin **sıfır dış bağımlılığı** vardır, yani yerel ikili dosyalar hakkında endişelenmeden herhangi bir Java projesine entegre edebilirsiniz. Median ve Wiener gibi yerleşik filtre seçenekleri kutudan çıkar çıkmaz hazırdır ve API, işleme sonrasında doğrudan GIF, PNG veya JPEG olarak dışa aktarmak için tek tıkla dönüşüm yolu sunar.

## Önkoşullar

Başlamadan önce şunların olduğundan emin olun:

1. **Aspose.PSD for Java Kütüphanesi** – Kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirin ve kurun. Diğer Aspose ürünleri için [buraya](https://releases.aspose.com/) bakın.  
2. **Java Geliştirme Ortamı** – JDK 8+ ve makinenizde bir IDE veya yapı aracı (Maven/Gradle) kurulu.

## Paketleri İçe Aktarma

`Image`, `RasterImage` ve filtre seçenek sınıfları, görüntü işleme ve gürültü azaltma üzerinde tam kontrol sağlar.

## Aspose.PSD (Java) Kullanarak PSD'yi GIF'e Nasıl Dönüştürürsünüz

PSD'nizi yükleyin, istediğiniz filtreyi uygulayın ve GIF formatıyla `save` metodunu çağırın—hepsi birkaç kısa satırda. Bu doğrudan‑cevap modeli, her bir adıma dalmadan önce tam dönüşüm akışını görmenizi sağlar. Kaydederken renk derinliği veya sıkıştırma seviyesi gibi ek seçenekler de belirtebilirsiniz.

## Adım Adım Filtre: Median Filtre Nasıl Uygulanır

Median filtresi, kenarları keskin tutarken **tuz‑ve‑biber gürültüsünü** ortadan kaldırır. Her piksel üzerinde bir pencere kaydırarak çalışır ve merkezdeki değeri çevredeki değerlerin medyanı ile değiştirir; böylece önemli detayları bulanıklaştırmadan aykırı değerleri etkili bir şekilde yok eder.

### Adım 1: Görüntüyü Yükle

`Image`, Aspose.PSD'nin desteklenen herhangi bir görüntü dosyasını temsil eden temel sınıfıdır.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

### Adım 2: Görüntüyü RasterImage'ye Dönüştür

`RasterImage`, `Image` sınıfını genişletir ve raster tabanlı işlemler için piksel‑seviye erişim sağlar.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### Adım 3: MedianFilterOptions Örneği Oluştur

`MedianFilterOptions`, median filtresini yapılandırır ve çekirdek (kernel) boyutunu ayarlamanıza olanak tanır.

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Adım 4: Median Filtreyi Uygula

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Adım 5: Sonuç Görüntüyü Kaydet (PSD'yi GIF'e Dönüştür)

`GifOptions`, GIF formatında bir görüntüyü kaydetmek için renk derinliği ve sıkıştırma gibi ayarları belirler. `ExportFormat.Gif`, bir görüntüyü GIF dosyası olarak kaydetmek için kullanılan enum değeridir.

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

Bu adımları izleyerek Median filtresini başarıyla uyguladınız ve temizlenmiş görüntüyü GIF olarak dışa aktardınız.

## Wiener Filtreyi Uygulama (İsteğe Bağlı Uzantı)

Wiener filtresi, yerel varyansı tahmin ederek uyarlamalı gürültü azaltma yapar; bu da değişken gürültü seviyelerine sahip görüntüler için idealdir. Median filtresini `WienerFilterOptions` ile değiştirin ve aynı iş akışını sürdürün.

> **Pro ipucu:** Her iki filtre için de farklı çekirdek boyutları deneyerek gürültü kaldırma ve detay koruma arasında en iyi dengeyi bulun.

## Yaygın Sorunlar ve Sorun Giderme

| Semptom | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| `ClassCastException` when casting to `RasterImage` | Girdi dosyası raster‑uyumlu bir PSD değil | PSD'nin raster katmanlar içerdiğini doğrulayın veya katmanları önce raster’a dönüştürün |
| Output GIF is blank | Hedef yol hatalı veya klasör yazma iznine sahip değil | `dataDir`'in mevcut ve yazılabilir bir dizine işaret ettiğinden emin olun |
| Filter seems to have no effect | Çekirdek boyutu gürültü seviyesi için çok küçük | Filtre boyutunu artırın (ör. `new MedianFilterOptions(6)`) |

## Sıkça Sorulan Sorular

**S1: Bu filtreleri herhangi bir formatta görüntülere uygulayabilir miyim?**  
C1: Evet, Aspose.PSD 30'dan fazla formatı destekler, bu yüzden PSD, PNG, JPEG, BMP, TIFF ve daha fazlasını filtreleyebilirsiniz.

**S2: Aspose.PSD for Java için ücretsiz deneme mevcut mu?**  
C2: Evet, ücretsiz denemeyi [buradan](https://releases.aspose.com/) alabilirsiniz.

**S3: Aspose.PSD for Java için desteği nasıl alabilirim?**  
C3: Topluluk desteği için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

**S4: Resmi belgeleri nerede bulabilirim?**  
C4: Belgeleri [buradan](https://reference.aspose.com/psd/java/) inceleyin.

**S5: Ticari lisansı nasıl satın alabilirim?**  
C5: Ürünü [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

## Sonuç

Bu rehberde, Aspose.PSD for Java kullanarak Median (ve isteğe bağlı olarak Wiener) filtrelerini uygulamak için bir **adım‑adım filtre** sürecini gösterdik ve gürültü azaltma sonrasında **PSD'yi GIF'e dönüştürmeyi** anlattık. Bu yapı taşlarıyla, fotoğrafları temizlemek, web için varlıkları hazırlamak veya toplu dönüşümleri otomatikleştirmek gibi senaryolarda, herhangi bir Java uygulamasına sağlam görüntü‑işleme boru hatları entegre edebilirsiniz.

---

**Son Güncelleme:** 2026-07-17  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [PSD'yi GIF'e Dönüştür - Aspose.PSD for Java ile Renkli Görüntüler İçin Gaussian ve Wiener Filtrelerini Uygula](/psd/java/image-processing/apply-gaussian-wiener-filters-color-image/)
- [Adım Adım Filtre - Aspose.PSD for Java ile Hareket Wiener Filtrelerini Uygula](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Aspose.PSD for Java Kullanarak PSD'yi GIF'e Nasıl Dönüştürürsünüz – Kayıplı Sıkıştırıcı](/psd/java/advanced-image-manipulation/implement-lossy-gif-compressor/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```