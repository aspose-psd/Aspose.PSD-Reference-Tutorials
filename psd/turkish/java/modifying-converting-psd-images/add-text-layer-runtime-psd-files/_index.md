---
date: 2026-03-07
description: Java ve Aspose.PSD kullanarak çalışma zamanında PSD dosyalarına metin
  eklemeyi öğrenin. Bu adım adım rehberi izleyerek bir PSD'de hızlıca metin katmanı
  oluşturun.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Java Kullanarak Çalışma Zamanında PSD Dosyalarına Metin Ekle
url: /tr/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Kullanarak Çalışma Zamanında PSD Dosyalarına Metin Ekleme

## Giriş
Photoshop belgesini manuel olarak düzenlediyseniz, katmanların ne kadar güçlü olduğunu bilirsiniz. Java uygulamanızdan **PSD dosyalarına metin ekleyebilir** misiniz? Aspose.PSD for Java kütüphanesi ile çalışma zamanında bir PSD'ye metin katmanı oluşturabilir, toplu işleme, dinamik grafik oluşturma ve otomatik marka oluşturma iş akışlarının kapılarını açabilirsiniz. Bu öğreticide projeyi kurmaktan güncellenmiş dosyayı kaydetmeye kadar tüm süreci adım adım göstereceğiz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java.  
- **Mevcut bir PSD'ye metin ekleyebilir miyim?** Evet – dosyayı yükleyin, bir `TextLayer` ekleyin ve kaydedin.  
- **Üretim için lisansa ihtiyacım var mı?** Değerlendirme dışı kullanım için ticari bir lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** JDK 8 ve üzeri (en son LTS sürümünü öneririz).  
- **Web back‑end'ler için uygun mu?** Kesinlikle – API herhangi bir Java tabanlı sunucu ortamında çalışır.

## “PSD'ye metin ekleme” nedir?
PSD'ye metin eklemek, bir Photoshop belgesi içinde programlı olarak yeni bir metin katmanı oluşturmak anlamına gelir. Katman, diğer Photoshop metin katmanları gibi davranır: taşıyabilir, içeriğini düzenleyebilir ve stil uygulayabilirsiniz—Photoshop açmadan.

## Java ile bir PSD'de metin katmanı neden oluşturulur?
- **Otomasyon** – Pazarlama varlıklarını, filigranları veya ürün etiketlerini toplu olarak oluşturun.  
- **Tutarlılık** – Binlerce dosyada aynı yazı tipi, boyut ve konumlandırmayı sağlayın.  
- **Entegrasyon** – Diğer Java hizmetleri (e‑ticaret, raporlama, CI boru hatları) ile birleştirerek grafikleri anında sunun.

