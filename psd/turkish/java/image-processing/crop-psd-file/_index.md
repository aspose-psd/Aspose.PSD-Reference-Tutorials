---
date: 2026-08-17
description: Aspose.PSD for Java ile psd dosyasını Java'da nasıl kırpacağınızı öğrenin
  – Java uygulamalarınızda Photoshop belgelerini hızlı ve hassas bir şekilde kırpmak
  için bir yöntem.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: PSD Dosyasını Kırp
og_description: Aspose.PSD for Java kullanarak Java'da psd dosyasını kırpın. Bu rehber,
  Photoshop dosyalarını verimli bir şekilde nasıl kırpacağınızı adım adım gösterir,
  kodsuz açıklamalar ve en iyi uygulama ipuçları sunar.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Aspose.PSD ile Java'da psd dosyasını kırp – hızlı görüntü kırpma
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Aspose.PSD kullanarak Java'da psd dosyasını kırp
url: /tr/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD ile Java'da PSD dosyasını kırpma

## Giriş

Eğer Photoshop belgelerini programlı olarak kırpmanız gerekiyorsa, **crop psd file java** grafik boru hatları, varlık boru hatları veya otomatik tasarım iş akışlarıyla çalışan Java geliştiricileri için yaygın bir görevdir. Aspose.PSD for Java, bir dikdörtgen tanımlamanıza ve ihtiyacınız olan bölgeyi sadece birkaç satır kodla çıkarmanıza olanak tanıyan özel bir API sağlar. Bu öğreticide, kütüphanenin yüksek performanslı kırpma için nasıl tasarlandığını, ortamınızı nasıl kuracağınızı ve hem PSD hem de PNG sonuçları üretmek için tam adımları öğreneceksiniz.

## Hızlı cevaplar
- **Java'da PSD kırpma işlemini hangi kütüphane yönetir?** Aspose.PSD for Java.
- **Temel bir kırpma için kaç satır kod gerekir?** Görüntüyü yükledikten sonra iki API çağrısı.
- **Kırpılmış alanı PNG olarak dışa aktarabilir miyim?** Evet, yerleşik PNG kaydetme seçenekleri kullanılarak.
- **Üretim kullanımında lisans gerekli mi?** Deneme süresinin ötesinde ticari bir lisans gereklidir.
- **Hangi Java sürümleri destekleniyor?** Java 8 ve sonrası, Java 11, 17 ve 21 dahil.

## crop psd file java nedir?

Crop psd file java, Java kodu kullanarak bir Photoshop Belgesi (.psd) içinden dikdörtgen bir bölgeyi programlı olarak kesme işlemine denir. Aspose.PSD ile bu işlemi Photoshop'u başlatmadan gerçekleştirebilir, bu da sunucu‑tarafı görüntü boru hatları için ideal hâle getirir.

## Neden Aspose.PSD for Java kullanmalısınız?

Aspose.PSD, **30+ giriş ve çıkış formatını** destekler ve belgenin tamamını belleğe yüklemeden **500 MB**'a kadar PSD dosyalarını işleyebilir; bu, akış (streaming) mimarisi sayesinde mümkündür. Kütüphane katmanları, maskeleri ve renk profillerini korur, Photoshop'un yerel çıktısına eşdeğer bir kırpılmış sonuç sunar. Bu ölçülebilir performans, tahmin edilebilir bellek kullanımıyla sıradan donanımlarda toplu işler yürütmenizi sağlar.

## Önkoşullar

