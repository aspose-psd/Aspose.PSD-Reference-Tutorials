---
date: 2026-11-04
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak kaydetmeyi, PNG'yi alfa
  kanalıyla dışa aktarmayı ve gölge katmanı eklemeyi öğrenin – eksiksiz, adım adım
  bir rehber.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- java image manipulation
lastmod: 2026-11-04
linktitle: Renderleme Gölge Uygula
og_description: Aspose.PSD for Java ile psd'yi png olarak kaydedin, PNG'yi alfa şeffaflığıyla
  dışa aktarın ve renderleme gölgesi ekleyin—Java geliştiricileri için adım adım rehber.
og_image_alt: Developer guide showing how to convert PSD to PNG and apply drop shadow
  using Aspose.PSD Java
og_title: psd'yi png olarak kaydedin ve Aspose.PSD for Java'da renderleme gölgesi
  uygulayın
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  headline: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  name: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  steps:
  - name: define document directory
    text: Define the directory path where your PSD files are stored.
  - name: set psd and png file paths
    text: Specify the full file paths for the source PSD and the target PNG.
  - name: load psd file with effects
    text: '`PsdImage` loads the PSD and gives access to its layers and effects.'
  - name: access drop shadow effect
    text: '`DropShadowEffect` represents a drop‑shadow layer effect that can be read
      or modified.'
  - name: validate shadow effect properties
    text: '`shadowEffect` holds the properties of the drop‑shadow such as opacity,
      distance, and size. > **Pro tip:** Adjust `setSpread()` or `setNoise()` to create
      softer or more textured shadows.'
  - name: save as png – the “save psd as png” step
    text: '`PngOptions` configures PNG export settings, including color type and alpha
      channel handling. At this point you have successfully **converted psd to png**,
      **exported png with alpha**, and applied a rendering drop shadow in a single
      workflow.'
  type: HowTo
