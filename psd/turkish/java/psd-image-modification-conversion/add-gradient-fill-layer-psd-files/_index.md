---
date: 2026-03-23
description: Java kullanarak Aspose.PSD ile degrade doldurmalı PSD dosyaları oluşturmayı
  öğrenin. Bu kılavuz, PSD degrade katmanlarını düzenlemeyi, renkleri, şeffaflığı
  ve diğer özellikleri programlı olarak ayarlamayı gösterir.
linktitle: Create Gradient Fill PSD with Java – Add Gradient Fill Layer
second_title: Aspose.PSD Java API
title: Java ile Gradyan Doldurma PSD Oluştur – Gradyan Doldurma Katmanı Ekle
url: /tr/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile PSD Dosyalarına Gradient Doldurma Katmanı Ekleme

## Giriş

PSD dosyalarınıza ekstra bir görsel sihir dokunuşu eklemek ve **Java ile gradient fill PSD nasıl oluşturulur** diye merak etmek istemez misiniz? Gradientler tasarımlarınıza derinlik katar, ancak bunları manuel olarak ayarlamak zahmetli olabilir. **Aspose.PSD for Java** sayesinde PSD gradientlerini programatik olarak düzenleyebilir, renkleri değiştirebilir, şeffaflığı ayarlayabilir ve her özelliği ince ayar yapabilirsiniz—zaman kazanır ve onlarca dosya arasında tutarlılığı sağlarsınız.

## Hızlı Yanıtlar
- **Java’da PSD gradientlerini düzenlemenizi sağlayan kütüphane nedir?** Aspose.PSD for Java.  
- **Bir PSD dosyasını yükleyen yöntem hangisidir?** `Image.load(path)`.  
- **Gradient açısını nasıl değiştirirsiniz?** `settings.setAngle(double)`.  
- **Yeni renk noktaları ekleyebilir misiniz?** Evet—`GradientColorPoint` nesneleri oluşturup renk noktaları listesine ekleyin.  
- **Üretim kullanımında lisansa ihtiyacınız var mı?** Ticari bir lisans gereklidir; değerlendirme için ücretsiz bir deneme sürümü mevcuttur.

## “create gradient fill PSD” nedir?
Gradient doldurma PSD oluşturmak, bir Photoshop belgesi içinde programatik olarak gradient tabanlı bir doldurma katmanı eklemek veya değiştirmek anlamına gelir. Bu, Photoshop’u açmadan otomatik stil verme, toplu işleme ve dinamik görüntü oluşturma imkanı sağlar.

## PSD gradientlerini düzenlemek için Aspose.PSD neden kullanılmalı?
- **Tam .PSD desteği** – akıllı nesneler dahil tüm katman tipleriyle çalışır.  
- **Photoshop gerekmez** – herhangi bir sunucu ya da CI boru hattında çalıştırabilirsiniz.  
- **İnce ayar kontrolü** – açı, ofsetler, dithering, renk noktaları ve şeffaflık noktalarını temiz bir Java API’si üzerinden ayarlayabilirsiniz.  

## Önkoşullar

İlerlemeye başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

- Java Development Kit (JDK):  Java kodunu çalıştırmak için stabil bir JDK sürümü gerekir. Oracle web sitesinden indirebilirsiniz: [Link to Oracle JDK download page]
- Aspose.PSD for Java: Bu güçlü kütüphane, Java uygulamalarınızda PSD dosyalarıyla çalışmanızı sağlar. Aspose web sitesinden indirin: [Link to Aspose.PSD for Java download] (Değerlendirme için ücretsiz deneme sürümü mevcut)

## Paketleri İçe Aktarma

PSD dosyalarıyla çalışmak için gerekli Aspose.PSD paketlerini içe aktararak başlayalım:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

Bu içe aktarmalar, PSD dosyalarını yükleme, manipüle etme ve kaydetme sınıfları ve yöntemlerine erişim sağlar.

Şimdi gradient doldurma katmanlarını değiştirme macerasına hazır olun!

## Java ile Gradient Doldurma PSD'si Nasıl Oluşturulur

### Adım 1: PSD Dosyasını Yükleyin

İlk olarak, değiştirmek istediğiniz gradient doldurma katmanını içeren PSD dosyasını yüklememiz gerekiyor. Dosya yolunu belirterek `Image.load` yöntemini kullanın:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

Bu kod parçacığı, belirtilen dizinden PSD dosyasını yükler ve `image` değişkenine atar.

### Adım 2: Gradient Doldurma Katmanını Belirleyin

