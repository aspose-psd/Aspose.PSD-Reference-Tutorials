---
date: 2026-03-15
description: Aspose.PSD for Java kullanarak PNG dosyalarını nasıl sıkıştıracağınızı
  öğrenin; PNG sıkıştırma, PNG boyutunu optimize etme ve PSD'yi PNG'ye verimli bir
  şekilde dönüştürme konusunda adım adım bir rehber.
linktitle: Compress PNG Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java kullanarak PNG dosyalarını nasıl sıkıştırabilirsiniz?
url: /tr/java/optimizing-png-files/compress-png-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java kullanarak PNG dosyalarını sıkıştırma

## Giriş

Yazılım geliştirmede görüntülerle çalışırken, **PNG dosyalarını nasıl sıkıştıracağınızı** verimli bir şekilde öğrenmek sayfa yükleme sürelerini büyük ölçüde iyileştirebilir ve bant genişliği kullanımını azaltabilir. Aspose.PSD for Java, Photoshop (PSD) dosyalarıyla çalışmanıza ve PNG dahil çeşitli formatlara dışa aktarmanıza olanak tanıyan güçlü bir kütüphanedir. **PNG boyutunu optimize etmeniz**, bir web galerisinde PSD'yi PNG'ye dönüştürmeniz veya **PNG sıkıştırma seviyelerini** ince ayarlamanız gerekirse, bu öğretici size eksiksiz, üretim‑hazır bir örnek sunar.

## Hızlı Yanıtlar
- **“PNG nasıl sıkıştırılır” ne anlama geliyor?** Bir PNG görüntüsünün dosya boyutunu, görsel kalitesini koruyarak, genellikle sıkıştırma parametrelerini ayarlayarak küçültmek anlamına gelir.  
- **Java PNG sıkıştırması için en iyi kütüphane hangisidir?** Aspose.PSD for Java, yerleşik PNG seçenekleri sunar ve tam bir sıkıştırma seviyesi aralığını (0‑9) destekler.  
- **Bir lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü çalışır; üretim kullanımı için ticari bir lisans gereklidir.  
- **Birden fazla sıkıştırma seviyesini otomatikleştirebilir miyim?** Evet—`setCompressionLevel` özelliği üzerinden döngü oluşturarak her seviyede PNG oluşturabilirsiniz.  
- **Bu yaklaşım büyük PSD dosyaları için uygun mu?** Kesinlikle; Aspose.PSD verileri verimli bir şekilde akıtarak yüksek çözünürlüklü varlıklar için güvenli olmasını sağlar.

## PNG sıkıştırması nedir?

PNG, kayıpsız sıkıştırma kullanır, yani görüntü kalitesi korunurken dosya boyutu küçülür. **PNG sıkıştırma seviyesi** (0 = sıkıştırma yok, 9 = maksimum sıkıştırma) ayarlanarak verinin ne kadar agresif paketleneceği kontrol edilir. Daha yüksek seviyeler işleme biraz daha uzun sürer ancak daha küçük dosyalar üretir—web optimizasyonu için mükemmeldir.

## Neden PNG sıkıştırmak için Aspose.PSD for Java kullanmalı?

- **Tam PSD desteği** – Bilgi kaybı olmadan PSD katmanlarını açın, düzenleyin ve dışa aktarın.  
- **Granüler kontrol** – Tam PNG sıkıştırma seviyelerini, renk tipini ve bit derinliğini ayarlayın.  
- **Çapraz platform** – Masaüstü uygulamalardan bulut hizmetlerine, Java uyumlu herhangi bir ortamda çalışır.  
- **Performans** – Optimize edilmiş yerel kod, büyük görüntülerde bile hızlı işleme sağlar.  

## Önkoşullar

Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

