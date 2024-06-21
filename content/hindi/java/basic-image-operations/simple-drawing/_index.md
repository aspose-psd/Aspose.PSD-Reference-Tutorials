---
title: जावा के लिए Aspose.PSD के साथ सरल आरेखण करें
linktitle: सरल रेखांकन करें
second_title: Aspose.PSD जावा एपीआई
description: जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में आकृतियाँ बनाना सीखें। यह चरण-दर-चरण मार्गदर्शिका कोड उदाहरणों के साथ बनाना, परतें जोड़ना और चित्र बनाना शामिल करती है।
type: docs
weight: 10
url: /hi/java/basic-image-operations/simple-drawing/
---
## परिचय

जावा के लिए Aspose.PSD का उपयोग करके सरल ड्राइंग करने पर इस चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है! इस ट्यूटोरियल में, हम एक नया PSD दस्तावेज़ बनाने, परतें जोड़ने और विभिन्न रंगों के साथ आकृतियाँ बनाने की मूल बातें जानेंगे। जावा के लिए Aspose.PSD एक शक्तिशाली लाइब्रेरी है जो आपको ग्राफ़िक डिज़ाइन कार्यों के लिए व्यापक कार्यक्षमता प्रदान करते हुए, प्रोग्रामेटिक रूप से PSD फ़ाइलों में हेरफेर करने में सक्षम बनाती है।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- आपकी मशीन पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
-  जावा लाइब्रेरी के लिए Aspose.PSD। आप इसे यहां से डाउनलोड कर सकते हैं[जावा दस्तावेज़ीकरण के लिए Aspose.PSD](https://reference.aspose.com/psd/java/).

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। अपनी जावा फ़ाइल की शुरुआत में निम्नलिखित कोड शामिल करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## चरण 1: एक नया दस्तावेज़ बनाएँ

आइए एक निर्दिष्ट चौड़ाई और ऊंचाई के साथ एक नया PSD दस्तावेज़ बनाकर शुरुआत करें:

```java
//एक्सस्टार्ट: दस्तावेज़ बनाएँ
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd: दस्तावेज़ बनाएँ
```

## चरण 2: एक परत जोड़ें

अब, बिना तर्क वाले कंस्ट्रक्टर का उपयोग करके दस्तावेज़ में एक परत जोड़ें:

```java
//एक्सस्टार्ट: परत जोड़ें
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd: परत जोड़ें
```

## चरण 3: आकृतियाँ बनाएँ

इस चरण में, हम बनाई गई परत पर आकृतियाँ बनाने के लिए ग्राफ़िक्स वर्ग का उपयोग करेंगे:

### पीले रंग से एक आयत बनाएं

```java
//एक्सस्टार्ट: ड्रारेक्टेंगलपीला
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangelYellow
```

### एक लाल आयत बनाएं

```java
//एक्सस्टार्ट: ड्रॉरेडरेक्टेंगल
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangel
```

### एक नीला आयत बनाएं

```java
//एक्सस्टार्ट: ड्राब्लूरेक्टेंगल
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:ड्रॉब्लूरेक्टेंगल
```

## चरण 4: परिवर्तन सहेजें

अंत में, परिवर्तनों सहित लोड की गई PSD फ़ाइल की एक प्रति सहेजें:

```java
//एक्सस्टार्ट: परिवर्तन सहेजें
image.save(outPsdFilePath);
//ExEnd: परिवर्तन सहेजें
```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.PSD का उपयोग करके सफलतापूर्वक सरल ड्राइंग निष्पादित की है। इस ट्यूटोरियल में एक नया दस्तावेज़ बनाना, परतें जोड़ना और विभिन्न रंगों से आयत बनाना शामिल है। अपनी ग्राफ़िक डिज़ाइन आवश्यकताओं के लिए लाइब्रेरी द्वारा दी जाने वाली अधिक उन्नत सुविधाओं का पता लगाने के लिए स्वतंत्र महसूस करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं मौजूदा PSD फ़ाइलों में हेरफेर करने के लिए Java के लिए Aspose.PSD का उपयोग कर सकता हूँ?

A1: हाँ, Java के लिए Aspose.PSD मौजूदा PSD फ़ाइलों को संपादित और हेरफेर करने के लिए व्यापक कार्यक्षमता प्रदान करता है।

### Q2: मुझे जावा के लिए Aspose.PSD के लिए समर्थन कहां मिल सकता है?

 A2: आप यहां जा सकते हैं[जावा फोरम के लिए Aspose.PSD](https://forum.aspose.com/c/psd/34) किसी भी समर्थन-संबंधी प्रश्न के लिए।

### Q3: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, आप नि:शुल्क परीक्षण संस्करण तक पहुंच सकते हैं।[यहाँ](https://releases.aspose.com/).

### Q4: मैं जावा के लिए Aspose.PSD का लाइसेंस कैसे खरीद सकता हूं?

 A4: आप यहां से लाइसेंस खरीद सकते हैं[Aspose.PSD खरीद पृष्ठ](https://purchase.aspose.com/buy).

### Q5: क्या जावा के लिए Aspose.PSD के लिए अस्थायी लाइसेंस उपलब्ध हैं?

 A5: हां, आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).