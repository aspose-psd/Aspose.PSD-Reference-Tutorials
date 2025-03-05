---
title: Aspose.PSD for Java ile Bir Görüntünün Parlaklığını Ayarlama
linktitle: Bir Görüntünün Parlaklığını Ayarlama
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java'da görüntü parlaklığını artırın. Görüntü parlaklığını programlı olarak ayarlamak için adım adım kılavuz.
type: docs
weight: 21
url: /tr/java/advanced-techniques/adjust-brightness/
---
## giriiş

Görüntüleri geliştirmek grafik tasarım ve dijital fotoğrafçılıkta yaygın bir gerekliliktir. Aspose.PSD for Java, görüntü parlaklığını programlı olarak ayarlamak için güçlü bir çözüm sunar. Bu eğitimde, bir görüntünün parlaklığını adım adım ayarlamak için Aspose.PSD for Java kütüphanesini nasıl kullanabileceğimizi keşfedeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

-  Aspose.PSD for Java Library: Kitaplığı şuradan indirip yükleyin:[Java belgeleri için Aspose.PSD](https://reference.aspose.com/psd/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarın. Bu örnekte aşağıdakileri kullanacağız:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Şimdi bir görüntünün parlaklığını ayarlama sürecini basit adımlara ayıralım:

## 1. Adım: Görüntüyü Yükleyin

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Mevcut bir görüntüyü RasterImage sınıfının bir örneğine yükleme
Image image = Image.load(sourceFile);
// Image nesnesini RasterImage'a yayınla
RasterImage rasterImage = (RasterImage) image;

// Daha iyi performans için RasterImage'ın önbelleğe alınıp alınmadığını kontrol edin ve RasterImage'ı Önbelleğe Alın
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Bu adımda hedef görüntüyü yükleyip bir`RasterImage` daha fazla işlem için.

## 2. Adım: Parlaklığı Ayarlayın

```java
// Parlaklığı ayarlayın
rasterImage.adjustBrightness(-50);
```

 Burada şunu kullanıyoruz:`adjustBrightness`Görüntünün parlaklığını değiştirme yöntemi. Bu örnekte parlaklığı 50 birim azalttık ama siz bu değeri ihtiyaçlarınıza göre özelleştirebilirsiniz.

## 3. Adım: TiffOptions'ı ayarlayın

```java
int[] ushort = {8, 8, 8};
// Ortaya çıkan görüntü için bir TiffOptions örneği oluşturun
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Yapılandır`TiffOptions` Ayarlanan görüntüyü kaydetmek için. Ayarlayın`bitsPerSample` Ve`photometric` Özel ihtiyaçlarınıza göre özellikler.

## Adım 4: Ortaya Çıkan Görüntüyü Kaydedin

```java
// Ortaya çıkan görüntüyü kaydedin
rasterImage.save(destName, tiffOptions);
```

 Son olarak, değiştirilen görüntüyü belirtilen yöntemi kullanarak kaydedin.`TiffOptions`.

## Çözüm

Aspose.PSD for Java ile görüntünün parlaklığını programlı olarak ayarlamak artık çok kolay. Bu eğitimde, bu işlevselliği Java uygulamalarınızda uygulamaya yönelik kapsamlı bir kılavuz sağlanmıştır.

## SSS'ler

### S1: Parlaklığı PSD'nin yanı sıra diğer görüntü formatlarında da ayarlayabilir miyim?

Cevap1: Evet, Aspose.PSD for Java, JPEG, PNG ve TIFF gibi çeşitli görüntü formatlarını destekler.

### S2: Görüntü ayarlama işlemi sırasındaki hataları nasıl halledebilirim?

Cevap2: Oluşabilecek istisnaları yönetmek için try-catch bloklarını kullanarak hata işlemeyi uygulayabilirsiniz.

### S3: Parlaklık ayarı aralığının bir sınırı var mı?

Cevap3: Ayar aralığı görüntü içeriğine ve formatına bağlıdır, ancak Aspose.PSD özelleştirmede esneklik sağlar.

### S4: Aspose.PSD for Java'yı ticari projelerde kullanabilir miyim?

 C4: Evet, Aspose.PSD for Java ticari bir kütüphanedir ve lisansını şu adresten alabilirsiniz:[Burada](https://purchase.aspose.com/buy).

### S5: Aspose.PSD for Java'nın ücretsiz deneme sürümü mevcut mu?

 C5: Evet, kütüphaneyi ücretsiz deneme sürümüyle keşfedebilirsiniz.[Burada](https://releases.aspose.com/).