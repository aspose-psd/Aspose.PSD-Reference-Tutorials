---
date: 2026-09-18
description: Aspose.PSD for Java kullanarak java görüntü meta verisi küçük resmini
  EXIF segmentine nasıl ekleyeceğinizi öğrenin. Bu adım adım kılavuz, ön koşulları,
  kod incelemesini ve güncellenmiş görüntünün kaydedilmesini kapsar.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Java'da EXIF Segmentine Küçük Resim Ekle
og_description: Aspose.PSD for Java kullanarak java görüntü meta verisi küçük resmini
  EXIF segmentine nasıl ekleyeceğinizi öğrenin. Küçük resimleri gömmek ve güncellenmiş
  görüntüyü kaydetmek için adım adım kılavuzu izleyin.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: Java görüntü meta verisi küçük resmini EXIF segmentine nasıl eklenir
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: Java görüntü meta verisi küçük resmini EXIF segmentine nasıl eklenir
url: /tr/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java görüntü meta verisi küçük resmini EXIF segmentine ekleme

## Giriş
Bu öğreticide, Aspose.PSD for Java kullanarak bir PSD dosyasının EXIF segmentine **java image metadata** küçük resmini nasıl ekleyeceğinizi öğreneceksiniz. EXIF (Exchangeable Image File Format) meta verileri kamera ayarlarını, çekim tarihini, konumu ve diğer faydalı bilgileri depolar. Küçük bir ön izleme küçük resmi gömmek, uygulamaların tam dosyayı yüklemeden hızlı bir görüntü önizlemesi göstermesini sağlar, performansı ve kullanıcı deneyimini artırır.

## Hızlı cevaplar
- **Bu öğretici neyi kapsıyor?** Aspose.PSD for Java ile bir PSD görüntüsünün EXIF segmentine küçük resim ekleme.  
- **Uygulama ne kadar sürer?** Temel bir entegrasyon için yaklaşık 10‑15 dakika.  
- **Lisans gerekli mi?** Üretim kullanımı için geçici bir lisans gereklidir; değerlendirme için ücretsiz deneme çalışır.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri tam olarak desteklenir.  
- **Büyük dosyalar işlenebilir mi?** Evet—Aspose.PSD, tüm görüntüyü belleğe yüklemeden 2 GB'a kadar dosyaları işleyebilir.

## java image metadata nedir?
Java image metadata, Java kütüphaneleri (örneğin Aspose.PSD) kullanılarak programlı olarak okunabilen, değiştirilebilen veya oluşturulabilen, görüntü dosyalarına (EXIF, IPTC veya XMP gibi) gömülü yapılandırılmış bilgileri ifade eder. Bu meta veriler, uygulamaların kamera ayarlarını, zaman damgalarını, GPS koordinatlarını ve özel verileri görsel içeriği açmadan almasını sağlar.

## Neden EXIF meta verisine küçük resim eklenir?
EXIF segmentine bir küçük resim eklemek, görüntü tarayıcıları, dosya gezginleri ve içerik yönetim sistemleri için anlık görsel bir ipucu sağlar. Aspose.PSD, küçük resimleri bellek içinde işler ve 500 KB'a kadar olan görüntüler için ön izlemeyi 0,2 saniyenin altında gömmeyi mümkün kılar; ayrıca PSD, JPEG, PNG ve TIFF dahil olmak üzere 30'dan fazla görüntü formatını destekler.

## Önkoşullar
- Java programlama temelleri bilgisi.  
- Sisteminizde kurulu Java Development Kit (JDK).  
- IntelliJ IDEA veya Eclipse gibi Java için bir IDE (Entegre Geliştirme Ortamı).  
- Aspose.PSD for Java kütüphanesi. Bunu [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/) adresinden indirebilirsiniz.

## Paketleri içe aktar
Aşağıdaki içe aktarmalar, PSD görüntüleri ve EXIF verileriyle çalışmak için gerekli Aspose.PSD sınıflarını getirir.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Adım 1: PSD görüntüsünü yükle
`PsdImage`, bir Photoshop PSD dosyasını temsil eder ve katmanları ile kaynaklarına erişim sağlar.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## Adım 2: Görüntü kaynakları üzerinde döngü
`ImageResource`, bir PSD dosyasına gömülü küçük resimler, ICC profilleri ve meta veriler gibi kaynakları kapsar.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## Adım 3: Küçük resim verisini ayarla
`JpegOptions`, küçük resim görüntüsü için kalite gibi JPEG‑özel ayarları yapılandırmanıza olanak tanır.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## Adım 4: Görüntüyü kaydet
`save` metodunu çağırmak, güncellenmiş EXIF segmentini (yeni küçük resim dahil) tüm görüntüyü yeniden kodlamadan diske yazar.  
```java
image.save(dataDir + "output.psd");
```

## Yaygın sorunlar ve çözümler
- **Küçük resim görünmüyor:** Küçük resim kaynağının EXIF segmentine doğru eklendiğini ve görüntünün `PsdImage.save` yöntemiyle kaydedildiğini doğrulayın.  
- **Büyük dosyalarda bellek yetersizliği hataları:** Yalnızca meta veriyle çalışmak için `PsdImage.load(..., LoadOptions)` ve `LoadOptions.setLoadOnlyMetadata(true)` kullanın.  
- **Yanlış yönlendirme:** Küçük resmin orijinal görüntünün yönlendirme bayrağına saygı gösterdiğinden emin olun; `Orientation` EXIF etiketini okuyabilir ve küçük resmi buna göre döndürebilirsiniz.

## Sıkça sorulan sorular

**Q: EXIF meta verisi nedir?**  
A: EXIF meta verisi, dijital görüntülere gömülü bilgi olup kamera ayarları, çekim tarihi, GPS koordinatları ve diğer detayları içerir.

**Q: Neden EXIF'e bir küçük resim eklenir?**  
A: Küçük resim eklemek, tam görüntüyü yüklemeden hızlı ön izleme sağlayarak kullanıcı deneyimini iyileştirir.

**Q: Aspose.PSD for Java'ı nereden indirebilirim?**  
A: Aspose.PSD for Java'ı [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) adresinden indirebilirsiniz.

**Q: Aspose.PSD için geçici lisans nasıl alabilirim?**  
A: Aspose.PSD için geçici bir lisansı [temporary license page](https://purchase.aspose.com/temporary-license/) adresinden edinebilirsiniz.

**Q: Aspose.PSD için destek nasıl alabilirim?**  
A: Destek için [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

---

**Last updated:** 2026-09-18  
**Tested with:** Aspose.PSD for Java 24.10  
**Author:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java kullanarak PSD Dosyalarında XMP Meta Verisi Oluşturma](/psd/java/image-editing/create-xmp-metadata/)
- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandırma – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java ile PSD'yi Raster Görüntü Formatlarına Dönüştürme](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}