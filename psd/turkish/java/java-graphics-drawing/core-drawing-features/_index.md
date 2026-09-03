---
date: 2026-09-03
description: Aspose.PSD kullanarak Java'da PSD'yi BMP'ye nasıl dönüştüreceğinizi öğrenin
  ve gradient uygulama ve rectangle oluşturma gibi temel çizim özelliklerini keşfedin.
keywords:
- convert PSD to BMP
- how to draw PSD
- apply gradient PSD
- create rectangle PSD
lastmod: 2026-09-03
linktitle: Java ile PSD'yi BMP'ye dönüştürme ve çizim yapma
og_description: Aspose.PSD ile Java'da PSD'yi BMP'ye dönüştürün. Bu rehber, PSD dosyalarını
  yükleme, pixel'leri işleme, gradient uygulama, rectangle oluşturma ve BMP olarak
  verimli bir şekilde kaydetme adımlarını adım adım gösterir.
og_image_alt: 'Tutorial: converting PSD to BMP and drawing shapes in Java using Aspose.PSD'
og_title: Java'da PSD'yi BMP'ye Dönüştürme – Core Drawing Guide
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to convert PSD to BMP in Java using Aspose.PSD, and discover
    core drawing features like applying gradients and creating rectangles.
  headline: How to convert PSD to BMP and draw with Java
  type: TechArticle
- questions:
  - answer: Yes, the library fully supports layered PSD files, including transparency,
      blending modes, and layer effects.
    question: Can Aspose.PSD for Java handle layers and transparency in PSD files?
  - answer: Absolutely. You can automate batch jobs by iterating over a folder, loading
      each PSD, applying the same drawing logic, and saving as BMP or any other supported
      format.
    question: Is Aspose.PSD for Java suitable for batch processing of PSD files?
  - answer: Besides PSD, the API handles BMP, PNG, JPEG, TIFF, GIF, and over 20 additional
      raster formats for both input and output.
    question: Does Aspose.PSD for Java support multiple image formats other than PSD?
  - answer: Visit the [Aspose.PSD temporary license](https://purchase.aspose.com/temporary-license/)
      page for obtaining a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Explore the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for
      community support, tips, and additional resources.
    question: Where can I find more help and resources for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
title: Java ile PSD'yi BMP'ye dönüştürme ve çizim yapma
url: /tr/java/java-graphics-drawing/core-drawing-features/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi BMP'ye Dönüştürme ve Java ile Çizme

## Giriş
Aspose.PSD for Java, Adobe Photoshop PSD dosyalarının programlı olarak oluşturulmasını, düzenlenmesini ve dönüştürülmesini sağlayan bir Java kütüphanesidir. Bu öğreticide **PSD'yi BMP'ye dönüştürmeyi** öğrenecek ve **PSD katmanlarını çizme, degrade uygulama ve dikdörtgenler oluşturma** gibi temel çizim özelliklerini doğrudan Java kodundan keşfedeceksiniz. Bu yetenekleri ustalaşmak, Photoshop yüklü olmadan karmaşık görüntü işleme boru hatlarını otomatikleştirmenizi sağlar.

## Hızlı Yanıtlar
- **PSD'yi BMP'ye tek satır kodla dönüştürebilir miyim?** Evet – PSD'yi `PsdImage` ile yükleyin ve `save("output.bmp", SaveFormat.Bmp)` çağırın.  
- **Aspose.PSD'nin hangi sürümü gerekiyor?** En son 24.x sürümü tüm temel çizim API'lerini destekler.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz geçici bir lisans çalışır; üretim için tam lisans gereklidir.  
- **Hangi Java sürümleri destekleniyor?** Java 8'den Java 21'e kadar tam uyumludur.  
- **Birçok PSD dosyasını toplu işleyebilir miyim?** Kesinlikle – bir dizin üzerinde döngü yapıp aynı dönüşüm mantığını yeniden kullanabilirsiniz.

## Java'da PSD'yi BMP'ye Dönüştürme
Kaynak PSD'yi yükleyin, isteğe bağlı olarak piksellerini veya çizim katmanlarını değiştirin ve ardından BMP dosyası olarak kaydedin. Dönüşüm bellek içinde gerçekleşir, bu sayede ara dosyalardan kaçınır ve binlerce görüntüyü verimli bir şekilde işleyebilirsiniz. Aspose.PSD verileri akış olarak işler, bu da çok sayfalı dosyaların bile yığın (heap) alanını tüketmeden işlenebileceği anlamına gelir.

### Aspose.PSD for Java'da temel çizim özellikleri nelerdir?
Kütüphane, programlı olarak **PSD şekilleri çizmeyi**, **degrade doldurmaları uygulamayı** ve **dikdörtgen katmanları oluşturmayı** sağlayan tam bir çizim ilkel seti sunar. Bu API'ler, Photoshop'un kullandığı aynı piksel‑seviyesi motoru üzerinde çalışır ve formatlar arasında görsel tutarlılığı garanti eder.

## Önkoşullar
Başlamadan önce aşağıdakilerin hazır olduğundan emin olun:

### Java geliştirme ortamı
Java Development Kit'i (JDK) [Oracle'ın web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) yükleyin. Öğretici JDK 11 ile test edilmiştir, ancak JDK 8+ herhangi bir sürüm çalışır.

### Aspose.PSD for Java kurulumu
1. **Aspose.PSD for Java'yi indirin** – [indirme sayfasına](https://releases.aspose.com/psd/java/) gidin ve en son ZIP arşivini alın.  
2. **JAR dosyalarını projenize ekleyin** – `aspose-psd.jar` ve bağımlılıklarını sınıf yolunuza (classpath) kopyalayın veya ürün belgelerinde açıklandığı gibi Maven/Gradle üzerinden referans verin.

Artık kodlamaya başlamak için ihtiyacınız olan her şeye sahipsiniz.

## Paketleri içe aktar
Aspose.PSD ile çalışmak için temel ad alanlarını (namespace) içe aktarmanız gerekir. Bu içe aktarmalar, görüntü yükleme, piksel manipülasyonu ve çizim yardımcı programlarına erişim sağlar.  
```java
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Adım 1: PSD görüntüsü yükleme
İlk adım, kaynak dosyayı bellek içinde temsil eden bir `PsdImage` örneği oluşturmaktır. Bu nesne, katmanlara, kanallara ve tek tek piksellere okuma/yazma erişimi sağlar.  
```java
String dataDir = "Your Document Directory";
String loadpath = dataDir + "sample.psd";
// Load the PSD image
PsdImage image = new PsdImage(loadpath);
```

## Adım 2: Pikselleri manipüle et
PSD yüklendikten sonra piksel verilerini değiştirebilir, yeni şekiller çizebilir veya degrade doldurmaları uygulayabilirsiniz. Çizim API'si, Photoshop'un araçlarını yansıtır ve sadece birkaç metod çağrısıyla **PSD dikdörtgenleri çizmeyi** veya **degrade PSD efektleri uygulamayı** sağlar.  
```java
// Load pixels of a specific region (e.g., a 100x10 rectangle starting from top-left corner)
int[] pixels = image.loadArgb32Pixels(new Rectangle(0, 0, 100, 10));
// Modify the pixels (e.g., apply a gradient effect)
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = i;  // Apply your desired manipulation logic here
}
```

## Adım 3: Değiştirilmiş görüntüyü kaydet
Düzenlemeyi bitirdikten sonra `save` metodunu çağırın ve `SaveFormat.Bmp` belirtin. Kütüphane, yaptığınız görsel değişiklikleri koruyan bir BMP dosyası yazar ve **PSD'yi BMP'ye dönüştür** iş akışını tamamlar.  
```java
String outpath = dataDir + "CoreDrawingFeatures.bmp";
// Save modified pixels back to the image
image.saveArgb32Pixels(new Rectangle(0, 0, 100, 10), pixels);
// Save the image to BMP format
image.save(outpath, new BmpOptions());
```

## Yaygın sorunlar ve hata ayıklama
- **Bellek yetersizliği hataları** – Aspose.PSD verileri akış olarak işler; ancak, çok büyük PSD'ler (>2 GB) hâlâ ek JVM yığını (`-Xmx4g`) gerektirebilir.  
- **Renk profili uyumsuzlukları** – Çıktı BMP soluk görünüyorsa, kaydetmeden önce `psdImage.getColorProfile()` çağırarak kaynak PSD'nin ICC profilinin korunduğundan emin olun.  
- **Dönüşüm sonrası eksik katmanlar** – Kaydetmeden önce `layer.isVisible()` kontrol ederek gizli katmanların atılmadığını doğrulayın.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java PSD dosyalarındaki katmanları ve şeffaflığı işleyebilir mi?**  
**C:** Evet, kütüphane katmanlı PSD dosyalarını, şeffaflık, karıştırma modları ve katman efektleri dahil olmak üzere tam olarak destekler.

**S: Aspose.PSD for Java PSD dosyalarını toplu işleme için uygun mu?**  
**C:** Kesinlikle. Bir klasör üzerinde yineleme yaparak, her PSD'yi yükleyip aynı çizim mantığını uygulayabilir ve BMP ya da başka bir desteklenen formatta kaydedebilirsiniz.

**S: Aspose.PSD for Java PSD dışındaki birden fazla görüntü formatını destekliyor mu?**  
**C:** PSD dışında, API BMP, PNG, JPEG, TIFF, GIF ve giriş ve çıkış için 20'den fazla ek raster formatını da işler.

**S: Aspose.PSD for Java için geçici bir lisans nasıl alınır?**  
**C:** Geçici bir lisans almak için [Aspose.PSD geçici lisans](https://purchase.aspose.com/temporary-license/) sayfasını ziyaret edin.

**S: Aspose.PSD for Java ile ilgili daha fazla yardım ve kaynak nerede bulunabilir?**  
**C:** Topluluk desteği, ipuçları ve ek kaynaklar için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) keşfedin.

---

**Son Güncelleme:** 2026-09-03  
**Test Edilen:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java'da Radial Degrade Efektleri Oluşturma](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Aspose.PSD for Java kullanarak PSD'de Dikdörtgen Çizme ve Kaydetme](/psd/java/basic-image-operations/simple-drawing/)
- [Aspose.PSD for Java ile PSD'yi Raster Görüntü Formatlarına Dönüştürme](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}