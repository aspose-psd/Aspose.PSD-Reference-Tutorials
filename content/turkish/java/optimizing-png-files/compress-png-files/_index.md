---
title: Aspose.PSD for Java kullanarak PNG Dosyalarını Sıkıştırın
linktitle: Aspose.PSD for Java kullanarak PNG Dosyalarını Sıkıştırın
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PNG dosyalarını verimli bir şekilde sıkıştırmayı öğrenin. Bu eğitim, en iyi dosya işlemeyi sağlayarak kod uygulaması boyunca size rehberlik eder.
type: docs
weight: 12
url: /tr/java/optimizing-png-files/compress-png-files/
---
## giriiş

Yazılım geliştirmede görüntülerin işlenmesi söz konusu olduğunda öne çıkan araçlardan biri Aspose.PSD for Java'dır. Bu güçlü kitaplık, geliştiricilerin Photoshop dosyalarını (PSD) sorunsuz bir şekilde işlemesine olanak tanır. İster bir web sitesi için görselleri optimize ediyor, ister yükleme sürelerini artırıyor, ister grafiklerinizden en iyi kaliteyi elde ediyor olun, bu kütüphaneyi etkili bir şekilde nasıl kullanacağınızı anlamak oyunun kurallarını değiştirebilir. Bu eğitimde, Aspose.PSD for Java kullanarak PNG dosyalarını sıkıştırmak gibi pratik bir örneğe bakacağız. Hadi başlayalım!

## Önkoşullar

Kodlama kısmına geçmeden önce her şeyin hazır olduğundan emin olalım. İşte ihtiyacınız olan şeylerin hızlı bir kontrol listesi:

1.  Java JDK: Java Geliştirme Kitinin (JDK) kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2. Aspose.PSD for Java Library: Photoshop dosya işlemlerini gerçekleştirmek için Aspose.PSD kütüphanesine ihtiyacınız olacak. En son sürümü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/psd/java/).

3. IDE/Kod Düzenleyici: IntelliJ IDEA, Eclipse gibi basit bir kod düzenleyici veya hatta Visual Studio Code gibi bir metin düzenleyici mükemmel çalışacaktır.

4. Temel Java Bilgisi: Java programlama ve istisnaları yönetme konusunda bilgi sahibi olmak, bu eğitimin takip edilmesini çok daha kolay hale getirecektir.

5. Örnek PSD Dosyası: Kodumuzu test etmek için bir PSD dosyasına ihtiyacınız olacak. Belirlediğiniz belge dizininde kullanışlı bir tane olduğundan emin olun.

Artık önkoşulları ele aldığımıza göre işin eğlenceli kısmına geçelim: PNG dosyalarını sıkıştırmak için kod yazmaya!

## Paketleri İçe Aktar

Sıkıştırma kodumuzu yazmaya başlamadan önce gerekli paketleri içe aktarmamız gerekiyor. Aşağıda ihtiyacınız olacak ithalatların kısa bir kontrol listesi bulunmaktadır:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Bu içe aktarmalar, PSD görüntülerini değiştirmemize ve PNG seçeneklerini kolayca yönetmemize olanak tanır.

Örneği net ve yönetilebilir adımlara ayıralım, böylece kaybolmadan ilerleyebilirsiniz. 

## 1. Adım: Projenizi Kurun

Öncelikle seçtiğiniz IDE'de yeni bir proje oluşturmak isteyeceksiniz. Henüz bir tane oluşturmadıysanız endişelenmeyin; bunu nasıl yapacağınız aşağıda açıklanmıştır:

1. IDE'nizi açın ve yeni bir Java projesi oluşturun.
2.  Buna alakalı bir ad verin, örneğin`PsdImageCompressor`.
3. Aspose.PSD JAR dosyasını projenizin derleme yoluna ekleyin. Bu adım, projenizin Aspose.PSD kütüphanesini tanımasına olanak tanıdığı için çok önemlidir.

## 2. Adım: Belge Dizininizi Tanımlayın

Daha sonra PSD dosyanızın bulunduğu yolu ayarlamak isteyeceksiniz. Bu adım, programınıza dosyaları nerede arayacağını söylemekle ilgilidir. Kodunuzda veri dizinini şu şekilde tanımlayabilirsiniz:

```java
String dataDir = "Your Document Directory"; // Gerçek yolla değiştir
```

 Sadece değiştirdiğinizden emin olun`"Your Document Directory"` makinenizde PSD dosyalarınızı kaydettiğiniz gerçek yolla.

## 3. Adım: PSD Görüntüsünü Yükleyin

Şimdi PSD görselinizi uygulamaya yükleyelim. Bu adım, bir kitabı okumadan önce açmaya benzer:

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

 Burada,`sample.psd`dosyanızın adıdır. Belirttiğiniz dizinde bulunduğundan emin olun! Dosya orada değilse, bir hatayla karşılaşırsınız.

## Adım 4: Sıkıştırma Seviyeleri Arasında Döngü

Görüntüyü yükledikten sonra sıkıştırmanın zamanı geldi. Sıkıştırma düzeyleri genellikle 0 (sıkıştırma yok) ile 9 (maksimum sıkıştırma) arasında değişir. Bir döngü kullanarak PSD dosyasının birden fazla PNG sürümünün kaydedilmesini otomatikleştirebiliriz:

```java
for (int i = 0; i <= 9; i++) {
    // PngOptions'ın yeni bir örneğini oluşturun
    PngOptions options = new PngOptions();
    options.setCompressionLevel(i); // Sıkıştırma düzeyini ayarlayın
```

Bu döngü, tüm sıkıştırma seviyelerini sorunsuz bir şekilde test etmemizi sağlar. 

## Adım 5: Sıkıştırılmış PNG Dosyalarını Kaydedin

Şimdi sıkıştırılmış görüntüleri dizininize kaydetmenin zamanı geldi. Bir dosyayı her kaydettiğimizde, sıkıştırma düzeyini dosya adına ekleyeceğiz. Bu şekilde farklı sıkıştırma düzeylerini kolayca ayırt edebilirsiniz:

```java
    psdImage.save(dataDir + i + "_out.png", options);
}
```

## Çözüm

Tebrikler! Aspose.PSD for Java kullanarak PNG dosyalarını PSD dosyasından nasıl sıkıştıracağınızı başarıyla öğrendiniz. Bu güçlü araç, yalnızca tasarımları verimli bir şekilde yönetmenize yardımcı olmakla kalmaz, aynı zamanda görsellerinizin herhangi bir platform veya uygulama için optimize edilmesini de sağlar. İster projenizin performansını artırmak isteyen bir geliştirici olun, ister yükleme sürelerinden ödün vermeden kaliteyi korumak isteyen bir tasarımcı olun, bu yaklaşım kesinlikle yardımcı olacaktır. O halde kollarınızı sıvayın, kodlamaya başlayın ve farklı sıkıştırma seviyelerini deneyin! 

## SSS'ler

### Java için Aspose.PSD nedir?  
Aspose.PSD for Java, geliştiricilerin Photoshop dosyalarını programlı olarak değiştirmesine olanak tanıyan bir kitaplıktır.

### PNG'nin yanı sıra diğer görüntü formatlarını da sıkıştırabilir miyim?  
Bu eğitim PNG'ye odaklanmaktadır ancak Aspose.PSD, PSD, TIFF ve JPEG dahil olmak üzere çeşitli formatları destekler.

### Aspose.PSD'yi kullanmak için lisansa ihtiyacım var mı?  
 Kütüphaneyi ücretsiz deneme sürümüyle kullanabilirsiniz ancak uzun süreli kullanım için tam lisans gereklidir. Bir tane alabilirsiniz[Burada](https://purchase.aspose.com/buy).

### Kodu çalıştırırken bir hatayla karşılaşırsam ne olur?  
Dosya yollarınızı bir kez daha kontrol edin, gerekli içe aktarma işlemlerinin dahil edildiğinden emin olun ve kitaplığın doğru sürümüne sahip olduğunuzu doğrulayın.

### Aspose.PSD for Java hakkında daha fazla belgeyi nerede bulabilirim?  
 Ayrıntılı belgeleri ve örnekleri şu adreste bulabilirsiniz:[Aspose.PSD referansı](https://reference.aspose.com/psd/java/).