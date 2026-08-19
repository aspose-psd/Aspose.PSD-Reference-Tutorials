---
date: 2026-04-03
description: Aspose.PSD for Java ile katmanları düzleştirerek PSD dosya boyutunu nasıl
  azaltacağınızı öğrenin. Bu adım adım kılavuz, PSD dosyalarını hızlı bir şekilde
  nasıl düzleştireceğinizi gösterir.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Katmanları Düzleştirerek PSD Dosya Boyutunu Azaltın – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Katmanları Düzleştirerek PSD Dosya Boyutunu Azaltın – Aspose.PSD Java
url: /tr/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosya Boyutunu Katmanları Düzleştirerek Azaltma – Aspose.PSD Java

## Giriş

Bir Photoshop belgesi açıp **PSD dosya boyutunu azaltma** yollarını merak ettiyseniz, katmanları düzleştirmek en etkili hilelerden biridir. Aspose.PSD for Java ile bir PSD'yi programlı olarak tamamen düzleştirebilir veya yalnızca seçtiğiniz katmanları birleştirebilirsiniz; bu sayede dosya ağırlığı üzerinde ince ayar yapabilir, görsel kaliteyi kaybetmeden dosyanızı küçültebilirsiniz. Bu öğreticide, tüm görüntüyü düzleştirme ve belirli katmanları birleştirme yaklaşımlarını adım adım inceleyeceğiz, böylece PSD dosyalarınızı hızlıca küçültebilir ve iş akışınızı sorunsuz tutabilirsiniz.

## Hızlı Yanıtlar
- **Düzleştirme ne yapar?** Görünür katmanları tek bir arka plan katmanına birleştirir, katman bilgilerini kaldırır ve genellikle dosya boyutunu azaltır.  
- **Yalnızca seçili katmanları düzleştirebilir miyim?** Evet, belirli katmanları birleştirebilir, diğerlerini dokunulmamış bırakabilirsiniz.  
- **Lisans gerekir mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Hangi Java sürümü gerekiyor?** JDK 8 veya üzeri.  
- **Düzleştirme görüntü kalitesini etkiler mi?** Hayır, görsel görünüm aynı kalır; sadece katman yapısı değişir.

## “PSD dosya boyutunu azaltma” nedir?

PSD dosya boyutunu azaltmak, gereksiz verileri—ekstra katmanlar, gizli kanallar veya aşırı meta veriler gibi—kaldırmak anlamına gelir; böylece dosya daha hafif ve daha hızlı yüklenir, paylaşılır veya işlenir. Katmanları düzleştirmek, ayrı katman nesnelerini atarak nihai birleşik görüntüyü koruyan yaygın bir tekniktir.

## Neden Aspose.PSD for Java ile katmanları düzleştirirsiniz?

- **Otomasyon:** Photoshop’u manuel olarak açmaya gerek yok; doğrudan Java uygulamalarınıza entegre edin.  
- **Kesinlik:** Tüm belgeyi ya da yalnızca görünür katmanları (`flattenImage`) düzleştirmeyi ya da seçili katmanları (`mergeLayers`) birleştirmeyi seçin.  
- **Performans:** Daha küçük dosyalar daha hızlı yüklenir ve sonraki işlemlerde daha az bellek tüketir.  
- **Çapraz platform:** Java’yı destekleyen herhangi bir işletim sisteminde çalışır.

## Önkoşullar

