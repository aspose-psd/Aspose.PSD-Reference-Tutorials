---
title: Aspose.PSD for .NET'te Alt Gölge Efekti Oluşturma
linktitle: Alt Gölge Efekti Oluşturma
second_title: Aspose.PSD .NET API'si
description: Bu eğitimde Aspose.PSD for .NET'in gücünü keşfedin ve büyüleyici alt gölge efektleri oluşturma sanatında ustalaşın.
type: docs
weight: 12
url: /tr/net/image-effects/render-drop-shadow/
---
## giriiş

Aspose.PSD for .NET'te alt gölge efektlerinin oluşturulmasıyla ilgili adım adım eğitimimize hoş geldiniz! Aspose.PSD'yi kullanarak görüntü işleme becerilerinizi geliştirmek istiyorsanız doğru yere geldiniz. Bu kılavuzda, resimlerinize alt gölge efektlerini kolaylıkla uygulama sürecinde size yol göstereceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD for .NET Library: Aspose.PSD kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/psd/net/).

- Belge Dizini: Belgelerinizin ve görsellerinizin saklandığı bir dizin oluşturun. Bu dizini kodda belirtmeniz gerekecek.

## Ad Alanlarını İçe Aktar

.NET projenizde gerekli ad alanlarını içe aktararak başlayın:

```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
using System;
```

Şimdi, daha net bir anlayış için kod örneğini birden çok adıma ayıralım:

## 1. Adım: Belge Dizininizi Ayarlayın

```csharp
string dataDir = "Your Document Directory";
```

"Belge Dizininiz"i, resimlerinizin depolandığı gerçek yolla değiştirdiğinizden emin olun.

## Adım 2: PSD Dosyasını Efekt Kaynağıyla Yükleme

```csharp
string sourceFileName = dataDir + "Shadow.psd";
string pngExportPath = dataDir + "Shadowchanged1.png";
var loadOptions = new PsdLoadOptions()
{
	LoadEffectsResource = true
};
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

Efekt kaynaklarının yüklenmesini etkinleştirerek PSD dosyanızı yükleyin.

## 3. Adım: Alt Gölge Efekti Özelliklerini Alın ve Doğrulayın

```csharp
var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);
if ((shadowEffect.Color != Color.Black) ||
	(shadowEffect.Opacity != 255) ||
	(shadowEffect.Distance != 3) ||
	(shadowEffect.Size != 7) ||
	(shadowEffect.UseGlobalLight != true) ||
	(shadowEffect.Angle != 90) ||
	(shadowEffect.Spread != 0) ||
	(shadowEffect.Noise != 0))
{
	throw new Exception("Shadow Effect properties were read wrong");
}
```

Alt gölge efekti özelliklerini alın ve bunları beklentilerinize göre doğrulayın.

## Adım 4: Görüntüyü Uygulanan Gölge Efektiyle Kaydetme

```csharp
var saveOptions = new PngOptions();
saveOptions.ColorType = PngColorType.TruecolorWithAlpha;
im.Save(pngExportPath, saveOptions);
```

Değiştirilen görüntüyü, uygulanan alt gölge efektiyle PNG formatında kaydedin.

Ve bu kadar! Aspose.PSD for .NET'i kullanarak başarılı bir şekilde gölge efekti oluşturdunuz.

## Çözüm

Bu eğitimde Aspose.PSD for .NET'te alt gölge efektleri oluşturma sürecini inceledik. Bu basit adımları izleyerek resimlerinize derinlik ve boyut katabilir, görsel açıdan büyüleyici sonuçları zahmetsizce yaratabilirsiniz.

## SSS'ler

### S1: Aspose.PSD for .NET tüm görüntü formatlarıyla uyumlu mu?

Cevap1: Aspose.PSD öncelikle PSD formatını destekler ancak aynı zamanda diğer çeşitli formatlar için dönüştürme seçenekleri de sağlar.

### S2: Alt gölge özelliklerini daha da özelleştirebilir miyim?

A2: Kesinlikle! Özel gereksinimlerinizi karşılamak ve istediğiniz görsel efektleri elde etmek için kodu ayarlamaktan çekinmeyin.

### S3: Aspose.PSD for .NET için ek belgeleri nerede bulabilirim?

 A3: Belgelere bakın[Burada](https://reference.aspose.com/psd/net/) Aspose.PSD işlevlerine ilişkin ayrıntılı bilgiler için.

### S4: Aspose.PSD for .NET'in ücretsiz deneme sürümü mevcut mu?

 C4: Evet, ücretsiz denemeyi keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S5: Aspose.PSD for .NET ile ilgili nasıl destek alabilirim veya yardım alabilirim?

 Cevap5: Aspose.PSD forumunu ziyaret edin[Burada](https://forum.aspose.com/c/psd/34) toplulukla etkileşime geçmek ve uzman tavsiyesi almak.