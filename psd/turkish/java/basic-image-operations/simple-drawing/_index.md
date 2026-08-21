---
date: 2026-06-13
description: Aspose.PSD for Java kullanarak PSD dosyalarında dikdörtgen çizmeyi öğrenin.
  Bu rehber adım adım kod, katman ekleme, sunucu tarafı görüntü işleme ve şekil çizimini
  gösterir.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Basit Çizim Yap
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile PSD'de Dikdörtgen Çizme
url: /tr/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile PSD'de Dikdörtgen Çizme

## Giriş

Bu öğreticide **dikdörtgen çizme** şekillerini saf‑Java Aspose.PSD kütüphanesini kullanarak bir Photoshop PSD dosyası içinde nasıl oluşturacağınızı keşfedeceksiniz. Sunucu‑tarafı varlık hattı oluşturuyor, küçük resim üretimini otomatikleştiriyor veya mevcut tasarımlara dinamik grafikler ekliyor olun, aşağıdaki adımlar eksiksiz, üretim‑hazır bir çözüm sunar. Yeni bir PSD belgesi oluşturma, bir katman ekleme, arka planı temizleme ve sonunda hem kırmızı hem de mavi dikdörtgenler çizme konularını Photoshop çalıştırmadan ele alacağız.

## Hızlı Yanıtlar
- **PSD dosyası oluşturmak için birincil sınıf nedir?** `PsdImage`
- **Katmanın arka plan rengini temizleyen yöntem hangisidir?** `Graphics.clear(Color)`
- **Kırmızı bir dikdörtgen nasıl çizilir?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme testi için çalışır; üretim için lisans gereklidir.
- **Aynı API ile mevcut PSD dosyalarını manipüle edebilir miyim?** Evet, Aspose.PSD tam PSD düzenlemeyi destekler.

## PSD dosyasında kırmızı bir dikdörtgen çizmek nedir?

Kırmızı bir dikdörtgen çizmek, `Graphics` nesnesini kullanarak belirli bir PSD görüntüsü katmanına kırmızı renk ile doldurulmuş veya kenarlıklı bir dikdörtgen şekli oluşturmak anlamına gelir. Bu işlem, alanları vurgulamak, yer tutucular oluşturmak veya programatik olarak basit grafikler eklemek için yaygın olarak kullanılır.

## Neden Aspose.PSD for Java'ı PSD dosyalarını manipüle etmek için kullanmalısınız?

Aspose.PSD for Java **50+** giriş ve çıkış formatını destekler, çok sayfalı PSD dosyalarını tüm dosyayı belleğe yüklemeden işleyebilir ve Java 8 veya üzerini destekleyen herhangi bir platformda çalışır. Sunucu‑tarafı görüntü işleme motoru Photoshop ihtiyacını ortadan kaldırır, lisans maliyetlerini azaltır ve mütevazı bir VM üzerinde saat başı **10 GB** görüntü verisini işleyebilen otomatik iş akışlarını mümkün kılar.

## Ön Koşullar

- Makinenizde Java Development Kit (JDK) 8 veya daha yeni bir sürüm yüklü olmalıdır.  
- Aspose.PSD for Java kütüphanesi. İndirmek için [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) adresini ziyaret edebilirsiniz.

## Paketleri İçe Aktarma

`import` ifadeleri, PSD görüntüleri, katmanlar, renkler ve grafiklerle çalışabilmeniz için gerekli sınıfları kapsam içine alır.

`PsdImage` sınıfı, Aspose.PSD'nin bellek içindeki tek bir PSD dosyasını temsil eden üst‑seviye nesnesidir.  
`Graphics` çizgi, dikdörtgen ve elips gibi çizim ilkelere sağlar.  
`Color` ve `Pen` çizgi renklerini ve kalınlığını belirlemenizi sağlar.  
`Layer` sınıfı, bir PSD belgesi içindeki bireysel görüntü katmanını temsil eder.  
`Rectangle` sınıfı, çizim işlemlerinde kullanılan dikdörtgen alanın konum ve boyutunu tanımlar.  
`SolidBrush` sınıfı, şekilleri katı bir renk ile doldurur.

## PSD belgesi oluşturmanın ilk adımı nedir?

`PsdImage` nesnesini, piksel cinsinden istenen tuval genişliği ve yüksekliğiyle örnekleyerek boş bir PSD dosya yapısı oluşturursunuz. Başlangıç katmanları veya arka plan ayarlandıktan sonra, belgeyi diske yazmak için `save` yöntemini bir dosya yolu ile çağırırsınız. Bu, sonraki düzenleme işlemleri için görüntüyü hazırlar.

## Adım 1: Yeni Bir Belge Oluşturma

İlk olarak, istediğiniz tuval boyutlarıyla yeni bir PSD belgesi oluşturun. Bu belge, çizim yapacağımız katmanı barındıracak.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## PSD görüntüsüne yeni bir boş katman nasıl eklenir?

Öncelikle, ebeveyn `PsdImage` ile aynı genişlik ve yüksekliğe sahip yeni bir `Layer` örneği oluşturun. Ardından bu katmanı, görüntünün `Layers` koleksiyonuna `add` yöntemiyle ekleyin. Katman görüntüye eklendikten sonra, çizim işlemlerini gerçekleştirmek için `Graphics` nesnesini alın; bu adım olmadan çizimler görünmez.

## Adım 2: Katman Ekleme

Şimdi, görüntünün tam genişlik ve yüksekliğini kapsayan yeni bir boş katman ekleyin. Katmanlar, çizim işlemlerini ayırmak için gereklidir.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Katmanın arka plan rengini temizlemenin amacı nedir?

