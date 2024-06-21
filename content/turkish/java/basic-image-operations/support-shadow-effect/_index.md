---
title: Java için Aspose.PSD'de Gölge Efektini Destekleyin
linktitle: Gölge Efektini Destekleyin
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java kullanarak görüntülere büyüleyici gölge efektlerini nasıl ekleyeceğinizi öğrenin. Bu adım adım eğitimle grafik tasarımınızı geliştirin.
type: docs
weight: 13
url: /tr/java/basic-image-operations/support-shadow-effect/
---
## giriiş

Görüntüleri gölge efektleriyle geliştirmek, grafik tasarımda derinlik ve gerçekçilik katan yaygın bir uygulamadır. Aspose.PSD for Java, gölge efektleri için güçlü bir destek sağlayarak geliştiricilerin bu efektleri Java uygulamalarına zahmetsizce entegre etmelerine olanak tanır. Bu eğitimde Aspose.PSD kullanarak gölge efektlerinin nasıl destekleneceğini adım adım inceleyeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java programlamanın temel bilgisi.
-  Aspose.PSD for Java yüklü. İndirebilirsin[Burada](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Java uygulamanızda Aspose.PSD işlevselliklerinden yararlanmak için gerekli paketleri içe aktardığınızdan emin olun. Aşağıdaki kod parçacığını kılavuz olarak kullanın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 1. Adım: PSD Görüntüsünü Yükleyin

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Adım 2: Gölge Efektini Alın

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## 3. Adım: Varsayılan Ayarları Doğrulayın

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## Adım 4: Gölge Efektini Özelleştirin

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Adım 5: Değiştirilen Görüntüyü Kaydedin

```java
im.save(psdPathAfterChange);
```

## Çözüm

Bu basit adımlarla Aspose.PSD for Java'da gölge efektlerini zahmetsizce destekleyerek resimlerinizin görsel çekiciliğini artırabilirsiniz.

## SSS'ler

### S1: Aspose.PSD for Java profesyonel grafik tasarım projelerine uygun mudur?

A1: Kesinlikle! Aspose.PSD for Java, profesyonel grafik tasarım görevleri için tasarlanmış güçlü bir kütüphanedir.

### S2: Aspose.PSD for Java'yı ticari uygulamalarda kullanabilir miyim?

 C2: Evet, Aspose.PSD for Java ticari bir üründür. Satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).

### S3: Ücretsiz deneme sürümü mevcut mu?

 C3: Evet, ücretsiz deneme sürümünü keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S4: Ayrıntılı belgeleri nerede bulabilirim?

 Cevap4: Kapsamlı belgelere bakın[Burada](https://reference.aspose.com/psd/java/).

### S5: Aspose.PSD for Java desteğini nasıl alabilirim?

 A5: Topluluk forumuna katılın.[Burada](https://forum.aspose.com/c/psd/34) herhangi bir destek sorgusu için.