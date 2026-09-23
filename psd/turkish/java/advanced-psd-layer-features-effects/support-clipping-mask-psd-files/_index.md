---
date: 2026-09-23
description: Aspose.PSD for Java kullanarak transparency ve clipping mask desteğini
  koruyarak PSD'yi PNG'ye nasıl dışa aktaracağınızı öğrenin. Bu kılavuz, transparency
  PNG'yi korumak için hızlı adımları gösterir.
keywords:
- how to export psd to png
- how to keep transparency png
- Aspose.PSD Java clipping mask
lastmod: 2026-09-23
linktitle: PSD'yi PNG olarak nasıl dışa aktarılır – Aspose.PSD Java
og_description: Aspose.PSD for Java kullanarak transparency ve clipping mask desteğini
  koruyarak PSD'yi PNG'ye nasıl dışa aktaracağınızı öğrenin. Adım adım kılavuzu takip
  ederek transparency PNG'yi koruyun.
og_image_alt: 'Guide: export PSD to PNG with clipping mask using Aspose.PSD Java'
og_title: Aspose.PSD kullanarak clipping mask ile PSD'yi PNG'ye nasıl dışa aktarılır
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to export PSD to PNG while keeping transparency and clipping
    mask support using Aspose.PSD for Java. This guide shows quick steps to keep transparency
    PNG.
  headline: How to export PSD to PNG with clipping mask using Aspose.PSD
  type: TechArticle
- description: Learn how to export PSD to PNG while keeping transparency and clipping
    mask support using Aspose.PSD for Java. This guide shows quick steps to keep transparency
    PNG.
  name: How to export PSD to PNG with clipping mask using Aspose.PSD
  steps:
  - name: define your document directory
    text: First, tell the program where your source PSD lives and where the PNG should
      be written. Replace `"Your Document Directory"` with the absolute path on your
      machine that contains the PSD files.
  - name: load the PSD file
    text: PsdImage represents a Photoshop document in memory, providing access to
      layers, masks, and metadata.
  - name: set up export options
    text: PngOptions configures how the PNG file is written, including color type
      and compression settings.
  - name: export the image
    text: Calling the save method writes the image to disk using the specified options.
      The resulting PNG can be used directly in web pages, mobile apps, or any place
      that accepts raster images.
  - name: clean up resources
    text: Dispose releases native resources held by the PsdImage instance to prevent
      memory leaks.
  type: HowTo
