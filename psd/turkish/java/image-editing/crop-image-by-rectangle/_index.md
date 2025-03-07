---
title: Java için Aspose.PSD'de Görüntüyü Dikdörtgenle Kırp
linktitle: Resmi Dikdörtgene Göre Kırp
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java'nın kesintisiz görüntü kırpma özelliklerini keşfedin. Aspose.PSD for Java'yı kullanarak görüntüleri zahmetsizce kırpmak için adım adım kılavuzumuzu izleyin.
weight: 15
url: /tr/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java için Aspose.PSD'de Görüntüyü Dikdörtgenle Kırp

## giriiş

Java geliştirme dünyasında görüntüleri değiştirmek yaygın bir görevdir ve Aspose.PSD for Java, görüntü işleme için güçlü bir çözüm sunar. Bu eğitimde, Aspose.PSD for Java'yı kullanarak bir görüntüyü dikdörtgen şeklinde kırpma sürecinde size rehberlik edeceğiz. Bunu kolaylıkla başarmak için aşağıdaki adımları izleyin.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Makinenizde Java Geliştirme Kiti (JDK) yüklü.
- Java kütüphanesi için Aspose.PSD. adresinden indirebilirsiniz.[web sitesi](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Aspose.PSD for Java'nın özelliklerinden yararlanmak için Java projenize gerekli paketleri eklediğinizden emin olun. Java dosyanızın başına aşağıdaki içe aktarma ifadelerini ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Şimdi Aspose.PSD for Java kullanarak bir görüntüyü dikdörtgen şeklinde kırpma konusunda size yol göstermek için süreci birden fazla adıma ayıralım.

## 1. Adım: Belge Dizininizi Kurun

```java
String dataDir = "Your Document Directory";
```

 Yer değiştirmek`"Your Document Directory"` PSD dosyanızın bulunduğu gerçek yolla.

## Adım 2: Kaynak ve Hedef Dosyaları Belirleyin

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Kaynak PSD dosyanızın ve hedef JPEG dosyasının yollarını tanımlayın.

## 3. Adım: Görüntüyü Yükleyin ve Önbelleğe Alın

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 PSD görüntüsünü bir`RasterImage` örneği ve verilerini önbelleğe alın.

## Adım 4: Kırpma Dikdörtgenini Oluşturun ve Tanımlayın

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Bir örneğini oluşturun`Rectangle` kırpma için istenen boyuta sahip sınıf.

## Adım 5: Görüntüyü Kırpın ve Kaydedin

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Belirtilen dikdörtgeni kullanarak kırpma işlemini gerçekleştirin ve sonuçları JPEG dosyası olarak kaydedin.

Parametreleri özel gereksinimlerinize göre ayarlayarak bu adımları gerektiği kadar tekrarlayın.

## Çözüm

Bu eğitimde Aspose.PSD for Java kullanarak bir görüntüyü dikdörtgen şeklinde kırpma sürecini anlattık. Bu adımları izleyerek güçlü görüntü işleme yeteneklerini Java uygulamalarınıza kolayca entegre edebilirsiniz.

## SSS'ler

### S1: Aspose.PSD for Java'yı diğer Java çerçeveleriyle kullanabilir miyim?

Cevap1: Evet, Aspose.PSD for Java, çeşitli Java çerçeveleriyle entegre edilebilir, bu da geliştirme projelerinizde esneklik sağlar.

### S2: Aspose.PSD for Java'nın ücretsiz deneme sürümü mevcut mu?

 Cevap2: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Nerede ek destek veya yardım bulabilirim?

 A3: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.

### S4: Aspose.PSD for Java için geçici lisansı nasıl edinebilirim?

 Cevap4: Geçici bir lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.PSD for Java'da kırpma için desteklenen görüntü formatları nelerdir?

Cevap5: Aspose.PSD for Java, PSD, PNG, JPEG ve daha fazlasını içeren çeşitli görüntü formatlarını destekler.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
