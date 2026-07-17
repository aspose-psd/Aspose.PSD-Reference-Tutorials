---
date: 2026-07-17
description: Aspose.PSD kullanarak Java görüntü işleme öğreticisi, Gaussian ve Wiener
  filtrelerini adım adım nasıl uygulayacağınızı öğrenin ve çarpıcı görsel sonuçlar
  elde edin.
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Gaussian ve Wiener Filtrelerini Uygula
og_description: Java görüntü işleme öğreticisi, Aspose.PSD for Java ile Gaussian ve
  Wiener filtrelerini uygulamayı gösterir, PNG ve diğer formatlara dışa aktarmayı
  içerir.
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: Java Görüntü İşleme Öğreticisi – Gaussian & Wiener Filtrelerini Uygulama
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: Java Görüntü İşleme Öğreticisi – Gaussian & Wiener Filtrelerini Uygulama
url: /tr/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Görüntü İşleme Eğitimi – Aspose.PSD ile Gaussian ve Wiener Filtrelerini Uygulama

## Giriş

Java için **java image processing tutorial**'ımıza hoş geldiniz. Bu eğitimde Aspose.PSD for Java kullanarak Gaussian ve Wiener filtrelerini nasıl uygulayacağınızı göstereceğiz. Gürültülü fotoğrafları temizlemek ya da web için grafik hazırlamak isterken, bu filtreler size pürüzsüz, profesyonel görünümlü sonuçlar verir. Önümüzdeki birkaç dakikada tam iş akışını göreceksiniz – bir PSD dosyasını yüklemekten filtrelenmiş çıktıyı GIF olarak kaydetmeye kadar.

## Hızlı Yanıtlar
- **Gaussian filtresi ne yapar?** Görüntüyü komşu pikselleri ortalayarak yumuşatır, yüksek frekanslı gürültüyü azaltır.  
- **Wiener filtresi nedir?** Kenarları korurken gürültüyü azaltan adaptif bir yumuşatma gerçekleştirir.  
- **Hangi kütüphane kullanılıyor?** Aspose.PSD for Java, her iki filtre için yerleşik destek sağlar.  
- **Lisans gerekir mi?** Deneme sürümü test için çalışır, ancak üretim ortamı için ticari lisans gereklidir.  
- **GIF dışındaki formatlar çıkış olarak alınabilir mi?** Evet—Aspose.PSD PNG, JPEG, BMP ve daha birçok formatı destekler.

## Java Görüntü İşleme Eğitimi Nedir?

Java görüntü işleme eğitimi, geliştiricilere bir görüntüyü yükleme, filtreleme veya yeniden boyutlandırma gibi dönüşümler uygulama ve son olarak istediğiniz formatta kaydetme adımlarını gösterir. Açık kod örnekleri ve açıklamalar sayesinde, görüntü işleme yeteneklerini doğrudan Java uygulamalarına entegre edebilir, harici araçlara olan ihtiyacı azaltabilirsiniz.

## Neden Gaussian ve Wiener Filtreleri Kullanılır?

Görüntünüzü yükleyin, birleşik Gaussian‑Wiener filtresini uygulayın ve tanelerde çarpıcı bir azalma, kenarların ise keskin kalmasını göreceksiniz—web grafiklerini veya arşiv taramalarını hazırlamak için ideal. Gaussian kısmı yüksek frekanslı gürültüyü ortadan kaldırırken, Wiener kısmı yerel varyansa göre uyum sağlayarak en önemli detayları korur.

## Ön Koşullar

Başlamadan önce şunların olduğundan emin olun:

