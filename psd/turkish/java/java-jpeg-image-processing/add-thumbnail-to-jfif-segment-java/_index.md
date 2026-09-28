---
date: 2026-09-28
description: Aspose.PSD kullanarak Java'da bir JFIF segmentine küçük resim ekleme.
  Küçük resimleri PSD dosyalarına hızlı ve güvenilir bir şekilde gömmek için bu adım
  adım kılavuzu izleyin.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Java'da JFIF segmentine küçük resim ekleme
og_description: Aspose.PSD kullanarak Java'da bir JFIF segmentine küçük resim ekleme.
  Küçük resimleri PSD dosyalarına hızlı ve güvenilir bir şekilde gömmek için bu adım
  adım kılavuzu izleyin.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Java'da JFIF segmentine küçük resim ekleme
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Java'da JFIF segmentine küçük resim ekleme
url: /tr/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da JFIF segmentine küçük resim ekleme

## Giriş
PSD dosyasının JFIF segmentine küçük resim eklemek, tam görüntüyü yüklemeden hızlı bir görsel önizleme gerektiğinde yaygın bir gereksinimdir. Bu öğreticide **küçük resim eklemeyi** Java’da Aspose.PSD kullanarak öğreneceksiniz. Rehberin sonunda çalıştırılabilir bir kod parçacığı, JFIF yapısının temelleri ve büyük dosyaları verimli bir şekilde işlemek için ipuçları elde edeceksiniz.

## Hızlı cevaplar
- **Gerekli kütüphane nedir?** Aspose.PSD for Java.
- **Hangi Java sürümü çalışır?** JDK 11 veya daha yenisi.
- **Kaç satır kod gerekir?** Yükleme, değiştirme ve kaydetme için yaklaşık 10 satır.
- **Multi‑megabayt dosyaları işleyebilir miyim?** Evet, Aspose.PSD verileri akış olarak işler, böylece bellek kullanımı düşük kalır.
- **Ticari bir lisans gerekli mi?** Üretim kullanımı için lisans gereklidir; ücretsiz deneme sürümü mevcuttur.

## JFIF segmenti nedir?
JFIF segmenti, küçük resimler, EXIF veya renk profilleri gibi isteğe bağlı verileri depolayabilen bir JPEG Dosya Değişim Formatı bloğudur.  
PSD dosyasının JPEG akışının içinde yer alır ve çoğu görüntü görüntüleyici tarafından hızlı önizleme oluşturmak için tanınır.

## Neden bir PSD dosyasına küçük resim eklenir?
Aspose.PSD for Java **30+ görüntü formatını** destekler ve belgeyi belleğe tamamen yüklemeden **2 GB**'a kadar dosyaları işleyebilir. Küçük resim eklemek, önizlemeleri iletirken ağ bant genişliğini azaltır ve galeri uygulamalarında UI render süresini hızlandırır.

## Önkoşullar
- Java Development Kit (JDK): Sisteminizde Java yüklü olduğundan emin olun. [Oracle'ın JDK web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.
- Aspose.PSD for Java: Aspose.PSD for Java kütüphanesine sahip olmanız gerekir. [Aspose.PSD Java indirme sayfasından](https://releases.aspose.com/psd/java/) edinebilirsiniz.
- Entegre Geliştirme Ortamı (IDE): Java geliştirme için IntelliJ IDEA veya Eclipse gibi bir IDE kullanın.
- Java'ya temel anlayış: Java programlama dili ve kavramlarına aşina olun.

## Java'da JFIF segmentine küçük resim nasıl eklenir?
Hedef PSD'yi yükleyin, JFIF kaynağını bulun, küçük resim verisini değiştirin ve dosyayı kaydedin. Tüm işlem birkaç basit API çağrısı ile yapılabilir ve Aspose.PSD düşük‑seviye JPEG yapısını sizin için yönetir.

### Adım 1: paketleri içe aktar
`Document`, `JfifResource` ve ilgili sınıflar Aspose.PSD ad alanının bir parçasıdır. Document, PSD dosya konteynerini temsil eder ve JfifResource, PSD içindeki JFIF segmentine erişim sağlar. Bunları kaynak dosyanızın en üstünde içe aktarın.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Adım 2: PSD görüntüsünü yükle
Dosya yolunu yapıcıya geçirerek bir `PsdImage` örneği oluşturun. PsdImage, Photoshop belgesini modelleyen Aspose.PSD sınıfıdır. Bu, belge meta verilerini yüklerken piksel verisini akış olarak işler.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Adım 3: görüntü kaynakları üzerinde döngü
`Resources` koleksiyonunda bir `JfifResource` arayın. Bulunduğunda, küçük resim bayt dizisini yeni JPEG‑kodlu önizleme ile değiştirebilirsiniz.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Adım 4: küçük resim verisini ayarla
Herhangi bir görüntü‑işleme kütüphanesi kullanarak küçük bir JPEG küçük resmi (ör. 120 × 120 px) oluşturun, ardından elde edilen bayt dizisini `jfifResource.ThumbnailData`'ya atayın.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Adım 5: değiştirilmiş görüntüyü kaydet
`PsdImage` nesnesinin `save` metodunu çağırın, çıktı yolunu ve istenen formatı belirtin. JFIF segmenti artık yeni küçük resmi içeriyor.

```java
image.save(dataDir + "output.psd");
```

## Yaygın sorunlar ve çözümler
- **Küçük resim görüntüleyicilerde görünmüyor:** Küçük resim verisinin geçerli bir JPEG bayt dizisi olduğundan ve boyutlarının JFIF spesifikasyonunda desteklenen maksimum 256 × 256 px içinde olduğundan emin olun.
- **Büyük PSD'lerde OutOfMemoryError:** Bellek tüketimini düşük tutmak için akış modunu etkinleştiren `PsdImage.load(inputStream, true)` kullanın.
- **Yanlış kaynak türü:** Değiştirdiğiniz kaynağın gerçekten bir `JfifResource` olduğundan emin olun; `ExifResource` gibi diğer kaynaklar küçük resim görüntülenmesini etkilemez.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, geliştiricilerin Adobe Photoshop gerektirmeden Photoshop PSD dosyalarını oluşturmasını, düzenlemesini, dönüştürmesini ve render etmesini sağlayan ticari bir kütüphanedir.

**S: Aspose.PSD for Java için daha fazla belgeyi nerede bulabilirim?**  
C: Ayrıntılı belgeler [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/) adresinde bulunabilir.

**S: Aspose.PSD for Java ticari kullanım için uygun mu?**  
C: Evet, Aspose.PSD for Java ticari olarak kullanılabilir. Lisansı [Aspose.PSD's purchase page](https://purchase.aspose.com/buy) üzerinden satın alabilirsiniz.

**S: Aspose.PSD for Java'ı satın almadan önce deneyebilir miyim?**  
C: Evet, ücretsiz deneme sürümünü [Aspose.PSD's trial download page](https://releases.aspose.com/) adresinden indirebilirsiniz.

**S: Aspose.PSD for Java için destek nasıl alınır?**  
C: Destek için [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

**Son Güncelleme:** 2026-09-28  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose PSD for Java kullanarak PSD Dosyalarına IOPA Kaynağı Ekle](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Görüntüye İmza Ekle – Aspose.PSD for Java ile Kanvasa Çiz](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Aspose.PSD for Java ile Belirli Bir Açıda Görüntüyü Döndürme](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}