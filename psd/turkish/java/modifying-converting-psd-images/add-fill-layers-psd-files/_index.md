---
date: 2026-03-04
description: Aspose.PSD for Java ile doldurma katmanları ekleyerek PSD katmanlarını
  programlı olarak nasıl değiştireceğinizi öğrenin. Tasarımlarınızı hızlı bir şekilde
  geliştirmek için bu adım adım kılavuzu izleyin.
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: PSD Katmanlarını Programatik Olarak Değiştir – Doldurma Katmanları Ekle (Java)
url: /tr/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Katmanlarını Programlı Olarak Değiştir – Doldurma Katmanları Ekle (Java)

Programlı olarak **PSD katmanlarını değiştirmek** istiyorsanız, doldurma katmanları eklemek Photoshop belgelerinizi Photoshop'u hiç açmadan zenginleştirmenin en hızlı yollarından biridir. Bu öğreticide yeni bir PSD oluşturmak, renk, degrade ve desen doldurma katmanları eklemek ve ardından sonucu kaydetmek için gereken adımları adım adım göstereceğiz—tüm bunlar Aspose.PSD for Java kullanılarak.

## Hızlı Yanıtlar
- **Ne başarabilirim?** PSD dosyasına programlı olarak renk, degrade ve desen doldurma katmanları ekleyin.  
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java (en son sürüm).  
- **Lisans gerekli mi?** Test için ücretsiz deneme çalışır; üretim için ticari lisans gerekir.  
- **Uygulama ne kadar sürer?** Temel bir örnek için yaklaşık 10‑15 dakika.  
- **Hangi Java sürümü destekleniyor?** JDK 11 veya daha yenisi.

## “Programlı olarak PSD katmanlarını değiştirmek” nedir?
Programlı olarak PSD katmanlarını değiştirmek, bir Photoshop belgesi içinde katmanları oluşturmak, düzenlemek veya silmek için kod kullanmak anlamına gelir ve tasarım iş akışı üzerinde manuel kullanıcı arayüzü etkileşimi olmadan tam kontrol sağlar.

## Neden Aspose.PSD ile doldurma katmanları ekleyelim?
- **Otomasyon** – Toplu işte onlarca PSD oluşturun.  
- **Tutarlılık** – Aynı renk, degrade veya deseni birden fazla dosyada aynı şekilde uygulayın.  
- **Hız** – Photoshop'taki zaman alan manuel adımları atlayın.  
- **Çapraz platform** – Java'yı destekleyen herhangi bir işletim sisteminde çalışır.

## Önkoşullar
Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – JDK 11 veya daha yenisini kurun. [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.  
2. **Aspose.PSD for Java** – Resmi indirme sayfasından en son kütüphaneyi alın: [burada](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Temel Java bilgisi** – Sınıflar ve metodlarla ilgili bir aşinalık yardımcı olur, ancak öğretici her şeyi adım adım açıklar.

## Paketleri İçe Aktarma
PSD dosyalarıyla çalışmaya başlamak için ilgili Aspose.PSD sınıflarını içe aktarmanız gerekir:

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

Bu importlar, `PsdImage` nesnesine (belgenin kendisi) ve kullanacağımız çeşitli `FillLayer` türlerine erişim sağlar.

## PSD Katmanlarını Programlı Olarak Değiştirme – Adım Adım Kılavuz

### Adım 1: Çıktı Dizinini Ayarlayın
Oluşturulan PSD'nin nerede kaydedileceğini tanımlayın, böylece daha sonra bulabilirsiniz.

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

`"Your Document Directory"` ifadesini makinenizdeki mutlak ya da göreli bir yol ile değiştirin.

### Adım 2: Yeni Bir Photoshop Belgesi Oluşturun
Doldurma katmanlarını barındıracak boş bir tuval oluşturun.

```java
PsdImage psdImage = new PsdImage(100, 100);
```

`100, 100` parametreleri genişlik ve yüksekliği piksel olarak temsil eder. Tasarım gereksinimlerinize göre ayarlayın.

### Adım 3: Renk Doldurma Katmanı Ekleyin
Katı renkli bir doldurma katmanı oluşturun ve ona anlaşılır bir ad verin.

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

Daha sonra katmanın doldurma ayarlarına erişerek gerçek rengi değiştirebilirsiniz (kısalık nedeniyle burada gösterilmemiştir).

### Adım 4: Degrade Doldurma Katmanı Ekleyin
Degrade doldurmalar derinlik ve görsel ilgi katar.

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

Katmanın ayarları aracılığıyla doğrusal veya radyal degradelerle denemeler yapmaktan çekinmeyin.

### Adım 5: Desen Doldurma Katmanı Ekleyin
Desen doldurmalar, bir katmanda görüntüleri veya dokuları döşemenize olanak tanır.

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

Opaklığı %50'ye ayarlamak, deseni alt katmanlarla güzel bir şekilde harmanlar.

### Adım 6: PSD Dosyanızı Kaydedin
Değişiklikleri diske kaydedin.

```java
psdImage.save(outPsdFilePath);
```

Kaydedilen dosyayı Photoshop'ta veya herhangi bir PSD görüntüleyicide açarak üç yeni doldurma katmanını görebilirsiniz.

### Adım 7: Kaynakları Temizleyin
Yerel belleği serbest bırakmak için `PsdImage` nesnesini her zaman dispose edin.

```java
psdImage.dispose();
```

## Yaygın Sorunlar ve İpuçları
- **Geçersiz çıktı yolu** – Dizin mevcut olduğundan ve yazma izniniz olduğundan emin olun.  
- **Bellek kullanımı** – Çok büyük tuvallar için, görüntüyü bitirir bitirmez `psdImage.dispose()` çağırın.  
- **Katman sırası** – Katmanlar varsayılan olarak yığının en üstüne eklenir; belirli bir sıra gerekiyorsa `psdImage.insertLayer(layer, index)` kullanın.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java kullanarak hangi tür doldurma katmanları ekleyebilirim?**  
**C:** Renk, degrade ve desen doldurma katmanları ekleyebilirsiniz.

**S: Aspose.PSD diğer görüntü formatlarını destekliyor mu?**  
**C:** Evet, BMP, JPEG, PNG ve daha birçok formatla çalışır.

**S: Aspose.PSD'yi ücretsiz kullanabilir miyim?**  
**C:** Aspose.PSD for Java ücretsiz deneme sürümünü [burada](https://releases.aspose.com/) keşfedebilirsiniz.

**S: Aspose.PSD hakkında daha fazla belgeyi nereden bulabilirim?**  
**C:** Tam dökümantasyona [buradan](https://reference.aspose.com/psd/java/) erişebilirsiniz.

**S: Aspose.PSD için bir destek topluluğu var mı?**  
**C:** Evet, Aspose forumunda topluluktan yardım alabilirsiniz: [burada](https://forum.aspose.com/c/psd/34).

## Sonuç
Artık Aspose.PSD for Java kullanarak çeşitli doldurma katmanları ekleyerek **PSD katmanlarını programlı olarak değiştirmeyi** öğrendiniz. Bu yaklaşım zaman kazandırır, projeler arasında tutarlılık sağlar ve güçlü toplu işleme senaryolarının kapısını açar. Farklı renkler, degradeler ve desenlerle deney yaparak otomatik tasarım oluşturmanın sınırlarını keşfedin.

---

**Son Güncelleme:** 2026-03-04  
**Test Edilen:** Aspose.PSD for Java (en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}