`Graphics.clear` metodunu belirli bir `Color` ile çağırmak, tüm katmanı o renk ile doldurarak piksel verisini sıfırlar. Bu, önceki içeriğin kaldırılmasını sağlar ve katmanın bilinen bir arka planla başlamasını temin eder; böylece PSD daha sonra Photoshop'ta açıldığında veya düzenlendiğinde beklenmedik şeffaflık ya da renk karışımı oluşmaz.

## Adım 3: Şekil Çizme

`Graphics` sınıfını kullanarak katmanın piksel verisini manipüle edeceğiz. Aşağıda, arka planı temizleme ve farklı renklerde dikdörtgenler çizme örnekleri yer almaktadır.

### Katman Rengini Temizle (arka planı sarı olarak ayarla)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Kırmızı Bir Dikdörtgen Çiz (ana odak)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Mavi Bir Dikdörtgen Çiz (ek örnek)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Düzenlenmiş PSD dosyasını diske nasıl kaydedersiniz?

`PsdImage` nesnesinin `save` metodunu, tam dosya yolu ve isteğe bağlı olarak istenen görüntü formatı (varsayılan olarak PSD) ile kullanın. Bu, tüm katmanları, maskeleri ve çizim komutlarını tek bir PSD dosyasına yazar; Photoshop spesifikasyonuna uygun şekilde açılabilir ve uyarı vermez.

## Adım 4: Değişiklikleri Kaydet

Son olarak, değiştirilmiş PSD görüntüsünü diske yazın. Dosya yeni katmanı ve çizilen şekilleri içerecektir.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Yaygın Sorunlar ve Çözümler

- **Katman çizimden sonra görünmüyor:** `Graphics` nesnesi oluşturulmadan **önce** katmanın görüntüye eklenmiş olduğundan emin olun. Çizim yüzeyi geçerli bir katmana bağlı olmalıdır.
- **Renkler yanlış görünüyor:** `Color.getRed()` (veya `Color.getBlue()`) kullandığınızı doğrulayın; 0‑255 aralığını aşan özel RGB değerleri oluşturmayın.
- **Dosya kaydedilmiyor:** `outputDir` yolunun var olduğunu ve uygulamanın yazma iznine sahip olduğunu kontrol edin. Linux'ta klasör sahipliğini ayarlamanız veya `Files.createDirectories` kullanmanız gerekebilir.
- **Büyük dosyalarda performans yavaşlıyor:** `PsdImage`’ın `setLoadOptions` metodunu kullanarak yalnızca gerekli kanalları yükleyin; bu, 200 MB üzerindeki PSD'lerde bellek tüketimini azaltır.

## Sık Sorulan Sorular

**Q1: Aspose.PSD for Java'ı mevcut PSD dosyalarını manipüle etmek için kullanabilir miyim?**  
A1: Evet, Aspose.PSD for Java mevcut PSD dosyalarını düzenleme, katman sırasını değiştirme, maske ayarları ve vektör çizimi gibi kapsamlı işlevler sunar.

**Q2: Aspose.PSD for Java için desteği nereden bulabilirim?**  
A2: Topluluk‑odaklı yardım ve resmi Aspose yanıtları için [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edebilirsiniz.

**Q3: Aspose.PSD for Java için ücretsiz deneme mevcut mu?**  
A3: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) erişebilirsiniz. Deneme tüm özellikleri içerir ancak kaydedilen dosyalara filigran ekler.

**Q4: Aspose.PSD for Java lisansını nasıl satın alabilirim?**  
A4: Lisansı [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) üzerinden alabilirsiniz. Lisans seçenekleri arasında kalıcı, abonelik ve site lisansları bulunur.

**Q5: Aspose.PSD for Java için geçici lisanslar mevcut mu?**  
A5: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

## Ek Sık Sorulan Sorular

**Q: Dikdörtgen dışında başka şekiller çizebilir miyim?**  
A: Evet, `Graphics` sınıfı ayrıca `drawPath` yöntemiyle elips, çizgi ve özel yollar çizmeyi destekler.

**Q: Aspose.PSD çizilen şekillerde şeffaflığı destekliyor mu?**  
A: Kesinlikle; `SolidBrush` ile ARGB renk kullanarak alfa şeffaflığı ekleyebilir, yarı şeffaf kaplamalar oluşturabilirsiniz.

**Q: Bir katmanın opaklığını düzenlemek mümkün mü?**  
A: Evet, her `Layer` nesnesinin `setOpacity` yöntemi 0‑255 arasında bir değer alır ve katman şeffaflığını hassas bir şekilde kontrol etmenizi sağlar.

**Q: Yeni bir şey oluşturmak yerine mevcut bir PSD dosyasını nasıl yüklerim?**  
A: Katmanları manipüle etmeden önce `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` kodunu kullanın. Yüklenen görüntü tüm orijinal katmanları ve maskeleri korur.

## Sonuç

Artık **dikdörtgen çizme** şekillerini ve katmanları Aspose.PSD for Java kullanarak bir PSD dosyası içinde nasıl yöneteceğinizi öğrendiniz. Bir belge oluşturup, katman ekleyip, arka planı temizleyip ve `Graphics` API'siyle çizim yaparak sunucu‑tarafında sayısız grafik‑tasarım görevini otomatikleştirebilirsiniz. Farklı kalemler, fırçalar ve katman efektleriyle deneyler yaparak bu temeli tam özellikli görüntü üretim hatlarına genişletebilirsiniz.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [Java’da Şekil Çizme – Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Aspose.PSD ile Basit Yeniden Boyutlandırma – Java Görüntü Manipülasyon Kütüphanesi](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java’da Dikdörtgen ile Görüntüyü Kırpma](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

**Son Güncelleme:** 2026-06-13  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Yazar:** Aspose