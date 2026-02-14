---
date: 2026-02-14
description: Aspose.PSD for Java kullanarak PSD dosyalarındaki katmanları nasıl bağlayacağınızı
  öğrenin. Bu adım adım öğretici, bağlı katman desteği eklemeyi, PSD dosyalarını toplu
  işlemeyi ve katmanların bağını etkili bir şekilde kaldırmayı gösterir.
linktitle: How to Link Layers in PSD Files Using Java
second_title: Aspose.PSD Java API
title: Java ile PSD Dosyalarındaki Katmanları Bağlama
url: /tr/java/advanced-psd-layer-features-effects/add-linked-layer-support-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# PSD Dosyalarında Katmanları Java Kullanarak Bağlama  

## Giriş  
Adobe Photoshop'un `.PSD` formatı katmanlı grafikler için endüstri standardıdır ve birçok geliştirici bu katmanları programlı olarak manipüle etmelidir. En güçlü tekniklerden biri **katmanları bağlama**dır; bu, katmanları tek bir birim olarak taşımanıza veya düzenlemenize izin verirken, her katmanın bireysel özelliklerini korur. Bu **Aspose.PSD öğreticisinde** Java kullanarak bir PSD dosyasında **katmanları nasıl bağlayacağınızı** adım adım göstereceğiz ve ayrıca **PSD katmanlarını yönetme**, **PSD katmanlarını bağlamayı kaldırma** ve değişiklikleri diske kaydetme konularını da göstereceğiz. Tasarım‑otomasyonu hattı oluşturuyor ya da bir masaüstü uygulamasını genişletiyor olsanız, bu adımlar katman ilişkileri üzerinde tam kontrol sağlayacaktır.  

## Hızlı Yanıtlar  
- **“Katmanları bağlamak” ne anlama gelir?** Katmanların düzleştirilmeden birlikte hareket etmesini sağlayan mantıksal bir grup oluşturur.  
- **Bu işlemi hangi kütüphane yönetir?** Aspose.PSD for Java, bir `LinkedLayersManager` API'si sağlar.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gerekir.  
- **Daha sonra bağlamayı kaldırabilir miyim?** Evet—`unlinkLayer` veya `unlinkLayers` metodlarını kullanın.  
- **Desteklenen Java sürümleri?** Java 8 ve üzeri.  

## PSD Dosyasında Katmanları Bağlama Nedir?  
Katmanları bağlama, birden fazla katmanı bir araya getirerek, dönüştürüldüğünde, taşındığında veya stillendirildiğinde tek bir varlık gibi davranmasını sağlayan bir Photoshop özelliğidir. Alttaki veri ayrı kalır, bu da daha sonra **PSD katmanlarını bağlamayı kaldırma** ve her birini bağımsız olarak düzenleyebileceğiniz anlamına gelir.  

## Neden PSD Katmanlarını Yönetmek İçin Aspose.PSD for Java Kullanmalı?  
- **Tam özellikli API** – Photoshop'u başlatmadan her Photoshop yapısına erişim sağlar.  
- **Çapraz platform** – Java'yı destekleyen herhangi bir işletim sisteminde çalışır.  
- **UI bağımlılığı yok** – Sunucu tarafı toplu işleme veya CI hatları için idealdir.  

## Ön Koşullar  
Koda geçmeden önce, şunların olduğundan emin olun:  

