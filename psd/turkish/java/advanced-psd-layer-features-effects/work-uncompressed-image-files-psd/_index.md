---
date: 2026-04-12
description: Bu adım adım rehberde Java ve Aspose.PSD kütüphanesini kullanarak PSD'yi
  RAW formatına dönüştürmeyi ve PSD'yi sıkıştırma olmadan dışa aktarmayı öğrenin.
keywords:
- convert psd to raw
- export psd without compression
- Aspose.PSD Java
linktitle: Java ile PSD'de Sıkıştırılmamış Görüntü Dosyalarıyla Çalışma
second_title: Aspose.PSD Java API
title: Java Kullanarak PSD'yi RAW'ye Dönüştürme (Sıkıştırılmamış Görüntü Dosyaları)
url: /tr/java/advanced-psd-layer-features-effects/work-uncompressed-image-files-psd/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Kullanarak PSD'yi RAW'ye Dönüştürme (Sıkıştırılmamış Görüntü Dosyaları)

## Giriş
Java'da Photoshop belgeleri (PSD) ile çalışırken **PSD'yi RAW'ye dönüştürme** ve PSD'yi sıkıştırma olmadan dışa aktarmayı anlamak, görüntü doğruluğunu korumak için çok önemlidir. Bu öğreticide, Aspose.PSD'nin sıkıştırılmamış görüntü dosyalarını yönetme sürecini, bir PSD'yi yüklemekten RAW‑stilinde sıkıştırılmamış bir dosya olarak kaydetmeye kadar nasıl basitleştirdiğini inceleyeceğiz. Grafik‑ağır bir uygulama geliştiriyor olun ya da kayıpsız görüntü dışa aktarımlarına ihtiyacınız olsun, burada ihtiyacınız olan her şeyi bulacaksınız. Başlamaya hazır mısınız? Hadi başlayalım!

## Hızlı Yanıtlar
- **“convert PSD to RAW” ne anlama geliyor?** PSD verilerini hiçbir sıkıştırma olmadan kaydeder, piksel verilerini orijinal biçiminde tutar.  
- **Bu işlemi hangi kütüphane yönetir?** Aspose.PSD for Java, sıkıştırılmamış kaydetmeler için basit bir API sunar.  
- **Lisans gereklimi?** Ücretsiz deneme sürümü test için çalışır; üretim için ticari bir lisans gereklidir.  
- **Gerekli Java sürümü nedir?** JDK 8 veya üzeri.  
- **Kaydettikten sonra dosyayı hâlâ düzenleyebilir miyim?** Evet – sıkıştırılmamış PSD'yi yeniden yükleyebilir ve çizim ya da katman eklemeye devam edebilirsiniz.

## “convert PSD to RAW” nedir?
Bir PSD'yi RAW'ye dönüştürmek, Photoshop belgesini **herhangi bir sıkıştırma olmadan** dışa aktarmak anlamına gelir. Ortaya çıkan dosya tam piksel verisini korur; bu, görüntü kalitesinin asla ödün verilemeyeceği durumlar için idealdir—örneğin arşivleme, bilimsel görüntüleme veya yüksek‑kalite baskı hatları gibi.

## Neden PSD'yi sıkıştırma olmadan dışa aktaralım?
- **Maksimum kalite:** Sıkıştırma artefaktlarından dolayı detay kaybı yok.  
- **Tahmin edilebilir dosya boyutu:** RAW dosyaları, görüntü boyutları ve bit derinliğini doğrudan yansıtan bir boyuta sahiptir.  
- **Basitleştirilmiş sonraki işleme:** Diğer araçlar, önce sıkıştırmayı açmaya gerek kalmadan piksel verisini okuyabilir.

## Önkoşullar
Kodlamaya başlamadan önce, listemizde işaretlememiz gereken birkaç önkoşul var. Endişelenmeyin; oldukça basitler!

