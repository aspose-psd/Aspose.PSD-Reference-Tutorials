---
date: 2026-01-22
description: Aspose.PSD for Java kullanarak JPEG görüntü yönlendirmesini otomatik
  olarak düzeltmek için bir Java görüntü işleme öğreticisini öğrenin.
linktitle: Auto Correct JPEG Image Orientation in Java
second_title: Aspose.PSD Java API
title: 'java görüntü işleme öğreticisi: JPEG yönünü otomatik düzelt'
url: /tr/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da JPEG Görüntü Yönünü Otomatik Düzeltme

## Giriş
Günümüz dijital çağında, gelmiştir. Bu **java image processing tutorial** size Aspose.PSD for Java kullanarak JPEG görüntü yönünü otomatik olarak nasıl düzelteceğinizi gösterir. Fotoğraf düzenleme uygulaması, içerik yönetim hattı veya otomatik bir görüntü işleme iş akışı oluşturuyor olun, aşağıdaki adımlar Java projelerinize sorunsuz yön düzeltme entegrasyonu sağlamanıza yardımcı olacaktır.

## Hızlı Yanıtlar
- **Otomatik döndürme ne yapar?** EXIF yönlendirme bayrağını okur ve JPEG küçük resmini doğru şekilde görüntülenecek şekilde döndürür.  
- **Hangi kütüphane döndürmeyi yönetir?** Aspose.PSD for Java `autoRotate()` metodunu sağlar.  
- **Bir lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Bir toplu işlemde birden fazla PSD dosyasını işleyebilir miyim?** Evet—kodu bir döngü içinde sarın ve her dosya için aynı mantığı yeniden kullanın.  
- **Ek bir bağımlılık gerekli mi?** Sadece Aspose.PSD JAR; dış görünt ihtiyaç yok.

## Java görüntü işleme öğreticisi nedir?
**java image processing tutorial** adım adım bir rehberdir ve Java kütüphanelerini kullanarak görüntüleri yeniden boyutlandırma, kırpma veya yönünü düzeltme gibi işlemlerle nasıl manipüle edeceğinizi öğretir. Bu rehberde, kamera veya mobil cihazların yönlendirme meta verilerini sakladığı varlıkları işlerken sık karşılaşılan bir ihtiyaç olan PSD dosyaları içinde gömülü JPEG yönünün düzeltilmesine odaklanıyoruz.

