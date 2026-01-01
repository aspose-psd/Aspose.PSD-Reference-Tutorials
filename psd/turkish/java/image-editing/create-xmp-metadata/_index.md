---
date: 2026-01-01
description: XMP meta verilerini nasıl oluşturacağınızı, XMP'yi PSD dosyalarına nasıl
  ekleyeceğinizi ve Aspose.PSD for Java ile görüntü meta verilerini nasıl güncelleyeceğinizi
  öğrenin. Şimdi adım adım bu rehberi izleyin.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java ile XMP Meta Verilerini Oluşturun
url: /tr/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile XMP Meta Verilerini Oluşturma

## Giriş

Görüntü meta verilerini yönetmek, Photoshop (PSD) dosyalarıyla çalışan Java geliştiricileri için yaygın bir gereksinimdir. Bu öğreticide **XMP meta verilerini nasıl oluşturacağınızı** Aspose.PSD kütüphanesini kullanarak öğrenecek, bir PSD görüntüsüne XMP ekleyecek ve görüntü meta verilerini programlı olarak güncelleyeceksiniz. Her adımı adım adım inceleyecek, her parçanın neden önemli olduğunu açıklayacak ve gerçek projelerde uygulayabileceğiniz pratik ipuçları vereceğiz.

## Hızlı Yanıtlar
- **XMP meta verileri nedir?** Görüntü dosyalarının içine gömülen (yazar, anahtar kelimeler vb.) tanımlayıcı bilgileri içeren standart bir formattır.  
- **Aspose.PSD neden kullanılır?** Photoshop olmadan PSD dosyalarını oluşturmak, okumak ve düzenlemek için saf‑Java bir API sağlar.  
- **Mevcut bir PSD'ye XMP ekleyebilir miyim?** Evet – `setXmpData` ile görüntü meta verilerini anında güncelleyebilirsiniz.  
- **Ana adımlar nelerdir?** Görüntü boyutunu ayarlayın, başlık/son ekleyin, XMP paketlerini oluşturun, ekleyin ve kaydedin.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gerekir.

## Java’da “XMP meta verileri oluşturma” nedir?

XMP meta verileri oluşturmak, görüntüyü tanımlayan bir XMP paketi (başlık, gövde, son) oluşturup bu paketi bir PSD dosyasına gömmek anlamına gelir. Aspose.PSD kütüphanesi düşük‑seviye detayları soyutlayarak, saklamak istediğiniz içeriğe odaklanmanızı sağlar.

## Neden PSD dosyalarına XMP eklenir?

- **Aranabilirlik:** Yazar, başlık veya özel etiketlere dayalı güçlü varlık‑yönetimi aramaları sağlar.  
- **Uyumluluk:** XMP, Adobe ürünleri, Lightroom ve birçok DAM sistemi tarafından tanınır.  
- **Sürüm kontrolü:** İşleme geçmişi (ör. şehir, renk modu) dosyanın içinde doğrudan saklanır.

## Önkoşullar

