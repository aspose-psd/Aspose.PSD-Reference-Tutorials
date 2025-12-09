---
date: 2025-12-08
description: Aspose.PSD kullanarak Java’da belirli bir açıyla resmi nasıl döndüreceğinizi
  öğrenin. Kılavuz, Java’da resmi döndürme, belirli bir açıyla resmi döndürme, arka
  plan işleme ve daha fazlasını kapsar.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Görüntüyü Belirli Bir Açıda Döndürme
url: /tr/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Belirli Bir Açıda Görüntüyü Döndürme: Aspose.PSD for Java ile

## Giriş

Java uygulamasında programlı olarak **görseli nasıl döndürürüm** ihtiyacınız varsa, Aspose.PSD for Java, ağır işleri halleden temiz ve yüksek performanslı bir API sunar. Bir fotoğraf editörü oluşturuyor, küçük resimler üretiyor ya da bir web servisi için varlıklar hazırlıyor olun, bir görüntüyü tam bir dereceyle döndürmek yaygın bir gereksinimdir. Bu öğreticide, PSD dosyasını yüklemekten döndürülmüş sonucu kaydetmeye kadar tüm süreci adım adım inceleyecek ve önbellekleme ve arka plan yönetimi gibi en iyi uygulamaları vurgulayacağız.

> **Hızlı Yanıtlar**  
> - **Java'da görüntü döndürmek için en iyi kütüphane hangisidir?** Aspose.PSD for Java.  
> - **Herhangi bir dereceyle döndürebilir miyim?** Evet, `rotate` yöntemi bir `float` açı (pozitif ya da negatif) kabul eder.  
> - **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim için lisans gereklidir.  
> - **Hangi görüntü formatları destekleniyor?** PSD, JPEG, PNG, TIFF, GIF, BMP ve daha birçokları.  
> - **Boş alan için arka plan rengi nasıl ayarlanır?** `rotate` yöntemine bir `Color` örneği geçirin.

## Java'da Görüntü Döndürme Nedir?

Görüntü döndürme, piksel matrisini bir pivot noktasının (genellikle merkez) etrafında belirli bir açıyla çevirmektir. Java’da bunu `Graphics2D` ile manuel olarak yapabilirsiniz, ancak Aspose.PSD matematiği soyutlar, farklı renk derinliklerini yönetir ve PSD dosyalarıyla çalışırken katman bilgilerini korur.

## Neden Aspose.PSD'yi Görüntü Döndürmek İçin Kullanmalısınız?

- **Hassasiyet:** Kalite kaybı olmadan herhangi bir kesirli dereceyle döndürün.  
- **Performans:** Yerleşik önbellekleme (`image.cacheData()`) büyük dosyaları hızlandırır.  
- **Arka Plan Kontrolü:** Döndürme sırasında oluşan boşlukları doldurmak için bir arka plan rengi belirleyin.  
- **Format Esnekliği:** PSD yükleyin, JPEG, PNG veya desteklenen herhangi bir formatta çıktı alın.

## Önkoşullar

Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

