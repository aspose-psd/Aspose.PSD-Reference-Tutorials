---
title: Java'da Dikdörtgen Çizimi
linktitle: Java'da Dikdörtgen Çizimi
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak görüntülere dikdörtgenler çizmeyi öğrenin. Bu eğitim, Java geliştiricilerine adım adım rehberlik eder. Görüntü işleme görevleri için mükemmeldir.
type: docs
weight: 17
url: /tr/java/java-graphics-drawing/drawing-rectangles/
---
## giriiş
Java geliştirme dünyasında, görüntüleri programlı olarak değiştirmek ve oluşturmak, çeşitli uygulamalarda ortak bir gereksinimdir. Sıklıkla karşılaşılan bu tür görevlerden biri, görüntülerin üzerine dikdörtgen gibi şekiller çizmek. Aspose.PSD for Java, bunu verimli bir şekilde gerçekleştirmek için güçlü bir araç ve işlevsellik seti sağlar. Bu eğitim, Aspose.PSD for Java kullanarak bir görüntü üzerinde dikdörtgenler çizme sürecinde size adım adım rehberlik edecektir.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulları oluşturduğunuzdan emin olun:
### Java Geliştirme Ortamı
Sisteminizde bir Java Development Kit'in (JDK) (tercihen JDK 8 veya üzeri) kurulu olduğundan emin olun.
### Java için Aspose.PSD
 Aspose.PSD for Java kütüphanesine sahip olmanız gerekir. adresinden indirebilirsiniz.[Java indirme sayfası için Aspose.PSD](https://releases.aspose.com/psd/java/) ve belgelerinde verilen kurulum talimatlarını izleyin.
## Paketleri İçe Aktar
Başlamak için gerekli Aspose.PSD for Java paketlerini Java dosyanıza aktarın:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Bu içe aktarmalar, görüntülere dikdörtgen çizmek için gereken sınıflara ve yöntemlere erişmenizi sağlayacaktır.
## 1. Adım: Yeni Bir Görüntü Oluşturun
 İlk önce yeni bir örnek oluşturun`PsdImage` Belirli bir genişlik ve yüksekliğe sahip sınıf.
```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Bir BmpOptions örneği oluşturun ve özelliklerini ayarlayın
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Belirtilen boyutlara sahip bir PsdImage örneği oluşturun
Image image = new PsdImage(100, 100);
```
 Bu adımda,`PsdImage` her biri 100 piksel genişlik ve yükseklikte başlatılır.
## Adım 2: Grafik Nesnesini Başlatın
 Daha sonra, bir başlatma işlemi gerçekleştirin`Graphics` kullanarak nesne`image` önceki adımda oluşturuldu.
```java
// Grafik nesnesini başlat
Graphics graphic = new Graphics(image);
```
 Bu`Graphics`nesne görüntü üzerinde çizim işlemlerini gerçekleştirmek için kullanılacaktır.
## 3. Adım: Grafik Yüzeyini Temizleyin
Belirli bir renk kullanarak görüntünün grafik yüzeyini temizleyin.
```java
// Sarı renkli net grafik yüzeyi
graphic.clear(Color.YELLOW);
```
Bu, görüntünün arka planını sarıya ayarlar.
## Adım 4: Dikdörtgenler Çizin
Şimdi görüntünün üzerine farklı renk ve boyutlarda dikdörtgenler çizin.
```java
// Kırmızı bir dikdörtgen çizin
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Mavi bir dikdörtgen çizin
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Bu komutlar, görüntü üzerinde belirtilen renklere (kırmızı ve mavi) ve konumlara sahip dikdörtgenler çizer.
## Adım 5: Görüntüyü Dışa Aktarın
Son olarak, değiştirilen görüntüyü bir BMP dosya formatında kaydedin.
```java
// Görüntüyü BMP dosya formatına aktar
image.save(outpath, saveOptions);
```
 Bu, çizilen dikdörtgenlere sahip görüntüyü aşağıdakiler tarafından belirtilen bir BMP dosyasına kaydeder:`outpath`.

## Çözüm
Aspose.PSD for Java kullanarak Java'daki görüntüler üzerinde programlı olarak dikdörtgenler çizmek, doğru araçlar ve kütüphaneler sayesinde çok kolaydır. Bu öğreticiyi takip ederek bir görüntüyü nasıl başlatacağınızı, grafik nesnelerini nasıl değiştireceğinizi, şekiller çizeceğinizi ve değiştirilen görüntüyü bir dosyaya nasıl kaydedeceğinizi öğrendiniz. Farklı şekiller, renkler ve boyutlarla denemeler yapmak, Java'da görüntü işleme konusundaki anlayışınızı daha da geliştirecektir.
## SSS'ler
### Aspose.PSD for Java dikdörtgenlerin yanı sıra diğer şekilleri de işleyebilir mi?
Aspose.PSD for Java, dikdörtgenlerin yanı sıra elips, çizgi ve çokgen gibi çeşitli şekillerin çizilmesini de destekler.
### Dikdörtgen kenarlığının kalınlığını nasıl değiştirebilirim?
 Dikdörtgen kenarlığının kalınlığını ayarlayarak ayarlayabilirsiniz.`Pen` kalınlık özelliği.
### Aspose.PSD for Java, yüksek performanslı görüntü işleme görevlerine uygun mu?
Evet, Aspose.PSD for Java, hem basit hem de karmaşık işlemlere yönelik kapsamlı özelliklerle yüksek performanslı görüntü işleme için tasarlanmıştır.
### Aspose.PSD for Java için daha fazla örneği ve öğreticiyi nerede bulabilirim?
 Daha fazla örneği ve ayrıntılı belgeleri inceleyebilirsiniz.[Java belgeleri için Aspose.PSD](https://reference.aspose.com/psd/java/).
### Aspose.PSD for Java, BMP'nin yanı sıra diğer görüntü formatlarını da destekliyor mu?
Evet, Aspose.PSD for Java PNG, JPEG, TIFF ve GIF dahil çok çeşitli görüntü formatlarını destekler.