- questions:
  - answer: A clipping mask uses the opacity of one layer to limit the visibility
      of another, allowing complex composites without permanently altering layers.
    question: What is a clipping mask in PSD files?
  - answer: Yes, you can edit layers, apply effects, and export to formats like PNG
      or JPEG.
    question: Can I use Aspose.PSD to edit PSD files?
  - answer: You can find comprehensive documentation for Aspose.PSD for Java on the
      [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find documentation for Aspose.PSD?
  - answer: Yes! You can access a free trial version of Aspose.PSD on the [Aspose.PSD
      free trial](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD?
  - answer: For any queries or issues, you can get support through the Aspose PSD
      forum at the [Aspose PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- clipping mask
- Aspose.PSD
- Java image processing
- PNG transparency
title: Aspose.PSD kullanarak clipping mask ile PSD'yi PNG'ye nasıl dışa aktarılır
url: /tr/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD kullanarak kırpma maskesiyle PSD'yi PNG'ye nasıl dışa aktarılır

## Giriş
Kırpma maskesi bilgilerini koruyarak **PSD'yi PNG'ye nasıl dışa aktaracağınızı** arıyorsanız, Aspose.PSD for Java bunu zahmetsiz hale getirir. Bu öğreticide, PSD dosyalarını programlı olarak nasıl işleyip, kırpma maskelerini uygulayacağınızı ve **PSD'yi PNG'ye kaydetmeyi** tam şeffaflık desteğiyle adım adım göstereceğiz. Sonunda, Java projelerinize doğrudan entegre edebileceğiniz yeniden kullanılabilir bir kod parçacığına sahip olacaksınız.

## Hızlı cevaplar
- **Kütüphane ne yapar?** Photoshop PSD dosyalarını Java'da okur, düzenler ve dışa aktarır.  
- **Kırpma maskelerini koruyabilir mi?** Evet – PNG'ye dışa aktarırken maskeler korunur.  
- **Kayıpsız dışa aktarım için hangi format kullanılır?** `TruecolorWithAlpha` ile PNG.  
- **Üretim için lisans gerekir mi?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **Hangi Java sürümü gereklidir?** JDK 8 veya üzeri.

## PSD dosyalarında kırpma maskesi nedir?
Kırpma maskesi, bir katmanın opaklığını kullanarak başka bir katmanın görünürlüğünü sınırlar, böylece alttaki katmanları kalıcı olarak değiştirmeden karmaşık kompozisyonlar oluşturulabilir.  
Dışa aktarırken, maskenin şeffaflığı çıkış formatına aktarılmalıdır, aksi takdirde sonuç opak görünür.

## Şeffaf PNG neden korunmalı?
Şeffaflığın korunması, dışa aktarılan görüntüyü herhangi bir arka plan üzerine görsel bozulma olmadan yerleştirmenizi sağlar. Aspose.PSD, **TruecolorWithAlpha** ile PNG'yi destekler; bu, kanal başına 8‑bit renk ve 8‑bit alfa kanalı depolar ve web ve mobil kullanım için kayıpsız şeffaflık garantisi verir.

## Önkoşullar
Kodun içine girmeden önce, aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – en az JDK 8. [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) indirin.  
2. **Aspose.PSD for Java Library** – en son JAR'ı [indirme sayfasından](https://releases.aspose.com/psd/java/) edinin. Ayrıca [ücretsiz deneme](https://releases.aspose.com/) sürümünü deneyebilirsiniz.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Temel Java Bilgisi** – dosya G/Ç ve nesne‑yönelimli kavramlara aşina olmak yardımcı olur.

## PSD'yi PNG olarak dışa aktar – adım adım kılavuz

### Adım 1: belge dizininizi tanımlayın
İlk olarak, programın kaynak PSD dosyanızın nerede olduğunu ve PNG'nin nereye yazılacağını bilmesini sağlayın.

`"Your Document Directory"` ifadesini, PSD dosyalarını içeren makinenizdeki mutlak yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

### Adım 2: PSD dosyasını yükleyin
PsdImage, bellekte bir Photoshop belgesini temsil eder ve katmanlara, maskelere ve meta verilere erişim sağlar.

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Adım 3: dışa aktarım seçeneklerini ayarlayın
PngOptions, PNG dosyasının nasıl yazılacağını, renk tipi ve sıkıştırma ayarları dahil olmak üzere yapılandırır.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### Adım 4: görüntüyü dışa aktar
save metodunu çağırmak, belirtilen seçenekleri kullanarak görüntüyü diske yazar.

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

Ortaya çıkan PNG, web sayfalarında, mobil uygulamalarda veya raster görüntü kabul eden herhangi bir yerde doğrudan kullanılabilir.

### Adım 5: kaynakları temizleyin
Dispose, PsdImage örneği tarafından tutulan yerel kaynakları serbest bırakarak bellek sızıntılarını önler.

```java
im.dispose();
```

### PSD'yi PNG'ye tek satırda nasıl kaydedilir
Aşağıdaki tek satır, dosyayı yükler, yapılandırır ve tek bir ifadeyle kaydeder.

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*(Yukarıdaki genişletilmiş sürüm, açıklık ve hata ayıklama kolaylığı için gösterilmiştir.)*

## Yaygın sorunlar ve çözümler
- **Şeffaflık eksik:** `PngColorType.TruecolorWithAlpha` ayarlandığından emin olun; aksi takdirde PNG opak olur.  
- **Dosya bulunamadı:** `dataDir`'in uygun yol ayırıcıyla (`/` veya `\\`) bittiğini doğrulayın.  
- **OutOfMemoryError:** Özellikle büyük dosyalar veya toplu işlemler yaparken `PsdImage`'i hemen Dispose edin.  
- **PSD'yi PNG'ye toplu dönüştürme:** Adımları bir döngü içinde sarın ve performansı artırmak için `PngOptions`'ı yeniden kullanın.

## Sıkça Sorulan Sorular

**Q: PSD dosyalarında kırpma maskesi nedir?**  
**A:** Kırpma maskesi, bir katmanın opaklığını kullanarak başka bir katmanın görünürlüğünü sınırlar, katmanları kalıcı olarak değiştirmeden karmaşık kompozisyonlara izin verir.

**Q: Aspose.PSD'yi PSD dosyalarını düzenlemek için kullanabilir miyim?**  
**A:** Evet, katmanları düzenleyebilir, efektler uygulayabilir ve PNG veya JPEG gibi formatlara dışa aktarabilirsiniz.

**Q: Aspose.PSD belgelerini nerede bulabilirim?**  
**A:** Aspose.PSD for Java için kapsamlı belgeleri [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) adresinde bulabilirsiniz.

**Q: Aspose.PSD için bir deneme sürümü mevcut mu?**  
**A:** Evet! Aspose.PSD'nin ücretsiz deneme sürümüne [Aspose.PSD free trial](https://releases.aspose.com/) üzerinden erişebilirsiniz.

**Q: Aspose.PSD sorunları için nasıl destek alabilirim?**  
**A:** Herhangi bir soru veya sorun için, [Aspose PSD forum](https://forum.aspose.com/c/psd/34) üzerinden destek alabilirsiniz.

## Sonuç
Artık Aspose.PSD for Java kullanarak kırpma maskelerini koruyarak **PSD'yi PNG'ye nasıl dışa aktaracağınızı** öğrendiniz. Bu yaklaşım, tasarım süreçlerini otomatikleştirmenizi, Photoshop varlıklarını arka uç hizmetlerine entegre etmenizi ve manuel dışa aktarım adımları olmadan görsel bütünlüğü korumanızı sağlar. Katman birleştirme, renk ayarlamaları ve toplu işleme gibi diğer Aspose.PSD özelliklerini keşfederek iş akışınızı daha da sadeleştirebilirsiniz.

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java kullanarak Katman Maskesi Desteğiyle PSD'yi PNG'ye Dönüştür](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Aspose.PSD for Java kullanarak Katman Efektleriyle PSD'yi PNG'ye Dışa Aktar](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD for Java ile PSD'yi PNG'ye Dönüştür ve Vektör Maskesi Oluştur – PSD Dosyalarındaki Vmsk Kaynağı](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}