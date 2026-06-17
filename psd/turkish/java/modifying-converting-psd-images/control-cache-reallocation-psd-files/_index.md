---
date: 2026-03-13
description: Aspose.PSD for Java ile önbellek yeniden tahsis yönetimini yaparken PSD
  görüntü Java projeleri oluşturmayı öğrenin. Bellek ve disk kullanımını verimli bir
  şekilde optimize edin.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Java ile PSD Görüntüsü Oluştur – Önbellek Yeniden Tahsisini Kontrol Et
url: /tr/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

 Turkish translation is natural.

Let's craft translations.

I'll write.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında Önbellek Yeniden Tahsisini Kontrol Etme

## Introduction
Eğer **create PSD image java** projelerini verimli bir şekilde oluşturmanız gerekiyorsa, önbellek yeniden tahsisinin kontrol edilmesi çok önemlidir. Görseller ve Photoshop dosyalarıyla programatik olarak çalışırken verimlilik temel bir faktördür. Aspose.PSD for Java, PSD dosyalarını sorunsuz bir şekilde yönetmek ve manipüle etmek için güçlü özellikler sunar. Performansı optimize etmenin temel yönlerinden biri, önbellek yeniden tahsisinin kontrol edilmesidir. Önbellek yönetimi, bellek ve disk kullanımı arasındaki dengeyi korumaya yardımcı olur, uygulamanızın beklenmedik çöküşler veya yavaşlamalar olmadan sorunsuz çalışmasını sağlar. 

## Quick Answers
- **Cache yeniden tahsisi ne işe yarar?** Büyük PSD dosyaları işlenirken bellek ve disk kullanımını dengeler.  
- **Büyük görseller için hangi önbellek türü en iyisidir?** `CacheOnDiskOnly`, önbelleği diske kaydederek belleği boş tutar.  
- **Ne kadar disk alanı ayırabilirim?** `setMaxDiskSpaceForCache` ile belirlediğiniz herhangi bir boyuta kadar, en fazla 1 GB.  
- **Bu özellikleri kullanmak için lisansa ihtiyacım var mı?** Bir lisans deneme sınırlamalarını kaldırır; Aspose satın alma sayfasına bakın.  
- **Çalışma zamanında önbellek kullanımını izleyebilir miyim?** Evet, `Cache.getAllocatedDiskBytesCount()` ve `Cache.getAllocatedMemoryBytesCount()` kullanın.

## Why Control Cache Reallocation?
Yüksek çözünürlüklü veya çok katmanlı dosyalarla çalışan **create PSD image java** uygulamaları geliştirirken önbelleği yönetmek kritik öneme sahiptir. Doğru önbellek ayarları, bellek dışı hataları önler, GC duraklamalarını azaltır ve sunucularda ya da masaüstü uygulamalarında öngörülebilir performans sağlar.

