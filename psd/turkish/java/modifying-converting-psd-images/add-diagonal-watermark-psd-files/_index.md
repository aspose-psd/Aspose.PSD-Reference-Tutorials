---
date: 2026-03-04
description: Aspose.PSD kullanarak Java’da grafik nesnesi oluşturmayı ve PSD dosyalarına
  çapraz bir filigran eklemeyi öğrenin. Bu adım adım rehber, Java görüntü filigran
  kütüphanesinin kullanımını kapsar.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: Java’da Grafik Nesnesi Oluştur – PSD için Çapraz Filigran
url: /tr/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile PSD Dosyalarına Çapraz Filigran Ekleme

## Giriiş
Bu öğreticide **grafik nesnesi oluşturma java** oluşturacak ve bunu PSD dosyalarını çapraz bir filigran seçmek için kullanacaksınız. İster işinizi koruyan bir tasarımcı, ister görsellere marka ekleyen bir pazarlamacı olun, temiz bir filigran çalışmanızı profesyonel ve güvenli gösterir. Her adımı net açıklamalarla anlatacağız, bu sayede teknolojiyi kendi projelerinizde özetle uygulayabilirsiniz.

## Hızlı Yanıtlar
- **Hangi kütüphaneye ihtiyacım var?** Aspose.PSD for Java (sağlam bir Java resim filigran kütüphanesi).
- **Bu eğitim hangi birincil anahtar kelimeyi kapsıyor?** Java grafik nesnesi oluşturun.
- **Lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test amacıyla çalışır; Üretim için ticari lisans gereklidir.
- **Filigran metnini ve stilini değiştirebilir miyim?** Evet – yazı tipini, rengi, opaklığı ve döndürmeyi özelleştirebilirsiniz.
- **Hangi çıktı formatları destekleniyor?** Örnek PNG olarak kaydediliyor, ancak Aspose.PSD PSD, JPEG, BMP ve daha fazlasına dışa aktarabiliyor.

## Java'da Grafik Nesnesi Nedir?

Bir **Grafik** nesnesi, bir görüntü için çizim yüzeyini temsil eder. Bir grafik nesnesi oluşturarak, metin, şekiller ve diğer görsel öğeleri doğrudan bitmap veya PSD tuvaline işlemenizi sağlayan yöntemlere erişim kazanırsınız. Bu, **create graphics object java** anahtar kelimesinin ardındaki temel kavramdır.

## Filigranlama için Aspose.PSD Neden Kullanılmalı?

Aspose.PSD, Adobe Photoshop olmadan çalışan özel bir **Java görüntü filigran kütüphanesidir**. Katmanlar, metin işleme ve görüntü dönüşümleri üzerinde tam kontrol sağlar ve bu da onu sunucu tarafı işleme veya toplu işlemler için ideal hale getirir.

## Önkoşullar
Koda geçmeden önce şunlara sahip olduğunuzdan emin olun:

### 1. Java Geliştirme Ortamı
En son JDK'yı [Java web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) yükleyin.

### 2. Aspose.PSD Kütüphanesi
Kütüphaneyi [Aspose İndirmeler sayfasından](https://releases.aspose.com/psd/java/) indirin. JAR dosyasını Maven, Gradle veya manuel sınıf yolu ekleme yoluyla projenize ekleyin.

### 3. Java'nın Temel Anlayışı
Sınıflar, nesneler ve dosya G/Ç'ye aşinalık, sorunsuz bir şekilde ilerlemenize yardımcı olacaktır.

### 4. IDE Kurulumu
Rahat bir kodlama deneyimi için IntelliJ IDEA, Eclipse veya NetBeans kullanın.

## Paketleri İçe Aktarma
PSD dosyalarını düzenlemek için gerekli Aspose.PSD sınıflarını içe aktarın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Now that we have our prerequisites sorted and the necessary packages imported, let’s walk through the steps to add a diagonal watermark to a PSD file.

## Adım 1: Dizininizi Kurun
```java
String dataDir = "Your Document Directory";
```
Replace `"Your Document Directory"` with the folder path that holds your PSD source file.

## Adım 2: PSD Dosyasını Yükleyin
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
The `Image.load` method reads the file and casts it to a `PsdImage` so we can work with PSD‑specific features.

## Adım 3: Bir Grafik Nesnesi Oluşturun
```java
Graphics graphics = new Graphics(psdImage);
```
Here we **create graphics object java**—the canvas on which we’ll draw the watermark.

## Adım 4: Filigran İçin Bir Yazı Tipi Oluşturun
```java
Font font = new Font("Arial", 20.0f);
```
Pick any installed font; the size controls how prominent the watermark appears.

## Adım 5: Filigran İçin Bir Fırça Oluşturun
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
The `alpha` value (first parameter) sets transparency. An alpha of 50 gives a subtle, semi‑transparent look.

## Adım 6: Dönüştürme Matrisini Kurun
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
We rotate the drawing surface 45° around the image center, creating the diagonal effect.

## Adım 7: Dize Hizalamasını Tanımlayın
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
Center alignment ensures the watermark sits nicely in the middle of the rotated rectangle.

## Adım 8: Filigranı Çizin
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
Replace `"Some watermark text"` with your brand name or copyright notice. The rectangle defines where the text is rendered.

## Adım 9: Resmi Kaydedin
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
The output is saved as PNG, but you can choose any format supported by Aspose.PSD.

## Yaygın Kullanım Alanları
- **Marka koruması:** Yetkisiz yeniden kullanımı önlemek için yarı saydam bir logo ekleyin.

- **Toplu işlem:** Sunucudaki büyük resim kütüphaneleri için filigran eklemeyi otomatikleştirin.

- **Yaratıcı önizlemeler:** Orijinal dosyaları değiştirmeden, filigranlı taslakları müşterilerinize gösterin.

## Sorun Giderme ve İpuçları
- **Saydamlık görünmüyor mu?** Daha güçlü bir filigran için alfa değerini (örneğin, `100`) artırın.

- **Filigran merkezden uzak mı görünüyor?** Döndürme noktasının resmin tam genişlik/yükseklik bölümünü kullandığından emin olun.

- **Performans sorunları:** Bir döngüde birden fazla resim işlerken aynı `Graphics` nesnesini yeniden kullanın.

## SSS

### Aspose.PSD nedir?
Aspose.PSD, Adobe Photoshop gerektirmeden PSD dosyalarıyla çalışmak ve bunları manipüle etmek için kullanılan bir Java kütüphanesidir.

### Filigran için başka yazı tipleri kullanabilir miyim?
Evet, sisteminizde yüklü olan herhangi bir yazı tipini filigran için kullanabilirsiniz.

### Filigranın şeffaflığını özelleştirmenin bir yolu var mı?
Kesinlikle! Şeffaflığı değiştirmek için SolidBrush'taki alfa değerini ayarlayabilirsiniz.

### Birden fazla filigran ekleyebilir miyim?
Evet, daha fazla filigran eklemek için `drawString` yöntemini farklı parametrelerle birden fazla kez çağırabilirsiniz.

### Aspose.PSD hakkında daha fazla bilgiyi nerede bulabilirim?
Belgeleri [burada](https://reference.aspose.com/psd/java/) inceleyebilirsiniz.

---

**Son Güncelleme:** 2026-03-04
**Test Edilen Sürüm:** Aspose.PSD 24.12 for Java
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}