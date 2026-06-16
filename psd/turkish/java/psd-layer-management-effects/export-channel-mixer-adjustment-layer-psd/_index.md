---
date: 2026-03-31
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak nasıl kaydedeceğinizi
  öğrenin. Bu PSD kanal karıştırıcı öğreticisi, PSD'yi PNG'ye nasıl dönüştüreceğinizi,
  RGB ve CMYK katmanlarını nasıl değiştireceğinizi ve PSD dosyalarını toplu olarak
  nasıl işleyebileceğinizi gösterir.
linktitle: Export Channel Mixer Adjustment Layer in PSD - Java
second_title: Aspose.PSD Java API
title: Java'da Kanal Karıştırıcı Ayar Katmanı ile PSD'yi PNG olarak nasıl kaydedilir
url: /tr/java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Kanal Mikseri Ayar Katmanı ile PSD'yi PNG olarak kaydetme

## Giriş

Channel Mixer katmanı ile yapılan ayarları koruyarak **save PSD as PNG** yapmanız gerekiyorsa, doğru yerdesiniz. Bu adım‑adım **psd channel mixer tutorial**'da bir PSD dosyasını yüklemeyi, hem RGB hem de CMYK Channel Mixer Adjustment Layers'ı ayarlamayı ve sonunda sonucu PNG olarak dışa aktarmayı göstereceğiz. Aynı yaklaşımın büyük ölçekli projeler için **batch process PSD files** nasıl ölçeklendirilebileceğini de göreceksiniz.

## Hızlı Yanıtlar
- **save PSD as PNG ne anlama geliyor?** Bir Photoshop belgesini şeffaflığı koruyarak kayıpsız bir PNG'ye dönüştürür.  
- **Hangi kütüphane dönüşümü gerçekleştirir?** Aspose.PSD for Java, ayar katmanları için tam destek sağlar.  
- **Hem RGB hem de CMYK dosyalarıyla çalışabilir miyim?** Evet – API, `RgbChannelMixerLayer` ve `CmykChannelMixerLayer` sınıflarını içerir.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Lisanslı bir sürüm gereklidir; test için geçici bir lisans mevcuttur.  
- **Toplu işleme mümkün mü?** Kesinlikle – bir klasördeki dosyalar üzerinde döngü kurarak aynı adımları her PSD'ye uygulayabilirsiniz.

## Channel Mixer Ayar Katmanı nedir?

Channel Mixer Ayar Katmanı, Kırmızı, Yeşil, Mavi (veya Camgöbeği, Macenta, Sarı, Siyah) kanallarının katkılarını yeniden karıştırarak hassas renk dengesi elde etmenizi sağlar. Normal bir katmandan farklı olarak, yok edici değildir; yani orijinal piksel verileri dokunulmaz kalır.

## Aspose.PSD'yi **convert PSD to PNG** için neden kullanmalısınız?

- **Full layer fidelity** – tüm ayar katmanları dönüşüm sırasında korunur.  
- **No Photoshop required** – kodu herhangi bir sunucu ya da CI hattında çalıştırabilirsiniz.  
- **Supports both RGB and CMYK** – baskıya hazır iş akışları için idealdir.  

## Önkoşullar

