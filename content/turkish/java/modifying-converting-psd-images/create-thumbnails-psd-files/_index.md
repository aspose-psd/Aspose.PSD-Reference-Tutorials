---
title: Java kullanarak PSD Dosyalarından Küçük Resimler Oluşturun
linktitle: Java kullanarak PSD Dosyalarından Küçük Resimler Oluşturun
second_title: Aspose.PSD Java API'si
description: Java ve Aspose.PSD kullanarak PSD dosyalarından zahmetsizce küçük resimler oluşturmayı öğrenin. Sorunsuz görüntü işleme için adım adım kılavuzumuzu izleyin.
type: docs
weight: 24
url: /tr/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---
## giriiş
Grafik tasarım dünyasında PSD (Photoshop Belgesi) dosyalarıyla çalışmak olağan bir durumdur. İster deneyimli bir geliştirici, ister grafik tasarımcı, ister yalnızca görüntü işlemeye dalmak isteyen biri olun, PSD dosyalarından küçük resimler oluşturmak size zaman kazandırabilir ve iş akışınızı kolaylaştırabilir. Bu eğitim Aspose.PSD for Java'yı kullanarak tüm süreç boyunca size rehberlik edecektir. Aspose.PSD yalnızca Photoshop dosyalarını yönetmek için güçlü bir kütüphane olmakla kalmaz, aynı zamanda eldeki görevi sezgisel ve yönetilebilir hale getirir. PSD dosyalarından verimli bir şekilde küçük resimler oluşturmayı öğrenmeye hazır mısınız?
## Önkoşullar
Küçük resim oluşturmanın en ince ayrıntılarına dalmadan önce, başlamak için neye ihtiyaç duyacağınıza değinelim.
### Java Geliştirme Ortamı
-  Java JDK: Bilgisayarınızda Java Development Kit'in (JDK) kurulu olduğundan emin olun. İndirebilirsin[Burada](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: IntelliJ IDEA, Eclipse veya NetBeans gibi bir Entegre Geliştirme Ortamı (IDE) kodlamayı kolaylaştıracaktır.
### Aspose.PSD Kütüphanesi
- Aspose.PSD kütüphanesini projenize dahil etmeniz gerekmektedir. Yapabilirsiniz[en son sürümü buradan indirin](https://releases.aspose.com/psd/java/).
### Temel Java Bilgisi
- Java'nın temellerine aşina olmak, örnek kodda daha etkili bir şekilde gezinmenize yardımcı olacaktır. Sınıflar, nesneler ve döngüler gibi kavramlar sıklıkla kullanılacaktır.
## Paketleri İçe Aktar
Aspose.PSD kütüphanesinden gerekli sınıfları içe aktararak başlayın. Bu adım çok önemlidir çünkü kodunuzdaki kitaplığın işlevlerinden yararlanmanıza olanak tanır.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Önkoşulları bir kenara bırakarak ana etkinliğe geçelim! PSD dosyalarından küçük resimler oluşturmak birkaç basit adımı içerir ve sizin için bunları ayrıntılı olarak anlatacağım.
## 1. Adım: Ortamınızı Kurun
Projenizi nasıl başlatacağınız ve küçük resim oluşturmaya nasıl hazırlanacağınız aşağıda açıklanmıştır.
1. Bir Java Projesi oluşturun:
   - IDE'nizi açın ve yeni bir Java projesi oluşturun.
   - Buna "PsdThumbnailGenerator" gibi bir ad verin.
2. Aspose.PSD Kitaplığını Dahil Et:
   -  Aspose.PSD JAR dosyasını projenizin derleme yoluna ekleyin. Maven kullanıyorsanız onu da ekleyin`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Adım 2: PSD Dosyasını Yükleyin
Daha sonra küçük resimler oluşturmak istediğimiz PSD dosyasını yüklememiz gerekiyor. 
1. Belge Dizininizi Belirtin:
   PSD dosyanızın bulunduğu dizini tanımlayın.
   ```java
   String dataDir = "Your Document Directory"; // Yolunuzla değiştirin
   ```
2. PSD Dosyasını Yükleyin:
    Şunu kullanın:`PsdImage` PSD dosyanızı yüklemek için class.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Burada,`sample.psd` PSD dosyanızın adıdır. Bunu dosyanızın adına göre ayarlayın.
## 3. Adım: PSD Kaynakları Üzerinde Yineleme Yapın
Artık PSD imajımızı yüklediğimize göre bir sonraki adım kaynaklarını incelemektir.
1. Kaynak Sayısını Alın:
   PSD dosyasındaki tüm kaynakları gözden geçireceğiz.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Kaynakları işleme
   }
   ```
   
2. Küçük Resim Kaynaklarını Tanımlayın:
   Döngünün içinde kaynağın küçük resim olup olmadığını kontrol edin.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Küçük resmi işle
   }
   ```
## 4. Adım: Küçük Resmi İşleyin
Bir küçük resim kaynağını belirledikten sonra onu uygun şekilde ele almamız gerekir.
1. Küçük Resim Formatını Alın ve Kontrol Edin:
   Kaynak gerçekten bir küçük resimse, onu alın ve biçimini kontrol edin.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Küçük resmi oluşturun ve kaydedin
   }
   ```
## Adım 5: Küçük Resmi Oluşturun ve Kaydedin
Sihrin gerçekleştiği yer burası! Küçük resim verisinden yeni bir resim oluşturup kaydedeceğiz.
1. Yeni Bir Resim Oluşturun:
   Yeni bir bitmap görüntüsü oluşturmak için küçük resim kaynağının genişliğini ve yüksekliğini kullanacağız.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Pikselleri Yeni Görüntüde Saklayın:
   Küçük resim verilerini yeni oluşturulan görüntüye aktarın.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Küçük Resim Görüntüsünü Kaydet:
   Son olarak, küçük resim görüntüsünü benzersiz bir adla belge dizininize kaydedin.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Çözüm
Java ve Aspose.PSD kullanarak PSD dosyalarından küçük resimler oluşturmak, bunu yönetilebilir adımlara ayırdığınızda basit bir iş olabilir. Bu eğitimle artık PSD dosyalarınızdan küçük resimleri kolaylıkla çıkarma gücüne sahip olacaksınız, bu da size iş akışınızı geliştirecek şık bir araç sunuyor. Peki seni durduran ne? Bazı PSD dosyalarına el atın ve deneyin!
## SSS'ler
### Aspose.PSD nedir?
Aspose.PSD, geliştiricilerin Photoshop dosyalarıyla çalışmasına olanak tanıyan, PSD dosyalarının programlı olarak işlenmesini ve yönetilmesini kolaylaştıran bir Java kitaplığıdır.
### Aspose.PSD'yi ücretsiz kullanabilir miyim?
Evet, Aspose, lisans satın almadan önce kütüphaneyi test etmek için kullanabileceğiniz ücretsiz bir deneme sunuyor.
### Küçük resimleri hangi formatlarda kaydedebilirim?
Bu örnekte küçük resimleri BMP formatında kaydettik ancak Aspose.PSD başka formatları da destekliyor.
### Aspose.PSD'yi kullanabilmek için Photoshop'un yüklü olması gerekiyor mu?
Hayır, Aspose.PSD Photoshop'tan bağımsız olarak çalışır.
### Aspose.PSD hakkında daha fazla bilgiyi nerede bulabilirim?
 Şunu kontrol edebilirsiniz:[Aspose.PSD belgeleri](https://reference.aspose.com/psd/java/) Daha fazla ayrıntı, öğreticiler ve kaynaklar için.