---
title: Java'da EXIF Segmentine Küçük Resim Ekleme
linktitle: Java'da EXIF Segmentine Küçük Resim Ekleme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java kullanarak görsel meta verilerini küçük resimlerle nasıl geliştireceğinizi öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin. Sorunsuz entegrasyon için.
weight: 10
url: /tr/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da EXIF Segmentine Küçük Resim Ekleme

## giriiş
Bu eğitimde Aspose.PSD for Java kullanarak EXIF segmentine küçük resim ekleyerek görüntü meta verilerini nasıl geliştirebileceğimizi keşfedeceğiz. EXIF (Değiştirilebilir Görüntü Dosyası Formatı) meta verileri, dijital fotoğrafçılıkta kamera ayarları, tarih ve konum gibi değerli bilgiler sağlayarak çok önemli bir rol oynar. Küçük resim eklemek, görüntüleri etkili bir şekilde önizleyerek kullanıcı deneyimini geliştirir.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
- Java programlamanın temel bilgisi.
- Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
- IntelliJ IDEA veya Eclipse gibi Java için IDE (Entegre Geliştirme Ortamı).
- Java kütüphanesi için Aspose.PSD. adresinden indirebilirsiniz.[Java İndirme sayfası için Aspose.PSD](https://releases.aspose.com/psd/java/).
## Paketleri İçe Aktar
Öncelikle gerekli paketleri Aspose.PSD ve Java'dan içe aktarın:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Aspose.PSD'yi kullanarak Java'da EXIF segmentine küçük resim ekleme işlemini ayrıntılı adımlara ayıralım:
## 1. Adım: PSD Görüntüsünü Yükleyin
PSD görüntü dosyasını bir PsdImage nesnesine yükleyin.
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```
## Adım 2: Görüntü Kaynaklarını Yineleyin
Uygun küçük resim kaynağını bulmak için görüntü kaynaklarını yineleyin.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Küçük resim kaynağını işle
    }
}
```
## 3. Adım: Küçük Resim Verilerini Ayarlayın
Küçük resim verilerini hazırlayın ve ayarlayın.
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // JPEG kalitesini ayarlayın
```
## Adım 4: Görüntüyü Kaydedin
Değiştirilen görüntüyü tekrar diske kaydedin.
```java
image.save(dataDir + "output.psd");
```
## Çözüm
Aspose.PSD kullanarak Java'da EXIF segmentine küçük resim eklemek, görüntü meta verilerinin kullanılabilirliğini artıran basit bir işlemdir. Bu eğitimde özetlenen adımları izleyerek görsellerinizi önizleme küçük resimleriyle verimli bir şekilde zenginleştirebilirsiniz.

## SSS'ler
### EXIF meta verileri nedir?
EXIF meta verileri, dijital görüntülere kamera ayarlarını, tarihi ve diğer ayrıntıları içeren gömülü bilgilerdir.
### EXIF'e neden küçük resim eklenmeli?
Küçük resim eklemek, görüntünün tamamını yüklemeden hızlı görüntü önizlemelerine izin vererek kullanıcı deneyimini iyileştirir.
### Aspose.PSD for Java'yı nereden indirebilirim?
 Aspose.PSD for Java'yı şu adresten indirebilirsiniz:[Burada](https://releases.aspose.com/psd/java/).
### Aspose.PSD için nasıl geçici lisans alabilirim?
 Aspose.PSD için geçici lisansı şu adresten edinebilirsiniz:[Burada](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD için nasıl destek alabilirim?
 Destek için şu adresi ziyaret edin:[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
