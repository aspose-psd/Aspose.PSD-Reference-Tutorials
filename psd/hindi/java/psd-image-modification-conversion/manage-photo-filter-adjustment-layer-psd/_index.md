---
title: PSD में फोटो फिल्टर समायोजन परत प्रबंधित करें - जावा
linktitle: PSD में फोटो फिल्टर समायोजन परत प्रबंधित करें - जावा
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java के साथ PSD फ़ाइलों में फ़ोटो फ़िल्टर एडजस्टमेंट लेयर्स को प्रबंधित करना सीखें। आसानी से संपादन और फ़िल्टर जोड़ने के लिए इस गाइड का पालन करें।
weight: 24
url: /hi/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में फोटो फिल्टर समायोजन परत प्रबंधित करें - जावा

## परिचय
क्या आप एक डेवलपर हैं जो Java का उपयोग करके अपनी ग्राफिक संपादन क्षमताओं को बढ़ाना चाहते हैं? खैर, आप सही जगह पर हैं! आज, हम Java के लिए Aspose.PSD का उपयोग करके फ़ोटो फ़िल्टर समायोजन परतों को प्रबंधित करने के तरीके के बारे में जानेंगे। यह शक्तिशाली लाइब्रेरी आपको PSD फ़ाइलों को सहजता से हेरफेर करने में सक्षम बनाती है, जिससे ग्राफिक डिज़ाइन में एक कुशल वर्कफ़्लो की अनुमति मिलती है। चाहे आप प्रभाव जोड़ना चाहते हों या मौजूदा परतों को संपादित करना चाहते हों, हमने आपको एक चरण-दर-चरण मार्गदर्शिका दी है जो प्रक्रिया को सरल बनाती है।
## आवश्यक शर्तें
इससे पहले कि हम इस यात्रा पर निकलें, आइए सुनिश्चित करें कि आपके पास वह सब कुछ है जो आपको चाहिए:
### आवश्यक सॉफ्टवेयर
1.  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके मशीन पर JDK का संगत संस्करण स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं[ओरेकल की वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java: PSD फ़ाइलों में हेरफेर करने के लिए, आपको Aspose.PSD लाइब्रेरी की आवश्यकता होगी। आप इसे यहाँ से डाउनलोड कर सकते हैं[Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/) इसे देखना न भूलें[Aspose दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/) अधिक जानकारी के लिए.
3. आईडीई (एकीकृत विकास पर्यावरण): इंटेलीज आईडीईए या एक्लिप्स जैसा एक अच्छा आईडीई आपके कोडिंग अनुभव को आसान बना देगा।
### मूल बातें समझना
जावा प्रोग्रामिंग से परिचित होना और PSD फ़ाइलें कैसे काम करती हैं, इसकी बुनियादी समझ फ़ायदेमंद होगी। यदि आप जावा में लाइब्रेरीज़ का उपयोग करने में नए हैं, तो फ़्रेमवर्क को आयात करने और उपयोग करने की आदत डालना एक अच्छा विचार है।
## पैकेज आयात करें
आरंभ करने के लिए, हमें Aspose.PSD लाइब्रेरी से आवश्यक क्लासेस आयात करने की आवश्यकता है। यहाँ एक सरल आयात कथन है जिसकी आपको अपनी जावा फ़ाइल की शुरुआत में आवश्यकता होगी:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
बस इसे अपनी जावा फ़ाइल के शीर्ष पर चिपकाएं, और आप PSD छवियों के साथ काम करना शुरू करने के लिए तैयार हैं!
## मौजूदा फोटो फ़िल्टर परत का संपादन
### चरण 1: डेटा निर्देशिका सेट करें
 सबसे पहले, आपको उस डायरेक्टरी को परिभाषित करना होगा जहाँ आपकी PSD फ़ाइलें संग्रहीत हैं।`"Your Document Directory"` वास्तविक पथ के साथ। इस तरह आप सब कुछ व्यवस्थित कर सकते हैं:
```java
String dataDir = "Your Document Directory";
```
### चरण 2: अपनी PSD फ़ाइल लोड करें
 अब, उस PSD फ़ाइल को लोड करें जिसे आप संपादित करना चाहते हैं। सुनिश्चित करें कि`PhotoFilterAdjustmentLayer.psd`आपके निर्दिष्ट निर्देशिका में मौजूद है.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```
### चरण 3: छवि ऑब्जेक्ट को आरंभ करें
Aspose की अंतर्निहित कार्यक्षमता का उपयोग करके, हम छवि को अपने प्रोजेक्ट में लोड करते हैं:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
### चरण 4: परतों के माध्यम से पुनरावृति करें
 आगे, हम PSD फ़ाइल के अंदर परतों की जांच करेंगे। हमारा लक्ष्य है कि हम उन परतों का पता लगाएँ जो PSD फ़ाइल में हैं।`PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // परत में परिवर्तन करें
    }
}
```
### चरण 5: फोटो फ़िल्टर परत को अनुकूलित करें
 यहाँ जादू होता है! आप इसे संशोधित कर सकते हैं`Color` और`Density`उदाहरण के लिए, हम रंग को जीवंत लाल रंग में सेट कर सकते हैं और घनत्व को समायोजित कर सकते हैं:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```
