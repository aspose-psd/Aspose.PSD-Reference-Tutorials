---
title: PSD'de Uzunluk Kayıt Verisi Özelliklerini Destekleme - Java
linktitle: PSD'de Uzunluk Kayıt Verisi Özelliklerini Destekleme - Java
second_title: Aspose.PSD Java API'si
description: Aspose.PSD'yi kullanarak Java'da uzunluk kaydı veri özelliklerine sahip PSD dosyalarını nasıl değiştireceğinizi öğrenin. Tüm ayrıntılar için bu adım adım kılavuzu izleyin.
weight: 14
url: /tr/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'de Uzunluk Kayıt Verisi Özelliklerini Destekleme - Java

## giriiş
Hiç Photoshop dosyalarıyla çalıştınız mı ve katmanları veya şekilleri programlı olarak değiştirmek istediniz mi? Öyleyse Aspose.PSD for Java kütüphanesinin güzelliğine rastladınız. Bu güçlü araç, geliştiricilerin Java kodu aracılığıyla PSD dosyalarıyla sorunsuz bir şekilde etkileşime girmesine ve bunları değiştirmesine olanak tanır. Bugünün makalesinde, bu kitaplığı kullanarak bir PSD dosyasındaki uzunluk kaydı veri özelliklerinin nasıl destekleneceğini ayrıntılı olarak inceleyeceğiz. 
İster deneyimli bir Java geliştiricisi olun ister yeni başlıyor olun, bu kılavuz bilmeniz gereken her şeyi size adım adım anlatacaktır. Sonunda, Java ortamınızın rahatlığından ayrılmadan bir PSD dosyasını açabilecek, vektör şekli özelliklerini değiştirebilecek ve değişikliklerinizi kaydedebileceksiniz. Haydi kollarımızı sıvayıp oyuna girelim!
## Önkoşullar
Başlamadan önce hazır olmanız gereken birkaç şey var. Her şeyin yerli yerinde olduğundan emin olmak süreci daha sorunsuz hale getirir ve hiç kimse son dakika mücadelesinden hoşlanmaz! İhtiyacınız olan şey:
1.  Java Geliştirme Kiti (JDK): Makinenizde JDK'nın kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Oracle'ın web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) veya bir paket yöneticisi kullanın.
2.  Aspose.PSD for Java Library: Aspose.PSD for Java kütüphanesini indirip projenize dahil etmeniz gerekecektir. Şuradan al:[Aspose sürümler sayfası](https://releases.aspose.com/psd/java/).
3. IDE: Daha iyi kod yönetimi için IntelliJ IDEA, Eclipse veya seçtiğiniz herhangi bir Java IDE gibi bir Entegre Geliştirme Ortamı (IDE) kullanın.
4. Bir PSD Dosyası: Bu eğitim için üzerinde çalışmak üzere bir PSD dosyasına ihtiyacınız olacak. Adobe Photoshop'ta bir tane oluşturabilir veya örnek bir PSD indirebilirsiniz.
5. Temel Java Bilgisi: Java sözdizimine aşina olmak, kolaylıkla takip etmenize yardımcı olacaktır.
## Paketleri İçe Aktar
Artık tüm önkoşulları ayarladığınıza göre, bir sonraki adım gerekli paketleri içe aktarmaktır. Bu adım, kullanacağımız sınıflara ve yöntemlere erişim sağlamak için çok önemlidir. Aşağıda gerekli paketleri Java projenize nasıl aktaracağınıza dair bir örnek verilmiştir:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```
Bu içe aktarmalarla artık PSD dosyalarını değiştirmeye hazırsınız!

## 1. Adım: Kaynak ve Çıkış Dizinlerinizi Ayarlayın
Herhangi bir dosya yüklemeden önce, giriş PSD dosyamızın nereden geldiğini ve değiştirilen dosyayı nereye kaydetmek istediğimizi belirleyelim. Dizin yollarını yerel makinenize göre ayarlayın.
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```
## Adım 2: PSD Dosyasını Yükleyin
 PSD dosyasını yükleme zamanı! Bunun için kullanacağımız`Image.load` Aspose.PSD kütüphanesinden yöntem. Bu yöntem, PSD dosyasını açmamıza ve katmanlarına ve kaynaklarına erişmemize olanak tanır.
```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```
Bu, bir kitabı açmak gibidir; sayfalarına (katmanlar ve kaynaklar) göz atabileceksiniz.
## Adım 3: Katmanda Vsms Kaynağını Bulun
Daha sonra, PSD dosyamızda belirli VsmsResource'u bulmamız gerekiyor. Bu kaynaklar, vektör şekli katmanlarına ilişkin verileri tutar. Sihrin gerçekleştiği yer burası! Bu kod parçasında, bu kaynağı bulmak için katmanın kaynakları arasında dolaşıyoruz.
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```
Bir hazine avı gibi, değerli vektör verilerini bulmak için katmanlar arasında arama yapıyorsunuz!
## Adım 4: Uzunluk Kayıtlarına Erişim
VsmsResource'a sahip olduğumuzda, HeightRecord nesnelerini çıkartabiliriz. Her bir Uzunluk Kaydı, vektör şekilleri içindeki bir yolu temsil eder. Burada, özelliklerini değiştirmek için üç Uzunluk Kaydına erişiyoruz.
```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```
Bu, bir tablonun hangi kısımlarına rötuş yapmak istediğinizi seçmek gibidir!
## Adım 5: Yol İşlemi Özelliklerini Değiştirin
Şimdi işin eğlenceli kısmı geliyor; yol özelliklerini değiştirmek! Burada setPathOperations yöntemi, şekillerin birbirleriyle nasıl etkileşimde bulunduğunu değiştirmeye olanak tanır. Üst üste binen alanları hariç tutmak veya ön şekli arkadan çıkarmak gibi işlemleri ayarlayabiliriz.
```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```
Bunu bir pastanın katmanlarını ayarlarken hayal edin; her katman, onu nasıl dilimlediğinize bağlı olarak farklı şekilde etkileşime girer!
## Adım 6: Değiştirilen PSD Dosyasını Kaydedin
Gerekli değişiklikleri yaptıktan sonraki adım, değiştirilen PSD dosyanızı kaydetmektir. Tüm sıkı çalışmanızın karşılığını alacağınız yer burasıdır. 
```java
psdImage.save(outPsdFilePath);
```
Başyapıtınız artık dünyanın görmesi için düzgün bir şekilde paketlendi!
## Adım 7: Kaynakları Temizleyin
Son olarak, hafızayı ve kaynakları boşaltmak için kullandığınız nesneleri atmanız çok önemlidir.
```java
psdImage.dispose();
```
Bunu bir sanat projesinden sonra çalışma alanınızı temizlemek gibi düşünün; her şeyin temiz ve düzenli olmasını sağlayın!
## Çözüm
İşte burada! Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki uzunluk kaydı veri özelliklerini desteklemeye ilişkin kapsamlı bir eğitimi tamamladınız. Dosyanın yüklenmesinden şekil özelliklerinin değiştirilmesine ve son ürünün kaydedilmesine kadar her adım bu kitaplığın gücünü ortaya çıkarır. İster yaratıcı projeler üzerinde çalışıyor olun ister grafik varlıklarını otomatikleştiriyor olun, Aspose.PSD yepyeni bir olasılıklar dünyasının kapılarını açar. Başlamaya hazır mısınız? PSD dosyalarınıza dalın ve yaratıcılığınızı serbest bırakın!
## SSS'ler
### Java için Aspose.PSD nedir?
Aspose.PSD for Java, geliştiricilerin Java kullanarak Photoshop PSD dosyalarını programlı olarak değiştirmesine ve bunlarla çalışmasına olanak tanıyan bir kitaplıktır.
### Aspose.PSD'yi ücretsiz bir projede kullanabilir miyim?
Evet, Aspose web sitesinde bulunan deneme sürümünü kullanarak kütüphaneyi ücretsiz olarak deneyebilirsiniz.
### PSD dosyalarında ne tür değişiklikler yapabilirim?
Katmanları, şekilleri, metinleri, yol işlemlerini ve çok daha fazlasını PSD dosyalarında değiştirebilirsiniz.
### Aspose.PSD diğer programlama dilleriyle uyumlu mu?
Evet, Aspose, .NET ve Python dahil olmak üzere farklı programlama dilleri için çeşitli kütüphaneler sunmaktadır.
### Aspose.PSD belgelerini nerede bulabilirim?
 Dokümantasyonun tamamına erişebilirsiniz[Burada](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
