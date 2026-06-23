---
date: 2026-06-23
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak kaydetmeyi, eksik yazı
  tiplerini değiştirmeyi ve görüntüleri dışa aktarmayı öğrenin – eksik yazı tipli
  PSD dosyalarını hızlı bir şekilde yönetin.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: Yazı Tiplerini Değiştir
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Java'da Aspose ile PSD'yi PNG Olarak Kaydetme ve Eksik Yazı Tiplerini Değiştirme
url: /tr/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# psd'yi png olarak kaydet – Java'da Eksik Yazı Tiplerini Değiştir

## Giriş

Photoshop (PSD) dosyası içinde eksik veya istenmeyen yazı tiplerini değiştirirken **PSD'yi PNG olarak kaydetmeniz** gerekiyorsa, Aspose PSD yazı tipi ikamesi bunu zahmetsiz hâle getirir. Java uygulamalarında bir PSD yükleyebilir, Aspose'a hangi yedek yazı tipinin kullanılacağını söyleyebilir ve ardından düzeltilmiş görüntüyü istediğiniz herhangi bir formatta dışa aktarabilirsiniz. Bu öğretici, proje kurulumundan güncellenmiş PNG'nin dışa aktarılmasına kadar tam iş akışını adım adım gösterir—böylece Photoshop açmadan **eksik yazı tiplerini PSD** senaryolarını güvenilir bir şekilde ele alabilirsiniz.

## Hızlı Yanıtlar
- **Yazı tipi ikamesini hangi kütüphane yönetir?** Aspose.PSD for Java  
- **Uygulamanın süresi ne kadar?** Temel bir senaryo için yaklaşık 5‑10 dakika  
- **Varsayılan yedek yazı tipi olarak hangisi kullanılır?** Herhangi bir TrueType yazı tipini ayarlayabilirsiniz, ör. “Arial”  
- **PNG dışındaki formatlarda kaydedebilir miyim?** Evet – PSD, JPEG, BMP ve daha fazlası desteklenir  
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için geçerli bir Aspose.PSD lisansı gereklidir  

## Aspose PSD Yazı Tipi İkamesi Nedir?

Aspose PSD font substitution, kütüphanenin bir PSD dosyasında eksik veya desteklenmeyen bir yazı tipiyle karşılaştığında kullanacağı ikame yazı tipini belirleme sürecidir. Bu, metin katmanlarının Photoshop'ta manuel düzenleme yapmadan doğru şekilde render edilmesini sağlar ve **eksik yazı tiplerini PSD** dosyalarını otomatik olarak ele almanıza olanak tanır.

## Neden Aspose.PSD for Java Kullanmalı?

Aspose.PSD for Java, Photoshop dosyalarıyla doğrudan Java kodundan çalışmak için kapsamlı, yüksek performanslı bir çözüm sunar ve Photoshop'a olan ihtiyacı ortadan kaldırır. Çeşitli katman tipleri, efektler ve büyük dosya boyutlarını desteklerken, yazı tipi ikamesi, görüntü dönüştürme ve meta veri işleme gibi görevler için basit API'ler sağlar.

- **Tam özellikli PSD işleme** – Aspose.PSD, **30+ katman tipi**, **20+ efekt** destekler ve **2 GB**'a kadar dosyaları belgenin tamamını belleğe yüklemeden işleyebilir.  
- **Çapraz platform** – Java 8+ destekleyen herhangi bir işletim sisteminde çalışır.  
- **Harici bağımlılık yok** – kütüphane yazı tipi ikamesini dahili olarak yönetir, böylece uygulamanızla ekstra yazı tipleri göndermenize gerek kalmaz.  

## Aspose PSD Kullanarak PSD'de Eksik Yazı Tiplerini Nasıl Değiştirilir

Eksik yazı tiplerini değiştirmek için önce PSD'yi yükleme seçeneklerinde tanımlı bir yedek yazı tipiyle yüklersiniz, ardından görüntüyü render eder veya kaydedersiniz. Kütüphane, eksik yazı tiplerini otomatik olarak belirttiğiniz yazı tipiyle ikame eder ve görsel çıktının manuel düzenleme olmadan beklentilerinize uymasını sağlar.

## Ön Koşullar

