---
title: Java ile PSD Dosyalarında Vmsk Kaynağını Destekleyin
linktitle: Java ile PSD Dosyalarında Vmsk Kaynağını Destekleyin
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki Vmsk kaynaklarını zahmetsizce yönetin. Hem geliştiriciler hem de tasarımcılar için ideal, kapsamlı, adım adım eğitim.
weight: 23
url: /tr/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile PSD Dosyalarında Vmsk Kaynağını Destekleyin

## giriiş
PSD (Photoshop Belgesi) dosyalarıyla çalışmak söz konusu olduğunda, özellikle Vmsk (Vektör Maskesi) kaynağı gibi özel özellikleri entegre ederken kaynakları yönetmek çok önemlidir. Vmsk kaynakları, karmaşık vektör şekilleri ekleyerek tasarımcılara güç verebilir ve onların çarpıcı grafikleri zahmetsizce oluşturmasına olanak tanır. Bu kılavuzda, Aspose.PSD for Java kullanarak PSD dosyalarındaki Vmsk kaynaklarını nasıl destekleyeceğinizi göstermek için uygulamalı bir yaklaşım izleyeceğiz. İster uygulamanızı geliştirmek isteyen bir geliştirici, ister otomasyon arayan bir tasarımcı olun, bu eğitim size süreç boyunca adım adım yol göstererek takip etmeyi ve uygulamayı kolaylaştıracaktır.
## Önkoşullar
Vmsk kaynaklarını kullanmanın ilginç ayrıntılarına dalmadan önce, kusursuz bir deneyim için her şeyin hazır olduğundan emin olalım.
### İhtiyacınız Olan Şey
-  Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun. Değilse, adresinden indirebilirsiniz.[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: Bu, PSD dosyalarını yönetmek için güçlü bir kütüphanedir. adresinden indirebilirsiniz.[Yayın sayfasını aspose edin](https://releases.aspose.com/psd/java/) . Satın almadan önce denemek isteyenler için şu adresten de başlayabilirsiniz:[ücretsiz deneme](https://releases.aspose.com/).
- Bir IDE: Java için herhangi bir IDE (IntelliJ IDEA, Eclipse vb. gibi) bu proje için çalışacaktır.
### Çalışma Alanınızı Ayarlama
1. Yeni Bir Java Projesi Oluşturun: Tercih ettiğiniz IDE'yi başlatın ve yeni bir Java projesi oluşturun. Burası kodla çalışmak için oyun alanınızdır.
2. Aspose Kütüphanesini Ekleyin: Aspose kütüphanesini indirdikten sonra jar dosyasını projenizin kütüphanelerine ekleyin. Bu adım çok önemlidir çünkü Aspose.PSD'nin tüm bu harika özelliklerinden yararlanmamıza olanak tanır.
Bu önkoşullar yerine getirildiğinde, Vmsk kaynaklarıyla PSD dosyalarını oluşturmaya, değiştirmeye ve yönetmeye hazırsınız. Haydi hemen programlamaya geçelim!
## Paketleri İçe Aktar
PSD dosyaları üzerinde çalışmaya başlamadan önce gerekli paketleri içe aktarmamız gerekiyor. Bu, kodumuzun omurgasıdır ve Aspose.PSD kütüphanesinin sunduğu çeşitli sınıflara ve yöntemlere erişmemizi sağlar.
```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```
Artık sahneyi hazırladığımıza göre harekete geçme zamanı! Bu bölümde kodu yönetilebilir adımlara ayıracağız. Bu adımlar bir PSD dosyasını okuma, Vmsk kaynağını kullanma ve hatta düzenleme konusunda size yol gösterecektir.
## 1. Adım: PSD Dosyanızı Yükleyin
Yapmak istediğiniz ilk şey PSD dosyanızı yüklemektir. İşte tüm sihrin başladığı yer burası.
```java
String dataDir = "Your Document Directory"; // Bu yolu güncelle
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  biz ayarladık`dataDir` PSD dosyanızın dizinine. 
-  için bir string oluşturuyoruz.`sourceFileName`dizini PSD dosyasının adıyla birleştirerek.
-  Son olarak PSD dosyasını bir klasöre yüklüyoruz.`PsdImage` kullanarak nesne`Image.load()`.
## Adım 2: Vmsk Kaynağını Alın
Artık PSD imajımızı yüklediğimize göre Vmsk kaynağını getirelim.
```java
VmskResource resource = getVmskResource(im);
```

-  biz diyoruz`getVmskResource()` Görüntüden Vmsk kaynağının aranmasını ve alınmasını sağlayan yöntem.
## 3. Adım: Vmsk Kaynak Özelliklerini Doğrulayın
Değişikliklere devam etmeden önce Vmsk kaynağımızın beklenen durumda olduğunu doğrulamak önemlidir.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Burada Vmsk kaynağının çeşitli özelliklerini kontrol ediyoruz. Devre dışı bırakılmadığından, ters çevrilmediğinden veya bağlantılı olmadığından ve doğru sayıda yola sahip olduğundan emin olmak istiyoruz.
## 4. Adım: Her Yola Erişin ve Doğrulayın
Biraz daha derine inelim ve Vmsk kaynağı içindeki yolları inceleyelim.
```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Kriterlerimize uyduklarından emin olmak için üç özel yol kaydını çıkarıyoruz ve türlerini ve özelliklerini doğruluyoruz.
## Adım 5: Vmsk Kaynağını Düzenleyin
Şimdi değişiklik kısmına geçiyoruz! Vmsk kaynağının özelliklerini gerektiği gibi değiştirebilirsiniz.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Bu blokta Vmsk kaynağının çeşitli özelliklerini değiştiriyoruz. Bunları true olarak ayarlayarak maskenin PSD dosyasında nasıl davranacağını kontrol edebiliriz.
## Adım 6: Bezier Düğüm Noktalarını Değiştirin
Bezier düğümleri vektör yolları için kritik öneme sahiptir. Burada bazı değerleri değiştirelim.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Spesifik olarak erişiyoruz`BezierKnotRecord` vektör maskesini potansiyel olarak yeniden şekillendirmek için yolları değiştirme ve noktalarını değiştirme.
## Adım 7: Değiştirilen PSD Dosyasını Kaydedin
Tüm düzenlemeler tamamlandıktan sonra değiştirilen PSD dosyasını kaydetme zamanı gelir. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Dışa aktarılan PSD dosyasının yolunu belirliyoruz ve ardından çağırıyoruz`im.save()` Değişiklikleri bu yeni dosyaya yazmak için.
## Adım 8: Kaynakları Temizleyin
Son olarak, kaynakları serbest bırakmak için görüntüyü uygun şekilde elden çıkardığımızdan emin olmalıyız.
```java
im.dispose();
```

- İşiniz bittiğinde herhangi bir kaynağı elden çıkarmak her zaman iyi bir uygulamadır. Bu, uygulamalarınızdaki bellek sızıntılarını önlemeye yardımcı olur.
## Çözüm
Tebrikler! Aspose.PSD for Java'yı kullanarak PSD dosyalarında Vmsk kaynaklarını desteklemeye yönelik ayrıntılı bir süreci tamamladınız. Görüntünün yüklenmesi, Vmsk kaynağının alınması ve doğrulanması, özelliklerinin düzenlenmesi ve ardından değiştirilmiş PSD'nizin kaydedilmesi gibi temel konuları ele aldınız. Bu becerilerle, PSD dosyalarındaki çeşitli kaynakları verimli bir şekilde yönetebilir ve kullanabilir, grafik tasarım projelerinizi veya otomasyon komut dosyalarınızı geliştirebilirsiniz.
## SSS'ler
### Vmsk kaynağı nedir?
Vmsk kaynağı, PSD dosyasındaki karmaşık vektör şekillerine ve düzenleme özelliklerine olanak tanıyan bir vektör maskesidir.
### Aspose.PSD'yi bir Maven projesinde kullanabilir miyim?
Evet, depodaki koordinatlarını kullanarak Aspose.PSD'yi Maven projenize bağımlılık olarak ekleyebilirsiniz.
### Değiştirilen PSD dosyalarımı hangi formatta kaydedebilirim?
Bunları PSD dosyaları olarak kaydedebilir veya PNG, JPEG vb. diğer formatlara aktarabilirsiniz.
### Aspose.PSD'nin ücretsiz deneme sürümü mevcut mu?
 Evet, özelliklerini test etmek için Aspose.PSD'nin ücretsiz deneme sürümüne erişebilirsiniz. Ziyaret edin[ücretsiz deneme bağlantısı](https://releases.aspose.com/).
### Aspose.PSD için nasıl destek alabilirim?
 Katılabilirsiniz[Forumu aspose](https://forum.aspose.com/c/psd/34)Destek ve sorun giderme yardımı için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
