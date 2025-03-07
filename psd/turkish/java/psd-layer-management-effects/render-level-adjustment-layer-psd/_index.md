---
title: PSD Dosyalarında İşleme Düzeyi Ayarlama Katmanı - Java
linktitle: PSD Dosyalarında İşleme Düzeyi Ayarlama Katmanı - Java
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak görüntü kontrastını ve canlılığını zahmetsizce nasıl geliştireceğinizi öğrenin. Bu adım adım kılavuzla Ana Seviye Ayarlama Katmanları.
weight: 17
url: /tr/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında İşleme Düzeyi Ayarlama Katmanı - Java

## giriiş

Hiç kontrast veya canlılıktan yoksun bir görüntü bulmak için bir PSD dosyasını açtığınız oldu mu? Korkmayın, resim düzenleme savaşçıları! Aspose.PSD for Java, güçlü Düzey Ayarlama Katmanı manipülasyon yetenekleriyle imdadınıza yetişiyor. Bu kılavuz, Seviyeleri kullanarak resimlerinize çok kolay bir şekilde ince ayar yapmanızı sağlayacak bilgiyle donatacaktır. 

## Önkoşullar

- Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın güncel bir sürümünün kurulu olduğundan emin olun. Oracle web sitesinden indirebilirsiniz ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java Library: Aspose.PSD for Java kütüphanesini indirme sayfasından indirin ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Tüm özellikleri kullanmak için geçerli bir lisansa ihtiyacınız olacak, ancak başlamanız için ücretsiz deneme sürümü mevcuttur ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Paketleri İçe Aktar

Koda dalmadan önce, PSD dosyalarıyla etkileşim kurmak için gerekli Aspose.PSD sınıflarını içe aktarmamız gerekiyor. İhtiyacınız olan şey:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

`com.aspose.psd` paket PSD manipülasyon işlevlerine erişim sağlarken,`com.aspose.psd.imaging.PngOptions` görüntüyü PNG olarak kaydederken seçenekleri tanımlamamıza olanak tanır.

Şimdi Seviye ayarlama maceramıza başlayalım:

## Adım 1: Dosya Yollarını Ayarlama:

- Belge dizininiz için değişkenleri tanımlayın (`dataDir`), kaynak PSD dosya adı (`sourceFileName`), değişiklikten sonra PSD dosya adını hedefleyin (`psdPathAfterChange`) ve son PNG dışa aktarma yolunu (`pngExportPath`). Kodun okunabilirliğini artırmak için açıklayıcı adlar kullanmayı düşünün.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Adım 2: PSD Görüntüsünün Yüklenmesi:

-  Şunu kullanın:`Image.load` Kaynak PSD dosyasını açma ve onu bir klasörde saklama yöntemi`PsdImage`nesne (`im`). Aspose.PSD dosya formatını otomatik olarak algılar.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Adım 3: Katmanlar Arasında Yineleme:

- PSD'nizde Düzey Ayarlama Katmanını bulmamız gerekiyor. Aspose, bir döngü kullanarak tüm katmanlar arasında yineleme yapmak için uygun bir yol sağlar.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (Seviyeler Katmanını kontrol edecek kod buraya eklenecektir)
}
```

## Adım 4: Düzeyler Katmanını Belirleme:

- Döngünün içinde geçerli katmanın (`im.getLayers()[i]` ) bunun bir örneğidir`LevelsLayer` kullanarak sınıf`instanceof` operatör. 
-  Eğer öyleyse, katmanı bir`LevelsLayer` daha fazla manipülasyon için nesne.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (seviyeleri ayarlama kodu buraya eklenecektir)
   }
}
```
## Adım 5: Seviyelerin İnce Ayarı (Devam):

-  Çıkış seviyelerini kullanarak ayarlayın.`setOutputShadowLevel` Ve`setOutputHighlightLevel` Ortaya çıkan görüntünün koyuluğunu ve açıklığını kontrol etmek için. Bu değerler, çıkış aralığına eşlenecek giriş düzeyi aralığını belirler.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Giriş Düzeylerini Ayarlayın (0-255):
	   channel.setInputShadowLevel((short) 10); // Gölgeleri hafifçe koyulaştırın
	   channel.setInputMidtoneLevel(2.0f);     // Orta tonları artır
	   channel.setInputHighlightLevel((short) 230); // Vurguları azaltın

	   // Çıkış Düzeylerini Ayarlayın (0-255):
	   channel.setOutputShadowLevel((short) 20); // Gölgeleri daha da koyulaştırın
	   channel.setOutputHighlightLevel((short) 200); //Vurguları aydınlat
   }
}
```

## Adım 6: Değiştirilen PSD'yi Kaydetme:

-  Şunu kullanın:`save` yöntemi`PsdImage` Değiştirilen görüntüyü belirtilen yola kaydetmek için nesne (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Adım 7: PNG olarak dışa aktarma (İsteğe bağlı):

-  Ayarlanan görüntünün PNG sürümüne ihtiyacınız varsa`PngOptions` nesneyi seçin ve renk türünü şu şekilde ayarlayın:`TruecolorWithAlpha` . Daha sonra şunu kullanın:`save` PNG dışa aktarma yolu ve seçenekleriyle yöntemi tekrar kullanın.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Ve işte karşınızda! Aspose.PSD for Java'yı kullanarak PSD dosyanızdaki Düzey Ayarlama Katmanını başarıyla ayarladınız. Bu adımları anlayarak ve farklı değerleri deneyerek görsellerinizin kontrastını ve genel görünümünü iyileştirebilirsiniz.

## Çözüm

Aspose.PSD for Java, görüntü düzenleme sürecinizin kontrolünü elinize almanızı sağlar. Düzey Ayarlama Katmanında ustalaşarak fotoğraflarınıza ve tasarımlarınıza yeni bir soluk getirebilirsiniz. Unutmayın, pratik mükemmelleştirir, bu nedenle bu güçlü aracın tüm potansiyelini denemekten ve keşfetmekten çekinmeyin.
 
## SSS'ler

### Bireysel renk kanallarını (RGB) ayrı ayrı ayarlayabilir miyim? 
Evet, her renk kanalına aşağıdaki düğmeyi kullanarak erişebilirsiniz:`getChannel` yöntemi`LevelsLayer` Nesneyi bağımsız olarak kullanın ve seviyelerini değiştirin.

### Bir PSD'de birden fazla Düzey Ayarlama Katmanını nasıl kullanırım?
Kod tüm katmanlar boyunca yinelenir, böylece görüntüde bulunan tüm ek Düzey katmanlarını otomatik olarak işler.

### Düzeyler dışında görüntü kontrastını ayarlamanın başka yolları var mı?
Kesinlikle! Aspose.PSD, Eğriler, Parlaklık/Kontrast ve daha fazlası gibi çeşitli görüntü ayarlama araçları sunar.

### Bu işlemi birden fazla görüntü için otomatikleştirebilir miyim? 
Evet, birden fazla PSD dosyasını verimli bir şekilde işlemek için bu kodu bir döngüye veya toplu işleme komut dosyasına dahil edebilirsiniz.

### Daha fazla bilgi ve desteği nerede bulabilirim?
Aspose kapsamlı belgeler sağlar ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) ve bir destek forumu ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) karşılaşabileceğiniz her türlü soru veya sorun için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
