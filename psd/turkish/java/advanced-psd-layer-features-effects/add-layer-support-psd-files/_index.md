---
date: 2026-07-22
description: Aspose.PSD for Java ile PSD katmanlarını nasıl çıkaracağınızı ve PSD
  katmanlarını PNG'ye dönüştüreceğinizi öğrenin. Sağlam grafik işleme ihtiyacı duyan
  geliştiriciler için idealdir.
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: Aspose.PSD Java kullanarak PSD Katmanlarını Çıkarın ve PSD Dosyaları için
  Katman Desteği Ekleyin
og_description: Aspose.PSD for Java ile PSD katmanlarını çıkarın ve PNG'ye dönüştürün.
  Katman çıkarma ve görüntü dönüştürmeyi otomatikleştirmek için adım adım kılavuzu
  izleyin.
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: PSD Katmanlarını Çıkarın – Aspose.PSD Java kullanarak PSD Dosyaları için
  Katman Desteği Ekleyin
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: Aspose.PSD Java kullanarak PSD Katmanlarını Çıkarın ve PSD Dosyaları için Katman
  Desteği Ekleyin
url: /tr/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java Kullanarak PSD Katmanlarını Çıkarın ve PSD Dosyaları İçin Katman Desteği Ekleyin

## Giriş
Photoshop Document (PSD) dosyalarıyla çalışmak, grafik tasarımcıları ve geliştiriciler için günlük bir gerçektir ve **extract psd layers** genellikle varlıkları yeniden kullanma veya görüntü iş akışlarını otomatikleştirme yolundaki ilk adımdır. Bu öğreticide, bir PSD'den tek tek katmanları nasıl çıkaracağınızı, tam katman desteğini nasıl etkinleştireceğinizi ve Aspose.PSD for Java kullanarak **convert PSD layers to PNG** işlemini öğreneceksiniz. Ortam kurulumundan en iyi uygulama ipuçlarına kadar her şeyi ele alacağız, böylece bu iş akışını birkaç dakika içinde herhangi bir Java uygulamasına entegre edebilirsiniz.

## Hızlı Yanıtlar
- **“extract PSD layers” ne anlama geliyor?** Bir PSD dosyasını yüklemek ve her bir katmana manipülasyon veya dışa aktarma için erişmek anlamına gelir.  
- **Bu işlemi Java'da hangi kütüphane yönetiyor?** Aspose.PSD for Java, Photoshop'a ihtiyaç duymadan tam özellikli PSD işleme sağlar.  
- **PSD katmanlarını tek seferde PNG'ye dönüştürebilir miyim?** Evet—dosyayı uygun seçeneklerle yükleyip şeffaflığı koruyan PNG seçenekleriyle kaydederek.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Üretim için ticari bir lisans gereklidir; değerlendirme için ücretsiz bir deneme sürümü mevcuttur.  
- **Hangi Java sürümü gerekiyor?** JDK 8 veya üzeri (öğreticide örnek olarak JDK 11 kullanılmıştır).

## Aspose.PSD for Java Kullanarak PSD Katmanlarını Nasıl Çıkarabilirsiniz?
PSD'yi yükleyin, katman efektlerini etkinleştirin ve sadece birkaç satır Java koduyla sonucu PNG olarak kaydedin. Bu doğrudan yaklaşım sunucuda Photoshop ihtiyacını ortadan kaldırır ve Java 8+ destekleyen herhangi bir platformda çalışır.  
İlk olarak `setLoadEffectsResource(true)` ve `setUseDiskForLoadEffectsResource(true)` ile bir `PsdLoadOptions` nesnesi oluşturursunuz, ardından dosyayı `PsdImage.load(path, options)` ile yüklersiniz. Yükleme sonrası katmanları `image.save(outputPath, new PngOptions())` ile birleştirebilir veya `image.getLayers()` üzerinden döngü yaparak her katmanı ayrı ayrı dışa aktarabilirsiniz; bu sayede tüm efektler korunur ve bellek kullanımı düşük tutulur.

## Neden PSD katmanlarını çıkarıp PNG'ye dönüştürmeliyiz?
Katmanları çıkarmak, **varlıkları yeniden kullanmanıza**, **küçük resim üretimini otomatikleştirmenize** ve web‑hazır grafiklerde **şeffaflığı korumanıza** olanak tanır. Aspose.PSD, **50+ giriş ve çıkış formatını** destekler ve disk‑tabanlı kaynak yönetimi sayesinde tüm dosyayı belleğe yüklemeden çok sayfalı PSD dosyalarını işleyebilir.

## Önkoşullar
Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Environment** – JDK yüklü. İndirmek için [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) adresini ziyaret edebilirsiniz.  
2. **Aspose.PSD for Java** – En son kütüphaneyi resmi indirme sayfasından [buradan](https://releases.aspose.com/psd/java/) alın.  
3. **Basic Java knowledge** – Java programlarını derleme ve çalıştırma konularına aşina olmalısınız.  
4. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
5. **A PSD file** – Sahip olduğunuz herhangi bir PSD dosyasını kullanın veya test için bir örnek PSD indirin.

Bu maddelere sahip olduğunuzda, PSD katmanlarını çıkarmaya başlayabilirsiniz.

## Paketleri İçe Aktarın
`PsdImage`, `PsdLoadOptions` ve `PngOptions` sınıfları iş akışının çekirdeğini oluşturur.  

`PsdImage`, Aspose.PSD'nin bellekte tek bir PSD dosyasını temsil eden üst‑seviye nesnesidir.  

`PsdLoadOptions`, katman efektleri gibi kaynakların nasıl yükleneceğini kontrol etmenizi sağlar.  

`PngOptions`, PNG dosyasının çıktı formatını ve şeffaflık işleme şeklini tanımlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: Dizinlerinizi Tanımlayın
Kaynak PSD ve çıktı PNG için yolları ayarlayın. `dataDir` değişkenini dosyalarınızın bulunduğu klasöre işaret edecek şekilde ayarlayın.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"` ifadesini gerçek klasör yolunuzla değiştirin.  
- `sourceFileName` – İşlemek istediğiniz PSD'nin tam yolu.  
- `output` – Çıkarılan katmanları içerecek PNG'nin hedef yolu.

## Adım 2: Yükleme Seçeneklerini Ayarlayın
`PsdLoadOptions` yapılandırması, tüm katman efektlerinin ve kaynakların doğru şekilde yüklenmesini sağlar; bu, **extract PSD layers** işlemi için kritiktir.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – Katmanlara eklenmiş ek efektleri (ör. gölgeler) yükler.  
- `setUseDiskForLoadEffectsResource(true)` – Ağır kaynakları diske yönlendirerek bellek üzerindeki baskıyı azaltır.

## Adım 3: PSD Dosyasını Yükleyin
Şimdi, yukarıda tanımlanan seçenekleri kullanarak PSD'yi bir `PsdImage` nesnesine yüklüyoruz.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

Bu noktada, `image` tüm katmanları, maskeleri ve efektleri içerir ve çıkarma için hazırdır.

## Adım 4: Kaydetme Seçeneklerini Ayarlayın
PNG'nin nasıl kaydedileceğini yapılandırın. `TruecolorWithAlpha` kullanmak, orijinal katmanlardaki şeffaflığı korur.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Adım 5: Görüntüyü Kaydedin (PSD Katmanlarını PNG'ye Dönüştürün)
Yüklenmiş PSD'yi (tüm katmanlarıyla) tek bir PNG dosyasına dışa aktarın. Bu adım, **convert psd layers png** işlemini tek bir adımda gerçekleştirir.

```java
image.save(output, saveOptions);
```

Her katmanı ayrı bir PNG olarak ihtiyacınız varsa, `image.getLayers()` üzerinden döngü yapabilirsiniz; ancak çoğu senaryoda birleştirilmiş bir PNG yeterli olur.

## Adım 6: İşlemi Tamamlayın
İşlemin başarılı olduğunu gösteren dostça bir konsol mesajı ekleyin.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Yaygın Sorunlar ve İpuçları
- **Out‑of‑Memory Errors:** Çok büyük PSD'ler işliyorsanız, geçici verileri diske yönlendirmek için `setUseDiskForLoadEffectsResource(true)` seçeneğini açık tutun.  
- **Missing Effects:** `setLoadEffectsResource(true)` ayarının yapıldığından emin olun; aksi takdirde bazı katman efektleri göz ardı edilebilir.  
- **Path Problems:** Platform bağımsız yol yönetimi için `java.nio.file` paketinden `Paths.get(...)` kullanın.

## Sık Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, Photoshop yüklü olmadan PSD dosyalarını manipüle etmenizi sağlayan bir kütüphanedir.

**S: Aspose.PSD'yi diğer dosya formatları için kullanabilir miyim?**  
C: Evet! Öncelikli olarak PSD dosyaları için olsa da, Aspose AI, PDF ve SVG dahil olmak üzere geniş bir format yelpazesi için kütüphaneler sunar.

**S: Deneme sürümü mevcut mu?**  
C: Kesinlikle! Ücretsiz bir deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

**S: Sorun yaşarsam nereden destek alabilirim?**  
C: PSD ile ilgili sorular için Aspose forumuna [buradan](https://forum.aspose.com/c/psd/34) ulaşabilirsiniz.

**S: Her katmanı ayrı bir PNG'ye dönüştürebilir miyim?**  
C: `image.getLayers()` üzerinden döngü yapın, her katman için yeni bir `Bitmap` oluşturun ve kendi `PngOptions` nesnesiyle kaydedin. Bu, katman başına ayrı PNG dosyaları üretir.

## Sonuç
Artık **extract PSD layers**, tam katman desteğini etkinleştirme ve Aspose.PSD for Java kullanarak **convert PSD layers to PNG** konularını öğrendiniz. İster otomatik bir varlık iş akışı oluşturun, ister masaüstü uygulamasına grafik yetenekleri ekleyin, bu yaklaşım Photoshop'a ihtiyaç duymadan Photoshop dosyaları üzerinde ince ayarlı kontrol sağlar. Filtreler uygulayarak, katmanları programatik olarak birleştirerek veya her katmanı ayrı ayrı dışa aktararak iş akışınızı daha da geliştirebilirsiniz.

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java Kullanarak PSD'yi PNG'ye Dışa Aktar ve Yeni Normal Katman Ekleyin](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Java'da Katman Maskesi Desteğiyle PSD'yi PNG'ye Dışa Aktar](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Java'da PSD'yi Görsele Dönüştür – Aspose.PSD ile Ayarlama Katmanlarını Uygula](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}