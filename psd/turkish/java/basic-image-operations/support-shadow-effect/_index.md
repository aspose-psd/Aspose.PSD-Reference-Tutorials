---
date: 2025-12-30
description: Aspose.PSD for Java kullanarak gölge rengini nasıl değiştireceğinizi
  ve gölge efektlerini nasıl özelleştireceğinizi öğrenin. Bu adım adım gölge efekti
  öğreticisini izleyin.
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Gölge Rengini Nasıl Değiştirilir
url: /tr/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Gölge Rengini Değiştirme Aspose.PSD for Java ile

## Giriş

Grafiklerinize derinlik katmak, genellikle tasarımın atmosferine uygun **gölge rengini değiştirmeyi** gerektirir. Aspose.PSD for Java ile drop shadow efektlerini kolayca ekleyebilir veya değiştirebilir, opaklığı kontrol edebilir ve diğer parametreleri ince ayar yapabilirsiniz—hepsi Java kodundan. Bu **gölge efekti öğreticisi**'nde bir PSD dosyasını yüklemeyi, mevcut gölgeyi okumayı, rengini, opaklığını, mesafesini özelleştirmeyi ve sonunda güncellenmiş dosyayı kaydetmeyi adım adım göstereceğiz.

## Hızlı Yanıtlar
- **“gölge rengini değiştirme” ne anlama geliyor?** Bir PSD katmanına uygulanan DropShadowEffect'in renk özelliğini günceller.  
- **Hangi kütüphane bunu destekliyor?** Aspose.PSD for Java gölge efektleri için tam destek sağlar.  
- **Lisans gerekli mi?** Geliştirme için deneme sürümü çalışır; üretim için ticari lisans gerekir.  
- **Gölge opaklığını ayarlayabilir miyim?** Evet – şeffaflığı (0‑255) tanımlamak için `setOpacity(byte)` kullanın.  
- **Kod Java 8+ ile uyumlu mu?** Kesinlikle, API Java 8 ve sonrası için hedeflenmiştir.

## PSD dosyalarında “gölge rengini değiştirme” nedir?

Gölge rengini değiştirmek, bir katmanın arkasında görünen drop shadow'ın görsel tonunu değiştirir. Bu, gerçekçi aydınlatma oluşturmak, marka renkleriyle eşleştirmek veya sadece sanatsal bir dokunuş eklemek için faydalıdır.

## Gölge efektlerini özelleştirmek için neden Aspose.PSD for Java kullanılmalı?

- **Tam PSD bütünlüğü** – gölgeler dahil tüm katman efektleri korunur.  
- **Photoshop gerekmez** – dosyaları herhangi bir sunucuda programlı olarak işleyin.  
- **İnce ayar kontrolü** – renk, opaklık, mesafe, açı, yayılım ve gürültüyü ayarlayın.  
- **Çapraz platform** – Windows, Linux ve macOS JVM'lerinde çalışır.

## Önkoşullar

- Java programlamaya temel bilgi.  
- Aspose.PSD for Java yüklü. İndirmek için [buraya](https://releases.aspose.com/psd/java/) tıklayın.  

## Paketleri İçe Aktarma

Başlamadan önce, görüntüler ve gölge efektleriyle çalışabilmek için gerekli sınıfları içe aktarın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Adım Adım Kılavuz

### Adım 1: PSD Görüntüsünü Yükleyin

Kaynak PSD'yi, efekt kaynaklarını yükleme özelliğini etkinleştirerek yükleyin:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Adım 2: Mevcut Drop Shadow Efektini Alın

İstenen katmanda (bu örnekte ikinci katman) gölge efektini bulun:

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Adım 3: Varsayılan Ayarları Doğrulayın (İsteğe Bağlı)

Bu doğrulamaları çalıştırmak, değiştirmeden önce orijinal değerleri anlamanıza yardımcı olur:

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

### Adım 4: **Gölge Rengini Değiştirin** ve Diğer Özellikleri Özelleştirin

Şimdi **gölge rengini** yeşile değiştiriyoruz, opaklığı, mesafeyi, boyutu ve diğer nitelikleri ayarlıyoruz. Bu, Aspose.PSD'nin **gölge efektini özelleştirme** yeteneklerini gösterir:

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### Adım 5: Değiştirilmiş Görüntüyü Kaydedin

Son olarak, güncellenmiş PSD'yi diske yazın:

```java
im.save(psdPathAfterChange);
```

## Yaygın Sorunlar ve İpuçları

- **Etkileri alırken NullPointerException** – `setLoadEffectsResource(true)` çağrıldığından emin olun; aksi takdirde efektler yüklenmez.  
- **Renk değişmiyor** – doğru katman indeksini (`im.getLayers()[1]` bu örnekte) düzenlediğinizden emin olun.  
- **Opaklık değişmemiş gibi görünüyor** – opaklığın bir byte (0‑255) olduğunu unutmayın. `(byte)` dönüşümü gereklidir.  

## Sonuç

Bu adımları izleyerek **gölge rengini değiştirebilir**, **gölge opaklığını ayarlayabilir** ve Aspose.PSD for Java kullanarak herhangi bir PSD dosyasında **gölge efekti** parametrelerini tamamen **özelleştirebilirsiniz**. Bu, manuel Photoshop işlemleri olmadan programlı olarak daha zengin grafikler oluşturmanızı sağlar.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java profesyonel grafik tasarım projeleri için uygun mu?**  
C: Kesinlikle! Aspose.PSD for Java, profesyonel grafik tasarım görevleri için tasarlanmış güçlü bir kütüphanedir.

**S: Aspose.PSD for Java'yi ticari uygulamalarda kullanabilir miyim?**  
C: Evet, Aspose.PSD for Java ticari bir üründür. Satın almak için [buraya](https://purchase.aspose.com/buy) tıklayabilirsiniz.

**S: Ücretsiz deneme sürümü mevcut mu?**  
C: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

**S: Ayrıntılı belgeleri nereden bulabilirim?**  
C: Kapsamlı belgeler için [buraya](https://reference.aspose.com/psd/java/) bakın.

**S: Aspose.PSD for Java için destek nasıl alabilirim?**  
C: Herhangi bir destek sorusu için topluluk forumuna [buradan](https://forum.aspose.com/c/psd/34) katılabilirsiniz.

---

**Last Updated:** 2025-12-30  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}