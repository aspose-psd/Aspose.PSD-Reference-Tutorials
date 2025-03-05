---
title: Aspose.PSD for Java ile Bir Görüntüyü Belirli Bir Açıda Döndürme
linktitle: Bir Görüntüyü Belirli Bir Açıda Döndürme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java ile Java'da görüntü döndürmeyi keşfedin. Görüntüleri belirli açılarda zahmetsizce döndürün.
type: docs
weight: 20
url: /tr/java/advanced-image-manipulation/rotate-image-specific-angle/
---
## giriiş

Java geliştirmenin dinamik dünyasında, görüntüleri değiştirmek çeşitli uygulamalar için ortak bir gereksinimdir. Aspose.PSD for Java, görüntü döndürme işlemini zahmetsizce gerçekleştirmek için güçlü özellikler sunan sağlam bir çözüm olarak ortaya çıkıyor. Bu eğitimde, Aspose.PSD for Java'yı kullanarak bir görüntüyü belirli bir açıda döndürme sürecinde size rehberlik edeceğiz. Ayrıntılara dalmadan önce bazı önkoşullarla zemini hazırlayalım.

## Önkoşullar

Bu görüntü döndürme yolculuğuna çıkmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

### 1. Java Geliştirme Ortamı
Sisteminizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

### 2. Java Kütüphanesi için Aspose.PSD
 Aspose.PSD for Java kütüphanesini indirip yükleyin. Gerekli kütüphaneyi ve dokümantasyonu bulabilirsiniz[Burada](https://reference.aspose.com/psd/java/).

### 3. Örnek Resim
Döndürmek istediğiniz örnek bir resmi (örneğin, "sample.psd") hazırlayın. Belge dizininize yerleştirin.

## Paketleri İçe Aktar

Şimdi görüntü döndürme işlemine başlamak için gerekli paketleri içe aktaralım:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

Şimdi bir görüntüyü belirli bir açıda döndürme işlemini takip edilmesi kolay bir dizi adıma ayıralım.

## 1. Adım: Belge Dizininizi Tanımlayın

```java
String dataDir = "Your Document Directory";
```

"Belge Dizininiz"i belge dizininizin gerçek yolu ile değiştirdiğinizden emin olun.

## Adım 2: Kaynak ve Hedef Dosya Yollarını Belirleyin

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Kaynak dosya yolunu örnek görüntünüzün konumuna ayarlayın ve döndürülen görüntünün hedef dosya yolunu belirtin.

## 3. Adım: Görüntüyü Yükleyin

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

Aspose.PSD'yi kullanarak örnek görüntüyü yükleyin.

## Adım 4: Görüntü Verilerini Önbelleğe Alın

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Döndürme sırasında daha iyi performans için görüntü verilerini önbelleğe alın.

## Adım 5: Görüntüyü Döndürün

```java
image.rotate(20f, true, Color.getRed());
```

Orantılı boyutu koruyarak ve kırmızı arka plan rengini kullanarak döndürmeyi 20 derecelik bir açıyla gerçekleştirin.

## Adım 6: Sonucu Kaydet

```java
image.save(destName, new JpegOptions());
```

Döndürülmüş görüntüyü belirtilen seçeneklerle (bu durumda JpegOptions kullanarak) yeni bir dosyaya kaydedin.

Tebrikler! Aspose.PSD for Java'yı kullanarak bir görüntüyü belirli bir açıda başarıyla döndürdünüz.

## Çözüm

Bu eğitimde Aspose.PSD for Java ile görüntüleri döndürmenin kusursuz sürecini araştırdık. Kütüphanenin güçlü özellikleri, Java geliştiricilerinin görüntüleri zahmetsizce değiştirmesine olanak tanır ve sayısız yaratıcı olasılığa kapı açar.

## SSS'ler

### S1: Aspose.PSD for Java'yı kullanarak şeffaf görüntüleri döndürebilir miyim?

Evet, Aspose.PSD for Java, görsellerin şeffaf olarak döndürülmesini destekler. Kodunuzda şeffaflıkla ilgili seçenekleri uygun şekilde ele aldığınızdan emin olun.

### S2: Döndürme için desteklenen görüntü dosyası formatlarında herhangi bir sınırlama var mı?

Hayır, Aspose.PSD for Java, aralarında PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF ve daha fazlasının da bulunduğu çok çeşitli görüntü dosyası formatlarını destekler.

### S3: Görüntüleri negatif açıyla döndürebilir miyim?

 Kesinlikle! Negatif bir açıyı belirtebilirsiniz.`image.rotate()` görüntüleri ters yönde döndürme yöntemi.

### S4: Aspose.PSD for Java, döndürme sırasında gerçek zamanlı görüntü önizlemesi sağlıyor mu?

Aspose.PSD for Java öncelikle arka uç görüntü işlemeye odaklanır. Gerçek zamanlı görüntü önizlemesi için diğer teknolojileri kullanarak bir ön uç çözümü uygulamanız gerekebilir.

### S5: Aspose.PSD için yardım isteyebileceğim bir topluluk forumu var mı?

 Evet, ziyaret edebilirsiniz[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) toplulukla etkileşime geçmek, sorular sormak ve yardım istemek.