## Prerequisites
Kodlama kısmına geçmeden önce her şeyin sorunsuz çalışması için aşağıdaki maddeleri kontrol edin:
1. Java Development Kit (JDK): Makinenizde JDK yüklü olduğundan emin olun. İndirmek için [Oracle'ın web sitesini](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ziyaret edin.
2. Aspose.PSD for Java: Aspose.PSD kütüphanesini indirmeniz gerekir. En son sürümü [burada](https://releases.aspose.com/psd/java/) bulabilirsiniz.
3. IDE Setup: IntelliJ IDEA veya Eclipse gibi bir Entegre Geliştirme Ortamı (IDE), kodunuzu yönetmenizi kolaylaştırır.
4. Basic Understanding of Java: Java programlamasına aşina olmak, kavramları ve kod parçacıklarını daha iyi anlamanıza yardımcı olur.
5. Aspose License (Optional): Filigranları kaldırmak ve tam işlevselliği elde etmek istiyorsanız, bir lisans satın almayı [buradan](https://purchase.aspose.com/buy) veya ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) değerlendirin.

## Import Packages
Kod yazmaya başlamadan önce gerekli paketlerin içe aktarıldığından emin olun. Aşağıda Java dosyanızın başında bulunması gereken kısa bir paket listesi yer almaktadır:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## How to Create PSD Image Java with Cache Control
Aşağıda, önbellek yapılandırmasını doğrudan Java’da PSD görüntüsü oluşturma sürecine bağlayan adım adım bir rehber bulacaksınız.

### Step 1: Setting Up Your Data Directory
İlk olarak, önbellek dosyalarınızın depolanmasını istediğiniz bir dizin oluşturmanız gerekir. Bu, önbelleği etkili bir şekilde yönetmek için gereklidir.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Belge önbelleğiniz için dizini tanımlar.  
- `Cache.setCacheFolder(dataDir)`: Bu yöntem, önbellek klasörünü belirtilen dizine ayarlar. Aspose tarafından oluşturulan tüm önbellek artık varsayılan geçici klasör yerine burada saklanır.

### Step 2: Configuring Cache To Disk
Sonra, önbelleğin yalnızca diske kaydedilmesini isteyeceğimizi belirteceğiz. Bu, uygulamanız büyük dosyalar kullanıyorsa ve belleğin serbest kalmasını sağlamak istiyorsanız özellikle faydalıdır.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Bu seçenek, önbelleğin bellekte tutulmamasını sağlar; bu da büyük PSD dosyalarını çok fazla RAM tüketmeden işlemenize yardımcı olur.

### Step 3: Setting Maximum Disk and Memory Cache Size
Şimdi önbellek boyutlarımızı sınırlayalım. Sınırsız önbellek, performans sorunlarına yol açabileceği için bu kritik bir adımdır.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Disk üzerindeki önbellek için 1 GB sınırı koyar. İhtiyacınıza göre bu boyutu ayarlayabilirsiniz.  
- `Cache.setMaxMemoryForCache(1073741824)`: Benzer şekilde, bellek içi önbelleği sınırlar ve uygulamanızın aşırı bellek kullanmasını engeller.

### Step 4: Manage Cache Reallocation Strategy
Önbelleğin nasıl yeniden tahsis edileceğini yönetmek, performansı korumak açısından önemlidir. İşte bunu nasıl ayarlayabileceğiniz:
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: `false` olarak ayarlandığında, Aspose önbellek yeniden tahsisinde daha esnek davranabilir ve bu da daha iyi performansa yol açabilir.

### Step 5: Check Allocated Cache Size
Bu adım, önbelleğin şu anda bellekte ya da diskte kaç bayt tahsis edildiğini izlemeyi kapsar. Şimdi bunu uygulayalım:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Diskte tahsis edilen bayt sayısını saklar.  
- `long l2`: Bellekte tahsis edilen bayt sayısını saklar.  
Bu değerleri istediğiniz zaman kontrol ederek uygulamanızın bellek ve disk kullanımını beklendiği gibi yönettiğinden emin olabilirsiniz.

### Step 6: Creating a PSD Image
Önbellek yapılandırmalarımız hazır olduğuna göre, basit bir PSD görüntüsü oluşturalım.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Photoshop görüntüsü oluştururken seçenekleri belirlemenizi sağlayan bir nesnedir.  
- `Color[] color`: Görüntü paletinde kullanılacak renkleri içeren bir dizi.

### Step 7: Saving Pixel Data to the Image
Şimdi görüntümüzü piksel verileriyle doldurup kaydedelim.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Renk nesnelerinden oluşan bir dizi. Burada beyaz piksellerle dolduruyoruz.  
- `image.savePixels(image.getBounds(), pixels)`: Bu yöntem, piksel verilerini görüntüye kaydeder. Tanımladığımız renklerle görüntüyü günceller.

### Step 8: Monitoring Allocated Cache After Image Creation
Görüntüyü oluşturduktan sonra, önbellekte kaç bayt tahsis edildiğini tekrar kontrol etmek iyi bir uygulamadır.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Görüntü oluşturulduktan sonra diskteki mevcut tahsisi yakalar.  
- `long memoryBytes`: Bellekteki mevcut tahsisi yakalar.  
Bu adım, işlemlerinizin ardından ne kadar önbellek tüketildiğini belirlemenize yardımcı olur.

### Step 9: Check for Proper Disposal
Son olarak, tüm Aspose.PSD nesnelerinin doğru bir şekilde serbest bırakıldığından emin olmak, bellek sızıntılarını önlemek için kritiktir.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` ve `l2`: Bu değişkenler, son tahsisi kontrol etmenize yardımcı olur. Eğer sıfır değillerse, bazı nesnelerin doğru şekilde serbest bırakılmadığını gösterir.

## Common Issues and Solutions
- **Cache folder not created** – `Cache.setCacheFolder` ile belirttiğiniz yola uygulamanın yazma izni olduğundan emin olun.  
- **Out‑of‑memory errors** – Büyük PSD dosyalarını yüklemeden önce `Cache.setCacheType(CacheType.CacheOnDiskOnly)` uygulandığını iki kez kontrol edin.  
- **Unexpected cache size** – Her büyük işlemden sonra `Cache.getAllocated*BytesCount()` metodlarını kullanarak büyümeyi izleyin.

## Frequently Asked Questions

**Q: Aspose.PSD nedir?**  
A: Aspose.PSD, .NET ve Java geliştiricileri için Photoshop (PSD) dosyalarını programatik olarak oluşturma, manipüle etme ve dönüştürme imkanı sağlayan bir kütüphanedir.

**Q: Tahsis edilen önbellek boyutunu nasıl kontrol ederim?**  
A: `Cache.getAllocatedDiskBytesCount()` ve `Cache.getAllocatedMemoryBytesCount()` gibi metodları kullanarak mevcut önbellek kullanımını izleyebilirsiniz.

**Q: Önbellek için özel bir dizin belirleyebilir miyim?**  
A: Evet, `Cache.setCacheFolder("Your Directory Path")` kullanarak farklı bir dizin belirtebilirsiniz.

**Q: Aspose.PSD ücretsiz mi?**  
A: Aspose.PSD ücretli bir kütüphanedir, ancak [web sitesinde](https://releases.aspose.com/) sunulan ücretsiz deneme sürümüyle başlayabilirsiniz.

**Q: Nesneleri serbest bırakmazsam ne olur?**  
A: Nesneleri serbest bırakmamak bellek sızıntılarına yol açar ve uygulamanızın gereğinden fazla kaynak tüketmesine neden olur.

## Conclusion
**create PSD image java** uygulamaları geliştirirken önbellek yeniden tahsisinin kontrol edilmesi performans üzerinde büyük bir fark yaratabilir. Yukarıdaki adımları izleyerek önbelleği verimli bir şekilde yönetecek, bellek tüketimini minimize edecek ve Aspose.PSD for Java ile yüksek kaliteli PSD dosyaları üretebileceksiniz. Bu teknikleri uygulayın, projeleriniz daha akıcı çalışsın ve ölçeklenebilirliği artsın.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}