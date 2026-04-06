---
date: 2026-01-07
description: Aspose.PSD for Java kullanarak Java’da nasıl resim kırpılacağını öğrenin.
  Resim kırpma, yeniden boyutlandırma ve PSD’den JPEG’e dönüştürme için adım adım
  rehber.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Görüntü Kırpma Java - Aspose.PSD for Java ile Görüntüleri Genişlet ve Kırp'
url: /tr/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Aspose.PSD for Java ile Görüntüleri Genişletin ve Kırpın

## Giriiş

Bu öğreticide, Aspose.PSD kütüphanesini kullanarak **crop image java**'yı nasıl keşfedeceksiniz. Kanvası genişletmeniz, istenmeyen bölümleriniz veya bir PSD dosyasını JPEG'e aktarmanız, aşağıdaki adımları temiz ve tekrarlanabilir bir süreç sunar. Gereksinimler, ithalat ifadeleri ve kod adımını net açıklamalarla elde edebileceğinizz, böylece teknolojinin gerçek dünya projelerinde uygulayabilirsiniz.

## Hızlı Yanıtlar
- **Görüntü kırpma java'sını hangi kütüphane yönetiyor?** Aspose.PSD for Java.
- **Geliştirme için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü testi amaçlanıyor; üretim için ticari lisans gereklidir.
- **Kırpma sırasında PSD'yi JPEG'e dönüştürebilir miyim?** Evet, yapabileceğin dosyalarıyla birlikte `JpegOptions` kullanarak yapabilirsiniz.
- **Java 8 destekleniyor mu?** Aspose.PSD, Java 8 ve daha yeni bir şekilde kullanılabilir.
- **Uygulama ne kadar sürer?** Temel bir kalıcı işlem genellikle 10dakikadan az sürer.

## "Resim kırpma javası" nedir?

Java’da bir arada kalmak, kaynak resminin bir bölgesini seçmek ve geri kalanını dağıtmak anlamına gelir. Aspose.PSD ile bu ayrıştırılabilir bir `Dikdörtgen` nesnesiyle tanımlayabilir, ardından sonucu JPEG gibi farklı bir formatta kaydedebilirsiniz.

## Java resim kırpma için neden Aspose.PSD kullanmalısınız?

- **Tam PSD desteği** – dağıtılmış PSD dosyalarıyla doğrudan kesilmesi, önce dönüştürülmesine gerek kalmaz.
- **Yüksek performanslı raster işleme** – büyük görüntüler için verimli bellek kullanımı.
- **Yerleşik dönüştürme** – yapılabilir veya kanvas genişletme sırasında JPEG, PNG, BMP vb. formatlara kolayca aktarılır.
- **Çapraz platform** – Java'yı çalıştırabilen herhangi bir sistem çalışır.

## Önkoşullar

Başlamadan önce paketin yüklü olduğundan emin olun:

1. **Java Development Kit (JDK)** – Java8 veya daha yeni bir sürüm yüklü.
2. **Aspose.PSD for Java** – resmi siteden kütüphaneyi **[buradan](https://releases.aspose.com/psd/java/)** indir.

> **Profesyonel ipucu:** Aspose.PSD JAR kopyalarının projenizin classpath'ine veya Maven/Gradle bağımlılıklarına eklenmesini sağlar, böylece `ClassNotFoundException` hatalarından kaçınırsınız.

## Paketleri İçe Aktar

Java dosya kaynağınıza gerekli ithalatları ekleyin. Bu sınıflar, görüntü yükleme, raster ayrıntıları, kayıtlı tanımlama ve JPEG seçenekleri seçeneklerine erişim sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Adım 1: Belge Dizininizi Ayarlayın

Kaynak PSD dosyasının bulunduğu klasörü belirtin. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Kaynak ve Hedef Yolları Belirtin

PSD'yi okuyacağınız ve kırpılmış JPEG'i yazacağınız yolları tanımlayın.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Adım 3: Görüntüyü Yükleyin ve Önbelleğe Alın

PSD'yi bir `RasterImage` nesnesine yükleyin. Önbelleğe alma, kırpma gibi sonraki işlemlerin performansını artırır.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Adım 4: Kırpma İçin Dikdörtgen Oluşturun

Tutmak istediğiniz bölgeyi tanımlayan bir `Rectangle` oluşturun. Koordinatlar negatif olabilir; bu, kırpmadan önce kanvası **genişletmek** için kullanışlıdır ve orijinal görüntünün etrafına kenar eklemenizi sağlar.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Why use negative coordinates?**  
> Negatif X/Y değerleri kırpma alanını sola/yukarı kaydırır, böylece son kırpmadan önce orijinal içeriğin etrafına boş alan (genişletme) eklenir.

## Adım 5: Kırpılmış Görüntüyü Kaydedin

Son olarak, `JpegOptions` kullanarak elde edilen görüntüyü kaydedin. Bu adım, kırpma dikdörtgeni uygulanırken **convert psd jpeg** işlemini de gösterir.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Sonuç:** `jpeg_out.jpg` artık her iki bölgede 200 piksel seçeneği ve tanımlı bölmeler kırpılmış 300×300 piksel bir görüntü içerir.

Tebrikler! **java image kırpma** işlemini başarıyla gerçekleştirdiniz, kanvasını genişlettiniz ve bir PSD bölümünü birkaç satır kodla JPEG'e dönüştürdünüz.

## Yaygın Kullanım Durumları

- **Varlıkları web için hazırlama** – web için varlıkları hazırlarken ekran görüntülerini veya tasarımları kırpıp yeniden boyutlandırmanın.
- **Küçük resimler oluşturuluyor** – büyük bir PSD'den ön izleme amaçlı belirli bir hareketlilik çıkararak küçük resimler birleştirilir.
- **Otomatik toplu işleme** – bir dizüstü bilgisayardaki PSD devresini değiştirerek aynı değiştirme yerinin birini değiştirmesini sağlar.

## Sorun Giderme ve İpuçları

| Sayı | Önerilen Düzeltme |
|----------|----------------|
| Büyük PSD'ler yüklenirken `OutOfMemoryError` | `rasterImage.cacheData()` yöntemini erken çağırmanın ve JVM yığın değişiminin (`-Xmx`) iyileştirilmesini düşünün. |
| Kırpılan alan merkezin dışında | Dikdörtgenin X/Y ofsetlerini kontrol edin; Negatif değerlerin kanvasını genişlettiğinizi unutmayın. |
| Çıktı JPEG bulanık görünüyor | `JpegOptions` kalite ayarını yapıldı (ör. `new JpegOptions { Quality = 90 }`). |

## Sıkça Sorulan Sorular

### S1: Aspose.PSD farklı Java sürümleriyle uyumlu mu?

C1: Evet, Aspose.PSD çeşitli Java sürümleriyle uyumludur ve geniş bir geliştirme ortamında çalışabilir.

### S2: Aspose.PSD'yi ticari projeler için kullanabilir miyim?

A2: elbette, Aspose.PSD ticari lisanslar sunar; Böylece hem kişisel hem de ticari projelerde kullanılabilir.

### S3: Desteklenen resim dosyası formatlarında herhangi bir sınırlama var mı?

C3: Aspose.PSD, PSD, JPEG, PNG ve daha fazlası dahil olmak üzere çeşitli görüntü dosyası formatlarını kullanılabilir. Tam liste için [belgeler](https://reference.aspose.com/psd/java/) sayfasına bakın.

### S4: Aspose.PSD ile ilgili sorgular için nasıl destek alabilirim?

Cevap4: [Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) üzerinden bölümden veya Aspose destek ekibinden yardım alabilirsiniz.

### S5: Ücretsiz deneme mevcut mu?

Cevap5: Evet, ücretsiz bir deneme sürümü mevcuttur. **[Buradan](https://releases.aspose.com/)** indirebilirsiniz.

---

**Son Güncelleme:** 2026-01-07
**Test Edildiği Sürüm:** Aspose.PSD for Java 24.12
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}