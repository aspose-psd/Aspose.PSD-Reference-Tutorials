---
date: 2026-02-20
description: Aspose.PSD for Java kullanarak şeffaflık ve kırpma maskesi desteğini
  koruyarak PSD'yi PNG olarak dışa aktarmayı öğrenin. Bu adım adım rehber, PSD'yi
  hızlıca PNG olarak kaydetmenin yolunu gösterir.
linktitle: How to Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Clipping Mask ile PSD'yi PNG Olarak Dışa Aktarma – Aspose.PSD Java
url: /tr/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında Kesme Maskesini Aspose.PSD Java ile Destekleyin

## Giriş
**PSD'yi PNG olarak nasıl dışa aktaracağınızı** kesme maskesi bilgilerini koruyarak arıyorsanız, Aspose.PSD for Java bu süreci sorunsuz hâle getirir. Bu öğreticide, PSD dosyalarını programatik olarak nasıl işleyip kesme maskeleri uygulayacağınızı ve tam şeffaflık desteğiyle **PSD'yi PNG olarak kaydetmeyi** adım adım göstereceğiz. Sonunda, Java projelerinize doğrudan entegre edebileceğiniz yeniden kullanılabilir bir kod parçasına sahip olacaksınız.

## Hızlı Yanıtlar
- **Bu kütüphane ne yapar?** Photoshop PSD dosyalarını Java’da okur, düzenler ve dışa aktarır.  
- **Kesme maskelerini koruyabilir mi?** Evet – PNG’ye dışa aktarırken maskeler korunur.  
- **Kayıpsız dışa aktarım için hangi format kullanılır?** TruecolorWithAlpha ile PNG.  
- **Üretim için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz bir deneme sürümü mevcuttur.  
- **Hangi Java sürümü gerekir?** JDK 8 veya üzeri.

## PSD'yi Kesme Maskesiyle PNG Olarak Nasıl Dışa Aktarılır
Bir PSD dosyasını PNG’ye dışa aktarmak, katmanlı Photoshop belgesini düz bir raster görüntüye dönüştürürken şeffaflığı korur. Bu, web‑hazır bir görüntüye ihtiyacınız olduğunda, **şeffaf PNG tutmak** istediğinizde veya PSD’yi otomatik bir boru hattında toplu olarak PNG’ye dönüştürmek istediğinizde özellikle faydalıdır.

## Bu Görev İçin Neden Aspose.PSD Kullanmalı?
Aspose.PSD, kesme maskeleri, ayar katmanları ve karıştırma modları gibi karmaşık Photoshop özelliklerini Photoshop kurulumu olmadan yönetir. Otomatik iş akışları, toplu işleme veya tasarım varlıklarını sunucu‑tarafı uygulamalara entegre etmeniz gerektiğinde **PSD'yi PNG olarak güvenilir bir şekilde dışa aktarmanıza** olanak tanır.

## Ön Koşullar
Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – en az JDK 8. [Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) üzerinden indirin.  
2. **Aspose.PSD for Java Library** – en son JAR dosyasını [indirme sayfası](https://releases.aspose.com/psd/java/) üzerinden edinin. Ayrıca [ücretsiz deneme](https://releases.aspose.com/) sürümünü de deneyebilirsiniz.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Temel Java Bilgisi** – dosya I/O ve nesne‑yönelimli kavramlara aşina olmak işinizi kolaylaştırır.

## Export PSD as PNG – Step‑by‑Step Guide

### Adım 1: Belge Dizinini Tanımlayın
İlk olarak, programın kaynak PSD dosyanızın nerede olduğunu ve PNG dosyasının nereye yazılacağını bilmesini sağlayın.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini, PSD dosyalarını içeren makinenizdeki mutlak yol ile değiştirin.

### Adım 2: PSD Dosyasını Yükleyin
Ardından, PSD'yi katmanları ve maskeleriyle çalışabilmek için bir `PsdImage` nesnesine yükleyin.

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Adım 3: Dışa Aktarma Seçeneklerini Ayarlayın
PNG dışa aktarma ayarlarını yapılandırın. `TruecolorWithAlpha` kullanmak, kesme maskeleri tarafından oluşturulan şeffaf bölgelerin korunmasını sağlar, böylece **şeffaf PNG tutarsınız**.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### Adım 4: Görüntüyü Dışa Aktarın
Şimdi PSD'yi (kesme maskesiyle birlikte) bir PNG dosyası olarak kaydedin.

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

Ortaya çıkan PNG, web sayfalarında, mobil uygulamalarda veya raster görüntü kabul eden herhangi bir yerde doğrudan kullanılabilir.

### Adım 5: Kaynakları Temizleyin
İşiniz bittiğinde yerel belleği serbest bırakmak için `PsdImage` nesnesini her zaman dispose edin.

```java
im.dispose();
```

### PSD'yi PNG Olarak Tek Satırda Kaydetme
Daha kompakt bir sürüm tercih ediyorsanız, tüm süreci tek bir satıra indirebilirsiniz:

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*(Yukarıdaki genişletilmiş sürüm, açıklık ve hata ayıklama kolaylığı sağlamak amacıyla gösterilmiştir.)*

## Yaygın Sorunlar ve Çözümler
- **Şeffaflık Eksik:** `PngColorType.TruecolorWithAlpha` ayarlandığından emin olun; aksi takdirde PNG opak olur.  
- **Dosya Bulunamadı:** `dataDir` değişkeninin uygun yol ayırıcı (`/` veya `\\`) ile bittiğini kontrol edin.  
- **OutOfMemoryError:** Özellikle büyük dosyalar veya toplu işlemler yaparken `PsdImage` nesnesini hemen dispose edin.  
- **Toplu PSD → PNG Dönüştürme:** Birden çok dosya dönüştürürken adımları bir döngü içinde sarın ve performansı artırmak için `PngOptions` nesnesini yeniden kullanın.

## Sıkça Sorulan Sorular

**S: PSD dosyalarında kesme maskesi nedir?**  
C: Kesme maskesi, bir katmanın opaklığını kullanarak başka bir katmanın görünürlüğünü sınırlar; böylece katmanları kalıcı olarak değiştirmeden karmaşık kompozisyonlar oluşturabilirsiniz.

**S: Aspose.PSD ile PSD dosyalarını düzenleyebilir miyim?**  
C: Evet, katmanları düzenleyebilir, efektler uygulayabilir ve PNG veya JPEG gibi formatlara dışa aktarabilirsiniz.

**S: Aspose.PSD dokümantasyonunu nerede bulabilirim?**  
C: Aspose.PSD for Java için kapsamlı dokümantasyonu [burada](https://reference.aspose.com/psd/java/) bulabilirsiniz.

**S: Aspose.PSD için deneme sürümü mevcut mu?**  
C: Evet! Aspose.PSD'nin ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

**S: Aspose.PSD sorunları için destek nasıl alabilirim?**  
C: Her türlü soru ve sorun için Aspose forumundan [burada](https://forum.aspose.com/c/psd/34) destek alabilirsiniz.

## Sonuç
Artık Aspose.PSD for Java kullanarak kesme maskelerini koruyarak **PSD'yi PNG olarak nasıl dışa aktaracağınızı** öğrendiniz. Bu yaklaşım, tasarım boru hatlarını otomatikleştirmenize, Photoshop varlıklarını arka uç hizmetlerine entegre etmenize ve manuel dışa aktarma adımlarına ihtiyaç duymadan görsel bütünlüğü korumanıza olanak tanır. Katman birleştirme, renk ayarları ve toplu işleme gibi diğer Aspose.PSD özelliklerini keşfederek iş akışınızı daha da sadeleştirin.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}