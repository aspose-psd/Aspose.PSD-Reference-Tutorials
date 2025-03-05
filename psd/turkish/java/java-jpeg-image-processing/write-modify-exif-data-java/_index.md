---
title: EXIF Verilerini Java'da Yazma ve Değiştirme
linktitle: EXIF Verilerini Java'da Yazma ve Değiştirme
second_title: Aspose.PSD Java API'si
description: Bu kapsamlı, adım adım kılavuzla Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki EXIF verilerini yazmayı ve değiştirmeyi öğrenin.
type: docs
weight: 22
url: /tr/java/java-jpeg-image-processing/write-modify-exif-data-java/
---
## giriiş
Java kullanarak PSD dosyalarındaki EXIF verilerini değiştirmek mi istiyorsunuz? Cevabınız evet ise o zaman doğru yerdesiniz! Bu kapsamlı kılavuz, güçlü Aspose.PSD kütüphanesini kullanarak Java'da EXIF verilerini yazma ve değiştirme adımlarında size yol gösterecektir. 
## Önkoşullar
Koda dalmadan önce her şeyin doğru şekilde kurulduğundan emin olalım.
1. Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun.
2.  Aspose.PSD for Java: Kütüphaneyi şu adresten indirin:[Burada](https://releases.aspose.com/psd/java/).
3. IDE: Sorunsuz bir kodlama deneyimi için IntelliJ IDEA veya Eclipse gibi bir IDE kullanın.
4. Temel Java Bilgisi: Java programlamaya aşinalık şarttır.
5.  Geçici Lisans Alın: Geçici bir lisans alın[Burada](https://purchase.aspose.com/temporary-license/) Aspose.PSD'nin tüm potansiyelini ortaya çıkarmak için.
## Paketleri İçe Aktar
Öncelikle gerekli paketleri Java projenize aktarmanız gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.exif.enums.ExifFlash;
import com.aspose.psd.exif.enums.ExifWhiteBalance;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Bu içe aktarmalar, PSD dosyalarıyla çalışmanıza, EXIF verilerini değiştirmenize ve Aspose.PSD'nin güçlü özelliklerinden yararlanmanıza olanak tanır.
Artık her şeyi ayarladığınıza göre, süreci basit, takip edilmesi kolay adımlara ayıralım.
## 1. Adım: PSD Görüntüsünü Yükleyin
Başlangıç olarak PSD dosyanızı projenize yüklemeniz gerekiyor. Bunu nasıl yapabileceğiniz aşağıda açıklanmıştır:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
Bu kod parçacığı, PSD görüntüsünü belirttiğiniz dizinden yükler.
## Adım 2: Görüntü Kaynaklarını Yineleyin
Daha sonra, küçük resim kaynağını bulmak için görüntü kaynakları üzerinde yineleme yapmanız gerekir. EXIF verilerinin genellikle JPEG formatında depolandığı yer burasıdır.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Küçük resim kaynaklarını kontrol edin
}
```
## 3. Adım: Küçük Resim Kaynağını Belirleyin
Bu adımda, resim kaynaklarından küçük resim kaynağını belirleyeceksiniz.
```java
if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
    // EXIF verilerini küçük resim kaynağından çıkarın
}
```
## Adım 4: EXIF Verilerini Çıkarın ve Yazdırın
Küçük resim kaynağını tanımladıktan sonraki adım, EXIF verilerini çıkarmak ve konsola yazdırmaktır.
```java
JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
if (exif != null) {
    // EXIF verilerini yazdır
}
```
## Adım 5: EXIF Verilerini Değiştirin
Şimdi işin eğlenceli kısmı geliyor; EXIF verilerini değiştirme. LensMake, WhiteBalance ve Flash bilgilerini şu şekilde ayarlayabilirsiniz.
```java
exif.setLensMake("Sony");
exif.setWhiteBalance(ExifWhiteBalance.Auto);
exif.setFlash(ExifFlash.Fired);
```
## Adım 6: Görüntüyü Kaydedin
Gerekli değişiklikleri yaptıktan sonra değişiklikleri uygulamak için resmi kaydedin.
```java
image.save(dataDir + "Modified_Zebras_Serengeti.psd");
```
## Çözüm
Ve işte karşınızda! Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki EXIF verilerini nasıl yazacağınızı ve değiştireceğinizi başarıyla öğrendiniz. Bu güçlü kitaplık, karmaşık görüntü formatlarıyla çalışmayı basitleştirerek onu grafik dosyalarıyla çalışan geliştiriciler için değerli bir araç haline getirir. 
 Daha ayrıntılı bilgi için şuraya göz atın:[Aspose.PSD Belgeleri](https://reference.aspose.com/psd/java/) . Herhangi bir sorunla karşılaşırsanız,[Destek Forumu](https://forum.aspose.com/c/psd/34) yardım almak için harika bir yerdir. Keşfetmeyi unutmayın[ücretsiz deneme](https://releases.aspose.com/) ve bir lisans satın almayı düşünün[Burada](https://purchase.aspose.com/buy) tüm özellikler için.
## SSS'ler
### EXIF verileri nedir?
EXIF (Değiştirilebilir Görüntü Dosyası Formatı) verileri, görüntü dosyalarına gömülü olan ve kamera ayarları, tarih, saat ve konum gibi bilgileri içeren meta verilerdir.
### Aspose.PSD diğer görüntü formatlarını destekleyebilir mi?
Evet, Aspose.PSD PNG, JPEG, BMP ve GIF dahil olmak üzere çeşitli görüntü formatlarını destekler.
### Aspose.PSD Java için ücretsiz mi?
Ücretsiz deneme sürümünü kullanabilirsiniz ancak tüm özellikler için bir lisans satın almanız gerekir.
### Aspose.PSD için geçici lisansı nasıl edinebilirim?
 Geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).
### Görüntüleri toplu işlemek için Aspose.PSD'yi kullanabilir miyim?
Evet, Aspose.PSD'nin güçlü özelliklerini kullanarak birden fazla görüntüyü toplu olarak işleyebilirsiniz.