---
date: 2026-04-22
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak kaydetmeyi, PNG'yi alfa
  kanalıyla dışa aktarmayı ve bir gölge katmanı eklemeyi öğrenin – eksiksiz, adım
  adım bir rehber.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- preserve png transparency
linktitle: Gölgeyi Uygula
second_title: Aspose.PSD Java API
title: PSD'yi PNG olarak kaydedin ve Aspose.PSD for Java'da Rendering Drop Shadow
  uygulayın
url: /tr/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG Olarak Kaydet ve Aspose.PSD for Java'da Rendering Drop Shadow Uygula

## Giriş

Java'da Photoshop dosyalarıyla çalışıyorsanız, **PSD'yi PNG olarak kaydetmek** karşılaşacağınız en yaygın görevlerden biridir. Birçok projede, varlıkları web veya mobil uygulamalara gönderirken şeffaflığı ve görsel efektleri korumak için **psd'yi png olarak kaydetmeniz** gerekir. Aspose.PSD ile sadece **PSD'yi PNG'ye dönüştürmek** değil, aynı zamanda **bir drop shadow katmanı ekleyerek** görüntüyü iyileştirebilirsiniz. Bu öğreticide, bir PSD'yi yükleme, rendering drop shadow uygulama ve sonunda **PSD'yi PNG dosyası olarak kaydetme** sürecini adım adım göstereceğiz; böylece bu iş akışını kendi projelerinize güvenle entegre edebilirsiniz.

## Hızlı Yanıtlar

- **PSD'den PNG'ye dönüşümü hangi kütüphane yönetir?** Aspose.PSD for Java.  
- **Drop‑shadow uygulaması ne kadar sürer?** Temel bir örnek için yaklaşık 10‑15 dakika.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için lisans gerekir.  
- **Gölgeyi birden fazla katmana uygulayabilir miyim?** Evet—istediğiniz katmanlar üzerinde döngü yapın, bu aynı zamanda toplu psd to png dönüşümü yapmanızı sağlar.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri.

## “PSD'yi PNG Olarak Kaydet” Nedir ve Neden Önemlidir?

**PSD'yi PNG olarak kaydetmek**, şeffaflığı koruyan, yaygın olarak desteklenen kayıpsız bir görüntü oluşturur. Bu, Photoshop varlıklarını web'de, mobil uygulamalarda veya daha büyük bir görüntü‑işleme hattının parçası olarak göstermeniz gerektiğinde çok önemlidir. Aynı anda bir drop shadow eklemek, Photoshop açmadan cilalı bir görsel efekt üretmenizi sağlar.

## Bu İş Akışı İçin Neden Aspose.PSD Kullanmalı?

* **Koddan tam kontrol** – Photoshop'u başlatmaya veya harici araçlara güvenmeye gerek yok.  
* **Katman efektlerini korur** – Drop shadow'lar, parlamalar ve diğer efektler, orijinal dosyada göründükleri gibi işlenir.  
* **Alfa kanallı PNG dışa aktar** – PNG çıktısı şeffaf arka planı korur, UI veya web kullanımı için **PNG şeffaflığını korumanızı** sağlar.  
* **Çapraz platform** – Java 8+ destekleyen herhangi bir işletim sisteminde çalışır.

## Önkoşullar

