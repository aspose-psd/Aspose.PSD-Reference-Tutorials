---
title: Aspose.PSD for .NET'te PSD Görüntü Zaman Çizelgesini Kullanma
linktitle: PSD Görüntü Zaman Çizelgesini Kullanma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'i kullanarak PSD görüntü zaman çizelgelerini zahmetsizce yönetmeyi öğrenin. Çerçeve ekleyin, sorunsuzca geçiş yapın ve görüntü düzenleme becerilerinizi geliştirin.
type: docs
weight: 17
url: /tr/net/psd-file-manipulation/psd-image-timeline/
---
## giriiş
Görüntü işlemenin dinamik dünyasında, Aspose.PSD for .NET, PSD görüntü zaman çizelgelerinin yönetimi için sağlam çözümler sunan güçlü bir araç seti olarak öne çıkıyor. İster deneyimli bir geliştirici ister kodlama meraklısı olun, bu eğitim Aspose.PSD'yi kullanarak görüntü zaman çizelgelerini kolaylıkla değiştirme sürecinde size rehberlik edecektir.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:
- Temel C# ve .NET framework bilgisi.
-  Aspose.PSD for .NET kuruldu. En son sürümü indirebilirsiniz[Burada](https://releases.aspose.com/psd/net/).
- Sorunsuz uygulama için Visual Studio gibi bir kod düzenleyici.
## Ad Alanlarını İçe Aktar
Aspose.PSD işlevlerine erişmek için C# projenizde gerekli ad alanlarını içe aktardığınızdan emin olun:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## 1. Adım: Projenizi Kurun
Tercih ettiğiniz geliştirme ortamında yeni bir C# projesi oluşturarak başlayın. Aspose.PSD for .NET'e başvurulduğundan emin olun.
## Adım 2: Dizinlerinizi Tanımlayın
Kaynak PSD dosyanız için dizinleri ve üzerinde değişiklik yapılan görüntünün kaydedileceği çıktı dizinini ayarlayın.
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
## 3. Adım: PSD Görüntüsünü Yükleme ve Düzenleme
Bir PSD dosyası yüklemek, zaman çizelgesine yeni bir kare eklemek, belirli bir kareye geçmek ve üzerinde değişiklik yapılan görüntüyü kaydetmek için aşağıdaki kod parçacığını kullanın.
```csharp
string sourceFile = Path.Combine(baseDir, "4_animated.psd");
string outputFile = Path.Combine(outputDir, "output_edited.psd");
using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    Timeline timeline = psdImage.Timeline;
    // Bir kare daha ekle
    List<Frame> frames = new List<Frame>(timeline.Frames);
    frames.Add(new Frame());
    timeline.Frames = frames.ToArray();
    timeline.SwitchActiveFrame(4);
    psdImage.Save(outputFile);
}
```
## Adım 4: Temizleme
Düzenlemeden sonra geçici dosyayı silin.
```csharp
File.Delete(outputFile);
```
## Adım 5: Yürütmeyi Doğrulayın
Son olarak kodun başarıyla yürütüldüğünü onaylayın.
```csharp
Console.WriteLine("SupportOfPsdImageTimelineProperty executed successfully");
```
## Çözüm
Tebrikler! Aspose.PSD for .NET'i kullanarak PSD görüntü zaman çizelgelerini yönetmenin inceliklerini başarıyla aştınız. Bu eğitim, çerçeveler eklemenizi, bunlar arasında geçiş yapmanızı ve düzenlenmiş görüntünüzü zahmetsizce kaydetmenizi sağlar.
## SSS'ler

### S1: Aspose.PSD for .NET'i diğer programlama dilleriyle kullanabilir miyim?

Cevap1: Hayır, Aspose.PSD özellikle .NET uygulamaları için tasarlanmıştır.

### S2: Aspose.PSD'yi kullanmak için lisans gerekli mi?

 A2: Evet, geçerli bir lisansa ihtiyacınız var. Anla[Burada](https://purchase.aspose.com/buy).

### S3: Lisans satın almadan önce Aspose.PSD'yi ücretsiz deneyebilir miyim?

 C3: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD için ayrıntılı belgeleri nerede bulabilirim?

 Cevap4: Belgelere bakın[Burada](https://reference.aspose.com/psd/net/).

### S5: Yardıma mı ihtiyacınız var veya sorularınız mı var?

 Cevap5: Aspose.PSD topluluk forumunu ziyaret edin[Burada](https://forum.aspose.com/c/psd/34).