---
date: 2025-12-22
description: Aspose PSD Java kütüphanesini kullanarak sıkıştırma olmadan PSD dışa
  aktarmayı öğrenin. Bu adım adım rehber, Java ile PSD'deki sıkıştırılmamış görüntü
  dosyalarını nasıl işleneceğini gösterir.
linktitle: Work with Uncompressed Image Files in PSD using Java
second_title: Aspose.PSD Java API
title: 'aspose psd java: PSD''de Sıkıştırılmamış Görüntü Dosyalarıyla Çalışma'
url: /tr/java/advanced-psd-layer-features-effects/work-uncompressed-image-files-psd/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'de Sıkıştırılmamış Görüntü Dosyalarıyla Java Kullanarak Çalışma

## Giriş
Java'da Photoshop belgeleri (PSD) ile çalışırken, **aspose psd java** kütüphanesi bu zengin görüntü dosyalarını etkili bir şekilde nasıl manipüle edip kaydedebileceğinizi anlamayı kritik hâle getirir. Bu öğreticide, sıkıştırılmamış görüntülerle çalışma dahil olmak üzere PSD dosyalarını yönetmeyi basitleştiren güçlü bir API olan Aspose.PSD'yi derinlemesine inceleyeceğiz. Uygulamanıza zengin grafikler eklemek isteyen bir geliştirici olun ya da Java'da PSD dosyalarını zahmetsizce işlemek isteyin, bu rehber sizi her adımda yönlendirecek. Başlamaya hazır mısınız? Hadi başlayalım!

## Hızlı Yanıtlar
- **Bir PSD'yi sıkıştırma olmadan nasıl dışa aktarabilirim?** Dosyayı kaydederken `PsdOptions` içinde `CompressionMethod.Raw` kullanın.  
- **Java'da sıkıştırılmamış PSD işleme desteği sağlayan kütüphane hangisidir?** **aspose psd java** kütüphanesi tam destek sunar.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Evet, üretim dağıtımları için ticari bir lisans gereklidir.  
- **Hangi Java sürümü gereklidir?** JDK 8 veya üzeri yeterlidir.  
- **Kaydettikten sonra katmanları manipüle edebilir miyim?** Kesinlikle – kaydedilen dosyayı yeniden yükleyin ve `Graphics` nesnesini kullanarak katmanları çizin veya düzenleyin.

## Sıkıştırma Olmadan PSD'yi Dışa Aktarma aspose psd java Kullanarak
Bir PSD'yi hiçbir sıkıştırma olmadan kaydetmek, orijinal piksel verilerini korur; bu, yüksek doğruluklu düzenleme hatları, arşivleme iş akışları veya sonraki işlem için piksel‑tam sonuçlar gerektiğinde kritiktir. Aşağıdaki adımlar, **aspose psd java** API'si ile bunu nasıl başaracağınızı tam olarak gösterir.

## Önkoşullar
Kodlamaya başlamadan önce kontrol etmemiz gereken birkaç önkoşul var. Endişelenmeyin; oldukça basit!

### Java Development Kit (JDK)
- Sisteminizde JDK 8 veya üzeri yüklü olduğundan emin olun. Yüklü değilse, [Oracle web sitesine](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) gidip en son sürümü indirin.

### Integrated Development Environment (IDE)
- IntelliJ IDEA, Eclipse veya NetBeans gibi iyi bir IDE, işinizi kolaylaştırır. Henüz kurmadıysanız bir tane kurun!

