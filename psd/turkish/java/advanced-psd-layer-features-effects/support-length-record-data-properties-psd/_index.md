---
date: 2026-09-23
description: Aspose.PSD for Java kullanarak PSD vector shapes'i nasıl değiştireceğinizi
  ve PSD dosyalarını batch process yapacağınızı öğrenin. Ayrıntılı adımlar, ipuçları
  ve code placeholders içeren tam bir çözüm.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: PSD'de Length Record Data Properties desteği - Java
og_description: Aspose.PSD for Java kullanarak PSD vector shapes'i nasıl değiştireceğinizi
  ve PSD dosyalarını batch process yapacağınızı öğrenin. Code placeholders ve uzman
  ipuçları içeren adım adım rehber.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Aspose.PSD for Java ile PSD vector shapes'i değiştirin
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Aspose.PSD for Java ile PSD vector shapes'i değiştirin
url: /tr/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD vektör şekillerini Aspose.PSD for Java ile değiştirin

## Giriş
If you need to **modify PSD vector shapes** programmatically, Aspose.PSD for Java gives you full control over Photoshop files directly from your Java code. This tutorial walks you through supporting length record properties—an essential step when editing vector shape layers. By the end you’ll be able to open a PSD, adjust its vector shape data, and save the updated file without ever launching Photoshop.

## Hızlı cevaplar
- **“modify PSD vector shapes” ne anlama geliyor?** Adjusting geometry, path operations, or other attributes of vector‑based layers inside a PSD file.  
- **Bu işlemi hangi kütüphane gerçekleştirir?** Aspose.PSD for Java.  
- **Lisans gerekli mi?** A free trial works for evaluation; a commercial license is required for production.  
- **Uygulama ne kadar sürer?** Around 10‑15 minutes for a basic shape‑modification script.  
- **Ana önkoşullar nelerdir?** Java JDK, Aspose.PSD for Java, and a sample PSD file.

## “Uzunluk kaydı özelliklerini destekleme” nedir?
Supporting length record properties means accessing and updating the `LengthRecord` objects that describe each vector path inside a PSD. These records store information such as the path’s length, type, and how it joins with other paths. Changing them lets you control how shapes combine, intersect, or subtract from one another, enabling precise vector editing.

## Neden Aspose.PSD for Java kullanarak uzunluk kaydı özelliklerini desteklemelisiniz?
Load your PSD, edit vector data, and save—all without Photoshop. Aspose.PSD processes multi‑hundred‑page PSDs in under 2 seconds on a typical server, offers over 150 classes (including 30+ vector‑related types), and runs on Windows, Linux, or macOS with any JDK 11+. This performance‑focused library eliminates the need for costly desktop software.

## Önkoşullar
1. **Java Development Kit (JDK)** – download from [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use your preferred package manager.  
2. **Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.  
4. **Bir PSD dosyası** – create one in Photoshop or grab a sample PSD to experiment with.  
5. **Temel Java bilgisi** – familiarity with classes, objects, and exception handling.

## Paketleri içe aktar
The import statements bring the core Aspose.PSD classes into scope, such as `PsdImage`, `VsmsResource`, and `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Adım 1: Kaynak ve çıktı dizinlerinizi ayarlayın
Define where the original PSD lives and where the modified file will be written.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Adım 2: PSD dosyasını yükleyin
Use `Image.load` to open the file and cast it to `PsdImage` for PSD‑specific features.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Adım 3: Katmandaki Vsms kaynağını bulun
`VsmsResource` is the container that stores vector shape data for a layer. Loop through the second layer’s resources to find it.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Adım 4: Uzunluk kayıtlarına erişin
`LengthRecord` represents a distinct vector path. Retrieve the records you intend to modify.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Adım 5: Yol işlem özelliklerini değiştirin
`PathOperations` defines how individual shapes interact (e.g., exclusion, intersection, subtraction). Changing these values updates the visual composition of the vector layer.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Adım 6: Değiştirilmiş PSD dosyasını kaydedin
Persist your changes to a new file.

```java
psdImage.save(outPsdFilePath);
```

## Adım 7: Kaynakları temizleyin
Dispose of the `PsdImage` instance to free memory and avoid resource leaks.

```java
psdImage.dispose();
```

## Uzunluk kaydı özelliklerini destekleyerek PSD dosyalarını toplu işleme nasıl yapılır
Wrap the single‑file workflow in a loop that iterates over a directory of PSDs, updating `inPsdFilePath` and `outPsdFilePath` for each file. This approach lets you apply identical vector‑shape adjustments to dozens or hundreds of files in minutes, ideal for automated asset pipelines.

## Yaygın tuzaklar ve ipuçları
- **Null kontrolleri** – always verify `resource` isn’t `null` before accessing its members.  
- **Yol indeks sınırları** – ensure the indices you use (e.g., `[2]`, `[7]`, `[11]`) exist for the specific PSD you’re editing.  
- **Lisans** – running without a valid license embeds a watermark in the saved PSD.  

## Sonuç
You now have a complete, end‑to‑end example of how to **modify PSD vector shapes** by supporting length record properties with Aspose.PSD for Java. Whether you’re automating an asset pipeline or building a custom design tool, these APIs give you the flexibility to manipulate vector layers without manual Photoshop work. Experiment with other `PathOperations` values or combine multiple `LengthRecord` edits to create complex shapes.

## Sıkça Sorulan Sorular

**Q: How do I handle a PSD that contains no vector shape layers?**  
A: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check and skip the modification step or inform the user.

**Q: Can I change other properties like fill color or stroke width?**  
A: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See the API docs for the full list.

**Q: Is it possible to batch‑process multiple PSD files?**  
A: Absolutely. Wrap the code inside a loop that iterates over a directory of PSD files, adjusting the input and output paths each time.

**Q: Do I need to close streams manually when loading from a file path?**  
A: `Image.load` handles file streams automatically, but if you load from an `InputStream`, remember to close it after use.

**Q: What version of Aspose.PSD is required for these APIs?**  
A: The `LengthRecord` and `PathOperations` classes have been available since Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## İlgili Eğitimler

- [Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD Files](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Convert PSD to PNG with Layer Mask Support Using Aspose.PSD for Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Add Layer Support Psd Files](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}