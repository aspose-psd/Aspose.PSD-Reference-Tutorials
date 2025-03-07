---
title: Java'da JPEG EXIF Etiketlerini Okuyun ve Değiştirin
linktitle: Java'da JPEG EXIF Etiketlerini Okuyun ve Değiştirin
second_title: Aspose.PSD Java API'si
description: Bu adım adım kılavuzda Aspose.PSD for Java kullanarak JPEG EXIF etiketlerini nasıl okuyacağınızı ve değiştireceğinizi öğrenin. Görüntü meta verilerini zahmetsizce işlemek isteyen geliştiriciler için mükemmeldir.
weight: 18
url: /tr/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da JPEG EXIF Etiketlerini Okuyun ve Değiştirin

## giriiş
Selam! Java kullanarak JPEG EXIF etiketlerini nasıl okuyabileceğinizi ve değiştirebileceğinizi hiç merak ettiniz mi? Eğer öyleyse, doğru yerdesiniz! Bu eğitim size Aspose.PSD for Java'yı kullanarak süreç boyunca adım adım rehberlik edecektir. İster deneyimli bir geliştirici olun ister yeni başlayan biri olun, bu kılavuzun sonunda JPEG EXIF etiketlerini bir profesyonel gibi kullanabileceksiniz. O halde hadi dalalım!
## Önkoşullar
Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:
1.  Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Kütüphanesi: Aspose.PSD for Java kütüphanesini indirmeniz gerekir. Şuradan al:[Aspose sürümler sayfası](https://releases.aspose.com/psd/java/).
3. Entegre Geliştirme Ortamı (IDE): IntelliJ IDEA veya Eclipse gibi bir IDE, kodlama deneyiminizi daha sorunsuz hale getirecektir.
4. Temel Java Bilgisi: Bu eğitimi takip etmek için Java'nın temel düzeyde anlaşılması gerekir.
## Paketleri İçe Aktar
Öncelikle gerekli paketleri import edelim. Java IDE'nizi açın ve yeni bir Java projesi oluşturun. Ardından Aspose.PSD for Java kütüphanesini proje bağımlılıklarınıza ekleyin.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## 1. Adım: PSD Görüntüsünü Yükleyin
Bu adımda EXIF verilerini okumak istediğimiz PSD görselini yükleyeceğiz. Resminizin doğru dizinde olduğundan emin olun.
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## Adım 2: Görüntü Kaynaklarını Yineleyin
Görüntü yüklendikten sonraki adım, genellikle EXIF verilerini içeren küçük resim kaynağını bulmak için kaynakları üzerinde yineleme yapmaktır.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Sonraki adıma geçin
    }
}
```
## Adım 3: EXIF Verilerini Çıkarın
Artık küçük resim kaynağına sahip olduğumuza göre, EXIF verilerini buradan çıkarabiliriz. EXIF verileri, kamera sahibinin adı, açıklık değeri, yönelim ve daha fazlası gibi değerli bilgiler içerir.
```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```
## Adım 4: EXIF Verilerini Değiştirin
EXIF verilerini okuduktan sonra bazı alanlarını değiştirmek isteyebilirsiniz. Bunu nasıl yapabileceğiniz aşağıda açıklanmıştır:
```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```
## Adım 5: Değişiklikleri Kaydedin
Son olarak EXIF verilerini değiştirdikten sonra değişiklikleri yeni bir PSD dosyasına kaydedin.
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Çözüm
Ve işte karşınızda! Bu adımları izleyerek Aspose.PSD for Java'yı kullanarak JPEG EXIF etiketlerini kolayca okuyabilir ve değiştirebilirsiniz. Bu güçlü kitaplık, görüntü meta verilerinin işlenmesini kolaylaştırır. Öyleyse devam edin ve kendi projelerinizde deneyin. Mutlu kodlama!
## SSS'ler
### EXIF verileri nedir?
EXIF (Değiştirilebilir Görüntü Dosyası Formatı) verileri, bir görüntüyle ilgili kamera ayarları ve yönlendirme gibi meta verileri içerir.
### Aspose.PSD'yi Java için ücretsiz kullanabilir miyim?
 adresinden ücretsiz deneme alabilirsiniz.[Aspose sürümler sayfası](https://releases.aspose.com/).
### Aspose.PSD for Java, Java'nın tüm sürümleriyle uyumlu mu?
Aspose.PSD for Java, Java SE 7 ve üzerini destekler.
### Aspose.PSD for Java hakkında daha fazla belgeyi nerede bulabilirim?
 Şuna göz atın:[dokümantasyon](https://reference.aspose.com/psd/java/) daha fazla ayrıntı için.
### Aspose.PSD for Java desteğini nasıl alabilirim?
 adresinden destek alabilirsiniz.[Aspose PSD destek forumu](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
