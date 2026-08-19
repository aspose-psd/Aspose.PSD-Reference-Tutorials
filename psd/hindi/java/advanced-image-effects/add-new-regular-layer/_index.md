---
date: 2026-04-08
description: जानेँ कि Aspose.PSD for Java का उपयोग करके अस्थायी लाइसेंस के साथ PSD
  को PNG में कैसे निर्यात करें और नया PSD लेयर कैसे बनाएं। यह चरण‑दर‑चरण ट्यूटोरियल
  PSD इमेज मैनिपुलेशन और लेयर की स्थिति सेट करने को कवर करता है।
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: PSD में नया नियमित लेयर जोड़ें
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java का उपयोग करके PSD को PNG में निर्यात करें और नया नियमित
  लेयर जोड़ें – अस्पोज़ अस्थायी लाइसेंस
url: /hi/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java का उपयोग करके PSD को PNG में निर्यात करें और एक नया नियमित लेयर जोड़ें

## परिचय

इस **aspose psd tutorial** में आप सीखेंगे कि कैसे **export PSD to PNG** करते हुए उसी फ़ाइल में **creating a new regular layer** किया जा सकता है, **using an aspose temporary license** विकास के लिए। चाहे आपको वेब‑तैयार थंबनेल बनाना हो, डिज़ाइन पाइपलाइन के लिए एसेट तैयार करना हो, या बस **psd image manipulation** के साथ प्रयोग करना हो, Aspose.PSD for Java आपको पूर्ण प्रोग्रामेटिक नियंत्रण देता है। हम हर कदम से गुजरेंगे—स्रोत फ़ाइल लोड करने से लेकर अपडेटेड PSD और PNG कॉपी दोनों को सहेजने तक—ताकि आप तुरंत PSD लेयर्स को मैनिपुलेट करना शुरू कर सकें।

## त्वरित उत्तर
- **क्या मैं एक कॉल से PSD को PNG में निर्यात कर सकता हूँ?** हाँ, लेयर्स जोड़ने के बाद आप `save` को `PngOptions` के साथ कॉल कर सकते हैं।
- **क्या विकास के लिए मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक temporary license काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।
- **कौन सा Java संस्करण समर्थित है?** Aspose.PSD Java 8 और उसके बाद के संस्करणों के साथ काम करता है।
- **क्या लेयर पोजिशनिंग पिक्सेल‑आधारित है?** हाँ, आप **set layer position** मेथड्स का उपयोग करके पिक्सेल में left, top, right, bottom निर्देशांक सेट करते हैं।
- **क्या PNG लेयर ट्रांसपैरेंसी को बनाए रखेगा?** PNG सभी दृश्यमान लेयर्स के मर्ज्ड परिणाम को शामिल करेगा।

## क्यों उपयोग करें aspose temporary license?

एक **aspose temporary license** आपको Aspose.PSD की पूरी फीचर सेट का मूल्यांकन बिना किसी कार्यात्मक प्रतिबंध के करने देता है। यह मूल्यांकन वॉटरमार्क को हटाता है, सभी APIs को अनलॉक करता है—जिसमें **create new psd layer** ऑब्जेक्ट बनाने की क्षमता शामिल है—और आपको स्थायी लाइसेंस खरीदने से पहले प्रोडक्शन‑जैसे वातावरण में अपना कोड टेस्ट करने की अनुमति देता है।

## आवश्यकताएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Java Development Environment** – JDK 8+ और एक बिल्ड टूल (Maven/Gradle) स्थापित हो।
- **Aspose.PSD for Java** – आधिकारिक साइट [here](https://releases.aspose.com/psd/java/) से नवीनतम JAR डाउनलोड करें।
- **A sample PSD file** – हम उदाहरणों में `OneLayer.psd` का उपयोग करेंगे।

## पैकेज इम्पोर्ट करें

अपने Java क्लास में आवश्यक इम्पोर्ट्स जोड़ें। ये क्लासेज **psd image manipulation** और लेयर हैंडलिंग के लिए कोर फ़ंक्शनैलिटी प्रदान करती हैं।

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position” क्या है और यह क्यों महत्वपूर्ण है?

जब आप एक नया लेयर जोड़ते हैं, तो आपको यह निर्धारित करना होता है कि वह कैनवास पर कहाँ दिखाई देगा। मेथड्स `setLeft`, `setTop`, `setRight`, और `setBottom` पिक्सेल कोऑर्डिनेट्स में **set layer position** सेट करते हैं। सही पोजिशनिंग यह सुनिश्चित करती है कि आपके ग्राफिक्स ठीक उसी जगह पर हों जहाँ आप चाहते हैं, जो UI एसेट्स को कॉम्पोज़िट करने या प्रिंट‑रेडी फ़ाइलें तैयार करने जैसे कार्यों के लिए अत्यंत महत्वपूर्ण है।

## चरण‑दर‑चरण गाइड

### चरण 1: PSD फ़ाइल लोड करें

पहले, उस मौजूदा PSD को लोड करें जिसे आप संशोधित करना चाहते हैं। यह आपको एक `PsdImage` ऑब्जेक्ट देता है जिससे आप काम कर सकते हैं।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### चरण 2: पिक्सेल डेटा और आयतें तैयार करें

हम दो पिक्सेल बफ़र (`int[]`) बनाएँगे और उन आयताकार क्षेत्रों को परिभाषित करेंगे जहाँ नए लेयर्स पेंट किए जाएंगे। यह **creating a new psd layer** की नींव है।

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### चरण 3: लेयर डेटा प्रारंभ करें

पिक्सेल बफ़र को एक डिफ़ॉल्ट ARGB मान से भरें। मान `-10000000` एक अर्द्ध‑पारदर्शी गहरे शेड के अनुरूप है।

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### चरण 4: नियमित लेयर्स जोड़ें (PSD लेयर्स को मैनिपुलेट करें)

अब हम PSD इमेज में **add regular layers** जोड़ते हैं और left, top, right, और bottom प्रॉपर्टीज़ का उपयोग करके **set layer position** सेट करते हैं। यह दर्शाता है कि कैसे **manipulate PSD layers** को प्रोग्रामेटिक रूप से किया जाता है।

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### चरण 5: PSD को PNG में निर्यात करें और अपडेटेड PSD सहेजें

लेयर्स स्थापित होने के बाद, संशोधित दस्तावेज़ को सहेजें। पहले हम परिणाम को PNG में निर्यात करते हैं (**export psd to png** चरण), फिर हम नए लेयर्स के साथ PSD को स्थायी रूप से सहेजते हैं।

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** यदि आपको केवल PNG चाहिए, तो आप PSD `save` कॉल को छोड़ सकते हैं और सीधे `save` को `PngOptions` के साथ invoke कर सकते हैं।

## सामान्य समस्याएँ और ट्रबलशूटिंग

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| PNG खाली दिख रहा है | लेयर्स अदृश्य या पूरी तरह से पारदर्शी हैं | सुनिश्चित करें कि आप गैर‑पारदर्शी पिक्सेल मान सेट करें या `layer.setVisible(true)` कॉल करें। |
| `ArrayIndexOutOfBoundsException` | आयत आकार और पिक्सेल एरे लंबाई में असंगति | सुनिश्चित करें कि `rect.width * rect.height == dataArray.length` है। |
| रनटाइम पर LicenseException | कोई वैध लाइसेंस लोड नहीं किया गया | किसी भी API मेथड को कॉल करने से पहले एक temporary या permanent लाइसेंस लोड करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.PSD Java 8 के साथ संगत है?**  
A: हाँ, Aspose.PSD Java 8 और बाद के संस्करणों का समर्थन करता है।

**Q: क्या मैं जोड़े गए लेयर्स पर ट्रांसफ़ॉर्मेशन (घुमाना, स्केल) लागू कर सकता हूँ?**  
A: बिल्कुल! `Layer` क्लास `rotate`, `scale`, और `translate` जैसे मेथड्स प्रदान करती है पूर्ण ट्रांसफ़ॉर्मेशन नियंत्रण के लिए।

**Q: अतिरिक्त Aspose.PSD दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: विस्तृत API दस्तावेज़ [here](https://reference.aspose.com/psd/java/) पर उपलब्ध हैं।

**Q: Aspose.PSD के लिए temporary license कैसे प्राप्त करें?**  
A: temporary‑license पेज पर जाएँ [here](https://purchase.aspose.com/temporary-license/)।

**Q: Aspose.PSD समर्थन के लिए कोई कम्युनिटी फ़ोरम हैं?**  
A: हाँ, Aspose फ़ोरम पर चर्चा में शामिल हों [here](https://forum.aspose.com/c/psd/34)।

## निष्कर्ष

अब आपने सीखा है कि कैसे Aspose.PSD for Java का उपयोग करके **export PSD to PNG** किया जाता है जबकि **adding new regular layers** किया जाता है, और आपने देखा कि कैसे एक **aspose temporary license** आपको इस वर्कफ़्लो को बिना किसी प्रतिबंध के आज़माने की अनुमति देता है। यह ट्यूटोरियल मुख्य **psd image manipulation** क्षमताओं को दर्शाता है: फ़ाइल लोड करना, लेयर्स बनाना, पिक्सेल डेटा भरना, और अंतिम कंपोज़िशन को निर्यात करना। विभिन्न आयत आकारों, पिक्सेल रंगों, या लेयर इफ़ेक्ट्स के साथ प्रयोग करने में संकोच न करें ताकि आउटपुट को अपने प्रोजेक्ट की आवश्यकताओं के अनुसार अनुकूलित कर सकें।

---

**अंतिम अपडेट:** 2026-04-08  
**परीक्षण किया गया:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}