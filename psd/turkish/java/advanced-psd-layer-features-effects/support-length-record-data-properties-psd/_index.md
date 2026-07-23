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

## Giriiş
Programlı olarak **PSD vektör şekillerini değiştirmek istiyorsanız**, Aspose.PSD for Java kütüphanesi, Photoshop dosyalarının Java üzerinde okunmasızdan tam kontrol edilmesini sağlar. Bu öğretirken, **uzunluk kayıt belirtme destekleme** konusunda gereken her şeyi adım adım ince başlatmak—vektör şekil katmanlarını düzenlemek istediğinizde kritik bir adımdır. Sonunda, bir PSD verilerini açabilecek, vektör simge özelliklerini ayarlayabileceğiniz ve güncellendiğini IDE'nizden çıkmadan kaydedebileceksiniz. Hadi başla!

## Hızlı Yanıtlar
- **“PSD vektör şekillerinin değişmesi” ne anlama geliyor?** Bir PSD dosyasındaki taşıyıcı tabanlı katmanların geometrisini, yol gelişmeleri veya diğer özellikleri ayarlanır.
- **Bu işlem hangi kütüphanede yapılıyor?** Aspose.PSD for Java.
- **Lisans gerekir mi?** Değerlendirme için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir.
- **Uygulama ne kadar sürer?** Temel bir şekil‑değiştirme betiği için yaklaşık 10‑15dakika.
- **Ana önkoşullar nelerdir?** JavaJDK, Aspose.PSD for Java ve örnek bir PSD dosyası.

## “Destek uzunluğu kaydı özellikleri” nedir?
Uzunluk kayıt özelliğini destekleme, bir PSD'deki her vektör yolunu gösteren `LengthRecord`u çalıştırır ve bunları güncellemek anlamına gelir. Bu değişiklikler, şekillerin nasıl birleştirileceği, birbirine ulaşacağı veya birbirinden çıkacağının kontrol edilmesini sağlar.

## Uzunluk kaydı özelliklerini desteklemek için neden Aspose.PSD for Java kullanmalısınız?
- **Photoshop'a gerek yoktur** – PSD dosyalarıyla doğrudan herhangi bir sunucuda bulunabilir.
- **Zengin API** – katmanlara, kaynaklara ve istatistiklere sahip güçlü tipli sınıflarla erişin.
- **Çapraz‑platform** – Windows, Linux veya macOS üzerinde herhangi bir JDK dosyası çalıştırılır.
- **Performansa odaklı** – verimli bellek yönetimi ve hızlı kayıt işlemleri.

