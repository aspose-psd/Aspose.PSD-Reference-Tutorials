---
title: Java ile PSD Dosyalarında Infx Kaynağını Destekleyin
linktitle: Java ile PSD Dosyalarında Infx Kaynağını Destekleyin
second_title: Aspose.PSD Java API'si
description: Bu kapsamlı, adım adım eğitimle Aspose.PSD for Java kullanarak PSD dosyalarındaki Infx Kaynağını nasıl değiştireceğinizi öğrenin. Her seviyedeki geliştiriciler için mükemmeldir.
type: docs
weight: 13
url: /tr/java/working-with-psd-files/support-infx-resource-psd-files/
---
## giriiş

Java'da PSD (Photoshop Belgesi) dosyalarıyla çalışmak göz korkutucu görünebilir, ancak öyle olmak zorunda değildir. Çeşitli kaynaklar içeren çok katmanlı bir PSD dosyanız olduğunu ve dosyanın bütünlüğünün bozulmadan kalmasını sağlarken InfxResource gibi belirli kaynakları değiştirmeniz gerektiğini düşünün. İşte tam bu noktada Aspose.PSD for Java devreye giriyor ve PSD dosyalarını sorunsuz bir şekilde yönetmek için sezgisel bir API sunuyor. Bu eğitimde, Aspose.PSD for Java kullanarak bir InfxResource'u PSD dosyasında nasıl bulacağınızı, düzenleyeceğinizi ve kaydedeceğinizi anlatacağız. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu kılavuz PSD kaynaklarının kullanımını mümkün olduğunca basit hale getirecektir.

## Önkoşullar

Öğreticiye dalmadan önce ihtiyacınız olan her şeye sahip olduğunuzdan emin olalım. İşte hızlı bir kontrol listesi:

1.  Java Geliştirme Kiti (JDK): Makinenizde JDK'nın en son sürümünün yüklü olduğundan emin olun. adresinden indirebilirsiniz.[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
  
2.  Aspose.PSD for Java Kütüphanesi: Aspose.PSD for Java'nın en son sürümünü şuradan indirin:[indirme bağlantısı](https://releases.aspose.com/psd/java/) Henüz yapmadıysanız, ücretsiz deneme sürümünden yararlanabilir veya adresinden lisans satın alabilirsiniz.[Burada](https://purchase.aspose.com/).

3. Entegre Geliştirme Ortamı (IDE): IntelliJ IDEA, Eclipse veya NetBeans gibi herhangi bir Java IDE işi yapacaktır.

4. Temel Java Bilgisi: Java programlama kavramlarına aşina olmak çok önemlidir. Java'da yeniyseniz, devam etmeden önce Java'nın temel bilgilerini tazelemeyi düşünün.

5. Örnek PSD Dosyası: Öğreticiyle birlikte takip etmek için InfxResource içeren örnek bir PSD dosyası gereklidir. Kendi dosyanızı kullanabilir veya örnek bir dosya indirebilirsiniz.

## Paketleri İçe Aktar

Aspose.PSD for Java'yı kullanmaya başlamanın ilk adımı gerekli paketleri Java projenize aktarmaktır. Bu adım, Java uygulamanızın Aspose.PSD kütüphanesinin özelliklerini kullanmasını sağladığından kritik öneme sahiptir.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layerresources.InfxResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.LayerResource;
import com.aspose.psd.systemexceptions.ArgumentNullException;
```

Şimdi kodu takip edilmesi kolay adımlara ayıralım.

## 1. Adım: Kaynak ve Hedef Yollarını Ayarlayın

Öncelikle PSD dosyanızın bulunduğu kaynak dizini ve değiştirilen dosyanın kaydedileceği hedef dizini belirtmeniz gerekir.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFileName = sourceDir + "SampleForInfxResource.psd";
String destinationFileName = outputDir + "SampleForInfxResource_out.psd";
```

 Burada,`sourceDir` orijinal PSD dosyanızın bulunduğu dizin yoludur ve`outputDir` değiştirilen PSD dosyasının kaydedileceği yerdir. Bu yolları ayarlayarak uygulamanızın çalışması gereken dosyaları nerede bulacağını ve saklayacağını bilmesini sağlarsınız.

## Adım 2: PSD Görüntüsünü Yükleyin

 Daha sonra PSD dosyasını bir`PsdImage` nesne. Bu nesne, PSD dosyasındaki katmanları ve kaynakları değiştirmenize olanak tanır.

```java
PsdImage im = null;
try {
    im = (PsdImage) Image.load(sourceFileName);
} catch (ArgumentNullException e) {
    System.out.println("File not found: " + e.getMessage());
}
```

`Image.load` PSD dosyasını yüklemek için burada yöntem kullanılır. Dosya bulunamazsa veya yol yanlışsa,`ArgumentNullException` yakalanacak ve uygun bir mesaj görüntülenecektir.

## 3. Adım: Katmanlar ve Kaynaklar Arasında Yineleme Yapın

 PSD dosyası yüklendikten sonraki adım, belirli bir dosyayı bulmak için katmanları boyunca yinelemektir.`InfxResource` arıyorsun.

