---
date: 2026-11-04
description: Aspose.PSD for Java'yı kullanarak invert adjustment layer uygulamayı,
  PSD görüntülerini toplu işleme almayı ve negatif görüntü PSD dosyaları oluşturmayı
  öğrenin.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Aspose.PSD for Java'yı kullanarak invert adjustment layer eklemeyi,
  PSD görüntülerini toplu işleme almayı ve negatif bir PSD oluşturmayı öğrenin. Adım
  adım kılavuzu izleyin.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Java'da invert adjustment layer eklemek için Aspose.PSD nasıl kullanılır
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Java'da invert adjustment layer eklemek için Aspose.PSD nasıl kullanılır
url: /tr/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD'yi Java'da ters çevirme ayar katmanı eklemek için nasıl kullanılır

## Giriş

Eğer sağlam bir **image processing java library** arıyorsanız, Aspose.PSD for Java piyasadaki en çok yönlü seçeneklerden biridir. Bu öğreticide **Aspose**'u nasıl kullanarak bir PSD dosyasına **Invert Adjustment Layer** ekleyeceğinizi, bunu diğer ayarlarla birleştireceğinizi ve hatta işlemi onlarca dosya üzerinde çalıştıracağınızı göreceksiniz. İster toplu‑işlem aracı, ister sunucu‑tarafı görüntü hizmeti, ister tek‑görüntü düzenleyici oluşturuyor olun, aşağıdaki adımlar kaynak PSD'den tamamen düzenlenebilir bir negatif görüntüye dakikalar içinde ulaşmanızı sağlayacak.

## Hızlı Yanıtlar
- **Invert Adjustment Layer ne yapar?** Seçili alandaki her RGB değerini ters çevirir ve görüntüyü fotoğrafik bir negatif haline getirir.  
- **Bu özelliği hangi kütüphane sağlar?** Aspose.PSD, önde gelen bir **image processing java library**.  
- **Bunu diğer ayarlarla birleştirebilir miyim?** Evet – Brightness/Contrast, Hue/Saturation gibi **apply multiple adjustment layers** ekleyebilir ve daha fazlasını yapabilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme mevcuttur; üretim kullanımı için lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir kullanım senaryosu için genellikle 10 dakikadan az sürer.

## Invert Adjustment Layer Nedir?

Invert Adjustment Layer, etkilediği her pikselin renk değerlerini tersine çeviren yok edici olmayan bir düzenlemedir. Katman yığını üzerinde en üstte yer aldığından, görünürlüğünü açıp kapatabilir veya yeniden sıralayabilirsiniz; orijinal görüntü verileri kalıcı olarak değişmez. Bu, **create negative image PSD** dosyaları oluşturmanın veya klasik film‑negatif görünüm elde etmenin en hızlı yoludur.

## Neden Aspose.PSD'yi image processing java library olarak kullanmalısınız?

Aspose.PSD, **200+ PSD features**'ı destekler, Photoshop gerektirmeden Photoshop dosyalarını okuyup yazabilir ve çok sayfalı belgeleri 500 MB'den az yığın belleği kullanarak işler. Herhangi bir Java çalışma zamanı (Java 6+) üzerinde çalışır, bu da Windows, Linux veya macOS sunucularında **batch process psd images** için ideal kılar.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Aspose.PSD for Java** – resmi siteden en son JAR'ı indirin [Aspose.PSD for Java indirme sayfası](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 veya daha yeni bir sürümün `PATH` içinde kurulu ve yapılandırılmış olduğundan emin olun.  

Artık kodu yazmaya hazırsınız.

## Paketleri İçe Aktarma

`PsdImage` sınıfı, bellekte bir bütün Photoshop belgesini temsil eder, ayar‑katman sınıfları ise `com.aspose.psd.layers.adjustments` paketinde bulunur.

`PsdImage` sınıfı, Aspose.PSD'nin üst‑seviye nesnesi olup bir PSD dosyasının yapısını ve piksel verilerini kapsar. Ad alanlarını içe aktarın, ardından PSD dosyalarını yükleyebilir, düzenleyebilir ve kaydedebilirsiniz.

## Adım 1: belge dizinini ayarlama

Kaynak PSD dosyanızı içeren ve çıktının kaydedileceği klasörü tanımlayın. Mutlak yollar kullanmak, çalışma dizini değiştiğinde `NullPointerException` oluşmasını önler.

## Adım 2: PSD dosyasını yükleme

Kaynak dosyayı bir `PsdImage` nesnesine yükleyin. Bu nesne, bellekte tam katman hiyerarşisini tutar ve yok edici olmayan düzenlemelere olanak tanır.

