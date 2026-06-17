---
date: 2026-06-03
description: Aspose.PSD for Java kullanarak PSD'yi PNG'ye nasıl dönüştüreceğinizi
  ve Vector Mask Java oluşturmayı öğrenin, Vector Mask PSD ekleyin ve Vmsk kaynaklarını
  programlı olarak yönetin.
keywords:
- convert psd to png
- add vector mask psd
- psd vector mask tutorial
- aspose psd maven
linktitle: PSD'yi PNG'ye Dönüştür ve Vector Mask Java Oluştur – PSD Dosyalarındaki
  Vmsk Kaynağı
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to convert PSD to PNG and create vector mask Java using Aspose.PSD
    for Java, add vector mask PSD, and manipulate Vmsk resources programmatically.
  headline: Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD
    Files
  type: TechArticle
- questions:
  - answer: Create a `VmskResource`, populate it with the required path records (e.g.,
      `BezierKnotRecord`), and attach it to the layer’s resources collection.
    question: How do I add a new vector mask to an existing layer?
  - answer: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")`
      specifying the PNG format.
    question: Can I convert the edited PSD directly to PNG without opening Photoshop?
  - answer: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle
      builds, Docker containers, or any CI system that supports Java.
    question: Is there a way to automate this in a CI/CD pipeline?
  - answer: All recent releases (2024‑2025) support Java 8 and above, including Java
      11, 17, and newer LTS versions.
    question: What versions of Aspose.PSD are compatible with Java 11+?
  - answer: A free evaluation license works for development and testing. For production
      deployments, a commercial license is required.
    question: Do I need a license for development builds?
  type: FAQPage
second_title: Aspose.PSD Java API
title: PSD'yi PNG'ye Dönüştür ve Vector Mask Java Oluştur – PSD Dosyalarındaki Vmsk
  Kaynağı
url: /tr/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dönüştür ve Vektör Maskesi Java Oluştur – PSD Dosyalarındaki Vmsk Kaynağı

## Giriş
Eğer Photoshop dosyaları içinde **convert PSD to PNG** yaparken aynı zamanda **create vector mask** (Vmsk) kaynaklarını da oluşturmanız gerekiyorsa, Aspose.PSD for Java her iki işlemi de temiz ve programatik bir şekilde yapmanızı sağlar. İster bir tasarım‑otomasyon aracı, varlıkları doğrulayan bir CI boru hattı ya da özel maskelerle grafik iş akışını genişletiyor olun, bu öğretici size her adımı gösterir—PSD'yi yükleme, Vmsk kaynağını okuma, özelliklerini ayarlama, sonucu PNG olarak dışa aktarma ve değiştirilmiş dosyayı kaydetme. Sonuna geldiğinizde vektör maskeleriyle rahatça çalışabilecek, PSD → PNG dönüştürme ve dosyayı ek vektör verileriyle genişletme konularında **convert PSD to PNG** tekniklerine hakim olacaksınız.

## Hızlı Yanıtlar
- **Vmsk kaynağı nedir?** PSD dosyası içinde depolanan vektör maske verisidir ve bir katman için karmaşık vektör şekilleri tanımlar.  
- **Hangi kütüphane bunu destekliyor?** Aspose.PSD for Java, Vmsk kaynaklarına tam okuma/yazma erişimi sağlar.  
- **Lisans gerekiyor mu?** Ücretsiz deneme mevcuttur; üretim kullanımı için ticari lisans gereklidir.  
- **Düzenlenmiş PSD'yi PNG'ye dönüştürebilir miyim?** Evet—kaydedildikten sonra PSD'yi yükleyebilir ve aynı API ile PNG'ye dışa aktarabilirsiniz.  
- **Maven desteği var mı?** Kesinlikle; Aspose.PSD bir Maven bağımlılığı olarak eklenebilir (“aspose psd maven” anahtar kelimesine bakın).

## Vektör Maskesi (Vmsk Kaynağı) Nedir?
Vektör maskesi (Vmsk), bir katmanda şeffaf ve opak bölgeleri tanımlamak için Bézier eğrileri ve yol kayıtlarını kullanan piksel‑tabanlı olmayan bir maskedir. Vektör tabanlı olduğu için kalite kaybı olmadan ölçeklenir—yüksek çözünürlüklü grafikler için mükemmeldir. Birden fazla yol içerebilir, her biri Bézier düğümlerinden oluşur ve opaklık, dolgu ve katman maskelerine bağlama gibi maske özelliklerini destekler.

