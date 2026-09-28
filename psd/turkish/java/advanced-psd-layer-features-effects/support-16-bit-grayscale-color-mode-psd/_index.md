---
date: 2026-09-28
description: Aspose.PSD for Java kullanarak PSD renk modunu 16-bit grayscale olarak
  ayarlarken PSD'yi PNG olarak nasıl dışa aktaracağınızı öğrenin. Adım adım kod örnekli
  rehber.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: PSD'yi PNG Olarak Dışa Aktar – 16-bit Grayscale – Java
og_description: Aspose.PSD for Java kullanarak 16‑bit grayscale ile PSD'yi PNG olarak
  dışa aktarın. 65.536 gri tonu korumak için bu adım adım öğreticiyi izleyin.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Java'da 16‑bit grayscale ile PSD'yi PNG Olarak Dışa Aktar – Aspose.PSD Kılavuzu
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Java'da 16‑bit grayscale renk modunda PSD'yi PNG olarak nasıl dışa aktarılır
url: /tr/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da 16‑bit gri tonlamalı renk modunda PSD'yi PNG olarak dışa aktar

## Giriş
PSD'yi PNG olarak dışa aktarırken 16‑bit gri tonlamalı renk modunu korumak, profesyonel bir fotoğrafın derinliğini ve PNG'nin evrensel uyumluluğunu size sunar. Bu rehberde Aspose.PSD for Java kullanarak **PSD renk modunu 16‑bit gri tonlamaya ayarlamayı** ve ardından **PSD'yi PNG olarak dışa aktarmayı** öğreneceksiniz. Öğretici, ön koşullardan sorun giderme adımlarına kadar her şeyi kapsar, böylece iş akışını herhangi bir Java tabanlı görüntü hattına entegre edebilirsiniz.

## Hızlı cevaplar
- **“PSD'yi PNG olarak dışa aktarma” neyi içerir?** Bir PSD dosyasını yükleyin, isteğe bağlı olarak renk modunu değiştirin ve PNG dosyası olarak kaydedin.  
- **Hangi Aspose sınıfı dönüşümü yönetir?** `PsdImage` PSD'yi yükler ve `PngOptions` PNG çıktı ayarlarını tanımlar.  
- **Üretim için lisansa ihtiyacım var mı?** Evet – deneme sürümü test için çalışır, ancak ticari kullanım için ücretli lisans gereklidir.  
- **16‑bit derinlik PNG'de korunabilir mi?** Kesinlikle, `PngColorType.GrayscaleWithAlpha` kullanarak.  
- **Hangi IDE'ler destekleniyor?** Herhangi bir Java IDE – IntelliJ IDEA, Eclipse, VS Code veya NetBeans.

## PSD'yi PNG olarak dışa aktarma nedir?
PSD'yi PNG olarak dışa aktarma, bir Adobe Photoshop belgesini (PSD) Portable Network Graphics (PNG) dosyasına dönüştürme sürecidir; bu işlem görüntünün piksel verilerini ve renk derinliğini korur. Bu dönüşüm, ton detayını kaybetmeden yüksek kaliteli gri tonlamalı varlıkları web üzerinde paylaşmak için yaygın olarak kullanılır.

## Neden PSD'yi 16‑bit gri tonlamalı PNG olarak dışa aktar?
16‑bit gri tonlamayı koruyarak PNG'ye dışa aktarmak, 65 536 gri tonunu korur; bu, 8‑bit görüntülerden çok daha fazla tonal zenginlik sağlar. PNG'nin evrensel desteği, dosyaların tarayıcılarda, mobil uygulamalarda ve masaüstü editörlerde kayıpsız görüntülenmesini garanti eder; Aspose.PSD'nin kayıpsız sıkıştırması ise hiçbir artefaktın ortaya çıkmamasını sağlar.

