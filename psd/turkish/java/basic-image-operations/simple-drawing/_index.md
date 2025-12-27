---
date: 2025-12-27
description: Aspose.PSD for Java kullanarak PSD dosyalarında kırmızı dikdörtgen ve
  diğer şekilleri nasıl çizeceğinizi öğrenin. Bu adım adım rehber, belge oluşturmayı,
  katman eklemeyi ve kod örnekleriyle çizmeyi kapsar.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Kırmızı Dikdörtgen Çizin
url: /tr/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Kırmızı Dikdörtgen Çizme

## Introduction

Aspose.PSD for Java kullanarak **kırmızı dikdörtgen çizmeyi** adım adım gösteren bu kılavuza hoş geldiniz! Bu öğreticide yeni bir PSD belgesi oluşturmayı, bir katman eklemeyi ve özel renklerle şekiller çizmeyi anlatacağız. Grafik varlıklarını otomatikleştiriyor ya da bir tasarım aracı arka ucunu inşa ediyor olun, bu öğretici size temel yapı taşlarını sunar.

## Quick Answers
- **PSD dosyası oluşturmak için birincil sınıf nedir?** `PsdImage`
- **Bir katmanın arka plan rengini temizleyen yöntem hangisidir?** `Graphics.clear(Color)`
- **Kırmızı bir dikdörtgen nasıl çizilir?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim için lisans gereklidir.
- **Aynı API ile mevcut PSD dosyalarını manipüle edebilir miyim?** Evet, Aspose.PSD tam PSD düzenlemeyi destekler.

## What is drawing a red rectangle in a PSD file?
Kırmızı bir dikdörtgen çizmek, `Graphics` nesnesini kullanarak bir PSD görüntüsünün belirli bir katmanına kırmızı renk ile doldurulmuş veya kenarlığı çizilmiş bir dikdörtgen şekli oluşturmak anlamına gelir. Bu işlem, alanları vurgulamak, yer tutucular oluşturmak veya basit grafikler eklemek için programlı olarak yaygın olarak kullanılır.

## Why use Aspose.PSD for Java to manipulate PSD files?
Aspose.PSD, Photoshop yüklü olmadan Photoshop PSD dosyalarını okumanıza, düzenlemenize ve yazmanıza olanak tanıyan saf Java API'si sunar. Katman yönetimi, renk manipülasyonu ve vektör çizimini destekler; bu da sunucu tarafı görüntü işleme, otomatik varlık hatları ve özel grafik üretimi için idealdir.

## Prerequisites

- Makinenizde Java Development Kit (JDK) yüklü olmalıdır.  
- Aspose.PSD for Java kütüphanesi. Bunu [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) adresinden indirebilirsiniz.

## Import Packages

Başlamak için, gerekli sınıfları Java projenize içe aktarın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Step 1: Create a New Document

İlk olarak, istenen tuval boyutuyla yeni bir PSD belgesi oluşturun. Bu belge, üzerinde çizeceğimiz katmanı barındıracaktır.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Step 2: Add a Layer

Sonra, görüntünün tam genişlik ve yüksekliğini kapsayan yeni bir boş katman ekleyin. Katmanlar, çizim işlemlerini ayırmak için gereklidir.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Step 3: Draw Shapes

`Graphics` sınıfını kullanarak katmanın piksel verilerini manipüle edeceğiz. Aşağıda arka planı temizleme ve farklı renklerde dikdörtgenler çizme örneklerini gösteren üç örnek bulunmaktadır.

### Clear Layer Color (set background to yellow)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Draw a Red Rectangle (primary focus)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Draw a Blue Rectangle (additional example)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Step 4: Save the Changes

Son olarak, değiştirilen PSD görüntüsünü diske yazın. Dosya yeni katmanı ve çizilen şekilleri içerecektir.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Common Issues and Solutions

- **Katman çizimden sonra görünmüyorsa:** Katmanın `Graphics` nesnesi oluşturulmadan **önce** görüntüye eklendiğinden emin olun.
- **Renkler yanlış görünüyor:** `Color.getRed()` (veya diğer statik yöntemler) kullandığınızı, aralık dışı özel RGB değerleri kullanmadığınızı doğrulayın.
- **Dosya kaydedilmiyor:** `outputDir` yolunun var olduğunu ve uygulamanın yazma izinlerine sahip olduğunu kontrol edin.

## Frequently Asked Questions

### Q1: Can I use Aspose.PSD for Java to manipulate existing PSD files?

A1: Evet, Aspose.PSD for Java mevcut PSD dosyalarını düzenlemek ve manipüle etmek için kapsamlı işlevsellik sunar.

### Q2: Where can I find support for Aspose.PSD for Java?

A2: Destekle ilgili sorularınız için [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edebilirsiniz.

### Q3: Is there a free trial available for Aspose.PSD for Java?

A3: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### Q4: How can I purchase a license for Aspose.PSD for Java?

A4: Lisansı [Aspose.PSD Satın Alma Sayfası](https://purchase.aspose.com/buy) üzerinden satın alabilirsiniz.

### Q5: Are temporary licenses available for Aspose.PSD for Java?

A5: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

## Additional Frequently Asked Questions

**S: Dikdörtgen dışında başka şekiller çizebilir miyim?**  
C: Evet, `Graphics` sınıfı elips, çizgi ve özel yollar çizmeyi de destekler.

**S: Çizilen şekillerde şeffaflık destekleniyor mu?**  
C: Kesinlikle; alfa şeffaflığı eklemek için ARGB renkli `SolidBrush` kullanabilirsiniz.

**S: Bir katmanın opaklığını düzenlemek mümkün mü?**  
C: Evet, her `Layer` nesnesinin 0 ile 255 arasında bir değer alan `setOpacity` yöntemi vardır.

**S: Yeni bir dosya oluşturmak yerine mevcut bir PSD dosyasını nasıl yüklersiniz?**  
C: Katmanları manipüle etmeden önce `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` ifadesini kullanın.

## Conclusion

Artık Aspose.PSD for Java kullanarak bir PSD dosusunda **kırmızı dikdörtgen** ve diğer temel şekilleri nasıl çizeceğinizi öğrendiniz. Bir belge oluşturup, bir katman ekleyip, arka planını temizleyerek ve `Graphics` API'siyle çizim yaparak birçok grafik‑tasarım görevini otomatikleştirebilirsiniz. Farklı fırçalar, katman efektleri ve dosya formatlarıyla deneyerek daha fazla keşfedin.

---

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}