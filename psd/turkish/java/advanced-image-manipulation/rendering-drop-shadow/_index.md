---
date: 2025-12-05
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak kaydetmeyi, PSD'yi PNG'ye
  dönüştürmeyi ve bir gölge katmanı uygulamayı öğrenin – eksiksiz, adım adım bir rehber.
language: tr
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: PSD'yi PNG olarak kaydedin ve Aspose.PSD for Java'da Rendering Drop Shadow
  uygulayın
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG Olarak Kaydet ve Aspose.PSD for Java'da Rendering Drop Shadow Uygula

## Giriş

Java'da Photoshop dosalarıyla çalışıyorsanız, **PSD'yi PNG olarak kaydetmek** karşılaşacağınız en yaygın görevlerden biridir. Aspose.PSD ile sadece **PSD'yi PNG'ye dönüştürmek** değil, aynı zamanda **drop shadow (gölge) katmanı ekleyerek** görüntüyü geliştirebilirsiniz. Bu öğreticide tüm süreci adım adım inceleyeceğiz—PSD'yi yükleme, rendering drop shadow uygulama ve sonunda **PSD'yi PNG dosyası olarak kaydetme**—böylece bu iş akışını kendi projelerinize güvenle entegre edebilirsiniz.

## Hızlı Yanıtlar
- **PSD'den PNG'ye dönüşümü hangi kütüphane yapar?** Aspose.PSD for Java.  
- **Drop‑shadow uygulaması ne kadar sürer?** Temel bir örnek için yaklaşık 10‑15 dakika.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme yeterlidir; üretim için lisans gerekir.  
- **Gölgeyi birden fazla katmana uygulayabilir miyim?** Evet—istediğiniz katmanlar üzerinde döngü kurabilirsiniz.  
- **Hangi Java sürümü gereklidir?** Java 8 ve üzeri.

## “PSD'yi PNG olarak kaydet” nedir ve neden önemlidir?

PSD'yi PNG olarak kaydetmek, şeffaflığı koruyan, kayıpsız ve yaygın olarak desteklenen bir görüntü oluşturur. Bu, Photoshop varlıklarını web'de, mobil uygulamalarda veya daha büyük bir görüntü işleme hattının parçası olarak göstermeniz gerektiğinde kritiktir. Aynı anda drop shadow eklemek, Photoshop açmadan da şık bir görsel etki üretmenizi sağlar.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm.  
- **Aspose.PSD for Java** – En son JAR dosyasını [Aspose.PSD indirme sayfasından](https://releases.aspose.com/psd/java/) indirin.  
- **Bir PSD dosyası** – En az bir katmanı drop shadow ile geliştirmek istediğiniz bir dosya (ör. *Shadow.psd*).  

## Paketleri İçe Aktar

İlk olarak ihtiyaç duyacağımız sınıfları içe aktaralım. Bu, görüntü yükleme, katman efektleri ve PNG dışa aktarma seçeneklerine erişmemizi sağlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: Belge Dizinini Tanımla  
Programın kaynak PSD dosyanızın nerede olduğunu bilmesini sağlayın.

```java
String dataDir = "Your Document Directory";
```

### Adım 2: PSD ve PNG Dosya Yollarını Ayarla  
Hem giriş PSD'sini hem de render edilmiş drop shadow içerecek çıkış PNG'sini belirtin.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Adım 3: Efektlerle PSD Dosyasını Yükle  
Drop‑shadow efektini manipüle edebilmek için efekt kaynaklarının yüklenmesini etkinleştirin.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Adım 4: Drop Shadow Efektine Eriş  
İkinci katmandan (indeks 1) ilk drop‑shadow efektini alın. Burada parametreleri doğrulayacak veya değiştireceksiniz.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Adım 5: Shadow Efekt Özelliklerini Doğrula  
Kaydetmeden önce efektin özelliklerinin beklentilerinize uygun olduğundan emin olun. Farklı bir görünüm elde etmek için bu değerleri de ayarlayabilirsiniz.

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

> **İpucu:** Daha yumuşak veya dokulu gölgeler oluşturmak için `setSpread()` veya `setNoise()` metodlarını ayarlayın.

### Adım 6: PNG Olarak Kaydet – “PSD'yi PNG olarak kaydet” adımı  
Değiştirilmiş görüntüyü PNG'ye dışa aktarın, gölgenin doğru karışması için alfa kanalını koruyun.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Bu noktada **PSD'yi PNG'ye dönüştürmüş** ve tek bir iş akışında rendering drop shadow uygulamış oldunuz.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Muhtemel Neden | Çözüm |
|-------|----------------|------|
| **Gölge görünmüyor** | `Opacity` 0 olarak ayarlanmış veya katman gizli | `shadowEffect.getOpacity()` değerinin 0'dan büyük olduğundan ve katman görünürlüğünün açık olduğundan emin olun. |
| **PNG düz görünüyor (şeffaflık yok)** | Yanlış `PngColorType` kullanıldı | Örnekte gösterildiği gibi `PngColorType.TruecolorWithAlpha` kullanın. |
| **Yükleme sırasında istisna** | Efektler yüklenmedi | `loadOptions.setLoadEffectsResource(true)` çağrısının yapıldığını doğrulayın. |
| **Yanlış katman indeksi** | PSD yapısı farklı | `im.getLayers()`'ı inceleyin ve doğru indeksi seçin. |

## Sık Sorulan Sorular

**S: Drop shadow'ı birden fazla katmana aynı anda uygulayabilir miyim?**  
C: Evet. `im.getLayers()` üzerinden döngü kurarak hedef katmanlar için bir `DropShadowEffect` ekleyebilir veya değiştirebilirsiniz.

**S: ‘Spread’ parametresi neyi kontrol eder?**  
C: `Spread`, gölgenin tam opaklıktan şeffaflığa ne kadar ani geçiş yaptığını belirler. Yüksek değer daha keskin bir kenar oluşturur.

**S: Aspose.PSD tüm Photoshop sürümleriyle uyumlu mu?**  
C: Aspose.PSD, Photoshop 3.0'dan en yeni sürüme kadar PSD dosyalarını destekler, çoğu katman tipi ve efekti işleyebilir.

**S: Lisans satın almadan kodu nasıl test edebilirim?**  
C: [Aspose.PSD indirme sayfasından](https://releases.aspose.com/psd/java/) ücretsiz deneme sürümünü indirip lisans anahtarı olmadan örnekleri çalıştırabilirsiniz.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
C: Sorununuzu [Aspose.PSD forumunda](https://forum.aspose.com/c/psd/34) paylaşabilirsiniz; topluluk ve Aspose mühendisleri yardımcı olacaktır.

## Sonuç

Artık **PSD'yi PNG olarak kaydet**, **PSD'yi PNG'ye dönüştür** ve **drop shadow katmanı uygula** işlemlerini Aspose.PSD for Java ile nasıl yapacağınızı biliyorsunuz. Bu kombinasyon, Photoshop açmadan web, mobil veya masaüstü uygulamaları için yüksek kaliteli görüntü hazırlamayı otomatikleştirmenizi sağlar.

---

**Son Güncelleme:** 2025-12-05  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}