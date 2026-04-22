---
date: 2026-02-07
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak kaydetmeyi, PNG'yi alfa
  kanalıyla dışa aktarmayı ve bir gölge katmanı eklemeyi öğrenin – eksiksiz, adım
  adım bir rehber.
linktitle: Apply Rendering Drop Shadow
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

Java'da Photoshop dosyalarıyla çalışıyorsanız, **PSD'yi PNG olarak kaydetmek** karşılaşacağınız en yaygın görevlerden biridir. Aspose.PSD ile sadece **PSD'yi PNG'ye dönüştürmek** değil, aynı zamanda **bir drop shadow katmanı ekleyerek** görüntüyü geliştirebilirsiniz. Bu öğreticide, bir PSD'yi yükleme, rendering drop shadow uygulama ve sonunda **PSD'yi PNG dosyası olarak kaydetme** sürecini adım adım göstereceğiz; böylece bu iş akışını kendi projelerinize güvenle entegre edebilirsiniz.

## Hızlı Yanıtlar
- **PSD'den PNG'ye dönüşümü hangi kütüphane yönetir?** Aspose.PSD for Java.  
- **Drop‑shadow uygulaması ne kadar sürer?** Temel bir örnek için yaklaşık 10‑15 dakika.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.  
- **Gölgeyi birden fazla katmana uygulayabilir miyim?** Evet—istediğiniz katmanlar üzerinde döngü oluşturmanız yeterli.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri.

## “PSD'yi PNG olarak kaydet” nedir ve neden önemlidir?

PSD'yi PNG olarak kaydetmek, şeffaflığı koruyan geniş çapta desteklenen kayıpsız bir görüntü oluşturur. Bu, Photoshop varlıklarını web'de, mobil uygulamalarda veya daha büyük bir görüntü işleme hattının parçası olarak göstermeniz gerektiğinde kritiktir. Aynı anda bir drop shadow eklemek, Photoshop açmadan da cilalı bir görsel etki üretmenizi sağlar.

## Bu iş akışı için neden Aspose.PSD kullanmalı?

* **Kod üzerinden tam kontrol** – Photoshop'u başlatmaya veya harici araçlara güvenmeye gerek yok.  
* **Katman efektlerini korur** – Drop shadow, glow ve diğer efektler, orijinal dosyada göründükleri şekilde tam olarak işlenir.  
* **Alfa kanallı PNG dışa aktarımı** – PNG çıktısı şeffaf arka planı korur, web veya UI kullanımına hazır hâle getirir.  
* **Çapraz platform** – Java 8+ destekleyen herhangi bir işletim sisteminde çalışır.