- questions:
  - answer: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect`
      for each target layer, which also lets you perform a batch psd to png conversion.
    question: Can I apply drop shadows to multiple layers simultaneously?
  - answer: '`Spread` determines how abruptly the shadow transitions from full opacity
      to transparent. A higher value creates a harder edge.'
    question: What does the ‘Spread’ parameter control?
  - answer: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release,
      handling most layer types and effects.
    question: Is Aspose.PSD compatible with all Photoshop versions?
  - answer: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/)
      and run the sample without a license key.
    question: How can I test the code before purchasing a license?
  - answer: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      where the community and Aspose engineers can assist.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd as png
- aspose psd java
- java image manipulation
- png transparency
- rendering drop shadow
title: psd'yi png olarak kaydedin ve Aspose.PSD for Java'da renderleme gölgesi uygulayın
url: /tr/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG olarak kaydet ve Aspose.PSD for Java'da renderleme gölge ekle

## Giriş

Java'da Photoshop dosyalarıyla çalışıyorsanız, **saving psd as png** en sık karşılaştığınız görevlerden biridir. Birçok projede **save psd as png** yaparak varlıkları web veya mobil uygulamalara göndermeniz gerekir, şeffaflığı ve görsel efektleri koruyarak. Aspose.PSD ile sadece **convert psd to png** yapmakla kalmaz, aynı zamanda **adding a drop shadow layer** ile görüntüyü geliştirebilirsiniz. Bu öğreticide tüm süreci adım adım göstereceğiz—bir PSD'yi yükleme, renderleme gölge ekleme ve sonunda **saving the PSD as a PNG** dosyasını kaydetme—böylece bu iş akışını kendi projelerinize güvenle entegre edebilirsiniz.

## Hızlı cevaplar
- **PSD'den PNG'ye dönüşümü hangi kütüphane yönetir?** Aspose.PSD for Java.  
- **Gölge uygulamasının süresi ne kadar?** Temel bir örnek için yaklaşık 10‑15 dakika.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.  
- **Gölgeyi birden fazla katmana uygulayabilir miyim?** Evet—isteğe bağlı katmanlar üzerinde döngü yaparak, aynı zamanda toplu psd to png dönüşümü yapabilirsiniz.  
- **Hangi Java sürümü gereklidir?** Java 8 ve üzeri.

## “save psd as png” nedir ve neden önemlidir?

**Saving a PSD as PNG creates a widely‑supported, lossless image that retains transparency.** Bu format, Photoshop varlıklarını webde, mobil uygulamalarda veya daha büyük bir görüntü işleme hattının parçası olarak göstermeniz gerektiğinde esastır. Aynı anda bir gölge eklemek, Photoshop açmadan cilalı bir görsel efekt üretmenizi sağlar.

## Bu iş akışı için Aspose.PSD neden kullanılmalı?

Katman efektlerinin yükleme zamanında renderlanması yerleşiktir, bu yüzden Photoshop'a ihtiyacınız yok. Aspose.PSD 50'den fazla giriş ve çıkış formatını (PSD, PNG, JPEG, TIFF, BMP) destekler ve tüm dosyayı belleğe yüklemeden büyük belgeleri işleyebilir. Gölge ve parıltı gibi efektleri tam olarak oldukları gibi korur ve PNG'yi otomatik olarak alfa şeffaflığıyla dışa aktarır.

## Önkoşullar

- **Java Geliştirme Ortamı** – JDK 8 ve üzeri kurulu.  
- **Aspose.PSD for Java** – En son JAR'ı [Aspose.PSD download page](https://releases.aspose.com/psd/java/) adresinden indirin.  
- **Bir PSD dosyası** – Dosya, gölge eklemek istediğiniz en az bir katman içermelidir (ör. *Shadow.psd*).  

## Paketleri içe aktar

`com.aspose.psd` ad alanı, görüntüleri yüklemek, katmanları manipüle etmek ve PNG dosyalarını dışa aktarmak için temel sınıfları sağlar. `PsdImage` PSD dosyalarını yüklemek ve manipüle etmek için kullanılan ana sınıftır.  

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım adım kılavuz

### Adım 1: belge dizinini tanımla
PSD dosyalarınızın bulunduğu dizin yolunu tanımlayın.  

```java
String dataDir = "Your Document Directory";
```

### Adım 2: psd ve png dosya yollarını ayarla
Kaynak PSD ve hedef PNG için tam dosya yollarını belirtin.  

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Adım 3: efektlerle psd dosyasını yükle
`PsdImage` PSD'yi yükler ve katmanları ile efektlerine erişim sağlar.  

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Adım 4: gölge efektine eriş
`DropShadowEffect` okunabilen veya değiştirilebilen bir gölge katman efekti temsil eder.  

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Adım 5: gölge efekt özelliklerini doğrula
`shadowEffect` gölgenin opaklık, mesafe ve boyut gibi özelliklerini tutar.  

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Pro tip:** `setSpread()` veya `setNoise()` ayarlayarak daha yumuşak veya daha dokulu gölgeler oluşturabilirsiniz.

### Adım 6: png olarak kaydet – “save psd as png” adımı
`PngOptions` PNG dışa aktarma ayarlarını yapılandırır, renk tipi ve alfa kanal işleme dahil.  

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Bu noktada **converted psd to png**, **exported png with alpha** işlemlerini başarıyla gerçekleştirdiniz ve tek bir iş akışında renderleme gölge eklediniz.

## Alfa şeffaflığıyla png dışa aktar

PNG çıktısının şeffaf arka planı koruması gerektiğinde—özellikle UI kaplamaları veya web grafikleri için—kaydetme adımında gösterildiği gibi `PngColorType.TruecolorWithAlpha` kullandığınızdan emin olun. Bu, gölgenin katı bir arka plan yerine şeffaf bir tuval üzerinde olmasını sağlar ve **preserve png transparency** konusunda yardımcı olur.

## Java kullanarak gölge katmanı ekle

PSD'niz birden fazla gölge gerektiren katman içeriyorsa, `im.getLayers()` üzerinde dönen bir döngü içinde **Step 4** ve **Step 5**'i tekrarlamanız yeterlidir. Her yineleme bir `DropShadowEffect` örneği oluşturabilir veya değiştirebilir, katman başına opaklık, mesafe, boyut ve açı üzerinde ayrıntılı kontrol sağlar. Bu yaklaşım ayrıca her dosyanın aynı gölge işlemini almasını sağlayan bir **batch psd to png** dönüşümünü de mümkün kılar.

## save psd as png için yaygın kullanım senaryoları

* **Web varlık hatları** – Tasarımcı tarafından sağlanan PSD'leri yerleşik gölgelerle web‑hazır PNG'lere dönüştürün.  
* **Mobil uygulama kaynakları** – Şeffaf PNG simgelerini anında oluşturun, manuel dışa aktarmayı önleyin.  
* **Toplu işleme** – Sunucu tarafı bir görevde yüzlerce PSD dosyasının dönüşümünü otomatikleştirin, her PNG'nin alfa kanalını ve görsel efektlerini korumasını sağlayın.  

## Yaygın sorunlar ve çözümler

| Sorun | Muhtemel neden | Çözüm |
|-------|----------------|-------|
| **Gölge görünmüyor** | `Opacity` 0 olarak ayarlanmış veya katman gizli | `shadowEffect.getOpacity()` > 0 ve katman görünürlüğünü doğrulayın. |
| **PNG düz görünüyor (şeffaflık yok)** | Yanlış `PngColorType` kullanılmış | Yukarıdaki gibi `PngColorType.TruecolorWithAlpha` kullanın. |
| **Yükleme sırasında istisna** | Efektler yüklenmemiş | `loadOptions.setLoadEffectsResource(true)` çağrıldığından emin olun. |
| **Yanlış katman indeksi** | PSD yapısı farklı | `im.getLayers()`'ı inceleyin ve doğru indeksi seçin. |

## Sıkça sorulan sorular

**S: Birden fazla katmana aynı anda gölgeler uygulayabilir miyim?**  
Evet. `im.getLayers()` üzerinde döngü yaparak her hedef katman için bir `DropShadowEffect` ekleyebilir veya değiştirebilirsiniz, bu aynı zamanda bir batch psd to png dönüşümü yapmanızı sağlar.

**S: ‘Spread’ parametresi neyi kontrol eder?**  
`Spread` gölgenin tam opaklıktan şeffaflığa ne kadar ani geçiş yaptığını belirler. Daha yüksek değer daha keskin bir kenar oluşturur.

**S: Aspose.PSD tüm Photoshop sürümleriyle uyumlu mu?**  
Aspose.PSD Photoshop 3.0'dan en son sürüme kadar PSD dosyalarını destekler, çoğu katman türü ve efekti işler.

**S: Lisans satın almadan kodu nasıl test edebilirim?**  
Ücretsiz deneme sürümünü [Aspose.PSD download page](https://releases.aspose.com/psd/java/) adresinden indirin ve lisans anahtarı olmadan örneği çalıştırın.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
Sorununuzu [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) üzerinden sorabilirsiniz; topluluk ve Aspose mühendisleri yardımcı olur.

## Sonuç

Artık Aspose.PSD for Java kullanarak **save psd as png**, **export png with alpha**, **convert psd to png** ve **apply a drop shadow layer** işlemlerini nasıl yapacağınızı biliyorsunuz. Bu kombinasyon, Photoshop açmadan web, mobil veya masaüstü uygulamaları için yüksek kaliteli görüntü hazırlamayı otomatikleştirmenizi sağlar.

---

**Son Güncelleme:** 2026-11-04  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Renk Katmanı ile PSD'yi PNG'ye Dönüştür – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [Java Kullanarak PSD'ye Gölge Ekleme – Gelişmiş Katman Efektleri](/psd/java/advanced-psd-layer-features-effects/)
- [Aspose.PSD for Java ile PSD'yi Raster Görüntü Formatlarına Dönüştürme](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}