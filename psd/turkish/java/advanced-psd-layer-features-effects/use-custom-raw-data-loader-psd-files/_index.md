---
date: 2026-02-22
description: Aspose.PSD for Java kullanarak PSD dosyalarında özel ham veri yükleme
  için IPartialRawDataLoader arayüzünün nasıl uygulanacağını öğrenin. Kurulum ve temizlik
  adımlarıyla adım adım rehber.
linktitle: Use Custom Raw Data Loader in PSD Files - Java
second_title: Aspose.PSD Java API
title: IPartialRawDataLoader'ı PSD Dosyaları için Uygula - Java
url: /tr/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/
weight: 29
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında Özel Raw Veri Yükleyicisini Kullanma - Java

## Giriş
Java'da PSD dosyalarıyla çalışmak özellikle raw veri işleme konusunda göz korkutucu görünebilir. Endişelenmeyin! Aspose.PSD for Java kullanarak PSD dosyalarından raw piksel verilerini kolayca manipüle edebilir ve **özel raw veri yükleyicisi** ile çıkarabilirsiniz. Bu öğreticide **IPartialRawDataLoader arayüzünü uygulamayı** öğrenecek ve piksel akışını tam istediğiniz gibi kontrol edebileceksiniz. Bu kılavuz, proje kurulumundan kaynakların temizlenmesine kadar tüm süreci adım adım gösterecek, böylece PSD katmanlarını güvenle işlemeye başlayabileceksiniz.

## Hızlı Yanıtlar
- **Özel bir raw veri yükleyicisi ne yapar?** PSD dosyası okunurken raw piksel baytlarını yakalamanıza ve işlemenize olanak tanır.  
- **Bu özelliği hangi kütüphane sağlar?** Aspose.PSD for Java, `IPartialRawDataLoader` arayüzünü içerir.  
- **Lisans gerekir mi?** Test için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Hangi Java sürümü gerekir?** Java 8 veya üzeri (JDK 11 önerilir).  
- **Yükleyiciyi birden fazla dosya için yeniden kullanabilir miyim?** Evet—yükleyicinizi bir kez örnekleyin ve görüntüler arasında yeniden kullanın.

## IPartialRawDataLoader arayüzünü nasıl uygularım
`IPartialRawDataLoader` arayüzünü uygulamak, raw‑data yükleme hattına bir kanca sağlar. Aşağıda, sözleşmeyi karşılayan ve kendi mantığınızı (örn. günlükleme, dönüşüm, akış) ekleyebileceğiniz bir sınıf oluşturacağız.

## Özel bir raw veri yükleyicisi nedir?
**custom raw data loader** bir kullanıcı‑tarafından uygulanan sınıftır ve `IPartialRawDataLoader` arayüzüne uyar. Raw piksel tamponlarını, dikdörtgen koordinatlarını ve isteğe bağlı yükleme seçeneklerini alır, piksel verisinin nasıl okunacağı, dönüştürüleceği veya saklanacağı üzerinde tam kontrol sağlar. Bu, özel görüntü analizi, anlık renk dönüşümü veya tüm görüntüyü belleğe yüklemeden büyük PSD'leri akış halinde işleme gibi senaryolar için özellikle yararlıdır.

## Aspose.PSD ile neden özel bir raw veri yükleyicisi kullanmalısınız?
- **Performans ayarı:** Sadece ihtiyacınız olan bölgeleri işleyerek bellek kullanımını azaltır.  
- **Özel iş akışları:** Piksel akışına doğrudan özel sıkıştırma, şifreleme veya analiz uygulayın.  
- **Entegrasyon esnekliği:** Mevcut görüntü hatlarına veya üçüncü‑taraf işleme kütüphanelerine bağlanın.

## Önkoşullar
Fun stuff'a dalmadan önce, Aspose.PSD ile Java’da başlamanız için ihtiyacınız olan her şeye sahip olduğunuzdan emin olalım. İşte ihtiyacınız olanlar:

1. **Java Temel Bilgisi** – Java programlamasına aşina olmak gereklidir.  
2. **Geliştirme Ortamı** – IntelliJ IDEA, Eclipse veya komut satırı derleme aracıyla çalışan herhangi bir editör.  
3. **Aspose.PSD Kütüphanesi** – Aspose.PSD for Java kütüphanesini [site](https://releases.aspose.com/psd/java/) üzerinden indirin. Ücretsiz deneme sürümü ya da satın alınmış lisans arasından seçim yapabilirsiniz.  
4. **Java Development Kit (JDK)** – Güncel bir JDK kurulu olduğundan emin olun. [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilir ya da OpenJDK kullanabilirsiniz.  
5. **PSD Dosyaları Bilgisi** – Katmanları ve piksel verilerini anlamak, yükleyiciden en iyi şekilde yararlanmanıza yardımcı olur.

Bu önkoşulları tamamladıktan sonra kodlamaya başlayabilirsiniz!

## Paketleri İçe Aktarma
Projede Aspose.PSD'yi etkili bir şekilde kullanabilmek için ilgili paketleri içe aktarmanız gerekir. Özel yükleyici örneği için ihtiyacınız olan minimal import aşağıdadır:

```java
import com.aspose.psd.*;
```

Bu paketler, PSD dosyalarıyla çalışmak ve **özel raw veri yükleyiciniz**i uygulamak için gerekli tüm sınıf ve arayüzleri sağlar.

## Adım 1: RawDataTester Sınıfını Oluşturun
İlk adım, `IPartialRawDataLoader` arayüzünü uygulayan bir sınıf tanımlamaktır. Bu sınıf, raw piksel verilerini işlemek için metodlar içerecektir.

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

`RawDataTester` sınıfının iki `process` aşırı yüklemesi vardır. Bu metodları piksel bilgilerini günlüğe kaydetmek, özel dönüşümler uygulamak veya veriyi başka bir servise akıtmak için özelleştirebilirsiniz.

## Adım 2: PSD Dosyası İçin Yolları Ayarlayın
Sonra, PSD dosyanızın bulunduğu kaynak dizinini belirtin.

```java
String sourceDir = "Your Source Directory";
String inFilePath = sourceDir + "CmykWithAlpha.psd";
```

`"Your Source Directory"` ifadesini PSD dosyanıza giden gerçek yol ile değiştirin. Dosya adının yüklemek istediğiniz PSD ile eşleştiğinden emin olun.

## Adım 3: PSD Dosyasını Yükleyin
Şimdi, `Image.load` metodunu kullanarak PSD dosyasını yükleyelim. Bu, görüntünün bellekte bir temsilini elde etmemizi sağlar.

```java
RasterImage image = (RasterImage)Image.load(inFilePath);
```

`RasterImage` tipine dönüştürme, daha sonra kullanacağımız `loadRawData` metodunu ortaya çıkardığı için gereklidir.

## Adım 4: RawDataSettings'i Başlatın
Görüntü yüklendikten sonra `RawDataSettings`i başlatabilirsiniz. Bu ayarlar, raw piksel verisinin nasıl işleneceğini belirler.

```java
try {
    RawDataSettings rawDataSettings = image.getRawDataSettings();
```

Bu adım, PSD dosyasındaki raw veriyle ilişkili ayarları çıkarır ve yükleme davranışını özelleştirmenize olanak tanır.

## Adım 5: Özel Yükleyici ile Raw Veriyi Yükleyin
Özel yükleyicinizi (`RawDataTester`) örnekleyin ve görüntüden raw veriyi yüklemek için kullanın.

```java
    RawDataTester loader = new RawDataTester();
    image.loadRawData(image.getBounds(), rawDataSettings, loader);
```

`loadRawData` çağrısı, piksel verisini `RawDataTester` uygulaması üzerinden akıtarak her bayt bloğu üzerinde tam kontrol sağlar.

## Adım 6: Kaynakları Temizleyin
Raw veriyi başarıyla yükledikten sonra, bellek sızıntılarını önlemek için kullanılan tüm kaynakları serbest bırakmak çok önemlidir.

```java
} finally {
    image.dispose();
}
```

`finally` bloğu, başarı ya da başarısızlık durumuna bakılmaksızın görüntü kaynaklarının doğru şekilde temizlenmesini garanti eder.

## Yaygın Tuzaklar ve Sorun Giderme
- **Yanlış yol:** Dosya yolunu iki kez kontrol edin; eksik bir eğik çizgi ya da yazım hatası `FileNotFoundException` hatasına yol açar.  
- **Tip dönüşüm hataları:** Yüklenen görüntünün gerçekten bir `RasterImage` olduğundan emin olun; aksi takdirde `ClassCastException` fırlatılır.  
- **Yükleyici çağrılmadı:** `RawDataTester` metodlarınızın doğru şekilde geçersiz kılındığını doğrulayın; aksi takdirde varsayılan yükleyici kullanılacaktır.  
- **Bellek kullanımı:** Çok büyük PSD'leri işlerken, bellek tüketimini düşük tutmak için tüm sınırlar yerine sadece belirli dikdörtgenleri yüklemeyi düşünün.

## Sıkça Sorulan Sorular
### Aspose.PSD for Java nedir?
Aspose.PSD for Java, geliştiricilerin PSD dosyalarını programatik olarak manipüle etmelerini sağlayan bir kütüphanedir; okuma, yazma ve PSD katmanlarını düzenleme gibi işlemleri içerir.

### Aspose.PSD'yi nasıl indiririm?
Aspose.PSD for Java'yi [sürüm sayfasından](https://releases.aspose.com/psd/java/) indirebilirsiniz.

### Aspose.PSD'yi ücretsiz kullanabilir miyim?
Evet, Aspose.PSD ücretsiz bir deneme sürümü sunar; bunu [buradan](https://releases.aspose.com/) erişebilirsiniz.

### Sorunla karşılaşırsam ya da desteğe ihtiyacım olursa?
Destek ve topluluk yardımı için [Aspose forumunu](https://forum.aspose.com/c/psd/34) ziyaret edebilirsiniz.

### Aspose.PSD için geçici bir lisans nasıl alabilirim?
Tüm özellikleri değerlendirmek için geçici bir lisans alabilirsiniz; bunun için [geçici lisans sayfasını](https://purchase.aspose.com/temporary-license/) ziyaret edin.

---

**Son Güncelleme:** 2026-02-22  
**Test Edilen:** Aspose.PSD for Java (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}