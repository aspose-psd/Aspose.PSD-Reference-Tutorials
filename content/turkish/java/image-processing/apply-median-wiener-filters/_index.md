---
title: Aspose.PSD for Java ile Medyan ve Wiener Filtrelerini Uygulayın
linktitle: Medyan ve Wiener Filtrelerini Uygula
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java'da görüntü işlemenin gücünü keşfedin. Medyan ve Wiener Filtrelerini adım adım nasıl uygulayacağınızı öğrenin. Görüntü kalitesini zahmetsizce artırın.
type: docs
weight: 12
url: /tr/java/image-processing/apply-median-wiener-filters/
---
## giriiş

Java programlama alanında Aspose.PSD, görüntü işleme ve işleme için güçlü bir araç olarak öne çıkıyor. Sunduğu temel işlevlerden biri, görüntü kalitesinin artırılmasında ve gürültünün azaltılmasında çok önemli bir rol oynayan Medyan ve Wiener Filtrelerinin uygulanmasıdır. Bu adım adım kılavuz, Aspose.PSD for Java kullanarak bu filtreleri uygulama sürecinde size yol gösterecektir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1.  Aspose.PSD for Java Library: Kütüphaneyi şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/psd/java/).
2. Java Geliştirme Ortamı: Sisteminizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

## Paketleri İçe Aktar

Java projenizde Aspose.PSD işlevselliğinden yararlanmak için gerekli paketleri içe aktararak başlayın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Medyan Filtresi Uygulama

### 1. Adım: Görüntüyü Yükleyin

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//Kaynak görüntüyü yükleyin
Image image = Image.load(sourceFile);
```

### Adım 2: Görüntüyü RasterImage'a Yayınlayın

```java
// Görüntüyü RasterImage'a yayınlayın
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### 3. Adım: MedianFilterOptions Örneği Oluşturun

```java
// MedianFilterOptions sınıfının bir örneğini oluşturun ve filtre boyutunu ayarlayın
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Adım 4: Medyan Filtresini Uygulayın

```java
// MedianFilterOptions filtresini RasterImage nesnesine uygulama
rasterImage.filter(image.getBounds(), options);
```

### Adım 5: Ortaya Çıkan Görüntüyü Kaydedin

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Ortaya çıkan görüntüyü GIF olarak kaydedin
image.save(destName, new GifOptions());
```

Bu adımları izleyerek Aspose.PSD for Java kullanarak Medyan Filtresini görüntünüze başarıyla uyguladınız.

## Çözüm

Bu eğitimde Aspose.PSD for Java kullanarak Medyan ve Wiener Filtrelerini uygulama sürecini inceledik. Bu filtreler Java uygulamalarınızdaki görüntü kalitesini artırmak ve gürültüyü azaltmak için vazgeçilmezdir. Aspose.PSD'nin gücünden yararlanarak bu filtreleri görüntü işleme iş akışlarınıza zahmetsizce dahil edebilirsiniz.

## SSS'ler

### S1: Bu filtreleri herhangi bir formattaki görsellere uygulayabilir miyim?

Cevap1: Evet, Aspose.PSD çok çeşitli görüntü formatlarını destekler, bu da onu çeşitli projeler için çok yönlü kılar.

### S2: Aspose.PSD for Java'nın ücretsiz deneme sürümü mevcut mu?

 A2: Evet, ücretsiz deneme sürümünden yararlanabilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.PSD for Java desteğini nasıl alabilirim?

 A3: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği için.

### S4: Aspose.PSD for Java belgelerini nerede bulabilirim?

 Cevap4: Belgelere bakın[Burada](https://reference.aspose.com/psd/java/).

### S5: Java için Aspose.PSD'yi nasıl satın alabilirim?

 A5: Ürünü satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).