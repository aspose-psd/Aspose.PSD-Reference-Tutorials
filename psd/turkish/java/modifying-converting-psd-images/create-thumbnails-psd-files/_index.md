---
date: 2026-03-13
description: Aspose.PSD kullanarak Java’da PSD küçük resmi oluşturmayı öğrenin. PSD
  dosyalarından hızlıca küçük resimler üretmek için adım adım rehberimizi izleyin.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: PSD Küçük Resim Oluşturma Java – PSD'den Küçük Resimler Oluştur
url: /tr/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Küçük Resim Oluşturma Java – PSD'den Küçük Resimler Oluşturma

## Giriş
Eğer Photoshop dosyalarından ön izleme görsellerini çıkaran **create PSD thumbnail Java** koduna ihtiyacınız varsa, doğru yerdesiniz. Dijital varlık yöneticisi, web galerisi ya da otomatik toplu‑işleme hattı oluşturuyor olun, PSD dosyalarından küçük resimler oluşturmak performansı ve kullanıcı deneyimini büyük ölçüde iyileştirebilir. Bu öğreticide Aspose.PSD for Java ile tüm süreci adım adım gösterecek, bir PSD'yi nasıl yükleyeceğinizi, gömülü küçük resim kaynaklarını nasıl bulacağınızı ve bunları ayrı görüntü dosyaları olarak nasıl kaydedeceğinizi anlatacağız.

## Hızlı Yanıtlar
- **PSD küçük resim çıkarımı için en iyi kütüphane nedir?** Aspose.PSD for Java.  
- **Uygulama ne kadar sürer?** Temel bir kurulum için yaklaşık 10‑15 dakika.  
- **Photoshop yüklü olması gerekiyor mu?** Hayır, Aspose.PSD bağımsız çalışır.  
- **Küçük resmi hangi görüntü formatlarına aktarabilirim?** Aspose.PSD tarafından desteklenen herhangi bir format (ör. BMP, PNG, JPEG).  
- **Üretim ortamı için lisans gerekli mi?** Evet, üretim kullanımı için ticari bir lisans gerekir.

## “create PSD thumbnail Java” nedir?
Java'da bir PSD küçük resmi oluşturmak, bir Photoshop Belgesi (PSD) içinde depolanan küçük resim ön izlemesini programlı olarak okuyup ayrı bir görüntü dosyası olarak yazmak anlamına gelir. Bu, tam ve genellikle büyük olan PSD içeriğini yüklemeden hızlı ön izlemeler oluşturmak için kullanışlıdır.

## Bu görev için neden Aspose.PSD kullanmalı?
- **Photoshop bağımlılığı yok:** JDK yüklü herhangi bir platformda çalışır.  
- **Tam PSD desteği:** Küçük resimler dahil tüm PSD sürümlerini ve kaynaklarını yönetir.  
- **Basit API:** Küçük resimleri çıkarmak ve kaydetmek için birkaç satır kod.  
- **Performans‑optimizeli:** Büyük dosyalar için verimli bellek yönetimi.

## Ön Koşullar
Küçük resim oluşturmanın ayrıntılarına girmeden önce, başlamanız için neler gerektiğini gözden geçirelim.

