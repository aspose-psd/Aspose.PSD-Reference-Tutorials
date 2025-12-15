---
date: 2025-12-13
description: Aspose.PSD for Java ile sıkıştırılmamış görüntü akışlarını işleyerek
  PSD grafik nesnesi oluşturmayı ve PSD katmanlarını manipüle etmeyi öğrenin.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: PSD Grafik Nesnesi Oluştur – Java’da Sıkıştırılmamış Akış
url: /tr/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Grafik Nesnesi Oluşturma – Java’da Sıkıştırılmamış Akış

## Introduction
Java’da görüntü işleme dünyasına hoş geldiniz! Bu öğreticide **PSD grafik nesnesi oluşturacak** ve Aspose.PSD for Java kullanarak sıkıştırılmamış görüntü akışı nesnelerini yöneteceksiniz. İş akışlarınızı otomatikleştirmek isteyen bir grafik tasarımcı ya da uygulamalarınıza güçlü görüntü işleme yetenekleri entegre etmek isteyen bir yazılım geliştiricisi olsanız, bu rehber tam size göre. Gereksinimlerden sonuca kadar her adımı birlikte inceleyecek ve Aspose.PSD ile nasıl başlayacağınızı sağlam bir şekilde öğreneceksiniz.

## Quick Answers
- **“PSD grafik nesnesi oluşturmak” ne anlama geliyor?** Bir PSD dosyası için bir grafik bağlamı örnekleyerek içeriğini çizebilmenizi veya düzenleyebilmenizi sağlar.  
- **Hangi kütüphane sıkıştırılmamış akışları yönetir?** Aspose.PSD for Java, ham (sıkıştırılmamış) görüntü verileri için tam destek sunar.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim ortamı için ticari lisans gereklidir.  
- **Grafik nesnesini oluşturduktan sonra PSD katmanlarını manipüle edebilir miyim?** Evet – Graphics örneği sayesinde herhangi bir katmanda çizebilirsiniz.  

## Prerequisites
Kodlamaya başlamadan önce, bu yolculuğa başlamak için ihtiyacınız olan her şeye sahip olduğunuzdan emin olalım. İşte gereksinimler:

### Java Development Kit (JDK)
Makinenizde JDK yüklü olduğundan emin olun. Oracle’ın web sitesinden indirebilir ya da OpenJDK kullanabilirsiniz.

### Aspose.PSD for Java
Aspose.PSD kütüphanesini indirip kurmanız gerekir. Bu güçlü kütüphane, PSD dosyalarını kolayca manipüle etmenizi sağlar. En son sürümü [bu bağlantıdan](https://releases.aspose.com/psd/java/) alabilirsiniz.

### Integrated Development Environment (IDE)
Java kodunuzu yazıp test etmek için bir IDE kullanmanız önerilir. IntelliJ IDEA, Eclipse veya tercih ettiğiniz başka bir IDE’yi kullanabilirsiniz.

### Basic Understanding of Java
Java programlamasına aşina olmak süreci kolaylaştırır. Sınıflar, metodlar ve istisna yönetimi gibi temel konuları bildiğinizden emin olun.

Her şey hazır olduğunda, kolları sıvayalım ve heyecan verici bölüme—kodlamaya—geçelim!

## Import Packages
Aspose.PSD ile çalışmak için gerekli paketleri içe aktarmamız gerekiyor. Aşağıda PSD dosyalarını işlemek için genellikle ihtiyaç duyacağınız importları bulacaksınız.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Şimdi kodu sindirilebilir adımlara ayıralım, böylece kolayca takip edebileceksiniz. Projeyi kuracak, bir PSD dosyasını yükleyecek, manipüle edecek ve çıktıyı kaydedeceksiniz.

## Step 1: Define Your Document Directory
Kodlamaya başlamadan önce, PSD dosyanızın nerede bulunduğunu tanımlamanız gerekir. Bu, projeniz için sahneyi hazırlamaya eşdeğerdir.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini PSD dosyanızın (ör. layers.psd) bulunduğu gerçek yol ile değiştirin. Böylece dosyalarınızı sorunsuz bir şekilde bulabilirsiniz.

## Step 2: Create a Byte Array Output Stream
Değiştirilmiş görüntüyü bir şeyler yapmadan önce saklayabileceğiniz bir yere ihtiyacınız var. `ByteArrayOutputStream`, görüntü verisini kolayca yakalamanıza yardımcı olur.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Bu satır, `ms` adında yeni bir `ByteArrayOutputStream` nesnesi başlatır. Bu nesneyi sıkıştırılmamış görüntünüzü kaydetmek için kullanacaksınız.

## Step 3: Load the PSD File
Şimdi gerçek PSD dosyasını yükleme zamanı. İşte sihrin başladığı yer!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Bu satır, PSD dosyanızı bir `PsdImage` nesnesine yükler. Doğru yolu belirttiğinizden emin olun; aksi takdirde bir hata ortaya çıkar.

## Step 4: Set Up the PsdOptions for Saving
Görüntünüzü nasıl kaydetmek istediğinizi belirtmeniz gerekir — elbette sıkıştırılmamış olarak!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Burada bir `PsdOptions` nesnesi oluşturur ve sıkıştırma yöntemini `Raw` olarak ayarlarsınız. Bu yöntem, görüntünün tam kalitesini korur ve hiçbir sıkıştırma uygulanmadan kaydedilir.

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

Bu satır, Step 2’de oluşturduğunuz `ByteArrayOutputStream` içine, Step 4’te tanımladığınız seçenekleri kullanarak değiştirilmiş görüntüyü kaydeder. `save` metodu, ayarlarınıza göre görüntüyü doğru şekilde kodlar.

## Step 6: Reset the Output Stream
Kaydetme işleminden sonra, çıktı akışı son konumda kalır. Baştan okumak için sıfırlamanız gerekir.

```java
ms.reset();
```

Bu `reset` metodu, `ByteArrayOutputStream`’inizi tekrar baştan okumaya hazır hâle getirir. Tıpkı bir kaseti geri sarmak gibi!

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Burada, `ByteArrayOutputStream`’ten görüntüyü yeni bir `PsdImage` nesnesine geri yüklüyoruz. Böylece önceki çalışmanızın sonuçlarını kontrol edebilirsiniz.

## Step 8: Create Graphics Object
Görüntüyü daha da değiştirmek veya renderlamak için bir grafik nesnesi oluşturmanız gerekir.

```java
Graphics graphics = new Graphics(psdImage);
```

Bu satır, `psdImage` kullanarak bir `Graphics` nesnesi başlatır. Artık bu grafik nesnesiyle istediğiniz gibi çizebilir veya görüntüyü manipüle edebilirsiniz. Elinizde bir fırça var gibi düşünün!

## Manipulate PSD Layers with Graphics Object
Artık bir **Graphics** örneğiniz olduğuna göre, **PSD katmanlarını** manipüle edebilirsiniz — örneğin şekil çizebilir, metin ekleyebilir veya belirli bir katmana filtre uygulayabilirsiniz. Grafik bağlamı doğrudan piksel verisi üzerinde çalışır ve her katmanın görünümünü ince ayarlarla kontrol etmenizi sağlar.

## Common Issues and Solutions
- **Dosya yüklenirken NullPointerException** – `dataDir` yolunu iki kez kontrol edin ve dosya adının doğru olduğundan emin olun.  
- **Raw kullanmanıza rağmen sıkıştırılmış çıktı** – `saveOptions.setCompressionMethod(CompressionMethod.Raw);` satırının `save` metodundan önce çağrıldığını doğrulayın.  
- **Graphics nesnesi boş görünüyor** – doğru `PsdImage` örneği üzerinde çizim yaptığınızdan emin olun (yeni oluşturulanı değil, yüklediğiniz örneği kullanın, aksi takdirde istenmeyen sonuçlar alabilirsiniz).

## FAQ'lar
### Aspose.PSD nedir?
Aspose.PSD, geliştiricilerin Photoshop PSD dosyalarını ve ilişkili görüntü formatlarını programatik olarak oluşturmasına, düzenlemesine ve manipüle etmesine olanak tanıyan bir .NET kütüphanesidir.

### Aspose.PSD for Java’yı nasıl indirebilirim?
En son sürümü [release sayfasından](https://releases.aspose.com/psd/java/) indirebilirsiniz.

### Aspose.PSD için ücretsiz deneme sürümü var mı?
Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) temin edebilirsiniz.

### Aspose.PSD için destek alabilir miyim?
Kesinlikle! [Aspose destek forumunda](https://forum.aspose.com/c/psd/34) yardım isteyebilirsiniz.

### Aspose.PSD için geçici bir lisans nasıl alınır?
Başlamak için [geçici lisans sayfasını](https://purchase.aspose.com/temporary-license/) ziyaret edin.

## Frequently Asked Questions

**Q: Grafik nesnesini sadece belirli bir katmanı düzenlemek için kullanabilir miyim?**  
A: Evet. PSD’yi yükledikten sonra istediğiniz katmanı `psdImage.getLayers().get_Item(index)` ile seçip `Graphics` yapıcısına geçirebilirsiniz.

**Q: Raw sıkıştırma yöntemi dosya boyutunu etkiler mi?**  
A: Raw, piksel verisini sıkıştırma olmadan saklar; bu nedenle dosya boyutu sıkıştırılmış PSD’lerden daha büyük olur, ancak görüntü kalitesi değişmez.

**Q: Düzenlenmiş PSD’yi başka bir formata (ör. PNG) dışa aktarmak mümkün mü?**  
A: Kesinlikle. Düzenleme sonrası uygun `Image.save` aşırı yüklemesini `PngOptions` ile kullanabilirsiniz.

**Q: Hangi Java sürümü gereklidir?**  
A: Aspose.PSD for Java, JDK 8 ve üzeri sürümleri destekler.

**Q: İşlem sonrası kaynakları nasıl serbest bırakırım?**  
A: `psdImage.dispose()` metodunu çağırın ve herhangi bir akışı kapatarak yerel kaynakları serbest bırakın.

---  

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}