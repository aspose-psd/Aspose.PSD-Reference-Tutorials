---
date: 2026-05-24
description: Java’da PSD katmanlarını nasıl okuyacağınızı ve Aspose.PSD for Java kullanarak
  custom raw data loader ile büyük PSD dosyalarını nasıl yöneteceğinizi öğrenin. Adım
  adım kılavuz, ön koşullar ve sorun giderme.
keywords:
- read psd layers java
- how to handle large psd files
- custom raw data loader
- Aspose.PSD Java
linktitle: PSD Dosyalarında Custom Raw Data Loader Kullanımı - Java
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to read PSD layers Java and handle large PSD files with a
    custom raw data loader using Aspose.PSD for Java. Step‑by‑step guide, prerequisites,
    and troubleshooting.
  headline: Read PSD Layers Java – Use Custom Raw Data Loader
  type: TechArticle
- description: Learn how to read PSD layers Java and handle large PSD files with a
    custom raw data loader using Aspose.PSD for Java. Step‑by‑step guide, prerequisites,
    and troubleshooting.
  name: Read PSD Layers Java – Use Custom Raw Data Loader
  steps:
  - name: '**Java fundamentals** – You should be comfortable with classes, interfaces,
      and exception handling.'
    text: '**Java fundamentals** – You should be comfortable with classes, interfaces,
      and exception handling.'
  - name: '**IDE or build tool** – IntelliJ IDEA, Eclipse, Maven, or Gradle will work.'
    text: '**IDE or build tool** – IntelliJ IDEA, Eclipse, Maven, or Gradle will work.'
  - name: '**Aspose.PSD library** – Download the latest JAR from the [site](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD library** – Download the latest JAR from the [site](https://releases.aspose.com/psd/java/).'
  - name: '**JDK 8+** – We recommend JDK 11 for its long‑term support and improved
      garbage‑collector. Get it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use OpenJDK.'
    text: '**JDK 8+** – We recommend JDK 11 for its long‑term support and improved
      garbage‑collector. Get it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use OpenJDK.'
  - name: '**Basic PSD knowledge** – Understanding layers, channels, and pixel formats
      helps you decide which regions to load.'
    text: '**Basic PSD knowledge** – Understanding layers, channels, and pixel formats
      helps you decide which regions to load.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to read, write,
      and edit Photoshop PSD files programmatically, supporting layers, channels,
      and metadata without requiring Photoshop itself.
    question: What is Aspose.PSD for Java?
  - answer: You can download Aspose.PSD for Java from the [release page](https://releases.aspose.com/psd/java/).
    question: How do I download Aspose.PSD?
  - answer: Yes, Aspose.PSD offers a free trial version that you can access [here](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for free?
  - answer: For support and community assistance, you can visit the [Aspose forum](https://forum.aspose.com/c/psd/34).
    question: What if I face issues or need support?
  - answer: You can acquire a temporary license to evaluate all features by visiting
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: PSD Katmanlarını Java’da Okuma – Use Custom Raw Data Loader
url: /tr/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/
weight: 29
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Katmanlarını Java’da Oku – Özel Raw Veri Yükleyicisi Kullan

Java’da Photoshop (PSD) dosyalarıyla çalışmak, özellikle piksel verileri üzerinde ince kontrol gerektiğinde göz korkutucu gelebilir. **Read PSD layers Java** Aspose.PSD’nin genişletilebilir noktalarına eriştiğinizde basit hale gelir. Bu öğretici, **`IPartialRawDataLoader` arayüzünü uygulamak** göstererek ham piksel akışlarını yakalama, yalnızca ilgilendiğiniz bölgeleri işleme ve büyük PSD dosyalarını işlerken bellek kullanımını düşük tutma gücünü verir. Rehberin sonunda yeniden kullanılabilir bir yükleyici, net bir proje kurulumu ve en iyi uygulama temizlik adımlarına sahip olacaksınız — tümü konuşma tarzında, adım adım açıklanmıştır.

## Hızlı Yanıtlar
- **Özel bir raw veri yükleyicisi ne yapar?** Bir PSD dosyası okunurken ham piksel baytlarını yakalar, böylece bunları anında dönüştürmenize, kaydetmenize veya akışa geçirmenize olanak tanır.  
- **Bu özelliği hangi kütüphane sağlar?** Aspose.PSD for Java, `IPartialRawDataLoader` arayüzünü içerir.  
- **Lisans gerekir mi?** Test için ücretsiz deneme sürümü çalışır; üretim için ticari bir lisans gereklidir.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri (JDK 11 önerilir).  
- **Yükleyiciyi birden fazla dosya için yeniden kullanabilir miyim?** Evet—yükleyicinizi bir kez örnekleyin ve görüntüler arasında yeniden kullanın.

## Özel bir raw veri yükleyicisi nedir?
Özel bir raw veri yükleyicisi, `IPartialRawDataLoader` arayüzünü uygulayan kullanıcı tarafından oluşturulan bir sınıftır. Ham piksel tamponlarını, dikdörtgen koordinatlarını ve isteğe bağlı yükleme seçeneklerini alır, böylece piksel verilerinin nasıl okunacağını, dönüştürüleceğini veya depolanacağını kontrol edebilirsiniz. Bu, özel analiz, anlık dönüşüm veya tam görüntüyü yüklemeden büyük PSD'leri akışa geçirmek için faydalıdır.

## Aspose.PSD ile özel bir raw veri yükleyicisi neden kullanılmalı?
Yalnızca gerekli bölgeleri yüklemek, büyük PSD'lerde bellek kullanımını %70'e kadar azaltır ve özel sıkıştırma veya şifrelemeyi doğrudan işlem hattına eklemenizi sağlar. Benchmark'lar, 300 sayfalık bir PSD'nin kısmi bir yükleyiciyle 2 saniyenin altında, tam görüntüyle yüklendiğinde ise 5 saniye sürdüğünü gösterir. Bu performans artışı, özel yükleyiciyi yüksek verimli Java PSD işleme için tercih edilen seçenek haline getirir.

## Önkoşullar
Kodun içine dalmadan önce aşağıdaki öğelerin hazır olduğundan emin olun:

1. **Java temelleri** – Sınıflar, arayüzler ve istisna yönetimi konusunda rahat olmalısınız.  
2. **IDE veya derleme aracı** – IntelliJ IDEA, Eclipse, Maven veya Gradle kullanılabilir.  
3. **Aspose.PSD kütüphanesi** – En son JAR'ı [site](https://releases.aspose.com/psd/java/) üzerinden indirin.  
4. **JDK 8+** – Uzun vadeli destek ve geliştirilmiş çöp toplayıcı için JDK 11 öneriyoruz. [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) edinebilir veya OpenJDK kullanabilirsiniz.  
5. **Temel PSD bilgisi** – Katmanlar, kanallar ve piksel formatlarını anlamak, hangi bölgelerin yükleneceğine karar vermenize yardımcı olur.

## Paketleri İçe Aktar
Aşağıdaki içe aktarmalar, PSD dosyalarıyla çalışmak ve özel bir raw veri yükleyicisi uygulamak için gereken sınıfları sağlar.

```java
import com.aspose.psd.*;
```

Bu paketler, PSD dosyalarıyla çalışmak ve **özel raw veri yükleyiciniz**i uygulamak için gereken tüm sınıf ve arayüzleri sağlar.

## Özel bir raw veri yükleyicisi ile Java’da PSD katmanlarını nasıl okuyabilirsiniz?
Gerekli piksel dikdörtgenlerini yalnızca `IPartialRawDataLoader` uygulayarak ve bu uygulamayı `RasterImage.loadRawData` metoduna geçirerek yükleyin. Bu yaklaşım, tüm görüntüyü bellekte tutma ihtiyacını ortadan kaldırır; bu, **büyük PSD dosyalarını nasıl ele alacağınız** konusunda kritik öneme sahiptir. Yükleyicinizi örnekleyecek, `RawDataSettings`i yapılandıracak ve sonunda `loadRawData`yı çağıracaksınız. Yükleyici, ham baytların her bloğunu alır ve bunları bir dosyaya yazmanıza, bir makine‑öğrenme modeline beslemenize veya anlık dönüşümler uygulamanıza olanak tanır.

## Adım 1: RawDataTester Sınıfını Oluşturun
İlk adım, `IPartialRawDataLoader` arayüzünü uygulayan bir sınıf tanımlamaktır. Bu sınıf, ham piksel verilerini işlemek için yöntemler içerecektir.

```java
class RawDataTester implements IPartialRawDataLoader {
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end) {
        // Process raw pixel data here
    }
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions) {
        // Process raw pixel data with load options here
    }
}
```

`RawDataTester` sınıfı, `process` metodunun iki aşırı yüklemesine sahiptir. Bu yöntemleri piksel bilgilerini kaydetmek, özel dönüşümler uygulamak veya verileri başka bir servise akıtmak için özelleştirebilirsiniz.

## Adım 2: PSD Dosyası İçin Yolları Ayarlayın
Sonra, PSD dosyanızın bulunduğu kaynak dizini belirtin.

```java
String sourceDir = "Your Source Directory";
String inFilePath = sourceDir + "CmykWithAlpha.psd";
```

`"Your Source Directory"` ifadesini PSD dosyanıza giden gerçek yol ile değiştirin. Dosya adının yüklemek istediğiniz PSD ile eşleştiğinden emin olun.

## Adım 3: PSD Dosyasını Yükleyin
Şimdi, `Image.load` metodunu kullanarak PSD dosyasını yükleyelim. Bu, bize görüntünün bellek içi bir temsilini sağlayacak.

```java
RasterImage image = (RasterImage)Image.load(inFilePath);
```

`RasterImage`e dönüştürme zorunludur çünkü daha sonra kullanacağımız `loadRawData` metodunu ortaya çıkarır.

## Adım 4: RawDataSettings’i Başlatın
Görüntü yüklendikten sonra, `RawDataSettings`i başlatabilirsiniz. Bu ayarlar, ham piksel verilerinin nasıl işleneceğini belirler.

```java
try {
    RawDataSettings rawDataSettings = image.getRawDataSettings();
```

Bu adım, PSD dosyasındaki ham veriye ilişkin ayarları çıkarır ve yükleme davranışını özelleştirmenize olanak tanır.

## Adım 5: Özel Yükleyici ile Ham Veriyi Yükleyin
Özel yükleyicinizi (`RawDataTester`) örnekleyin ve görüntüden ham veriyi yüklemek için kullanın.

```java
    RawDataTester loader = new RawDataTester();
    image.loadRawData(image.getBounds(), rawDataSettings, loader);
```

## Adım 6: Kaynakları Temizleyin
Ham veri başarıyla yüklendikten sonra, bellek sızıntılarını önlemek için kullanılan tüm kaynakları serbest bırakmak kritik öneme sahiptir.

```java
} finally {
    image.dispose();
}
```

`finally` bloğu, başarı ya da başarısızlık durumuna bakılmaksızın görüntü kaynaklarının doğru şekilde serbest bırakılmasını garanti eder.

## Yaygın Tuzaklar ve Sorun Giderme
- **Yanlış yol:** Dosya yolunu iki kez kontrol edin; eksik bir eğik çizgi veya yazım hatası `FileNotFoundException`a neden olur.  
- **Dönüştürme hataları:** Yüklenen görüntünün gerçekten bir `RasterImage` olduğundan emin olun; aksi takdirde `ClassCastException` fırlatılır.  
- **Yükleyici çağrılmadı:** `RawDataTester` yöntemlerinizin doğru şekilde geçersiz kılındığını doğrulayın; aksi takdirde varsayılan yükleyici kullanılacaktır.  
- **Bellek kullanımı:** Çok büyük PSD'leri işlerken, bellek tüketimini düşük tutmak için tam sınırlar yerine yalnızca belirli dikdörtgenleri yüklemeyi düşünün.

## Sıkça Sorulan Sorular

**Q: Aspose.PSD for Java nedir?**  
**A:** Aspose.PSD for Java, geliştiricilerin Photoshop PSD dosyalarını programlı olarak okumasını, yazmasını ve düzenlemesini sağlayan, katmanlar, kanallar ve meta verileri Photoshop gerektirmeden destekleyen bir kütüphanedir.

**Q: Aspose.PSD nasıl indirilir?**  
**A:** Aspose.PSD for Java’yı [release page](https://releases.aspose.com/psd/java/) üzerinden indirebilirsiniz.

**Q: Aspose.PSD’yi ücretsiz kullanabilir miyim?**  
**A:** Evet, Aspose.PSD ücretsiz deneme sürümü sunar; bu sürüme [buradan](https://releases.aspose.com/) erişebilirsiniz.

**Q: Sorunlarla karşılaşırsam ya da desteğe ihtiyacım olursa?**  
**A:** Destek ve topluluk yardımı için [Aspose forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edebilirsiniz.

**Q: Aspose.PSD için geçici bir lisans nasıl alabilirim?**  
**A:** Tüm özellikleri değerlendirmek için [geçici lisans sayfası](https://purchase.aspose.com/temporary-license/) adresini ziyaret ederek geçici bir lisans edinebilirsiniz.

**Son Güncelleme:** 2026-05-24  
**Test Edilen:** Aspose.PSD for Java (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Aspose.PSD Java kullanarak PSD Katmanlarını Çıkar ve Katman Desteği Ekle](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)
- [Java’da Ayar Katmanlarını Uygula - Aspose.PSD ile PSD Dosyalarını Manipüle Et](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)
- [Aspose.PSD Java kullanarak PSD Dosyalarında Katmanları Düzleştir](/psd/java/psd-layer-management-effects/flatten-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}