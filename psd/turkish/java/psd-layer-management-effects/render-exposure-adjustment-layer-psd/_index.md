---
date: 2026-04-05
description: Aspose.PSD for Java kullanarak PSD dosyalarında pozlama ayar katmanını
  nasıl render edeceğinizi öğrenin. Pozlama katmanlarını değiştirme ve ekleme için
  adım adım kılavuz ve kod örnekleri.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: PSD Dosyalarında Pozlama Ayar Katmanını İşleme - Java
second_title: Aspose.PSD Java API
title: PSD Dosyalarında Poz Ayar Katmanını Render Et - Java
url: /tr/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında Pozlama Ayar Katmanını Oluşturma - Java

## Giriş

Photoshop PSD dosyalarıyla çalışıyor musunuz ve programlı olarak **pozlama ayar katmanını render** etmeniz mi gerekiyor? Mevcut katmanları ayarlıyor ya da yenilerini ekliyor olun, Aspose.PSD for Java bu görevleri güçlü ve sezgisel bir şekilde yönetmenizi sağlar. Bu rehberde, Aspose.PSD for Java’yı kullanarak PSD dosyalarında pozlama ayar katmanlarını nasıl render edip değiştireceğinizi adım adım göstereceğiz. Bu öğreticinin sonunda, mevcut katmanlardaki pozlama ayarlarını nasıl düzenleyeceğinizi ve PSD dosyalarınıza yeni pozlama ayar katmanları ekleyeceğinizi öğreneceksiniz. Hadi başlayalım!

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java
- **Mevcut bir pozlama katmanını düzenleyebilir miyim?** Evet, pozlamayı, offseti ve gama düzeltmesini değiştirebilirsiniz.
- **Yeni bir pozlama ayar katmanı nasıl eklenir?** `PsdImage` örneği üzerinde `addExposureAdjustmentLayer()` kullanın.
- **PNG dışa aktarımı destekleniyor mu?** Kesinlikle – sonucu PNG olarak kaydetmek için `PngOptions` kullanın.
- **Üretim için lisansa ihtiyacım var mı?** Üretim kullanımında ticari bir lisans gereklidir; ücretsiz deneme mevcuttur.

## Render pozlama ayar katmanı nedir?

Pozlama ayar katmanı, alttaki görüntünün parlaklığını, offsetini ve gamasını değiştiren, yıkıcı olmayan bir Photoshop katmanıdır. Render edilmesi, bu ayarların uygulanması ve görsel sonucun ayarlamaları yansıtması anlamına gelir; ardından PNG gibi formatlara dışa aktarabilirsiniz.

## Aspose.PSD for Java ile pozlama ayar katmanını render etmek neden tercih edilmeli?

- **Tam kontrol** – Photoshop açmadan katman özelliklerini yönetin.
- **Toplu işleme** – birçok dosyada ayarları otomatikleştirin.
- **Çapraz platform** – JDK yüklü herhangi bir sistemde çalışır.
- **PSD yapısını korur** – katmanları gelecekteki düzenlemeler için düzenlenebilir tutar.

## Önkoşullar

1. **Java Development Kit (JDK)** – en az JDK 8.
2. **Aspose.PSD for Java** – bunu [buradan](https://releases.aspose.com/psd/java/) indirin.
3. **Temel Java bilgisi** – standart Java sözdizimiyle rahat olmalısınız.
4. **IDE veya Metin Editörü** – IntelliJ IDEA, Eclipse, VS Code veya tercih ettiğiniz herhangi bir editör.

## Paketleri İçe Aktarma

İlk olarak, gerekli Aspose.PSD sınıflarını içe aktarın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Pozlama ayar katmanını render etme – Adım Adım Kılavuz

### Adım 1: PSD Dosyasını Yükle

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

`"Your Document Directory"` ifadesini PSD dosyalarınızı içeren klasörle değiştirin. `Image.load()` yöntemi, belge katmanlarına tam erişim sağlayan bir `PsdImage` nesnesi döndürür.

### Adım 2: Mevcut Bir Pozlama Ayar Katmanını Düzenle

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

Döngü, her katmanı dolaşır, herhangi bir `ExposureLayer` bulur ve üç ana parametresini günceller. Bu, **pozlama ayar katmanını render etmenin** temelidir ve kendi değerlerinizi uygular.

### Adım 3: Değiştirilmiş PSD Dosyasını Kaydet

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

Değiştirilmiş PSD, tüm orijinal katmanları korur, ancak pozlama ayarı artık yeni ayarları yansıtır.

### Adım 4: Sonucu PNG Olarak Dışa Aktar

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

`TruecolorWithAlpha` ile `PngOptions` kullanmak, dışa aktarılan PNG’nin tam renk derinliğini ve PSD’den gelen şeffaflığı korumasını sağlar.

### Adım 5: Yeni Bir Pozlama Ayar Katmanı Ekle

Mevcut bir belgeye **yeni bir pozlama ayar katmanı** eklemeniz gerekiyorsa, aşağıdaki kodu kullanın:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

`addExposureAdjustmentLayer` yöntemi, belirtilen pozlama, offset ve gama değerleriyle yeni bir ayar katmanı oluşturur; ardından onu önceki gibi render edip dışa aktarabilirsiniz.

## Yaygın Sorunlar ve İpuçları

- **Katman bulunamadı** – PSD'nin gerçekten bir `ExposureLayer` içerdiğinden emin olun. `ClassCastException` almamak için gösterildiği gibi `instanceof ExposureLayer` kullanın.
- **Dosya yolu hataları** – Mutlak yollar kullanın veya `dataDir`'in bir dosya ayırıcı (`/` veya `\`) ile bittiğini doğrulayın.
- **Lisans istisnası** – Geçerli bir lisans olmadan çalıştırmak çıktıya bir filigran ekleyecektir. Lisansınızı kodun başında kaydedin (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## SSS

### Aspose.PSD for Java nedir?

Aspose.PSD for Java, Java kullanarak PSD dosyalarını programlı olarak oluşturmanıza, düzenlemenize ve dönüştürmenize olanak tanıyan bir kütüphanedir. Photoshop belgeleriyle çalışmak için kapsamlı işlevsellik sunar.

### Aspose.PSD for Java'ı diğer katman türlerini manipüle etmek için kullanabilir miyim?

Evet, Aspose.PSD for Java metin katmanları, ayar katmanları ve görüntü katmanları dahil olmak üzere çeşitli katman türlerini destekler ve PSD dosyalarında kapsamlı manipülasyon imkanı sağlar.

### Aspose.PSD for Java ile nasıl başlayabilirim?

Kütüphaneyi [web sitesinden](https://releases.aspose.com/psd/java/) indirebilir ve ayrıntılı kılavuzlar ve örnekler için [belgelere](https://reference.aspose.com/psd/java/) başvurabilirsiniz.

### Aspose.PSD for Java için ücretsiz deneme mevcut mu?

Evet, ücretsiz bir deneme mevcuttur. Bunu [buradan](https://releases.aspose.com/) indirebilirsiniz.

### Aspose.PSD for Java için destek nasıl alabilirim?

Destek için [Aspose destek forumunu](https://forum.aspose.com/c/psd/34) ziyaret edebilir, sorular sorabilir ve topluluktan yardım alabilirsiniz.

**Ek Sorular**

**S: Birden fazla PSD dosyasını toplu‑işlem yapabilir miyim?**  
C: Kesinlikle. Yükleme, düzenleme ve kaydetme mantığını, dosya yolu listesi üzerinde dönen bir döngüye sarın.

**S: Yeni bir pozlama katmanı eklediğimde kütüphane katman hiyerarşisini korur mu?**  
C: Evet. Yeni katman mevcut katmanların üzerine eklenir ve orijinal hiyerarşi korunur.

**S: PNG dışında hangi görüntü formatlarına dışa aktarabilirim?**  
C: Aspose.PSD, ilgili `*Options` sınıfları aracılığıyla JPEG, BMP, TIFF ve birkaç başka formatı destekler.

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}