---
date: 2026-03-26
description: Aspose.PSD for Java kullanarak psd görüntülerini katmanlara nasıl içe
  aktaracağınızı öğrenin. Bu adım adım kılavuz, görüntüyü nasıl ekleyeceğinizi, katman
  koordinatlarını nasıl ayarlayacağınızı ve psd katman rengini nasıl dolduracağınızı
  gösterir.
linktitle: How to Import PSD Images to Layers using Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Aspose.PSD Java ile PSD Görüntülerini Katmanlara Nasıl İçe Aktarırsınız
url: /tr/java/psd-image-modification-conversion/import-images-psd-layers/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java kullanarak PSD Görüntülerini Katmanlara Nasıl İçe Aktarılır

## Giriş
PSD dosyalarıyla çalışırken **psd dosyalarını nasıl içe aktarılır** sorusunun programatik olarak yanıtını bilmek, saatler süren manuel işi ortadan kaldırabilir. İster bir grafik tasarımcı, ister bir tasarım‑otomasyon aracı geliştiren bir geliştirici, ister sadece bir sunumu renklendirmek isteyen biri olun, katman manipülasyonunu öğrenmek yaratıcı olasılıkların kapılarını açar. Bu öğreticide, Aspose.PSD for Java kullanarak **psd görüntülerini katmanlara nasıl içe aktarılır** adım adım, bolca pratik ipucu eşliğinde öğreneceksiniz. Bir kahve alın ve başlayalım!

## Hızlı Yanıtlar
- **Bu öğretici neyi kapsıyor?** Aspose.PSD for Java ile bir PSD katmanına görüntü ekleme.  
- **Hangi kütüphane sürümü gerekiyor?** API geriye dönük uyumlu olduğu için herhangi bir yeni Aspose.PSD for Java sürümü yeterlidir.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü yeterli; üretim ortamı için ticari lisans gerekir.  
- **Uygulama ne kadar sürer?** Temel bir içe aktarma için yaklaşık 10‑15 dakika.  
- **Görüntü boyutunu veya konumunu değiştirebilir miyim?** Evet – katman koordinatlarını ve doldurma renklerini ihtiyacınıza göre ayarlayabilirsiniz.

## “how to import psd” nedir?
PSD içe aktarmak, bir Photoshop belgesini programatik olarak yüklemek, katmanlarını (örneğin bir görüntü ekleyerek) değiştirmek ve ardından güncellenmiş dosyayı kaydetmek anlamına gelir. Bu yaklaşım toplu işleme, otomatik grafik üretimi veya tasarım varlıklarını daha büyük uygulamalara entegre etme gibi senaryolar için idealdir.

## Neden Aspose.PSD for Java Kullanmalı?
Aspose.PSD, karmaşık PSD dosya formatını soyutlayan tamamen yönetilen, lisans‑ücretsiz bir API sunar. Şunları elde edersiniz:
- Katmanlara, maskelere ve kanal verilerine doğrudan erişim.  
- Photoshop veya üçüncü‑taraf yerel kütüphanelere ihtiyaç yok.  
- Renk profilleri, karıştırma modları ve sıkıştırma için tam destek.  

## Önkoşullar
Eğlenceli bölümlere geçmeden önce her şeyin hazır olduğundan emin olalım! İşte ihtiyacınız olanlar:

