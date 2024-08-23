---
title: PSD Dosyalarında Önbellek Yeniden Tahsilatını Kontrol Etme
linktitle: PSD Dosyalarında Önbellek Yeniden Tahsilatını Kontrol Etme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PSD dosyalarında önbellek yeniden tahsisini yönetin. Geliştiriciler için ideal olan belleği ve dosya işlemeyi verimli bir şekilde nasıl optimize edeceğinizi öğrenin.
type: docs
weight: 22
url: /tr/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---
## giriiş
Görüntülerle ve Photoshop dosyalarıyla programlı olarak çalışırken verimlilik önemli bir faktördür. Aspose.PSD for Java, PSD dosyalarını sorunsuz bir şekilde yönetmek ve işlemek için güçlü özellikler sunar. Performansı optimize etmenin temel yönlerinden biri, önbellek yeniden tahsisinin kontrol edilmesidir. Önbellek yönetimi, bellek ve disk kullanımı arasındaki dengenin korunmasına yardımcı olarak uygulamanızın beklenmedik çökmeler veya yavaşlamalar olmadan sorunsuz bir şekilde çalışmasını sağlar. 
## Önkoşullar
Kodlama kısmına geçmeden önce her şeyin sorunsuz ilerlemesi için emin olmanız gereken birkaç şey var:
1. Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Oracle'ın web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Aspose.PSD kütüphanesini indirmeniz gerekir. En son sürümü bulabilirsiniz[Burada](https://releases.aspose.com/psd/java/).
3. IDE Kurulumu: IntelliJ IDEA veya Eclipse gibi bir Entegre Geliştirme Ortamı (IDE), kodunuzu yönetmenizi kolaylaştıracaktır.
4. Temel Java Anlayışı: Java programlamaya aşinalık, kavramları ve kod parçacıklarını daha iyi anlamanıza yardımcı olacaktır.
5.  Lisansı Aspose (İsteğe bağlı): Filigranları kaldırmak ve tam işlevsellik kazanmak istiyorsanız bir lisans satın almayı düşünün[Burada](https://purchase.aspose.com/buy) veya ücretsiz denemeyi denemek[Burada](https://releases.aspose.com/).
## Paketleri İçe Aktar
Kodu yazmaya başlamadan önce gerekli paketlerin içe aktarıldığından emin olalım. Aşağıda Java dosyanızın başına neler ekleyeceğinizin kısa bir listesi verilmiştir:
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
## 1. Adım: Veri Dizininizi Kurma
Öncelikle önbellek dosyalarınızın saklanmasını istediğiniz bir dizin ayarlamanız gerekir. Bu, önbelleği etkili bir şekilde yönetmek için gereklidir.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Belge önbelleğiniz için dizini tanımlayın.
- Cache.setCacheFolder(dataDir): Bu yöntem, önbellek klasörünü belirtilen dizine ayarlar. Aspose tarafından oluşturulan önbellek artık varsayılan geçici dizin yerine burada saklanacak.
## Adım 2: Önbelleği Diske Yapılandırma
Daha sonra önbelleğimizin yalnızca diskte saklanmasını istediğimizi belirteceğiz. Bu, özellikle uygulamanız büyük dosyalar kullanıyorsa ve belleğin boş kalmasını istiyorsanız kullanışlıdır.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Bu seçenek, önbelleğin bellekte tutulmamasını sağlar; bu, çok fazla RAM tüketmeden büyük PSD dosyalarının işlenmesi için faydalıdır.
## 3. Adım: Maksimum Disk ve Bellek Önbellek Boyutunu Ayarlama
Şimdi önbellek boyutlarımızı kısıtlayalım. Bu çok önemlidir çünkü sınırsız önbellek performans sorunlarına yol açabilir.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabayt
Cache.setMaxMemoryForCache(1073741824); // 1 gigabayt
```

- Cache.setMaxDiskSpaceForCache(1073741824): Bu, diskteki önbellek için 1 GB sınırını ayarlar. Bu boyutu ihtiyaçlarınıza göre ayarlayabilirsiniz.
- Cache.setMaxMemoryForCache(1073741824): Benzer şekilde, bu, bellek içi önbelleği sınırlayarak uygulamanızın aşırı bellek kullanmamasını sağlar.
## 4. Adım: Önbellek Yeniden Tahsilat Stratejisini Yönetin
Performansı korumak için önbelleğin nasıl yeniden tahsis edildiğini yönetmek önemlidir. Bunu nasıl ayarlayabileceğiniz aşağıda açıklanmıştır.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): False olarak ayarlandığında bu, Aspose'un önbellek yeniden tahsisini daha esnek bir şekilde yönetmesine olanak tanır ve bu da daha iyi performans sağlayabilir.
## Adım 5: Ayrılan Önbellek Boyutunu Kontrol Edin
Bu adım, bellekte veya diskte önbellek için şu anda kaç bayt ayrıldığının izlenmesiyle ilgilidir. Bunu uygulayalım:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Diskte ayrılan bayt sayısını saklar.
- long l2: Bellekte ayrılan bayt sayısını saklar. 
Uygulamanızın bellek ve disk kullanımını beklendiği gibi yönettiğinden emin olmak için bu değerleri istediğiniz zaman kontrol edebilirsiniz.
## Adım 6: PSD Görüntüsü Oluşturma
Artık önbellek yapılandırmalarımızı ayarladığımıza göre basit bir PSD görüntüsü oluşturalım.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions seçenekleri: Bu nesne, Photoshop görüntüsü oluştururken seçenekleri belirlemenizi sağlar.
- Renk[] color: Görüntü paletinde kullanılacak renkleri içeren dizi.
## Adım 7: Piksel Verilerini Görüntüye Kaydetme
Şimdi görselimizi piksel verileriyle doldurup kaydedelim.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Renk[] piksel: Bu, renkli nesnelerin dizisidir. Burada onu beyaz piksellerle dolduruyoruz.
- image.savePixels(image.getBounds(), piksel): Bu yöntem piksel verilerini görüntüye kaydeder. Görüntüyü tanımladığımız renklerle günceller.
## Adım 8: Görüntü Oluşturulduktan Sonra Ayrılan Önbelleği İzleme
Görüntüyü oluşturduktan sonra önbelleğe kaç bayt ayrıldığını tekrar kontrol etmek iyi bir uygulamadır.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: Görüntü oluşturulduktan sonra diskteki mevcut tahsisi yakalar.
- long MemoryBytes: Bellekteki mevcut tahsisi yakalar. 
Bu adım, işlemlerinizden sonra ne kadar önbellek tüketildiğini belirlemenize yardımcı olacaktır.
## Adım 9: Uygun İmha Edildiğini Kontrol Edin
Son olarak, bellek sızıntılarını önlemek için tüm Aspose.PSD nesnelerinin uygun şekilde atıldığından emin olmak çok önemlidir.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 ve l2: Bu değişkenler nihai tahsisi kontrol etmenize yardımcı olacaktır. Sıfır değilse bu, bazı nesnelerin uygun şekilde atılmadığını gösterir.
## Çözüm
Aspose.PSD for Java'da önbellek yeniden tahsisini kontrol etmek, uygulamanızın performansında önemli bir fark yaratabilir. Yukarıda özetlenen adımları izleyerek önbelleği etkili bir şekilde yönetebilir, bellek kullanımını en aza indirebilir ve güzel PSD dosyalarını verimli bir şekilde oluşturabilirsiniz. Bu teknikleri benimseyin ve uygulamalarınızın optimum performansla gelişmesini izleyin!
## SSS'ler
### Aspose.PSD nedir?
Aspose.PSD, .NET ve Java geliştiricilerinin Photoshop (PSD) dosyalarını programlı olarak oluşturmasına, değiştirmesine ve dönüştürmesine yönelik bir kitaplıktır.
### Ayrılan önbellek boyutunu nasıl kontrol ederim?
 Gibi yöntemleri kullanın`Cache.getAllocatedDiskBytesCount()` Ve`Cache.getAllocatedMemoryBytesCount()` mevcut önbellek kullanımını izlemek için.
### Önbellek için özel bir dizin ayarlayabilir miyim?
 Evet, kullanarak farklı bir dizin belirleyebilirsiniz.`Cache.setCacheFolder("Your Directory Path")`.
### Aspose.PSD'nin kullanımı ücretsiz mi?
Aspose.PSD ücretli bir kütüphanedir, ancak kendi sitelerinde bulunan ücretsiz deneme sürümüyle başlayabilirsiniz.[web sitesi](https://releases.aspose.com/).
### Nesneleri atmazsam ne olur?
Nesnelerin atılmaması bellek sızıntılarına yol açarak uygulamanızın gereğinden fazla kaynak kullanmasına neden olabilir.