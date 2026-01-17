---
date: 2026-01-17
description: Aspose.PSD kullanarak Java’da bir Bezier eğrisi görüntüsü oluşturmayı
  öğrenin. Bu adım adım rehber, bezier eğrisi Java tekniklerini çizmeyi, kalem kalınlığı
  ayarlarını ve sonucu dışa aktarmayı kapsar.
linktitle: How to Create Bezier Curve Image in Java
second_title: Aspose.PSD Java API
title: Java'da Bezier Eğrisi Görüntüsü Nasıl Oluşturulur
url: /tr/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Bezier Eğrisi Görüntüsü Nasıl Oluşturulur

## Introduction
Java masaüstü veya sunucu‑tarafı uygulamanız için **Bezier eğrisi görüntüsü oluşturmanız** gerektiğinde, Aspose.PSD for Java işi zahmetsiz hâle getirir. Bu öğreticide pürüzsüz bir bezier eğrisi çizmeyi, kalem kalınlığını özelleştirmeyi ve sonucu bitmap olarak kaydetmeyi adım adım inceleyeceğiz. Sonunda `drawBezier()` metoduna hâkim olacak ve vektör‑stil grafiklerini herhangi bir Java projesine entegre etmeye hazır olacaksınız.

## Quick Answers
- **Java'da eğri çizmek için en iyi kütüphane hangisidir?** Aspose.PSD for Java tam özellikli bir grafik API'si sunar.  
- **Temel bir Bezier eğrisi görüntüsü oluşturmak ne kadar sürer?** SDK kurulduktan sonra genellikle 10 dakikadan az sürer.  
- **Hangi görüntü formatları dışa aktarım için desteklenir?** BMP, PNG, JPEG, TIFF ve daha fazlası.  
- **Eğrinin kalem kalınlığını değiştirebilir miyim?** Evet – `Pen` yapıcısı ihtiyacınız olan herhangi bir genişliği belirlemenize izin verir.  
- **Üretim ortamında lisansa ihtiyacım var mı?** Değerlendirme dışı dağıtımlar için ticari bir lisans gereklidir.

## What is “create bezier curve image”?
Bezier eğrisi görüntüsü oluşturmak, matematiksel olarak tanımlanmış bir eğriyi içeren bir raster resim üretmek anlamına gelir. Eğri, bir başlangıç noktası, iki kontrol noktası ve bir bitiş noktasıyla tanımlanır; bu sayede herhangi bir boyutta güzel görünen, pürüzsüz ve ölçeklenebilir şekiller elde edebilirsiniz.

## Why use Aspose.PSD for Java?
- **Zengin grafik ilkelileri** – düşük‑seviye piksel manipülasyonu ile uğraşmadan çizgiler, şekiller ve eğriler çizin.  
- **Çapraz‑platform** – Java'yı destekleyen her işletim sisteminde çalışır.  
- **Yüksek çözünürlük desteği** – aşırı bellek tüketimi olmadan büyük tuvalleri işleyin.  
- **Kolay dışa aktarım** – tek bir kod satırıyla BMP, PNG, JPEG, TIFF arasında geçiş yapın.

