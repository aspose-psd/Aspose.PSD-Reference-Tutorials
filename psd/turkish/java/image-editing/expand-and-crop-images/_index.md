---
date: 2026-07-08
description: 'Java image editing library öğreticisi: Aspose.PSD for Java kullanarak
  Java''da görüntüyü crop, resize, expand canvas ve PSD''yi JPEG''e convert etmeyi
  öğrenin.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Expand ve Crop Images
og_description: Java image editing library öğreticisi, Aspose.PSD for Java ile dakikalar
  içinde PSD'yi JPEG'e convert, crop ve expand canvas nasıl yapılacağını gösterir.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java Image Editing Library – Aspose.PSD ile Crop Image
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java Image Editing Library – Aspose.PSD ile Crop Image
url: /tr/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Editing Library: Java ile Görüntü Kırpma Aspose.PSD

## Giriş

Bu öğreticide **java image editing library**—özellikle Aspose.PSD for Java—kullanarak PSD dosyalarını kırpma, genişletme ve JPEG'e dönüştürmeyi öğreneceksiniz. Web portalı için varlıklar hazırlıyor ya da küçük resim oluşturmayı otomatikleştiriyor olun, aşağıdaki adımlar herhangi bir Java 8+ projesine entegre edebileceğiniz tekrarlanabilir, üretim‑hazır bir iş akışı sunar.

## Hızlı Yanıtlar
- **Hangi kütüphane crop image java işlemini yapar?** Aspose.PSD for Java.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme testi için çalışır; üretim için ticari lisans gereklidir.  
- **Kırpma sırasında PSD'yi JPEG'e dönüştürebilir miyim?** Evet, `JpegOptions` ile kırpma dikdörtgeni birlikte kullanarak.  
- **Java 8 destekleniyor mu?** Aspose.PSD, Java 8 ve daha yeni sürümleri destekler.  
- **Uygulama ne kadar sürer?** Temel bir kırpma işlemi için genellikle 10 dakikadan az.

## “crop image java” nedir?

Crop image java, kaynak resmin dikdörtgen bir bölgesini seçmek ve bu bölgenin dışındaki her şeyi atmak anlamına gelir. Aspose.PSD ile, alanı tanımlayan bir `Rectangle` oluşturur, bunu bir `RasterImage`'a uygular ve ardından sonucu JPEG gibi desteklenen herhangi bir formatta kaydedersiniz.

## Java görüntü kırpma için Aspose.PSD neden kullanılmalı?

Aspose.PSD, **java image editing library** sağlayarak PSD dosyalarını yerel olarak işler, 100 den fazla katman özelliğini destekler ve bellek kullanımını 500 MB altında tutarak 10 000 × 10 000 piksel boyutuna kadar görüntü işleyebilir. Ayrıca JPEG, PNG, BMP ve daha fazlasına yerleşik dönüşüm sunar, dış araçlara ihtiyaç duymaz. Bu, toplu‑işlem hatlarını hızlı, güvenilir ve bakımının kolay olmasını sağlar.

## Önkoşullar

1. **Java Development Kit (JDK)** – Java 8 veya daha yeni bir sürüm yüklü.  
2. **Aspose.PSD for Java** – kütüphaneyi resmi siteden **[buradan](https://releases.aspose.com/psd/java/)** indirin.  

> **İpucu:** `ClassNotFoundException` hatasından kaçınmak için Aspose.PSD JAR'ını projenizin sınıf yoluna veya Maven/Gradle bağımlılıklarına ekleyin.

## Paketleri İçe Aktarın

Java kaynak dosyanıza gerekli içe aktarmaları ekleyin. Bu sınıflar, görüntü yükleme, raster manipülasyonu, dikdörtgen tanımlama ve JPEG dışa aktarım seçeneklerine erişim sağlar.

## Aspose.PSD Kullanarak Java'da Görüntü Kırpma Nasıl Yapılır?

`RasterImage` ile kaynak PSD'yi yükleyin, kırpma alanını tanımlayan bir `Rectangle` oluşturun (negatif koordinatlar kanvası genişletebilir) ve son olarak sonucu `JpegOptions` ile kaydedin. Bu üç‑adımlı akış, kırpma ve format dönüşümünü tek bir geçişte gerçekleştirir, ara dosyalara ihtiyaç duymaz.

## Adım 1: Belge Dizininizi Ayarlayın

Kaynak PSD dosyasını içeren klasörü belirtin. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Adım 2: Kaynak ve Hedef Yolları Belirleyin

PSD'yi nereden okuyacağınızı ve kırpılmış JPEG'i nereye yazacağınızı tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## Adım 3: Görüntüyü Yükleyin ve Önbelleğe Alın

`RasterImage`, bir PSD dosyasının bellek içindeki rasterleştirilmiş sürümünü temsil eder.  
PSD'yi bir `RasterImage` nesnesine yükleyin. Önbelleğe alma, kırpma gibi sonraki işlemlerin performansını artırır.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Adım 4: Kırpma İçin Dikdörtgen Oluşturun

`Rectangle`, kırpma bölgesinin X, Y koordinatlarını ve genişlik/yüksekliğini tanımlar.  
Tutmak istediğiniz bölgeyi tanımlayan bir `Rectangle` oluşturun. Koordinatlar, kırpmadan önce kanvası **genişletmek** için negatif olabilir; bu, orijinal görüntünün etrafına kenarlık eklemek için faydalıdır.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Negatif koordinatlar neden kullanılır?**  
> Negatif X/Y değerleri kırpma alanını sola/üste kaydırır, böylece son kırpmadan önce orijinal içeriğin etrafına boş alan (genişleme) eklenir.

## Adım 5: Kırpılmış Görüntüyü Kaydedin

`JpegOptions`, kalite ve sıkıştırma gibi JPEG çıktısı ayarlarını belirler.  
Son olarak, `JpegOptions` kullanarak elde edilen görüntüyü kaydedin. Bu adım aynı zamanda kırpma dikdörtgeni uygulanırken **convert psd jpeg** işlemini de gösterir.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Sonuç:** `jpeg_out.jpg` şimdi her iki taraftan 200 px genişletilmiş ve tanımlı dikdörtgene kırpılmış 300 × 300 piksel bir görüntü içerir.

Tebrikler! **java image cropping** işlemini başarıyla gerçekleştirdiniz, kanvası genişlettiniz ve bir PSD dosyasını JPEG'e dönüştürdünüz—tüm bunlar birkaç özlü kod satırıyla.

## Yaygın Kullanım Durumları

- **Web için varlıkları hazırlama** – yüklemeden önce ekran görüntülerini veya tasarımları kırpın ve yeniden boyutlandırın.  
- **Küçük resim oluşturma** – önizleme amaçlı büyük bir PSD'den belirli bir bölgeyi çıkarın.  
- **Otomatik toplu işleme** – bir klasördeki PSD dosyalarını döngüye alarak her birine aynı kırpma dikdörtgenini uygulayın.

## Sorun Giderme ve İpuçları

| Sorun | Önerilen Çözüm |
|-------|----------------|
| Büyük PSD'ler yüklenirken `OutOfMemoryError` | `rasterImage.cacheData()`'yı erken çağırın ve JVM yığın boyutunu (`-Xmx`) artırmayı düşünün. |
| Kırpılan alan merkezin dışında | Dikdörtgenin X/Y ofsetlerini kontrol edin; negatif değerlerin kanvası genişlettiğini unutmayın. |
| Çıktı JPEG bulanık görünüyor | `JpegOptions` kalite ayarını değiştirin (ör. `new JpegOptions { Quality = 90 }`). |

## Sık Sorulan Sorular

### Q1: Aspose.PSD farklı Java sürümleriyle uyumlu mu?

A1: Evet, Aspose.PSD Java 8, 11, 17 ve daha yeni sürümleri destekler, böylece geliştirme ortamları arasında geniş uyumluluk sağlar.

### Q2: Aspose.PSD'yi ticari projelerde kullanabilir miyim?

A2: Kesinlikle, Aspose.PSD geliştiriciler için ticari lisanslar sunar ve hem kişisel hem de ticari uygulamalarda kullanılabilir.

### Q3: Desteklenen görüntü dosya formatlarıyla ilgili sınırlamalar var mı?

A3: Aspose.PSD 30+ görüntü formatını destekler, PSD, JPEG, PNG, BMP, TIFF ve daha fazlası dahil. Tam liste için [documentation](https://reference.aspose.com/psd/java/) sayfasına bakın.

### Q4: Aspose.PSD ile ilgili sorular için nasıl destek alabilirim?

A4: Topluluk ve Aspose destek ekibinden yardım almak için [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

### Q5: Ücretsiz deneme mevcut mu?

A5: Evet, Aspose.PSD'yi ücretsiz deneme sürümüyle keşfedebilirsiniz. İndirmek için [buradan](https://releases.aspose.com/) erişin.

---

**Last Updated:** 2026-07-08  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## İlgili Öğreticiler

- [Aspose.PSD ile Basit Yeniden Boyutlandırma – Java Görüntü İşleme Kütüphanesi](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java ile Görüntüyü 270 Derece Döndürme](/psd/java/advanced-image-manipulation/rotate-image/)
- [Aspose.PSD ile Java Görüntü İşleminde Gamma Ayarlama](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}