## Neden Aspose.PSD ile Vektör Maskesi Oluşturmalısınız?
Vektör maskelerini programlı olarak oluşturmak, manuel Photoshop düzenlemesine olan ihtiyacı ortadan kaldırır, büyük dosya gruplarında tutarlılığı sağlar ve otomatik yapı veya dağıtım boru hatlarına entegrasyonu mümkün kılar. Aspose.PSD ile kesin maske geometrisi oluşturabilir, herhangi bir katmana uygulayabilir ve tam düzenlenebilirliği koruyabilirsiniz; bu, dinamik grafik üretimi ve duyarlı tasarım iş akışları için esastır.
- **Otomasyon:** Photoshop açmadan programlı olarak maskeler ekleyebilir veya değiştirebilirsiniz.  
- **Tutarlılık:** Oluşturduğunuz her PSD'nin aynı maske kurallarını izlediğinden emin olun.  
- **Çapraz‑platform:** Java'yı destekleyen herhangi bir işletim sisteminde çalışır.  
- **Entegrasyon:** Diğer Aspose API'leriyle (ör. convert PSD → PNG) birleştirerek uç‑uç iş akışları oluşturabilirsiniz.  
- **Ölçeklenebilirlik:** Vektör maskeler herhangi bir boyutta net kalır, bu da duyarlı tasarımlar için idealdir.

## Java Geliştiricileri İçin Bunun Önemi
**create vector mask java** tekniklerini kullanmak, gelişmiş grafik mantığını doğrudan arka uç hizmetlerine, CI boru hatlarına veya masaüstü yardımcı programlara yerleştirmenizi sağlar. Artık bir tasarımcının maskeleri manuel eklemesine ihtiyaç yok; kodunuz bunları anında oluşturabilir veya ayarlayabilir, zaman tasarrufu sağlar ve insan hatasını azaltır.

## Ön Koşullar
Koda geçmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

