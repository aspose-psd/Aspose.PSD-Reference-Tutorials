---
date: 2025-12-10
description: Aspose.PSD for Java kullanarak PSD katmanlarını nasıl çıkaracağınızı
  ve PSD katmanlarını PNG'ye nasıl dönüştüreceğinizi öğrenin. Güçlü grafik manipülasyonu
  gerektiren geliştiriciler için idealdir.
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Aspose.PSD Java kullanarak PSD Katmanlarını Çıkarın ve PSD Dosyaları için Katman
  Desteği Ekleyin
url: /tr/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java Kullanarak PSD Katmanlarını Çıkarın ve PSD Dosyaları için Katman Desteği Ekleyin

## Introduction
Photoshop Document (PSD) dosyalarıyla çalışmak, grafik tasarımcılar ve geliştiriciler için günlük bir gerçektir. En yaygın görevlerden biri **PSD katmanlarını çıkarmaktır**, böylece bu katmanlar düzenlenebilir, yeniden kullanılabilir veya PNG gibi diğer formatlara dönüştürülebilir. Java uygulamalarında Aspose.PSD bu süreci basit ve kod‑dostu hâle getirir. Bu öğreticide, PSD katmanlarını çıkarmak, katman desteğini etkinleştirmek ve **PSD katmanlarını PNG’ye dönüştürmek** için gereken adımları net açıklamalar ve pratik ipuçlarıyla adım adım göstereceğiz.

## Quick Answers
- **“extract PSD layers” ne anlama geliyor?** Bir PSD dosyasını yükleyip her bir katmana erişerek onları manipüle etmek veya dışa aktarmak anlamına gelir.  
- **Java’da bunu hangi kütüphane sağlıyor?** Aspose.PSD for Java, Photoshop’a ihtiyaç duymadan tam özellikli PSD işleme sunar.  
- **PSD katmanlarını tek seferde PNG’ye dönüştürebilir miyim?** Evet—dosyayı uygun seçeneklerle yükleyip şeffaflığı koruyan PNG seçenekleriyle kaydederek.  
- **Üretim kullanımı için lisansa ihtiyacım var mı?** Üretim için ticari bir lisans gereklidir; değerlendirme amacıyla ücretsiz bir deneme sürümü mevcuttur.  
- **Hangi Java sürümü gerekiyor?** JDK 8 veya üzeri (öğreticide örnek olarak JDK 11 kullanılmıştır).

## What is “extract PSD layers”?
PSD katmanlarını çıkarmak, bir PSD dosyasının iç yapısını okuyup her katmanı bağımsız bir görüntü nesnesi olarak elde etmeyi ifade eder. Bu sayede katmanları programatik olarak düzenleyebilir, gizleyebilir, yeniden sıralayabilir veya tek tek dışa aktarabilirsiniz—tıpkı tasarımcıların Photoshop’ta yaptığı gibi.

## Why extract PSD layers and convert them to PNG?
- **Varlıkları yeniden kullanma:** Manuel dışa aktarma yapmadan bir master PSD’den ikon, buton veya UI öğelerini çekin.  
- **Otomasyon:** Anlık olarak küçük resimler veya web‑hazır görüntüler üretin.  
- **Şeffaflığı koruma:** PNG, alfa kanallarını tutar ve web grafikleri için mükemmeldir.  

