---
title: Java için Aspose.PSD ile Bir Görüntünün Gamasını Ayarlama
linktitle: Bir Görüntünün Gamasını Ayarlama
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak görüntü gammasını zahmetsizce ayarlamayı öğrenin. En iyi sonuçları elde etmek için adım adım kılavuzumuzu izleyin.
type: docs
weight: 23
url: /tr/java/advanced-techniques/adjust-gamma/
---
## giriiş

Görüntü işleme alanında, bir görüntünün gamasını ayarlamak, görsel çekiciliğini artırmak için çok önemli bir adımdır. Aspose.PSD for Java, Java geliştiricilerinin görüntü gammasını zahmetsizce işlemesi için güçlü bir çözüm sunar. Bu eğitimde, Aspose.PSD'yi kullanarak gammayı nasıl ayarlayacağınızı keşfedeceğiz ve sorunsuz bir uygulama sağlamak için her adımı ayrıntılı olarak inceleyeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulları oluşturduğunuzdan emin olun:

1. Java Geliştirme Ortamı: Sisteminizde bir Java geliştirme ortamının kurulu olduğundan emin olun.
2.  Aspose.PSD Kütüphanesi: Aspose.PSD kütüphanesini indirin ve Java projenize entegre edin. Gerekli kaynakları şurada bulabilirsiniz.[dokümantasyon](https://reference.aspose.com/psd/java/).
3. Örnek Resim: Gama ayarlamasını uygulamak için kullanacağınız örnek bir PSD görüntüsü hazırlayın.

## Paketleri İçe Aktar

Süreci başlatmak için gerekli paketleri Java projenize aktarın. Bu, Aspose.PSD işlevlerinin sorunsuz bir şekilde kullanılmasına zemin hazırlıyor.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1. Adım: Görüntüyü Yükleyin

 Örnek PSD görüntüsünü bir örneğine yükleyerek başlayın.`RasterImage` sınıf. Bu daha sonraki gama ayarlamalarının temelini oluşturur.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Mevcut bir görüntüyü RasterImage sınıfının bir örneğine yükleme
Image image = Image.load(sourceFile);

// Image nesnesini RasterImage'a yayınla
RasterImage rasterImage = (RasterImage)image;

// Daha iyi performans için RasterImage'ın önbelleğe alınıp alınmadığını kontrol edin
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## 2. Adım: Gamayı Ayarlayın

 Şimdi yüklenen görüntünün gammasını kullanarak ayarlayın.`adjustGamma` Yöntem. Gereksinimlerinize göre gama değerlerine ince ayar yapın.

```java
// Gamayı ayarlayın
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 3. Adım: TiffOptions'ı oluşturun

 Bir örneğini oluşturun`TiffOptions` ortaya çıkan görüntü için. Çıktıyı spesifikasyonlarınıza göre uyarlamak için örnek başına bit sayısı ve fotometrik seçenekler gibi çeşitli özellikleri ayarlayın.

```java
// Ortaya çıkan görüntü için bir TiffOptions örneği oluşturun
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Adım 4: Ortaya Çıkan Görüntüyü Kaydedin

 Değiştirilen görüntüyü önceden tanımlanan yöntemi kullanarak TIFF formatında kaydedin.`TiffOptions`.

```java
// Ortaya çıkan görüntüyü TIFF formatında kaydedin
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Çözüm

Tebrikler! Aspose.PSD for Java'yı kullanarak bir görüntünün gammasını başarıyla ayarladınız. Bu süreç, geliştiricilerin görüntü kalitesini zahmetsizce geliştirmelerine olanak tanır ve görsel olarak çekici bir kullanıcı deneyimine katkıda bulunur.

## SSS'ler

### S1: Aspose.PSD belgelerini nerede bulabilirim?

 A1: Belgelere şu adresten erişebilirsiniz:[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### S2: Aspose.PSD for Java'yı nasıl indirebilirim?

 A2: Kütüphaneyi şuradan indirin:[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### S3: Aspose.PSD'yi nereden satın alabilirim?

 A3: Ziyaret edin[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) Aspose.PSD'yi satın almak için.

### S4: Ücretsiz deneme sürümü mevcut mu?

 C4: Evet, ücretsiz deneme sürümünü şuradan keşfedebilirsiniz:[https://releases.aspose.com/](https://releases.aspose.com/).

### S5: Aspose.PSD için nereden destek alabilirim?

 Cevap5: Destek için Aspose.PSD forumunu ziyaret edin:[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).