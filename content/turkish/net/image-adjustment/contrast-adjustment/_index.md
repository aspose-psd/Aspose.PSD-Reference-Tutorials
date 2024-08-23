---
title: Aspose.PSD for .NET'te Kontrast Ayarlamasının Uygulanması
linktitle: Kontrast Ayarlamanın Uygulanması
second_title: Aspose.PSD .NET API'si
description: Bu adım adım kılavuzla Aspose.PSD for .NET'te kontrast ayarının nasıl uygulanacağını öğrenin.
type: docs
weight: 11
url: /tr/net/image-adjustment/contrast-adjustment/
---
## giriiş

Aspose.PSD for .NET'te kontrast ayarının uygulanmasına ilişkin bu kapsamlı kılavuza hoş geldiniz! Bu eğitimde, güçlü bir .NET görüntüleme kütüphanesi olan Aspose.PSD'yi kullanarak bir görüntünün kontrastını geliştirme sürecini inceleyeceğiz. Bu kılavuzun sonunda kontrast ayarlamalarını resimlerinize sorunsuz bir şekilde nasıl uygulayacağınıza dair sağlam bir anlayışa sahip olacaksınız.

## Önkoşullar

Adım adım sürece dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1.  Aspose.PSD for .NET Kütüphanesi: Aspose.PSD for .NET kütüphanesini indirip yükleyin. İndirme linkini bulabilirsiniz[Burada](https://releases.aspose.com/psd/net/).

2. Belge Dizini: Kaynak ve hedef dosyalarınızın depolanacağı bir dizin ayarlayın. Sağlanan koddaki "Belge Dizininiz"i bu dizinin yoluyla değiştirin.

Artık önkoşullarımızı sıraladığımıza göre uygulamaya geçebiliriz.

## Ad Alanlarını İçe Aktar

Bu adımda Aspose.PSD kütüphanesinin sağladığı işlevlere erişmek için gerekli ad alanlarını içe aktaracağız.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 1. Adım: Görüntüyü Yükleyin

Kaynak görüntüyü bir örneğine yükleyin`RasterImage` sınıf.

```csharp
//ExStart:Resim Yükle
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Bir sonraki adıma geçin...
}
//ExEnd:Resim Yükle
```

## 2. Adım: Kontrastı Ayarlayın

Bu adımda yüklenen görüntünün kontrastını ayarlayacağız.

```csharp
//ExStart:Kontrast'ı Ayarlayın
rasterImage.AdjustContrast(50); // Kontrastı %50 oranında ayarlayın
// Bir sonraki adıma geçin...
//ExEnd:Kontrast'ı Ayarlayın
```

## 3. Adım: TIFF Seçenekleri Oluşturun

 Bir örneğini oluşturun`TiffOptions` ortaya çıkan görüntü için çeşitli özellikleri ayarlayın ve görüntüyü TIFF formatında kaydedin.

```csharp
//ExStart:CreateTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

Tebrikler! Aspose.PSD for .NET'i kullanarak kontrast ayarını başarıyla uyguladınız.

## Çözüm

Bu eğitimde Aspose.PSD for .NET ile görüntü kontrastını geliştirme sürecini inceledik. Kitaplık, görüntü özelliklerini değiştirmek için basit bir yol sağlayarak geliştiricilerin zahmetsizce görsel olarak çekici görüntüler oluşturmasına olanak tanır.

## SSS'ler

### S1: Aspose.PSD for .NET yeni başlayanlar için uygun mu?

Cevap1: Aspose.PSD for .NET, geliştirici dostu olacak şekilde tasarlanmıştır; bu da onu hem yeni başlayanlar hem de deneyimli geliştiriciler için uygun hale getirir.

### S2: Aspose.PSD'yi ticari projeler için kullanabilir miyim?

 C2: Evet, Aspose.PSD for .NET ticari projelerde kullanılabilir. Lisans ayrıntıları için şu adresi ziyaret edin:[Burada](https://purchase.aspose.com/buy).

### S3: Ücretsiz deneme sürümü mevcut mu?

 Cevap3: Evet, Aspose.PSD for .NET'in ücretsiz deneme sürümünü keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD for .NET desteğini nerede bulabilirim?

 Cevap4: Aspose.PSD for .NET destek forumunu ziyaret edin[Burada](https://forum.aspose.com/c/psd/34) yardım için.

### S5: Geçici lisansı nasıl alabilirim?

 Cevap 5: Gerekirse geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).