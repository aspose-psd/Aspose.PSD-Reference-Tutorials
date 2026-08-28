---
date: 2026-08-28
description: Aspose.PSD ile Java'da katmana pattern ekleyin. Bu adım adım kılavuzu
  izleyerek stroke layer effect uygulayın, pattern kaynaklarını yapılandırın ve PSD
  dosyalarınızı verimli bir şekilde kaydedin.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Java'da Stroke Layer Pattern ekleme
og_description: Aspose.PSD kullanarak Java'da katmana pattern ekleyin. Bu özlü kılavuzu
  izleyerek stroke layer effect uygulayın, pattern kaynaklarını yapılandırın ve PSD
  dosyalarınızı verimli bir şekilde kaydedin.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Java'da katmana pattern ekleme – Aspose.PSD tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Java'da katmana pattern ekleme
url: /tr/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da katmana desen ekleme

## Giriş
Java'da katmana desen ekleme, Photoshop PSD dosyalarını özel çizgi (stroke) efektleriyle zenginleştirmeniz gerektiğinde yaygın bir gereksinimdir. Aspose.PSD for Java ile bu görev basitleşir, hatta kütüphaneye yeniyseniz bile. Bu öğreticide bir PSD'yi nasıl yükleyeceğinizi, bir desen kaynağı oluşturacağınızı, bunu bir stroke efektine ekleyeceğinizi ve sonucu kaydedeceğinizi—adım adım net talimatlarla öğreneceksiniz.

## Hızlı cevaplar
- **Gerekli kütüphane nedir?** Aspose.PSD for Java.  
- **Uygulama ne kadar sürer?** Temel bir desen için yaklaşık 10‑15 dakika.  
- **Lisans gerekir mi?** Geliştirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Hangi Java sürümü desteklenir?** JDK 8 veya daha yeni.  
- **Bunu bir web hizmetinde kullanabilir miyim?** Evet, API platformdan bağımsızdır ve herhangi bir Java ortamında çalışır.

## Katmana desen eklemek ne anlama gelir?
Katmana desen eklemek, bir stroke veya dolgu efektine döşenen bir bitmap atamaktır; böylece grafik şeklin konturu boyunca tekrar eder. Bu teknik, dekoratif kenarlıklar, dokular ve marka kaplamaları için yaygın olarak kullanılır ve tasarımcıların her öğeyi manuel olarak çizmeye gerek kalmadan tutarlı görsel temalar oluşturmasını sağlar.

## Bu görev için neden Aspose.PSD kullanılmalı?
Aspose.PSD **30+ görüntü formatını** destekler ve **2 GB**'a kadar PSD dosyalarını bellek içinde tüm belgeyi yüklemeden işleyebilir, tipik sunucu donanımında hızlı performans sunar. Akıcı API'si sayesinde katman efektleri programatik olarak yönetilebilir, otomatikleştirilmiş iş akışlarında Photoshop'a ihtiyaç kalmaz.

## Önkoşullar
Başlamadan önce şunların yüklü olduğundan emin olun:
- Java Development Kit (JDK) 8 veya daha yeni kurulu.
- Aspose.PSD for Java – **Aspose.PSD for Java indirme sayfası**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) üzerinden indirin ve JAR dosyasını projenizin classpath'ine ekleyin.
- IntelliJ IDEA veya Eclipse gibi bir IDE, örnek kodu düzenlemek ve çalıştırmak için.
- Değiştirmek istediğiniz şekil katmanını içeren bir örnek PSD dosyası.

## Paketleri içe aktar
İlk olarak, PSD nesnelerine, kaynaklara ve efektlere erişim sağlayan ad alanlarını içe aktarın.

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## Java'da katmana desen ekleme nasıl yapılır?

Hedef PSD'yi yükleyin, bir desen kaynağı oluşturun, istediğiniz katmanın stroke efektine ekleyin ve sonunda dosyayı kaydedin. Bu uçtan uca akış sadece birkaç satır kodla gerçekleşir ve herhangi bir standart PSD'de vektör şekil katmanı bulunduğu sürece çalışır.

### Adım 1: PSD dosyasını yükle
Belgeyi yüklemek, katman hiyerarşisine ve efekt koleksiyonuna erişim sağlar.  
`PsdLoadOptions` PSD'nin nasıl okunacağını yapılandırırken, `PsdImage` bellekte yüklü dosyayı temsil eder.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

PSD dosyasını yükleyerek katmanlarını ve efektlerini artık erişebilir ve değiştirebilirsiniz.

