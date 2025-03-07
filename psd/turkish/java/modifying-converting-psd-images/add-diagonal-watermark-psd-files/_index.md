---
title: Java ile PSD Dosyalarına Çapraz Filigran Ekleme
linktitle: Java ile PSD Dosyalarına Çapraz Filigran Ekleme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java kullanarak PSD dosyalarına nasıl kolayca çapraz filigran ekleyeceğinizi öğrenin. Resimlerinizi güvenle geliştirmek için adım adım kılavuz.
weight: 12
url: /tr/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile PSD Dosyalarına Çapraz Filigran Ekleme

## giriiş
Günümüzün dijital dünyasında çarpıcı bir görsele sahip olmak büyük fark yaratabilir. İster işinizi korumak isteyen bir tasarımcı olun, ister görsellere marka eklemek isteyen bir pazarlamacı olun, filigran uygulamak çok önemlidir. Bu derste, PSD dosyalarını işlemek için güçlü bir kütüphane olan Aspose.PSD'nin yardımıyla Java kullanarak PSD dosyalarına çapraz filigranın nasıl ekleneceğini keşfedeceğiz.
## Önkoşullar
İlginç kodlama kısmına geçmeden önce birkaç şeyin ayarlandığından emin olmanız gerekir:
### 1. Java Geliştirme Ortamı
 Makinenizde Java'nın kurulu olduğundan emin olun. En son sürümü adresinden indirebilirsiniz.[Java web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
