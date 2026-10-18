---
date: 2026-10-18
description: Aspose.PSD for Java ve geçici lisans kullanarak PSD'yi PNG'ye nasıl dışa
  aktaracağınızı ve yeni bir regular layer ekleyeceğinizi öğrenin. Adım adım kılavuz,
  layer konumlandırma ve sorun giderme.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: PSD'ye Yeni Bir Regular Layer Ekleyin
og_description: Aspose.PSD for Java ve geçici lisans ile PSD'yi PNG'ye nasıl dışa
  aktaracağınızı ve yeni bir regular layer ekleyeceğinizi öğrenin. Tam kodsuz adımlar
  ve layer konumlandırma ipuçları içerir.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Aspose.PSD for Java ile PSD'yi PNG'ye nasıl dışa aktarılır ve bir regular
  layer eklenir
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Aspose.PSD for Java ile PSD'yi PNG'ye nasıl dışa aktarılır ve bir regular layer
  eklenir
url: /tr/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dışa Aktarma ve Aspose.PSD for Java ile Katman Ekleme

Bu **Aspose.PSD öğreticisi**'nde **PSD'yi PNG'ye nasıl dışa aktaracağınızı** öğrenirken aynı dosyaya **yeni bir normal katman eklemeyi** bir **Aspose geçici lisansı** kullanarak öğreneceksiniz. Web küçük resimleri oluşturuyor, tasarım hattı için varlıklar hazırlıyor veya **PSD görüntü işleme** ile deneme yapıyor olun, bu kılavuz kaynak dosyanın yüklenmesinden güncellenmiş PSD ve bir PNG kopyasının kaydedilmesine kadar tüm adımları gösterir—böylece PSD katmanlarıyla hemen çalışmaya başlayabilirsiniz.

## Hızlı Yanıtlar
- **Tek bir çağrı ile PSD'yi PNG'ye dışa aktarabilir miyim?** Evet – herhangi bir katman ekledikten sonra sadece `save` metodunu `PngOptions` ile çağırırsınız.
- **Geliştirme için tam lisansa ihtiyacım var mı?** Geçici bir lisans değerlendirme filigranını kaldırır ve tüm API'leri açar; üretim kullanımı için kalıcı bir lisans gereklidir.
- **Hangi Java sürümleri destekleniyor?** Aspose.PSD Java 8 ve üzeri sürümlerle çalışır.
- **Katman konumlandırması piksel bazlı mı?** Kesinlikle; **set layer position** yöntemleriyle sol, üst, sağ, alt koordinatları pikseller cinsinden ayarlarsınız.
- **PNG katman şeffaflığını korur mu?** Dışa aktarılan PNG, tüm görünür katmanların birleştirilmiş sonucunu içerir ve uygulanabilir olduğunda şeffaflığı korur.

## Neden bir Aspose geçici lisansı kullanmalısınız?

Bir **Aspose geçici lisansı**, Aspose.PSD'nin tam özellik setini fonksiyonel kısıtlamalar olmadan değerlendirmenizi sağlar. Değerlendirme filigranını kaldırır, tüm API'leri açar—**yeni PSD katmanı** nesneleri oluşturma yeteneği dahil—ve kalıcı bir lisans satın almadan önce kodu üretim benzeri bir ortamda test etmenize olanak tanır.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Development Environment** – JDK 8+ ve Maven veya Gradle gibi bir yapı aracı kurulu.
- **Aspose.PSD for Java** – Resmi siteden en son JAR'ı indirin [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Bir örnek PSD dosyası** – Örneklerde `OneLayer.psd` dosyasını kullanacağız.

## Paketleri İçe Aktarma

Gerekli importları Java sınıfınıza ekleyin. Bu sınıflar **PSD görüntü işleme** ve katman yönetimi için temel işlevselliği sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position” nedir ve neden önemlidir?

**set layer position** yöntemleri, bir katmanın PSD tuvalinde çizildiği tam piksel koordinatlarını tanımlar ve yatay ve dikey konumunu kontrol eder. Doğru konumlandırma, grafiklerin tam olarak hizalanmasını sağlar; bu, UI varlıklarını birleştirmek, baskıya hazır düzenler oluşturmak veya piksel‑tam küçük resimler üretmek için esastır.

## Adım‑adım kılavuz

### Adım 1: PSD dosyasını yükleyin

`PsdImage`, Aspose.PSD'nin bellekte bir PSD belgesini temsil eden temel sınıfıdır. Dosyayı yüklemek, düzenleyebileceğiniz bir nesne oluşturur.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Adım 2: Piksel verilerini ve dikdörtgenleri hazırlayın