1. **Aspose.PSD for Java** – [download page](https://releases.aspose.com/psd/java/) adresinden indirin.  
2. **Java Development Kit (JDK) 8+** – `java`'nın PATH'ınızda olduğundan emin olun.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Sample PSD files** – Channel Mixer Adjustment Layers içeren dosyalar (hem RGB hem de CMYK varyantları).  

## Paketleri İçe Aktarma

İlk olarak, ihtiyacımız olan sınıfları içe aktarın. Bu, PSD dosyalarıyla çalışmak ve PNG dışa aktarma seçenekleri için ortamı hazırlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## **save PSD as PNG** – RGB Örneği

### Adım 1: RGB Channel Mixer Layer içeren PSD dosyasını yükleyin

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";

PsdImage im = (PsdImage) Image.load(sourceFileName);
```

`dataDir` adlı klasöre işaret ediyor ve dosyayı bir `PsdImage` nesnesine yüklüyoruz; bu nesne katmanlarına tam erişim sağlar.

### Adım 2: RGB Channel Mixer Layer'ı değiştirin

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof RgbChannelMixerLayer) {
        RgbChannelMixerLayer rgbLayer = (RgbChannelMixerLayer) im.getLayers()[i];
        rgbLayer.getRedChannel().setBlue((short) 100);
        rgbLayer.getBlueChannel().setGreen((short) -100);
        rgbLayer.getGreenChannel().setConstant((short) 50);
    }
}
```

Her katmanı dolaşıyoruz, `RgbChannelMixerLayer`'ı buluyor ve kanal değerlerini ayarlıyoruz. Bu örnek, kırmızı kanalda mavi katkısını artırıyor, mavi kanalda yeşili azaltıyor ve yeşil kanala sabit bir ofset ekliyor.

### Adım 3: Değiştirilen PSD'yi kaydedin (hala bir PSD)

```java
String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
im.save(psdPathAfterChange);
```

Dosyayı kaydetmek, ayar katmanını korur; böylece gerektiğinde Photoshop'ta tekrar açabilirsiniz.

### Adım 4: Görüntüyü PNG olarak dışa aktarın (**save PSD as PNG** adımı)

```java
String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

`PngOptions` örneği oluşturuyor, renk tipini `TruecolorWithAlpha` olarak ayarlayarak şeffaflığı koruyor ve ardından görüntüyü dışa aktarıyoruz.

## **save PSD as PNG** – CMYK Örneği

### Adım 5: CMYK Channel Mixer Layer içeren PSD dosyasını yükleyin

```java
sourceFileName = dataDir + "ChannelMixerAdjustmentLayerCmyk.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

Yükleme işlemi aynı; sadece CMYK renk modelini kullanan farklı bir dosyayla çalışıyoruz.

### Adım 6: CMYK Channel Mixer Layer'ı değiştirin

```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof CmykChannelMixerLayer) {
        CmykChannelMixerLayer cmykLayer = (CmykChannelMixerLayer) img.getLayers()[i];
        cmykLayer.getCyanChannel().setBlack((short) 20);
        cmykLayer.getMagentaChannel().setYellow((short) 50);
        cmykLayer.getYellowChannel().setCyan((short) -25);
        cmykLayer.getBlackChannel().setYellow((short) 25);
    }
}
```

Burada CMYK kanallarını ayarlıyoruz: cyan'a siyah eklemek, magenta'nın sarı bileşenini ayarlamak vb. Bu, API'nin baskı odaklı dosyalar için esnekliğini gösterir.

### Adım 7: Değiştirilen CMYK PSD'yi kaydedin

```java
psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
img.save(psdPathAfterChange);
```

Yine, yeni ayarlarla bir PSD sürümünü tutuyoruz.

### Adım 8: CMYK görüntüyü PNG olarak dışa aktarın

```java
pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
img.save(pngExportPath, options);
```

Kaynak CMYK olsa bile, PNG dışa aktarımı otomatik olarak bir RGB tabanlı PNG'ye dönüştürür ve şeffaflığı korur.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| PNG yanlış renklerle görünüyor | Uygun profil olmadan CMYK → RGB dönüşümü | Kaynak PSD'nin gömülü bir ICC profiline sahip olduğundan emin olun; Aspose.PSD dışa aktarım sırasında buna saygı gösterir. |
| Ayar katmanı bulunamadı | Katman tipi uyuşmazlığı (ör. bir “Color Balance” katmanı yerine) | Dönüştürmeden önce katman sınıfını (`RgbChannelMixerLayer` veya `CmykChannelMixerLayer`) doğrulayın. |
| Çalışma zamanında lisans istisnası | Geçerli bir lisans olmadan kütüphaneyi kullanmak | Geliştirme sırasında [temporary license](https://purchase.aspose.com/temporary-license/) sayfasından geçici bir lisans uygulayın. |

## Sıkça Sorulan Sorular

**Q: Aspose.PSD for Java'yı diğer görüntü formatlarıyla kullanabilir miyim?**  
**A:** Evet, kütüphane PSD dışında PNG, JPEG, BMP, TIFF ve daha birçok formatı destekler.

**Q: Eğriler veya Seviyeler gibi diğer ayar katmanlarıyla nasıl çalışırım?**  
**A:** Her ayar türünün kendi sınıfı vardır (ör. `CurvesAdjustmentLayer`). Bunları kanal mikseri örneğine benzer şekilde manipüle edebilirsiniz.

**Q: **batch process PSD files** PNG'ye dönüştürmek için bir yol var mı?**  
**A:** Kesinlikle. Yukarıdaki adımları bir dizindeki dosyalar üzerinde dönen bir `for‑each` döngüsü içinde sararak aynı değişiklikleri ve dışa aktarma mantığını uygulayabilirsiniz.

**Q: Dönüştürürken maksimum görüntü kalitesini korumak için en iyi uygulama nedir?**  
**A:** `TruecolorWithAlpha` ile `PngOptions` kullanın ve down‑sampling'den kaçının. Ayrıca, daha sonra kayıpsız düzenlemeler için orijinal PSD'yi saklayın.

**Q: Üretim kullanımında ücretli bir lisansa ihtiyacım var mı?**  
**A:** Evet. Değerlendirme için geçici bir lisans yeterli, ancak ticari dağıtım için tam lisans gereklidir.

---

**Son Güncelleme:** 2026-03-31  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}