## Neden Aspose.PSD'yi otomatik döndürme için kullanmalıs okur.  
- **Harici yerel JDK çalıştıran herhangi bir platformda çalışır.  
- **Yüksek performans** – büyük PSD dosyaları ve toplu işlemler için optimize edilmiştir.ı:DK)üphanesini [here](https://releases.aspose.com/psd/java/) adresinden indirin.  
- Entegre Geliştirme Ortamı (IDE): Java geliştirme için IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir IDE'yi kullanın.  
- Java ve Görüntü İşleme Temel Bilgisi: Java programlaması ve görüntü işleme temel kavramlarına aşina olmak faydalı olacaktır.

## Paketleri İçe Aktarma
Örneğe başlamadan önce, Aspose.PSD for Java'dan gerekli paketleri içe aktardığınızdan emin olun:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Adım 1: PSD Görüntüsünü Yükleyin
İlk olarak, yönünün düzeltilmesi gereken JPEG küçük resmini içeren PSD görüntüsünü yükleyin:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
`"Your Document Directory"` ifadesini PSD dosyanızın bulunduğu gerçek dizin yolu ile değiştirin.

## Adım 2: Görüntü Kaynakları Üzerinde Döngü
Sonra, JPEG küçük resim kaynağını bulmak için görüntü kaynakları üzerinde döngü yapın:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Find thumbnail resource. Typically they are in the Jpeg file format.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Adjust thumbnail data.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // If there is a thumbnail stored, auto-rotate it.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```

## Adım 3: Görüntüyü Kaydedin
Son olarak, otomatik döndürmeyi uyguladıktan sonra düzeltilmiş görüntüyü kaydedin:
```java
image.save();
```
Bu adım, görüntüde yapılan değişikliklerin kalıcı olmasını sağlar.

## Yaygın Sorunlar ve Çözümler
- **Küçük resim bulunamadı** – PSD'nin gerçekten bir JPEG küçük resmi içerdiğinden emin olun; bazı PSD'ler sadece tam çözünürlüklü görüntüyü saklar.  
- **`autoRotate()` etkisiz** – EXIF yönlendirme bayrağının mevcut olduğunu doğrulayın; eksikse, görüntü zaten doğru konumdadır.  
- **Büyük dosyalarda bellek yetersizliği hataları** – JVM yığın boyutunu (`-Xmx`) artırın veya dosyaları daha küçük partilerde işleyin.

## Sonuç
Sonuç olarak, Aspose.PSD for Java kullanmak, PSD dosyaları içinde JPEG görüntü yönlerini otomatik olarak düzeltmek için güçlü bir çözüm sunar. Bu **java image processing tutorial**'da belirtilen adımları izleyerek, geliştiriciler görüntü işleme iş akışlarını geliştirebilir ve görüntülerin çeşitli platform ve cihazlarda doğru şekilde görüntülenmesini sağlayabilir.

## SSS
### Aspose.PSD for Java nedir?
Aspose.PSD for Java, Java geliştiricilerinin PSD, JPEG ve diğer görüntü formatlarıyla programlı olarak çalışmasını sağlayan güçlü bir kütüphanedir.

### Aspose.PSD for Java'ı nasıl indirebilirim?
Kütüphaneyi [here](https://releases.aspose.com/psd/java/) adresinden indirebilirsiniz.

### Aspose.PSD for Java görüntü manipülasyonunu destekliyor mu?
Evet, yeniden boyutlandırma, kırpma ve yön ayarlama gibi çeşitli görüntü manipülasyon görevlerini destekler.

### Aspose.PSD for Java belgelerini nerede bulabilirim?
Kapsamlı dokümantasyon [here](https://reference.aspose.com/psd/java/) adresinde mevcuttur.

### Aspose.PSD for Java'ı ücretsiz deneyebilir miyim?
Evet, ücretsiz deneme sürümünü [here](https://releases.aspose.com/) adresinden alabilirsiniz.

## Sıkça Sorulan Sorular

**S: Bu kodu çoklu iş parçacıklı bir ortamda kullanabilir miyim?**  
C: Evet, ancak eşzamanlılık sorunlarından kaçınmak için her iş parçacığı için ayrı bir `PsdImage` örneği oluşturun.

**S: Otomatik döndürme orijinal PSD dosyasını etkiler mi?**  
C: Döndürme yalnızca JPEG küçük resmine uygulanır; ana PSD katmanları, açıkça değiştirilmedikçe değişmeden kalır.

**S: JPEG küçük resmi olmayan PSD dosyalarını nasıl ele alırım?**  
C: `exifData.getThumbnail()` değerini `null` için kontrol edin. `null` ise, kendiniz bir küçük resim oluşturmanız veya döndürmeyi atlamanız gerekebilir.

**S: PSD dosyalarının bulunduğu bir klasörü toplu işleme yoluyla işleyebilir miyim?**  
C: Yükleme, döndürme ve kaydetme mantığını, hedef dizindeki tüm `.psd` dosyalarını dönen bir `File[]` döngüsü içinde sarın.

**S: Hangi Aspose.PSD sürümü gereklidir?**  
C: Kod, 2023‑2024 sürümleri dahil olmak üzere herhangi bir yeni sürümle çalışır. API değişiklikleri için her zaman sürüm notlarına bakın.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-22  
**Test Edilen:** Aspose.PSD for Java 24.11 (yazım zamanı en son sürüm)  
**Yazar:** Aspose