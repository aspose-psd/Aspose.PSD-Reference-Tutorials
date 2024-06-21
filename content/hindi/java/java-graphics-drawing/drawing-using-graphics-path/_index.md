---
title: जावा में ग्राफ़िक्स पथ का उपयोग करके आरेखण
linktitle: जावा में ग्राफ़िक्स पथ का उपयोग करके आरेखण
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के ग्राफ़िक्स पथ वर्ग का उपयोग करके जावा में जटिल ग्राफ़िक्स बनाने का तरीका जानें। यह ट्यूटोरियल आश्चर्यजनक छवि निर्माण के लिए प्रत्येक चरण में आपका मार्गदर्शन करता है।
type: docs
weight: 19
url: /hi/java/java-graphics-drawing/drawing-using-graphics-path/
---
## परिचय
प्रोग्रामेटिक रूप से छवियां बनाना और उनमें हेरफेर करना जावा डेवलपर्स के लिए एक रोमांचक काम हो सकता है, खासकर जब Aspose.PSD जैसी लाइब्रेरी का उपयोग कर रहे हों। इस ट्यूटोरियल में, हम Aspose.PSD के साथ जावा में ग्राफिक्स पाथ क्लास का उपयोग करके जटिल ग्राफिक्स बनाने की प्रक्रिया के बारे में जानेंगे।
## आवश्यक शर्तें
इससे पहले कि हम कोडिंग भाग में आगे बढ़ें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
1.  जावा डेवलपमेंट किट (जेडीके): आपकी मशीन पर स्थापित जेडीके का एक स्थिर संस्करण। आप इसे यहां से डाउनलोड कर सकते हैं[ओरेकल की साइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  जावा लाइब्रेरी के लिए Aspose.PSD: जावा लाइब्रेरी के लिए Aspose.PSD यहां से डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/). डाउनलोड करने के बाद, JAR फ़ाइल को अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।
3. इंटीग्रेटेड डेवलपमेंट एनवायरनमेंट (आईडीई): चाहे वह एक्लिप्स, इंटेलीजे आईडीईए, या कोई अन्य हो, आपको जावा कोड लिखने और चलाने के लिए एक आईडीई की आवश्यकता होती है।
इन पूर्वावश्यकताओं के साथ, आइए जानें कि ग्राफ़िक्स पथ वर्ग का उपयोग करके दृश्य रूप से आकर्षक छवियां कैसे बनाई जाएं।
## पैकेज आयात करें
आरंभ करने के लिए, आपको आवश्यक पैकेज आयात करने होंगे:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```
ये आयात Aspose.PSD का उपयोग करके छवियों को बनाने और उनमें हेरफेर करने के लिए आवश्यक मुख्य कार्यक्षमता तक पहुंच प्रदान करते हैं।
## चरण 1: छवि और ग्राफ़िक्स आरंभ करें
आरंभ करने के लिए, आइए एक नई छवि सेट करें और एक ग्राफ़िक्स ऑब्जेक्ट प्रारंभ करें:
```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```
यहां, हम ड्राइंग के लिए 500x500 पिक्सेल छवि और एक ग्राफिक ऑब्जेक्ट बनाते हैं।
## चरण 2: ग्राफ़िक्स पथ बनाएं और कॉन्फ़िगर करें
 अगला, हम एक बनाते हैं`GraphicsPath` ड्राइंग पथ को परिभाषित करने के लिए ऑब्जेक्ट:
```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```
इस चरण में, हम अपनी आकृति में एक वृत्त, एक आयत और एक टेक्स्ट लेबल जोड़ रहे हैं और फिर इस आकृति को अपने ग्राफ़िक्स पथ में जोड़ रहे हैं।
## चरण 3: पथ बनाएं और भरें
अब जब हमने अपना पथ परिभाषित कर लिया है, तो हम इसे बना सकते हैं और भर सकते हैं:
```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```
इस चरण में, हम नीले पेन का उपयोग करके पथ बनाते हैं और इसे हैच ब्रश का उपयोग करके ऊर्ध्वाधर हैच पैटर्न से भरते हैं।
## चरण 4: छवि सहेजें
अंत में, छवि को एक फ़ाइल में सहेजें:
```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```
इस अंतिम चरण के साथ, ग्राफ़िक्स पथ का उपयोग करके आपकी छवि निर्माण पूरा हो गया है।
## निष्कर्ष
Aspose.PSD के साथ ग्राफ़िक्स पथ क्लास का उपयोग करके जटिल छवियां बनाना शक्तिशाली और आकर्षक दोनों है। इस गाइड का पालन करके, आप ग्राफ़िकल डिज़ाइन में अपने जावा एप्लिकेशन की क्षमताओं का विस्तार कर सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD क्या है?
Aspose.PSD एक लाइब्रेरी है जो डेवलपर्स को फ़ोटोशॉप फ़ाइलों के साथ काम करने और प्रोग्रामेटिक रूप से छवि परतों में हेरफेर करने की अनुमति देती है।
### क्या मैं PSD के अलावा अन्य प्रारूपों के लिए Aspose.PSD का उपयोग कर सकता हूँ?
इस गाइड के अनुसार, Aspose.PSD विशेष रूप से PSD फ़ाइलों से संबंधित है लेकिन विभिन्न छवि प्रारूपों को संभालने के लिए एक्सटेंशन प्रदान करता है।
### क्या Aspose.PSD के लिए एक परीक्षण संस्करण उपलब्ध है?
 हाँ, आप Aspose.PSD का निःशुल्क परीक्षण प्राप्त कर सकते हैं।[यहाँ](https://releases.aspose.com/).
### मैं Aspose.PSD कैसे खरीद सकता हूँ?
 आप Aspose.PSD से खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
### मुझे Aspose.PSD के लिए समर्थन कहाँ से मिल सकता है?
आप समर्थन और चर्चा की मांग कर सकते हैं[Aspose का मंच](https://forum.aspose.com/c/psd/34).