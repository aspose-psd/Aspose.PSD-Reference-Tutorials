---
date: 2026-01-07
description: Aspose.PSD for Java kullanarak Medyan ve Wiener filtrelerini uygulamak
  için adım adım filtre tekniklerini öğrenin ve PSD'yi verimli bir şekilde GIF'e dönüştürün.
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
title: 'Adım Adım Filtre - Medyan ve Wiener Filtrelerini Uygula (Java)'
url: /tr/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adım Adım Filtre: Median ve Wiener Filtrelerini Uygulama (Java)

## Giriş

Eğer Java’da gürültülü görüntüleri temizlemek için bir **adım adım filtre** iş akışı arıyorsanız, doğru yerdesiniz. Aspose.PSD for Java, Median ve Wiener filtrelerini uygulamayı basitleştirir ve işlem sonrası **PSD'yi GIF'e dönüştür** yapmanıza bile izin verir. Bu öğreticide, kütüphaneyi kurmaktan filtrelenmiş sonucu kaydetmeye kadar ihtiyacınız olan her şeyi adım adım göstereceğiz; böylece uygulamalarınıza yüksek kaliteli görüntü gürültü azaltma entegrasyonunu güvenle ekleyebilirsiniz.

## Hızlı Yanıtlar
- **Median filtresi ne yapar?** Tuz ve biber gürültüsünü azaltır ve kenarları korur.  
- **Wiener filtresini ne zaman kullanmalıyım?** Yerel görüntü varyansını dikkate alan uyarlamalı gürültü azaltma için.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme yeterlidir; üretim için ticari lisans gereklidir.  
- **Çıktıyı GIF olarak kaydedebilir miyim?** Evet—Aspose.PSD tek adımda **PSD'yi GIF'e dönüştür** yapmanıza izin verir.  
- **Uygulama ne kadar sürer?** Temel kurulum için genellikle 10 dakikadan az.

## Adım Adım Filtre Nedir?

*Adım adım filtre* yaklaşımı, görüntü işleme sürecini net, yönetilebilir aşamalara böler—görüntüyü yükleme, filtre seçeneklerini yapılandırma, filtreyi uygulama ve sonunda sonucu kaydetme. Bu metodik akış, her bölümü hata ayıklamayı, kodu yeniden kullanmayı ve farklı görüntü formatları için süreci uyarlamayı kolaylaştırır.

## Neden Aspose.PSD for Java Kullanmalı?

- **Geniş format desteği** – PSD, PNG, JPEG, GIF ve daha fazlasını işler.  
- **Harici bağımlılık yok** – Saf Java, herhangi bir projeye kolayca entegre edilebilir.  
- **Yerleşik filtre seçenekleri** – Median, Wiener ve diğer gelişmiş filtreler kutudan çıkar çıkmaz hazır.  
- **Tek tıkla dönüşüm** – İşleme sonrası doğrudan GIF, PNG veya JPEG olarak dışa aktar.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Aspose.PSD for Java Kütüphanesi** – Kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirin ve kurun.  
2. **Java Geliştirme Ortamı** – JDK 8+ ve makinenizde bir IDE veya yapı aracı (Maven/Gradle) kurulu.

## Paketleri İçe Aktarma

Görüntü işleme ve filtre seçeneklerine erişmenizi sağlayacak gerekli sınıfları içe aktararak başlayın.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Adım Adım Filtre: Median Filtre Nasıl Uygulanır

### Adım 1: Görüntüyü Yükle

İlk olarak, temizlemek istediğiniz PSD dosyasına API’yı yönlendirin.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### Adım 2: Görüntüyü RasterImage'ye Dönüştür

Filtre raster veriler üzerinde çalıştığı için, genel `Image` nesnesini bir `RasterImage` nesnesine dönüştürürüz.

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Adım 3: MedianFilterOptions Örneği Oluştur

Median çekirdeğinin boyutunu yapılandırın. **4** boyutu orta seviyedeki gürültü için iyi çalışır.

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Adım 4: Median Filtreyi Uygula

Şimdi filtreyi tüm görüntü sınırlarına uygulayın.

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### Adım 5: Sonuç Görüntüyü Kaydet (PSD'yi GIF'e Dönüştür)

Filtreleme sonrası çıktıyı bir GIF olarak kaydedeceğiz—**PSD'yi GIF'e dönüştür** yeteneğini göstererek.

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

Bu adımları izleyerek bir Median filtresi başarıyla uyguladınız ve temizlenmiş görüntüyü GIF olarak dışa aktardınız.

## Wiener Filtreyi Uygulama (İsteğe Bağlı Uzantı)

Projeniz uyarlamalı gürültü azaltma gerektiriyorsa, Median filtresini Wiener filtresiyle değiştirebilirsiniz. Kod yapısı aynı kalır; sadece `WienerFilterOptions` sınıfını içe aktarmanız ve istediğiniz yarıçapla örneklemeniz yeterlidir.

> **Pro tip:** Her iki filtre için de farklı çekirdek boyutları deneyerek gürültü giderme ile detay koruma arasındaki ideal dengeyi bulun.

## Yaygın Sorunlar ve Çözümleme

| Belirti | Muhtemel Neden | Çözüm |
|---------|----------------|------|
| `RasterImage`'e dönüştürürken `ClassCastException` | Giriş dosyası raster‑uyumlu bir PSD değil | PSD'nin raster katmanlar içerdiğini doğrulayın veya katmanları önce rastera dönüştürün |
| Çıktı GIF boş | Hedef yol hatalı veya klasörün yazma izni yok | `dataDir`'in mevcut ve yazılabilir bir dizine işaret ettiğinden emin olun |
| Filtre etkisiz görünüyor | Çekirdek boyutu gürültü seviyesine göre çok küçük | Filtre boyutunu artırın (ör. `new MedianFilterOptions(6)`) |

## Sıkça Sorulan Sorular

**S1: Bu filtreleri herhangi bir formatta görüntülere uygulayabilir miyim?**  
C1: Evet, Aspose.PSD geniş bir görüntü formatı yelpazesini destekler, bu da onu çeşitli projeler için çok yönlü kılar.

**S2: Aspose.PSD for Java için ücretsiz bir deneme mevcut mu?**  
C2: Evet, ücretsiz bir deneme alabilirsiniz [buradan](https://releases.aspose.com/).

**S3: Aspose.PSD for Java için desteği nasıl alabilirim?**  
C3: Topluluk desteği için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

**S4: Aspose.PSD for Java dokümantasyonunu nerede bulabilirim?**  
C4: Dokümantasyona [buradan](https://reference.aspose.com/psd/java/) göz atın.

**S5: Aspose.PSD for Java nasıl satın alınır?**  
C5: Ürünü [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

## Sonuç

Bu rehberde, Aspose.PSD for Java kullanarak Median (ve isteğe bağlı olarak Wiener) filtrelerini uygulamak için bir **adım adım filtre** sürecini gösterdik ve gürültü azaltma sonrası **PSD'yi GIF'e dönüştür** işlemini sergiledik. Bu temel bileşenlerle, fotoğrafları temizlemek, web için varlıkları hazırlamak veya toplu dönüşümleri otomatikleştirmek isterken, herhangi bir Java uygulamasına sağlam bir görüntü‑işleme hattı entegre edebilirsiniz.

---

**Son Güncelleme:** 2026-01-07  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}