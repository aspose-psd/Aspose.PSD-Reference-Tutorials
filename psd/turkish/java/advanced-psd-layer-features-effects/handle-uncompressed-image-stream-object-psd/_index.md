---
date: 2026-02-17
description: Aspose.PSD for Java ile PSD'yi PNG'ye nasıl dışa aktaracağınızı ve sıkıştırılmamış
  görüntü akışlarını nasıl yöneteceğinizi öğrenin.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: PSD'yi PNG'ye Dışa Aktar – PSD Grafik Nesnesi Oluştur – Java'da Sıkıştırılmamış
  Akış
url: /tr/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dışa Aktarma – PSD Grafik Nesnesi Oluşturma – Java'da Sıkıştırılmamış Akış

## Introduction
Java'da görüntü işleme dünyasına hoş geldiniz! Bu öğreticide **bir PSD grafik nesnesi oluşturacak**, sıkıştırılmamış görüntü akışı nesnelerini yönetecek ve Aspose.PSD for Java kullanarak **PSD'yi PNG'ye dışa aktarmayı** öğreneceksiniz. İster iş akışlarınızı otomatikleştirmek isteyen bir grafik tasarımcı, ister uygulamalarınıza güçlü görüntü‑işleme yetenekleri entegre etmek isteyen bir yazılım geliştiricisi olun, bu rehber tam size göre. Gereksinimlerden son dışa aktarmaya kadar her adımı adım adım inceleyecek ve sürecin tamamını sağlam bir şekilde kavramanızı sağlayacağız.

## Quick Answers
- **“create PSD graphics object” ne anlama geliyor?** Bir PSD dosyası için bir grafik bağlamı örnekleyerek içeriğini çizebilir veya düzenleyebilirsiniz.  
- **Hangi kütüphane sıkıştırılmamış akışları yönetir?** Aspose.PSD for Java, ham (sıkıştırılmamış) görüntü verileri için tam destek sağlar.  
- **Düzenleme sonrası PSD'yi PNG'ye dışa aktarabilir miyim?** Evet—bir `Graphics` nesnesine sahip olduğunuzda PSD'yi render edip PNG olarak kaydedebilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir.  
- **Dışa aktarım kayıpsız mı?** PNG'ye dışa aktarma görüntü kalitesini korur; dosya boyutu JPEG'den büyük ama sıkıştırılmamış bir PSD'den küçüktür.  

## How to export PSD to PNG using Aspose.PSD for Java
**PSD'yi PNG'ye dışa aktarmanız** gerektiğinde tipik iş akışı şu şekildedir:

1. PSD dosyasını yükleyin (veya oluşturun).  
2. `Graphics` nesnesiyle istediğiniz çizim veya katman manipülasyonlarını yapın.  
3. `PngOptions` kullanarak ortaya çıkan görüntüyü kaydedin (aynı `Graphics` örneği yeniden kullanılabilir).  

Bu öğretici sıkıştırılmamış akışlarla çalışmaya odaklansa da, oluşturduğunuz aynı `Graphics` nesnesi daha sonra PSD'yi bir PNG dosyasına render etmek için yeniden kullanılabilir.

## Prerequisites
Kodlamaya başlamadan önce, bu yolculuğa başlamak için ihtiyacınız olan her şeye sahip olduğunuzdan emin olalım. İşte gereksinimler:

### Java Development Kit (JDK)
Makinenizde JDK yüklü olduğundan emin olun. Oracle'ın sitesinden indirebilir veya OpenJDK kullanabilirsiniz.

