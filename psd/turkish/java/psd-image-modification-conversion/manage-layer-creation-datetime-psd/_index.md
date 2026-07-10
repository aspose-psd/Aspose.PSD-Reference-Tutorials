---
date: 2026-03-28
description: Aspose.PSD for Java kullanarak yeni bir PSD katmanı oluşturmayı ve oluşturulma
  tarih‑saatini yönetmeyi öğrenin. Bu adım‑adım kılavuz, katmanların yüklenmesi, okunması,
  doğrulanması ve eklenmesini kapsar.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Yeni PSD Katmanı Oluştur ve Oluşturma Tarih‑Saatini Java'da Yönet
url: /tr/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Yeni PSD Katmanı Oluşturma ve Oluşturulma Tarih‑Saatini Java’da Yönetme

## Giriş
Photoshop (PSD) dosyalarıyla programlı olarak çalışırken, **create new PSD layer** nesneleri oluşturabilmek ve oluşturulma zaman damgalarını takip edebilmek gerçek bir oyun değiştiricidir. Tasarım varlıkları için bir sürüm kontrol sistemi kuruyor olun, toplu düzenlemeleri otomatikleştiriyor olun ya da sadece işbirlikçi projeler için bir denetim izi gerekiyor olsun, katmanın oluşturulma tarihini okuyup ayarlamayı bilmek her değişikliğin tam kökenini korumanızı sağlar. Bu öğreticide Aspose.PSD for Java kullanarak tüm süreci adım adım inceleyeceğiz—bir PSD dosyasını yüklemek, bir katmanın oluşturulma tarihini almak, doğrulamak ve sonunda yepyeni bir ayar katmanı eklemek.

## Hızlı Yanıtlar
- **Java’da PSD dosyalarını işleyen kütüphane nedir?** Aspose.PSD for Java  
- **Bir katmanın oluşturulma tarihini okuyabilir miyim?** Evet, `layer.getLayerCreationDateTime()` kullanarak  
- **Yeni bir ayar katmanı eklemek mümkün mü?** Kesinlikle – `im.addLevelsAdjustmentLayer()` bir tane oluşturur  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Deneme dışı dağıtımlar için ticari bir lisans gereklidir  
- **Hangi Java sürümü destekleniyor?** JDK 8 veya üzeri  

## “create new PSD layer” nedir?
Yeni bir PSD katmanı oluşturmak, programlı olarak mevcut bir PSD belgesine yeni bir katman nesnesi—örneğin bir ayar, metin veya piksel katmanı—eklemek anlamına gelir. Bu işlem, Photoshop’u manuel olarak açmadan görüntüyü genişletmenizi veya değiştirmenizi sağlar.

## Katman oluşturulma Tarih‑Saatini neden yönetmeliyiz?
Her katmanın oluşturulma Tarih‑Saatini takip etmek şunlara yardımcı olur:
- **Revizyonları denetle** – bir katmanın ne zaman eklendiğini tam olarak bilin.  
- **Varlıkları senkronize et** ekipler arasında zaman damgalarını karşılaştırarak.  
- **Zaman‑tabanlı kurallara** (ör. bir aydan eski katmanları gizle) dayanan iş akışlarını otomatikleştir.  

