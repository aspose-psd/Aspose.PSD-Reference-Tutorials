---
title: Aspose.PSD for .NET'te Görüntüleri Genişletme ve Kırpma
linktitle: Görüntüleri Genişletme ve Kırpma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'i kullanarak görüntüleri dinamik olarak nasıl genişleteceğinizi ve kırpacağınızı öğrenin. Sorunsuz görüntü işleme için adım adım kılavuzumuzu izleyin.
type: docs
weight: 13
url: /tr/net/image-manipulation/expand-crop-images/
---
## giriiş

Aspose.PSD for .NET, geliştiricilerin .NET uygulamalarında çeşitli görüntü formatlarıyla çalışmasına olanak tanıyan kapsamlı bir görüntüleme kitaplığıdır. Öne çıkan özelliklerinden biri, görüntüleri kolaylıkla değiştirebilme yeteneğidir. Bu eğitimde, görüntüleri genişletmeye ve kırpmaya odaklanacağız ve size Aspose.PSD kullanarak bu görevleri gerçekleştirmeniz için uygulamalı bir kılavuz sunacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.PSD for .NET Library: Aspose.PSD for .NET kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[.NET belgeleri için Aspose.PSD](https://reference.aspose.com/psd/net/).

- Örnek Resim: Eğitim için kullanacağınız örnek bir resim dosyası (örneğin, "example1.psd") hazırlayın.

Şimdi adım adım kılavuza başlayalım.

## Ad Alanlarını İçe Aktar

Aspose.PSD for .NET tarafından sağlanan işlevlerden yararlanmak için gerekli ad alanlarını içe aktararak başlayın. Aşağıdaki ad alanlarını kodunuza ekleyin:

```csharp
using Aspose.PSD.ImageOptions;
```

## Adım 1: Projeyi Kurun

 Aspose.PSD for .NET ile entegre edilmiş bir projenizin olduğundan emin olun. Değilse, aşağıdakileri izleyin[dokümantasyon](https://reference.aspose.com/psd/net/) rehberlik için.

## 2. Adım: Görüntüyü Yükleyin

Örnek görüntüyü aşağıdaki kodu kullanarak yükleyin:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

//Resmi yükle
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Görüntü işlemeye yönelik ek kod buraya gelecek
}
```

## 3. Adım: Görüntü Verilerini Önbelleğe Alın

Performansı optimize etmek için görüntü verilerini önbelleğe alın:

```csharp
rasterImage.CacheData();
```

## Adım 4: Hedef Dikdörtgeni Tanımlayın

Rectangle sınıfının bir örneğini oluşturun ve dikdörtgenin X, Y, Genişlik ve Yüksekliğini tanımlayın. Bu, görüntünün genişletileceği veya kırpılacağı alan olacaktır.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Adım 5: Çıktı Görüntüsünü Kaydedin

Çıktı görüntüsünü belirtilen seçeneklerle ve hedef dikdörtgenle kaydedin:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak görüntüleri nasıl genişleteceğinizi ve kırpacağınızı başarıyla öğrendiniz. Bu güçlü kitaplık, .NET uygulamalarınızda görüntü işleme için bir olasılıklar dünyasının kapılarını açar.

## SSS'ler

### S1: Aspose.PSD, PSD'nin yanı sıra diğer görüntü formatlarını da destekleyebilir mi?

Cevap1: Evet, Aspose.PSD, JPEG, PNG, GIF ve daha fazlasını içeren çok çeşitli görüntü formatlarını destekler.

### S2: Aspose.PSD desteğini nerede bulabilirim?

 C2: Şu adreste destek bulabilir ve toplulukla etkileşime geçebilirsiniz:[Aspose.PSD Forumu](https://forum.aspose.com/c/psd/34).

### S3 Aspose.PSD for .NET'in ücretsiz deneme sürümü mevcut mu?

 C3: Evet, aşağıdaki ücretsiz deneme sürümüyle özellikleri keşfedebilirsiniz:[Aspose.PSD Ücretsiz Deneme](https://releases.aspose.com/).

### S4: Aspose.PSD için geçici lisansı nasıl edinebilirim?

 Cevap4: Geçici lisansı şu adresten alabilirsiniz:[Aspose.PSD Geçici Lisansı](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.PSD for .NET'i nereden satın alabilirim?

 Cevap5: Kütüphaneyi şu adresten satın alabilirsiniz:[Aspose.PSD Satın Alma Sayfası](https://purchase.aspose.com/buy).