---
date: 2026-03-23
description: Aspose.PSD for Java kullanarak bir resmi PSD olarak kaydetmeyi öğrenin.
  PSD renk modunu ayarlama, bitmap'i PSD'ye dönüştürme ve görüntüleri programlı olarak
  dışa aktarma adım adım rehberi.
linktitle: Export Images to PSD Format with Java
second_title: Aspose.PSD Java API
title: Java ile Aspose.PSD kullanarak Görüntüyü PSD olarak Kaydetme
url: /tr/java/psd-image-modification-conversion/export-images-psd-format/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile Aspose.PSD Kullanarak Görüntüyü PSD Olarak Kaydetme

## Java ile Görüntüyü PSD Olarak Kaydetme

Bu öğreticide, Java ve Aspose.PSD kütüphanesini kullanarak **görüntüyü PSD olarak kaydetmeyi** öğreneceksiniz. Katmanlı Photoshop dosyalarıyla çalışmak birçok grafik‑tasarım geliştiricisinin günlük görevidir ve PSD dosyalarının oluşturulmasını otomatikleştirmek iş akışlarını büyük ölçüde hızlandırabilir. PSD renk modunu ayarlamayı, bir bitmap oluşturmayı ve bu bitmap'i PSD dosyasına dönüştürmeyi adım adım göstereceğiz—başlamanız için ihtiyacınız olan her şey. Hadi başlayalım!

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java (resmi siteden indirilebilir).  
- **Renk modunu ayarlayabilir miyim?** Evet – RGB, CMYK vb. seçmek için `PsdOptions.setColorMode()` kullanın.  
- **Bitmap'i PSD'ye dönüştürme destekleniyor mu?** Kesinlikle; boyutlardan veya mevcut bir bitmap'ten `PsdImage` oluşturup kaydedebilirsiniz.  
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için ticari bir lisans gereklidir.  
- **Hangi Java sürümü gerekiyor?** Java 8 veya üzeri.

## “Görüntüyü PSD Olarak Kaydet” Nedir?

Bir görüntüyü PSD olarak kaydetmek, raster bir grafiği Adobe Photoshop'un yerel katmanlı formatına dışa aktarmak anlamına gelir. Bu, sonraki araçların (Photoshop, GIMP vb.) katmanları, kanalları ve düzenlenebilirliği korumasını sağlar. Aspose.PSD ile Photoshop'u hiç açmadan programatik olarak PSD dosyaları oluşturabilirsiniz.

## Neden Aspose.PSD for Java Kullanmalı?

