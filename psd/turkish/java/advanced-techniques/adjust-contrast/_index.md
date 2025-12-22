---
date: 2025-12-21
description: Aspose.PSD for Java, önde gelen bir Java görüntü işleme kütüphanesini
  kullanarak görüntülerin kontrastını nasıl ayarlayacağınızı öğrenin ve PSD'yi verimli
  bir şekilde TIFF'e dönüştürün.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile bir görüntünün kontrastını nasıl ayarlarsınız
url: /tr/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Bir Görüntünün Kontrastını Nasıl Ayarlarsınız

## Giriş

Java projelerinizde **kontrastı nasıl ayarlayacağınızı** arıyorsanız, doğru yerdesiniz. Aspose.PSD for Java, kontrast, parlaklık ve daha fazlası gibi görüntü özelliklerini ince ayar yapmanızı sağlayan güçlü bir **java image manipulation library**'dir. Bu öğreticide bir PSD dosyasının kontrastını artırmak ve ardından **PSD'yi TIFF'e dönüştürmek** için gerekli adımları adım adım göstereceğiz.

## Hızlı Yanıtlar
- **“adjust contrast” ne anlama gelir?** En koyu ve en parlak pikseller arasındaki farkı değiştirir, detayları ortaya çıkarır.
- **Bu işlemi hangi kütüphane gerçekleştirir?** Aspose.PSD for Java – tam özellikli bir görüntü işleme araç seti.
- **Lisans gerekli mi?** Test için geçici bir lisans yeterlidir; üretim için tam lisans gereklidir.
- **Sonucu TIFF olarak kaydedebilir miyim?** Evet, işlenmiş görüntüyü dışa aktarmak için `TiffOptions` kullanacağız.
- **Kodun çalışması ne kadar sürer?** Standart boyuttaki PSD dosyaları için genellikle bir saniyenin altında.

## Kontrast Ayarlaması Nedir?

Kontrast ayarlaması, bir görüntünün ton aralığını değiştirerek ışık ve karanlık bölgeler arasındaki farkı artırır. Bu, tarama sonrası görüntüler düz göründüğünde veya baskı için grafik hazırlarken özellikle faydalıdır.

## Neden Aspose.PSD for Java Kullanmalısınız?

- **Zengin format desteği** – PSD, TIFF, PNG, JPEG ve daha birçok formatı açma, düzenleme ve kaydetme.
- **Yüksek performans** – önbellekleme ve raster‑görüntü optimizasyonları bellek kullanımını azaltır.
- **Kullanımı kolay API** – `adjustContrast` gibi tek‑metot çağrıları kodun okunabilirliğini artırır.

## Ön Koşullar

Başlamadan önce şunlara sahip olduğunuzdan emin olun:

- Java programlama temelleri.
- Aspose.PSD for Java kütüphanesi kurulu. Kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.

## Paketleri İçe Aktarın

Gerekli içe aktarmaları Java sınıfınıza ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Adım 1: Görüntüyü Yükleyin

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Kaynak PSD dosyasını (`sample.psd`) bir `Image` nesnesine yüklüyoruz; bu nesne sonraki tüm işlemler için giriş noktasıdır.

## Adım 2: RasterImage'ye Dönüştürün ve Veriyi Önbelleğe Alın

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage`'e dönüştürme, piksel‑düzeyinde işlemlere erişim sağlar. Önbellekleme, özellikle büyük dosyalarda performansı artırır.

## Görüntünün Kontrastını Nasıl Ayarlarsınız

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` metodu, yüzde değişimini temsil eden bir tam sayı alır. Bu örnekte kontrastı **% 50** artırıyoruz.

## Aspose.PSD Kullanarak PSD'yi TIFF'e Dönüştürme

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Burada `TiffOptions` (örnek başına bit, fotometrik yorumlama) yapılandırılır ve kontrastı artırılmış görüntü bir TIFF dosyasına yazılır.

## Yaygın Sorunlar ve Çözümleri
- **Görüntü önbelleğe alınmadı:** Büyük PSD'lerde `OutOfMemoryError` almamak için her zaman `cacheData()` çağırın.
- **Beklenmeyen renk kayması:** `setPhotometric`'in hedef renk uzayınıza (RGB vs. CMYK) uygun olduğundan emin olun.
- **Dosya bulunamadı:** `dataDir`'in doğru klasöre işaret ettiğini ve dosya adının doğru yazıldığını kontrol edin.

## Sıkça Sorulan Sorular

### S1: Aspose.PSD farklı görüntü formatlarıyla uyumlu mu?

C1: Evet, Aspose.PSD çeşitli görüntü formatlarını destekler ve projelerinizde esneklik sağlar.

### S2: Aspose.PSD için geçici bir lisans nasıl alabilirim?

C2: Geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

### S3: Aspose.PSD belgelerini nerede bulabilirim?

C3: Belgeler [buradan](https://reference.aspose.com/psd/java/) mevcuttur.

### S4: Aspose.PSD için hangi destek seçenekleri mevcuttur?

C4: Destek için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

### S5: Aspose.PSD satın alabilir miyim?

C5: Evet, Aspose.PSD'yi [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

## Sonuç

Artık Aspose.PSD for Java kullanarak bir PSD görüntüsünün **kontrastını nasıl ayarlayacağınızı** ve **PSD'yi TIFF'e nasıl dönüştüreceğinizi** biliyorsunuz. Bu adımlar, kodu temiz ve sürdürülebilir tutarken görüntü kalitesi üzerinde ayrıntılı kontrol sağlar. `adjustBrightness` veya `adjustGamma` gibi diğer görüntü‑ayar yöntemleriyle deney yapmaktan çekinmeyin.

---

**Son Güncelleme:** 2025-12-21  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}