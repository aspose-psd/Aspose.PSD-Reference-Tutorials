---
title: Aspose.PSD for .NET ile Eliptik Şekiller Oluşturma
linktitle: Aspose.PSD for .NET ile Eliptik Şekiller Oluşturma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD'yi kullanarak .NET'te eliptik şekillerin nasıl çizileceğini öğrenin. Kod örnekleri içeren adım adım kılavuz. Zahmetsizce çarpıcı grafikler oluşturun.
type: docs
weight: 13
url: /tr/net/psd-drawing-techniques/creating-elliptical-shapes/
---
## giriiş

Aspose.PSD for .NET kullanarak eliptik şekiller oluşturmaya ilişkin kapsamlı kılavuzumuza hoş geldiniz. Aspose.PSD, geliştiricilerin Adobe Photoshop gerektirmeden Photoshop dosyalarını değiştirmesine ve dönüştürmesine olanak tanıyan güçlü bir .NET kitaplığıdır. Bu eğitimde, kütüphaneyi kullanarak eliptik şekiller çizme sürecinde size yol göstereceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD for .NET Library: .NET projenizde Aspose.PSD kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Aspose.PSD for .NET Belgeleri](https://reference.aspose.com/psd/net/).

- .NET Ortamı: Bu eğitimde, .NET çerçevesi hakkında çalışma bilgisine sahip olduğunuz varsayılmaktadır.

## Ad Alanlarını İçe Aktar

Başlamak için gerekli ad alanlarını projenize aktarın. Bu, eliptik şekilleri çizmek için gereken sınıflara ve yöntemlere erişmenizi sağlar. İşte bir örnek:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Şimdi eliptik şekiller oluşturma sürecini birden fazla adıma ayıralım:

## 1. Adım: Belge Dizinini Ayarlayın

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";
```

## Adım 2: BmpOptions Örneğini Oluşturun

```csharp
// Bir BmpOptions örneği oluşturun ve çeşitli özelliklerini ayarlayın
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## 3. Adım: Bir Görüntü Örneği Oluşturun

```csharp
// Görüntünün bir örneğini oluşturun
using (Image image = new PsdImage(100, 100))
{
    // Graphics sınıfının ve Clear Graphics yüzeyinin bir örneğini oluşturun ve başlatın
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Adım 4: Noktalı Elips Şekli Çizin

```csharp
    // Kırmızı renge sahip Kalem nesnesini ve onu çevreleyen bir Dikdörtgeni belirterek noktalı bir elips şekli çizin
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Adım 5: Sürekli Bir Elips Şekli Çizin

```csharp
    // Mavi renkli düz bir fırçaya ve onu çevreleyen bir Dikdörtgene sahip Kalem nesnesini belirterek sürekli bir elips şekli çizin
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Görüntüyü bmp dosya formatına aktarın.
    image.Save(outpath, saveOptions);
}
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak başarıyla eliptik şekiller oluşturdunuz. Bu eğitim, ortamın ayarlanmasından hem noktalı hem de sürekli elips şekillerinin çizilmesine kadar temel adımları kapsıyordu.

## SSS'ler

### S1: Aspose.PSD for .NET belgelerini nerede bulabilirim?

 A1: Belgeler mevcut[Burada](https://reference.aspose.com/psd/net/).

### S2: Aspose.PSD for .NET'i nasıl indirebilirim?

 A2: Sürüm sayfasından indirebilirsiniz[Burada](https://releases.aspose.com/psd/net/).

### S3: Ücretsiz deneme sürümü mevcut mu?

 C3: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD for .NET desteğini nasıl alabilirim?

 Cevap4: Destek forumunu ziyaret edin[Burada](https://forum.aspose.com/c/psd/34).

### S5: Test için geçici bir lisansa ihtiyacım var mı?

 Cevap5: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).