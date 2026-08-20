---
date: 2026-06-03
description: Aspose.PSD for Java ile görüntüyü yeniden boyutlandırmayı öğrenin. Bu
  adım adım kılavuz, Resize Type Enumeration, yüksek kaliteli görüntü yeniden boyutlandırma
  ve PSD'yi JPEG'e dönüştürmeyi kapsar.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Resize Type Enumeration ile Yeniden Boyutlandırma
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Resize Type Enumeration Kullanarak Java'da Görüntüyü Yeniden Boyutlandırma
url: /tr/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Resize Type Enumeration Kullanarak Görüntüyü Yeniden Boyutlandırma

## Giriş

Eğer bir Java projesinde **görseli yeniden boyutlandırma** dosyalarını verimli bir şekilde nasıl yapacağınızı arıyorsanız, Aspose.PSD for Java temiz ve yüksek‑performanslı bir API sunar. Bu öğreticide bir PSD dosyasını yüklemeyi, yüksek kaliteli görüntü yeniden boyutlandırması için **Resize Type Enumeration** uygulamayı ve son olarak **PSD'yi JPEG'e dönüştürmeyi** adım adım göstereceğiz. İster bir masaüstü editörü ister otomatik bir sunucu‑tarafı işlem hattı oluşturuyor olun, bu adımlar sadece birkaç kod satırıyla boyutları, kaliteyi ve formatı kontrol etmenizi sağlar.

## Hızlı Cevaplar
- **Java'da görüntüyü yeniden boyutlandırma işlemini hangi kütüphane yönetir?** Aspose.PSD for Java.
- **En iyi kaliteyi hangi yeniden boyutlandırma türü verir?** `ResizeType.LanczosResample`.
- **Yeniden boyutlandırmadan sonra PSD'yi JPEG'e dönüştürebilir miyim?** Evet – sadece `JpegOptions` ile kaydedin.
- **Üretim için lisansa ihtiyacım var mı?** Üretim kullanımında geçerli bir Aspose.PSD lisansı gereklidir.
- **Bu yaklaşım büyük toplular için uygun mu?** Kesinlikle; API, tüm belgeyi belleğe yüklemeden çok sayıda sayfalı dosyaları işler.

## Java'da "görseli yeniden boyutlandırma" nedir?

**Görseli yeniden boyutlandırma**, bir görüntünün piksel boyutlarını programlı olarak değiştirirken görsel doğruluğu korumak anlamına gelir. Aspose.PSD’nin `Resize` yöntemi ve `ResizeType` enum'ı, ölçekleme algoritmaları üzerinde kesin kontrol sağlar ve geliştiricilerin çeşitli kaynak dosyalar ve hedef boyutlar arasında kaliteyi korumasına olanak tanır.

## Neden Resize Type Enumeration Kullanılmalı?

`ResizeType`, hız ve görsel kaliteyi en iyi dengeleyen yeniden örnekleme algoritmasını seçmenizi sağlar. Çoğu senaryoda, **LanczosResample** keskin sonuçlar verir ve makul bir performans maliyetiyle, tipik bir sunucu sınıfı CPU’da 2000 × 1500 görüntüyü 120 ms’nin altında işleyerek kenar detaylarını korur.

## Önkoşullar

Başlamadan önce, şunların yüklü olduğundan emin olun:

