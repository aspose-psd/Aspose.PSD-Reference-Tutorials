---
title: Aspose.PSD for Java'da Görüntü Döndürme
linktitle: Bir Görüntüyü Döndürme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java'da görüntü döndürmeyi zahmetsizce keşfedin. PSD dosyalarını kolayca döndürün, çevirin ve kaydedin.
type: docs
weight: 19
url: /tr/java/advanced-image-manipulation/rotate-image/
---
## giriiş

Aspose.PSD for Java, görüntülerle çalışmak için güçlü bir dizi özellik sunarak geliştiricilerin PSD dosyalarını verimli bir şekilde yönetmesine ve işlemesine olanak tanır. Bu eğitimde belirli bir göreve odaklanacağız: bir görüntüyü döndürme. İster bir fotoğraf düzenleme uygulaması oluşturuyor olun ister yalnızca bir görüntünün yönünü ayarlamanız gerekiyor olsun, Aspose.PSD süreci kolaylaştırır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.PSD for Java Library: Aspose.PSD for Java kütüphanesini indirip yüklediğinizden emin olun. Kütüphaneyi ve ayrıntılı belgeleri bulabilirsiniz.[Burada](https://reference.aspose.com/psd/java/).

- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

-  Örnek PSD Dosyası: Döndürmek istediğiniz örnek bir PSD dosyası hazırlayın. Ayarlayın`sourceFile` örnek koddaki değişkeni PSD dosyanızın yolu ile birlikte kullanın.

## Paketleri İçe Aktar

Aspose.PSD'nin özelliklerinden yararlanmak için gerekli paketleri içe aktararak başlayın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 1. Adım: Görüntüyü Yükleyin

 Mevcut görüntüyü bir örneğine yükleyin`Image` sınıf:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Adım 2: Görüntüyü Döndürün

 kullanarak görüntüyü döndürün.`rotateFlip` Yöntem. Bu örnekte görüntüyü 270 derece döndürüyoruz:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 3. Adım: Döndürülmüş Görüntüyü Kaydetme

 Döndürülmüş görüntüyü kullanarak kaydedin.`save` yöntemi ve çıktı biçimini belirtme (bu durumda JPEG):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Çözüm

Tebrikler! Aspose.PSD for Java'yı kullanarak bir görüntüyü başarıyla döndürdünüz. Bu basit ama güçlü kitaplık, Java uygulamalarınızda görüntü işleme için birçok olasılıklar dünyasının kapılarını açar.

## SSS'ler

### S1: Aspose.PSD farklı görüntü formatlarıyla uyumlu mudur?

Cevap1: Evet, Aspose.PSD, PSD, JPEG, PNG ve daha fazlası dahil olmak üzere çeşitli görüntü formatlarını destekler.

### S2: Yalnızca önceden tanımlanmış döndürmelerin yanı sıra özel döndürmeler de uygulayabilir miyim?

A2: Kesinlikle! Aspose.PSD, özel gereksinimlerinizi karşılamak için özel rotasyonlar uygulama esnekliği sağlar.

### S3: Nerede ek destek veya yardım bulabilirim?

 C3: Her türlü soru veya sorun için şu adresi ziyaret edin:[Aspose.PSD Forumu](https://forum.aspose.com/c/psd/34) topluluk desteği için.

### S4: Ücretsiz deneme sürümü mevcut mu?

 C4: Evet, Aspose.PSD'yi bir[ücretsiz deneme](https://releases.aspose.com/).

### S5: Geçici lisansı nasıl edinebilirim?

 Cevap5: Geçici bir lisansa ihtiyacınız varsa bir tane alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).