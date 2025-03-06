---
title: Java'da Belirli EXIF Etiketi Bilgilerini Okuyun
linktitle: Java'da Belirli EXIF Etiketi Bilgilerini Okuyun
second_title: Aspose.PSD Java API'si
description: Adım adım eğitimimizle Aspose.PSD for Java kullanarak PSD görüntülerinden belirli EXIF etiketlerini nasıl okuyacağınızı öğrenin. Görüntü işleme becerilerinizi geliştirin.
weight: 19
url: /tr/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Belirli EXIF Etiketi Bilgilerini Okuyun

## giriiş
Java ile PSD dosya işleme dünyasına dalmak mı istiyorsunuz? PSD görsellerinden belirli EXIF etiketlerinin nasıl okunacağını öğrenmek istiyorsanız doğru yerdesiniz. Bu eğitim, ortamınızın kurulumundan ayrıntılı EXIF verilerinin çıkarılmasına kadar Aspose.PSD for Java'yı kullanmanın tüm süreci boyunca size yol gösterecektir. Hadi başlayalım!
## Önkoşullar
Kodun ayrıntılarına girmeden önce, uygulamanız gereken birkaç şey var:
1.  Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Oracle JDK web sitesi](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java: Kütüphaneyi şu adresten indirin:[Burada](https://releases.aspose.com/psd/java/).
3. Entegre Geliştirme Ortamı (IDE): IntelliJ IDEA, Eclipse veya NetBeans gibi bir IDE, kodlamayı daha kolay hale getirecektir.
4. PSD Dosyası: EXIF verilerini içeren bir PSD dosyası. Bu eğitimde sağlanan örneği veya EXIF etiketli başka herhangi bir PSD dosyasını kullanabilirsiniz.
## Paketleri İçe Aktar
Öncelikle gerekli Aspose.PSD paketlerini Java projenize aktarmanız gerekecek. Bunu nasıl ayarlayacağınız aşağıda açıklanmıştır.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## 1. Adım: PSD Görüntüsünü Yükleyin
Başlamak için PSD dosyanızı uygulamaya yüklemeniz gerekir. Dosya yolunuzun doğru şekilde belirtildiğinden emin olun.
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Bu adımda PSD dosyasını kullanarak yüklüyoruz.`Image.load()` Yöntem.`PsdImage` sınıfı PSD görüntüsünü temsil etmek için kullanılır ve PSD'ye özgü işlevlere erişmek için yüklenen görüntüyü bu sınıfa aktarırız.
## Adım 2: Görüntü Kaynaklarını Yineleyin
Şimdi, genellikle EXIF verilerini içeren küçük resim kaynağını bulmak için görüntü kaynakları üzerinde yinelememiz gerekiyor.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Daha fazla işlem burada yapılacak
    }
}
```
 Bir kullanarak görüntü kaynakları arasında dolaşıyoruz.`for` döngü. Amaç, örnekleri olan kaynakları belirlemektir.`ThumbnailResource` veya`Thumbnail4Resource`, çünkü bunlar EXIF verilerini tutan türlerdir.
## Adım 3: EXIF Verilerini Çıkarın
Küçük resim kaynağını belirledikten sonra EXIF verilerini çıkarıp konsola yazdırıyoruz.
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
 Bir kullanıyoruz`if` Kaynağın bir örneği olup olmadığını kontrol etmek için ifade`ThumbnailResource` . Eğer öyleyse, onu atarız ve geri alırız.`JpegOptions` erişmek için`ExifData`Son olarak WhiteBalance, Pixel Dimensions, ISOSpeed ve FocalLength gibi çeşitli EXIF etiketlerinin çıktısını alıyoruz.

## Çözüm
Bu adımları izleyerek Aspose.PSD for Java kullanarak bir PSD görüntüsünden belirli EXIF etiketlerini nasıl okuyacağınızı öğrendiniz. Bu süreç, görüntünün yüklenmesini, kaynakları üzerinde yineleme yapılmasını, küçük resim kaynağının tanımlanmasını ve EXIF verilerinin çıkarılmasını içerir. Bu bilgiyle artık PSD dosyalarınızdaki EXIF verilerini keşfedebilir ve işleyebilir, böylece daha karmaşık görüntü işleme görevlerine olanak tanıyabilirsiniz.
## SSS'ler
### EXIF verileri nedir?
EXIF (Değiştirilebilir Görüntü Dosyası Formatı) verileri, görüntü dosyalarına gömülü olan ve kamera ayarları, tarih ve saat ile görüntü boyutları gibi bilgileri içeren meta verilerdir.
### Aspose.PSD'yi kullanarak EXIF verilerini düzenleyebilir miyim?
Evet, Aspose.PSD EXIF verilerini okumanıza ve değiştirmenize olanak sağlar. Etiketleri güncelleyebilir ve değişiklikleri tekrar görüntü dosyasına kaydedebilirsiniz.
### Aspose.PSD Java için ücretsiz mi?
 Aspose.PSD, indirebileceğiniz ücretsiz bir deneme sürümü sunuyor[Burada](https://releases.aspose.com/). Tüm özellikler için bir lisans satın almanız gerekir.
### Aspose.PSD başka hangi formatları destekliyor?
Aspose.PSD, PSD, PSB ve daha fazlası dahil olmak üzere çeşitli Adobe Photoshop formatlarını destekler. Ayrıca bu formatları PNG, JPEG, TIFF vb. gibi diğer formatlara dönüştürme seçenekleri de sunar.
### Aspose.PSD için nasıl destek alabilirim?
 Aspose.PSD aracılığıyla destek alabilirsiniz[forum](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
