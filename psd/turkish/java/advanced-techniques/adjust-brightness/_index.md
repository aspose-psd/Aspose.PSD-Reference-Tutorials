---
date: 2026-09-28
description: Java görüntü işleme öğreticisi, bir görüntünün parlaklığını Aspose.PSD
  for Java kullanarak nasıl ayarlayacağınızı gösterir. PSD veya TIFF dosyalarını yüklemek,
  değiştirmek ve kaydetmek için adım adım kodu izleyin.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Bir Görüntünün Parlaklığını Ayarlama
og_description: Java görüntü işleme öğreticisi, bir görüntünün parlaklığını Aspose.PSD
  for Java kullanarak nasıl ayarlayacağınızı gösterir. PSD veya TIFF dosyalarını yüklemek,
  değiştirmek ve kaydetmek için adım adım kodu izleyin.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Java görüntü işleme: Aspose.PSD ile parlaklığı ayarlama'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Java görüntü işleme: Aspose.PSD ile parlaklığı ayarlama'
url: /tr/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bir Görüntünün Parlaklığını Aspose.PSD for Java ile Ayarlama

## Giriş

Bu **java image processing** öğreticisinde, bir resmin parlaklığını doğrudan Java kodundan nasıl ayarlayacağınızı öğreneceksiniz. Parlaklık ayarlaması, grafik tasarımcıları, fotoğrafçılar ve görüntü‑işleme hatları oluşturan herkes için sık bir görevdir. Bu **java image manipulation** rehberinde, Aspose.PSD for Java kütüphanesini kullanarak tam iş akışını—PSD/TIFF yükleme, parlaklık ofseti uygulama ve sonucu kaydetme—adım adım inceleyeceğiz.

## Hızlı cevaplar
- **Parlaklığı hangi kütüphane yönetir?** Aspose.PSD for Java.  
- **Parlaklığı hangi yöntem değiştirir?** `RasterImage.adjustBrightness()`.  
- **PSD ve TIFF dosyalarıyla çalışabilir miyim?** Evet, API her iki formatı ve 10+ ek görüntü türünü destekler.  
- **Üretim için lisansa ihtiyacım var mı?** Değerlendirme dışı kullanım için ticari bir lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir ayarlama için genellikle 10 dakikadan az sürer.

## java image processing nedir?
`Java image processing`, Java kullanarak programlı bir şekilde görüntü verilerini okumanıza, dönüştürmenize ve yazmanıza olanak tanıyan teknikler kümesini ifade eder. Parlaklık ayarlaması, her pikselin genel ışıklılığını değiştiren temel işlemlerden biridir; karanlık bölgeleri aydınlatır veya parlak bölgeleri karartır.

## Neden Aspose.PSD for Java kullanmalı?
Aspose.PSD for Java, geniş bir raster ve vektör formatı yelpazesini destekleyen, yerel bağımlılıkları ortadan kaldıran ve büyük dosyalar için yüksek performanslı önbellekleme sunan kapsamlı, saf‑Java bir çözüm sağlar. Geniş API'si, geliştiricilerin karmaşık renk düzeltme ve katman‑tabanlı düzenlemeleri minimal kodla gerçekleştirmesine olanak tanır; bu da hem basit ayarlamalar hem de gelişmiş görüntü‑işleme hatları için idealdir.

- **10+ raster ve vektör formatını destekler** – PSD, TIFF, JPEG, PNG, BMP, GIF ve daha fazlası.  
- **Saf‑Java uygulaması** – yerel DLL'ler veya dış bağımlılıklar yoktur, bu yüzden herhangi bir JVM'de çalışır.  
- **Yüksek performanslı önbellekleme** – raster verileri önbelleğe alınabilir, büyük dosyalarda tekrarlanan düzenlemeleri 2× daha hızlı yapmayı sağlar.  
- **Zengin API yüzeyi** – renk düzeltme, katman yönetimi, maskeler ve birleştirme için 150'den fazla yöntem.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- Aspose.PSD for Java Kütüphanesi: Kütüphaneyi [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) adresinden indirin ve kurun.  
- Java Development Kit (JDK) 8 veya üzeri makinenize kurulu.  
- IntelliJ IDEA, Eclipse veya VS Code gibi bir geliştirme ortamı (IDE).

## Paketleri içe aktar

Başlamak için, Java projenize gerekli paketleri içe aktarın. Bu örnekte aşağıdakileri kullanacağız:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Şimdi, bir görüntünün parlaklığını ayarlama sürecini basit adımlara ayıralım:

## Aspose.PSD kullanarak parlaklık nasıl ayarlanır?

Kaynak görüntünüzü yükleyin, bir parlaklık ofseti uygulayın, kaydetme seçeneklerini yapılandırın ve sonucu diske yazın—tüm bunlar dört kısa adımda. Aşağıdaki bölümler, kendi projenize kopyalayabileceğiniz net, adım adım bir rehber sunar. Bu yaklaşım, her işlemin verimli bir şekilde gerçekleştirilmesini ve son görüntünün orijinal kalitesini korurken istenen parlaklık değişikliğini yansıtmasını sağlar.

### Adım 1: Görüntüyü yükle

`RasterImage` sınıfı, bellekte bir PSD veya TIFF dosyasının rasterleştirilmiş sürümünü temsil eder. Renk düzeltme işlemleri için doğrudan piksel erişimi sağlar.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Bu adımda, hedef görüntüyü yüklüyor ve daha sonraki işlemler için bir `RasterImage` nesnesine dönüştürüyoruz.

### Adım 2: Parlaklığı ayarla

`adjustBrightness(int value)` her pikselin ışıklılığını belirtilen tam sayı değeriyle değiştirir. Pozitif sayılar görüntüyü aydınlatır; negatif sayılar karartır. Metot, görüntüyü yerinde işler, bu yüzden ek nesne oluşturulmasına gerek yoktur.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Burada, `adjustBrightness` metodunu kullanarak görüntünün parlaklığını değiştiriyoruz. Bu örnekte parlaklığı 50 birim azaltıyoruz, ancak ihtiyacınıza göre bu değeri özelleştirebilirsiniz.

### Adım 3: TiffOptions ayarla

`TiffOptions`, TIFF çıktısı için kodlama parametrelerini (örneğin örnek başına bit ve fotometrik yorumlama) belirler. Sonuç dosyasının nasıl kodlanacağını kontrol etmenizi sağlar.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

`TiffOptions`'ı ayarlanmış görüntüyü kaydetmek için yapılandırın. `bitsPerSample` ve `photometric` özelliklerini özel ihtiyaçlarınıza göre ayarlayın.

### Adım 4: Oluşan görüntüyü kaydet

`save` çağrısı, işlenmiş raster verilerini önceden tanımlanmış seçeneklerle bir dosyaya yazar. İşlem atomiktir ve çıktı dosyasının geçerli bir TIFF görüntüsü olmasını garanti eder.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Son olarak, belirtilen `TiffOptions` ile değiştirilmiş görüntüyü kaydedin.

## Yaygın sorunlar ve çözümler

| Issue | Reason | Solution |
|-------|--------|----------|
| **`ClassCastException` Image cast edilirken** | Dosya raster görüntü değil (ör. vektör PSD). | Kaynak dosya formatını doğrulayın veya cast etmeden önce `image instanceof RasterImage` kontrol edin. |
| **Parlaklık değişikliği etkisiz** | Görüntü ayarlamadan önce önbelleğe alınmamış. | `rasterImage.cacheData()` metodunu Adım 1'de gösterildiği gibi çağırın. |
| **Kaydedilen dosya bozuk görünüyor** | `TiffOptions` yapılandırması hatalı. | `bitsPerSample` değerinin kaynak görüntünün derinliğiyle (genellikle kanal başına 8‑bit) eşleştiğinden emin olun. |

## Sıkça sorulan sorular

**Q:** PSD dışındaki diğer görüntü formatlarında parlaklığı ayarlayabilir miyim?  
**A:** Evet, Aspose.PSD for Java PSD ve TIFF'e ek olarak JPEG, PNG, BMP, GIF ve birçok diğer raster formatını destekler.

**Q:** Görüntü ayarlama sürecinde hataları nasıl ele alabilirim?  
**A:** İşleme kodunu bir try‑catch bloğuna sarın ve `IOException` veya `ImageProcessingException` yakalayarak dosya erişimi ve raster işlemleri hatalarını yönetin.

**Q:** Parlaklık ayarlama aralığına bir limit var mı?  
**A:** Metot –255 ile +255 arasında tam sayı değerleri kabul eder; bu aralığın dışındaki değerler en yakın sınıra kırpılır.

**Q:** Aspose.PSD for Java'ı ticari projelerde kullanabilir miyim?  
**A:** Evet, üretim kullanımı için ticari bir lisans gereklidir. Lisansı [buradan](https://purchase.aspose.com/buy) satın alın.

**Q:** Ücretsiz deneme mevcut mu?  
**A:** Evet, kütüphaneyi [buradan](https://releases.aspose.com/) ücretsiz deneme ile keşfedebilirsiniz.

**Q:** `adjustBrightness` metodu katman görünürlüğünü etkiler mi?  
**A:** Metot rasterleştirilmiş birleşik görüntü üzerinde çalışır, bu yüzden gizli katmanlar rasterleştirme sırasında göz ardı edilir ve istenen görsel sonuç korunur.

**Q:** Birden fazla ayarlamayı (ör. kontrast, doygunluk) bir arada zincirleyebilir miyim?  
**A:** Kesinlikle. Parlaklığı ayarladıktan sonra aynı `RasterImage` örneğinde `adjustContrast`, `adjustSaturation` veya diğer renk‑düzeltme metodlarını çağırabilirsiniz.

---

**Last Updated:** 2026-09-28  
**Test Edilen:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Java Kütüphanesi ile Görüntü İşleme: Aspose.PSD kullanarak Katmanı Ters Çevir](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Aspose.PSD for Java ile Görüntüyü Gri Tonlamaya Dönüştür](/psd/java/advanced-techniques/grayscale-image/)
- [Aspose.PSD for Java ile Belirli Bir Açıda Görüntüyü Döndürme](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}