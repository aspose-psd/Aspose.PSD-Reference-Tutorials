---
title: जावा में JPEG छवि अभिविन्यास को स्वतः सही करें
linktitle: जावा में JPEG छवि अभिविन्यास को स्वतः सही करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD का उपयोग करके जावा में JPEG इमेज ओरिएंटेशन को स्वचालित रूप से सही करना सीखें। अपने इमेज प्रोसेसिंग कौशल को सहजता से बढ़ाएँ।
type: docs
weight: 12
url: /hi/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## परिचय
आज के डिजिटल युग में, प्रोग्रामेटिक रूप से छवियों में हेरफेर और अनुकूलन करना विभिन्न डोमेन के डेवलपर्स के लिए एक महत्वपूर्ण कार्य बन गया है। Aspose.PSD for Java डेवलपर्स को PSD, JPEG और अन्य छवि प्रारूपों को कुशलतापूर्वक संभालने के लिए मजबूत टूल प्रदान करता है। यह ट्यूटोरियल एक विशिष्ट कार्य में गोता लगाता है: Aspose.PSD for Java का उपयोग करके JPEG छवि अभिविन्यास को स्वचालित रूप से सही करना। चाहे आप कोई फोटो एडिटिंग ऐप बना रहे हों, कंटेंट मैनेजमेंट सिस्टम में इमेज रिसोर्स को मैनेज कर रहे हों या इमेज प्रोसेसिंग वर्कफ़्लो को ऑटोमेट कर रहे हों, यह गाइड आपको इस कार्यक्षमता को अपने Java एप्लिकेशन में सहजता से एकीकृत करने के लिए आवश्यक ज्ञान से लैस करेगा।
## आवश्यक शर्तें
इस ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:
- जावा डेवलपमेंट एनवायरनमेंट: सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (JDK) स्थापित है।
-  Aspose.PSD for Java JAR: Aspose.PSD for Java लाइब्रेरी को यहाँ से डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/).
- एकीकृत विकास वातावरण (IDE): जावा विकास के लिए IntelliJ IDEA, Eclipse या अपनी पसंद के किसी भी IDE का उपयोग करें।
- जावा और इमेज प्रोसेसिंग की बुनियादी समझ: जावा प्रोग्रामिंग और इमेज प्रोसेसिंग की बुनियादी अवधारणाओं से परिचित होना लाभदायक होगा।

## पैकेज आयात करें
उदाहरण शुरू करने से पहले, Java के लिए Aspose.PSD से आवश्यक पैकेज आयात करना सुनिश्चित करें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## चरण 1: PSD छवि लोड करें
सबसे पहले, PSD छवि लोड करें जिसमें JPEG थंबनेल है जिसके ओरिएंटेशन में सुधार की आवश्यकता है:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 प्रतिस्थापित करें`"Your Document Directory"` वास्तविक निर्देशिका पथ के साथ जहां आपकी PSD फ़ाइल स्थित है।
## चरण 2: छवि संसाधनों पर पुनरावृति करें
इसके बाद, JPEG थंबनेल संसाधन को खोजने के लिए छवि संसाधनों के माध्यम से पुनरावृति करें:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // थंबनेल संसाधन खोजें। आमतौर पर वे Jpeg फ़ाइल प्रारूप में होते हैं।
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // थम्बनेल डेटा समायोजित करें.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // यदि कोई थम्बनेल संग्रहीत है, तो उसे स्वचालित रूप से घुमाएं।
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## चरण 3: छवि सहेजें
अंत में, ऑटो-रोटेशन लागू करने के बाद सही छवि को सहेजें:
```java
image.save();
```
यह चरण यह सुनिश्चित करता है कि छवि में किए गए परिवर्तन बरकरार रहें।

## निष्कर्ष
निष्कर्ष में, जावा के लिए Aspose.PSD का उपयोग PSD फ़ाइलों के भीतर JPEG छवि अभिविन्यास को स्वचालित रूप से सही करने के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, डेवलपर्स अपने इमेज प्रोसेसिंग वर्कफ़्लो को बढ़ा सकते हैं, यह सुनिश्चित करते हुए कि विभिन्न प्लेटफ़ॉर्म और डिवाइस पर छवियाँ सही ढंग से प्रदर्शित होती हैं।
## अक्सर पूछे जाने वाले प्रश्न
### Java के लिए Aspose.PSD क्या है?
Aspose.PSD for Java एक शक्तिशाली लाइब्रेरी है जो जावा डेवलपर्स को PSD, JPEG और अन्य छवि प्रारूपों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है।
### मैं Java के लिए Aspose.PSD कैसे डाउनलोड कर सकता हूँ?
 आप लाइब्रेरी को यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
### क्या Aspose.PSD for Java छवि हेरफेर का समर्थन करता है?
हां, यह विभिन्न छवि हेरफेर कार्यों जैसे आकार बदलने, क्रॉप करने और अभिविन्यास समायोजित करने का समर्थन करता है।
### मैं Java के लिए Aspose.PSD हेतु दस्तावेज़ कहां पा सकता हूं?
 व्यापक दस्तावेज उपलब्ध है[यहाँ](https://reference.aspose.com/psd/java/).
### क्या मैं Java के लिए Aspose.PSD को निःशुल्क आज़मा सकता हूँ?
 हां, आप यहां से निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).