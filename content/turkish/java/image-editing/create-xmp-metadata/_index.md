---
title: Aspose.PSD for Java ile XMP Meta Verileri Oluşturun
linktitle: XMP Meta Verileri Oluşturun
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java uygulamalarınızı geliştirin. XMP meta verilerini zahmetsizce oluşturmayı öğrenin. Şimdi adım adım kılavuzumuzu takip edin.
type: docs
weight: 12
url: /tr/java/image-editing/create-xmp-metadata/
---
## giriiş

Java geliştirme alanında, görüntü meta verilerini yönetmek ve değiştirmek, çeşitli uygulamalar için çok önemlidir. Aspose.PSD for Java, PSD dosyalarını işlemek için güçlü bir araç olarak öne çıkıyor ve bu eğitimde, bu sağlam kitaplığı kullanarak XMP meta verileri oluşturmayı derinlemesine inceleyeceğiz.

## Önkoşullar

Bu eğitime başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java Geliştirme Ortamı: Sisteminizde Java'nın kurulu olması ve Java programlamaya ilişkin temel bir anlayışa sahip olmanız.
-  Aspose.PSD Kütüphanesi: Java için Aspose.PSD kütüphanesini indirin ve kurun. Kütüphaneyi ve ayrıntılı belgeleri bulabilirsiniz.[Burada](https://reference.aspose.com/psd/java/).
- Belge Dizininiz: Belge dosyalarınızın saklandığı dizini tanımlayın.

## Paketleri İçe Aktar

Aspose.PSD işlevlerinden yararlanmak için Java projenize gerekli paketleri içe aktarın:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## 1. Adım: Görüntü Boyutunu Belirleyin

```java
//Bir Dikdörtgen tanımlayarak görüntünün boyutunu belirtin
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## 2. Adım: Yeni Bir Görüntü Oluşturun

```java
// Örnek amaçlı yepyeni bir resim oluşturun
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## 3. Adım: XMP Başlığı Oluşturun

```java
// Bir XMP-Header örneği oluşturun
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## 4. Adım: XMP Fragmanı Oluşturun

```java
// Xmp-TrailerPi'nin bir örneğini oluşturun
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 5. Adım: XMP Meta Verilerini Oluşturun

```java
// Farklı nitelikleri ayarlamak için XMPmeta sınıfının bir örneğini oluşturun
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Adım 6: XMP Paket Sarmalayıcı Oluşturun

```java
// Tüm meta verileri içeren bir XmpPacketWrapper örneği oluşturun
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Adım 7: Photoshop Niteliklerini Ayarlayın

```java
// Photoshop paketinin bir örneğini oluşturun ve Photoshop niteliklerini ayarlayın
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Adım 8: Photoshop Paketini XMP Meta Verilerine Ekleme

```java
// Photoshop paketini XMP meta verilerine ekleme
xmpData.addPackage(photoshopPackage);
```

## Adım 9: DublinCore Niteliklerini Ayarlayın

```java
// DublinCore paketinin bir örneğini oluşturun ve DublinCore niteliklerini ayarlayın
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Adım 10: DublinCore Paketini XMP Meta Verilerine Ekleme

```java
// DublinCore Paketini XMP meta verilerine ekleyin
xmpData.addPackage(dublinCorePackage);
```

## Adım 11: XMP Meta Verilerini Görüntüye Güncelleyin

```java
//XMP meta verilerini görüntüye güncelleyin
image.setXmpData(xmpData);
```

## Adım 12: Resmi Kaydet

```java
// Görüntüyü diske veya bellek akışına kaydedin
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Çözüm

Tebrikler! Aspose.PSD for Java'yı kullanarak bir görüntü için XMP meta verilerini başarıyla oluşturdunuz. Bu eğitim sizi Java uygulamalarınızdaki meta verileri sorunsuz bir şekilde geliştirmek ve yönetmek için gerekli adımlarla donattı.

## SSS'ler

### S1: Aspose.PSD farklı görüntü formatlarıyla uyumlu mudur?

Cevap1: Evet, Aspose.PSD çeşitli görüntü formatlarını destekleyerek farklı dosya türlerinin işlenmesinde çok yönlülük sağlar.

### S2: Aspose.PSD'yi kullanarak mevcut meta verileri değiştirebilir miyim?

Cevap2: Kesinlikle Aspose.PSD, görsellerdeki mevcut meta verileri değiştirmenize ve güncellemenize olanak tanır.

### S3: Aspose.PSD'nin işleyebileceği görüntü boyutunda herhangi bir sınırlama var mı?

Cevap3: Aspose.PSD, çeşitli boyutlardaki görüntüleri işleyecek şekilde tasarlanmıştır ve projeleriniz için ölçeklenebilirlik sağlar.

### S4: Aspose.PSD'nin deneme sürümü mevcut mu?

 Cevap4: Evet, ücretsiz deneme sürümünü edinerek Aspose.PSD'nin yeteneklerini keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S5: Aspose.PSD ile ilgili sorgular için nereden destek alabilirim?

 A5: Herhangi bir yardım veya soru için şu adresi ziyaret edin:[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34).