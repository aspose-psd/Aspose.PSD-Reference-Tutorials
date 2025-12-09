---
date: 2025-12-08
description: Aspose.PSD kullanarak Java’da PSD’yi PNG’ye dönüştürmeyi ve görüntüleri
  orantılı olarak yeniden boyutlandırmayı öğrenin. Bu adım adım öğretici, görüntü
  önbelleğe almayı, yeniden boyutlandırmayı ve PNG olarak kaydetmeyi kapsar.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile PSD'yi PNG'ye Dönüştürme ve Orantılı Yeniden Boyutlandırma
url: /tr/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dönüştürme ve Aspose.PSD for Java ile Orantılı Yeniden Boyutlandırma

## Giriş

Eğer **PSD'yi PNG'ye dönüştürmek** ve orijinal en-boy oranını korumak istiyorsanız doğru yerdesiniz. Bu öğreticide, Java'da **Aspose.PSD öğreticisi** kapsamında **görüntüyü nasıl orantılı olarak yeniden boyutlandıracağınızı**, görüntüyü optimum performans için önbelleğe almayı ve son olarak sonucu PNG olarak kaydetmeyi adım adım göstereceğiz. Sonunda bu iş akışını herhangi bir Java tabanlı görüntü işleme hattına entegre edebileceksiniz.

## Hızlı Yanıtlar
- **Aspose.PSD PSD'yi PNG'ye dönüştürebilir mi?** Evet – PSD'yi yükleyip `PngOptions` ile kaydedin.
- **Kütüphane orantılı yeniden boyutlandırmayı destekliyor mu?** Kesinlikle; `resizeWidthProportionally` ve `resizeHeightProportionally` kullanın.
- **Önce görüntüyü önbelleğe almam gerekiyor mu?** Önbellekleme (`image.cacheData()`) büyük PSD dosyalarında performansı artırır.
- **Hangi Java sürümü gerekiyor?** Java 8 veya daha yenisi tam olarak desteklenir.
- **Üretim ortamında lisans gerekli mi?** Evet, ticari lisans değerlendirme filigranlarını kaldırır.

## “PSD'yi PNG'ye dönüştürme” nedir ve neden önemlidir?

Bir Photoshop belgesini (PSD) taşınabilir ağ grafiği (PNG) dosyasına dönüştürmek, katmanlı tasarımları hafif ve web‑dostu bir formatta paylaşmanızı sağlar. PNG şeffaflığı ve kayıpsız kalitesi korur, bu da UI varlıkları, küçük resimler veya görüntü netliğinin kritik olduğu herhangi bir senaryo için idealdir.

## Java'da görüntüyü orantılı olarak yeniden boyutlandırmak neden önemlidir?

**Görüntüyü nasıl yeniden boyutlandırırız** sorusuna, en‑boy oranını bozmadan cevap vermek, grafiklerin farklı ekranlarda doğal görünmesini sağlar. `Aspose.PSD` API'si, eşleşen yükseklik veya genişliği otomatik olarak hesaplayan özel orantılı ölçekleme yöntemleri sunar, böylece manuel matematik hatalarından kaçınırsınız.

## Önkoşullar

Kodlamaya başlamadan önce şunların yüklü olduğundan emin olun:

1. **Java Development Kit (JDK)** – Java 8 veya üzeri.
2. **Aspose.PSD for Java** – en son JAR dosyasını resmi siteden [burada](https://releases.aspose.com/psd/java/) indirin.
3. Projenizde referans verebileceğiniz bir klasörde bulunan örnek PSD dosyası (`sample.psd`).

## Paketleri İçe Aktarma

Java sınıfınıza gerekli importları ekleyin. Bu sınıflar, görüntü yükleme, önbellekleme, yeniden boyutlandırma ve PNG çıktı seçeneklerine erişim sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: PSD Görüntüsünü Yükleme

İlk olarak kaynak PSD dosyasını yükleyin. Dosya büyükse, görüntü verisini önbelleğe almak sonraki işlemlerde bellek tüketimini azaltır.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Adım 2: Görüntüyü Orantılı Olarak Yeniden Boyutlandırma (Java)

Şimdi yeni boyutları belirleyin. Bu örnekte, görüntüyü **yarı** oranına küçültürken en‑boy oranını koruyoruz. İhtiyacınıza göre hedef genişlik veya yüksekliği ayarlayabilirsiniz.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **İpucu:** `resizeWidthProportionally` *veya* `resizeHeightProportionally` yöntemlerinden birini kullanın — kütüphane diğer boyutu otomatik olarak hesaplayarak görüntüyü orantılı tutar.

## Adım 3: Yeniden Boyutlandırılmış Görüntüyü PNG Olarak Kaydetme

Son olarak, yeniden boyutlandırılmış görüntüyü PNG formatına dışa aktarın. Bu adım, **PSD'yi PNG'ye dönüştürme** iş akışını tamamlar.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Kod çalıştığında, orijinal PSD'nin yarısı boyutunda, aynı görsel kaliteyi koruyan ve bozulma içermeyen bir PNG dosyası elde edeceksiniz.

## Yaygın Sorunlar & Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **OutOfMemoryError** | Büyük PSD önbelleğe alınmamış | Yeniden boyutlandırmadan önce `image.cacheData()` çağırın |
| **Boş PNG çıktısı** | Yanlış dosya yolu | `dataDir` ve yazma izinlerini kontrol edin |
| **En‑boy oranı bozuk** | Genişlik ve yükseklik aynı anda manuel ayarlandı | Aspose.PSD tarafından sağlanan orantılı yöntemleri kullanın |

## Sık Sorulan Sorular

**S: Aspose.PSD tüm görüntü formatlarıyla uyumlu mu?**  
C: Aspose.PSD, PSD, PNG, JPEG, BMP, GIF ve daha birçok formatı destekler. Tam listeyi [belgelendirmede](https://reference.aspose.com/psd/java/) bulabilirsiniz.

**S: Aspose.PSD'yi ticari projelerde kullanabilir miyim?**  
C: Evet. Ticari lisansı [Aspose mağazasında](https://purchase.aspose.com/buy) satın alabilirsiniz.

**S: Test amaçlı geçici lisanslar mevcut mu?**  
C: Kesinlikle – değerlendirme amaçlı geçici bir lisans için [buradan](https://purchase.aspose.com/temporary-license/) talepte bulunun.

**S: Topluluk desteği nereden alınır?**  
C: Sorularınızı sorup çözümler paylaşabileceğiniz harika bir yer olan [Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) bulunmaktadır.

**S: Tam API referansına nasıl ulaşabilirim?**  
C: Ayrıntılı API dokümantasyonu [burada](https://reference.aspose.com/psd/java/) mevcuttur.

## Sonuç

Artık **PSD'yi PNG'ye dönüştürme**, görüntüyü orantılı olarak yeniden boyutlandırma ve önbellekleme işlemlerini Aspose.PSD for Java kullanarak nasıl yapacağınızı biliyorsunuz. Bu adımları kendi uygulamalarınıza entegre ederek, yerel Photoshop kurulumlarına ihtiyaç duymadan hızlı ve yüksek kalite görüntü işleme sağlayabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-08  
**Test Edilen Versiyon:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose