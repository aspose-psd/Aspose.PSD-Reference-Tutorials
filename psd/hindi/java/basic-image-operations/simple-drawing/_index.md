---
date: 2026-06-13
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में rectangle कैसे बनाएं,
  सीखें। यह गाइड step‑by‑step code, layers जोड़ना, server‑side image processing और
  shape drawing दिखाता है।
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: सरल ड्राइंग
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ PSD में Rectangle कैसे बनाएं
url: /hi/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में आयत कैसे बनाएं Aspose.PSD for Java के साथ

## परिचय

इस ट्यूटोरियल में आप Photoshop PSD फ़ाइल के भीतर **आयत कैसे बनाएं** आकार को शुद्ध‑Java Aspose.PSD लाइब्रेरी का उपयोग करके खोजेंगे। चाहे आप सर्वर‑साइड एसेट पाइपलाइन बना रहे हों, थंबनेल निर्माण को स्वचालित कर रहे हों, या मौजूदा डिज़ाइनों में गतिशील ग्राफ़िक्स जोड़ रहे हों, नीचे दिए गए चरण आपको एक पूर्ण, प्रोडक्शन‑रेडी समाधान प्रदान करते हैं। हम एक नया PSD दस्तावेज़ बनाना, लेयर जोड़ना, पृष्ठभूमि साफ़ करना, और अंत में लाल और नीली दोनों आयतें बनाना—बिना Photoshop लॉन्च किए—को कवर करेंगे।

## त्वरित उत्तर
- **PSD फ़ाइल बनाने के लिए मुख्य क्लास कौन सी है?** `PsdImage`
- **कौन सा मेथड लेयर की पृष्ठभूमि रंग को साफ़ करता है?** `Graphics.clear(Color)`
- **लाल आयत कैसे बनाते हैं?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **क्या विकास के लिए लाइसेंस की आवश्यकता है?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।
- **क्या मैं उसी API से मौजूदा PSD फ़ाइलों को संशोधित कर सकता हूँ?** हाँ, Aspose.PSD पूर्ण PSD संपादन का समर्थन करता है।

## PSD फ़ाइल में लाल आयत बनाना क्या है?

लाल आयत बनाना का अर्थ है `Graphics` ऑब्जेक्ट का उपयोग करके PSD छवि की किसी विशिष्ट लेयर पर लाल रंग से भरी या रूपरेखा वाली आयताकार आकृति बनाना। यह ऑपरेशन क्षेत्रों को हाइलाइट करने, प्लेसहोल्डर बनाने, या प्रोग्रामेटिक रूप से सरल ग्राफ़िक्स जोड़ने के लिए सामान्य है।

## PSD फ़ाइलों को संभालने के लिए Aspose.PSD for Java का उपयोग क्यों करें?

Aspose.PSD for Java **50+ इनपुट और आउटपुट फ़ॉर्मेट** का समर्थन करता है, पूरी फ़ाइल को मेमोरी में लोड किए बिना कई‑सौ पृष्ठों वाली PSD फ़ाइलों को प्रोसेस कर सकता है, और किसी भी प्लेटफ़ॉर्म पर चलता है जो Java 8 या उससे ऊपर का समर्थन करता है। इसका सर्वर‑साइड इमेज प्रोसेसिंग इंजन Photoshop की आवश्यकता को समाप्त करता है, लाइसेंसिंग लागत को कम करता है, और एक साधारण VM पर प्रति घंटे **10 GB** इमेज डेटा संभालने वाले स्वचालित वर्कफ़्लो को सक्षम करता है।

## पूर्वापेक्षाएँ

- आपके मशीन पर Java Development Kit (JDK) 8 या बाद का स्थापित हो।
- Aspose.PSD for Java लाइब्रेरी। आप इसे [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) से डाउनलोड कर सकते हैं।

## पैकेज आयात करें

`import` स्टेटमेंट आवश्यक क्लासेज़ को स्कोप में लाते हैं ताकि आप PSD इमेज, लेयर्स, रंग और ग्राफ़िक्स के साथ काम कर सकें।

`PsdImage` क्लास Aspose.PSD का टॉप‑लेवल ऑब्जेक्ट है जो मेमोरी में एकल PSD फ़ाइल का प्रतिनिधित्व करता है।  
`Graphics` रेखाएँ, आयत और दीर्घवृत्त जैसी ड्राइंग प्रिमिटिव्स प्रदान करता है।  
`Color` और `Pen` आपको स्ट्रोक रंग और मोटाई निर्दिष्ट करने देते हैं।  
`Layer` क्लास PSD दस्तावेज़ के भीतर एक व्यक्तिगत इमेज लेयर का प्रतिनिधित्व करता है।  
`Rectangle` क्लास ड्राइंग ऑपरेशनों के लिए उपयोग किए जाने वाले आयताकार क्षेत्र की स्थिति और आकार को परिभाषित करता है।  
`SolidBrush` क्लास आकारों को ठोस रंग से भरता है।

