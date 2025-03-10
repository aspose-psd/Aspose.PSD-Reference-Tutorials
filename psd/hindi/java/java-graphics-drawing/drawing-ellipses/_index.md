---
title: जावा में दीर्घवृत्त बनाना
linktitle: जावा में दीर्घवृत्त बनाना
second_title: Aspose.PSD जावा एपीआई
description: सटीक ग्राफ़िक डिज़ाइन और छवि हेरफेर के लिए Aspose.PSD का उपयोग करके जावा में दीर्घवृत्त बनाना सीखें। चरण-दर-चरण ट्यूटोरियल में महारत हासिल करें।
weight: 15
url: /hi/java/java-graphics-drawing/drawing-ellipses/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में दीर्घवृत्त बनाना

## परिचय
इस ट्यूटोरियल में, आप सीखेंगे कि जावा के लिए Aspose.PSD का उपयोग करके दीर्घवृत्त कैसे बनाएं। Aspose.PSD एक शक्तिशाली लाइब्रेरी है जो जावा डेवलपर्स को PSD फ़ाइलों के साथ काम करने और आसानी से छवियों में हेरफेर करने की अनुमति देती है। दीर्घवृत्त जैसी आकृतियाँ बनाना इमेज प्रोसेसिंग और ग्राफ़िक डिज़ाइन में एक बुनियादी काम है। इस गाइड का पालन करके, आप Aspose.PSD का उपयोग करके प्रोग्रामेटिक रूप से दीर्घवृत्त बनाने में व्यावहारिक अनुभव प्राप्त करेंगे।
## आवश्यक शर्तें
आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:
- जावा प्रोग्रामिंग का बुनियादी ज्ञान.
- आपके सिस्टम पर JDK (जावा डेवलपमेंट किट) स्थापित है।
- एकीकृत विकास वातावरण (आईडीई) जैसे कि इंटेलीज आईडिया या एक्लिप्स।
-  Aspose.PSD for Java लाइब्रेरी। आप इसे यहाँ से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
## पैकेज आयात करें
सबसे पहले, आपको Aspose.PSD से आवश्यक पैकेज आयात करने की आवश्यकता है:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
## चरण 1: अपना जावा प्रोजेक्ट सेट अप करें
कोडिंग शुरू करने से पहले, सुनिश्चित करें कि आपका जावा प्रोजेक्ट निर्भरता के रूप में Aspose.PSD सहित सही ढंग से सेटअप किया गया है।
## चरण 2: PsdImage का एक उदाहरण बनाएँ
वांछित चौड़ाई और ऊंचाई के साथ PsdImage का एक नया उदाहरण आरंभ करें।
```java
Image image = new PsdImage(100, 100);
```
## चरण 3: ग्राफ़िक्स ऑब्जेक्ट को आरंभ करें
छवि के साथ कार्य करने के लिए Graphics का एक उदाहरण बनाएं और आरंभ करें।
```java
Graphics graphics = new Graphics(image);
```
## चरण 4: ग्राफ़िक्स सतह साफ़ करें
चित्र बनाने से पहले, ग्राफ़िक्स सतह को किसी विशिष्ट रंग से साफ़ करें (वैकल्पिक)।
```java
graphics.clear(Color.getYellow());
```
## चरण 5: एक बिंदुयुक्त दीर्घवृत्त बनाएं
लाल रंग के पेन ऑब्जेक्ट का उपयोग करें और निर्दिष्ट आयत के भीतर एक बिंदुयुक्त दीर्घवृत्त बनाएं।
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## चरण 6: एक सतत दीर्घवृत्त बनाएं
एक ठोस नीले ब्रश से एक पेन ऑब्जेक्ट बनाएं और दूसरे आयत के भीतर एक सतत दीर्घवृत्त बनाएं।
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## चरण 7: छवि सहेजें
अंत में, उत्पन्न छवि को BMP प्रारूप में निर्दिष्ट पथ पर सहेजें।
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## निष्कर्ष
बधाई हो! आपने सफलतापूर्वक सीख लिया है कि Aspose.PSD for Java का उपयोग करके प्रोग्रामेटिक रूप से दीर्घवृत्त कैसे बनाएं। इस ट्यूटोरियल में आपके प्रोजेक्ट को सेट करना, ग्राफ़िक्स को आरंभ करना, डॉटेड और निरंतर दीर्घवृत्त बनाना और परिणामी छवि को सहेजना शामिल है। अब आप इन तकनीकों को विभिन्न ग्राफ़िक डिज़ाइन और छवि हेरफेर कार्यों के लिए अपने जावा अनुप्रयोगों में एकीकृत कर सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### क्या मैं Aspose.PSD का निःशुल्क उपयोग कर सकता हूँ?
Aspose.PSD एक निःशुल्क परीक्षण संस्करण प्रदान करता है, जिससे आप खरीदने से पहले इसकी सुविधाओं का मूल्यांकन कर सकते हैं।
### मैं और अधिक उदाहरण और दस्तावेज कहां पा सकता हूं?
 मिलने जाना[Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/) विस्तृत मार्गदर्शिका और उदाहरण के लिए.
### मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 अस्थायी लाइसेंस निम्नलिखित से प्राप्त किए जा सकते हैं:[Aspose.PSD अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD छवियों को किस प्रारूप में सहेज सकता है?
Aspose.PSD BMP, PNG, JPEG, और PSD सहित विभिन्न प्रारूपों में छवियों को सहेजने का समर्थन करता है।
### क्या Aspose.PSD उद्यम उपयोग के लिए उपयुक्त है?
हां, Aspose.PSD को व्यावसायिक और उद्यम-स्तरीय छवि प्रसंस्करण कार्यों के लिए डिज़ाइन किया गया है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
