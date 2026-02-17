---
date: 2026-02-17
description: Aspose.PSD kullanarak Java'da PSD'yi PNG'ye dönüştürmeyi, PNG şeffaflığını
  korumayı ve PSD katmanlarını döndürmeyi öğrenin. Kod örnekleriyle adım adım rehber.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Java kullanarak PSD'yi PNG'ye dönüştürün ve PSD dosyalarındaki katmanları döndürün
url: /tr/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dönüştürme ve PSD Dosyalarındaki Katmanları Java ile Döndürme

## Giriş
**PSD'yi PNG'ye dönüştürürken** aynı zamanda katmanları döndürmeniz gerekiyorsa, bu kılavuz tam size göre. İster toplu‑işlem aracı, ister anlık görüntü işleme gerektiren bir web servisi, ister sadece tasarım iş akışını otomatikleştiriyor olun, programlı olarak yapmak zamanı tasarruf ettirir ve Adobe Photoshop bağımlılığını ortadan kaldırır. Bu öğreticide **PSD katmanlarını nasıl döndüreceğinizi** ve sonucu Aspose.PSD for Java kütüphanesini kullanarak PNG olarak dışa aktaracağınızı adım adım göstereceğiz. Kolları sıvayalım ve tasarım iş akışınızı sorunsuz hale getirelim!

## Hızlı Yanıtlar
- **Hangi kütüphaneyi kullanabilirim?** Aspose.PSD for Java  
- **Hem döndürüp hem de dönüştürebilir miyim?** Evet – PSD'yi döndürün, ardından PNG olarak kaydedin  
- **Lisans gerekir mi?** Test için ücretsiz deneme sürümü yeterli; üretim için ücretli lisans gerekir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri  
- **PNG çıktısı şeffaf mı?** Evet, `PngColorType.TruecolorWithAlpha` ayarlandığında

## “PSD'yi PNG'ye dönüştürmek” nedir?
Bir Photoshop belgesini (PSD) PNG görüntüsüne dönüştürmek, görsel içeriği—tüm katmanlar, maskeler ve şeffaflık dahil—geniş çapta desteklenen bir raster formata çıkarmak anlamına gelir. PNG alfa kanallarını korur, bu da web grafikleri, küçük resimler ve sonraki görüntü işleme için idealdir.

## Neden PSD'yi PNG'ye dönüştürmek ve PSD katmanlarını döndürmek için Aspose.PSD for Java kullanmalı?
- **Photoshop gerekmez** – herhangi bir sunucu ya da CI ortamında çalışır  
- **Tam katman desteği** – şeffaflık ve katman efektleri korunur  
- **Basit API** – birkaç metod çağrısıyla döndürme, çevirme ve kaydetme  
- **Çapraz‑platform** – Windows, Linux ve macOS’ta çalışır  
- **Java görüntü dönüşümü** tek bir kütüphane ile zahmetsizce yapılır  