- Java geliştirme ortamı (JDK 8 veya daha yeni).  
- Aspose.PSD for Java kütüphanesi. **[burada](https://releases.aspose.com/psd/java/)** indirebilirsiniz.  
- Java sözdizimi ve nesne‑yönelimli kavramlara temel aşinalık.

## Paketleri İçe Aktar

İçe aktarma ifadeleri, raster görüntüler, filtre seçenekleri ve çıktı formatlarıyla çalışabilmeniz için Aspose.PSD sınıflarını kapsam içine alır.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Bu importlar, görüntü yükleme, raster manipülasyonu, filtre seçenekleri ve çıktı formatlarına erişim sağlar.

## Adım 1: Görüntüyü Yükle

`RasterImage` sınıfı, piksel piksel işlenebilen raster‑tabanlı bir görüntüyü temsil eder.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

Belirtilen dizinden bir PSD dosyasını yüklüyor ve piksel verileriyle çalışabilmek için `RasterImage` tipine dönüştürüyoruz.

## Adım 2: RasterImage'ı Kontrol Et

Bir güvenlik kontrolü, yüklenen dosyanın raster‑tabanlı olduğunu doğrular; aksi takdirde rutin nazikçe sonlanır.

```java
if (rasterImage == null) {
    return;
}
```

## Adım 3: Filtre Seçeneklerini Yapılandır

`GaussWienerFilterOptions` sınıfı, tek bir nesnede hem Gaussian hem de Wiener parametrelerini ince ayar yapmanıza olanak tanır.

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- İlk argüman (`12`), Gaussian çekirdeği için yarıçap boyutunu tanımlar.  
- İkinci argüman (`3`), Wiener algoritması tarafından kullanılan yumuşaklık değerini ayarlar.  
- `setGrayscale(true)` filtreden gri tonlamada çalışmasını söyler; bu genellikle gürültü azaltma için daha temiz sonuçlar verir.

## Adım 4: Filtreyi Uygula ve Kaydet

`filter` yöntemi, yapılandırılmış Gaussian‑Wiener kombinasyonunu tüm görüntü sınırlarına uygular. Son olarak, işlenmiş görüntüyü `GifOptions` kullanarak GIF olarak kaydederiz. `GifOptions` yerine `PngOptions`, `JpegOptions` vb. kullanarak **PNG Java** ya da diğer formatları dışa aktarabilirsiniz.

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## Yaygın Sorunlar ve İpuçları

- **Null RasterImage:** Kaynak dosyanın PSD veya başka bir raster‑uyumlu format olduğundan emin olun.  
- **Performance:** Büyük görüntüler daha uzun sürebilir; yarıçapı azaltmayı veya önce ölçeklenmiş bir kopya işlemeyi düşünün.  
- **Color vs. Grayscale:** Renk korumanız gerekiyorsa, `options.setGrayscale(false)` ayarlayın.

## Sıkça Sorulan Sorular

**S1: Bu filtreleri PSD dışındaki formatlardaki görüntülere uygulayabilir miyim?**  
C1: Evet, Aspose.PSD for Java PSD dışındaki PNG, JPEG, BMP ve GIF gibi çeşitli görüntü formatlarını destekler.

**S2: Aspose.PSD for Java deneme sürümünde herhangi bir kısıtlama var mı?**  
C2: Deneme sürümü çıktı boyutunu sınırlar ve bir filigran ekler. Tam yetenekleri açmak için geçerli bir lisans alın.

**S3: Aspose.PSD for Java için desteği nasıl alabilirim?**  
C3: Topluluk yardımı ve resmi yanıtlar için **[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)** adresini ziyaret edin.

**S4: Test amaçlı geçici bir lisans mevcut mu?**  
C4: Evet, geçici lisansı **[burada](https://purchase.aspose.com/temporary-license/)** alabilirsiniz.

**S5: Aspose.PSD for Java için ayrıntılı belgeleri nerede bulabilirim?**  
C5: Derin API referansları ve ek örnekler için **[belgelendirme](https://reference.aspose.com/psd/java/)** adresine bakın.

## Sonuç

Artık Aspose.PSD for Java kullanarak **Gaussian** ve Wiener filtrelerini **uygulayan** tam bir **java image processing tutorial**'ı tamamladınız. Farklı yarıçap ve yumuşaklık değerleriyle deney yapın, gri tonlamayı açıp kapatın ve PNG gibi diğer çıktı formatlarını deneyerek filtrelerin görüntülerinize etkisini görün. Kodlamanın tadını çıkarın!

---

**Son Güncelleme:** 2026-07-17  
**Test Edilen Versiyon:** Aspose.PSD for Java 23.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose

## İlgili Eğitimler

- [Adım Adım Filtre - Aspose.PSD for Java kullanarak Hareket Wiener Filtrelerini Uygula](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Adım Adım Filtre - Median & Wiener Filtrelerini Uygula (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [Aspose.PSD for Java'da PNG Dosyalarını Nasıl Filtrelersiniz](/psd/java/optimizing-png-files/apply-filters-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}