## Önkoşullar
1. **Java Development Kit (JDK)** – [Oracle'ın web sitesinde](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin veya tercih ettiğiniz paket yöneticisini kullanın.
2. **Aspose.PSD for Java** – en yeni JAR sürümü [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) başlatır.
3. **IDE** – IntelliJ IDEA, Eclipse veya herhangi bir Java uyumlu editör.
4. **Bir PSD dosyası** – Photoshop'ta birleştirme veya deneme amaçlı bir örnek PSD alın.
5. **Temel Java bilgisi** – sınıflar, nesneler ve istisna yönetimi konularına hakim olun.

## Paketleri İçe Aktar
İlk olarak, PSD dosyaları ve vektör şekil kaynaklarıyla çalışmak için ihtiyaç duyacağınız sınıfları içe aktarın.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Adım 1: Kaynak ve Çıkış Dizinlerinizi Ayarlayın
Orijinal PSD'nin bulunduğu yeri ve değiştirilmiş dosyanın kaydedileceği yeri tanımlayın.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Adım 2: PSD Dosyasını Yükleyin
Dosyayı açmak için `Image.load` kullanın ve PSD‑özel özellikler için `PsdImage` tipine dönüştürün.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Adım 3: Katmanda Vsms Kaynağını Bulun
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

## Adım 4: Uzunluk Kayıtlarına Erişin
Her `LengthRecord` ayrı bir vektör yolunu temsil eder. Değiştirmeyi planladığınız kayıtları alın.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Adım 5: Yol İşlemi Özelliklerini Değiştirin
Şimdi `PathOperations` değerlerini değiştirerek **PSD vektör şekillerini** modifiye edebilirsiniz. Bu, şekillerin nasıl etkileşeceğini (ör. dışlama, kesişim, çıkarma) belirler.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Adım 6: Değiştirilen PSD Dosyasını Kaydedin
Değişikliklerinizi yeni bir dosyaya kaydedin.

```java
psdImage.save(outPsdFilePath);
```

## Adım 7: Kaynakları Temizleyin
Belleği serbest bırakmak için `PsdImage` nesnesini dispose edin.

```java
psdImage.dispose();
```

## Destek uzunluğu kayıt özellikleriyle PSD dosyaları toplu olarak nasıl işlenir
Aynı vektör‑şekil düzeni birçok PSD'ye uygulamanız yapılır, satır kodu bir dizideki dosyalar üzerinde dönen bir döngüye yerleştirilmiştir. Her yineleme için `inPsdFilePath` ve `outPsdFilePath` değerlerini güncelleyin; Böylece **PSD'lerin toplu işleme** verimli bir şekilde yapabilirsiniz.

## Yaygın Tuzaklar ve İpuçları
- **Null kontrolleri** – `resource` nesnesinin kayıtlarından önce her zaman `null` olmadığını doğrulayın.
- **Yol indeks sınırları** – indekslerin (`[2]`, `[7]`, `[11]`) ilgili PSD içinde mevcut olduğundan emin olun.
- **Lisans** – geçerli bir lisans olmadan kullanabilirsiniz, giriş PSD'ye bir dosya ekleyecektir.

## Çözüm
Artık Aspose.PSD for Java ile parça kayıt özelliklerini destekleyerek **PSD vektör şekillerini değiştirme** konusunda eksiksiz bir uçtan‑uca örneğe uygunluğu. İster varlıkları hatlarını otomatik hale getirin, ister özel bir tasarım aracı geliştiriyor olun, bu API’ler vektör katmanlarını manuel Photoshop müdahalesi olmadan manipüle etme içerir. Diğer `PathOperations` deneyerek veya birden fazla `LengthRecord` düzenlemesini birleştirerek daha karmaşık sözler oluşturabilirsiniz.

## Sıkça Sorulan Sorular

**S: Vektör şekil dağıtımlarının bir PSD'si nasıl alınır?**
A: `VsmsResource` bulunmayacak, bu nedenle `resource` `null` kalacak. Bir kontrol değişikliği değişiklik adımını atın veya kullanıcıyı bilgilendirin.

**S: Doldurma rengi veya çizgi sızıntıları gibi diğer özellikler ortaya çıkabilir mi?**
C: Evet, `LengthRecord` doldurma, çizgi ve opaklık için ek ayarlayıcı yöntemler sunar. Ayrıntılar için API bilgilerine bakın.

**S: Birden fazla PSD toplamı toplu işlem yapmak mümkün mü?**
C: elbette. Kodu bir dizideki PSD dosyaları üzerinde dönen bir döngüye yerleştirerek, her fırsata giriş ve çıkış programlarını düzenler.

**S: Dosya akışı sırasında yüklemeleri manuel olarak kapatmam gerekir mi?**
A: `Image.load` yöntemi dosya aktarımlarını dahili olarak yönetir, ancak bir `InputStream` üzerinden yüklüyorsanız, kullanımdan sonra kapatmayı unutmayın.

**S: Bu API'ler için hangi Aspose.PSD sürümü gerekiyor?**
A: `LengthRecord` ve `PathOperations` sınıfları Aspose.PSD 20.10'dan itibaren mevcuttur. Yeni sürümün kullanılması tavsiye edilir.

---

**Son Güncelleme:** 2026-02-20
**Şunlarla Test Edildi:** Java 24.11 için Aspose.PSD
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}