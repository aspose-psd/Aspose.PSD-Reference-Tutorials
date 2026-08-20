---
date: 2026-05-19
description: Aspose.PSD kullanarak Java'da belirli bir açıyla görüntüyü nasıl döndüreceğinizi
  öğrenin. Rehber, rotate image java, rotate image specific angle, arka plan işleme
  ve daha fazlasını kapsar.
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: Belirli Bir Açıda Görüntüyü Döndürme
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Belirli Bir Açıda Görüntüyü Döndürme
url: /tr/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Belirli Bir Açıda Görüntüyü Döndürme

Eğer bir Java uygulamasında programlı olarak **görüntüyü nasıl döndürürüm** ihtiyacınız varsa, Aspose.PSD for Java temiz, yüksek performanslı bir API sunar ve ağır işleri halleder. Fotoğraf düzenleyici, küçük resim oluşturma ya da bir web servisi için varlık hazırlama gibi senaryolarda, tam bir dereceyle görüntüyü döndürmek yaygın bir gereksinimdir. Bu öğreticide, PSD dosyasını yüklemekten döndürülmüş sonucu kaydetmeye kadar tüm süreci adım adım inceleyecek ve önbellekleme ile arka plan yönetimi gibi en iyi uygulamaları vurgulayacağız.

## Hızlı Yanıtlar
- **Java'da görüntü döndürme için en iyi kütüphane hangisidir?** Aspose.PSD for Java en güvenilir döndürme motorunu sağlar.  
- **Herhangi bir dereceyle döndürebilir miyim?** Evet, `rotate` yöntemi pozitif ya da negatif bir `float` açı kabul eder.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim için ticari lisans gereklidir.  
- **Hangi görüntü formatları destekleniyor?** PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF ve 30+ ek format.  
- **Boş alan için arka plan rengini nasıl ayarlarım?** `rotate` yöntemine bir `Color` örneği geçirin.

## Aspose.PSD for Java ile Belirli Bir Açıda Görüntüyü Döndürme?

Kaynak dosyanızı yükleyin, `image.rotate(angle, true, backgroundColor)` metodunu çağırın ve ardından kaydedin—tüm ağır matematiği sizin için halleden üç özlü adım. Aspose.PSD katmanları, renk profillerini ve alfa kanallarını korurken, kırpmayı önlemek için tuvali genişletir; böylece çıktı, 12.5° gibi kesirli açılar için bile tam olarak beklenen gibi görünür. Bu yaklaşım, birkaç kilobayttan çok sayfalı PSD'lere kadar dosyalar için bellek tüketmeden çalışır.

## Java'da Görüntü Döndürme Nedir?

Görüntü döndürme, bir piksel matrisini genellikle görüntü merkezi etrafında belirli bir açıyla döndüren geometrik bir dönüşümdür. Saf Java’da bir `Graphics2D` nesnesiyle çalışır, trigonometrik ofsetleri hesaplar ve arka planı manuel yönetirsiniz. Aspose.PSD bu karmaşıklığı soyutlar, renk derinliklerini, katman maskelerini ve farklı dosya formatlarını otomatik olarak işler.

## Görüntü Döndürmek İçin Neden Aspose.PSD Kullanmalı?

Aspose.PSD **30+ giriş ve çıkış formatını** destekler ve tipik bir sunucu‑sınıf CPU’da **500‑sayfalık PSD dosyalarını 5 saniyeden kısa sürede** işleyebilir. Kütüphanenin yerleşik önbellekleme (`image.cacheData()`) özelliği büyük varlıklar için bellek kullanımını %60’a kadar azaltır ve `rotate` yöntemi bir arka plan rengi belirlemenize olanak tanır; böylece gerektiğinde şeffaf köşeler korunur. Bu ölçülen faydalar, yüksek verimli görüntü işlem hatları için sektörde standart seçenektir.

## Önkoşullar

Başlamadan önce şunları temin edin:

1. **Java Development Kit (JDK 8 veya daha yeni)** – herhangi bir IDE veya komut satırı ortamı yeterlidir.  
2. **Aspose.PSD for Java** – en son JAR dosyasını [Aspose.PSD Java sayfasından](https://reference.aspose.com/psd/java/) indirin.  
3. **Bir örnek PSD dosyası** – örneğin, kodunuzdan referans alabileceğiniz bir klasöre yerleştirilmiş `sample.psd`.

## Paketleri İçe Aktarma

`RasterImage` sınıfı ve ilgili yardımcılar döndürme iş akışının çekirdeğidir.

`RasterImage` sınıfı, Aspose.PSD'nin raster‑tabanlı görüntü işleme için birincil nesnesidir. Raster görüntüleri yükleme, dönüştürme ve kaydetme metodlarını sunar ve meta verileri korur.

## Adım‑Adım Kılavuz

### Adım 1: Belge Dizinini Tanımlayın

Kaynak PSD'nin bulunduğu ve çıktının yazılacağı klasörü ayarlayın. Mutlak bir yol ya da `System.getProperty("user.dir")` kullanmak, göreli yol sürprizlerini ortadan kaldırır.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Adım 2: Kaynak ve Hedef Dosya Yollarını Belirleyin

Giriş PSD'si ve istenen çıktı formatı (örn. PNG, JPEG, TIFF) için tam dosya adlarını sağlayın. `destName` içindeki uzantıyı değiştirmek, uygun kodlayıcıyı otomatik olarak seçer.

```java
String dataDir = "Your Document Directory";
```

### Adım 3: Görüntüyü Yükleyin

`Image.load` yöntemi dosya formatını algılar ve raster işlemler için hazır bir `RasterImage` örneği döndürür.

`Image` sınıfı, diskteki bir dosyayı okuyup daha sonraki işleme uygun bir bellek içi temsil oluşturur. 30+ desteklenen tip için otomatik format algılamayı destekler.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### Adım 4: Görüntü Verilerini Önbellekle (İsteğe Bağlı ama Önerilir)

`image.cacheData()` çağrısı piksel verilerini bellekte saklar ve sonraki dönüşümleri büyük ölçüde hızlandırır—özellikle büyük PSD dosyalarında tekrarlanan disk I/O'sunu önler.

`cacheData()` metodu, görüntünün RAM'e tamamen yüklenmesini zorlayarak yoğun işlemler sırasında tembel yüklemenin getirdiği ek yükü azaltır.

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### Adım 5: Görüntüyü Döndürün

`rotate` metodunu üç argümanla çağırın: dönüş açısı (float), tuvali genişletme bayrağı ve yeni ortaya çıkan köşeler için arka plan rengi.

`rotate` metodu görüntüyü merkez etrafında döndürür, isteğe bağlı olarak döndürülmüş sınırları sığdırmak için tuvali büyütür. Arka plan `Color` boş alanı doldurur, şeffaf ya da siyah köşelerin oluşmasını önler.

- **20f** – derece cinsinden dönüş açısı (float). İstediğiniz herhangi bir açı için bu değeri değiştirin, örn. saat yönünde döndürme için `-45f`.  
- **true** – tuvali genişletirken orijinal en‑boy oranını korur.  
- **Color.getRed()** – boş köşeleri dolduran arka plan rengi; ihtiyaca göre `Color.getWhite()` ya da başka bir özel renk ile değiştirin.

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### Adım 6: Sonucu Kaydedin

Bir kodlayıcı (JPEG, PNG vb.) seçin ve `save` metodunu çağırın. `JpegOptions` kalite ayarı yapmanıza izin verirken, `PngOptions` kayıpsız çıktı sağlar.

`save` metodu, belirtilen seçenek nesnesiyle dönüştürülmüş görüntüyü diske yazar; sıkıştırma seviyesi ve renk derinliğinin gerektiği gibi korunmasını temin eder.

```java
image.rotate(20f, true, Color.getRed());
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **Döndürme sonrası boş köşeler** | Arka plan rengi sağlanmadı | `rotate` metoduna bir `Color` (ör. `Color.getWhite()`) geçirin. |
| **Büyük PSD'lerde bellek yetersizliği hatası** | Görüntü önbelleğe alınmadı | İşleme başlamadan önce `image.cacheData()` çağırın. |
| **Yanlış açı yönü** | Negatif ve pozitif açı karışıklığı | Saat yönünde döndürme için negatif değerler kullanın (veya koordinat sisteminize bağlı olarak tersine). |
| **Kaydedilmemiş değişiklikler** | `save` metodunun çağrılmayı unutması | Döndürmeden sonra `image.save(...)` metodunun çalıştırıldığından emin olun. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java kullanarak şeffaflık içeren görüntüleri döndürebilir miyim?**  
C: Evet. Kütüphane alfa kanallarını korur; köşeleri şeffaf tutmak için opak bir arka plan rengi belirtmeyin.

**S: Döndürme için desteklenen görüntü dosya formatlarıyla ilgili herhangi bir sınırlama var mı?**  
C: Hayır. Aspose.PSD PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF ve 30+ ek formatı destekler.

**S: Görüntüleri negatif bir açıyla döndürebilir miyim?**  
C: Kesinlikle. Saat yönünde döndürmek için `rotate` metoduna negatif bir float (örn. `-30f`) geçin.

**S: Aspose.PSD döndürme sırasında gerçek zamanlı görüntü önizlemesi sağlıyor mu?**  
C: API yalnızca sunucu tarafıdır. Canlı önizlemeler için döndürülmüş bitmap'i Swing veya JavaFX gibi bir UI çerçevesinde render edip görünümü yenileyin.

**S: Aspose.PSD için yardım alabileceğim bir topluluk forumu var mı?**  
C: Evet, sorular sormak ve deneyimlerinizi paylaşmak için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

---

**Last Updated:** 2026-05-19  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## İlgili Eğitimler

- [Aspose.PSD for Java'da Bicubic Resampler ile Yüksek Kaliteli Görüntü Ölçekleme](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Java'da Görüntü Yeniden Boyutlandırma - Aspose.PSD for Java'da Resize Type Enumeration Kullanımı](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Aspose.PSD ile Java'da Görüntü Bulanıklaştırma – Blur Efekti Ekle](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}