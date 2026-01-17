---
date: 2026-01-17
description: Aspose.PSD for Java ile Java’da çizgi deseni eklemeyi öğrenin. PSD görüntülerinizi
  hızlıca geliştirmek için bu adım adım rehberi izleyin.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Aspose.PSD Kullanarak Java'da Çizgi Deseni Nasıl Eklenir
url: /tr/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Kullanarak Java'da Çizgi Deseni Ekleme

## Giriş
Bir Photoshop dosyasına **çizgi deseni java** eklemeniz gerekiyorsa, Aspose.PSD for Java bunu şaşırtıcı derecede basit hale getirir. Grafik‑tasarım aracı geliştiriyor, toplu düzenlemeleri otomatikleştiriyor ya da sadece katman efektleriyle deneme yapıyor olun, bu öğretici PSD'yi yüklemeden yeni deseni doğrulamaya kadar her adımı size gösterir. Hadi başlayalım ve görüntülerinizi ne kadar hızlı geliştirebileceğinizi görelim.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java  
- **Hangi Java sürümü destekleniyor?** JDK 8 ve üzeri  
- **Test için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme yeterlidir; üretim için lisans gereklidir  
- **Uygulama ne kadar sürer?** Temel bir desen çizgisi için yaklaşık 10‑15 dakika  
- **Deseni birden fazla katmanda yeniden kullanabilir miyim?** Evet, aynı `PattResource`'u diğer katmanlara atamanız yeterlidir  

## add stroke pattern java nedir?
Java’da bir çizgi desenini eklemek, bir katmanın çizgi etkisine özel bir dolgu (genellikle tekrarlayan bir bitmap) uygulamak anlamına gelir. Bu teknik, kesikli bir çizgi, tuğla dokusu ya da özel bir grafik kenarlık gibi stilize hatlar oluşturmanıza olanak tanır; Photoshop açmadan doğrudan bir PSD dosyası içinde gerçekleşir.

## Aspose.PSD ile add stroke pattern java neden tercih edilmeli?
- **Tam PSD bütünlüğü** – Tüm katman efektleri, kaynaklar ve karışım modları korunur.  
- **Yerel Photoshop gerekmez** – JDK yüklü herhangi bir işletim sisteminde çalışır.  
- **Programatik kontrol** – Toplu işleme otomasyonu ya da sunucu‑tarafı hizmetlere entegrasyon sağlar.  
- **Zengin API** – Global kaynaklara, desen dolguya ve karışım modlarına tek bir akıcı arabirimle erişim.

## Önkoşullar
- **Java Development Kit (JDK)** – JDK 8 ve üzeri yüklü olduğundan emin olun.  
- **Aspose.PSD for Java** – Kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirin ve JAR dosyasını projenizin classpath'ine ekleyin.  
- **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.

## Paketleri İçe Aktarma
PSD dosyalarını, renkleri, dikdörtgenleri ve çizgi efektlerini işlemek için ihtiyaç duyacağınız sınıfları içe aktarın.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## Adım 1: PSD Dosyasını Yükleme
Kaynak PSD'yi yükleyin, böylece katmanları ve kaynakları üzerinde çalışabilirsiniz.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Adım 2: Yeni Desen Verisini Hazırlama
Çizgi için kullanılacak basit bir 4 × 4 piksel desen oluşturun.

```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```

## Adım 3: Çizgi Efektine Erişim
Hedef katmanda (bu örnekte dördüncü katman) çizgi efektini bulun.

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Adım 4: Çizgi Efektini Değiştirme
### Çizgi Efekti Özelliklerini Güncelleme
Yeni desenin görsel etkisini görmek için opaklığı ve karışım modunu ayarlayın.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Desen Kaynağını Güncelleme
Mevcut global desen kaynağını az önce oluşturduğunuzla değiştirin.

```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```

## Adım 5: Yeni Deseni Uygulama
Güncellenen desen kaynağını çizgi efektine bağlayın ve PSD'yi kaydedin.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Adım 6: Değişiklikleri Doğrulama
Dosyayı yeniden yükleyin ve yeni desenin, opaklığın ve karışım modunun doğru şekilde uygulandığını doğrulayın.

```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```

## Yaygın Sorunlar ve Çözümler
| Sorun | Neden | Çözüm |
|-------|-------|-----|
| Desen görünmüyor | Yanlış `PatternId` referansı | `PattResource` üzerindeki `PatternId` değerinin `PatternFillSettings` içinde kullanılanla aynı olduğundan emin olun. |
| Kaydettiğinizde çizgi kayboluyor | Opaklık 0 olarak ayarlanmış veya efekt gizli | `setOpacity` değerinin 0‑255 arasında olduğundan ve `isVisible()` metodunun `true` döndürdüğünden emin olun. |
| Beklenmedik renkler | Karışım modu uyumsuzluğu | Tasarım amacınıza uygun `BlendMode.Color` (veya başka bir mod) kullanın. |

## SSS
### Aspose.PSD for Java nedir?
Aspose.PSD for Java, geliştiricilerin PSD (Photoshop Document) dosyalarını programatik olarak oluşturmasına, düzenlemesine ve dönüştürmesine olanak tanıyan bir kütüphanedir.

### Aspose.PSD for Java'yi ticari bir projede kullanabilir miyim?
Evet, ticari projelerde kullanabilirsiniz. Lisansı [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

### Aspose.PSD for Java için ücretsiz bir deneme mevcut mu?
Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

### Aspose.PSD for Java için destek nasıl alınır?
Aspose topluluk forumlarından [burada](https://forum.aspose.com/c/psd/34) destek alabilirsiniz.

### Aspose.PSD for Java için sistem gereksinimleri nelerdir?
JDK yüklü olmalı ve geliştirme için bir IDE bulunmalıdır. Kütüphane Windows, Linux ve macOS dahil olmak üzere birden fazla işletim sistemini destekler.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-17  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose