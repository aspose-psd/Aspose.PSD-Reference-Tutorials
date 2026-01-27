---
date: 2026-01-27
description: Aspose.PSD for Java (asp) kullanarak PSD görüntülerinden belirli EXIF
  etiketlerini okumayı adım adım öğreticiyle öğrenin. Görüntü işleme becerilerinizi
  geliştirin.
linktitle: Read Specific EXIF Tags Information in Java
second_title: Aspose.PSD Java API
title: Java'da Aspose (asp) ile Belirli EXIF Etiket Bilgilerini Okuma
url: /tr/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile Aspose (asp) Kullanarak Belirli EXIF Etiket Bilgilerini Okuma

## Giriş
Java **asp kütüphanesini (Aspose.PSD)** kullanarak PSD dosya manipülasyonu dünyasına dalmak mı istiyorsunuz? Bu öğreticide bir PSD görüntüsünden **Java tarzında EXIF verilerini çıkarmayı**, yalnızca ihtiyacınız olan etiketleri okumayı ve bunları konsola yazdırmayı öğreneceksiniz. Geliştirme ortamınızı kurmaktan WhiteBalance, ISO hızı ve odak uzaklığı gibi meta verileri çekmeye kadar her şeyi adım adım göstereceğiz. Hadi başlayalım!

## Hızlı Yanıtlar
- **Java'da PSD'den EXIF verilerini okuyan kütüphane nedir?** Aspose.PSD (asp)  
- **Hangi etiketler çıkarılabilir?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, vb.  
- **Üretim için lisansa ihtiyacım var mı?** Evet, ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **Bunu diğer görüntü formatlarıyla kullanabilir miyim?** Aynı API, `java image metadata extraction` aracılığıyla PNG, JPEG, TIFF'yi destekler.  
- **Uygulama ne kadar sürer?** Temel sadece okuma senaryosu için yaklaşık 10‑15 dakika.

## **asp** (Aspose.PSD for Java) nedir?
Aspose.PSD for Java, geliştiricilerin Photoshop yüklü olmadan Adobe Photoshop dosyaları (PSD, PSB) ile çalışmasını sağlayan güçlü, **pure‑Java** bir kütüphanedir. Katmanlara, kaynaklara ve meta verilere—EXIF etiketleri dahil—tam erişim sağlar ve **java image metadata extraction** görevleri için idealdir.

## EXIF çıkarımı için neden Aspose.PSD (asp) kullanmalı?
- **Yerel Photoshop gerekmez** – Java çalışan herhangi bir platformda çalışır.  
- **Yüksek doğrulukta meta veri erişimi** – dosyada saklanan tam kamera ayarlarını alır.  
- **Basit API** – temiz, nesne‑yönelimli metodlar kodunuzu okunabilir tutar.  
- **Geniş format desteği** – PSD, PSB'yi işleyebilir ve PNG/JPEG/TIFF'ye sorunsuz dönüştürür.

## Önkoşullar
Koda geçmeden önce, hazır bulundurmanız gereken birkaç şey var:

