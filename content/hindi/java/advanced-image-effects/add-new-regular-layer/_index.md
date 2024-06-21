---
title: जावा के लिए Aspose.PSD के साथ PSD में एक नई नियमित परत जोड़ें
linktitle: PSD में एक नई नियमित परत जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में एक नई नियमित परत जोड़ने का तरीका जानें। निर्बाध PSD हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/java/advanced-image-effects/add-new-regular-layer/
---
## परिचय

PSD फ़ाइल में एक नई नियमित परत जोड़ने के लिए जावा के लिए Aspose.PSD का उपयोग करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। Aspose.PSD एक शक्तिशाली जावा लाइब्रेरी है जो डेवलपर्स को PSD फ़ाइलों के साथ कुशलतापूर्वक हेरफेर करने और काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको PSD फ़ाइल में एक नई नियमित परत जोड़ने की प्रक्रिया में मार्गदर्शन करेंगे, विस्तृत चरण और कोड उदाहरण प्रदान करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- जावा विकास वातावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा विकास वातावरण स्थापित है।
-  Aspose.PSD लाइब्रेरी: जावा लाइब्रेरी के लिए Aspose.PSD डाउनलोड और इंस्टॉल करें। आप पुस्तकालय पा सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। Aspose.PSD कार्यक्षमताओं के साथ काम करने के लिए ये पैकेज आवश्यक हैं। अपनी जावा फ़ाइल की शुरुआत में निम्नलिखित पंक्तियाँ शामिल करें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## चरण 1: PSD फ़ाइल लोड करें

निम्नलिखित कोड का उपयोग करके वह PSD फ़ाइल लोड करें जिसे आप संपादित करना चाहते हैं:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## चरण 2: डेटा सारणी और आयत तैयार करें

इस प्रकार दो पूर्णांक सरणियाँ और दो आयत वस्तुएँ तैयार करें:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## चरण 3: परत डेटा प्रारंभ करें

डिफ़ॉल्ट मान के साथ डेटा सारणी प्रारंभ करें:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## चरण 4: नियमित परतें जोड़ें

PSD छवि में दो नियमित परतें जोड़ें:

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

## चरण 5: PSD और PNG सहेजें

संशोधित PSD और एक अतिरिक्त PNG फ़ाइल सहेजें:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

बधाई हो! आपने जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइल में सफलतापूर्वक एक नई नियमित परत जोड़ दी है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइल में एक नई नियमित परत जोड़ने की प्रक्रिया को कवर किया। यह शक्तिशाली लाइब्रेरी PSD हेरफेर को सरल बनाती है, जिससे यह जावा डेवलपर्स के लिए सुलभ हो जाती है। Aspose.PSD की पूरी क्षमता का पता लगाने के लिए विभिन्न मापदंडों और कार्यात्मकताओं के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD जावा 8 के साथ संगत है?

A1: हाँ, Aspose.PSD Java 8 और बाद के संस्करणों का समर्थन करता है।

### Q2: क्या मैं अतिरिक्त परतों में परिवर्तन लागू कर सकता हूँ?

ए2: बिल्कुल! Aspose.PSD परतों के लिए परिवर्तन विकल्पों की एक श्रृंखला प्रदान करता है।

### Q3: मुझे अतिरिक्त Aspose.PSD दस्तावेज़ कहां मिल सकते हैं?

 A3: आप दस्तावेज़ का संदर्भ ले सकते हैं।[यहाँ](https://reference.aspose.com/psd/java/).

### Q4: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 ए4: विजिट करें[इस लिंक](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस विकल्पों के लिए.

### Q5: क्या Aspose.PSD समर्थन के लिए कोई सामुदायिक मंच हैं?

 A5: हाँ, आप समर्थन और चर्चाएँ पा सकते हैं।[यहाँ](https://forum.aspose.com/c/psd/34).