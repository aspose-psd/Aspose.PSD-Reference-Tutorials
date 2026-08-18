---
date: 2026-03-21
description: Aspose.PSD for Java kullanarak PSD'yi PNG'ye dönüştürmeyi ve PSD dosyalarını
  kırpmayı öğrenin. Bu rehber, Java uygulamalarında adım adım görüntü işleme gösterir.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile kırparak PSD'yi PNG'ye nasıl dönüştürürsünüz.
url: /tr/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile kırpma yaparken psd'yi png'ye dönüştürme

## Introduction
Dinamik Java geliştirme dünyasında, verimli görüntü işleme konusunda uzmanlaşmak çok önemlidir. Bu öğreticide **psd'yi png'ye nasıl dönüştüreceğinizi** ve güçlü Aspose.PSD for Java kütüphanesini kullanarak tek bir iş akışında görüntüyü nasıl kırpacağınızı öğreneceksiniz. Bu adım adım rehberin sonunda, PNG dışa aktarımlarınıza hassas kırpma ekleyebilecek ve Java uygulamalarınızın PSD varlıklarını güvenle işleyebileceksiniz.

## Quick Answers
- **Kod ne yapıyor?** Bir PSD yükler, bir dikdörtgeni kırpar ve PNG olarak kaydeder.  
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java (en son sürüm).  
- **Lisans gerekir mi?** Evet, üretim kullanımında ticari bir lisans gereklidir.  
- **Herhangi bir kırpma bölgesi tanımlayabilir miyim?** Kesinlikle – ihtiyacınız olan X, Y, genişlik ve yüksekliği belirlersiniz.  
- **Bu yaklaşım büyük dosyalar için hızlı mı?** Evet, Aspose.PSD yüksek performanslı işleme için optimize edilmiştir.

## What is convert psd to png?
psd'yi png'ye dönüştürmek nedir?
PSD'yi PNG'ye dönüştürmek, katmanlı bir Photoshop belgesini alıp kayıpsız bir PNG görüntüsüne düzleştirmek anlamına gelir. Bu format, web teslimatı, küçük resimler veya orijinal katmanlar olmadan bir raster görüntüye ihtiyaç duyduğunuz herhangi bir senaryo için idealdir.

## Why crop PSD before converting to PNG?
PNG'ye dönüştürmeden önce PSD'yi neden kırpmalıyız?
Kırpma, sadece ihtiyacınız olan tasarım bölümünü çıkarmanıza olanak tanır, dosya boyutunu azaltır ve ilgili görsel içeriğe odaklanır. Özellikle küçük resimler, UI varlıkları üretmek veya responsive (duyarlı) düzenler için görüntüleri hazırlamakta faydalıdır.

## Prerequisites
Önkoşullar
- Java programlama temellerine hâkim olmak.  
- Sisteminizde Java Development Kit (JDK) kurulu olması.  
- Aspose.PSD for Java kütüphanesini indirip projenize eklemiş olmak.  
- Deneme amaçlı bir örnek PSD dosyası.

## Import Packages
Paketleri İçe Aktarma
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Set Up Your Project
Adım 1: Projenizi Kurun
İlk olarak bir Java projesi oluşturun ve Aspose.PSD for Java kütüphanesini projenizin sınıf yoluna (classpath) ekleyin. Bu, ihtiyaç duyacağınız tüm görüntü işleme sınıflarına erişmenizi sağlar.

## Step 2: Load PSD Image
Adım 2: PSD Görüntüsünü Yükleyin
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*Burada kaynak PSD dosyasını bir `RasterImage` nesnesine yüklüyoruz; bu nesne kırpma gibi raster tabanlı işlemler sağlar.*

## Step 3: Define Crop Region
Adım 3: Kırpma Bölgesini Tanımlayın
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*`Rectangle` tutmak istediğiniz alanı tanımlar. Tasarımınıza uygun olarak `x`, `y`, `width` ve `height` değerlerini ayarlayın. Bu adım, “kırpma bölgesi tanımla” anahtar kelimesine doğrudan yanıt verir.*

## Step 4: Crop PSD Image
Adım 4: PSD Görüntüsünü Kırpın
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*`crop` metodunu çağırmak, görüntüyü bellek içinde değiştirir ve belirtilen dikdörtgenin dışındaki her şeyi atar.*

## Step 5: Set PNG Export Options
Adım 5: PNG Dışa Aktarım Seçeneklerini Ayarlayın
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions`, sıkıştırma seviyesi, renk tipi ve daha fazlası gibi PNG'ye özgü ayarları kontrol etmenizi sağlar.*

## Step 6: Save Cropped Image as PNG
Adım 6: Kırpılmış Görüntüyü PNG Olarak Kaydedin
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*`save` metodu, tanımladığınız kırpmayı koruyarak **psd'yi png'ye dönüştürme** işlemini gerçekleştirir.*

## Common Pitfalls & Tips
Yaygın Tuzaklar ve İpuçları
- **Yanlış dikdörtgen boyutları:** Genişlik ve yüksekliğin orijinal görüntü boyutunu aşmadığından emin olun, aksi takdirde bir istisna fırlatılır.  
- **Büyük PSD'lerde bellek kullanımı:** Kaydettikten sonra `RasterImage` nesnesini (`image.dispose()`) serbest bırakarak yerel kaynakları temizleyin.  
- **Lisans ayarlanmamış:** Geçerli bir lisans olmadan kodu çalıştırırsanız, çıktı PNG üzerinde bir filigran görünecektir.

## Frequently Asked Questions
Sıkça Sorulan Sorular
### Can I crop PSD files with irregular shapes using Aspose.PSD for Java?
Aspose.PSD for Java kullanarak düzensiz şekilli PSD dosyalarını kırpabilir miyim?
Evet, Aspose.PSD for Java, özel bir kırpma bölgesi tanımlamanıza izin verir ve böylece görüntüleri çeşitli şekillere kırpabilirsiniz.

### Is Aspose.PSD for Java suitable for large‑scale image processing tasks?
Aspose.PSD for Java büyük ölçekli görüntü işleme görevleri için uygun mu?
Kesinlikle! Aspose.PSD, büyük görüntüleri verimli bir şekilde işlemek üzere tasarlanmıştır ve kapsamlı görüntü işleme gereksinimleri olan projeler için idealdir.

### Do I need a license for Aspose.PSD for Java?
Aspose.PSD for Java için bir lisansa ihtiyacım var mı?
Evet, ticari kullanım için geçerli bir lisans gereklidir. Lisansı [Aspose Purchase](https://purchase.aspose.com/buy) adresinden edinebilirsiniz.

### How can I seek help or report issues with Aspose.PSD for Java?
Aspose.PSD for Java ile ilgili yardım nasıl alabilir veya sorunları nasıl bildirebilirim?
Yardım almak, deneyimlerinizi paylaşmak ve karşılaştığınız sorunları bildirmek için [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

### Can I try Aspose.PSD for Java before purchasing?
Aspose.PSD for Java'ı satın almadan önce deneyebilir miyim?
Elbette! Kütüphanenin özelliklerini ücretsiz deneme sürümüyle [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

---

**Son Güncelleme:** 2026-03-21  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}