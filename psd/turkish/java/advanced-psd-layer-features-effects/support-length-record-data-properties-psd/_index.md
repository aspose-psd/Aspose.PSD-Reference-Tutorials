---
date: 2025-12-17
description: Aspose.PSD for Java kullanarak uzunluk kayıt verisi özelliklerini destekleyerek
  PSD vektör şekillerini nasıl değiştireceğinizi öğrenin. Kod örnekleriyle adım adım
  rehber.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: PSD vektör şekillerini nasıl değiştirilir – Java’da Uzunluk Kayıt Veri Özelliklerini
  Destekleme
url: /tr/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'de Uzunluk Kaydı Veri Özelliklerini Destekleme - Java

## Giriş
Eğer programlı olarak **modify PSD vector shapes** yapmanız gerekiyorsa, Aspose.PSD for Java kütüphanesi Photoshop dosyaları üzerinde Java kodunuzdan tam kontrol sağlar. Bu öğreticide, uzunluk kaydı veri özelliklerini desteklemek için bilmeniz gereken her şeyi adım adım inceleyeceğiz—vektor şekil katmanlarını düzenlemek istediğinizde kritik bir adımdır. Sonunda bir PSD dosyasını açabilecek, vektör şekil özelliklerini ayarlayabilecek ve güncellenmiş dosyayı IDE'nizden çıkmadan kaydedebileceksiniz. Hadi başlayalım!

## Hızlı Yanıtlar
- **“modify PSD vector shapes” ne anlama geliyor?** Bir PSD dosyası içindeki vektör tabanlı katmanların geometrisini, yol işlemlerini veya diğer özelliklerini ayarlamak.  
- **Bu işlemi hangi kütüphane yapar?** Aspose.PSD for Java.  
- **Bir lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir şekil değiştirme betiği için yaklaşık 10‑15 dakika.  
- **Ana önkoşullar nelerdir?** Java JDK, Aspose.PSD for Java ve örnek bir PSD dosyası.

## “modify PSD vector shapes” nedir?
PSD vektör şekillerini değiştirmek, temel vektör yol verilerini—örneğin uzunluk kayıtları ve yol işlemleri—değiştirmeyi içerir; böylece şekillerin görsel görünümü buna göre güncellenir. Bu, otomatik grafik boru hatları, toplu işleme veya özel tasarım araçları için özellikle faydalıdır.

## PSD vektör şekillerini değiştirmek için Aspose.PSD for Java neden kullanılmalı?
- **Photoshop gerekmez** – herhangi bir sunucuda PSD dosyalarıyla doğrudan çalışın.  
- **Zengin API** – katmanlara, kaynaklara ve vektör verilerine güçlü tipli sınıflarla erişin.  
- **Çapraz platform** – herhangi bir JDK ile Windows, Linux veya macOS'ta çalıştırın.  
- **Performansa odaklı** – verimli bellek yönetimi ve hızlı kaydetme işlemleri.

