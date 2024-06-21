---
title: जावा में EXIF डेटा लिखें और संशोधित करें
linktitle: जावा में EXIF डेटा लिखें और संशोधित करें
second_title: Aspose.PSD जावा एपीआई
description: इस व्यापक, चरण-दर-चरण मार्गदर्शिका के साथ जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में EXIF डेटा लिखना और संशोधित करना सीखें।
type: docs
weight: 22
url: /hi/java/java-jpeg-image-processing/write-modify-exif-data-java/
---
## परिचय
क्या आप जावा का उपयोग करके PSD फ़ाइलों में EXIF डेटा में हेरफेर करना चाह रहे हैं? यदि हां, तो आप सही जगह पर हैं! यह व्यापक मार्गदर्शिका आपको शक्तिशाली Aspose.PSD लाइब्रेरी का उपयोग करके जावा में EXIF डेटा लिखने और संशोधित करने के चरणों के बारे में बताएगी। 
## आवश्यक शर्तें
कोड में गोता लगाने से पहले, आइए सुनिश्चित करें कि आपने सब कुछ सही ढंग से सेट किया है।
1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपकी मशीन पर जेडीके स्थापित है।
2.  जावा के लिए Aspose.PSD: यहां से लाइब्रेरी डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/).
3. आईडीई: सहज कोडिंग अनुभव के लिए IntelliJ IDEA या Eclipse जैसी IDE का उपयोग करें।
4. बुनियादी जावा ज्ञान: जावा प्रोग्रामिंग से परिचित होना आवश्यक है।
5.  अस्थायी लाइसेंस स्वीकार करें: से अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/) Aspose.PSD की पूरी क्षमता को अनलॉक करने के लिए।
## पैकेज आयात करें
सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। यह कैसे करना है यहां बताया गया है:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.exif.enums.ExifFlash;
import com.aspose.psd.exif.enums.ExifWhiteBalance;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
ये आयात आपको PSD फ़ाइलों के साथ काम करने, EXIF डेटा में हेरफेर करने और Aspose.PSD की शक्तिशाली सुविधाओं का उपयोग करने की अनुमति देंगे।
अब जब आपने सब कुछ सेट कर लिया है, तो आइए इस प्रक्रिया को सरल, पालन में आसान चरणों में विभाजित करें।
## चरण 1: PSD छवि लोड करें
आरंभ करने के लिए, आपको अपनी PSD फ़ाइल को अपने प्रोजेक्ट में लोड करना होगा। यहां बताया गया है कि आप यह कैसे कर सकते हैं:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
यह कोड स्निपेट आपकी निर्दिष्ट निर्देशिका से PSD छवि लोड करता है।
## चरण 2: छवि संसाधनों पर पुनरावृति करें
इसके बाद, आपको थंबनेल संसाधन ढूंढने के लिए छवि संसाधनों पर पुनरावृति करने की आवश्यकता है। यह वह जगह है जहां EXIF डेटा आमतौर पर JPEG प्रारूप में संग्रहीत किया जाता है।
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
एक बार जब आप थंबनेल संसाधन की पहचान कर लेते हैं, तो अगला चरण EXIF डेटा निकालना और उसे कंसोल पर प्रिंट करना है।
```java
JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
if (exif != null) {
    // EXIF डेटा प्रिंट करें
}
```
## चरण 5: EXIF डेटा को संशोधित करें
अब मज़ेदार हिस्सा आता है - EXIF डेटा को संशोधित करना। यहां बताया गया है कि आप लेंसमेक, व्हाइटबैलेंस और फ्लैश जानकारी कैसे सेट कर सकते हैं।
```java
exif.setLensMake("Sony");
exif.setWhiteBalance(ExifWhiteBalance.Auto);
exif.setFlash(ExifFlash.Fired);
```
## चरण 6: छवि सहेजें
आवश्यक संशोधन करने के बाद, परिवर्तनों को लागू करने के लिए छवि को सहेजें।
```java
image.save(dataDir + "Modified_Zebras_Serengeti.psd");
```
## निष्कर्ष
आखिर तुमने इसे हासिल कर ही लिया है! आपने जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में EXIF डेटा को लिखना और संशोधित करना सफलतापूर्वक सीख लिया है। यह शक्तिशाली लाइब्रेरी जटिल छवि प्रारूपों के साथ काम करना सरल बनाती है, जिससे यह ग्राफिक फ़ाइलों के साथ काम करने वाले डेवलपर्स के लिए एक मूल्यवान उपकरण बन जाती है। 
 अधिक विस्तृत जानकारी के लिए, देखें[Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/) . यदि आपको कोई समस्या आती है, तो[सहयता मंच](https://forum.aspose.com/c/psd/34) सहायता पाने के लिए एक बेहतरीन जगह है. अन्वेषण करना न भूलें[मुफ्त परीक्षण](https://releases.aspose.com/) और लाइसेंस खरीदने पर विचार करें[यहाँ](https://purchase.aspose.com/buy) पूर्ण सुविधाओं के लिए.
## अक्सर पूछे जाने वाले प्रश्न
### EXIF डेटा क्या है?
EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) डेटा इमेज फाइलों में एम्बेडेड मेटाडेटा है, जिसमें कैमरा सेटिंग्स, दिनांक, समय और स्थान जैसी जानकारी होती है।
### क्या Aspose.PSD अन्य छवि प्रारूपों को संभाल सकता है?
हां, Aspose.PSD पीएनजी, जेपीईजी, बीएमपी और जीआईएफ सहित विभिन्न छवि प्रारूपों का समर्थन करता है।
### क्या जावा के लिए Aspose.PSD निःशुल्क है?
आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं, लेकिन पूर्ण सुविधाओं के लिए, आपको लाइसेंस खरीदना होगा।
### मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
 आपको अस्थायी लाइसेंस मिल सकता है[यहाँ](https://purchase.aspose.com/temporary-license/).
### क्या मैं बैच प्रोसेसिंग छवियों के लिए Aspose.PSD का उपयोग कर सकता हूँ?
हां, आप Aspose.PSD की मजबूत सुविधाओं का उपयोग करके एक बैच में कई छवियों को संसाधित कर सकते हैं।