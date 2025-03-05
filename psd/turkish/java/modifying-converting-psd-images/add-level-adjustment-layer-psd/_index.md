---
title: PSD'ye Seviye Ayarlama Katmanı Ekleme
linktitle: PSD'ye Seviye Ayarlama Katmanı Ekleme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PSD dosyalarınıza etkili bir Düzey Ayarlama Katmanı eklemeyi öğrenin. Resim düzenleme becerilerinizi geliştirin.
type: docs
weight: 16
url: /tr/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## giriiş
Görüntü düzenleme söz konusu olduğunda seviyeleri yönetmek, fotoğraflarınızın canlılığı ve netliği açısından büyük fark yaratabilir. Photoshop cephaneliğindeki kullanışlı araçlardan biri, resimlerinizin ton aralığını ve renk dengesini ayarlamanıza olanak tanıyan "Seviye Ayarlama Katmanı"dır. Bu kılavuzda, Aspose.PSD for Java kullanarak bir PSD dosyasında Seviye Ayarlama Katmanını nasıl uygulayacağınız konusunda size yol göstereceğiz. O halde Java IDE'nizi alın.
## Önkoşullar
Seviye ayarlamaları dünyasına atlamadan önce, sorunsuz bir sürüş sağlamak için birkaç şeyi ayarlamanız gerekir:
1.  Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun. Elinizde yoksa oradan alabilirsiniz.[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) veya OpenJDK'yi kullanın.
2.  Aspose.PSD for Java Library: PSD dosyalarını yönetmek için Aspose.PSD kütüphanesini indirmeniz gerekir. En son sürümü buradan edinebilirsiniz[indirme bağlantısı](https://releases.aspose.com/psd/java/) ve JAR'ı projenizin kütüphanesine eklediğinizden emin olun.
3. Temel Java Bilgisi: Bu eğitim boyunca kod parçacıklarına dalacağımız için Java programlamaya ilişkin temel bir anlayışa sahip olmak yardımcı olacaktır.
4. IDE Kurulumu: Kodunuzu yazmak ve çalıştırmak için IntelliJ IDEA, Eclipse veya NetBeans gibi tercih ettiğiniz herhangi bir Java IDE'yi kullanabilirsiniz. Java projenizi kurduğunuzdan ve Aspose.PSD kütüphanesini eklediğinizden emin olun.

## Paketleri İçe Aktar
Kodumuzu yazmaya başlamadan önce Aspose.PSD kütüphanesinden gerekli paketleri import etmemiz gerekiyor. Bunu nasıl yapabileceğiniz aşağıda açıklanmıştır:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Bu paketleri içe aktararak PSD dosyalarımızı yüklemek, değiştirmek ve kaydetmek için gerekli sınıflara erişebileceğiz.

Şimdi süreci sindirilebilir adımlara ayıralım. PSD dosyasını yükleme, seviyeleri ayarlama ve değişikliklerinizi kaydetme adımlarını adım adım takip edin. 
## 1. Adım: Dosya Yollarınızı Ayarlayın
İlk adım, PSD dosyamızın nerede olduğunu ve değiştirilen çıktıyı nereye kaydetmek istediğimizi tanımlamaktır. Dizin yolunu ihtiyaçlarınıza uyacak şekilde özelleştirebilirsiniz.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 İşte, değiştir`"Your Document Directory"`sisteminizde PSD dosyanızın depolandığı gerçek yolla. Bu, bundan sonra yapacağımız her şeye zemin hazırlıyor.
## Adım 2: PSD Dosyasını Yükleyin
 Şimdi PSD dosyasını kullanarak yükleyelim.`PsdImage` sınıf. Bu adım, katmanlara erişmemize ve bunları yönetmemize olanak tanıdığı için önemlidir.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 aradığınızda`Image.load()` PSD dosyasını okuyacak ve bir örneğini oluşturacaktır.`PsdImage` ile çalışabilirsiniz.
## Adım 3: Katmanlar Arasında Yineleme Yapın
Seviye Ayarlama Katmanını ayarlamak istediğimiz için PSD dosyamızdaki her katman arasında döngü yapmamız gerekecek. Bu, değiştirmek istediğimiz belirli katmanı bulmamıza yardımcı olur.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Daha fazla manipülasyon buraya gelecek...
    }
}
```
 Bu döngüde,`instanceof LevelsLayer` geçerli katmanın Düzey Ayarlama Katmanı olup olmadığını kontrol eder. Eğer öyleyse, özelliklerini değiştirmeye devam edebiliriz.
## Adım 4: Seviye Kanal Ayarlarını Yapın
Doğru katmanı belirledikten sonra giriş ve çıkış seviyelerini değiştirebiliriz. Sihrin gerçekleştiği yer burası! Görüntüyü nasıl etkilediklerini görmek için farklı parametreleri ayarlayın.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Her parametrenin yaptığı şey:
- Giriş Orta Ton Düzeyi: Orta tonları ayarlar.
- Giriş Gölge Düzeyi: Görüntünün daha karanlık alanlarını ayarlar.
- Giriş Vurgulama Düzeyi: Görüntünün parlak alanlarını değiştirir.
- Çıkış Gölge Düzeyi: Koyu gölgelerin nasıl görüneceğini ayarlar.
- Çıkış Vurgulama Düzeyi: Işık vurgularının nasıl görüneceğini ayarlar.
Farklı değerleri denemekten çekinmeyin!
## Adım 5: Değiştirilen PSD Dosyasını Kaydedin
Ayarlamalarımızı yaptığımıza göre artık değiştirilen PSD dosyasını kaydetme zamanı geldi. Bu adım, değişikliklerinizin uygulandığından ve saklandığından emin olmak için çok önemlidir.
```java
im.save(psdPathAfterChange);
```
 Artık ayarlanan PSD dosyanızı belirtilen konumda bulabilirsiniz.`psdPathAfterChange`. 
## Çözüm
Aspose.PSD for Java'yı kullanarak PSD dosyasına Seviye Ayarlama Katmanını nasıl ekleyeceğinizi öğrendiniz! Bu kılavuzu takip ederek görsellerinizin ton kalitesini zahmetsizce ayarlayabilir ve daha canlı ve görsel olarak çekici çıktıların önünü açabilirsiniz. Unutmayın, pratik yapmak mükemmelleştirir; bu nedenle, ayarlamalarda ince ayar yapmaktan ve değişikliklerin etkilerini görmek için farklı PSD dosyalarını keşfetmekten çekinmeyin.
## SSS'ler
### Seviye Ayarlama Katmanı Nedir?
Düzey Ayarlama Katmanı, gölgeleri, orta tonları ve açık tonları dengeleyerek görüntülerinizdeki ton aralığını düzeltmenize olanak tanır.
### Aspose.PSD'yi satın almadan kullanabilir miyim?
Evet! Aspose, satın almadan önce kütüphaneyi test etmek için ücretsiz bir deneme sunuyor.
### Aspose.PSD belgelerini nerede bulabilirim?
 Belgeleri bulabilirsiniz[Burada](https://reference.aspose.com/psd/java/).
### Aspose ürünleri için herhangi bir topluluk desteği var mı?
 Kesinlikle! Soru sorabilir ve destek alabilirsiniz.[Forumu aspose](https://forum.aspose.com/c/psd/34).
### Aspose.PSD için nasıl geçici lisans alabilirim?
 Geçici lisans başvurusunda bulunabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).