## Önkoşullar
1. **Java Development Kit (JDK)** – [Oracle'ın web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin veya tercih ettiğiniz paket yöneticisini kullanın.  
2. **Aspose.PSD for Java** – en son JAR dosyasını [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) edinin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya herhangi bir Java uyumlu editör.  
4. **Bir PSD dosyası** – Photoshop'ta oluşturun veya deneme amaçlı bir örnek PSD alın.  
5. **Temel Java bilgisi** – sınıflar, nesneler ve istisna yönetimi konularına aşina olun.

## Paketleri İçe Aktarma
İlk olarak, PSD dosyaları ve vektör şekil kaynaklarıyla çalışmak için ihtiyaç duyacağınız sınıfları içe aktarın.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Adım 1: Kaynak ve Çıktı Dizinlerinizi Ayarlayın
Orijinal PSD'nin nerede bulunduğunu ve değiştirilmiş dosyanın nereye kaydedileceğini tanımlayın.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Adım 2: PSD Dosyasını Yükleyin
`Image.load` kullanarak dosyayı açın ve PSD‑özel özellikler için `PsdImage` tipine dönüştürün.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Adım 3: Katmandaki Vsms Kaynağını Bulun
Vektör şekil verileri bir `VsmsResource` içinde bulunur. İkinci katmanın kaynakları arasında döngü yaparak onu bulun.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Adım 4: Uzunluk Kayıtlarına Erişin
Her `LengthRecord` ayrı bir vektör yolunu temsil eder. Değiştirmeyi planladığınız kayıtları alın.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Adım 5: Yol İşlem Özelliklerini Değiştirin
Şimdi `PathOperations`'ı değiştirerek **modify PSD vector shapes** yapabilirsiniz. Bu, şekillerin nasıl etkileşeceğini belirler (ör. dışlama, kesişim, çıkarma).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Adım 6: Değiştirilmiş PSD Dosyasını Kaydedin
Değişikliklerinizi yeni bir dosyaya kaydedin.

```java
psdImage.save(outPsdFilePath);
```

## Adım 7: Kaynakları Temizleyin
Belleği serbest bırakmak için `PsdImage`'i yok edin.

```java
psdImage.dispose();
```

## Yaygın Tuzaklar ve İpuçları
- **Null kontrolleri** – yolları erişmeden önce `resource`'un `null` olmadığını her zaman doğrulayın.  
- **Yol indeks sınırları** – kullandığınız indekslerin (`[2]`, `[7]`, `[11]`) düzenlediğiniz belirli PSD'de mevcut olduğundan emin olun.  
- **Lisans** – geçerli bir lisans olmadan çalıştırmak, kaydedilen PSD'ye bir filigran ekleyecektir.  

## Sonuç
Artık Aspose.PSD for Java ile uzunluk kaydı veri özelliklerini destekleyerek **modify PSD vector shapes** nasıl yapılır konusunda tam, uçtan uca bir örneğe sahipsiniz. Varlık boru hatlarını otomatikleştiriyor ya da özel bir tasarım aracı geliştiriyor olun, bu API'ler vektör katmanlarını manuel Photoshop çalışması olmadan manipüle etme esnekliği sağlar. Diğer `PathOperations` ile deney yaparak veya karmaşık şekiller için birden fazla `LengthRecord` düzenlemesini birleştirerek daha fazla keşfedin.

## SSS

### Aspose.PSD for Java nedir?
Aspose.PSD for Java, geliştiricilerin Java kullanarak Photoshop PSD dosyalarını programlı bir şekilde manipüle etmelerini ve çalıştırmalarını sağlayan bir kütüphanedir.

### Aspose.PSD'yi ücretsiz bir projede kullanabilir miyim?
Evet, Aspose web sitesinde bulunan deneme sürümünü kullanarak kütüphaneyi ücretsiz deneyebilirsiniz.

### PSD dosyalarına hangi tür değişiklikleri yapabilirim?
PSD dosyaları içinde katmanları, şekilleri, metinleri, yol işlemlerini ve çok daha fazlasını manipüle edebilirsiniz.

### Aspose.PSD diğer programlama dilleriyle uyumlu mu?
Evet, Aspose .NET ve Python dahil olmak üzere çeşitli programlama dilleri için farklı kütüphaneler sunar.

### Aspose.PSD belgelerine nereden ulaşabilirim?
Tam belgeleri [buradan](https://reference.aspose.com/psd/java/) erişebilirsiniz.

## Sık Sorulan Sorular

**Q:** Vektör şekil katmanı içermeyen bir PSD'yi nasıl ele alırım?  
**A:** `VsmsResource` bulunmayacak, bu yüzden `resource` `null` kalır. Bir kontrol ekleyin ve değiştirme adımını atlayın ya da kullanıcıyı bilgilendirin.

**Q:** Dolgu rengi veya çizgi kalınlığı gibi diğer özellikleri değiştirebilir miyim?  
**A:** Evet, `LengthRecord` dolgu, çizgi ve opaklık için ek ayarlayıcılar sağlar. Tam detaylar için API belgelerine bakın.

**Q:** Birden fazla PSD dosyasını toplu işleme yapmak mümkün mü?  
**A:** Kesinlikle. Kodu, PSD dosyalarının bulunduğu bir dizinde dönen bir döngüye sarın ve her seferinde giriş ve çıkış yollarını ayarlayın.

**Q:** Dosya yolundan yüklerken akışları manuel olarak kapatmam gerekir mi?  
**A:** `Image.load` yöntemi dosya akışlarını dahili olarak yönetir, ancak bir `InputStream`'den yüklüyorsanız, kullanım sonrası kapatmayı unutmayın.

**Q:** Bu API'ler için hangi Aspose.PSD sürümü gereklidir?  
**A:** `LengthRecord` ve `PathOperations` sınıfları Aspose.PSD 20.10'dan itibaren mevcuttur. En son sürümün kullanılması önerilir.

---

**Son Güncelleme:** 2025-12-17  
**Test Edildi:** Aspose.PSD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}