İlerlemeye başlamadan önce şunların olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü.  
- **Aspose.PSD for Java** – En son JAR dosyasını [Aspose.PSD download page](https://releases.aspose.com/psd/java/) adresinden indirin.  
- **Bir PSD dosyası** – Dosya, drop shadow ile geliştirmek istediğiniz en az bir katman içermelidir (ör. *Shadow.psd*).

## Paketleri İçe Aktar

İlk olarak, ihtiyacımız olan sınıfları içe aktarın. Bu, görüntü yükleme, katman efektleri ve PNG dışa aktarım seçeneklerine erişim sağlar.

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

### Adım 1: Belge Dizini Tanımla  
Programın kaynak PSD dosyanızın nerede olduğunu bilmesini sağlayın.

```java
String dataDir = "Your Document Directory";
```

### Adım 2: PSD ve PNG Dosya Yollarını Ayarla  
Render edilmiş drop shadow içerecek giriş PSD ve çıkış PNG dosyalarını belirtin.

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
İkinci katmandan (indeks 1) ilk drop‑shadow efektini alın. Burada parametreleri doğrulayacak veya değiştireceğiz.

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

> **Pro ipucu:** Daha yumuşak veya daha dokulu gölgeler oluşturmak için `setSpread()` veya `setNoise()` yöntemlerini ayarlayın.

### Adım 6: PNG Olarak Kaydet – “PSD'yi PNG Olarak Kaydet” adımı  
Değiştirilmiş görüntüyü PNG olarak dışa aktarın, alfa kanalını koruyarak gölgenin doğru şekilde karışmasını sağlayın.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Bu noktada **PSD'yi PNG'ye dönüştürdünüz**, **PNG'yi alfa ile dışa aktardınız** ve tek bir iş akışında rendering drop shadow uyguladınız.

## Alfa Şeffaflığıyla PNG Dışa Aktar

PNG çıktısının şeffaf arka planını koruması gerektiğinde—özellikle UI katmanları veya web grafikleri için—kaydetme adımında gösterildiği gibi `PngColorType.TruecolorWithAlpha` kullandığınızdan emin olun. Bu, drop shadow'un katı bir arka plan yerine şeffaf bir tuval üzerinde olmasını sağlar ve **PNG şeffaflığını korumanıza** yardımcı olur.

## Java Kullanarak Drop Shadow Katmanı Ekle

PSD'niz birden fazla gölge gerektiren katman içeriyorsa, `im.getLayers()` üzerinde dönen bir döngü içinde **Adım 4** ve **Adım 5**'i tekrarlamanız yeterlidir. Her yineleme bir `DropShadowEffect` örneği oluşturabilir veya değiştirebilir, katman başına opaklık, mesafe, boyut ve açı üzerinde ayrıntılı kontrol sağlar. Bu yaklaşım aynı zamanda her dosyanın aynı gölge işlemini almasını sağlayan bir **batch psd to png** dönüşümünü de mümkün kılar.

## PSD'yi PNG Olarak Kaydetmek İçin Yaygın Kullanım Senaryoları

* **Web varlık hatları** – Tasarımcıların sağladığı PSD'leri yerleşik gölgelerle web‑hazır PNG'lere dönüştürün.  
* **Mobil uygulama kaynakları** – Manuel dışa aktarmaya gerek kalmadan şeffaf PNG simgeleri anında oluşturun.  
* **Toplu işleme** – Sunucu tarafı bir işte yüzlerce PSD dosyasının dönüşümünü otomatikleştirin, her PNG'nin alfa kanalını ve görsel efektlerini koruduğundan emin olun.

## Yaygın Sorunlar ve Çözümler

| Sorun | Muhtemel Neden | Çözüm |
|-------|----------------|------|
| **Gölge görünmüyor** | `Opacity` 0 olarak ayarlanmış veya katman gizli | `shadowEffect.getOpacity()` > 0 ve katman görünürlüğünü doğrulayın. |
| **PNG düz görünüyor (şeffaflık yok)** | Yanlış `PngColorType` kullanılmış | Gösterildiği gibi `PngColorType.TruecolorWithAlpha` kullanın. |
| **Yükleme sırasında istisna** | Efektler yüklenmemiş | `loadOptions.setLoadEffectsResource(true)` çağrıldığından emin olun. |
| **Yanlış katman indeksi** | PSD yapısı farklı | `im.getLayers()`'ı inceleyin ve doğru indeksi seçin. |

## Sıkça Sorulan Sorular

**S: Drop shadow'ları birden fazla katmana aynı anda uygulayabilir miyim?**  
C: Evet. `im.getLayers()` üzerinde döngü yaparak her hedef katmana bir `DropShadowEffect` ekleyebilir veya değiştirebilirsiniz; bu aynı zamanda bir batch psd to png dönüşümü yapmanızı sağlar.

**S: ‘Spread’ parametresi neyi kontrol eder?**  
C: `Spread`, gölgenin tam opaklıktan şeffaflığa ne kadar ani geçiş yaptığını belirler. Daha yüksek bir değer daha keskin bir kenar oluşturur.

**S: Aspose.PSD tüm Photoshop sürümleriyle uyumlu mu?**  
C: Aspose.PSD, Photoshop 3.0'dan en yeni sürüme kadar PSD dosyalarını destekler ve çoğu katman türü ve efekti işler.

**S: Lisans satın almadan kodu nasıl test edebilirim?**  
C: Ücretsiz deneme sürümünü [Aspose.PSD download page](https://releases.aspose.com/psd/java/) adresinden indirin ve lisans anahtarı olmadan örneği çalıştırın.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
C: Sorunuzu [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) adresine gönderin; topluluk ve Aspose mühendisleri yardımcı olacaktır.

## Sonuç

Artık Aspose.PSD for Java kullanarak **psd'yi png olarak kaydetmeyi**, **PNG'yi alfa ile dışa aktarmayı**, **PSD'yi PNG'ye dönüştürmeyi** ve **drop shadow katmanı uygulamayı** biliyorsunuz. Bu kombinasyon, Photoshop'u hiç açmadan web, mobil veya masaüstü uygulamaları için yüksek kaliteli görüntü hazırlamayı otomatikleştirmenizi sağlar.

---

**Son Güncelleme:** 2026-04-22  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}