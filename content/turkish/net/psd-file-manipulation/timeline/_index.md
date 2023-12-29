---
title: Aspose.PSD for .NET'te Zaman Çizelgesi ile Çalışmak
linktitle: Zaman Çizelgesi ile Çalışmak
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET Timeline sınıfı ile PSD görüntü işlemeyi geliştirin. Çerçeve özelliklerini, katman durumlarını kontrol edin ve yaratıcı olasılıkları zahmetsizce ortaya çıkarın.
type: docs
weight: 16
url: /tr/net/psd-file-manipulation/timeline/
---
## giriiş
Grafik tasarımın ve görüntü manipülasyonunun dinamik dünyasında, görüntülerin zaman çizelgesini kontrol etme ve değiştirme yeteneği çok önemlidir. Aspose.PSD for .NET, Timeline sınıfıyla güçlü bir çözüm sunar. Bu üst düzey özellik, kullanıcıların PsdImage'ın zaman çizelgesinde kare gecikmesini değiştirmek, belirli karelerdeki katman durumlarını düzenlemek ve daha fazlası gibi değişiklikler yapmasına olanak tanır.
## Önkoşullar
Zaman Çizelgesi sınıfının sunduğu heyecan verici olanaklara dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
-  Aspose.PSD for .NET Library: Aspose.PSD for .NET kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[.NET belgeleri için Aspose.PSD](https://reference.aspose.com/psd/net/).
-  Belge ve Çıktı Dizinleri: Koddaki belgenizin ve çıktı dizinlerinizin yollarını tanımlayın. Ayarlayın`baseDir` Ve`outputDir` proje yapınıza göre değişkenler.
Şimdi Timeline sınıfının nasıl kullanılacağını adım adım inceleyelim.
## Ad Alanlarını İçe Aktar
Timeline sınıfıyla çalışmaya başlamak için kodunuza gerekli ad alanlarını içe aktarın:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## 1. Adım: PSD Görüntüsünü Yükleyin
Belirtilen kaynak dosyadan PSD görüntüsünü yükleyerek başlayın. Kaynak dosya yolunun doğru şekilde ayarlandığından emin olun:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Daha sonraki işlemler için kodunuz buraya gelecek
}
```
## 2. Adım: Zaman Çizelgesi'ne erişin
PSD görüntüsü yüklendikten sonra aşağıdaki kodu kullanarak Zaman Çizelgesi'ne erişin:
```csharp
Timeline timeline = psdImage.Timeline;
```
## 3. Adım: İmha Yöntemini Değiştirin
Belirli bir çerçevenin imha yöntemini değiştirin. Bu örnekte, çerçeve 1'in imha yöntemini değiştiriyoruz:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## 4. Adım: Kare Gecikmesini Ayarlayın
Belirli bir karenin gecikmesini değiştirin. Burada 2. karenin gecikmesini 15 olarak değiştiriyoruz:
```csharp
timeline.Frames[1].Delay = 15;
```
## 5. Adım: Katman Durumunu Düzenleyin
Belirli bir karedeki 'Katman 1'in opaklığını değiştirin. Bu örnekte, kare 2'de opaklığı 50'ye ayarladık:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Adım 6: Katmanı Taşı
'Katman 1'i belirli bir karenin sol alt köşesine taşıyın (bu örnekte kare 3):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Adım 7: Yeni Çerçeve Ekle
Zaman çizelgesine yeni bir kare ekleyin:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Adım 8: Karışım Modunu Değiştirin
Belirli bir karede (bu durumda kare 4) 'Katman 1'in karışım modunu değiştirin:
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Adım 9: Değişiklikleri Kaydet
Değişiklikleri PsdImage örneğine geri uygulayın ve değiştirilen PSD görüntüsünü kaydedin:
```csharp
psdImage.Save(outputPsd);
```
## Adım 10: Temizleme
Son olarak geçici çıktı dosyasını silerek temizleyin:
```csharp
File.Delete(outputPsd);
```
## Çözüm

Sonuç olarak, Aspose.PSD for .NET'teki Timeline sınıfı, geliştiricilerin PSD görüntülerinin zaman çizelgesi üzerinde ayrıntılı kontrole sahip olmalarını sağlar. Bir dizi basit adımla çerçeve özelliklerini, katman durumlarını ve daha fazlasını değiştirerek yaratıcı olasılıklara kapı açabilirsiniz.

## SSS'ler

### S1: Aspose.PSD for .NET yeni başlayanlar için uygun mu?

A1: Kesinlikle! Aspose.PSD for .NET, kullanıcı dostu bir arayüz ve kapsamlı belgeler sunarak hem yeni başlayanlar hem de deneyimli geliştiriciler için erişilebilir olmasını sağlar.

### S2: Zaman çizelgesi değişikliklerini GIF görüntülerine uygulayabilir miyim?

Cevap2: Timeline sınıfı özellikle PSD görüntüleri için tasarlanmıştır. GIF manipülasyonu için Aspose.GIF for .NET'e bakın.

### S3: Nerede ek destek bulabilirim veya sorunları tartışabilirim?

 A3: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) Topluluk desteği ve konu tartışmaları için.

### S4: Aspose.PSD for .NET için nasıl geçici lisans alabilirim?

 Cevap4: Geçici bir lisans edinin[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.PSD for .NET kullanmanın temel faydaları nelerdir?

Cevap5: Aspose.PSD for .NET, gelişmiş görüntü işleme yetenekleri, PSD dosya işleme ve yüksek performanslı işleme sunar.