- **Java Development Kit (JDK)** – 8 veya daha yüksek bir sürüm yüklü.  
- **Aspose.PSD for Java** – en son JAR dosyasını [release page](https://releases.aspose.com/psd/java/) adresinden indirin.  
- **Bir IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  

## Paketleri İçe Aktar

`PsdImage` sınıfı, bellekte bir Photoshop belgesini temsil eder ve katmanlara, metne ve render yeteneklerine erişim sağlar. `PsdLoadOptions` dosyanın nasıl okunacağını, yedek yazı tipini dahil ederek kontrol eder, `SaveOptions` (veya format‑spesifik alt sınıflar) ise görüntünün nasıl yazılacağını tanımlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Adım 1: Belge Dizinini Ayarlayın

Kaynak PSD dosyasını içeren klasörü belirtin. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

`File` nesnesi sadece işlemek istediğiniz PSD'ye işaret eder; burada ek bir yapılandırma gerekmez.  

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Görüntüyü Değiştirme Yazı Tipiyle Yükleyin

`PsdLoadOptions` bir örnek oluşturun, varsayılan değiştirme yazı tipini (ör. **Arial**) ayarlayın ve PSD'yi yükleyin. Aspose, eksik bir yazı tipiyle karşılaştığında yedek yazı tipini otomatik olarak uygular.

`PsdLoadOptions`, yükleme davranışını tanımlamanıza izin verir; bu, içe aktarma aşamasında eksik herhangi bir yazı tipini ikame eden yedek yazı tipini içerir.  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Adım 3: Değiştirilen Görüntüyü PNG Olarak Kaydedin

Yazı tipi ikamesinden sonra görüntüyü herhangi bir desteklenen formatta dışa aktarabilirsiniz. Burada PNG olarak kaydediyoruz, ancak JPEG, BMP seçebilir veya hatta PSD'ye geri yazabilirsiniz.

`PsdImage`'in `save` yöntemi bir `SaveOptions` nesnesi alır; `PngOptions` kullanmak, çıktının web veya sonraki işlemler için uygun kayıpsız bir PNG olmasını sağlar.  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Yazı tiplerini değiştirdikten sonra PSD'yi PNG olarak nasıl kaydederim?

PSD'yi bir yedek yazı tipiyle yükleyin, ardından `psdImage.save("output.png", new PngOptions())` çağrısını yapın. Bu tek satırlık kaydetme işlemi, ikame edilen yazı tipini yansıtan tam olarak render edilmiş bir PNG yazar ve görüntüyü eksik yazı tipleri hakkında endişelenmeden istediğiniz yere yerleştirmenizi sağlar. Kaydetmeden önce değiştirme yazı tipini uyguladığınızdan emin olun ve isteğe bağlı olarak `PngOptions` nesnesiyle PNG sıkıştırma ayarlarını optimal dosya boyutu için ayarlayın.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| Değiştirme sonrası metin bozuk görünüyor | Yedek yazı tipi gerekli glifleri içermiyor | Gerekli Unicode aralığını destekleyen bir yazı tipi seçin (ör. “Arial Unicode MS”). |
| `OutOfMemoryError` büyük PSD'lerde | Yeterli heap olmadan çok yüksek çözünürlüklü bir dosya yükleniyor | JVM heap boyutunu (`-Xmx2g`) artırın veya mümkünse görüntüyü akış modunda yükleyin. |
| Lisans istisnası | Deneme sürümünü üretimde kullanmak | Görüntüyü yüklemeden önce geçerli bir kalıcı veya geçici lisans uygulayın. |

## Sıkça Sorulan Sorular

**Q: PSD dışındaki diğer görüntü formatlarında yazı tiplerini değiştirebilir miyim?**  
A: Evet. Birincil kullanım senaryosu PSD olsa da, Aspose.PSD PNG, JPEG, BMP ve TIFF'i de destekler, böylece metin katmanlarının bulunduğu her yerde yazı tipi değişimi yapılabilir.

**Q: Varsayılan değiştirme yazı tipi zorunlu mu?**  
A: Hayır. Tercih ettiğiniz herhangi bir TrueType yazı tipini ayarlayabilirsiniz veya ayarı atlayarak Aspose'un dahili varsayılanını kullanmasına izin verebilirsiniz.

**Q: Aspose.PSD kullanmak için lisans gereksinimleri var mı?**  
A: Üretim dağıtımları için ticari bir lisans gereklidir. Ayrıntılar için [purchase page](https://purchase.aspose.com/buy) adresine bakın.

**Q: Test için geçici bir lisans alabilir miyim?**  
A: Kesinlikle. Aspose değerlendirme için ücretsiz geçici lisanslar sunar – [temporary license page](https://purchase.aspose.com/temporary-license/) adresini ziyaret edin.

**Q: Ek destek bulabileceğim veya Aspose.PSD ile ilgili konuları tartışabileceğim yer neresi?**  
A: Topluluk forumu sorular sormak için harika bir yerdir: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Birden fazla eksik yazı tipi içeren PSD dosyalarını nasıl ele alırım?**  
A: Varsayılan değiştirme yazı tipini bir kez ayarlayın (gösterildiği gibi) – bu, yükleme işlemi sırasında *tüm* eksik yazı tiplerine uygulanacaktır.

**Q: Görüntü kaydedildikten sonra yazı tiplerini değiştirmek mümkün mü?**  
A: Yazı tipi ikamesi yükleme aşamasında gerçekleşmelidir. Yazı tiplerini daha sonra değiştirmek için PSD'yi farklı bir değiştirme yazı tipiyle yeniden yükleyin ve tekrar kaydedin.

## Sonuç

Artık Java'da tam bir **psd'yi png olarak kaydet** iş akışını gördünüz—doğru sınıfları içe aktarmaktan, yedek bir yazı tipi yapılandırmaya, PSD'yi yüklemeye ve düzeltilmiş PNG'yi dışa aktarmaya kadar. Bu deseni görüntü işleme hatlarınıza entegre ederek tüm PSD varlıklarınızda tutarlı tipografi sağlayabilir ve **eksik yazı tiplerini PSD** otomatik olarak ele alabilirsiniz.

---

**Son Güncelleme:** 2026-06-23  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım anındaki en son)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.PSD for Java'da Eksik Yazı Tiplerini Değiştirme Ayarları](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Aspose.PSD for Java'da PSD'yi PNG Olarak Kaydet ve Rendering Drop Shadow Uygula](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java ile PSD'yi PNG'ye Dönüştürme ve Orantılı Yeniden Boyutlandırma](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}