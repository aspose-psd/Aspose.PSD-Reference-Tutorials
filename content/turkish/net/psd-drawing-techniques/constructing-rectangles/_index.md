---
title: Aspose.PSD for .NET'te Dikdörtgenler Oluşturma
linktitle: Dikdörtgenler Oluşturma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD ile .NET'te dikdörtgen çizme sanatını keşfedin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin. Görüntü işleme oyununuzu zahmetsizce yükseltin.
type: docs
weight: 15
url: /tr/net/psd-drawing-techniques/constructing-rectangles/
---
## giriiş

.NET geliştirmenin dinamik alanında Aspose.PSD, görüntü manipülasyonunu yönetmek için güçlü bir araç olarak öne çıkıyor. Bu eğitim temel bir göreve odaklanıyor: Aspose.PSD for .NET kullanarak dikdörtgenler oluşturmak. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu adım adım kılavuz süreç boyunca size yol gösterecek ve her konsepti iyice kavramanızı sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Ortam Kurulumu: Aspose.PSD entegreli, çalışan bir .NET geliştirme ortamına sahip olun. Henüz yapmadıysanız, bkz.[dokümantasyon](https://reference.aspose.com/psd/net/) Kurulum talimatları için.

-  Aspose.PSD'yi İndirin: Aspose.PSD kitaplığını şu adresten indirdiğinizden emin olun:[İndirme: {link](https://releases.aspose.com/psd/net/).

-  Lisans Alın: Aspose.PSD'yi üretim ortamında kullanıyorsanız geçerli bir lisansınız olduğundan emin olun. Bir tane alabilirsiniz[Burada](https://purchase.aspose.com/buy) veya bir kullanın[geçici lisans](https://purchase.aspose.com/temporary-license/) test için.

## Ad Alanlarını İçe Aktar

Gerekli ad alanlarını .NET projenize aktararak başlayın. Bu ad alanları dikdörtgen çizmek için gereken Aspose.PSD işlevselliğine erişim sağlar.

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## 1. Adım: Belge Dizinini Başlatın

Çıktı görüntüsünün kaydedileceği belge dizininizin yolunu ayarlayın.

```csharp
string dataDir = "Your Document Directory";
```

## Adım 2: Dikdörtgen Çizimi

Şimdi Aspose.PSD kullanarak dikdörtgen çizme sürecine bakalım.

### Adım 2.1: BmpOptions Örneğini Oluşturun

```csharp
string outpath = dataDir + "Rectangle.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

### Adım 2.2: Bir Görüntü Örneği Oluşturun

```csharp
using (Image image = new PsdImage(100, 100))
{
    // Adım 2.3: Grafik Sınıfını Başlatın ve Grafik Yüzeyini Temizleyin
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);

    // Adım 2.4: Dikdörtgenler Çizin
    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Adım 2.5: Görüntüyü BMP Dosya Formatına Aktarın
    image.Save(outpath, saveOptions);
}
```

## Çözüm

Tebrikler! Aspose.PSD for .NET'i kullanarak başarıyla dikdörtgenler oluşturdunuz. Bu eğitim sizi görüntü işlemeyi .NET uygulamalarınıza sorunsuz bir şekilde entegre etme bilgisiyle donattı.

## SSS'ler

### S1: Aspose.PSD tüm .NET ortamlarıyla uyumlu mudur?

C1: Evet, Aspose.PSD, çeşitli .NET ortamlarıyla çalışacak ve farklı platformlar arasında uyumluluk sağlayacak şekilde tasarlanmıştır.

### S2: Aspose.PSD'yi ticari projeler için lisanssız kullanabilir miyim?

Cevap2: Hayır, ticari kullanım için geçerli bir lisans gereklidir. Lisansınızı alın[Burada](https://purchase.aspose.com/buy).

### S3: Aspose.PSD ile nasıl yardım isteyebilirim veya deneyimlerimi paylaşabilirim?

 A3: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) toplulukla bağlantı kurmak ve yardım almak için.

### S4: BmpOptions'ta piksel başına 32 bit (Bpp) ne gibi avantajlar sunuyor?

Cevap4: 32 Bpp'nin kullanılması daha zengin renk temsiline olanak tanıyarak daha ayrıntılı ve canlı görüntüler sağlar.

### S5: Aspose.PSD'nin ücretsiz deneme sürümü mevcut mu?

 Cevap5: Evet, Aspose.PSD'yi ücretsiz deneme sürümüyle keşfedebilirsiniz. İndir[Burada](https://releases.aspose.com/).