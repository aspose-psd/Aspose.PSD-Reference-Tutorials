---
date: 2026-04-08
description: Bir aspose geçici lisansı kullanarak Aspose.PSD for Java ile PSD'yi PNG'ye
  nasıl dışa aktaracağınızı ve yeni bir PSD katmanı oluşturacağınızı öğrenin. Bu adım
  adım öğretici, PSD görüntü işleme ve katman konumunu ayarlamayı kapsar.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: PSD'ye yeni bir normal katman ekle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java kullanarak PSD'yi PNG'ye dışa aktar ve yeni bir normal
  katman ekle – aspose geçici lisansı
url: /tr/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dışa Aktar ve Aspose.PSD for Java Kullanarak Yeni Normal Katman Ekle

## Giriş

Bu **aspose psd tutorial** içinde **export PSD to PNG** yapmayı ve aynı dosya içinde **creating a new regular layer** oluşturmayı, **using an aspose temporary license** ile geliştirme aşamasında keşfedeceksiniz. Web‑hazır küçük resimler oluşturmanız, bir tasarım hattı için varlıkları hazırlamanız veya sadece **psd image manipulation** ile deneme yapmanız gerekse, Aspose.PSD for Java size tam programatik kontrol sunar. Kaynak dosyayı yüklemekten güncellenmiş PSD ve bir PNG kopyasını kaydetmeye kadar her adımı adım adım göstereceğiz; böylece PSD katmanlarını hemen manipüle etmeye başlayabilirsiniz.

## Hızlı Yanıtlar
- **PSD'yi PNG'ye tek bir çağrı ile dışa aktarabilir miyim?** Evet, katmanları ekledikten sonra `save` metodunu `PngOptions` ile çağırabilirsiniz.
- **Geliştirme için bir lisansa ihtiyacım var mı?** Test için geçici bir lisans yeterlidir; üretim için tam lisans gereklidir.
- **Hangi Java sürümü destekleniyor?** Aspose.PSD, Java 8 ve üzeri sürümlerle çalışır.
- **Katman konumlandırması piksel bazlı mı?** Evet, **set layer position** metodlarını kullanarak sol, üst, sağ, alt koordinatları piksellerle ayarlarsınız.
- **PNG katman şeffaflığını koruyacak mı?** PNG, tüm görünür katmanların birleştirilmiş sonucunu içerir.

## Neden aspose geçici lisansı kullanmalısınız?

