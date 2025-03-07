---
title: Java kullanarak PSD'ye Eğri Ayarlama Katmanı ekleme
linktitle: Java kullanarak PSD'ye Eğri Ayarlama Katmanı ekleme
second_title: Aspose.PSD Java API'si
description: Bu ayrıntılı eğitimde Aspose.PSD for Java kullanarak bir PSD dosyasına Eğri Ayarlama katmanını nasıl ekleyeceğinizi öğrenin. Resimlerinizi kolayca geliştirin.
weight: 11
url: /tr/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java kullanarak PSD'ye Eğri Ayarlama Katmanı ekleme

## giriiş
PSD formatındaki görselleri değiştirmeye çalışırken kendinizi hiç sıkışmış halde buldunuz mu? İster yeni yetişen bir grafik tasarımcı, ister deneyimli bir profesyonel olun, Photoshop dosyalarıyla çalışmak bazen bir labirentte gezinmek gibi gelebilir. Neyse ki bu süreci kolaylaştıran bir araç var: Aspose.PSD for Java. Bu eğitimde Aspose.PSD kullanarak bir PSD dosyasına Eğri Ayarlama katmanını nasıl ekleyeceğinizi inceleyerek görüntü düzenleme görevlerinizi daha kolay ve verimli hale getireceğiz. Adım adım rehberlikle, geleneksel olarak görüntü manipülasyonuyla ilişkilendirilen karmaşıklıklara takılıp kalmadan, görüntülerinizi bir profesyonel gibi geliştirebileceksiniz.
## Önkoşullar
Koda dalmadan önce, her şeyin hazır olduğundan emin olalım. İhtiyacınız olan önkoşullar şunlardır:
1. Java Geliştirme Kiti (JDK): Bilgisayarınızda JDK'nın kurulu olması gerekir. En iyi uyumluluk için en son sürüm olduğundan emin olun.
2. Aspose.PSD for Java Library: PSD dosyalarını yönetmek için Aspose.PSD kütüphanesini indirip projenize eklemeniz gerekir. Onu yakalayabilirsin[Burada](https://releases.aspose.com/psd/java/).
3. Bir IDE: Kodunuzu yazmak için IntelliJ IDEA, Eclipse gibi herhangi bir Java IDE'yi veya hatta basit bir metin düzenleyiciyi kullanın.
4. Temel Java Anlayışı: Java programlamaya aşinalık, sorunsuz bir şekilde ilerlemenize yardımcı olacaktır.
Herşeyi aldın mı? Mükemmel! Gelelim işin eğlenceli kısmına.
## Paketleri İçe Aktarma
Öncelikle gerekli paketleri içe aktarmanız gerekir. İşte bunu nasıl yapacağınız:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
```
Bu paketleri içe aktararak, Java uygulamanıza PSD dosyalarını işlemek ve özellikle Eğri Ayarlama katmanlarıyla çalışmak için ihtiyaç duyduğu sınıfları anlatmış olursunuz.
Artık her şeyi ayarladığımıza göre kodu parçalara ayıralım ve adım adım Eğri Ayarlama katmanını nasıl ekleyeceğimizi görelim.
## 1. Adım: Veri Dizininizi Tanımlayın
İlk adım, PSD dosyalarınızın nerede saklanacağını belirlemektir. Her şeyi düzenli tutmak için bir dizin ayarlayın.
```java
String dataDir = "Your Document Directory"; // Bu yolu güncelle
```
 Düşün`dataDir`çalışma alanınız olarak; tüm sihrin gerçekleştiği yer burası! Değiştirdiğinizden emin olun`Your Document Directory` PSD dosyalarınızın bulunduğu veya bulunacağı asıl yolla.
## Adım 2: PSD Dosyanızı Yükleyin
Daha sonra düzenlemek istediğiniz PSD dosyasını yüklemeniz gerekecektir. Bu, aşağıdaki kod kullanılarak yapılır:
```java
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
```
 Bu kod parçacığında,`sourceFileName` orijinal PSD dosyasını işaret ederken`psdPathAfterChange` değiştirilen dosyanızı kaydedeceğiniz yerdir. Eklemeyi unutmayın`.psd` daha sonra kodda.
## Adım 3: Katmanlar Üzerinde Yineleme Yapın
Artık PSD dosyanızın katmanlarını incelemenin zamanı geldi. Eğri Ayarlama katmanlarını bulmak için her katmanda döngü yapacağız.
```java
for (int j = 1; j < 2; j++) {
    String fileName = sourceFileName + ".psd";
    PsdImage im = (PsdImage) Image.load(fileName);
    
    for(int k = 0; k < im.getLayers().length; k++) {
        if (im.getLayers()[k] instanceof CurvesLayer) {
            // Eğri Katmanı İşleme Buraya Gelecek
        }
    }
}
```
İşte olup bitenlerin bir dökümü:
-  PSD dosyasını bir klasöre yükleyerek başlıyoruz.`PsdImage` adlı nesne`im`.
-  Daha sonra, görüntüdeki tüm katmanları kullanarak döngü yapıyoruz.`im.getLayers().length` . Bu bize her katmana erişim sağlayarak bunun bir katman olup olmadığını kontrol etmemizi sağlar.`CurvesLayer`.
## Adım 4: Eğriler Katmanını Değiştirin
 kontrol eden döngünün içinde`CurvesLayer`eğrileri değiştirmek için mantık ekleyeceksiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:
```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager) curvesLayer.getCurvesManager();
    for (int i = 10; i < 50; i++) {
        manager.setValueInPosition(0, (byte) i, (byte) (15 + (i * 2)));
    }
} else {
    CurvesContinuousManager manager = (CurvesContinuousManager) curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte) 0, (byte) 50, (byte) 100);
    manager.addCurvePoint((byte) 0, (byte) 150, (byte) 130);
}
```
Bu segmentte:
- Eğriler katmanının ayrık bir yönetici mi yoksa sürekli bir yönetici mi kullandığını kontrol ediyoruz.
- Ayrı bir yönetici ise her pozisyon için 10'dan 49'a kadar yeni değerler belirliyoruz.
- Bunun tersine, sürekli bir yönetici ile eğrileri gerektiği gibi ayarlamak için eğri noktaları ekliyoruz.
## Adım 5: Değiştirilen PSD'yi kaydedin
Ayarlamalarınızı yaptıktan sonra son adım, değiştirilen PSD dosyasını kaydetmektir.
```java
im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
```
 Bu satır, ayarlanan PSD'yi daha önce tanımladığınız yola kaydeder. Her değişiklik yaptığınızda, döngü sayacına bağlı olarak farklı bir son eke sahip yeni bir dosya oluşturulacaktır.`j`.
## Çözüm
Tebrikler! Aspose.PSD for Java kullanarak bir PSD dosyasına Eğri Ayarlama katmanını nasıl ekleyeceğinizi başarıyla öğrendiniz. Yalnızca birkaç adımla görsellerinizi geliştirebilir ve ihtiyaçlarınıza göre değiştirebilirsiniz. Bu kitaplığın sağladığı esneklik, onu PSD dosyalarıyla çalışan herkes için paha biçilmez bir araç haline getiriyor. Şimdi devam edin ve farklı eğrileri deneyin ve yaratıcılığınızın akmasına izin verin.
## SSS'ler
### Aspose.PSD nedir?
Aspose.PSD, Photoshop PSD dosyalarını Java dahil çeşitli programlama dillerinde işlemeye yönelik bir kütüphanedir.
### Aspose.PSD'yi ücretsiz kullanabilir miyim?
 Evet, Aspose, satın almadan önce keşfedebileceğiniz ücretsiz bir deneme sunuyor. Kontrol edin[ücretsiz deneme indir](https://releases.aspose.com/) bağlantı.
### Photoshop'un yüklü olması gerekli mi?
Hayır, Aspose.PSD ile çalışmak için Photoshop'un makinenizde kurulu olmasına gerek yok.
### Eğri Ayarlama katmanları dışındaki katmanları değiştirebilir miyim?
Kesinlikle! Aspose.PSD, PSD dosyalarındaki çeşitli katman türlerinin manipülasyonuna olanak tanır.
### Daha fazla belgeyi nerede bulabilirim?
 Ayrıntılı belgeler için şu adresi ziyaret edin:[Java belgeleri için Aspose.PSD](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
