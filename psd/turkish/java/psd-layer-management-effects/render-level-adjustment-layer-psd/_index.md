---
date: 2026-04-05
description: Aspose.PSD for Java kullanarak PSD'yi PNG'ye nasıl dışa aktaracağınızı
  ve görüntü kontrastını zahmetsizce nasıl artıracağınızı öğrenin. Bu adım adım kılavuzla
  Seviye Ayar Katmanlarını ustalaşın.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: PSD'yi PNG'ye Dışa Aktar ve Java'da Seviye Ayar Katmanını İşle
second_title: Aspose.PSD Java API
title: PSD'yi PNG'ye Dışa Aktar ve Java'da Seviye Ayar Katmanını Renderla
url: /tr/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dışa Aktarma ve Java'da Seviye Ayarlama Katmanını İşleme

## Giriş

Hiç bir PSD dosyasını açıp renklerin düz göründüğünü veya kontrastın eksik olduğunu fark ettiniz mi? Aspose.PSD for Java kullanarak bir Levels Adjustment Layer ile görüntüyü ince ayar yaparken **PSD'yi PNG'ye dışa aktar**abilirsiniz. Bu öğreticide, bir PSD'yi yüklemek, seviyelerini ayarlamak ve sonucu PNG olarak kaydetmek gibi tüm süreci adım adım göstereceğiz—böylece renk canlılığını artırabilir ve web için hazır varlıkları dakikalar içinde hazırlayabilirsiniz.

## Hızlı Yanıtlar
- **“PSD'yi PNG'ye dışa aktarma” ne anlama geliyor?** Photoshop belgesini şeffaflığı koruyan kayıpsız bir PNG görüntüsüne dönüştürür.  
- **Dışa aktarmadan önce seviyeleri ayarlayabilir miyim?** Evet, Aspose.PSD giriş ve çıkış seviyelerini programlı olarak değiştirmenize olanak tanır.  
- **Bir lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Toplu işleme mümkün mü?** Kesinlikle—kodunuzu bir döngü içinde yerleştirerek birden fazla PSD dosyasını işleyebilirsiniz.  
- **Hangi Java sürümü gerekiyor?** Java 8 veya daha yenisi önerilir.

## “PSD'yi PNG'ye dışa aktarma” nedir?
Bir PSD'yi PNG'ye dışa aktarmak, katmanlı Photoshop dosyasını alıp Portable Network Graphics (PNG) görüntüsü olarak düzleştirmek anlamına gelir. PNG, kayıpsız sıkıştırma ve alfa kanalı destekler; bu da onu web grafikleri ve UI varlıkları için ideal kılar.

## Dışa aktarmadan önce seviyeleri neden ayarlamalısınız?
Seviyeleri ayarlamak, gölgeleri, orta tonları ve vurguları kontrol etmenizi sağlar, genel kontrastı ve renk dengesini iyileştirir. Bu adım, son PNG'nin Photoshop'ta manuel düzenleme ihtiyacı olmadan cilalı görünmesini sağlar.

## Önkoşullar

- **Java Development Kit (JDK)** – en son sürümü Oracle web sitesinden indirin ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – resmi indirme sayfasından edinin ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Ücretsiz bir deneme sürümü mevcuttur ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Paketleri İçe Aktar

Koda dalmadan önce, PSD manipülasyonu ve PNG dışa aktarımına erişim sağlayan sınıfları içe aktarın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım Adım Kılavuz

### Adım 1: Dosya Yollarını Tanımla (PSD İşlemini Otomatikleştirme)

Kaynak PSD, değiştirilmiş PSD ve nihai PNG dışa aktarım konumu için net ve açıklayıcı değişkenler belirleyin.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Adım 2: PSD Görüntüsünü Yükle

`Image.load` kullanarak PSD dosyasını bir `PsdImage` nesnesine okuyun. Aspose.PSD formatı otomatik olarak algılar.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Adım 3: Katmanlar Üzerinde Döngü (Seviyeleri Ayarlama)

