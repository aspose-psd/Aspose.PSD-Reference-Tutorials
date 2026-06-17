---
date: 2026-05-29
description: Aspose.PSD for Java kullanarak renkli metinle PSD'yi PNG olarak nasıl
  kaydedeceğinizi öğrenin. Bu adım adım rehber, PSD'yi PNG'ye verimli bir şekilde
  dönüştürmeyi gösterir.
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: Metin Katmanında Farklı Renklerde Metin Oluşturma
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Renkli Metin Kullanarak PSD'yi PNG Olarak Kaydet
url: /tr/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java kullanarak Renkli Metinle PSD'yi PNG Olarak Kaydet

Aspose.PSD for Java kullanarak farklı renkli metinle **PSD'yi PNG olarak kaydetme** konusunda adım adım rehberimize hoş geldiniz. Aspose.PSD, Photoshop dosyalarını programlı olarak manipüle etmenizi sağlayan güçlü bir Java kütüphanesidir ve PSD ve PSB dosya formatlarıyla çalışmak için kapsamlı yetenekler sunar.

Bu öğreticide, Aspose.PSD kullanarak bir metin katmanında çeşitli renklerde metin oluşturma sürecini adım adım göstereceğiz. Rehberin sonunda, bu görevi sorunsuz bir şekilde nasıl gerçekleştireceğinizi net bir şekilde anlayacaksınız.

## Hızlı Yanıtlar
- **PSD'yi PNG olarak nasıl kaydedilir?** Aspose.PSD'nin `PsdImage` sınıfını kullanarak PSD'yi yükleyin ve `PngOptions` ile `save` metodunu çağırın.
- **Tek bir metin katmanında birden fazla renk oluşturabilir miyim?** Evet, metnin her bir `Portion`'ına farklı `Color` nesneleri atayabilirsiniz.
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri desteklenir.
- **Üretim için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.
- **Kütüphane büyük dosyalar için bellek verimli mi?** Tam bellek içinde yükleme yapmadan 2 GB'a kadar dosyaları işleyebilir.

## Renkli Metinle PSD'yi PNG Olarak Nasıl Kaydedilir?
PSD dosyanızı yükleyin, metin katmanının bölümlerini (portion) farklı renkler atayacak şekilde değiştirin ve ardından görüntüyü PNG olarak kaydedin—bu tüm iş akışı sadece birkaç Java kod satırıyla gerçekleştirilir. Aspose.PSD, düzenlenen katmanı otomatik olarak rasterleştirir, şeffaflığı ve renk doğruluğunu korur, böylece ortaya çıkan PNG orijinal tasarımla eşleşir.

## Aspose.PSD for Java Nedir?
Aspose.PSD for Java, Photoshop (PSD/PSB) dosyalarının programlı olarak oluşturulmasını, düzenlenmesini ve dönüştürülmesini sağlayan bir kütüphanedir. **50+ görüntü formatını** destekler ve tüm dosyayı belleğe yüklemeden çok sayfalı belgeleri işleyebilir, sunucu tarafı otomasyon için yüksek performans sunar.

## Önkoşullar
- Java programlama temellerine aşina olmak.
- Aspose.PSD for Java kütüphanesinin yüklü olması. Kütüphaneyi [Aspose.PSD for Java belgeleri](https://reference.aspose.com/psd/java/) adresinden indirebilirsiniz.

## Paketleri İçe Aktarma
`Image` görüntü dosyalarını yüklemek ve kaydetmek için temel sınıftır. `PsdImage` bir Photoshop belgesini temsil eder, `TextLayer` ise metin katmanı özelliklerine erişim sağlar. `PngOptions` PNG dışa aktarımı için ayarları tanımlar.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: Projenizi Kurun
Yeni bir Java projesi oluşturun ve Aspose.PSD kütüphanesini ekleyin. Proje dizininizdeki dosyalara erişim ve değiştirme izinlerinizin olduğundan emin olun.

## Adım 2: Kaynak ve Çıktı Dizinlerini Tanımlayın
PSD dosyalarınızın bulunduğu kaynak dizini ve üretilen görüntülerin kaydedileceği çıktı dizinini belirtin. `sourceDir` ve `outputDir` değişkenlerini buna göre güncelleyin.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## Adım 3: PSD Dosyasını Yükleyin ve Metin Katmanına Erişin
`PsdImage` bir PSD dosyasını belleğe yükler ve `TextLayer` bu katmandaki metin içeriğini manipüle etmenizi sağlar.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## Adım 4: PNG Ayarlarını Belirleyin ve Oluşan Görüntüyü Kaydedin
`PngOptions` renk tipi ve sıkıştırma gibi PNG çıktı parametrelerini yapılandırır.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## Yaygın Sorunlar ve Çözümleri
- **Lisans eksikliği hatası:** Herhangi bir kaydetme işlemi çağırmadan önce geçerli bir lisans dosyası uyguladığınızdan emin olun.
- **Renk uygulanmadı:** Metin katmanındaki her bir `Portion`'ın `Color` özelliğinin doğru ayarlandığını doğrulayın.
- **Büyük dosya bellek kullanımı:** Büyük dosyaları akış olarak işlemek için `PsdImage`'ın `loadOptions` ile `load` aşırı yüklemesini (overload) kullanın.

## Sıkça Sorulan Sorular
**Q: Aspose.PSD for Java'yi diğer programlama dilleriyle kullanabilir miyim?**  
A: Aspose.PSD öncelikle Java için tasarlanmıştır, ancak Aspose çeşitli programlama dilleri için benzer kütüphaneler sunar.

**Q: Aspose.PSD for Java için deneme sürümü mevcut mu?**  
A: Evet, ücretsiz bir deneme sürümünü [Aspose.PSD](https://releases.aspose.com/) adresinden edinebilirsiniz.

**Q: Ek destek veya yardım nereden bulunabilir?**  
A: Topluluk desteği ve tartışmalar için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edin.

**Q: Aspose.PSD for Java için geçici bir lisans nasıl alınır?**  
A: Geçici bir lisansı [Aspose.PSD](https://purchase.aspose.com/temporary-license/) adresinden talep edebilirsiniz.

**Q: Aspose.PSD için başka öğreticiler mevcut mu?**  
A: Evet, daha fazla öğretici ve örnek için [Aspose.PSD belgelerini](https://reference.aspose.com/psd/java/) inceleyebilirsiniz.

**Q: Kütüphane birden fazla PSD dosyasını PNG'ye toplu dönüştürmeyi destekliyor mu?**  
A: Evet, bir klasördeki PSD dosyaları üzerinde döngüyle iterasyon yapabilir, aynı metin‑renk mantığını uygulayabilir ve her birini PNG olarak kaydedebilirsiniz.

**Q: Çıktı PNG kayıpsız mı?**  
A: Aspose.PSD ile kaydedilen PNG tam kayıpsız kaliteyi korur, tüm renk ve şeffaflık bilgilerini saklar.

---

**Son Güncelleme:** 2026-05-29  
**Test Edilen Versiyon:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler
- [Aspose.PSD for Java kullanarak PSD'yi PNG olarak Dışa Aktar ve Yeni Normal Katman Ekle](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Aspose.PSD for Java'da PSD'yi PNG olarak Kaydet ve Render Gölgeli Düşme Uygula](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java ile Renk Katmanı Kullanarak PSD'yi PNG'ye Dönüştür](/psd/java/advanced-image-manipulation/rendering-color-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}