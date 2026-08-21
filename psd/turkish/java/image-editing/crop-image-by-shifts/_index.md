---
date: 2026-07-03
description: Aspose.PSD for Java kullanarak Java'da görüntüyü nasıl kırpacağınızı
  öğrenin. Bu adım adım görüntü kırpma öğreticisi, PSD dosyalarının yüklenmesi, kaydırma
  değerlerinin ayarlanması ve sonucun kaydedilmesini kapsar.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Shift'lerle Görüntü Kırpma
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Shift'lerle Görüntü Kırpma Java, Aspose.PSD ile
url: /tr/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kaydırmalarla Java’da Görüntü Kırpma Aspose.PSD ile

## Giriş

Java görüntü işleme içinde, **crop image java** grafikler, küçük resimler veya UI varlıkları hazırlamak için yaygın bir gereksinimdir. Aspose.PSD for Java, desteklenen herhangi bir raster formatında çalışan basit bir `crop` yöntemi sunarak bu görevi kolaylaştırır. Bu öğreticide bir PSD dosyasını nasıl yükleyeceğinizi, sol‑sağ‑üst‑alt kaydırma değerlerini nasıl tanımlayacağınızı, kırpmayı nasıl uygulayacağınızı ve sonucu nasıl kaydedeceğinizi öğreneceksiniz — özel piksel‑manipülasyon kodu yazmadan.

## Hızlı Yanıtlar
- **Kırpmayı hangi kütüphane yönetir?** Aspose.PSD for Java provides a built‑in `crop` method.  
- **Lisans gereklimi?** A temporary license works for evaluation; a full license is required for production.  
- **Desteklenen formatlar?** Over 30 raster formats, including PSD, JPEG, PNG, BMP, and TIFF.  
- **Maksimum dosya boyutu?** Handles files up to 2 GB without loading the entire image into memory.  
- **Kaç satır kod?** Only five logical steps—load, cache, define shifts, crop, and save.

## crop image java nedir?
`crop image java`, bir Java uygulamasında bitmap kırpma işlemini ifade eder. Aspose.PSD kullanarak, bu işlem `crop` yöntemiyle gerçekleştirilir; yöntem, görüntünün her bir kenarı için kaydırma değerlerini alır ve yeni bir görüntü örneği döndürür.

## Neden Aspose.PSD'yi görüntü kırpmak için kullanmalısınız?
Aspose.PSD, **30+** görüntü formatını destekler ve çok sayfalı PSD dosyalarını 150 MB'den az RAM kullanarak işleyebilir, çünkü tembel‑yükleme mimarisine sahiptir. Kütüphane ayrıca piksel‑tam sonuçlar garantiler, katmanları, maskeleri ve renk profillerini korur — birçok genel görüntü kütüphanesinin sağlayamadığı bir şey.

## Önkoşullar

### Java Geliştirme Kiti (JDK)

Sisteminizde en son JDK sürümünün yüklü olduğundan emin olun. [buradan](https://www.oracle.com/java/technologies/javase-downloads.html) indirebilirsiniz.

### Aspose.PSD for Java Kütüphanesi

Başlamak için Aspose.PSD for Java kütüphanesini edinmeniz gerekir. [indirme sayfasına](https://releases.aspose.com/psd/java/) gidin ve en son sürümü alın.

### Entegre Geliştirme Ortamı (IDE)

Eclipse veya IntelliJ gibi favori Java IDE'nizi seçerek sorunsuz bir kodlama deneyimi elde edin.

## crop image java nasıl kırpılır?

Kaynak dosyanızı yükleyin, her bir kenar için piksel kaydırma değerlerini tanımlayın ve `crop` yöntemini çağırın — bu tüm iş akışı beş kısa satır kodla yazılabilir. `crop` işlemi, yalnızca belirttiğiniz bölgeyi içeren yeni bir görüntü oluşturur ve orijinal dosyayı dokunulmaz bırakır.

### Adım 1: Görüntüyü Yükle

`Image`, Aspose.PSD'deki tüm görüntü türleri için temel sınıftır.  
`RasterImage` bir raster görüntüyü temsil eder ve kırpma yetenekleri sağlar.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Adım 2: Görüntü Verisini Önbellekle

`cacheData()` görüntü verisini daha hızlı işleme için belleğe yükler.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Adım 3: Kaydırma Değerlerini Tanımla

Görüntünün dört kenarı için (sol, üst, sağ, alt) piksel cinsinden kaydırma değerlerini belirtin.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Adım 4: Kırpmayı Uygula

`crop(left, right, top, bottom)` görüntüyü her bir kenarda belirtilen piksel kaydırmalarıyla kırpar.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Adım 5: Sonuçları Kaydet

`JpegOptions`, kalite ve renk profili gibi JPEG kodlama ayarlarını tanımlar.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Tebrikler! Aspose.PSD for Java kullanarak bir görüntüyü başarıyla kırptınız.

## Yaygın Sorunlar ve Çözümler

- **Görüntü değişmemiş gibi görünüyor:** Kaydırma değerlerinin pozitif olduğundan ve orijinal boyutları aşmadığından emin olun.  
- **Büyük dosyalarda OutOfMemoryError:** Adım 2'de gösterildiği gibi önbellekleme etkinleştirin; bu, Aspose.PSD'nin tüm görüntüyü RAM'de tutmak yerine geçici bir dosya kullanmasını sağlar.  
- **Kırpmadan sonra renk kayması:** Kesin renk doğruluğu gerekiyorsa `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` çağırarak renk profilini koruduğunuzdan emin olun.

## Sıkça Sorulan Sorular

**Q: Aspose.PSD tüm görüntü formatlarıyla uyumlu mu?**  
A: Evet, Aspose.PSD PSD, JPEG, PNG, BMP, TIFF ve GIF dahil olmak üzere 30'dan fazla raster formatını destekler ve geniş bir uyumluluk sağlar.

**Q: Aynı görüntüye birden fazla kırpma işlemi uygulayabilir miyim?**  
A: Kesinlikle. Her `crop` çağrısından sonra yeni bir görüntü nesnesi alırsınız; ihtiyacınıza göre tekrar kırpabilirsiniz.

**Q: Aspose.PSD desteği için bir topluluk forumu var mı?**  
A: Evet, [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) adresinde destek bulabilir ve toplulukla etkileşime geçebilirsiniz.

**Q: Aspose.PSD için geçici bir lisans nasıl alabilirim?**  
A: Geçici lisans almak için [buraya](https://purchase.aspose.com/temporary-license/) gidin.

**Q: Aspose.PSD işlevselliğini gösteren örnek projeler var mı?**  
A: [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/) adresindeki dokümantasyon ve örnekleri inceleyin.

---

**Son Güncelleme:** 2026-07-03  
**Test Edilen:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## İlgili Öğreticiler

- [Aspose.PSD for Java'da Dikdörtgen ile Görüntü Kırpma](/psd/java/image-editing/crop-image-by-rectangle/)
- [Aspose.PSD for Java ile Görüntü Kırpma Java - Genişletme ve Kırpma](/psd/java/image-editing/expand-and-crop-images/)
- [Aspose.PSD for Java'da Görüntü Yeniden Boyutlandırma Java - Resize Type Enumeration Kullanımı](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}