### 2. Aspose.PSD Kütüphanesi
 PSD dosyalarıyla çalışmak için Aspose.PSD kütüphanesine ihtiyacınız olacak. adresinden indirebilirsiniz.[İndirilenler sayfasını Aspose](https://releases.aspose.com/psd/java/)Proje yapınıza bağlı olarak Maven veya başka bir bağımlılık yönetimi aracı kullanıyor olabilirsiniz; bu nedenle, bunu ihtiyaçlarınıza göre dahil etmekten çekinmeyin.
### 3. Java'nın Temel Anlayışı
Java'yı sağlam bir şekilde kavramak, bu öğreticiyi sorunsuz bir şekilde takip etmenize yardımcı olacaktır. Java'da sınıflar, nesneler ve temel dosya işleme konusunda rahat olduğunuzdan emin olun.
### 4.IDE Kurulumu
Kodlamak için IntelliJ IDEA, Eclipse veya NetBeans gibi herhangi bir Entegre Geliştirme Ortamını (IDE) kullanın. Kodlamayı çok daha kolaylaştırıyor, öyle değil mi?
## Paketleri İçe Aktar
PSD dosyalarını yönetmek için Aspose.PSD'den belirli paketleri içe aktarmanız gerekir. Java dosyanızın en üstüne eklemeniz gereken paketler şunlardır:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```
Artık önkoşullarımızı sıraladığımıza ve gerekli paketleri içe aktardığımıza göre, PSD dosyasına çapraz filigran ekleme adımlarını izleyelim.
## 1. Adım: Dizininizi Kurun
```java
String dataDir = "Your Document Directory";
```
Öncelikle PSD dosyalarınızın bulunduğu dizini belirtmeniz gerekecek. Bu dizin görüntünün yüklenmesi için başlangıç noktası olacaktır. Öyleyse değiştir`"Your Document Directory"` PSD dosyanızın bulunduğu gerçek yolla.
## Adım 2: PSD Dosyasını Yükleyin
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
 Şimdi çalışmak istediğiniz PSD dosyasını yükleyeceğiz.`Image.load` yöntem dosyayı okur ve onu bir`PsdImage` nesne. Bu durumda PSD dosyanızın tam adını verdiğinizden emin olun.`"layers.psd"`.
## Adım 3: Grafik Nesnesi Oluşturun
```java
Graphics graphics = new Graphics(psdImage);
```
 Bu adımda bir oluşturuyoruz.`Graphics` Yüklenen görüntü üzerinde çizim işlemleri yapmamızı sağlayan nesne. Bunu, filigranımızı boyayabileceğimiz bir tuval hazırlamak gibi düşünün.
## Adım 4: Filigran için Yazı Tipi Oluşturun
```java
Font font = new Font("Arial", 20.0f);
```
Burada filigran metnimiz için yazı tipi stilini ve boyutunu tanımlıyoruz. Bu durumda, 20 boyutunda Arial'ı seçtik. Sisteminizde yüklü olan herhangi bir yazı tipini seçmekten çekinmeyin; işleri biraz renklendirin!
## Adım 5: Filigran için Fırça Oluşturun
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 Daha sonra bir tane oluşturuyoruz`SolidBrush` filigranımızı renklendirecek nesne.`Color.fromArgb`yöntem dört parametre alır: alfa, kırmızı, yeşil ve mavi. Alfa değeri şeffaflığı kontrol eder (0 tamamen şeffaftır ve 255 tamamen opaktır). Güzel bir yarı şeffaf etki için bunu 50'ye ayarladık.
## Adım 6: Dönüşüm Matrisini Ayarlayın
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
 Sihrin gerçekleştiği yer burası! Filigranı döndürmek için bir dönüşüm matrisi oluşturuyoruz.`rotateAt` işlevi iki parametre alır: açı (çapraz görünüm için 45 derece) ve etrafında döndürülecek nokta (bu bizim durumumuzda görüntünün merkezidir).
## Adım 7: Dize Hizalamasını Tanımlayın
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
 Filigranımızın ortalandığından emin olmamız gerekiyor.`StringFormat` class, metni görüntünün merkezine mükemmel bir şekilde hizalayarak bize bu konuda yardımcı olur. Sonuçta kim dağınık yerleşimlerden hoşlanır?
## Adım 8: Filigranı Çizin
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
 Şimdi filigranı gerçekten çizmenin zamanı geldi! kullanarak`drawString`yönteminde filigranımızın içeriğini (metni özelleştirmekten çekinmeyin), yazı tipini, fırçayı, çizilmesini istediğimiz alanı ve hizalama ayarını belirtiriz. Filigranınız dikdörtgende belirlediğimiz parametreler kullanılarak uygulanacaktır!
## Adım 9: Görüntüyü Kaydedin
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
 Son olarak değiştirdiğimiz görselimizi kaydediyoruz. Burada onu PNG dosyası olarak dışa aktarıyoruz. Çıktı dosyanıza, mevcut dosyaların üzerine yazılmaması için benzersiz bir ad verdiğinizden emin olun.`PngOptions` class görüntü formatını belirtmeye yardımcı olur.
## Çözüm
Ve böylece, Java'yı kullanarak PSD dosyanıza başarıyla çapraz bir filigran eklediniz! Bu basit bir süreçtir ancak görsellerinizin profesyonelliğini önemli ölçüde artırabilir. İster sanat eserinizi koruyor olun, ister markanızı tanıtıyor olun, filigran basit ama etkili bir çözümdür.

## SSS'ler
### Aspose.PSD nedir?
Aspose.PSD, Adobe Photoshop gerektirmeden PSD dosyalarıyla çalışmak ve bunları değiştirmek için kullanılan bir Java kütüphanesidir.
### Filigranlama için başka yazı tipleri kullanabilir miyim?
Evet, filigran eklemek için sisteminizde yüklü olan herhangi bir yazı tipini seçebilirsiniz.
### Filigranın şeffaflığını özelleştirmenin bir yolu var mı?
Kesinlikle! Şeffaflığı değiştirmek için SolidBrush'taki alfa değerini ayarlayabilirsiniz.
### Birden fazla filigran ekleyebilir miyim?
 Evet, arayabilirsiniz`drawString` Daha fazla filigran eklemek için yöntemi farklı parametrelerle birden çok kez kullanın.
### Aspose.PSD hakkında daha fazla bilgiyi nerede bulabilirim?
 Belgeleri kontrol edebilirsiniz[Burada](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