## Prerequisites
Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Java Development Kit (JDK)** – herhangi bir güncel sürüm (8 veya üzeri).  
2. **Aspose.PSD for Java JAR** – [buradan](https://releases.aspose.com/psd/java/) indirin ve projenizin classpath'ine ekleyin.  
3. **IDE** – Eclipse, IntelliJ IDEA veya tercih ettiğiniz herhangi bir editör, JDK ile yapılandırılmış.

## Import Packages
Uygulamaya geçmeden önce gerekli Aspose.PSD sınıflarını içe aktarın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Step‑by‑Step Guide

### Step 1: Create an Image Instance
İlk olarak, bellekte bir PSD görüntüsü temsil eden `PsdImage` sınıfının bir örneğini oluşturmanız gerekir.

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```

*Explanation*: `PsdImage`, **100 × 100 piksel** genişlik ve yükseklikte başlatılır – daha yüksek çözünürlük için bu değerleri artırabilirsiniz.

### Step 2: Initialize Graphics Context
Sonra, görüntü üzerinde çizim işlemleri yapmak için `Graphics` sınıfının bir örneğini başlatın.

```java
Graphics graphics = new Graphics(image);
```

*Explanation*: `Graphics` nesnesi, az önce oluşturduğumuz `image` ile çizim komutlarını ilişkilendirir.

### Step 3: Clear the Graphics Surface
Belirli bir arka plan rengiyle grafik yüzeyini temizleyin; burada `Color.getYellow()` kullanılıyor.

```java
graphics.clear(Color.getYellow());
```

*Explanation*: Parlak sarı bir arka plan ayarlanır, böylece siyah bezier eğrisi daha belirgin hâle gelir.

### Step 4: Initialize Pen for Drawing
Eğrinin nasıl çizileceğini tanımlamak için renk ve genişlik gibi özelliklere sahip bir `Pen` nesnesi oluşturun.

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```

*Explanation*: Kalem siyah ve **3 piksel genişliğinde** – kalemi daha kalın ya da ince yapmak için genişliği (`java graphics pen width`) ayarlayabilirsiniz.

### Step 5: Define Bezier Curve Parameters
Bezier eğrisi için kontrol ve bitiş noktalarını belirtin.

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```

*Explanation*:  
- `startX`, `startY` – eğrinin başlangıç noktası.  
- `controlX1`, `controlY1` – birinci kontrol noktası.  
- `controlX2`, `controlY2` – ikinci kontrol noktası.  
- `endX`, `endY` – bitiş noktası.

### Step 6: Draw the Bezier Curve
Önceden tanımlanan `Pen` ve kontrol noktalarını kullanarak `drawBezier()` metoduyla bezier eğrisini çizin.

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```

*Explanation*: Bu tek çağrı, sağladığınız kontrol noktalarını izleyen pürüzsüz bir **draw bezier curve java** çizgisi oluşturur.

### Step 7: Save the Image
Çizilen görüntüyü BMP dosya formatında kaydedin.

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

*Explanation*: `BmpOptions` nesnesi, Aspose.PSD'nin dosyayı BMP olarak yazmasını sağlar. Farklı bir format gerekiyorsa `PngOptions`, `JpegOptions` vb. ile değiştirin.

## Common Issues & Solutions
- **Eğri düz görünüyor** – Kontrol noktası koordinatlarını tekrar kontrol edin; başlangıç/bitiş noktalarıyla aynı doğrultuda olmamalıdır.  
- **Görüntü boş** – Çizimden önce `graphics.clear()` çağrıldığından ve `Pen` renginin arka planla kontrast oluşturduğundan emin olun.  
- **Büyük tuvallerde OutOfMemoryError** – JVM yığın boyutunu (`-Xmx`) artırın veya döşeli (tiled) görüntülerle çalışın.

## FAQ's
### Can I draw multiple Bezier curves in the same image?
Evet, bir döngü içinde işlemi tekrarlayarak, kontrol ve bitiş noktalarını gerektiği gibi değiştirerek birden fazla eğri çizebilirsiniz.

### How can I change the color of the Bezier curve?
`drawBezier()` çağrısından önce `Pen` nesnesinin renk özelliğini (`Color.getBlack()` örneğinde) değiştirin.

### Is Aspose.PSD for Java suitable for high-resolution images?
Evet, Aspose.PSD for Java yüksek çözünürlüklü görüntüler için verimli bellek yönetimi sağlar.

### Can I export the image to formats other than BMP?
Evet, Aspose.PSD for Java PNG, JPEG, TIFF vb. çeşitli formatlarda dışa aktarmayı destekler.

### Where can I find more examples and documentation?
Kapsamlı kılavuzlar ve kod örnekleri için [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) adresini ziyaret edin.

## Conclusion
Bu **bezier curve tutorial java** rehberini izleyerek, Aspose.PSD for Java kullanarak **Bezier eğrisi görüntüsü oluşturmayı** öğrendiniz. Farklı kontrol noktaları, kalem renkleri ve çizgi kalınlıklarıyla deneyler yaparak Java uygulamalarınızda çeşitli sanatsal efektler elde edebilirsiniz.

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}