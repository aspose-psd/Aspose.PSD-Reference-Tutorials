---
title: PSD Dosyalarında İşleme Eğrileri Ayarlama Katmanı - Java
linktitle: PSD Dosyalarında İşleme Eğrileri Ayarlama Katmanı - Java
second_title: Aspose.PSD Java API'si
description: Bu ayrıntılı adım adım kılavuzla Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki Eğri Ayarlama Katmanlarını nasıl oluşturacağınızı ve ayarlayacağınızı öğrenin.
weight: 16
url: /tr/java/psd-layer-management-effects/render-curves-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında İşleme Eğrileri Ayarlama Katmanı - Java

## giriiş

Photoshop'un Eğri Ayarlama Katmanı, görüntüleri geliştirmek için sihirli bir değnek gibidir. Başyapıtınızın renklerinde ve tonlarında ince ayar yapan bir sanatçı olduğunuzu hayal edin; her eğri ayarı, ışık ve renk dengesini inanılmaz bir hassasiyetle kontrol etmenize olanak tanır. PSD dosyalarıyla çalışıyorsanız ve bu eğrileri programlı olarak değiştirmeniz gerekiyorsa, Aspose.PSD for Java başvurulacak aracınızdır. Bu kılavuzda, Aspose.PSD for Java kullanarak PSD dosyalarındaki Eğri Ayarlama Katmanlarının nasıl oluşturulacağını ve ayarlanacağını açıklayacağız. İster görüntü tonlarını güncelliyor ister sonuçlarınızı dışa aktarıyor olun, bu eğitim, başlamak için ihtiyacınız olan her şeyi kapsayacaktır.

## Önkoşullar

Kodlama ayrıntılarına dalmadan önce, her şeyin hazır olduğundan emin olalım. İşte ihtiyacınız olan şey:

1. Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun. Aspose.PSD for Java, Java 8 veya üzerini gerektirir.
   
