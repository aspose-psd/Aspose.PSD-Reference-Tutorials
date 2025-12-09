---
date: 2025-12-02
description: Aspose.PSD görüntü işleme Java kütüphanesini kullanarak, Ters Çevirme
  Ayar Katmanı da dahil olmak üzere birden fazla ayar katmanını uygulamayı öğrenin
  ve sorunsuz PSD manipülasyonu yapın.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Görüntü İşleme Java Kütüphanesi: Aspose.PSD ile Katmanı Tersine Çevir'
url: /tr/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java'da Invert Ayar Katmanı

## Giriş

Sağlam bir **image processing java library** arıyorsanız, Aspose.PSD for Java piyasadaki en çok yönlü seçeneklerden biridir. Bu öğreticide, bir PSD dosyasına **Invert Ayar Katmanı** eklemeyi adım adım göstereceğiz; bu tekniği diğer ayar katmanlarıyla birleştirerek karmaşık görsel efektler elde edebilirsiniz. İster toplu işleme aracı ister tek bir resim editörü geliştirin, bu kılavuz işi hızlıca halletmeniz için net bir yol haritası sunar.

## Hızlı Yanıtlar
- **Invert Ayar Katmanı ne işe yarar?** Seçili alandaki tüm renk değerlerini ters çevirir, negatif‑görüntü etkisi oluşturur.  
- **Bu özelliği hangi kütüphane sağlar?** Aspose.PSD, önde gelen bir image processing java library.  
- **Diğer ayarlarla birleştirebilir miyim?** Evet – **Brightness/Contrast**, **Hue/Saturation** gibi birden fazla ayar katmanını **apply multiple adjustment layers** şeklinde uygulayabilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü mevcuttur; üretim kullanımı için lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir senaryo için genellikle 10 dakikadan az sürer.

## Invert Ayar Katmanı Nedir?

Invert Ayar Katmanı, etkilediği her pikselin RGB değerlerini ters çeviren yıkıcı olmayan bir düzenlemedir. Katman yığını üzerinde bulunduğu için görünürlüğünü açıp kapatabilir veya yeniden sıralayabilirsiniz; orijinal görüntü verileri kalıcı olarak değişmez.

## Neden Aspose.PSD'yi Image Processing Java Library'niz Olarak Kullanmalısınız?

- **Tam PSD desteği** – Photoshop yüklü olmadan Photoshop dosyalarını okuyabilir, düzenleyebilir ve yazabilirsiniz.  
- **Çapraz platform** – herhangi bir Java çalışma zamanı (Java 6+) üzerinde çalışır.  
- **Zengin ayar özellikleri** – birçok yaygın düzenleme için yerleşik metodlar içerir, bu da **apply multiple adjustment layers** işlemini tek bir iş akışında kolaylaştırır.  
- **Performans‑optimizeli** – büyük dosyaları verimli bir şekilde işler, bu da toplu işleme için kritiktir.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.PSD Kütüphanesi** – resmi siteden [buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.  
2. **Java Geliştirme Ortamı** – JDK 6.0 veya daha yeni bir sürüm kurulu ve yapılandırılmış olmalı.  

Şimdi koda dalalım.

## Paketleri İçe Aktarma

Gerekli sınıfları içe aktararak başlayın. Bu importlar, çekirdek image‑handling API'lerine ve PSD‑özel işlevselliğe erişim sağlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Adım 1: Belge Dizinini Ayarlama

Kaynak PSD dosyanızın bulunduğu ve çıktının kaydedileceği klasörü tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: PSD Dosyasını Yükleme

Kaynak dosyayı bir `PsdImage` nesnesine yükleyin. Bu nesne, PSD belgesinin tamamını bellekte temsil eder.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Adım 3: Invert Ayar Katmanı Ekleme

Mevcut katman yığını üzerine bir Invert Ayar Katmanı eklemek için yerleşik metodu çağırın. Daha sonra (ör. Brightness, Hue) ek katmanlar ekleyerek **apply multiple adjustment layers** yapabilirsiniz.

```java
im.addInvertAdjustmentLayer();
```

## Adım 4: Çıktıyı Kaydetme

Değiştirilmiş PSD'yi diske kalıcı olarak kaydedin. Kaydedilen dosya artık Invert Ayar Katmanı içerir ve Photoshop ya da herhangi bir PSD‑uyumlu görüntüleyicide açılabilir.

```java
im.save(outputPath);
```

### Ne oldu?

- PSD belleğe yüklendi.  
- En üst katman olarak bir Invert Ayar Katmanı eklendi.  
- Görüntü kaydedildi, yıkıcı olmayan düzenleme korundu.

Artık bir **image processing java library** olan Aspose.PSD'yi kullanarak bir PSD dosyasını başarıyla manipüle ettiniz.

## Yaygın Sorunlar & İpuçları

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| **`Image.load` üzerinde NullPointerException** | Yanlış dosya yolu veya dosyanın eksik olması | `dataDir` ve dosya adını kontrol edin; test için mutlak yollar kullanın |
| **Katman sırası beklendiği gibi değil** | Katman ekleme işlemi mevcut katmanların üzerine yapıldığında yığın değişir | Diğer ayarlardan önce `im.addInvertAdjustmentLayer()` çağırın veya `im.getLayers()` ile katmanları yeniden sırala |
| **Büyük PSD'lerde performans yavaşlaması** | Çok büyük dosyaların belleğe yüklenmesi | Sayfaları parçalar halinde işleyin veya JVM heap boyutunu artırın (`-Xmx2g`) |

## Sık Sorulan Sorular

**S: Aspose.PSD tüm Java sürümleriyle uyumlu mu?**  
C: Aspose.PSD Java 6.0 ve sonraki sürümleri destekler.

**S: Tek bir işlemde birden fazla ayar katmanı uygulayabilir miyim?**  
C: Evet, Invert, Brightness ve Hue/Saturation gibi birden fazla ayar katmanını üst üste ekleyerek karmaşık efektler elde edebilirsiniz.

**S: Aspose.PSD için ek dokümantasyon nerede bulunur?**  
C: Kapsamlı kılavuzlar ve API referansları için [buradaki](https://reference.aspose.com/psd/java/) dokümantasyona bakın.

**S: Aspose.PSD için ücretsiz deneme mevcut mu?**  
C: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

**S: Aspose.PSD için geçici bir lisans nasıl alınır?**  
C: Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

---

**Son Güncelleme:** 2025-12-02  
**Test Edilen Sürüm:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}