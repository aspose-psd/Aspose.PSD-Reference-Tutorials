---
date: 2026-03-26
description: Aspose.PSD for Java kullanarak psd katmanlarını png'ye dışa aktarmayı
  öğrenin. Psdi raster görüntülere dönüştürün ve psd katmanlarını toplu olarak verimli
  bir şekilde dışa aktarın.
linktitle: Export psd layers to png using Java
second_title: Aspose.PSD Java API
title: Java kullanarak psd katmanlarını png'ye aktar
url: /tr/java/psd-image-modification-conversion/export-psd-layers-raster-images/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java kullanarak psd katmanlarını png olarak dışa aktar

## Giriş

Dijital tasarım dünyasında, katmanlı görüntülerle çalışmak hem bir avantaj hem de bir zorluk olabilir. Photoshop’ta (PSD formatı) birden fazla katmanla tasarımınızı hayata geçiren harika bir görsel oluşturmak için saatler harcadığınızı hayal edin. Şimdi, bu katmanları **psd katmanlarını png olarak dışa aktarmak** isteyebilirsiniz. İşte Aspose.PSD for Java devreye giriyor; bir PSD dosyasındaki her katmanı yüksek kalitede PNG gibi raster görüntülere dönüştürme görevini otomatikleştiriyor. Bu kapsamlı rehberde, ortamınızı kurmaktan sadece birkaç satır kodla psd katmanlarını toplu olarak dışa aktarmaya kadar tüm süreci adım adım göstereceğiz.

## Hızlı Yanıtlar
- **Bu öğretici neyi kapsıyor?** Aspose.PSD for Java kullanarak her PSD katmanını bir PNG dosyasına dışa aktarmak.  
- **Ana fayda?** Photoshop’ta manuel olarak katmanları çıkarmaya kıyasla saatler tasarruf sağlar.  
- **Önkoşullar?** JDK 8+, Aspose.PSD kütüphanesi ve bir örnek PSD dosyası.  
- **Diğer raster formatlarına dışa aktarım mümkün mü?** Evet – BMP, TIFF veya JPEG gibi raster formatlarına da dönüştürebilirsiniz.  
- **Toplu işleme destekleniyor mu?** Kesinlikle; kod içindeki döngü, psd katmanlarını tek bir çalıştırmada toplu dışa aktarmanızı sağlar.

## “psd katmanlarını png’ye” nedir?
**psd katmanlarını png olarak dışa aktarmak**, bir Photoshop belgesindeki her ayrı katmanı ayrı bir PNG görüntüsü olarak kaydetmek anlamına gelir. PNG, şeffaflığı korur ve web grafikleri, UI varlıkları ve ileri görüntü işleme için idealdir.

## Neden Aspose.PSD for Java kullanmalı?
- **Photoshop gerekmez** – herhangi bir sunucu veya CI ortamında çalışır.  
- **Yüksek doğruluk** – katman efektleri, maskeler ve alfa kanallarını korur.  
- **Ölçeklenebilir** – otomatikleştirilmiş hatlarda psd katmanlarını toplu dışa aktarmak için mükemmeldir.  

## Önkoşullar

Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **Aspose.PSD for Java** – en yeni kütüphaneyi [Aspose Releases](https://releases.aspose.com/psd/java/) adresinden indirin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Örnek PSD dosyası** – ör. `sample.psd`, proje klasörünüzde bulunmalı.

Şimdi her şey hazır, kodlamaya başlayalım!

## Paketleri İçe Aktar

İlk olarak, Aspose.PSD kütüphanesinden ihtiyacınız olan sınıfları içe aktarın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Bu importlar, görüntü yükleme, PNG seçenekleri ve katman manipülasyonu işlevlerine erişmenizi sağlar.

## Adım 1: Belge Dizinini Tanımlayın

Kaynak PSD ve ortaya çıkan PNG dosyalarının bulunduğu konumu belirtin:

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini `sample.psd` dosyanızın mutlak ya da göreli yolu ile değiştirin.

## Adım 2: PSD Dosyasını Yükleyin

PSD dosyasını bir `PsdImage` nesnesine yükleyin, böylece katmanlarıyla çalışabilirsiniz:

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

`PsdImage` tipine dönüştürmek, katmana özgü işlevselliği açar.

## Adım 3: PNG Seçeneklerini Yapılandırın

PNG dışa aktarma parametrelerini ayarlayın. `TruecolorWithAlpha` kullanmak şeffaflığı korur:

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Adım 4: Katmanları Döngüyle Gezin ve Her Birini Dışa Aktarın

Her katmanı tek tek dolaşarak ayrı bir PNG dosyası olarak kaydedin. Bu döngü, **psd katmanlarını toplu dışa aktarmayı** otomatikleştirir:

```java
for (int i = 0; i < psdImage.getLayers().length; i++) {
    // Convert and save the layer to PNG file format.
    psdImage.getLayers()[i].save(dataDir + String.format("layer_out%d.png", i + 1), pngOptions);
}
```

Her yineleme `layer_out1.png`, `layer_out2.png` vb. dosyalarını üretir.

## Yaygın Sorunlar ve Çözümler

- **FileNotFoundException** – `dataDir`'in doğru klasöre işaret ettiğinden ve `sample.psd` dosyasının mevcut olduğundan emin olun.  
- **OutOfMemoryError** – Çok büyük PSD dosyaları için katmanları daha küçük partilerde işleyin veya JVM yığın boyutunu (`-Xmx`) artırın.  
- **Şeffaflık Eksik** – `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)` ayarının yapıldığından emin olun; aksi takdirde PNG alfa kanalı olmadan kaydedilir.

## Sıkça Sorulan Sorular

### Aspose.PSD for Java nedir?
Aspose.PSD for Java, geliştiricilerin Adobe Photoshop’a ihtiyaç duymadan Photoshop dosyaları oluşturmasına, değiştirmesine, dönüştürmesine ve render etmesine olanak tanıyan güçlü bir kütüphanedir.

### Katmanları PNG dışındaki formatlara dışa aktarabilir miyim?
Evet, Aspose.PSD BMP, TIFF, JPEG ve birçok diğer raster formatını destekler. İlgili seçenek sınıfını (ör. `JpegOptions`) oluşturup `save` metoduna geçirmeniz yeterlidir.

### Aspose.PSD için ücretsiz deneme sürümü var mı?
Kesinlikle! Aspose.PSD’yi ücretsiz olarak denemek için [free trial page](https://releases.aspose.com/) adresinden indirebilirsiniz.

### Aspose.PSD kullanırken sorunlarla karşılaşırsam ne yapmalıyım?
Aspose topluluğundan yardım ve destek alabilirsiniz. Destek forumlarını [buradan](https://forum.aspose.com/c/psd/34) ziyaret edin.

### Aspose.PSD için lisans nereden satın alınabilir?
Aspose.PSD lisansını satın almak için [buradaki](https://purchase.aspose.com/buy) satın alma sayfasını kullanabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-26  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose