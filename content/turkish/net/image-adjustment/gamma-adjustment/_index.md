---
title: Aspose.PSD for .NET'te Gama Ayarlamasının Uygulanması
linktitle: Gama Ayarlamasının Uygulanması
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'in gücünü Gama Ayarlamanın uygulanmasına ilişkin adım adım kılavuzumuzla keşfedin. Görüntü parlaklığına ve kontrastına zahmetsizce ince ayar yapın.
type: docs
weight: 12
url: /tr/net/image-adjustment/gamma-adjustment/
---
## giriiş

Aspose.PSD for .NET'te Gama Ayarlamasının uygulanmasına ilişkin bu kapsamlı kılavuza hoş geldiniz! Gama ayarı, bir görüntünün parlaklığına ve kontrastına ince ayar yapmanızı sağlayan çok önemli bir görüntü işleme tekniğidir. Bu eğitimde, .NET için güçlü Aspose.PSD kütüphanesini kullanarak süreç boyunca size yol göstereceğiz.

## Önkoşullar

Uygulamaya geçmeden önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD for .NET Library: Aspose.PSD for .NET kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/psd/net/).

- .NET Framework: Bu eğitimde, .NET geliştirme konusunda temel bilgiye sahip olduğunuz ve .NET Framework'ün yüklü olduğu varsayılmaktadır.

- Tümleşik Geliştirme Ortamı (IDE): .NET geliştirme için Visual Studio gibi tercih ettiğiniz IDE'yi seçin.

## Ad Alanlarını İçe Aktar

.NET projenize Aspose.PSD ile çalışmak için gerekli ad alanlarını içe aktararak başlayın:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 1. Adım: Projenizi Kurun

Seçtiğiniz IDE'de yeni bir .NET projesi oluşturun. Aspose.PSD kütüphanesine referanslar eklediğinizden emin olun.

## Adım 2: Belge Dizinini Tanımlayın

```csharp
string dataDir = "Your Document Directory";
```

## 3. Adım: Görüntüyü Yükleyin

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Bu kullanma bloğunun içinde ek adımlar gerçekleştirilecektir.
}
```

## Adım 4: RasterImage ve Önbellek Verilerine Yayınlama

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Adım 5: Gamayı Ayarlayın

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Adım 6: TiffOptions Oluşturun ve Kaydedin

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak Gama Ayarını başarıyla uyguladınız. Bu güçlü kitaplık, görüntü işleme için güçlü yetenekler sunarak onu .NET geliştiricileri için değerli bir araç haline getirir.

## SSS'ler

### S1: Aspose.PSD belgelerini nerede bulabilirim?

 A1: Belgelere başvurabilirsiniz[Burada](https://reference.aspose.com/psd/net/).

### S2: Aspose.PSD for .NET'i nasıl indirebilirim?

 A2: Kütüphaneyi indirebilirsiniz[Burada](https://releases.aspose.com/psd/net/).

### S3: Ücretsiz deneme sürümü mevcut mu?

 A3: Evet, ücretsiz deneme sürümünden yararlanabilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD için nereden destek alabilirim?

 Cevap4: Destek forumunu ziyaret edebilirsiniz[Burada](https://forum.aspose.com/c/psd/34).

### S5: Geçici bir lisansa ihtiyacım var mı?

 Cevap5: Gerekirse geçici lisans alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).