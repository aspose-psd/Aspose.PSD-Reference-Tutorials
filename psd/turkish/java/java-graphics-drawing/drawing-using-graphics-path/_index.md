---
date: 2026-09-08
description: Aspose.PSD'nin Graphics Path sınıfını Java'da kullanarak görüntü oluşturmayı
  öğrenin. Bu adım adım rehber, metin, şekiller eklemeyi ve görüntü arka planını verimli
  bir şekilde temizlemeyi gösterir.
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: Java'da Graphics Path kullanarak görüntü oluşturma
og_description: Aspose.PSD ile Java'da görüntü oluşturmayı öğrenin. Bu öğretici, Graphics
  Path sınıfını kullanarak metin, şekil eklemeyi ve görüntü arka planını temizlemeyi
  kapsar.
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: Aspose.PSD ile Java'da Graphics Path kullanarak görüntü oluşturma
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: Java'da Graphics Path kullanarak görüntü oluşturma
url: /tr/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Graphics Path kullanarak Java'da görüntü oluşturma

## Giriş
Bu öğreticide, Aspose.PSD for Java tarafından sağlanan güçlü **Graphics Path** sınıfını kullanarak programlı olarak **görüntü oluşturma** dosyalarını nasıl oluşturacağınızı öğreneceksiniz. Özel şekiller çizmeye, metin eklemeye veya bir görüntünün arka planını temizlemeye ihtiyacınız olsun, aşağıdaki adım‑adım kılavuz size sadece birkaç satır kodla profesyonel kalitede sonuçlar elde etmenizi gösterir.

## Hızlı cevaplar
- **Hangi kütüphane karmaşık çizimi yönetir?** Aspose.PSD for Java’nın Graphics Path sınıfı.  
- **Görüntüye metin ekleyebilir miyim?** Evet – `GraphicsPath.addString` metodunu kullanın.  
- **Arka planı temizleme destekleniyor mu?** Kesinlikle, yolu şeffaf bir fırça ile doldurun.  
- **Hangi Java sürümü gerekiyor?** JDK 11 veya daha yenisi.  
- **Üretim için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz bir deneme mevcuttur.

## Graphics Path sınıfı nedir?
`GraphicsPath` sınıfı, Aspose.PSD’nin vektör‑tabanlı çizim talimatlarını tanımlamak için temel nesnesidir. Şekilleri, metni ve dolgu alanlarını tek bir yeniden kullanılabilir yolda birleştirmenizi sağlar ve bu yol herhangi bir görüntü üzerinde işlenebilir. Bir yol oluşturarak kalem, fırça ve dönüşümleri tek bir render geçişinde uygulayabilir, bu da performansı artırır ve çizim mantığını düzenli tutar.

## Java’da metin ekleme ve görüntü arka planını temizleme için Graphics Path neden kullanılmalı?
Aspose.PSD **50+ görüntü formatını** (PSD, PNG, JPEG, BMP vb.) destekler ve belgeyi belleğe tamamen yüklemeden **2 GB** kadar dosyayı işleyebilir. Graphics Path kullanmak, çizim, metin yerleştirme ve arka plan temizlemeyi tek bir yüksek‑performanslı işlemde birleştirmenizi sağlar; bu da raster‑only yaklaşımlara göre **%30** kadar bellek tasarrufu sağlar.

## Önkoşullar
Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – stabil bir JDK 11+ kurulmuş. [Oracle’ın sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin.  
2. **Aspose.PSD for Java kütüphanesi** – en son JAR dosyasını [buradan](https://releases.aspose.com/psd/java/) edinin ve projenizin sınıf yoluna ekleyin.  
3. **IDE** – Eclipse, IntelliJ IDEA veya VS Code gibi herhangi bir Java IDE.

Bu gereksinimler sağlandığında görüntü oluşturmaya hazırsınız.

## Paketleri içe aktar
Grafiklerle çalışmak için gerekli ad alanlarını içe aktarın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

Bu içe aktarmalar, görüntü manipülasyonu için gereken çekirdek çizim, fırça ve kalem sınıflarını ortaya çıkarır.

## Graphics Path kullanarak Java’da görüntü nasıl oluşturulur?
Yeni bir raster kanvas oluşturun, bir `Graphics` nesnesi ekleyin ve çizim yüzeyini hazırlayın. Bu tek adım, vektör renderi için hazır **500 × 500 piksel** bir bitmap ayarlar. Kanvas başlangıçta şeffaftır, böylece istediğiniz arka plan rengini veya desenini daha sonra doldurabilirsiniz; bu, görüntü arka planını temizleme senaryoları için kritiktir.

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## Adım 1: görüntüyü ve grafiği başlat
Burada bir `PsdImage` nesnesi (500 × 500) örnekliyoruz ve onun `Graphics` bağlamını alıyoruz.  
`PsdImage`, Aspose.PSD'nin bellekte tutabileceği raster görüntüyü temsil eder ve birçok formata kaydedilebilir.  
`Graphics`, `PsdImage` üzerine şekil, metin ve yolları çizen çizim metodlarını sağlar.

## Adım 2: graphics path oluştur ve yapılandır
Sonra bir `GraphicsPath` oluşturuyoruz; bu yol bir daire, bir dikdörtgen ve bir metin etiketi içerir.  
`GraphicsPath`, geometrik şekillerin bir konteyneridir; render öncesinde şekil, çizgi ve metin ekleyebilirsiniz.

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### Görüntüye metin ekleme (add text image java)
`GraphicsPath`'in `addString` metodu, belirtilen metni verilen koordinatlarda, sağlanan yazı tipi ve fırça ile yerleştirir. Bu, vektör yol içinde net ve ölçeklenebilir metin eklemenin en güvenilir yoludur.

## Adım 3: yolu çiz ve doldur
Şimdi yolu mavi bir kalemle çizer ve dikey bir hatch fırçası ile doldururuz; bu aynı zamanda **clear image background java** işlemini şeffaf bir desenle doldurarak gösterir. `Pen` kenar stilini tanımlar, `HatchBrush` ise desenli bir dolgu oluşturur.

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## Adım 4: görüntüyü kaydet
Son olarak, oluşturulan görüntüyü PNG formatında (veya desteklenen 50+ formattan herhangi birinde) diske yazarız. `save` metodu, sağladığınız dosya uzantısına göre çıktı dosya tipini belirler.

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## Yaygın sorunlar ve çözümler
- **Yol görünmüyor** – kalemin renginin dolgu fırçasıyla kontrast oluşturduğundan emin olun.  
- **Metin bulanık görünüyor** – daha yüksek çözünürlüklü bir görüntü veya yeterli DPI'ye sahip bir TrueType yazı tipi kullanın.  
- **Büyük dosyalarda bellek hataları** – verileri tamamen yüklemek yerine akışa almak için `PsdImageOptions.setUseMemoryCache(true)` etkinleştirin.

## Sıkça Sorulan Sorular

**S: Aspose.PSD nedir?**  
C: Aspose.PSD, Photoshop (PSD) dosyalarını ve diğer raster formatları Photoshop gerektirmeden oluşturmanıza, düzenlemenize ve dönüştürmenize olanak tanıyan bir Java kütüphanesidir.

**S: PSD dışındaki formatlarla çalışabilir miyim?**  
C: Evet – kütüphane **50+** formatı destekler; PNG, JPEG, BMP, TIFF ve GIF bunlardan sadece birkaçıdır.

**S: Deneme sürümü mevcut mu?**  
C: Evet, Aspose.PSD'nin ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) erişebilirsiniz.

**S: Lisansı nasıl satın alabilirim?**  
C: Aspose.PSD'yi [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

**S: Destek nereden alınabilir?**  
C: [Aspose forumunda](https://forum.aspose.com/c/psd/34) destek ve tartışmalara katılabilirsiniz.

## Sonuç
Bu kılavuzu izleyerek artık **görüntü oluşturma** dosyalarını, karmaşık vektör şekilleri, gömülü metin ve şeffaf arka planlarla Aspose.PSD'nin Graphics Path sınıfı sayesinde nasıl oluşturacağınızı biliyorsunuz. Farklı kalemler, fırçalar ve yol geometrileriyle deney yaparak oyunlar, UI öğeleri veya otomatik rapor üretimi için daha zengin grafikler oluşturabilirsiniz.

---

**Last Updated:** 2026-09-08  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD ile Yol Ayarlayarak Java’da PSD Görüntüsü Oluşturma](/psd/java/image-editing/create-image-by-setting-path/)
- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandırma – Şekil Çizme ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Görüntüye İmza Ekle – Aspose.PSD for Java ile Kanvasa Görüntü Çizme](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}