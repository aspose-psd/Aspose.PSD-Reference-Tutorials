---
date: 2026-10-18
description: Aspose.PSD kullanarak Java görüntülerinde radial gradient etkileri nasıl
  oluşturulacağını öğrenin. Sorunsuz entegrasyon için bu step‑by‑step kılavuzu izleyin.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Gradient etkileri ekle
og_description: Aspose.PSD kullanarak Java'da radial gradient etkileri oluşturmayı
  öğrenin. Bu öğreticide, gradient overlay'leri dakikalar içinde ekleme, özelleştirme
  ve kaydetme yöntemleri gösterilmektedir.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Aspose.PSD ile Java'da radial gradient oluşturun – step‑by‑step kılavuz
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Aspose.PSD for Java'da radial gradient etkileri nasıl oluşturulur
url: /tr/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java'da radyal degrade efektleri nasıl oluşturulur

## Giriş

Bu rehberde Aspose.PSD kütüphanesini kullanarak **radyal degrade java** efektleri oluşturmayı öğreneceksiniz. Radyal degrade'ler, Photoshop açmadan PSD katmanlarınıza derinlik, odak veya hafif bir parıltı eklemek için mükemmeldir. Öğreticinin sonunda bir PSD'yi yükleyebilecek, bir degrade kaplaması uygulayabilecek, özelliklerini ayarlayabilecek ve sonucu Java kodu ile kaydedebileceksiniz.

## Hızlı cevaplar
- **Ne başarabilirim?** PSD katmanları üzerinde radyal degrade kaplamalarını ekleyin, düzenleyin ve karıştırın.  
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java (en son sürüm).  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir radyal degrade kaplaması için yaklaşık 10‑15 dakika.  
- **Java 8+ ile uyumlu mu?** Evet, API Java 8 ve daha yeni çalışma zamanlarını destekler.

## Önkoşullar

Öğreticiye başlamadan önce, aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1. **Aspose.PSD for Java Kütüphanesi** – Aspose.PSD for Java kütüphanesini indirdiğinizden ve kurduğunuzdan emin olun. Kütüphaneyi ve belgelerini [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/) adresinde bulabilirsiniz.  
2. **Java Geliştirme Ortamı** – Makinenizde bir Java geliştirme ortamı kurun (JDK 8 veya üzeri, tercih ettiğiniz IDE).  
3. **En Son Aspose.PSD Sürümü** – En yeni sürümü [Aspose releases page](https://releases.aspose.com/) adresinden indirin.  
4. **Destek kaynakları** – Sorunlarla karşılaşırsanız, [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34) adresine bakın.  
5. **Lisans satın alma** – Üretime geçmeye hazır olduğunuzda, lisansı [purchase page](https://purchase.aspose.com/buy) üzerinden edinin.

Şimdi her şey hazır olduğuna göre, adım adım kılavuza geçelim.

## Gradient overlay efekti nedir?

Gradient overlay efekti, bir katmanın seçili alanı boyunca iki veya daha fazla renk arasında yumuşak bir geçiş uygular. Photoshop'ta bu efekt karıştırılabilir, renklendirilebilir ve konumlandırılabilir, böylece karmaşık görsel tasarımlar oluşturulur. `GradientOverlayEffect` sınıfı, Aspose.PSD'nin bu katman stilinin temsili olup renk durakları, opaklık, karıştırma modu ve degrade stili gibi özellikleri ortaya çıkarır.

## Radyal degrade efekti nasıl oluşturulur

PSD'yi yükleyin, hedef katmanı bulun, `GradientOverlayEffect` özelliklerini ayarlayın ve sonunda dosyayı kaydedin. Görüntü yüklendikten sonra tam iş akışı dört kısa Java satırı içinde gerçekleşir.

### Adım 1: PSD dosyasını yükleyin ve degrade kaplamasına erişin

`PsdLoadOptions`, bir PSD dosyasının nasıl yükleneceğini yapılandırır ve efekt kaynaklarının yüklenmesini etkinleştirmenizi sağlar. `Image.load`, dosyayı bir `Image` nesnesine okur.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

Bu adımda, bir PSD dosyası yüklüyor ve ikinci katmandan (indeks 1) ilk `GradientOverlayEffect` nesnesini alıyoruz. `loadOptions.setLoadEffectsResource(true)` çağrısı, efekt kaynaklarının düzenleme için kullanılabilir olmasını sağlar.

### Adım 2: İlk Ayarları Doğrula

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Değişiklik yapmadan önce, mevcut karıştırma modunu, opaklığı ve görünürlüğü doğrulamak iyi bir uygulamadır. Bu, degrade kaplamasının temel durumunu anlamanıza yardımcı olur.

### Adım 3: Degrade Ayarlarını Değiştir

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Burada degrade rengini, opaklığını ve karıştırma modunu özelleştirebilirsiniz. Örnekte renk yeşile değiştiriliyor, opaklık 193'e (255 üzerinden) düşürülüyor ve karıştırma modu **Lighten** olarak ayarlanıyor. `Multiply`, `Screen` veya `Overlay` gibi diğer `BlendMode` değerleriyle denemeler yapabilirsiniz.

### Adım 4: Düzenlenmiş Görüntüyü Kaydet

```java
// Save the edited image
im.save(exportPath);
```

Değişikliklerinizi uyguladıktan sonra, PSD'yi yeni bir dosyaya kaydederek değişiklikleri kalıcı hale getirin. Bu adım, orijinal dosyanın dokunulmaz kalmasını sağlar.

### Adım 5: Değişiklikleri Doğrula

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

Yukarıdaki kod parçacığı, bir PSD'yi nasıl açacağınızı, ikinci katmanın ilk efektini (degrade kaplaması olduğu varsayılıyor) alıp, değişiklik için nasıl hazırlayacağınızı gösterir.

### Adım 2: Orijinal ayarları doğrula (isteğe bağlı ancak önerilir)

Herhangi bir şey değiştirmeden önce, mevcut karıştırma modu, opaklık ve görünürlüğü kontrol etmek temel durumu anlamanıza yardımcı olur. Koddaki `Assert` çağrıları, etkinin şu anda **Normal** karıştırma modunda, tamamen opak ve görünür olduğunu doğrular.

### Adım 3: Radyal bir stil elde etmek için degrade özelliklerini ayarla

Degrade rengini, opaklığını ve karıştırma modunu değiştirebilirsiniz. Gerçek bir radyal efekt için degrade stilini şu şekilde ayarlayın:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Pro ipucu:* Başlangıç rengini tanımlamak için `Color.getGreen()` veya herhangi bir `java.awt.Color` örneğini, bitiş rengi için ise `gradientOverlay.setColor2(Color.getBlue())` kullanın.

### Adım 4: Düzenlenmiş PSD'yi kaydet

`im.save(exportPath);` çağrısı, değiştirilmiş görüntüyü diske yazar. Kaydedilen dosya radyal degrade kaplamasını korur ve Photoshop'ta açılabilir, tarayıcılarda önizlenebilir veya diğer formatlara dönüştürülebilir.

## Neden radyal degrade kaplamaları oluşturmalıyız?

Radyal degrade'ler tasarımlara derinlik ve odak ekler, öğeleri üç boyutlu veya spot ışıklı gösterir. Şunlar için idealdir:

- **Arka plan doldurmaları** ki gözleri merkezi konuya çeker.  
- **Düğme veya simge vurguları** hafif bir parıltı gerektiğinde.  
- **Yaratıcı fotoğraf efektleri** gibi vignette'ler veya ışık patlamaları.  

Aspose.PSD, **50+ giriş ve çıkış formatını** işleyebilir ve tüm belgeyi belleğe yüklemeden çok sayfalı PSD dosyalarını yönetebilir; bu sayede büyük varlık kütüphanelerinde degrade oluşturmayı otomatikleştirebilirsiniz.

## Yaygın sorunlar ve ipuçları

- **Efekt görünmüyor:** `gradientOverlay.isVisible()` değerinin `true` olduğundan emin olun. Bazı PSD dosyaları efektleri varsayılan olarak gizler.  
- **Yanlış katman indeksi:** Katmanlar sıfır tabanlıdır; doğru katmana (`im.getLayers()[1]` ikinci katmana işaret eder) hedeflediğinizden emin olun.  
- **Opaklık dönüşümü:** `setOpacity` metodu bir `byte` bekler. `int` geçirirseniz derleme hatası alırsınız; örnekte gösterildiği gibi açıkça dönüştürün.  
- **Kaynak yükleme:** Efektlere erişirken `null` alırsanız, görüntüyü yüklemeden önce `loadOptions.setLoadEffectsResource(true)` ayarlandığını kontrol edin.

## Sıkça Sorulan Sorular

**S: Tek bir görüntüye birden fazla degrade efekti uygulayabilir miyim?**  
E: Evet. Katmanın `BlendingOptions` nesnesini alın, `Effects` koleksiyonunda döngü yapın ve ihtiyacınız olan her degrade için yeni bir `GradientOverlayEffect` ekleyin.

**S: Gradient overlay'larla başka hangi efektleri birleştirebilirim?**  
E: Aspose.PSD gölgeler, parıltılar, kenar çerçeveleri ve daha fazlasını sağlar. Her efekt `Effects` dizisinde yer alır ve bağımsız olarak yapılandırılabilir.

**S: Efektler doğru render edilmiyorsa nasıl sorun gideririm?**  
E: `setLoadEffectsResource(true)` ile PSD'nin yüklendiğini doğrulayın, katman görünürlüğünü kontrol edin ve doğru efekt indeksini değiştirdiğinizden emin olun.

**S: Aspose.PSD for Java için bir deneme sürümü mevcut mu?**  
E: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) alabilirsiniz.

**S: Aspose.PSD for Java için lisansı nereden satın alabilirim?**  
E: Lisans bilgileri için [purchase page](https://purchase.aspose.com/buy) adresini ziyaret edin.

## Ek Sıkça Sorulan Sorular

**S: Degrade yönünü programlı olarak değiştirebilir miyim?**  
E: Evet. `GradientOverlayEffect.setAngle(float angle)` metodunu kullanarak derece cinsinden degrade açısını ayarlayabilirsiniz. Radyal degrade'lerde açı göz ardı edilir, ancak metod yine de çağrılmalıdır.

**S: Aspose.PSD radyal degrade'leri destekliyor mu?**  
E: Kesinlikle. `GradientOverlayEffect` özellikleri aracılığıyla degrade stilini `GradientStyle.Radial` olarak ayarlayın.

**S: PSD'yi diğer formatlara (ör. PNG) dönüştürdüğünüzde gradient overlay'lar korunur mu?**  
E: PSD'yi rasterleştirdiğinizde (ör. PNG olarak kaydettiğinizde), gradient overlay'ın görsel sonucu korunur, ancak efekt kendisi piksel verisinin bir parçası haline gelir.

**S: Bir katmandan gradient overlay'ı nasıl kaldırırım?**  
E: Katmanın `BlendingOptions` nesnesini alın, `Effects` koleksiyonunda `GradientOverlayEffect`'ı bulun ve `remove(effect)` ile kaldırın.

**S: Degrade değişikliklerini animasyon haline getirmek mümkün mü?**  
E: Aspose.PSD doğrudan animasyon işlemez, ancak farklı degrade parametreleriyle bir dizi PSD dosyası oluşturup, bunları başka bir kütüphane ile video veya GIF'e dönüştürebilirsiniz.

## Sonuç

Tebrikler! Aspose.PSD for Java kullanarak **radyal degrade java** efektlerini görüntülerinize nasıl ekleyeceğinizi öğrendiniz. Yukarıdaki adımları izleyerek, programlı olarak degrade kaplamalarını ekleyebilir, değiştirebilir ve kaydedebilirsiniz; bu da PSD varlıkları üzerinde tam yaratıcı kontrol sağlar. İhtiyacınız olan görsel etkiyi elde etmek için farklı renkler, karıştırma modları ve opaklık değerleriyle denemeler yapın.

---

**Son Güncelleme:** 2026-10-18  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## İlgili Öğreticiler

- [Java ile Aspose.PSD kullanarak Gradient Fill PSD Oluştur – Gradient Fill Katmanı Ekle](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Pattern Overlay PSD: Aspose.PSD for Java ile Efekt Ekle](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Java ile Aspose.PSD kullanarak Color Overlay Uygula ve Opaklığı Ayarla](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}