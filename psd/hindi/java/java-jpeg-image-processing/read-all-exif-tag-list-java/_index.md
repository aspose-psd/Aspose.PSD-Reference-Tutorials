---
title: जावा में सभी EXIF टैग सूची पढ़ें
linktitle: जावा में सभी EXIF टैग सूची पढ़ें
second_title: Aspose.PSD जावा एपीआई
description: हमारे व्यापक ट्यूटोरियल और कोड उदाहरणों के साथ Java के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों से EXIF मेटाडेटा निकालने का तरीका जानें।
weight: 16
url: /hi/java/java-jpeg-image-processing/read-all-exif-tag-list-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में सभी EXIF टैग सूची पढ़ें

### परिचय
जावा विकास के क्षेत्र में, PSD फ़ाइलों का प्रबंधन और हेरफेर करना कई अनुप्रयोगों के लिए एक महत्वपूर्ण आवश्यकता है। Aspose.PSD for Java, Photoshop Document (PSD) फ़ाइलों को प्रोग्रामेटिक रूप से संभालने के लिए एक मजबूत समाधान प्रदान करता है, जो डेवलपर्स को PSD फ़ाइलों को पढ़ने, लिखने और संशोधित करने के लिए उपकरणों का एक सूट प्रदान करता है। यह ट्यूटोरियल आपको Aspose.PSD for Java का उपयोग करके PSD फ़ाइल से सभी EXIF टैग पढ़ने की प्रक्रिया के माध्यम से मार्गदर्शन करेगा। अंत तक, आपको PSD छवियों में एम्बेडेड EXIF मेटाडेटा को निकालने और उसका उपयोग करने के तरीके के बारे में स्पष्ट समझ होगी।
### आवश्यक शर्तें
इस ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:
- आपके सिस्टम पर जावा डेवलपमेंट किट (JDK) स्थापित है।
- एकीकृत विकास वातावरण (आईडीई) जैसे कि इंटेलीज आईडिया या एक्लिप्स।
-  Aspose.PSD for Java लाइब्रेरी डाउनलोड की गई। आप इसे यहाँ से प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
## पैकेज आयात करें
आरंभ करने के लिए, अपने प्रोजेक्ट में Aspose.PSD for Java से आवश्यक पैकेज आयात करें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import java.util.Properties;
```
## चरण 1: PSD फ़ाइल लोड करें
 सबसे पहले PSD फ़ाइल को एक में लोड करें`PsdImage` वस्तु:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "example.psd");
```
## चरण 2: छवि संसाधनों पर पुनरावृति करें
इसके बाद, EXIF डेटा खोजने के लिए छवि संसाधनों के माध्यम से पुनरावृति करें:
```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null) {
            // EXIF डेटा गुण संसाधित करें
            for(int j = 0; j < exifData.getProperties().length; j++) {
                System.out.println(exifData.getProperties()[j].getId() + ": " + exifData.getProperties()[j].getValue());
            }
        }
    }
}
```

## निष्कर्ष
निष्कर्ष में, जावा के लिए Aspose.PSD का लाभ उठाने से PSD फ़ाइलों से EXIF मेटाडेटा निकालने का कार्य सरल हो जाता है। इस ट्यूटोरियल ने आपको इस कार्यक्षमता को अपने जावा अनुप्रयोगों में सहजता से एकीकृत करने के लिए आवश्यक चरणों से सुसज्जित किया है।
## अक्सर पूछे जाने वाले प्रश्न
### Java के लिए Aspose.PSD क्या है?
Aspose.PSD for Java एक लाइब्रेरी है जो जावा डेवलपर्स को फ़ोटोशॉप इंस्टॉल किए बिना PSD फ़ाइलों के साथ काम करने की अनुमति देती है।
### मैं Aspose.PSD for Java दस्तावेज़ कहां पा सकता हूं?
 आप दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).
### मैं Java के लिए Aspose.PSD हेतु अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
 मिलने जाना[यहाँ](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस विकल्पों के लिए.
### क्या Aspose.PSD for Java PSD फ़ाइलें लिखने का समर्थन करता है?
हां, यह PSD फ़ाइलों को पढ़ने और लिखने दोनों का समर्थन करता है।
### मैं Java के लिए Aspose.PSD का समर्थन कहां से प्राप्त कर सकता हूं?
 सहायता के लिए, यहां जाएं[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
