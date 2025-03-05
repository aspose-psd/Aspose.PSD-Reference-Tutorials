---
title: Java kullanarak PSD Dosyalarına Ayarlama Katmanlarını Uygulayın
linktitle: Java kullanarak PSD Dosyalarına Ayarlama Katmanlarını Uygulayın
second_title: Aspose.PSD Java API'si
description: Geliştiricilere yönelik bu eksiksiz adım adım kılavuzda Java için Aspose.PSD'yi kullanarak PSD dosyalarına ayarlama katmanları uygulamayı öğrenin.
type: docs
weight: 15
url: /tr/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---
## giriiş
PSD dosyalarında depolanan görselleri geliştirmek isteyen bir Java geliştiricisi misiniz? Eğer öyleyse, doğru yerdesiniz! Bu makalede, Java için Aspose.PSD kütüphanesini kullanarak PSD dosyalarına ayarlama katmanlarının nasıl uygulanacağını inceleyeceğiz. İster kişisel bir proje üzerinde ister profesyonel bir uygulama üzerinde çalışıyor olun, PSD dosyalarının nasıl değiştirileceğini anlamak, yazılımınızın yeteneklerini önemli ölçüde artırabilir. 

## Önkoşullar
Koda geçmeden ve bu ayarlama katmanlarını uygulamaya başlamadan önce ihtiyacınız olacak birkaç önkoşul vardır:
1. Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Oracle'ın web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD Kütüphanesi: Henüz yapmadıysanız, Java için Aspose.PSD kütüphanesini indirmeniz gerekecektir. Onu bulabilirsin[Burada](https://releases.aspose.com/psd/java/).
3. Geliştirme Ortamı: Kodunuzu yazıp çalıştıracağınız IntelliJ IDEA veya Eclipse gibi bir Java entegre geliştirme ortamı (IDE) kurun.
4. Java ile Temel Bilgi: Java programlamaya ilişkin genel bir anlayış, sorunsuz bir şekilde ilerlemenize yardımcı olacaktır.
5. PSD Dosyaları: Test amacıyla elinizde birkaç PSD dosyası bulundurun. Adobe Photoshop kullanarak bazılarını oluşturabilir veya internetten örnek dosyalar indirebilirsiniz.
## Paketleri İçe Aktar
Kodlamaya başlamadan önce hangi paketleri import etmemiz gerektiğini açıklayalım. Aspose.PSD, Photoshop dosyalarıyla çeşitli şekillerde çalışmamıza olanak tanıyor; o halde PSD görüntülerini ve ayarlama katmanlarını yönetmek için gerekli sınıfları alalım.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
Artık paketlerimizi hazırladığımıza göre örnekleri adım adım inceleyelim!
## Adım 1: PSD Dosyasını Yükleyin
Yolculuğumuzun ilk adımı PSD dosyasını yüklemektir. Bu, ayarlama katmanlarımızı uygulamak için üzerinde çalışacağımız dosyadır.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 Bu snippet'te PSD dosyalarımızın bulunduğu dizini tanımlıyoruz ve işlemek istediğimiz belirli dosyayı yüklüyoruz. Değiştirdiğinizden emin olun`"Your Document Directory"` makinenizdeki PSD dosyalarınızın gerçek yolu ile.
## Adım 2: Katmanlar Üzerinde Yineleme Yapın
Artık PSD dosyasını yüklediğimize göre, ayarlama katmanlarımızı bulmak için katmanları arasında yineleme yapmak isteyeceğiz.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 Bu adımda, PSD dosyasındaki her katmanın içinden geçerek aşağıdaki katmanlardan herhangi birini belirleriz:`AdjustmentLayer` tip. Bir tane bulursak, onu genellikle ilk katman olan temel katmanla birleştiririz (`im.getLayers()[0]`). Bu birleştirme işlemi, ayarlamaları imajımıza etkili bir şekilde uygular. 
## Adım 3: Değiştirilen PSD Dosyasını Kaydedin
Katmanları değiştirdikten sonra yaptığımız değişiklikleri kaydetmemiz çok önemlidir. Bunu bir sonraki adımda yapalım.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 Burada değiştirilen PSD dosyamızın dışa aktarma yolunu belirtiyoruz ve`save()` Değişikliklerimizi diske yazma yöntemi.
## Adım 4: Düzey Ayarlama Katmanı
Farklı türde bir ayarlama katmanı için işlemi tekrarlayalım: Düzeyler ayarlama katmanı. 
### Düzey Ayarlama Katmanı PSD'sini yükleyin
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
Daha önce olduğu gibi Düzeyler ayarlama katmanımızı içeren PSD dosyasını yüklüyoruz. 
### Düzey Katmanları Arasında Yineleme
Daha sonra, tıpkı daha önce yaptığımız gibi katmanlar arasında tekrar döngü yapacağız, ancak şimdi başka bir PSD dosyasıyla çalışıyoruz.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
Bu kod önceki yinelemeye benzer şekilde davranır; mevcut PSD dosyasındaki ayarlama katmanlarını arayarak mevcut tüm ayarlamaları uygulamamıza olanak tanır.
## Düzey Ayarlama Katmanı PSD'sini kaydedin
Son olarak ayarlamaları uyguladıktan sonra bu yeni dosyayı kaydedeceğiz.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
Artık Seviye ayarlama katmanını başarıyla işledik!
## Çözüm
Tebrikler! Java ve Aspose.PSD kütüphanesini kullanarak PSD dosyalarına ayarlama katmanlarının nasıl uygulanacağını öğrendiniz. İster renkleri değiştiriyor ister seviyeleri ayarlıyor olun, artık PSD dosyalarını programlı olarak işlemek için temel becerilere sahipsiniz.
Aspose.PSD'yi kullanmak, görüntü düzenlemede iş akışlarını önemli ölçüde kolaylaştırabilir ve geleneksel araçların yapamayacağı şekillerde otomasyona ve özelleştirmeye olanak tanır. Kütüphaneyi daha fazla keşfetmekten ve farklı katman türlerini deneyerek hangi yaratıcı olanakların mevcut olduğunu görmekten çekinmeyin.
## SSS'ler
### Aspose.PSD kütüphanesi nedir?
Aspose.PSD, geliştiricilerin Photoshop PSD dosyalarını Java uygulamalarına yüklemesine, değiştirmesine ve kaydetmesine olanak tanıyan bir kitaplıktır.
### Aspose.PSD'yi ücretsiz kullanabilir miyim?
 Evet! Aspose, kütüphanelerini keşfetmeniz için ücretsiz bir deneme sunuyor. Kayıt olabilirsiniz[Burada](https://releases.aspose.com/).
### Aspose.PSD'yi kullanabilmek için Photoshop'un yüklü olması gerekiyor mu?
Hayır Photoshop'a ihtiyacınız yok. Aspose.PSD, PSD dosyalarını programlı olarak işlemek için bağımsız olarak çalışır.
### Aspose.PSD belgelerini nerede bulabilirim?
Dokümantasyon sayfasını ziyaret edebilirsiniz[Burada](https://reference.aspose.com/psd/java/) özellikleri, sınıfları ve yöntemleri keşfetmek için.
### Aspose ürünleri için nasıl destek alabilirim?
 Desteğe şu adresten ulaşabilirsiniz:[Forumu aspose](https://forum.aspose.com/c/psd/34) Soru sorabileceğiniz ve çözüm bulabileceğiniz yer.