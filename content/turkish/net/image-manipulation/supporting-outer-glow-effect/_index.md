---
title: Aspose.PSD for .NET'te Dış Işıma Efektini Destekleme
linktitle: Dış Işıma Efektini Destekleme
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'te Outer Glow Effect'in gücünü keşfedin. Bu adım adım eğitimle görsel tasarımlarınızı geliştirin.
type: docs
weight: 16
url: /tr/net/image-manipulation/supporting-outer-glow-effect/
---
## giriiş

Aspose.PSD for .NET'te Dış Işıma Efektini desteklemeye yönelik adım adım kılavuzumuza hoş geldiniz. Aspose.PSD, .NET uygulamalarında PSD dosyalarının kusursuz şekilde işlenmesini sağlayan güçlü bir kütüphanedir. Bu eğitimde, Dış Işıma Efektinin uygulanmasını inceleyeceğiz ve bunu projelerinize entegre etmek için ayrıntılı bir yol göstereceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD for .NET Kütüphanesi: Kütüphaneyi şuradan indirin:[Aspose.PSD .NET Belgeleri](https://reference.aspose.com/psd/net/).

- Geliştirme Ortamı: Tercih ettiğiniz .NET geliştirme ortamını kurun.

- Belge ve Çıktı Dizinleri: Belgenizi ve çıktı dizinlerinizi sağlanan kodda tanımlayın.

## Ad Alanlarını İçe Aktar

Bu bölümde Outer Glow Effect uygulamamızı başlatmak için gerekli ad alanlarını içe aktaracağız. Bu adımları takip et:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

Şimdi, Dış Işıma Etkisini elde etmek için verilen örneği birden fazla adıma ayıralım.

## 1. Adım: Belgeyi ve Çıktı Yollarını Ayarlayın

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## Adım 2: PSD Görüntüsünü Yükleyin

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    // Uygulama adımları aşağıya eklenecektir.
}
```

## Adım 3: Dış Işıma Efekti Ekleyin

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## Adım 4: Dış Işıma Parametrelerini Yapılandırma

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## Adım 5: Görüntüyü Kaydedin

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## Adım 6: Temizleme

```csharp
File.Delete(outputPng);
```

## Adım 7: Başarı Mesajını Görüntüleyin

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak Dış Işıma Efektini başarıyla uyguladınız. Bu güçlü özellik, görsellerinizin görsel çekiciliğini artırarak tasarımlarınıza benzersiz bir dokunuş sağlar.

## SSS'ler

### S1: Aspose.PSD tüm .NET çerçeveleriyle uyumlu mudur?

Cevap1: Evet, Aspose.PSD çok çeşitli .NET çerçevelerini destekleyerek çeşitli geliştirme ortamlarıyla uyumluluk sağlar.

### S2: Aspose.PSD için ek belgeleri nerede bulabilirim?

 A2: Bkz.[Aspose.PSD .NET Belgeleri](https://reference.aspose.com/psd/net/) Kapsamlı bilgi ve örnekler için.

### S3: Aspose.PSD için nasıl geçici lisans alabilirim?

 A3: Ziyaret edin[Aspose.PSD Geçici Lisansı](https://purchase.aspose.com/temporary-license/) Geçici lisanslama seçenekleri için.

### S4: Aspose.PSD kullanıcıları için hangi destek mevcut?

 A4: Katılın[Aspose.PSD Forumu](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.

### S5: .NET için Aspose.PSD'yi satın alabilir miyim?

 Cevap5: Evet, lisanslama seçeneklerini araştırın ve satın alma işleminizi yapın[Burada](https://purchase.aspose.com/buy).