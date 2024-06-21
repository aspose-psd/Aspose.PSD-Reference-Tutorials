---
title: Aspose.PSD for .NET'te PNG'ye Dönüştürürken PSD Dosyalarını Kırpma
linktitle: PNG'ye Dönüştürürken PSD Dosyalarını Kırpma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET'i kullanarak PSD dosyalarını zahmetsizce nasıl kırpacağınızı öğrenin. PNG'ye sorunsuz dönüşüm için adım adım kılavuzumuzu izleyin.
type: docs
weight: 18
url: /tr/net/psd-file-manipulation/crop-psd-conversion-png/
---
## giriiş
.NET geliştirme alanında görüntüleri değiştirmek ve dönüştürmek yaygın bir görevdir. Aspose.PSD for .NET, bu süreci kolaylaştırmak için güçlü bir araç seti sağlar. Sık karşılaşılan gereksinimlerden biri, PSD dosyalarını PNG'ye dönüştürmeden önce kırpmaktır. Bu adım adım eğitimde Aspose.PSD for .NET'i kullanarak süreci derinlemesine inceleyeceğiz.
## Önkoşullar
Bu yolculuğa çıkmadan önce aşağıdakilere sahip olduğunuzdan emin olun:
-  Aspose.PSD for .NET Library: Kitaplığı şuradan indirip yükleyin:[Aspose.PSD for .NET Belgeleri](https://reference.aspose.com/psd/net/).
- Örnek PSD Dosyası: Deney için hazır bir PSD dosyası bulundurun. Eğer elinizde yoksa eğitimde verilen örneği kullanabilirsiniz.
- .NET Ortamı: Çalışan bir .NET geliştirme ortamı kurduğunuzdan emin olun.
- Belge Dizini: Kodda belge dizininizin yolunu belirtin.
## Ad Alanlarını İçe Aktar
.NET projenize Aspose.PSD for .NET için gerekli ad alanlarını ekleyin:
```csharp
using Aspose.PSD.ImageOptions;
```
## 1. Adım: PSD Görüntüsünü Yükleyin
```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// Mevcut bir PSD görüntüsünü yükleyin
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // Daha sonraki adımlara ilişkin kodunuz buraya gelecek
}
```
## Adım 2: Kırpma Dikdörtgenini Tanımlayın
```csharp
// X, y, genişlik ve yüksekliği ileterek Rectangle sınıfının bir örneğini oluşturun
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## 3. Adım: Görüntüyü Kırpın
```csharp
// Image sınıfının kırpma yöntemini çağırın ve dikdörtgen sınıfı örneğini iletin
image.Crop(cropRectangle);
```
## Adım 4: PNG Seçeneklerini Belirleyin
```csharp
// PngOptions sınıfının bir örneğini oluşturun
PngOptions pngOptions = new PngOptions();
```
## Adım 5: Kırpılan Resmi PNG olarak kaydedin.
```csharp
// Kaydetme yöntemini çağırın, çıktı yolunu sağlayın ve PSD dosyasını PNG'ye dönüştürmek ve çıktıyı kaydetmek için PngOptions'ı kullanın.
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## Çözüm

Tebrikler! Aspose.PSD for .NET kullanarak PSD dosyalarını PNG'ye dönüştürürken nasıl kırpacağınızı başarıyla öğrendiniz. Bu yetenek, çeşitli görüntü işleme senaryolarında çok değerli olabilir.

## SSS'ler

### S1: Bu kütüphaneyi ticari bir projede kullanabilir miyim?

 Cevap1: Evet, Aspose.PSD for .NET ticari kullanıma açıktır. Bakınız[Aspose.PSD Lisanslaması](https://purchase.aspose.com/buy) detaylar için.

### S2: Ücretsiz deneme sürümü var mı?

 A2: Kesinlikle! Ücretsiz deneme sürümünü keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.PSD for .NET desteğini nerede bulabilirim?

 A3: Ziyaret edin[Aspose.PSD Forumu](https://forum.aspose.com/c/psd/34) herhangi bir yardım veya sorularınız için.

### S4: Geçici lisansı nasıl edinebilirim?

 Cevap4: Geçici bir lisansa ihtiyacınız varsa bir tane alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Belgelerde herhangi bir örnek veya eğitim var mı?

 A5: Evet, kapsamlı belgeler ve örnekler bulabilirsiniz[Burada](https://reference.aspose.com/psd/net/).