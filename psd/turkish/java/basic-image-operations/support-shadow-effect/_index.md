---
date: 2026-06-18
description: Java'da shadow color nasıl değiştirileceğini ve Aspose.PSD for Java kullanarak
  shadow effects nasıl özelleştirileceğini öğrenin. Bu adım adım shadow effect tutorial'ı
  izleyin.
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: Destek Shadow Effect
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Java'da Shadow Color Değiştir
url: /tr/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Java'da Gölge Rengini Değiştir

## Giriş

Grafiklerinize derinlik eklemek genellikle tasarımın atmosferine uyması için **gölge rengini değiştirmeyi** gerektirir. Aspose.PSD for Java ile drop‑shadow efektlerini kolayca ekleyebilir veya değiştirebilir, opaklığı kontrol edebilir ve diğer parametreleri ince ayar yapabilirsiniz—hepsi Java kodundan. Bu **gölge efekti öğreticisinde** bir PSD'yi yüklemeyi, mevcut gölgeyi okumayı, rengini, opaklığını, mesafesini özelleştirmeyi ve sonunda güncellenmiş dosyayı kaydetmeyi adım adım göstereceğiz. Bu kılavuz, **gölge rengini java ile değiştirme** ifadesinin yeniden üretilebilir bir şekilde nasıl yapılacağını tam olarak gösterir.

## Hızlı Yanıtlar
- **“change shadow color” ne anlama geliyor?** Bu, bir PSD katmanına uygulanan DropShadowEffect'in renk özelliğini günceller.  
- **Hangi kütüphane bunu destekliyor?** Aspose.PSD for Java, gölge efektleri için tam destek sağlar.  
- **Lisans gerekir mi?** Geliştirme için deneme sürümü çalışır; üretim için ticari bir lisans gereklidir.  
- **Gölge opaklığını ayarlayabilir miyim?** Evet – şeffaflığı (0‑255) tanımlamak için `setOpacity(byte)` kullanın.  
- **Kod Java 8+ ile uyumlu mu?** Kesinlikle, API Java 8 ve üzerini hedef alır.

## PSD dosyalarında “change shadow color” nedir?

Gölge rengini değiştirmek, bir katmanın arkasında görünen drop shadow'ın görsel tonunu değiştirir. Bu ayar, tasarımcılara farklı aydınlatma koşullarını simüle etme, gölgeleri marka renk paletleriyle hizalama ve kompozisyonlara sanatsal bir dokunuş ekleme imkanı verir. Tonu değiştirerek gölgelerin daha sıcak, daha soğuk ya da belirli bir renk şemasına tamamen uymasını sağlayabilir, genel görsel etkiyi artırabilirsiniz.

## Gölge efektlerini özelleştirmek için Aspose.PSD for Java neden kullanılmalı?

Aspose.PSD for Java, **100+ görüntü formatını** korur ve PSD dosyalarını **2 GB**'a kadar bellek içinde tüm belgeyi yüklemeden işleyebilir, kurumsal düzeyde performans sunar. Kütüphane, renk, opaklık, mesafe, açı, yayılma ve gürültü gibi her gölge özelliği üzerinde tam kontrol sağlar—Photoshop yüklü olmasına gerek yoktur. Windows, Linux ve macOS JVM'lerinde çalışır, bu da otomatik grafik boru hatları için en güvenilir seçeneği yapar.

## Önkoşullar