### चरण 6: संपादित PSD फ़ाइल को सहेजें
अंत में, अपने समायोजनों के साथ एक नई PSD फ़ाइल बनाने के लिए परिवर्तनों को सहेजें:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
आपने अभी-अभी PSD फ़ाइल में एक फोटो फ़िल्टर समायोजन परत संपादित की है।
## नई फोटो फ़िल्टर परत जोड़ना
### चरण 1: निर्देशिका पथ सेट करें
पहले की तरह, हम अपनी डेटा निर्देशिका को परिभाषित करने से शुरू करते हैं:
```java
String dataDir = "Your Document Directory";
```
### चरण 2: स्रोत फ़ाइल लोड करें
इस उदाहरण के लिए, आइए एक अलग PSD फ़ाइल लोड करें जहां हम एक नया फोटो फ़िल्टर जोड़ना चाहते हैं:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```
### चरण 3: छवि ऑब्जेक्ट को पुनः आरंभ करें
 हमें एक नया निर्माण करना होगा`PsdImage` उदाहरण, इसलिए हम फ़ाइल लोड करते हैं:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
### चरण 4: फ़ोटो फ़िल्टर परत जोड़ें
अब, हम कस्टमाइज़्ड रंग के साथ एक नई फोटो फ़िल्टर परत जोड़ सकते हैं। यह इस प्रकार किया जाता है:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```
### चरण 5: नई PSD फ़ाइल सहेजें
एक बार फिर, हमारे बदलावों को सहेजने का समय आ गया है। ऐसा करने के लिए यह लाइन है:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
आपने अपनी PSD फ़ाइल में एक नई फोटो फ़िल्टर परत सफलतापूर्वक जोड़ ली है।
## निष्कर्ष
Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में फ़ोटो फ़िल्टर समायोजन परतों को प्रबंधित करना न केवल सरल है, बल्कि ग्राफ़िक संपादन के लिए संभावनाओं की एक दुनिया भी खोलता है। इन चरण-दर-चरण मार्गदर्शिकाओं का पालन करके, आप अपनी PSD फ़ाइलों को जीवंत फ़िल्टर के साथ बढ़ा सकते हैं और शानदार ग्राफ़िक्स बना सकते हैं। अपने अनुप्रयोगों में इन कार्यक्षमताओं का परीक्षण करें; आप निश्चित रूप से इसे अपनी परियोजनाओं के लिए कुशल पाएंगे!
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD क्या है?
Aspose.PSD PSD फ़ाइलें बनाने, संपादित करने और परिवर्तित करने के लिए एक .NET और Java लाइब्रेरी है।
### क्या मैं Aspose.PSD को निःशुल्क आज़मा सकता हूँ?
 हां, Aspose एक निःशुल्क परीक्षण संस्करण प्रदान करता है। इसे देखें[यहाँ](https://releases.aspose.com/).
### मैं दस्तावेज़ कहां पा सकता हूं?
 आप संपूर्ण दस्तावेज़ यहां पा सकते हैं[Aspose का संदर्भ पृष्ठ](https://reference.aspose.com/psd/java/).
### मैं Aspose.PSD कैसे खरीद सकता हूं?
 आप यह सॉफ्टवेयर यहाँ से खरीद सकते हैं[इस लिंक](https://purchase.aspose.com/buy).
### क्या Aspose.PSD के लिए समर्थन उपलब्ध है?
 बिल्कुल! आप Aspose सहायता फ़ोरम के माध्यम से सहायता प्राप्त कर सकते हैं[यहाँ](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
