---
date: 2026-02-12
description: Aspose.PSD for Java kullanarak görüntüyü nasıl döndüreceğinizi ve görüntüyü
  270 derece nasıl döndüreceğinizi öğrenin. Bu rehber, PSD dosyalarını döndürmeyi,
  görüntüleri çevirmeyi ve Photoshop olmadan PSD'yi JPEG'e dönüştürmeyi kapsar.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Görüntüyü 270 Derece Döndürme
url: /tr/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Görüntüyü 270 Derece Döndürme

## Introduction

Bu **java görüntü işleme öğreticisinde**, Aspose.PSD for Java kullanarak **görüntüyü 270 derece döndürmenin** hızlı ve güvenilir yolunu keşfedeceksiniz. Fotoğraf düzenleme aracı geliştiriyor, toplu dönüşümleri otomatikleştiriyor ya da sadece bir PSD katmanını yeniden yönlendirmeniz gerekiyorsa, kütüphane bu görevi zahmetsiz hâle getirir. Ayrıca **flip image java** tekniklerine ve döndürülmüş PSD'yi JPEG'e dönüştürmeye de değineceğiz, böylece Photoshop olmadan tam bir uçtan uca iş akışı elde edersiniz.

## Quick Answers
- **Rotasyonu hangi kütüphane yönetir?** Aspose.PSD for Java  
- **Örnekte hangi döndürme açısı kullanılıyor?** 270 degrees  
- **Görüntüyü aynı zamanda çevirebilir miyim?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **Sonucu nasıl kaydederim?** In the example we save as JPEG using `JpegOptions`  
- **Üretim için lisansa ihtiyacım var mı?** A valid Aspose.PSD license is required for commercial use  

## What is “rotate image 270 degrees”?

Bir görüntüyü 270 derece döndürmek, resmi saat yönünde tam bir dairenin üçte üçü kadar (veya saat yönünün tersine 90 derece) çevirmek anlamına gelir. Birçok grafik düzenleme senaryosunda bu yönlendirme, bir dizi dönüşümden sonra orijinal portre düzeniyle eşleşir.

## Why Use Aspose.PSD for This Task?
- **Tam PSD desteği** – katmanlar, maskeler ve ayar nesneleriyle çalışır.  
- **Yerel Photoshop gerekmez** – herhangi bir Java çalışma ortamında çalışır.  
- **Basit API** – tek bir metod çağrısı (`rotateFlip`) döndürme ve çevirme işlemlerini gerçekleştirir.  
- **Kolay format dönüşümü** – doğrudan JPEG, PNG veya diğer yaygın formatlara dışa aktarır.

## How to Rotate Image with Aspose.PSD for Java
Aşağıda, bir PSD'yi yükleme, 270° döndürme uygulama, isteğe bağlı olarak görüntüyü çevirme ve son olarak sonucu JPEG olarak kaydetme adımlarını içeren adım adım bir kılavuz bulacaksınız.

### Prerequisites

Before you start, make sure you have:

- **Aspose.PSD for Java** kütüphanesinin kurulu olduğundan emin olun. İndirebilir ve tam API referansını [buradan](https://reference.aspose.com/psd/java/) görüntüleyebilirsiniz.  
- Java geliştirme ortamı (JDK 8 veya üzeri).  
- Döndürmek istediğiniz örnek bir PSD dosyası. Koddaki `sourceFile` değişkenini dosyanızın doğru yolu ile güncelleyin.

### Import Packages

İlk olarak Aspose.PSD paketinden gerekli sınıfları içe aktarın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Step 1: Load the Image

`source` PSD dosyanıza işaret eden bir `Image` örneği oluşturun:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Step 2: Rotate the Image 270 Degrees

`rotateFlip` metodunu `RotateFlipType.Rotate270FlipNone` ile kullanarak herhangi bir çevirme olmadan 270 derecelik döndürmeyi gerçekleştirin:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro ipucu:** Görüntüyü yatay ya da dikey olarak da çevirmeniz gerekiyorsa, `Rotate90FlipX` veya `Rotate180FlipY` gibi farklı bir `RotateFlipType` seçin. Bu, **flip image java** işlemlerinin en yaygın yoludur.

### Step 3: Convert PSD to JPEG and Save

Döndürmeden sonra, uygun seçenek sınıfını kullanarak **PSD'yi JPEG'e dönüştürebilir** (veya başka bir desteklenen formata) aşağıdaki gibi:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

`RotatedImage_out.jpg` dosyası artık orijinal PSD içeriğini 270 derece döndürülmüş ve JPEG olarak kaydedilmiş şekilde içerir.

## Why This Matters – Real‑World Use Cases
- **Ürün kataloglarının toplu işlenmesi** – yayınlamadan önce onlarca PSD varlığını tek bir yönlendirmeye döndürün.  
- **Otomatik küçük resim oluşturma** – Photoshop açmadan web galerileri için doğru yönlendirilmiş ön izlemeler oluşturun.  
- **Mobil uygulama arka uçları** – kullanıcı tarafından yüklenen PSD dosyalarını sunucu tarafında saf Java kullanarak yeniden yönlendirin.

## Common Pitfalls & Troubleshooting

| Issue | Solution |
|-------|----------|
| **Görüntü ters görünüyor** | Kullandığınızın `Rotate270FlipNone` olduğundan emin olun. Saat yönünde 90 derece döndürme için `Rotate90FlipNone` kullanın. |
| **Çıktı dosyası bozuk** | Hedef klasörün var olduğundan ve yazma izninizin bulunduğundan emin olun. |
| **Lisans istisnası** | Üretimde görüntüyü yüklemeden önce geçici veya kalıcı bir Aspose.PSD lisansı kurun. |
| **Photoshop olmadan görüntüyü döndürme ihtiyacı** | Bu API, döndürmeyi tamamen kod içinde gerçekleştirir ve Photoshop bağımlılığını ortadan kaldırır. |
| **Aynı işlemde görüntüyü çevirmek istiyorum** | `Rotate90FlipX` gibi diğer `RotateFlipType` değerlerini kullanın (**how to flip image** kapsar). |

## Frequently Asked Questions

**S: Aspose.PSD farklı görüntü formatlarıyla uyumlu mu?**  
C: Evet, Aspose.PSD PSD, JPEG, PNG, BMP, GIF ve birçok diğer raster formatını destekler.

**S: Önceden tanımlı çevirilerin dışında özel döndürmeler uygulayabilir miyim?**  
C: Kesinlikle! `RotateFlipType` yaygın açıları sağlarken, birden fazla çağrıyı birleştirerek veya dönüşüm matrisleri kullanarak isteğe bağlı açıları elde edebilirsiniz.

**S: Döndürülmüş PSD'yi başka bir formata, örneğin PNG'e nasıl dönüştürürüm?**  
C: `save` metodunda `JpegOptions` yerine `PngOptions` (veya uygun seçenek sınıfı) kullanın.

**S: Ek destek veya yardım nereden bulabilirim?**  
C: Topluluk yardımı için [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

**S: Ücretsiz deneme mevcut mu?**  
C: Evet, bir [ücretsiz deneme](https://releases.aspose.com/) ile Aspose.PSD'yi keşfedebilirsiniz.

**S: Geçici bir lisans nasıl alabilirim?**  
C: Geçici bir lisansa ihtiyacınız varsa, [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

**S: Bu yöntem başsız (headless) sunucularda çalışır mı?**  
C: Evet, Aspose.PSD for Java herhangi bir standart JVM ortamında çalışır, bu da CI/CD boru hatları veya bulut fonksiyonları için idealdir.

## Conclusion

Artık Aspose.PSD for Java kullanarak **görüntüyü 270 derece döndürmeyi**, gerektiğinde **görüntüyü çevirmeyi** ve sonucu JPEG olarak dışa aktarmayı öğrendiniz. Bu basit iş akışı, daha büyük Java tabanlı görüntü işleme boru hatlarına entegre edilebilir ve Photoshop'a bağımlı olmadan PSD manipülasyonu üzerinde tam kontrol sağlar.

---

**Son Güncelleme:** 2026-02-12  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}