## Ön Koşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü.  
- **Aspose.PSD for Java** – En son JAR dosyasını [Aspose.PSD indirme sayfasından](https://releases.aspose.com/psd/java/) indirin.  
- **Bir PSD dosyası** – Dosyada drop shadow ile geliştirmek istediğiniz en az bir katman bulunmalı (ör. *Shadow.psd*).  

## Paketleri İçe Aktarma

İhtiyacımız olan sınıfları içe aktararak başlayalım. Bu, görüntü yükleme, katman efektleri ve PNG dışa aktarım seçeneklerine erişmemizi sağlar.

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
Giriş PSD'si ve render edilmiş drop shadow içerecek çıkış PNG'si için yolları belirtin.

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

> **Pro ipucu:** `setSpread()` veya `setNoise()` metodlarını ayarlayarak daha yumuşak ya da dokulu gölgeler oluşturabilirsiniz.

### Adım 6: PNG Olarak Kaydet – “PSD'yi PNG olarak kaydet” adımı  
Değiştirilmiş görüntüyü PNG olarak dışa aktarın, gölgenin doğru karışması için alfa kanalını koruyun.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Bu noktada **PSD'yi PNG'ye dönüştürdünüz**, **alfa kanallı PNG dışa aktardınız** ve tek bir iş akışında rendering drop shadow uyguladınız.

## Alfa Şeffaflığıyla PNG Dışa Aktarma

PNG çıktısının şeffaf arka planını koruması gerektiğinde—özellikle UI bindirmeleri veya web grafikleri için—kaydetme adımında gösterildiği gibi `PngColorType.TruecolorWithAlpha` kullanın. Bu, drop shadow'ın katı bir arka plan yerine şeffaf bir tuval üzerinde yer almasını garantiler.

## Java ile Drop Shadow Katmanı Ekleme

PSD'nizde gölge gerektiren birden fazla katman varsa, **Adım 4** ve **Adım 5**'i `im.getLayers()` üzerinde dönen bir döngü içinde tekrarlamanız yeterlidir. Her yineleme bir `DropShadowEffect` örneği oluşturup/ değiştirebilir; böylece katman başına opaklık, mesafe, boyut ve açı üzerinde ince ayar yapabilirsiniz.

## Java ile Photoshop PNG Dönüştürme – Yaygın Kullanım Senaryoları

* **Web varlık hatları** – Tasarımcıların sağladığı PSD'leri gömülü gölgelerle web‑hazır PNG'lere dönüştürün.  
* **Mobil uygulama kaynakları** – Manuel dışa aktarım yapmadan şeffaf PNG simgeleri anında üretin.  
* **Toplu işleme** – Sunucu tarafı bir görevde yüzlerce PSD dosyasının dönüşümünü otomatikleştirin.

## Yaygın Sorunlar ve Çözümler

| Sorun | Muhtemel Neden | Çözüm |
|-------|----------------|-------|
| **Gölge görünmüyor** | `Opacity` 0 olarak ayarlanmış veya katman gizli | `shadowEffect.getOpacity()` değerinin 0'dan büyük ve katmanın görünür olduğundan emin olun. |
| **PNG şeffaf değil (düz görünüyor)** | Yanlış `PngColorType` kullanılmış | Yukarıda gösterildiği gibi `PngColorType.TruecolorWithAlpha` kullanın. |
| **Yükleme sırasında istisna** | Efektler yüklenmemiş | `loadOptions.setLoadEffectsResource(true)` çağrısının yapıldığını doğrulayın. |
| **Yanlış katman indeksi** | PSD yapısı farklı | `im.getLayers()`'ı inceleyerek doğru indeksi seçin. |

## Sık Sorulan Sorular

**S: Drop shadow'ları birden fazla katmana aynı anda uygulayabilir miyim?**  
C: Evet. `im.getLayers()` üzerinden döngü kurup hedef katmanlar için bir `DropShadowEffect` ekleyebilir veya değiştirebilirsiniz.

**S: ‘Spread’ parametresi neyi kontrol eder?**  
C: `Spread`, gölgenin tam opaklıktan şeffaflığa ne kadar ani geçiş yaptığını belirler. Daha yüksek değer daha keskin bir kenar oluşturur.

**S: Aspose.PSD tüm Photoshop sürümleriyle uyumlu mu?**  
C: Aspose.PSD, Photoshop 3.0'dan en yeni sürüme kadar olan PSD dosyalarını destekler ve çoğu katman türü ile efekti işler.

**S: Lisans satın almadan kodu nasıl test edebilirim?**  
C: [Aspose.PSD indirme sayfasından](https://releases.aspose.com/psd/java/) ücretsiz deneme sürümünü indirip lisans anahtarı olmadan örnekleri çalıştırabilirsiniz.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
C: [Aspose.PSD forumunda](https://forum.aspose.com/c/psd/34) topluluk ve Aspose mühendislerinden destek alabilirsiniz.

## Sonuç

Artık **PSD'yi PNG olarak kaydet**, **alfa kanallı PNG dışa aktar**, **Photoshop PNG dosyalarını dönüştür** ve **Aspose.PSD for Java** kullanarak **drop shadow katmanı uygula** konularında bilgi sahibisiniz. Bu kombinasyon, Photoshop açmadan web, mobil veya masaüstü uygulamaları için yüksek kaliteli görüntü hazırlamayı otomatikleştirmenizi sağlar.

---

**Son Güncelleme:** 2026-02-07  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}