1. **Java Development Kit (JDK) 8+** – En son JDK önerilir.  
2. **Aspose.PSD for Java** – [Aspose sürüm sayfasından](https://releases.aspose.com/psd/java/) indirin.  
3. **IDE veya editör** – Eclipse, IntelliJ IDEA, VS Code vb.  
4. **Örnek PSD dosyası** – Photoshop'ta oluşturun veya test için ücretsiz bir örnek alın.  

## Paketleri İçe Aktarma  
Kodlamaya başlamadan önce gerekli Aspose.PSD sınıflarını içe aktarın:  

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```  

Bu içe aktarmalar, temel görüntü işleme, PSD‑özel özellikler ve katman manipülasyon metodlarına erişmenizi sağlar.  

## Adım‑Adım Kılavuz  

### Adım 1: PSD Dosyanızı Yükleyin  
İlk olarak, üzerinde çalışmak istediğiniz PSD'yi açın.  

```java
String dataDir = "Your Document Directory"; // specify your document directory
PsdImage psd = (PsdImage) Image.load(dataDir + "LinkedLayerexample.psd");
```  

Yolun mevcut bir dosyaya işaret ettiğinden emin olun; aksi takdirde `Image.load()` bir istisna fırlatır.  

### Adım 2: Tüm Katmanları Alın (PSD Katmanlarını Yönetme)  
Her katmanı alın ki hangi katmanları gruplayacağınızı seçebilesiniz.  

```java
Layer[] layers = psd.getLayers();
```  

`layers` dizisi artık belgenin tam katman yığınına sahiptir.  

### Adım 3: Katmanları Bağlayın  
Yönetici API'sini kullanarak bir bağlı‑katman grubu oluşturun.  

```java
short layersLinkGroupId = psd.getLinkedLayersManager().linkLayers(layers);
```  

Bu çağrı, yeni bağ grupunu benzersiz şekilde tanımlayan bir **grup kimliği** döndürür.  

### Adım 4: Bağ Grup Kimliğini Doğrulayın  
Döndürülen kimliğin, ilk katman için saklanan kimlikle eşleştiğini iki kez kontrol edin.  

```java
short linkGroupId = psd.getLinkedLayersManager().getLinkGroupId(layers[0]);
if (layersLinkGroupId != linkGroupId) {
    throw new Exception("layersLinkGroupId and linkGroupId are not equal.");
}
```  

Kimlikler farklıysa, bağlama sırasında bir şeyler ters gitmiştir.  

### Adım 5: Katmanları Alın ve Bağlamayı Kaldırın (PSD Katmanlarını Bağlamayı Kaldırma)  
İlişkiyi kesmeniz gerektiğinde, grup kimliğiyle bağlı katmanları alın ve tek tek bağlamayı kaldırın.  

```java
Layer[] linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
for (Layer linkedLayer : linkedLayers) {
    psd.getLinkedLayersManager().unlinkLayer(linkedLayer);
}
```  

Her yineleme, katmanın özgün verisini korurken bağlamayı kaldırır.  

### Adım 6: Bağlamayı Kaldırma İşlemini Doğrulayın  
Grup içinde hiçbir katmanın kalmadığını doğrulayın.  

```java
linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
if (linkedLayers != null) {
    throw new Exception("The linkedLayers field is not NULL.");
}
```  

`linkedLayers` hâlâ doluysa, bağlamayı kaldırma işlemi başarısız oldu.  

### Adım 7: Güncellenmiş PSD'yi Kaydedin  
Değiştirilen belgeyi diske geri yazın.  

```java
psd.save(dataDir + "LinkedLayerexample_output.psd");
```  

Kaydetme, yeni bağ grubunu veya onun kaldırılmasını da içeren tüm değişiklikleri korur.  

### Adım 8: PSD Nesnesini Serbest Bırakın  
Bellek sızıntılarını önlemek için yerel kaynakları serbest bırakın.  

```java
finally {
    psd.dispose();
}
```  

`dispose()` çağrısı, özellikle bir döngüde çok sayıda dosya işliyorsanız en iyi uygulamadır.  

## Batch İşlem PSD İş Akışlarında Bağlı Katman Desteği Nasıl Eklenir  
Aynı bağlama mantığını onlarca ya da yüzlerce dosyaya uygulamanız gerekiyorsa, yukarıdaki adımları PSD dizininde dönen basit bir döngüye sarın. **Aspose.PSD** bir UI gerektirmediği için bu kodu başsız bir sunucuda çalıştırabilirsiniz; bu da **batch process psd** senaryoları için mükemmeldir. İş parçacığı güvenliği sorunlarından kaçınmak için her dosya için yeni bir `PsdImage` örneği oluşturmayı unutmayın.  

## Yaygın Tuzaklar ve İpuçları  

- **Yanlış dosya yolu** – Her zaman mutlak yollar kullanın veya çalışma dizinini doğrulayın.  
- **Lisans eksik** – Deneme sürümü değerlendirme için çalışır, ancak tam lisans değerlendirme filigranlarını kaldırır.  
- **Sadece bir alt küme bağlama** – Katman yığınının sadece bir kısmına ihtiyacınız varsa, `linkLayers` çağırmadan önce istenen katmanlarla yeni bir `Layer[]` oluşturun.  
- **İş parçacığı güvenliği** – `PsdImage` örnekleri iş parçacığı‑güvenli değildir; her iş parçacığı için ayrı bir örnek oluşturun.  

## Sonuç  
Artık Aspose.PSD for Java kullanarak PSD dosyalarında **katmanları nasıl bağlayacağınız** konusunda eksiksiz, üretime hazır bir iş akışına sahipsiniz. Bu API'leri ustalıkla kullanarak karmaşık tasarım görevlerini otomatikleştirebilir, özel editörler oluşturabilir veya Photoshop‑stilinde katman yönetimini herhangi bir Java uygulamasına entegre edebilirsiniz. Katman efektleri, maskeler ve akıllı nesneler gibi diğer özelliklerle denemeler yaparak araç setinizi daha da genişletin.  

## Sıkça Sorulan Sorular  

**Q:** Aspose.PSD for Java nedir?  
**A:** Aspose.PSD for Java, geliştiricilerin Photoshop yüklü olmadan Photoshop PSD dosyalarını programlı olarak manipüle etmelerini sağlayan bir kütüphanedir.  

**Q:** Aspose.PSD'yi herhangi bir işletim sisteminde kullanabilir miyim?  
**A:** Evet, Java tabanlı olduğu için Windows, Linux, macOS veya Java'yı destekleyen herhangi bir platformda çalışır.  

**Q:** Deneme sürümü mevcut mu?  
**A:** Evet, Aspose.PSD for Java'yi ücretsiz olarak deneyebilirsiniz. [Ücretsiz deneme bağlantısını](https://releases.aspose.com/) kontrol edin.  

**Q:** Daha fazla belgeyi nerede bulabilirim?  
**A:** Geniş kapsamlı belgeleri [buradan](https://reference.aspose.com/psd/java/) inceleyebilirsiniz.  

**Q:** Sorunlarla karşılaşırsam nasıl destek alabilirim?  
**A:** Herhangi bir sorunla karşılaşırsanız, [destek forumunda](https://forum.aspose.com/c/psd/34) yardım bulabilirsiniz.  

---  

**Son Güncelleme:** 2026-02-14  
**Test Edilen Versiyon:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}  

{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}  

{{< blocks/products/products-backtop-button >}}