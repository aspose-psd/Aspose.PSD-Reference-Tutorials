---
date: 2026-01-25
description: Aspose.PSD for Java kullanarak PSD dosyalarından küçük resim (thumbnail)
  nasıl çıkarılacağını öğrenin. Yükleme, çıkarma ve küçük resimleri hızlı bir şekilde
  kaydetme adım adım rehberini izleyin.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: Java'da PSD'den Küçük Resim Çıkar
url: /tr/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'den Küçük Resim ÇıBu öğreticidearmayı** öğreneceksiniz. Küçük resimler, PSD belgelerinin içinde gömülü olan minik önizleme görselleridir ve bunları çıkarmak, hızlı önizlemeler oluşturmanıza, görüntü galerileri yapmanıza veya yalnızca orijinal eserin küçük bir PSD dos çıkarmaresmi Aspose sitesinden indirilebilir).  
- **Lisans gerekli mi?** Üretim kullanımı için geçici veya tam lisans gerekir; ücretsiz deneme sürümü mevcuttur.  
- **Hangi çıktı formatı kullanılıyor?** Örnekte küçük resim JPEG dosyası olarak kaydedilir, ancak Aspose.Pilebilir.  
- **Uygulama ne kadar sürer?** Temel Java kavramlarına aşina bir geliştirici için yaklaşık 5‑10 dakikadır.

## “PSD'den küçük resim çıkarma” nedir?
PSD'den küçük resim çıkarmak, Photoshop'un dosyanın kaynak düşük çözünü kütüphanelerinin toplu işlenmesi için mükemmel.  
- **Çapraz platform:** Java'yı destekleyen herhangi bir işletim sisteminde çalışır, Photoshop gerektirmez.  
- **Format esnekliği:** Küçük resmi JPEG, PNG veya Aspose.PSD tarafından desteklenen herhangi bir formata dönüştürebilirsiniz.

## Önkoşullar
Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:
- Sisteminizde Java Development Kit (JDK) kurulu olmalıdır.  
- Aspose.PSD for Java kütüphanesi. [Buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.  
- Java programlamaya temel bir bilgi.

## Paketleri İçe Aktarma
Başlamak için Java sınıfınıza gerekli Aspose.PSD paketini ekleyin:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Aspose.PSD for Java Kullanarak PSD'den Küçük Resim Nasıl Çıkarılır
Aşağıda adım adım kılavuz bulunmaktadır. Her adım kısa bir açıklama ve kopyalamanız gereken tam kodu içerir.

### Adım 1: PSD Dosyasını Yükle
Öncelikle, içinde çıkarmak istediğiniz küçük resim bulunan PSD dosyasını yükleyin.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
`"Your_Document_Directory/"` ifadesini PSD dosyanızın bulunduğu dizin yolu ile, `"your_file.psd"` ifadesini ise PSD dosyanızın adıyla değiştirin.

### Adım 2: Görüntü Kaynakları Üzerinde Döngü
Küçük resim kaynağını bulmak için görüntü kaynakları arasında dolaşın.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```

### Adım 3: Çıkarılan Küçük Resmi Kaydet
Önceki adımda yer alan kod, aynı dizinde `extracted_thumbnail.jpg` adlı bir JPEG dosyası olarak küçük resmi zaten kaydeder. `save` yöntemi parametrelerini ayarlayarak dosya adını veya formatını değiştirebilirsiniz.

### Adım 4: Farklı Küçük Resim Türlerini İşleme
PSD dosyanız birden fazla küçük resim türü (ör. `Thumbnail4Resource`) içerebilir; bu durumda döngü içinde `instanceof Thumbnail4Resource` kontrolü ekleyerek aynı desenle işleyebilirsiniz.

## Yaygın Sorunlar ve Çözümler
- **Küçük resim bulunamadı:** Tüm PSD dosyalarında küçük resim kaynağı bulunmaz. Photoshop'ta (Dosya → Dışa Aktar → Küçük Resim) kontrol edin veya önizleme içeren başka bir PSD deneyin.  
- **Desteklenmeyen görüntü formatı hatası:** Hedef formatı destekleyen güncel bir Aspose.PSD sürümü kullandığınızdan emin olun.  
- **Kaydederken izin hataları:** Uygulamanın çıktı dizinine yazma izni olduğundan emin olun.

## Sık Sorulan Sorular

**S: Aspose.PSD nedir?**  
C: Aspose.PSD, geliştiricilerin PSD ve diğer görüntü dosya formatlarıyla programatik olarak çalışmasına olanak tanıyan bir Java kütüphanesidir.

**S: Aspose.PSD for Java hakkında daha fazla belgeye nereden ulaşabilirim?**  
C: Ayrıntılı API referansları ve örnekler için [belgelere](https://reference.aspose.com/psd/java/) bakabilirsiniz.

**S: Aspose.PSD'yi satın almadan ücretsiz deneyebilir miyim?**  
C: Evet, kütüphanenin yeteneklerini değerlendirmek için bir [ücretsiz deneme](https://releases.aspose.com/) indirebilirsiniz.

**S: Aspose.PSD için geçici lisanslar nasıl alınır?**  
C: Geçici lisansları [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

**S: Aspose.PSD ticari kullanım için uygun mu?**  
C: Evet, Aspose.PSD hem kişisel hem de ticari projelerde lisans koşulları çerçevesinde kullanılabilir.

## Sonuç
Bu öğreticide, Aspose.PSD for Java kullanarak **PSD dosyalarından küçük resim (thumbnail) çıkarmayı** inceledik. Yukarıdaki adımları izleyerek PSD belgelerinizde gömülü küçük resimleri verimli bir şekilde alabilir ve kaydedebilir, böylece daha hızlı önizlemeler ve düzenli görüntü iş akışları elde edebilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-25  
**Test Edilen:** Aspose.PSD for Java (en son sürüm)  
**Yazar:** Aspose