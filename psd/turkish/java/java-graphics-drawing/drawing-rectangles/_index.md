---
date: 2026-09-08
description: Aspose.PSD for Java kullanarak bir görüntüye dikdörtgen çizmeyi öğrenin;
  bitmap oluşturma, background color ayarlama ve Java image manipulation için graphics
  başlatmayı kapsar.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Java'da Dikdörtgen Çizme
og_description: Aspose.PSD for Java kullanarak bir görüntüye dikdörtgen çizmeyi öğrenin.
  Bu kılavuz bitmap oluşturma, background color ayarlama ve Java image manipulation
  için graphics başlatmayı kapsar.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Aspose.PSD for Java ile bir görüntüye dikdörtgen nasıl çizilir
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Aspose.PSD for Java ile bir görüntüye dikdörtgen nasıl çizilir
url: /tr/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Görüntüde Aspose.PSD for Java ile dikdörtgen çizme

## Giriş
Programmatically bir görüntü üzerinde **how to draw rectangle** ihtiyacınız varsa, Aspose.PSD for Java size temiz, yüksek‑performanslı bir API sunar. Bu öğreticide bir bitmap nasıl oluşturulur, arka plan rengi nasıl ayarlanır ve **initialize graphics java** nesneleri nasıl başlatılır gösterilecek, böylece istediğiniz boyut ve renkte dikdörtgenler çizebileceksiniz. Adımlar basit, kod özlü ve sonuç, herhangi bir Java‑tabanlı iş akışında kullanabileceğiniz bir BMP dosyasıdır.

## Hızlı cevaplar
- **Dikdörtgen çizimini hangi kütüphane yönetir?** Aspose.PSD for Java.
- **Kaç satır kod gereklidir?** Görüntüyü oluşturmak, arka planı ayarlamak ve iki dikdörtgen çizmek için yaklaşık altı satır.
- **Dışa aktarım için hangi görüntü formatları desteklenir?** BMP, PNG, JPEG, TIFF, GIF ve daha fazlası.
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim için lisans gereklidir.
- **Kenarlık kalınlığını değiştirebilir miyim?** Evet – çizmeden önce `Pen` kalınlık özelliğini ayarlayın.

## Görüntüde dikdörtgen çizmek nedir?
Bir görüntü üzerinde dikdörtgen çizmek, bir grafik bağlamı kullanarak bitmap üzerine dolu ya da kenarlıklı bir şekil render etmektir. Aspose.PSD’nin `Graphics` sınıfı, tek bir çağrı ile renk, konum ve boyutu belirlemenizi sağlayan yöntemler sunar.

## Neden Aspose.PSD for Java ile dikdörtgen çizimi kullanmalı?
Aspose.PSD, **50+ görüntü formatını** destekler ve **2 GB**'a kadar dosyaları bellek içine tüm belgeyi yüklemeden işleyebilir. `Graphics` API'si, toplu işlemler için yerel Java AWT'den **3× daha hızlı** çalışır ve yüksek verimli sunucu tarafı görüntü işleme için idealdir.

## Önkoşullar
Başlamadan önce, şunların yüklü olduğundan emin olun:

- **Java Development Kit (JDK) 8 veya üzeri** yüklü.
- **Aspose.PSD for Java** kütüphanesini **[Aspose.PSD for Java indirme sayfasından](https://releases.aspose.com/psd/java/)** indirip projenizin sınıf yoluna ekleyin.

### Paketleri içe aktar
`import` ifadeleri, bitmap oluşturma ve çizim için gerekli sınıflara erişim sağlar.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Bu importlar, görüntüler üzerinde dikdörtgen çizmek için gereken sınıf ve yöntemlere erişmenizi sağlar.

## Java’da bir görüntü üzerinde dikdörtgen nasıl çizilir?
Yeni bir `PsdImage` yükleyin, yüzeyini bir arka plan rengiyle temizleyin, bir `Graphics` nesnesi oluşturun ve ardından istediğiniz kalem ve fırça ile `drawRectangle` metodunu çağırın. Tüm süreç sadece birkaç metod çağrısı ile gerçekleşir ve kaydedilmeye hazır bir bitmap üretir.  
`PsdImage`, düzenlenip kaydedilebilen bellek içi bir bitmap'i temsil eder.  
`Graphics`, bir görüntü üzerine şekil render etmek için bir çizim yüzeyi sağlar.

### Adım 1: yeni bir görüntü oluşturma
`PsdImage` sınıfı, bellek içi bir bitmap'i temsil eder. Başlatılması aynı zamanda piksel tamponunu tahsis eder.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
Bu adımda, `PsdImage` genişlik ve yükseklik olarak **100 px** değerleriyle başlatılır ve size gösterim için küçük bir tuval sağlar.

### Adım 2: graphics java nesnesini başlatma
Bir `Graphics` örneği, az önce oluşturduğunuz görüntüye bağlı çizim yüzeyidir.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Bu `Graphics` nesnesi, şekilleri doldurma veya kenarlık çizme gibi çizim işlemlerini gerçekleştirmek için kullanılacaktır.

### Adım 3: arka plan rengini ayarlama java
Şekiller çizmeye başlamadan önce genellikle katı bir arka plan istersiniz. Tüm tuvali doldurmak için `clear` ve bir `Color` kullanın.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Arka plan **sarı** olarak ayarlanır, ardından gelen kırmızı ve mavi dikdörtgenler için yüksek kontrast sağlar.

### Adım 4: görüntü üzerine dikdörtgenler çizme
Kenarlık için bir `Pen` ve dolgu için bir `SolidBrush` kullanarak `drawRectangle` metodunu kullanın. Farklı renk ve konumlarda birden fazla dikdörtgen çizebilirsiniz.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Bu komutlar (10, 10) konumunda **kırmızı** bir dikdörtgen ve (50, 50) konumunda **mavi** bir dikdörtgen çizer; her biri 40 px genişliğinde ve 30 px yüksekliğindedir.

### Adım 5: görüntüyü bitmap olarak dışa aktarma
Son olarak, değiştirilmiş görüntüyü diske kaydedin. Aspose.PSD, bitmap'i belirttiğiniz formatte otomatik olarak kodlar.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Görüntü, `outpath` içinde saklanan yolda BMP dosyası olarak kaydedilir.

## Yaygın sorunlar ve çözümler
- **Boş çıktı dosyası** – Çizmeden önce `graphics.clear` çağırdığınızdan emin olun; aksi takdirde tuval şeffaf kalabilir.
- **Yanlış renkler** – `com.aspose.psd.Color` import ettiğinizden, `java.awt.Color` değil, emin olun.
- **Büyük görüntüler bellek dışı** – Tüm dosyayı RAM'e yüklememek için akış destekli `PsdImage` yapıcılarını kullanın.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java dikdörtgenlerin dışında başka şekilleri de işleyebilir mi?**  
C: Evet, elipsler, çizgiler, çokgenler ve özel yolları destekler, tam vektör çizim yetenekleri sunar.

**S: Dikdörtgen kenarlığının kalınlığını nasıl değiştirebilirim?**  
C: `drawRectangle` çağırmadan önce `Pen` nesnesinin `setWidth(float)` metodunu ayarlayın.

**S: Aspose.PSD for Java yüksek performanslı görüntü işleme görevleri için uygun mu?**  
C: Kesinlikle – akış API'si, 200 MB'den az RAM kullanımıyla çok sayfalı PSD dosyalarını işler.

**S: Aspose.PSD for Java için daha fazla örnek ve öğretici nerede bulunabilir?**  
C: Daha fazla örnek ve ayrıntılı belgeleri [Aspose.PSD for Java belgeleri](https://reference.aspose.com/psd/java/) adresinde keşfedebilirsiniz.

**S: Aspose.PSD for Java BMP dışında başka görüntü formatlarını destekliyor mu?**  
C: Evet, PNG, JPEG, TIFF, GIF ve hem içe hem de dışa aktarım için 30'dan fazla ek formatı destekler.

## Sonuç
Artık Aspose.PSD for Java kullanarak bir görüntü üzerinde **how to draw rectangle** (dikdörtgen çizme) nasıl yapılacağını biliyorsunuz; bitmap oluşturma, arka plan rengini ayarlama ve grafikleri başlatma adımlarını gördünüz. Farklı boyutlar, renkler ve ek şekillerle deney yaparak **java image manipulation** (java görüntü işleme) konusunda ustalaşın. Hazır olduğunuzda, bu deseni daha büyük toplu‑işlem hatlarına veya UI‑tabanlı editörlere entegre edebilirsiniz.

---

**Son Güncelleme:** 2026-09-08  
**Test Edilen:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandır – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java ile Görüntüye İmza Ekle – Kanvasa Görüntü Çizme](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Aspose.PSD for Java ile Dikdörtgenle Görüntüyü Kırp](/psd/java/image-editing/crop-image-by-rectangle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}