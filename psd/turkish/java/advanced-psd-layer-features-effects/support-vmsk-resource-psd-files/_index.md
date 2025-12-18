---
date: 2025-12-18
description: Aspose.PSD for Java kullanarak PSD dosyalarında vektör maskesi (Vmsk
  kaynağı) oluşturmayı öğrenin. Bu adım adım öğretici, vektör maskesi eklemeyi, PSD'yi
  PNG'ye dönüştürmeyi ve daha fazlasını gösterir.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Java ile PSD Dosyalarında Vektör Maskesi (Vmsk Kaynağı) Oluşturma
url: /tr/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında Java ile Vektör Maskesi (Vmsk Kaynağı) Oluşturma

## Giriş
Photoshop (PSD) dosyaları içinde **vektör maskesi** (Vmsk) kaynakları oluşturmanız gerekiyorsa, Aspose.PSD for Java bunu temiz ve programatik bir şekilde yapmanızı sağlar. Tasarım‑otomasyon aracı geliştiriyor ya da mevcut bir grafik boru hattına özel maske desteği ekliyor olun, bu öğretici sizi her adımda yönlendirecek—PSD'yi yükleme, Vmsk kaynağını okuma, özelliklerini ayarlama ve sonucu kaydetme. Sonuna geldiğinizde, vektör maskeleriyle rahatça çalışabilecek, PSD'yi PNG'ye dönüştürebilecek ve dosyayı ek vektör verileriyle genişletebileceksiniz.

## Hızlı Cevaplar
- **Vmsk kaynağı nedir?** PSD dosyası içinde depolanan vektör maske verisidir ve bir katmanın karmaşık vektör şekillerini tanımlar.  
- **Hangi kütüphane bunu destekliyor?** Aspose.PSD for Java, Vmsk kaynaklarına tam okuma/yazma erişimi sağlar.  
- **Lisans gerekir mi?** Ücretsiz deneme mevcuttur; üretim kullanımı için ticari lisans gereklidir.  
- **Düzenlenmiş PSD'yi PNG'ye dönüştürebilir miyim?** Evet—kaydedildikten sonra PSD'yi yükleyip aynı API ile PNG olarak dışa aktarabilirsiniz.  
- **Maven desteği var mı?** Kesinlikle; Aspose.PSD, Maven bağımlılığı olarak eklenebilir (bkz. “aspose psd maven” anahtar kelimesi).

## Vektör Maskesi (Vmsk Kaynağı) Nedir?
Vektör maskesi (Vmsk), bir katmanda şeffaf ve opak bölgeleri tanımlamak için Bézier eğrileri ve yol kayıtları kullanan piksel‑tabanlı olmayan bir maskedir. Vektör tabanlı olduğu için kalite kaybı olmadan ölçeklenir—yüksek çözünürlüklü grafikler için mükemmeldir.

## Aspose.PSD ile Neden Vektör Maskesi Oluşturmalısınız?
- **Otomasyon:** Photoshop açmadan maskeleri programatik olarak ekleyebilir veya değiştirebilirsiniz.  
- **Tutarlılık:** Oluşturduğunuz her PSD'nin aynı maske kurallarını izlemesini sağlayın.  
- **Çapraz‑platform:** Java'yı destekleyen herhangi bir işletim sisteminde çalışır.  
- **Entegrasyon:** Diğer Aspose API'leriyle (ör. PSD → PNG dönüşümü) birleştirerek uç‑uç iş akışları oluşturabilirsiniz.

## Önkoşullar
Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

