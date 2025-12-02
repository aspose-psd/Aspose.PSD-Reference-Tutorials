---
date: 2025-12-02
description: Aspose.PSD kullanarak Java’da tuval üzerine resim çizmeyi ve bir imza
  eklemeyi öğrenin. Bu adım adım Java görüntü işleme öğreticisini izleyin ve sonucu
  PNG olarak kaydedin.
language: tr
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Tuval Üzerine Görüntü Çizin – Aspose.PSD for Java ile İmza Ekleyin
url: /java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Canvas Üzerine Görüntü Çiz – Aspose.PSD for Java ile İmza Ekle

## Giriş

Bir resme el yazısı veya dijital imza eklemek, sözleşmeler, faturalar veya kimliğin kanıtlanması gereken herhangi bir belge için sık bir gereksinimdir. **Aspose.PSD for Java** ile **draw image on canvas** yapabilir ve imzayı sadece başka bir üst katman olarak ele alabilirsiniz. Bu **java image processing tutorial** içinde tüm iş akışını adım adım inceleyeceğiz—temel resmi ve imza dosyasını yüklemekten, grafik başlatmaya, üst katmanı çizmeye ve sonunda **save image png java**‑stilinde kaydetmeye kadar.

## Hızlı Yanıtlar
- **draw image on canvas ne anlama geliyor?** `Graphics` sınıfını kullanarak bir görüntüyü diğerinin üzerine render etmeyi ifade eder.  
- **Java’da imza nasıl eklenir?** İmza dosyasını bir `Image` olarak yükleyin ve `Graphics.drawImage` kullanın.  
- **Hangi Aspose.PSD sürümü gerekiyor?** Herhangi bir son 24.x sürümü; kod en yeni kütüphane ile çalışır.  
- **Birden fazla görüntüyü üst üste ekleyebilir miyim?** Evet—farklı kaynaklarla `drawImage` çağrısını tekrarlayın.  
- **Lisans gerekli mi?** Deneme sürümü geliştirme için çalışır; üretim için ticari lisans gerekir.

## “Draw Image on Canvas” Nedir?
Aspose.PSD terminolojisinde, bir kanvas üzerine görüntü çizmek, bir `Image` nesnesini bir `Graphics` bağlamı kullanarak diğerine boyamak anlamına gelir. Bu işlem, **overlay images java** gibi filigran, logo veya imza ekleme tekniklerinin temelini oluşturur.

## Neden Aspose.PSD'yi İmza Üst Üste Eklemek İçin Kullanmalısınız?
- **Tam PSD desteği** – katmanlar, maskeler ve şeffaflık ile çalışır.  
- **Yerel OS bağımlılığı yok** – saf Java, sunucu tarafı işleme için mükemmel.  
- **Yüksek performanslı render** – büyük dosyalar ve karmaşık kompozisyonlar için optimize edilmiştir.  

## Önkoşullar
- Java Development Kit (JDK) 8 veya üzeri.  
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

> **Pro ipucu:** Çizim sırasında beklenmeyen renk kaymalarını önlemek için her iki görüntüyü de aynı renk modunda (RGB) tutun.

## Adım 2: Grafik Başlat (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` nesnesi, **draw image on canvas** yapmanızı sağlayan bir fırça gibi davranır. Bunu birincil `Image` ile başlatmak, sonraki tüm çizim komutlarını bu kanvasa bağlar.

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

| Belirti | Neden | Çözüm |
|---------|-------|-------|
| İmza bozulmuş görünüyor | Kanvas ve imza arasında DPI uyumsuzluğu | `signature.resize` kullanarak çizmeden önce yeniden boyutlandırın veya her iki dosyanın da aynı DPI'ye sahip olduğundan emin olun. |
| Çıktı dosyası çok büyük | Sıkıştırma olmadan kaydediliyor | `CompressionLevel` daha yüksek bir değere ayarlanmış yapılandırılmış bir `PngOptions` geçirin. |
| Hiçbir şey çizilmiyor | Graphics nesnesi serbest bırakılmadı | Çizimden sonra `graphics.dispose()` çağırın (isteğe bağlı, ancak iyi bir uygulamadır). |

## Sonuç

Bu adımları izleyerek **draw image on canvas** nasıl yapılacağını ve Aspose.PSD for Java kullanarak sorunsuz bir şekilde **imza eklemeyi** öğrendiniz. Bu teknik, filigran, logo veya herhangi bir üst katman grafiğine genişletilebilir ve Java uygulamalarınıza güçlü **java image processing** yetenekleri kazandırır.

## SSS

### S1: Bir görüntüye birden fazla imza ekleyebilir miyim?

Evet, farklı imza görüntüleriyle adımları tekrarlayarak birden fazla imza ekleyebilirsiniz.

### S2: Aspose.PSD diğer görüntü formatlarını destekliyor mu?

Evet, Aspose.PSD geniş bir görüntü formatı yelpazesini destekler, bu da görüntü işleme esnekliği sağlar.

### S3: Aspose.PSD for Java kullanmak için lisans gerekli mi?

Evet, Aspose.PSD kullanmak için geçerli bir lisansa ihtiyacınız var. Lisans detayları için [Purchase Aspose.PSD](https://purchase.aspose.com/buy) adresini ziyaret edin.

### S4: Aspose.PSD için destek nasıl alabilirim?

Topluluk desteği ve tartışmalar için [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edin.

### S5: Aspose.PSD for Java'ı satın almadan deneyebilir miyim?

Evet, satın almadan önce özellikleri keşfetmek için bir [ücretsiz deneme](https://releases.aspose.com/) alabilirsiniz.

## Ek Sık Sorulan Sorular

**S: İmzanın opaklığını nasıl değiştiririm?**  
C: `drawImage` çağırmadan önce `graphics.setOpacity(float opacity)` kullanın. Değerler 0.0 (şeffaf) ile 1.0 (opak) arasında değişir.

**S: İmza döndürülebilir mi?**  
C: Evet—çizmeden önce `graphics.rotateTransform(angle)` ile bir dönüşüm matrisi uygulayın.

**S: İmzayı PNG yerine JPEG üzerine çizebilir miyim?**  
C: Kesinlikle. `PngOptions` yerine `JpegOptions` kullanın ve istediğiniz kalite seviyesini belirtin.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}