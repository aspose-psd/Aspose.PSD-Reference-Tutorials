---
date: 2026-10-08
description: Aspose.PSD for Java kullanarak JFIF görüntülerinden thumbnail çıkarmayı
  öğrenin. Adım adım kılavuz, kod parçacıkları ve Java geliştiricileri için en iyi
  uygulamalar.
keywords:
- how to extract thumbnail
- how to read jfif
- java extract image metadata
lastmod: 2026-10-08
linktitle: Java'da JFIF'ten thumbnail çıkarma
og_description: Aspose.PSD for Java kullanarak JFIF görüntülerinden thumbnail çıkarmayı
  öğrenin. JFIF dosyalarını okumak ve görüntü metadata'sını verimli bir şekilde elde
  etmek için bu ayrıntılı öğreticiyi izleyin.
og_image_alt: Screenshot of Java code extracting a thumbnail from a JFIF image with
  Aspose.PSD
og_title: Java'da JFIF'ten thumbnail çıkarma – Aspose.PSD rehberi
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to extract thumbnail from JFIF images using Aspose.PSD for
    Java. Step‑by‑step guide, code snippets, and best practices for Java developers.
  headline: How to extract thumbnail from JFIF in Java
  type: TechArticle
- description: Learn how to extract thumbnail from JFIF images using Aspose.PSD for
    Java. Step‑by‑step guide, code snippets, and best practices for Java developers.
  name: How to extract thumbnail from JFIF in Java
  steps:
  - name: load the PSD image
    text: First, create a `PsdImage` object that represents the source file. This
      object gives you access to all embedded resources, including thumbnails. Replace
      `"Your Document Directory"` with the actual path to your JFIF/PSD file.
  - name: iterate over image resources
    text: Next, loop through the image’s resources collection to find the thumbnail
      entry. The thumbnail is stored as a `JfifResource` object. This loop checks
      each resource in the PSD image to find the thumbnail resource.
  - name: extract JFIF data
    text: When the thumbnail resource is found, cast it to `JfifResource` and read
      its raw JFIF byte array. You can then write the bytes to a file or process them
      in memory. If the JFIF data is present, you can extract and utilize it for your
      application.
  - name: extract EXIF data (optional)
    text: If you also need metadata such as camera model or capture date, the same
      `JfifResource` exposes an `ExifData` object. Pull the desired tags and use them
      as needed. This step allows you to retrieve and work with EXIF information associated
      with the thumbnail.
  - name: save the thumbnail (optional)
    text: Finally, write the extracted JFIF bytes to a `.jpg` file so you can view
      the thumbnail directly. Saving the thumbnail makes it easy to verify the extraction
      result.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to read, edit,
      and export PSD, JPEG, JFIF, and many other image formats programmatically.
    question: What is Aspose.PSD for Java?
  - answer: You can download Aspose.PSD for Java from the **Aspose.PSD for Java download
      page**([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)).
    question: How can I download Aspose.PSD for Java?
  - answer: Yes, you can get a free trial from the **Aspose free trial page**([https://releases.aspose.com/](https://releases.aspose.com/)).
    question: Is a free trial available?
  - answer: You can find the documentation on the **Aspose.PSD Java API reference**([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)).
    question: Where is the official documentation?
  - answer: You can get support from the Aspose.PSD community forum **Aspose PSD forum**([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).
    question: How do I obtain support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract thumbnail
- Aspose.PSD
- Java image processing
title: Java'da JFIF'ten thumbnail çıkarma
url: /tr/java/java-jpeg-image-processing/extract-thumbnail-from-jfif-java/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JFIF'ten Java'da Küçük Resim Nasıl Çıkarılır

## Giriş
Bu öğreticide, Aspose.PSD for Java kullanarak JFIF görüntülerinden **küçük resmi nasıl çıkarılır** öğreneceksiniz. Küçük resim çıkarma, büyük görüntü koleksiyonlarının hızlı ön izlemelerine ihtiyaç duyduğunuzda, galeriler oluşturduğunuzda veya çoklu ortam uygulamalarında düşük çözünürlüklü ön izlemeler gömmek istediğinizde sıkça karşılaşılan bir gereksinimdir. Kılavuzun sonunda, bir JFIF dosyasını okuyabilecek, küçük resim kaynağını bulabilecek ve gömülü görüntü verilerini sadece birkaç Java kod satırıyla elde edebileceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphane gereklidir?** Aspose.PSD for Java.
- **Hedeflenen birincil format nedir?** JFIF (JPEG File Interchange Format) thumbnails.
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme geliştirme için çalışır; üretim için ticari lisans gereklidir.
- **Kaç satır kod gereklidir?** Dört adımda yaklaşık 10‑15 satır.
- **EXIF meta verilerini de okuyabilir miyim?** Evet – aynı küçük resim kaynağı EXIF verilerini ortaya çıkarabilir.

## 'Küçük resmi nasıl çıkarılır' nedir?
**Küçük resmi nasıl çıkarılır**, bir JFIF veya PSD dosyasının içinde depolanan küçük ön izleme görüntüsünü programlı olarak elde etmek anlamına gelir. Bu ön izleme genellikle 100 × 100 px veya daha küçüktür ve tam çözünürlüklü görüntüyü yüklemeden hızlı görsel tanımlama için kullanılır.

## Neden Aspose.PSD for Java kullanmalısınız?
Aspose.PSD, **30+ görüntü formatını** (PSD, PSB, BMP, JPEG, PNG ve JFIF dahil) destekler ve tüm görüntüyü belleğe yüklemeden **2 GB**'a kadar dosyaları işleyebilir. Kütüphane, EXIF ve IPTC gibi karmaşık meta veri yapılarını yönetir ve Windows, macOS ve Linux JVM'lerinde tutarlı bir API sağlar.

## Ön Koşullar
Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Java programlama temellerine temel bilgi.
- Makinenizde yüklü JDK (Java Development Kit).
- Aspose.PSD for Java kütüphanesi. **Aspose.PSD for Java indirme sayfasından**([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)) indirebilirsiniz.
- IntelliJ IDEA veya Eclipse gibi bir bütünleşik geliştirme ortamı (IDE) kurulmuş.

## Java'da bir JFIF görüntüsünden küçük resim nasıl çıkarılır?
JFIF dosyasını yükleyin, küçük resim kaynağını bulun ve ikili verisini alın – tümü dört kısa adımda. Aşağıdaki kod parçacıkları her adımı gösterir; yalnızca yer tutucu yolu kendi görüntü dosyanızın konumuyla değiştirmeniz gerekir.

### Adım 1: PSD görüntüsünü yükle
İlk olarak, kaynak dosyayı temsil eden bir `PsdImage` nesnesi oluşturun. Bu nesne, küçük resimler dahil tüm gömülü kaynaklara erişim sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.jpeg.JFIFData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```  
`"Your Document Directory"` ifadesini JFIF/PSD dosyanızın gerçek yolu ile değiştirin.

### Adım 2: görüntü kaynakları üzerinde döngü
Sonra, küçük resim girişini bulmak için görüntünün kaynak koleksiyonunda döngü oluşturun. Küçük resim bir `JfifResource` nesnesi olarak depolanır.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "example.psd");
```  
Bu döngü, PSD görüntüsündeki her kaynağı kontrol ederek küçük resim kaynağını bulur.

### Adım 3: JFIF verisini çıkar
Küçük resim kaynağı bulunduğunda, onu `JfifResource` tipine dönüştürün ve ham JFIF bayt dizisini okuyun. Ardından baytları bir dosyaya yazabilir veya bellekte işleyebilirsiniz.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Further processing steps go here.
    }
}
```  
JFIF verisi mevcutsa, uygulamanız için çıkarabilir ve kullanabilirsiniz.

### Adım 4: EXIF verisini çıkar (isteğe bağlı)
Kamera modeli veya çekim tarihi gibi meta verilere de ihtiyacınız varsa, aynı `JfifResource` bir `ExifData` nesnesi sunar. İstediğiniz etiketleri alın ve gerektiği gibi kullanın.

```java
ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
JfifData jfif = thumbnail.getJpegOptions().getJfif();
if (jfif != null) {
    // Extract JFIF data and process.
}
```  
Bu adım, küçük resimle ilişkili EXIF bilgilerini almanızı ve üzerinde çalışmanızı sağlar.

### Adım 5: küçük resmi kaydet (isteğe bağlı)
Son olarak, çıkarılan JFIF baytlarını bir `.jpg` dosyasına yazarak küçük resmi doğrudan görüntüleyebilirsiniz.

```java
JpegExifData exif = thumbnail.getJpegOptions().getExifData();
if (exif != null) {
    // Extract EXIF data and process.
}
```  
Küçük resmi kaydetmek, çıkarma sonucunu doğrulamayı kolaylaştırır.

## Yaygın sorunlar ve sorun giderme
- **Null küçük resim kaynağı** – Bazı JFIF dosyaları gömülü bir küçük resim içermez. Kaynak görüntünün bir ön izleme içerdiğini doğrulayın veya farklı bir dosya kullanın.
- **Desteklenmeyen görüntü boyutu** – Aşırı büyük dosyalar varsayılan bellek sınırını aşabilir. `OutOfMemoryError` alırsanız, JVM yığın boyutunu `-Xmx2g` ile artırın.
- **Yanlış dosya yolu** – Yolun ileri eğik çizgi (`/`) veya Windows'ta çift ters eğik çizgi (`\\`) kullandığından emin olun.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, geliştiricilerin PSD, JPEG, JFIF ve birçok diğer görüntü formatını programlı olarak okuyup, düzenleyip, dışa aktarmasını sağlayan bir kütüphanedir.

**S: Aspose.PSD for Java nasıl indirilebilir?**  
C: Aspose.PSD for Java'yi **Aspose.PSD for Java indirme sayfasından**([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)) indirebilirsiniz.

**S: Ücretsiz deneme mevcut mu?**  
C: Evet, **Aspose ücretsiz deneme sayfasından**([https://releases.aspose.com/](https://releases.aspose.com/)) ücretsiz deneme alabilirsiniz.

**S: Resmi dokümantasyon nerede?**  
C: Dokümantasyonu **Aspose.PSD Java API referansında**([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) bulabilirsiniz.

**S: Aspose.PSD için desteği nasıl alabilirim?**  
C: Aspose.PSD topluluk forumu **Aspose PSD forumundan**([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) destek alabilirsiniz.

**S: Küçük resim dışında başka meta verileri çıkarabilir miyim?**  
C: Evet, aynı `JfifResource` EXIF, IPTC ve XMP meta verilerine erişim sağlar.

**S: Kütüphane tüm büyük işletim sistemlerinde çalışıyor mu?**  
C: Kütüphane saf Java'dır ve Windows, macOS ve Linux'ta yerel bağımlılıklar olmadan çalışır.

---

**Son Güncelleme:** 2026-10-08  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Java Jpeg Görüntü İşleme](/psd/java/java-jpeg-image-processing/)
- [Aspose.PSD for Java ile Görüntü Yeniden Boyutlandırma – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Aspose.PSD ile Basit Yeniden Boyutlandırma Nasıl Yapılır – Java Görüntü Manipülasyon Kütüphanesi](/psd/java/basic-image-operations/simple-resizing/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}