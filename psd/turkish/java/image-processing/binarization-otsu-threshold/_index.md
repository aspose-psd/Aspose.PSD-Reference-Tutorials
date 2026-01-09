---
date: 2026-01-09
description: Aspose.PSD for Java kullanarak görüntü segmentasyonu Otsu'nun nasıl yapılacağını
  öğrenin. Bu öğreticide Java görüntü işleme, nasıl ikilileştirileceği ve Otsu eşiğinin
  nasıl uygulanacağı ele alınmaktadır.
linktitle: Binarization with Otsu Threshold
second_title: Aspose.PSD Java API
title: Görüntü Segmentasyonu Otsu – Aspose.PSD for Java'da Otsu Eşiği ile İkilileştirme
url: /tr/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Otsu Eşiği Kullanarak İkilileştirme

## Giriş

Hoş geldiniz! Bu adım adım kılavuzda Aspose.PSD for Java kütüphanesini kullanarak **image segmentation otsu** öğreneceksiniz. Fotoğraf düzenleme aracı, otomatik belge analiz hattı ya da herhangi bir **java image processing** projesi geliştiriyor olun, Otsu eşiğiyle görüntüleri ikilileştirmeyi öğrenmek, temiz bir **binary image conversion** oluşturmanın güvenilir bir yolunu sağlayacaktır. Ortamı kurmaktan son JPEG'i kaydetmeye kadar tüm süreci birlikte inceleyelim; böylece Otsu'yu kendi uygulamalarınızda kullanabilirsiniz.

## Hızlı Yanıtlar
- **Otsu eşiği ne yapar?** Ön plan ve arka plan piksellerini ayıran optimal gri seviye kesimini otomatik olarak bulur.  
- **Java'da hangi kütüphane bunu destekler?** Aspose.PSD for Java, yerleşik `binarizeOtsu()` metodunu sağlar.  
- **Denemek için lisansa ihtiyacım var mı?** Ücretsiz deneme mevcuttur; üretim kullanımı için lisans gereklidir.  
- **Hangi çıktı formatını kullanabilirim?** Örnek bir JPEG kaydeder, ancak `RasterCachedImage.save()` tarafından desteklenen herhangi bir format çalışır.  
- **Uygulama ne kadar sürer?** Hazır API sayesinde 10 dakikadan kısa bir sürede çalışan bir çözüm elde edebilirsiniz.

## Image Segmentation Otsu Nedir?

**Image segmentation otsu**, gri tonlamalı bir görüntüyü ikili görüntüye dönüştürmek için optimal eşik değerini belirleyen istatistiksel bir tekniktir. Yöntem, ön plan ve arka planın sınıf içi varyansını değerlendirir ve bu varyansı en aza indiren eşiği seçer; bu da nesnelerin arka plandan net bir şekilde ayrılmasını sağlar.

## Neden Aspose.PSD for Java Kullanmalı?

- **Yüksek performanslı önbellekleme** – büyük PSD dosyalarıyla verimli çalışır.  
- **Tek satır ikilileştirme** – `binarizeOtsu()` ağır işi halleder.  
- **Çapraz format desteği** – PSD'yi yükleyin, işleyin ve JPEG, PNG vb. olarak kaydedin.  
- **Kurumsal lisanslama** – ticari uygulamalar için uygundur.

## Ön Koşullar