### Java Geliştirme Kiti (JDK)
- Sisteminizde JDK 8 veya üzeri yüklü olduğundan emin olun. Yüklü değilse, [Oracle web sitesine](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) giderek en son sürümü indirin.

### Entegre Geliştirme Ortamı (IDE)
- IntelliJ IDEA, Eclipse veya NetBeans gibi iyi bir IDE, işinizi kolaylaştırır. Henüz kurmadıysanız birini kurun!

### Aspose.PSD for Java Kütüphanesi
- Aspose.PSD for Java kütüphanesini indirin. En son sürümleri [buradan](https://releases.aspose.com/psd/java/) alabilirsiniz. 

### Java Temel Bilgisi
- Java programlaması ve nesne‑yönelimli paradigma hakkında temel bir anlayışa sahip olmalısınız, böylece sorunsuz bir şekilde takip edebilirsiniz.

### Bir PSD Dosyası
- Test için bir örnek PSD dosyasına sahip olun. Bunu Photoshop'ta oluşturabilir veya çevrimiçi ücretsiz bir örnek indirebilirsiniz. 

Her şey hazır olduğuna göre, koda dalalım!

## Paketleri İçe Aktar
Başlamak için, kodumuz için gerekli paketleri içe aktarmamız gerekiyor. Aşağıda ihtiyacınız olacak import listesi yer alıyor:

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

Bu importlar, gerekli sınıf ve metodları projemize getirerek PSD dosyalarını sorunsuz bir şekilde manipüle etmemizi sağlar. Süreci yönetilebilir adımlara bölelim.

## Adım 1: Dosya Dizinini Ayarlama
İlk olarak, PSD dosyanızın nerede bulunduğunu ve çıktıyı nereye kaydetmek istediğinizi belirtmeniz gerekir. Örnek kodumuzda, dizin yolunu tutacak bir değişken oluşturacağız.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini PSD dosyanızın (`layers.psd`) saklandığı gerçek yol ile değiştirin. Bunu yaparak programınızın dosyayı nerede arayacağını belirtmiş olursunuz.

## Adım 2: PSD Dosyasını Yükleme
Şimdi, `Image.load()` metodunu kullanarak PSD dosyasını yükleyelim ve `PsdImage` tipine dönüştürelim.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Bu satır, `Image` sınıfının `load` metodunu çağırarak PSD dosyanızı belleğe yükler. `PsdImage`'a dönüştürerek, Java'ya bu görüntüyü PSD dosyası olarak ve PSD işlemleriyle ilgili belirli işlevselliklere sahip olarak ele almasını söylüyoruz.

## Adım 3: Kaydetme Seçeneklerini Yapılandırma
Şimdi, dosyamızı kaydetmek için seçenekleri ayarlamamız gerekiyor; özellikle çıktının **sıkıştırılmamış** olmasını (yani PSD'yi RAW'ye dönüştürme) belirtmeliyiz.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

`PsdOptions` sınıfı, PSD dosyamızı kaydetmek için çeşitli seçenekler belirlememizi sağlar. `setCompressionMethod`'u `CompressionMethod.Raw` olarak ayarlamak, kaydedilen dosyanın sıkıştırılmamış olmasını ve yüksek kaliteyi korumasını sağlar.

## Adım 4: Sıkıştırılmamış PSD Dosyasını Kaydetme
Şimdi yeni yapılandırılmış PSD görüntüsünü kaydetme zamanı.

```java
psdImage.save(dataDir + "uncompressed_out.psd", saveOptions);
```

Bu satır, `PsdImage` örneğimiz (`psdImage`) üzerindeki kaydetme işlevini yürütür. Dosyayı belirtilen dizinde `uncompressed_out.psd` olarak kaydeder ve önceki adımda tanımlanan seçenekleri uygular.

## Adım 5: Yeni Oluşturulan Görüntüyü Yeniden Açma
Kaydettikten sonra, çıktımızı yeniden yükleyerek her şeyin beklendiği gibi çalıştığını doğrulayalım.

```java
PsdImage img = (PsdImage) Image.load(dataDir + "uncompressed_out.psd");
```

`load` metodunu tekrar çağırarak, kaydedilen dosyaya karşılık gelen yeni bir `PsdImage` örneği oluşturabiliriz. Bu adım, kaydettikten sonra görüntüyü manipüle etmek veya göstermek istiyorsanız kritik öneme sahiptir.

## Adım 6: Görüntüyü Çizme veya Manipüle Etme
Son olarak, yeni açılan görüntü üzerinde çizim yapmak veya manipülasyon yapmak isteyebilirsiniz.

```java
Graphics graphics = new Graphics(img);
```

Burada, `img` üzerinde çeşitli grafik işlemleri yapmamızı sağlayan bir `Graphics` nesnesi başlatıyoruz. İsterseniz şekiller çizebilir, metin ekleyebilir ya da katmanları değiştirebilirsiniz!

## Yaygın Kullanım Durumları
- **Arşivleme:** Orijinal sanat eserini hiçbir kayıp olmadan koruyun.  
- **Bilimsel görüntüleme:** Analiz için ham piksel verilerini dışa aktarın.  
- **Baskı üretimi:** Dosyaları bir yazıcıya göndermeden önce en yüksek doğruluğu sağlayın.  

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, geliştiricilerin Photoshop PSD dosyalarıyla programlı olarak çalışmasını sağlayan bir Java kütüphanesidir.

**S: Aspose.PSD kullanarak bir PSD dosyasındaki katmanları manipüle edebilir miyim?**  
C: Evet! Aspose.PSD, katmanlara erişmenizi ve onları manipüle etmenizi sağlar, böylece karmaşık işlemleri kolayca yapabilirsiniz.

**S: Aspose.PSD ücretsiz mi?**  
C: Ücretsiz bir deneme sürümü mevcuttur, ancak kapsamlı kullanım ve gelişmiş özelliklere erişim için bir lisans satın almanız gerekebilir.

**S: Sorunla karşılaşırsam destek ile nasıl iletişime geçebilirim?**  
C: Yardım için [Aspose destek forumuna](https://forum.aspose.com/c/psd/34) ulaşabilirsiniz.

**S: Aspose.PSD, PSD dışındaki formatlarda kaydetmeyi destekliyor mu?**  
C: Evet, Aspose.PSD, gereksinimlerinize bağlı olarak PNG, JPEG ve daha fazlası gibi farklı formatlarda kaydetmeye olanak tanır.

**S: Diğer platformlarda PSD'yi sıkıştırma olmadan dışa aktarabilir miyim?**  
C: Aynı yaklaşım .NET ve C++ sürümlerinde de çalışır; yalnızca dil‑spesifik sözdizimini ayarlamanız gerekir.

## Sonuç
Tebrikler! Java ve Aspose.PSD kütüphanesini kullanarak **PSD'yi RAW'ye dönüştürmeyi** ve PSD'yi sıkıştırma olmadan dışa aktarmayı yeni öğrendiniz. Bu güçlü API, PSD dosyalarını kolayca yönetmenizi sağlar—yükleme, manipülasyon ve sıkıştırılmamış olarak kaydetme. İlerleyin, grafik nesnesiyle deneyler yapın, katman ekleyin, şekil çizin veya bu iş akışını daha büyük bir görüntü‑işleme hattına entegre edin.

Daha gelişmiş özellikler ve seçenekler için [belgelere](https://reference.aspose.com/psd/java/) göz atmayı unutmayın. Hemen başlamak isterseniz, kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirebilir veya ücretsiz deneme sürümüne başlayabilirsiniz. Herhangi bir sorunuz olursa, topluluktan yardım almak için [destek forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

---

**Son Güncelleme:** 2026-04-12  
**Test Edilen Sürüm:** Aspose.PSD for Java 24.12 (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}