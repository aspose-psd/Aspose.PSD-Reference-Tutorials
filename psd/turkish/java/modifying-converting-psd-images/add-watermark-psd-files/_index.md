---
title: Aspose.PSD for Java ile PSD Dosyalarına Filigran Ekleme
linktitle: Aspose.PSD for Java ile PSD Dosyalarına Filigran Ekleme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PSD dosyalarınıza zahmetsizce nasıl filigran ekleyeceğinizi öğrenin. Basit, adım adım kılavuzla görsellerinizi koruyun.
weight: 18
url: /tr/java/modifying-converting-psd-images/add-watermark-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile PSD Dosyalarına Filigran Ekleme

## giriiş
Filigranlar, görsellerinizi korumanın ve sahipliğinizi belirtmenin ince ama etkili bir yoludur. İster portfolyonuzu sergileyen bir fotoğrafçı olun ister en son çalışmanızı sunan bir tasarımcı olun, filigran eklemek marka kimliğinizi korumak açısından çok önemli olabilir. Bu eğitimde Aspose.PSD for Java'yı kullanarak PSD dosyalarınıza nasıl zahmetsizce filigran ekleyeceğinizi açıklayacağız. O halde bir fincan kahve alın, rahatlayın ve başlayalım!
## Önkoşullar
Koda dalmadan önce, filigranı PSD dosyalarınıza başarılı bir şekilde uygulamak için gerekli araç ve paketlere sahip olduğunuzdan emin olmanız önemlidir. İşte hazırlamanız gerekenler:
1. Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun. PATH değişkenini yapılandırmak da gerekli olabilir.
2. Aspose.PSD for Java Library: Bu, filigran uygulamamızın kalbidir. Kütüphaneyi şuradan indirmeniz gerekiyor:[Web sitesi](https://releases.aspose.com/psd/java/).
3. IDE: Seçtiğiniz herhangi bir Java IDE işinizi görecektir. İster Eclipse, ister IntelliJ IDEA, hatta basit bir metin düzenleyici olsun, seçim yapmakta özgürsünüz.
4.  PSD Dosyası: Bir PSD dosyasını elinizin altında bulundurun. Bir tane oluşturabilir veya çevrimiçi bir örnek bulabilirsiniz. Biz buna şu şekilde değineceğiz:`layers.psd`.
5. Temel Java Bilgisi: Java'nın temellerini iyi anlamak, takip etmenize çok yardımcı olacaktır.
## Paketleri İçe Aktar
Artık her şeyi ayarladığınıza göre gerekli paketleri içe aktaralım. Java'daki içe aktarmalar, çeşitli kitaplıklardan sınıfları ve işlevleri getirmenize olanak tanıyarak kodunuzu daha verimli hale getirir. İhtiyacınız olan şey aşağıdadır:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```
## 1. Adım: Dizininizi Kurun
Öncelikle PSD dosyanızın bulunduğu yerin yolunu ayarlamamız gerekiyor. Bu çok önemlidir çünkü Java'nın dosyalarınızı nerede bulacağını bilmesi gerekir. 
```java
String dataDir = "Your Document Directory";
```
 Yer değiştirmek`Your Document Directory` PSD dosyanızın bulunduğu gerçek dizininizle.
## Adım 2: PSD Dosyasını Yükleyin
 Daha sonra, PSD dosyasını yükleyip bir`PsdImage`Bu adım, dosyayı değiştirebileceğimiz bir formata dönüştürür.
```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```
 Bu satırın yaptığı, mevcut PSD dosyanızı alıp belleğe bir dosya olarak yüklemektir.`PsdImage`. Bunu, içine yazmaya başlayabileceğiniz bir kitabı açmak gibi düşünün.
## Adım 3: Grafik Nesnesi Oluşturun
 Artık PSD dosyamız yüklendiğinde, bir oluşturmamız gerekiyor.`Graphics` nesne. Bu, tuvalinize renk katmak için bir boya fırçası almak gibi çizim işlemlerini gerçekleştirmemize olanak tanır.
```java
Graphics graphics = new Graphics(psdImage);
```
## Adım 4: Filigranınızın Yazı Tipini Tanımlayın
Şimdi filigranınızın nasıl görüneceğini seçme zamanı. Arial'ı 20 yazı tipi boyutunda kullanacağız. Burası tarzınızı sergileyebileceğiniz yerdir!
```java
Font font = new Font("Arial", 20.0f);
```
## Adım 5: Filigranlama için Katı Bir Fırça Oluşturun
Filigranınıza rengini ve opaklığını veren sağlam bir fırçadır. Dikkat çekici olmasını ancak çok fazla olmamasını istiyoruz, bu nedenle kısmen şeffaf bir görünüm için alfa değerini 0'a yakın bir değere ayarlayalım.
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 Burada,`Color.fromArgb(50, 128, 128, 128)` %50 opaklığa sahip gri bir renk oluşturur. Sanki canlı bir gökyüzünü yumuşakça gölgeleyen bir bulut gibi.
## Adım 6: Filigranınız için Dize Hizalamasını Ayarlayın
Filigranınızın görselin tam ortasında görünmesini sağlamak için dize hizalama seçeneklerini ayarlayacağız. Bu adım tamamen hassasiyetle ilgilidir!
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```
## Adım 7: Filigranı Çizin
Şimdi heyecan verici kısma geliyoruz! Grafik bağlamımız ayarlandığında, filigranı görüntünün üzerine çizmenin zamanı geldi.
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```
 İşte, değiştir`"Some watermark text"` İstediğiniz filigran metniyle. Bu adım bir başyapıta imzanızı atmak gibidir!
## Adım 8: Görüntüyü PNG Formatına Aktarın
Artık resmimiz hazır olduğuna göre, onu yeni bir dosya biçiminde (bu durumda PNG) kaydetmemiz gerekiyor. 
```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```
Bu satırı uygulayarak çalışmanızı yeni bir formatta etkili bir şekilde ölümsüzleştirir ve filigranı dünyanın görmesi için korursunuz!
## Çözüm
Ve işte karşınızda! Aspose.PSD for Java'yı kullanarak PSD dosyanıza başarıyla filigran eklediniz. Bu süreç yalnızca içeriğinizi güvence altına almakla kalmaz, aynı zamanda markanızın görünürlüğünü de artırır. Unutmayın, attığınız adımlar yalnızca bir başlangıç noktasıdır. Yaratıcı olmaktan çekinmeyin; farklı yazı tipleri, stiller ve renklerle denemeler yapın! Çalışmanızı korumaya ve markanızı gururla sergilemeye devam edin. 
## SSS'ler
### Filigran metnini özelleştirebilir miyim?
 Kesinlikle! Sadece içindeki metni değiştirin`drawString` İstediğiniz filigranı içeren yöntemi kullanın.
### Farklı bir yazı tipi istersem ne olur?
 Yazı tipini farklı bir yazı tipi seçerek kolayca değiştirebilirsiniz.`Font` örnekleme.
### Opaklığı ayarlamanın bir yolu var mı?
 Evet! Alfa değerini değiştirin`Color.fromArgb()` filigranın opaklığını değiştirmek için.
### Diğer resim formatlarını kullanabilir miyim?
 Evet, JPEG veya BMP gibi çeşitli formatlarda kaydedebilirsiniz. Sadece değiştir`PngOptions()` İstenilen seçeneklerle.
### Daha fazla yardımı nerede bulabilirim?
 Detaylı sorularınız için adresini ziyaret edebilirsiniz.[forumlar](https://forum.aspose.com/c/psd/34) veya kontrol edin[dokümantasyon](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
