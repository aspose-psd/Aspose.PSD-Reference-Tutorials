---
date: 2026-02-14
description: Aspose.PSD for Java kullanarak iç gölge PSD eklemeyi öğrenin ve bu adım
  adım öğreticiyle PSD katman efektini programlı olarak uygulayın; ipuçları ve en
  iyi uygulamaları da içerir.
linktitle: Add Inner Shadow PSD Layer Effect in Java
second_title: Aspose.PSD Java API
title: Java'da PSD Katmanına İç Gölge Efekti Nasıl Eklenir
url: /tr/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da İç Gölge PSD Katman Efekti Nasıl Eklenir

## Giriş
If you need to **add inner shadow PSD** programmatically, you’ve landed in the right spot. In this guide, we’ll show you **how to add inner shadow** to any Photoshop document using Aspose.PSD for Java. Whether you’re building a batch‑processing tool, an automated design pipeline, or just experimenting with image effects, the steps below will give you a solid, production‑ready solution you can integrate into your Java applications.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java.  
- **Uygulama ne kadar sürer?** Temel bir kurulum için yaklaşık 10‑15 dakika.  
- **Photoshop yüklü olması gerekiyor mu?** Hayır, kütüphane Photoshop'tan bağımsız çalışır.  
- **Gölge rengini değiştirebilir miyim?** Evet – `setColor` metodu herhangi bir `Color` kabul eder.  
- **Üretim için lisans gerekli mi?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.

## “add inner shadow psd” nedir?
Adding an inner shadow to a PSD file means creating a subtle, inset shading effect that gives the impression of depth inside the layer. This effect is commonly used to make UI elements, icons, or text stand out without adding external glow.

## Neden Java ile PSD katman efekti uygulanır?
Using Java to **apply PSD layer effect** lets you automate repetitive design tasks, integrate image processing into backend services, and generate assets on the fly without manual Photoshop work. Aspose.PSD provides a clean, object‑oriented API that abstracts the PSD file format complexities.

## Ön Koşullar
1. **Java Development Kit (JDK 11 veya üzeri)** – [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin.  
2. **Aspose.PSD for Java** – en son JAR dosyasını [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) edinin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya NetBeans (herhangi biri yeterlidir).  
4. **Temel Java bilgisi** – sınıflar, nesneler ve istisna yönetimi konularında rahat olmalısınız.  
5. **Örnek PSD dosyası** – iç gölge efektini test etmek için en az bir katmana sahip basit bir PSD.

## Gerekli Paketleri İçe Aktarın
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
These imports give you access to the core classes needed for loading a PSD, manipulating layers, and configuring shadow effects.

## Java kullanarak bir PSD dosyasına iç gölge nasıl eklenir
Below is a step‑by‑step guide. Each step includes a short explanation followed by the exact code you need to copy.

### Adım 1: Kaynak ve hedef dizinleri tanımlayın
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
Replace the placeholder paths with the actual locations on your machine.

### Adım 2: Efekt kaynaklarıyla PSD dosyasını yükleyin
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
`setLoadEffectsResource(true)` ensures that any existing layer effects are loaded, allowing us to modify them.

### Adım 3: Hedef katmana erişin
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
Here we grab the **last layer** in the document, which is often the one you want to edit. Adjust the index if you need a different layer.

### Adım 4: İç gölge efektini yapılandırın
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
This block **applies the inner shadow** and customizes its appearance:
- **Renk** – yeşil olarak ayarlanır (istediğiniz herhangi bir `Color`a değiştirilebilir).  
- **Opaklık** – %50 şeffaflık (`255` içinde `128`).  
- **Mesafe, Boyut, Açı** – gölgenin kayma ve yayılmasını kontrol eder.  
- **Yayılım & Gürültü** – sanatsal varyasyon ekler.

### Adım 5: Değiştirilmiş PSD'yi kaydedin
```java
    image.save(destName, new PsdOptions(image));
```
The file `sample_out.psd` now contains the inner shadow effect.

### Adım 6: Kaynakları temizleyin
```java
} finally {
    image.dispose();
}
```
Disposing of the `image` object frees memory and prevents leaks, which is especially important when processing many files in a loop.

## Yaygın Kullanım Senaryoları
- **Otomatik marka oluşturma hatları** – yayınlamadan önce logolara tutarlı iç gölgeler ekleyin.  
- **Dinamik UI varlık üretimi** – web veya mobil uygulamalar için anlık olarak derinliğe sahip buton durumları oluşturun.  
- **Eski PSD kütüphanelerinin toplu işlenmesi** – Photoshop açmadan eski tasarımlara modern gölgelendirme ekleyin.

## Yaygın Sorunlar ve Çözümler
| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| **`ArrayIndexOutOfBoundsException` on `getEffects()[0]`** | Hedef katmanda henüz bir efekt ekli değil. | Dönüştürmeden önce `layer.getBlendingOptions().addEffect(new ShadowEffect())` ile yeni bir `IShadowEffect` ekleyin. |
| **Shadow color not changing** | Katmanda gölgeyi geçersiz kılan farklı bir efekt türü zaten var. | Doğru efekt indeksini düzenlediğinizden emin olun veya mevcut efektleri `layer.getBlendingOptions().clearEffects()` ile temizleyin. |
| **File not saved** | Hedef dizin mevcut değil veya yazma izniniz yok. | Dizini önceden oluşturun (`new File(outputDir).mkdirs();`) veya yazılabilir bir yol seçin. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD nedir?**  
C: Aspose.PSD, PSD dosyalarıyla çalışmak için bir Java kütüphanesidir; geliştiricilerin katman efektlerini, maskeleri ve görüntü özelliklerini programlı olarak manipüle etmelerini sağlar.

**S: Aspose.PSD kullanmak için Photoshop'a ihtiyacım var mı?**  
C: Hayır, Aspose.PSD kullanmak için Photoshop'a ihtiyacınız yoktur. Kütüphane, PSD dosyası manipülasyonu için bağımsız çalışır.

**S: Aynı katmana birden fazla efekt uygulayabilir miyim?**  
C: Kesinlikle! İç gölge efektine eriştiğimiz gibi, her bir efekt tipine erişerek birden fazla efekt uygulayabilirsiniz.

**S: Aspose.PSD ücretsiz mi?**  
C: Aspose.PSD ticari bir üründür; ancak Aspose üzerinden sunulan ücretsiz deneme sürümünü kullanabilirsiniz.

**S: Daha fazla belgeyi nerede bulabilirim?**  
C: Aspose.PSD için kapsamlı belgeleri [burada](https://reference.aspose.com/psd/java/) bulabilirsiniz.

## Sonuç
You’ve now seen how to **add inner shadow PSD** and **apply PSD layer effect** using Aspose.PSD for Java. This approach lets you automate sophisticated design tweaks, integrate them into backend services, or build batch processors for large image libraries. Feel free to experiment with other effect types—drop shadows, glows, bevels—to expand your toolkit.

---

**Son Güncelleme:** 2026-02-14  
**Test Edilen Versiyon:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}