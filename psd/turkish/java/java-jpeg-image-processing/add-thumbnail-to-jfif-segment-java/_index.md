---
title: Java'da JFIF Segmentine Küçük Resim Ekleme
linktitle: Java'da JFIF Segmentine Küçük Resim Ekleme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD'yi kullanarak Java'da bir PSD görüntüsüne nasıl küçük resim ekleyeceğinizi adım adım öğrenin. Görüntü işleme yeteneklerini geliştirmek isteyen Java geliştiricileri için idealdir.
weight: 11
url: /tr/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da JFIF Segmentine Küçük Resim Ekleme

## giriiş
Java geliştirme alanında, görüntü işleme yeteneklerinin entegre edilmesi, basit görüntü manipülasyonlarından karmaşık grafik tasarım görevlerine kadar çeşitli uygulamalar için çok önemlidir. Aspose.PSD for Java, PSD (Photoshop Document) dosyalarını kolaylıkla işlemek için tasarlanmış güçlü bir kütüphane olarak öne çıkıyor. Bu eğitim belirli bir göreve odaklanıyor: Aspose.PSD for Java kullanarak bir görüntünün JFIF segmentine küçük resim eklemek. Bu kılavuzun sonunda, her bir parçayı iyice kavramanızı sağlayacak şekilde bunu adım adım nasıl gerçekleştireceğinizi öğreneceksiniz.
## Önkoşullar
Bu eğitime dalmadan önce aşağıdaki önkoşulların ayarlandığından emin olun:
-  Java Geliştirme Kiti (JDK): Sisteminizde Java'nın kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Oracle'ın JDK web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
-  Aspose.PSD for Java: Aspose.PSD for Java kütüphanesine sahip olmanız gerekir. adresinden temin edebilirsiniz.[Aspose.PSD Java indirme sayfası](https://releases.aspose.com/psd/java/).
- Entegre Geliştirme Ortamı (IDE): Java geliştirme için IntelliJ IDEA veya Eclipse gibi bir IDE kullanın.
- Temel Java Anlayışı: Java programlama dili ve kavramlarına aşinalık.
## Paketleri İçe Aktar
Kodlamaya başlamadan önce Aspose.PSD işlevlerini kullanmak için gerekli paketleri içe aktarın:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## 1. Adım: PSD Görüntüsünü Yükleyin
İlk olarak, küçük resmi eklemek istediğiniz yere PSD görüntüsünü yükleyin:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```
## 2. Adım: Görüntü Kaynakları Üzerinde Yineleme Yapın
JFIF segmentini bulmak için görüntü kaynaklarını yineleyin:
```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Küçük resim işlemeye devam et
    }
}
```
## 3. Adım: Küçük Resim Verilerini Ayarlayın
Yeni bir küçük resim görüntüsü oluşturun ve onu verilerle doldurun:
```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Küçük resim verilerini doldurun (örnek: basit bir piksel dizisi oluşturun)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    //Küçük resim verilerini kaydet
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Küçük resim verilerini Jpeg seçeneklerine ayarlayın
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Küçük resim kaynağına ilişkin seçenekleri ayarlayın
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // İstisnaları ele alın
} finally {
    // Kaynakları imha edin
}
```
## Adım 4: Değiştirilen Görüntüyü Kaydedin
Son olarak değiştirilen PSD görüntüsünü kaydedin:
```java
image.save(dataDir + "output.psd");
```

## Çözüm
Sonuç olarak bu eğitim, Aspose.PSD for Java kullanarak bir PSD görüntüsünün JFIF segmentine küçük resim ekleme sürecinde size yol gösterdi. Bu adımları izleyerek Java uygulamalarınızı Aspose.PSD'nin sunduğu güçlü görüntü işleme özellikleriyle geliştirebilirsiniz.
## SSS'ler
### Java için Aspose.PSD nedir?
Aspose.PSD for Java, Java geliştiricilerinin PSD dosyalarını programlı olarak işlemesine olanak tanıyan bir kütüphanedir.
### Aspose.PSD for Java ile ilgili daha fazla belgeyi nerede bulabilirim?
 Ayrıntılı belgeler şu adreste bulunabilir:[Aspose.PSD for Java dokümantasyon sayfası](https://reference.aspose.com/psd/java/).
### Aspose.PSD for Java ticari kullanıma uygun mu?
 Evet, Aspose.PSD for Java ticari olarak kullanılabilir. adresinden lisans satın alabilirsiniz.[Aspose.PSD'nin satın alma sayfası](https://purchase.aspose.com/buy).
### Satın almadan önce Aspose.PSD for Java'yı deneyebilir miyim?
 Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Aspose.PSD'nin deneme indirme sayfası](https://releases.aspose.com/).
### Aspose.PSD for Java desteğini nasıl alabilirim?
 Destek için şu adresi ziyaret edin:[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
