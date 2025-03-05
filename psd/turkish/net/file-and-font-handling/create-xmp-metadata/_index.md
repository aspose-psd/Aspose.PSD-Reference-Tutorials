---
title: Aspose.PSD for .NET'te XMP Meta Verisi Oluşturma
linktitle: XMP Meta Verileri Oluşturma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'te XMP meta verisi oluşturmayı keşfedin. Kusursuz manipülasyonla görüntü organizasyonunu geliştirin.
type: docs
weight: 10
url: /tr/net/file-and-font-handling/create-xmp-metadata/
---
## giriiş

.NET geliştirmenin dinamik dünyasında, görüntüleri hassas bir şekilde değiştirmek birçok uygulamanın çok önemli bir yönüdür. Bu eğitim, görüntü işleme görevlerini basitleştiren güçlü bir kütüphane olan Aspose.PSD for .NET'te XMP meta verilerinin oluşturulmasını araştırıyor. XMP (Genişletilebilir Meta Veri Platformu), meta verileri görüntü dosyalarına yerleştirmenize olanak tanıyarak, görüntülerle ilişkili bilgilerin verimli bir şekilde düzenlenmesini ve alınmasını kolaylaştırır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD for .NET Library: Kitaplığı şuradan indirip yükleyin:[Aspose.PSD belgeleri](https://reference.aspose.com/psd/net/).

- Geliştirme Ortamı: Visual Studio veya tercih ettiğiniz IDE ile bir .NET geliştirme ortamı kurun.

- Temel .NET Bilgisi: Bu eğitimde .NET geliştirme konusunda temel bir anlayış varsayıldığından, temel .NET kavramlarına aşina olun.

## Ad Alanlarını İçe Aktar

.NET projenize Aspose.PSD işlevselliğine erişmek için gerekli ad alanlarını ekleyin:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

Şimdi XMP meta verileri oluşturma sürecini bir dizi kapsamlı adıma ayıralım.

## 1. Adım: Görüntü Boyutunu ve Dikdörtgeni Belirleyin

```csharp
// Belgeler dizininin yolu.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//Bir Dikdörtgen tanımlayarak görüntünün boyutunu belirtin
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## 2. Adım: Yeni Bir Görüntü Oluşturun

```csharp
// Örnek amaçlı olarak yepyeni bir görüntü oluşturun
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // Resim işleme kodu buraya gelecek...
}
```

## 3. Adım: XMP Başlığı ve XMP Fragmanı Oluşturun

```csharp
// Bir XMP-Header örneği oluşturun
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Farklı nitelikleri ayarlamak için XMP-TrailerPi, XMPmeta sınıfının bir örneğini oluşturun
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## 4. Adım: XMP Niteliklerini Ayarlayın

```csharp
// XMP niteliklerini ayarlayın, örneğin:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Adım 5: XMP Paket Sarmalayıcı Oluşturun

```csharp
// Tüm meta verileri içeren bir XmpPacketWrapper örneği oluşturun
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Adım 6: Photoshop Paketi Oluşturun ve Nitelikleri Ayarlayın

```csharp
// Photoshop paketinin bir örneğini oluşturun ve photoshop niteliklerini ayarlayın
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## Adım 7: Photoshop Paketini XMP Meta Verilerine Ekleme

```csharp
// Photoshop paketini XMP meta verilerine ekleyin
xmpData.AddPackage(photoshopPackage);
```

## Adım 8: DublinCore Paketi Oluşturun ve Nitelikleri Ayarlayın

```csharp
// DublinCore paketinin bir örneğini oluşturun ve dublinCore niteliklerini ayarlayın
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Adım 9: DublinCore Paketini XMP Meta Verilerine Ekleme

```csharp
// DublinCore Paketini XMP meta verilerine ekleyin
xmpData.AddPackage(dublinCorePackage);
```

## 10. Adım: XMP Meta Verilerini Güncelleyin ve Görüntüyü Kaydedin

```csharp
using (var ms = new MemoryStream())
{
    // XMP meta verilerini görüntüye güncelleyin ve görüntüyü diske veya bellek akışına kaydedin
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## Adım 11: Görüntüyü Yükleyin ve Meta Verileri Okuyun

```csharp
// Meta verileri okumak/almak için görüntüyü bellek akışından veya diskten yükleyin
using (var img = (PsdImage)Image.Load(ms))
{
    // XMP meta verilerini alma
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // Paket verilerini kullan...
    }
}
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'te XMP meta verilerini başarıyla oluşturdunuz. Bu güçlü yetenek, görüntü işleme yeteneklerinizi geliştirerek, etkili bir organizasyona ve hayati bilgilerin alınmasına olanak tanır.

## SSS'ler

### S1: Aspose.PSD for .NET tüm görüntü formatlarıyla uyumlu mu?

Cevap1: Aspose.PSD öncelikle PSD (Adobe Photoshop) dosya formatına odaklanır ancak diğer çeşitli formatları da destekler.

### S2: Mevcut XMP meta verilerini Aspose.PSD for .NET kullanarak değiştirebilir miyim?

C2: Evet, Aspose.PSD mevcut XMP meta verilerini hem okumanıza hem de değiştirmenize olanak tanır.

### S3: Aspose.PSD for .NET kullanılırken görüntü boyutunda herhangi bir sınırlama var mı?

Cevap3: Aspose.PSD farklı boyutlardaki görselleri işleyebilir ancak çok büyük görseller ek hususlar gerektirebilir.

### S4: Aspose.PSD for .NET ne sıklıkla güncelleniyor?

Cevap4: En son .NET framework sürümleri ve endüstri standartlarıyla uyumluluğu sağlamak için güncellemeler düzenli olarak yayınlanmaktadır.

### S5: Aspose.PSD desteği için bir topluluk forumu var mı?

 C: Evet, şu konuda destek ve tartışmalar bulabilirsiniz:[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34).