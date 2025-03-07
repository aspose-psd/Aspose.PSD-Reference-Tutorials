---
title: Ton Doygunluğu Ayarlama Katmanını PSD'ye ekleyin
linktitle: Ton Doygunluğu Ayarlama Katmanını PSD'ye ekleyin
second_title: Aspose.PSD Java API'si
description: Bu kapsamlı, adım adım eğitimde Aspose.PSD for Java kullanarak PSD'ye renk doygunluğu ayarlama katmanlarını nasıl ekleyeceğinizi öğrenin. Grafik tasarım iş akışınızı geliştirin.
weight: 14
url: /tr/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ton Doygunluğu Ayarlama Katmanını PSD'ye ekleyin

## giriiş
Grafik tasarım söz konusu olduğunda, renk manipülasyonu çok önemli bir rol oynar; özellikle renk tonu, doygunluk ve açıklığın ayarlanması, herhangi bir görüntünün ruh halini ve kalitesini büyük ölçüde değiştirebilir. Bunu başarmanın etkili bir yolu Photoshop'taki (PSD dosyaları) ayarlama katmanlarının kullanılmasıdır. PSD dosyalarınızı Java kullanarak programlı olarak geliştirmek istiyorsanız Aspose.PSD kütüphanesi size yardımcı olmak için burada! Bu eğitim, PSD dosyalarınıza Ton Doygunluğu Ayarlama Katmanı ekleme adımlarını size gösterecek ve iş akışlarınızı daha üretken ve verimli hale getirecektir.
Bu kılavuzda gerekli paketlerin içe aktarılmasından kod örneklerinin en ince ayrıntılarına kadar her şeyi ele alacağız.
## Önkoşullar
Koda geçmeden önce aşağıdakilerin mevcut olduğundan emin olun:
1.  Java Geliştirme Kiti (JDK): Makinenizde JDK 8 veya üstünün kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Java SE Geliştirme Seti İndirmeleri](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library: Aspose.PSD kütüphanesine sahip olmanız gerekir.[buradan indir](https://releases.aspose.com/psd/java/). 
3. IDE: Java geliştirme için IntelliJ IDEA veya Eclipse gibi uygun bir Entegre Geliştirme Ortamı (IDE).
4. Temel Java Bilgisi: Java programlamaya aşina olmak bir artıdır ancak endişelenmeyin; Kodu size adım adım anlatacağız.
Artık önkoşullarımızı sıraladığımıza göre işin eğlenceli kısmına geçelim: kodlama!
## Paketleri İçe Aktar
Aspose.PSD kütüphanesiyle çalışmaya başlamak için ilk adım gerekli sınıfları içe aktarmaktır. Bunu Java dosyanızda şu şekilde yapabilirsiniz:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Bu içe aktarma işlemlerinin sorunsuz çalışması için projenize uygun kitaplıkların eklendiğinden emin olun.
## 1. Adım: Belge Dizininizi Kurun
Her projenin bir başlangıç noktasına ihtiyacı vardır ve bizimki de bir istisna değildir. PSD dosyalarınızın saklandığı dizini belirtmeniz gerekir. Bu, görüntülerin düzgün bir şekilde yüklenmesi ve kaydedilmesi için çok önemlidir.
```java
String dataDir = "Your Document Directory"; // Bu yolu gerçek dizininize güncelleyin
```
## Adım 2: Mevcut Bir PSD Dosyasını Yükleyin
Mevcut bir PSD dosyasını değiştirmek için öncelikle onu programımıza yüklememiz gerekir. Bunu nasıl yapabileceğiniz aşağıda açıklanmıştır:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Bu kodda güncelleme`"HueSaturationAdjustmentLayer.psd"` düzenlemek istediğiniz mevcut PSD dosyanızın adına.
## 3. Adım: Ton/Doygunluk Katmanını Düzenleyin
Daha sonra, mevcut Ton/Doygunluk katmanlarını bulmak ve düzenlemek için yüklü PSD görüntümüzün katmanları arasında dolaşacağız. Bu adım, renk tonu, doygunluk ve açıklık değerlerinin değiştirilmesini içerir.
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
- Ton'u -25'e, doygunluğu -12'ye ve açıklığı +67'ye ayarlıyoruz.
- `getRange(2)` yöntemi, belirli renk aralıklarını istediğimiz gibi ayarlamamıza olanak tanır.
## Adım 4: Değiştirilen PSD Dosyasını Kaydedin
Ayarlamaları yaptıktan sonraki adım dosyayı kaydetmektir. Bu, yaptığımız değişikliklerin kaybolmamasını sağlayan sürecimizin hayati bir parçasıdır.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Adım 5: Yeni Bir Ton/Doygunluk Katmanı Ekleyin
Daha sonra başka bir PSD dosyasına yeni bir Ton/Doygunluk ayarlama katmanı eklemek isteyebilirsiniz. Daha önce kullandığınız yaklaşımın aynısını farklı PSD dosyalarıyla uygulayın.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Adım 6: Yeni Katman için Yeni Ton/Doygunluk Değerlerini Ayarlayın
Artık bu yeni katmanı oluşturduğunuza göre istediğiniz renk tonu, doygunluk ve açıklık ayarlarını daha önce olduğu gibi uygulayın.
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
Son olarak, değişikliklerinizi görebilmeniz için PSD dosyasını eklenen Ton/Doygunluk katmanıyla birlikte kaydedin.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Tebrikler! Aspose.PSD for Java'yı kullanarak PSD dosyalarını başarıyla değiştirdiniz. Artık farklı görseller ve daha derin değişiklikler deneyerek grafik tasarım projelerinizi hayata geçirebilirsiniz.
## Çözüm
Grafiklerle programlı olarak çalışmak bir olasılıklar dünyasının kapılarını açar. Ton Doygunluğu Ayarlama Katmanlarını eklemek ve değiştirmek için Aspose.PSD for Java'yı kullanmak, tasarım iş akışınızı kolaylaştırabilecek esneklik ve verimlilik sağlar. İster bir proje için fotoğrafları geliştiriyor olun ister çarpıcı görsel içerik oluşturuyor olun, bu araçlarda uzmanlaşmak çıktılarınızı büyük ölçüde geliştirebilir.
 Aspose.PSD'nin diğer işlevlerini keşfetmekten çekinmeyin[dokümantasyon](https://reference.aspose.com/psd/java/) ya da takılmayı düşün[geçici lisans](https://purchase.aspose.com/temporary-license/) Kütüphanenin tam gücünü test etmek için.
## SSS'ler
### Ton Doygunluğu Ayarlama Katmanı nedir?
Ton Doygunluğu Ayarlama Katmanı, orijinal pikselleri kalıcı olarak değiştirmeden bir görüntünün renk özelliklerini değiştirmenize olanak tanır.
### Aspose.PSD'yi kullanabilmek için Photoshop'un yüklü olması gerekiyor mu?
Hayır, Aspose.PSD, Photoshop'tan bağımsız çalışan bağımsız bir kütüphanedir.
### Toplu işlemler için Aspose.PSD'yi kullanabilir miyim?
Evet, Aspose.PSD ile birden fazla PSD dosyasını otomatikleştirebilir ve toplu işleyebilirsiniz.
### Aspose.PSD ücretsiz mi?
Aspose.PSD ücretsiz deneme sürümü sunuyor ancak uzun süreli kullanım için lisans gerekiyor. Fiyatlandırmayı görüntüleyebilirsiniz[Burada](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
