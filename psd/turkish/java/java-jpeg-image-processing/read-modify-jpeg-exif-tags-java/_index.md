---
date: 2026-10-03
description: Bu step‑by‑step rehberde, Aspose.PSD for Java ile java kullanarak görüntü
  meta verilerini okuma ve JPEG EXIF etiketlerini değiştirmeyi öğrenin; görüntü meta
  verileriyle verimli çalışan geliştiriciler için mükemmeldir.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Java'da JPEG EXIF Etiketlerini Okuma ve Değiştirme
og_description: Aspose.PSD for Java ile java kullanarak görüntü meta verilerini okuma
  ve JPEG EXIF etiketlerini değiştirmeyi öğrenin. Bu rehber, EXIF bilgilerini çıkarmak
  ve güncellemek için step‑by‑step kod örneklerini gösterir.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: java ile görüntü meta verilerini okuma ve JPEG EXIF etiketlerini değiştirme
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: java ile görüntü meta verilerini okuma ve JPEG EXIF etiketlerini değiştirme
url: /tr/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JPEG EXIF etiketlerini Java'da okuyun ve değiştirin

## Giriş
JPEG dosyalarından **java read image metadata**'yi programlı bir şekilde okumanız ve değiştirmeniz gerekiyorsa, doğru yerdesiniz. Bu öğreticide Aspose.PSD for Java kullanarak EXIF etiketlerini çıkarmayı ve güncellemeyi adım adım göstereceğiz. Sonunda kamera detaylarını, yönlendirmeyi ve özel alanları alabilecek ve bunları dosyaya geri yazabileceksiniz — tüm bunlar bir grafik editörüne ihtiyaç duymadan.

## Hızlı cevaplar
- **Java'da JPEG EXIF'i hangi kütüphane yönetir?** Aspose.PSD for Java.
- **EXIF'i okumak için kaç satır kod gerekir?** Görüntüyü yükledikten sonra yaklaşık üç satır.
- **EXIF etiketlerini değiştirebilir misiniz?** Evet, herhangi bir standart veya özel etiketi değiştirebilir ve sonucu kaydedebilirsiniz.
- **Desteklenen görüntü formatları?** PSD, JPEG, PNG, TIFF ve BMP dahil olmak üzere 150'den fazla format.
- **Minimum Java sürümü?** Java 7 veya üzeri.

## Neden Aspose.PSD for Java kullanmalısınız?
Aspose.PSD, **150+ görüntü formatını** destekler ve **2 GB**'a kadar dosyaları belgenin tamamını belleğe yüklemeden işleyebilir, bu da büyük fotoğraf koleksiyonlarında hızlı ve düşük bellekli metadata işlemleri sağlar. Ayrıca EXIF, IPTC ve XMP verilerini okuma ve yazma için basit bir API sunar, bu da binlerce görüntünün toplu işlenmesini verimli ve güvenilir kılar.

## Önkoşullar
1. **Java Development Kit (JDK)** – JDK 11 veya daha yeni bir sürümünüz olduğundan emin olun. Bunu [Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) üzerinden indirebilirsiniz.  
2. **Aspose.PSD for Java kütüphanesi** – En son JAR dosyasını [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) edinin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Temel Java bilgisi** – Projeler oluşturma ve harici JAR'lar ekleme konusunda rahat olmalısınız.

## Java read image metadata nedir?
Java read image metadata, Java kodu kullanarak görüntü dosyalarının içinde depolanmış EXIF, IPTC ve XMP gibi gömülü bilgilere programlı olarak erişme sürecini ifade eder. Bu metadata kamera ayarları, zaman damgaları, GPS koordinatları, telif hakkı bildirimleri ve kullanıcı yorumları gibi bilgileri içerebilir ve uygulamaların görüntüleri açıklayıcı verilerine göre düzenlemesine, aramasına ve manipüle etmesine olanak tanır.

## Paketleri içe aktar
İlk olarak, Aspose.PSD JAR dosyasını projenizin sınıf yoluna ekleyin ve gerekli sınıfları içe aktarın.

`com.aspose.psd` paketi, görüntüleri yüklemek ve kaynaklarına erişmek için temel API'yi sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## JPEG dosyalarından Java'da görüntü metadata'sı nasıl okunur?
`PsdImage.load("image.jpg")` ile JPEG'i yükleyin, EXIF verisini içeren thumbnail kaynağını bulun ve ardından `ExifData.read()` çağırarak doldurulmuş bir `ExifData` nesnesi elde edin. Bu tek adımlı yaklaşım, tüm standart EXIF alanlarına ve eklediğiniz özel etiketlere tam erişim sağlar.

## Adım 1: PSD görüntüsünü yükleyin
PsdImage, bir PSD dosyasını temsil eden Aspose.PSD sınıfıdır ve kaynaklarına ve metadata'ya erişim sağlayan yöntemler sunar.  
Bu adımda, EXIF verisini okumak istediğimiz PSD görüntüsünü yükleyeceğiz. Görüntünüzün doğru dizinde olduğundan emin olun.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Adım 2: Görüntü kaynakları üzerinde döngü
ThumbnailResource, bir PSD dosyasında depolanan ve genellikle gömülü EXIF verisi içeren küçük resim görüntüsünü temsil eder.  
Görüntü yüklendikten sonra, bir sonraki adım, genellikle EXIF verisini içeren thumbnail kaynağını bulmak için kaynakları döngüyle gezmektir.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Adım 3: EXIF verisini çıkarın
JpegExifData, bir JPEG görüntüsünden çıkarılan EXIF bilgilerini tutan sınıftır ve bireysel etiketleri okumanıza ve değiştirmenize olanak tanır.  
Şimdi thumbnail kaynağımız olduğuna göre, EXIF verisini ondan çıkarabiliriz. EXIF verisi, kamera sahibinin adı, diyafram değeri, yönlendirme ve daha fazlası gibi değerli bilgileri içerir.

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

## Adım 4: EXIF verisini değiştirin
EXIF verisini okuduktan sonra, bazı alanlarını değiştirmek isteyebilirsiniz. İşte bunu nasıl yapacağınız:

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

## Adım 5: Değişiklikleri kaydedin
Son olarak, EXIF verisini değiştirdikten sonra, değişiklikleri yeni bir PSD dosyasına kaydedin.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Yaygın sorunlar ve çözümler
- **Thumbnail kaynağı eksik** – Bazı JPEG'ler EXIF'i doğrudan ana görüntü başlığında saklar. Thumbnail kaynağı yoksa, bunun yerine `image.getExifData()` kullanın.  
- **Büyük dosyalar OutOfMemoryError hatasına neden olur** – JVM'yi yeterli yığın (`-Xmx2g`) ile çalıştırdığınızdan emin olun veya `PsdImage.load(inputStream, loadOptions)` kullanarak görüntüyü akış modunda işleyin.  
- **Desteklenmeyen etiket tipleri** – Aspose.PSD tüm standart EXIF etiketlerini destekler; özel etiketler manuel bayt‑seviyesi işleme gerektirebilir.

## Sıkça sorulan sorular

**Q: EXIF verisi nedir?**  
A: EXIF (Exchangeable Image File Format) metadata, JPEG ve diğer görüntü dosyalarına gömülü kamera ayarları, zaman damgaları, GPS koordinatları ve diğer bilgileri saklar.

**Q: Aspose.PSD for Java'yı ücretsiz kullanabilir miyim?**  
A: [Aspose sürüm sayfasından](https://releases.aspose.com/) ücretsiz deneme alabilirsiniz.

**Q: Aspose.PSD for Java tüm Java sürümleriyle uyumlu mu?**  
A: Aspose.PSD for Java, Java SE 7 ve üzerini destekler.

**Q: Aspose.PSD for Java hakkında daha fazla belgeleri nereden bulabilirim?**  
A: Daha fazla detay için [belgelere](https://reference.aspose.com/psd/java/) göz atın.

**Q: Aspose.PSD for Java için desteği nasıl alabilirim?**  
A: [Aspose PSD destek forumundan](https://forum.aspose.com/c/psd/34/) destek alabilirsiniz.

## Sonuç
Bu adımları izleyerek herhangi bir JPEG'den **java read image metadata**'yi okuyabilir, ihtiyacınız olan EXIF alanlarını ayarlayabilir ve güncellenmiş veriyi dosyaya geri yazabilirsiniz — hepsi birkaç satır temiz Java kodu ile. Aspose.PSD'nin zengin API'si metadata işlemlerini güvenilir ve yüksek performanslı hâle getirir, böylece bunu toplu işleme boru hatlarına, fotoğraf yönetim araçlarına veya görüntü bilgileriyle çalışması gereken herhangi bir uygulamaya entegre edebilirsiniz.

---

**Son Güncelleme:** 2026-10-03  
**Test Edilen:** Aspose.PSD for Java 24.5  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Java'da Aspose ile Belirli EXIF Etiket Bilgilerini Oku (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Aspose.PSD for Java Kullanarak PSD Dosyalarında XMP Metadata Oluşturma](/psd/java/image-editing/create-xmp-metadata/)
- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandır – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}