- **Tam kontrol** renk modları, sıkıştırma ve Photoshop sürüm uyumluluğu üzerinde.  
- **Harici bağımlılık yok** – saf Java, sunucu‑tarafı render için ideal.  
- **Yüksek performans** – binlerce görüntünün toplu işlenmesi için uygun.  

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Temel Java bilgisi** – Java programlarını derleyip çalıştırma konusunda rahat olmalısınız.  
2. **Aspose.PSD for Java kütüphanesi** – [buradan indirebilirsiniz](https://releases.aspose.com/psd/java/).  
3. **Java Development Kit (JDK)** – Makinenizde JDK 8 veya daha yeni bir sürüm yüklü olmalı.  
4. **IDE veya Metin Düzenleyici** – IntelliJ IDEA, Eclipse, VS Code veya tercih ettiğiniz herhangi bir düzenleyici.  
5. **Görüntü kavramları hakkında anlayış** – renk modları, sıkıştırma ve bitmap temelleri yardımcı olur ancak zorunlu değildir.

Her şey hazır mı? Harika, devam edelim.

## Paketleri İçe Aktarma

İlk olarak, Aspose.PSD kütüphanesinden ihtiyacımız olan sınıfları içe aktarın:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

Bu içe aktarmalar, çizim yardımcıları, renk işleme ve PSD‑özel seçeneklerine erişim sağlar.

## Adım 1: Belge Dizinini Başlatma

Oluşturulan PSD dosyasının kaydedileceği yeri tanımlayın:

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini projenizdeki `"C:/Images/"` gibi mutlak bir yol ya da göreli bir yol ile değiştirin.

## Adım 2: Yeni Bir Görüntü Oluşturma (Bitmap'i PSD'ye Dönüştürme)

Şimdi, daha sonra **bitmap'i PSD'ye dönüştürmek** için PSD seçenekleriyle kaydedeceğimiz boş bir bitmap oluşturuyoruz:

```java
PsdImage bmpImage = new PsdImage(300, 300);
```

`300, 300` değerlerini ihtiyacınıza uygun boyutlarla değiştirmekten çekinmeyin.

## Adım 3: Görüntü Verisini Doldurma

Bitmap'e bazı grafikler ekleyin, böylece ortaya çıkan PSD sadece boş bir tuval olmaz:

```java
Graphics graphics = new Graphics(bmpImage);
graphics.clear(Color.getWhite());
Pen pen = new Pen(Color.getBrown());
graphics.drawRectangle(pen, bmpImage.getBounds());
```

- `graphics.clear(Color.getWhite())` tüm tuvali beyaz renkle doldurur.  
- Kahverengi kalem, görüntü sınırlarını çizen bir dikdörtgen çizer.

## Adım 4: PSD Seçeneklerini Ayarlama (PSD Renk Modunu Ayarlama)

Burada dosyanın nasıl kaydedileceğini yapılandırıyoruz. **PSD renk modunu** RGB olarak ayarladığımız, sıkıştırmayı seçtiğimiz ve Photoshop sürümünü belirttiğimiz yer:

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setColorMode(ColorModes.Rgb);
psdOptions.setCompressionMethod(CompressionMethod.Raw);
psdOptions.setVersion(4);
```

- `ColorModes.Rgb` – web ve ekran grafikleri için en yaygın olanı.  
- `CompressionMethod.Raw` – en yüksek kalite için sıkıştırma olmadan piksel verisini saklar.  
- `setVersion(4)` – dosyayı geniş uyumluluğa sahip Photoshop 4.0 formatında kaydeder.

## Adım 5: Görüntüyü Kaydetme

Son olarak, bitmap'i PSD dosyası olarak dışa aktarın—bu, temel **görüntüyü PSD olarak kaydet** işlemdir:

```java
bmpImage.save(dataDir + "ExportImageToPSD_output.psd", psdOptions);
```

`ExportImageToPSD_output.psd` dosyası belirttiğiniz dizinde görünecektir.

## Yaygın Kullanım Senaryoları

- **Otomatik rapor oluşturma**; grafiklerin Photoshop'ta düzenlenebilir olması gereken durumlar.  
- **Toplu dönüşüm**; katman gerektiren tasarımcılar için PNG/JPEG varlıklarını PSD'ye dönüştürme.  
- **Sunucu‑tarafı görüntü birleştirme**; müşterilere PSD şablonları sunan web hizmetleri için.

## Yaygın Sorunlar ve Çözümler

| Issue | Solution |
|-------|----------|
| **Dosya bulunamadı** hatası kaydedilirken | `dataDir` değişkeninin bir yol ayırıcı (`/` veya `\\`) ile bittiğini ve klasörün var olduğunu doğrulayın. |
| **Boş görüntü** kaydettikten sonra | Kaydetmeden önce `graphics.clear()` çağırdığınızdan ve bir şeyler çizdiğinizden emin olun. |
| **Desteklenmeyen renk modu** | CMYK çıktısına ihtiyacınız varsa `ColorModes.Cmyk` kullanın; grafiklerinizi buna göre ayarlamayı unutmayın. |
| **LicenseException** çalışma zamanında | Geçerli bir Aspose.PSD lisansı kurun veya deneme modunda çalıştırın (değerlendirme filigranı görünebilir). |

## Sıkça Sorulan Sorular

**Q:** Aspose.PSD for Java nedir?  
**A:** Aspose.PSD for Java, geliştiricilerin Adobe Photoshop kullanmadan Photoshop PSD dosyalarını oluşturmasını, düzenlemesini, dönüştürmesini ve render etmesini sağlayan güçlü bir API'dir.

**Q:** Mevcut bir PSD dosyasını değiştirebilir miyim?  
**A:** Evet, `new PsdImage("input.psd")` ile mevcut bir PSD'yi açabilir, değişiklikler yapabilir ve tekrar kaydedebilirsiniz.

**Q:** Ücretsiz bir deneme sürümü mevcut mu?  
**A:** Kesinlikle! Aspose.PSD'nin ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

**Q:** Daha fazla belgeyi nerede bulabilirim?  
**A:** Aspose.PSD kullanımını daha ayrıntılı öğrenmek için kapsamlı [belgelere](https://reference.aspose.com/psd/java/) göz atabilirsiniz.

**Q:** Sorunlarla karşılaştığımda nasıl destek alabilirim?  
**A:** Destek için [Aspose forumunu](https://forum.aspose.com/c/psd/34) ziyaret edebilirsiniz.

## Sonuç

Artık Java ile **görüntüyü PSD olarak kaydetmeyi**, **PSD renk modunu ayarlamayı** ve Aspose.PSD kullanarak **bitmap'i PSD'ye dönüştürmeyi** biliyorsunuz. Bu yaklaşım, Photoshop dosyaları üzerinde tam programatik kontrol sağlar, otomatik tasarım hatları, dinamik görüntü üretimi ve mevcut Java uygulamalarıyla sorunsuz entegrasyon için kapılar açar. Farklı renk modları, boyutlar ve çizim işlemleriyle deney yaparak PSD dosyalarını tam ihtiyacınıza göre özelleştirin.

---

**Last Updated:** 2026-03-23  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}