---
title: जावा में ग्राफ़िक्स पथ का उपयोग करके आरेखण
linktitle: जावा में ग्राफ़िक्स पथ का उपयोग करके आरेखण
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के Graphics Path क्लास का उपयोग करके Java में जटिल ग्राफ़िक्स बनाना सीखें। यह ट्यूटोरियल आपको शानदार इमेज बनाने के प्रत्येक चरण के बारे में बताता है।
weight: 19
url: /hi/java/java-graphics-drawing/drawing-using-graphics-path/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में ग्राफ़िक्स पथ का उपयोग करके आरेखण

## परिचय
जावा डेवलपर्स के लिए प्रोग्रामेटिक रूप से इमेज बनाना और उनमें हेरफेर करना एक रोमांचक काम हो सकता है, खासकर जब Aspose.PSD जैसी लाइब्रेरी का इस्तेमाल किया जाता है। इस ट्यूटोरियल में, हम Aspose.PSD के साथ जावा में ग्राफ़िक्स पाथ क्लास का उपयोग करके जटिल ग्राफ़िक्स बनाने की प्रक्रिया में गोता लगाएँगे।
## आवश्यक शर्तें
इससे पहले कि हम कोडिंग भाग में जाएं, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:
1.  जावा डेवलपमेंट किट (JDK): आपकी मशीन पर इंस्टॉल किया गया JDK का एक स्थिर संस्करण। आप इसे यहाँ से डाउनलोड कर सकते हैं[ओरेकल की साइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java लाइब्रेरी: Aspose.PSD for Java लाइब्रेरी को यहाँ से डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/)डाउनलोड करने के बाद, JAR फ़ाइल को अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।
3. एकीकृत विकास वातावरण (आईडीई): चाहे वह एक्लिप्स हो, इंटेलीज आईडिया हो या कोई अन्य, आपको जावा कोड लिखने और चलाने के लिए आईडीई की आवश्यकता होती है।
इन पूर्वावश्यकताओं के साथ, आइए जानें कि ग्राफ़िक्स पथ वर्ग का उपयोग करके दृश्यात्मक रूप से आकर्षक छवियां कैसे बनाई जाती हैं।
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
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```
ये आयात Aspose.PSD का उपयोग करके छवियों को बनाने और उनमें हेरफेर करने के लिए आवश्यक मुख्य कार्यक्षमता तक पहुंच प्रदान करते हैं।
## चरण 1: छवि और ग्राफ़िक्स आरंभ करें
आरंभ करने के लिए, आइए एक नई छवि सेट करें और एक ग्राफ़िक्स ऑब्जेक्ट आरंभ करें:
```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```
यहां, हम 500x500 पिक्सेल की छवि और ड्राइंग के लिए एक ग्राफ़िक्स ऑब्जेक्ट बनाते हैं।
## चरण 2: ग्राफ़िक्स पथ बनाएँ और कॉन्फ़िगर करें
 इसके बाद, हम एक बनाते हैं`GraphicsPath` ड्राइंग पथ को परिभाषित करने के लिए ऑब्जेक्ट:
```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```
इस चरण में, हम अपनी आकृति में एक वृत्त, एक आयत और एक पाठ लेबल जोड़ रहे हैं और फिर इस आकृति को अपने ग्राफिक्स पथ में जोड़ रहे हैं।
## चरण 3: पथ बनाएं और भरें
अब जबकि हमने अपना पथ निर्धारित कर लिया है, हम इसे बना सकते हैं और भर सकते हैं:
```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```
इस चरण में, हम नीले पेन का उपयोग करके पथ बनाते हैं और हैच ब्रश का उपयोग करके इसे ऊर्ध्वाधर हैच पैटर्न से भरते हैं।
## चरण 4: छवि सहेजें
अंत में, छवि को एक फ़ाइल में सहेजें:
```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```
इस अंतिम चरण के साथ, ग्राफ़िक्स पथ का उपयोग करके आपकी छवि निर्माण प्रक्रिया पूरी हो जाती है।
## निष्कर्ष
Aspose.PSD के साथ Graphics Path क्लास का उपयोग करके जटिल छवियाँ बनाना शक्तिशाली और आकर्षक दोनों है। इस गाइड का पालन करके, आप ग्राफिकल डिज़ाइन में अपने Java एप्लिकेशन की क्षमताओं का विस्तार कर सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD क्या है?
Aspose.PSD एक लाइब्रेरी है जो डेवलपर्स को फ़ोटोशॉप फ़ाइलों के साथ काम करने और प्रोग्रामेटिक रूप से छवि परतों में हेरफेर करने की अनुमति देती है।
### क्या मैं PSD के अलावा अन्य प्रारूपों के लिए Aspose.PSD का उपयोग कर सकता हूँ?
इस गाइड के अनुसार, Aspose.PSD विशेष रूप से PSD फाइलों से संबंधित है, लेकिन विभिन्न छवि प्रारूपों को संभालने के लिए एक्सटेंशन प्रदान करता है।
### क्या Aspose.PSD के लिए परीक्षण संस्करण उपलब्ध है?
 हां, आप Aspose.PSD का निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मैं Aspose.PSD कैसे खरीद सकता हूं?
 आप Aspose.PSD यहाँ से खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
### मुझे Aspose.PSD के लिए समर्थन कहां मिल सकता है?
आप समर्थन और चर्चा की मांग कर सकते हैं[Aspose का मंच](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
