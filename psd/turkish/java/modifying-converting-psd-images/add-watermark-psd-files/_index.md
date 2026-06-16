---
date: 2026-03-07
description: Aspose.PSD for Java kullanarak PSD dosyalarına görüntü filigranı eklemeyi
  öğrenin – PSD görüntü işleme ve grafiklerinizi koruma konusunda hızlı bir rehber.
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile PSD Dosyalarına Görüntü Filigranı Nasıl Oluşturulur
url: /tr/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile PSD Dosyalarına Filigran Ekleme

## Giriş
Filigranlar, görüntülerinizi korumanın ve sahipliği iletmenin ince ama etkili bir yoludur. Bu öğreticide, Aspose.PSD for Java kullanarak PSD dosyalarında **create image watermark** oluşturmayı öğreneceksiniz. Portföyünüzü sergileyen bir fotoğrafçı ya da son çalışmalarını sunan bir tasarımcı olun, bir filigran eklemek marka kimliğinizi korumak için çok önemli olabilir. O halde bir fincan kahve alın, rahatlayın ve başlayalım!

## Hızlı Yanıtlar
- **Ana hedef nedir?** Programlı olarak bir PSD dosyasında image watermark oluşturmak.  
- **Hangi kütüphane kullanılıyor?** Aspose.PSD for Java.  
- **Uygulama ne kadar sürer?** Temel bir filigran için yaklaşık 10‑15 dakika.  
- **Ana önkoşullar nelerdir?** Java JDK, Aspose.PSD kütüphanesi ve bir kaynak PSD dosyası.  
- **Sonucu PNG olarak dışa aktarabilir miyim?** Evet – `save` metodunu `PngOptions` ile kullanın.

## **create image watermark** nedir?
Bir image watermark oluşturmak, sahiplik bilgisinin doğrudan görsel içeriğe yerleştirilmesi için görüntü dosyasının üzerine yarı saydam metin veya grafiklerin programlı olarak bindirilmesi anlamına gelir.

## psd görüntü işleme için Aspose.PSD for Java neden kullanılmalı?
Aspose.PSD, **psd image processing** için zengin bir API seti sunar; katmanları manipüle etmenize, efektler uygulamanıza ve Photoshop'a ihtiyaç duymadan son görüntüyü oluşturmanıza olanak tanır. Yüksek doğrulukta render, toplu işlemler ve tüm büyük işletim sistemlerinde çalışır.

