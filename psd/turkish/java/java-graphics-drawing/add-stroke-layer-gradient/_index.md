---
date: 2026-01-14
description: Aspose.PSD for Java kullanarak PSD dosyalarında degrade çizgi katmanı
  oluşturmayı ve çizgi degradelerini özelleştirmeyi bu adım adım öğretici ile öğrenin.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Java'da Gradyan Çizgi Katmanı Nasıl Oluşturulur
url: /tr/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Gradient Stroke Katmanı Nasıl Oluşturulur

## Giriş
Java kullanarak PSD dosyalarınızda **gradient stroke layer** oluşturmayı hiç merak ettiniz mi? Doğru yerdesiniz! Bugün Aspose.PSD for Java'ya dalacağız—PSD dosyalarını zahmetsizce manipüle etmenizi sağlayan güçlü bir kütüphane. Grafik programlamada yeni olun ya da mevcut tasarımları ince ayar yapmak isteyin, bu rehber adım adım stroke gradient'lerini eklemenizi ve özelleştirmenizi gösterecek.

## Hızlı Yanıtlar
- **Ana hedef nedir?** Bir PSD dosyasında gradient stroke katmanı oluşturmak.  
- **Hangi kütüphane gereklidir?** Aspose.PSD for Java.  
- **Lisans gerekir mi?** Evet, üretim için geçerli (veya geçici) bir lisans gereklidir.  
- **Hangi Java sürümü çalışır?** Java 8 ve üzeri.  
- **Uygulama ne kadar sürer?** Temel bir gradient stroke için yaklaşık 10‑15 dakika.

## Gradient Stroke Katmanı Nedir?
Gradient stroke katmanı, bir şekil veya metin etrafında renkler arasında sorunsuz bir geçiş sağlayan vektörel bir konturdur. Aspose.PSD kullanarak renkleri, opaklığı, açıyı ve türü (lineer, radyal vb.) programatik olarak tanımlayabilirsiniz.

## Neden Aspose.PSD for Java Kullanmalı?
- **Tam PSD desteği** – Photoshop olmadan PSD dosyalarını okuma, düzenleme ve yazma.  
- **Zengin efekt API'si** – stroke, gölge, parıltı ve birçok diğer katman efektine erişim.  
- **Çapraz platform** – Java destekleyen herhangi bir işletim sisteminde çalışır.  
- **Yerel bağımlılık yok** – saf Java, CI boru hatlarına entegrasyonu kolay.

## Önkoşullar
1. **Java Development Kit (JDK)** – En son JDK'yı [Oracle'ın web sitesinden](https://www.oracle.com/java/technologies/javase-downloads.html) yükleyin.  
2. **Aspose.PSD for Java** – Kütüphaneyi [Aspose.PSD indirme sayfasından](https://releases.aspose.com/psd/java/) indirin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya NetBeans.  
4. **Lisans** – Tam lisansınız yoksa bir [geçici lisans](https://purchase.aspose.com/temporary-license/) edinin.

## Paketleri İçe Aktarma
İlk olarak, PSD'yi yüklemek, efektlere erişmek ve gradient doldurmaları yapılandırmak için ihtiyaç duyacağımız sınıfları içe aktarın.

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

Şimdi süreci net adımlara ayıralım.

## Adım 1: PSD Dosyasını Yükleyin
Kaynak PSD'yi yükleyip stroke efektinin kullanılabilir olması için efekt kaynaklarını etkinleştiriyoruz.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Adım 2: Stroke Efektine Erişin
Değiştirmek istediğimiz stroke'ın üçüncü katmanda (indeks 2) olduğunu varsayarak `StrokeEffect`'i alıyoruz.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Adım 3: Stroke Efekt Özelliklerini Doğrulayın
Değişiklik yapmadan önce mevcut ayarları kontrol ederek neyi güncelleyeceğimizi kesin olarak belirliyoruz.

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

## Adım 4: Gradient Doldurma Ayarlarını Değiştirin
İstenen görünümü elde etmek için renk, opaklık, karışım modu ve diğer özellikleri burada değiştiriyoruz.

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

## Adım 5: Renk ve Şeffaflık Noktalarını Ekleyin ve Değiştirin
Yeni renk ve şeffaflık noktaları ekliyor, ardından mevcut olanları ayarlayarak gradient'i şekillendiriyoruz.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## Adım 6: Değiştirilen PSD Dosyasını Kaydedin
Tüm ayarlamaları tamamladıktan sonra güncellenmiş dosyayı diske yazıyoruz.

```java
im.save(exportPath);
```

## Adım 7: Değişiklikleri Doğrulayın
Kaydedilen dosyayı yeniden yükleyip her özelliğin uyguladığımız değişiklikleri yansıttığını doğruluyoruz.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
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
// Check transparency points
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

## Sonuç
Artık Aspose.PSD for Java kullanarak PSD dosyalarında **gradient stroke layer** efektleri oluşturmayı biliyorsunuz. Bir PSD'yi yükleyip stroke efektine erişerek gradient doldurma ayarlarını ince ayar yapıp sonucu kaydedebilir, Photoshop açmadan profesyonel kalitede grafikler üretebilirsiniz.

## SSS
### Aspose.PSD for Java nedir?
Aspose.PSD for Java, geliştiricilerin Java uygulamalarında PSD dosyalarıyla çalışmasını sağlayan, PSD dosyalarını oluşturma, manipüle etme ve dönüştürme özellikleri sunan bir kütüphanedir.

### Aspose.PSD for Java kullanmak için lisans gerekir mi?
Evet, Aspose.PSD for Java kullanmak için geçerli bir lisans gerekir. Değerlendirme amaçlı bir [geçici lisans](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

### Aspose.PSD for Java ile sıfırdan PSD dosyaları oluşturabilir miyim?
Kesinlikle! Aspose.PSD for Java, PSD dosyalarını programatik olarak oluşturmak ve manipüle etmek için kapsamlı API'ler sağlar.

### Aspose.PSD for Java kullanarak diğer efektleri uygulamak mümkün mü?
Evet, Aspose.PSD for Java ile gölge, parıltı ve daha fazlası gibi çeşitli efektleri uygulayabilirsiniz.

### Aspose.PSD for Java belgelerini nerede bulabilirim?
Belgeleri [burada](https://reference.aspose.com/psd/java/) bulabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-14  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose