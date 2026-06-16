---
date: 2026-04-03
description: Aspose.PSD for Java kullanarak bir çizgi efekti ve renk doldurmasıyla
  PSD'yi PNG olarak kaydetmeyi öğrenin. Bu adım adım rehber, PSD'yi hızlıca PNG'ye
  dışa aktarmayı gösterir.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: PSD'yi Çizgi Efektiyle PNG Olarak Kaydet – Java
second_title: Aspose.PSD Java API
title: PSD'yi Çizgi Efektiyle PNG Olarak Kaydet – Java
url: /tr/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG Olarak Kaydet, Çizgi Efekti ve Renk Doldurması – Java

## Giriş

Bu rehberde, Aspose.PSD for Java kullanarak **PSD'yi PNG olarak kaydet** ve renk doldurmasıyla bir çizgi efekti uygulamayı öğreneceksiniz. İster deneyimli bir geliştirici olun, ister yeni başlayın, bu adım adım öğretici işi kolayca halletmenizi sağlayacak. Ortamınızı kurmaktan son görüntüyü dışa aktarmaya kadar her şeyi ele alacağız, böylece kendi projelerinizde hızlıca **PSD'yi PNG'ye dışa aktar**abilirsiniz.

## Hızlı Yanıtlar
- **Bu öğretici neyi başarmak için?** Özelleştirilebilir bir çizgi efekti uyguladıktan sonra bir PSD dosyasını PNG olarak kaydetmeyi gösterir.  
- **Hangi kütüphane kullanılıyor?** Aspose.PSD for Java.  
- **Lisans gerekli mi?** Test için ücretsiz deneme sürümü çalışır; üretim için bir lisans gereklidir.  
- **Çizgi rengini değiştirebilir miyim?** Evet – `ColorFillSettings` aracılığıyla herhangi bir renk ayarlayabilirsiniz.  
- **Toplu işleme mümkün mü?** Kesinlikle – kodu bir döngü içinde sararak birden fazla PSD dosyasını işleyebilirsiniz.

## “PSD'yi PNG Olarak Kaydet” ne demektir?
Bir PSD'yi PNG olarak kaydetmek, Photoshop'un yerel katmanlı dosyasını, görsel bütünlüğü koruyarak düz, web‑uyumlu bir görüntü formatına dönüştürmek anlamına gelir. Bu, PSD içeriğini web sitelerinde, mobil uygulamalarda veya doğrudan PSD dosyalarını desteklemeyen herhangi bir platformda göstermeniz gerektiğinde faydalıdır.

## Neden renk doldurmalı bir çizgi efekti uygulamalısınız?
Bir çizgi, katman içeriğinin etrafına net bir kenarlık ekler ve grafiklerin karmaşık arka planlarda öne çıkmasını sağlar. Bunu özel bir doldurma rengiyle birleştirerek görüntülere marka ekleyebilir, UI öğelerini vurgulayabilir veya Photoshop'tan çıkmadan göz alıcı küçük resimler oluşturabilirsiniz.

## Ön Koşullar

1. **Java Development Kit (JDK) 8+** – `java`'nın PATH'inizde olduğundan emin olun.  
2. **Aspose.PSD for Java** – [web sitesinden](https://releases.aspose.com/psd/java/) indirin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  
4. **Örnek PSD** – zaten bir çizgi efekti içeren bir dosya (veya Photoshop'ta ekleyin).  
5. **Temel Java bilgisi** – birkaç satır kod yazacaksınız, ancak ileri seviye bir şey değil.

Bu ön koşullar hazır olduğunda, kodlamaya başlayabiliriz.

## Paketleri İçe Aktar

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Bu içe aktarmalar, bir PSD'yi yüklemek, çizgisini değiştirmek ve hem PSD hem de PNG çıktıları kaydetmek için gereken tüm sınıfları getirir.

## Çizgi Efektiyle PSD'yi PNG Olarak Kaydetme

### Adım 1: PSD Dosyasını Yükle

İlk olarak, kaynak PSD'nizin bulunduğu klasöre işaret edin.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini makinenizdeki gerçek yol ile değiştirin.

Şimdi, mevcut efekt kaynaklarını koruyarak dosyayı yükleyin:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Adım 2: Çizgi Rengini Ayarla (ve isteğe bağlı olarak genişliği özelleştir)

Aşağıdaki döngü her katmanı dolaşır, ilk `StrokeEffect`'i alır ve doldurma rengini değiştirir. **Çizgi genişliğini özelleştirmeniz** gerekiyorsa, `StrokeEffect` nesnesinde `setWidth` veya `setPosition` metodlarını da ayarlayabilirsiniz.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Pro ipucu:** `Color.getDeepPink()` sadece bir örnek. Özel RGB değerleri için `new Color(r, g, b)` kullanın.

### Adım 3: Değiştirilmiş PSD'yi Kaydet (isteğe bağlı)

Güncellenmiş çizgiyle bir PSD sürümünü tutmak istiyorsanız, şu şekilde kaydedin:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Adım 4: Görüntüyü PNG Olarak Dışa Aktar (temel “PSD'yi PNG Olarak Kaydet” adımı)

Son olarak, düzenlenmiş PSD'yi web kullanımı için hazır bir PNG dosyasına dönüştürün:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG, daha önce ayarladığınız derin pembe çizgiyi korur ve `TruecolorWithAlpha` seçeneği şeffaflığın korunmasını sağlar.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | Katmanda hiçbir efekt yok veya ilk efekt bir `StrokeEffect` değil. | Katmanın gerçekten bir çizgi içerdiğini doğrulayın veya doğru türü bulmak için `getEffects()` üzerinden döngü yapın. |
| **Renk değişmiyor** | Ayarların bir kopyasını düzenliyor olabilirsiniz, orijinali değil. | `effect.getFillSettings()`'den doğrudan `ColorFillSettings`'e cast ettiğinizden emin olun. |
| **PNG boş görünüyor** | PSD, katmanı rasterleştirmeden yüklendi. | Tüm değişikliklerden sonra `im.save(..., new PngOptions())` çağırın; değişikliklerden önce orijinal `im`'i kaydetmekten kaçının. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java kullanarak tek bir katmana birden fazla efekt uygulayabilir miyim?**  
C: Evet, katmanın karıştırma seçeneklerine erişebilir ve gölgeler, parlamalar ve çizgiler dahil olmak üzere ihtiyaç duyulan kadar efekt ekleyebilirsiniz.

**S: Bir grup PSD dosyası için süreci otomatikleştirmek mümkün mü?**  
C: Kesinlikle. Yükleme, efekt uygulama ve kaydetme mantığını bir dizindeki dosyalar üzerinde yineleyen bir `for‑each` döngüsü içinde sarabilirsiniz.

**S: PSD dosyasında yapılan değişiklikleri nasıl geri alabilirim?**  
C: Herhangi bir değişikliği kaydetmeden önce orijinal dosyayı yeniden yükleyin; Aspose.PSD bir geri alma yığını sağlamaz.

**S: Çizgi genişliğini ve konumunu özelleştirebilir miyim?**  
C: Evet. Kalınlığı ve konumu (iç, dış veya ortalanmış) kontrol etmek için `effect.setWidth(float)` ve `effect.setPosition(StrokeEffect.Position)` kullanın.

**S: Aspose.PSD for Java kütüphanesi ücretsiz mi?**  
C: Değerlendirme için ücretsiz bir deneme sürümü mevcuttur. Tam işlevsellik bir lisans satın almayı gerektirir. Ayrıntılar için [satın alma seçeneklerine](https://purchase.aspose.com/buy) bakın.

---

**Son Güncelleme:** 2026-04-03  
**Test Edilen Versiyon:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}