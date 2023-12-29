---
title: Aspose.PSD for .NET'te Bradley Eşiğini Uygulama
linktitle: Bradley Eşiğinin Uygulanması
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'te Bradley Threshold'u kullanarak görüntü segmentasyonunu geliştirin. Etkili ikilileştirme için adım adım kılavuz.
type: docs
weight: 15
url: /tr/net/image-processing/apply-bradley-threshold/
---
## giriiş

Aspose.PSD for .NET'te Bradley Eşiğinin uygulanmasına ilişkin kapsamlı eğitimimize hoş geldiniz. Aspose.PSD for .NET, .NET uygulamalarınızda Photoshop dosyalarıyla çalışmanıza olanak tanıyan güçlü bir kütüphanedir. Bradley Eşikleme, görüntülerin ikilileştirilmesi için kullanılan ve nesnelerin arka plandan etkili bir şekilde ayrılmasına yardımcı olan bir tekniktir.

Bu eğitimde, Aspose.PSD for .NET'i kullanarak Bradley Eşiği uygulama sürecinde size yol göstereceğiz. Adımlara geçmeden önce gerekli önkoşulların mevcut olduğundan emin olun.

## Önkoşullar

Başlamadan önce aşağıdaki kurulumlara sahip olduğunuzdan emin olun:

-  Aspose.PSD for .NET Library: Kitaplığı şuradan indirip yükleyin:[.NET belgeleri için Aspose.PSD](https://reference.aspose.com/psd/net/).
- Belge Dizini: Kaynak PSD dosyanızı ve sonuçta ortaya çıkan ikili görüntüyü depolamak için bir dizin oluşturun.

Artık önkoşullar hazır olduğuna göre adım adım kılavuza geçelim.

## Ad Alanlarını İçe Aktar

Aspose.PSD işlevselliğine erişmek için .NET projenizde gerekli ad alanlarını içe aktardığınızdan emin olun:

```csharp
// Aspose.PSD ad alanlarını içe aktar
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## 1. Adım: Gürültülü Görüntüyü Yükleyin

Kaynak PSD dosyanızın yolunu ve ikilileştirilmiş çıktının hedefini tanımlayın:

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"binarized_out.png";
```

## Adım 2: Bradley Eşiğini Kullanarak Görüntüyü İkili Hale Getirin

PSD görüntüsünü yükleyin, eşik değerini belirtin, Bradley Eşiğini uygulayın ve çıktıyı PNG görüntüsü olarak kaydedin:

```csharp
// Bir resim yükle
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    // Eşik değerini tanımlayın
    double threshold = 0.15;

    // BinarizeBradley yöntemini çağırın ve eşik değerini parametre olarak iletin
    image.BinarizeBradley(threshold);

    // Çıktı görüntüsünü kaydedin
    image.Save(destName, new PngOptions());
}
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'te Bradley Eşiğini başarıyla uyguladınız. Bu teknik, çeşitli uygulamalarda görüntü bölümlemesini geliştirmek için çok değerlidir.

Görüntü işleme görevlerinizi optimize etmek için Aspose.PSD for .NET tarafından sağlanan daha fazla özellik ve işlevi keşfetmekten çekinmeyin.

## SSS'ler

### S1: Bradley Eşiği'ni herhangi bir görüntü türüne uygulayabilir miyim?

Cevap1: Evet, Bradley Eşikleme, çeşitli görüntü türlerine uygun, çok yönlü bir tekniktir.

### S2: Ek Aspose.PSD belgelerini nerede bulabilirim?

 A2: Bkz.[dokümantasyon](https://reference.aspose.com/psd/net/) Aspose.PSD for .NET hakkında ayrıntılı bilgi için.

### S3: Ücretsiz deneme sürümü mevcut mu?

 Cevap3: Evet, Aspose.PSD for .NET'in ücretsiz deneme sürümünü keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD için nasıl destek alabilirim?

 A4: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.

### S5: Aspose.PSD lisansını nereden satın alabilirim?

 A5: Bir lisans satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).