## Prerequisites
Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Environment** – JDK yüklü. [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.  
2. **Aspose.PSD for Java** – En son kütüphaneyi resmi indirme sayfasından [burada](https://releases.aspose.com/psd/java/) alın.  
3. **Temel Java bilgisi** – Java programlarını derleme ve çalıştırma konusunda deneyim.  
4. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
5. **Bir PSD dosyası** – Kendi PSD’nizi kullanın veya test için bir örnek PSD indirin.

Bu gereksinimler hazır olduğunda PSD katmanlarını çıkarmaya başlayabilirsiniz.

## Import Packages
Aspose.PSD kütüphanesinden ihtiyacımız olan sınıfları içe aktarın.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Define Your Directories
Kaynak PSD ve çıktı PNG için yolları ayarlayın. `dataDir` değişkenini dosyalarınızın bulunduğu klasöre göre güncelleyin.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"` ifadesini gerçek klasör yolunuzla değiştirin.  
- `sourceFileName` – İşlemek istediğiniz PSD’nin tam yolu.  
- `output` – Çıkarılan katmanları içerecek PNG’nin hedef yolu.

## Step 2: Set Up the Load Options
`PsdLoadOptions` yapılandırması, tüm katman efektleri ve kaynaklarının doğru şekilde yüklenmesini sağlar; bu, **extract PSD layers** işlemi için kritiktir.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – Katmanlara eklenmiş ek efektleri (gölge gibi) yükler.  
- `setUseDiskForLoadEffectsResource(true)` – Ağır kaynakları diske yönlendirerek bellek yükünü azaltır.

## Step 3: Load the PSD File
Tanımladığınız seçenekleri kullanarak PSD’yi bir `PsdImage` nesnesine yükleyin.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

Bu noktada `image` tüm katmanları, maskeleri ve efektleri içerir ve çıkarılmaya hazırdır.

## Step 4: Set Up the Save Options
PNG’nin nasıl kaydedileceğini yapılandırın. `TruecolorWithAlpha` seçeneği, orijinal katmanlardaki şeffaflığı korur.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 5: Save the Image (Convert PSD Layers to PNG)
Yüklenen PSD’yi (tüm katmanlarıyla) tek bir PNG dosyasına dışa aktarın. Bu adım **convert psd layers png** işlemini tek seferde gerçekleştirir.

```java
image.save(output, saveOptions);
```

Her katmanı ayrı bir PNG olarak kaydetmek isterseniz `image.getLayers()` üzerinde döngü kurabilirsiniz—ancak çoğu senaryoda birleştirilmiş PNG yeterli olur.

## Step 6: Wrap It Up
İşlemin başarılı olduğunu gösteren dostça bir konsol mesajı ekleyin.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Common Issues & Tips
- **Out‑of‑Memory Errors:** Çok büyük PSD’ler işliyorsanız `setUseDiskForLoadEffectsResource(true)` seçeneğini açık tutarak geçici verileri diske yönlendirin.  
- **Missing Effects:** `setLoadEffectsResource(true)` ayarının yapıldığından emin olun; aksi takdirde bazı katman efektleri göz ardı edilebilir.  
- **Path Problems:** Platform bağımsız yol yönetimi için `java.nio.file` paketinden `Paths.get(...)` kullanın.

## Frequently Asked Questions

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, Photoshop yüklü olmadan PSD dosyalarını manipüle etmenizi sağlayan bir kütüphanedir.

**S: Aspose.PSD’yi diğer dosya formatları için de kullanabilir miyim?**  
C: Evet! Öncelikli olarak PSD dosyaları için olsa da Aspose, çeşitli diğer formatlar için de kütüphaneler sunar.

**S: Deneme sürümü mevcut mu?**  
C: Kesinlikle! Ücretsiz bir deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

**S: Yardıma ihtiyacım olursa nereden destek alabilirim?**  
C: Aspose forumunda [buradan](https://forum.aspose.com/c/psd/34) destek bulabilirsiniz.

**S: PNG’den PSD’ye geri dönüştürme yapabilir miyim?**  
C: Aspose.PSD kütüphanesi daha çok PSD dosyalarını okuma ve manipüle etme üzerine odaklanır; diğer formatları PSD’ye dönüştürme bu kapsamda değildir.

**S: Her katmanı ayrı bir PNG olarak nasıl çıkarabilirim?**  
C: `image.getLayers()` üzerinde döngü kurun, her katman için yeni bir `Bitmap` oluşturun ve kendi `PngOptions` ile kaydedin. Böylece katman başına ayrı PNG dosyaları elde edersiniz.

## Conclusion
Artık **PSD katmanlarını çıkarmayı**, tam katman desteğini etkinleştirmeyi ve **PSD katmanlarını PNG’ye dönüştürmeyi** Aspose.PSD for Java kullanarak öğrendiniz. İster otomatik bir varlık hattı oluşturuyor olun, ister masaüstü uygulamanıza grafik yetenekleri ekliyor olun, bu yaklaşım Photoshop’a ihtiyaç duymadan Photoshop dosyaları üzerinde ince kontrol sağlar. Filtre uygulama, programatik olarak katman birleştirme veya her katmanı ayrı ayrı dışa aktarma gibi konuları keşfetmeye devam edin.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}