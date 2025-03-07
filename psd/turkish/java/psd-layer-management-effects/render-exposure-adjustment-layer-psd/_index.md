---
title: PSD Dosyalarında Pozlama Ayarlama Katmanını Oluşturma - Java
linktitle: PSD Dosyalarında Pozlama Ayarlama Katmanını Oluşturma - Java
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki pozlama katmanlarını nasıl oluşturacağınızı ve ayarlayacağınızı öğrenin. Pozlama katmanlarını değiştirmek ve eklemek için kod örnekleri içeren adım adım kılavuz.
weight: 15
url: /tr/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında Pozlama Ayarlama Katmanını Oluşturma - Java

## giriiş

Photoshop PSD dosyalarıyla mı çalışıyorsunuz ve pozlamayı ayarlamanız veya programlı olarak bir poz ayarlama katmanı eklemeniz mi gerekiyor? İster mevcut katmanlarda ince ayarlar yapıyor ister yenilerini ekliyor olun, Aspose.PSD for Java bu görevleri yerine getirmeniz için güçlü ve sezgisel bir yol sunar. Bu kılavuzda, PSD dosyalarındaki pozlama ayarlama katmanlarını oluşturmak ve değiştirmek için Aspose.PSD for Java'nın nasıl kullanılacağını açıklayacağız. Bu eğitimin sonunda, mevcut katmanlardaki pozlama ayarlarını nasıl ayarlayacağınızı ve PSD dosyalarınıza yeni pozlama ayarlama katmanlarını nasıl ekleyeceğinizi öğreneceksiniz. Hadi dalalım!

## Önkoşullar

Eğiticiye geçmeden önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Java Development Kit (JDK): Makinenizde JDK'nın kurulu olması gerekmektedir. Bu kılavuzda en az JDK 8'e sahip olduğunuz varsayılmaktadır.
2.  Aspose.PSD for Java: PSD dosyalarıyla çalışmak için Aspose.PSD kütüphanesine ihtiyacınız var. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/psd/java/).
3. Temel Java Bilgisi: Java programlamaya aşinalık, kolayca ilerlemenize yardımcı olacaktır.
4. IDE veya Metin Düzenleyici: Java kodunu yazmak ve çalıştırmak için IntelliJ IDEA, Eclipse gibi herhangi bir IDE'yi veya seçtiğiniz bir metin düzenleyiciyi kullanın.

## Paketleri İçe Aktar

Öncelikle Aspose.PSD for Java'dan gerekli paketleri içe aktaralım. Bu adım, kodumuzun PSD dosyalarını işlemek için kitaplığın özelliklerini kullanabilmesini sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: PSD Dosyasını Yükleyin

Başlamak için PSD dosyanızı uygulamaya yüklemeniz gerekir. Bunu nasıl yapabileceğiniz aşağıda açıklanmıştır:

```java
String dataDir = "Your Document Directory";  // Belge dizininizi tanımlayın
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Kaynak PSD dosya yolu

PsdImage im = (PsdImage) Image.load(sourceFileName);  // PSD dosyasını yükleyin
```

 Bu kod parçacığında değiştirin`"Your Document Directory"` PSD dosyalarınızın bulunduğu yolla.`Image.load()` yöntem PSD dosyasını bir örneğine yükler`PsdImage`, katmanlarını değiştirmenize olanak tanır.

## Adım 2: Mevcut Pozlama Ayarlama Katmanını Düzenleyin

PSD dosyası yüklendikten sonra mevcut katmanlara erişebilir ve bunları değiştirebilirsiniz. Dosya bir pozlama ayarlama katmanı içeriyorsa özelliklerini ayarlayabilirsiniz:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Pozlama düzeyini ayarlayın
        expLayer.setOffset(-0.25f);  // Ofseti ayarlayın
        expLayer.setGammaCorrection(0.5f);  // Gama düzeltmesini ayarlayın
    }
}
```

Bu döngüde PSD dosyasının tüm katmanlarını yineliyoruz. Eğer bir tane bulursak`ExposureLayer` , onu değiştiriyoruz`Exposure`, `Offset` , Ve`GammaCorrection` özellikler. Bu, pozlama ayarlama katmanının görsel çıktısına ince ayar yapmanızı sağlar.

## Adım 3: Değiştirilen PSD Dosyasını Kaydedin

Değişiklik yaptıktan sonra güncellenen PSD dosyasını kaydetmeniz gerekir:

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Değiştirilen PSD dosyasını kaydetme yolu

im.save(psdPathAfterChange);  // Değişiklikleri PSD dosyasına kaydedin
```

Bu satır, değiştirilen PSD dosyasını belirtilen yola kaydederek pozlama ayarlarınızı korur.

## Adım 4: PNG olarak dışa aktarın

Güncellenen PSD dosyasını PNG olarak dışa aktarmak için şu adımları izleyin:

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // PNG dosyasını kaydetme yolu

PngOptions saveOptions = new PngOptions();  // PNG seçenekleri oluşturun
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Renk türünü Alpha ile Truecolor olarak ayarlayın

im.save(pngExportPath, saveOptions);  // PNG olarak kaydet
```

 Burada,`PngOptions` PNG dışa aktarma ayarlarını yapılandırmak için kullanılır.`PngColorType.TruecolorWithAlpha` PNG dosyasının renk derinliğini ve şeffaflığını korumasını sağlar.

## Adım 5: Yeni Pozlama Ayarlama Katmanı Ekleme

Mevcut bir PSD dosyasına yeni bir pozlama ayarlama katmanı eklemek istiyorsanız bunu aşağıdaki kodla yapabilirsiniz:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Kaynak PSD dosya yolu

PsdImage img = (PsdImage) Image.load(sourceFileName);  // PSD dosyasını yükleyin

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Yeni pozlama ayarlama katmanı ekle

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Değiştirilen PSD dosyasını kaydetme yolu
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // PNG dosyasını kaydetme yolu

img.save(psdPathAfterChange);  // Değişiklikleri PSD dosyasına kaydedin

PngOptions options = new PngOptions();  // PNG seçenekleri oluşturun
options.setColorType(PngColorType.TruecolorWithAlpha);  // Renk türünü Alpha ile Truecolor olarak ayarlayın

img.save(pngExportPath, options);  // PNG olarak kaydet
```

Bu adımda, PSD dosyasına belirtilen pozlama, ofset ve gama düzeltme değerlerine sahip yeni bir pozlama ayarlama katmanı eklenir. Güncellenen PSD ve PNG dosyaları daha sonra kaydedilir.

## Çözüm

Ve işte karşınızda! Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki pozlama katmanlarını nasıl oluşturacağınızı ve ayarlayacağınızı öğrendiniz. Mevcut pozlama katmanlarını nasıl değiştireceğinizi, yenilerini nasıl ekleyeceğinizi ve çalışmanızı PNG dosyaları olarak nasıl dışa aktaracağınızı ele aldık. İster fotoğraflarda ince ayarlar yapıyor ister tasarım varlıkları hazırlıyor olun, bu beceriler PSD dosyalarını programlı olarak yönetme yeteneğinizi geliştirecektir. Mutlu kodlama!

## SSS'ler

### Java için Aspose.PSD nedir?

Aspose.PSD for Java, Java kullanarak PSD dosyalarını programlı olarak oluşturmanıza, düzenlemenize ve dönüştürmenize olanak tanıyan bir kitaplıktır. Photoshop belgeleriyle çalışmak için kapsamlı işlevsellik sağlar.

### Aspose.PSD for Java'yı diğer katman türlerini işlemek için kullanabilir miyim?

Evet, Aspose.PSD for Java, metin katmanları, ayarlama katmanları ve görüntü katmanları da dahil olmak üzere çeşitli katman türlerini destekler ve PSD dosyalarının kapsamlı şekilde değiştirilmesine olanak tanır.

### Aspose.PSD for Java'yı nasıl kullanmaya başlarım?

 Kütüphaneyi indirerek başlayabilirsiniz.[web sitesi](https://releases.aspose.com/psd/java/) ve buna atıfta bulunarak[dokümantasyon](https://reference.aspose.com/psd/java/) ayrıntılı kılavuzlar ve örnekler için.

### Aspose.PSD for Java'nın ücretsiz deneme sürümü var mı?

 Evet, ücretsiz deneme mevcuttur. İndirebilirsin[Burada](https://releases.aspose.com/).

### Aspose.PSD for Java desteğini nasıl alabilirim?

 Destek için şu adresi ziyaret edebilirsiniz:[Aspose destek forumu](https://forum.aspose.com/c/psd/34) soru sorabileceğiniz ve topluluktan yardım alabileceğiniz yer.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
