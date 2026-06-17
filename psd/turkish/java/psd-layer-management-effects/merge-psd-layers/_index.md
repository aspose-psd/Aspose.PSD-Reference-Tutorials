---
date: 2026-04-05
description: Aspose.PSD for Java kullanarak PSD'yi PNG'ye nasıl dışa aktaracağınızı
  ve PSD katmanlarını nasıl birleştireceğinizi öğrenin. PSD'yi JPEG'e dönüştürme,
  JPEG kalitesini ayarlama ve PSD'den TIFF'e dönüşüm ipuçlarını içerir.
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: Aspose.PSD for Java kullanarak PSD'yi PNG'ye dışa aktar ve katmanları birleştir
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java kullanarak PSD'yi PNG'ye dışa aktar ve katmanları birleştir
url: /tr/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG'ye Dışa Aktarın & Katmanları Aspose.PSD for Java ile Birleştirin

## Giriş

Grafik tasarımcıların Photoshop'ta o karmaşık, katmanlı görüntüleri nasıl elde ettiğini hiç merak ettiniz mi? Sır genellikle **exporting PSD to PNG** ve katmanları akıllıca birleştirmekte yatar. Java'da PSD dosyalarıyla çalışıyorsanız, bu tekniklerde ustalaşmak bileşik görüntüler oluşturmanıza, dosya boyutunu azaltmanıza ve varlıkları web ya da mobil dağıtıma hazırlamanıza yardımcı olabilir. Bu öğreticide, Aspose.PSD for Java kullanarak **how to merge PSD** katmanlarını adım adım inceleyecek ve sonucu PNG'ye (gerekirse JPEG/TIFF olarak) dışa aktarmayı da göstereceğiz. Sonunda, katman yönetimini ve dışa aktarma iş akışlarını doğrudan Java uygulamanızdan otomatikleştirebileceksiniz.

## Hızlı Yanıtlar
- **Java'da PSD dosyalarını işleyen kütüphane nedir?** Aspose.PSD for Java.  
- **PSD'yi PNG'ye dışa aktarabilir miyim?** Evet – sadece uygun görüntü seçeneklerini ayarlayın.  
- **Birden fazla katmanı nasıl birleştiririm?** PSD'yi yükleyin, `Layer` koleksiyonunu değiştirin, ardından kaydedin.  
- **JPEG kalite kontrolüne ihtiyacım olursa ne yapmalıyım?** `JpegOptions` kullanın ve kaliteyi (0‑100) ayarlayın.  
- **Photoshop gerekli mi?** Hayır, Aspose.PSD Adobe yazılımından bağımsız çalışır.

## PSD'yi PNG'ye dışa aktarmak nedir?
Exporting PSD to PNG, bir Photoshop belgesini (PSD) taşınabilir ağ grafiği (PNG) dosyasına dönüştürmek anlamına gelir; isteğe bağlı olarak katmanları düzleştirebilir veya birleştirebilir. PNG şeffaflığı korur ve web üzerinde geniş destek bulur, bu da UI varlıkları için popüler bir format olmasını sağlar.

## PSD katmanlarını programlı olarak neden birleştirirsiniz?
- **Otomasyon:** Yüzlerce dosyayı manuel tıklama olmadan toplu işleyin.  
- **Performans:** Birleştirilmiş katmanlar, sonraki uygulamalarda render süresini azaltır.  
- **Dosya boyutu:** Gereksiz katmanları düzleştirmek, son görüntüyü küçültebilir.  
- **Tutarlılık:** Derlemeler arasında aynı katman sırasını ve karışımını garanti eder.

## Ön Koşullar

1. **Aspose.PSD for Java Kütüphanesi** – [Aspose.PSD for Java indirme bağlantısı](https://releases.aspose.com/psd/java/) adresinden indirin.  
2. **Java Geliştirme Ortamı** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir IDE.  
3. **Örnek PSD Dosyası** – birden fazla katmana sahip bir dosya (ör. `layers.psd`).  
4. **Temel Java Bilgisi** – sınıflar ve metodlarla rahat olmalısınız.  
5. **Aspose Geçici Lisansı (İsteğe Bağlı)** – daha büyük dosyalar için veya deneme sınırlamalarını kaldırmak amacıyla bir [geçici lisans](https://purchase.aspose.com/temporary-license/) edinin.

## Paketleri İçe Aktar

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Adım Adım Kılavuz

### Adım 1: PSD Dosyasını Yükle

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> Bu, `layers.psd` dosyasını bir `PsdImage` nesnesine yükler ve katmanlarına tam erişim sağlar.

### Adım 2: Katmanları İncele (psd nasıl birleştirilir)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> Katman adlarını incelemek, hangi katmanları düzleştireceğinize veya ayrı tutacağınıza karar vermenize yardımcı olur.

### Adım 3: Görüntü Seçeneklerini Ayarla (jpeg kalitesini ayarla)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> PNG veya TIFF tercih ediyorsanız, `JpegOptions` yerine `PngOptions` veya `TiffOptions` kullanabilirsiniz – işte **psd to tiff conversion**'ın yapılandırılacağı yer.

### Adım 4: Birleştirilmiş Görüntüyü Kaydet (psd'yi png'ye dışa aktar)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> `save` metodu birleştirilmiş sonucu `MergePSDlayers_output.png` dosyasına yazar.  
> *İpucu:* PNG'ye dışa aktarmak için `jpgOptions` yerine bir `PngOptions` örneği kullanın; kodun geri kalanı aynı kalır.

## Yaygın Sorunlar ve Çözümler

- **File‑not‑found exception:** `dataDir`'in bir yol ayırıcı (`/` veya `\\`) ile bittiğini ve `layers.psd` dosyasının mevcut olduğunu doğrulayın.  
- **Unexpected colors after merge:** Katman karışım modlarının uyumlu olduğundan emin olun; `layer.setBlendMode(...)` ile ayarlayabilirsiniz.  
- **Large output file:** JPEG kalitesini düşürün veya PNG sıkıştırma seviyelerini kullanarak boyutu azaltın.

## Sıkça Sorulan Sorular

**Q: JPEG dışındaki formatlarda birleştirilmiş görüntüyü kaydetmek mümkün mü?**  
**A:** Kesinlikle! Aspose.PSD PNG, BMP, TIFF ve daha fazlasını destekler. Sadece ilgili seçenek sınıfını (`PngOptions`, `BmpOptions`, `TiffOptions`) kullanın.

**Q: Farklı çıktı formatları için görüntü kalitesini nasıl ayarlayabilirim?**  
**A:** Her seçenek sınıfı kendi kalite/sıkıştırma ayarlarını sunar. JPEG için `setQuality(int)` kullanın. PNG için `CompressionLevel`'ı kontrol edebilirsiniz.

**Q: Aspose.PSD for Java kullanmak için Photoshop yüklü olması gerekir mi?**  
**A:** Hayır. Aspose.PSD Adobe Photoshop'tan bağımsız çalışır, bu yüzden herhangi bir sunucu veya CI ortamında çalıştırabilirsiniz.

**Q: Kaydetmeden önce görüntü seçeneklerini ayarlamazsam ne olur?**  
**A:** Kütüphane varsayılan ayarları uygular (ör. JPEG kalite 75). Seçenekleri belirlemek, nihai çıktıyı kontrol etmenizi sağlar.

**Q: PSD'yi doğrudan bir adımda TIFF'e dönüştürebilir miyim?**  
**A:** Evet – `TiffOptions` oluşturun ve `psdImage.save("output.tiff", tiffOptions);` metodunu çağırın.

---

**Son Güncelleme:** 2026-04-05  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım zamanındaki en son)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}