## Önkoşullar
Başlamadan önce, aşağıdakilerin hazır olduğundan emin olun:

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans veya tercih ettiğiniz herhangi bir editör.  
3. **Aspose.PSD for Java** – kurulum için [buradan indirebilirsiniz](https://releases.aspose.com/psd/java/).  
4. **Temel Java bilgisi** – Java’ya yeniyseniz endişelenmeyin; kod tamamen yorumlanmıştır.

Her şey hazır mı? Harika! Kodlamanın eğlenceli kısmına geçelim.

## Paketleri İçe Aktar
İlk olarak, ihtiyacınız olan Aspose.PSD sınıflarını ve Java yardımcı programlarını içe aktarın. Bu içe aktarmalar, görüntü işleme, katman manipülasyonu ve tarih biçimlendirme erişimi sağlar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## Adım 1: Belge Dizinini Ayarla
Üzerinde çalışmak istediğiniz PSD dosyasını içeren klasörü belirtin. Yer tutucuyu makinenizdeki mutlak yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: PSD Dosyasını Yükle
Hedef dosyayı yükleyerek bir `PsdImage` örneği oluşturun. Bu nesne, tüm katman işlemleri için giriş noktasıdır.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## Adım 3: Katmana ve Oluşturulma Tarihine Eriş
İlk katmanı (indeks 0) alın ve oluşturulma zaman damgasını alın. Bu, daha sonra karşılaştıracağınız veya kaydedeceğiniz tarihtir.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## Adım 4: Oluşturulma Tarihini Biçimlendir
Ham `Date` nesnesini insan tarafından okunabilir bir dizeye dönüştürün. Farklı bir format tercih ederseniz deseni ayarlayın.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## Adım 5: Oluşturulma Tarihini Doğrula
Gösterim amaçlı, alınan tarihi beklenen bir değerle karşılaştırıyoruz. Gerçek projelerde bir veritabanı kaydı veya yapılandırma dosyasıyla karşılaştırabilirsiniz.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## Adım 6: Yeni Bir Katman Oluştur
Şimdi gerçekten **create new PSD layer** nesneleri oluşturuyoruz. Burada bir Levels ayar katmanı ekliyoruz; bu, orijinal pikselleri değiştirmeden ton aralıklarını ayarlamanızı sağlar.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **Pro ipucu:** `now` değişkeni katmanı eklediğiniz anı yakalar; özel bir zaman damgasına ihtiyacınız olursa bunu daha sonra meta veri olarak saklayabilirsiniz.

## Yaygın Sorunlar ve Çözümleri
| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| `layer.getLayerCreationDateTime()` üzerinde `NullPointerException` | PSD'de katman yoktur veya katman indeksi aralık dışındadır. | Erişmeden önce `im.getLayers().length > 0` olduğundan emin olun. |
| Doğrulamada tarih uyumsuzluğu | `Date` yapıcı, dizeleri yerel ayara bağlı olarak ayrıştırır. | Güvenilir ayrıştırma için `SimpleDateFormat.parse("2018/07/17 08:57:24")` kullanın. |
| Yeni katman Photoshop'ta görünmüyor | Ayar katmanı varsayılan olarak gizli olabilir. | Oluşturduktan sonra `createdLayer.setVisible(true);` çağırın. |

## Sonuç
Artık **create new PSD layer** nesnelerini nasıl oluşturacağınızı, oluşturulma zaman damgalarını nasıl okuyacağınızı, bu zaman damgalarını nasıl doğrulayacağınızı ve ayar katmanları ekleyeceğinizi biliyorsunuz—hepsi Aspose.PSD for Java kullanarak. Bu yetenek, herhangi bir Java tabanlı görüntü işleme hattında gelişmiş otomasyon, denetim izleri ve işbirlikçi iş akışlarının kapılarını açar.

Bu öğreticiden keyif aldıysanız, katman birleştirme, filtre uygulama veya farklı formatlara dışa aktarma gibi diğer Aspose.PSD özelliklerini keşfedin. Olanaklar sonsuz!

## SSS
### Aspose.PSD nedir?
Aspose.PSD, Photoshop (PSD) dosyalarıyla programlı olarak çalışmak için güçlü bir kütüphanedir.

### Aspose.PSD'yi ücretsiz kullanabilir miyim?
Evet! Ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) başlayabilirsiniz.

### Uzun vadeli kullanım için lisans satın almam gerekiyor mu?
Evet, hazır olduğunuzda [buradan](https://purchase.aspose.com/buy) bir lisans alabilirsiniz.

### Aspose.PSD hakkında daha fazla bilgi nereden bulabilirim?
Detaylı kılavuzlar ve API referansları için [belgelere](https://reference.aspose.com/psd/java/) göz atabilirsiniz.

### Aspose.PSD ile ilgili sorun yaşarsam nasıl destek alabilirim?
Topluluk desteği için [destek forumunu](https://forum.aspose.com/c/psd/34) ziyaret etmekten çekinmeyin.

---

**Son Güncelleme:** 2026-03-28  
**Test Edilen Sürüm:** Aspose.PSD for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}