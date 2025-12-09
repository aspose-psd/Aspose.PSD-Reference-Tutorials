---
date: 2025-12-01
description: Aspose.PSD for Java kullanarak PSD dosyasını nasıl kaydedeceğinizi, yazı
  tipi önbelleğini nasıl zorlayacağınızı ve görüntü performansını nasıl artıracağınızı
  öğrenin. Görüntü işleme optimizasyonu için adım adım rehber.
linktitle: Force Font Cache
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile PSD Dosyasını Kaydetme ve Yazı Tipi Önbelleğini Zorla
url: /tr/java/advanced-image-manipulation/force-font-cache/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyasını Kaydetme ve Aspose.PSD for Java ile Yazı Tipi Önbelleğini Zorlamak

## Giriş

**PSD dosyasını kaydetme** nesnelerini hızlı bir şekilde kaydetmeniz ve doğru yazı tiplerinin mevcut olduğundan emin olmanız gerekiyorsa, doğru yerdesiniz. Yazı tipi önbelleği, özellikle büyük Photoshop belgelerini tekrar tekrar işlediğinizde **görüntü performansını** önemli ölçüde **artırabilir**. Bu öğreticide, önbelleği zorlamak, bir PSD görüntüsü yüklemek ve sonunda Aspose.PSD for Java kullanarak yeni yüklü yazı tipleriyle **PSD dosyasını kaydetme** adımlarını adım adım göstereceğiz.

## Hızlı Yanıtlar
- **Yazı tipi önbelleğini zorlamak ne işe yarar?** Aspose.PSD'nin sistem yazı tiplerini yeniden taramasını sağlar, böylece yeni yüklü yazı tipleri anında tanınır.  
- **Bir yazı tipinin kurulması ne kadar sürer?** Örnek kod **2 dakika** bekletir; bu genellikle manuel kurulum için yeterlidir.  
- **Bunu herhangi bir PSD dosyasıyla kullanabilir miyim?** Evet – dosya erişilebilir olduğu ve gerekli yazı tipleri sistemde yüklü olduğu sürece.  
- **Bu kodu çalıştırmak için lisansa ihtiyacım var mı?** Üretim kullanımı için geçici veya tam lisans gerekir; değerlendirme için ücretsiz deneme sürümü çalışır.  
- **Hangi Java sürümleri destekleniyor?** Aspose.PSD for Java, JDK 8 ve üzeri sürümlerle çalışır.

## “PSD dosyasını kaydetme” nedir ve neden önemlidir?

Katmanları, metni veya yazı tiplerini değiştirdikten sonra bir PSD dosyasını kaydetmek, değişikliklerin kalıcı olmasını sağlar. Yazı tipi önbelleği güncel değilse, kaydedilen dosya varsayılan yazı tiplerine geri dönebilir ve görsel tutarsızlıklara yol açar. Önce önbelleği zorlayarak, **PSD dosyasını kaydetme** işleminin doğru tipografiyi gömmesini garantilersiniz.

## Neden Aspose.PSD ile yazı tipi önbelleğini zorlamalısınız?

- **Performans artışı** – Tekrarlanan yazı tipi aramalarını azaltır.  
- **Güvenilirlik** – Kaydedilen PSD dosyalarının herhangi bir makinede tam olarak aynı şekilde render edilmesini sağlar.  
- **Basitlik** – Tek bir metod çağrısı (`OpenTypeFontsCache.updateCache()`) tüm işi halleder.

## Ön Koşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- Java Development Kit (JDK) 8 veya daha yeni bir sürüm.  
- Aspose.PSD for Java kütüphanesi (resmi [download link](https://releases.aspose.com/psd/java/) üzerinden indirin).  
- Kodunuzdan referans verebileceğiniz bir klasörde bulunan örnek PSD dosyası (`sample.psd`).  

Her şey hazır olduğuna göre, uygulamaya geçelim.

## Paketleri İçe Aktarma

PSD görüntüleri ve yazı tipi önbelleğiyle çalışmak için gerekli sınıfları içe aktarın. Bu ifadeleri Java sınıfınızın en üstüne yerleştirin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.OpenTypeFontsCache;

import com.aspose.psd.fileformats.psd.PsdImage;
import java.io.Console;
import java.util.concurrent.TimeUnit;
```

### Adım 1: PSD Görüntüsünü Yükleme (How to load PSD)

Orijinal PSD dosyasını yükleyerek başlarız. Bu, yazı tipi önbelleği güncellenmeden önce yeniden kaydedebileceğimiz bir temel görüntü nesnesi sağlar.

```java
String dataDir = "Your Document Directory";

PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
image.save(dataDir + "NoFont.psd");
```

- **Açıklama:**  
  - `Image.load` dosyayı belleğe okur.  
  - `image.save` **NoFont.psd** adında bir kopya oluşturur; bu, yeni yazı tipleri mevcut **olmadan** önceki durumu yansıtır.  
  - Bu adım, karşılaştırma yapmak ve sonraki önbellek güncellemesinin çıktıyı gerçekten değiştirdiğini doğrulamak için faydalıdır.

### Adım 2: Yazı Tipi Kurulumunu Bekleme (Improve image performance)

Kullanıcıya gerekli yazı tipini manuel olarak kurması için zaman tanırız. Gerçek bir senaryoda bu adımı otomatikleştirebilirsiniz, ancak duraklama önbellek yenileme mekanizmasını gösterir.

```java
System.out.println("You have 2 minutes to install the font");
Thread.sleep(2 * 60 * 1000);
OpenTypeFontsCache.updateCache();
```

- **Açıklama:**  
  - `Thread.sleep` yürütmeyi **2 dakika** (2 × 60 × 1000 ms) duraklatır.  
  - `OpenTypeFontsCache.updateCache()` Aspose.PSD'nin sistemin OpenType yazı tiplerini yeniden taramasını zorlar, böylece yeni yüklenen yazı tipleri anında render için kullanılabilir.

### Adım 3: Güncellenmiş PSD Görüntüsünü Yükleme (Load PSD image) ve **PSD dosyasını kaydetme**

Önbellek yenilendikten sonra orijinal PSD'yi tekrar yükleriz. Bu kez yazı tipi bilgileri günceldir ve **PSD dosyasını kaydetme** işlemini doğru tipografiyle gerçekleştirebiliriz.

```java
PsdImage image1 = (PsdImage)Image.load(dataDir + "sample.psd");
image1.save(dataDir + "HasFont.psd");
```

- **Açıklama:**  
  - İkinci yükleme yeni yüklenen yazı tipini alır.  
  - **HasFont.psd** olarak kaydetmek, artık doğru yazı tipi render'ı içeren bir dosya üretir ve önbellek güncellemesinin başarılı olduğunu kanıtlar.

## Yaygın Sorunlar ve Çözümler

| Sorun | Nedeni | Çözüm |
|-------|--------|----------|
| Kaydedilen PSD hâlâ varsayılan yazı tipini gösteriyor | Yazı tipi, OS tarafından taranan bir konuma kurulmamış | Yazı tipini sistem yazı tipleri klasörüne (ör. Windows'ta `C:\Windows\Fonts`) kurun ve `updateCache()`'i yeniden çalıştırın. |
| `Thread.sleep` `InterruptedException` fırlatıyor | Metod imzası denetlenen istisnaları ele almıyor | `main` metodunuza `throws InterruptedException` ekleyin veya çağrıyı try‑catch bloğuna alın. |
| `OpenTypeFontsCache.updateCache()` bir şey yapmıyor | Yazı tipi yapılandırması olmayan bir headless sunucuda çalışıyor | Sunucunun gerekli yazı tiplerine sahip olduğundan ve Java sürecinin bunları okuma iznine sahip olduğundan emin olun. |

## Sık Sorulan Sorular

**S: Aspose.PSD tüm Java sürümleriyle uyumlu mu?**  
C: Aspose.PSD for Java, JDK 8 ve üzeri sürümleri destekler; bu, modern Java uygulamalarının çoğunu kapsar.

**S: Aspose.PSD'yi ticari projelerde kullanabilir miyim?**  
C: Evet. Üretim kullanımı için bir ticari lisans gereklidir. Lisansı [satın alma sayfasından](https://purchase.aspose.com/buy) temin edebilirsiniz.

**S: Ücretsiz bir deneme sürümü var mı?**  
C: Kesinlikle! Deneme sürümünü [releases sayfasından](https://releases.aspose.com/) indirebilirsiniz.

**S: Topluluk desteğini nereden bulabilirim?**  
C: İpuçları ve sorun giderme için [Aspose.PSD forumuna](https://forum.aspose.com/c/psd/34) katılabilirsiniz.

**S: Test için geçici bir lisans nasıl alabilirim?**  
C: Kısa vadeli bir lisans talep etmek için [geçici lisans sayfasını](https://purchase.aspose.com/temporary-license/) ziyaret edin.

## Sonuç

Artık **PSD dosyasını kaydetme** işlemini yazı tipi önbelleğini zorlayarak nasıl yapacağınızı öğrendiniz; böylece PSD çıktılarınız her seferinde doğru tipografiyle render edilir. Bu teknik, **görüntü işleme optimizasyonu**nun basit ama güçlü bir parçasıdır ve güvenilir, yüksek performanslı PSD manipülasyonu gerektiren daha büyük iş akışlarına entegre edilebilir.

---

**Son Güncelleme:** 2025-12-01  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en yeni)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}