Bir **aspose temporary license**, Aspose.PSD'nin tam özellik setini herhangi bir fonksiyonel kısıtlama olmadan değerlendirmenizi sağlar. Değerlendirme filigranını kaldırır, **create new psd layer** nesneleri oluşturma dahil tüm API'leri açar ve kalıcı bir lisans satın almadan önce kodunuzu üretim‑benzeri bir ortamda test etmenize olanak tanır.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Development Environment** – JDK 8+ ve bir derleme aracı (Maven/Gradle) kurulu.
- **Aspose.PSD for Java** – En son JAR dosyasını resmi siteden [burada](https://releases.aspose.com/psd/java/) indirin.
- **A sample PSD file** – Örneklerde `OneLayer.psd` dosyasını kullanacağız.

## Paketleri İçe Aktar

Java sınıfınıza gerekli importları ekleyin. Bu sınıflar **psd image manipulation** ve katman yönetimi için temel işlevselliği sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position” nedir ve neden önemlidir?

Yeni bir katman eklediğinizde, katmanın tuval üzerinde nerede görüneceğini tanımlamanız gerekir. `setLeft`, `setTop`, `setRight` ve `setBottom` metodları **set layer position** değerlerini piksel koordinatlarıyla ayarlar. Doğru konumlandırma, grafiklerinizin tam olarak istediğiniz yerde hizalanmasını sağlar; bu, UI varlıklarını birleştirme veya baskıya hazır dosyalar hazırlama gibi görevler için kritiktir.

## Adım‑adım kılavuz

### Adım 1: PSD Dosyasını Yükle

İlk olarak, değiştirmek istediğiniz mevcut PSD dosyasını yükleyin. Bu, üzerinde çalışabileceğiniz bir `PsdImage` nesnesi oluşturur.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Adım 2: Piksel Verilerini ve Dikdörtgenleri Hazırla

İki piksel tamponu (`int[]`) oluşturacak ve yeni katmanların boyanacağı dikdörtgen alanları tanımlayacağız. Bu, **creating a new psd layer** için temel oluşturur.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Adım 3: Katman Verilerini Başlat

Piksel tamponlarını varsayılan bir ARGB değeriyle doldurun. `-10000000` değeri yarı şeffaf koyu bir tonla eşleşir.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Adım 4: Normal Katmanlar Ekle (PSD Katmanlarını Manipüle Et)

Şimdi **add regular layers** işlemini PSD görüntüsüne uygulayıp **set layer position** metodlarıyla sol, üst, sağ ve alt özelliklerini ayarlayacağız. Bu, **manipulate PSD layers** programatik olarak nasıl yapılır gösterir.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Adım 5: PSD'yi PNG'ye Dışa Aktar ve Güncellenmiş PSD'yi Kaydet

Katmanlar yerleştirildikten sonra, değiştirilmiş belgeyi kaydedin. İlk olarak sonucu PNG'ye dışa aktaracağız (**export psd to png** adımı), ardından yeni katmanlarla PSD'yi kalıcı hâle getireceğiz.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Sadece PNG'ye ihtiyacınız varsa, PSD `save` çağrısını atlayabilir ve doğrudan `save` metodunu `PngOptions` ile çalıştırabilirsiniz.

## Yaygın Sorunlar ve Sorun Giderme

| Semptom | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| PNG boş görünüyor | Katmanlar görünmez veya tamamen şeffaf | Şeffaf olmayan piksel değerleri ayarladığınızdan emin olun veya `layer.setVisible(true)` metodunu çağırın. |
| `ArrayIndexOutOfBoundsException` | Dikdörtgen boyutu ile piksel dizisi uzunluğu eşleşmiyor | `rect.width * rect.height == dataArray.length` eşitliğini doğrulayın. |
| LicenseException çalışma zamanında | Geçerli bir lisans yüklenmemiş | API metodlarını çağırmadan önce geçici veya kalıcı bir lisans yükleyin. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD Java 8 ile uyumlu mu?**  
C: Evet, Aspose.PSD Java 8 ve sonraki sürümlerini destekler.

**S: Eklenen katmanlara dönüşümler (döndürme, ölçekleme) uygulayabilir miyim?**  
C: Kesinlikle! `Layer` sınıfı, tam dönüşüm kontrolü için `rotate`, `scale` ve `translate` gibi metodlar sunar.

**S: Ek Aspose.PSD belgelerini nerede bulabilirim?**  
C: Ayrıntılı API dokümantasyonu [burada](https://reference.aspose.com/psd/java/) mevcuttur.

**S: Aspose.PSD için geçici bir lisans nasıl alınır?**  
C: Geçici‑lisans sayfasını [burada](https://purchase.aspose.com/temporary-license/) ziyaret edin.

**S: Aspose.PSD desteği için topluluk forumları var mı?**  
C: Evet, Aspose forumlarında [burada](https://forum.aspose.com/c/psd/34) tartışmalara katılabilirsiniz.

## Sonuç

Artık **export PSD to PNG** yaparken **adding new regular layers** işlemini Aspose.PSD for Java ile nasıl gerçekleştireceğinizi öğrendiniz ve **aspose temporary license** sayesinde bu iş akışını kısıtlama olmadan deneyebileceğinizi gördünüz. Bu öğretici, temel **psd image manipulation** yeteneklerini gösteriyor: bir dosyayı yükleme, katman oluşturma, piksel verilerini doldurma ve son kompozisyonu dışa aktarma. Farklı dikdörtgen boyutları, piksel renkleri veya katman efektleriyle deney yaparak çıktıyı projenizin ihtiyaçlarına göre özelleştirmekten çekinmeyin.

---

**Son Güncelleme:** 2026-04-08  
**Test Edildiği Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}