---
title: Java के लिए Aspose.PSD में गाऊसी और वीनर फ़िल्टर लागू करें
linktitle: गॉसियन और वीनर फ़िल्टर लागू करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ अपनी जावा इमेज प्रोसेसिंग को बेहतर बनाएँ। शानदार विज़ुअल परिणामों के लिए गॉसियन और वीनर फ़िल्टर को चरण-दर-चरण लागू करना सीखें।
type: docs
weight: 10
url: /hi/java/image-processing/apply-gaussian-wiener-filters/
---
## परिचय

Aspose.PSD for Java में गॉसियन और वीनर फ़िल्टर लगाने के बारे में हमारे विस्तृत ट्यूटोरियल में आपका स्वागत है! इस गाइड में, हम आपको इन शक्तिशाली फ़िल्टर का उपयोग करके अपनी छवियों को बेहतर बनाने की प्रक्रिया से अवगत कराएँगे। Aspose.PSD for Java छवि प्रसंस्करण के लिए सुविधाओं का एक मजबूत सेट प्रदान करता है, और गॉसियन और वीनर फ़िल्टर के अनुप्रयोग के साथ, आप चिकनी और अधिक परिष्कृत छवियाँ प्राप्त कर सकते हैं।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में आगे बढ़ें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- जावा विकास वातावरण: सुनिश्चित करें कि आपके मशीन पर जावा विकास वातावरण स्थापित है।

- Aspose.PSD for Java लाइब्रेरी: Aspose.PSD for Java लाइब्रेरी डाउनलोड करें और इंस्टॉल करें। आप डाउनलोड लिंक पा सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, Aspose.PSD के लिए आवश्यक पैकेज आयात करें। आरंभ करने के लिए यहाँ एक नमूना आयात कथन दिया गया है:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

अब, आइए गॉसियन और वीनर फिल्टर को लागू करने के लिए उदाहरण को कई चरणों में विभाजित करें।

## चरण 1: छवि लोड करें

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

इस चरण में, हम निर्दिष्ट निर्देशिका से PSD छवि फ़ाइल लोड करते हैं।

## चरण 2: रास्टरइमेज की जाँच करें

```java
if (rasterImage == null) {
    return;
}
```

सुनिश्चित करें कि लोड की गई छवि एक वैध RasterImage है; अन्यथा, प्रक्रिया समाप्त हो जाएगी।

## चरण 3: फ़िल्टर विकल्प कॉन्फ़िगर करें

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

GaussWienerFilterOptions का एक उदाहरण बनाएं, त्रिज्या का आकार, स्मूथ मान सेट करें, और निर्दिष्ट करें कि क्या आप फ़िल्टर को ग्रेस्केल में लागू करना चाहते हैं।

## चरण 4: फ़िल्टर लागू करें और सहेजें

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

अंत में, कॉन्फ़िगर किए गए गॉसियन और वीनर फ़िल्टर को रैस्टरइमेज पर लागू करें और परिणामी छवि को GIF प्रारूप में सहेजें।

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके Gaussian और Wiener फ़िल्टर को लागू करना सफलतापूर्वक सीख लिया है। वांछित छवि संवर्द्धन प्राप्त करने के लिए विभिन्न मापदंडों के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं इन फिल्टरों को PSD के अलावा अन्य प्रारूपों वाली छवियों पर भी लागू कर सकता हूँ?

A1: हां, Aspose.PSD for Java PSD से परे विभिन्न छवि प्रारूपों का समर्थन करता है।

### प्रश्न 2: क्या Java के लिए Aspose.PSD के परीक्षण संस्करण में कोई प्रतिबंध हैं?

उत्तर2: परीक्षण संस्करण की कुछ सीमाएँ हैं, और आप वैध लाइसेंस प्राप्त करके इसकी सम्पूर्ण क्षमताओं का पता लगा सकते हैं।

### प्रश्न 3: मैं Java के लिए Aspose.PSD का समर्थन कैसे प्राप्त कर सकता हूं?

 A3: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन और चर्चा के लिए।

### प्रश्न 4: क्या परीक्षण प्रयोजनों के लिए कोई अस्थायी लाइसेंस उपलब्ध है?

 A4: हां, आप एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### प्रश्न 5: मैं Java के लिए Aspose.PSD हेतु विस्तृत दस्तावेज़ कहां पा सकता हूं?

 A5: देखें[प्रलेखन](https://reference.aspose.com/psd/java/) गहन जानकारी के लिए.