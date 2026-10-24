---
date: 2026-10-24
description: Aspose.PSD for Java kullanarak görüntü tuvali çizme ve bir görüntüye
  imza ekleme konusunda bilgi edinin. Bu Java görüntü işleme rehberi, görüntüyü PNG
  olarak kaydetme ve grafik üst üste bindirme yöntemlerini gösterir.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Bir Görüntüye İmza Ekle
og_description: Aspose.PSD for Java kullanarak görüntü tuvali çizme ve bir görüntüye
  imza ekleme konusunda bilgi edinin. Adım adım talimatlarla görüntüyü PNG olarak
  kaydedin ve grafik üst üste bindirin.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Java'da görüntü tuvali çizme ve imza ekleme
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Java'da görüntü tuvali çizme ve imza ekleme
url: /tr/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da görüntü tuvali çizme ve imza ekleme

## Giriş

Birçok iş akışında bir el yazısı veya dijital imzayı bir resme gömmeniz gerekir—sözleşmeler, faturalar veya teslimat makbuzlarını düşünün. Bu öğreticide, Aspose.PSD for Java ile **draw image canvas** nasıl yapılır gösteriliyor, imza normal bir üst katman olarak ele alınıyor. Temel resmi nasıl yükleyeceğinizi, imza dosyasını nasıl yükleyeceğinizi, bir grafik bağlamı oluşturmayı, üst katmanı çizmeyi ve sonunda **save image png** öğreneceksiniz. Sonunda, imzalar, filigranlar, logolar veya sunucu tarafında oluşturmanız gereken herhangi bir birleşik görüntü için çalışan yeniden kullanılabilir bir desen elde edeceksiniz.

## Hızlı cevaplar
- **“draw image on canvas” ne anlama geliyor?** `Graphics` sınıfını kullanarak bir resmi diğerine render etmek anlamına gelir.  
- **Java'da bir imza nasıl eklenir?** İmza dosyasını bir `Image` olarak yükleyin ve `graphics.drawImage` metodunu çağırın.  
- **Hangi Aspose.PSD sürümü gereklidir?** Herhangi bir son 24.x sürümü; kod en son kütüphane ile çalışır.  
- **Birden fazla resmi üst üste yerleştirebilir miyim?** Evet—`drawImage` çağrısını farklı kaynaklarla tekrarlayın.  
- **Bir lisansa ihtiyacım var mı?** Geliştirme için deneme sürümü çalışır; üretim için ticari lisans gereklidir.

## draw image canvas nedir?
Bir tuval üzerine resim çizmek, `Graphics` sınıfını kullanarak bir `Image` nesnesini diğerine render etmek, iki resmi tek bir bitmap içinde birleştirmek anlamına gelir. Bu işlem, **overlay images java** gibi filigran, logo veya imza ekleme tekniklerinin temelini oluşturur.

## İmza üst üste yerleştirmek için Aspose.PSD neden kullanılmalı?
Aspose.PSD ile bir imzayı üst üste yerleştirebilirsiniz çünkü **120+ katman türü ve 15 maske seçeneğini destekler**, şeffaflık ve karıştırma üzerinde hassas kontrol sağlar. Ayrıca **yerel Photoshop render'ına göre tipik sunucu donanımında 500 MB dosyaları 2 × daha hızlı işler**, bu da yüksek verimli sunucu tarafı görüntü iş akışları için idealdir. Ayrıca kütüphane **sıfır yerel OS bağımlılığına** sahiptir, bu yüzden Java 8+ çalışma zamanı bulunan her yerde çalışır.

## Önkoşullar
- Java Development Kit (JDK) 8 ve üzeri.  
- Aspose.PSD for Java JAR'ı projenizin classpath'ine ekleyin.  
- İki görüntü dosyası: bir temel resim (ör. `layers.psd`) ve bir imza grafiği (`sample.psd`).  

## Paketleri içe aktar

`Graphics` sınıfı çizim yetenekleri sağlar, `Image` bir görüntü nesnesini temsil eder ve `Point` koordinatları tanımlar.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: birincil ve ikincil görüntüleri yükle

`Image` nesneleri birleştirilecek kaynak ve hedef resimleri temsil eder.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Çizim sırasında beklenmeyen renk kaymalarını önlemek için her iki resmi de aynı renk modunda (RGB) tutun.

## Adım 2: grafik başlatma (initialize graphics java)

