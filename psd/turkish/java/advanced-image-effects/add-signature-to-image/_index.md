---
date: 2026-04-28
description: Aspose.PSD for Java ile bir kanvasa resim çizerek görüntüye imza eklemeyi
  öğrenin. Bu Java görüntü işleme öğreticisi, görüntüyü PNG olarak kaydetmeyi ve grafik
  üst üste bindirmeyi gösterir.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: Bir Görsele İmza Ekle
second_title: Aspose.PSD Java API
title: Görüntüye İmza Ekle – Aspose.PSD for Java ile Kanvasa Resim Çizin
url: /tr/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Görüntüye İmza Ekle – Aspose.PSD for Java ile Kanvasa Görüntü Çizme

## Giriş

El yazısı veya dijital **add signature to image** eklemek, sözleşmeler, faturalar veya kimlik doğrulaması gerektiren herhangi bir belge için yaygın bir gereksinimdir. Bu öğreticide, Aspose.PSD for Java'nın **draw image on canvas** yapmanıza ve imzayı sadece başka bir kaplama katmanı olarak ele almanıza nasıl izin verdiğini göreceksiniz. Temel resmi yükleme, imza dosyasını yükleme, bir grafik bağlamı başlatma, kaplamayı çizme ve sonunda **save image as PNG** adımlarını göstereceğiz. Sonunda, bir **java image processing** senaryosu için, ister imza, ister filigran, ister logo olsun, yeniden kullanılabilir bir desen elde edeceksiniz.

## Hızlı Yanıtlar
- **draw image on canvas** ne anlama geliyor? Bir `Graphics` sınıfı kullanarak bir görüntüyü diğerine render etmeyi ifade eder.  
- **Java'da imza nasıl eklenir?** İmza dosyasını bir `Image` olarak yükleyin ve `Graphics.drawImage` kullanın.  
- **Hangi Aspose.PSD sürümü gereklidir?** Herhangi bir son 24.x sürümü; kod en son kütüphane ile çalışır.  
- **Birden fazla görüntüyü üst üste ekleyebilir miyim?** Evet—farklı kaynaklarla `drawImage` çağrısını tekrarlayın.  
- **Lisans gerekli mi?** Geliştirme için deneme sürümü çalışır; üretim için ticari bir lisans gereklidir.

## “Draw Image on Canvas” Nedir?
Aspose.PSD terminolojisinde, bir kanvasa görüntü çizmek, bir `Image` nesnesini bir `Graphics` bağlamı kullanarak diğerine boyamak anlamına gelir. Bu işlem, filigran, logo veya imza ekleme gibi **overlay images java** tekniklerinin temelini oluşturur.

## İmza Üst Üste Eklemek İçin Aspose.PSD Neden Kullanılmalı?
- **Full PSD support** – katmanlar, maskeler ve şeffaflık ile çalışır.  
- **No native OS dependencies** – saf Java, sunucu‑tarafı işleme için mükemmel.  
- **High‑performance rendering** – büyük dosyalar ve karmaşık kompozisyonlar için optimize edilmiştir.  

## Önkoşullar
- Java Development Kit (JDK) 8 ve üzeri.  
- Aspose.PSD for Java JAR dosyasını projenizin classpath'ine ekleyin.  
- İki görüntü dosyası: bir temel resim (ör. `layers.psd`) ve bir imza grafiği (`sample.psd`).  

## Paketleri İçe Aktar

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: Birincil ve İkincil Görüntüleri Yükle

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Çizim sırasında beklenmeyen renk kaymalarını önlemek için her iki görüntüyü de aynı renk modunda (RGB) tutun.

## Adım 2: Grafik Başlatma (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` nesnesi, **draw image on canvas** yapmanızı sağlayan bir fırça gibi çalışır. Bunu birincil `Image` ile başlatmak, sonraki tüm çizim komutlarını bu kanvasa bağlar.

## Adım 3: Görüntüye İmza Ekle (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Bu kod parçasında, imzayı sağ‑alt köşeye konumlandırarak **overlay images java** yapıyoruz. Farklı bir konumlandırma gerekiyorsa `Point` değerlerini ayarlayın.

## Yaygın Sorunlar ve Çözümler
| Semptom | Neden | Çözüm |
|---------|-------|-----|
| İmza bozuk görünüyor | Kanvas ve imza arasındaki DPI uyumsuzluğu | Çizmeden önce `signature.resize` kullanın veya her iki dosyanın da aynı DPI'ye sahip olduğundan emin olun. |
| Çıktı dosyası çok büyük | Sıkıştırma olmadan kaydetme | Daha yüksek bir değerle `CompressionLevel` ayarlanmış yapılandırılmış bir `PngOptions` geçirin. |
| Hiçbir şey çizilmiyor | Graphics nesnesi serbest bırakılmadı | Çizimden sonra `graphics.dispose()` çağırın (isteğe bağlı, ancak iyi bir uygulamadır). |

## Gerçek Dünya Kullanımı İçin Ek İpuçları
- **Multiple signatures:** Farklı `Image` nesneleri ve koordinatlarla `graphics.drawImage`'i tekrarlayın.  
- **Opacity control:** İmzayı yarı şeffaf yapmak için çizmeden önce `graphics.setOpacity(float opacity)` kullanın.  
- **Rotating the signature:** Eğik bir imza gerektiğinde `graphics.rotateTransform(angle)` uygulayın.  
- **Saving to other formats:** JPEG, BMP vb. çıktılar için `PngOptions` yerine `JpegOptions` veya `BmpOptions` kullanın.

## Sıkça Sorulan Sorular

### Q1: Bir görüntüye birden fazla imza ekleyebilir miyim?
A1: Evet, farklı imza görüntüleriyle adımları tekrarlayarak birden fazla imza ekleyebilirsiniz.

### Q2: Aspose.PSD diğer görüntü formatlarını destekliyor mu?
A2: Evet, Aspose.PSD geniş bir görüntü formatı yelpazesini destekler, bu da görüntü işleme esnekliği sağlar.

### Q3: Aspose.PSD for Java kullanmak için lisans gerekli mi?
A3: Evet, Aspose.PSD kullanmak için geçerli bir lisansa ihtiyacınız var. Lisans detayları için [Purchase Aspose.PSD](https://purchase.aspose.com/buy) adresini ziyaret edin.

### Q4: Aspose.PSD için destek nasıl alabilirim?
A4: Topluluk desteği ve tartışmalar için [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

### Q5: Aspose.PSD for Java'yi satın almadan önce deneyebilir miyim?
A5: Evet, satın almadan önce özellikleri keşfetmek için bir [free trial](https://releases.aspose.com/) alabilirsiniz.

**Ek SSS**

**Q:** İmzanın opaklığını nasıl değiştiririm?  
**A:** `graphics.setOpacity(float opacity)` kullanın. Değerler 0.0 (şeffaf) ile 1.0 (opak) arasında değişir.

**Q:** İmzayı döndürmek mümkün mü?  
**A:** Evet—çizmeden önce `graphics.rotateTransform(angle)` ile bir dönüşüm matrisi uygulayın.

**Q:** İmzayı PNG yerine JPEG üzerine çizebilir miyim?  
**A:** Kesinlikle. `PngOptions` yerine `JpegOptions` kullanın ve istenen kalite seviyesini belirtin.

## Sonuç

Bu adımları izleyerek Aspose.PSD for Java ile **how to add signature to image** ve **drawing an image on canvas** yöntemini öğrendiniz. Aynı desen, filigranlar, logolar veya herhangi bir kaplama grafiği için genişletilebilir ve Java uygulamalarınıza güçlü **java image processing** yetenekleri kazandırır.

---

**Son Güncelleme:** 2026-04-28  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}