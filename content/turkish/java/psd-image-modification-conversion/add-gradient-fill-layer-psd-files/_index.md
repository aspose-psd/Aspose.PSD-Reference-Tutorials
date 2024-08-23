---
title: Java ile PSD Dosyalarına Degrade Dolgu Katmanı Ekleme
linktitle: Java ile PSD Dosyalarına Degrade Dolgu Katmanı Ekleme
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki degrade dolgu katmanlarını değiştirin. Renkleri, şeffaflığı ve diğer degrade özelliklerini programlı olarak nasıl değiştireceğinizi öğrenin.
type: docs
weight: 15
url: /tr/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
---
## giriiş

Hiç PSD dosyalarınız için ekstra görsel sihir dokunuşunu arzuladınız mı? Degradeler, tasarımlarınıza derinlik ve boyut katmanın çarpıcı bir yolunu sunar. Peki ya bu degradeleri Java kullanarak programlı olarak değiştirmek isterseniz? Aspose.PSD kurtarmaya geliyor! Bu kapsamlı kılavuz, Aspose.PSD'yi kullanarak PSD dosyalarındaki degrade dolgu katmanlarını değiştirmenizi sağlayacak ve heyecan verici süreçte sizi adım adım yönlendirecektir.

## Önkoşullar

Dalışa başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

-  Java Geliştirme Kiti (JDK): Java kodunu çalıştırmak için JDK'nın kararlı bir sürümü gereklidir. Oracle web sitesinden indirebilirsiniz:[Oracle JDK indirme sayfasına bağlantı]
-  Aspose.PSD for Java: Bu güçlü kütüphane, Java uygulamalarınızda PSD dosyalarıyla çalışmanıza olanak tanır. Aspose web sitesinden indirin:[Java indirmesi için Aspose.PSD bağlantısı] (Ücretsiz deneme mevcut)

## Paketleri İçe Aktar

PSD dosyalarıyla çalışmak için gereken temel Aspose.PSD paketlerini içe aktararak başlayalım:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

Bu içe aktarmalar, PSD dosyalarını yüklemek, değiştirmek ve kaydetmek için sınıflara ve yöntemlere erişim sağlar.

Şimdi, degrade dolgu katmanlarını değiştirmenin heyecan verici yolculuğu için kemerlerinizi bağlayın!

## Adım 1: PSD Dosyasını Yükleyin

 Öncelikle değiştirmek istediğiniz degrade dolgu katmanını içeren PSD dosyasını yüklememiz gerekiyor. Şunu kullanın:`Image.load` dosya yolunu belirten yöntem:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

 Bu kod parçacığı, PSD dosyasını belirtilen dizinden yükler ve onu`image` değişken.

## Adım 2: Degrade Dolgu Katmanını Tanımlayın

 PSD dosyaları çok sayıda katman içerebilir. Düzenlemek istediğimiz degrade dolguyu içeren belirli katmanı izole etmemiz gerekiyor. Yineleyin`image.getLayers()` İstenilen katmanı bulmak için dizi:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Burada daha fazla kontrol ve değişiklik yapılacak
   break;
}
}
```

 Bu döngü her katmanı kontrol eder. Eğer bir katman bir`FillLayer` , şuraya döküldü:`FillLayer` yazın ve içine kaydedin`fillLayer`Daha ileri işlemler için değişken. Hedef katmanı tanımlamak için belirli kriterleriniz varsa (örn. katman adı) döngüye ek kontroller ekleyebiliriz.

## 3. Adım: Degrade Dolgu Türünü Doğrulayın

Tüm dolgu katmanları degradeleri kullanmaz. Bu kod parçacığı, tanımlanan katmanın gerçekten de degrade dolgusu içerip içermediğini doğrular:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

 Eğer`getFillType` yöntem geri dönmüyor`FillType.Gradient`, yanlış katmanla çalıştığımızı belirten bir istisna atılır.

## 4. Adım: Degrade Özelliklerine Erişin ve Değiştirin

 Sihir burada gerçekleşiyor! Aspose.PSD, çeşitli degrade dolgu özelliklerine erişim sağlar.`IGradientFillSettings` arayüz. Gerektiğinde bunları alabilir ve değiştirebiliriz:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Özellikleri değiştirin (istenen değerlerle değiştirin)
settings.setAngle(0.0);  // Açıyı 0 dereceye ayarla
settings.setDither(false);  // Titremeyi devre dışı bırak
settings.setAlignWithLayer(true); // Degradeyi katmanla hizalayın
settings.setReverse(true);  // Ters degrade yönü
settings.setHorizontalOffset(25);  // Yatay ofseti ayarla
settings.setVerticalOffset(-15);  // Dikey ofseti ayarla
```

 Bu kod şunu alır:`IGradientFillSettings`nesneyi kullanır ve ardından açı, renk taklidi, hizalama ve uzaklıklar gibi özellikleri değiştirir. Hayal ettiğiniz degrade efektini elde etmek için sağlanan değerleri istediğiniz ayarlarla değiştirin.