PSD dosyalarında çok sayıda katman bulunabilir. Düzenlemek istediğimiz gradient doldurma katmanını izole etmemiz gerekir. `image.getLayers()` dizisi üzerinde dolaşarak istenen katmanı bulun:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Further checks and modifications will happen here
   break;
}
}
```

Bu döngü her katmanı kontrol eder. Bir katman `FillLayer` ise, `FillLayer` tipine dönüştürülür ve sonraki işlemler için `fillLayer` değişkenine atanır. Hedef katmanı tanımlamak için (örneğin katman adı) ek kontroller ekleyebilirsiniz.

### Adım 3: Gradient Doldurma Türünü Doğrulayın

Tüm doldurma katmanları gradient kullanmaz. Bu kod parçacığı, belirlenen katmanın gerçekten bir gradient doldurma içerip içermediğini doğrular:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

`getFillType` yöntemi `FillType.Gradient` döndürmezse, yanlış katmanla çalıştığımıza dair bir istisna fırlatılır.

## Aspose.PSD Kullanarak PSD Gradientini Düzenleme

### Adım 4: Gradient Özelliklerine Erişin ve Değiştirin

İşte sihir burada gerçekleşiyor! Aspose.PSD, `IGradientFillSettings` arayüzü aracılığıyla çeşitli gradient doldurma özelliklerine erişim sağlar. İhtiyacınıza göre bu özellikleri alıp değiştirebilirsiniz:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modify properties (replace with desired values)
settings.setAngle(0.0);  // Set angle to 0 degrees
settings.setDither(false);  // Disable dithering
settings.setAlignWithLayer(true); // Align gradient with layer
settings.setReverse(true);  // Reverse gradient direction
settings.setHorizontalOffset(25);  // Set horizontal offset
settings.setVerticalOffset(-15);  // Set vertical offset
```

Bu kod, `IGradientFillSettings` nesnesini alır ve açı, dithering, hizalama ve ofset gibi özellikleri değiştirir. İstediğiniz gradient etkisini elde etmek için verilen değerleri kendi ayarlarınızla değiştirin.

### Adım 5: Renk ve Şeffaflık Noktalarını Manipüle Edin

Gradientler, spektrum boyunca renk ve şeffaflık noktalarıyla tanımlanır. Aspose.PSD, bu noktaları hassas kontrol için değiştirmenize olanak tanır:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Add a new color point
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modify an existing color point
colorPoints.get(1).setLocation(3000);

// Add a new transparency point
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modify an existing transparency point
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

### Adım 6: PSD Dosyasını Güncelleyin ve Kaydedin

Gerekli değişiklikleri yaptıktan sonra doldurma katmanını güncelleyin ve PSD dosyasını kaydedin:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

`fillLayer.update()` yöntemi gradient doldurma katmanına yapılan değişiklikleri uygular, `image.save` ise değiştirilmiş PSD dosyasını belirtilen çıkış yoluna kaydeder.

## Yaygın Sorunlar ve Çözümler

- **“Wrong Fill Layer” istisnası** – Gerçekten bir gradient kullanan bir `FillLayer` hedeflediğinizden emin olun. Katman adını veya indeksini kontrol edip dönüştürmeden önce doğrulayın.  
- **Renk noktaları değişiklikleri yansımıyor** – Noktalar listesini değiştirdikten sonra her zaman `settings.setColorPoints(...)` ve `settings.setTransparencyPoints(...)` çağırarak güncellemeleri katmana geri gönderin.  
- **Büyük PSD'lerde performans** – Çok sayıda dosya işliyorsanız aynı `PsdOptions` örneğini yeniden kullanın ve `image.dispose()` ile görüntüleri hızlıca kapatarak belleği serbest bırakın.

## Sık Sorulan Sorular

**S: Gradient'e birden fazla renk ve şeffaflık noktası ekleyebilir miyim?**  
C: Kesinlikle! İstediğiniz kadar renk ve şeffaflık noktası ekleyerek istediğiniz gradient etkisini elde edebilirsiniz. Yeni noktalar oluşturup ilgili listelere ekleyin.

**S: Gradient'ten bir renk veya şeffaflık noktasını nasıl kaldırırım?**  
C: Listenin `remove` metodunu kullanın, örneğin `colorPoints.remove(index)`, istenmeyen noktayı silin ve ardından `setColorPoints` çağırın.

**S: Gradient tipini (linear, radial vb.) değiştirebilir miyim?**  
C: Aspose.PSD şu anda lineer gradientleri desteklemektedir. Gelecek sürümlerde daha fazla tip eklenebilir, ancak renk ve şeffaflık noktalarını manipüle ederek diğer efektleri taklit edebilirsiniz.

**S: Gradientleri değiştirirken performans etkisi olur mu?**  
C: Etki, gradientin karmaşıklığı ve yapılan değişiklik sayısına bağlıdır. Çoğu senaryoda ek yük minimaldir, ancak büyük dosyaların toplu işlenmesi bellek yönetimi ayarlarıyla iyileştirilebilir.

**S: Bir PSD dosyasındaki birden fazla gradient doldurma katmanına bu tekniği uygulayabilir miyim?**  
C: Evet. `image.getLayers()` üzerinden döngü kurun, her `FillLayer` için `FillType.Gradient` kontrolü yapın ve aynı değişiklikleri uygulayın.

**S: Üretim kullanımında ticari bir lisansa ihtiyacım var mı?**  
C: Üretim dağıtımları için geçerli bir Aspose.PSD lisansı gereklidir. Değerlendirme amaçlı ücretsiz bir deneme sürümü mevcuttur.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Son Güncelleme:** 2026-03-23  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11 (en son)  
**Yazar:** Aspose