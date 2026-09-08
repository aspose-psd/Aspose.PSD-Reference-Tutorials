---
date: 2026-09-08
description: Aspose.PSD for Java kullanarak Java'da bezier eğrileri nasıl çizeceğinizi
  öğrenin. Adım adım talimatları, önkoşulları ve kod içermeyen örnekleri izleyin.
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: Java'da Bezier Eğrileri Çizme
og_description: Aspose.PSD kullanarak Java'da bezier eğrileri nasıl çizeceğinizi öğrenin.
  Bu rehber, önkoşulları, adım adım çizmeyi ve yüksek çözünürlüklü görüntüler için
  ipuçlarını kapsar.
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: Java'da Aspose.PSD kütüphanesi ile bezier eğrileri nasıl çizilir
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: Java'da Aspose.PSD kütüphanesi ile bezier eğrileri nasıl çizilir
url: /tr/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Aspose.PSD kütüphanesi ile bezier eğrileri nasıl çizilir

## Giriş
Java masaüstü veya sunucu uygulamasında **how to draw bezier** şekillerini nasıl çizeceğinizi öğrenmeniz gerekiyorsa, Aspose.PSD for Java size temiz, bellek‑verimli bir API sunar. Bu öğreticide, bir PSD tuvali oluşturma, bir çizim kalemi yapılandırma, kontrol noktalarını tanımlama ve pürüzsüz bir Bezier eğrisi render etme adımlarını tam olarak göreceksiniz — düşük seviyeli piksel manipülasyonu kodu yazmadan.

## Hızlı cevaplar
- **Çizimi hangi kütüphane yönetir?** Aspose.PSD for Java.
- **Kaç satır kod gereklidir?** Yaklaşık on kısa ifade.
- **Eğri rengini değiştirebilir miyim?** Evet, `Pen` renk özelliğini ayarlayarak.
- **Yüksek çözünürlüklü çıktı destekleniyor mu?** Evet, tam bellek yüklemesi olmadan 500 MB dosyalara kadar.
- **Ticari bir lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.

## Bezier eğrisi nedir?
Bezier eğrisi, iki veya daha fazla nokta tarafından kontrol edilen matematiksel olarak tanımlanmış pürüzsüz bir çizgidir. Vektör grafikleri, animasyon ve UI tasarımında zarif, ölçeklenebilir şekiller oluşturmak için yaygın olarak kullanılır. Eğrinin şekli, başlangıç noktası, bitiş noktası ve eğriliğini etkileyen bir veya daha fazla kontrol noktası tarafından belirlenir; bu sayede tasarımcılar karmaşık yolları basit parametrelerle modelleyebilir.

## Bezier eğrileri çizerken neden Aspose.PSD kullanmalı?
Aspose.PSD, **30+ image formats** desteği sunar ve **multi‑hundred‑page PSD files** tüm belgeyi RAM'e yüklemeden işleyebilir. Kütüphanenin `drawBezier()` yöntemi otomatik olarak anti‑aliasing ve renk yönetimini gerçekleştirir, tipik 100 × 100 tuvallar için bir saniyeden kısa sürede piksel‑mükemmel sonuçlar sağlar.

## Önkoşullar
Başlamadan önce, aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
1. **Java Development Kit (JDK)** – herhangi bir yeni sürüm (8 veya üzeri) kurulu ve yapılandırılmış.
2. **Aspose.PSD for Java JAR** – Aspose.PSD for Java kütüphanesini [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) adresinden indirin ve projenizin sınıf yoluna ekleyin.
3. **Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA veya NetBeans gibi, JDK ile kurulmuş bir IDE.

## Paketleri içe aktar
Aşağıdaki içe aktarmalar, görüntü oluşturma ve çizim için gerekli Aspose.PSD sınıflarını getirir.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Java'da bezier eğrileri nasıl çizilir?
Boş bir `PsdImage` yükleyin, bir `Graphics` nesnesi oluşturun, bir `Pen` yapılandırın, başlangıç, kontrol ve bitiş noktalarını tanımlayın, `drawBezier()` metodunu çağırın ve sonunda görüntüyü kaydedin. Bu sıralama, tek bir metod çağrısı ile pürüzsüz bir eğri üretir ve manuel piksel hesaplamaları gerektirmez.

### Adım 1: bir görüntü örneği oluştur
`PsdImage` sınıfı, Aspose.PSD'nin bellekte tek bir PSD dosyasını temsil eden üst‑seviye nesnesidir. İlk olarak, bellekte bir PSD görüntüsü temsil eden `PsdImage` sınıfının bir örneğini oluşturmanız gerekir.
```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
Açıklama:
- `PsdImage`, genişlik ve yükseklik parametreleriyle (bu örnekte 100 × 100 piksel) örneklenir.

### Adım 2: grafik bağlamını başlat
`Graphics` sınıfı, bir `PsdImage` üzerinde çizim yetenekleri sağlar. Sonra, görüntü üzerinde çizim işlemleri yapmak için `Graphics` sınıfının bir örneğini başlatın.
```java
Graphics graphics = new Graphics(image);
```
Açıklama:
- `Graphics` nesnesi, çizim işlemlerine izin veren `image` örneğiyle başlatılır.

### Adım 3: grafik yüzeyini temizle
`clear()` yöntemi, grafik yüzeyinin arka plan rengini ayarlar. Grafik yüzeyini belirli bir arka plan rengiyle temizleyin, burada `Color.getYellow()`.
```java
graphics.clear(Color.getYellow());
```
Açıklama:
- `clear()` yöntemi, grafik yüzeyinin arka plan rengini ayarlar.

### Adım 4: çizim için kalemi başlat
`Pen` nesnesi, renk ve genişlik gibi çizgi özelliklerini tanımlar. Eğrinin nasıl çizileceğini belirlemek için renk ve genişlik gibi özelliklere sahip bir `Pen` nesnesi oluşturun.
```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
Açıklama:
- `Pen`, siyah renk ve 3 piksel genişlik ile başlatılır.

### Adım 5: bezier eğri parametrelerini tanımla
Kontrol noktaları eğriliği belirler. Bezier eğrisi için kontrol noktalarını ve bitiş noktalarını belirtin.
```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
Açıklama:
- `startX`, `startY`: Eğrinin başlangıç noktası.  
- `controlX1`, `controlY1`: İlk kontrol noktası.  
- `controlX2`, `controlY2`: İkinci kontrol noktası.  
- `endX`, `endY`: Eğrinin bitiş noktası.

### Adım 6: bezier eğrisini çiz
`drawBezier()` yöntemi, sağlanan `Pen` ve noktalarla eğriyi render eder. Daha önce tanımlanan `Pen` ve kontrol noktalarını kullanarak Bezier eğrisini görüntüye çizmek için `drawBezier()` yöntemini kullanın.
```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
Açıklama:
- `drawBezier()` yöntemi, belirtilen parametrelerle `blackPen` kullanarak eğriyi çizer.

### Adım 7: görüntüyü kaydet
Görüntüyü kaydetmek, çizimi diske kalıcı hale getirir. Çizilen görüntüyü BMP dosya formatında kaydedin.
```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## Yaygın sorunlar ve çözümler
- **Eğri düz görünüyor** – Kontrol noktalarının başlangıç ve bitiş noktalarıyla aynı doğrultuda olmadığını doğrulayın. Hafifçe kaydırarak eğrilik oluşturun.  
- **Renk değişmiyor** – `drawBezier()` çağırmadan önce `Pen` rengini değiştirdiğinizden emin olun.  
- **Büyük tuvallarda bellek yetersizliği hataları** – Akışı etkinleştiren `PsdImage` yapıcılarını kullanın veya çizimi parçalara bölün.

## Sıkça sorulan sorular

**Q:** Aynı görüntüde birden fazla Bezier eğrisi çizebilir miyim?  
**A:** Evet, bir döngü içinde `drawBezier()` çağrısını tekrarlayarak, her eğri için kontrol noktalarını güncelleyebilirsiniz.

**Q:** Bezier eğrisinin rengini nasıl değiştirebilirim?  
**A:** `drawBezier()` metodunu çağırmadan önce `Pen` nesnesinin renk özelliğini (`örnekteki `Color.getBlack()`) değiştirin.

**Q:** Aspose.PSD for Java yüksek çözünürlüklü görüntüler için uygun mu?  
**A:** Evet, Aspose.PSD for Java, verimli bellek yönetimiyle yüksek çözünürlüklü görüntüleri destekler; dosyanın tamamını belleğe yüklemeden 500 MB'den büyük dosyaları işleyebilir.

**Q:** Görüntüyü BMP dışındaki formatlara dışa aktarabilir miyim?  
**A:** Evet, Aspose.PSD for Java PNG, JPEG, TIFF ve birçok diğer raster formata dışa aktarmayı destekler.

**Q:** Daha fazla örnek ve belgeyi nerede bulabilirim?  
**A:** Kapsamlı rehberler ve kod örnekleri için [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) adresini ziyaret edin.

---

**Last Updated:** 2026-09-08  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandır – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java kullanarak PSD'de Bir Dikdörtgen Çiz ve Kaydet](/psd/java/basic-image-operations/simple-drawing/)
- [Aspose.PSD Kullanarak Java'da Çizgi Rengini Değiştirme](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}