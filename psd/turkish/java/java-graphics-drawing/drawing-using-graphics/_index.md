---
date: 2026-09-13
description: Java'da Aspose.PSD ile bir elips ve diğer şekilleri nasıl çizeceğinizi
  öğrenin. Bu adım adım Java graphics öğreticisi, gradient fills, polygon fills ve
  image export gösterir.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Java'da graphics kullanarak çizim
og_description: Java'da Aspose.PSD kullanarak bir elipsin nasıl çizileceğini öğrenin.
  Bu Java graphics öğreticisi, shape drawing, gradient fills, polygon filling ve image
  exporting kapsar.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Java'da Aspose.PSD ile graphics kullanarak elips çizme
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Java'da Aspose.PSD ile graphics kullanarak elips çizme
url: /tr/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Aspose.PSD ile grafik kullanarak elips çizme

## Giriş
Bu Java grafik öğreticisinde Aspose.PSD for Java kullanarak **elips nasıl çizilir** nesnelerini ve diğer şekilleri programlı olarak keşfedeceksiniz. Dinamik küçük resimler oluşturmanız, özel UI öğeleri tasarlamanız veya tasarım iş akışlarını otomatikleştirmeniz gerekse, elips çizimini ve degrade doldurmalarını ustalaşmak size kesin görsel kontrol sağlar. Aşağıdaki adımlar, grafikleri başlatmayı, kalem ve fırça yapılandırmayı ve sonucu yaygın görüntü formatlarında dışa aktarmayı size gösterir.

## Hızlı cevaplar
- **Gerekli kütüphane nedir?** Aspose.PSD for Java (resmi siteden indirin).  
- **Öğretici hangi şekle odaklanıyor?** Bir elips çizmek ve bir çokgeni doldurmak.  
- **BMP dışındaki formatlara dışa aktarabilir miyim?** Evet – PNG, JPEG, TIFF ve daha fazlası desteklenir.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz geçici bir lisans çalışır; üretim için tam lisans gereklidir.  
- **API büyük görüntüler için uygun mu?** Aspose.PSD, tüm bitmap'i belleğe yüklemeden 500 MB'a kadar dosyaları işler.

## Java'da elips nasıl çizilir?
İstenilen genişlik ve yükseklikte bir `PsdImage` yükleyin, bir `Graphics` nesnesi oluşturun, bir `Pen` ayarlayın ve sınırlayıcı dikdörtgenle `drawEllipse` metodunu çağırın. Tüm işlem yalnızca birkaç metod çağrısı gerektirir ve modern donanımda tipik 800×600 görüntüler için bir saniyeden kısa sürede çalışır.

## Aspose.PSD for Java nedir?
Aspose.PSD for Java, **Adobe Photoshop'a ihtiyaç duymadan 50+ görüntü formatı dönüşümü ve tam PSD düzenleme yetenekleri sunan saf‑Java kütüphanesidir**. Çok katmanlı dosyaları render edebilir, değiştirebilir ve dışa aktarabilir; bellek kullanımını düşük tutarak sunucu‑tarafı grafik üretimi için idealdir.

## Şekil çizmek için Aspose.PSD neden kullanılmalı?
Aspose.PSD yüksek performans, geniş format desteği ve kesin render sağladığından sunucu‑tarafı grafik üretimi ve karmaşık şekil çizimi için idealdir.

- **Performans:** 500 MB'a kadar görüntüyü 150 MB'den az yığın kullanımıyla işler (≈%30 daha az bellek tüketimi).  
- **Format desteği:** BMP, PNG, JPEG, TIFF ve PSD dahil 50+ giriş ve çıkış formatı.  
- **Kesinlik:** Alt‑piksel render, yüksek DPI ekranlarda net elipsler ve yumuşak degradeler sağlar.

