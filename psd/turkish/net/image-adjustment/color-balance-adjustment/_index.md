---
title: Aspose.PSD for .NET'te Renk Dengesi Ayarını Uygulama
linktitle: Renk Dengesi Ayarını Uygulama
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'in Renk Dengesi Ayarlama özelliği ile PSD görüntü renklerini zahmetsizce geliştirin. Çarpıcı sonuçlar için adım adım kılavuzumuzu izleyin.
weight: 14
url: /tr/net/image-adjustment/color-balance-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET'te Renk Dengesi Ayarını Uygulama

## giriiş

Aspose.PSD for .NET'te Renk Dengesi Ayarlamasının uygulanmasına ilişkin bu kapsamlı kılavuza hoş geldiniz! Aspose.PSD, geliştiricilerin PSD dosyalarıyla verimli bir şekilde çalışmasına olanak tanıyan güçlü bir .NET kitaplığıdır. Bu eğitimde, PSD görsellerinizin renk dengesini kolaylıkla geliştirmenizi sağlayan Renk Dengesi Ayarlama özelliğine odaklanacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD for .NET Library: Kitaplığı şuradan indirip yükleyin:[Aspose.PSD web sitesi](https://releases.aspose.com/psd/net/).
- Geliştirme Ortamı: Makinenizde çalışan bir .NET geliştirme ortamının kurulu olduğundan emin olun.
- PSD Dosyası: Renk Dengesi Ayarını uygulamak istediğiniz bir PSD dosyasını hazır bulundurun.

## Ad Alanlarını İçe Aktar

.NET projenize Aspose.PSD özelliklerini kullanmak için gerekli ad alanlarını ekleyin. Kodunuza aşağıdaki satırları ekleyin:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Şimdi Renk Dengesi Ayarlama sürecini birden fazla adıma ayıralım:

## Adım 1: PSD Dosyasını Yükleyin

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Renk Dengesi Ayarı Kodu sonraki adımlarda eklenecektir.
}
```

## 2. Adım: Renk Dengesine Erişin ve Ayarlayın

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## 3. Adım: Ayarlanan Görüntüyü Kaydedin

```csharp
im.Save(outputPath);
```

Artık Aspose.PSD for .NET'i kullanarak Renk Dengesi Ayarını PSD dosyanıza başarıyla uyguladınız!

## Çözüm

Tebrikler! Aspose.PSD for .NET ile PSD görsellerinizin renk dengesini nasıl geliştireceğinizi öğrendiniz. İstenilen görsel efektleri elde etmek için farklı denge değerleriyle denemeler yapın.

## SSS'ler

### S1: Renk Dengesi Ayarını birden fazla katmana uygulayabilir miyim?

Cevap1: Evet, PSD dosyanızdaki tüm katmanları yineleyebilir ve renk dengesini gerektiği gibi ayarlayabilirsiniz.

### S2: Aspose.PSD for .NET, PSD dosyalarının toplu işlenmesi için uygun mudur?

A2: Kesinlikle! Aspose.PSD, PSD dosyaları için etkili toplu işleme yetenekleri sağlar.

### S3: Aspose.PSD for .NET için nasıl geçici lisans alabilirim?

 A3: Ziyaret edin[Aspose.PSD Geçici Lisansı](https://purchase.aspose.com/temporary-license/) Geçici bir lisans için.

### S4: Daha fazla örneği ve belgeyi nerede bulabilirim?

 A4: Keşfedin[Aspose.PSD belgeleri](https://reference.aspose.com/psd/net/) ayrıntılı örnekler ve kılavuzlar için.

### S5: Aspose.PSD for .NET için hangi destek seçenekleri mevcut?

 A5: ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