1. **Java Development Kit (JDK):** JDK 8 veya daha yeni bir sürüm yüklü.  
2. **Aspose.PSD for Java:** Kütüphaneyi [burada](https://releases.aspose.com/psd/java/) indirin.  
3. **IDE:** IntelliJ IDEA, Eclipse veya herhangi bir Java uyumlu IDE.  
4. **Temel Java bilgisi:** Adımları takip etmek için faydalı ancak zorunlu değil.  
5. **Örnek PSD:** Birden çok katmana sahip bir dosya (biz `ThreeRegularLayersSemiTransparent.psd` dosyasını kullanacağız).

Şimdi her şey hazır olduğuna göre, koda dalalım.

## Paketleri İçe Aktarma

Başlamak için gerekli Aspose.PSD sınıflarını içe aktarın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Bu içe aktarmalar, PSD dosyalarını yüklememizi, katmanlarıyla çalışmamızı ve sonuçları kaydetmemizi sağlar.

## Adım 1: Tüm PSD Görüntüsünü Düzleştirme

Tüm görüntüyü düzleştirmek, **PSD dosya boyutunu azaltmanın** en hızlı yoludur çünkü tüm ayrı katman verilerini kaldırır.

### 1.1 PSD Dosyasını Yükle

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Görüntüyü Düzleştir

```java
im.flattenImage();
```

### 1.3 Düzleştirilmiş Görüntüyü Kaydet

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

Yeni dosyanız artık tek bir arka plan katmanı içeriyor; bu genellikle daha küçük bir PSD boyutu anlamına gelir.

## Adım 2: Belirli Katmanları Birleştirme (PSD'yi seçici olarak düzleştirme)

Bazen yalnızca **görünür katmanları düzleştirmek** veya bir alt küme katmanı birleştirip diğerlerini düzenlenebilir tutmak istersiniz.

### 2.1 PSD Dosyasını Tekrar Yükle

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Katmanları Tanımla ve Seç

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Katmanları Birleştir

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Mevcut Katmanları Birleştirilmiş Katmanla Değiştir

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Güncellenmiş PSD Dosyasını Kaydet

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Şimdi PSD yalnızca birleştirilmiş katmanı içeriyor; bu, istediğiniz katmanları korurken dosya boyutunu küçültmenizi sağlar.

## Yaygın Sorunlar ve İpuçları

- **Düzleştirmeden önce yedek alın:** Katmanlar düzleştirildiğinde işlem geri alınamaz. Orijinal PSD'nin bir kopyasını saklayın.  
- **Görünürlük önemlidir:** `flattenImage()` yalnızca *görünür* katmanları birleştirir. Dahil etmek istemediğiniz katmanları gizleyin.  
- **Bellek kullanımı:** Büyük PSD'ler önemli miktarda RAM tüketebilir; yeterli belleğe sahip bir makinede işlemeyi düşünün.  
- **Karıştırma modları:** Birleştirme, her katmanın karıştırma modunu korur, böylece görsel sonuç Photoshop'ta gördüklerinizle aynı olur.

## Sıkça Sorulan Sorular

**S: Aspose.PSD'de katmanların düzleştirilmesini geri alabilir miyim?**  
C: Hayır, düzleştirme geri alınamaz. Her zaman orijinal dosyanın bir yedeğini tutun.

**S: Yalnızca görünür katmanları düzleştirmek mümkün mü?**  
C: Evet. `flattenImage()` katman görünürlüğüne saygı gösterir, bu yüzden yöntemi çağırmadan önce düzleştirmek istemediğiniz katmanları gizleyin.

**S: Katmanları düzleştirmek dosya boyutunu azaltır mı?**  
C: Genel olarak evet. Katman verilerini ve meta verileri kaldırmak genellikle daha küçük bir PSD'ye yol açar, ancak kesin azalma içeriğe bağlıdır.

**S: Farklı karıştırma modlarına sahip katmanları birleştirebilir miyim?**  
C: Kesinlikle. Aspose.PSD, katmanları birleştirirken karıştırma modlarıyla oluşturulan görsel görünümü korur.

**S: Ardışık olmayan katmanları birleştirmeye çalışırsam ne olur?**  
C: Aspose.PSD, yığındaki konumlarından bağımsız olarak herhangi bir katmanı birleştirmeye izin verir; sonuç, birleşik görünümü yansıtır.

**Son Güncelleme:** 2026-04-03  
**Test Edilen:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}