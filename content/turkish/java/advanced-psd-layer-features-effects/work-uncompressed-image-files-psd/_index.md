---
title: Java kullanarak PSD'de Sıkıştırılmamış Görüntü Dosyalarıyla Çalışma
linktitle: Java kullanarak PSD'de Sıkıştırılmamış Görüntü Dosyalarıyla Çalışma
second_title: Aspose.PSD Java API'si
description: Bu kapsamlı adım adım eğitimde Java ve Aspose.PSD kütüphanesini kullanarak PSD formatındaki sıkıştırılmamış görüntü dosyalarıyla nasıl çalışılacağını öğrenin.
type: docs
weight: 27
url: /tr/java/advanced-psd-layer-features-effects/work-uncompressed-image-files-psd/
---
## giriiş
Java'da Photoshop belgeleriyle (PSD) çalışmak söz konusu olduğunda, bu zengin görüntü dosyalarının etkili bir şekilde nasıl işleneceğini ve kaydedileceğini anlamak çok önemlidir. Bu eğitimde, sıkıştırılmamış görüntülerle çalışmak da dahil olmak üzere PSD dosyalarının yönetimini kolaylaştıran güçlü bir API olan Aspose.PSD'nin kullanımına derinlemesine bakacağız. İster uygulamanızı zengin grafiklerle geliştirmek isteyen bir geliştirici olun, ister sadece PSD dosyalarını Java'da zahmetsizce işlemek istiyor olun, bu kılavuz yolun her adımında size yol gösterecektir. Başlamaya hazır mısınız? Hadi atlayalım!
## Önkoşullar
Kollarımızı sıvayıp kodlamaya başlamadan önce listemize göz atmamız gereken birkaç önkoşul var. Merak etme; oldukça basitler!
### Java Geliştirme Kiti (JDK)
- Sisteminizde JDK 8 veya üzerinin kurulu olduğundan emin olun. Değilse, şu adrese gidin:[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ve en son sürümü indirin.
### Entegre Geliştirme Ortamı (IDE)
- IntelliJ IDEA, Eclipse veya NetBeans gibi iyi bir IDE hayatınızı kolaylaştıracaktır. Henüz yapmadıysanız bir tane ayarlayın!
### Java Kütüphanesi için Aspose.PSD
-  Aspose.PSD for Java kütüphanesini indirin. En son sürümleri alabilirsiniz[Burada](https://releases.aspose.com/psd/java/). 
### Temel Java Bilgisi 
- Sorunsuz bir şekilde takip edebilmek için Java programlama ve nesne yönelimli paradigma hakkında temel bir anlayışa sahip olmalısınız.
### Bir PSD Dosyası
- Örnek bir PSD dosyasını test için hazır bulundurun. Photoshop'ta bir tane oluşturabilir veya çevrimiçi olarak ücretsiz bir örnek indirebilirsiniz. 
Artık her şey hazır olduğuna göre kodlara geçelim!
## Paketleri İçe Aktar
Başlangıç olarak kodumuz için gerekli olan paketleri içe aktarmamız gerekiyor. İhtiyaç duyacağınız ithalatların listesi aşağıdadır:
```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
Bu içe aktarmalar, gerekli sınıfları ve yöntemleri projemize getirecek ve PSD dosyalarını sorunsuz bir şekilde işlememize olanak tanıyacaktır. 
Süreci yönetilebilir adımlara ayıralım. 
## 1. Adım: Dosya Dizininizi Ayarlama
Öncelikle PSD dosyanızın nerede bulunduğunu ve çıktınızı nereye kaydetmek istediğinizi belirtmeniz gerekir. Örnek kodumuzda dizin yolunu tutacak bir değişken oluşturacağız.
```java
String dataDir = "Your Document Directory";
```
 Yer değiştirmek`"Your Document Directory"` PSD dosyanızın bulunduğu gerçek yolla (`layers.psd`) saklanır. Bunu yaparak programınızın dosyayı nerede arayacağını bilmesini sağlarsınız.
## Adım 2: PSD Dosyasını Yükleme
 Şimdi PSD dosyasını kullanarak yükleyelim.`Image.load()` bir yönteme dönüştürerek`PsdImage` tip.
```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```
 Bu satır şunu çağırır:`load` gelen yöntem`Image` sınıf, PSD dosyanızı belleğe yüklüyor. Onu dökerek`PsdImage`, Java'ya bu görüntüyü PSD işlemleriyle ilgili belirli işlevlere sahip bir PSD dosyası olarak ele almasını söylüyoruz.
## 3. Adım: Kaydetme Seçeneklerini Yapılandırma
Daha sonra, özellikle çıktının sıkıştırılmamış olmasını istediğimizi belirterek, dosyamızı kaydetme seçeneklerini ayarlamamız gerekiyor.
```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```
`PsdOptions` class, PSD dosyamızı kaydetmek için çeşitli seçenekler belirlememize olanak tanır. Ayar`setCompressionMethod` ile`CompressionMethod.Raw` kaydedilen dosyamızın sıkıştırılmamış olmasını ve yüksek kaliteyi korumasını sağlar.
## Adım 4: Sıkıştırılmamış PSD Dosyasını Kaydetme
Şimdi yeni yapılandırılan PSD görüntüsünü kaydetmenin zamanı geldi.
```java
psdImage.save(dataDir + "uncompressed_out.psd", saveOptions);
```
 Bu satır bizim cihazımızdaki kaydetme fonksiyonunu çalıştırır.`PsdImage` misal (`psdImage` ). Dosyayı şu şekilde kaydeder:`uncompressed_out.psd` belirtilen dizinde bulunur ve daha önce tanımlanan seçenekleri uygular.
## Adım 5: Yeni Oluşturulan Resmi Yeniden Açma
Kaydettikten sonra her şeyin beklendiği gibi çalıştığını doğrulamak için çıktı görselimizi yeniden yükleyelim.
```java
PsdImage img = (PsdImage) Image.load(dataDir + "uncompressed_out.psd");
```
 Arayarak`load` tekrar yeni bir örnek oluşturabiliriz`PsdImage` bu kaydedilen dosyaya karşılık gelir. Görüntüyü kaydettikten sonra değiştirmek veya görüntülemek istiyorsanız bu adım çok önemlidir.
## Adım 6: Görüntüyü Çizmek veya Değiştirmek
Son olarak, yeni açılan görüntünün üzerine çizim yapmak veya üzerinde değişiklik yapmak isteyebilirsiniz.
```java
Graphics graphics = new Graphics(img);
```
 Burada bir başlatıyoruz`Graphics` nesnemiz üzerinde çeşitli grafiksel işlemler yapmamızı sağlayan nesnedir.`img`. İsterseniz şekiller çizebilir, metin ekleyebilir ve hatta katmanları değiştirebilirsiniz!
## Çözüm
Tebrikler! Java ve Aspose.PSD kütüphanesini kullanarak PSD formatındaki sıkıştırılmamış görüntü dosyalarıyla nasıl çalışacağınızı öğrendiniz. Bu güçlü API, PSD dosyalarını yüklerken, değiştirirken veya farklı formatlarda kaydederken kolaylıkla yönetmenize olanak tanır. Öyleyse devam edin ve bir tur atın! Farklı özellikleri deneyin, grafiklerle oynayın ve ne kadar heyecan verici şeyler yaratabileceğinizi görün.
 Kontrol etmeyi unutmayın[dokümantasyon](https://reference.aspose.com/psd/java/) Daha gelişmiş özellikler ve seçenekler için. Doğrudan konuya dalmak istiyorsanız kütüphaneyi indirebilirsiniz.[Burada](https://releases.aspose.com/psd/java/) veya ücretsiz deneme sürümünü başlatın. Herhangi bir sorunuz varsa, ziyaret etmekten çekinmeyin[destek forumu](https://forum.aspose.com/c/psd/34) toplumdan yardım almak için.
## SSS'ler
### Java için Aspose.PSD nedir?
Aspose.PSD for Java, geliştiricilerin Photoshop PSD dosyalarıyla programlı olarak çalışmasına olanak tanıyan bir Java kitaplığıdır.
### Aspose.PSD'yi kullanarak bir PSD dosyasındaki katmanları değiştirebilir miyim?
Evet! Aspose.PSD, katmanlara erişmenizi ve bunları değiştirmenizi sağlayarak karmaşık işlemleri gerçekleştirmenizi kolaylaştırır.
### Aspose.PSD'nin kullanımı ücretsiz mi?
Ücretsiz deneme sürümü mevcuttur ancak kapsamlı kullanım ve gelişmiş özelliklere erişim için bir lisans satın almanız gerekebilir.
### Sorunlarla karşılaşırsam destek ekibiyle nasıl iletişime geçebilirim?
 aracılığıyla ulaşabilirsiniz.[Aspose destek forumu](https://forum.aspose.com/c/psd/34) yardım için.
### Aspose.PSD, PSD dışındaki formatlarda kaydetmeyi destekliyor mu?
Evet, Aspose.PSD, gereksinimlerinize bağlı olarak PNG, JPEG ve daha fazlası gibi farklı formatlarda kaydetmenize olanak tanır.