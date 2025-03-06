---
title: Aspose.PSD for Java ile Görüntüyü Orantılı Olarak Yeniden Boyutlandır
linktitle: Görüntüyü Orantılı Olarak Yeniden Boyutlandır
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java uygulamalarınızı geliştirin. Görüntüleri orantılı olarak zahmetsizce yeniden boyutlandırmak için kılavuzumuzu izleyin. Görüntü işleme yeteneklerinizi bugün artırın.
weight: 17
url: /tr/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Görüntüyü Orantılı Olarak Yeniden Boyutlandır

## giriiş

Aspose.PSD for Java kullanarak görüntüleri orantılı olarak yeniden boyutlandırmaya yönelik adım adım kılavuzumuza hoş geldiniz. Java uygulamalarınızı etkili görüntü yeniden boyutlandırma özellikleriyle geliştirmek istiyorsanız doğru yere geldiniz. Bu eğitimde, açık ve özlü adımları kullanarak süreç boyunca size yol göstereceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Java Ortamı: Sisteminizde Java'nın kurulu olduğundan emin olun.
2.  Aspose.PSD Kütüphanesi: Aspose.PSD kütüphanesini indirip yükleyin. Gerekli kaynakları bulabilirsiniz[Burada](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Önkoşullarınızı sıraladıktan sonra gerekli paketleri Java projenize aktarın. Aspose.PSD kütüphanesine projenizde doğru şekilde referans verildiğinden emin olun.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## 1. Adım: Görüntüyü Yükleyin

Yeniden boyutlandırmak istediğiniz görüntüyü Java uygulamanıza yükleyerek başlayın.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Adım 2: Genişliği ve Yüksekliği Belirleyin

Yeniden boyutlandırılan görüntünüzün yeni genişliğini ve yüksekliğini belirleyin. Bu örnekte görseli orijinal boyutlarının yarısına kadar yeniden boyutlandıracağız.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## 3. Adım: Yeniden Boyutlandırılan Resmi Kaydedin

Yeniden boyutlandırılan görüntüyü, format seçeneklerini (bu durumda PNG) belirterek istediğiniz konuma kaydedin.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Ve işte karşınızda! Aspose.PSD for Java'yı kullanarak bir görüntüyü başarıyla orantılı olarak yeniden boyutlandırdınız.

## Çözüm

Bu eğitimde, Java için Aspose.PSD kütüphanesini kullanarak görüntüleri orantılı olarak yeniden boyutlandırmak için gerekli adımları ele aldık. Artık, gelişmiş görüntü işleme için bu işlevselliği Java uygulamalarınıza zahmetsizce entegre edebilirsiniz.

## SSS'ler

### S1: Aspose.PSD tüm görüntü formatlarıyla uyumlu mu?

 Cevap1: Aspose.PSD, PSD, PNG, JPEG ve daha fazlası dahil olmak üzere çeşitli görüntü formatlarını destekler. Kontrol edin[dokümantasyon](https://reference.aspose.com/psd/java/) kapsamlı bir liste için.

### S2: Aspose.PSD'yi ticari projeler için kullanabilir miyim?

 A2: Evet, yapabilirsin. Ziyaret edin[satın alma sayfası](https://purchase.aspose.com/buy) lisans ayrıntıları için.

### S3: Test amaçlı geçici lisanslar mevcut mu?

 Cevap3: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/) değerlendirme için.

### S4: Aspose.PSD desteğini nerede bulabilirim?

 A4: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) Toplumsal destek ve yardım için.

### S5: Aspose.PSD belgelerine nasıl erişebilirim?

 A5: Ayrıntılı belgelere bakın[Burada](https://reference.aspose.com/psd/java/).
'
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