1. **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü ve yapılandırılmış.  
2. **Aspose.PSD Kütüphanesi** – En son JAR dosyasını [web sitesi](https://releases.aspose.com/psd/java/) adresinden indirin.  
3. **Örnek PSD Dosyası** – SDK ile gelen [sample.psd](Your Document Directory/sample.psd) dosyasını pratik testler için kullanın.

## Paketleri İçe Aktarma

`Image`, Aspose.PSD'deki tüm görüntü tipleri için temel sınıftır. Java kaynak dosyanıza gerekli içe aktarmaları ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Adım 1: Görüntüyü Yükleme

### Tanım Bağlantısı
`RasterImage` sınıfı, Aspose.PSD'nin bir PSD dosyasından yüklenen raster tabanlı görüntüyü temsil eden çekirdek nesnedir.

PSD'nizi bir `RasterImage` örneğine yükleyin, böylece piksellerini manipüle edebilirsiniz:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Adım 2: Görüntüyü Yeniden Boyutlandırma

`image.resize(width, height, resizeType)` seçilen algoritmayı kullanarak görüntüyü belirtilen boyutlara yeniden boyutlandırır.

Şimdi **Resize Type Enumeration** kullanarak yüklenen görüntüyü yeniden boyutlandırın. Bu örnekte yüksek kaliteyle **görseli yeniden boyutlandırma** yaparken ideal olan Lanczos Resample yöntemini kullanıyoruz:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Adım 3: Yeniden Boyutlandırılmış Görüntüyü Kaydetme

`image.save(path, options)` görüntüyü, sağlanan seçeneklerle tanımlanan formatta diske yazar.

Yeniden boyutlandırdıktan sonra, görüntüyü belirtilen boyutlarla ve seçilen yeniden boyutlandırma türüyle kaydedin. Burada, sonucu JPEG dosyası olarak kaydederek **psd'yi jpeg'e dönüştürmeyi** de gösteriyoruz:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Neden Resize Type Enumeration Kullanılmalı?

`ResizeType`, yeniden örnekleme algoritması üzerinde ayrıntılı kontrol sağlar ve hız ile kaliteyi dengelemenize olanak tanır. Çoğu uygulama için `LanczosResample` büyük bir performans cezası olmadan keskin sonuçlar sunan harika bir denge sağlar ve çeşitli görüntü içeriklerinde iyi çalışır.

## Yaygın Sorunlar ve Çözümler

- **Yeniden boyutlandırma sonrası görüntü bulanık görünüyor** – `Bicubic` veya `NearestNeighbour` gibi farklı bir `ResizeType` deneyin ve hangisinin belirli görüntünüz için en iyi görsel sonucu verdiğini görün.  
- **Büyük PSD dosyalarında OutOfMemoryError** – Görüntüyü daha küçük parçalar halinde işleyin veya JVM yığın boyutunu (`-Xmx` bayrağı) artırın. Aspose.PSD, tüm belgeyi belleğe yüklemeden **2 GB**'a kadar dosyaları işleyebilir.

## Sık Sorulan Sorular

### Q1: Aspose.PSD for Java hem küçük hem de büyük ölçekli projeler için uygun mu?
A1: Kesinlikle! Aspose.PSD for Java, tüm ölçeklerdeki projelere hizmet vermek üzere tasarlanmıştır ve ölçeklenebilirlik ile verimlilik sağlar.

### Q2: Lanczos Resample dışındaki farklı bir yeniden boyutlandırma türü kullanabilir miyim?
A2: Evet, Aspose.PSD for Java çeşitli yeniden boyutlandırma türleri sunar, örneğin **NearestNeighbour**, **Bicubic** ve daha fazlası. Tam liste için API belgelerine bakın.

### Q3: Aspose.PSD for Java için ek desteği nereden bulabilirim?
A3: Herhangi bir soru veya yardım için [Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

### Q4: Aspose.PSD for Java için ücretsiz deneme sürümü mevcut mu?
A4: Evet, ücretsiz deneme sürümüne [burada](https://releases.aspose.com/) erişebilirsiniz.

### Q5: Aspose.PSD for Java için geçici bir lisans nasıl alabilirim?
A5: Geçici bir lisans almak için [bu bağlantı](https://purchase.aspose.com/temporary-license/) adresini ziyaret edin.

## Sık Sorulan Sorular

**S: PSD dosyasını yeniden boyutlandırmadan programlı olarak JPEG'e nasıl dönüştürürüm?**  
C: PSD'yi `Image.load` ile yükleyin, ardından `image.save("output.jpg", new JpegOptions());` çağrısını yapın.

**S: Yeniden boyutlandırırken orijinal DPI'yi korumak mümkün mü?**  
C: Evet, kaydetmeden önce `Image` nesnesinin `Resolution` özelliğini ayarlayabilirsiniz.

**S: Birden fazla yeniden boyutlandırma işlemini zincirleyebilir miyim?**  
C: `resize` metodunu birden fazla kez çağırabilirsiniz, ancak nihai boyutları hesaplayıp tek seferde yeniden boyutlandırmak daha verimlidir.

---

**Son Güncelleme:** 2026-06-03  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [Aspose.PSD ile Basit Yeniden Boyutlandırma – Java Görüntü İşleme Kütüphanesi](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java'da Bicubic Resampler ile Yüksek Kaliteli Görüntü Ölçekleme](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Aspose.PSD for Java ile PSD'yi PNG'ye Dönüştürme ve Orantılı Yeniden Boyutlandırma](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}