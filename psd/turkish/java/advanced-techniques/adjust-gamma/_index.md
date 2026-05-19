---
date: 2026-02-27
description: Aspose.PSD kullanarak Java görüntü işleme'de gamma ayarlamayı, PSD'yi
  TIFF'e dönüştürmeyi ve soluk görüntüleri düzeltmeyi kısa bir öğreticide öğrenin.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD ile Java Görüntü İşleme'de Gamma Nasıl Ayarlanır
url: /tr/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Görüntü İşleme'de Gamma Nasıl Ayarlanır Aspose.PSD ile

## Giriş

**java image processing** ile çalışıyorsanız, **gamma nasıl ayarlanır** öğrenmek, detay kaybetmeden parlaklık ve kontrastı iyileştiren temel bir tekniktir. Bu öğreticide **Aspose.PSD for Java** kullanarak bir PSD dosyasına gamma düzeltmesi uygulamayı, **PSD'yi TIFF'e dönüştürmeyi** ve **soluk bir görüntü** oluşumunu önlemeyi adım adım göstereceğiz. Bu yaklaşımın hızlı, güvenilir ve sunucu‑tarafı görüntü iş akışları için mükemmel olduğunu göreceksiniz.

## Hızlı Yanıtlar
- **Gamma düzeltmesi ne işe yarar?** Luminans değerlerini yeniden haritalayarak karanlık alanları daha parlak, parlak alanları daha karanlık hâle getirir ve genel detayı korur.  
- **İşlemi hangi kütüphane gerçekleştirir?** Aspose.PSD for Java, raster görüntüler için özel bir `adjustGamma` metodu sağlar.  
- **Aynı akışta PSD'yi TIFF'e dönüştürebilir miyim?** Evet – gamma ayarlamasından sonra görüntüyü doğrudan `TiffOptions` kullanarak TIFF olarak kaydedebilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü çalışır; üretim kullanımı için ticari lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Aspose.PSD, Java 8 ve üzeri sürümleri destekler.

## Java Görüntü İşleme'de Gamma Nasıl Ayarlanır
Gamma ayarlama, parlaklık veya kontrastla ilgili **java image processing tutorial**ların temel bir parçasıdır. Aşağıda adımları ayrıntılı olarak açıklıyor, her satırın neden önemli olduğunu gösteriyor ve süreci mevcut kod tabanınıza nasıl entegre edeceğinizi anlatıyoruz.

## Java Gamma Düzeltmesi Nedir?
Gamma düzeltmesi, kodlanmış piksel değerleri ile ekranda gösterilen parlaklık arasındaki doğrusal olmayan ilişkiyi değiştirir. Gamma eğrisini ayarlayarak **soluk görüntü** sorunlarını düzeltebilir veya gölgelerdeki detayları vurgularken parlak alanları aşırı aydınlatmadan koruyabilirsiniz.

## Gamma Düzeltmesi İçin Neden Aspose.PSD Kullanılmalı?
Aspose.PSD, PSD formatının karmaşıklıklarını soyutlayan güçlü bir **java image processing library**dir. Renk profillerini, önbellekleme işlemlerini yönetir ve basit bir `adjustGamma` çağrısı sunar; bu da **java gamma correction** ve **convert PSD to TIFF** iş akışları için idealdir.

## Önkoşullar

1. **Java Geliştirme Ortamı** – Java 8 veya daha yeni bir sürüm yüklü olmalı.  
2. **Aspose.PSD Kütüphanesi** – JAR dosyasını projenize indirin ve ekleyin. Resmi [documentation](https://reference.aspose.com/psd/java/) sayfasına bakın.  
3. **Örnek Görüntü** – İşlemek istediğiniz bir PSD dosyası (ör. `sample.psd`).  

## Paketleri İçe Aktar

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Adım 1: Görüntüyü Yükle

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

**Pro tip:** Raster verisini bir kez önbelleğe almak, ardışık ayarlamalar yaparken bellek tüketimini azaltır.

## Adım 2: Gamma'yı Ayarla

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Kırmızı, yeşil ve mavi kanallar için farklı değerler geçirerek kanal‑özgü ayarlamalar yapabilirsiniz.

## Adım 3: TiffOptions Oluştur

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

8‑bit örnek (`{8,8,8}`) ayarlamak, TIFF dosya boyutunu makul tutarken renk doğruluğunu korur.

## Adım 4: Sonuç Görüntüyü Kaydet

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Kaydettikten sonra TIFF'i baskı hizmetleri veya web API'leri gibi sonraki sistemlere besleyebilirsiniz.

## Yaygın Kullanım Senaryoları

- **Otomatik grafik iş akışları** – Küçük resimler oluşturulmadan önce gamma'yı anında ayarlayın.  
- **Toplu dönüşüm araçları** – Parlaklığı normalleştirirken büyük PSD arşivlerini TIFF'e dönüştürün.  
- **Web servisleri** – PSD alan, gamma düzeltmesi uygulayan ve istemciye TIFF döndüren bir uç nokta sunun.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Neden Oluşur | Nasıl Çözülür |
|-------|--------------|---------------|
| **Görüntü soluk görünüyor** | Gamma değeri çok yüksek (ör. > 2.5) | Gamma faktörünü 1.8 ile 2.2 arasında bir değere düşürün. |
| **`rasterImage.isCached()` false döndürüyor** | Görüntü henüz belleğe yüklenmemiş | Gamma ayarlamadan önce `rasterImage.cacheData()` metodunu çağırın. |
| **TIFF dosya boyutu büyük** | Örnek başına bit sayısı 16‑bit olarak ayarlanmış | Örnekte gösterildiği gibi 8‑bit örnek (`{8,8,8}`) kullanın. |

## Sıkça Sorulan Sorular

**S: Her renk kanalı için farklı gamma değerleri uygulayabilir miyim?**  
C: Evet – `adjustGamma` metodu, kırmızı, yeşil ve mavi kanallar için ayrı float değerleri kabul eder.

**S: Kaydetmeden önce birden fazla görüntü ayarlamasını zincirleme yapabilir miyim?**  
C: Kesinlikle. Aynı `RasterImage` örneği üzerinde yeniden boyutlandırma, kırpma veya renk düzeltmeleri gibi işlemleri sıralı olarak gerçekleştirebilirsiniz.

**S: Aspose.PSD çok sayfalı PSD dosyalarını destekliyor mu?**  
C: Evet, her katmana ayrı ayrı erişebilir ve işleyebilirsiniz.

**S: TIFF dışındaki hangi formatlara dışa aktarabilirim?**  
C: Aspose.PSD, PNG, JPEG, BMP ve ilgili seçenek sınıfları aracılığıyla birçok diğer formatı destekler.

**S: Gamma düzeltmesinden sonra soluk bir görüntüyü nasıl önleyebilirim?**  
C: Orta seviyede bir gamma (yaklaşık 2.0) ile başlayın ve sonucu önizleyin; görüntü çok parlak görünürse gamma değerini azaltın.

## Sonuç

Tebrikler! **java image processing** iş akışında **gamma nasıl ayarlanır** konusunu başarıyla öğrendiniz, bir PSD'yi TIFF'e dönüştürdünüz ve **soluk bir görüntü** gibi yaygın sorunları önlediniz. Bu desen, parlaklık ve kontrast üzerinde ince ayar yapmanızı sağlar; otomatik grafik iş akışları, web servisleri veya masaüstü yardımcı programları için idealdir.

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}