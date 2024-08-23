---
title: जावा में EXIF डेटा लिखें और संशोधित करें
linktitle: जावा में EXIF डेटा लिखें और संशोधित करें
second_title: Aspose.PSD जावा एपीआई
description: इस व्यापक, चरण-दर-चरण मार्गदर्शिका के साथ Java के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में EXIF डेटा लिखना और संशोधित करना सीखें।
type: docs
weight: 22
url: /hi/java/java-jpeg-image-processing/write-modify-exif-data-java/
---
## परिचय
क्या आप जावा का उपयोग करके PSD फ़ाइलों में EXIF डेटा को हेरफेर करना चाहते हैं? यदि हाँ, तो आप सही जगह पर हैं! यह व्यापक गाइड आपको शक्तिशाली Aspose.PSD लाइब्रेरी का उपयोग करके जावा में EXIF डेटा लिखने और संशोधित करने के चरणों के माध्यम से मार्गदर्शन करेगा। 
## आवश्यक शर्तें
कोड में आगे बढ़ने से पहले, आइए सुनिश्चित करें कि आपने सब कुछ सही ढंग से सेट किया है।
1. जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके मशीन पर JDK स्थापित है।
2.  Aspose.PSD for Java: लाइब्रेरी को यहाँ से डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/).
3. IDE: निर्बाध कोडिंग अनुभव के लिए IntelliJ IDEA या Eclipse जैसे IDE का उपयोग करें।
4. बुनियादी जावा ज्ञान: जावा प्रोग्रामिंग से परिचित होना आवश्यक है।
5.  Aspose अस्थायी लाइसेंस: से एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/) Aspose.PSD की पूरी क्षमता को अनलॉक करने के लिए.
## पैकेज आयात करें
सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। इसे कैसे करें, यहाँ बताया गया है:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.exif.enums.ExifFlash;
import com.aspose.psd.exif.enums.ExifWhiteBalance;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
ये आयात आपको PSD फ़ाइलों के साथ काम करने, EXIF डेटा में हेरफेर करने और Aspose.PSD की शक्तिशाली सुविधाओं का उपयोग करने की अनुमति देंगे।
अब जब आपने सब कुछ सेट कर लिया है, तो आइए प्रक्रिया को सरल, आसान चरणों में विभाजित करें।
## चरण 1: PSD छवि लोड करें
सबसे पहले आपको अपनी PSD फ़ाइल को अपने प्रोजेक्ट में लोड करना होगा। आप इसे इस तरह से कर सकते हैं:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
यह कोड स्निपेट आपकी निर्दिष्ट निर्देशिका से PSD छवि लोड करता है।
## चरण 2: छवि संसाधनों पर पुनरावृति करें
इसके बाद, आपको थंबनेल संसाधन खोजने के लिए छवि संसाधनों पर पुनरावृति करनी होगी। यह वह जगह है जहाँ EXIF डेटा आमतौर पर JPEG प्रारूप में संग्रहीत होता है।
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // थंबनेल संसाधनों की जाँच करें
}
```
## चरण 3: थंबनेल संसाधन की पहचान करें
इस चरण में, आप छवि संसाधनों से थंबनेल संसाधन की पहचान करेंगे।
```java
if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
    // थंबनेल संसाधन से EXIF डेटा निकालें
}
```
## चरण 4: EXIF डेटा निकालें और प्रिंट करें
एक बार जब आप थंबनेल संसाधन की पहचान कर लेते हैं, तो अगला चरण EXIF डेटा को निकालना और उसे कंसोल पर प्रिंट करना होता है।
```java
JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
if (exif != null) {
    // EXIF डेटा प्रिंट करें
}
```
## चरण 5: EXIF डेटा संशोधित करें
अब आता है मज़ेदार हिस्सा - EXIF डेटा को संशोधित करना। यहाँ बताया गया है कि आप LensMake, WhiteBalance और Flash जानकारी कैसे सेट कर सकते हैं।
```java
exif.setLensMake("Sony");
exif.setWhiteBalance(ExifWhiteBalance.Auto);
exif.setFlash(ExifFlash.Fired);
```
## चरण 6: छवि सहेजें
आवश्यक संशोधन करने के बाद, परिवर्तन लागू करने के लिए छवि को सहेजें।
```java
image.save(dataDir + "Modified_Zebras_Serengeti.psd");
```
## निष्कर्ष
और अब आप समझ गए होंगे! आपने सफलतापूर्वक सीख लिया है कि Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में EXIF डेटा कैसे लिखें और संशोधित करें। यह शक्तिशाली लाइब्रेरी जटिल छवि प्रारूपों के साथ काम करना आसान बनाती है, जिससे यह ग्राफ़िक फ़ाइलों के साथ काम करने वाले डेवलपर्स के लिए एक मूल्यवान उपकरण बन जाता है। 
 अधिक विस्तृत जानकारी के लिए देखें[Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/) यदि आपको कोई समस्या आती है, तो[सहयता मंच](https://forum.aspose.com/c/psd/34) सहायता पाने के लिए यह एक बेहतरीन जगह है। इसे एक्सप्लोर करना न भूलें[मुफ्त परीक्षण](https://releases.aspose.com/) और लाइसेंस खरीदने पर विचार करें[यहाँ](https://purchase.aspose.com/buy) पूर्ण सुविधाओं के लिए.
## अक्सर पूछे जाने वाले प्रश्न
### EXIF डेटा क्या है?
EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) डेटा, इमेज फाइलों में सन्निहित मेटाडेटा है, जिसमें कैमरा सेटिंग्स, दिनांक, समय और स्थान जैसी जानकारी शामिल होती है।
### क्या Aspose.PSD अन्य छवि प्रारूपों को संभाल सकता है?
हां, Aspose.PSD PNG, JPEG, BMP और GIF सहित विभिन्न छवि प्रारूपों का समर्थन करता है।
### क्या Java के लिए Aspose.PSD निःशुल्क है?
आप निःशुल्क परीक्षण का उपयोग कर सकते हैं, लेकिन पूर्ण सुविधाओं के लिए आपको लाइसेंस खरीदना होगा।
### मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?
 आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
### क्या मैं छवियों के बैच प्रसंस्करण के लिए Aspose.PSD का उपयोग कर सकता हूँ?
हां, आप Aspose.PSD की मजबूत सुविधाओं का उपयोग करके एक बैच में कई छवियों को संसाधित कर सकते हैं।