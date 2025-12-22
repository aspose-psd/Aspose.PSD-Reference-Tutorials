---
date: 2025-12-21
description: Aspose.PSD ile görüntü gammasını ayarlayarak Java görüntü işleme nasıl
  yapılır öğrenin. PSD'yi TIFF'e dönüştürmek ve gama düzeltmesi uygulamak için adım
  adım rehber.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java Görüntü İşleme – Aspose.PSD ile Gamma Ayarlama
url: /tr/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Görüntü İşleme – Aspose.PSD ile Gamma Ayarlama

## Giriş

**java image processing** ile çalışıyorsanız, bir resmin gammasını ayarlamak, ayrıntıyı kaybetmeden parlaklık ve kontrastı iyileştirmenin temel bir tekniğidir. Bu öğreticide **Aspose.PSD for Java** kullanarak bir PSD dosyasına gamma düzeltmesi uygulamayı ve ardından sonucu TIFF görüntüsü olarak dışa aktarmayı adım adım göstereceğiz. Bu yaklaşımın neden hızlı, güvenilir ve sunucu‑tarafı görüntü iş akışları için mükemmel olduğunu göreceksiniz.

## Hızlı Yanıtlar
- **Gamma düzeltmesi ne yapar?** Parlaklık değerlerini yeniden eşler; karanlık bölgeleri daha aydınlık, parlak bölgeleri ise daha karanlık yapar ve genel ayrıntıyı korur.  
- **İşlemi hangi kütüphane gerçekleştirir?** Aspose.PSD for Java, raster görüntüler için özel bir `adjustGamma` yöntemi sunar.  
- **Aynı akışta PSD’yi TIFF’e dönüştürebilir miyim?** Evet – gamma ayarlamasından sonra görüntüyü doğrudan `TiffOptions` kullanarak TIFF olarak kaydedebilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim kullanımı için ticari lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Aspose.PSD, Java 8 ve üzeri sürümleri destekler.

## Java görüntü işleme nedir?

Java görüntü işleme, Java kütüphanelerini kullanarak görsel verilerin manipülasyonu, analizi ve dönüşümünü ifade eder. İşler arasında yeniden boyutlandırma, filtreleme, renk düzeltmesi ve format dönüşümü bulunur – tümü masaüstü veya web uygulamalarında otomatikleştirilebilir.

## Gamma düzeltmesi için Aspose.PSD neden tercih edilmeli?

Aspose.PSD, PSD formatının karmaşıklığını soyutlayan yüksek seviyeli bir API sunar, böylece gerçek görüntü ayarlamalarına odaklanabilirsiniz. Önbellekleme, renk profilleri yönetimi ve basit bir `adjustGamma` çağrısı sağlar; bu da **image gamma correction** ve **convert psd to tiff** iş akışları için idealdir.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdaki önkoşulları yerine getirdiğinizden emin olun:

1. **Java Geliştirme Ortamı** – Sisteminizde bir Java geliştirme ortamı kurulu olmalı.  
2. **Aspose.PSD Kütüphanesi** – Aspose.PSD kütüphanesini indirin ve Java projenize entegre edin. Gerekli kaynakları [documentation](https://reference.aspose.com/psd/java/) adresinde bulabilirsiniz.  
3. **Örnek Görüntü** – Gamma ayarlaması uygulayacağınız bir PSD örnek görüntüsü hazırlayın.

## Paketleri İçe Aktarma

İşleme başlamak için Java projenizde gerekli paketleri içe aktarın. Bu, Aspose.PSD işlevlerini sorunsuz bir şekilde kullanmanızı sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Adım 1: Görüntüyü Yükleme

Örnek PSD görüntüsünü `RasterImage` sınıfının bir örneğine yükleyerek başlayın. Bu, sonraki gamma ayarlamaları için temel oluşturur.

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

## Adım 2: Gamma’yı Ayarlama

Yüklenen görüntünün gammasını `adjustGamma` yöntemiyle ayarlayın. Gamma değerlerini ihtiyacınıza göre ince ayar yapın.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Adım 3: TiffOptions Oluşturma

Sonuç görüntüsü için bir `TiffOptions` örneği oluşturun. Örnek başına bit sayısı ve fotometrik seçenekler gibi çeşitli özellikleri, çıktıyı gereksinimlerinize göre özelleştirmek için ayarlayın.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Adım 4: Sonuç Görüntüyü Kaydetme

Önceden tanımlanan `TiffOptions` kullanarak manipüle edilmiş görüntüyü TIFF formatında kaydedin.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|-------|
| **Görüntü soluk çıkıyor** | Gamma değeri çok yüksek (ör. > 2.5) | Gamma faktörünü 1.8 ile 2.2 arasında bir değere düşürün. |
| **`rasterImage.isCached()` false döndürüyor** | Görüntü henüz belleğe yüklenmemiş | Gamma ayarlamadan önce `rasterImage.cacheData()` çağırın. |
| **TIFF dosya boyutu büyük** | Örnek başına bit 16‑bit olarak ayarlanmış | Örnekte gösterildiği gibi 8‑bit örnek (`{8,8,8}`) kullanın. |

## Sık Sorulan Sorular

**S: Her renk kanalı için farklı gamma değerleri uygulayabilir miyim?**  
C: Evet – `adjustGamma` yöntemi kırmızı, yeşil ve mavi kanallar için ayrı float değerleri kabul eder.

**S: Kaydetmeden önce birden fazla görüntü ayarlamasını zincirleme yapabilir miyim?**  
C: Kesinlikle. Aynı `RasterImage` örneği üzerinde yeniden boyutlandırma, kırpma veya renk düzeltmeleri gibi işlemleri sıralı olarak gerçekleştirebilirsiniz.

**S: Aspose.PSD çok‑sayfalı PSD dosyalarını destekliyor mu?**  
C: Evet, her katmana ayrı ayrı erişebilir ve işleyebilirsiniz.

**S: TIFF dışındaki hangi formatlara dışa aktarabilirim?**  
C: Aspose.PSD, ilgili seçenek sınıfları aracılığıyla PNG, JPEG, BMP ve birçok başka formatı destekler.

## Sonuç

Tebrikler! Aspose.PSD for Java kullanarak bir PSD dosyasının gammasını ayarlayıp sonucu TIFF görüntüsü olarak dışa aktararak **java image processing** işlemini başarıyla tamamladınız. Bu iş akışı, görüntü parlaklığı ve kontrastı üzerinde ince ayar kontrolü sağlar; otomatik grafik hatları, web servisleri veya masaüstü yardımcı programları için idealdir.

---

**Son Güncelleme:** 2025-12-21  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## SSS

### S1: Aspose.PSD dokümantasyonunu nerede bulabilirim?

C1: Dokümantasyona [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/) adresinden ulaşabilirsiniz.

### S2: Aspose.PSD for Java’yı nasıl indirebilirim?

C2: Kütüphaneyi [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/) adresinden indirebilirsiniz.

### S3: Aspose.PSD’yi nereden satın alabilirim?

C3: Aspose.PSD’yi satın almak için [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) adresini ziyaret edin.

### S4: Ücretsiz deneme sürümü mevcut mu?

C4: Evet, ücretsiz deneme sürümünü [https://releases.aspose.com/](https://releases.aspose.com/) adresinde keşfedebilirsiniz.

### S5: Aspose.PSD için destek alabileceğim yer neresi?

C5: Destek için Aspose.PSD forumuna [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34) adresinden ulaşabilirsiniz.

---