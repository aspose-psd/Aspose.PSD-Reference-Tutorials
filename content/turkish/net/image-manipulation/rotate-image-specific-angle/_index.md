---
title: Aspose.PSD for .NET'te Bir Görüntüyü Belirli Bir Açıda Döndürme
linktitle: Bir Görüntüyü Belirli Bir Açıda Döndürme
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'in gücünü keşfedin. Görüntüleri belirli açılarda zahmetsizce döndürün. Kitaplığı indirin ve görüntüleri sorunsuz bir şekilde değiştirmeye başlayın.
type: docs
weight: 16
url: /tr/net/image-manipulation/rotate-image-specific-angle/
---
.NET ile görüntü işleme dünyasına giriyorsanız Aspose.PSD güçlü bir çözüm sunar. Bu eğitimde, Aspose.PSD'yi kullanarak bir görüntüyü belirli bir açıda döndürme sürecinde size rehberlik edeceğiz. Adımlara dalmadan önce bir girişle sahneyi hazırlayalım.

## giriiş

Aspose.PSD for .NET, geliştiricilerin PSD ve taramalı görüntü formatlarıyla sorunsuz bir şekilde çalışmasına olanak tanıyan çok yönlü bir kitaplıktır. Temel özelliklerinden biri, görüntüleri hassas açılarda döndürerek görüntü manipülasyonunda esneklik sağlamasıdır. Bu eğitim, Aspose.PSD for .NET kullanarak bir görüntüyü belirli bir açıda döndürme adımlarında size yol gösterecektir.

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.PSD for .NET Library: Kitaplığı şuradan indirip yükleyin:[indirme sayfası](https://releases.aspose.com/psd/net/).
- Belge Dizini: Kaynak ve çıktı dosyalarınızı depolamak için bir dizin ayarlayın.

## Ad Alanlarını İçe Aktar

Başlamak için .NET projenize gerekli ad alanlarını içe aktarın:

```csharp
using Aspose.PSD.ImageOptions;
```

Şimdi örneği adım adım kılavuz formatında birden fazla adıma ayıralım.

## 1. Adım: Belge Dizininizi Ayarlayın

```csharp
string dataDir = "Your Document Directory";
```

 Yer değiştirmek`"Your Document Directory"` kaynak ve çıktı dosyalarınızı sakladığınız dizinin yolu ile birlikte.

## 2. Adım: Görüntüyü Yükleyin

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Buraya ek adımlar eklenecek
}
```

 Döndürmek istediğiniz görüntüyü bir örneğine yükleyin`RasterImage`.

## 3. Adım: Görüntü Verilerini Önbelleğe Alın

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Döndürme sırasında daha iyi performans için görüntü verilerini önbelleğe alın.

## 4. Adım: Görüntüyü Döndürün

```csharp
image.Rotate(20f, true, Color.Red);
```

Orantılı boyutu koruyarak ve kırmızı bir arka plan kullanarak görüntüyü 20 derece döndürün.

## Adım 5: Sonucu Kaydet

```csharp
image.Save(destName, new JpegOptions());
```

Döndürülmüş görüntüyü belirtilen seçeneklerle kaydedin (bu durumda JPEG olarak).

## Çözüm

 Tebrikler! Aspose.PSD for .NET'i kullanarak bir görüntüyü belirli bir açıda başarıyla döndürdünüz. Bu kütüphane, görüntü işleme için güçlü bir araç seti sağlar ve bu eğitim buzdağının sadece görünen kısmıdır. Keşfedin[dokümantasyon](https://reference.aspose.com/psd/net/) Daha fazla özellik ve seçenek için.

## SSS'ler

### S1: Görüntüleri 20 dereceden farklı açılarla döndürebilir miyim?

 A1: Evet, açı parametresini özelleştirebilirsiniz.`image.Rotate` yöntemi istenilen herhangi bir değere ayarlayın.

### S2: Aspose.PSD, JPEG'in yanı sıra diğer görüntü formatlarını da destekliyor mu?

A2: Kesinlikle! Aspose.PSD PNG, GIF, BMP ve TIFF dahil çok çeşitli formatları destekler.

### S3: Döndürmeden önce görüntü verilerinin önbelleğe alınması gerekli midir?

Cevap3: Zorunlu olmasa da, verileri önbelleğe almak, özellikle büyük resimlerde performansı önemli ölçüde artırabilir.

### S4: Aspose.PSD ile ilgili sorgular için nereden destek alabilirim?

 A4: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.

### S5: Satın almadan önce Aspose.PSD'yi deneyebilir miyim?

 A5: Kesinlikle! Tutun[ücretsiz deneme](https://releases.aspose.com/) Kütüphanenin yeteneklerini keşfetmek için.