- **Java Geliştirme Ortamı:** JDK 8 veya üzeri yüklü ve Java’ya temel bir anlayışınız olsun.  
- **Aspose.PSD Kütüphanesi:** Aspose.PSD for Java kütüphanesini indirin ve kurun. Kütüphaneyi ve ayrıntılı belgeleri [burada](https://reference.aspose.com/psd/java/) bulabilirsiniz.  
- **Belge Dizininiz:** PSD dosyalarını sisteminizde nereden okuyup/ yazacağınızı belirleyin.

## Paketleri İçe Aktarma

Java projenizde Aspose.PSD işlevlerini kullanmak için gerekli paketleri içe aktarın:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Adım 1: Görüntü Boyutunu Belirleme

Yeni PSD görüntüsü için tuval boyutlarını tanımlayın.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Adım 2: Yeni Bir Görüntü Oluşturma

Daha sonra XMP meta verileriyle zenginleştireceğimiz boş bir PSD görüntüsü oluşturun.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Adım 3: XMP Başlığı Oluşturma

Başlık, açılış XML işleme talimatını ve belgeyi tanımlayan bir GUID içerir.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Adım 4: XMP Sona Ekleme

Son ek, XMP paketinin sonunu işaret eder. `true` bayrağını ayarlamak kapanış işleme talimatını yazar.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Adım 5: XMP Meta Verilerini Oluşturma

Yazar ve açıklama gibi genel özellikleri temel XMP meta veri nesnesine ekleyin.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Adım 6: XMP Paket Sargısı Oluşturma

Başlık, son ve temel meta verileri tek bir paket içinde birleştirerek görüntüye eklenebilir hâle getirin.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Adım 7: Photoshop Özelliklerini Ayarlama

Adobe araçlarının çoğunun beklediği Photoshop‑özel alanları (şehir, ülke, renk modu) doldurun.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Adım 8: Photoshop Paketini XMP Meta Verilerine Ekleme

Photoshop paketini XMP paketine ekleyin.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Adım 9: DublinCore Özelliklerini Ayarlama

Yazar, başlık ve özel bir film etiketi gibi Dublin Core meta verilerini ekleyin.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Adım 10: DublinCore Paketini XMP Meta Verilerine Ekleme

Mevcut XMP paketine Dublin Core paketini birleştirin.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Adım 11: XMP Meta Verilerini Görüntüye Güncelleme

Tam XMP paketini PSD görüntüsüne gömün.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Adım 12: Görüntüyü Kaydetme

Meta verilerin kalıcı olması için PSD dosyasını diske (veya bir bellek akışına) yazın.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|-------|
| **`NullPointerException` on `setXmpData`** | XMP paketi tam olarak oluşturulmadı (başlık/son eksik). | `XmpHeaderPi`, `XmpTrailerPi` oluşturduğunuzdan ve tüm paketleri `setXmpData` çağırmadan önce eklediğinizden emin olun. |
| **Metadata not visible in Photoshop** | Photoshop, XMP paketinin doğru şekilde sarılmasını bekler. | `XmpTrailerPi(true)` kullanıldığını ve paketin görüntüyle birlikte kaydedildiğini doğrulayın. |
| **File path errors** | İzinleri olmayan bir göreli yol kullanılıyor. | Mutlak bir yol kullanın veya uygulamanın hedef klasöre yazma izni olduğundan emin olun. |

## Sıkça Sorulan Sorular

**S: Aspose.PSD farklı görüntü formatlarıyla uyumlu mu?**  
C: Evet, Aspose.PSD PSD, PSB, BMP, GIF, JPEG, PNG, TIFF ve daha fazlasını destekleyerek formatlar arasında esneklik sağlar.

**S: Mevcut meta verileri Aspose.PSD ile değiştirebilir miyim?**  
C: Kesinlikle. Mevcut bir PSD'yi yükleyebilir, `getXmpData()` ile XMP verisini alabilir, paketi değiştirebilir ve tekrar kaydedebilirsiniz.

**S: Aspose.PSD'nin işleyebileceği görüntü boyutu konusunda sınırlamalar var mı?**  
C: Aspose.PSD, yalnızca mevcut bellekle sınırlı olmak üzere, birkaç gigapiksel büyüklüğe kadar büyük görüntülerle çalışmak üzere tasarlanmıştır.

**S: Aspose.PSD için deneme sürümü mevcut mu?**  
C: Evet, ücretsiz bir deneme sürümünü [buradan](https://releases.aspose.com/) alarak Aspose.PSD'nin yeteneklerini keşfedebilirsiniz.

**S: Aspose.PSD ile ilgili sorular için nereden destek alabilirim?**  
C: Her türlü yardım ve soru için [Aspose.PSD forumunu](https://forum.aspose.com/c/psd/34) ziyaret edebilirsiniz.

## Sonuç

Artık **XMP meta verilerini nasıl oluşturacağınızı**, bir PSD'ye XMP eklemeyi ve Aspose.PSD for Java kullanarak görüntü meta verilerini güncellemeyi öğrendiniz. Bu adımlar, görüntülerinizde gömülü açıklayıcı bilgileri tam kontrol etmenizi sağlar; böylece dosyalar aranabilir, yönetilebilir ve sonraki iş akışlarına hazır hâle gelir. Ek XMP şemalarıyla denemeler yapmaktan veya bu kodu daha büyük görüntü‑işleme hatlarına entegre etmekten çekinmeyin.

---

**Son Güncelleme:** 2026-01-01  
**Test Edilen:** Aspose.PSD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}