## Önkoşullar
Kod yazmadan önce şunlara sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – JDK 8 ve üzeri kurun. [buradan indirebilirsiniz](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – En son JAR dosyasını [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) alın.  
3. **IDE (isteğe bağlı ama faydalı)** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Temel Java bilgisi** – Sınıflar, nesneler ve dosya G/Ç konusunda rahat olmalısınız.  
5. **Örnek bir PSD** – Bu kılavuzda `OneLayer.psd` dosyasını tercih ettiğiniz bir klasöre koyarak kullanacağız.

## Paketleri İçe Aktarma
İlk olarak, PSD dosyaları ve metin katmanlarıyla çalışmak için gerekli sınıfları içe aktarın.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Bu içe aktarmalar, temel Aspose.PSD işlevselliğine erişmenizi sağlar.

## Adım Adım Kılavuz

### Adım 1: Belge Dizinini Ayarlama
Kaynak PSD'nizin bulunduğu ve çıktının kaydedileceği klasörü tanımlayın.

```java
String dataDir = "Your Document Directory"; 
```

`"Your Document Directory"` ifadesini dosyalarınızın mutlak ya da göreli yolu ile değiştirin.

### Adım 2: Kaynak PSD Dosyasını Yükleme
Mevcut PSD'yi `Image.load()` ile belleğe alın.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Yol doğruysa, `img` artık yüklenmiş Photoshop belgesini temsil eder.

### Adım 3: `PsdImage`'a Dönüştürme
Photoshop'a özgü özelliklerle çalıştığımız için, genel `Image` nesnesini `PsdImage`'a dönüştürün.

```java
PsdImage im = (PsdImage)img;
```

Bu dönüşüm, `addTextLayer()` gibi yöntemlerin kullanılmasını sağlar.

### Adım 4: Metin Katmanı İçin Dikdörtgeni Tanımlama
Yeni metnin nerede görüneceğini belirtin. Dikdörtgen, konumu (x, y) ve boyutu (genişlik, yükseklik) tanımlar.

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

Hesaplamaları, düzen ihtiyaçlarınıza göre ayarlamaktan çekinmeyin.

### Adım 5: Metin Katmanını Ekleme
Tanımlanan dikdörtgen içinde gerçek metin katmanını oluşturun.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

`"Added text"` ifadesini PSD'de görünmesini istediğiniz herhangi bir dizeyle değiştirin. İşte **programlı olarak metin katmanı PSD** oluşturduğumuz yer.

### Adım 6: Güncellenmiş PSD Dosyasını Kaydetme
Değiştirilen belgeyi yeni bir dosyaya yazarak orijinali üzerine yazmamayı sağlayın.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Çalıştırdıktan sonra, hedef klasörde `ImageWithTextLayer.psd` dosyasını bulacaksınız; artık yeni metin katmanını içeriyor.

## Yaygın Sorunlar ve Çözümler
| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **`NullPointerException` on `im.addTextLayer`** | PSD doğru şekilde yüklenmedi (yanlış yol). | `sourceFileName`'in mevcut bir PSD'ye işaret ettiğini doğrulayın. |
| **Text not visible** | Dikdörtgen tuvalin dışına yerleştirilmiş veya katman gizli. | Dikdörtgen koordinatlarını ayarlayın veya katman görünürlüğünü `layer.setVisible(true)` ile kontrol edin. |
| **LicenseException** | Kütüphaneyi üretimde geçerli bir lisans olmadan kullanmak. | Ticari bir lisans edinin ve `License license = new License(); license.setLicense("Aspose.PSD.lic");` kodu ile ayarlayın. |

## Sıkça Sorulan Sorular

**S: Birden fazla metin katmanı ekleyebilir miyim?**  
C: Evet – eklemek istediğiniz her metin için Adım 4 ve 5'i tekrarlamanız yeterlidir.

**S: Metni (yazı tipi, boyut, renk) nasıl biçimlendirebilirim?**  
C: `TextLayer` sınıfı, `Font`, `FontSize`, `Color` ve diğer stil özelliklerini değiştirebileceğiniz bir `getTextData()` yöntemi sunar. Ayrıntılı bilgi için Aspose.PSD API belgelerine bakın.

**S: PSD'mde zaten birçok katman varsa ne olur?**  
C: Aspose.PSD, karmaşık katman yapılarıyla çalışır. Belirli grupları hedefleyebilir veya `addTextLayer` aşırı yüklemelerini kullanarak yeni metin katmanını istediğiniz bir indekse ekleyebilirsiniz.

**S: Bu yaklaşım web uygulamaları için uygun mu?**  
C: Kesinlikle. Sunucunuz Java çalıştırdığı sürece, PSD'leri anında oluşturabilir veya değiştirebilir ve müşterilere sunabilirsiniz.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
C: Hem topluluk hem de Aspose mühendislerinin yardımcı olabileceği [Aspose destek forumlarını](https://forum.aspose.com/c/psd/34) ziyaret edin.

## Sonuç
Artık Java ve Aspose.PSD kullanarak çalışma zamanında **PSD dosyalarına metin eklemenin** ne kadar kolay olduğunu gördünüz. Bu teknik, grafik oluşturmayı otomatikleştirmenizi, varlıkları kişiselleştirmenizi ve Photoshop seviyesinde düzenlemeyi herhangi bir Java tabanlı çözüme entegre etmenizi sağlar. Aspose.PSD API'sinin geri kalanını keşfederek şekiller, raster katmanlar ekleyebilir veya daha zengin otomasyon için filtreler uygulayabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose