---
title: Aspose.PSD for .NET'te Görüntüleri Dikdörtgenle Kırpma
linktitle: Görüntüleri Dikdörtgene Göre Kırpma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD ile .NET görüntü işleme becerilerinizi geliştirin. Hassasiyet için dikdörtgenleri kullanarak adım adım görüntü kırpmayı öğrenin.
type: docs
weight: 11
url: /tr/net/image-manipulation/crop-image-rectangle/
---
## giriiş

.NET programlama alanında görüntüleri değiştirmek ve geliştirmek yaygın bir görevdir ve Aspose.PSD for .NET bu süreci kolaylaştıran güçlü bir kütüphanedir. Bu eğitim, temel ama çok önemli bir görüntü işleme tekniğine odaklanıyor: görüntüleri bir dikdörtgenle kırpma. Bu kılavuzun sonunda Aspose.PSD for .NET kullanarak görüntülerin nasıl hassas bir şekilde kırpılacağına dair sağlam bir anlayışa sahip olacaksınız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.PSD for .NET: Kütüphanenin kurulu olduğundan emin olun. Değilse indirebilirsiniz[Burada](https://releases.aspose.com/psd/net/).

- Belge Dizininiz: Görüntü dosyalarınızın depolandığı bir dizin ayarlayın.

- Entegre Geliştirme Ortamı (IDE): Kusursuz kodlama için Visual Studio gibi .NET uyumlu bir IDE kullanın.

## Ad Alanlarını İçe Aktar

Başlamak için projenize gerekli ad alanlarını ekleyin:

```csharp
using Aspose.PSD.ImageOptions;
```

## 1. Adım: Belge Dizinini Ayarlayın

Belge dizininizin yolunu belirterek başlayın:

```csharp
string dataDir = "Your Document Directory";
```

## 2. Adım: Görüntüyü Yükleyin ve Önbelleğe Alın

Görüntüyü kaynak dosyadan yükleyin ve verilerini önbelleğe alın:

```csharp
//ExStart:Dikdörtgene Göre Kırpma
string sourceFile = dataDir + @"sample.psd";

// Mevcut bir görüntüyü RasterImage sınıfının bir örneğine yükleme
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    //Sonraki adımlara ilişkin kodunuz buraya gelecek
}
//ExEnd:Dikdörtgenle Kırpma
```

## Adım 3: Kırpma Dikdörtgenini Tanımlayın

 Bir örneğini oluşturun`Rectangle` kırpma için istenen boyuta sahip sınıf:

```csharp
// İstenilen boyutta Rectangle sınıfının bir örneğini oluşturun
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

## Adım 4: Kırpma İşlemini Gerçekleştirin

 Kırpma işlemini şu şekilde gerçekleştirin:`RasterImage` tanımlanmış dikdörtgeni kullanan nesne:

```csharp
rasterImage.Crop(rectangle);
```

## Adım 5: Sonuçları Kaydedin

Kırpılan görüntüyü belirtilen formatta (bu durumda JPEG) diske kaydedin:

```csharp
string destName = dataDir + @"CroppingByRectangle_out.jpg";
rasterImage.Save(destName, new JpegOptions());
```

Farklı kırpma senaryoları için dikdörtgen parametrelerini ayarlayarak bu adımları gerektiği kadar tekrarlayın.

## Çözüm

Sonuç olarak, Aspose.PSD for .NET'i kullanarak görüntüleri dikdörtgen şeklinde kırpma sanatında ustalaşmak, görüntü manipülasyonu için birçok olasılık dünyasının kapılarını açıyor. Bu eğitim, bu özelliği .NET uygulamalarınıza sorunsuz bir şekilde entegre etmek için gerekli adımları size sağladı.

## SSS'ler

### S1: Aspose.PSD for .NET tüm görüntü formatlarıyla uyumlu mu?

Cevap1: Evet, Aspose.PSD for .NET, JPEG, PNG, SVG, TIFF, BMP, GIF, PSD ve Jpeg2000 dahil çok çeşitli formatları destekler.

### S2: Aynı görüntüye birden fazla kırpma işlemi uygulayabilir miyim?

A2: Kesinlikle! İstenilen sonucu elde etmek için birden fazla kırpma işlemini sırayla gerçekleştirebilirsiniz.

### S3: Aspose.PSD for .NET ile işlenen görüntüler için herhangi bir boyut sınırlaması var mı?

Cevap3: Aspose.PSD for .NET, çeşitli boyutlardaki görüntüleri işlemek için tasarlanmıştır. Ancak olağanüstü büyük görüntülerle çalışırken sistem kaynaklarını ve belleği göz önünde bulundurun.

### S4: Aspose.PSD for .NET'in deneme sürümü mevcut mu?

 Cevap4: Evet, ücretsiz deneme sürümünü edinerek kütüphanenin özelliklerini keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S5: Nerede ek destek veya yardım bulabilirim?

 A5: ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) toplulukla bağlantı kurmak ve destek aramak.