Kodun içine dalmadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha üstü yüklü.  
- **Aspose.PSD for Java Kütüphanesi** – Resmi siteden indirin [buradan](https://releases.aspose.com/psd/java/).  
- **Örnek PSD Dosyası** – İkilileştirmek istediğiniz bir PSD (ör. `sample.psd`).  

## Paketleri İçe Aktarma

Gerekli sınıfları içe aktararak başlayın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Adım 1: Belge Dizinini Ayarlama

Kaynak PSD'nizin bulunduğu ve çıktının yazılacağı klasörü tanımlayın:

```java
String dataDir = "Your Document Directory";
```

## Adım 2: PSD Dosyasını Yükleme

PSD'yi bir `Image` nesnesine yükleyin, böylece onunla çalışabilirsiniz:

```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Adım 3: Görüntüyü Önbellekleme

Görüntü hâlâ önbelleğe alınmamışsa, işleme hızını artırmak için önbelleğe alın:

```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

## Adım 4: Görüntüyü Otsu Eşiğiyle İkilileştirme

Otsu algoritmasını uygulayın—bu, **how to apply otsu** için **binary image conversion**'ın çekirdeğidir:

```java
rasterCachedImage.binarizeOtsu();
```

## Adım 5: Sonuç Görüntüyü Kaydetme

Son olarak, ikilileştirilmiş görüntüyü `JpegOptions` kullanarak diske yazın (PNG veya BMP de kullanabilirsiniz):

```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **`ClassCastException`** | Raster olmayan bir görüntüyü dönüştürmeye çalıştı | PSD'nin raster katmanlar içerdiğinden emin olun veya dönüştürmeden önce `image.convertToRasterImage()` kullanın. |
| **Out‑of‑Memory** | Büyük PSD dosyaları çok fazla RAM tüketir | `rasterCachedImage.cacheData()` metodunu erken çağırın ve JVM yığın boyutunu (`-Xmx`) artırmayı düşünün. |
| **Incorrect output colors** | Görüntü düzgün şekilde önbelleğe alınmamış | `binarizeOtsu()` çağırmadan önce `isCached()` metodunun `true` döndürdüğünü doğrulayın. |

## Sıkça Sorulan Sorular

### Q1: Otsu Eşiğiyle İkilileştirme nedir?

A1: Otsu Eşiğiyle İkilileştirme, görüntü segmentasyonu için kullanılan bir yöntemdir; optimal eşikleme temelinde bir görüntüyü ön plan ve arka plan olarak ayırır.

### Q2: Aspose.PSD for Java'yı ücretsiz kullanabilir miyim?

A2: Aspose.PSD for Java ticari bir kütüphanedir, ancak ücretsiz deneme sürümüyle özelliklerini keşfedebilirsiniz. [buradan](https://releases.aspose.com/) edinin.

### Q3: Aspose.PSD for Java dokümantasyonunu nerede bulabilirim?

A3: Dokümantasyon [burada](https://reference.aspose.com/psd/java/) mevcuttur.

### Q4: Aspose.PSD for Java için destek nasıl alabilirim?

A4: Topluluk desteği için Aspose.PSD forumunu [buradan](https://forum.aspose.com/c/psd/34) ziyaret edin.

### Q5: Aspose.PSD for Java için geçici bir lisans mevcut mu?

A5: Evet, geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**Ekstra Soru & Cevap**

**S: Bu yöntem daha büyük bir java image processing iş akışına nasıl uyum sağlar?**  
C: İkilileştirmeden sonra ikili görüntüyü kontur tespiti, OCR ön işleme veya şekil analizi modüllerine besleyebilirsiniz.

**S: Otsu algoritması parametrelerini ayarlayabilir miyim?**  
C: `binarizeOtsu()` metodu standart Otsu uygulamasını kullanır; özel eşikler için `binarize(int threshold)` metodunu kullanın.

## Sonuç

Artık Aspose.PSD for Java kullanarak **image segmentation otsu** nasıl yapılacağını gördünüz. Ortamı kurma, PSD'yi yükleme ve önbellekleme, `binarizeOtsu()` uygulama ve sonucu kaydetme adımlarını izleyerek, herhangi bir **java image processing** projesine sağlam bir ikili görüntü dönüşümünü entegre edebilirsiniz. Farklı kaynak dosyalarla deney yapın, çıktıyı OCR ile birleştirin veya birden fazla PSD'yi otomatik olarak işlemek için toplu bir işlemci oluşturun.

---

**Son Güncelleme:** 2026-01-09  
**Test Edilen:** Aspose.PSD for Java 24.11 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}