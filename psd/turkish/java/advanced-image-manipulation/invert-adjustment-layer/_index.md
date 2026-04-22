---
date: 2026-02-07
description: Aspose.PSD görüntü işleme Java kütüphanesini kullanarak, Ters Çevirme
  Ayar Katmanı da dahil olmak üzere birden fazla ayar katmanını uygulamayı ve sorunsuz
  PSD manipülasyonu yapmayı öğrenin.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Görüntü İşleme Java Kütüphanesi: Aspose.PSD ile Katmanı Ters Çevir'
url: /tr/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java'da Ters Çevirme Ayar Katmanı

## Introduction

Eğer sağlam bir **image processing java library** arıyorsanız, Aspose.PSD for Java piyasadaki en çok yönlü seçeneklerden biridir. Bu öğreticide, bir PSD dosyasına **Invert Adjustment Layer** eklemenin adımlarını göstereceğiz; bu tekniği diğer ayar katmanlarıyla birleştirerek karmaşık görsel efektler elde edebilirsiniz. İster toplu‑işleme aracı ister tek‑resim editörü geliştirin, bu kılavuz işi hızlı bir şekilde tamamlamanız için net, adım‑adım bir yol sunar.

## Quick Answers
- **Invert Adjustment Layer ne yapar?** Seçili alandaki tüm renk değerlerini ters çevirir ve negatif‑görüntü etkisi oluşturur.  
- **Bu özelliği hangi kütüphane sağlar?** Aspose.PSD, önde gelen bir image processing java library.  
- **Diğer ayarlarla birleştirilebilir mi?** Evet – **apply multiple adjustment layers** gibi Brightness/Contrast, Hue/Saturation ve daha fazlasını ekleyebilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme mevcuttur; üretim kullanımı için lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir senaryo için genellikle 10 dakikadan az sürer.

## What is the Invert Adjustment Layer?

Invert Adjustment Layer, etkilediği her pikselin RGB değerlerini ters çeviren yıkıcı olmayan bir düzenlemedir. Katman yığını üzerinde bulunduğu için görünürlüğünü açıp kapatabilir veya yeniden sıralayabilirsiniz; orijinal görüntü verileri kalıcı olarak değişmez.

## How to invert layer using Aspose.PSD

Aşağıda bir PSD dosyasında **how to invert layer** işleminin tam olarak nasıl yapılacağını göreceksiniz. Adımlar özellikle basit tutulmuştur, böylece kavrama odaklanabilir, kod kalabalığından uzak durabilirsiniz.

## Why Use Aspose.PSD as Your Image Processing Java Library?

- **Full PSD support** – Photoshop yüklü olmadan Photoshop dosyalarını okuyun, düzenleyin ve yazın.  
- **Cross‑platform** – herhangi bir Java çalışma ortamında (Java 6+) çalışır.  
- **Rich adjustment features** – birçok yaygın düzenleme için yerleşik yöntemler içerir, bu da **apply multiple adjustment layers** işlemini tek bir iş akışında kolaylaştırır.  
- **Performance‑optimized** – büyük dosyaları verimli bir şekilde işler, bu da toplu işleme için kritiktir.

## Prerequisites

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.PSD Library** – resmi siteden [here](https://releases.aspose.com/psd/java/) indirebilirsiniz.  
2. **Java Development Environment** – JDK 6.0 veya daha yeni bir sürüm kurulu ve yapılandırılmış olmalı.  

Şimdi koda dalalım.

## Import Packages

Gerekli sınıfları içe aktararak başlayın. Bu importlar, çekirdek image‑handling API'lerine ve PSD‑özel işlevselliğe erişim sağlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Step 1: Set Up Document Directory

Kaynak PSD dosyanızın bulunduğu ve çıktının kaydedileceği klasörü tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load PSD File

Kaynak dosyayı bir `PsdImage` nesnesine yükleyin. Bu nesne, tüm PSD belgesini bellekte temsil eder.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Step 3: Add Invert Adjustment Layer

Mevcut katman yığınının üzerine bir Invert Adjustment Layer eklemek için yerleşik yöntemi çağırın. Daha sonra (ör. Brightness, Hue) ek katmanlar ekleyerek **apply multiple adjustment layers** yapabilirsiniz.

```java
im.addInvertAdjustmentLayer();
```

## Step 4: Save the Output

Değiştirilmiş PSD'yi diske kaydedin. Kaydedilen dosya artık Invert Adjustment Layer'ı içerir ve Photoshop ya da herhangi bir PSD‑uyumlu görüntüleyicide açılabilir.

```java
im.save(outputPath);
```

### What just happened?

- PSD belleğe yüklendi.  
- En üst katman olarak bir Invert Adjustment Layer eklendi.  
- Görüntü kaydedildi, yıkıcı olmayan düzenleme korunmuş oldu.

Artık bir **image processing java library** olan Aspose.PSD'yi kullanarak bir PSD dosyasını başarıyla manipüle ettiniz.

## Common Issues & Tips

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | Yanlış dosya yolu veya eksik dosya | `dataDir` ve dosya adını doğrulayın; test için mutlak yollar kullanın |
| **Layer order not as expected** | Katmanlar mevcut olanların üzerine eklendiğinde yığın değişir | Diğer ayarlardan önce `im.addInvertAdjustmentLayer()` kullanın veya katmanları `im.getLayers()` ile yeniden sıralayın |
| **Performance slowdown on large PSDs** | Çok büyük dosyaların belleğe yüklenmesi | Sayfaları parçalar halinde işleyin veya JVM yığın boyutunu artırın (`-Xmx2g`) |

## Frequently Asked Questions

**Q: Aspose.PSD tüm Java sürümleriyle uyumlu mu?**  
A: Aspose.PSD Java 6.0 ve sonraki sürümleri destekler.

**Q: Tek bir işlemde birden fazla ayar katmanı uygulayabilir miyim?**  
A: Evet, Invert, Brightness ve Hue/Saturation gibi birden fazla ayar katmanını üst üste ekleyerek karmaşık efektler elde edebilirsiniz.

**Q: Aspose.PSD için ek belgeleri nerede bulabilirim?**  
A: Kapsamlı kılavuzlar ve API referansları için belgeleri [here](https://reference.aspose.com/psd/java/) inceleyin.

**Q: Aspose.PSD için ücretsiz deneme mevcut mu?**  
A: Evet, ücretsiz denemeyi [here](https://releases.aspose.com/) keşfedebilirsiniz.

**Q: Aspose.PSD için geçici bir lisans nasıl alabilirim?**  
A: Geçici lisansı [here](https://purchase.aspose.com/temporary-license/) üzerinden temin edebilirsiniz.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}