## Adım 5: Renk ve Şeffaflık Noktalarını Yönetin

Degradeler, bir spektrum boyunca renk ve şeffaflık noktalarıyla tanımlanır. Aspose.PSD, hassas kontrol için bu noktaları değiştirmenize olanak tanır:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Yeni bir renk noktası ekleyin
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Mevcut bir renk noktasını değiştirme
colorPoints.get(1).setLocation(3000);

// Yeni bir şeffaflık noktası ekleyin
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Mevcut bir şeffaflık noktasını değiştirme
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

## Adım 6: PSD Dosyasını Güncelleyin ve Kaydedin

Gerekli değişiklikleri yaptıktan sonra dolgu katmanını güncelleyin ve PSD dosyasını kaydedin:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

`fillLayer.update()` yöntem, değişiklikleri degrade dolgu katmanına uygular ve`image.save` değiştirilen PSD dosyasını belirtilen çıktı yoluna kaydeder.

## Çözüm

Aspose.PSD for Java'yı kullanarak PSD dosyalarındaki degrade dolgu katmanlarını değiştirme sanatında başarıyla ustalaştınız! Bu adımları izleyerek yaratıcılığınızı serbest bırakabilir ve programatik hassasiyetle çarpıcı görsel efektler oluşturabilirsiniz.

## SSS'ler

### Bir degradeye birden fazla renk ve şeffaflık noktası ekleyebilir miyim?
Kesinlikle! İstediğiniz degrade efektini elde etmek için gerektiği kadar renk ve şeffaflık noktası ekleyebilirsiniz. Sadece yeni noktalar oluşturun ve bunları ilgili listelere ekleyin.

### Bir renk veya şeffaflık noktasını degradeden nasıl kaldırırım?
 Bir noktayı kaldırmak için uygun listenin`remove` Yöntem. Örneğin,`colorPoints.remove(index)` belirtilen dizindeki renk noktasını kaldırır.

### Degrade türünü (doğrusal, radyal vb.) değiştirebilir miyim?
Aspose.PSD şu anda doğrusal degradeleri desteklemektedir. Gelecek sürümlerde diğer degrade türleri desteklense de, renk ve şeffaflık noktalarını yaratıcı bir şekilde işleyerek benzer efektleri elde edebilirsiniz.

### Degradeleri değiştirirken performansa bir etkisi var mı?
Performans etkisi, degradenin karmaşıklığına ve yapılan değişiklik sayısına bağlıdır. Çoğu pratik kullanım durumunda performansın kabul edilebilir olması gerekir. Ancak büyük ölçekli görüntü işlemede kodunuzu verimlilik açısından optimize etmeyi düşünün.

### Bu tekniği bir PSD dosyasındaki birden fazla degrade dolgu katmanına uygulayabilir miyim?
Evet, katmanlar arasında geçiş yapabilir ve değişiklikleri kriterlerinizi karşılayan her degrade dolgu katmanına uygulayabilirsiniz.