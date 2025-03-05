---
title: Küçük Resmi Java'da PSD'den Çıkarın
linktitle: Küçük Resmi Java'da PSD'den Çıkarın
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java kullanarak PSD dosyalarından küçük resimleri nasıl çıkaracağınızı öğrenin. Bu adım adım kılavuz, kurulumdan çıkarılan görüntülerin kaydedilmesine kadar her şeyi kapsar.
type: docs
weight: 15
url: /tr/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## giriiş
Bu eğitimde Aspose.PSD for Java kullanarak PSD dosyalarından küçük resimlerin nasıl çıkarılacağını inceleyeceğiz. Küçük resimler, hızlı önizlemeler için veya PSD belgelerine gömülü görüntülerin daha küçük sürümlerini oluşturmak için yararlı olabilir. Aspose.PSD'yi kullanarak bunu başarmak için gereken adımlara bakalım.
## Önkoşullar
Başlamadan önce aşağıdaki kurulumlara sahip olduğunuzdan emin olun:
- Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
-  Java kütüphanesi için Aspose.PSD. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/psd/java/).
- Java programlamanın temel bilgisi.
## Paketleri İçe Aktar
Başlamak için gerekli Aspose.PSD paketini Java sınıfınıza ekleyin:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Adım 1: PSD Dosyasını Yükleyin
Öncelikle çıkarmak istediğiniz küçük resmin bulunduğu PSD dosyasını yükleyin.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Yer değiştirmek`"Your_Document_Directory/"` PSD dosyanızın bulunduğu dizin yolu ile ve`"your_file.psd"` PSD dosyanızın adıyla.
## Adım 2: Görüntü Kaynaklarını Yineleyin
Küçük resim kaynağını bulmak için görüntü kaynaklarını yineleyin.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Küçük resim verilerini çıkar
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Çıkarılan küçük resim verileriyle yeni bir resim oluşturun
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Çıkarılan küçük resmi ayrı bir JPEG dosyası olarak kaydedin
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Çıkış başarı mesajı
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Küçük resim bulunup işlendiğinde döngüden çıkın
    }
}
```
## 3. Adım: Çıkarılan Küçük Resmi Kaydedin
Çıkarılan küçük resmi ayrı bir görüntü dosyası olarak kaydedin (bu durumda JPEG dosyası olarak).
## Adım 4: Farklı Küçük Resim Türlerini Kullanma
 PSD dosyanız birden fazla türde küçük resim içeriyorsa, örneğin`Thumbnail4Resource`, bu durumları benzer şekilde ele almak için mantığı genişletebilirsiniz.

## Çözüm
Bu eğitimde Aspose.PSD for Java kullanarak PSD dosyalarından küçük resimlerin nasıl çıkarılacağını araştırdık. Yukarıda özetlenen adımları izleyerek, PSD belgelerinize gömülü küçük resimleri etkili bir şekilde alıp kaydedebilirsiniz.

## SSS'ler
### Aspose.PSD nedir?
Aspose.PSD, geliştiricilerin PSD ve diğer görüntü dosyası formatlarıyla programlı olarak çalışmasına olanak tanıyan bir Java kütüphanesidir.
### Aspose.PSD for Java hakkında daha fazla belgeyi nerede bulabilirim?
 Şuraya başvurabilirsiniz:[dokümantasyon](https://reference.aspose.com/psd/java/) ayrıntılı API referansları ve örnekleri için.
### Satın almadan önce Aspose.PSD'yi ücretsiz deneyebilir miyim?
 Evet, indirebilirsiniz[ücretsiz deneme](https://releases.aspose.com/) Kütüphanenin yeteneklerini değerlendirmek.
### Aspose.PSD için nasıl geçici lisans alabilirim?
 Geçici lisanslar şu adresten alınabilir:[Burada](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD ticari kullanıma uygun mudur?
Evet, Aspose.PSD, lisans koşulları kapsamında hem kişisel hem de ticari projeler için kullanılabilir.