## PSD दस्तावेज़ बनाने का पहला कदम क्या है?

आप `PsdImage` को कैनवास की चौड़ाई और ऊँचाई पिक्सेल में प्रदान करके इंस्टैंसिएट करते हैं, जिससे एक खाली PSD फ़ाइल संरचना बनती है। प्रारंभिक लेयर्स या पृष्ठभूमि सेट करने के बाद, दस्तावेज़ को डिस्क पर लिखने के लिए `save` मेथड को फ़ाइल पाथ के साथ कॉल करें। यह इमेज को आगे के संपादन ऑपरेशनों के लिए तैयार करता है।

## चरण 1: नया दस्तावेज़ बनाएं

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## PSD छवि में नई खाली लेयर कैसे जोड़ें?

पहले, पैरेंट `PsdImage` के समान चौड़ाई और ऊँचाई के साथ एक नया `Layer` इंस्टेंस बनाएं। फिर `add` मेथड का उपयोग करके इस लेयर को इमेज की `Layers` कलेक्शन में जोड़ें। एक बार लेयर इमेज का हिस्सा बन जाने के बाद, ड्राइंग ऑपरेशनों को करने के लिए उसका `Graphics` ऑब्जेक्ट प्राप्त करें; इस चरण के बिना ड्रॉइंग दिखाई नहीं देगा।

## चरण 2: लेयर जोड़ें

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## लेयर की पृष्ठभूमि रंग को साफ़ करने का उद्देश्य क्या है?

`Graphics.clear` को एक विशिष्ट `Color` के साथ कॉल करने से पूरी लेयर उस रंग से भर जाती है, जिससे सभी पिक्सेल डेटा प्रभावी रूप से रीसेट हो जाता है। यह सुनिश्चित करता है कि कोई भी पूर्व सामग्री हटाई गई है और लेयर ज्ञात पृष्ठभूमि से शुरू होती है, जिससे बाद में Photoshop में PSD खोलने या संपादित करने पर अप्रत्याशित ट्रांसपेरेंसी या रंग मिश्रण से बचा जा सके।

## चरण 3: आकार बनाएं

हम `Graphics` क्लास का उपयोग करके लेयर के पिक्सेल डेटा को बदलेंगे। नीचे तीन उदाहरण हैं जो पृष्ठभूमि साफ़ करने और विभिन्न रंगों की आयतें बनाने को दर्शाते हैं।

### लेयर रंग साफ़ करें (पृष्ठभूमि को पीला सेट करें)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### लाल आयत बनाएं (मुख्य फोकस)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### नीली आयत बनाएं (अतिरिक्त उदाहरण)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## संपादित PSD फ़ाइल को डिस्क पर कैसे सहेजें?

`PsdImage` ऑब्जेक्ट पर `save` मेथड का उपयोग करें, पूर्ण फ़ाइल पाथ पास करें और वैकल्पिक रूप से इच्छित इमेज फ़ॉर्मेट (डिफ़ॉल्ट रूप से PSD) निर्दिष्ट करें। यह सभी लेयर्स, मास्क और ड्रॉइंग कमांड्स को एकल PSD फ़ाइल में लिखता है जो Photoshop स्पेसिफिकेशन के अनुरूप है, जिससे इसे बिना चेतावनी के खोला जा सकता है।

## चरण 4: परिवर्तन सहेजें

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## सामान्य समस्याएँ और समाधान

