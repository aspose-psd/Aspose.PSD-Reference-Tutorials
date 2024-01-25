---
title: Aspose.PSD for Java'da Desen Efektleri Ekleme
linktitle: Desen Efektleri Ekle
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java ile Java görüntü desenlerinizi zahmetsizce geliştirin. Büyüleyici desen efektleri eklemek için adım adım eğitimimizi izleyin.
type: docs
weight: 12
url: /tr/java/advanced-image-effects/add-pattern-effects/
---
## giriiş

Java geliştirme dünyasında görüntü modellerini geliştirmek yaygın bir görevdir ve Aspose.PSD for Java bunun için sağlam bir çözüm sunar. Bu eğitim, Aspose.PSD'yi kullanarak desen efektleri ekleme sürecinde size rehberlik edecek ve görsellerinizin benzersiz katmanlar ve geliştirmelerle öne çıkmasını sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
-  Aspose.PSD for Java kütüphanesi indirildi ve projenize eklendi. adresinden indirebilirsiniz.[Aspose.PSD web sitesi](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Aspose.PSD ile çalışmak için gerekli paketleri Java projenize aktarın. Java sınıfınızın başına aşağıdaki kodu ekleyin:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## 1. Adım: Görüntüyü Yükleyin

```java
// PSD görüntüsünü yükleyin
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

"YourImagePath" ve "YourExportPath" öğelerini projenizdeki gerçek yollarla değiştirdiğinizden emin olun.

## Adım 2: Desen Kaplama Bilgilerini Çıkarın

```java
// Desen kaplamasıyla ilgili bilgileri çıkarın
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## 3. Adım: Desen Yerleşimi Ayarlarını Değiştirin

```java
// Desen kaplama ayarlarını değiştirin
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## Adım 4: Desen Verilerini Düzenleyin

```java
// Desen verilerini düzenleyin
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## Adım 5: Düzenlenen Resmi Kaydedin

```java
// Düzenlenen resmi kaydedin
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Adım 6: Değişiklikleri Doğrulayın

```java
// Düzenlenen dosyadaki değişiklikleri doğrulayın
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Değişikliklerin başarıyla uygulandığından emin olmak için iddialar ekleyin
```

## Çözüm

Tebrikler! Aspose.PSD for Java'yı kullanarak desen efektlerini nasıl ekleyeceğinizi başarıyla öğrendiniz. Bu güçlü kitaplık, özelleştirilmiş desenlerle görsel olarak çekici görüntüler oluşturmanıza olanak tanıyarak Java tabanlı projeleriniz için sonsuz olanaklar sunar.

## SSS'ler

### S1: Aspose.PSD for Java'yı diğer Java görüntü işleme kütüphaneleriyle birlikte kullanabilir miyim?

Cevap1: Aspose.PSD for Java bağımsız çalışacak şekilde tasarlanmıştır, ancak gerekirse onu diğer Java kitaplıklarıyla entegre edebilirsiniz.

### S2: Aspose.PSD for Java'nın ayrıntılı belgelerini nerede bulabilirim?

 A2: Bkz.[Java belgeleri için Aspose.PSD](https://reference.aspose.com/psd/java/) kapsamlı bilgi için.

### S3: Aspose.PSD for Java'nın ücretsiz deneme sürümü mevcut mu?

 C3: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD for Java desteğini nasıl alabilirim?

 A4: Ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği için veya bir destek planı satın almayı düşünün.

### S5: Aspose.PSD for Java için geçici bir lisans alabilir miyim?

Cevap5: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).