1. **Java JDK** – En son JDK'yı [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin.  
2. **Aspose.PSD for Java kütüphanesi** – Resmi indirme sayfasından en yeni JAR dosyasını [buradan](https://releases.aspose.com/psd/java/) alın.  
3. **IDE veya kod editörü** – IntelliJ IDEA, Eclipse veya VS Code sorunsuz çalışır.  
4. **Temel Java bilgisi** – İstisna yönetimi ve dosya G/Ç konularına aşina olmak öğrenme eğrisini hızlandırır.  
5. **Örnek PSD dosyası** – `sample.psd` gibi bir PSD dosyasını belge dizini olarak referans göstereceğiniz bir klasöre yerleştirin.

Bu öğelere sahip olmak, **java görüntü optimizasyonu** adımlarına odaklanmanızı sağlar, kurulum sıkıntılarına takılmadan.

## Paketleri İçe Aktarma

Aşağıdaki içe aktarmalar, temel Aspose.PSD sınıflarına ve PNG seçeneklerine erişmenizi sağlar:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Bu sınıflar bir PSD'yi yüklemenize, PNG ayarlarını yapılandırmanıza ve sonucu kaydetmenize olanak tanır.

## Adım 1: Projenizi Kurun

Yeni bir Java projesi (ör. `PsdImageCompressor`) oluşturun ve Aspose.PSD JAR'ını derleme yoluna ekleyin. Bu, derleyicinin yukarıda referans verilen sınıfları bulmasını sağlar.

## Adım 2: Belge Dizinini Tanımlayın

Programa kaynak PSD dosyasının nerede olduğunu ve sıkıştırılmış PNG'lerin nereye yazılacağını söyleyin:

```java
String dataDir = "Your Document Directory"; // Replace with actual path
```

`"Your Document Directory"` ifadesini `sample.psd` dosyasını içeren mutlak ya da göreli yol ile değiştirin. Yolu yapılandırılabilir tutmak, farklı ortamlarda **PSD'yi PNG'ye dönüştürmeyi** kolaylaştırır.

## Adım 3: PSD Görüntüsünü Yükleyin

PSD dosyasını belleğe yükleyin. Bu adım, okumaya başlamadan önce bir kitabı açmaya benzer:

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Dosya bulunamazsa, Aspose.PSD bilgilendirici bir istisna fırlatır—dosya adı ve yolu iki kez kontrol edin.

## Adım 4: Sıkıştırma Seviyeleri Üzerinde Döngü

Her olası **png sıkıştırma seviyesini** keşfetmek için basit bir `for` döngüsü kullanıyoruz. Bu, otomatik olarak farklı sıkıştırma ayarına sahip dokuz ek PNG oluşturur:

```java
for (int i = 0; i <= 9; i++) {
    // Create a new instance of PngOptions
    PngOptions options = new PngOptions();
    options.setCompressionLevel(i); // Set the compression level
```

Döngü 0 (sıkıştırma yok) ile 9 (maksimum sıkıştırma) arasında çalışır ve dosya boyutu ile işleme süresi arasındaki dengeyi net bir şekilde görmenizi sağlar.

## Adım 5: Sıkıştırılmış PNG Dosyalarını Kaydedin

Döngü içinde, her PNG'yi sıkıştırma seviyesini yansıtan bir dosya adıyla kaydedin. Bu, karşılaştırmayı basitleştirir:

```java
    psdImage.save(dataDir + i + "_out.png", options);
}
```

Döngü tamamlandıktan sonra, dizininizde `0_out.png`, `1_out.png`, … `9_out.png` adlı dosyalar bulunur.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| **FileNotFoundException** | `dataDir` yolunun yanlış olması veya `sample.psd` dosyasının eksik olması. | Yol dizesini doğrulayın ve PSD dosyasının mevcut olduğundan emin olun. |
| **OutOfMemoryError** büyük PSD'lerde | Yeterli yığın (heap) alanı olmadan büyük bir PSD yüklemek. | JVM yığınını (`-Xmx2g`) artırın veya görüntüyü parçalara bölerek işleyin. |
| **Sıkıştırılmış PNG değişmemiş gibi görünüyor** | Düşük bir sıkıştırma seviyesi (0‑2) kullanmak. | Önemli bir boyut küçülmesi için seviyeyi 5‑9'a yükseltin. |
| **LicenseException** | Geçerli bir Aspose.PSD lisansı olmadan çalıştırmak. | Deneme lisansı uygulayın veya tam bir lisans satın alın. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, geliştiricilerin Photoshop dosyalarını programlı olarak manipüle etmelerini sağlayan bir kütüphanedir; okuma, düzenleme ve PNG, JPEG ve TIFF gibi formatlara dışa aktarma işlemlerini içerir.

**S: PNG dışındaki diğer görüntü formatlarını sıkıştırabilir miyim?**  
C: Bu öğretici PNG'ye odaklanmıştır, ancak Aspose.PSD PSD, TIFF, JPEG, BMP ve daha fazlasını destekler. Farklı bir format hedeflemek için çıktı seçenekleri sınıfını değiştirebilirsiniz.

**S: Aspose.PSD kullanmak için bir lisansa ihtiyacım var mı?**  
C: Kütüphaneyi ücretsiz deneme sürümüyle değerlendirebilirsiniz, ancak üretim ortamları için tam bir lisans gereklidir. Lisansı [buradan](https://purchase.aspose.com/buy) edinebilirsiniz.

**S: Kodu çalıştırırken bir hata alırsam ne yapmalıyım?**  
C: Dosya yollarınızı iki kez kontrol edin, tüm içe aktarma ifadelerinin mevcut olduğundan emin olun ve uyumlu bir Aspose.PSD JAR sürümü kullandığınızı doğrulayın.

**S: Aspose.PSD for Java hakkında daha fazla belgeleri nereden bulabilirim?**  
C: Ayrıntılı API referansları ve ek örnekler [Aspose.PSD referansında](https://reference.aspose.com/psd/java/) mevcuttur.

---

**Son Güncelleme:** 2026-03-15  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}