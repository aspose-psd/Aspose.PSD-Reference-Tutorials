---
date: 2025-12-04
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak kaydetmeyi ve bir render
  gölgesi eklemeyi öğrenin. Bu kılavuz, gölge eklemeyi, PSD'yi PNG'ye dönüştürmeyi
  ve Java'da drop shadow uygulamayı kapsar.
language: tr
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: PSD'yi PNG Olarak Kaydet ve Aspose.PSD Java ile Gölge Ekle
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG Olarak Kaydet ve Aspose.PSD Java ile Gölge Ekle

## Giriş

Java'da Photoshop dosyalarıyla çalışıyorsanız, **PSD'yi PNG olarak kaydet** ve profesyonel görünümlü bir gölge eklemek yaygın bir gereksinimdir. Aspose.PSD bu görevi birkaç satır kodla **PSD'yi PNG'ye dönüştürmenize** ve **Java'da gölge eklemenize** olanak tanır. Bu öğreticide, bir PSD dosyasını yüklemekten gölgelendirilmiş son PNG'yi dışa aktarmaya kadar tüm süreci adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **“PSD'yi PNG olarak kaydet” ne anlama geliyor?** Katmanlı bir Photoshop dosyasını, şeffaflığı koruyan düz bir PNG görüntüsüne dönüştürür.  
- **Dönüştürürken gölge ekleyebilir miyim?** Evet—Aspose.PSD, dışa aktarmadan önce katman efektlerini değiştirmenize izin verir.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü yeterlidir; üretim ortamında lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.  
- **Gölge efekti özelleştirilebilir mi?** Kesinlikle—renk, opaklık, mesafe, boyut, açı ve daha fazlasını ayarlayabilirsiniz.

## Önkoşullar

Başlamadan önce şunların yüklü olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm.  
- **Aspose.PSD Kütüphanesi** – En son JAR dosyasını resmi siteden [burada](https://releases.aspose.com/psd/java/) indirin.  
- **Bir PSD dosyası** – Üzerine gölge eklemek istediğiniz en az bir katman içeren bir dosya.  

## Java'da PSD'yi PNG Olarak Kaydet ve Gölge Ekleme

Aşağıda adım adım bir kılavuz bulunmaktadır. Her adım kısa bir açıklama ve kopyalamanız gereken tam kodu içerir.

### Adım 1: Gerekli Paketleri İçe Aktarın

Gerekli sınıfları, görüntü yükleme, efekt işleme ve PNG dışa aktarma yeteneklerini sağlamak için içe aktararak başlıyoruz.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Adım 2: Belge Dizini Tanımlayın

Kaynak PSD ve oluşturulacak PNG'nin bulunacağı klasörü ayarlayın.

```java
String dataDir = "Your Document Directory";
```

### Adım 3: PSD ve PNG Dosya Yollarını Belirleyin

Giriş PSD ve çıkış PNG için tam yolları belirtin.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Adım 4: Efektler Etkinleştirilmiş PSD Dosyasını Yükleyin

**loadEffectsResource** özelliğini etkinleştirmek, gölgeler gibi katman efektlerinin manipülasyona açık olmasını sağlar.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Adım 5: Gölge Efektine Erişin

Burada ikinci katmana (indeks 1) uygulanan ilk efekti alıyoruz. Gölge parametrelerini okuyup değiştireceğimiz yer burasıdır.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Adım 6: Gölge Efekti Özelliklerini Doğrulayın (İsteğe Bağlı ama Faydalı)

Mevcut özellikleri kontrol etmek, bir şey değiştirmeniz gerekip gerekmediğine karar vermenize yardımcı olur. Aşağıdaki doğrulamalar varsayılan değerleri onaylar.

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

> **İpucu:** Özel ayarlarla **gölge eklemek** istiyorsanız, kaydetmeden önce `shadowEffect` üzerindeki özellikleri değiştirin (ör. `shadowEffect.setColor(Color.getRed());`).

### Adım 7: Değiştirilmiş Görüntüyü PNG Olarak Kaydedin

Son olarak, PSD'yi (gölge render edilmiş olarak) bir PNG dosyasına dışa aktarıyoruz. `TruecolorWithAlpha` seçeneği şeffaflığı korur.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Ve işte—tek bir geçişte **PSD'yi PNG'ye dönüştürme** ve **Java'da gölge uygulama** iş akışı tamamlandı.

## Bu görev için neden Aspose.PSD kullanmalı?

- **Yerel Photoshop gerekmez** – Java destekleyen herhangi bir platformda çalışır.  
- **Tam PSD bütünlüğü** – Tüm katman bilgileri, maskeler ve efektler korunur.  
- **İnce ayar kontrolü** – Dışa aktarmadan önce gölgenin her parametresini ayarlayabilirsiniz.  
- **Yüksek performans** – Büyük dosyalar ve toplu işleme için optimize edilmiştir.

## Yaygın Sorunlar ve Çözümleme

| Belirti | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| `NullPointerException` on `shadowEffect` | Hedef katmanda efekt yok veya indeks hatalı. | Katman indeksini (`im.getLayers()[i]`) doğrulayın ve bir efektin mevcut olduğundan emin olun. |
| Dışa aktarılan PNG boş | PNG seçenekleri doğru ayarlanmamış veya görüntü kaydedilmemiş. | `PngColorType.TruecolorWithAlpha` kullanın ve `im.save()` yolunun yazılabilir olduğundan emin olun. |
| Gölge rengi görünmüyor | Gölge opaklığı 0 olarak ayarlanmış veya renk arka planla aynı. | `shadowEffect.setOpacity(255);` yapın ve kontrast bir renk seçin. |

## Sık Sorulan Sorular

**S: Birden fazla katmana aynı anda gölge uygulayabilir miyim?**  
C: Evet. `im.getLayers()` üzerinden döngü kurarak her katmanın `DropShadowEffect`'ini ihtiyacınıza göre değiştirebilirsiniz.

**S: ‘Spread’ parametresi ne işe yarar?**  
C: Gölgenin tamamen opaktan şeffafa geçişinin ne kadar keskin olduğunu kontrol eder. Yüksek spread, daha sert bir kenar oluşturur.

**S: Aspose.PSD tüm Photoshop sürümleriyle uyumlu mu?**  
C: Erken sürümlerden en yeni Photoshop CC dosyalarına kadar geniş bir PSD versiyon yelpazesini destekler.

**S: Sorun yaşarsam nasıl yardım alabilirim?**  
C: Topluluk desteği ve resmi yardım için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

**S: Aspose.PSD'yi satın almadan denemek mümkün mü?**  
C: Kesinlikle. Ücretsiz deneme sürümünü [Aspose web sitesinden](https://releases.aspose.com/) indirebilirsiniz.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Son Güncelleme:** 2025-12-04  
**Test Edilen:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose  

---