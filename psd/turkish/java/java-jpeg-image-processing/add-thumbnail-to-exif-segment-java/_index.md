---
date: 2026-01-22
description: Aspose.PSD for Java kullanarak Java EXIF küçük resim öğreticisini öğrenin
  ve EXIF meta verilerine küçük resimler eklerken JPEG kalitesini nasıl ayarlayacağınızı
  keşfedin.
linktitle: Add Thumbnail to EXIF Segment in Java
second_title: Aspose.PSD Java API
title: Java EXIF Küçük Resim Öğreticisi – Küçük Resmi EXIF Segmentine Ekle
url: /tr/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java EXIF Küçük Resim Öğreticisi – EXIF Segmentine Küçük Resim Ekleme

## Giriş
Bu **java exif thumbnail tutorial** içinde, Aspose.PSD for Java kullanarak bir PSD dosyasının EXIF segmentine ön izleme küçük resmi yerleştirmek için gereken tam adımları inceleyeceğiz. Küçük bir resim eklemek yalnızca görüntü meta verilerini zenginleştirmekle kalmaz, aynı zamanda galerilerde veya dosya gezginlerinde kullanıcıya hızlı bir görsel ipucu sunar. Bu rehberin sonunda, küçük resimlerin neden önemli olduğunu, jpeg kalitesini java nasıl ayarlayacağınızı ve güncellenmiş dosyayı diske nasıl kaydedeceğinizi anlayacaksınız.

## Hızlı Yanıtlar
- **Bu öğretici neyi kapsıyor?** Aspose.PSD for Java ile bir PSD görüntüsünün EXIF segmentine küçük resim ekleme.  
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java (resmi Aspose sitesinden indirin).  
- **Lisans gerekli mi?** Üretim kullanımı için geçici veya tam lisans gereklidir.  
- **JPEG kalitesini kontrol edebilir miyim?** Evet – `JpegOptions` kullanarak jpeg quality java ayarlayabilirsiniz.  
- **Uygulama ne kadar sürer?** Temel bir küçük resim ekleme işlemi genellikle 10 dakikadan az sürer.

## Java EXIF Küçük Resim Öğreticisi Nedir?
EXIF küçük resmi, görüntünün meta verileri içinde depolanan küçük bir JPEG ön izlemesidir. Uygulamalar, tam çözünürlüklü görüntüyü yüklemeden mini bir versiyon göstererek ön izlemeleri hızlandırır ve bellek kullanımını azaltır.

## Java EXIF Küçük Resmi Neden Kullanmalı?
- **Dosya yöneticileri ve web galerilerinde daha hızlı ön izlemeler.**  
- **Görüntü listeleri aktarılırken daha az bant genişliği kullanımı.**  
- **Büyük PSD dosyalarıyla çalışan fotoğrafçılar ve geliştiriciler için geliştirilmiş kullanıcı deneyimi.**

## Ön Koşullar
Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Java programlamaya temel aşinalık.  
- Java Development Kit (JDK) yüklü.  
- IntelliJ IDEA veya Eclipse gibi bir IDE.  
- Aspose.PSD for Java kütüphanesi – [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/) adresinden indirin.

## Paketleri İçe Aktarma
İlk olarak, Aspose.PSD ve Java’dan gerekli sınıfları içe aktarın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Adım 1: PSD Görüntüsünü Yükleme
PSD dosyasını bir `PsdImage` nesnesine yükleyin, böylece kaynaklarıyla çalışabilirsiniz.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## Adım 2: Görüntü Kaynaklarını Döngüyle İşleme
Mevcut küçük resim kaynaklarını bulmak için görüntünün kaynak koleksiyonunu tarayın.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## Java’da JPEG kalitesini nasıl ayarlarsınız
Küçük resim görüntüsünün sıkıştırma seviyesini kontrol etmeniz gerekiyorsa, JPEG kalite ayarlarını değiştirebilirsiniz. İşte **set jpeg quality java** anahtar kelimesinin doğal olarak yer aldığı yer.

## Adım 3: Küçük Resim Verisini Ayarlama
Bir `JpegOptions` örneği oluşturun ve istenen kaliteyi (0‑100) ayarlayın. 100 kalite, maksimum detayı korur.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## Adım 4: Görüntüyü Kaydetme
Küçük resmi ve diğer EXIF verilerini güncelledikten sonra PSD dosyasını diske kaydedin.

```java
image.save(dataDir + "output.psd");
```

## Sonuç
Bu **java exif thumbnail tutorial**, Aspose.PSD for Java kullanarak bir PSD dosyasının EXIF segmentine ön izleme küçük resmi yerleştirmenin basit bir yolunu gösterir. jpeg quality java kontrolü sayesinde dosya boyutu ile görsel sadakati dengeleyebilir, son kullanıcılar için daha akıcı bir deneyim sunabilirsiniz.

## Sıkça Sorulan Sorular
**S: EXIF meta verileri nedir?**  
C: EXIF meta verileri, dijital görüntülerde kamera ayarları, tarih, konum ve diğer detayları içeren gömülü bilgilerdir.

**S: EXIF’e küçük resim eklemek neden önemli?**  
C: Küçük resim eklemek, tam boyutlu dosyayı yüklemeden hızlı görüntü ön izlemeleri sağlayarak kullanıcı deneyimini iyileştirir.

**S: Aspose.PSD for Java’yı nereden indirebilirim?**  
C: Aspose.PSD for Java’yı [buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.

**S: Aspose.PSD için geçici bir lisans nasıl alınır?**  
C: Aspose.PSD için geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**S: Aspose.PSD desteği nasıl alınır?**  
C: Destek için [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

---

**Son Güncelleme:** 2026-01-22  
**Test Edilen Versiyon:** Aspose.PSD for Java (en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}