`PsdImage` sınıfı, dosya başlığını okuyan, formatı doğrulayan ve manipülasyona hazır bir bellek içi temsil oluşturan statik bir `load` yöntemi sunar.

## Adım 3: invert adjustment layer ekleme

Mevcut katman yığınının üstüne bir Invert Adjustment Layer eklemek için yerleşik yöntemi çağırın. Daha sonra (ör. Brightness, Hue) gibi daha fazla katman ekleyerek tek bir iş akışında **apply multiple adjustment layers** yapabilirsiniz.

`addInvertAdjustmentLayer()` PSD'nin katman koleksiyonuna bir Invert Adjustment Layer ekler.

## Adım 4: çıktıyı kaydetme

Değiştirilmiş PSD'yi diske kaydedin.

`save()` belirtilen yola, tüm katmanlar ve meta veriler dahil PSD dosyasını yazar.

Kaydetme, tüm ayar katmanları, maskeler ve meta veriler dahil tam belgeyi belirtilen formata yazan aynı `save` yöntemini kullanır.

### Ne oldu?

PSD dosyası bir `PsdImage` nesnesine yüklendi, bir `InvertAdjustmentLayer` oluşturuldu ve en üst katman olarak eklendi, ardından belge kaydedildi. Bu sıra, orijinal görüntü verilerini korurken daha sonra açılıp kapatılabilir veya yeniden sıralanabilir bir yok edici olmayan ters çevirme etkisi ekler.

Artık bir PSD dosyasını manipüle etmek için Aspose.PSD, bir **image processing java library**, başarıyla kullandınız.

## Invert ayarıyla PSD görüntülerini toplu işleme nasıl yapılır?

Her dosyayı bir `for` döngüsü içinde yükleyin, aynı adımları uygulayın ve her yineleme için `save` çağırın. Aspose.PSD dosyaları akış biçiminde işlediği için aynı `PsdImage` örneğini yeniden kullanarak **hundreds of PSDs** işleyebilir ve bellek kullanımını 300 MB'nin altında tutabilirsiniz.

## Bir PSD'yi negatif görüntüye nasıl dönüştürürsünüz?

Invert Adjustment Layer'ı en üst öğe olarak ekleyin ve belgeyi kaydedin – bu işlem **convert PSD to negative** ile eşdeğerdir. Daha sonra katmanı devre dışı bırakabilir veya silebilir ve kaynak dosyayı yeniden yüklemeden orijinal görünüme geri dönebilirsiniz.

## Yaygın sorunlar ve ipuçları

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| **`Image.load` sırasında NullPointerException** | Yanlış dosya yolu veya eksik dosya | `dataDir` ve dosya adını doğrulayın; test için mutlak yollar kullanın |
| **Katman sırası beklenildiği gibi değil** | Mevcut katmanların üzerine katman eklemek yığını değiştirir | Invert katmanını diğer ayarlardan önce ekleyin veya `psdImage.getLayers().move()` ile yeniden sıralayın |
| **Büyük PSD'lerde performans yavaşlaması** | Çok büyük dosyaları belleğe yüklemek | JVM yığınını artırın (`-Xmx2g`) veya `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` kullanarak dosyaları parçalar halinde işleyin |

## Sıkça Sorulan Sorular

**S: Aspose.PSD tüm Java sürümleriyle uyumlu mu?**  
A: Evet, Java 6.0 ve üzerini, Java 8, 11 ve 17 dahil destekler.

**S: Tek bir işlemde birden fazla ayar katmanı uygulayabilir miyim?**  
A: Kesinlikle. Invert katmanını ekledikten sonra `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()` gibi metodları çağırarak efektleri üst üste ekleyebilirsiniz.

**S: Tam API referansını nerede bulabilirim?**  
A: Tam dökümantasyon [Aspose.PSD Java API referansı](https://reference.aspose.com/psd/java/) adresinde mevcuttur.

**S: Aspose.PSD için ücretsiz deneme var mı?**  
A: Evet, bir deneme sürümünü [Aspose.PSD deneme indirme](https://releases.aspose.com/) adresinden indirebilirsiniz.

**S: Test için geçici bir lisans nasıl alabilirim?**  
A: Geçici bir lisans talep edin [geçici lisans talep sayfası](https://purchase.aspose.com/temporary-license/).

**Son Güncelleme:** 2026-11-04  
**Test Edilen:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## İlgili Öğreticiler

- [Aspose.PSD for Java ile PSD Dosyalarına Seviye Ayar Katmanı Ekleme](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [PSD'de Ayar Katmanı – Kanal Karıştırıcı Nasıl Eklenir (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [PSD'yi Düzenleme - Java Kullanarak Eğriler Ayar Katmanı Ekleme](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}