2.  Aspose.PSD for Java Kütüphanesi: Aspose.PSD for Java kütüphanesini şu adresten indirin:[Aspose sürümler sayfası](https://releases.aspose.com/psd/java/). 

3. IDE (Entegre Geliştirme Ortamı): IntelliJ IDEA veya Eclipse gibi Java uyumlu herhangi bir IDE çalışacaktır.

4. Temel Java Programlama Bilgisi: Java sözdizimini ve temel programlama kavramlarını anlamak, öğreticiyi takip etmenize yardımcı olacaktır.

5. PSD Dosyası: Düzenlemek istediğiniz Eğri Ayarlama Katmanını içeren bir PSD dosyası. 

Bu önkoşulları yerine getirdikten sonra PSD dosyalarınızı değiştirmeye hazırsınız.

## Paketleri İçe Aktar

Başlangıç olarak gerekli paketleri Aspose.PSD'den içe aktarmanız gerekiyor. Bu kütüphaneler, eğriler katmanını okumak ve değiştirmek de dahil olmak üzere PSD dosyası işlemlerini gerçekleştirecektir.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: PSD Dosyasını Yükleyin

 Öncelikle PSD dosyanızı uygulamaya yüklemeniz gerekiyor.`PsdImage` Aspose.PSD'nin sınıfı, PSD dosyalarını açmanıza ve değiştirmenize olanak tanır.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
PsdImage im = (PsdImage)Image.load(sourceFileName + ".psd");
```

 İşte, değiştir`"Your Document Directory/CurvesAdjustmentLayer"` PSD dosyanızın yolu ile birlikte. Bu kod parçacığı PSD dosyasını bir`PsdImage` nesne.

## Adım 2: Katmanlar Arasında Yineleme Yapın

PSD dosyaları birden fazla katman içerebilir. Eğri Ayarlama Katmanını bulmak ve değiştirmek için PSD dosyanızın katmanları arasında yineleme yapmanız gerekir.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof CurvesLayer) {
        CurvesLayer curvesLayer = (CurvesLayer)im.getLayers()[i];
        // Ek işlemler burada gerçekleştirilecek
    }
}
```

Bu döngü, her katmanın bir örnek olup olmadığını belirlemek için kontrol eder.`CurvesLayer`. Eğer öyleyse, eğrileri ayarlamaya devam edebilirsiniz.

## 3. Adım: Eğriler Katmanını Değiştirin

Eğri Ayarlama Katmanını belirledikten sonra ayarlarını değiştirebilirsiniz. Katmanın ayrık veya sürekli bir yönetici kullanmasına bağlı olarak yaklaşım farklılık gösterecektir.

### Ayrık Eğriler Yöneticisini Değiştirme

 Eğer`CurvesLayer` bir kullanır`CurvesDiscreteManager`eğri noktalarını doğrudan ayarlayabilirsiniz.

```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();
    
    for (int k = 10; k < 50; k++) {
        manager.setValueInPosition(0, (byte)k, (byte)(15 + (k * 2)));
    }
}
```

Bu kod parçasında eğri değerlerini ayrı bir şekilde ayarlıyoruz. Bu, değerlerin çeşitli konumlara ayarlanmasını ve eğrinin şeklinin etkili bir şekilde değiştirilmesini içerir.

### Sürekli Eğriler Yöneticisini Değiştirme

 Katmanlar için`CurvesContinuousManager`, eğri noktaları ekleyeceksiniz.

```java
else {
    CurvesContinuousManager manager = (CurvesContinuousManager)curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte)0, (byte)50, (byte)100);
    manager.addCurvePoint((byte)0, (byte)150, (byte)130);
}
```

Bu kod, eğrinin şeklini sürekli değerlerle ayarlayarak iki eğri noktası ekler. 

## Adım 4: PSD Dosyasını Kaydedin

Ayarlamalarınızı yaptıktan sonra değiştirilen PSD dosyasını kaydedin. Bu adım, tüm değişikliklerinizin saklanmasını sağlar.

```java
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
im.save(psdPathAfterChange + ".psd");
```

Burada, değiştirilen PSD dosyasının kaydedileceği yolu belirtirsiniz. 

## Adım 5: PNG'ye aktarın

 Ayarlanan PSD dosyasını PNG olarak dışa aktarmak için`PngOptions` ve dosyayı kaydedin.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
String pngExportPath = dataDir + "CurvesAdjustmentLayerChanged";
im.save(pngExportPath + ".png", saveOptions);
```

Bu kod parçası, alfa şeffaflığına sahip renk türü de dahil olmak üzere PNG dışa aktarma seçeneklerini ayarlar ve dosyayı PNG olarak kaydeder.

## Çözüm

Aspose.PSD for Java kullanarak PSD dosyalarındaki Eğri Ayarlama Katmanlarını değiştirmek ilk başta karmaşık görünebilir, ancak bu adım adım talimatlarla bunu yönetilebilir ve sezgisel bulacaksınız. Bu kılavuzu izleyerek görüntü tonlarında zahmetsizce ince ayar yapabilir ve sonuçlarınızı çeşitli formatlarda dışa aktarabilirsiniz. İster bir proje için görüntüleri geliştiriyor olun, ister toplu işlemleri otomatikleştiriyor olun, Aspose.PSD, profesyonel sonuçlara kolaylıkla ulaşmak için ihtiyaç duyduğunuz araçları sağlar.

## SSS'ler

### Eğri Ayarlama Katmanı nedir?
Photoshop'taki Eğri Ayarlama Katmanı, RGB eğrilerini değiştirerek görüntünün parlaklığını ve kontrastını ayarlamanıza olanak tanır. Ton ayarlamaları üzerinde hassas kontrol sağlar.

### Aspose.PSD for Java'yı diğer görüntü formatlarıyla kullanabilir miyim?
Evet, Aspose.PSD for Java öncelikle PSD dosyaları içindir, ancak düzenlenmiş görsellerinizi PNG, TIFF ve JPEG gibi formatlara aktarabilirsiniz.

### Aspose.PSD for Java'yı kullanabilmek için Photoshop'un yüklü olması gerekiyor mu?
Hayır, Aspose.PSD for Java, Photoshop'tan bağımsız olarak çalışarak PSD dosyalarını programlı olarak değiştirmenize olanak tanır.

### Aspose.PSD for Java'nın ücretsiz deneme sürümünü nasıl edinebilirim?
 Aspose.PSD for Java'nın ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Aspose sürümler sayfası](https://releases.aspose.com/psd/java/).

### Aspose.PSD for Java desteğini nerede bulabilirim?
 Destek için şu adresi ziyaret edebilirsiniz:[Aspose destek forumu](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
