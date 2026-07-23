---
date: 2026-02-20
description: Aspose.PSD for Java kullanarak PSD'nin renk modunu 16‑bit gri tonlamaya
  ayarlarken PSD'yi PNG'ye nasıl dönüştüreceğinizi öğrenin. Adım adım rehber ve kod
  örnekleri.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Java'da 16-bit Gri Tonlamalı Renk Modu ile PSD'yi PNG'ye Nasıl Dönüştürülür
url: /tr/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java’da 16‑bit Gri Tonlamalı Renk Modu ile PSD’yi PNG’ye Dönüştürme

## Giriiş
Grafik tasarım ve görüntü işleme farklılıkları daldığınızda, **PSD'den PNG'ye nasıl dönüştürülür** bilmek bir gizli silah gibi. 16‑bit gri tonlamalı mod kullanarak inanılmaz derinlik ve ton zenginliği ekler, açıklıklarınız öne çıkar. Bu öğreticide **PSD renk modunu ayarlama**'u 16‑bit gri tonlamaya nasıl ayarlayacağınızı ve ardından Aspose.PSD for Java kullanarak **PSD'yi PNG olarak dışa aktar**'yi nasıl bitireceğinizi adım adım gösterirz. Görüntü iş veriminizi bir üst seviyeye taşımaya hazır mısınız? Hadi başla.

## Hızlı Yanıtlar
- **"PSD'yi PNG'ye dönüştürme" neyi içerir?** PSD yükleme, isteğe bağlı olarak renk modunu değiştirme ve PNG dosyası olarak kaydetme.
- **Dönüştürmeyi hangi Aspose sınıfı gerçekleştiriyor?** Yükleme için "PsdImage" ve kaydetme için "PngOptions".
- **Özel bir lisansa ihtiyacım var mı?** Deneme, test amaçlı çalışır; Üretim için ücretli lisans gereklidir.
- **PNG'de 16 bit derinliği koruyabilir miyim?** Evet, `PngColorType.GrayscaleWithAlpha` kullanarak.

- **Hangi IDE'ler destekleniyor?** Herhangi bir Java IDE – IntelliJ IDEA, Eclipse, VSCode, vb.

## PSD'yi 16 bit Gri Tonlamalı PNG'ye Dönüştürmenin Nedenleri

* **Ton detayını koruyun:** 16 bit gri tonlama, 8 bitlik bir görüntünün 256 tonundan çok daha fazla olan 65536 gri tonunu depolar.
* **Geniş uyumluluk:** PNG, yüksek kaliteli verileri korurken tarayıcılar, mobil uygulamalar ve masaüstü araçları arasında yaygın olarak desteklenir.
* **Kayıpsız iş akışı:** Aspose.PSD ile dönüştürme, arşivleme veya daha fazla işleme için ideal olan istenmeyen sıkıştırma bozulmalarını önler.

## Önkoşullar
Başlamadan önce, bu eğitimden en iyi şekilde yararlanabilmeniz için her şeyin hazır olduğundan emin olalım. İşte ihtiyacınız olanlar:

1. **Java Geliştirme Kiti (JDK)** – En son sürümün kurulu olduğundan emin olun. Bunu [Oracle'ın sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.
2. **Aspose.PSD for Java Kütüphanesi** – Bu, PSD dosyalarını manipüle etmemizi sağlayacak motordur. Bunu [Aspose indirme sayfasından](https://releases.aspose.com/psd/java/) edinebilirsiniz.
3. **Bir IDE** – IntelliJ IDEA, Eclipse veya Visual Studio Code gayet iyi çalışacaktır.
4. **Temel Java bilgisi** – Java sözdizimine aşinalık adımları daha sorunsuz hale getirecektir.
5. **Örnek bir PSD dosyası** – Adobe Photoshop'ta bir tane oluşturun veya çevrimiçi olarak ücretsiz bir örnek indirin.

Hazır mısınız? Harika! Gerekli paketleri içe aktaralım ve kodlamaya başlayalım.

## Paketleri İçe Aktarma
Başlamak için, gerekli Aspose.PSD içe aktarmalarını Java dosyanıza ekleyin:

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
Öncelikle, kaynak ve çıktı klasörlerini ayarlayın. Bu, programa orijinal PSD dosyasını nereden okuyacağını ve dönüştürülen dosyaları nereye yazacağını söyler.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Yer tutucu dizeleri makinenizdeki gerçek yollarla değiştirin.

## Adım 2: Görüntü İşlemeyi Yönetmek İçin Bir Yöntem Oluşturun
Dönüştürme mantığını yeniden kullanılabilir bir yöntemin içine yerleştireceğiz. Renk modu, bit derinliği ve sıkıştırma gibi değiştirmek isteyebileceğiniz tüm parametreleri alır.

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

Bu yöntem, tek bir akışta **PSD renk modunu ayarlamanıza** ve ardından **PSD'yi PNG olarak dışa aktarmanıza** olanak tanır.

## Adım 3: Dosya Yollarını Tanımlayın ve PSD'yi Yükleyin
Metodun içinde, tam dosya yollarını oluşturun ve orijinal 16 bit gri tonlamalı PSD dosyasını yükleyin:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix`, dışa aktarılan her dosya için kullanılan ayarları takip etmenize yardımcı olur.

## Adım 4: Katmanı veya Tam Görüntüyü İşleyin
Şimdi ya belirli bir katmana ya da tüm görüntüye çizim yapıyoruz. Bu örnekte, sonucu daha görünür hale getirmek için ince bir gri kenarlık ekliyoruz.

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

Dikdörtgen dinamik olarak hesaplanır, bu nedenle görüntü boyutundan bağımsız olarak ortalanmış kalır.

## Adım 5: Değiştirilmiş PSD Dosyasını Kaydedin
Çizimden sonra, belirttiğiniz tam renk modu ve bit derinliğiyle PSD dosyasını kaydediyoruz. Bu, dönüştürmeden önce **PSD renk modunu ayarlamanın** özüdür.

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
Son olarak, yeni kaydedilen PSD dosyasını yüklüyor ve PNG olarak dışa aktarıyoruz. `PngColorType.GrayscaleWithAlpha` kullanarak PNG dosyasındaki 16 bitlik renk derinliğini koruyoruz.

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

Artık yüksek kaliteli 16 bit gri tonlamalı verileri koruyarak **PSD dosyasını PNG'ye başarıyla dönüştürdünüz**.

## Sık Karşılaşılan Sorunlar ve Çözümler
| Sorun | Neden Oluşur | Çözüm |

|-------|----------------|-----|
| **“Desteklenmeyen renk türü” istisnası** | Desteklenmeyen bir kanal yapılandırmasıyla PSD kaydetmeye çalışılıyor. | `channelBitsCount` değerinin gerçek bit derinliğiyle (16) eşleştiğinden ve `channelsCount` değerinin gri tonlama için doğru (1) olduğundan emin olun. |
| **Dosya bulunamadı** | Yanlış kaynak dizin yolu. | `sourceDir` dizesini tekrar kontrol edin ve PSD dosyasının mevcut olduğunu doğrulayın. |
| **Çıktı PNG'si siyah görünüyor** | Alfa kanalı işlenmeden kaydedilen PNG. | Yukarıda gösterildiği gibi `PngColorType.GrayscaleWithAlpha` kullanın. |

## Sıkça Sorulan Sorular

**S: 16 bit gri tonlama renk modu nedir?**
C: 65536 gri tonu sağlar ve standart 8 bit (256 ton) ile karşılaştırıldığında çok daha fazla ton detayı sunar.

**S: Aspose.PSD'yi gri tonlamalı olmayan görüntüler için kullanabilir miyim?**
C: Kesinlikle! Aspose.PSD, RGB, CMYK, Lab ve diğer birçok renk modunu destekler.

**S: Aspose.PSD'nin deneme sürümü var mı?**
C: Evet, Aspose.PSD'nin ücretsiz deneme sürümünü deneyebilirsiniz. [Aspose indirme sayfasına](https://releases.aspose.com/) gidin.

**S: Aspose.PSD kullanımına dair daha fazla örneği nerede bulabilirim?**
C: Daha ayrıntılı örnekler ve eğitimler için [belgelere](https://reference.aspose.com/psd/java/) göz atabilirsiniz.

**S: Aspose.PSD için nasıl lisans satın alabilirim?**
C: [Aspose satın alma sayfasına](https://purchase.aspose.com/buy) giderek lisans satın alabilirsiniz.

---

**Son Güncelleme:** 2026-02-20
**Test Edilen Sürüm:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}