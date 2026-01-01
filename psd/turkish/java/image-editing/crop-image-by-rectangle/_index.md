---
date: 2026-01-01
description: Aspose.PSD for Java kullanarak Java’da görüntüyü nasıl kırpacağınızı
  keşfedin. PSD dosyasını yüklemek, görüntü dikdörtgenini kırpmak ve PSD’yi JPEG’e
  dönüştürmek için adım adım rehberimizi izleyin.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Görüntüyü Kırp Java: Aspose.PSD ile Dikdörtgen Kullanarak Görüntüyü Kırp'
url: /tr/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Aspose.PSD ile Dikdörtgen Kullanarak Görüntüyü Kırpma

## Giriş

Grafiklerle çalışmak, **java image processing**'in rutin bir parçasıdır ve Aspose.PSD for Java, PSD dosyalarıyla çalışmak için temiz, yüksek performanslı bir API sunar. Bu öğreticide, bir dikdörtgen kullanarak **görüntüyü nasıl kırpacağınızı**, bir PSD dosyasını nasıl yükleyeceğinizi ve sonunda sonucu JPEG'e nasıl dönüştüreceğinizi öğreneceksiniz—tüm bunlar sadece birkaç satır Java kodu ile.

## Hızlı Yanıtlar
- **crop image java** ne anlama geliyor? Java kodu kullanarak bir görüntüyü tanımlı bir dikdörtgene kırpmak anlamına gelir.  
- **Which library handles the operation?** Aspose.PSD for Java gerekli sınıfları sağlar.  
- **Do I need a license for testing?** Ücretsiz deneme mevcuttur; üretim için bir lisans gereklidir.  
- **Can I convert the cropped PSD to JPEG?** Evet—kaydederken `JpegOptions` kullanın.  
- **How long does the implementation take?** Genellikle temel bir senaryo için 10 dakikadan az sürer.

## Java’da bir görüntüyü dikdörtgen ile kırpma nedir?

Bir görüntüyü dikdörtgen ile kırpmak, belirli bir alanı (X, Y, genişlik ve yükseklik ile tanımlanan) seçmek ve bu alanın dışındaki her şeyi atmak anlamına gelir. Bu işlem, daha büyük bir PSD belgesinin belirli bir bölgesine odaklanmanız gerektiğinde yaygındır.

## Bu görev için neden Aspose.PSD kullanılmalı?

- **No external dependencies** – saf Java ile çalışır.  
- **Supports PSD, PNG, JPEG, and many other formats** – **convert PSD to JPEG** işlemini anında yapabilirsiniz.  
- **High‑fidelity rendering** – kırpma sırasında katman bilgilerini ve renk profillerini korur.

## Ön Koşullar

- Java Development Kit (JDK) yüklü.  
- Aspose.PSD for Java kütüphanesi – [website](https://releases.aspose.com/psd/java/) adresinden indirin.

## Paketleri İçe Aktarma

Aspose.PSD for Java yeteneklerinden faydalanmak için Java projenize gerekli paketleri eklediğinizden emin olun. Java dosyanızın başına aşağıdaki import ifadelerini ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Şimdi, Aspose.PSD for Java kullanarak bir dikdörtgen ile görüntüyü kırpma sürecini adım adım açıklayalım.

## Adım 1: Belge Dizinini Ayarlayın

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini PSD dosyanızın bulunduğu gerçek yol ile değiştirin.

## Adım 2: Kaynak ve Hedef Dosyaları Belirleyin

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Kaynak PSD dosyanız ve hedef JPEG dosyanız için yolları tanımlayın.

## Adım 3: Görüntüyü Yükleyin ve Önbelleğe Alın

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Burada **PSD dosyasını** bir `RasterImage` örneğine yüklüyoruz ve performansı artırmak için verilerini önbelleğe alıyoruz.

## Adım 4: Kırpma Dikdörtgenini Oluşturun ve Tanımlayın

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Kırpma için istediğiniz boyutta bir `Rectangle` sınıfı örneği oluşturun. Parametreler sırasıyla **X**, **Y**, **width** ve **height** değerlerini temsil eder.

## Adım 5: Görüntüyü Kırpın ve Kaydedin

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Belirtilen dikdörtgeni kullanarak kırpma işlemini gerçekleştirin ve sonucu `JpegOptions` ile kaydederek **convert PSD to JPEG** işlemini yapın.

Bu adımları ihtiyacınıza göre tekrarlayın, parametreleri özel gereksinimlerinize göre ayarlayın.

## Yaygın Sorunlar ve İpuçları

- **Rectangle outside image bounds** – dikdörtgenin koordinatlarının kaynak görüntünün boyutları içinde olduğundan emin olun.  
- **Memory consumption** – işiniz bittiğinde yerel kaynakları serbest bırakmak için `rasterImage.dispose()` çağırın.  
- **Quality control** – çıkış JPEG'inin sıkıştırma seviyesini kontrol etmek için `JpegOptions.setQuality(int)` ayarlayabilirsiniz.

## Sonuç

Bu öğreticide, Aspose.PSD for Java kullanarak bir dikdörtgen ile **crop image java** sürecini adım adım inceledik. Bu adımları izleyerek, bir PSD dosyasını yükleme, belirli bir bölgeyi kırpma ve sonucu JPEG'e dönüştürme gibi güçlü görüntü işleme yeteneklerini herhangi bir Java uygulamasına kolayca entegre edebilirsiniz.

## SSS

### S1: Aspose.PSD for Java'ı diğer Java çerçeveleriyle kullanabilir miyim?

C1: Evet, Aspose.PSD for Java çeşitli Java çerçeveleriyle entegre edilebilir ve geliştirme projelerinizde esneklik sağlar.

### S2: Aspose.PSD for Java için ücretsiz deneme mevcut mu?

C2: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) erişebilirsiniz.

### S3: Ek destek veya yardım nereden bulabilirim?

C3: Topluluk desteği ve tartışmalar için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

### S4: Aspose.PSD for Java için geçici bir lisans nasıl alabilirim?

C4: Geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

### S5: Aspose.PSD for Java'da kırpma için desteklenen görüntü formatları nelerdir?

C5: Aspose.PSD for Java, PSD, PNG, JPEG ve daha fazlası dahil olmak üzere çeşitli görüntü formatlarını destekler.

---

**Son Güncelleme:** 2026-01-01  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}