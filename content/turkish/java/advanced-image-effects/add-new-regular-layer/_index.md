---
title: Aspose.PSD for Java ile PSD'ye Yeni Bir Normal Katman Ekleme
linktitle: PSD'ye Yeni Bir Normal Katman Ekleme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java kullanarak PSD dosyalarına nasıl yeni bir normal katman ekleyeceğinizi öğrenin. Kusursuz PSD manipülasyonu için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/java/advanced-image-effects/add-new-regular-layer/
---
## giriiş

Bir PSD dosyasına yeni bir normal katman eklemek için Aspose.PSD for Java'nın kullanımına ilişkin bu kapsamlı eğitime hoş geldiniz. Aspose.PSD, geliştiricilerin PSD dosyalarını verimli bir şekilde yönetmesine ve bunlarla çalışmasına olanak tanıyan güçlü bir Java kitaplığıdır. Bu eğitimde, ayrıntılı adımlar ve kod örnekleri sunarak, PSD dosyasına yeni bir normal katman ekleme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java Geliştirme Ortamı: Sisteminizde bir Java geliştirme ortamının kurulu olduğundan emin olun.
-  Aspose.PSD Kütüphanesi: Aspose.PSD for Java kütüphanesini indirip yükleyin. Kütüphaneyi bulabilirsiniz[Burada](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarın. Bu paketler Aspose.PSD işlevleriyle çalışmak için gereklidir. Java dosyanızın başına aşağıdaki satırları ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Adım 1: PSD Dosyasını Yükleyin

Düzenlemek istediğiniz PSD dosyasını aşağıdaki kodu kullanarak yükleyin:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Adım 2: Veri Dizilerini ve Dikdörtgenleri Hazırlayın

İki int dizisini ve iki Rectangle nesnesini aşağıdaki gibi hazırlayın:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## 3. Adım: Katman Verilerini Başlatın

Veri dizilerini varsayılan değerle başlatın:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Adım 4: Normal Katmanlar Ekleyin

PSD görüntüsüne iki normal katman ekleyin:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Adım 5: PSD ve PNG'yi kaydedin

Değiştirilen PSD'yi ve ek bir PNG dosyasını kaydedin:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Tebrikler! Aspose.PSD for Java'yı kullanarak PSD dosyasına başarıyla yeni bir normal katman eklediniz.

## Çözüm

Bu eğitimde Aspose.PSD for Java kullanarak bir PSD dosyasına yeni bir normal katman ekleme sürecini ele aldık. Bu güçlü kitaplık, PSD işlemlerini basitleştirerek onu Java geliştiricileri için erişilebilir hale getirir. Aspose.PSD'nin tüm potansiyelini keşfetmek için farklı parametreler ve işlevlerle denemeler yapın.

## SSS'ler

### S1: Aspose.PSD Java 8 ile uyumlu mu?

Cevap1: Evet, Aspose.PSD, Java 8 ve sonraki sürümlerini destekler.

### S2: Eklenen katmanlara dönüşüm uygulayabilir miyim?

A2: Kesinlikle! Aspose.PSD, katmanlar için çeşitli dönüştürme seçenekleri sunar.

### S3: Ek Aspose.PSD belgelerini nerede bulabilirim?

 A3: Belgelere başvurabilirsiniz.[Burada](https://reference.aspose.com/psd/java/).

### S4: Aspose.PSD için nasıl geçici lisans alabilirim?

 A4: Ziyaret edin[bu bağlantı](https://purchase.aspose.com/temporary-license/) geçici lisans seçenekleri için.

### S5: Aspose.PSD desteği için herhangi bir topluluk forumu var mı?

 A5: Evet, destek ve tartışmalar bulabilirsiniz.[Burada](https://forum.aspose.com/c/psd/34).