### Aspose.PSD for Java Library
- Aspose.PSD for Java kütüphanesini indirin. En son sürümleri [buradan](https://releases.aspose.com/psd/java/) alabilirsiniz. 

### Basic Knowledge of Java 
- Java programlama ve nesne‑yönelimli paradigma hakkında temel bir anlayışa sahip olmalısınız.

### A PSD File
- Test için bir örnek PSD dosyanız olsun. Photoshop'ta oluşturabilir veya çevrimiçi ücretsiz bir örnek indirebilirsiniz. 

Şimdi her şey hazır, koda dalalım!

## Paketleri İçe Aktarma
Başlamak için kodumuzda ihtiyaç duyacağımız paketleri içe aktarmamız gerekir. Aşağıda ihtiyaç duyacağınız import listesini bulabilirsiniz:
```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
Bu importlar, proje içinde gerekli sınıf ve metodları kullanmamıza olanak tanır, böylece PSD dosyalarını sorunsuz bir şekilde manipüle edebiliriz. Süreci yönetilebilir adımlara bölelim.

## Adım 1: Dosya Dizinini Ayarlama
İlk olarak, PSD dosyanızın bulunduğu yeri ve çıktıyı nereye kaydedeceğinizi belirtmeniz gerekir. Örnek kodumuzda, dizin yolunu tutacak bir değişken oluşturacağız.
```java
String dataDir = "Your Document Directory";
```
`"Your Document Directory"` ifadesini PSD dosyanızın (`layers.psd`) bulunduğu gerçek yol ile değiştirin. Böylece programınız dosyayı nereden bulacağını bilir.

## Adım 2: PSD Dosyasını Yükleme
Şimdi, `Image.load()` metodunu kullanarak PSD dosyasını yükleyelim ve `PsdImage` tipine dönüştürelim.
```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```
Bu satır, `Image` sınıfının `load` metodunu çağırarak PSD dosyanızı belleğe alır. `PsdImage` tipine cast ederek, Java'ya bu görüntünün PSD dosyası olduğunu ve PSD işlemleriyle ilgili özel işlevselliğe sahip olduğunu söylüyoruz.

## Adım 3: Kaydetme Seçeneklerini Yapılandırma
Sonraki adımda, dosyamızı kaydederken özellikle çıktının sıkıştırılmamış olmasını belirten seçenekleri ayarlamamız gerekir.
```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```
`PsdOptions` sınıfı, PSD dosyamızı kaydederken çeşitli ayarları belirtmemizi sağlar. `setCompressionMethod` değerini `CompressionMethod.Raw` olarak ayarlamak, kaydedilen dosyanın sıkıştırılmamış olmasını ve yüksek kaliteyi korumasını sağlar.

## Adım 4: Sıkıştırılmamış PSD Dosyasını Kaydetme
Şimdi yeni yapılandırılmış PSD görüntüsünü kaydetme zamanı.
```java
psdImage.save(dataDir + "uncompressed_out.psd", saveOptions);
```
Bu satır, `PsdImage` örneğimiz (`psdImage`) üzerinde kaydetme işlevini yürütür. Dosyayı belirtilen dizinde `uncompressed_out.psd` adıyla kaydeder ve önceki adımda tanımlanan seçenekleri uygular.

## Adım 5: Yeni Oluşturulan Görüntüyü Yeniden Açma
Kaydettikten sonra, her şeyin beklendiği gibi çalıştığını doğrulamak için çıktıyı yeniden yükleyelim.
```java
PsdImage img = (PsdImage) Image.load(dataDir + "uncompressed_out.psd");
```
`load` metodunu tekrar çağırarak, kaydedilen dosyaya karşılık gelen yeni bir `PsdImage` örneği oluşturabiliriz. Bu adım, kaydettikten sonra görüntüyü manipüle etmek veya göstermek istediğinizde kritiktir.

## Adım 6: Görüntüyü Çizme veya Manipüle Etme
Son olarak, yeni açılan görüntü üzerinde çizim yapabilir veya manipülasyon gerçekleştirebilirsiniz.
```java
Graphics graphics = new Graphics(img);
```
Burada bir `Graphics` nesnesi başlatıyoruz; bu nesne `img` üzerinde çeşitli grafiksel işlemler yapmamıza olanak tanır. Şekil çizebilir, metin ekleyebilir veya isterseniz katmanları bile değiştirebilirsiniz!

## Yaygın Sorunlar ve Çözümleri
- **FileNotFoundException** – `dataDir` yolunu iki kez kontrol edin ve PSD dosya adının tam olarak eşleştiğinden emin olun.  
- **UnsupportedCompressionException** – `CompressionMethod.Raw`ı destekleyen güncel bir Aspose.PSD sürümü kullandığınızdan emin olun.  
- **License Not Found** – Üretim kullanımında, değerlendirme filigranlarından kaçınmak için API metodlarını çağırmadan önce Aspose lisansınızı yükleyin.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, geliştiricilerin Photoshop PSD dosyalarıyla programatik olarak çalışmasını sağlayan bir Java kütüphanesidir.

**S: Aspose.PSD kullanarak bir PSD dosyasındaki katmanları manipüle edebilir miyim?**  
C: Evet! Aspose.PSD, katmanlara erişim ve manipülasyon imkanı sunar, böylece karmaşık işlemleri kolayca gerçekleştirebilirsiniz.

**S: Aspose.PSD ücretsiz mi?**  
C: Ücretsiz bir deneme sürümü mevcuttur, ancak kapsamlı kullanım ve gelişmiş özelliklere erişim için lisans satın almanız gerekebilir.

**S: Sorun yaşarsam nasıl destek alabilirim?**  
C: Yardım için [Aspose destek forumuna](https://forum.aspose.com/c/psd/34) ulaşabilirsiniz.

**S: Aspose.PSD, PSD dışındaki formatlarda kaydetmeyi destekliyor mu?**  
C: Evet, Aspose.PSD, gereksinimlerinize bağlı olarak PNG, JPEG ve daha fazlası gibi farklı formatlarda kaydetmeye olanak tanır.

**S: Bu kütüphane ile sıkıştırma olmadan bir PSD dışa aktarabilir miyim?**  
C: Kesinlikle – öğreticide gösterildiği gibi `PsdOptions` içinde `CompressionMethod.Raw` ayarlayın.

## Sonuç
Tebrikler! Java ve **aspose psd java** kütüphanesini kullanarak PSD formatında sıkıştırılmamış görüntü dosyalarıyla nasıl çalışılacağını öğrendiniz. Bu güçlü API, PSD dosyalarını yükleme, manipülasyon ve farklı formatlarda kaydetme gibi işlemleri kolaylaştırır. Şimdi denemeye başlayın! Farklı özellikleri keşfedin, grafiklerle oynayın ve neler yaratabileceğinizi görün.

Daha gelişmiş özellikler ve seçenekler için [belgelere](https://reference.aspose.com/psd/java/) göz atmayı unutmayın. Hemen başlamak isterseniz kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirebilir veya ücretsiz deneme sürümünü kullanabilirsiniz. Sorularınız olursa, topluluktan yardım almak için [destek forumuna](https://forum.aspose.com/c/psd/34) ziyaret etmeyi çekinmeyin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

---