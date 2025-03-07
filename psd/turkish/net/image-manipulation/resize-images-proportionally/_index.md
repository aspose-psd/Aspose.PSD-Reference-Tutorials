---
title: Aspose.PSD for .NET'te Görüntüleri Orantılı Olarak Yeniden Boyutlandırma
linktitle: Görüntüleri Orantılı Olarak Yeniden Boyutlandırma
second_title: Aspose.PSD .NET API'si
description: Aspose.PSD for .NET ile kusursuz görüntü yeniden boyutlandırmayı keşfedin. Kütüphaneyi indirin, eğitimimizi takip edin ve görüntü işleme yeteneklerinizi geliştirin.
weight: 14
url: /tr/net/image-manipulation/resize-images-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET'te Görüntüleri Orantılı Olarak Yeniden Boyutlandırma

Görüntü manipülasyonu alanında Aspose.PSD for .NET, geliştiricilere görüntüleri orantısal olarak kolaylıkla yeniden boyutlandırma yeteneği sağlayan güçlü bir araç seti olarak öne çıkıyor. Bu adım adım kılavuzda, Aspose.PSD for .NET kullanarak görselleri yeniden boyutlandırma sürecinde size yol göstereceğiz ve görsellerinizin orantılarını kusursuz bir şekilde korumasını sağlayacağız.

## giriiş

Görüntüleri orantılı olarak yeniden boyutlandırmak birçok uygulamada yaygın bir görevdir ve Aspose.PSD for .NET, geliştiriciler için bu süreci basitleştirir. İster bir web uygulaması, masaüstü yazılımı veya mobil uygulama üzerinde çalışıyor olun, en boy oranlarını korurken görüntüleri nasıl yeniden boyutlandıracağınızı anlamak, görsel çekiciliği ve tutarlılığı korumak açısından çok önemlidir.

## Önkoşullar

Aspose.PSD for .NET ile yeniden boyutlandırma büyüsüne dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1.  Aspose.PSD for .NET Library: Aspose.PSD for .NET kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Aspose.PSD for .NET sürümleri](https://releases.aspose.com/psd/net/) sayfa.

2. Belge Dizini: Belgelerinizi saklamak için bir dizin oluşturun ve sağlanan koddaki "Belge Dizininiz" kısmını bu dizine giden gerçek yolla değiştirin.

Artık önkoşulları ayarladığınıza göre, adım adım kılavuza geçelim.

## Ad Alanlarını İçe Aktar

```csharp
using Aspose.PSD.ImageOptions;
```

Gerekli sınıflara ve yöntemlere erişmek için gerekli ad alanlarını içe aktarın.

## 1. Adım: Görüntüyü Yükleyin

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Mevcut bir görüntüyü RasterImage sınıfının bir örneğine yükleme
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Adımların geri kalanı buraya gider
}
```

 Kaynak görüntüyü şunu kullanarak yükleyin:`Image.Load` Yöntem.

## Adım 2: Genişliği ve Yüksekliği Belirleyin

```csharp
// Genişlik ve yüksekliğin belirtilmesi
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Yeniden boyutlandırılan görüntünün yeni genişliğini ve yüksekliğini belirleyin. Bu örnekte genişlik ve yükseklik yarıya indirilmiştir ancak bu değerleri gereksinimlerinize göre ayarlayabilirsiniz.

## 3. Adım: Yeniden Boyutlandırılan Resmi Kaydedin

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Yeniden boyutlandırılan görüntüyü kullanarak kaydedin.`Save` belirtilen seçeneklere sahip yöntem. Bu durumda onu PNG dosyası olarak kaydediyoruz.

## Çözüm

Aspose.PSD for .NET'te görüntüleri orantılı olarak yeniden boyutlandırmak, görüntü işleme iş akışınıza değer katan basit bir işlemdir. Bu kılavuz, bu işlevselliği uygulamalarınıza sorunsuz bir şekilde entegre edebilmeniz için sizi bilgiyle donattı.

## SSS'ler

### S1: Görüntüleri belirli boyutlara göre yeniden boyutlandırabilir miyim?

Cevap1: Evet, yeni genişlik ve yüksekliği koddaki gereksinimlerinize göre özelleştirebilirsiniz.

### S2: Aspose.PSD for .NET, toplu görüntü yeniden boyutlandırmaya uygun mu?

A2: Kesinlikle! Birden fazla görüntüyü toplu olarak işlemek için bu adımları bir döngüye dahil edebilirsiniz.

### S3: Aspose.PSD for .NET'te başka görüntü işleme özellikleri var mı?

Cevap3: Evet, Aspose.PSD for .NET, görüntülere kırpma, döndürme ve filtre uygulama dahil çok çeşitli özellikler sunar.

### S4: Aspose.PSD for .NET'in ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, Aspose.PSD for .NET'in özelliklerini ücretsiz denemeyle keşfedebilirsiniz. Ziyaret etmek[Burada](https://releases.aspose.com/) başlamak için.

### S5: Aspose.PSD for .NET desteğini nerede bulabilirim?

 A5: ziyaret edin[.NET forumu için Aspose.PSD](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