## Önkoşullar
Koda başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – herhangi bir güncel sürüm (8 veya üzeri).  
2. **Aspose.PSD for Java Library** – [Aspose web sitesinden](https://releases.aspose.com/psd/java/) indirin.  
3. **IDE** – Eclipse, IntelliJ IDEA veya tercih ettiğiniz herhangi bir editör.  
4. **PSD File** – çalışma dizininizde `layers.psd` adlı örnek bir dosya.  
5. **Basic Java knowledge** – sınıflar, nesneler ve dosya I/O konularına aşinalık.

## Paketleri İçe Aktarma
Her şeyi kurduğunuza göre, gerekli paketleri içe aktaralım. Java'da importlar, çeşitli kütüphanelerden sınıf ve fonksiyonları getirmenizi sağlar ve kodunuzu daha verimli kılar. Aşağıda ihtiyacınız olanlar yer alıyor:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## **create image watermark** Nasıl Yapılır – Adım‑Adım Kılavuz

### Adım 1: Dizinini Ayarla
İlk olarak, PSD dosyanızın bulunduğu yolu ayarlamamız gerekiyor. Bu, Java'nın dosyalarınızı nerede bulacağını bilmesi açısından kritiktir.

```java
String dataDir = "Your Document Directory";
```

`Your Document Directory` ifadesini `layers.psd` dosyasını içeren gerçek klasörle değiştirin.

### Adım 2: PSD Dosyasını Yükle
Sonra, PSD dosyasını yükleyecek ve `PsdImage` tipine dönüştüreceğiz. Bu adım, dosyayı manipüle edebileceğimiz bir formata çevirir.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Bunu, sayfalarına yazmaya başlayabileceğiniz bir kitabı açmak gibi düşünün.

### Adım 3: Graphics Nesnesi Oluştur
PSD dosyamız yüklendiğine göre, bir `Graphics` nesnesi oluşturmamız gerekiyor. Bu, çizim işlemleri yapmamızı sağlar—temelde tuvaliniz için bir fırça almış gibi.

```java
Graphics graphics = new Graphics(psdImage);
```

### Adım 4: Filigranınız İçin Yazı Tipini Tanımla
Şimdi filigranınızın nasıl görüneceğini seçme zamanı. Arial yazı tipini 20 punto ile kullanacağız. Yazı tipi adını veya boyutunu marka stilinize göre değiştirmekten çekinmeyin.

```java
Font font = new Font("Arial", 20.0f);
```

### Adım 5: Filigran İçin Katı Fırça Oluştur
Katı bir fırça, filigranınıza renk ve opaklık verir. Yarı saydam gri için alfa değerini 255 üzerinden 50 olarak ayarlayacağız.

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

Burada, `Color.fromArgb(50, 128, 128, 128)` %50 opaklığa sahip bir gri renk oluşturur—ince bir imza için mükemmel.

### Adım 6: Filigranınız İçin Metin Hizalamasını Ayarla
Filigranın görüntünün tam ortasında görünmesini sağlamak için metin hizalama seçeneklerini yapılandıracağız.

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### Adım 7: Filigranı **java graphics drawstring** ile Çiz
Şimdi heyecan verici bölüme geldik. Grafik bağlamı hazır olduğunda, `java graphics drawstring` kullanarak filigran metnini görüntüye çizeceğiz.

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

`"Some watermark text"` ifadesini PSD'de görünmesini istediğiniz gerçek metinle değiştirin.

### Adım 8: **Save PSD as PNG** – **export psd png**
Filigran yerleştirildiğine göre, **save psd png** (yani PSD'yi PNG olarak dışa aktar) yapacağız, böylece sonuç herhangi bir tarayıcı veya görüntüleyicide görüntülenebilir.

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

Bu satırı çalıştırmak, filigranınızı içeren yeni bir PNG dosyası oluşturur.

## Yaygın Sorunlar ve Çözümler
- **Filigran görünmüyor mu?** `Color.fromArgb()` içindeki alfa değerini kontrol edin; daha düşük bir değer filigranı daha şeffaf yapar.  
- **Yanlış boyutlar?** Dikdörtgen için `psdImage.getWidth()` ve `psdImage.getHeight()` kullandığınızdan emin olun, böylece metin görüntü boyutuna göre ölçeklenir.  
- **Lisans istisnaları?** Geçici bir değerlendirme lisansı test için çalışır, ancak üretim kullanımı için tam lisans gereklidir.

## Sıkça Sorulan Sorular

**S: Filigran metnini özelleştirebilir miyim?**  
C: Kesinlikle! `drawString` metodundaki dizeyi istediğiniz metinle değiştirmeniz yeterli.

**S: Farklı bir font istesem ne olur?**  
C: `Font` nesnesinin oluşturulmasını herhangi bir yüklü fonta değiştirin, örneğin `new Font("Times New Roman", 24.0f)`.

**S: Opaklığı ayarlamanın bir yolu var mı?**  
C: Evet—`Color.fromArgb(alpha, r, g, b)`'nin ilk parametresini değiştirin. Daha düşük `alpha` değerleri şeffaflığı artırır.

**S: PNG dışında başka görüntü formatları kullanabilir miyim?**  
C: Elbette. `new PngOptions()` ifadesini `new JpegOptions()` ya da `new BmpOptions()` ile değiştirerek **save psd png**'i farklı bir formatta kaydedebilirsiniz.

**S: Daha fazla yardımı nereden bulabilirim?**  
C: Ayrıntılı sorular için [Aspose forumlarını](https://forum.aspose.com/c/psd/34) ziyaret edin ya da [dökümantasyonlarına](https://reference.aspose.com/psd/java/) bakın.

## Sonuç
Artık Aspose.PSD for Java kullanarak bir PSD dosyasında **create image watermark** nasıl yapılacağını öğrendiniz. Bu teknik, içeriğinizi korumanın yanı sıra tüm görsel varlıklarınızda marka varlığınızı güçlendirir. Farklı fontlar, renkler ve opaklık seviyeleriyle denemeler yapın ve **save psd png** ya da **export psd png**'i ihtiyacınız olan herhangi bir formata dönüştürebileceğinizi unutmayın.

---

**Son Güncelleme:** 2026-03-07  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}