## Önkoşullar
- Java programlamaya temel bilgi.  
- Java Development Kit (JDK) yüklü.  
- IntelliJ IDEA veya Eclipse gibi bir IDE.  
- Aspose.PSD for Java kütüphanesi. [Aspose.PSD Java indirme](https://releases.aspose.com/psd/java/) adresinden indirebilirsiniz.

## Paketleri içe aktar
Başlamak için gerekli Aspose.PSD sınıflarını ve standart Java yardımcılarını içe aktarın. Aşağıdaki sınıflar çizim primitive'leri ve renk işleme sağlar:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Adım 1: bir görüntü nesnesi oluşturun
`PsdImage`, çeşitli formatlarda kaydedilebilen ve üzerine çizim yapılabilen bellek içi raster tuvalini temsil eder.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Adım 2: grafik nesnesini başlatın
`Graphics`, bir `PsdImage` ile ilişkilendirilen çizim yüzeyidir; şekil çizme gibi vektör işlemlerine olanak tanır.
```java
Graphics graphics = new Graphics(image);
```

## Adım 3: görüntü yüzeyini temizleyin
`clear`, tüm tuvali tek bir arka plan rengiyle doldurur.
```java
graphics.clear(Color.getWhite());
```

## Adım 4: kalem nesnesi oluşturun ve yapılandırın
`Pen`, kontur çizerken kullanılan renk, genişlik ve stil gibi özellikleri tanımlar.
```java
Pen pen = new Pen(Color.getBlue());
```

## Adım 5: şekilleri çizin
`drawEllipse`, mevcut kalemi kullanarak belirtilen dikdörtgen içine sığan bir elips çizer.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Adım 6: doldurma için fırçaları kullanın
`LinearGradientBrush`, tanımlı bir alanda iki renk arasında geçiş yapan bir degrade doldurma oluşturur.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Adım 7: değiştirilmiş görüntüyü kaydedin
`save`, `PsdImage`'ı BMP veya PNG gibi seçilen formatta diske yazar.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Yaygın hatalar ve sorun giderme
- **Graphics üzerinde NullPointerException:** `Graphics` nesnesi oluşturulmadan önce `PsdImage`'ın tam olarak örneklenmiş olduğundan emin olun.  
- **Yanlış renkler:** Varsayılan palet beklentileri karşılamıyorsa tam ARGB değerlerini belirtmek için `Color.fromArgb` kullanın.  
- **Büyük görüntülerde performans düşüklüğü:** Bellek yükünü azaltmak için `PsdImageOptions` ile `compression = CompressionType.Rle` etkinleştirin.

## Sıkça sorulan sorular

**S: Aspose.PSD karmaşık görüntü manipülasyonlarını yönetebilir mi?**  
C: Evet, katman birleştirme, kanal ayarlamaları, metin render'ı ve gelişmiş maskeleme gibi işlemleri şekil çiziminin yanı sıra destekler.

**S: Aspose.PSD yüksek‑performanslı uygulamalar için uygun mu?**  
C: Kesinlikle; kütüphane hız için optimize edilmiştir ve tipik bir sunucuda 10 MP bir görüntüyü 2 saniyeden kısa sürede işleyebilir.

**S: Daha fazla örnek ve dokümantasyona nereden ulaşabilirim?**  
C: Kapsamlı kılavuzlar ve API referansları için [Aspose.PSD Java belgeleri](https://reference.aspose.com/psd/java/) sayfasını ziyaret edin.

**S: Aspose.PSD dışa aktarma için birden fazla görüntü formatını destekliyor mu?**  
C: Evet, BMP, PNG, JPEG, TIFF, GIF ve PSD dahil birçok formata dışa aktarabilirsiniz.

**S: Sorun yaşarsam nasıl destek alabilirim?**  
C: [destek forumu](https://forum.aspose.com/c/psd/34) üzerinden Aspose.PSD topluluğuna ulaşabilir veya öncelikli yardım için bir [geçici lisans](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

---

**Son güncelleme:** 2026-09-13  
**Test edilen sürüm:** Aspose.PSD for Java 24.10  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandır – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java kullanarak PSD içinde Dikdörtgen Çiz ve Kaydet](/psd/java/basic-image-operations/simple-drawing/)
- [Görüntüye İmza Ekle – Aspose.PSD for Java ile Kanvasa Görüntü Çiz](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}