Levels Adjustment Layer'ı bulmak için her katman üzerinde döngü yapın.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Adım 4: Seviye Katmanını Belirle

Her katmanı `instanceof LevelsLayer` ile kontrol edin. Bulunduğunda, özelliklerini değiştirebilmek için tip dönüşümü yapın.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Adım 5: Seviyeleri İnce Ayarla (Seviyeleri Ayarlama)

İlk kanal (genellikle birleşik kanal) için giriş ve çıkış seviyelerini ayarlayın. Bu değerler örnek niteliğindedir; denemekten çekinmeyin.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Adım 6: Değiştirilmiş PSD'yi Kaydet (PSD'yi Otomatikleştirme)

Değişiklikleri yeni bir PSD dosyasına kaydedin.

```java
im.save(psdPathAfterChange);
```

### Adım 7: PNG Olarak Dışa Aktar (PSD'yi PNG'ye Dışa Aktarma)

Bir PNG sürümüne ihtiyacınız varsa, `PngOptions` yapılandırın ve görüntüyü kaydedin.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Ortak Kullanım Durumları

- **Web varlık hazırlığı:** Tasarımcı tarafından sağlanan PSD mockup'larını tarayıcılara hazır PNG'lere dönüştürün.  
- **Toplu işleme:** CI pipeline'ında onlarca PSD dosyasının dönüşümünü otomatikleştirin.  
- **Dinamik görüntü oluşturma:** Dışa aktarmadan önce **kullanıcı girdisine** göre seviyeleri anlık olarak ayarlayın.

## Sorun Giderme ve İpuçları

- **Katmanlara erişirken null pointer:** PSD'nin gerçekten bir Levels Adjustment Layer içerdiğinden emin olun; aksi takdirde null kontrolü ekleyin.  
- **Dışa aktarma sonrası beklenmeyen renkler:** PNG renk tipinin şeffaflığı korumak için `TruecolorWithAlpha` olarak ayarlandığını doğrulayın.  
- **Birçok dosyada performans:** Bellek tüketimini azaltmak için bir toplu işlemde aynı `PsdImage` örneğini yeniden kullanın.

## Sıkça Sorulan Sorular

**S: Bireysel renk kanallarını (RGB) ayrı ayrı ayarlayabilir miyim?**  
C: Evet. Her kanalı bağımsız olarak ayarlamak için `levelsLayer.getChannel(index)` kullanın; `index` = 0 (Kırmızı), 1 (Yeşil), 2 (Mavi).

**S: Tek bir PSD içinde birden fazla Levels Adjustment Layer nasıl yönetilir?**  
C: Döngü her katmanı işler; bulunan her `LevelsLayer`, `if` bloğu içindeki koda göre ayarlanır.

**S: Seviyeler dışında kontrastı artırmanın başka yolları var mı?**  
C: Aspose.PSD ayrıca Curves, Brightness/Contrast ve Histogram Equalization ayarlarını da sunar.

**S: Bu işlemi bir klasördeki PSD dosyaları için otomatikleştirebilir miyim?**  
C: Tüm iş akışını `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` döngüsü içinde sarın ve her dosyayı sırasıyla işleyin.

**S: Daha fazla dokümantasyon ve destek nerede bulunabilir?**  
C: Resmi referansa ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) ve topluluk forumuna ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) göz atın.

## Sonuç

**export PSD to PNG** iş akışını ve **seviye ayarlamayı** programlı olarak öğrenerek, Java ortamınızdan çıkmadan görüntü kalitesi üzerinde tam kontrol elde edersiniz. Web için varlıklar hazırlıyor, tasarım hattını otomatikleştiriyor ya da toplu işlemci oluşturuyorsanız, Aspose.PSD for Java işi basit ve güvenilir kılar.

---

**Son Güncelleme:** 2026-04-05  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}