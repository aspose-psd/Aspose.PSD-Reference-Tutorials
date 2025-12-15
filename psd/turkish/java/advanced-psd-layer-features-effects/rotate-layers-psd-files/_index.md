---
date: 2025-12-15
description: Aspose.PSD kullanarak Java'da PSD'yi PNG'ye dönüştürmeyi ve PSD katmanlarını
  döndürmeyi öğrenin. Kod örnekleriyle adım adım rehber.
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
Eğer **PSD'yi PNG'ye dönüştürmek** ve aynı zamanda katmanları döndürmek istiyorsanız, bu kılavuz tam size göre. İster toplu‑işlem aracı oluşturuyor olun, ister bir web hizmetine görüntü işleme entegrasyonu yapıyor olun, bunu programlı olarak yapmak zaman kazandırır ve Adobe Photoshop bağımlılığını ortadan kaldırır. Bu öğreticide **PSD'yi nasıl döndüreceğinizi** gösterecek ve sonucu Java için Aspose.PSD kütüphanesini kullanarak PNG olarak dışa aktaracağız. Kolları sıvayalım ve tasarım iş akışınızı sorunsuz bir şekilde çalıştırmaya başlayalım!

## Hızlı Yanıtlar
- **Hangi kütüphaneyi kullanabilirim?** Aspose.PSD for Java  
- **Hem döndürebilir hem de aynı anda dönüştürebilir miyim?** Evet – PSD'yi döndürün, ardından PNG olarak kaydedin  
- **Lisans gerekir mi?** Ücretsiz deneme sürümü test için çalışır; üretim için ücretli lisans gereklidir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve sonrası  
- **PNG çıktısı şeffaf mı?** Evet, `PngColorType.TruecolorWithAlpha` ayarlandığında  

## “PSD'yi PNG'ye dönüştürmek” nedir?
Bir Photoshop belgesini (PSD) PNG görüntüsüne dönüştürmek, görsel içeriği—tüm katmanlar, maskeler ve şeffaflık dahil—geniş desteklenen bir raster formata çıkarmak anlamına gelir. PNG, alfa kanallarını korur ve bu da web grafikleri, küçük resimler ve ileri görüntü işleme için idealdir.

## Neden PSD'yi PNG'ye dönüştürmek ve PSD katmanlarını döndürmek için Aspose.PSD for Java kullanmalısınız?
- **Photoshop gerekmez** – herhangi bir sunucu veya CI ortamında çalışır  
- **Tam katman desteği** – şeffaflık ve katman efektlerini olduğu gibi tutar  
- **Basit API** – sadece birkaç metod çağrısı ile döndürür, çevirir ve kaydeder  
- **Çapraz‑platform** – Windows, Linux ve macOS üzerinde çalışır  