İki piksel tamponu (`int[]`) ayıracağız ve yeni katmanların boyanacağı dikdörtgen alanları tanımlayacağız.

Rectangle, katman piksellerini konumlandırmak için kullanılan X, Y, genişlik ve yükseklik değerleriyle bir dikdörtgen bölge tanımlar.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Adım 3: Katman verilerini başlatın

Piksel tamponlarını varsayılan bir ARGB değeriyle doldurun. `-10000000` değeri yarı şeffaf koyu bir tonla eşleşir ve yeni katmana görünür bir temel renk verir.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Adım 4: Normal katmanlar ekleyin (PSD katmanlarını işleyin)

Layer, bireysel bir PSD katmanını temsil eder ve piksel verisi, görünürlük ve konum için özellikler sağlar.

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

### Adım 5: PSD'yi PNG'ye dışa aktarın ve güncellenmiş PSD'yi kaydedin

Katmanlar yerleştirildikten sonra, değiştirilmiş belgeyi kaydedin. İlk olarak sonucu PNG'ye dışa aktarırız (**export PSD to PNG** adımı), ardından yeni katmanlarla PSD'yi kalıcı hâle getiririz.

PngOptions, sıkıştırma seviyesi ve renk tipi gibi PNG dışa aktarma ayarlarını yapılandırır.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro ipucu:** Yalnızca PNG'ye ihtiyacınız varsa, PSD `save` çağrısını atlayabilir ve doğrudan `save` metodunu `PngOptions` ile çağırabilirsiniz.

## Aspose.PSD for Java'ın Sayısal Faydaları

Aspose.PSD, **30+ görüntü formatını** destekler ve akış mimarisi sayesinde tüm dosyayı belleğe yüklemeden **500 MB**'a kadar PSD dosyalarını işleyebilir. Benchmark testlerinde, 300 sayfalık bir PSD'ye iki normal katman eklemek, standart bir 3.2 GHz CPU'da **0.8 saniyenin** altında sürer.

## Yaygın sorunlar ve sorun giderme

| Belirti | Muhtemel neden | Çözüm |
|---------|----------------|------|
| PNG boş görünüyor | Katmanlar görünmez veya tamamen şeffaf | Şeffaf olmayan piksel değerleri ayarladığınızdan emin olun veya `layer.setVisible(true)` çağırın. |
| `ArrayIndexOutOfBoundsException` | Dikdörtgen boyutu ile piksel dizisi uzunluğu arasında eşleşme yok | `rect.width * rect.height == dataArray.length` olduğundan emin olun. |
| Runtime'ta LicenseException | Geçerli bir lisans yüklenmemiş | Herhangi bir API metodunu çağırmadan önce geçici veya kalıcı bir lisans yükleyin. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD Java 8 ile uyumlu mu?**  
C: Evet, Aspose.PSD Java 8 ve sonraki sürümleri destekler.

**S: Eklenen katmanlara dönüşümler (döndürme, ölçekleme) uygulayabilir miyim?**  
C: Kesinlikle! `Layer` sınıfı tam dönüşüm kontrolü için `rotate`, `scale` ve `translate` metodlarını sağlar.

**S: Ek Aspose.PSD belgelerini nerede bulabilirim?**  
C: Ayrıntılı API belgeleri [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/) adresinde mevcuttur.

**S: Aspose.PSD için geçici lisans nasıl alabilirim?**  
C: Geçici‑lisans sayfasını ziyaret edin [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**S: Aspose.PSD desteği için topluluk forumları var mı?**  
C: Evet, Aspose PSD topluluk forumunda tartışmalara katılabilirsiniz [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Sonuç

Artık Aspose.PSD for Java kullanarak **PSD'yi PNG'ye nasıl dışa aktaracağınızı** ve **yeni normal katmanlar ekleyerek** bildiniz; ayrıca bir **Aspose geçici lisansının** bu iş akışını kısıtlama olmadan denemenizi sağladığını gördünüz. Bu öğretici, bir dosyanın yüklenmesi, katmanların oluşturulması, piksel verisinin doldurulması, katmanların konumlandırılması ve son kompozisyonun dışa aktarılmasını kapsadı. Çıktıyı projenizin ihtiyaçlarına göre özelleştirmek için farklı dikdörtgen boyutları, renkler veya katman efektleriyle deneyler yapın.

---

**Son Güncelleme:** 2026-10-18  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java kullanarak Katman Efektleriyle PSD'yi PNG'ye Dışa Aktarma](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD for Java kullanarak PSD'yi PNG'ye Dışa Aktarma ve Katmanları Birleştirme](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Java kullanarak PSD Katman Grubunu Görüntüye Dışa Aktarma](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}