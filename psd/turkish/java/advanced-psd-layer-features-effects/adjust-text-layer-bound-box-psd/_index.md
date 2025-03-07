---
title: Java kullanarak PSD'de Metin Katmanı Bağlı Kutuyu Ayarlama
linktitle: Java kullanarak PSD'de Metin Katmanı Bağlı Kutuyu Ayarlama
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java kullanarak PSD dosyalarındaki metin katmanı sınırlarını ayarlamayı öğrenin. Adım adım talimatlar içeren basit kılavuz.
weight: 25
url: /tr/java/advanced-psd-layer-features-effects/adjust-text-layer-bound-box-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java kullanarak PSD'de Metin Katmanı Bağlı Kutuyu Ayarlama

## giriiş
Photoshop belgelerinin programlı olarak işlenmesi söz konusu olduğunda, Java için Aspose.PSD kütüphanesi göz kamaştırıyor. Bir PSD dosyasındaki metin katmanının sınırlarını ayarlamak istiyorsanız doğru yere geldiniz! Bu eğitim, Java kullanarak metin katmanının ilişkili kutusunu ayarlama sürecinde size adım adım yol gösterecektir.
Takip edilmesi kolay örnekler ve işleri ilgi çekici kılmak için konuşma tonuyla, PSD dosyalarını değiştirmenin sanıldığı kadar göz korkutucu olmadığını göreceksiniz. İster deneyimli bir geliştirici olun ister Java'ya yeni başlıyor olun, burada değerli bilgiler bulacaksınız. PSD manipülasyonunun heyecan verici dünyasına dalalım.
## Önkoşullar
Bu kodlama macerasına yelken açmadan önce, yerine getirmeniz gereken bazı önkoşullar var:
1. Java Geliştirme Kiti (JDK): JDK'nın kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Entegre Geliştirme Ortamı (IDE): Java kodunuzu yazmak ve yürütmek için Eclipse, IntelliJ IDEA veya NetBeans gibi seçtiğiniz bir IDE'yi kullanın. IDE'ler, sözdizimi vurgulama ve hata ayıklama araçları gibi özelliklerle kodlamayı basitleştirir.
3.  Aspose.PSD for Java Library: Aspose.PSD kütüphanesini indirmelisiniz. En son sürümü şuradan alabilirsiniz:[Aspose sürümler sayfası](https://releases.aspose.com/psd/java/). 
4. Temel Java Bilgisi: Java'nın temellerini iyi anlamak, sorunsuz bir şekilde ilerlemenize yardımcı olacaktır.
Harika! Artık gerekli gereksinimleri karşıladığınıza göre, işin eğlenceli kısmına, yani kodu yazmaya geçelim.
## Paketleri İçe Aktar
Fiyat yolculuğumuzun ilk adımı gerekli paketleri ithal etmektir. Bunu, bir Kendin Yap projesine başlamadan önce ihtiyacınız olan tüm araçları toplamak olarak düşünün. Bunu nasıl yapacağınız aşağıda açıklanmıştır:
```java
import com.aspose.psd.Image;
import com.aspose.psd.Size;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```
Bu paketler, PSD dosyaları ve bunların öğeleriyle çalışmak için gereken sınıflara ve yöntemlere erişmenizi sağlar.
## 1. Adım: Dosya Yollarınızı Ayarlayın
Başlamak için PSD dosyanızın yolunu belirtmeniz gerekir. Bu, performansınız için sahneyi hazırlamaya benzer; betiğinizin (veya bu durumda PSD dosyasının) nerede bulunduğunu bilmelisiniz.

```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "LayerWithText.psd";
```
 Burada,`dataDir` PSD dosyanızın saklandığı dizini gösterir. Değiştirdiğinizden emin olun`"Your Document Directory"` gerçek yol ile.`sourceFileName` değişken bu yolu PSD katmanınızın dosya adıyla birleştirir.
## Adım 2: PSD Dosyasını Yükleyin
Daha sonra PSD dosyasını programımıza yüklememiz gerekiyor. Bu adımı, bir kitabı okumadan önce açmak gibi düşünün.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Bu kod satırı PSD dosyasını bir örneğine yükler.`PsdImage`. Artık katmanları işlemek için ihtiyacımız olan her şeye sahibiz.
## 3. Adım: Metin Katmanını Alın
Çalışmak istediğimiz belirli katmanı, yani metin katmanını çıkaralım. Bir PSD dosyası birden fazla katman içerebileceğinden, hangi katmanı ayarlamak istediğinizi tam olarak bilmeniz önemlidir.

```java
TextLayer textLayer = (TextLayer) im.getLayers()[1];
```
`getLayers()`yöntemi, PSD dosyasındaki bir dizi katmanı döndürür. Burada ikinci katmana erişiyoruz (dizilerin sıfır indeksli olduğunu unutmayın!). Doğru katmanı hedeflediğinizden emin olun.
## Adım 4: Katmanın Boyutunu Kontrol Edin
Şimdi metin katmanının boyutunu kontrol edelim. Bu adım, herhangi bir değişiklik yapmadan önce bir ön kontrol görevi görür. Beklenen değerlerle çalışmamızı sağlar.

```java
Size correctOpticalSize = new Size(127, 45);
Size opticalSize = textLayer.getSize();
Assert.areEqual(correctOpticalSize, opticalSize);
```
 Tanımlıyoruz`correctOpticalSize` metin katmanının beklenen boyutu olarak.`getSize()` yöntemi katmanın geçerli boyutunu alır ve`Assert` sınıf eşleşip eşleşmediğini kontrol eder. Eğer yapmazlarsa, bir şeylerin ters gittiğini anlayacaksınız!
## Adım 5: Ciltli Kutu Boyutunu Alın
Sıradaki — metne bağlı kutu boyutunu inceleyelim. Bu size metne uymaya odaklanan alan hakkında fikir verecektir.

```java
Size correctBoundBox = new Size(172, 62);
Size boundBox = textLayer.getTextBoundBox();
Assert.areEqual(correctBoundBox, boundBox);
```
 Daha önce olduğu gibi, beklenen sınırlı kutu boyutumuzun ne olması gerektiğini tanımlıyoruz.`getTextBoundBox()` yöntem gerçek boyutun alınmasına yardımcı olur ve`Assert` beklentilerimizle uyumu bir kez daha teyit ediyor.
## Çözüm
Ve işte karşınızda! Java ve Aspose.PSD kütüphanesini kullanarak Photoshop belgesindeki metin katmanı ciltli kutusunu başarıyla ayarladınız. Sadece birkaç basit adımla bir PSD dosyası yükledik, katmanlarına eriştik ve boyutları doğruladık. Becerilerinizi daha da geliştirmek istiyorsanız Aspose belgelerini daha derinlemesine incelemeyi düşünün[Burada](https://reference.aspose.com/psd/java/) daha karmaşık işlemler için.
## SSS'ler
### Aspose.PSD nedir?
Aspose.PSD, Adobe Photoshop dosyalarını programlı olarak değiştirmek için güçlü bir kütüphanedir ve geliştiricilerin PSD belgeleri oluşturmasına, düzenlemesine ve dönüştürmesine olanak tanır.
### Aspose.PSD'yi kullanabilmek için Photoshop'un yüklü olması gerekiyor mu?
Hayır, Aspose.PSD, Adobe Photoshop'tan bağımsız olarak çalışır ve yazılımın kurulu olmasına gerek kalmadan PSD dosyalarını değiştirmenize olanak tanır.
### Aspose.PSD'yi diğer programlama dilleriyle kullanabilir miyim?
Evet, Aspose.PSD, Java'nın yanı sıra .NET ve Python da dahil olmak üzere çeşitli programlama platformları için mevcuttur.
### Aspose.PSD desteğini nerede bulabilirim?
Destek ve topluluk tartışmalarını kendi sitelerinde bulabilirsiniz.[Aspose Forumu](https://forum.aspose.com/c/psd/34).
### Aspose.PSD'nin deneme sürümü mevcut mu?
 Evet! Ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Web sitesi](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
