---
title: Aspose.PSD for .NET'te Görüntülere Degrade Efektleri Ekleme
linktitle: Görüntülere Degrade Efektleri Ekleme
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'i kullanarak görüntülerinizi büyüleyici degrade efektleriyle geliştirin. Yaratıcı görsel dönüşümler için adım adım eğitimimizi takip edin.
type: docs
weight: 11
url: /tr/net/image-manipulation/adding-gradient-effects/
---
## giriiş

Görüntüleri degrade efektleriyle geliştirmek, görsel içeriğinize büyüleyici bir boyut katabilir. Aspose.PSD for .NET, görsellerinize degrade kaplamalar eklemek için güçlü bir platform sağlar. Bu eğitimde Aspose.PSD for .NET'i kullanarak degrade efektleri ekleme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.PSD for .NET Library: Kütüphaneyi şuradan indirip yükleyin:[Aspose.PSD for .NET Belgeleri](https://reference.aspose.com/psd/net/).
- .NET Ortamı: Makinenizde çalışan bir .NET ortamının kurulu olduğundan emin olun.

## Ad Alanlarını İçe Aktar

Gerekli ad alanlarını projenize aktararak başlayın:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## 1. Adım: Görüntüyü Yükleyin ve Yolları Tanımlayın

```csharp
// Belgeler dizininin yolu.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFileName = Path.Combine(SourceDir, "GradientOverlay.psd");
string exportPath = Path.Combine(OutputDir, "GradientOverlayChanged.psd");

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};
```

## Adım 2: Başlangıç Ayarlarını Onaylayın

Degrade katmanının başlangıç ayarlarının beklendiği gibi olduğundan emin olun:

```csharp
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    // Başlangıç ayarları için onaylama kontrolleri
    // ...

    // Renk Noktaları
    // ...

    //Şeffaflık noktaları
    // ...
}
```

## 3. Adım: Degrade Kaplama Ayarlarını Değiştirin

Degrade kaplama ayarlarını tercihlerinize göre ayarlayın:

```csharp
// Test düzenleme
settings.Color = Color.Green;

gradientOverlay.Opacity = 193;
gradientOverlay.BlendMode = BlendMode.Lighten;

settings.AlignWithLayer = false;
settings.GradientType = GradientType.Radial;
settings.Angle = 45;
settings.Dither = true;
settings.HorizontalOffset = 15;
settings.VerticalOffset = 11;
settings.Reverse = true;

// Yeni renk noktası ekle
// ...

// Önceki noktanın konumunu değiştir
// ...

// Yeni şeffaflık noktası ekle
// ...

// Önceki şeffaflık noktasının konumunu değiştir
// ...

im.Save(exportPath);
```

## 4. Adım: Düzenlenen Dosyayı Doğrulayın

Değişikliklerin başarıyla uygulanıp uygulanmadığını kontrol edin:

```csharp
// Düzenlemeden sonra dosyayı test edin
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];
    try
    {
        // Değiştirilen ayarlar için onaylama kontrolleri
        // ...
    }
    catch (Exception e)
    {
        string ex = e.StackTrace;
    }
}
```

## Çözüm

Aspose.PSD for .NET kullanarak görüntülere degrade efektleri eklemek, yaratıcı olasılıklarla dolu bir dünyanın kapılarını açar. Resimlerinizde istediğiniz görsel etkiyi elde etmek için çeşitli ayarlarla denemeler yapın.

## SSS'ler

### S1: Degrade efektlerini birden fazla katmana aynı anda uygulayabilir miyim?

Cevap1: Evet, her katmanı yineleyerek ve istediğiniz ayarları uygulayarak birden çok katmana degrade efektleri uygulayabilirsiniz.

### S2: Aspose.PSD for .NET hangi dosya formatlarını destekliyor?

Cevap2: Aspose.PSD for .NET, PSD, PNG, JPEG, BMP ve GIF dahil olmak üzere çeşitli görüntü dosyası formatlarını destekler.

### S3: Aspose.PSD for .NET'in deneme sürümü mevcut mu?

 C3: Evet, Aspose.PSD for .NET'in yeteneklerini aşağıdaki ücretsiz deneme sürümünü indirerek keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD for .NET desteğini nasıl alabilirim?

 A4: Herhangi bir yardım veya soru için şu adresi ziyaret edin:[Aspose.PSD for .NET Destek Forumu](https://forum.aspose.com/c/psd/34).

### S5: Aspose.PSD for .NET'i nereden satın alabilirim?

 Cevap5: Kütüphaneyi şu adresten satın alabilirsiniz:[Aspose.PSD for .NET Satın Alma Sayfası](https://purchase.aspose.com/buy).