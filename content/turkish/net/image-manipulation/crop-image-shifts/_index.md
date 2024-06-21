---
title: Aspose.PSD for .NET'te Görüntüleri Kaydırarak Kırpma
linktitle: Görüntüleri Kaydırarak Kırpma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'i kullanarak görüntüleri zahmetsizce kırpmayı öğrenin. Hassas görüntü ayarları için adım adım kılavuzumuzu izleyin.
type: docs
weight: 12
url: /tr/net/image-manipulation/crop-image-shifts/
---
## giriiş

.NET geliştirme alanında Aspose.PSD, görüntü işleme görevleri için güçlü bir araç seti olarak öne çıkıyor. Dikkate değer özelliklerinden biri, 'Vardiyalarla Kırpma' işlevi sayesinde görüntüleri hassas bir şekilde kırpabilme yeteneğidir. Bu adım adım kılavuzda, Aspose.PSD for .NET kullanarak görüntüleri sorunsuz bir şekilde kırpma sürecinde size yol göstereceğiz.

## Önkoşullar

Eğiticiye başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.PSD for .NET Library: Kütüphanenin kurulu olduğundan emin olun. Değilse, adresinden indirebilirsiniz.[yayın sayfası](https://releases.aspose.com/psd/net/).

- .NET Ortamı: Makinenizde bir .NET geliştirme ortamının kurulu olduğundan emin olun.

- Örnek Resim: Çalışmak istediğiniz PSD formatında örnek bir resim hazırlayın.

## Ad Alanlarını İçe Aktar

Gerekli ad alanlarını .NET projenize aktararak başlayın. Bu ad alanları Aspose.PSD sınıflarına ve görüntü kırpma için gerekli yöntemlere erişim sağlar.

```csharp
using Aspose.PSD.ImageOptions;
```

## 1. Adım: Belge Dizininizi Tanımlayın

Kaynak ve hedef dosyaların bulunacağı belge dizininizin yolunu ayarlayın.

```csharp
string dataDir = "Your Document Directory";
```

## Adım 2: Kaynak Görüntüyü Yükleyin

Kırpmak istediğiniz PSD görüntüsünü yükleyin. "Sample.psd"yi kaynak dosyanızın adıyla değiştirdiğinizden emin olun.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## 3. Adım: Daha İyi Performans için Görüntü Verilerini Önbelleğe Alın

Kırpmadan önce, daha iyi performans için görüntü verilerinin önbelleğe alınması önerilir.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Adım 4: Kırpma için Kaydırma Değerlerini Tanımlayın

Görüntünün sol, sağ, üst ve alt tarafları için kaydırma değerlerini belirtin. Bu değerleri kırpma gereksinimlerinize göre ayarlayın.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## 5. Adım: Kırpmayı Uygulayın ve Sonuçları Kaydedin

 Kullanın`Crop` Belirtilen kaydırmaları uygulama ve kırpılan görüntüyü hedef dosyaya kaydetme yöntemini kullanın.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak görüntüleri vardiyalara göre nasıl kırpacağınızı başarıyla öğrendiniz. Bu güçlü işlevsellik, çeşitli görüntü işleme görevleri için gereken hassasiyeti ve kontrolü sağlar.

## SSS'ler

### S1: Yalnızca PSD'yi değil, farklı formatlardaki görüntüleri de kırpabilir miyim?

Cevap1: Evet, Aspose.PSD çeşitli görüntü formatlarını destekleyerek JPEG, PNG ve daha birçok formattaki görüntüleri kırpmanıza olanak tanır.

### S2: Aspose.PSD for .NET'i satın almadan önce deneme sürümü mevcut mu?

 A2: Kesinlikle! Ücretsiz deneme sürümüyle araç setini keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.PSD for .NET için geçici lisansı nasıl edinebilirim?

 Cevap3: Test amacıyla geçici bir lisans alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).

### S4: Aspose.PSD ile ilgili ek destek ve tartışmaları nerede bulabilirim?

 A4: Ziyaret edin[Aspose.PSD Forumu](https://forum.aspose.com/c/psd/34) Destek ve ilgi çekici tartışmalar için.

### S5: Aspose.PSD for .NET'i doğrudan web sitesinden satın alabilir miyim?

 Cevap5: Evet, kütüphaneyi güvenli bir şekilde satın alabilirsiniz.[satın alma sayfası](https://purchase.aspose.com/buy).
