---
date: 2025-12-05
description: Java'da Aspose PSD yazı tipi değişimini nasıl yapacağınızı öğrenin. Bu
  adım adım Java görüntü işleme öğreticisi, PSD dosyalarındaki yazı tiplerini verimli
  bir şekilde nasıl değiştireceğinizi gösterir.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Aspose PSD Yazı Tipi Değiştirme Java’da – PSD Dosyalarındaki Yazı Tiplerini
  Değiştir
url: /tr/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Aspose PSD Yazı Tipi Değiştirme

## Giriş

Photoshop (PSD) dosyası içinde eksik veya istenmeyen yazı tiplerini değiştirmeniz gerekiyorsa, **Aspose PSD font replacement** bunu zahmetsiz hâle getirir. Java uygulamalarında bir PSD yükleyebilir, Aspose'a hangi yedek yazı tipinin kullanılacağını söyleyebilir ve ardından sonucu istediğiniz herhangi bir formatta kaydedebilirsiniz. Bu öğretici, projenizi kurmaktan güncellenmiş görüntüyü dışa aktarmaya kadar tam **aspose psd font replacement** iş akışını adım adım gösterir.

## Hızlı Yanıtlar
- **Yazı tipi değiştirmeyi hangi kütüphane yönetir?** Aspose.PSD for Java  
- **Uygulamanın ne kadar sürer?** Temel bir senaryo için yaklaşık 5‑10 dakika  
- **Varsayılan yedek yazı tipi olarak hangi font kullanılır?** İstediğiniz herhangi bir TrueType fontunu ayarlayabilirsiniz, ör. “Arial”  
- **PNG dışındaki formatlara kaydedebilir miyim?** Evet – PSD, JPEG, BMP vb. desteklenir  
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için geçerli bir Aspose.PSD lisansı gereklidir  

## Aspose PSD Yazı Tipi Değiştirme Nedir?

Aspose PSD yazı tipi değiştirme, kütüphanenin bir PSD dosyasında eksik veya desteklenmeyen bir yazı tipiyle karşılaştığında kullanacağı yedek bir yazı tipini belirleme sürecidir. Bu, metin katmanlarının Photoshop'ta manuel düzenleme yapmadan doğru şekilde render edilmesini sağlar.

## Neden Aspose.PSD for Java Kullanmalı?

- **Tam özellikli PSD işleme** – katmanlar, maskeler, efektler ve metin API aracılığıyla erişilebilir.  
- **Çapraz platform** – Java destekleyen herhangi bir işletim sisteminde çalışır.  
- **Harici bağımlılık yok** – kütüphane yazı tipi ikamesini dahili olarak yönetir, bu sayede uygulamanıza ekstra font eklemenize gerek kalmaz.  

## Önkoşullar

Başlamadan önce şunların yüklü olduğundan emin olun:

- **Java Development Kit (JDK)** – sürüm 8 veya üzeri yüklü.  
- **Aspose.PSD for Java** – en son JAR dosyasını [sürüm sayfasından](https://releases.aspose.com/psd/java/) indirin.  
- **Bir IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  

## Paketleri İçe Aktarın

İhtiyacınız olan sınıfları içe aktararak başlayın. Bu, görüntü yükleme, yük‑seçenekleri ve kaydetme işlevlerine erişmenizi sağlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: Belge Dizinini Ayarlayın

Kaynak PSD dosyasını içeren klasörü tanımlayın. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Görüntüyü Yedek Yazı Tipiyle Yükleyin

Bir `PsdLoadOptions` örneği oluşturun, varsayılan yedek yazı tipini (ör. **Arial**) belirtin ve PSD'yi yükleyin. Aspose, eksik bir fontla karşılaştığında otomatik olarak yedek fontu uygular.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Adım 3: Değiştirilen Görüntüyü Kaydedin

Yazı tipi ikamesinden sonra görüntüyü istediğiniz desteklenen formatta dışa aktarabilirsiniz. Burada PNG olarak kaydediyoruz, ancak JPEG, BMP ya da PSD olarak da kaydedebilirsiniz.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| Değiştirme sonrası metin bozuk görünüyor | Yedek yazı tipi gerekli glifleri içermiyor | Gerekli Unicode aralığını destekleyen bir yazı tipi seçin (ör. “Arial Unicode MS”). |
| `OutOfMemoryError` büyük PSD'lerde | Yeterli heap olmadan çok yüksek çözünürlüklü bir dosya yüklemek | JVM heap boyutunu (`-Xmx2g`) artırın veya mümkünse görüntüyü akış modunda yükleyin. |
| Lisans istisnası | Deneme sürümünü üretimde kullanmak | Görüntüyü yüklemeden önce geçerli kalıcı veya geçici bir lisans uygulayın. |

## Sık Sorulan Sorular

**S: PSD dışındaki diğer görüntü formatlarında yazı tiplerini değiştirebilir miyim?**  
C: Evet. Birincil kullanım senaryosu PSD olsa da, Aspose.PSD PNG, JPEG, BMP ve TIFF formatlarını da destekler; metin katmanlarının bulunduğu yerlerde yazı tipi değiştirme yapılabilir.

**S: Varsayılan yedek yazı tipi zorunlu mu?**  
C: Hayır. İstediğiniz herhangi bir TrueType fontunu ayarlayabilir veya ayarı atlayarak Aspose'un dahili varsayılanını kullanmasına izin verebilirsiniz.

**S: Aspose.PSD kullanmak için lisans gereksinimleri var mı?**  
C: Üretim ortamlarında ticari bir lisans gereklidir. Ayrıntılar için [satın alma sayfasını](https://purchase.aspose.com/buy) inceleyin.

**S: Test amaçlı geçici bir lisans alabilir miyim?**  
C: Kesinlikle. Aspose, değerlendirme için ücretsiz geçici lisanslar sunar – [geçici lisans sayfasını](https://purchase.aspose.com/temporary-license/) ziyaret edin.

**S: Aspose.PSD ile ilgili ek destek nereden bulunur veya konular tartışılır?**  
C: Topluluk forumu sorularınızı sormak için harika bir yerdir: [Aspose.PSD forumu](https://forum.aspose.com/c/psd/34).

**S: Birden fazla eksik font içeren PSD dosyalarını nasıl yönetirim?**  
C: Varsayılan yedek yazı tipini bir kez ayarlayın (yukarıda gösterildiği gibi) – bu, yükleme sırasında *tüm* eksik fontlara uygulanır.

**S: Görüntü kaydedildikten sonra yazı tiplerini değiştirmek mümkün mü?**  
C: Yazı tipi ikamesi yalnızca yükleme aşamasında gerçekleşir. Yazı tiplerini daha sonra değiştirmek için PSD'yi farklı bir yedek fontla yeniden yükleyip tekrar kaydedin.

## Sonuç

Artık Java'da **aspose psd font replacement** iş akışını baştan sona gördünüz – doğru sınıfları içe aktarmaktan, yedek bir font yapılandırmaya, PSD'yi yüklemeye ve düzeltilmiş görüntüyü dışa aktarmaya kadar. Bu deseni görüntü işleme hatlarınızda kullanarak tüm PSD varlıklarınızda tutarlı tipografi sağlayabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-05  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

---