---
date: 2026-08-01
description: Aspose.PSD for Java ile PSD'yi PNG'ye nasıl dönüştüreceğinizi ve sıkıştırılmamış
  görüntü akışlarını nasıl yöneteceğinizi öğrenin.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: PSD'de Sıkıştırılmamış Görüntü Akışı Nesnesini İşleyin – Java
og_description: Aspose.PSD for Java kullanarak psd'yi png'ye dönüştürün. Sıkıştırılmamış
  görüntü akışlarını yönetmeyi, grafik nesneleri oluşturmayı ve yüksek kaliteli PNG'ler
  kaydetmeyi öğrenin.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: psd'yi png'ye dönüştür – Sıkıştırılmamış PSD akışları için Java rehberi
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: PSD'yi PNG'ye Dönüştür – PSD Grafik Nesnesi Oluştur – Java'da Sıkıştırılmamış
  Akış
url: /tr/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dışa Aktar – PSD Grafik Nesnesi Oluştur – Java'da Sıkıştırılmamış Akış

## Giriş
Bu adım adım rehberde, Aspose.PSD for Java kullanarak sıkıştırılmamış bir görüntü akışıyla çalışırken **PSD'yi PNG'ye dışa aktaracaksınız**. Tasarım hattını otomatikleştiriyor ya da özel bir editör oluşturuyorsanız, Photoshop dosyasını kalite kaybı olmadan renderleyebilme yeteneği çok önemlidir. Gerekli kurulumu yaparak başlayacağız, bir `Graphics` nesnesi oluşturmayı adım adım inceleyecek ve kayıpsız bir PNG dışa aktarımıyla sonlandıracağız. Sonunda, Aspose.PSD'nin ham akışları neden verimli bir şekilde işlediğini ve bunu herhangi bir Java projesine nasıl entegre edeceğinizi anlayacaksınız.

## Hızlı Yanıtlar
- **“create PSD graphics object” ne anlama geliyor?** Bu, bir PSD görüntüsü üzerinde programlı olarak çizim yapmanıza veya değiştirmenize izin veren bir `Graphics` bağlamı oluşturmak anlamına gelir.  
- **Hangi kütüphane sıkıştırılmamış akışları yönetir?** Aspose.PSD for Java, ham (sıkıştırılmamış) görüntü verileri için tam destek sağlar.  
- **Düzenleme sonrası PSD'yi PNG'ye dışa aktarabilir miyim?** Evet—bir `Graphics` nesnesine sahip olduğunuzda PSD'yi renderleyebilir ve tek bir çağrıyla PNG olarak kaydedebilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim dağıtımları için ticari lisans gereklidir.  
- **Dışa aktarım kayıpsız mı?** PNG'ye dışa aktarma, orijinal piksel verilerini korur ve ham PSD'ye göre daha küçük dosya boyutuyla kayıpsız kalite sunar.

## PSD'yi PNG'ye dışa aktarmak nedir?
PSD'yi PNG'ye dışa aktarmak, katmanlı bir Photoshop belgesini tek katmanlı, kayıpsız bir raster görüntüye dönüştürür; bu görüntü herhangi bir web tarayıcısı veya görüntüleyici tarafından görüntülenebilir. İşlem, şeffaflığı, renk derinliğini ve katman efektlerini korurken Photoshop'a özgü meta verileri atar. Ayrıca doğru renk üretimi için orijinal renk profilini de korur.

## Görüntü işleme için Aspose.PSD for Java neden kullanılmalı?
Aspose.PSD, **50+** giriş ve çıkış formatını destekler—PSD, PNG, JPEG, BMP ve TIFF dahil—ve **200+ katman** içeren dosyaları belgenin tamamını belleğe yüklemeden işleyebilir. `Raw` sıkıştırma seçeneği piksel verilerini sıkıştırılmadan saklar ve sonraki düzenleme veya arşivleme için piksel‑tam doğruluk garantiler.

## Önkoşullar
Koda başlamadan önce aşağıdakilere sahip olduğunuzu doğrulayın:

- **Java Development Kit (JDK)** – JDK 8 veya daha yeni bir sürüm yüklü.  
- **Aspose.PSD for Java** – En son JAR dosyasını resmi sürüm sayfasından indirin: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). Ayrıca [this link](https://releases.aspose.com/psd/java/) veya [release page](https://releases.aspose.com/psd/java/) üzerinden erişebilirsiniz. Diğer Aspose ürünleri için [here](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse veya herhangi bir Java uyumlu editör.  
- **Temel Java bilgisi** – sınıflar, metodlar ve istisna yönetimi konusunda aşinalık.

Bu koşullar sağlandığında kodlamaya başlayabilirsiniz.

## Paketleri İçe Aktar
`Graphics` sınıfı, Aspose.PSD'nin doğrudan piksel verilerini renderlemenize veya düzenlemenize izin veren çizim yüzeyidir. `PsdImage` sınıfı bellekte bir PSD dosyasını temsil eder, `PsdOptions` ise görüntünün nasıl kaydedileceğini kontrol eder.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Şimdi kodu sindirilebilir adımlara ayıralım, böylece kolayca takip edebilirsiniz. Ortamı kuracağız, bir PSD dosyasını yükleyecek, üzerinde değişiklik yapacak ve sonunda çıktıyı kaydedeceğiz.

## Adım 1: Belge Dizinini Tanımlayın
Herhangi bir dosya işlemi yapmadan önce programın PSD varlıklarınızı nerede arayacağını belirtmeniz gerekir. Bu dizin yolu eğitim boyunca kullanılacaktır.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini `layers.psd` dosyasını içeren mutlak yol ile değiştirin. Yolu yapılandırılabilir tutmak, kodun projeler arasında yeniden kullanılabilir olmasını sağlar.

## Adım 2: Byte Array Output Stream Oluşturun
`ByteArrayOutputStream`, verileri bellek içinde bir bayt dizisi olarak tutan bir Java akışıdır. Değiştirilen görüntü için bellek içi bir tampon görevi görür ve ham baytları diske yazmadan veya ağa göndermeden önce yakalamanıza olanak tanır.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

`ms` değişkeni, `save` işlemi sonrasında sıkıştırılmamış görüntü verilerini tutacaktır.

## Adım 3: PSD Dosyasını Yükleyin
`PsdImage` sınıfı, bir PSD dosyasını manipülasyon için belleğe yükler. Dosyanın yüklenmesi, diskteki PSD'yi bir `PsdImage` nesnesine dönüştürür; bu nesne üzerinde değişiklik yapabilirsiniz. Bu adımda Aspose.PSD dosya başlığını, katmanları ve kaynakları okur.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Yol hatalıysa, Aspose.PSD bir `FileNotFoundException` fırlatır; bu, üretim kodunda yakalanmalıdır.

## Adım 4: Kaydetme İçin PsdOptions Ayarlayın
`PsdOptions`, PSD dosyaları için kaydetme parametrelerini belirler. Sıkıştırma yöntemini `Raw` olarak ayarlamak, piksel verilerinin sıkıştırma olmadan saklanacağını, bellekte göründüğü gibi her pikselin tam olarak korunacağını gösterir.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

`CompressionMethod.Raw` seçeneği piksel verilerini hiçbir sıkıştırma olmadan saklar; bu, daha sonra ek düzenlemeler yapmayı planladığınızda idealdir.

## Adım 5: Görüntüyü Çıktı Akışına Kaydedin
Şimdi PSD'yi (herhangi bir değişiklikle birlikte) önceden oluşturulmuş `ByteArrayOutputStream` içine kalıcı hale getiriyoruz. `save` metodu, yapılandırdığınız `PsdOptions` değerlerine saygı gösterir.

```java
psdImage.save(ms, saveOptions);
```

Bu noktada, `ms` sıkıştırılmamış PSD'nin tam ikili temsilini içerir.

## Adım 6: Çıktı Akışını Sıfırla
Yazma işleminden sonra akışın iç göstergesi son konumda durur. Sıfırlamak, akışı başa sarar, böylece baştan okuyabilirsiniz.

```java
ms.reset();
```

Bunu, oynatmadan önce kaset kafasını başa döndürmek gibi düşünün.

## Adım 7: Yeni Oluşturulan Görüntüyü Yükleyin
Artık bayt dizisinden doğrudan yeni bir `PsdImage` örneği oluşturabilirsiniz. Bu adım, kaydedilen verilerin bozulmadan yeniden yüklenebildiğini doğrular.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Görüntü sorunsuz yüklenirse, sıkıştırılmamış akışın doğru şekilde yazıldığını bilirsiniz.

## Adım 8: Graphics Nesnesi Oluşturun
`Graphics` sınıfı, Aspose.PSD'nin çizim tuvalidir. Bir `PsdImage`'ın piksel matrisine doğrudan şekil, metin çizme ve filtre uygulama metodları sağlar.

```java
Graphics graphics = new Graphics(psdImage);
```

Bu `Graphics` örneğiyle yeni içerik boyayabilir, bölümleri silebilir veya ek katmanlar birleştirebilirsiniz.

## Aspose.PSD for Java kullanarak PSD'yi PNG'ye nasıl dışa aktarırım?
PSD'yi `new PsdImage(dataDir + "layers.psd")` ile yükleyin, bir `Graphics` nesnesi oluşturun, ihtiyacınız olan çizimleri yapın, ardından `psdImage.save("output.png", new PngOptions())` çağrısını yapın. Bu sıralama, düzenlenmiş PSD'yi renderler ve tek adımda kayıpsız bir PNG yazar; Aspose.PSD'nin yerleşik dönüşüm motorundan faydalanır.

## Graphics Nesnesi ile PSD Katmanlarını Manipüle Edin
Bir `Graphics` örneğine sahip olmak, her katman üzerinde piksel‑seviyesinde kontrol sağlar. Geometrik şekiller çizebilir, metin renderleyebilir veya özel filtreler uygulayabilirsiniz. Grafik bağlamı katmanın rasterleştirilmiş görünümünde çalıştığı için, değişiklikler görüntüyü kaydettiğinizde anında görülür.

## Yaygın Sorunlar ve Çözümler
- **Dosya yüklenirken NullPointerException** – `dataDir` yolunu iki kez kontrol edin ve dosya adının büyük/küçük harf duyarlılığı dahil tam olarak eşleştiğinden emin olun.  
- **Raw kullanmasına rağmen sıkıştırılmış çıktı** – `saveOptions.setCompressionMethod(CompressionMethod.Raw);` ifadesinin `save` çağrısından **önce** yapıldığını doğrulayın.  
- **Graphics nesnesi boş görünüyor** – doğru `PsdImage` örneği üzerinde (yüklediğiniz, yeni oluşturulmuş boş bir görüntü değil) çizim yaptığınızdan emin olun.  
- **Büyük dosyalarda OutOfMemoryError** – `PsdImage.load(dataDir, LoadOptions)` ile `loadOptions.setLoadMode(LoadMode.Memory)` kullanarak belgeyi tamamen belleğe yüklemeden büyük dosyaları akış olarak işleyin.

## SSS

### Aspose.PSD nedir?
Aspose.PSD, geliştiricilerin Adobe Photoshop gerektirmeden programlı olarak Photoshop PSD dosyaları oluşturmasını, düzenlemesini ve dönüştürmesini sağlayan bir Java kütüphanesidir. PSD dosyalarını okuma ve yazma, katmanlar, maskeler, kanallar ve çeşitli görüntü kaynaklarını yönetme desteği sunar; raster ve vektör işlemleri için API'ler sağlar ve sunucu‑tarafı görüntü işleme ve otomasyon görevleri için uygundur.

### Aspose.PSD for Java'ı nasıl indirebilirim?
Resmi sürüm sayfasından indirebilirsiniz: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Aspose.PSD için ücretsiz deneme sürümü var mı?
Evet, aynı indirme sayfasında tam işlevsel bir deneme sürümü mevcuttur. Geliştirme ve değerlendirme amaçları için çalışır.

### Aspose.PSD için destek alabilir miyim?
Kesinlikle! Aspose destek forumu, ürün ekibi ve topluluktan yanıtlar sağlar: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### Aspose.PSD için geçici bir lisans nasıl alabilirim?
Aspose'un lisans portalından doğrudan geçici bir lisans talep edebilirsiniz; bu portal 30 gün geçerli bir zaman‑sınırlı anahtar sunar. Bu, ticari bir lisans satın almadan Aspose.PSD'nin tam işlevselliğini değerlendirmenizi sağlar. Deneme süresi sonunda, kütüphaneyi üretimde kullanmaya devam etmek için geçici anahtarı kalıcı bir lisansla değiştirmeniz gerekir. Zaman‑sınırlı bir anahtar oluşturmak için geçici lisans portalını ziyaret edin: [temporary license page](https://purchase.aspose.com/temporary-license/).

## Sıkça Sorulan Sorular

**Q: Graphics nesnesini yalnızca belirli bir katmanı düzenlemek için kullanabilir miyim?**  
A: Evet. PSD'yi yükledikten sonra istenen katmanı `psdImage.getLayers().get_Item(index)` ile alıp bu katmanı `Graphics` yapıcısına geçirebilirsiniz.

**Q: Raw sıkıştırma yöntemi dosya boyutunu etkiler mi?**  
A: Raw, piksel verilerini hiçbir sıkıştırma olmadan saklar; bu nedenle ortaya çıkan dosya sıkıştırılmış bir PSD'den daha büyük olur, ancak %100 piksel doğruluğu garantiler.

**Q: Düzenlenmiş PSD'yi başka bir formata (ör. PNG) dışa aktarmak mümkün mü?**  
A: Kesinlikle. Düzenlemeden sonra `psdImage.save("output.png", new PngOptions())` çağrısını yapın—bu, **PSD'yi PNG'ye dışa aktarmanın** kayıpsız kaliteyle standart yoludur.

**Q: Hangi Java sürümü gereklidir?**  
A: Aspose.PSD for Java, JDK 8 ve üzerini destekler; JDK 21'e kadar tüm LTS sürümlerini kapsar.

**Q: İşlem sonrası kaynakları nasıl serbest bırakırım?**  
A: `psdImage.dispose()` metodunu çağırın ve tüm akışları (ör. `ms.close()`) kapatın; bu, yerel belleği serbest bırakır ve sızıntıları önler.

---

**Son Güncelleme:** 2026-08-01  
**Test Edilen:** Aspose.PSD for Java (latest release)  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [Aspose.PSD for Java ile Görüntüleri Akışa Kaydet](/psd/java/advanced-techniques/save-images-to-stream/)
- [Java ile PSD Katman Grubunu Görüntüye Dışa Aktar](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Aspose.PSD for Java'da Akış Kullanarak Görüntü Oluştur](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}