### Java Geliştirme Ortamı
- **Java JDK:** Bilgisayarınızda Java Development Kit (JDK) yüklü olduğundan emin olun. [buradan](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.  
- **IDE:** IntelliJ IDEA, Eclipse veya NetBeans gibi bir Entegre Geliştirme Ortamı (IDE) kodlamayı kolaylaştırır.

### Aspose.PSD Kütüphanesi
- Projenize Aspose.PSD kütüphanesini eklemeniz gerekir. [En son sürümü buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.

### Java Temel Bilgisi
- Java temellerine aşina olmak, örnek kodu daha etkili bir şekilde takip etmenize yardımcı olur. Sınıflar, nesneler ve döngüler gibi kavramlar sıkça kullanılacaktır.

## Paketleri İçe Aktarma
Aspose.PSD kütüphanesinden gerekli sınıfları içe aktararak başlayın. Bu adım, kütüphanenin işlevlerini kodunuzda kullanabilmeniz için kritiktir.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

Ön koşullar halledikten sonra ana konuya geçelim! PSD dosyalarından küçük resim oluşturmak birkaç basit adım içerir ve bunları sizin için açıklayacağım.

## PSD küçük resmi Java ile nasıl oluşturulur – Adım‑Adım Kılavuz

### Adım 1: Ortamınızı Kurun
Projenizi başlatmak ve küçük resim üretimine hazırlamak için aşağıdakileri yapın.

1. **Java Projesi Oluşturun**  
   - IDE'nizi açın ve yeni bir Java projesi oluşturun.  
   - `"PsdThumbnailGenerator"` gibi bir ad verin.

2. **Aspose.PSD Kütüphanesini Ekleyin**  
   - Aspose.PSD JAR dosyasını projenizin derleme yoluna ekleyin.  
   - Maven kullanıyorsanız, `pom.xml` dosyanıza ekleyin:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### Adım 2: PSD Dosyasını Yükleyin
Sonra, küçük resim oluşturmak istediğimiz PSD dosyasını yüklememiz gerekiyor.

1. **Belge Dizinini Belirleyin**  
   PSD dosyanızın bulunduğu dizini tanımlayın.

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **PSD Dosyasını Yükleyin**  
   PSD dosyanızı yüklemek için `PsdImage` sınıfını kullanın.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **Pro ipucu:** Yol sorunlarından kaçınmak için PSD dosyalarınızı ayrı bir klasörde tutun (ör. `src/main/resources`).

### Adım 3: PSD Kaynakları Üzerinde Döngü
PSD görüntümüz yüklendiğine göre, sonraki adım kaynaklarını incelemektir.

1. **Kaynak Sayısını Alın**  
   PSD dosyasındaki tüm kaynaklar üzerinde döngü yapacağız.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **Küçük Resim Kaynaklarını Belirleyin**  
   Döngü içinde, bir kaynağın küçük resim olup olmadığını kontrol edin.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### Adım 4: Küçük Resmi İşleyin
Bir küçük resim kaynağı belirlediğimizde, ona uygun şekilde işlem yapmamız gerekir.

1. **Küçük Resim Formatını Alın ve Kontrol Edin**  
   Kaynak gerçekten bir küçük resimse, onu alın ve formatını kontrol edin.

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### Adım 5: Küçük Resmi Oluşturun ve Kaydedin
İşte sihrin gerçekleştiği yer! Küçük resim verisinden yeni bir görüntü oluşturacak ve kaydedeceğiz.

1. **Yeni Bir Görüntü Oluşturun**  
   Küçük resim kaynağının genişlik ve yüksekliğini kullanarak yeni bir bitmap görüntüsü oluşturacağız.

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **Piksel Verilerini Yeni Görüntüye Aktarın**  
   Küçük resim verisini yeni oluşturulan görüntüye aktarın.

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **Küçük Resim Görüntüsünü Kaydedin**  
   Son olarak, küçük resim görüntüsünü belge dizininize benzersiz bir adla kaydedin.

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **Yaygın hata:** `PsdImage` nesnelerini kapatmayı unutmak bellek sızıntılarına yol açabilir. Java 7+ kullanıyorsanız, görüntü işleme kodunu try‑with‑resources bloğu içinde sarın.

## Sonuç
Bu adımları izleyerek, artık herhangi bir Photoshop dosyasından ön izleme görselleri çıkaran **create PSD thumbnail Java** uygulamaları için sağlam ve yeniden kullanılabilir bir yönteminiz var. Bu teknik, toplu işlemciler, web servisleri veya masaüstü yardımcı programlara entegre edilerek görüntü kataloglamayı hızlandırabilir ve UI yanıt süresini artırabilir. Kendi PSD koleksiyonunuzla deneyin ve hafif ön izlemeleri ne kadar hızlı üretebileceğinizi görün!

## SSS

### Aspose.PSD nedir?
Aspose.PSD, geliştiricilerin Photoshop dosyalarıyla çalışmasını sağlayan bir Java kütüphanesidir; PSD dosyalarını programlı olarak manipüle etmeyi ve yönetmeyi kolaylaştırır.

### Aspose.PSD'yi ücretsiz kullanabilir miyim?
Evet, Aspose bir lisans satın almadan önce kütüphaneyi denemeniz için ücretsiz bir deneme sunar.

### Küçük resimleri hangi formatlarda kaydedebilirim?
Bu örnekte küçük resimleri BMP formatında kaydettik, ancak Aspose.PSD ayrıca çeşitli diğer formatları da destekler.

### Aspose.PSD'yi kullanmak için Photoshop yüklü olması gerekir mi?
Hayır, Aspose.PSD Photoshop'tan bağımsız çalışır.

### Aspose.PSD hakkında daha fazla bilgi nereden bulunur?
Daha fazla detay, öğretici ve kaynak için [Aspose.PSD belgelerine](https://reference.aspose.com/psd/java/) göz atabilirsiniz.

## Sıkça Sorulan Sorular

**S: Şifre‑korumalı bir PSD'den küçük resimleri nasıl çıkarırım?**  
C: Şifre parametresi kabul eden `Image.load` metodunun uygun aşırı yüklemesini kullanarak PSD'yi yükleyin.

**S: BMP yerine PNG formatında küçük resimler oluşturabilir miyim?**  
C: Kesinlikle. `save` metodundaki dosya uzantısını değiştirin, Aspose.PSD dönüşümü gerçekleştirecektir.

**S: Birden fazla PSD dosyasını toplu‑işlem yapmak mümkün mü?**  
C: PSD dosyalarının bulunduğu bir dizini döngüyle gezerek kodu sarmalayın, her dosya için aynı çıkarma mantığını yeniden kullanın.

**S: Hangi Java sürümü gereklidir?**  
C: Aspose.PSD, Java 8 ve üzerini destekler. Performans ve güvenlik için en yeni JDK kullanılması önerilir.

**S: Kütüphane büyük PSD dosyalarını verimli bir şekilde yönetiyor mu?**  
C: Evet, Aspose.PSD tembel yükleme ve optimize edilmiş bellek yönetimi kullanarak büyük dosyaları heap alanını tüketmeden işler.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-03-13  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java (yazım anındaki en son sürüm)  
**Yazar:** Aspose