1. **Java Development Kit (JDK 8 veya üzeri)** – çalışan bir Java IDE’si ya da komut satırı ortamı.  
2. **Aspose.PSD for Java** – en yeni JAR dosyasını [Aspose.PSD Java sayfasından](https://reference.aspose.com/psd/java/) indirin.  
3. **Örnek PSD dosyası** – örneğin, kodunuzdan erişebileceğiniz bir klasörde `sample.psd` dosyası.

## Paketleri İçe Aktarma

İhtiyacımız olan sınıfları içe aktaralım. Bu importlar, seçtiğiniz döndürme açısına bakılmaksızın aynı kalır.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Adım Adım Kılavuz

### Adım 1: Belge Dizinini Tanımlayın

Kaynak PSD’nin bulunduğu ve çıktının yazılacağı klasörü ayarlayın.

```java
String dataDir = "Your Document Directory";
```

> **İpucu:** Göreli yol sürprizlerinden kaçınmak için mutlak yol ya da `System.getProperty("user.dir")` kullanın.

### Adım 2: Kaynak ve Hedef Dosya Yollarını Belirleyin

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

İhtiyacınıza göre `destName` değerini `.png`, `.tiff` vb. desteklenen herhangi bir uzantıya değiştirebilirsiniz.

### Adım 3: Görüntüyü Yükleyin

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` dosya formatını otomatik olarak algılar ve raster‑tabanlı işlemler için somut bir `RasterImage` döndürür.

### Adım 4: Görüntü Verilerini Önbellekle (İsteğe Bağlı ama Önerilir)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Önbellekleme, görüntü piksellerini bellekte tutar ve sonraki dönüşümler için hızı artırır—özellikle büyük PSD dosyalarında faydalıdır.

### Adım 5: Görüntüyü Döndürün

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – derece cinsinden döndürme açısı (float). Bu değeri istediğiniz açıya değiştirin, örn. saat yönünün tersine `-45f`.  
- **true** – döndürülmüş görüntüyü sığdırmak için tuvali genişletirken orijinal en‑boy oranını korur.  
- **Color.getRed()** – döndürme sırasında oluşan boş köşeleri dolduran arka plan rengi. İhtiyaca göre `Color.getWhite()` ya da özel bir renk ile değiştirin.

### Adım 6: Sonucu Kaydedin

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` kalite, sıkıştırma ve diğer JPEG‑özel ayarları kontrol etmenizi sağlar. Kayıpsız çıktı için `PngOptions` ile değiştirin.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|------|
| **Döndürme sonrası boş köşeler** | Arka plan rengi belirtilmemiş | `rotate` metoduna bir `Color` (örn. `Color.getWhite()`) geçirin. |
| **Büyük PSD’lerde bellek hatası** | Görüntü önbelleğe alınmamış | İşleme başlamadan `image.cacheData()` çağırın. |
| **Açı yönü hatalı** | Pozitif ve negatif açı karışıklığı | Saat yönünün tersine döndürmek için negatif değer kullanın (veya koordinat sisteminize göre tersine). |
| **Değişiklikler kaydedilmiyor** | `save` çağrısı unutulmuş | Döndürmeden sonra `image.save(...)` metodunun çalıştığından emin olun. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java ile şeffaflık içeren görüntüleri döndürebilir miyim?**  
C: Evet. Kütüphane alfa kanallarını korur; şeffaf köşeler istiyorsanız opak bir arka plan rengi belirtmeyin.

**S: Döndürme için desteklenen görüntü dosya formatlarıyla ilgili bir sınırlama var mı?**  
C: Hayır. Aspose.PSD PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF ve daha birçok formatı destekler.

**S: Görüntüleri negatif bir açıyla döndürebilir miyim?**  
C: Kesinlikle. Saat yönünde döndürmek için negatif bir float değeri (`-30f` gibi) `rotate` metoduna geçirin.

**S: Aspose.PSD döndürme sırasında gerçek zamanlı ön izleme sağlar mı?**  
C: API yalnızca sunucu tarafıdır. Canlı ön izleme için döndürülmüş bitmap’i bir UI çerçevesine (Swing, JavaFX) entegre edip görünümü yenileyin.

**S: Aspose.PSD için topluluk forumu var mı?**  
C: Evet, sorularınızı sorabilir ve deneyimlerinizi paylaşabilirsiniz: [Aspose.PSD forumu](https://forum.aspose.com/c/psd/34).

## Sonuç

Artık Aspose.PSD for Java kullanarak belirli bir açıyla **görseli nasıl döndürürüm** sorusunun yanıtını biliyorsunuz. Önbellekleme, arka plan rengi kontrolü ve esnek çıktı seçeneklerinden yararlanarak herhangi bir Java‑tabanlı görüntü iş akışına hassas döndürme işlevi entegre edebilirsiniz.

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}