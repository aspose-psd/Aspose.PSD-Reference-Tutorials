---
date: 2025-12-30
description: Aspose.PSD kullanarak iki resmi birleştirerek Java’da PSD dosyası oluşturmayı
  öğrenin. Görüntüleri hızlıca bir PSD dosyasına birleştirmek için adım adım rehberimizi
  izleyin.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Java ile PSD dosyası oluşturma – Aspose.PSD ile Görüntüleri Birleştirme
url: /tr/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java’da PSD Dosyası Oluştur – Aspose.PSD ile Görüntüleri Birleştir

## Giriş

Eğer birkaç resmi birleştirerek **Java’da bir PSD dosyası oluşturmanız** gerekiyorsa, Aspose.PSD işi kolaylaştırır. Bu öğreticide iki resmi tek bir PSD tuvaline birleştirmeyi adım adım gösterecek, bu yaklaşımın neden faydalı olduğunu açıklayacak ve çalıştırmaya hazır kod sağlayacağız. Sonunda **Java tarzında iki resmi birleştirebilecek** ve profesyonel görünümlü katmanlı bir dosya oluşturabileceksiniz.

## Hızlı Yanıtlar
- **PSD’ye görüntü birleştirmek için en iyi kütüphane nedir?** Aspose.PSD for Java.
- **Uygulama ne kadar sürer?** Temel bir birleştirme için yaklaşık 10‑15 dakika.
- **Lisans gerekli mi?** Test için ücretsiz deneme çalışır; üretim için ticari bir lisans gereklidir.
- **İki'den fazla resim ekleyebilir miyim?** Evet – her ek katman için `drawImage` çağrılarını tekrarlayın.
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.

## Ön Koşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.PSD Library** – [buradan](https://releases.aspose.com/psd/java/) indirin.  
2. **Java Development Kit (JDK)** – Java 8+ önerilir.  
3. **Document Directory** – kaynak resimlerin ve oluşturulacak PSD’nin saklanacağı makinenizdeki bir klasör.

## Paketleri İçe Aktarma

Gerekli Aspose.PSD sınıflarını projenize içe aktararak başlayın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Adım Adım Kılavuz

### Adım 1: PSD Seçeneklerini Oluştur (dosyayı hazırlama)

İlk olarak çıkış ayarlarını tutacak bir `PsdOptions` örneği oluştururuz.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Adım 2: FileCreateSource Ayarla (PSD’nin nereye kaydedileceğini tanımla)

İstenilen sonuç dosyasına işaret eden bir `FileCreateSource` nesnesini seçeneklere atayın.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Adım 3: Image Örneği Oluştur (tuval boyutunu başlat)

Seçeneklerle bir `Image` nesnesi oluşturun ve 600 × 600 piksel bir tuval belirtin.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Adım 4: Graphics’i Başlat ve İlk Resmi Çiz

Bir `Graphics` nesnesi tuval üzerine çizmemizi sağlar. Arka planı beyaza temizliyoruz ve ilk kaynak resmi sol yarıya çiziyoruz.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Adım 5: İkinci Resmi Çiz (birleştirmeyi tamamla)

Şimdi aynı tuvalin sağ yarısına ikinci resmi yerleştiriyoruz.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Adım 6: Oluşan PSD Dosyasını Kaydet

Son olarak, birleştirilmiş tuvali diske kaydedin.

```java
image.save();
```

Tebrikler! Başarıyla **görüntüleri PSD’ye birleştirdiniz** ve Java’da bir PSD dosyası oluşturdunuz.

## Neden Aspose.PSD ile görüntüleri birleştirirsiniz?

- **Katman‑bilinçli** – her `drawImage` çağrısı daha sonra düzenleyebileceğiniz ayrı bir katman ekler.  
- **Format esnekliği** – PSD, PNG, JPEG, BMP ve daha fazlasını destekler.  
- **Yerel bağımlılık yok** – saf Java, JDK’yı çalıştıran herhangi bir işletim sisteminde çalışır.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| `File not found` hatası kaynak resimler yüklenirken | Yanlış `dataDir` yolu | `dataDir`'in `example1.psd` ve `example2.psd` içeren klasöre işaret ettiğini doğrulayın. |
| Çıktı PSD boş | `graphics.clear` çizimden sonra çağrıldı | `graphics.clear(Color.getWhite())`'ın herhangi bir `drawImage` çağrısından **önce** çalıştırıldığından emin olun. |
| Çalışma zamanında lisans istisnası | Eksik veya süresi dolmuş Aspose.PSD lisansı | Herhangi bir API çağrısından önce `License license = new License(); license.setLicense("Aspose.PSD.lic");` kodunu kullanarak geçerli bir lisans uygulayın. |

## Sıkça Sorulan Sorular

### S1: Aspose.PSD tüm görüntü formatlarıyla uyumlu mu?
**C1:** Aspose.PSD öncelikle PSD dosya formatına odaklanır. Ancak, giriş ve çıkış için çeşitli diğer formatları da destekler.

### S2: Birleştirilen görüntü üzerinde ek değişiklikler yapabilir miyim?
**C2:** Kesinlikle! Görüntüleri birleştirdikten sonra, Aspose.PSD'nin kapsamlı özelliklerini kullanarak oluşan PSD'yi daha da manipüle edebilirsiniz.

### S3: Aspose.PSD kullanımı için lisans gereksinimleri var mı?
**C3:** Evet, ticari kullanım için geçerli bir lisans gereklidir. Lisansı [buradan](https://purchase.aspose.com/buy) edinin.

### S4: Aspose.PSD için ücretsiz deneme mevcut mu?
**C4:** Evet, Aspose.PSD'yi ücretsiz deneme ile [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

### S5: Aspose.PSD ile ilgili sorular için nereden destek bulabilirim?
**C5:** Topluluk desteği ve tartışmalar için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

---

**Son Güncelleme:** 2025-12-30  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}