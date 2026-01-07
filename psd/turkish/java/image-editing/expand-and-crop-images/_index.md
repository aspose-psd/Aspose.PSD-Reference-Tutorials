---
date: 2026-01-07
description: Aspose.PSD for Java kullanarak Java’da nasıl resim kırpılacağını öğrenin.
  Resim kırpma, yeniden boyutlandırma ve PSD’den JPEG’e dönüştürme için adım adım
  rehber.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Görüntü Kırpma Java: Aspose.PSD for Java ile Görüntüleri Genişlet ve Kırp'
url: /tr/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Aspose.PSD for Java ile Görüntüleri Genişletin ve Kırpın

## Introduction

Bu öğreticide, Aspose.PSD kütüphanesini kullanarak **crop image java** nasıl yapılacağını keşfedeceksiniz. Kanvası genişletmeniz, istenmeyen kenarları kırpmanız veya bir PSD dosyasını JPEG'e dönüştürmeniz gerekse, aşağıdaki adımlar temiz ve tekrarlanabilir bir süreç sunar. Gereksinimler, import ifadeleri ve her kod adımını net açıklamalarla ele alacağız, böylece tekniği gerçek dünya projelerinde uygulayabilirsiniz.

## Quick Answers
- **What library handles crop image java?** Aspose.PSD for Java.
- **Do I need a license for development?** Geliştirme için ücretsiz deneme sürümü test amaçlı çalışır; üretim için ticari lisans gereklidir.
- **Can I convert PSD to JPEG while cropping?** Evet, kırpma dikdörtgeniyle birlikte `JpegOptions` kullanarak yapabilirsiniz.
- **Is Java 8 supported?** Aspose.PSD, Java 8 ve daha yeni sürümleri destekler.
- **How long does the implementation take?** Temel bir kırpma işlemi genellikle 10 dakikadan az sürer.

## What is “crop image java”?

Java’da bir görüntüyü kırpmak, kaynak resmin dikdörtgen bir bölgesini seçmek ve geri kalanını atmak anlamına gelir. Aspose.PSD ile bu bölgeyi bir `Rectangle` nesnesiyle tanımlayabilir, ardından sonucu JPEG gibi farklı bir formatta kaydedebilirsiniz.

## Why use Aspose.PSD for Java image cropping?

- **Full PSD support** – katmanlı PSD dosyalarıyla doğrudan çalışın, önce dönüştürmeye gerek kalmaz.  
- **High‑performance raster handling** – büyük görüntüler için verimli bellek kullanımı.  
- **Built‑in conversion** – kırpma veya kanvas genişletme sırasında JPEG, PNG, BMP vb. formatlara kolayca dışa aktarın.  
- **Cross‑platform** – Java çalıştırabilen herhangi bir sistemde çalışır.

## Prerequisites

Başlamadan önce şunların yüklü olduğundan emin olun:

1. **Java Development Kit (JDK)** – Java 8 veya daha yeni bir sürüm yüklü.  
2. **Aspose.PSD for Java** – resmi siteden kütüphaneyi **[buradan](https://releases.aspose.com/psd/java/)** indirin.  

> **Pro tip:** Aspose.PSD JAR dosyasını projenizin classpath'ine veya Maven/Gradle bağımlılıklarına ekleyin, böylece `ClassNotFoundException` hatasından kaçınırsınız.

## Import Packages

Java kaynak dosyanıza gerekli importları ekleyin. Bu sınıflar, görüntü yükleme, raster manipülasyonu, dikdörtgen tanımlama ve JPEG dışa aktarım seçeneklerine erişim sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step 1: Set Your Document Directory

Kaynak PSD dosyasının bulunduğu klasörü belirtin. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Specify Source and Destination Paths

PSD'yi okuyacağınız ve kırpılmış JPEG'i yazacağınız yolları tanımlayın.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Step 3: Load and Cache the Image

PSD'yi bir `RasterImage` nesnesine yükleyin. Önbelleğe alma, kırpma gibi sonraki işlemlerin performansını artırır.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Step 4: Create Rectangle for Cropping

Tutmak istediğiniz bölgeyi tanımlayan bir `Rectangle` oluşturun. Koordinatlar negatif olabilir; bu, kırpmadan önce kanvası **genişletmek** için kullanışlıdır ve orijinal görüntünün etrafına kenar eklemenizi sağlar.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Why use negative coordinates?**  
> Negatif X/Y değerleri kırpma alanını sola/yukarı kaydırır, böylece son kırpmadan önce orijinal içeriğin etrafına boş alan (genişletme) eklenir.

## Step 5: Save the Cropped Image

Son olarak, `JpegOptions` kullanarak elde edilen görüntüyü kaydedin. Bu adım, kırpma dikdörtgeni uygulanırken **convert psd jpeg** işlemini de gösterir.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Result:** `jpeg_out.jpg` artık her iki taraftan 200 px genişletilmiş ve tanımlı dikdörtgene kırpılmış 300 × 300 piksel bir görüntü içerir.

Tebrikler! **java image cropping** işlemini başarıyla gerçekleştirdiniz, kanvası genişlettiniz ve bir PSD dosyasını birkaç satır kodla JPEG'e dönüştürdünüz.

## Common Use Cases

- **Preparing assets for web** – web için varlıkları hazırlarken ekran görüntülerini veya tasarımları kırpıp yeniden boyutlandırın.  
- **Generating thumbnails** – büyük bir PSD'den ön izleme amaçlı belirli bir bölgeyi çıkararak küçük resimler oluşturun.  
- **Automated batch processing** – bir klasördeki PSD dosyalarını döngüye alarak aynı kırpma dikdörtgenini her birine uygulayın.

## Troubleshooting & Tips

| Issue | Suggested Fix |
|-------|----------------|
| `OutOfMemoryError` when loading large PSDs | `rasterImage.cacheData()` metodunu erken çağırın ve JVM heap boyutunu (`-Xmx`) artırmayı düşünün. |
| Cropped area is off‑center | Dikdörtgenin X/Y ofsetlerini kontrol edin; negatif değerlerin kanvası genişlettiğini unutmayın. |
| Output JPEG looks blurry | `JpegOptions` kalite ayarını değiştirin (ör. `new JpegOptions { Quality = 90 }`). |

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with different Java versions?

A1: Evet, Aspose.PSD çeşitli Java sürümleriyle uyumludur ve geniş bir geliştirme ortamı yelpazesinde çalışabilir.

### Q2: Can I use Aspose.PSD for commercial projects?

A2: Kesinlikle, Aspose.PSD ticari lisanslar sunar; böylece hem kişisel hem de ticari projelerde kullanılabilir.

### Q3: Are there any limitations on the image file formats supported?

A3: Aspose.PSD, PSD, JPEG, PNG ve daha fazlası dahil olmak üzere çeşitli görüntü dosyası formatlarını destekler. Tam liste için [documentation](https://reference.aspose.com/psd/java/) sayfasına bakın.

### Q4: How can I get support for Aspose.PSD-related queries?

A4: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) üzerinden topluluktan veya Aspose destek ekibinden yardım alabilirsiniz.

### Q5: Is there a free trial available?

A5: Evet, ücretsiz bir deneme sürümü mevcuttur. **[Buradan](https://releases.aspose.com/)** indirebilirsiniz.

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}