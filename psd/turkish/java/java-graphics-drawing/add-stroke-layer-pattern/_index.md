---
title: Java'da Kontur Katmanı Deseni Nasıl Eklenir
linktitle: Java'da Kontur Katmanı Deseni Nasıl Eklenir
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java kullanarak PSD dosyalarına kontur katmanı desenini nasıl ekleyeceğinizi öğrenin. Resimlerinizi kolayca geliştirmek için bu adım adım kılavuzu izleyin.
type: docs
weight: 11
url: /tr/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## giriiş
Java'da bir görüntüye kontur katmanı deseni eklemek göz korkutucu bir görev gibi görünebilir, ancak Aspose.PSD for Java ile bu düşündüğünüzden daha kolaydır. İster grafik tasarlıyor olun ister fotoğraf düzenleme uygulamaları üzerinde çalışıyor olun, bu kılavuz süreç boyunca size adım adım yol gösterecektir. Başlamaya hazır mısınız? Hadi dalalım!
## Önkoşullar
Başlamadan önce birkaç şeye ihtiyacınız olacak:
- Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun.
-  Aspose.PSD for Java: Kütüphaneyi şu adresten indirin:[Burada](https://releases.aspose.com/psd/java/) ve bunu projenize dahil edin.
- Bir IDE: IntelliJ IDEA veya Eclipse gibi favori Entegre Geliştirme Ortamınızı (IDE) kullanın.
## Paketleri İçe Aktar
Öncelikle gerekli paketleri Java projenize aktarmanız gerekir. Bu paketler Aspose.PSD ile çalışmak için gereklidir.
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
## Adım 1: PSD Dosyasını Yükleyin
Kontur katmanı deseni eklemenin ilk adımı, düzenlemek istediğiniz PSD dosyasını yüklemektir.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Artık PSD dosyasını yükleyerek katmanlarına ve efektlerine erişebilir ve bunları değiştirebilirsiniz.
## Adım 2: Yeni Desen Verilerini Hazırlayın
Daha sonra kontur katmanına uygulayacağınız yeni desen verilerini hazırlamanız gerekiyor.
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
Bu desen verileri yeni kontur efektini oluşturmak için kullanılacaktır.
## 3. Adım: Vuruş Efektine Erişin
Kontur efektini değiştirmek için belirli katmana ve onun karıştırma seçeneklerine erişmeniz gerekir.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Bu, doğru katman ve efektle çalışmanızı sağlar.
## Adım 4: Kontur Efektini Değiştirin
Şimdi kontur efektini yeni desen verileriyle değiştirelim.
### Kontur Efekti Özelliklerini Güncelle
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Kalıp Kaynağını Güncelleyin
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
Bu kod parçacığı, kalıp kaynağını yeni kalıp verileriyle günceller.
## Adım 5: Yeni Deseni Uygulayın
Son olarak yeni deseni kontur efektine uygulayın ve değişiklikleri kaydedin.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Bu, yeni desenin doğru şekilde uygulanmasını ve dosyanın değişikliklerle birlikte kaydedilmesini sağlar.
## Adım 6: Değişiklikleri Doğrulayın
Her şeyin doğru çalıştığından emin olmak için dosyayı tekrar yükleyin ve değişiklikleri doğrulayın.
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
Bu adım, desen verilerinin kontur efektine doğru şekilde uygulandığını doğrular.
## Çözüm
Ve işte karşınızda! Aspose.PSD for Java'yı kullanarak bir PSD dosyasına başarıyla kontur katmanı deseni eklediniz. Bu adımları izleyerek görsellerinizi kolaylıkla özelleştirebilir ve geliştirebilirsiniz. Mutlu kodlama!
## SSS'ler
### Java için Aspose.PSD nedir?
Aspose.PSD for Java, geliştiricilerin PSD (Photoshop Belgesi) dosyalarını programlı olarak oluşturmasına, düzenlemesine ve dönüştürmesine olanak tanıyan bir kitaplıktır.
### Aspose.PSD for Java'yı ticari bir projede kullanabilir miyim?
 Evet ticari projelerde kullanabilirsiniz. adresinden lisans satın alabilirsiniz.[Burada](https://purchase.aspose.com/buy).
### Aspose.PSD for Java'nın ücretsiz deneme sürümü var mı?
 Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).
### Aspose.PSD for Java desteğini nasıl alabilirim?
 Aspose topluluk forumlarından destek alabilirsiniz[Burada](https://forum.aspose.com/c/psd/34).
### Aspose.PSD for Java'nın sistem gereksinimleri nelerdir?
Geliştirme için JDK'nın kurulu olması ve bir IDE'ye ihtiyacınız var. Kütüphane, Windows, Linux ve macOS dahil olmak üzere birden fazla işletim sistemini destekler.