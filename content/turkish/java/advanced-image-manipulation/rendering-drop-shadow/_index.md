---
title: Aspose.PSD for Java'da Rendering Drop Shadow'u uygulayın
linktitle: Oluşturma Alt Gölgesini Uygula
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'da görüntü işleme alt gölgelerini uygulamaya yönelik adım adım kılavuzu keşfedin ve görüntü işleme becerilerinizi zahmetsizce geliştirin.
type: docs
weight: 16
url: /tr/java/advanced-image-manipulation/rendering-drop-shadow/
---
## giriiş

Java ile görüntü işlemeye başlıyorsanız, Aspose.PSD, PSD dosyalarının sorunsuz ve verimli şekilde işlenmesi için başvuracağınız araçtır. Bu eğitimde Aspose.PSD for Java kullanarak alt gölge oluşturma sürecini inceleyeceğiz. Sizin için adımları sıralarken kemerlerinizi bağlayın.

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java Geliştirme Ortamı: Makinenizde Java'nın kurulu olduğundan emin olun.
- Aspose.PSD Kütüphanesi: Aspose.PSD kütüphanesini indirin ve kurun. Kütüphaneyi bulabilirsiniz[Burada](https://releases.aspose.com/psd/java/).
- PSD Dosyası: Alt gölgeyi uygulamak istediğiniz katmanı içeren bir PSD dosyası hazırlayın.

## Paketleri İçe Aktar

Gerekli paketleri içe aktararak işe başlayalım. Bu adım, kodun sorunsuz bir şekilde yürütülmesi için gerekli araçların elinizin altında olmasını sağlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

Şimdi her adımı ayrı ayrı ele alalım.

## 1. Adım: Belge Dizinini Tanımlayın

PSD dosyanızın bulunduğu dizini belirterek başlayın.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: PSD ve PNG Dosya Yollarını Ayarlayın

Kaynak PSD dosyanızın ve hedef PNG dosyasının yollarını tanımlayın.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

## Adım 3: Efektli PSD Dosyasını Yükleyin

Efekt kaynaklarının yüklenmesini etkinleştirerek PSD dosyasını yükleyin.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Adım 4: Alt Gölge Efektine Erişim

Belirtilen katmandan alt gölge efektini alın.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Adım 5: Gölge Efekti Özelliklerini Doğrulayın

Alt gölge efekti özelliklerinin beklentilerinizi karşıladığından emin olun.

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

## Adım 6: PNG olarak kaydedin

Değiştirilen görüntüyü PNG dosyası olarak kaydedin.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Ve işte karşınızda: Aspose.PSD for Java'da görüntü oluşturma alt gölgelerini uygulamaya yönelik adım adım kılavuz.

## Çözüm

Aspose.PSD ile Java'da görüntü manipülasyonunda uzmanlaşmak çocuk oyuncağı haline geliyor. Alt gölgeleri oluşturmanın sırlarını çözdünüz ve yaratıcı olasılıklarla dolu bir dünyanın kapısını araladınız.

## SSS'ler

### S1: Alt gölgeleri aynı anda birden çok katmana uygulayabilir miyim?

Cevap1: Evet, katmanlar arasında geçiş yapabilir ve gerektiği gibi alt gölgeler uygulayabilirsiniz.

### S2: Alt gölgelerde 'Yayılma' parametresinin önemi nedir?

Cevap2: 'Yayılma' parametresi, gölgeli ve gölgesiz alanlar arasındaki geçişi kontrol eder.

### S3: Aspose.PSD, Photoshop dosyalarının tüm sürümleriyle uyumlu mudur?

Cevap3: Aspose.PSD, çok çeşitli PSD dosya sürümleriyle uyumluluk sağlayarak çok yönlülük sağlar.

### S4: Aspose.PSD ile ilgili sorunları nasıl bildirebilirim veya yardım isteyebilirim?

 A4: Şuraya gidin:[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) kapsamlı destek için.

### S5: Satın almadan önce Aspose.PSD'yi test edebilir miyim?

 A5: Kesinlikle, kullanın[ücretsiz deneme](https://releases.aspose.com/) Bir satın alma işlemine başlamadan önce yetenekleri keşfetmek.