```java
boolean isRequiredResourceFound = false;

for (Layer layer : im.getLayers()) {
    for (LayerResource layerResource : layer.getResources()) {
        if (layerResource instanceof InfxResource) {
            InfxResource resource = (InfxResource) layerResource;
            isRequiredResourceFound = true;
            
            // Kaynağı doğrulayın ve değiştirin
            if (!resource.getBlendInteriorElements()) {
                resource.setBlendInteriorElements(true);
                im.save(destinationFileName);
            }
            break;
        }
    }
}
```

 Burada her katman ve onunla ilişkili kaynaklar arasında geçiş yapıyoruz. Eğer bir`InfxResource`bulunduğunda kontroller veya değişiklikler yaparız. Özellikle, olup olmadığını kontrol ediyoruz`BlendInteriorElements` yanlıştır ve eğer öyleyse, doğru olarak ayarlayın ve değiştirilen dosyayı kaydedin.

## Adım 4: Görüntüyü Kaydedin ve Atın

Kaynağı değiştirdikten sonra, değişiklikleri kaydetmek ve bellekte yer açmak için görüntü nesnesini elden çıkarmak önemlidir.

```java
finally {
    if (im != null) im.dispose();
}
```

`finally` blok şunları sağlar:`PsdImage` nesnenin uygun şekilde imha edilmesi, bellek sızıntılarının önlenmesi ve uygulamanızın verimli kalmasının sağlanması.

## Adım 5: Değiştirilen PSD Dosyasını Yükleyin ve Doğrulayın

Artık değiştirilen PSD dosyasını kaydettiğinize göre, son adım dosyayı tekrar yüklemek ve değişikliklerin doğru şekilde uygulandığını doğrulamaktır.

```java
PsdImage im2 = null;
try {
    im2 = (PsdImage) Image.load(destinationFileName);
    for (Layer layer : im2.getLayers()) {
        for (LayerResource layerResource : layer.getResources()) {
            if (layerResource instanceof InfxResource) {
                InfxResource resource = (InfxResource) layerResource;
                Assert.isTrue(resource.getBlendInteriorElements(), "The InfxResource.BlendInteriorElements should change to true");
                break;
            }
        }
    }
} finally {
    if (im2 != null) im2.dispose();
}
```

 Bu adım, değişikliğin beklendiği gibi uygulandığından emin olmak için çok önemlidir. Değiştirilen dosyayı yüklersiniz ve kontrol edersiniz.`BlendInteriorElements` olarak ayarlandığından emin olmak için özellik`true`.

## Çözüm

 Tebrikler! Nasıl manipüle edeceğinizi başarıyla öğrendiniz.`InfxResource`Aspose.PSD for Java kullanarak bir PSD dosyasında. İster küçük bir proje üzerinde çalışıyor olun ister bu işlevselliği daha büyük bir uygulamaya entegre ediyor olun, bu eğitimde özetlenen adımlar sağlam bir temel oluşturacaktır. Aspose.PSD for Java'nın gücü, esnekliğinde ve kullanım kolaylığında yatıyor; bu da onu PSD dosyalarıyla çalışan geliştiriciler için vazgeçilmez bir araç haline getiriyor. Öyleyse devam edin, daha fazla özelliği keşfedin ve Aspose.PSD for Java ile başka neler başarabileceğinizi görün!

## SSS'ler

### Bir PSD dosyasındaki diğer kaynakları yönetmek için Aspose.PSD for Java'yı kullanabilir miyim?

 Evet, Aspose.PSD for Java, bir PSD dosyasındaki çeşitli kaynakları ve özellikleri değiştirmenize olanak tanır;`InfxResource`.

###  Eğer`InfxResource` is not found in the PSD file?

 Eğer`InfxResource` bulunamazsa kod yürütülmeye devam eder ancak belirtilen eylemler gerçekleştirilmez ve hata ayıklama amacıyla bir mesaj günlüğe kaydedilebilir.

### Birden çok katmana sahip büyük PSD dosyalarını nasıl işleyebilirim?

Çok katmanlı büyük PSD dosyalarının işlenmesi daha fazla bellek ve işlem gücü gerektirebilir. Ortamınızın optimize edildiğinden emin olun ve kaynakları serbest bırakmak için artık ihtiyaç duyulmadığında nesneleri elden çıkarmayı düşünün.

### PSD dosyasında yapılan değişiklikleri geri almak mümkün müdür?

Değişiklikler kaydedildikten sonra, orijinal dosyanın yedeğini almadığınız sürece kalıcı olurlar. Orijinali değiştirmeden saklamanız gerekiyorsa her zaman dosyanın bir kopyası üzerinde çalışın.

### Aspose.PSD for Java'yı kullanarak birden fazla PSD dosyasında değişiklik yapmayı otomatikleştirebilir miyim?

Evet, her dosyaya aynı değişiklikleri uygulayarak birden çok PSD dosyasını toplu olarak işlemek için komut dosyaları oluşturabilirsiniz.