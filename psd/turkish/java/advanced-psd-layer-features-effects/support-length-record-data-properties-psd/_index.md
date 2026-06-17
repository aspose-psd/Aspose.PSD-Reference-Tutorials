---
date: 2026-02-20
description: Aspose.PSD for Java kullanarak uzun kayıt özelliklerini nasıl destekleyeceğinizi
  ve PSD dosyalarını toplu işleme alacağınızı öğrenin. Kod örnekleriyle adım adım
  rehber.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Uzunluk Kayıt Özelliklerini Destekle – PSD Vektör Şekillerini Değiştir (Java)
url: /tr/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uzunluk Kayıt Özelliklerini Destekleme – PSD Vektör Şekillerini Değiştirme (Java)

## Introduction
Programlı olarak **PSD vektör şekillerini değiştirmek** istiyorsanız, Aspose.PSD for Java kütüphanesi, Photoshop dosyaları üzerinde Java kodunuzdan tam kontrol sağlar. Bu öğreticide, **uzunluk kayıt özelliklerini destekleme** konusunda bilmeniz gereken her şeyi adım adım inceleyeceğiz—vektör şekil katmanlarını düzenlemek istediğinizde kritik bir adımdır. Sonunda, bir PSD dosyasını açabilecek, vektör şekil özelliklerini ayarlayabilecek ve güncellenmiş dosyayı IDE'nizden çıkmadan kaydedebileceksiniz. Hadi başlayalım!

## Quick Answers
- **“PSD vektör şekillerini değiştirmek” ne anlama geliyor?** Bir PSD dosyasındaki vektör tabanlı katmanların geometrisini, yol işlemlerini veya diğer özelliklerini ayarlamak.  
- **Bu işlemi hangi kütüphane yapıyor?** Aspose.PSD for Java.  
- **Lisans gerekir mi?** Değerlendirme için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir şekil‑değiştirme betiği için yaklaşık 10‑15 dakika.  
- **Ana önkoşullar nelerdir?** Java JDK, Aspose.PSD for Java ve örnek bir PSD dosyası.

## What is “support length record properties”?
Uzunluk kayıt özelliklerini desteklemek, bir PSD içindeki her vektör yolunu tanımlayan `LengthRecord` nesnelerine erişmek ve bunları güncellemek anlamına gelir. Bu kayıtları değiştirmek, şekillerin nasıl birleştirileceğini, kesişeceğini veya birbirinden çıkarılacağını kontrol etmenizi sağlar.

## Why use Aspose.PSD for Java to support length record properties?
- **Photoshop gerekmez** – PSD dosyalarıyla doğrudan herhangi bir sunucuda çalışın.  
- **Zengin API** – katmanlara, kaynaklara ve vektör verilerine güçlü tipli sınıflarla erişin.  
- **Çapraz‑platform** – Windows, Linux veya macOS üzerinde herhangi bir JDK ile çalıştırın.  
- **Performansa odaklı** – verimli bellek yönetimi ve hızlı kaydetme işlemleri.  

## Prerequisites
1. **Java Development Kit (JDK)** – [Oracle'ın web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin veya tercih ettiğiniz paket yöneticisini kullanın.  
2. **Aspose.PSD for Java** – en yeni JAR dosyasını [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) edinin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya herhangi bir Java‑uyumlu editör.  
4. **Bir PSD dosyası** – Photoshop'ta oluşturun veya deneme amaçlı bir örnek PSD alın.  
5. **Temel Java bilgisi** – sınıflar, nesneler ve istisna yönetimi konularına aşina olun.

## Import Packages
İlk olarak, PSD dosyaları ve vektör şekil kaynaklarıyla çalışmak için ihtiyaç duyacağınız sınıfları içe aktarın.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Step 1: Set Up Your Source and Output Directories
Orijinal PSD'nin bulunduğu yeri ve değiştirilmiş dosyanın kaydedileceği yeri tanımlayın.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Step 2: Load the PSD File
Dosyayı açmak için `Image.load` kullanın ve PSD‑özel özellikler için `PsdImage` tipine dönüştürün.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Step 3: Locate the Vsms Resource in the Layer
Vektör şekil verileri bir `VsmsResource` içinde bulunur. İkinci katmanın kaynakları arasında dolaşarak bunu bulun.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Step 4: Access Length Records
Her `LengthRecord` ayrı bir vektör yolunu temsil eder. Değiştirmeyi planladığınız kayıtları alın.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Step 5: Modify Path Operation Properties
Şimdi `PathOperations` değerlerini değiştirerek **PSD vektör şekillerini** modifiye edebilirsiniz. Bu, şekillerin nasıl etkileşeceğini (ör. dışlama, kesişim, çıkarma) belirler.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Step 6: Save the Modified PSD File
Değişikliklerinizi yeni bir dosyaya kaydedin.

```java
psdImage.save(outPsdFilePath);
```

## Step 7: Clean Up Resources
Belleği serbest bırakmak için `PsdImage` nesnesini dispose edin.

```java
psdImage.dispose();
```

## How to batch process PSD files with support length record properties
Aynı vektör‑şekil ayarlarını birçok PSD’ye uygulamanız gerekiyorsa, yukarıdaki kodu bir dizindeki dosyalar üzerinde dönen bir döngüye yerleştirin. Her yineleme için `inPsdFilePath` ve `outPsdFilePath` değerlerini güncelleyin; böylece **PSD dosyalarını toplu işleme** verimli bir şekilde yapabilirsiniz.

## Common Pitfalls & Tips
- **Null kontrolleri** – `resource` nesnesine erişmeden önce her zaman `null` olmadığını doğrulayın.  
- **Yol indeks sınırları** – kullandığınız indekslerin (`[2]`, `[7]`, `[11]`) ilgili PSD içinde mevcut olduğundan emin olun.  
- **Lisans** – geçerli bir lisans olmadan çalıştırmak, kaydedilen PSD’ye bir filigran ekleyecektir.  

## Conclusion
Artık Aspose.PSD for Java ile uzunluk kayıt özelliklerini destekleyerek **PSD vektör şekillerini değiştirme** konusunda eksiksiz bir uçtan‑uca örneğe sahipsiniz. İster varlık hatlarını otomatikleştiriyor olun, ister özel bir tasarım aracı geliştiriyor olun, bu API’ler vektör katmanlarını manuel Photoshop müdahalesi olmadan manipüle etme esnekliği sunar. Diğer `PathOperations` seçeneklerini deneyerek veya birden fazla `LengthRecord` düzenlemesini birleştirerek daha karmaşık şekiller oluşturabilirsiniz.

## Frequently Asked Questions

**Q: Vektör şekil katmanı içermeyen bir PSD nasıl ele alınır?**  
A: `VsmsResource` bulunmayacak, bu yüzden `resource` `null` kalacaktır. Bir kontrol ekleyip değişiklik adımını atlayın veya kullanıcıyı bilgilendirin.

**Q: Doldurma rengi veya çizgi kalınlığı gibi diğer özellikleri değiştirebilir miyim?**  
A: Evet, `LengthRecord` doldurma, çizgi ve opaklık için ek setter metodları sunar. Ayrıntılar için API belgelerine bakın.

**Q: Birden fazla PSD dosyasını toplu‑işlem yapmak mümkün mü?**  
A: Kesinlikle. Kodu bir dizindeki PSD dosyaları üzerinde dönen bir döngüye yerleştirerek, her seferinde giriş ve çıkış yollarını ayarlayın.

**Q: Dosya yolundan yüklerken akışları manuel olarak kapatmam gerekir mi?**  
A: `Image.load` yöntemi dosya akışlarını dahili olarak yönetir, ancak bir `InputStream` üzerinden yüklüyorsanız, kullanım sonrası kapatmayı unutmayın.

**Q: Bu API’ler için hangi Aspose.PSD sürümü gerekiyor?**  
A: `LengthRecord` ve `PathOperations` sınıfları Aspose.PSD 20.10’dan itibaren mevcuttur. En yeni sürümün kullanılması tavsiye edilir.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}