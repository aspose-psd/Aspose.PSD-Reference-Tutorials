---
title: Aspose.PSD for .NET'te Görüntüleri Birleştirme
linktitle: Görselleri Birleştirme
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD ile görüntüleri .NET'te zahmetsizce birleştirin. Sorunsuz görüntü işleme için adım adım eğitimimizi izleyin.
type: docs
weight: 10
url: /tr/net/image-manipulation/combine-images/
---
## giriiş

Aspose.PSD for .NET kullanarak görüntüleri birleştirmeye yönelik adım adım eğitimimize hoş geldiniz! Aspose.PSD, geliştiricilerin Adobe Photoshop dosyalarıyla sorunsuz bir şekilde çalışmasına olanak tanıyan güçlü bir .NET kitaplığıdır. Bu eğitimde, Aspose.PSD kullanarak görüntüleri birleştirme sürecinde size pratik örnekler ve ayrıntılı adımlar sunarak rehberlik edeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD Kütüphanesi: Aspose.PSD kütüphanesinin kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/psd/net/).

Şimdi öğreticiye geçelim!

## Ad Alanlarını İçe Aktar

Öncelikle Aspose.PSD ile çalışmak için gerekli ad alanlarını içe aktarmanız gerekiyor. .NET dosyanızın başına aşağıdaki kod parçacığını ekleyin:

```csharp
using Aspose.PSD.ImageOptions;
using Aspose.PSD.Sources;
```

## 1. Adım: Ortamı Ayarlayın

Ortamı ayarlayarak ve resimleriniz için dizini belirterek başlayın.

```csharp
// Belgeler dizininin yolu.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
```

## 2. Adım: PsdOptions Örneği Oluşturun

Özelliklerini gerektiği gibi ayarlayarak bir PsdOptions örneği oluşturun.

```csharp
PsdOptions imageOptions = new PsdOptions();
```

## 3. Adım: FileCreateSource'u oluşturun

FileCreateSource'un bir örneğini oluşturun ve bunu imageOptions'ın Source özelliğine atayın.

```csharp
imageOptions.Source = new FileCreateSource(dataDir + "Two_images_result_out.psd", false);
```

## 4. Adım: Görüntü Örneği Oluşturun

Bir Image örneği oluşturun ve tuval boyutunu tanımlayın.

```csharp
using (var image = Image.Create(imageOptions, 600, 600))
```

## Adım 5: Grafikleri Başlatın ve Görüntüleri Çizin

Graphics'in bir örneğini başlatın, görüntü yüzeyini beyaz renkle temizleyin ve görüntüleri tuval üzerine çizin.

```csharp
var graphics = new Graphics(image);
graphics.Clear(Color.White);
graphics.DrawImage(Image.Load(dataDir + "example1.psd"), 0, 0, 300, 600);
graphics.DrawImage(Image.Load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

## Adım 6: Birleştirilmiş Görüntüyü Kaydedin

Son birleştirilmiş görüntüyü kaydedin.

```csharp
image.Save();
```

Tebrikler! Aspose.PSD for .NET'i kullanarak iki görüntüyü başarıyla birleştirdiniz.

## Çözüm

Bu eğitimde, Aspose.PSD'yi kullanarak görüntüleri birleştirme sürecinde size yol gösterdik. Sezgisel API'si ile Aspose.PSD, geliştiricilerin Photoshop dosyalarını .NET uygulamalarında sorunsuz bir şekilde kullanmalarına olanak tanır.

## SSS'ler

### S1: Aspose.PSD, .NET'in tüm sürümleriyle uyumlu mudur?

C1: Evet, Aspose.PSD, .NET'in tüm sürümleriyle uyumludur ve geliştirme projelerinizde çok yönlülük sağlar.

### S2: Aspose.PSD'yi ticari amaçlarla kullanabilir miyim?

 C2: Evet, Aspose.PSD hem kişisel hem de ticari amaçlarla kullanılabilir. Lisans ayrıntılarını kontrol edin[Burada](https://purchase.aspose.com/buy).

### S3: Aspose.PSD desteğini nasıl alabilirim?

 A3: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği için veya bir destek planı satın almayı düşünün.

### S4: Aspose.PSD için ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S5: Aspose.PSD için geçici bir lisans alabilir miyim?

 Cevap5: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).