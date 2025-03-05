---
title: Java'da Grafik Yolunu Kullanarak Çizim Yapma
linktitle: Java'da Grafik Yolunu Kullanarak Çizim Yapma
second_title: Aspose.PSD Java API'si
description: Aspose.PSD'nin Graphics Path sınıfını kullanarak Java'da karmaşık grafikler oluşturmayı öğrenin. Bu eğitim, çarpıcı görüntü oluşturmanın her adımında size rehberlik eder.
type: docs
weight: 19
url: /tr/java/java-graphics-drawing/drawing-using-graphics-path/
---
## giriiş
Görüntüleri programlı olarak oluşturmak ve değiştirmek, özellikle Aspose.PSD gibi kütüphaneleri kullanırken Java geliştiricileri için heyecan verici bir görev olabilir. Bu derste Aspose.PSD ile Java'daki Graphics Path sınıfını kullanarak karmaşık grafikler çizme sürecine dalacağız.
## Önkoşullar
Kodlama kısmına geçmeden önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
1.  Java Geliştirme Kiti (JDK): Makinenizde yüklü olan JDK'nın kararlı bir sürümü. Şuradan indirebilirsiniz[Oracle'ın sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Library: Aspose.PSD for Java kütüphanesini şu adresten indirin:[Burada](https://releases.aspose.com/psd/java/). İndirdikten sonra JAR dosyasını projenizin sınıf yoluna ekleyin.
3. Entegre Geliştirme Ortamı (IDE): Eclipse, IntelliJ IDEA veya başka herhangi bir şey olsun, Java kodunu yazmak ve çalıştırmak için bir IDE'ye ihtiyacınız vardır.
Bu önkoşullar yerine getirildikten sonra, Graphics Path sınıfını kullanarak görsel olarak ilgi çekici görsellerin nasıl oluşturulacağını keşfedelim.
## Paketleri İçe Aktar
Başlamak için gerekli paketleri içe aktarmanız gerekir:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```
Bu içe aktarmalar, Aspose.PSD kullanarak görseller oluşturmak ve işlemek için gereken temel işlevlere erişim sağlar.
## 1. Adım: Görüntüyü ve Grafiği Başlatın
Başlamak için yeni bir görüntü oluşturalım ve bir grafik nesnesini başlatalım:
```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```
Burada 500x500 piksellik bir görüntü ve çizim için bir grafik nesnesi oluşturuyoruz.
## Adım 2: Grafik Yolu Oluşturun ve Yapılandırın
 Daha sonra bir tane oluşturuyoruz`GraphicsPath` Çizim yolunu tanımlamak için nesne:
```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```
Bu adımda şekilimize bir daire, bir dikdörtgen ve bir metin etiketi ekliyoruz ve ardından bu şekli grafik yolumuza ekliyoruz.
## Adım 3: Yolu Çizin ve Doldurun
Artık yolumuzu tanımladığımıza göre onu çizip doldurabiliriz:
```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```
Bu adımda mavi kalem kullanarak yolu çiziyoruz ve tarama fırçası kullanarak dikey tarama deseni ile dolduruyoruz.
## Adım 4: Görüntüyü Kaydedin
Son olarak görüntüyü bir dosyaya kaydedin:
```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```
Bu son adımla grafik yolunu kullanarak görüntü oluşturma işleminiz tamamlanır.
## Çözüm
Aspose.PSD ile Graphics Path sınıfını kullanarak karmaşık görüntüler oluşturmak hem güçlü hem de ilgi çekicidir. Bu kılavuzu takip ederek Java uygulamanızın grafik tasarım yeteneklerini genişletebilirsiniz.
## SSS'ler
### Aspose.PSD nedir?
Aspose.PSD, geliştiricilerin Photoshop dosyalarıyla çalışmasına ve görüntü katmanlarını programlı olarak değiştirmesine olanak tanıyan bir kitaplıktır.
### Aspose.PSD'yi PSD dışındaki formatlar için kullanabilir miyim?
Bu kılavuzdan itibaren Aspose.PSD, özellikle PSD dosyalarıyla ilgilenmektedir ancak farklı görüntü formatlarını işlemek için uzantılar sunmaktadır.
### Aspose.PSD'nin deneme sürümü mevcut mu?
 Evet, Aspose.PSD'nin ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
### Aspose.PSD'yi nasıl satın alabilirim?
 Aspose.PSD'yi şu adresten satın alabilirsiniz:[Burada](https://purchase.aspose.com/buy).
### Aspose.PSD için nereden destek alabilirim?
Bu konuda destek ve tartışmalar arayabilirsiniz.[Aspose'un forumu](https://forum.aspose.com/c/psd/34).