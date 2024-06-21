---
title: जावा में सभी EXIF टैग पढ़ें
linktitle: जावा में सभी EXIF टैग पढ़ें
second_title: Aspose.PSD जावा एपीआई
description: Java के लिए Aspose.PSD का उपयोग करके PSD छवियों से EXIF टैग निकालना सीखें। कुशल मेटाडेटा निष्कर्षण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 17
url: /hi/java/java-jpeg-image-processing/read-all-exif-tags-java/
---
## परिचय
जावा विकास के क्षेत्र में, छवियों से मेटाडेटा को संभालना और निकालना एक सामान्य कार्य है, खासकर जब PSD (फ़ोटोशॉप दस्तावेज़) फ़ाइलों से निपटना हो। EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) टैग में मूल्यवान मेटाडेटा होता है जो छवि के बारे में जानकारी प्रदान करता है, जैसे कैमरा सेटिंग्स, स्थान और बहुत कुछ। यह ट्यूटोरियल जावा के लिए Aspose.PSD का उपयोग करने पर केंद्रित है, जो EXIF टैग को कुशलतापूर्वक पढ़ने के लिए PSD फ़ाइलों में हेरफेर करने के लिए एक शक्तिशाली लाइब्रेरी है।
## आवश्यक शर्तें
इस ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:
- जावा प्रोग्रामिंग का बुनियादी ज्ञान।
- आपकी मशीन पर JDK (जावा डेवलपमेंट किट) स्थापित है।
- आईडीई (एकीकृत विकास पर्यावरण) जैसे इंटेलीजे आईडीईए या एक्लिप्स।
-  जावा लाइब्रेरी के लिए Aspose.PSD। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
## पैकेज आयात करें
आरंभ करने के लिए, Java के लिए Aspose.PSD से आवश्यक पैकेज आयात करें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
ये आयात आपको PSD छवियों के साथ काम करने और EXIF मेटाडेटा को कुशलतापूर्वक निकालने की अनुमति देंगे।
## चरण 1: PSD छवि लोड करें
सबसे पहले, आपको PSD छवि फ़ाइल लोड करनी होगी जिससे आप EXIF टैग निकालना चाहते हैं:
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```
 प्रतिस्थापित करें`"Your_Document_Directory/"` PSD फ़ाइल वाली आपकी निर्देशिका के पथ के साथ, और`"your_image.psd"` वास्तविक फ़ाइलनाम के साथ.
## चरण 2: छवि संसाधनों पर पुनरावृति करें
इसके बाद, EXIF डेटा खोजने के लिए छवि संसाधनों के माध्यम से पुनरावृति करें:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        JpegExifData exif = thumbnail.getJpegOptions().getExifData();
        
        if (exif != null) {
            // चरण 3: EXIF गुण निकालें और प्रिंट करें
            for (int j = 0; j < exif.getProperties().length; j++) {
                System.out.println(exif.getProperties()[j].getId() + ":" + exif.getProperties()[j].getValue());
            }
        }
    }
}
```

## निष्कर्ष
इस ट्यूटोरियल में, आपने सीखा कि PSD छवियों से EXIF टैग पढ़ने के लिए जावा के लिए Aspose.PSD का उपयोग कैसे करें। यह क्षमता उन अनुप्रयोगों के लिए महत्वपूर्ण है जिनके लिए छवियों से विस्तृत मेटाडेटा को कुशलतापूर्वक निकालने की आवश्यकता होती है।
## अक्सर पूछे जाने वाले प्रश्न
### जावा के लिए Aspose.PSD क्या है?
जावा के लिए Aspose.PSD एक जावा लाइब्रेरी है जिसका उपयोग प्रोग्रामेटिक रूप से PSD फ़ाइलों को संसाधित करने और हेरफेर करने के लिए किया जाता है।
### मैं जावा के लिए Aspose.PSD कैसे डाउनलोड करूं?
 आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
### क्या मैं खरीदने से पहले जावा के लिए Aspose.PSD आज़मा सकता हूँ?
 हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मुझे जावा के लिए Aspose.PSD के लिए समर्थन कहां मिल सकता है?
 Aspose.PSD फोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/psd/34) किसी भी समर्थन प्रश्न के लिए.
### क्या मुझे Java के लिए Aspose.PSD का उपयोग करने के लिए लाइसेंस की आवश्यकता है?
 हां, आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy) या अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).