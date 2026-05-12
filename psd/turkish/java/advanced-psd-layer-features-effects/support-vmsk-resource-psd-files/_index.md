---
date: 2026-02-22
description: Aspose.PSD for Java kullanarak vektör maskesi Java oluşturmayı, vektör
  maskesi PSD eklemeyi ve Vmsk kaynaklarını programlı olarak manipüle etmeyi öğrenin.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Java ile Vektör Maskesi Oluştur – PSD Dosyalarındaki Vmsk Kaynağı
url: /tr/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java’da Vektör Maskesi Oluşturma – PSD Dosyalarındaki Vmsk Kaynağı

## Giriş
Eğer Photoshop (PSD) dosyaları içinde **create vector mask** (Vmsk) kaynakları oluşturmanız gerekiyorsa, Aspose.PSD for Java bunu temiz ve programatik bir şekilde yapmanızı sağlar. İster bir tasarım‑otomasyon aracı oluşturuyor olun, ister mevcut bir grafik boru hattına özel maske desteği ekliyor olun, bu öğretici sizi her adımda yönlendirir—PSD'yi yükleme, Vmsk kaynağını okuma, özelliklerini ayarlama ve sonucu kaydetme. Sonuna geldiğinizde, vektör maskeleriyle rahatça çalışabilecek, PSD'yi PNG'ye dönüştürebilecek ve dosyayı ek vektör verileriyle genişletebileceksiniz—hepsi **create vector mask java** teknikleriyle.

## Hızlı Cevaplar
- **Vmsk kaynağı nedir?** Bir PSD dosyası içinde depolanan vektör maskesi verisidir ve bir katman için karmaşık vektör şekilleri tanımlar.  
- **Hangi kütüphane bunu destekler?** Aspose.PSD for Java, Vmsk kaynaklarına tam okuma/yazma erişimi sağlar.  
- **Lisans gerekir mi?** Ücretsiz deneme mevcuttur; üretim kullanımı için ticari lisans gereklidir.  
- **Düzenlenmiş PSD'yi PNG'ye dönüştürebilir miyim?** Evet—kaydedildikten sonra PSD'yi yükleyip aynı API ile PNG olarak dışa aktarabilirsiniz.  
- **Maven desteği mevcut mu?** Kesinlikle; Aspose.PSD bir Maven bağımlılığı olarak eklenebilir (bkz. “aspose psd maven” anahtar kelimesi).

## Vektör Maskesi (Vmsk Kaynağı) nedir?
Bir vektör maskesi (Vmsk), bir katmanda şeffaf ve opak bölgeleri tanımlamak için Bézier eğrileri ve yol kayıtları kullanan piksel‑temelli olmayan bir maskedir. Vektör‑tabanlı olduğu için kalite kaybı olmadan ölçeklenir—yüksek çözünürlüklü grafikler için mükemmeldir.

## Aspose.PSD ile Neden Vektör Maskesi Oluşturmalısınız?
- **Otomasyon:** Photoshop açmadan maskeleri programatik olarak ekleyebilir veya değiştirebilirsiniz.  
- **Tutarlılık:** Oluşturduğunuz her PSD'nin aynı maske kurallarını izlediğinden emin olun.  
- **Çapraz platform:** Java'yı destekleyen herhangi bir işletim sisteminde çalışır.  
- **Entegrasyon:** Diğer Aspose API'leriyle (ör. PSD → PNG dönüştürme) birleştirerek uçtan uca iş akışları oluşturabilirsiniz.  
- **Ölçeklenebilirlik:** Vektör maskeler her boyutta net kalır, bu da onları duyarlı tasarımlar için ideal kılar.

## Java Geliştiricileri için Bunun Önemi Nedir
**create vector mask java** tekniklerini kullanarak gelişmiş grafik mantığını doğrudan arka‑uç hizmetlerine, CI boru hatlarına veya masaüstü yardımcı programlara gömebilirsiniz. Artık bir tasarımcının maskeleri manuel eklemesi gerekmez; kodunuz bunları anında üretebilir veya ayarlayabilir, zaman kazandırır ve insan hatasını azaltır.

## Önkoşullar
Koda geçmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

### Gerekli Araçlar
- **Java Development Kit (JDK):** Makinenizde JDK kurulu olduğundan emin olun. Yoksa, [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-downloads.html) indirebilirsiniz.  
- **Aspose.PSD for Java Library:** PSD dosyalarını yönetmek için güçlü bir kütüphanedir. [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) indirebilirsiniz. Satın almadan önce denemek isteyenler için ayrıca [ücretsiz deneme](https://releases.aspose.com/) seçeneği de vardır.  
- **Bir IDE:** Java için herhangi bir IDE (IntelliJ IDEA, Eclipse vb.) bu proje için yeterlidir.

### Çalışma Alanınızı Kurma
1. **Yeni bir Java Projesi Oluşturun** – Tercih ettiğiniz IDE'yi açın ve yeni bir proje başlatın.  
2. **Aspose Kütüphanesini Ekleyin** – Aspose JAR dosyasını indirdikten sonra, proje derleme yoluna ekleyin, böylece PSD‑ile ilgili tüm sınıflara erişebilirsiniz.

Ortam hazır olduğunda, gerçek uygulamaya geçelim.

## Java ile PSD dosyalarında vektör maskesi nasıl oluşturulur
Aşağıda adım‑adım bir rehber bulacaksınız. Kod blokları orijinal öğreticiden değiştirilmemiştir; sadece her adımı netleştirmek için açıklayıcı metin eklenmiştir.

### Paketleri İçe Aktarın
PSD dosyaları üzerinde çalışabilmek için Aspose.PSD kütüphanesinden gerekli sınıfları içe aktarmamız gerekir.

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

Şimdi sahneyi kurduğumuza göre, her işlemi birlikte inceleyelim.

### Adım 1: PSD Dosyanızı Yükleyin
İlk yapmanız gereken PSD dosyanızı yüklemektir. Burası tüm sihrin başladığı yerdir.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` değişkenini PSD dosyanızın dizinine ayarladık.  
- `sourceFileName` için bir dize oluşturduk, dizini PSD dosyasının adıyla birleştirerek.  
- Son olarak, `Image.load()` kullanarak PSD dosyasını bir `PsdImage` nesnesine yükledik.

### Adım 2: Vmsk Kaynağını Alın
PSD görüntümüz yüklendiğine göre, Vmsk kaynağını alalım.

```java
VmskResource resource = getVmskResource(im);
```

- `getVmskResource()` metodunu çağırıyoruz; bu metod görüntüden Vmsk kaynağını arar ve getirir.

### Adım 3: Vmsk Kaynağı Özelliklerini Doğrulayın
Değişikliklere geçmeden önce, Vmsk kaynağımızın beklenen durumda olduğundan emin olmak önemlidir.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Burada Vmsk kaynağının çeşitli özelliklerini kontrol ediyoruz. Devre dışı bırakılmadığını, ters çevrilmediğini, bağlanmadığını ve doğru sayıda yol içerdiğini doğrulamak istiyoruz.

### Adım 4: Her Yola Erişin ve Doğrulayın
Biraz daha derine inelim ve Vmsk kaynağındaki yolları inceleyelim.

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

- Üç belirli yol kaydını çıkarıyor ve türlerini ve özelliklerini doğruluyoruz; böylece kriterlerimize uyduklarından emin oluyoruz.

### Adım 5: Vmsk Kaynağını Düzenleyin
Şimdi değişiklik kısmına giriyoruz! Vmsk kaynağının özelliklerini ihtiyacınıza göre ayarlayabilirsiniz.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Bu blokta Vmsk kaynağının çeşitli özelliklerini `true` olarak ayarlıyoruz; böylece maskenin PSD dosyasındaki davranışını kontrol edebiliyoruz.

### Adım 6: Bezier Düğüm Noktalarını Değiştirin
Bezier düğümleri vektör yolları için kritiktir. Burada bazı değerleri değiştirelim.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Belirli `BezierKnotRecord` yollarına erişiyor ve noktalarını değiştirerek vektör maskesini yeniden şekillendirebiliyoruz.

### Adım 7: Değiştirilen PSD Dosyasını Kaydedin
Tüm düzenlemeler tamamlandığında, değiştirilen PSD dosyasını kaydetme zamanı.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Dışa aktarılacak PSD dosyasının yolunu ayarlıyoruz ve ardından `im.save()` çağrısıyla bu yeni dosyaya değişiklikleri yazıyoruz.

### Adım 8: Kaynakları Temizleyin
Son olarak, görüntüyü doğru bir şekilde serbest bırakarak kaynakları temizlediğimizden emin olmalıyız.

```java
im.dispose();
```

- İşiniz bittiğinde her zaman kaynakları serbest bırakmak iyi bir uygulamadır. Bu, uygulamanızda bellek sızıntılarını önlemeye yardımcı olur.

## Yaygın Sorunlar ve Çözümleri
| Sorun | Neden Oluşur | Nasıl Çözülür |
|-------|--------------|---------------|
| **`VmskResource` not found** | PSD, bir vektör maske katmanı içermiyor. | Kaynak PSD'nin bir vektör maskesi içerdiğini doğrulayın veya kodu çalıştırmadan önce Photoshop'ta manuel olarak bir maske ekleyin. |
| **`ArrayIndexOutOfBoundsException` on path access** | Beklenen yol kaydı sayısı farklı. | `resource.getPaths().length` değerini inceleyin ve indeks kullanımını buna göre ayarlayın. |
| **License exception** | Geçerli bir Aspose.PSD lisansı olmadan çalıştırılıyor. | `License license = new License(); license.setLicense("Aspose.PSD.lic");` kodu ile deneme ya da satın alınmış bir lisans uygulayın. |
| **Memory leak** | Uzun süren işlemlerde görüntü serbest bırakılmıyor. | `im.dispose()` metodunu her zaman bir `finally` bloğunda çağırın veya mümkünse try‑with‑resources kullanın. |

## Sıkça Sorulan Sorular

**S: Mevcut bir katmana yeni bir vektör maskesi nasıl eklerim?**  
C: Bir `VmskResource` oluşturun, gerekli yol kayıtları (ör. `BezierKnotRecord`) ile doldurun ve katmanın kaynak koleksiyonuna ekleyin.

**S: Düzenlenmiş PSD'yi Photoshop açmadan doğrudan PNG'ye dönüştürebilir miyim?**  
C: Evet—PSD'yi kaydettikten sonra `Image.load()` ile tekrar yükleyin ve `im.save("output.png")` çağrısıyla PNG formatını belirterek kaydedin.

**S: Bunu bir CI/CD boru hattında otomatikleştirmenin bir yolu var mı?**  
C: Kesinlikle. İşlem tamamen Java olduğundan, Maven/Gradle derlemelerine, Docker konteynerlerine veya Java destekleyen herhangi bir CI sistemine entegre edilebilir.

**S: Aspose.PSD'nin hangi sürümleri Java 11+ ile uyumludur?**  
C: 2024‑2025 sürümleri dahil tüm son sürümler Java 8 ve üzerini, Java 11, 17 ve daha yeni LTS sürümlerini destekler.

**S: Geliştirme derlemeleri için lisansa ihtiyacım var mı?**  
C: Ücretsiz değerlendirme lisansı geliştirme ve test için çalışır. Üretim dağıtımları için ticari lisans gereklidir.

---

**Son Güncelleme:** 2026-02-22  
**Test Edilen Sürüm:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}