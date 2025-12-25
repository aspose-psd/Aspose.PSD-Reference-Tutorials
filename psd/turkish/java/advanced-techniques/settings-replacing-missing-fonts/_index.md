---
date: 2025-12-25
description: Aspose.PSD for Java ile PSD dosyalarındaki yazı tiplerini nasıl değiştireceğinizi
  öğrenin – aynı zamanda PSD'yi PNG olarak kaydetmeyi ve eksik yazı tiplerini yönetmeyi
  gösteren adım adım bir rehber.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java'da Yazı Tiplerini Nasıl Değiştirilir
url: /tr/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java'da Yazı Tiplerini Nasıl Değiştirilir

## Introduction

Java uygulamanızda Photoshop (PSD) dosyalarıyla çalışıyorsanız, eksik yazı tipleri görsel düzeni bozabilir ve render hatalarına yol açabilir. **Yazı tiplerini değiştirme** işlemini hızlı ve güvenilir bir şekilde yapmak, tasarım bütünlüğünü korumak için çok önemlidir. Bu öğreticide, eksik yazı tiplerini değiştirmek, sonucu PNG'ye dönüştürmek ve görüntü dönüştürme iş akışınızı sorunsuz tutmak için Aspose.PSD for Java'yı nasıl kullanacağınızı öğreneceksiniz. Sonunda, görüntülerde yazı tiplerini değiştirebilecek, PSD'yi PNG olarak kaydedebilecek ve geliştiricilerin sıkça karşılaştığı sorunlardan kaçınabileceksiniz.

## Quick Answers
- **“replace fonts” PSD işleme içinde ne anlama geliyor?** Eksik veya mevcut olmayan yazı tiplerini, belirttiğiniz yedek bir yazı tipiyle değiştirir.  
- **Bu işlemi otomatik olarak hangi kütüphane yapıyor?** Aspose.PSD for Java, `PsdLoadOptions.setDefaultReplacementFont` metodunu sağlar.  
- **Değiştirme sonrası PSD'yi PNG'ye de dönüştürebilir miyim?** Evet – `PngOptions` kullanın ve `psdImage.save` metodunu çağırın.  
- **Üretim ortamında lisansa ihtiyacım var mı?** Değerlendirme dışı derlemeler için geçerli bir Aspose.PSD lisansı gereklidir.  
- **Hangi Java sürümü destekleniyor?** Şu anki Aspose.PSD sürümü, Java 8+ çalışma zamanlarıyla uyumludur.

## What is Font Replacement in PSD Files?

Bir PSD, ana bilgisayarda yüklü olmayan bir yazı tipine referans verdiğinde, render motoru genellikle genel bir yazı tipine geri döner ve bu da metnin hizalanmasının bozulmasına neden olur. Yazı tipi değiştirme, eksik bir yazı tipiyle karşılaştığında kütüphanenin kullanacağı varsayılan bir yazı tipi (ör. Arial) tanımlamanıza olanak tanır; böylece tutarlı bir görsel çıktı elde edilir.

## Why Replace Missing Fonts with Aspose.PSD?

- **Zero‑dependency solution** – Yerel Photoshop veya dış araçlara gerek yok.  
- **Batch‑ready** – Aynı ayarlarla döngü içinde onlarca dosyayı işleyin.  
- **Image conversion ready** – Değiştirme sonrası **save PSD as PNG** veya **convert PSD to PNG** işlemlerini ekstra adım olmadan doğrudan yapabilirsiniz.  
- **Cross‑platform** – Windows, Linux ve macOS Java çalışma zamanlarında çalışır.

## Prerequisites

1. **Aspose.PSD Library** – Aspose.PSD for Java kütüphanesini [releases page](https://releases.aspose.com/psd/java/) üzerinden indirin ve kurun.  
2. **Java Development Environment** – JDK 8 veya daha yeni bir sürüm yüklü ve yapılandırılmış olmalı.  

Şimdi temel gereksinimler elimizde, koda geçelim.

## Import Packages

Gerekli Aspose.PSD sınıflarını içe aktararak başlayın. Bu, görüntü yükleme, yazı tipi değiştirme seçenekleri ve PNG dışa aktarım yeteneklerine erişmenizi sağlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Set Up Your Document Directory

Kaynak PSD'nin bulunduğu ve üretilen PNG'nin kaydedileceği klasörü tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Specify Source and Destination Files

Giriş PSD ve çıkış PNG için tam yolları belirtin. Bu, iş akışını netleştirir ve kodun bakımını kolaylaştırır.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Step 3: Configure Font Replacement Settings

Bir `PsdLoadOptions` örneği oluşturun ve Aspose.PSD'ye eksik bir yazı tipiyle karşılaştığında hangi yazı tipini kullanacağını söyleyin. Bu örnekte **Arial** kullanıyoruz, ancak sisteminizde yüklü herhangi bir yazı tipiyle değiştirebilirsiniz.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Step 4: Load PSD Image and Replace Fonts

Yukarıda tanımladığınız seçeneklerle PSD'yi yükleyin. Kütüphane, eksik tüm yazı tiplerini belirttiğiniz varsayılanla otomatik olarak değiştirir.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Step 5: Save the Modified Image

Şeffaflığı korumak için alfa kanalı içeren gerçek renkli PNG dışa aktarım seçeneklerini yapılandırın. Bu adım aynı zamanda yazı tipi değiştirme sonrası **image conversion PSD to PNG** işlemini gösterir.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### What Just Happened?

- PSD, yedek bir yazı tipi (Arial) ile açıldı.  
- Başlangıçta eksik yazı tiplerine referans veren tüm metin katmanları artık Arial ile render edildi.  
- Son görüntü PNG olarak kaydedildi; böylece **saving PSD as PNG** işlemi görsel bütünlüğü koruyarak tamamlandı.

## Common Issues & Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| Metin hâlâ yanlış görünüyor | Yazı tipi metrikleri farklı (boyut, kalınlık) | Değiştirme yazı tipi boyutunu programatik olarak ayarlayın veya benzer metriklere sahip bir yazı tipi seçin. |
| PNG beklenenden büyük | Varsayılan PNG seçenekleri 32‑bit renk kullanıyor | Alfa kanalı gerekmediğinde `PngColorType`'ı `Truecolor` olarak değiştirin. |
| Lisans istisnası | Geçerli bir lisans olmadan çalıştırılıyor | Görüntüyü yüklemeden önce geçici veya kalıcı bir Aspose.PSD lisansı uygulayın. |

## Frequently Asked Questions

**Q: Aspose.PSD tüm PSD dosya sürümleriyle uyumlu mu?**  
A: Aspose.PSD, erken Photoshop sürümlerinden en yeni özelliklere kadar geniş bir PSD sürüm yelpazesini destekler.

**Q: Aspose.PSD'de değiştirme için özel yazı tipleri kullanabilir miyim?**  
A: Evet, sadece özel yazı tipi adını `setDefaultReplacementFont` metoduna geçirin. Yazı tipinin JVM tarafından erişilebilir olduğundan emin olun.

**Q: Aspose.PSD için lisans seçenekleri mevcut mu?**  
A: İhtiyacınıza en uygun planı seçmek için lisans seçeneklerini [burada](https://purchase.aspose.com/buy) inceleyin.

**Q: Aspose.PSD desteği için bir topluluk forumu var mı?**  
A: Evet, topluluk desteği ve tartışmalar için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

**Q: Aspose.PSD için geçici bir lisans nasıl alabilirim?**  
A: Test ve değerlendirme amaçları için geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

---

**Last Updated:** 2025-12-25  
**Tested With:** Aspose.PSD 24.11 for Java (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}