- Java programlama temelleri.  
- Aspose.PSD for Java yüklü. İndirmek için [buraya](https://releases.aspose.com/psd/java/) tıklayın.  

## Paketleri İçe Aktarma

Başlamadan önce, görüntüler ve gölge efektleriyle çalışabilmek için gerekli sınıfları içe aktarın:

`Color` sınıfı, API genelinde kullanılan bir renk değerini temsil eder.  
`Image` sınıfı, tüm görüntü nesneleri için temel tiptir.  
`PsdImage` sınıfı, PSD dosyalarına özgü işlevsellik sağlar.  
`PsdLoadOptions` sınıfı, PSD dosyalarını yüklerken efekt kaynaklarını etkinleştirme gibi seçenekleri belirtmenizi sağlar.  
`DropShadowEffect` sınıfı, bir PSD katmanına uygulanan drop‑shadow filtresini temsil eder ve tüm ayarlanabilir özelliklerine erişim sağlar.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: PSD Görüntüsünü Yükle

İlk olarak, efekt kaynaklarının yüklenmesini etkinleştirerek kaynak PSD'yi yükleyin:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Adım 2: Mevcut Drop Shadow Efektini Al

İstenen katmanda gölge efektini bulun (bu örnekte ikinci katman):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Adım 3: Varsayılan Ayarları Doğrula (İsteğe Bağlı)

Bu doğrulamaları çalıştırmak, değiştirmeden önce orijinal değerleri anlamanıza yardımcı olur:

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

### Adım 4: **Gölge Rengini Değiştir** ve Diğer Özellikleri Özelleştir

Şimdi gerçekten **gölge rengini** yeşile değiştiriyoruz, opaklığı, mesafeyi, boyutu ve diğer özellikleri ayarlıyoruz. Bu, Aspose.PSD'nin **gölge efektini özelleştir** yeteneklerini gösterir. `setOpacity(byte)` yöntemi, gölgenin opaklık seviyesini (0‑255) ayarlar.  

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### Adım 5: Değiştirilmiş Görüntüyü Kaydet

Son olarak, güncellenmiş PSD'yi `PsdImage`'in `save` yöntemiyle diske yazın:

```java
im.save(psdPathAfterChange);
```

## Yaygın Sorunlar ve İpuçları

- **Efektleri alırken NullPointerException** – `setLoadEffectsResource(true)` çağrıldığından emin olun; aksi takdirde efektler yüklenmez.  
- **Renk değişmiyor** – Bu örnekte doğru katman indeksini (`im.getLayers()[1]`) düzenlediğinizden emin olun.  
- **Opaklık değişmemiş gibi görünüyor** – Opaklığın bir byte (0‑255) olduğunu unutmayın. `(byte)` dönüşümü gereklidir.  

## Sonuç

Bu adımları izleyerek Aspose.PSD for Java kullanarak herhangi bir PSD dosyasında **gölge rengini değiştirebilir**, **gölge opaklığını ayarlayabilir** ve **gölge efektini tamamen özelleştirebilir**. Bu, manuel Photoshop çalışması olmadan programlı olarak daha zengin grafikler oluşturmanızı sağlar; otomatik tasarım boru hatları ve toplu işleme için mükemmeldir.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java profesyonel grafik tasarım projeleri için uygun mu?**  
C: Kesinlikle! Aspose.PSD for Java, profesyonel grafik tasarım görevleri için tasarlanmış güçlü bir kütüphanedir.

**S: Aspose.PSD for Java'yi ticari uygulamalarda kullanabilir miyim?**  
C: Evet, Aspose.PSD for Java ticari bir üründür. Bunu [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

**S: Ücretsiz deneme sürümü mevcut mu?**  
C: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) inceleyebilirsiniz.

**S: Ayrıntılı belgeleri nerede bulabilirim?**  
C: Kapsamlı belgeler için [buraya](https://reference.aspose.com/psd/java/) bakın.

**S: Aspose.PSD for Java için desteği nasıl alabilirim?**  
C: Herhangi bir destek sorusu için topluluk forumuna [buradan](https://forum.aspose.com/c/psd/34) katılın.

---

**Son Güncelleme:** 2026-06-18  
**Test Edilen:** Aspose.PSD for Java 24.10  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Java Görüntü İşleme - Aspose.PSD for Java ile Çalışma Zamanında Efekt Ekle](/psd/java/advanced-techniques/add-effects-runtime/)
- [PSD'yi PNG olarak kaydet ve Aspose.PSD for Java'da Rendering Drop Shadow uygula](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Java'da Görüntüyü Bulanıklaştır - Aspose.PSD – Blur Efekti Ekle](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}