---
date: 2026-03-18
description: Aspose.PSD for Java ile psd'yi png'ye dönüştürürken png bit derinliğini
  değiştirmeyi öğrenin – adım adım rehber ve kod örnekleri.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java Kullanarak Belirli Bit Derinliğiyle PSD'yi PNG'ye Dönüştürme
url: /tr/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java Kullanarak Belirtilen Bit Derinliğiyle PSD'yi PNG'ye Dönüştürme

## Introduction
Eğer **psd'yi png'ye dönüştürmeniz** ve tam PNG bit derinliğini kontrol etmeniz gerekiyorsa doğru yerdesiniz. Bu öğreticide, Aspose.PSD for Java ile bir PSD dosyasını PNG görüntüsü olarak kaydederken png bit derinliğini nasıl değiştireceğinizi adım adım göstereceğiz. İster toplu‑işlem aracı, bir web servisi ya da bir masaüstü yardımcı programı geliştiriyor olun, **png'yi seçeneklerle kaydetme** gibi gri tonlamalı renk tipi ve özel bit derinliği gibi özellikler, görüntü kalitesi ve dosya boyutu üzerinde ayrıntılı kontrol sağlar.

## Quick Answers
- **PNG bit derinliğini değiştirebilir miyim?** Evet – `PngOptions.setBitDepth()` kullanarak 1, 2, 4, 8 veya 16 bit belirtebilirsiniz.  
- **Hangi renk tipleri destekleniyor?** Gri tonlamalı, TrueColor, Indexed ve diğerleri `PngColorType` aracılığıyla.  
- **Aspose.PSD için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir.  
- **Hangi Java sürümü gerekiyor?** Java 8+ (kütüphane daha yeni JDK'larla uyumludur).  
- **Kod olduğu gibi çalıştırılabilir mi?** Evet – sadece yer tutucu yolu kendi klasörünüzle değiştirin.

## What is “convert psd to png” with custom bit depth?
Photoshop PSD dosyasını PNG görüntüsüne dönüştürmek, web‑uyumlu bir format gerektiğinde yaygın bir görevdir. Bit derinliğini ayarlayarak **png kalitesini ayarlama** yeteneği eklemek, görsel doğruluk ile dosya boyutu arasında denge kurmanızı sağlar; bu, özellikle küçük resimler, simgeler veya bant genişliği sınırlı olduğunda faydalıdır.

## Why use Aspose.PSD for Java?
Aspose.PSD for Java, PSD formatının karmaşıklığını soyutlayan yüksek seviyeli bir API sunar. **gri tonlamalı png oluşturmanıza**, **png'yi seçeneklerle kaydetmenize** ve renk profillerini düşük seviyeli bayt manipülasyonu yapmadan yönetmenize olanak tanır. Kütüphane tamamen yönetilen, çok platformlu ve düzenli güncellemeler alır.

## Prerequisites
Koda geçmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – [Oracle’ın web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin.  
2. **Aspose.PSD for Java** – en son JAR dosyasını [bu linkten](https://releases.aspose.com/psd/java/) edinin.  
3. **Temel Java bilgisi** – sınıflar, metodlar ve istisna yönetimi konusunda rahat olmalısınız.  
4. **Bir IDE** (IntelliJ IDEA veya Eclipse gibi) (isteğe bağlı ama önerilir).  
5. **Örnek bir PSD dosyası** – kodda referans göstereceğiniz bir klasöre yerleştirin.

Her şey hazır mı? Harika – gerekli paketleri içe aktaralım.

## Import Packages
Gereksinimlerimizi karşıladığımıza göre, Java uygulamamızda ilgili paketleri içe aktararak ortamımızı kurma zamanı. Kodlama ortamınızı başlatın ve Java dosyanızın en üstüne aşağıdaki import ifadelerini ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Bu ifadeler, öğretici boyunca kullanacağımız sınıfları içe aktarır ve PSD dosyalarını yükleyip belirtilen bit derinliğiyle PNG görüntüleri olarak kaydetmemizi sağlar.

## Step 1: Set Up Your Document Directory
Görüntü işlemine başlamadan önce, görüntülerimizin saklanacağı bir dizin tanımlayalım. Bu, bir el işi projesine başlamadan önce sanat malzemeleriniz için bir klasör oluşturmak gibidir.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the PSD Image
Sırada, dönüştürmek istediğiniz PSD görüntü dosyasını yüklememiz var. Bunu, tüm çalışmanızı yapacağınız bir tuvali açmak olarak düşünün.

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Burada, örnek PSD dosyamızı okumak ve PSD‑özel özelliklerine erişmek için `Image.load()` metodunu kullanıyor ve sonucu `PsdImage` tipine dönüştürüyoruz.

## Step 3: Create PNG Options
Tuvalimizi açtıktan sonra, görüntüyü nasıl kaydedeceğimize dair bir dizi seçenek belirlememiz gerekiyor. Bu, resim yapmaya başlamadan önce renklerinizi ve fırça stillerinizi seçmek gibidir.

```java
PngOptions options = new PngOptions();
```

Bu adımda, PNG çıktımız için parametreleri belirlememizi sağlayan bir `PngOptions` örneği başlatıyoruz.

## Step 4: Set the Desired Color Type
Şimdi, nihai PNG görüntümüzde hangi renk tipini istediğimize karar veriyoruz. Renkli bir palet mi yoksa tek renkli bir stil mi tercih ediyorsunuz? Kararı verelim!

```java
options.setColorType(PngColorType.Grayscale);
```

Bu örnekte renk tipini gri tonlamalı olarak ayarlıyoruz. Tam renkli bir görüntü isterseniz `PngColorType.TrueColor` seçeneğini de kullanabilirsiniz. İşte **gri tonlamalı png oluşturma** kısmı.

## Step 5: Specify the Bit Depth
Şimdi bit derinliğini belirleyelim. Bu, yazıcınıza görüntüyü ne kadar ince basması gerektiğini söylemek gibidir – daha fazla bit, daha fazla detay!

```java
options.setBitDepth((byte)1);
```

Burada, basit gri tonlamalı görüntüler için uygun olan **1 bit** bit derinliğini ayarlıyoruz. Kalite gereksinimlerinize bağlı olarak değeri 2, 4, 8 veya 16 olarak değiştirebilirsiniz – **png bit derinliğini değiştirme** klasik bir örneğidir.

## Step 6: Save the PNG Image
Son olarak, başyapıtınızı kaydetme zamanı! Bu adım, sanat eserimizi düzenleme tuvalinden galeri duvarına aktarmamızı sağlayarak projemizi tamamlar.

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

`PsdImage`'in `save()` metodunu kullanarak, tanımladığımız seçenekleri uygulayarak dönüştürülmüş dosyayı kaydediyoruz. İşte! Görüntümüz artık özel bit derinliğiyle kaydedildi.

## Common Issues and Solutions
- **PSD yüklenirken `NullPointerException`** – `dataDir`'in doğru klasöre işaret ettiğini ve `sample.psd` dosyasının mevcut olduğunu iki kez kontrol edin.  
- **Desteklenmeyen bit derinliği** – Aspose.PSD, PNG için 1, 2, 4, 8 ve 16 biti destekler. Başka bir değer kullanmak `IllegalArgumentException` hatasına yol açar.  
- **Renk tipi uyumsuzluğu** – seçilen `PngColorType` ile uyumlu olmayan bir bit derinliği ayarlarsanız, kütüphane otomatik olarak en yakın desteklenen ayara geçer.

## Frequently Asked Questions

**Q: Aspose.PSD for Java nedir?**  
A: Aspose.PSD for Java, Java uygulamalarında PSD dosyalarıyla çalışmak için bir kütüphanedir; görüntüleri manipüle etmenize ve dönüştürmenize olanak tanır.

**Q: Farklı bit derinliklerini nasıl belirtebilirim?**  
A: `options.setBitDepth((byte)n)` metodunu kullanarak bit derinliğini ayarlayabilirsiniz; `n` yerine istediğiniz değeri koyun.

**Q: Aspose.PSD'yi ücretsiz kullanabilir miyim?**  
A: Evet, kütüphaneyi ücretsiz deneme sürümüyle deneyebilirsiniz; deneme sürümünü [burada](https://releases.aspose.com/) bulabilirsiniz.

**Q: Aspose için destek lisansı nereden alınır?**  
A: Geçici bir lisans için [buradan](https://purchase.aspose.com/temporary-license/) başvurabilirsiniz.

**Q: Hangi tür görüntüleri dönüştürebilirim?**  
A: Aspose.PSD öncelikle PSD dosyalarıyla çalışır, ancak PNG, JPEG ve TIFF gibi çeşitli formatlara dönüştürmeyi destekler.

## Conclusion
Artık Aspose.PSD for Java kullanarak PNG bit derinliğini kontrol ederken **psd'yi png'ye dönüştürmeyi** öğrendiniz. `PngOptions`'ı ayarlayarak **png kalitesini ayarlayabilir**, **gri tonlamalı png** oluşturabilir ve herhangi bir senaryo için dosya boyutunu ince ayar yapabilirsiniz. Farklı renk tipleri ve bit derinlikleriyle deney yaparak uygulamanız için mükemmel dengeyi bulun.

---

**Son Güncelleme:** 2026-03-18  
**Test Edilen:** Aspose.PSD for Java 24.11 (yazım sırasında en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}