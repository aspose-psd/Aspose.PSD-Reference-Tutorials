---
title: Aspose.PSD for .NET'te Bir Görüntüyü Döndürme
linktitle: Bir Görüntüyü Döndürme
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD ile .NET'te görüntüleri zahmetsizce döndürmeyi öğrenin. Adım adım eğitimimizi takip edin.
weight: 15
url: /tr/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET'te Bir Görüntüyü Döndürme

## giriiş

.NET kullanarak görüntü işleme dünyasına dalıyorsanız, Aspose.PSD kusursuz ve verimli görüntü işleme için başvuracağınız araçtır. Bu eğitimde temel bir göreve odaklanacağız: Aspose.PSD for .NET kullanarak bir görüntüyü döndürme. Süreci basit, uygulanabilir adımlara ayırırken takip edin.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.PSD for .NET Library: Kitaplığı şuradan indirip yükleyin:[Aspose.PSD .NET belgeleri](https://reference.aspose.com/psd/net/).

- Belge Dizininiz: Resimlerinizin depolandığı bir dizin oluşturun. Kod pasajındaki "Belge Dizininiz"i bu dizinin yoluyla değiştirin.

## Ad Alanlarını İçe Aktar

Aspose.PSD işlevselliğine erişmek için gerekli ad alanlarını eklediğinizden emin olun. .NET projenizin başına aşağıdaki satırları ekleyin:

```csharp
using Aspose.PSD.ImageOptions;
```

## 1. Adım: Görüntüyü Yükleyin

```csharp
string sourceFile = dataDir + @"sample.psd";

// Mevcut bir görüntüyü RasterImage sınıfının bir örneğine yükleme
using (Image image = Image.Load(sourceFile))
{
```

## Adım 2: Görüntüyü Döndürün

```csharp
    // Resmi saat yönünde 270 derece döndürün
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 3. Adım: Döndürülmüş Görüntüyü Kaydetme

```csharp
    // Döndürülmüş görüntüyü JPEG dosyası olarak kaydedin
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

İşte bu! Sadece birkaç satır kodla Aspose.PSD for .NET'i kullanarak bir görüntüyü başarıyla döndürdünüz.

## Çözüm

Bu eğitimde Aspose.PSD for .NET kullanarak görüntüleri döndürmenin temellerini inceledik. Aspose.PSD, görüntü işleme için güçlü bir araç seti sağlar ve bu da onu .NET geliştiricileri için vazgeçilmez bir kitaplık haline getirir. Farklı rotasyonlarla denemeler yapın ve görüntü işleme iş akışlarınızı geliştirmek için daha fazla özellik keşfedin.

## SSS'ler

### S1: Aspose.PSD'yi kullanarak görüntüleri özel bir açıyla döndürebilir miyim?

 Evet, Aspose.PSD, dönüş için özel bir açı belirlemenize olanak tanır. Basitçe değiştirin`RotateFlipType.Rotate270FlipNone` İstediğiniz dönüş açısına göre hizalayın.

### S2: Aspose.PSD çeşitli görüntü formatlarıyla uyumlu mudur?

 Kesinlikle. Aspose.PSD, PSD, JPEG, PNG ve daha fazlasını içeren çok çeşitli görüntü formatlarını destekler. Kontrol edin[dokümantasyon](https://reference.aspose.com/psd/net/) tam liste için.

### S3: Aspose.PSD için nasıl geçici lisans alabilirim?

 Ziyaret edin[geçici lisans sayfası](https://purchase.aspose.com/temporary-license/) Değerlendirme amacıyla geçici bir lisans almak için Aspose web sitesinde.

### S4: Aspose.PSD desteğini nerede bulabilirim?

 Sorularınız veya yardım için şu adresi ziyaret edin:[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) ve toplulukla bağlantı kurun.

### S5: Aspose.PSD'yi ticari kullanım için satın alabilir miyim?

 Kesinlikle. Keşfedin[satın alma sayfası](https://purchase.aspose.com/buy) İhtiyaçlarınıza uygun bir lisans almak için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
