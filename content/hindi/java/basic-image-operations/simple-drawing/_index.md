---
title: Java के लिए Aspose.PSD के साथ सरल ड्राइंग करें
linktitle: सरल चित्र बनाएं
second_title: Aspose.PSD जावा एपीआई
description: जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में आकृतियाँ बनाना सीखें। यह चरण-दर-चरण मार्गदर्शिका कोड उदाहरणों के साथ परतों को बनाना, जोड़ना और आरेखण करना सिखाती है।
type: docs
weight: 10
url: /hi/java/basic-image-operations/simple-drawing/
---
## परिचय

Aspose.PSD for Java का उपयोग करके सरल ड्राइंग करने के लिए इस चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है! इस ट्यूटोरियल में, हम एक नया PSD दस्तावेज़ बनाने, परतें जोड़ने और विभिन्न रंगों के साथ आकृतियाँ बनाने की मूल बातें जानेंगे। Aspose.PSD for Java एक शक्तिशाली लाइब्रेरी है जो आपको PSD फ़ाइलों को प्रोग्रामेटिक रूप से हेरफेर करने में सक्षम बनाती है, जो ग्राफिक डिज़ाइन कार्यों के लिए व्यापक कार्यक्षमता प्रदान करती है।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- आपकी मशीन पर जावा डेवलपमेंट किट (JDK) स्थापित है।
- Aspose.PSD for Java लाइब्रेरी। आप इसे यहाँ से डाउनलोड कर सकते हैं[Aspose.PSD for Java दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/).

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। अपनी जावा फ़ाइल की शुरुआत में निम्न कोड शामिल करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## चरण 1: नया दस्तावेज़ बनाएँ

आइए एक निर्दिष्ट चौड़ाई और ऊंचाई के साथ एक नया PSD दस्तावेज़ बनाकर शुरू करें:

```java
//एक्सस्टार्ट: क्रिएटडॉक्यूमेंट
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## चरण 2: एक परत जोड़ें

अब, आइए नो-आर्गुमेंट कन्स्ट्रक्टर का उपयोग करके दस्तावेज़ में एक परत जोड़ें:

```java
//एक्सस्टार्ट:एडलेयर
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## चरण 3: आकृतियाँ बनाएँ

इस चरण में, हम बनाई गई परत पर आकृतियाँ बनाने के लिए ग्राफ़िक्स वर्ग का उपयोग करेंगे:

### पीले रंग से एक आयत बनाएं

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### लाल आयत बनाएं

```java
//एक्सस्टार्ट:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### एक नीला आयत बनाएं

```java
//एक्सस्टार्ट:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## चरण 4: परिवर्तन सहेजें

अंत में, परिवर्तनों सहित लोड की गई PSD फ़ाइल की एक प्रतिलिपि सहेजें:

```java
//ExStart:परिवर्तन सहेजें
image.save(outPsdFilePath);
//ExEnd:परिवर्तन सहेजें
```

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके सरल ड्राइंग सफलतापूर्वक की है। इस ट्यूटोरियल में एक नया दस्तावेज़ बनाना, परतें जोड़ना और विभिन्न रंगों के साथ आयत बनाना शामिल है। अपनी ग्राफिक डिज़ाइन आवश्यकताओं के लिए लाइब्रेरी द्वारा दी जाने वाली अधिक उन्नत सुविधाओं का पता लगाने के लिए स्वतंत्र महसूस करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं मौजूदा PSD फ़ाइलों में हेरफेर करने के लिए Java के लिए Aspose.PSD का उपयोग कर सकता हूं?

A1: हां, Aspose.PSD for Java मौजूदा PSD फ़ाइलों को संपादित और हेरफेर करने के लिए व्यापक कार्यक्षमता प्रदान करता है।

### प्रश्न 2: मैं Java के लिए Aspose.PSD का समर्थन कहां पा सकता हूं?

 A2: आप यहां जा सकते हैं[Aspose.PSD for Java फ़ोरम](https://forum.aspose.com/c/psd/34) किसी भी सहायता-संबंधी प्रश्नों के लिए.

### प्रश्न 3: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A3: हां, आप निःशुल्क परीक्षण संस्करण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 4: मैं Java के लिए Aspose.PSD का लाइसेंस कैसे खरीद सकता हूं?

 A4: आप यहाँ से लाइसेंस खरीद सकते हैं[Aspose.PSD खरीद पृष्ठ](https://purchase.aspose.com/buy).

### प्रश्न 5: क्या Java के लिए Aspose.PSD हेतु अस्थायी लाइसेंस उपलब्ध हैं?

 A5: हाँ, आप यहाँ से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).