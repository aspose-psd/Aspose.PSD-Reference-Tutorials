---
date: 2026-01-17
description: Aspose.PSD for Java kullanarak Java grafiklerinde yay çizimini öğrenin.
  Grafik uygulamaları için kod örnekleriyle adım adım öğretici.
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: Java Grafiklerinde Aspose.PSD ile Yay Çizme – Adım Adım Kılavuz
url: /tr/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD ile Java Grafik Çizgi Arkı

## Giriş
Bu öğreticide, Aspose.PSD for Java kütüphanesi ile **java graphics draw arc** nasıl yapılacağını keşfedeceksiniz. Arkları programlı olarak çizmek, özel UI bileşenleri, veri görselleştirmeleri veya hassas eğri kontrolü gerektiren herhangi bir grafik için kullanışlıdır. Projeyi kurmaktan arkı render etmeye ve sonucu kaydetmeye kadar her adımı adım adım göstereceğiz—böylece bu yeteneği Java uygulamalarınıza hemen ekleyebilirsiniz.

## Hızlı Yanıtlar
- **Java'nın arkları kolayca çizmeye yarayan kütüphane hangisidir?** Aspose.PSD for Java.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü çalışır; üretim için lisans gereklidir.  
- **Hangi çıktı formatları destekleniyor?** BMP, PNG, JPEG, TIFF, GIF ve daha fazlası.  
- **Arc kalınlığını veya rengini değiştirebilir miyim?** Evet—`Pen` nesnesinin özelliklerini ayarlayın.  
- **Kod Java 8+ ile uyumlu mu?** Kesinlikle, API Java 8 ve üzerini hedefler.

## “java graphics draw arc” nedir?
Bu ifade, Java kodu kullanarak bir grafik tuvaline eğri bir segment (ark) çizmek anlamına gelir. Aspose.PSD ile, çizim işlemlerini basitleştiren, renk yönetimi, anti‑aliasing ve dosya dışa aktarmayı arka planda yöneten yüksek seviyeli bir `Graphics` sınıfı elde edersiniz.

## Arc çizimi için neden Aspose.PSD kullanmalı?
- **Tam PSD desteği** – Photoshop yüklü olmadan Photoshop dosyaları oluşturun veya düzenleyin.  
- **Zengin çizim API’si** – `drawArc` gibi yöntemler, boyut, açı ve stil ayarlarını tek bir çağrıda belirlemenizi sağlar.  
- **Çapraz format dışa aktarım** – Arkınızı birkaç satır kodla BMP, PNG, JPEG vb. formatlarda kaydedin.  
- **Performansa odaklı** – Büyük görüntüler ve toplu işleme için optimize edilmiştir.

## Önkoşullar
1. **Java Geliştirme Ortamı** – Java (JDK 8 veya daha yeni) kurun. [Oracle'ın web sitesinden](https://www.oracle.com/java/) indirin.  
2. **Aspose.PSD for Java** – Kütüphaneyi [indirme sayfasından](https://releases.aspose.com/psd/java/) alın ve JAR dosyasını projenizin sınıf yoluna ekleyin.

## Paketleri İçe Aktarma
İlk olarak, gerekli Aspose.PSD sınıflarını kapsam içine getirin:

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

Bu içe aktarmalar, renk tanımları, çizim araçları, görüntü kapsayıcıları ve dosya kaydetme seçeneklerine erişmenizi sağlar.

## Adım Adım Kılavuz

### Adım 1: Java Projenizi Kurun
Yeni bir Maven veya Gradle projesi oluşturun, Aspose.PSD JAR dosyasını ekleyin ve IDE'nin içe aktarmaları hatasız çözdüğünden emin olun.

### Adım 2: Görüntü ve Grafik Nesnelerini Başlatın
Boş bir `PsdImage` tuvali ve üzerine çizecek bir `Graphics` örneği oluşturun:

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

`"Your Document Directory"` ifadesini çıktının kaydedileceği klasörle değiştirin.

### Adım 3: Ark Parametrelerini Tanımlayın
Arkı şekillendiren boyut ve açıları belirtin:

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

İhtiyacınız olan görsel stile uyacak şekilde bu sayıları istediğiniz gibi ayarlayabilirsiniz.

### Adım 4: Arkı Çizin ve Kaydedin
`drawArc` metodunu kullanın, ardından görüntüyü dışa aktarın:

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

Kod, sarı bir arka plan üzerinde siyah bir ark çizer ve sonucu `Arc.bmp` dosyasına yazar. Farklı bir format veya kalite tercih ediyorsanız `outputPath` ve `BmpOptions` değerlerini değiştirin.

## Yaygın Sorunlar ve Çözümler
- **Dosya bulunamadı hatası** – `dataDir`'in bir yol ayırıcı (`/` veya `\\`) ile bittiğinden ve dizinin mevcut olduğundan emin olun.  
- **Arc bir çizgi gibi görünüyor** – `width` ve `height` değerlerinin sıfırdan büyük olduğundan ve `sweepAngle`'ın 360°'nin katı olmadığından (tam bir elips çizer) emin olun.  
- **Renk uygulanmadı** – Etkiyi daha net görmek için `new Pen(Color.getRed())` kullanın veya `pen.setWidth(2)` ayarlayın.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java, ark dışında başka şekilleri de işleyebilir mi?**  
A: Evet, aynı `Graphics` API'si aracılığıyla dikdörtgenler, elipsler, çizgiler ve özel yolları destekler.

**S: Arkın kalınlığını veya rengini nasıl değiştiririm?**  
A: İstediğiniz `Color` ve `Width` değerleriyle (örneğin `new Pen(Color.getBlue(), 3)`) bir `Pen` oluşturun ve `drawArc` metoduna geçirin.

**S: Arcı BMP dışındaki formatlara dışa aktarmak mümkün mü?**  
A: Kesinlikle. `BmpOptions` yerine `PngOptions`, `JpegOptions`, `TiffOptions` vb. kullanın.

**S: Daha fazla örnek ve destek nereden bulunabilir?**  
A: [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin; topluluk yardımı, resmi dokümantasyon ve kod örnekleri bulabilirsiniz.

## Sonuç
Artık Aspose.PSD for Java kullanarak **java graphics draw arc** nasıl yapılır konusunda eksiksiz, üretime hazır bir örneğe sahipsiniz. Parametreleri, kalem ayarlarını ve çıktı seçeneklerini ayarlayarak, özel arkları herhangi bir Java tabanlı grafik iş akışına entegre edebilirsiniz.

---

**Son Güncelleme:** 2026-01-17  
**Test Edilen Sürüm:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}