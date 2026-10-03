---
date: 2026-10-03
description: Aspose.PSD kullanarak Java'da PSD'den küçük resmi nasıl çıkaracağınızı
  öğrenin. Bu adım adım kılavuz, kurulum, kod parçacıkları ve küçük resmi JPEG görüntüsü
  olarak kaydetmeyi kapsar.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Java'da PSD'den küçük resim çıkarma
og_description: Aspose.PSD ile Java'da PSD'den küçük resmi nasıl çıkaracağınızı öğrenin.
  Bu kılavuz, kurulum, dosyayı yükleme, küçük resmi çıkarma ve JPEG görüntüsü olarak
  kaydetme adımlarını size gösterir.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Aspose.PSD kullanarak Java'da PSD'den küçük resim çıkarma
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Java'da PSD'den küçük resim çıkarma
url: /tr/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da PSD'den Küçük Resim Çıkarma

## Giriş
Bir PSD dosyasından küçük resim çıkarmak, tam çözünürlüklü görüntüyü yüklemeden hızlı ön izlemeler oluşturmanızı sağlar. Java'da Aspose.PSD bu süreci basit ve yüksek performanslı hâle getirir. Bu öğreticide, kütüphaneyi nasıl kuracağınızı, küçük resim kaynağını nasıl bulacağınızı ve JPEG dosyası olarak nasıl kaydedeceğinizi öğreneceksiniz — sadece birkaç satır kodla.

## Hızlı Yanıtlar
- **PSD küçük resimlerini hangi kütüphane yönetir?** Aspose.PSD for Java.
- **Gerekli kod satırı sayısı nedir?** Yükleme, çıkarma ve kaydetme için yaklaşık beş satır.
- **Büyük PSD dosyalarından küçük resim çıkarabilir miyim?** Evet, Aspose.PSD tam bellek yüklemesi yapmadan 500 MB'a kadar dosyaları işleyebilir.
- **Geliştirme için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.
- **Hangi çıktı formatları destekleniyor?** Çıkarılan küçük resim JPEG, PNG veya BMP olarak kaydedilebilir.

## PSD'den Küçük Resim Çıkarma Nedir?
PSD'den küçük resim çıkarma, bir Photoshop (PSD) belgesine gömülü olan küçük ön izleme görüntüsünü okuma sürecidir. Bu ön izleme bir kaynak olarak depolanır ve kataloglama veya gösterim amaçları için bağımsız olarak kaydedilebilir. Küçük resim genellikle tam boyutlu görüntüyü yüklemeden hızlı bir görsel özet sunmak için uygulamalar tarafından kullanılan düşük çözünürlüklü bir temsildir.

## Bu görev için Aspose.PSD neden kullanılmalı?
Aspose.PSD **30+ görüntü formatını** destekler ve **500 MB**'a kadar PSD dosyalarını, kaynakları talep üzerine okuduğu için düşük bellek kullanımıyla işleyebilir. API ayrıca güçlü hata yönetimi sağlar, böylece bozuk dosyalardan bile güvenilir bir şekilde küçük resim çıkarabilirsiniz.

## Önkoşullar
- Java Development Kit (JDK) yüklü.
- Aspose.PSD for Java kütüphanesi [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/) adresinden indirildi.
- Java sözdizimi ve proje kurulumu hakkında temel bilgi.

## Java'da bir PSD dosyasından küçük resim nasıl çıkarılır?
PSD dosyasını `PsdImage` ile yükleyin, `ThumbnailResource` öğesini bulun ve görüntü verisini JPEG olarak kaydedin. Aspose.PSD düşük seviyeli ayrıştırmayı soyutladığı için yalnızca `getResources()` çağırıp ardından çıkarılan görüntünün `save()` metodunu kullanmanız yeterlidir. Bu yaklaşım, dosya boyutu ne olursa olsun küçük resim içeren herhangi bir PSD için çalışır.

## Paketleri İçe Aktarma
`Image` görüntüleri yüklemek için temel sınıftır. `PsdImage` bir PSD belgesini temsil eder. `ThumbnailResource` ve `Thumbnail4Resource` küçük resim kaynaklarını temsil eder. `JpegOptions` JPEG kaydetme seçeneklerini belirtir.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Adım 1: PSD dosyasını yükleyin
İlk olarak, PSD dosyanıza işaret eden bir `PsdImage` örneği oluşturun. Yapıcı yalnızca başlığı ve gerekli kaynakları okur, böylece bellek kullanımı en düşük seviyede tutulur.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

`"Your_Document_Directory/"` ifadesini PSD dosyanızın bulunduğu klasör yolu ile, `"your_file.psd"` ifadesini ise PSD dosyanızın adıyla değiştirin.

## Adım 2: Görüntü kaynakları üzerinde döngü
Aspose.PSD, küçük resimleri görüntünün kaynak koleksiyonundaki `ThumbnailResource` nesneleri olarak depolar. Koleksiyon içinde döngü yapın, kaynak tipini kontrol edin ve karşılaştığınız ilk küçük resmi yakalayın.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Adım 3: Çıkarılan küçük resmi kaydet
Küçük resim görüntüsüne sahip olduğunuzda, `save` metodunu çağırarak diske yazın. JPEG, PNG veya BMP seçeneklerinden birini tercih edebilirsiniz; JPEG web ön izlemeleri için en yaygın formattır.

## Adım 4: Farklı küçük resim türlerini işleme
Bir PSD birden fazla küçük resim çeşidi (ör. `Thumbnail4Resource`) içeriyorsa, yineleme mantığını her tip için kontrol edecek şekilde genişletin. API, her kaynak için ayrı sınıflar sunar ve ihtiyacınız olan çözünürlüğü seçmenize olanak tanır.

## Yaygın sorunlar ve çözümler
- **Küçük resim bulunamadı:** Tüm PSD dosyaları ön izleme içermez. Kaynak dosyayı Photoshop'un “File → File Info” panelinden doğrulayın.
- **Desteklenmeyen format hatası:** En son Aspose.PSD sürümünü kullandığınızdan emin olun; eski sürümler yeni küçük resim kaynak türlerini içermeyebilir.
- **Büyük dosyalarda bellek yetersizliği:** Yalnızca küçük resim gerektiğinde tam görüntü verisini yüklememek için `PsdImage.load(..., LoadOptions)` ve `LoadOptions.setLoadResourcesOnly(true)` kullanın.

## Sıkça Sorulan Sorular

**S: Aspose.PSD nedir?**  
C: Aspose.PSD, Adobe Photoshop gerektirmeden PSD ve diğer raster görüntü formatlarının programatik olarak oluşturulmasını, manipüle edilmesini ve dönüştürülmesini sağlayan bir Java kütüphanesidir.

**S: Aspose.PSD for Java hakkında daha fazla belgeyi nereden bulabilirim?**  
C: Ayrıntılı API referansları ve örnekler için [documentation](https://reference.aspose.com/psd/java/) sayfasına bakabilirsiniz.

**S: Aspose.PSD'yi satın almadan önce ücretsiz denemek mümkün mü?**  
C: Evet, kütüphanenin yeteneklerini değerlendirmek için bir [free trial](https://releases.aspose.com/) indirebilirsiniz.

**S: Aspose.PSD için geçici bir lisans nasıl alınır?**  
C: Geçici lisanslar [temporary license](https://purchase.aspose.com/temporary-license/) sayfasından temin edilebilir.

**S: Aspose.PSD ticari kullanım için uygun mu?**  
C: Evet, Aspose.PSD lisans koşulları kapsamında hem kişisel hem de ticari projelerde kullanılabilir.

---

**Son Güncelleme:** 2026-10-03  
**Test Edilen Sürüm:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java ile PSD'yi Raster Görüntü Formatlarına Dönüştürme](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Aspose.PSD Java ile PSD'yi JPEG Olarak Kaydet ve RGB Renk Desteği](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandır – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}