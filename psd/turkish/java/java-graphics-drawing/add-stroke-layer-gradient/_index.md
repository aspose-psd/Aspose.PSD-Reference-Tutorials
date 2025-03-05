---
title: Java'da Kontur Katmanı Gradyanı Nasıl Eklenir
linktitle: Java'da Kontur Katmanı Gradyanı Nasıl Eklenir
second_title: Aspose.PSD Java API'si
description: Bu kapsamlı adım adım eğitimle Aspose.PSD for Java kullanarak PSD dosyalarına kontur katmanı degradelerini nasıl ekleyeceğinizi ve özelleştireceğinizi öğrenin.
type: docs
weight: 10
url: /tr/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## giriiş
Java kullanarak resimlerinize nasıl kontur katmanı degradesi ekleyeceğinizi hiç merak ettiniz mi? Peki, doğru yerdesiniz! Bugün, PSD dosyalarını kolaylıkla değiştirmenize yardımcı olan güçlü bir kütüphane olan Aspose.PSD for Java dünyasına dalıyoruz. İster yeni başlayan ister deneyimli bir geliştirici olun, bu adım adım kılavuz, PSD dosyalarınıza kontur katmanı degradesi ekleme sürecinde size yol gösterecektir. O halde kemerlerinizi bağlayın ve grafik düzenleme becerilerinizi geliştirmeye hazırlanın!
## Önkoşullar
Başlamadan önce, yerinde olması gereken birkaç şey var. Aşağıdakilere sahip olduğunuzdan emin olun:
1.  Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Oracle'ın web sitesi](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library: Buradan indirebilirsiniz.[Aspose.PSD indirme sayfası](https://releases.aspose.com/psd/java/).
3. Entegre Geliştirme Ortamı (IDE): IntelliJ IDEA, Eclipse veya NetBeans gibi herhangi bir IDE çalışacaktır.
4.  Geçerli bir lisans: Alabilirsiniz[geçici lisans](https://purchase.aspose.com/temporary-license/) eğer tam bir tane yoksa.
## Paketleri İçe Aktar
Öncelikle gerekli paketleri import edelim. Bunlar, PSD dosyasını işlemek için gereken sınıfları ve yöntemleri kullanmamızı sağlayacaktır.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
Şimdi daha iyi anlamak için örneği birden fazla adıma ayıralım.
## Adım 1: PSD Dosyasını Yükleyin
 Öncelikle değiştirmek istediğimiz PSD dosyasını yüklememiz gerekiyor. biz kullanacağız`PsdLoadOptions` efekt kaynaklarını yüklemek istediğimizi belirtmek için.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Adım 2: Vuruş Efektine Erişim
Daha sonra ilgilendiğimiz katmanın kontur efektine erişmemiz gerekiyor. Burada bunun PSD dosyasındaki üçüncü katman (indeks 2) olduğunu varsayıyoruz.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## 3. Adım: Kontur Efekti Özelliklerini Doğrulayın
Herhangi bir değişiklik yapmadan önce, doğru ayarları değiştirdiğimizden emin olmak için kontur efektinin özelliklerini doğrulayalım.
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
## 4. Adım: Degrade Dolgu Ayarlarını Değiştirin
Artık degrade dolgu ayarlarını gereksinimlerimize göre değiştirme zamanı geldi. Rengi, opaklığı, karışım modunu ve diğer özellikleri değiştireceğiz.
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
## 5. Adım: Renk ve Saydamlık Noktalarını Ekleme ve Değiştirme
İstediğiniz degrade efektini elde etmek için yeni renk ve şeffaflık noktaları ekleyelim ve mevcut olanları değiştirelim.
```java
// Yeni renk noktası ekle
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Önceki noktanın konumunu değiştir
fillSettings.getColorPoints()[1].setLocation(1899);
// Yeni şeffaflık noktası ekle
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Önceki şeffaflık noktasının konumunu değiştir
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Adım 6: Değiştirilen PSD Dosyasını Kaydedin
Gerekli tüm değişiklikleri yaptıktan sonra PSD dosyasını kaydetmemiz gerekiyor.
```java
im.save(exportPath);
```
## Adım 7: Değişiklikleri Doğrulayın
Son olarak kayıtlı PSD dosyasını yükleyelim ve değişikliklerimizin doğru şekilde uygulandığını doğrulayalım.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Renk noktalarını kontrol edin
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Şeffaflık noktalarını kontrol edin
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## Çözüm
Ve işte karşınızda! Artık Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki kontur katmanı degradelerini nasıl ekleyeceğinizi ve değiştireceğinizi biliyorsunuz. Bu eğitim, PSD dosyasının yüklenmesini, kontur efektlerine erişmeyi ve bunları değiştirmeyi ve değişiklikleri kaydetmeyi kapsıyordu. Bu becerilerle görsel olarak çekici degradeler oluşturabilir ve PSD dosyalarınızı ihtiyaçlarınıza göre özelleştirebilirsiniz.
## SSS'ler
### Java için Aspose.PSD nedir?
Aspose.PSD for Java, geliştiricilerin Java uygulamalarında PSD dosyalarıyla çalışmasına olanak tanıyan, PSD dosyalarını oluşturma, işleme ve dönüştürme özellikleri sunan bir kütüphanedir.
### Aspose.PSD for Java'yı kullanmak için lisansa ihtiyacım var mı?
 Evet, Aspose.PSD for Java'yı kullanmak için geçerli bir lisansa ihtiyacınız var. Alabilirsin[geçici lisans](https://purchase.aspose.com/temporary-license/) değerlendirme amaçlı.
### Sıfırdan PSD dosyaları oluşturmak için Aspose.PSD for Java'yı kullanabilir miyim?
Kesinlikle! Aspose.PSD for Java, PSD dosyalarını programlı olarak oluşturmak ve yönetmek için kapsamlı API'ler sağlar.
### Aspose.PSD for Java kullanarak başka efektler uygulamak mümkün mü?
Evet, Aspose.PSD for Java'yı kullanarak gölge, parlaklık ve daha fazlası gibi çeşitli efektleri uygulayabilirsiniz.
### Aspose.PSD for Java belgelerini nerede bulabilirim?
 Belgeleri bulabilirsiniz[Burada](https://reference.aspose.com/psd/java/).