### Aspose.PSD for Java
Aspose.PSD kütüphanesini indirip kurmanız gerekir. Bu güçlü kütüphane, PSD dosyalarını kolayca manipüle etmenizi sağlar. En son sürümü [bu bağlantı](https://releases.aspose.com/psd/java/) üzerinden alabilirsiniz.

### Integrated Development Environment (IDE)
Java kodunuzu yazıp test etmek için bir IDE kullanmanız önerilir. IntelliJ IDEA, Eclipse veya tercih ettiğiniz başka bir IDE'yi kullanabilirsiniz.

### Basic Understanding of Java
Java programlamasına aşina olmak süreci kolaylaştırır. Sınıflar, metodlar ve istisna yönetimi gibi temel konuları bildiğinizden emin olun.

Her şey hazır olduğunda, kolları sıvayalım ve heyecan verici bölüme—kodlamaya—geçelim!

## Import Packages
İşe başlamak için Aspose.PSD ile çalışmak üzere gerekli paketleri içe aktarmamız gerekiyor. Aşağıda PSD dosyalarını işlemek için genellikle ihtiyaç duyacağınız import satırlarını bulacaksınız.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Şimdi kodu sindirilebilir adımlara ayıralım, böylece rahatça takip edebilirsiniz. Projeyi kuracak, PSD dosyasını yükleyecek, manipüle edecek ve çıktıyı kaydedeceğiz.

## Step 1: Define Your Document Directory
Kodlamaya başlamadan önce PSD dosyanızın bulunduğu yeri tanımlamanız gerekir. Bu, projeniz için sahneyi hazırlamaya eşdeğerdir.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini PSD dosyanızın (ör. layers.psd) bulunduğu gerçek yol ile değiştirin. Böylece dosyalarınızı sorunsuz bir şekilde bulabilirsiniz.

## Step 2: Create a Byte Array Output Stream
Değiştirilmiş görüntüyü bir şeyler yapmadan önce saklayacağınız bir yere ihtiyacınız var. `ByteArrayOutputStream` bu görüntü verisini kolayca yakalamanıza yardımcı olur.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Bu satır, `ms` adlı yeni bir `ByteArrayOutputStream` nesnesi başlatır. Bu nesneyi sıkıştırılmamış görüntünüzü kaydetmek için kullanacaksınız.

## Step 3: Load the PSD File
Şimdi gerçek PSD dosyasını yükleme zamanı. İşte sihrin başladığı yer!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Bu satır, PSD dosyanızı bir `PsdImage` nesnesine yükler. Doğru yolu verdiğinizden emin olun; aksi takdirde bir hata ortaya çıkar.

## Step 4: Set Up the PsdOptions for Saving
Görüntünüzü nasıl kaydetmek istediğinizi belirtmeniz gerekir — elbette sıkıştırılmamış olarak!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Burada bir `PsdOptions` nesnesi oluşturup sıkıştırma yöntemini `Raw` olarak ayarlıyorsunuz. Bu yöntem, görüntünün tam kalitesini korur ve sıkıştırma olmadan kaydedilir.

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

Bu satır, Step 2'de oluşturduğunuz `ByteArrayOutputStream` içine, Step 4'te tanımladığınız seçeneklerle değiştirilmiş görüntüyü kaydeder. `save` metodu, ayarlarınıza göre görüntüyü doğru şekilde kodlar.

## Step 6: Reset the Output Stream
Kaydetme işleminden sonra çıktı akışı son konumda olur. Baştan okumak için akışı sıfırlamanız gerekir.

```java
ms.reset();
```

Bu `reset` metodu, `ByteArrayOutputStream`'inizi tekrar baştan okumaya hazır hâle getirir. Bir kaseti geri sarmak gibi düşünün!

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Burada, `ByteArrayOutputStream`'den yeni bir `PsdImage` nesnesine görüntüyü tekrar yüklüyoruz. Böylece önceki çalışmanızın sonuçlarını kontrol edebilirsiniz.

## Step 8: Create Graphics Object
Görüntüyü daha da değiştirmek veya render etmek için bir graphics nesnesi oluşturmanız gerekir.

```java
Graphics graphics = new Graphics(psdImage);
```

Bu satır, `psdImage` kullanarak bir `Graphics` nesnesi başlatır. Artık bu graphics nesnesiyle istediğiniz gibi çizebilir veya görüntüyü manipüle edebilirsiniz. Elinizde bir fırça gibi!

## Manipulate PSD Layers with Graphics Object
Artık bir **Graphics** örneğine sahip olduğunuz için **PSD katmanlarını manipüle** edebilirsiniz—örneğin şekil çizebilir, metin ekleyebilir veya belirli bir katmana filtre uygulayabilirsiniz. Grafik bağlamı doğrudan piksel verisi üzerinde çalışır ve her katmanın görünümünü ince ayarlarla kontrol etmenizi sağlar.

## Common Issues and Solutions
- **NullPointerException dosya yüklenirken** – `dataDir` yolunu iki kez kontrol edin ve dosya adının doğru olduğundan emin olun.  
- **Raw kullanmanıza rağmen sıkıştırılmış çıktı** – `saveOptions.setCompressionMethod(CompressionMethod.Raw);` satırının `save` metodundan önce çağrıldığını doğrulayın.  
- **Graphics nesnesi boş görünüyor** – doğru `PsdImage` örneği üzerinde çizim yaptığınızdan emin olun (yeni oluşturulanı değil, yüklediğiniz örneği kullanın, aksi takdirde istenmeyen sonuçlar alabilirsiniz).

## FAQ's
### What is Aspose.PSD?
Aspose.PSD, geliştiricilerin Photoshop PSD dosyalarını ve ilişkili görüntü formatlarını programatik olarak oluşturmasına, düzenlemesine ve manipüle etmesine olanak tanıyan bir .NET kütüphanesidir.

### How can I download Aspose.PSD for Java?
[release page](https://releases.aspose.com/psd/java/) üzerinden indirebilirsiniz.

### Is there a free trial for Aspose.PSD?
Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) temin edebilirsiniz.

### Can I get support for Aspose.PSD?
Kesinlikle! [Aspose destek forumu](https://forum.aspose.com/c/psd/34) üzerinden yardım alabilirsiniz.

### How can I obtain a temporary license for Aspose.PSD?
Başlamak için [temporary license page](https://purchase.aspose.com/temporary-license/) adresini ziyaret edin.

## Frequently Asked Questions

**Q: Can I use the graphics object to edit only one specific layer?**  
A: Evet. PSD'yi yükledikten sonra `psdImage.getLayers().get_Item(index)` ile istediğiniz katmanı seçip `Graphics` yapıcısına geçirebilirsiniz.

**Q: Does the Raw compression method affect file size?**  
A: Raw, piksel verisini sıkıştırma olmadan saklar; bu yüzden dosya boyutu sıkıştırılmış PSD'lerden daha büyük olur, ancak görüntü kalitesi değişmez.

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: Kesinlikle. Düzenlemeden sonra uygun `Image.save` aşırı yüklemesiyle `PngOptions` kullanarak **PSD'yi PNG'ye dışa aktarabilirsiniz**.

**Q: What Java version is required?**  
A: Aspose.PSD for Java, JDK 8 ve üzeri sürümleri destekler.

**Q: How do I release resources after processing?**  
A: `psdImage.dispose()` metodunu çağırın ve herhangi bir akışı kapatarak yerel kaynakları serbest bırakın.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}