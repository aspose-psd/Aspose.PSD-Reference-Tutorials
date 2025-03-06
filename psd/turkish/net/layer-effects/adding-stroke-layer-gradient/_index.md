---
title: Aspose.PSD for .NET'te Gradyanlı Kontur Katmanı Ekleme
linktitle: Degrade ile Kontur Katmanı Ekleme
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'te degrade kontur katmanını nasıl ekleyeceğinizi öğrenin. Bu kapsamlı eğitimle görüntü işleme becerilerinizi geliştirin.
weight: 12
url: /tr/net/layer-effects/adding-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET'te Gradyanlı Kontur Katmanı Ekleme

## giriiş

.NET uygulamalarınızı büyüleyici grafik efektleriyle geliştirmek istiyorsanız Aspose.PSD for .NET, başvuracağınız çözümdür. Bu eğitimde Aspose.PSD for .NET'i kullanarak degradeli kontur katmanı ekleme sürecini ayrıntılı olarak ele alacağız. Bu adım adım kılavuz, görsellerinizin görsel çekiciliğini zahmetsizce artırmanıza yardımcı olacaktır.

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- C# ve .NET geliştirme konusunda çalışma bilgisi.
-  Aspose.PSD for .NET kütüphanesi kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/psd/net/).
- Sağlanan örnekleri uygulamak için Visual Studio gibi bir kod düzenleyici.

## Ad Alanlarını İçe Aktar

İşleri başlatmak için gerekli ad alanlarını projemize aktaralım. Bu ad alanları Aspose.PSD for .NET'in işlevselliklerinden yararlanmak için çok önemlidir.

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## 1. Adım: Belge Dizinini Ayarlayın

Koddaki belgeler dizininizin yolunu tanımlayarak başlayın. Bu, gerekli dosyaların doğru konumdan yüklenmesini ve kaydedilmesini sağlar.

```csharp
string dataDir = "Your Document Directory";
```

## Adım 2: PSD Dosyasını Yükleyin

Kaynak PSD dosyasını Aspose.PSD for .NET'i kullanarak yükleyin. Katmanları etkili bir şekilde yönetmek için efekt kaynağının yüklendiğinden emin olun.

```csharp
string sourceFileName = dataDir + "Stroke.psd";
string exportPath = dataDir + "StrokeGradientChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // PSD dosyasını işlemeye yönelik kod buraya gelir
}
```

## 3. Adım: Degrade Kontur Ayarlarını Doğrulayın

Karışım modu, opaklık ve görünürlük gibi çeşitli ayarları kontrol ederek degradeli kontur katmanının doğru şekilde yapılandırıldığından emin olun.

```csharp
var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

// Degrade kontur ayarları için iddia kontrolleri
AssertIsTrue(gradientStroke.BlendMode == BlendMode.Normal);
AssertIsTrue(gradientStroke.Opacity == 255);
AssertIsTrue(gradientStroke.IsVisible);

// Doldurma ayarları için daha fazla onay kontrolü
// ...
```

Renk noktaları ve şeffaflık noktaları dahil diğer dolgu ayarları için onay kontrolleri uygulamaya devam edin.

## 4. Adım: Degrade Kontur Ayarlarını Düzenleyin

Şimdi degrade kontur ayarlarında bazı değişiklikler yapalım. İstenilen görsel efekti elde etmek için renk, opaklık, karışım modu ve degrade türü gibi parametreleri değiştirin.

```csharp
// Degrade kontur ayarlarını değiştirme kodu
// ...
```

## Adım 5: Düzenlenen PSD Dosyasını Kaydedin

Düzenlenen PSD dosyasını belirtilen dışa aktarma yoluna kaydedin.

```csharp
im.Save(exportPath);
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak degradeli bir kontur katmanını başarıyla eklediniz. Bu eğitim sizi görsellerinizi programlı olarak geliştirmeniz için gereken bilgilerle donattı.

## SSS'ler

### S1: Aspose.PSD for .NET'i diğer .NET çerçeveleriyle kullanabilir miyim?

Cevap1: Evet, Aspose.PSD for .NET çeşitli .NET çerçeveleriyle uyumludur.

### S2: Aspose.PSD for .NET'in ücretsiz deneme sürümü mevcut mu?

 C2: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.PSD for .NET desteğini nasıl alabilirim?

 A3: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği için.

### S4: Aspose.PSD for .NET'in kapsamlı belgelerini nerede bulabilirim?

 A4: Bkz.[dokümantasyon](https://reference.aspose.com/psd/net/) detaylı bilgi için.

### S5: Aspose.PSD for .NET lisansını nasıl satın alabilirim?

 A5: Bir lisans satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
