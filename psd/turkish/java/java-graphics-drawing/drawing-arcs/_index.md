---
date: 2026-09-03
description: Aspose.PSD for Java kullanarak java graphics draw arc nasıl yapılacağını
  öğrenin. PSD dosyalarında yaylar oluşturmak için adım adım rehber ve kod parçacıkları.
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Java'da Yay Çizme
og_description: Aspose.PSD for Java ile java graphics draw arc nasıl yapılacağını
  öğrenin. Bu öğreticide ön koşullar, kod adımları ve PSD dosyalarında yaylar oluşturmak
  için ipuçları gösterilmektedir.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: Java'da java graphics draw arc nasıl yapılır – Aspose.PSD rehberi
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: Java'da java graphics draw arc nasıl yapılır
url: /tr/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da graphics draw arc nasıl yapılır

## Giriş
Bu öğreticide Aspose.PSD for Java kütüphanesini kullanarak **java graphics draw arc** nasıl yapılacağını keşfedeceksiniz. Yayları programlı olarak çizmek, özel UI bileşenleri, veri görselleştirmeleri ve grafik‑zengin raporlar için yaygın bir gereksinimdir. Aspose.PSD for Java, Photoshop (PSD) dosyaları üzerinde tam kontrol sağlar; Photoshop yüklü olmadan görüntüler oluşturmanıza, düzenlemenize ve dışa aktarmanıza olanak tanır.

## Hızlı cevaplar
- **Java'da yay çizimini destekleyen kütüphane hangisidir?** Aspose.PSD for Java.
- **Üretim kullanımında lisansa ihtiyacım var mı?** Evet, deneme dışı dağıtımlar için ticari bir lisans gereklidir.
- **Hangi dosya formatlarına dışa aktarabilirim?** BMP, PNG, JPEG, TIFF, GIF ve daha fazlası.
- **Yayın kalınlığını ve rengini değiştirebilir miyim?** Evet, `drawArc` metoduna geçirilen `Pen` nesnesi aracılığıyla.
- **API Java 8 ve sonrası ile uyumlu mu?** Java 8‑21 ile tamamen uyumludur.

## Java graphics draw arc nedir?
`java graphics draw arc`, Java'ın çizim API'lerini kullanarak bir grafik yüzeyine eğri bir çizgi segmenti—bir yay—çizme sürecine denir. Aspose.PSD bağlamında, bu işlem bir PSD dosyasındaki katmanı temsil eden `Graphics` nesnesi üzerinde gerçekleştirilir.

## Yayları çizmek için Aspose.PSD for Java neden kullanılmalı?
Aspose.PSD, **50+** görüntü ve belge formatını destekler, **2 GB**'a kadar PSD dosyalarını işleyebilir ve tüm dosyayı belleğe yüklemeden çok sayfalı belgeleri işleyebilir. Bu ölçülebilir performans, hız ve bellek kullanımının önemli olduğu sunucu‑tarafı grafik üretimi için idealdir.

## Önkoşullar
1. **Java Geliştirme Ortamı** – Java'yı [Oracle'ın web sitesinden](https://www.oracle.com/java/) indirin.  
2. **Aspose.PSD for Java Kütüphanesi** – En son JAR'ı [indirme sayfasından](https://releases.aspose.com/psd/java/) indirin. Sağlanan talimatları izleyerek JAR'ı projenizin sınıf yoluna ekleyin.

## Java'da graphics draw arc nasıl yapılır?
Yeni bir `PsdImage` yükleyin, onun `Graphics` yüzeyini elde edin, istediğiniz renk ve kalınlıkta bir `Pen` yapılandırın ve `drawArc` metodunu çağırın. Bu kısa sekans yay oluşturur ve sonucu tek bir metod zincirinde kaydeder. Sınırlayıcı dikdörtgeni ve açı parametrelerini ayarlayarak yayının boyutunu, konumunu ve süresini tasarım gereksinimlerinize göre kontrol edebilirsiniz.

### Adım 1: Java projenizi kurun
Favori IDE'nizde yeni bir Java projesi oluşturun ve Aspose.PSD JAR'ını derleme yoluna ekleyin. JAR'ın doğru şekilde referans alındığından emin olun, böylece derleyici kütüphane sınıflarını bulabilir.

### Adım 2: Gerekli paketleri içe aktarın
Başlamak için, Aspose.PSD for Java'dan gerekli paketleri içe aktarın:
`Pen` sınıfı, yay çizmek için kullanılan çizginin rengini, genişliğini ve stilini tanımlar.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
Bu içe aktarmalar, yay çizimi için gereken `PsdImage`, `Graphics`, `Pen` ve renk sınıflarını ortaya çıkarır.

### Adım 3: Görüntü ve grafik nesnelerini başlatın
`PsdImage` örneği oluşturun ve üzerine çizim yapmak için bir `Graphics` nesnesi edinin:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
`"Your Document Directory"` ifadesini, çıktı dosyalarını kaydetmek istediğiniz klasörle değiştirin.

### Adım 4: Yay parametrelerini tanımlayın
Yayın geometrisini ve stilini ayarlayın—sınırlayıcı dikdörtgeni, başlangıç açısını, süpürme açısını, rengi ve kalınlığı:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
Değerleri ihtiyacınız olan görsel tasarıma uyacak şekilde ayarlayın; örneğin, 45°'de başlayan ve 270° süren 200 px yarıçaplı bir yay.

### Adım 5: Yayı çizin ve görüntüyü kaydedin
`Graphics` nesnesi üzerinde `drawArc` metodunu çağırın ve PSD'yi (veya başka bir formata dışa aktarın) kalıcı hale getirin:
`Graphics` sınıfının `drawArc` metodu, belirtilen `Pen` kullanarak sınırlayıcı dikdörtgen, başlangıç açısı ve süpürme açısı ile tanımlanan bir yay çizer.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
Bu kod parçacığı yayını tuval üzerine çizer ve BMP dosyası olarak kaydeder. `outputPath` içindeki dosya uzantısını değiştirerek PNG, JPEG veya TIFF olarak dışa aktarabilirsiniz.

## Yaygın tuzaklar ve sorun giderme
- **Incorrect angle units** – Aspose.PSD açıları derece olarak bekler, radyan olarak değil. Radyan sağlamak beklenmedik sonuçlar verir.
- **Pen thickness too large** – Çok kalın kalemler yayının görüntü sınırlarını aşmasına neden olabilir; kalınlığı azaltın veya tuvali büyütün.
- **File path issues** – Mutlak yollar kullanın veya çalışma dizininin yazma izinlerine sahip olduğundan emin olun, `IOException` hatasından kaçınmak için.

## Sıkça sorulan sorular

**Q: Aspose.PSD for Java yaylar dışında başka şekilleri de işleyebilir mi?**  
**A:** Evet, kütüphane aynı `Graphics` API'sini kullanarak dikdörtgenler, elipsler, çizgiler, çokgenler ve özel yollar çizebilir.

**Q: Yay rengini ve kalınlığını nasıl değiştiririm?**  
**A:** İstediğiniz `Color` ve genişlikte bir `Pen` oluşturun, ardından bu `Pen` örneğini `drawArc` metoduna geçirin.

**Q: PSD'yi BMP dışındaki bir formata dışa aktarmak mümkün mü?**  
**A:** Kesinlikle. Aspose.PSD PNG, JPEG, TIFF, GIF ve daha birçok formatı destekler – sadece `save` metodundaki dosya uzantısını değiştirin.

**Q: Daha fazla örnek ve topluluk desteği nereden bulunur?**  
**A:** Eğitimler, kod örnekleri ve diğer geliştiricilerden yardım için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

**Q: Kütüphane büyük PSD dosyalarıyla çalışır mı?**  
**A:** Evet, akış mimarisi sayesinde dosyaları 2 GB'a kadar işleyebilir ve tüm belgeyi belleğe yüklemeden yayları çizebilir.

---

**Son Güncelleme:** 2026-09-03  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java kullanarak bir PSD'de Dikdörtgen Çiz ve Kaydet](/psd/java/basic-image-operations/simple-drawing/)
- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandır – Şekil Çiz ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Aspose.PSD kullanarak Java'da Çizgi Rengini Değiştirme](/psd/java/advanced-image-effects/add-stroke-layer-color/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}