## Önkoşullar
Koda geçmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Development Kit (JDK)** – [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-downloads.html) indirin.  
- **Entegre Geliştirme Ortamı (IDE)** – IntelliJ IDEA, Eclipse veya NetBeans hepsi uygundur.  
- **Aspose.PSD for Java kütüphanesi** – en son JAR dosyasını [sürüm sayfasından](https://releases.aspose.com/psd/java/) edinin.  
- **Temel Java bilgisi** – sınıflar, nesneler ve istisna yönetimi konularına aşina olmak.  

## Adım Adım Kılavuz

### Adım 1: Java Projenizi Kurun
IDE'nizde yeni bir Java projesi oluşturun ve Aspose.PSD JAR dosyasını projenin derleme yoluna ekleyin.

### Adım 2: Gerekli Sınıfları İçe Aktarın
Java kaynak dosyanızın en üstüne aşağıdaki içe aktarmaları ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Bu sınıflar, görüntü yükleme, döndürme ve PNG‑özel seçeneklerine erişmenizi sağlar.

### Adım 3: Dosya Yollarını Tanımlayın
Kaynak PSD dosyanızın nerede bulunduğunu ve çıktı dosyalarının nereye yazılacağını belirtin.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro ipucu:** Test sırasında “dosya bulunamadı” hatalarını önlemek için mutlak bir yol kullanın.

### Adım 4: PSD Dosyasını Yükleyin
PSD'yi manipüle edilebilir bir nesneye yükleyin.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Şimdi `im`, tüm katmanlar dahil olmak üzere bütün Photoshop belgesini temsil ediyor.

### Adım 5: Görüntüyü Döndürün (PSD'yi nasıl döndürürsünüz)
`RotateFlipType` içinden bir döndürme tipi seçin. Bu örnekte 270° döndürüp her iki ekseni de çeviriyoruz.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone` veya `Rotate180FlipX` gibi diğer değerlerle denemeler yapabilirsiniz.

### Adım 6: Döndürülmüş Görüntüyü PNG Olarak Kaydedin (PSD'yi PNG'ye dönüştürün)
Şeffaflığı korumak için PNG seçeneklerini yapılandırın, ardından kaydedin.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Ortaya çıkan PNG, katman şeffaflığını korur ve web kullanımına hazırdır.

### Adım 7: Değiştirilmiş PSD'yi Kaydedin (isteğe bağlı)
Eğer döndürme uygulanmış yeni bir PSD'ye de ihtiyacınız varsa, onu geri kaydedin.

```java
im.save(psdPath);
```

Artık bir PNG önizlemesi ve güncellenmiş bir PSD dosyanız var.

## Yaygın Sorunlar ve Çözümler
- **Dosya bulunamadı:** `dataDir`'in bir yol ayırıcı (`/` veya `\`) ile bittiğini doğrulayın.  
- **Büyük PSD'lerde OutOfMemoryError:** JVM yığın boyutunu artırın (`-Xmx2g`).  
- **Şeffaflık kayboldu:** `PngColorType.TruecolorWithAlpha` ayarlandığından emin olun; aksi takdirde PNG alfa olmadan kaydedilir.

## SSS

### Bir PSD dosyasındaki belirli bir katmanı döndürebilir miyim?
Evet, `im.getLayers()` üzerinden döndükten sonra bireysel katmanlarda `Layer.rotateFlip()` kullanabilirsiniz.

### Aspose.PSD for Java ile ilgili bir performans sınırlaması var mı?
Kütüphane çoğu dosyayı verimli bir şekilde işler, ancak çok büyük PSD'ler (>500 MB) ek bellek gerektirebilir.

### Aspose.PSD ücretsiz kullanılabilir mi?
Aspose ücretsiz bir deneme sunar, ancak üretim için ücretli lisans gerekir. Test için [geçici lisansı](https://purchase.aspose.com/temporary-license/) kontrol edin.

### Ayrıntılı belgeleri nerede bulabilirim?
Kapsamlı belgeleri [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) adresinde bulabilirsiniz.

### Aspose.PSD kullanırken sorunlarla karşılaşırsam ne yapmalıyım?
Yardım için [Aspose Support Forum](https://forum.aspose.com/c/psd/34) üzerinden iletişime geçin.

## Additional Frequently Asked Questions

**Q: PSD'yi PNG'ye dönüştürmek katman efektlerini korur mu?**  
**A:** Evet, `PngColorType.TruecolorWithAlpha` ile kaydettiğinizde, çoğu görsel efekt PNG'ye rasterleştirilir.

**Q: Birden fazla PSD dosyasını toplu işleme alabilir miyim?**  
**A:** Kesinlikle. Kodu, bir dizindeki PSD dosyaları üzerinde dönen bir döngüye sarın.

**Q: PNG sıkıştırma seviyesini ayarlamak mümkün mü?**  
**A:** `PngOptions` sınıfı, ince ayar için bir `setCompressionLevel(int)` metoduna sahiptir.

**Q: Görüntü nesnesini kapatmam gerekiyor mu?**  
**A:** `PsdImage` `Closeable` arayüzünü uygular; `im.close()`'ı bir `finally` bloğunda çağırın veya try‑with‑resources kullanın.

**Q: Döndürülmüş PNG orijinaliyle aynı boyutlara sahip olacak mı?**  
**A:** 90° veya 270° döndürmek genişlik ve yüksekliği değiştirir. PNG yeni yönelimi yansıtacaktır.

## Sonuç
Aspose.PSD for Java'ı kullanarak, sadece birkaç kod satırıyla **PSD'yi PNG'ye dönüştürebilir** ve **PSD** katmanlarını döndürebilirsiniz. Bu yaklaşım Photoshop ihtiyacını ortadan kaldırır, otomatik iş akışlarını hızlandırır ve görüntü çıktısı üzerinde tam kontrol sağlar. Kendi projelerinizde deneyin ve ne kadar zaman kazandığınızı görün!

---

**Son Güncelleme:** 2025-12-15  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}