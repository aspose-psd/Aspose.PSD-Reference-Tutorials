---
date: 2026-03-07
description: Aspose.PSD for Java kullanarak PSD dosyalarına Level Adjustment Layer
  ekleyerek seviyeleri nasıl ayarlayacağınızı öğrenin. Tonal ayarlamaları hızlıca
  ustalaşın.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Seviye Ayarlarını Nasıl Düzenlersiniz – PSD'de Seviye Ayar Katmanı Ekle
url: /tr/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'de Seviye Ayarlama Katmanı Ekleme

## Introduction
Photoshop belgelerinizde **seviye ayarlamayı** nasıl yapacağınızı arıyorsanız, Seviye Ayarlama Katmanı mükemmel bir araçtır. Orijinal pikselleri kalıcı olarak değiştirmeden gölgeleri, orta tonları ve vurguları ince ayar yapmanızı sağlar. Bu öğreticide, Aspose.PSD for Java kullanarak bir PSD dosyasına Seviye Ayarlama Katmanı eklemeyi adım adım göstereceğiz, böylece sadece birkaç adımda profesyonel düzeyde ton kontrolü elde edebilirsiniz.

## Quick Answers
- **Bir Seviye Ayarlama Katmanı ne yapar?** Görüntünün ton aralığını yok edici olmayan bir şekilde değiştirir.  
- **Hangi kütüphane kullanılıyor?** Aspose.PSD for Java.  
- **Bir lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir ayarlama için yaklaşık 10‑15 dakika.  
- **Birden fazla kanalı ayarlayabilir miyim?** Evet, her renk kanalı için giriş/çıkış seviyelerini ayrı ayrı ayarlayabilirsiniz.

## What is a Level Adjustment Layer?
Seviye Ayarlama Katmanı, bir görüntünün ton dengesini giriş gölgeleri, orta tonları ve vurguları ile çıkış seviyelerini ayarlayarak düzeltmenizi sağlar. Kendi katmanında bulunduğu için görünürlüğünü açıp kapatabilir veya alt katmandaki çalışmayı etkilemeden silebilirsiniz.

## Why add a Level Adjustment Layer with Aspose.PSD?
- **Otomasyon:** Seviye ayarlarını toplu işleme boru hatlarına entegre edin.  
- **Çapraz platform:** Java'yı destekleyen herhangi bir işletim sisteminde çalışır.  
- **Hassasiyet:** Her kanalın ayarlarına programatik olarak erişerek kesin sonuçlar elde edin.  

## Prerequisites
1. Java Development Kit (JDK). Eğer yoksa, [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirin veya OpenJDK kullanın.  
2. Aspose.PSD for Java kütüphanesi – en yeni JAR dosyasını bu [indirme bağlantısından](https://releases.aspose.com/psd/java/) alın.  
3. Java programlamaya temel bir aşinalık.  
4. Aspose.PSD JAR'ı proje sınıf yoluna eklenmiş bir IDE (IntelliJ IDEA, Eclipse veya NetBeans gibi).

## Import Packages
Kod yazmaya başlamadan önce Aspose.PSD kütüphanesinden gerekli paketleri içe aktarmamız gerekiyor. İşte nasıl yapacağınız:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Bu içe aktarmalar, PSD dosyalarını yüklemek, seviye ayarlama katmanlarıyla çalışmak ve bireysel kanal ayarlarını manipüle etmek için sınıflara erişim sağlar.

## How to Adjust Levels in a PSD File
Aşağıda, **seviye ayarlamayı** programatik olarak nasıl yapacağınızı adım adım gösteren bir rehber bulacaksınız.

### Step 1: Set Up Your File Paths
Kaynak PSD'nin nerede bulunduğunu ve düzenlenmiş dosyanın nereye kaydedileceğini tanımlayın.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
`"Your Document Directory"` ifadesini makinenizdeki gerçek klasörle değiştirin.

### Step 2: Load the PSD File
Kaynak dosyadan bir `PsdImage` örneği oluşturun.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Artık PSD içindeki tüm katmanlara tam erişiminiz var.

### Step 3: Iterate Through the Layers
Değiştirmek istediğiniz Seviye Ayarlama Katmanını bulun.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
`instanceof LevelsLayer` kontrolü, yalnızca seviye ayarlama katmanlarıyla çalıştığımızı garanti eder.

### Step 4: Adjust the Level Channel Settings
Seçilen kanal için giriş ve çıkış değerlerini ayarlayın.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Input Midtone Level:** Orta ton aralığını kaydırır.  
- **Input Shadow Level:** Gölgeleri karartır veya aydınlatır.  
- **Input Highlight Level:** En parlak bölgeleri kontrol eder.  
- **Output Shadow/Highlight Levels:** Son çıkış aralığını tanımlar.

Farklı değerlerle denemeler yaparak görüntünün nasıl etkilendiğini görebilirsiniz.

### Step 5: Save the Modified PSD File
Değişikliklerinizi yeni bir dosyaya kaydedin.
```java
im.save(psdPathAfterChange);
```
Güncellenmiş PSD'yi `psdPathAfterChange` içinde belirttiğiniz konumda bulacaksınız.

## Common Issues and Solutions
- **File not found:** `dataDir`'in doğru klasöre işaret ettiğini ve kaynak PSD'nin mevcut olduğunu doğrulayın.  
- **ClassCastException:** Yüklediğiniz dosyanın gerçekten bir PSD olduğundan emin olun; diğer formatlar farklı sınıflar gerektirir.  
- **License errors:** Üretim sürümleri için geçerli bir Aspose.PSD lisansı kullanın; deneme sürümü geliştirme için çalışır.

## Conclusion
Artık Aspose.PSD for Java ile bir PSD dosyasına Seviye Ayarlama Katmanı ekleyerek **seviye ayarlamayı** nasıl yapacağınızı biliyorsunuz. Bu teknik, ton dengesine kesin kontrol sağlar ve iş akışınızı tamamen otomatik tutar. Farklı kanal değerleriyle denemeler yapmaya devam edin ve aynı ayarları birden fazla görüntüye uygulamak için toplu işleme keşfedin.

## Frequently Asked Questions

**Q: Seviye Ayarlama Katmanı nedir?**  
A: Görüntünün ton aralığını (gölgeler, orta tonlar, vurgular) değiştirebilen yok edici olmayan bir katmandır.

**Q: Aspose.PSD'yi lisans satın almadan kullanabilir miyim?**  
A: Evet, kütüphaneyi ücretsiz deneme ile değerlendirebilirsiniz, ancak ticari dağıtım için lisans gereklidir.

**Q: Aspose.PSD dokümantasyonunu nerede bulabilirim?**  
A: Dokümantasyonu [burada](https://reference.aspose.com/psd/java/) bulabilirsiniz.

**Q: Aspose ürünleri için topluluk desteği var mı?**  
A: Kesinlikle! Sorular sorabilir ve yardım alabilirsiniz: [Aspose forumu](https://forum.aspose.com/c/psd/34).

**Q: Aspose.PSD için geçici bir lisans nasıl alabilirim?**  
A: Geçici lisans başvurusunu [buradan](https://purchase.aspose.com/temporary-license/) yapabilirsiniz.

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD latest version (Java)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}