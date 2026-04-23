---
date: 2026-02-09
description: Aspose.PSD kullanarak Java’da PSD’yi PNG’ye dönüştürmeyi ve görüntüleri
  orantılı olarak yeniden boyutlandırmayı öğrenin. Bu adım‑adım öğretici, görüntü
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

# Aspose.PSD for Java ile PSD'yi PNG'ye Dönüşme ve Orantılı Yeniden Boyutlandırma

## Giriiş

Orijinal en‑boy lisanslarını koruyarak **PSD'yi PNG'ye dönüştürmeniz** gerektiği doğru yere geldiniz. Bu **Aspose.PSD Java** öğretmenlerinde, **java görüntü işleme öğreticisi** kapsamında **görüntü nasıl yeniden boyutlandırılır** aralıkları olarak yeniden boyutlandırmayı, görünümü önbelleğe alarak performansı artırmayı ve son olarak sonucu PNG olarak kaydetmeyi adım adım adım gösteririz. Sonuna geldiğinizde bu iş verimi herhangi bir Java tabanlı görüntü işleme hattına entegre edilebiliyorsunuz.

## Hızlı Yanıtlar
- **Aspose.PSD, PSD'yi PNG'ye dönüştürebilir mi?** Evet – sadece PSD'yi yükleyin ve `PngOptions' ile kaydedin.
- **Kütüphane orantılı yeniden boyutlandırmayı destekliyor mu?** Kesinlikle; 'resizeWidthProportionally' ve 'resizeHeightProportionally' kullanın.
- **Önce görüntüyü önbelleğe almam gerekir mi?** Önbelleğe alma (`image.cacheData()`), büyük PSD dosyalarının performansını artırır.
- **Hangi Java sürümü gereklidir?** Java8 veya daha yenisi tam olarak desteklenir.
- **Üretim için lisans gerekli midir?** Evet, ticari lisans, değerlendirme filigranlarını kaldırır.

## "PSD'yi PNG'ye dönüştürme" nedir ve neden önemlidir?

Photoshop belgesinin (PSD) taşınabilir ağ grafiği (PNG) dosyasının dönüştürülmesine, genişletilebilir tasarımlarının hafif ve web dostu bir formatta paylaşılmasını sağlar. PNG'yi, şeffaflığını ve kayıpsız kalitesini korur; bu UI varlıkları, küçük resimler veya görüntü bütünlüğünün önemli olduğu herhangi bir senaryo için idealdir.

## Java'da görüntüyü neden orantılı olarak yeniden boyutlandıralım?

**görüntü nasıl yeniden boyutlandırılır**'ı en-boy bozulmadan yeniden boyutlandırma, grafiklerin farklı ekranlarda doğal görünmesini sağlar. `Aspose.PSD` API'si, **görüntüyü orantılı olarak yeniden boyutlandırma** için özel yedekler sunar; Bu yöntemler otomatik olarak uygun yükseklik veya daha fazla hesaplama yaparak manuel matematik hatalarından sizi korur.

## Geliştiriciler için neden önemli?

- **Küçültülmüş PSD dosya boyutu** – Dönüştürmeden önce büyük PSD dosyalarını küçülterek bellek kullanımını azaltır ve sonraki işlemleri hızlandırırsınız.

- **Tutarlı kullanıcı arayüzü oluşturma** – Orantılı yeniden boyutlandırma, simgelerin ve grafiklerin cihazlar arasında görsel dengelerini korumasını garanti eder.

- **Photoshop bağımlılığı yok** – Bu işlemleri Photoshop kurmadan bir sunucuda veya CI hattında gerçekleştirebilirsiniz.

## Önkoşullar

Koda geçmeden önce şunlara sahip olduğunuzdan emin olun:

1. **Java Geliştirme Kiti (JDK)** – Java 8 veya üzeri kurulu olmalıdır.

