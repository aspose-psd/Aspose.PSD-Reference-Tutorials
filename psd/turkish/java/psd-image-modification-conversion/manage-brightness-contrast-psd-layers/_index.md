---
date: 2026-03-28
description: Aspose.PSD for Java kullanarak PSD dosyalarında parlaklık ayarlamayı
  öğrenin; PSD katmanının parlaklık ve kontrastını nasıl değiştireceğinizi de kapsar.
  Geliştiriciler ve grafik tasarımcılar için idealdir.
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: Parlaklığı Ayarla PSD Java – Parlaklık ve Kontrastı Yönet
url: /tr/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Parlaklığı Ayarlama PSD Java – Parlaklık ve Kontrastı Yönetme

## Giriş

PSD (Photoshop Document) dosyalarıyla sık sık çalışan bir grafik tasarımcı veya geliştirici misiniz? Java ortamınızı terk etmeden **adjust brightness psd java**'yi hızlı ve güvenilir bir şekilde yapmanız mı gerekiyor? Bu öğreticide, Aspose.PSD Java kütüphanesini kullanarak PSD katmanının parlaklık ve kontrastını nasıl değiştireceğinizi tam olarak göstereceğiz. Herhangi bir otomatik görüntü‑işleme hattına entegre edilebilecek yeniden kullanılabilir bir kod parçacığı elde edeceksiniz. Kolları sıvayalım ve başlayalım!

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java  
- **Birden fazla katmanı aynı anda değiştirebilir miyim?** Yes – iterate through all `BrightnessContrastLayer` objects.  
- **Hangi Java sürümü gerekiyor?** JDK 8 or higher.  
- **Üretim için lisansa ihtiyacım var mı?** Yes, a commercial license is required for non‑evaluation use.  
- **Kod Maven/Gradle projeleriyle uyumlu mu?** Absolutely – just add the Aspose.PSD dependency.

## “adjust brightness psd java” nedir?

Java üzerinden bir PSD dosyasında parlaklığı ayarlamak, `BrightnessContrastLayer` değerlerini programlı olarak değiştirmek anlamına gelir; bu sayede Photoshop'ta manuel olarak yapılması gereken görsel ayarlamaları otomatikleştirebilirsiniz.

## Neden PSD katmanlarında parlaklık ve kontrast ayarlamalısınız?

- **Batch işleme hızını artırın** – büyük tasarım kütüphaneleri için mükemmeldir.  
- **Katman yapısını koruyun** – yalnızca hedeflenen ayar katmanları değiştirilir, maskeler ve efektler korunur.  
- **CI/CD hatlarına entegre edin** – ön izleme görüntüleri veya küçük resimler otomatik olarak oluşturulur.

## Önkoşullar

Java ile PSD dosyalarını manipüle etme yolculuğuna başlamadan önce, her şeyin doğru şekilde kurulduğundan emin olmak önemlidir. Bu öğreticiyi başarıyla tamamlamak için aşağıdakilere ihtiyacınız olacak:

1. **Java Development Kit (JDK)** – Makinenizde JDK 8 veya üzeri yüklü olduğundan emin olun. [Oracle'ın web sitesinden](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) indirebilirsiniz.

2. **Aspose.PSD for Java Library** – PSD dosyalarıyla çalışmak için Aspose.PSD kütüphanesine ihtiyacınız olacak. En son sürümü [release page](https://releases.aspose.com/psd/java/) adresinden indirebilirsiniz.

3. **IDE** – IntelliJ IDEA, Eclipse veya NetBeans gibi bir Entegre Geliştirme Ortamı (IDE), Java kodunuzu yazmak ve çalıştırmak için tercih edilir.

4. **Java Temel Bilgisi** – Java programlamasına aşina olmak, üzerinde çalışacağımız kod parçacıklarını anlamanıza yardımcı olacaktır.

Bu önkoşulları tamamladıktan sonra, ilerlemeye hazırız. Şimdi favori kod düzenleyicinizi alın ve kodlamaya başlayalım!

## Paketleri İçe Aktarma

Kodlama yolculuğumuzun ilk adımı gerekli paketleri içe aktarmaktır. Aspose.PSD tarafından sağlanan işlevleri kullanabilmek için, kütüphanenin sınıf yolunuzda olduğundan emin olmanız gerekir. İşte bunu yapmanın yolu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

Bu adımları tamamlayarak, PSD dosyalarıyla etkili bir şekilde çalışmak için ortamı hazırlamış oluyorsunuz!

Her şey kurulduğuna göre, öğreticinin özüne geçme zamanı: PSD katmanlarında parlaklık ve kontrastı ayarlamak. Bu süreci net adımlara böleceğiz, böylece kolayca takip edebilirsiniz.

## Adım 1: Belge Dizinini Tanımlayın

PSD dosyalarınızın bulunduğu dizini tanımlayarak başlayın. Bu adım dosyalarınızı verimli bir şekilde düzenlemenize yardımcı olur.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini PSD dosya dizininizin gerçek yolu ile değiştirin.

## Adım 2: Kaynak ve Hedef Dosya Adlarını Belirleyin

Sonra, PSD dosyanızın kaynak dosya adını ve düzenlenmiş PSD'nin kaydedileceği hedef dosyayı belirtmeniz gerekir.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

Bu örnekte, dizininizde `BrightnessContrastModern.psd` adlı bir PSD dosyanız olduğunu varsayıyoruz.

## Adım 3: PSD Dosyasını Yükleyin

Artık PSD dosyasını uygulamanıza yükleyerek üzerinde işlem yapma zamanı.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Bu kod satırı, PSD dosyanızı temsil eden bir `PsdImage` örneği oluşturur. Böylece artık PSD'nin tüm katmanlarına erişebilirsiniz.

## Adım 4: Katmanlar Üzerinde Döngü Oluşturun

Sonraki adım, PSD dosyanızdaki her katmanı dolaşarak parlaklık ve kontrast ayarlarını bulmak ve değiştirmektir.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

`for` döngüsü PSD'nin her katmanını dolaşır. Bir katmanın `BrightnessContrastLayer` örneği olup olmadığını kontrol ediyoruz. Bu, sadece doğru katmanlarda PSD katman parlaklığını değiştirmeye çalıştığınızdan emin olmak için gereklidir.

## Adım 5: Parlaklık ve Kontrastı Ayarlayın

Döngü içinde, her `BrightnessContrastLayer` için parlaklık ve kontrastı ayarlayabilirsiniz. 

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

Bu örnekte, parlaklık ve kontrastı `50` olarak ayarladık. Bu değerleri gereksinimlerinize göre ayarlayabilirsiniz. Daha yüksek bir sayı parlaklık/kontrastı artırırken, daha düşük bir sayı azaltır.

## Adım 6: Değişiklikleri Kaydedin

Son adım, değişikliklerinizi PSD dosyasına kaydetmektir. Değiştirilmiş görüntüyü belirtilen hedefe geri yazmak isteyeceksiniz.

```java
im.save(psdPathAfterChange);
```

Bu kod satırı, yeni parlaklık ve kontrast ayarlarıyla düzenlenmiş PSD dosyasını kaydeder.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| **`BrightnessContrastLayer` bulunamadı** | PSD farklı bir ayar türü (ör. Levels) kullanıyor olabilir. | Katman tipini doğrulayın veya ayarı `BrightnessContrastLayer`'a dönüştürün. |
| **Kaydedilen dosya bozuk görünüyor** | Lisans eksik veya eski bir Aspose.PSD sürümü kullanılıyor. | Geçerli bir lisans uygulayın ve en son kütüphane sürümünü kullandığınızdan emin olun. |
| **Değerler aralık dışında** | Parlaklık/Kontrast değerleri -100 ile 100 arasında olmalıdır. | `setBrightness`/`setContrast` çağırmadan önce değerleri sınırlayın. |

## Sıkça Sorulan Sorular

**Q:** Aspose.PSD for Java nedir?  
**A:** Aspose.PSD for Java, geliştiricilerin PSD dosyalarını programlı olarak manipüle etmelerini sağlayan bir kütüphanedir; bu sayede Photoshop‑ile ilgili görevlerin otomasyonu mümkün olur.

**Q:** Birden fazla katmanın parlaklık ve kontrastını aynı anda ayarlayabilir miyim?  
**A:** Evet, bu öğreticide kullanılan yöntem PSD'deki tüm katmanları dolaşır ve birden fazla `BrightnessContrastLayer` örneğini ayarlamanıza olanak tanır.

**Q:** Aspose.PSD için geçici bir lisans nasıl alabilirim?  
**A:** [temporary license page](https://purchase.aspose.com/temporary-license/) adresini ziyaret ederek geçici bir lisans edinebilirsiniz.

**Q:** Aspose.PSD için ücretsiz deneme sürümü var mı?  
**A:** Evet, Aspose.PSD'nin ücretsiz deneme sürümünü [release page](https://releases.aspose.com/) adresinden indirebilirsiniz.

**Q:** Aspose.PSD için ek destek nereden bulunabilir?  
**A:** Aspose.PSD desteğini [support forum](https://forum.aspose.com/c/psd/34) üzerinden alabilirsiniz.

---

**Son Güncelleme:** 2026-03-28  
**Test Edilen Versiyon:** Aspose.PSD for Java 24.12 (yazım zamanındaki en son)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}