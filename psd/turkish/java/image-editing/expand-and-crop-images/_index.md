---
title: Aspose.PSD for Java ile Görüntüleri Genişletin ve Kırpın
linktitle: Görüntüleri Genişletin ve Kırpın
second_title: Aspose.PSD Java API'si
description: Aspose.PSD'yi kullanarak Java'da görüntüleri nasıl genişleteceğinizi ve kırpacağınızı öğrenin. Verimli görüntü işleme için adım adım kılavuz.
type: docs
weight: 18
url: /tr/java/image-editing/expand-and-crop-images/
---
## giriiş

Bu eğitimde, görüntüleri verimli bir şekilde genişletmek ve kırpmak için Aspose.PSD for Java'nın nasıl kullanılacağını keşfedeceğiz. Aspose.PSD, Java uygulamalarında PSD dosyalarıyla çalışmak için çok çeşitli özellikler sunan güçlü bir kütüphanedir. Bu kılavuzda gerekli önkoşulları, paketleri içe aktarmayı ele alacağız ve her adımı ayrıntılı açıklamalarla ele alacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Java Geliştirme Ortamı: Sisteminizde Java'nın kurulu olduğundan emin olun.

2.  Aspose.PSD Kütüphanesi: Aspose.PSD kütüphanesini indirip yükleyin. Kütüphaneyi bulabilirsiniz[Burada](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Artık önkoşullarınızı sıraladığınıza göre Aspose.PSD for Java ile çalışmaya başlamak için gerekli paketleri içe aktarın. Java kodunuza aşağıdaki satırları ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Bu paketler Aspose.PSD kullanılarak görüntü işleme için gerekli sınıfları ve yöntemleri sağlar.

## 1. Adım: Belge Dizininizi Ayarlayın

PSD dosyanızın bulunduğu dizini ayarlayarak başlayın. "Belge Dizininiz"i gerçek yolla değiştirin.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Kaynak ve Hedef Yollarını Belirleyin

Çıkış görüntüsü için kaynak PSD dosyasını ve hedef yolunu tanımlayın.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## 3. Adım: Görüntüyü Yükleyin ve Önbelleğe Alın

 PSD dosyasını bir`RasterImage` nesnesini oluşturun ve verilerini önbelleğe alın.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Adım 4: Kırpma için Dikdörtgen Oluşturun

 Bir örnek oluştur`Rectangle` nesneyi seçin ve X, Y koordinatlarını, genişliğini ve yüksekliğini tanımlayın. Bu dikdörtgen kırpılan bölgeyi belirleyecektir.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

## Adım 5: Kırpılan Resmi Kaydedin

 Kırpılan görüntüyü tanımlanmış dikdörtgeni ve`JpegOptions` sınıf.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

Tebrikler! Aspose.PSD for Java'yı kullanarak bir görüntüyü başarılı bir şekilde genişletip kırptınız.

## Çözüm

Bu eğitimde Aspose.PSD for Java kütüphanesini kullanarak görüntüleri genişletme ve kırpma sürecini inceledik. Aspose.PSD, güçlü özellikleriyle görüntü işleme görevlerini basitleştirerek onu Java geliştiricileri için mükemmel bir seçim haline getiriyor.

## SSS'ler

### S1: Aspose.PSD farklı Java sürümleriyle uyumlu mu?

Cevap1: Evet, Aspose.PSD çeşitli Java sürümlerini destekleyerek çok çeşitli geliştirme ortamlarıyla uyumluluk sağlar.

### S2: Aspose.PSD'yi ticari projeler için kullanabilir miyim?

Cevap2: Aspose.PSD kesinlikle geliştiricilere ticari lisanslar sağlayarak hem kişisel hem de ticari projelerde kullanılmasına olanak tanıyor.

### S3: Desteklenen resim dosyası formatlarında herhangi bir sınırlama var mı?

 Cevap3: Aspose.PSD, PSD, JPEG, PNG ve daha fazlası dahil olmak üzere çeşitli görüntü dosyası formatlarını destekler. Şuraya bakın:[dokümantasyon](https://reference.aspose.com/psd/java/) tam bir liste için.

### S4: Aspose.PSD ile ilgili sorgular için nasıl destek alabilirim?

 A4: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluktan veya Aspose destek ekibinden yardım istemek için.

### S5: Ücretsiz deneme sürümü var mı?

 Cevap5: Evet, Aspose.PSD'yi ücretsiz deneme sürümüyle keşfedebilirsiniz. İndir[Burada](https://releases.aspose.com/).