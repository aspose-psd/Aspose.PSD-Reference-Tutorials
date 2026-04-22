---
date: 2026-04-22
description: Görüntü işleme Java kütüphanesi Aspose.PSD'yi kullanarak, Invert Ayar
  Katmanı da dahil olmak üzere birden fazla ayar katmanını uygulamayı ve sorunsuz
  PSD manipülasyonu yapmayı öğrenin.
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: Ters Çevirme Ayarlama Katmanı
second_title: Aspose.PSD Java API
title: 'Görüntü İşleme Java Kütüphanesi: Aspose.PSD ile Katmanı Tersine Çevir'
url: /tr/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java'da Ters Çevirme Ayar Katmanı

## Giriş

Eğer sağlam bir **image processing java library** arıyorsanız, Aspose.PSD for Java piyasadaki en çok yönlü seçeneklerden biridir. Bu öğreticide bir PSD dosyasına **Invert Adjustment Layer** eklemeyi adım adım göstereceğiz; bu tekniği diğer ayar katmanlarıyla birleştirerek karmaşık görsel efektler elde edebilirsiniz. İster toplu‑işlem aracı, ister sunucu‑tarafı görüntü hizmeti, ister tek‑görüntü düzenleyici oluşturuyor olun, bu kılavuz işi hızlı ve güvenilir bir şekilde tamamlamak için net bir adım‑adım yolu sunar.

## Hızlı Yanıtlar
- **Invert Ayar Katmanı ne yapar?** Seçili alandaki tüm renk değerlerini tersine çevirir, negatif‑görüntü etkisi oluşturur (yani **converts PSD to negative**).  
- **Bu özelliği hangi kütüphane sağlar?** Aspose.PSD, önde gelen bir **image processing java library**.  
- **Bunu diğer ayarlarla birleştirebilir miyim?** Evet – **apply multiple adjustment layers** gibi Parlaklık/Kontrast, Renk/Doygunluk gibi birden fazla ayar katmanı ekleyebilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme mevcuttur; üretim kullanımı için bir lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir kullanım senaryosu için genellikle 10 dakikadan az sürer.

## Invert Ayar Katmanı nedir?

Invert Ayar Katmanı, etkilediği her pikselin RGB değerlerini tersine çeviren bir non‑destructive (yıkıcı olmayan) düzenlemedir. Katman yığını üzerinde en üstte yer aldığından, görünürlüğünü açıp kapatabilir veya yeniden sıralayabilirsiniz; bu, orijinal görüntü verisini kalıcı olarak değiştirmez. **invert colors PSD** dosyalarını ters çevirmek veya fotoğrafik bir negatif oluşturmak için en kolay yoldur.

## Neden Aspose.PSD'yi Görüntü İşleme Java Kütüphaneniz Olarak Kullanmalısınız?

- **Full PSD support** – Photoshop yüklü olmadan Photoshop dosyalarını okuyabilir, düzenleyebilir ve yazabilirsiniz.  
- **Cross‑platform** – herhangi bir Java çalışma zamanında (Java 6+) çalışır.  
- **Rich adjustment features** – birçok yaygın düzenleme için yerleşik yöntemler içerir, tek bir iş akışında **apply multiple adjustment layers** eklemeyi kolaylaştırır.  
- **Performance‑optimized** – büyük dosyaları verimli bir şekilde işler, bu da **batch process psd images** için çok önemlidir.  

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.PSD Library** – resmi siteden [burada](https://releases.aspose.com/psd/java/) indirin.  
2. **Java Development Environment** – JDK 6.0 veya daha yeni bir sürüm kurulu ve yapılandırılmış.  

Şimdi, koda dalalım.

## Paketleri İçe Aktar

Gerekli sınıfları içe aktararak başlayın. Bu içe aktarmalar, temel görüntü‑işleme API'lerine ve PSD‑özel işlevselliğine erişim sağlar.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Adım 1: Belge Dizinini Ayarla

Kaynak PSD dosyanızı içeren ve çıktının kaydedileceği klasörü tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: PSD Dosyasını Yükle

Kaynak dosyayı bir `PsdImage` nesnesine yükleyin. Bu nesne, tüm PSD belgesini bellekte temsil eder.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Adım 3: Invert Ayar Katmanı Ekle

Mevcut katman yığınının üstüne bir Invert Ayar Katmanı eklemek için yerleşik yöntemi çağırın. Daha sonra daha fazla katman (ör. Parlaklık, Renk) ekleyerek **apply multiple adjustment layers** yapabilirsiniz.

```java
im.addInvertAdjustmentLayer();
```

## Adım 4: Çıktıyı Kaydet

Değiştirilmiş PSD'yi diske kaydedin. Kaydedilen dosya artık Invert Ayar Katmanı içeriyor ve Photoshop ya da herhangi bir PSD‑uyumlu görüntüleyicide açılabilir.

```java
im.save(outputPath);
```

### Ne oldu?

- PSD belleğe yüklendi.  
- Bir Invert Ayar Katmanı en üst katman olarak eklendi.  
- Görüntü kaydedildi, non‑destructive düzenleme korundu.

Artık bir PSD dosyasını manipüle etmek için Aspose.PSD'yi, bir **image processing java library** olarak başarıyla kullandınız.

## Invert ayarıyla PSD görüntülerinin toplu işlenmesi

Aynı invert efektini onlarca ya da yüzlerce dosyaya uygulamanız gerekiyorsa, yukarıdaki kodu PSD'lerin bulunduğu bir dizini dönen basit bir döngü içinde kullanabilirsiniz. Kütüphane **performance‑optimized** olduğu için büyük toplu işlemler hızlı kalır ve aynı döngüde invert adımını diğer ayarlarla (ör. parlaklık, renk) birleştirebilirsiniz.

## Bir PSD'yi negatif görüntüye dönüştürme

Invert Ayar Katmanı temelde **convert PSD to negative** işlemi gibidir. Bu katmanı en üst öğe olarak ekleyerek, orijinal piksel verisini kalıcı olarak değiştirmeden tam bir negatif etki elde edersiniz. Katmanı daha sonra kaldırabilir veya devre dışı bırakabilirsiniz; böylece orijinal görünüme geri dönersiniz.

## Yaygın Sorunlar ve İpuçları

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | Yanlış dosya yolu veya eksik dosya | `dataDir` ve dosya adını doğrulayın; test için mutlak yollar kullanın |
| **Katman sırası beklenildiği gibi değil** | Mevcut katmanların üzerine katman eklemek yığını değiştirir | `im.addInvertAdjustmentLayer()`'ı diğer ayarları eklemeden önce kullanın veya katmanları `im.getLayers()` ile yeniden sıralayın |
| **Büyük PSD'lerde performans yavaşlaması** | Çok büyük dosyaları belleğe yüklemek | Sayfaları parçalar halinde işlemeyi düşünün veya JVM yığın boyutunu (`-Xmx2g`) artırın |

## Sık Sorulan Sorular

**Q: Aspose.PSD tüm Java sürümleriyle uyumlu mu?**  
A: Aspose.PSD, Java 6.0 ve sonraki sürümleri destekler.

**Q: Tek bir işlemde birden fazla ayar katmanı uygulayabilir miyim?**  
A: Evet, Invert, Parlaklık ve Renk/Doygunluk gibi birkaç ayar katmanını bir araya getirerek karmaşık efektler elde edebilirsiniz.

**Q: Aspose.PSD için ek belgeleri nerede bulabilirim?**  
A: Kapsamlı kılavuzlar ve API referansları için belgeleri [burada](https://reference.aspose.com/psd/java/) inceleyin.

**Q: Aspose.PSD için ücretsiz deneme mevcut mu?**  
A: Evet, ücretsiz denemeyi [burada](https://releases.aspose.com/) keşfedebilirsiniz.

**Q: Aspose.PSD için geçici bir lisans nasıl alabilirim?**  
A: Geçici bir lisansı [burada](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

---

**Son Güncelleme:** 2026-04-22  
**Test Edilen:** Aspose.PSD 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}