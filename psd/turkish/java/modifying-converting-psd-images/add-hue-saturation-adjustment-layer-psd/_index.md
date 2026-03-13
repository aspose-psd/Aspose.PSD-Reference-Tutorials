---
date: 2026-03-13
description: Aspose.PSD for Java kullanarak PSD dosyalarına renk tonu ve doygunluk
  katmanı eklemeyi öğrenin. Bu kılavuz ayrıca PSD dosyalarını toplu işleme ve renk
  tonu ayar katmanını programlı olarak oluşturmayı gösterir.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile PSD'ye Hue Saturation Katmanı Ekle
url: /tr/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'ye Hue Saturation Katmanı Ekle

## Giriş
Grafik tasarımda renk manipülasyonu kritik bir rol oynar—özellikle hue, saturation ve lightness değerlerini ayarlamak, bir görüntünün atmosferini ve kalitesini köklü bir şekilde değiştirebilir. Bunu başarmanın etkili bir yolu, Photoshop (PSD dosyaları) içinde ayar katmanları kullanmaktır. Java ile **hue saturation katmanı eklemek** istiyorsanız, Aspose.PSD kütüphanesi tam da bu iş için burada! Bu öğreticide, PSD dosyalarınıza Hue Saturation Adjustment Layer eklemek için gereken adımları adım adım gösterecek ve iş akışınızı daha üretken ve verimli hâle getireceğiz.

## Hızlı Yanıtlar
- **Java'da hue saturation katmanı eklemenizi sağlayan kütüphane hangisidir?** Aspose.PSD for Java.  
- **Photoshop yüklü olması gerekiyor mu?** Hayır, kütüphane Photoshop'tan bağımsız çalışır.  
- **Bu yöntemle PSD dosyalarını toplu işleyebilir miyim?** Evet—adımları otomatikleştirdikten sonra birçok dosyaya aynı işlemi uygulayabilirsiniz.  
- **Hangi Java sürümü gereklidir?** JDK 8 veya üzeri.  
- **Üretim kullanımında lisans gerekli mi?** Evet, deneme süresi sonrasında ticari bir lisans gereklidir.

## “add hue saturation layer” işlemi nedir?
Bir **add hue saturation layer** işlemi, orijinal piksel verilerini değiştirmeden hue, saturation ve lightness değerlerini düzenlemenizi sağlayan yıkıcı olmayan bir ayar katmanı oluşturur. Bu, tüm kompozisyon ya da belirli renk aralıkları üzerinde renkleri ince ayar yapmak için idealdir.

## Neden Aspose.PSD for Java?
- **Photoshop bağımlılığı yok** – Java çalıştırabilen herhangi bir platformda çalışır.  
- **Tam PSD bütünlüğü** – tüm katman bilgilerini, maskeleri ve efektleri korur.  
- **Toplu işleme hazır** – klasörlerdeki dosyaları döngüyle işleyerek aynı ayarı onlarca dosyaya uygulayabilirsiniz.  
- **Performansa odaklı** – büyük belgeler ve sunucu‑tarafı otomasyon için optimize edilmiştir.

## Önkoşullar
Kodlamaya geçmeden önce aşağıdakilerin hazır olduğundan emin olun:

1. **Java Development Kit (JDK):** Makinenizde JDK 8 veya üzeri yüklü olmalı. [Java SE Development Kit İndirmeleri](https://www.oracle.com/java/technologies/javase-downloads.html) adresinden indirebilirsiniz.  
2. **Aspose.PSD for Java Library:** Aspose.PSD kütüphanesine ihtiyacınız var; bunu [buradan indirebilirsiniz](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA veya Eclipse gibi bir Entegre Geliştirme Ortamı (IDE).  
4. **Temel Java Bilgisi:** Java programlamaya aşina olmak faydalı, ancak endişelenmeyin—her satırı birlikte inceleyeceğiz.

Şimdi önkoşullarımız hazır, hadi eğlenceli bölüme—kodlamaya—geçelim!

## Paketleri İçe Aktarma
Aspose.PSD kütüphanesiyle çalışmaya başlamak için gerekli sınıfları içe aktarmanız gerekir. Java dosyanızda bunu şu şekilde yapabilirsiniz:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Bu importların sorunsuz çalışması için projenize uygun kütüphaneleri eklediğinizden emin olun.

## Adım 1: Belge Dizinini Ayarlayın
Her projenin bir başlangıç noktası gerekir, bizimki de istisna değil. PSD dosyalarınızın bulunduğu dizini belirtmeniz gerekir. Bu, görüntüleri doğru şekilde yükleyip kaydetmek için kritiktir.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Adım 2: Mevcut Bir PSD Dosyasını Yükleyin
Var olan bir PSD dosyasını manipüle edebilmek için önce programınıza yüklemeniz gerekir. İşte bunu yapmanın yolu:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Bu kodda `"HueSaturationAdjustmentLayer.psd"` ifadesini düzenleyerek, üzerinde değişiklik yapmak istediğiniz mevcut PSD dosyasının adını girin.

## Adım 3: Hue/Saturation Katmanını Düzenleyin
Yüklediğimiz PSD görüntüsünün katmanları arasında dolaşarak mevcut Hue/Saturation katmanlarını bulup düzenleyeceğiz. Bu adım hue, saturation ve lightness değerlerini değiştirmeyi içerir.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

Bu örnekte:  
- Hue değerini **-25**, saturation değerini **-12**, lightness değerini ise **+67** olarak ayarlıyoruz.  
- `getRange(2)` metodu, istediğiniz spesifik renk aralıklarını ayarlamanıza olanak tanır.

## Adım 4: Değiştirilmiş PSD Dosyasını Kaydedin
Ayarlamaları yaptıktan sonra dosyayı kaydetmek bir sonraki adımdır. Bu, yaptığınız değişikliklerin kaybolmamasını sağlar.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Adım 5: Yeni Bir Hue/Saturation Katmanı Ekleyin
Sıfırdan **hue adjustment layer** oluşturmanız gerekiyorsa, başka bir PSD dosyasına tamamen yeni bir Hue/Saturation ayar katmanı ekleyebilirsiniz. Aynı yükleme desenini izleyin, ancak `addHueSaturationAdjustmentLayer()` metodunu kullanın.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Adım 6: Yeni Katman İçin Hue/Saturation Değerlerini Belirleyin
Bu yeni katmanı oluşturduğunuza göre, istediğiniz hue, saturation ve lightness ayarlarını önceki gibi uygulayın.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Adım 7: Güncellenmiş PSD Dosyasını Kaydedin
Eklenmiş Hue/Saturation katmanı ile PSD dosyasını kaydedin, böylece değişikliklerinizi görebilirsiniz.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Tebrikler! Aspose.PSD for Java kullanarak PSD dosyalarını başarıyla manipüle ettiniz. Şimdi farklı görüntüler ve daha derin değişikliklerle deneyler yapabilir, grafik tasarım projelerinizi hayata geçirebilirsiniz.

## Hue ayarlarıyla PSD dosyalarını toplu işleme nasıl yapılır
Yukarıdaki kod tamamen scriptlenebilir olduğundan, bir klasördeki her `.psd` dosyasını döngüyle işleyen bir yapı oluşturabilirsiniz. Bu sayede **psd dosyalarını toplu işleyebilir** ve aynı hue, saturation ve lightness ayarlarını tek bir çalıştırmada uygulayabilirsiniz—büyük ölçekli marka güncellemeleri için mükemmeldir.

## Yaygın Sorunlar ve Çözümler
- **Dosya yüklenirken NullPointerException:** `dataDir` değişkeninin uygun dosya ayırıcı (`/` veya `\`) ile bittiğinden ve dosya adının doğru olduğundan emin olun.  
- **Ayarlama değerleri aralık dışı:** Hue, saturation ve lightness değerleri -255 ile 255 arasında olmalıdır. Sayılarınızı bu aralıkta tutun.  
- **Katman bulunamadı:** PSD dosyasında Hue/Saturation katmanı yoksa, `instanceof` kontrolü bloğu atlanır. Önce `addHueSaturationAdjustmentLayer()` ile bir katman oluşturun.

## Sık Sorulan Sorular

**S: Hue Saturation Adjustment Layer nedir?**  
C: Görüntünün renk özelliklerini orijinal pikselleri kalıcı olarak değiştirmeden düzenlemenizi sağlar.

**S: Aspose.PSD kullanmak için Photoshop yüklü olması gerekiyor mu?**  
C: Hayır, Aspose.PSD bağımsız bir kütüphane olup Photoshop'tan bağımsız çalışır.

**S: Aspose.PSD ile toplu işleme yapabilir miyim?**  
C: Evet, Aspose.PSD ile birden fazla PSD dosyasını otomatikleştirip toplu işleyebilirsiniz.

**S: Aspose.PSD ücretsiz mi?**  
C: Aspose.PSD ücretsiz bir deneme sunar, ancak uzun vadeli kullanım için lisans gereklidir. Fiyatlandırmayı [buradan](https://purchase.aspose.com/buy) inceleyebilirsiniz.

## Sonuç
Grafikleri programatik olarak işlemek, yeni olasılıkların kapılarını açar. Aspose.PSD for Java ile **hue saturation katmanı eklemek** ve **hue adjustment layer oluşturmak**, tasarım iş akışınızı esnek ve verimli hâle getirir. Projelerinizde fotoğrafları iyileştirmek ya da çarpıcı görsel içerikler üretmek isterken, bu araçları ustalıkla kullanmak çıktılarınızı büyük ölçüde artıracaktır.

Daha fazla Aspose.PSD işlevselliğini keşfetmek için [belgelere](https://reference.aspose.com/psd/java/) göz atabilir veya kütüphanenin tam gücünü test etmek amacıyla bir [geçici lisans](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-03-13  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose