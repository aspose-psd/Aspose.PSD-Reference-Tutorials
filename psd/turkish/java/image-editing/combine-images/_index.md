---
date: 2026-06-28
description: Aspose.PSD kullanarak Java ile görselleri nasıl birleştireceğinizi öğrenin,
  iki resmi bir PSD tuvaline birleştirin ve sadece birkaç dakika içinde katmanlı bir
  dosya oluşturun.
keywords:
- combine images java
- java graphics draw image
- merge images into psd
linktitle: Görselleri Birleştir
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  headline: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  type: TechArticle
- description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  name: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  steps:
  - name: Create PSD Options (prepare the file)
    text: '`PsdOptions` holds the configuration for the output PSD, such as compression
      level and color depth.'
  - name: Set the FileCreateSource (define where the PSD will be saved)
    text: '`FileCreateSource` tells Aspose where to write the generated file.'
  - name: Create Image Instance (initialize canvas size)
    text: The `Image` constructor creates a blank PSD canvas with the dimensions you
      specify.
  - name: Initialize Graphics and draw the first picture
    text: '`Graphics` provides drawing capabilities on the canvas. We clear the background
      to white and render the first source image on the left half.'
  - name: Draw the second picture (complete the combine)
    text: Now we place the second image on the right half of the same canvas, creating
      a second layer automatically.
  - name: Save the resulting PSD file
    text: Persist the combined canvas to disk. The resulting `combined.psd` contains
      two editable layers. Congratulations! You have successfully **combine images
      java** and generated a layered PSD file ready for further Photoshop editing.
  type: HowTo
- questions:
  - answer: Aspose.PSD natively reads and writes **15+ formats**, including PSD, PNG,
      JPEG, BMP, TIFF, GIF, and more, making it a versatile choice for image pipelines.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Each `drawImage` call creates a separate PSD layer, which you can
      later reposition, apply filters, or mask using Aspose.PSD’s extensive layer‑editing
      API.
    question: Can I perform additional edits after combining images?
  - answer: A valid license is required for production use. You can obtain one from
      the Aspose store; a free trial is available for evaluation.
    question: Do I need a commercial license for production?
  - answer: Simply repeat `graphics.drawImage(...)` with appropriate coordinates for
      each additional image. Each call adds a new layer.
    question: How do I add more than two pictures?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support, or consult the official documentation linked in the download page.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Görselleri Birleştir Java – Aspose.PSD ile Resimleri Birleştirerek PSD Dosyası
  Oluştur
url: /tr/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile Görüntüleri Birleştir – Aspose.PSD ile Resimleri Birleştirerek PSD Dosyası Oluştur

## Giriş

Eğer birkaç resmi tek bir Photoshop uyumlu dosyada birleştirerek **combine images java** yapmanız gerekiyorsa, Aspose.PSD for Java süreci sorunsuz hâle getirir. Bu öğreticide 600 × 600 piksel bir PSD tuvali oluşturmayı, iki kaynak resmi yan yana çizmeyi ve sonucu katmanlı bir PSD dosyası olarak kaydetmeyi adım adım göstereceğiz. Sonunda bu tekniğin otomatik grafik boru hatları için neden değerli olduğunu ve herhangi bir sayıda görüntüye nasıl genişletebileceğinizi anlayacaksınız.

## Hızlı Yanıtlar
- **PSD'ye görüntü birleştirmek için en iyi kütüphane nedir?** Aspose.PSD for Java.
- **Temel bir birleştirme ne kadar sürer?** Kodu yazıp çalıştırmak yaklaşık 10‑15 dakika sürer.
- **Geliştirme için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim dağıtımları için ticari lisans gereklidir.
- **İki'den fazla görüntü ekleyebilir miyim?** Kesinlikle – her ekstra katman için `drawImage` çağrılarını tekrarlamanız yeterlidir.
- **Hangi Java sürümleri destekleniyor?** Java 8 ve üzeri (Java 21'e kadar).

## combine images java nedir?

*Combine images java*, birden fazla raster resmin Java API'leri kullanılarak programlı bir şekilde tek bir görüntü dosyasında birleştirilmesi anlamına gelir. Aspose.PSD, yerel Photoshop bağımlılıkları olmadan bunu yapmanın yüksek seviyeli, saf Java yolunu sunar; böylece bileşimi otomatikleştirebilir, katmanları koruyabilir ve daha sonra Photoshop veya diğer PSD‑uyumlu araçlarda düzenlenebilen Photoshop uyumlu bir PSD çıktısı alabilirsiniz.

## Aspose.PSD ile görüntüleri neden birleştirirsiniz?

Aspose.PSD, **15+ image formats** (PSD, PNG, JPEG, BMP, TIFF, GIF ve daha fazlası dahil) destekler ve akış mimarisi sayesinde tüm dosyayı belleğe yüklemeden **multi‑hundred‑page documents** işleyebilir. Kütüphane **%100 yönetilen Java**'dır, bu yüzden JDK'yı destekleyen herhangi bir işletim sisteminde çalışır ve yerel DLL sorunlarını ortadan kaldırır.

## Önkoşullar

1. **Aspose.PSD Library** – indirin [buradan](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Java 8+ gereklidir; daha iyi performans için Java 11 veya üzeri önerilir.  
3. **Working Directory** – makinenizde kaynak resimleri (`example1.png`, `example2.png`) içeren ve çıktının PSD (`combined.psd`) yazılacağı bir klasör.  
4. **License Purchase** – üretim kullanımı için bir ticari lisans edinin [buradan](https://purchase.aspose.com/buy).  
5. **Other Aspose Releases** – ek ürün ve güncellemeleri keşfedin [buradan](https://releases.aspose.com/).

## Paketleri İçe Aktar

`import` ifadeleri, gerekli Aspose.PSD sınıflarını kapsam içine getirir.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdOptions;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.PsdImageLayer;
import com.aspose.psd.imageoptions.FileCreateSource;
import com.aspose.psd.graphics.Graphics;
import com.aspose.psd.Color;
```

## Aspose.PSD kullanarak combine images java nasıl birleştirilir?

Boş bir tuval yükleyin, her resmi tuval üzerine çizin ve ardından sonucu bir PSD dosyası olarak kaydedin – bu, üç kısa adımda tüm iş akışıdır. API, her `drawImage` çağrısı için otomatik olarak ayrı bir katman oluşturur ve böylece Photoshop'ta daha sonra tam düzenlenebilirlik sağlar.

### Adım 1: PSD Seçeneklerini Oluştur (dosyayı hazırlama)

`PsdOptions`, sıkıştırma seviyesi ve renk derinliği gibi çıktı PSD'sinin yapılandırmasını tutar.

```java
PsdOptions psdOptions = new PsdOptions();
```

### Adım 2: FileCreateSource'ı Ayarla (PSD'nin nereye kaydedileceğini tanımla)

`FileCreateSource`, Aspose'a oluşturulan dosyanın nereye yazılacağını bildirir.

```java
psdOptions.setSource(new FileCreateSource(dataDir + "combined.psd", false));
```

### Adım 3: Image Örneği Oluştur (tuval boyutunu başlat)

`Image` yapıcı metodu, belirttiğiniz boyutlarda boş bir PSD tuvali oluşturur.

```java
Image image = new Image(psdOptions, 600, 600);
```

### Adım 4: Graphics'i Başlat ve İlk Resmi Çiz

`Graphics`, tuval üzerinde çizim yetenekleri sağlar. Arka planı beyaza temizliyoruz ve ilk kaynak resmi sol yarıya render ediyoruz.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(dataDir + "example1.png", new Rectangle(0, 0, 300, 600));
```

### Adım 5: İkinci Resmi Çiz (birleştirmeyi tamamla)

Şimdi aynı tuvalin sağ yarısına ikinci resmi yerleştiriyoruz, bu da otomatik olarak ikinci bir katman oluşturur.

```java
graphics.drawImage(dataDir + "example2.png", new Rectangle(300, 0, 300, 600));
```

### Adım 6: Oluşan PSD Dosyasını Kaydet

Birleştirilmiş tuvali diske kaydedin. Oluşan `combined.psd` iki düzenlenebilir katman içerir.

```java
image.save();
```

Tebrikler! Başarıyla **combine images java** yaptınız ve daha fazla Photoshop düzenlemesi için hazır katmanlı bir PSD dosyası oluşturdunuz.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| `File not found` kaynak resimler yüklenirken | Yanlış `dataDir` yolu | `dataDir`'in `example1.png` ve `example2.png` içeren klasöre işaret ettiğini doğrulayın. |
| Çıktı PSD boş | `graphics.clear` çizimden sonra çağrıldı | `graphics.clear(Color.getWhite())` çağrısını **herhangi bir** `drawImage` işleminden **önce** yapın. |
| Çalışma zamanında lisans istisnası | Eksik veya süresi dolmuş Aspose.PSD lisansı | Geçerli bir lisansı, herhangi bir API çağrısından önce `License license = new License(); license.setLicense("Aspose.PSD.lic");` kullanarak uygulayın. |

## Sıkça Sorulan Sorular

**Q: Aspose.PSD tüm görüntü formatlarıyla uyumlu mu?**  
A: Aspose.PSD, PSD, PNG, JPEG, BMP, TIFF, GIF ve daha fazlası dahil **15+ format**ı yerel olarak okur ve yazar, bu da onu görüntü boru hatları için çok yönlü bir seçim yapar.

**Q: Görüntüleri birleştirdikten sonra ek düzenlemeler yapabilir miyim?**  
A: Evet. Her `drawImage` çağrısı ayrı bir PSD katmanı oluşturur; bu katmanı daha sonra konumlandırabilir, filtre uygulayabilir veya Aspose.PSD’nin kapsamlı katman‑düzenleme API'siyle maskeleme yapabilirsiniz.

**Q: Üretim için ticari lisansa ihtiyacım var mı?**  
A: Üretim kullanımında geçerli bir lisans gereklidir. Bir lisansı Aspose mağazasından temin edebilirsiniz; değerlendirme için ücretsiz deneme mevcuttur.

**Q: İki'den fazla resim eklemek nasıl yapılır?**  
A: Her ek resim için uygun koordinatlarla `graphics.drawImage(...)` kodunu tekrarlamanız yeterlidir. Her çağrı yeni bir katman ekler.

**Q: Sorun yaşarsam nereden yardım alabilirim?**  
A: Topluluk desteği için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin veya indirme sayfasındaki resmi belgelere bakın.

---

**Son Güncelleme:** 2026-06-28  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Aspose.PSD for Java'da Yolu Ayarlayarak Görüntü Oluştur](/psd/java/image-editing/create-image-by-setting-path/)
- [Aspose.PSD for Java'da Akış Kullanarak Görüntü Oluştur](/psd/java/image-editing/create-image-using-stream/)
- [Java'da Görüntüyü Yeniden Boyutlandır - Aspose.PSD for Java'da Yeniden Boyutlandırma Türü Enumsiyonu Kullanarak](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

```java
PsdOptions imageOptions = new PsdOptions();
```

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

```java
Image image = Image.create(imageOptions, 600, 600);
```

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

```java
image.save();
```