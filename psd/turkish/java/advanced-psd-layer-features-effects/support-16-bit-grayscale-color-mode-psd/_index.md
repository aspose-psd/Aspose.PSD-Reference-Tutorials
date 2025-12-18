---
date: 2025-12-17
description: PSD'yi PNG'ye dönüştürmeyi ve PSD renk modunu 16-bit gri tonlamaya ayarlamayı
  Aspose.PSD for Java ile öğrenin. Adım adım rehber ve kod örnekleri.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Java'da 16-bit Gri Tonlamalı Renk Modu ile PSD'yi PNG'ye Nasıl Dönüştürülür
url: /tr/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi Java'da 16-bit Gri Tonlamalı Renk Modu ile PNG'ye Dönüştürme

## Giriş
Grafik tasarım ve görüntü işleme dünyasına daldığınızda, **PSD'yi PNG'ye dönüştürmeyi** anlamak bir gizli silah gibi. Özellikle, 16‑bit gri tonlama modu, görüntülerinize çarpıcı bir derinlik ve detay kazandırır ve gerçekten öne çıkar. Bu öğreticide, **PSD renk modunu** 16‑bit gri tonlamaya nasıl **ayarlayacağınızı** ve ardından Aspose.PSD for Java kullanarak **PSD'yi PNG olarak dışa aktaracağınızı** adım adım göstereceğiz. Görüntü iş akışınızı bir üst seviyeye taşımaya hazır mısınız? Hadi başlayalım.

## Hızlı Yanıtlar
- **“PSD'yi PNG'ye dönüştürmek” neyi kapsar?** Bir PSD'yi yüklemek, isteğe bağlı olarak renk modunu değiştirmek ve PNG dosyası olarak kaydetmek.  
- **Dönüşümü hangi Aspose sınıfı yönetir?** Yükleme için `PsdImage` ve kaydetme için `PngOptions`.  
- **Özel bir lisansa ihtiyacım var mı?** Test için bir deneme sürümü yeterli; üretim için ücretli lisans gereklidir.  
- **PNG'de 16‑bit derinliği koruyabilir miyim?** Evet, `PngColorType.GrayscaleWithAlpha` kullanarak.  
- **Hangi IDE'ler destekleniyor?** Herhangi bir Java IDE – IntelliJ IDEA, Eclipse, VS Code vb.

## Önkoşullar
Başlamadan önce, bu öğreticiden en iyi şekilde yararlanabilmeniz için her şeyin kurulu olduğundan emin olalım. İşte ihtiyacınız olanlar:

1. **Java Development Kit (JDK)** – En son sürümün yüklü olduğundan emin olun. [Oracle'ın sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.  
2. **Aspose.PSD for Java Library** – PSD dosyalarını manipüle etmemizi sağlayan motor. [Aspose indirme sayfasından](https://releases.aspose.com/psd/java/) edinebilirsiniz.  
3. **Bir IDE** – IntelliJ IDEA, Eclipse veya Visual Studio Code yeterli olacaktır.  
4. **Temel Java bilgisi** – Java sözdizimine aşina olmak adımları daha sorunsuz yapar.  
5. **Örnek bir PSD dosyası** – Adobe Photoshop'ta oluşturabilir ya da çevrimiçi ücretsiz bir örnek indirebilirsiniz.

Hazır mısınız? Harika! Gerekli paketleri içe aktaralım ve kodlamaya başlayalım.

## Paketleri İçe Aktarma
İşe başlamak için Java dosyanıza gerekli Aspose.PSD içe aktarmalarını ekleyin:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Bu içe aktarmalar, PSD dosyalarını manipüle etmek, renk modunu ayarlamak ve sonucu PNG olarak dışa aktarmak için kullanacağınız işlevlere erişmenizi sağlar.

## Adım 1: Dizinlerinizi Tanımlayın
İlk olarak, kaynak ve çıktı klasörlerini ayarlayın. Bu, programın orijinal PSD'yi nereden okuyacağını ve dönüştürülmüş dosyaları nereye yazacağını belirler.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Yer tutucu dizeleri, makinenizdeki gerçek yollarla değiştirin.

## Adım 2: Görüntü İşleme İçin Bir Metod Oluşturun
Dönüşüm mantığını yeniden kullanılabilir bir metod içinde kapsülleneceğiz. Renk modu, bit derinliği ve sıkıştırma gibi ayarlamak isteyebileceğiniz tüm parametreleri alır.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Bu metod, **PSD renk modunu** ayarlamanıza ve ardından **PSD'yi PNG olarak dışa aktarmanıza** tek bir akışta olanak tanır.

## Adım 3: Dosya Yollarını Tanımlayın ve PSD'yi Yükleyin
Metod içinde tam dosya yollarını oluşturun ve orijinal 16‑bit gri tonlamalı PSD'yi yükleyin:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix`, her dışa aktarılan dosya için kullanılan ayarları takip etmenize yardımcı olur.

## Adım 4: Katmanı veya Tam Görüntüyü İşleyin
Şimdi ya belirli bir katmana ya da tüm görüntüye çizebiliriz. Bu örnekte, sonucu daha görünür kılmak için ince bir gri kenarlık ekliyoruz.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Dikdörtgen, görüntü boyutundan bağımsız olarak ortalanmış kalması için dinamik olarak hesaplanır.

## Adım 5: Değiştirilmiş PSD Dosyasını Kaydedin
Çizimden sonra, PSD'yi belirttiğiniz tam renk modu ve bit derinliğiyle kaydederiz. Bu, dönüşümden önce **PSD renk modunu** ayarlamanın özüdür.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Adım 6: PSD'yi PNG'ye Dönüştürün
Son olarak, yeni kaydedilen PSD'yi yükleyip PNG olarak dışa aktarırız. `PngColorType.GrayscaleWithAlpha` kullanarak PNG dosyasında 16‑bit derinliği koruruz.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Artık yüksek kaliteli 16‑bit gri tonlamalı veriyi koruyarak **PSD'yi PNG'ye başarıyla dönüştürmüş** oldunuz.

## Yaygın Sorunlar ve Çözümleri
| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|------|
| **“Unsupported color type” exception** | Desteklenmeyen bir kanal yapılandırmasıyla PSD kaydetmeye çalışmak. | `channelBitsCount` değerinin gerçek bit derinliği (16) ile eşleştiğinden ve `channelsCount` değerinin gri tonlama için (1) doğru olduğundan emin olun. |
| **Dosya bulunamadı** | Yanlış kaynak dizini yolu. | `sourceDir` dizesini tekrar kontrol edin ve PSD dosyasının mevcut olduğundan emin olun. |
| **Çıktı PNG siyah görünüyor** | PNG, alfa kanalı işlenmeden kaydedildi. | Yukarıda gösterildiği gibi `PngColorType.GrayscaleWithAlpha` kullanın. |

## Sıkça Sorulan Sorular

**Q: 16-bit gri tonlamalı renk modu nedir?**  
A: 65 536 gri ton sunar, standart 8‑bit (256 ton) moduna göre çok daha fazla ton detayına sahip olur.

**Q: Aspose.PSD'yi gri tonlamalı olmayan görüntüler için kullanabilir miyim?**  
A: Kesinlikle! Aspose.PSD, RGB, CMYK, Lab ve birçok diğer renk modunu destekler.

**Q: Aspose.PSD'nin deneme sürümü var mı?**  
A: Evet, Aspose.PSD'nin ücretsiz deneme sürümünü deneyebilirsiniz. Sadece [Aspose indirme sayfasına](https://releases.aspose.com/) gidin.

**Q: Aspose.PSD kullanımına dair daha fazla örnek nereden bulabilirim?**  
A: Daha ayrıntılı örnekler ve öğreticiler için [dökümantasyona](https://reference.aspose.com/psd/java/) göz atabilirsiniz.

**Q: Aspose.PSD için lisans nasıl satın alınır?**  
A: [Aspose satın alma sayfasını](https://purchase.aspose.com/buy) ziyaret ederek lisans satın alabilirsiniz.

---

**Son Güncelleme:** 2025-12-17  
**Test Edilen Sürüm:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}