- **ड्रॉइंग के बाद लेयर दिखाई नहीं दे रही है:** सुनिश्चित करें कि लेयर को `Graphics` ऑब्जेक्ट बनाने **से पहले** इमेज में जोड़ा गया है। ड्रॉइंग सतह को एक वैध लेयर से जुड़ा होना चाहिए।
- **रंग गलत दिख रहे हैं:** जांचें कि आप `Color.getRed()` (या `Color.getBlue()`) का उपयोग कर रहे हैं, न कि ऐसा कस्टम RGB मान बना रहे हैं जो 0‑255 रेंज से अधिक हो।
- **फ़ाइल सहेजी नहीं गई:** पुष्टि करें कि `outputDir` पाथ मौजूद है और एप्लिकेशन के पास लिखने की अनुमति है। Linux पर, आपको फ़ोल्डर की स्वामित्व समायोजित करने या `Files.createDirectories` का उपयोग करने की आवश्यकता हो सकती है।
- **बड़ी फ़ाइलों पर प्रदर्शन में गिरावट:** केवल आवश्यक चैनल लोड करने के लिए `PsdImage` की `setLoadOptions` का उपयोग करें, जिससे 200 MB से बड़ी PSDs के लिए मेमोरी खपत कम हो जाती है।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं Aspose.PSD for Java का उपयोग करके मौजूदा PSD फ़ाइलों को संशोधित कर सकता हूँ?**  
A1: हाँ, Aspose.PSD for Java मौजूदा PSD फ़ाइलों को संपादित और संशोधित करने के लिए व्यापक कार्यक्षमता प्रदान करता है, जिसमें लेयर पुनः क्रमबद्ध करना, मास्क समायोजन और वेक्टर ड्रॉइंग शामिल हैं।

**Q2: Aspose.PSD for Java के लिए समर्थन कहाँ मिल सकता है?**  
A2: आप समुदाय‑आधारित सहायता और आधिकारिक Aspose उत्तरों के लिए [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) पर जा सकते हैं।

**Q3: क्या Aspose.PSD for Java के लिए मुफ्त ट्रायल उपलब्ध है?**  
A3: हाँ, आप मुफ्त ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) से एक्सेस कर सकते हैं। ट्रायल में सभी फीचर शामिल हैं लेकिन सहेजी गई फ़ाइलों में वॉटरमार्क जोड़ता है।

**Q4: Aspose.PSD for Java के लिए लाइसेंस कैसे खरीदें?**  
A4: आप लाइसेंस [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) से खरीद सकते हैं। लाइसेंस विकल्पों में स्थायी, सब्सक्रिप्शन और साइट लाइसेंस शामिल हैं।

**Q5: क्या Aspose.PSD for Java के लिए अस्थायी लाइसेंस उपलब्ध हैं?**  
A5: हाँ, आप अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं आयत के अलावा अन्य आकार भी बना सकता हूँ?**  
A: हाँ, `Graphics` क्लास `drawPath` मेथड के माध्यम से दीर्घवृत्त, रेखाएँ और कस्टम पाथ ड्रॉ करने का भी समर्थन करता है।

**Q: क्या Aspose.PSD ड्रॉ किए गए आकारों में पारदर्शिता का समर्थन करता है?**  
A: बिल्कुल; आप `SolidBrush` को ARGB रंग के साथ उपयोग करके अल्फा पारदर्शिता शामिल कर सकते हैं, जिससे अर्ध‑पारदर्शी ओवरले सक्षम होते हैं।

**Q: क्या लेयर की अपारदर्शिता (opacity) को संपादित करना संभव है?**  
A: हाँ, प्रत्येक `Layer` ऑब्जेक्ट में `setOpacity` मेथड है जो 0 से 255 तक का मान लेता है, जिससे लेयर की पारदर्शिता पर सूक्ष्म नियंत्रण मिलता है।

**Q: नया बनाने के बजाय मौजूदा PSD फ़ाइल को कैसे लोड करें?**  
A: लेयर्स को संशोधित करने से पहले `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` का उपयोग करें। लोड की गई इमेज सभी मूल लेयर्स और मास्क को बरकरार रखती है।

## निष्कर्ष

आपने अब Aspose.PSD for Java का उपयोग करके PSD फ़ाइल के भीतर **आयत कैसे बनाएं** आकार और लेयर्स को संभालना पूरी तरह से सीख लिया है। एक दस्तावेज़ बनाकर, लेयर जोड़कर, उसकी पृष्ठभूमि साफ़ करके, और `Graphics` API से ड्रॉ करके, आप सर्वर‑साइड पर अनगिनत ग्राफ़िक‑डिज़ाइन कार्यों को स्वचालित कर सकते हैं। विभिन्न पेन, ब्रश और लेयर इफ़ेक्ट्स के साथ प्रयोग करें ताकि इस आधार को पूर्ण‑फ़ीचर इमेज जेनरेशन पाइपलाइन में विस्तारित किया जा सके।

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Java में आकार कैसे बनाएं – बेसिक इमेज ऑपरेशन्स](/psd/java/basic-image-operations/)
- [Aspose.PSD के साथ सरल रिसाइज़िंग – Java इमेज मैनिपुलेशन लाइब्रेरी](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java में आयत द्वारा इमेज क्रॉप करें](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**अंतिम अपडेट:** 2026-06-13  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**लेखक:** Aspose