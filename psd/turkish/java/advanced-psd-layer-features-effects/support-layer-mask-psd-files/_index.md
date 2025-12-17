---
date: 2025-12-17
description: Aspose.PSD for Java kullanarak katman maskelerini koruyarak PSD'yi PNG'ye
  nasıl dışa aktaracağınızı öğrenin – Java görüntü dönüşümü için adım adım bir rehber.
linktitle: Export PSD to PNG with Layer Mask Support in Java
second_title: Aspose.PSD Java API
title: Java'da Katman Maskesi Desteğiyle PSD'yi PNG'ye Dışa Aktar
url: /tr/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Katman Maskesi Desteğiyle PSD'yi PNG'ye Dışa Aktarma

## Introduction
Karmaşık katman maskelerini bozulmadan **export PSD to PNG** yapmanız gerektiğinde, güvenilir bir Java kütüphanesi size saatler süren manuel işi tasarruf ettirebilir. Bu öğreticide, Aspose.PSD Java API'sını kullanarak bir PSD dosyasını yüklemekten tam alfa‑kanalı desteğiyle PNG görüntüsü olarak kaydetmeye kadar tüm süreci adım adım ele alacağız. İster toplu‑işlem aracı, ister otomatik varlık hattı oluşturuyor olun, ya da sadece hızlı bir dönüşüm betiğine ihtiyacınız olsun, görevi basitleştiren net ve konuşma tarzı adımlar bulacaksınız.

## Quick Answers
- **“export PSD to PNG” ne anlama geliyor?** Photoshop PSD dosyasını görsel bütünlüğü koruyarak bir PNG raster görüntüsüne dönüştürmek.  
- **Hangi kütüphane katman maskelerini yönetiyor?** Aspose.PSD for Java, maskeler ve alfa kanalları için yerleşik destek sağlar.  
- **Lisans gerekir mi?** Test için ücretsiz deneme sürümü yeterlidir; üretim kullanımı için ticari lisans gereklidir.  
- **Herhangi bir işletim sisteminde çalıştırabilir miyim?** Evet – Java API platform‑bağımsızdır.  
- **Dönüşüm ne kadar sürer?** Standart boyuttaki dosyalar için genellikle bir saniyenin altında.

## What is “export PSD to PNG” and why does it matter?
PSD'yi PNG'ye dışa aktarmak, Photoshop çalışmanızı web'de paylaşmak, uygulamalara gömmek veya küçük resimler üretmek istediğinizde kritik öneme sahiptir. PNG şeffaflığı korur, bu da katman maskeleri içeren varlıklar için idealdir. Java ile dönüşümü otomatikleştirerek manuel dışa aktarma adımlarını ortadan kaldırır ve büyük toplularda tutarlı sonuçlar elde edersiniz.

## Prerequisites
Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Development Kit (JDK)** – `java -version` komutuyla doğrulayın. Gerekirse [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) adresinden indirin.  
- **Aspose.PSD library** – En yeni JAR dosyasını [download page](https://releases.aspose.com/psd/java/) üzerinden edinin veya Maven/Gradle ile ekleyin.  
- **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir Java geliştirme editörü.

### 1. Java Development Environment
11 veya daha yeni bir JDK, Aspose.PSD API ile uyumluluğu garanti eder.

### 2. Aspose.PSD Library
Kütüphane **java image conversion**, maske ayrıştırma ve PNG dışa aktarma seçeneklerini yönetir.

### 3. IDE (Integrated Development Environment)
Bir IDE, hata ayıklamayı ve proje kurulumunu kolaylaştırır.

## Import Packages
Java sınıfınıza gerekli importları ekleyin. Bu sınıflar PSD dosyalarını yüklemenizi, maskelerle çalışmanızı ve PNG dışa aktarma ayarlarını yapılandırmanızı sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Export PSD to PNG with Layer Mask Support
Aşağıda **save psd as png** işlemini maskeleri koruyarak gerçekleştiren eksiksiz, adım‑adım iş akışı yer almaktadır.

### Step 1: Set Up Your Project Directory
Kaynak PSD'nin bulunduğu ve çıktının PNG olarak kaydedileceği klasörü tanımlayın.

```java
String dataDir = "Your Document Directory";
```

`Your Document Directory` ifadesini makinenizdeki mutlak yol ile değiştirin.

### Step 2: Specify the Source PSD File
Dönüştürmek istediğiniz PSD dosyasını gösterin. Bu örnekte karmaşık bir maske içeren bir dosya kullanıyoruz.

```java
String sourceFileName = dataDir + "MaskComplex.psd";
```

### Step 3: Define the Export Path for the PNG
Programın oluşturulan PNG dosyasını nereye yazacağını belirtin.

```java
String exportPath = dataDir + "MaskComplex.png";
```

### Step 4: Load the PSD File
Bu, **how to load psd** adımıdır. `Image.load` metodu dosyayı bir `PsdImage` nesnesine okur.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Step 5: Set Up PNG Export Options
Alfa kanalını koruyacak şekilde PNG'yi yapılandırın; bu, katman maskesi şeffaflığı için kritiktir.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### Step 6: Save the PNG File
Son olarak **convert psd to png** işlemini gerçekleştirin.

```java
im.save(exportPath, saveOptions);
```

Her şey doğru ayarlandıysa, `MaskComplex.png` dosyasını çıktı klasörünüzde bulacaksınız ve orijinal PSD'nin maskeli bölgelerini mükemmel bir şekilde gösterecektir.

## Common Issues and Solutions
- **File‑not‑found errors** – `dataDir` yolunu iki kez kontrol edin ve PSD dosya adının büyük/küçük harf duyarlılığıyla tam olarak eşleştiğinden emin olun.  
- **Missing transparency** – `saveOptions.setColorType(PngColorType.TruecolorWithAlpha)` ayarının uygulandığını doğrulayın; aksi takdirde PNG alfa kanalı olmadan kaydedilir.  
- **Out‑of‑memory for large files** – Çok büyük PSD'leri işlerken JVM yığın boyutunu (`-Xmx2g`) artırmayı düşünün.

## Frequently Asked Questions

**Q: PSD dosyalarında katman maskesi nedir?**  
A: Katman maskesi, bir katmanın şeffaflığını kontrol eder; pikselleri kalıcı olarak silmeden görüntünün belirli bölümlerini gizlemenize veya ortaya çıkarmanıza olanak tanır.

**Q: Programlama bilgisi olmadan PSD dosyalarıyla çalışabilir miyim?**  
A: Aspose.PSD kod gerektirse de, grafik tasarımcılar manuel dönüşüm için Photoshop veya diğer GUI araçlarını kullanabilir.

**Q: Aspose.PSD ücretsiz mi?**  
A: İndirme sayfasından ücretsiz bir deneme sürümü mevcuttur; ticari projeler için ücretli lisans gereklidir.

**Q: PSD dosyam maskeler içermiyorsa ne olur?**  
A: Dönüşüm yine çalışır; ortaya çıkan PNG sadece maskesiz şeffaflık etkileri olmayacaktır.

**Q: Sorun yaşarsam nereden destek alabilirim?**  
A: [support forum](https://forum.aspose.com/c/psd/34) adresini ziyaret ederek Aspose uzmanlarından ve topluluktan yardım alabilirsiniz.

## Conclusion
Artık Aspose.PSD Java API'sını kullanarak katman maskelerini koruyarak **export PSD to PNG** işlemini nasıl yapacağınızı öğrendiniz. Bu yöntem **java image conversion** sürecini basitleştirir, toplu işlem desteği sağlar ve görsel varlıklarınızın istenen şeffaflığı korumasını garantiler. Farklı PNG seçenekleriyle denemeler yapabilir veya bu iş akışını daha büyük otomasyon hatlarına entegre edebilirsiniz.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}