2. **Aspose.PSD for Java** – En son JAR dosyasını resmi siteden [buradan](https://releases.aspose.com/psd/java/) indirin.

3. Projenizden referans verebileceğiniz bir dizine yerleştirilmiş örnek bir PSD dosyası (`sample.psd`).

## Paketleri İçe Aktarma

Java sınıfınıza gerekli içe aktarmaları ekleyin. Bu sınıflar, görüntü yükleme, önbelleğe alma, yeniden boyutlandırma ve PNG çıktı seçeneklerine erişmenizi sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: PSD Görüntüsünü Yükleyin

Öncelikle, kaynak PSD dosyasını yükleyin. Dosya büyükse, görüntü verilerini önbelleğe almak, sonraki işlemleri gerçekleştirirken bellek kullanımını azaltır.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Adım 2: Görüntüyü Orantılı Olarak Yeniden Boyutlandırın (Java)

Şimdi yeni boyutları belirleyin. Bu örnekte, en boy oranını koruyarak görüntüyü orijinal boyutunun **yarısı**na küçültüyoruz. Hedef genişliği veya yüksekliği gerektiği gibi ayarlayabilirsiniz.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **İpucu:** `resizeWidthProportionally` *veya* `resizeHeightProportionally` kullanın; kütüphane, görüntünün orantılı kalması için diğer boyutu otomatik olarak hesaplar.

## Adım 3: Yeniden Boyutlandırılmış Görüntüyü PNG Olarak Kaydedin

Son olarak, yeniden boyutlandırılmış görüntüyü PNG formatına dışa aktarın. Bu adım, **PSD'yi PNG'ye dönüştürme** iş akışını tamamlar.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Kod çalıştırıldığında, orijinal PSD dosyasının yarısı boyutunda, aynı görsel kaliteye sahip ve bozulma içermeyen bir PNG dosyası bulacaksınız.

## Sık Karşılaşılan Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |

|-------|-------|-----|

| **Bellek Yetersizliği Hatası** | Büyük PSD önbelleğe alınmamış | Yeniden boyutlandırmadan önce `image.cacheData()`'ı çağırın |

| **Boş PNG çıktısı** | Yanlış dosya yolu | `dataDir` ve yazma izinlerini doğrulayın |

| **En boy oranı yanlış görünüyor** | Hem genişliği hem de yüksekliği manuel olarak kullanma | Aspose.PSD tarafından sağlanan orantılı yöntemleri kullanın |

## PSD Dosya Boyutunu Küçültme İpuçları

- Dosyayı yüklemeden önce **gereksiz katmanları kırpın**.

- Boyutları erken küçültmek için yukarıda gösterildiği gibi **orantılı olarak yeniden boyutlandırın**.

- Fazla veriden kaçınmak için **uygun bit derinliğiyle PNG olarak kaydedin**.

## Sıkça Sorulan Sorular

**S: Aspose.PSD tüm resim formatlarıyla uyumlu mu?**
C: Aspose.PSD, PSD, PNG, JPEG, BMP, GIF ve daha birçok formatı destekler. Tam listeyi [belgelerde](https://reference.aspose.com/psd/java/) bulabilirsiniz.

**S: Aspose.PSD'yi ticari projelerde kullanabilir miyim?**
C: Evet. [Aspose mağazasından](https://purchase.aspose.com/buy) ticari lisans satın alabilirsiniz.

**S: Test amaçlı geçici lisanslar mevcut mu?**
C: Kesinlikle – değerlendirme amacıyla [buradan](https://purchase.aspose.com/temporary-license/) geçici lisans talep edebilirsiniz.

**S: Topluluk desteğini nerede bulabilirim?**
C: [Aspose.PSD forumu](https://forum.aspose.com/c/psd/34), sorular sormak ve çözümler paylaşmak için harika bir yerdir.

**S: Tam API referansına nasıl erişebilirim?**
C: Ayrıntılı API belgelerine [buradan](https://reference.aspose.com/psd/java/) ulaşabilirsiniz.

## Sonuç

Artık Aspose.PSD for Java kullanarak **PSD'yi PNG'ye dönüştürmeyi**, **görüntüyü orantılı olarak yeniden boyutlandırmayı** ve önbelleğe almayı verimli bir şekilde nasıl yöneteceğinizi biliyorsunuz. Bu adımları kendi uygulamalarınıza entegre ederek, yerel Photoshop kurulumlarına güvenmeden hızlı ve yüksek kaliteli görüntü işleme sağlayabilirsiniz. Bu **aspose psd java** yaklaşımı, herhangi bir **java görüntü işleme eğitiminin** güvenilir bir parçasıdır ve görsel doğruluğu korurken PSD dosya boyutlarını kontrol altında tutmanıza yardımcı olur.

---

**Son Güncelleme:** 2026-02-09
**Test Edildiği Sürüm:** Aspose.PSD 24.12 for Java
**Yazar:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
