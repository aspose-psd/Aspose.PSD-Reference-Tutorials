---
date: 2025-12-17
description: Aspose.PSD for Java kullanarak kırpma maskesi desteğiyle PSD'yi PNG olarak
  nasıl dışa aktaracağınızı öğrenin. PSD'yi hızlıca PNG'ye kaydetmek için adım adım
  rehberimizi izleyin.
linktitle: Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: PSD'yi Kesme Maskesiyle PNG Olarak Dışa Aktar – Aspose.PSD Java
url: /tr/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java ile PSD Dosyalarında Kırpma Maskesini Destekleme

## Introduction
Eğer **PSD'yi PNG olarak dışa aktarmak** ve kırpma maskesi bilgilerini korumak istiyorsanız, Aspose.PSD for Java bu süreci sorunsuz hâle getirir. Bu öğreticide, PSD dosyalarını programatik olarak nasıl işleyeceğinizi, kırpma maskelerini nasıl uygulayacağınızı ve **PSD'yi PNG olarak kaydetmeyi** tam şeffaflık desteğiyle adım adım göstereceğiz. Sonunda, Java projelerinize doğrudan entegre edebileceğiniz yeniden kullanılabilir bir kod parçacığına sahip olacaksınız.

## Quick Answers
- **Kütüphane ne işe yarar?** Photoshop PSD dosyalarını Java’da okur, düzenler ve dışa aktarır.  
- **Kırpma maskelerini koruyabilir mi?** Evet – maskeler PNG’ye dışa aktarılırken korunur.  
- **Kayıpsız dışa aktarım için hangi format kullanılır?** TruecolorWithAlpha ile PNG.  
- **Üretim için lisans gerekiyor mu?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **Hangi Java sürümü gereklidir?** JDK 8 veya üzeri.

## What is “export psd as png”?
PSD dosyasını PNG’ye dışa aktarmak, katmanlı Photoshop belgesini şeffaflığı koruyan düz bir raster görüntüye dönüştürür. Bu, web‑hazır bir görsele ihtiyacınız olduğunda veya Photoshop uygulaması olmadan tasarımları paylaşmak istediğinizde özellikle faydalıdır.

## Why use Aspose.PSD for this task?
Aspose.PSD, kırpma maskeleri, ayar katmanları ve karıştırma modları gibi karmaşık Photoshop özelliklerini Photoshop yüklü olmadan yönetir. Otomatik iş akışları, toplu işleme veya tasarım varlıklarını sunucu‑tarafı uygulamalara entegre etmek için idealdir.

## Prerequisites
Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – en az JDK 8. İndirmek için [Oracle web sitesini](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) ziyaret edin.  
2. **Aspose.PSD for Java Library** – en yeni JAR dosyasını [indirme sayfasından](https://releases.aspose.com/psd/java/) alın. Ayrıca [ücretsiz deneme](https://releases.aspose.com/) sürümünü de deneyebilirsiniz.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Basic Java Knowledge** – dosya I/O ve nesne‑yönelimli kavramlara aşina olmak faydalı olacaktır.

## Export PSD as PNG – Step‑by‑Step Guide

### Step 1: Define Your Document Directory
İlk olarak, programın kaynak PSD dosyanızın nerede bulunduğunu ve PNG’nin nereye yazılacağını bilmesini sağlayın.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini, PSD dosyalarınızı içeren makinenizdeki mutlak yol ile değiştirin.

### Step 2: Load the PSD File
Ardından, PSD dosyasını bir `PsdImage` nesnesine yükleyin; böylece katmanları ve maskeleri üzerinde çalışabilirsiniz.

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Step 3: Setup Export Options
PNG dışa aktarım ayarlarını yapılandırın. `TruecolorWithAlpha` kullanmak, kırpma maskeleri tarafından oluşturulan şeffaf bölgelerin korunmasını sağlar.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### Step 4: Export the Image
Şimdi PSD’yi (kırpma maskesiyle birlikte) bir PNG dosyası olarak kaydedin.

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

Ortaya çıkan PNG, web sayfalarında, mobil uygulamalarda veya raster görüntü kabul eden herhangi bir yerde doğrudan kullanılabilir.

### Step 5: Clean Up Resources
İşiniz bittiğinde `PsdImage` nesnesini her zaman serbest bırakın; böylece yerel bellek temizlenir.

```java
im.dispose();
```

### How to Save PSD to PNG in One Line
Daha kompakt bir versiyon tercih ediyorsanız, tüm süreci tek satıra indirebilirsiniz:

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*(Yukarıdaki genişletilmiş sürüm, açıklık ve hata ayıklama kolaylığı sağlamak amacıyla gösterilmiştir.)*

## Common Issues and Solutions
- **Missing Transparency:** `PngColorType.TruecolorWithAlpha` ayarının yapıldığından emin olun; aksi takdirde PNG opak olur.  
- **File Not Found:** `dataDir` değişkeninin uygun yol ayırıcı (`/` veya `\\`) ile bittiğini kontrol edin.  
- **OutOfMemoryError:** Özellikle büyük dosyalar veya toplu işlemler yaparken `PsdImage` nesnesini zamanında serbest bırakın.

## Frequently Asked Questions

**S: PSD dosyalarında kırpma maskesi nedir?**  
C: Kırpma maskesi, bir katmanın opaklığını kullanarak başka bir katmanın görünürlüğünü sınırlar; böylece katmanları kalıcı olarak değiştirmeden karmaşık kompozisyonlar oluşturulabilir.

**S: Aspose.PSD ile PSD dosyalarını düzenleyebilir miyim?**  
C: Evet, katmanları düzenleyebilir, efektler uygulayabilir ve PNG ya da JPEG gibi formatlara dışa aktarabilirsiniz.

**S: Aspose.PSD dokümantasyonunu nereden bulabilirim?**  
C: Aspose.PSD for Java için kapsamlı dokümantasyonu [burada](https://reference.aspose.com/psd/java/) bulabilirsiniz.

**S: Aspose.PSD için deneme sürümü mevcut mu?**  
C: Evet! Aspose.PSD'nin ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

**S: Aspose.PSD ile ilgili sorunlarda nasıl destek alabilirim?**  
C: Herhangi bir soru ya da sorun için Aspose forumundan [burada](https://forum.aspose.com/c/psd/34) destek alabilirsiniz.

## Conclusion
Artık Aspose.PSD for Java kullanarak **PSD'yi PNG olarak dışa aktarmayı** ve kırpma maskelerini korumayı öğrendiniz. Bu yöntem, tasarım hatlarını otomatikleştirmenize, Photoshop varlıklarını arka uç hizmetlerine entegre etmenize ve manuel dışa aktarım adımlarına ihtiyaç duymadan görsel bütünlüğü korumanıza olanak tanır. Katman birleştirme, renk ayarları ve toplu işleme gibi diğer Aspose.PSD özelliklerini keşfederek iş akışınızı daha da verimli hâle getirebilirsiniz.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}