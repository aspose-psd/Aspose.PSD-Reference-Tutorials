---
date: 2025-12-27
description: Aspose.PSD for Java kullanarak PSD dosyalarında kırmızı dikdörtgen ve
  diğer şekilleri nasıl çizeceğinizi öğrenin. Bu adım adım rehber, belge oluşturmayı,
  katman eklemeyi ve kod örnekleriyle çizmeyi kapsar.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile Kırmızı Dikdörtgen Çizin
url: /tr/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Kırmızı Dikdörtgen Çizme

## Giriiş

Aspose.PSD for Java kullanarak **kırmızı dikdörtgen çizmeyi** adım adım gösteren bu kılavuza hoş geldiniz! Bu öğreticide yeni bir PSD belgesi oluşturmayı, bir katman eklemeyi ve özel renklerle sunacağımız çizmeyi anlatacağız. Grafik varlıklarını otomatik olarak yükselten ya da bir tasarım aracının arka gücünü geliştiren olun, bu öğretici boyutta temel yapı taşlarını sunar.

## Hızlı Yanıtlar
- **PSD dosyası oluşturmak için birincil sınıf nedir?** `PsdImage`
- **Bir koridorun arka planı temizleyen yöntem hangisidir?** `Graphics.clear(Color)`
- **Kırmızı bir dikdörtgen nasıl çizilir?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))'
- **Geliştirme için lisansa ihtiyacı var mı?** Ücretsiz deneme sürümü testi için çalışır; üretim için lisans gereklidir.
- **Aynı API ile mevcut PSD'yi manipüle edebilir miyim?** Evet, Aspose.PSD tam PSD düzenlemeyi desteklemesi.

## PSD dosyasında kırmızı bir dikdörtgen çizmek nedir?
Kırmızı bir dikdörtgen çizmek, `Graphics` nesnesini kullanarak bir PSD depolamanın ayrıntılı bir bölüme kırmızı renk ile doldurulmuş veya kenarlığı düzenleme bir düzenli biçim oluşturmak gelir. Bu işlemi, alanlarını vurgulamak, yer güçlendirmek veya basit parçaları değiştirmek için programlı olarak yaygın olarak kullanılır.

## PSD dosyalarını değiştirmek için neden Aspose.PSD for Java kullanmalısınız?
Aspose.PSD, Photoshop olmadan yüklü Photoshop PSD kartlarını okumanıza, düzenlemenize ve yazmanıza olanak sağlayan saf Java API'si sunar. Katman yönetimi, renk değişikliği ve vektörlerin gösterimini sağlamak; bu da sunucu tarafı görüntü işleme, otomatik varlık çizgileri ve özel grafik üretimi için sağlanır.

## Önkoşullar

- Makinenizde Java Development Kit (JDK) yüklü olmalıdır.
- Java kütüphanesi için Aspose.PSD. Bunu [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) adresinden indirebilirsiniz.

## Paketleri İçe Aktar

Başlamak için gerekli sınıfları Java projenize aktarın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Adım 1: Yeni Bir Belge Oluşturun

İlk olarak, istenen tuval boyutuyla yeni bir PSD belgesi oluşturun. Bu belge, üzerinde çizeceğimiz katmanı barındıracaktır.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Adım 2: Katman Ekle

Sonra, görüntünün tam genişlik ve yüksekliğini kapsayan yeni bir boş katman ekleyin. Katmanlar, çizim işlemlerini ayırmak için gereklidir.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Adım 3: Şekiller Çizin

`Grafik` sınıfını kullanarak katmanların piksel kümelerini manipüle eder. Burada arka plan temizleme ve farklı yapılandırmalar çizme örneklerini gösteren üç örnek bulunmaktadır.

### Katman Rengini Temizle (arka planı sarıya ayarla)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Kırmızı Bir Dikdörtgen Çizin (birincil odak)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Mavi Bir Dikdörtgen Çizin (ek örnek)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Adım 4: Değişiklikleri Kaydet

Son olarak, değiştirilen PSD görüntüsünü diske yazın. Dosya yeni katmanı ve çizilen şekilleri içerecektir.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Yaygın Sorunlar ve Çözümler

- **Katman çizimden sonra görünmüyorsa:** Katmanın `Graphics` nesnesi oluşturulmadan **önce** görüntüye eklendiğinden emin olun.
- **Renkler yanlış görünüyor:** `Color.getRed()` (veya diğer statik izleme) kullanımını, aralık dışı özel RGB değerlerini kullanmadığınızı doğrulayın.
- **Dosya kaydedilmiyor:** `outputDir` yolunun var olup olmadığını ve kayıt yazmaya izinlerine sahip olup olmadığını kontrol edin.

## Sıkça Sorulan Sorular

### S1: Mevcut PSD dosyalarını değiştirmek için Aspose.PSD for Java'yı kullanabilir miyim?

C1: Evet, Aspose.PSD for Java mevcut PSD'yi düzenlemek ve düzenlemek için kapsamlı bir işlevsellik sunar.

### S2: Aspose.PSD for Java desteğini nerede bulabilirim?

C2: Destekle ilgili dağıtmak için [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) adresini ziyaret edebilirsiniz.

### S3: Aspose.PSD for Java'nın ücretsiz deneme sürümü mevcut mu?

C3: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### S4: Aspose.PSD for Java lisansını nasıl satın alabilirim?

A4: Lisansı [Aspose.PSD Satın Alma Sayfası](https://purchase.aspose.com/buy) üzerinden satın alabilirsiniz.

### S5: Aspose.PSD for Java için geçici lisanslar mevcut mu?

C5: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

## Ek Sıkça Sorulan Sorular

**S: Dikdörtgen dışında başka sözler çizebilir miyim?**
C: Evet, `Graphics` sınıfı elips, çizgi ve özel yolların çizilmeyi de desteklemesi.

**S: Çizilenin şeffaflığı destekleniyor mu?**
C:kesinlikle; alfa şeffaflığı seçmek için ARGB renkli `SolidBrush` kullanabilirsiniz.

**S: Bir güvenliğin opaklığını düzenlemek mümkün mü?**
C: Evet, her `Layer` nesnesinin 0 ile 255 arasında bir değer alan `setOpacity` yöntemi vardır.

**S: Yeni bir dosya oluşturmak yerine mevcut bir PSD dosyalarını nasıl yüklersiniz?**
C: Katmanları manipüle etmeden önce `PsdImage image = (PsdImage)Image.load("path/to/file.psd");`yi kullanın.

## Çözüm

Artık Aspose.PSD for Java kullanarak bir PSD dozunda **kırmızı dikdörtgen** ve diğer temel bilgileri nasıl çizeceğinizi bilgilerinize ekleyin. Bir belge oluşturup, bir katman ekleyerek, arka planını temizleyerek ve `Graphics` API'siyle çizim yaparak birçok grafik‑tasarım görevini otomatikleştirebilirsiniz. Farklı fırçalar, katman oluşturma ve dosya formatlarıyla deneyler yaparak daha fazla büyüme.

---

**Son Güncelleme:** 2025-12-27
**Test Edilenler:** Aspose.PSD for Java 24.12 (bu yazının yazıldığı tarihteki en son sürüm)
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}