---
date: 2026-03-28
description: Aspose.PSD for Java kullanarak exposure katmanı oluşturmayı öğrenin –
  PSD dosyalarında exposure ayar katmanlarını ekleme, düzenleme ve kaydetme konusunda
  adım adım rehber.
linktitle: How to create exposure layer java with Aspose.PSD
second_title: Aspose.PSD Java API
title: Aspose.PSD ile Java'da pozlama katmanı nasıl oluşturulur
url: /tr/java/psd-image-modification-conversion/manage-exposure-adjustment-layer-psd/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile PSD'de Pozlama Ayar Katmanını Yönetme

## Giriş
When it comes to working with Photoshop files programmatically, learning how to **create exposure layer java** using Aspose.PSD is a real game‑changer. The Exposure Adjustment Layer lets you fine‑tune brightness, offset, and gamma with just a few lines of code. In this tutorial we’ll walk through every step needed to add, modify, and save exposure adjustment layers inside a PSD file with Java.

## Hızlı Yanıtlar
- **Hangi kütüphane?** Aspose.PSD for Java  
- **Ana görev?** Create exposure layer java and adjust its properties  
- **Tipik uygulama süresi?** 10–15 minutes for a basic script  
- **Önkoşullar?** JDK 11+, an IDE, and the Aspose.PSD JAR  
- **Gerekli lisans?** A temporary or full Aspose.PSD license for production use  

## create exposure layer java nedir?
Creating an exposure layer in Java means programmatically inserting an **Exposure Adjustment Layer** into a Photoshop document (PSD). This layer behaves like the “Exposure” adjustment you’d add manually in Photoshop, allowing you to control exposure, offset, and gamma without rasterizing the image.

## Bu görev için Aspose.PSD neden kullanılmalı?
- **No Photoshop required** – work entirely on the server or in CI pipelines.  
- **Full layer fidelity** – keep all original layers intact while tweaking exposure.  
- **Cross‑platform** – run on Windows, Linux, or macOS with the same Java code.  

## Önkoşullar
Before we embark on this exciting journey of manipulating PSD files, you’ll need a few things set up on your end:

### Java Ortamı
1. Java Development Kit (JDK): Ensure you have JDK installed on your machine. If not, download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. IDE of Your Choice: Use any IDE like IntelliJ IDEA, Eclipse, or even a simple text editor to write your Java code.  
3. Aspose.PSD Library: You’ll need the Aspose.PSD library for Java. You can download it from the [Aspose release page](https://releases.aspose.com/psd/java/).  
4. Basic Knowledge of Java: A foundational understanding of Java programming will go a long way in helping you grasp the concepts covered in this tutorial.  

Once you're all set up, we can dive into the nitty‑gritty of adding, modifying, and saving exposure adjustment layers in your PSD files!

## Paketleri İçe Aktar
Before we can get into editing our PSD files, we’ll need to import the necessary packages provided by Aspose.PSD. Here’s how to do that:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
```
These imports give us access to the core functionalities we need to manipulate PSD files.

## Adım 1: Belge Dizinini Ayarlayın
First things first, let's define the directory where your PSD files are located. You’ll want to replace `"Your Document Directory"` with the path to your local directory.
```java
String dataDir = "Your Document Directory";
```
Here, we're essentially preparing the workspace for our application. It’s just like setting up your workstation before starting a DIY project—everything needs to be just right!

## Adım 2: Düzenleme İçin PSD Dosyasını Yükleyin
Now, let's load the PSD file where we want to adjust the exposure. We'll be working with an example file named `ExposureAdjustmentLayer.psd`. 
```java
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
This is the moment we engage with our file! It’s like opening a book and getting ready to dive into the pages—each layer is a story waiting to be told.

## Adım 3: Mevcut Pozlama Ayar Katmanlarını Değiştirin
Next, we’ll loop through each layer in our PSD file to check if there exists an Exposure Adjustment Layer. If we find one, we’ll modify its properties!
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);
        expLayer.setOffset(-0.25f);
        expLayer.setGammaCorrection(0.5f);
    }
}
```
Here’s where the magic happens. Think of it as adjusting the dials on an old radio to get that perfect sound—only now, you’re tuning the exposure levels!

## Adım 4: Değiştirilmiş PSD Dosyasını Kaydedin
Once you've adjusted the exposure to your liking, it’s time to save the edited file. We'll save it as `ExposureAdjustmentLayerChanged.psd`.
```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
It’s like locking in that perfect recipe you just crafted—saving it guarantees that all your hard work won’t go to waste!

## Adım 5: Yeni Bir Pozlama Ayar Katmanı Eklemek
Now that we’ve modified an existing one, let’s add a brand‑new Exposure Adjustment Layer to another PSD file, `PhotoExample.psd`. 
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
Just like picking another canvas to paint on, we’re preparing another PSD document!

## Adım 6: Yeni Pozlama Katmanını Yapılandırın
We’ll create and configure the new Exposure Layer with your desired settings.
```java
ExposureLayer newlayer = img.addExposureAdjustmentLayer(10, -0.25f, 2f);
```
This is similar to adding a fresh coat of paint to your masterpiece—it enhances and rejuvenates the image, adding depth and character.

## Adım 7: Yeni PSD Dosyasını Kaydedin
Finally, let’s save our newly edited image as `PhotoExampleAddedExposure.psd`.
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";
img.save(psdPathAfterChange);
```
And just like that, we’ve wrapped up another project, ready to showcase our new creation!

## Sonuç
Managing exposure adjustment layers in PSD files using Aspose.PSD for Java is not just efficient; it’s empowering. You can modify existing layers or even add new ones, all while ensuring your creative vision shines through. By following the steps outlined above, you can effectively manipulate your images with just a few lines of code.

As you continue to explore the possibilities of image management and manipulation with Aspose, remember that each adjustment is a step toward crafting the perfect image.

## Sıkça Sorulan Sorular

**Q: Aspose.PSD for Java nedir?**  
A: Aspose.PSD for Java, Photoshop dosyalarıyla programlı olarak çalışmanıza olanak tanıyan bir kütüphanedir; katman manipülasyonu, renderleme ve dönüşüm gibi özellikler sunar.

**Q: Aspose.PSD'yi bir web uygulamasında kullanabilir miyim?**  
A: Evet, Aspose.PSD sunucu‑tarafı görüntü işleme imkanı sağlayarak web uygulamalarına entegre edilebilir.

**Q: Aspose.PSD'yi kullanmak için bir lisansa ihtiyacım var mı?**  
A: Evet, ücretsiz deneme sürümü mevcut olsa da uzun vadeli kullanım için geçerli bir lisans gereklidir. Geçici bir lisans alabilirsiniz [buradan](https://purchase.aspose.com/temporary-license/).

**Q: Aspose.PSD için destek nasıl alınır?**  
A: Aspose forumlarında topluluk desteğine [buradan](https://forum.aspose.com/c/psd/34) ulaşabilirsiniz.

**Q: Başlangıç için örnek bir proje var mı?**  
A: Evet, örnek projeleri ve dokümantasyonu [Aspose.PSD Referans sayfasında](https://reference.aspose.com/psd/java/) bulabilirsiniz.

---

**Son Güncelleme:** 2026-03-28  
**Test Edildi:** Aspose.PSD for Java 24.12 (latest)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}