- Java Development Kit (JDK): Makinenizde JDK yüklü olduğundan emin olun. En son sürümü [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.  
- Aspose.PSD for Java: Aspose.PSD kütüphanesine ihtiyacınız var. İndirme bağlantısı için [release link](https://releases.aspose.com/psd/java/) adresini ziyaret edin. Bu kütüphane, PSD dosyalarını manipüle etmek için gerekli tüm işlevleri sağlar.  
- IDE: IntelliJ IDEA veya Eclipse gibi bir Entegre Geliştirme Ortamı kodlamayı ve hata ayıklamayı kolaylaştırır.  
- Temel Java Bilgisi: Temel Java kavramlarına aşina olmak, içeriği sorunsuz takip etmenizi sağlar.  

Bu önkoşulları tamamladıysanız, PSD maceranıza hazırsınız!

## PSD Görüntülerini Katmanlara Nasıl İçe Aktarılır
Aşağıda **psd katmanına görüntü ekleme**, **katman koordinatlarını ayarlama** ve **psd katman rengini doldurma** adımlarını açıklayan net, numaralı bir rehber bulacaksınız.

### Adım 1: Gerekli Paketleri İçe Aktar
İlk olarak, ihtiyacımız olan Aspose.PSD sınıflarını içe aktarırız. Bu, kodun geri kalan kısmı için temeli oluşturur.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

### Adım 2: Belge Dizini Ayarla
Kaynak PSD dosyanızın bulunduğu ve sonucun kaydedileceği yeri tanımlayın.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini, PSD dosyalarınızın bulunduğu gerçek dosya yolu ile değiştirin.

### Adım 3: PSD Dosyanızı Yükleyin
Katmanlarla çalışabilmek için PSD dosyasını açın.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

`"sample.psd"` kısmının, düzenlemek istediğiniz dosya adıyla eşleştiğinden emin olun.

### Adım 4: Hedef Katmanı Çıkar
Yeni görüntüyü alacak katmanı seçin. Bu örnekte ikinci katman (indeks 1) kullanılıyor.

```java
Layer layer = image.getLayers()[1];
```

Farklı bir katman gerekiyorsa, sadece indeksi değiştirin.

### Adım 5: İçe Aktarmak İçin Yeni Bir Görüntü Oluştur
Şimdi **psd katmanına görüntü ekleme** işlemini gerçekleştirmek için yeni bir `PsdImage` oluşturacağız ve üzerine çizeceğiz.

```java
PsdImage drawImage = new PsdImage(200, 200);
```

Kaynak resminizle aynı boyutta olması için genişlik ve yüksekliği ayarlayabilirsiniz.

### Adım 6: Görüntü Yüzeyini Doldur (Katman Rengini Ayarla)
**psd katman rengini doldurma** örneği olarak parlak sarı bir arka plan ekleyelim. Bu, katmana bir katı renk atamayı gösterir.

```java
Graphics g = new Graphics(drawImage);
g.clear(Color.getYellow());
```

`Color.getYellow()` ifadesini, tercih ettiğiniz başka bir `Color` ile değiştirebilirsiniz.

### Adım 7: Görüntüyü Katmana Çizin (Katman Koordinatlarını Ayarla)
İşte **psd katmanına görüntü ekleme**nin özü – yeni oluşturulan görüntüyü seçilen katmana belirli koordinatlarda yerleştiriyoruz.

```java
layer.drawImage(new Point(10, 10), drawImage);
```

`Point(10, 10)` çağrısı **katman koordinatlarını ayarlar** (X = 10, Y = 10). Görüntüyü tam istediğiniz konuma yerleştirmek için bu değerleri değiştirin.

### Adım 8: Güncellenmiş PSD Dosyasını Kaydet
Son olarak, değişiklikleri diske yazın.

```java
image.save(dataDir + "ImportImageToPSDLayer_out.psd");
```

Çıktı dosyasına anlamlı bir ad verin; örnek, orijinali bozulmasın diye `_out` ekliyor.

## Yaygın Sorunlar ve Çözümleri
- **Görüntü boş görünüyor** – Çizim yapmadan önce `Graphics.clear()` çağırdığınızdan emin olun; aksi takdirde tuval şeffaf kalabilir.  
- **Yanlış katman değiştiriliyor** – Katman indekslerinin 0’dan başladığını unutmayın. `getLayers()` içinde kullandığınız indeksi iki kez kontrol edin.  
- **Desteklenmeyen renk profili** – Aspose.PSD çoğu profili yönetir, ancak renk kayması görürseniz, kaynak resmi içe aktarmadan önce sRGB’ye dönüştürmeyi deneyin.  

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, geliştiricilerin PSD dosyalarıyla programatik olarak çalışmasını sağlayan, katmanları, görüntüleri ve diğer özellikleri manipüle etmeye imkan veren bir kütüphanedir.

**S: Aspose.PSD'i başka programlama dillerinde kullanabilir miyim?**  
C: Evet! Aspose, .NET, C++ ve Python dahil olmak üzere çeşitli programlama dilleri için kütüphaneler sunar.

**S: Aspose.PSD for Java için ücretsiz bir sürüm var mı?**  
C: Evet, Aspose [ücretsiz bir deneme sürümü](https://releases.aspose.com/) sunar; indirip denemeye başlayabilirsiniz.

**S: Sorun yaşarsam ne yapmalıyım?**  
C: Yardım almak için [Aspose Destek Forumunu](https://forum.aspose.com/c/psd/34) ziyaret edebilir, topluluk ve Aspose uzmanlarından destek alabilirsiniz.

**S: Aspose.PSD for Java lisansı nasıl satın alınır?**  
C: Lisans satın almak için [Aspose satın alma sayfasını](https://purchase.aspose.com/buy) ziyaret edebilirsiniz.

---

**Son Güncelleme:** 2026-03-26  
**Test Edilen:** Aspose.PSD for Java (en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}