1. Java Development Kit (JDK): Makinenizde JDK yüklü olduğundan emin olun. [Oracle JDK web sitesinden](https://www.oracle.com/java/technologies/javase-downloads.html) indirebilirsiniz.  
2. Aspose.PSD for Java: Kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.  
3. Entegre Geliştirme Ortamı (IDE): IntelliJ IDEA, Eclipse veya NetBeans gibi bir IDE kodlamayı daha rahat hale getirir.  
4. PSD Dosyası: EXIF verisi içeren bir PSD dosyası. Bu öğreticide sağlanan örnek dosyayı veya EXIF etiketli herhangi bir PSD dosyasını kullanabilirsiniz.

## Paketleri İçe Aktarma
İlk olarak, Java projenize gerekli Aspose.PSD paketlerini içe aktarmanız gerekir. İşte nasıl ayarlanacağı.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Adım 1: PSD Görüntüsünü Yükleme
Başlamak için PSD dosyanızı uygulamaya yüklemeniz gerekir. Dosya yolunun doğru belirtildiğinden emin olun.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

Bu adımda, `Image.load()` yöntemiyle PSD dosyasını yüklüyoruz. `PsdImage` sınıfı PSD görüntüsünü temsil eder ve yüklenen görüntüyü bu sınıfa dönüştürerek PSD‑özel işlevlere erişiyoruz.

## Adım 2: Görüntü Kaynakları Üzerinde Döngü
Şimdi, genellikle EXIF verilerini içeren küçük resim kaynağını bulmak için görüntü kaynakları üzerinde döngü yapmamız gerekiyor.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Bir `for` döngüsüyle görüntü kaynakları arasında dolaşıyoruz. Amaç, EXIF verilerini tutan `ThumbnailResource` veya `Thumbnail4Resource` örneklerini belirlemektir.

## Adım 3: EXIF Verilerini Çıkarma
Küçük resim kaynağını belirledikten sonra EXIF verilerini çıkarır ve konsola yazdırırız.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Bir `if` ifadesiyle kaynağın `ThumbnailResource` örneği olup olmadığını kontrol ederiz. Eğer öyleyse, onu dönüştüp `JpegOptions` üzerinden `ExifData`'ya erişiriz. Son olarak WhiteBalance, Piksel Boyutları, ISOSpeed ve FocalLength gibi çeşitli EXIF etiketlerini yazdırırız.

## Yaygın Sorunlar ve İpuçları
- **Null EXIF verisi:** Bazı PSD dosyaları EXIF bilgisi içeren bir küçük resim kaynağı içermeyebilir. Etiket değerlerine erişmeden önce her zaman `null` kontrolü yapın.  
- **Dosya yolu hataları:** Mutlak yollar kullanın veya çalışma dizininin PSD dosyanızın bulunduğu klasöre işaret ettiğinden emin olun.  
- **Lisans kısıtlamaları:** Ücretsiz deneme sürümü işleyebileceğiniz sayfa sayısını sınırlamaktadır; sınırsız kullanım için tam lisansa yükseltin.

## Sık Sorulan Sorular
### EXIF verisi nedir?
EXIF (Exchangeable Image File Format) verisi, görüntü dosyalarına gömülü meta veridir ve kamera ayarları, tarih ve saat, görüntü boyutları gibi bilgileri içerir.

### Aspose.PSD ile EXIF verisini düzenleyebilir miyim?
Evet, Aspose.PSD EXIF verisini okuyup değiştirebilir. Etiketleri güncelleyebilir ve değişiklikleri görüntü dosyasına geri kaydedebilirsiniz.

### Aspose.PSD for Java ücretsiz mi?
Aspose.PSD, [buradan](https://releases.aspose.com/) indirebileceğiniz ücretsiz bir deneme sürümü sunar. Tam özellikler için bir lisans satın almanız gerekir.

### Aspose.PSD hangi diğer formatları destekliyor?
Aspose.PSD, PSD, PSB ve daha fazlası dahil olmak üzere çeşitli Adobe Photoshop formatlarını destekler. Ayrıca bu formatları PNG, JPEG, TIFF gibi diğerlerine dönüştürme seçenekleri sunar.

### Aspose.PSD için desteği nasıl alabilirim?
Aspose.PSD [forumundan](https://forum.aspose.com/c/psd/34) destek alabilirsiniz.

### Bu, **java image metadata extraction** konusunda nasıl yardımcı olur?
`JpegExifData` nesnesini kullanarak ihtiyacınız olan herhangi bir EXIF etiketini programlı olarak çekebilirsiniz; bu da görüntü formatları arasında daha geniş meta veri çıkarma görevleri için sağlam bir temel oluşturur.

## Sonuç
Bu adımları izleyerek Aspose.PSD (asp) kullanarak bir PSD görüntüsünden **Java tarzında EXIF verilerini çıkarmayı** öğrendiniz. Bu süreç, görüntüyü yüklemeyi, kaynakları üzerinde döngü yapmayı, küçük resim kaynağını tanımlamayı ve ihtiyacınız olan EXIF etiketlerini okumayı içerir. Bu bilgiyle, Java uygulamalarınıza ayrıntılı görüntü meta verilerini ekleyebilir, daha zengin fotoğraf yönetimi, analiz veya otomatik işleme hatları oluşturabilirsiniz.

---

**Son Güncelleme:** 2026-01-27  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}