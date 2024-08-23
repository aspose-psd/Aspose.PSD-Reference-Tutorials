---
title: Aspose.PSD for .NET'te Katmanlara Kontur Efektleri Ekleme
linktitle: Katmanlara Kontur Efektleri Ekleme
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET ile görüntü estetiğini geliştirin. Adım adım vuruş efektleri eklemeyi öğrenin. Ücretsiz deneme sürümünü şimdi indirin, satın alın veya deneyin.
type: docs
weight: 10
url: /tr/net/layer-effects/adding-stroke-effects/
---
## giriiş

Aspose.PSD for .NET'te katmanlara kontur efektleri eklemeye yönelik bu adım adım eğitime hoş geldiniz. Kontur efektiyle görsellerinizin görsel çekiciliğini artırmak çok kolaydır ve Aspose.PSD, bunu .NET geliştiricileri için kusursuz hale getirir. Bu kılavuzda, bu güçlü özellikte uzmanlaşmanıza yardımcı olacak net adımlar ve örnekler sunarak süreç boyunca size yol göstereceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

- Aspose.PSD for .NET: Aspose.PSD kütüphanesini şu adresten indirip yükleyin:[web sitesi](https://releases.aspose.com/psd/net/).

- Belge Dizini: Kontur efektleri uygulamak istediğiniz PSD belgesini içeren bir dizin hazırlayın.

- Çıkış Dizini: Çıkış görüntülerini kontur efektleriyle depolamak için ayrı bir dizine sahip olun.

- Visual Studio: Visual Studio'ya veya tercih edilen herhangi bir .NET geliştirme ortamına sahip olduğunuzdan emin olun.

## Ad Alanlarını İçe Aktar

.NET projenize Aspose.PSD işlevselliğinden yararlanmak için gerekli ad alanlarını ekleyin:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## 1. Adım: PSD Belgesini Yükleyin

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // PSD belgesini yükleme kodunuz buraya gelecek
}
```

## Adım 2: Renk Kontur Efekti Ekleyin

```csharp
// İçerideki konumuna Renk dolgusu ekler
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Adım 3: Dış Konum

```csharp
// Dış konumuna Renk dolgusu ekler
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Adım 4: Merkez Konumu

```csharp
// Merkez konumuna Renk dolgusu ekler
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Ayarları uygun şekilde ayarlayarak Degrade ve Desen dolguları için benzer adımları tekrarlayın.

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak katmanlara kontur efektleri eklemeyi başarıyla öğrendiniz. Resimlerinizde istediğiniz görsel etkiyi elde etmek için farklı ayarlarla denemeler yapın.

## SSS'ler

### S1: Kontur efektlerini yalnızca belirli katmanlara uygulayabilir miyim?

Cevap1: Evet, koddaki katman indeksini ayarlayarak belirli katmanları hedefleyebilirsiniz.

### S2: Aspose.PSD en son .NET çerçevesiyle uyumlu mu?

A2: Kesinlikle! Aspose.PSD, en yeni .NET çerçeveleriyle sorunsuz bir şekilde entegre olacak şekilde tasarlanmıştır.

### S3: Kontur rengini nasıl özelleştirebilirim?

 A3: Basitçe değiştirin`Color` İstenilen kontur rengini elde etmek için koddaki özellik.

### S4: Aspose.PSD birden fazla PSD dosyası için toplu işlemeyi destekliyor mu?

Cevap4: Evet, birden fazla PSD dosyası arasında geçiş yapabilir ve benzer bir yaklaşım kullanarak kontur efektini uygulayabilirsiniz.

### S5: Aspose.PSD'yi satın almadan önce deneme sürümünü kullanabilir miyim?

 A5: Kesinlikle! Yakala[ücretsiz deneme](https://releases.aspose.com/) satın almadan önce Aspose.PSD'nin yeteneklerini keşfetmek için.