### Gereksinimler
- Java Development Kit (JDK): Makinenizde JDK yüklü olmalı. Değilse, [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-downloads.html) indirebilirsiniz.  
- Aspose.PSD for Java Kütüphanesi: PSD dosyalarını yönetmek için güçlü bir kütüphanedir. [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) indirebilirsiniz. Satın almadan önce denemek isteyenler için [ücretsiz deneme](https://releases.aspose.com/) de mevcuttur.  
- Bir IDE: Java için herhangi bir IDE (IntelliJ IDEA, Eclipse vb.) bu proje ile çalışacaktır.

### Çalışma Alanınızı Kurma
1. **Yeni bir Java Projesi Oluşturun** – Tercih ettiğiniz IDE'yi açın ve yeni bir proje başlatın.  
2. **Aspose Kütüphanesini Ekleyin** – Aspose JAR dosyasını indirdikten sonra proje derleme yoluna ekleyin, böylece PSD‑ile ilgili tüm sınıflara erişebilirsiniz.

Ortam hazır olduğuna göre, gerçek uygulamaya geçelim.

## Java ile PSD Dosyalarında Vektör Maskesi Nasıl Oluşturulur
Aşağıda adım‑adım bir rehber bulunmaktadır. Kod blokları orijinal öğreticiden değiştirilmemiştir; sadece her adımı netleştirmek için açıklayıcı metin eklenmiştir.

## Paketleri İçe Aktarma
PSD dosyaları üzerinde çalışmadan önce Aspose.PSD kütüphanesinden gerekli sınıfları içe aktarmamız gerekir.

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

Şimdi sahneyi hazırladığımıza göre, her bir işlemi inceleyelim.

## Adım 1: PSD Dosyanızı Yükleyin
İlk olarak PSD dosyanızı yüklemeniz gerekir. İşte sihrin başladığı yer.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` değişkenini PSD dosyanızın bulunduğu klasöre ayarlıyoruz.  
- `sourceFileName` değişkeni, klasör yolu ile PSD dosyasının adını birleştiriyor.  
- Son olarak, `Image.load()` ile PSD dosyasını bir `PsdImage` nesnesine yüklüyoruz.

## Adım 2: Vmsk Kaynağını Alın
PSD görüntümüz yüklendiğine göre, Vmsk kaynağını alalım.

```java
VmskResource resource = getVmskResource(im);
```

- `getVmskResource()` metodunu çağırıyoruz; bu metod görüntüden Vmsk kaynağını arar ve getirir.

## Adım 3: Vmsk Kaynağı Özelliklerini Doğrulayın
Değişiklik yapmadan önce, Vmsk kaynağının beklenen durumda olduğundan emin olmak gerekir.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Burada Vmsk kaynağının çeşitli özelliklerini kontrol ediyoruz. Devre dışı bırakılmadığını, ters çevrilmediğini, bağlantısının kesik olmadığını ve doğru sayıda yol içerdiğini doğrulamak istiyoruz.

## Adım 4: Her Yolu Erişin ve Doğrulayın
Vmsk kaynağı içindeki yolları biraz daha derinlemesine inceleyelim.

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
Şimdi değişiklik kısmına giriyoruz! Vmsk kaynağının özelliklerini ihtiyacınıza göre ayarlayabilirsiniz.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Bu blokta Vmsk kaynağının çeşitli özelliklerini `true` olarak ayarlıyoruz; böylece maskenin PSD dosyasında nasıl davranacağını kontrol edebiliyoruz.

## Adım 6: Bézier Düğüm Noktalarını Değiştirin
Bézier düğümleri vektör yolları için kritiktir. Burada bazı değerleri değiştirelim.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Belirli `BezierKnotRecord` yollarına erişiyor ve noktalarını değiştirerek vektör maskesini yeniden şekillendirebiliyoruz.

## Adım 7: Düzenlenmiş PSD Dosyasını Kaydedin
Tüm düzenlemeler tamamlandığında, değiştirilen PSD dosyasını kaydetme zamanı.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Dışa aktarılacak PSD dosyasının yolunu ayarlıyoruz ve ardından `im.save()` çağrısıyla bu yeni dosyaya değişiklikleri yazıyoruz.

## Adım 8: Kaynakları Temizleyin
Son olarak, görüntüyü doğru bir şekilde serbest bırakarak kaynakları temizlemeliyiz.

```java
im.dispose();
```

- İşiniz bittiğinde her zaman kaynakları serbest bırakmak iyi bir uygulamadır; bu, uygulamanızda bellek sızıntılarını önlemeye yardımcı olur.

## Sonuç
Tebrikler! Aspose.PSD for Java kullanarak PSD dosyalarında **vektör maskesi** (Vmsk) kaynaklarını oluşturma sürecini ayrıntılı bir şekilde tamamladınız. Görüntüyü yüklemek, Vmsk kaynağını almak ve doğrulamak, özelliklerini düzenlemek ve değiştirilmiş PSD'yi kaydetmek konularında sağlam bir temele sahipsiniz. Bu teknikleri tasarım boru hatlarınızı zenginleştirmek, diğer Aspose API'leriyle (ör. PSD'yi PNG'ye dönüştürme) entegre etmek veya özel grafik araçları oluşturmak için kullanabilirsiniz.

## SSS'ler
### Vmsk kaynağı nedir?
Vmsk kaynağı, PSD dosyasında karmaşık vektör şekilleri ve düzenleme özellikleri sağlayan bir vektör maskesidir.

### Aspose.PSD'yi bir Maven projesinde kullanabilir miyim?
Evet, Aspose.PSD'yi Maven projenize bağımlılık olarak ekleyebilir ve depo koordinatları aracılığıyla kullanabilirsiniz.

### Değiştirilmiş PSD dosyalarımı hangi formatta kaydedebilirim?
PSD dosyalarını tekrar PSD olarak kaydedebilir veya PNG, JPEG gibi diğer formatlara dışa aktarabilirsiniz.

### Aspose.PSD için ücretsiz deneme mevcut mu?
Evet, Aspose.PSD'nin ücretsiz deneme sürümüne erişebilir ve özelliklerini test edebilirsiniz. [Ücretsiz deneme bağlantısı](https://releases.aspose.com/) ziyaret edin.

### Aspose.PSD için nasıl destek alabilirim?
Destek ve sorun giderme yardımı için [Aspose forumuna](https://forum.aspose.com/c/psd/34) katılabilirsiniz.

## Sık Sorulan Sorular
**Q:** **Mevcut bir katmana yeni bir vektör maskesi nasıl eklenir?**  
**A:** Bir `VmskResource` oluşturun, gerekli yol kayıtlarıyla (ör. `BezierKnotRecord`) doldurun ve katmanın kaynak koleksiyonuna ekleyin.

**Q:** **Düzenlenmiş PSD'yi doğrudan PNG'ye Photoshop açmadan dönüştürebilir miyim?**  
**A:** Evet—PSD'yi kaydettikten sonra `Image.load()` ile tekrar yükleyip `im.save("output.png")` çağrısı yaparak PNG formatını belirtebilirsiniz.

**Q:** **Bunu bir CI/CD boru hattında otomatikleştirmenin bir yolu var mı?**  
**A:** Kesinlikle. Süreç tamamen Java olduğundan Maven/Gradle build'lerine, Docker konteynerlerine veya Java destekli herhangi bir CI sistemine entegre edilebilir.

**Q:** **Aspose.PSD'nin hangi sürümleri Java 11+ ile uyumludur?**  
**A:** Son sürümler (2024‑2025) Java 8 ve üzeri, özellikle Java 11, 17 ve yeni LTS sürümlerini destekler.

**Q:** **Geliştirme build'leri için lisans gerekir mi?**  
**A:** Geliştirme ve test için ücretsiz değerlendirme lisansı yeterlidir. Üretim dağıtımları için ticari lisans gereklidir.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-18  
**Test Edilen:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

---