## Ön Koşullar
1. **Java Development Kit (JDK)** – En son JDK'yı [Oracle'ın sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) yükleyin.  
2. **Aspose.PSD for Java library** – JAR dosyasını [Aspose indirme sayfasından](https://releases.aspose.com/psd/java/) indirin.  
3. **Bir IDE** – IntelliJ IDEA, Eclipse veya Visual Studio Code mükemmel çalışır.  
4. **Temel Java bilgisi** – Sınıflar oluşturma, istisna yönetimi ve dosya yolları ile çalışmada rahat olmalısınız.  
5. **Bir örnek PSD dosyası** – Adobe Photoshop'ta bir dosya oluşturun veya çevrimiçi ücretsiz bir örnek alın.

## PSD'yi PNG olarak dışa aktarma adım adım

## PSD renk modunu 16‑bit gri tonlamaya nasıl ayarlarsınız?
PsdImage, bir PSD dosyasını bellekte yükleyen ve temsil eden Aspose.PSD sınıfıdır.  
ColorMode, bir PSD görüntüsünün renk modunu tanımlayan bir enumdur.  

PSD'yi `PsdImage` ile yükleyin, `ColorMode` özelliğini kullanarak renk modunu değiştirin ve ardından değiştirilmiş dosyayı kaydedin. Bu işlem tamamen bellek içinde çalışır, ara dosyalara ihtiyaç duymaz ve dönüşümün hızlı ve verimli olmasını sağlar.

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

Bu importlar, PSD dosyalarını manipüle etmek, renk modunu ayarlamak ve sonucu PNG olarak dışa aktarmak için kullanacağınız işlevlere erişmenizi sağlar.

## Kaynak ve çıktı dizinlerini nasıl tanımlarsınız?
`File`, dosya sisteminde bir dosya veya dizin yolunu temsil eden java.io sınıfıdır.  

Programın orijinal PSD'yi nereden okuyacağını ve dönüştürülmüş PNG'yi nereye yazacağını belirtmeniz gerekir. Mutlak veya göreli yollar kullanılabilir, ancak ortamlar arasında tutarlı tutarak yol çözümleme hatalarından kaçının.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Yer tutucu dizeleri, makinenizdeki gerçek yollarla değiştirin.

## Dönüşüm mantığını yeniden kullanılabilir bir yöntemde nasıl kapsüllersiniz?
`convertPsdToPng`, bir PSD dosyasını isteğe bağlı ayarlarla PNG'ye dönüştürmek için gereken tüm adımları kapsülleyen özel bir yöntemdir.  

Özel bir yöntem oluşturmak, aynı dönüşüm adımlarını birden fazla dosya veya farklı ayarlar için yeniden kullanmanıza olanak tanır. Kaynak yol, hedef klasör ve isteğe bağlı sıkıştırma seviyesi gibi parametreleri geçerek iş akışını esnek ve sürdürülebilir hâle getirir.

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

Bu yöntem, **PSD renk modunu ayarlamanıza** ve ardından **PSD'yi PNG olarak dışa aktarmanıza** tek bir akışta olanak tanır.

## PSD'yi nasıl yüklersiniz ve 16‑bit gri tonlama modunu uygularsınız?
PsdImage, bir PSD dosyasını belleğe yükleyen Aspose.PSD sınıfıdır.  
ColorMode.GRAYSCALE_16, görüntüyü 16‑bit gri tonlamaya ayarlayan bir enum değeridir.  
`channelBitsCount`, kanal başına bit sayısını belirten bir özelliktir.  

Dönüşüm yönteminin içinde tam dosya yollarını oluşturun, `PsdImage` örneğini yaratın ve `ColorMode` özelliğini `ColorMode.GRAYSCALE_16` olarak değiştirin. `channelBitsCount` özelliği, yüksek bit derinliğini korumak için 16 olarak ayarlanmalıdır; bu, görüntünün tüm tonal bilgisini tutmasını sağlar.

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

## Görüntüye ince bir kenarlık nasıl çizilir (isteğe bağlı adım)?
`Graphics`, bir `PsdImage` tuvali üzerinde çizim yetenekleri sağlayan bir sınıftır.  

İsteğe bağlı olarak, çıktıyı test sırasında daha görünür kılmak için görüntünün etrafına gri bir dikdörtgen çizebilirsiniz. Bu adım, katmanlar ve grafik nesneleriyle nasıl çalışılacağını gösterir ve dikdörtgen, görüntü boyutundan bağımsız olarak ortalanmış kalacak şekilde dinamik olarak hesaplanır.

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

Dikdörtgen, görüntü boyutundan bağımsız olarak ortalanmış kalacak şekilde dinamik olarak hesaplanır.

## Değiştirilen PSD'yi yeni renk modu ile nasıl kaydedersiniz?
`PsdOptions`, bir PSD dosyasının nasıl kaydedileceğini kontrol eden bir sınıftır; renk modu ve bit derinliği ayarlarını içerir.  

Çizim (veya bu adımı atlama) işleminden sonra, `PsdImage` örneğinde `save` metodunu çağırın ve 16‑bit gri tonlama yapılandırmasını koruyan bir `PsdOptions` nesnesi geçirin. Bu, kaydedilen PSD'nin istenen renk modunu veri kaybı olmadan korumasını sağlar.

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

## PSD'yi 16‑bit derinliği koruyarak PNG'ye nasıl dönüştürürsünüz?
`PngOptions`, renk tipi ve sıkıştırma seviyesi gibi PNG çıktı ayarlarını tanımlayan bir sınıftır.  
`PngColorType.GrayscaleWithAlpha`, alfa kanalıyla birlikte 16‑bit gri tonlama verisini depolayan bir enum değeridir.  

Yeni kaydedilen PSD'yi yükleyin, `PngOptions`'ı `PngColorType.GrayscaleWithAlpha` ile yapılandırın ve `save` metodunu çağırın. Bu, PNG dosyası içinde 16‑bit gri tonlama verisini korur ve sonraki işleme veya dağıtıma uygun kayıpsız, yüksek kaliteli bir görüntü sağlar.

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

Artık yüksek kaliteli 16‑bit gri tonlama verisini koruyarak **PSD'yi PNG olarak dışa aktardınız**.

## Yaygın sorunlar ve çözümler
| Sorun | Neden olur | Çözüm |
|-------|------------|-------|
| **“Unsupported color type” exception** | Desteklenmeyen kanal yapılandırmasıyla PSD kaydetmeye çalışmak. | `channelBitsCount`'ın gerçek bit derinliği (16) ile eşleştiğinden ve `channelsCount`'ın gri tonlama için doğru (1) olduğundan emin olun. |
| **File not found** | Yanlış kaynak dizin yolu. | `sourceDir` dizesini iki kez kontrol edin ve PSD dosyasının o konumda mevcut olduğunu doğrulayın. |
| **Output PNG appears black** | PNG, uygun alfa işleme olmadan kaydedildi. | Yukarıda gösterildiği gibi `PngColorType.GrayscaleWithAlpha` kullanın. |
| **Memory overflow on large PSDs** | Tüm dosyanın belleğe yüklenmesi. | Büyük dosyaları verimli işlemek için `PsdImage.load(inputStream, new LoadOptions())` ile akış modunu etkinleştirin. |

## Sıkça Sorulan Sorular

**S: 16‑bit gri tonlama renk modu nedir?**  
C: 65 536 gri tonunu sağlar ve standart 8‑bit (256 ton) renk modundan çok daha fazla tonal detay sunar.

**S: Aspose.PSD'yi gri tonlamalı olmayan görüntüler için kullanabilir miyim?**  
C: Kesinlikle! Aspose.PSD, RGB, CMYK, Lab, Indexed ve birçok diğer renk modunu destekler.

**S: Aspose.PSD'nin deneme sürümü var mı?**  
C: Evet, Aspose.PSD'nin ücretsiz deneme sürümünü deneyebilirsiniz. Sadece [Aspose indirme sayfasına](https://releases.aspose.com/) gidin.

**S: Daha fazla Aspose.PSD örneği nerede bulunabilir?**  
C: Derinlemesine öğreticiler, API referansları ve örnek projeler için resmi [dokümantasyona](https://reference.aspose.com/psd/java/) bakın.

**S: Aspose.PSD için lisans nasıl satın alınır?**  
C: [Aspose satın alma sayfasını](https://purchase.aspose.com/buy) ziyaret ederek lisans satın alabilirsiniz.

**Son Güncelleme:** 2026-09-28  
**Test Edilen Sürüm:** Aspose.PSD for Java 24.12 (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java kullanarak Belirli Bit Derinliğiyle PSD'yi PNG'ye Dönüştür](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Aspose.PSD for Java kullanarak Katman Efektleriyle PSD'yi PNG'ye Dışa Aktar](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD Java ile PSD'yi JPEG olarak Kaydet ve RGB Renk Desteği](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}