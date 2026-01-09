---
date: 2026-01-09
description: Aspose.PSD for Java'da Bradley Eşikleme kullanarak PSD'yi PNG'ye nasıl
  dönüştüreceğinizi öğrenin. Bu kılavuz, optimal eşiği nasıl seçeceğinizi ve PSD görüntüsünü
  verimli bir şekilde ikili hâle getireceğinizi gösterir.
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: Bradley Eşikleme ile PSD'yi PNG'ye Dönüştür (Aspose.PSD Java)
url: /tr/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bradley Eşiğe Çevirme ile PSD'yi PNG'ye Dönüştürme (Aspose.PSD Java)

Aspose.PSD for Java'da Bradley Eşiğe Çevirme kullanarak **PSD'yi PNG'ye dönüştür** hakkında bu kapsamlı rehbere hoş geldiniz. Önümüzdeki birkaç dakikada, bu tekniğin Photoshop belgelerinden yüksek kontrastlı, ikili PNG dosyaları oluşturmak için neden mükemmel olduğunu göreceksiniz ve adım adım bir uygulamalı rehber alacaksınız.

## Hızlı Yanıtlar
- **Aspose.PSD ile PSD'yi PNG'ye dönüştürebilir miyim?** Evet – PSD'yi yükleyin, `binarizeBradley` uygulayın ve ardından PNG olarak kaydedin.  
- **“choose optimal threshold” ne anlama geliyor?** Bu, koyu/aydınlık piksellerin nasıl sınıflandırılacağını belirleyen (0‑1) duyarlılık değeridir.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü değerlendirme için çalışır.  
- **Kaydetme için hangi görüntü formatları destekleniyor?** PNG, JPEG, BMP ve `ImageOptions` sınıfları aracılığıyla birçok diğer format.  
- **Kod Java 8 ve sonrası ile uyumlu mu?** Kesinlikle – Aspose.PSD Java API Java 8+ destekler.

## Bradley Eşiğe Çevirme Nedir?
Bradley Eşiğe Çevirme, her piksel için yerel ortalama hesaplayan ve pikselin yoğunluğunu bu ortalamanın kullanıcı tarafından tanımlanan eşik değeriyle çarpımına karşılaştıran uyarlamalı bir ikileştirme algoritmasıdır. Sonuç, önemli detayları koruyan temiz bir siyah‑beyaz görüntüdür.

## Bradley Eşiğe Çevirme ile PSD'yi PNG'ye Neden Dönüştürmeliyiz?
- **Keskin kenarları koruyun** – OCR, barkod algılama veya ön plan ile arka plan arasında net bir ayrım gerektiren herhangi bir iş akışı için idealdir.  
- **Dosya boyutunu küçültün** – PNG kayıpsızdır ancak ikileştirmeden sonra genellikle daha küçüktür.  
- **Çapraz platform uyumluluğu** – PNG her yerde çalışır, PSD ise sadece Photoshop'a özgüdür.

## Önkoşullar
İlerlemeye başlamadan önce şunların olduğundan emin olun:

1. **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü.  
2. **Aspose.PSD Kütüphanesi** – En son JAR dosyasını [buradan](https://releases.aspose.com/psd/java/) indirin.  
3. **Örnek PSD Görüntüsü** – Dönüştürmek istediğiniz herhangi bir PSD dosyası; ayrıca Aspose örneklerinde sağlanan örneği de kullanabilirsiniz.

## Paketleri İçe Aktarın
Gerekli sınıfları Java projenize içe aktararak başlayın:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Bradley Eşiğe Çevirme Kullanarak PSD'yi PNG'ye Nasıl Dönüştürülür
Aşağıda, net ve numaralı adımlara bölünmüş tam iş akışı yer almaktadır. Her adım kısa bir açıklama ve kopyalayıp yapıştırmanız gereken tam kodu içerir.

### Adım 1: PSD Görüntüsünü Yükleyin
İlk olarak, kaynak dosyanıza işaret edin ve Aspose.PSD ile yükleyin.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### Adım 2: Optimum Eşiği Seçin
Eşik değeri (aralık 0 – 1) ikileştirmenin ne kadar agresif olacağını kontrol eder. Tipik bir başlangıç noktası **0.15**'tir, ancak görüntünüze göre ayarlayabilirsiniz.

```java
// Define threshold value
double threshold = 0.15;
```

### Adım 3: PSD Görüntüsünü İkileştir
Şimdi Bradley algoritmasını uygulayın. Bu adım, seçtiğiniz eşiğe göre **PSD görüntüsünü ikileştir**.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### Adım 4: Çıktıyı PNG Olarak Kaydedin
Son olarak, işlenmiş görüntüyü PNG formatında diske yazın.

```java
// Save the output image
image.save(destName, new PngOptions());
```

İşlemeniz gereken herhangi bir sayıda PSD dosyası için bu adımları tekrarlayın, en iyi görsel sonucu elde etmek için eşiği gerektiği gibi ayarlayın.

## Yaygın Sorunlar ve İpuçları
- **Eşik çok düşük/çok yüksek:** Çıktı çok gürültülü ya da soluk görünüyorsa, `threshold` değerini adım adım ayarlayın (ör. 0.10 – 0.20).  
- **Bellek tüketimi:** Büyük PSD dosyaları bellek yoğun olabilir. Bunları tek tek işlemek veya JVM yığın boyutunu (`-Xmx`) artırmayı düşünün.  
- **Kaydetmeden önce ön izleme:** Son PNG dışa aktarımından önce ikileştirilmiş sonucu incelemek için `image.save("preview.bmp", new BmpOptions());` kullanın.

## Sıkça Sorulan Sorular

**S: `binarizeBradley` ile diğer eşikleme yöntemleri arasındaki fark nedir?**  
C: `binarizeBradley`, her piksel için yerel ortalama hesaplar, bu da global eşiklemeye kıyasla düzensiz aydınlatmalı görüntülerde daha dayanıklı olmasını sağlar.

**S: Bradley Eşiğe Çevirme'yi JPEG veya BMP dosyalarına uygulayabilir miyim?**  
C: Evet. `Image.load(...)` ile desteklenen herhangi bir formatı yükleyin, ardından kaydetmeden önce `binarizeBradley` çağırın.

**S: Kaydetmeden önce ikileştirilmiş görüntüyü ön izlemek için bir yol var mı?**  
C: Kesinlikle. Aspose.PSD'nin herhangi bir görüntü kaydetme seçeneğini (ör. BMP) kullanarak geçici bir ön izleme dosyası yazabilirsiniz.

**S: Daha fazla destek ve kaynak nerede bulunabilir?**  
C: Topluluk yardımı için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin ve gelişmiş senaryolar için tam [belgelendirmeyi](https://reference.aspose.com/psd/java/) keşfedin.

## Sonuç
Artık **PSD'yi PNG'ye dönüştürmeyi**, **optimum bir eşik seçerek** ve Bradley Eşiğe Çevirme ile **PSD görüntüsünü ikileştirerek** verimli bir şekilde öğrendiniz. Bu yaklaşım, karmaşık Photoshop dosyalarından temiz, yüksek kontrastlı PNG çıktıları gerektiren iş akışları için mükemmeldir.

---

**Son Güncelleme:** 2026-01-09  
**Test Edilen Versiyon:** Aspose.PSD Java 23.12 (yazım zamanındaki en son)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}