### Gereksinimler
- **Java Development Kit (JDK):** JDK 8 veya daha yenisini kurun. [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) adresinden indirebilirsiniz.  
- **Aspose.PSD for Java Library:** Bu güçlü kütüphane PSD dosyalarını yönetir. [Aspose release page](https://releases.aspose.com/psd/java/) adresinden indirin. Hızlı bir başlangıç için aynı sayfadan veya [free trial](https://releases.aspose.com/) üzerinden ücretsiz deneme sürümünü alın.  
- **Bir IDE:** Herhangi bir Java IDE (IntelliJ IDEA, Eclipse, NetBeans) çalışır.

### Çalışma Alanınızı Ayarlama
1. **Yeni bir Java Projesi Oluşturun** – Tercih ettiğiniz IDE'yi açın ve yeni bir proje başlatın.  
2. **Aspose Kütüphanesini Ekleyin** – Aspose JAR dosyasını indirdikten sonra, proje derleme yoluna ekleyin, böylece tüm PSD‑ile ilgili sınıflara erişebilirsiniz.

Ortam hazır olduğunda, gerçek uygulamaya göz atalım.

## Aspose.PSD for Java Kullanarak PSD'yi PNG'ye Nasıl Dönüştürülür?
Kaynak PSD'nizi `PsdImage.load()` ile yükleyin, isteğe bağlı olarak vektör maskesini düzenleyin, ardından `ExportFormat.Png` belirterek `save()` çağırın. Aspose.PSD tüm renk profillerini, katmanları ve maske verilerini otomatik olarak işler ve orijinal görsel görünümüyle eşleşen piksel‑kusursuz bir PNG üretir. Bu iki adımlı akış, boyutu ne olursa olsun herhangi bir PSD için çalışır ve herhangi bir Java‑uyumlu platformda çalışır.

## Paketleri İçe Aktarma
`com.aspose.psd` paketi, PSD dosyalarını işlemek için çekirdek sınıflar sağlar; bunlar arasında görüntü yükleme, kaynak manipülasyonu ve dışa aktarma yetenekleri bulunur.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Artık ortamı hazırladığımıza göre, her bir işlemi inceleyelim.

## Adım 1: PSD Dosyanızı Yükleyin
Dosyayı yüklemek, bellekte tüm belgeyi temsil eden bir `PsdImage` nesnesi sağlar.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` değişkenini PSD dosyanızın bulunduğu dizine ayarladık.  
- `sourceFileName` için bir dize oluşturduk; dizini PSD dosyasının adıyla birleştirdik.  
- Son olarak, `Image.load()` kullanarak PSD dosyasını bir `PsdImage` nesnesine yükledik.

## Adım 2: Vmsk Kaynağını Alın
`VmskResource` sınıfı, bir PSD katmanı içinde depolanan vektör maske verilerini kapsüller. Onu almak, maske yollarını incelemenize veya değiştirmenize olanak tanır.

```java
VmskResource resource = getVmskResource(im);
```

- `getVmskResource()` metodunu çağırıyoruz; bu metod görüntüden Vmsk kaynağını arar ve getirir.

## Adım 3: Vmsk Kaynağı Özelliklerini Doğrulama
Değişiklik yapmadan önce, maskenin etkin, doğru yönlendirilmiş ve beklenen yol sayısını içerdiğini doğrulayın.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Burada, Vmsk kaynağının çeşitli özelliklerini kontrol ediyoruz. Maskenin devre dışı bırakılmadığından, ters çevrilmediğinden, bağlanmadığından ve doğru sayıda yol içerdiğinden emin olmak istiyoruz.

## Adım 4: Her Yola Erişin ve Doğrulayın
Her yol kaydı, vektör şeklinin bir bölümünü tanımlar. Bunları incelemek, doğru geometriyle çalıştığınızı garanti eder.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Üç belirli yol kaydını çıkarıyor ve tiplerini ve özelliklerini doğruluyoruz; böylece kriterlerimize uyduklarından emin oluyoruz.

## Adım 5: Vmsk Kaynağını Düzenleyin
Şimdi değişiklik kısmına giriyoruz! Maskenin davranış bayraklarını iş akışınıza uygun şekilde değiştirebilirsiniz.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Bu blokta, Vmsk kaynağının çeşitli özelliklerini değiştiriyoruz. `true` olarak ayarlayarak maskenin PSD dosyasında nasıl davranacağını kontrol edebiliriz.

## Adım 6: Bezier Düğüm Noktalarını Değiştirin
Bezier düğümleri, her vektör segmentinin eğriliğini tanımlar. Bunları ayarlamak, maskeyi rasterleştirmeden yeniden şekillendirir.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Belirli `BezierKnotRecord` yollarına erişiyor ve noktalarını değiştirerek vektör maskesini yeniden şekillendirebiliyoruz.

## Adım 7: Değiştirilen PSD Dosyasını Kaydedin
Tüm düzenlemeler tamamlandıktan sonra, değişiklikleri yeni bir PSD dosyasına kaydedin.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Dışa aktarılan PSD dosyasının yolunu ayarlıyoruz ve ardından `im.save()` çağırarak değişiklikleri bu yeni dosyaya yazıyoruz.

## Adım 8: PSD'yi PNG Olarak Dışa Aktarın
PSD artık güncellenmiş maskeyi içerdiğine göre, doğrudan PNG olarak dışa aktarın. Bu adım **convert PSD to PNG** iş akışını gösterir.

```java
im.dispose();
```

- `im.save("output.png", ExportFormat.Png)` kullanarak düzenlenmiş vektör maskesini yansıtan yüksek kaliteli bir PNG oluşturun.

## Kaynakları Temizleme
Son olarak, görüntüyü düzgün bir şekilde serbest bırakarak kaynakları temizlediğimizden emin olmalıyız.

CODE_BLOCK_PLACEHOLDER_9_END

- İşiniz bittiğinde her zaman kaynakları serbest bırakmak iyi bir uygulamadır. Bu, uygulamalarınızdaki bellek sızıntılarını önlemeye yardımcı olur.

## Yaygın Sorunlar ve Çözümler
| Sorun | Neden Oluşur | Nasıl Düzeltilir |
|-------|----------------|------------|
| **`VmskResource` not found** | PSD'de vektör maske katmanı bulunmuyor. | Kaynak PSD'nin bir vektör maskesi içerdiğini doğrulayın veya kodu çalıştırmadan önce Photoshop'ta manuel olarak ekleyin. |
| **`ArrayIndexOutOfBoundsException` on path access** | Beklenen yol kayıt sayısı farklı. | `resource.getPaths().length` değerini inceleyin ve indeks kullanımını buna göre ayarlayın. |
| **License exception** | Geçerli bir Aspose.PSD lisansı olmadan çalıştırılıyor. | `License license = new License(); license.setLicense("Aspose.PSD.lic");` kodunu kullanarak deneme veya satın alınmış lisans uygulayın. |
| **Memory leak** | Uzun süren işlemlerde görüntü serbest bırakılmıyor. | `finally` bloğunda her zaman `im.dispose()` çağırın veya destekleniyorsa try‑with‑resources kullanın. |

## Sıkça Sorulan Sorular

**Q: Mevcut bir katmana yeni bir vektör maskesi nasıl eklenir?**  
A: Bir `VmskResource` oluşturun, gerekli yol kayıtlarıyla (ör. `BezierKnotRecord`) doldurun ve katmanın kaynak koleksiyonuna ekleyin.

**Q: Düzenlenmiş PSD'yi Photoshop açmadan doğrudan PNG'ye dönüştürebilir miyim?**  
A: Evet—PSD'yi kaydettikten sonra `Image.load()` ile tekrar yükleyin ve PNG formatını belirterek `im.save("output.png")` çağırın.

**Q: Bunu bir CI/CD boru hattında otomatikleştirmenin bir yolu var mı?**  
A: Kesinlikle. İşlem tamamen Java olduğundan, Maven/Gradle derlemelerine, Docker konteynerlerine veya Java destekleyen herhangi bir CI sistemine entegre edebilirsiniz.

**Q: Aspose.PSD'nin hangi sürümleri Java 11+ ile uyumludur?**  
A: Tüm son sürümler (2024‑2025) Java 8 ve üzerini, özellikle Java 11, 17 ve daha yeni LTS sürümlerini destekler.

**Q: Geliştirme derlemeleri için lisans gerekiyor mu?**  
A: Ücretsiz deneme lisansı geliştirme ve test için çalışır. Üretim dağıtımları için ticari lisans gereklidir.

**Son Güncelleme:** 2026-06-03  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Java'da Katman Maskesi Desteğiyle PSD'yi PNG'ye Dışa Aktar](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Aspose.PSD for Java ile PSD'yi PNG'ye Dönüştür ve Orantılı Yeniden Boyutlandır](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Renk Katmanı ile PSD'yi PNG'ye Dönüştür – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}