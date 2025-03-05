---
title: Java'da Otomatik Düzeltme JPEG Görüntü Yönlendirmesi
linktitle: Java'da Otomatik Düzeltme JPEG Görüntü Yönlendirmesi
second_title: Aspose.PSD Java API'si
description: Aspose.PSD'yi kullanarak Java'da JPEG görüntü yönelimini otomatik olarak düzeltmeyi öğrenin. Görüntü işleme becerilerinizi zahmetsizce geliştirin.
type: docs
weight: 12
url: /tr/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## giriiş
Günümüzün dijital çağında, görüntüleri programlı olarak değiştirmek ve optimize etmek, çeşitli alanlardaki geliştiriciler için çok önemli bir görev haline geldi. Aspose.PSD for Java, geliştiricilere PSD, JPEG ve diğer görüntü formatlarını verimli bir şekilde kullanmaları için güçlü araçlar sağlar. Bu eğitimde belirli bir görev ele alınmaktadır: Aspose.PSD for Java kullanılarak JPEG görüntü yöneliminin otomatik olarak düzeltilmesi. İster bir fotoğraf düzenleme uygulaması oluşturuyor olun, ister bir içerik yönetim sisteminde görüntü kaynaklarını yönetiyor olun, ister görüntü işleme iş akışlarını otomatikleştiriyor olun, bu kılavuz sizi bu işlevselliği Java uygulamalarınıza sorunsuz bir şekilde entegre etmek için gerekli bilgilerle donatacaktır.
## Önkoşullar
Bu eğitime dalmadan önce aşağıdaki önkoşulların ayarlandığından emin olun:
- Java Geliştirme Ortamı: Sisteminizde Java Geliştirme Kitinin (JDK) kurulu olduğundan emin olun.
-  Aspose.PSD for Java JAR: Aspose.PSD for Java kütüphanesini şu adresten indirin:[Burada](https://releases.aspose.com/psd/java/).
- Entegre Geliştirme Ortamı (IDE): Java geliştirme için IntelliJ IDEA, Eclipse veya seçtiğiniz herhangi bir IDE'yi kullanın.
- Java ve Görüntü İşlemenin Temel Anlayışı: Java programlamaya aşinalık ve görüntü işlemenin temel kavramları faydalı olacaktır.

## Paketleri İçe Aktar
Örneğe başlamadan önce gerekli paketleri Aspose.PSD for Java'dan içe aktardığınızdan emin olun:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## 1. Adım: PSD Görüntüsünü Yükleyin
İlk olarak, yönünün düzeltilmesi gereken JPEG küçük resmini içeren PSD görüntüsünü yükleyin:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Yer değiştirmek`"Your Document Directory"` PSD dosyanızın bulunduğu gerçek dizin yolu ile.
## Adım 2: Görüntü Kaynaklarını Yineleyin
Ardından, JPEG küçük resim kaynağını bulmak için görüntü kaynaklarını yineleyin:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Küçük resim kaynağını bulun. Genellikle Jpeg dosya formatındadırlar.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Küçük resim verilerini ayarlayın.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // Saklanan bir küçük resim varsa otomatik olarak döndürün.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## 3. Adım: Görüntüyü Kaydedin
Son olarak, otomatik döndürmeyi uyguladıktan sonra düzeltilen görüntüyü kaydedin:
```java
image.save();
```
Bu adım, görüntüde yapılan değişikliklerin kalıcı olmasını sağlar.

## Çözüm
Sonuç olarak Aspose.PSD for Java'yı kullanmak, PSD dosyalarındaki JPEG görüntü yönelimlerini otomatik olarak düzeltmek için güçlü bir çözüm sunar. Geliştiriciler, bu eğitimde özetlenen adımları izleyerek görüntü işleme iş akışlarını iyileştirerek görüntülerin çeşitli platformlarda ve cihazlarda doğru şekilde görüntülenmesini sağlayabilirler.
## SSS'ler
### Java için Aspose.PSD nedir?
Aspose.PSD for Java, Java geliştiricilerinin PSD, JPEG ve diğer görüntü formatlarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir kütüphanedir.
### Aspose.PSD for Java'yı nasıl indirebilirim?
 Kütüphaneyi adresinden indirebilirsiniz.[Burada](https://releases.aspose.com/psd/java/).
### Aspose.PSD for Java görüntü işlemeyi destekliyor mu?
Evet, yeniden boyutlandırma, kırpma ve yönlendirmeyi ayarlama gibi çeşitli görüntü işleme görevlerini destekler.
### Aspose.PSD for Java belgelerini nerede bulabilirim?
 Kapsamlı belgeler mevcut[Burada](https://reference.aspose.com/psd/java/).
### Aspose.PSD for Java'yı ücretsiz deneyebilir miyim?
 Evet, şu adresten ücretsiz deneme alabilirsiniz:[Burada](https://releases.aspose.com/).