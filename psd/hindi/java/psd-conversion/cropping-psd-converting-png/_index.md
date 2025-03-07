---
title: Aspose.PSD for Java के साथ PNG में कनवर्ट करते समय PSD को क्रॉप करना
linktitle: PNG में परिवर्तित करते समय PSD को क्रॉप करना
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों को क्रॉप करना और उन्हें PNG में बदलना सीखें। कुशल छवि प्रसंस्करण के साथ अपने Java अनुप्रयोगों को बेहतर बनाएँ।
weight: 13
url: /hi/java/psd-conversion/cropping-psd-converting-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ PNG में कनवर्ट करते समय PSD को क्रॉप करना

## परिचय
जावा विकास की गतिशील दुनिया में, कुशल छवि प्रसंस्करण में महारत हासिल करना महत्वपूर्ण है। यह ट्यूटोरियल आपको शक्तिशाली Aspose.PSD for Java लाइब्रेरी का उपयोग करके PSD फ़ाइलों को PNG में परिवर्तित करते समय उन्हें क्रॉप करने की प्रक्रिया के माध्यम से मार्गदर्शन करेगा। इस चरण-दर-चरण मार्गदर्शिका के अंत तक, आप सहज छवि हेरफेर के साथ अपने जावा अनुप्रयोगों को बढ़ाने के लिए ज्ञान से लैस होंगे।
## आवश्यक शर्तें
ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:
- जावा प्रोग्रामिंग का बुनियादी ज्ञान.
- आपके सिस्टम पर जावा डेवलपमेंट किट (JDK) स्थापित है।
- Aspose.PSD for Java लाइब्रेरी डाउनलोड की गई और आपके प्रोजेक्ट में जोड़ दी गई।
- प्रयोग के लिए एक नमूना PSD फ़ाइल.
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में, Aspose.PSD कार्यक्षमताओं का उपयोग करने के लिए आवश्यक पैकेजों को आयात करना सुनिश्चित करें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```
## चरण 1: अपना प्रोजेक्ट सेट करें
एक जावा प्रोजेक्ट बनाकर और अपने प्रोजेक्ट के क्लासपाथ में Aspose.PSD for Java लाइब्रेरी जोड़कर शुरुआत करें।
## चरण 2: PSD छवि लोड करें
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// मौजूदा PSD छवि लोड करें
RasterImage image = (RasterImage)Image.load(srcPath);
```
## चरण 3: फसल क्षेत्र निर्धारित करें
```java
// x, y, चौड़ाई और ऊँचाई पास करके Rectangle वर्ग का एक उदाहरण बनाएँ
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
## चरण 4: PSD छवि क्रॉप करें
```java
// Image क्लास की crop विधि को कॉल करें और Rectangle इंस्टैंस को पास करें
image.crop(cropRegion);
```
## चरण 5: PNG निर्यात विकल्प सेट करें
```java
// PngOptions वर्ग का एक उदाहरण बनाएँ
PngOptions pngOptions = new PngOptions();
```
## चरण 6: क्रॉप की गई छवि को PNG के रूप में सहेजें
```java
// PSD फ़ाइल को PNG में बदलने और आउटपुट को सहेजने के लिए आउटपुट पथ और PngOptions प्रदान करें
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
## निष्कर्ष
बधाई हो! आपने सफलतापूर्वक सीख लिया है कि Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों को PNG में परिवर्तित करते समय उन्हें कैसे क्रॉप किया जाए। यह कौशल निस्संदेह जावा अनुप्रयोगों में आपकी छवि प्रसंस्करण क्षमताओं को बढ़ाएगा।
## अक्सर पूछे जाने वाले प्रश्नों
### क्या मैं Java के लिए Aspose.PSD का उपयोग करके अनियमित आकृतियों वाली PSD फ़ाइलों को क्रॉप कर सकता हूँ?
हां, Java के लिए Aspose.PSD आपको एक कस्टम फसल क्षेत्र को परिभाषित करने की अनुमति देता है, जिससे आप विभिन्न आकृतियों में छवियों को क्रॉप कर सकते हैं।
### क्या Aspose.PSD for Java बड़े पैमाने पर छवि प्रसंस्करण कार्यों के लिए उपयुक्त है?
बिल्कुल! Aspose.PSD को बड़ी छवियों को कुशलतापूर्वक संभालने के लिए डिज़ाइन किया गया है, जो इसे व्यापक छवि प्रसंस्करण आवश्यकताओं वाली परियोजनाओं के लिए आदर्श बनाता है।
### क्या मुझे Java के लिए Aspose.PSD का लाइसेंस चाहिए?
 हां, व्यावसायिक उपयोग के लिए वैध लाइसेंस की आवश्यकता है। आप इसे यहां से प्राप्त कर सकते हैं[Aspose खरीद](https://purchase.aspose.com/buy).
### मैं Aspose.PSD for Java के साथ सहायता कैसे प्राप्त कर सकता हूँ या समस्याओं की रिपोर्ट कैसे कर सकता हूँ?
 दौरा करना[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सहायता प्राप्त करने, अपने अनुभव साझा करने, तथा सामने आने वाली किसी भी समस्या की रिपोर्ट करने के लिए।
### क्या मैं खरीदने से पहले Java के लिए Aspose.PSD आज़मा सकता हूँ?
 ज़रूर! निःशुल्क परीक्षण के साथ लाइब्रेरी की विशेषताओं का अन्वेषण करें[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