- **Java development environment** – JDK 8 veya daha yeni bir sürüm kurulu ve yapılandırılmış.
- **Aspose.PSD for Java** – en son JAR ve belgeleri indirin [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **Sample PSD file** – kodun bulabilmesi için .psd dosyasını proje dizininize yerleştirin.

## Java'da bir PSD dosyasını nasıl kırparız?

Kaynak dosyayı yükleyin, tutmak istediğiniz dikdörtgeni tanımlayın, kırpma işlemini uygulayın ve sonunda sonucu istediğiniz formatlarda kaydedin. Tüm iş akışı sadece beş basit adım gerektirir; her adım, kendi kodunuzu ekleyeceğiniz bir yer tutucu ile gösterilmiştir.

### Adım 1: belge dizinini ayarla

“Your Document Directory” ifadesini, işlemek istediğiniz PSD dosyasını içeren mutlak ya da göreli yol ile değiştirin.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Adım 2: PSD dosyasını yükle

`RasterImage` sınıfı, Aspose.PSD'nin bir PSD dosyası üzerinde raster‑tabanlı işlemler için giriş noktasıdır. Dosyayı yüklemek, bellekte bir temsil oluşturur ve bu temsil üzerinde değişiklik yapabilirsiniz.

```java
String dataDir = "Your Document Directory";
```

### Adım 3: kırpma alanını tanımla

`Rectangle`, tutmak istediğiniz bölgenin X ve Y koordinatlarını, genişlik ve yükseklik değerleriyle tanımlar. Bu sınıf, standart Java AWT paketinin bir parçasıdır ve Aspose.PSD tarafından kırpma sınırlarını belirtmek için kullanılır.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Adım 4: kırpılmış PSD'yi kaydet

Kırpma uygulandıktan sonra, sonucu PSD formatında geri kaydedebilirsiniz. Kütüphane yalnızca kırpılmış pikselleri yazar, orijinal renk modu ve bit derinliğini korur.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Adım 5: kırpılmış görüntüyü PNG olarak kaydet

Web‑uyumlu bir sürüme ihtiyacınız varsa, kırpılmış rasteri PNG olarak dışa aktarın. Aspose.PSD, sıkıştırma seviyesini ve tarama (interlacing) ayarını kontrol etmenizi sağlayan PNG kaydetme seçenekleri sunar.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Yaygın sorunlar ve çözümler

- **Incorrect rectangle coordinates** – X/Y değerlerinin sol‑üst köşe için 0’dan başladığından emin olun; negatif değerler `ArgumentException` hatası verir.
- **Memory spikes on large files** – Gizli katmanlara ihtiyacınız olmadığında belleği azaltmak için `loadOptions.setLoadOnlyVisibleLayers(true)` seçeneğini kullanın.
- **Color profile loss** – Kırpmadan önce `image.getColorProfile()` çağırarak orijinal ICC profilini koruyun ve işlem sonrası tekrar atayın.

## Sıkça sorulan sorular

### Q1: Aspose.PSD for Java'yı diğer formatlarda görüntü kırpmak için kullanabilir miyim?

A1: Aspose.PSD öncelikle PSD dosyalarını hedef alır, ancak hem giriş hem de çıkış için BMP, GIF, JPEG, PNG, TIFF ve birkaç diğer raster formatını da destekler.

### Q2: Aspose.PSD for Java büyük ölçekli görüntü işleme için uygun mu?

A2: Evet. Kütüphanenin akış mimarisi, 100 MB'den az bir bellek ayak iziyle çok sayfalı PSD dosyalarını işleyebilir; bu da toplu işler için idealdir.

### Q3: Aspose.PSD for Java kullanımıyla ilgili lisans hususları var mı?

A3: Üretim dağıtımları için ticari bir lisans gereklidir. Ayrıntılar [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy) adresinde mevcuttur.

### Q4: Aspose.PSD for Java ile ilgili sorunlar için nasıl destek alabilirim?

A4: Sorular sormak, kod parçacıkları paylaşmak ve topluluktan ve ürün mühendislerinden yardım almak için [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

### Q5: Aspose.PSD for Java'yı satın almadan önce deneyebilir miyim?

A5: Evet, tam işlevsel ücretsiz deneme sürümünü [Aspose.PSD free trial download](https://releases.aspose.com/) adresinden indirebilirsiniz.

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## İlgili Öğreticiler

- [Aspose.PSD for Java'da Dikdörtgen ile Görüntü Kırpma](/psd/java/image-editing/crop-image-by-rectangle/)
- [Aspose.PSD for Java'da Kaydırmalarla Görüntü Kırpma](/psd/java/image-editing/crop-image-by-shifts/)
- [Aspose.PSD ile Java'da Görüntüyü Döndürme](/psd/java/advanced-image-manipulation/rotate-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}