## Önkoşullar
Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Development Kit (JDK)** – [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-downloads.html) indirin.  
- **Entegre Geliştirme Ortamı (IDE)** – IntelliJ IDEA, Eclipse veya NetBeans yeterli.  
- **Aspose.PSD for Java kütüphanesi** – En yeni JAR dosyasını [sürüm sayfasından](https://releases.aspose.com/psd/java/) edinin.  
- **Temel Java bilgisi** – sınıflar, nesneler ve istisna yönetimi konularına aşina olun.

## Adım‑Adım Kılavuz

### Adım 1: Java Projenizi Kurun
IDE’nizde yeni bir Java projesi oluşturun ve Aspose.PSD JAR dosyasını projenin derleme yoluna ekleyin.

### Adım 2: Gerekli Sınıfları İçe Aktarın
Java kaynak dosyanızın en üstüne aşağıdaki import satırlarını ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Bu sınıflar, görüntü yükleme, döndürme ve PNG‑özel seçeneklerine erişim sağlar.

### Adım 3: Dosya Yollarını Tanımlayın
Kaynak PSD dosyanızın ve çıktı dosyalarının nerede bulunacağını belirtin.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **İpucu:** Test aşamasında “dosya bulunamadı” hatalarını önlemek için mutlak yol kullanın.

### Adım 4: PSD Dosyasını Yükleyin
PSD dosyasını manipüle edilebilir bir nesneye yükleyin.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Artık `im` tüm Photoshop belgesini, tüm katmanlarıyla birlikte temsil ediyor.

### Adım 5: Görüntüyü Döndürün (PSD'yi nasıl döndürürsünüz)
`RotateFlipType` içinden bir döndürme türü seçin. Bu örnekte 270° döndürüp iki eksende de çeviriyoruz.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone` veya `Rotate180FlipX` gibi diğer değerlerle deneme yapmaktan çekinmeyin. Bu, öğreticinin **PSD'yi nasıl döndürürsünüz** kısmıdır.

### Adım 6: Döndürülmüş Görüntüyü PNG Olarak Kaydedin (PSD'yi PNG'ye dönüştürün)
Şeffaflığı korumak için PNG seçeneklerini yapılandırın, ardından kaydedin.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Ortaya çıkan PNG katman şeffaflığını korur, böylece **PNG şeffaflığını koruma** sonraki kullanım için sağlanır.

### Adım 7: Değiştirilmiş PSD'yi Kaydedin (isteğe bağlı)
Döndürme uygulanmış yeni bir PSD dosyasına da ihtiyacınız varsa, onu geri kaydedin.

```java
im.save(psdPath);
```

Artık bir PNG önizlemeniz ve güncellenmiş bir PSD dosyanız var.

## Yaygın Sorunlar ve Çözümler
- **Dosya bulunamadı:** `dataDir` sonunun bir yol ayırıcı (`/` veya `\`) ile bittiğinden emin olun.  
- **Büyük PSD'lerde OutOfMemoryError:** JVM yığın boyutunu artırın (`-Xmx2g`).  
- **Şeffaflık kayboldu:** `PngColorType.TruecolorWithAlpha` ayarlandığından emin olun; aksi takdirde PNG alfa kanalı olmadan kaydedilir.  
- **PSD görüntüsü beklenildiği gibi çevrilmiyor:** Seçtiğiniz `RotateFlipType` sabitini tekrar kontrol edin; bazı sabitler döndürme ve çevirme işlemini tek adımda birleştirir.

## Sıkça Sorulan Sorular

**S: Bir PSD dosyasındaki belirli bir katmanı döndürebilir miyim?**  
C: Evet, `im.getLayers()` üzerinden döngü kurup her bir katmana `Layer.rotateFlip()` uygulayabilirsiniz.

**S: Aspose.PSD for Java’da performans sınırlamaları var mı?**  
C: Kütüphane çoğu dosyayı verimli işler, ancak çok büyük PSD'ler (>500 MB) ek bellek gerektirebilir.

**S: Aspose.PSD ücretsiz mi?**  
C: Aspose ücretsiz bir deneme sunar, ancak üretim için ücretli lisans gerekir. Test için [geçici lisans](https://purchase.aspose.com/temporary-license/) sayfasına bakın.

**S: Ayrıntılı belgeleri nerede bulabilirim?**  
C: Kapsamlı dokümantasyonu [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) adresinde bulabilirsiniz.

**S: Aspose.PSD kullanırken sorun yaşarsam ne yapmalıyım?**  
C: Yardım için [Aspose Support Forum](https://forum.aspose.com/c/psd/34) üzerinden destek alabilirsiniz.

**S: PSD'yi PNG'ye dönüştürürken katman efektleri korunur mu?**  
C: Evet, `PngColorType.TruecolorWithAlpha` ile kaydedildiğinde çoğu görsel efekt PNG'ye rasterleştirilir.

**S: Birden fazla PSD dosyasını toplu işleyebilir miyim?**  
C: Kesinlikle. Kodu bir dizindeki PSD dosyaları üzerinde dönen bir döngüye yerleştirin.

**S: PNG sıkıştırma seviyesini ayarlamak mümkün mü?**  
C: `PngOptions` sınıfı, ince ayar için `setCompressionLevel(int)` metodunu sunar.

**S: Görüntü nesnesini kapatmam gerekiyor mu?**  
C: `PsdImage` `Closeable` arayüzünü uygular; `im.close()` metodunu `finally` bloğunda çağırın ya da try‑with‑resources kullanın.

**S: Döndürülmüş PNG orijinal boyutlarla aynı olur mu?**  
C: 90° veya 270° döndürme genişlik ve yüksekliği değiştirir. PNG yeni yönelimle kaydedilir.

## Sonuç
Aspose.PSD for Java’yı kullanarak **PSD'yi PNG'ye dönüştürebilir**, **PNG şeffaflığını koruyabilir** ve **PSD katmanlarını** sadece birkaç satır kodla döndürebilirsiniz. Bu yöntem Photoshop ihtiyacını ortadan kaldırır, otomatik iş akışlarını hızlandırır ve görüntü çıktısı üzerinde tam kontrol sağlar. Kendi projelerinizde deneyin ve ne kadar zaman kazandığınızı görün!

---

**Son Güncelleme:** 2026-02-17  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}