### Adım 2: yeni desen verisini hazırla
Döşeme olarak kullanılacak bitmap'i tutan bir `PatternResource` oluşturun.  
`PatternResource` tekrarlayan bitmap desenini saklayan bir PSD global kaynağıdır. `Rectangle` desenin sınırlarını tanımlar, `UUID` ise benzersiz bir tanımlayıcı sağlar.

```
// Placeholder for original code.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
```

Bu desen verisi yeni stroke efektini oluşturmak için kullanılacak.

### Adım 3: stroke efektine eriş
Zaten bir stroke içeren şekil katmanını belirleyin, ardından `StrokeEffect` nesnesini alın.  
`StrokeEffect` bir şekil katmanına uygulanan stroke katman efektini temsil eder.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Bu, doğru katman ve efekt üzerinde çalıştığınızı doğrular.

### Adım 4: stroke efektini değiştir
Artık stroke özelliklerini yeni desen kaynağına referans verecek şekilde güncelleyin.

#### Stroke efekt özelliklerini güncelle
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Desen kaynağını güncelle
`PattResource` desen verisini saklayan bir PSD global katman kaynağıdır.

```
// Placeholder for original code.
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
```

Bu kod parçacıkları mevcut deseni sizin sağladığınız desenle değiştirir.

### Adım 5: yeni deseni uygula
`PatternFillSettings` desen tabanlı bir stroke efektinin dolgu ayarlarını tutar. Değişiklikleri katmana işleyin ve güncellenmiş PSD'yi diske kaydedin.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Bu, yeni desenin doğru şekilde uygulanmasını ve dosyanın değişikliklerle kaydedilmesini sağlar.

### Adım 6: değişiklikleri doğrula
Dosyayı yeniden yükleyin ve stroke'ı inceleyerek desenin beklendiği gibi göründüğünden emin olun.

```
// Placeholder for original code.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
```

Bu adım, desen verisinin stroke efektine doğru şekilde uygulandığını doğrular.

## Yaygın sorunlar ve hata ayıklama
- **Desen görünmüyor:** Desen görüntüsünün DPI'sinin PSD çözünürlüğüyle eşleştiğinden ve stroke'un `Enabled` bayrağının `true` olarak ayarlandığından emin olun.  
- **Büyük PSD dosyaları OutOfMemoryError oluşturur:** Katmanları isteğe bağlı olarak yüklemek için `PsdImage.load(..., LoadOptions)` ve `LoadOptions.setLoadAllLayers(false)` kullanın.  
- **Yanlış katman seçildi:** Efektlerine erişmeden önce katman indeksini veya adını doğrulayın; mevcut katmanları listelemek için `psdImage.getLayers()`'ı döngüye alabilirsiniz.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
A: Aspose.PSD for Java, geliştiricilerin PSD (Photoshop Document) dosyalarını programatik olarak oluşturmasını, düzenlemesini ve dönüştürmesini sağlayan bir kütüphanedir.

**S: Aspose.PSD for Java'yi ticari bir projede kullanabilir miyim?**  
A: Evet, ticari projelerde kullanabilirsiniz. **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)) üzerinden lisans satın alabilirsiniz.

**S: Aspose.PSD for Java için ücretsiz deneme mevcut mu?**  
A: Evet, **Aspose releases page**([Aspose releases page](https://releases.aspose.com/)) üzerinden ücretsiz deneme sürümünü indirebilirsiniz.

**S: Aspose.PSD for Java için destek nasıl alabilirim?**  
A: Aspose topluluk forumlarından **burada**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)) destek alabilirsiniz.

**S: Aspose.PSD for Java için sistem gereksinimleri nelerdir?**  
A: Bir JDK ve geliştirme için bir IDE gerekir. Kütüphane Windows, Linux ve macOS'u destekler.

## Sonuç
Artık Aspose.PSD kullanarak Java'da katmana desen eklemeyi öğrendiniz. Yukarıdaki adımları izleyerek PSD dosyalarına programatik olarak özel stroke desenleri ekleyebilir, marka iş akışlarını otomatikleştirebilir ve grafik işleme yeteneklerini herhangi bir Java‑tabanlı uygulamaya entegre edebilirsiniz. Katman birleştirme, renk ayarlamaları ve PNG veya JPEG olarak dışa aktarma gibi diğer Aspose.PSD özelliklerini keşfederek görüntü‑işleme araç setinizi daha da genişletebilirsiniz.

---

**Son Güncelleme:** 2026-08-28  
**Test Edilen:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose

## İlgili Eğitimler

- [Desen Dolgu Katmanını İşleme](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Desen Katmanı PSD: Aspose.PSD for Java ile Efekt Ekle](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Java'da Stroke Rengini Değiştirme Aspose.PSD Kullanarak](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}