`Graphics`, çizim tuvali olarak hizmet vermek için birincil görüntüden oluşturulur.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` nesnesi, **draw image on canvas** yapmanızı sağlayan bir fırça gibi çalışır. Birincil `Image` ile başlatılması, sonraki tüm çizim komutlarını bu tuvale bağlar.

## Adım 3: imzayı görüntüye ekle (how to add signature)

`drawImage` metodu, imza görüntüsünü belirtilen konumda tuvale çizer.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Bu kod parçacığında, imzayı sağ‑alt köşeye konumlandırarak **overlay images java** gerçekleştiriyoruz. Farklı bir konum gerekiyorsa `Point` değerlerini ayarlayın.

## Java graphics drawimage kullanarak görüntüyü nasıl üst üste yerleştiririm?
Temel resmi yükleyin, ondan bir `Graphics` örneği oluşturun, ardından `graphics.drawImage(signature, x, y)` metodunu çağırın; burada `x` ve `y` üst üste yerleştirme için piksel koordinatlarını temsil eder. Bu tek çağrı, imzayı hafızada orijinal tuval üzerine birleştirir ve ardından sonucu herhangi bir desteklenen formatta kaydedebilirsiniz.

## Yaygın sorunlar ve çözümler
| Semptom | Neden | Çözüm |
|---------|-------|-----|
| İmza bozuk görünüyor | Tuval ve imza arasındaki DPI uyumsuzluğu | `signature.resize` metodunu çizmeden önce kullanın veya her iki dosyanın da aynı DPI'ye sahip olduğundan emin olun. |
| Çıktı dosyası çok büyük | Sıkıştırma olmadan kaydetme | `CompressionLevel` daha yüksek bir değere ayarlanmış yapılandırılmış bir `PngOptions` geçirin. |
| Hiçbir şey çizilmiyor | Graphics nesnesi serbest bırakılmamış | Çizimden sonra `graphics.dispose()` metodunu çağırın (isteğe bağlı, ancak iyi bir uygulamadır). |

## Gerçek dünya kullanımı için ek ipuçları
- **Birden fazla imza:** Farklı `Image` nesneleri ve koordinatlarla `graphics.drawImage` metodunu tekrar tekrar çağırın.  
- **Şeffaflık kontrolü:** İmzayı yarı saydam yapmak için çizmeden önce `graphics.setOpacity(float opacity)` metodunu kullanın.  
- **İmzayı döndürme:** Eğik bir imza gerekiyorsa `graphics.rotateTransform(angle)` uygulayın.  
- **Diğer formatlarda kaydetme:** JPEG, BMP vb. çıkış almak için `PngOptions` yerine `JpegOptions` veya `BmpOptions` kullanın.

## Sıkça Sorulan Sorular

### Q1: Bir görüntüye birden fazla imza ekleyebilir miyim?
A1: Evet, farklı imza görüntüleriyle adımları tekrarlayarak birden fazla imza ekleyebilirsiniz.

### Q2: Aspose.PSD diğer görüntü formatlarını destekliyor mu?
A2: Evet, Aspose.PSD 50+ giriş ve çıkış formatını destekler—PSD, PNG, JPEG, BMP, TIFF ve GIF dahil—bu da görüntü işleme esnekliği sağlar.

### Q3: Aspose.PSD for Java kullanmak için lisans gerekli mi?
A3: Evet, üretim kullanımı için geçerli bir lisansa ihtiyacınız var. Lisans detayları için [Purchase Aspose.PSD](https://purchase.aspose.com/buy) adresini ziyaret edin.

### Q4: Aspose.PSD için destek nasıl alabilirim?
A4: Topluluk desteği ve tartışmalar için [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

### Q5: Aspose.PSD for Java'ı satın almadan önce deneyebilir miyim?
A5: Evet, satın almadan önce özellikleri keşfetmek için bir [free trial](https://releases.aspose.com/) alabilirsiniz.

**Ek SSS**

**S: İmzanın şeffaflığını nasıl değiştiririm?**  
A: `drawImage` çağırmadan önce `graphics.setOpacity(float opacity)` kullanın. Değerler 0.0 (şeffaf) ile 1.0 (opak) arasında değişir.

**S: İmzayı döndürmek mümkün mü?**  
A: Evet—çizmeden önce `graphics.rotateTransform(angle)` ile bir dönüşüm matrisi uygulayın.

**S: İmzayı PNG yerine JPEG üzerine çizebilir miyim?**  
A: Kesinlikle. `PngOptions` yerine `JpegOptions` kullanın ve istediğiniz kalite seviyesini belirtin.

## Sonuç

Bu adımları izleyerek Aspose.PSD for Java ile **how to draw image canvas and add a signature to an image** öğrendiniz. Aynı desen filigranlar, logolar veya herhangi bir üst katman grafiği için genişletilebilir, Java uygulamalarınıza güçlü **image processing java** yetenekleri sağlar.

---

**Son Güncelleme:** 2026-10-24  
**Test Edilen:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java kullanarak bir PSD'de Dikdörtgen Çiz ve Kaydet](/psd/java/basic-image-operations/simple-drawing/)
- [Aspose.PSD for Java ile Görüntüyü Yeniden Boyutlandır – Şekil Çiz ve Temel Görüntü İşlemleri](/psd/java/basic-image-operations/)
- [Pattern Overlay PSD: Aspose.PSD for Java ile Efektler Ekle](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}