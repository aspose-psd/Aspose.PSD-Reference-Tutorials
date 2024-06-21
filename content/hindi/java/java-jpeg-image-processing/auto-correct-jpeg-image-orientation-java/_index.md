---
title: जावा में स्वचालित रूप से सही JPEG इमेज ओरिएंटेशन
linktitle: जावा में स्वचालित रूप से सही JPEG इमेज ओरिएंटेशन
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD का उपयोग करके जावा में JPEG छवि अभिविन्यास को स्वचालित रूप से सही करना सीखें। अपने छवि प्रसंस्करण कौशल को सहजता से बढ़ाएं।
type: docs
weight: 12
url: /hi/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## परिचय
आज के डिजिटल युग में, छवियों को प्रोग्रामेटिक रूप से हेरफेर करना और अनुकूलित करना विभिन्न डोमेन के डेवलपर्स के लिए एक महत्वपूर्ण कार्य बन गया है। जावा के लिए Aspose.PSD डेवलपर्स को PSD, JPEG और अन्य छवि प्रारूपों को कुशलतापूर्वक संभालने के लिए मजबूत टूल के साथ सशक्त बनाता है। यह ट्यूटोरियल एक विशिष्ट कार्य में गोता लगाता है: जावा के लिए Aspose.PSD का उपयोग करके स्वचालित रूप से JPEG छवि अभिविन्यास को सही करना। चाहे आप एक फोटो संपादन ऐप बना रहे हों, सामग्री प्रबंधन प्रणाली में छवि संसाधनों का प्रबंधन कर रहे हों, या छवि प्रसंस्करण वर्कफ़्लो को स्वचालित कर रहे हों, यह मार्गदर्शिका आपको इस कार्यक्षमता को आपके जावा अनुप्रयोगों में निर्बाध रूप से एकीकृत करने के लिए आवश्यक ज्ञान से लैस करेगी।
## आवश्यक शर्तें
इस ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपने निम्नलिखित आवश्यक शर्तें स्थापित कर ली हैं:
- जावा विकास पर्यावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
-  जावा JAR के लिए Aspose.PSD: जावा लाइब्रेरी के लिए Aspose.PSD डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/).
- एकीकृत विकास पर्यावरण (आईडीई): जावा विकास के लिए IntelliJ IDEA, Eclipse, या अपनी पसंद के किसी भी IDE का उपयोग करें।
- जावा और इमेज प्रोसेसिंग की बुनियादी समझ: जावा प्रोग्रामिंग और इमेज प्रोसेसिंग की बुनियादी अवधारणाओं से परिचित होना फायदेमंद होगा।

## पैकेज आयात करें
उदाहरण शुरू करने से पहले, जावा के लिए Aspose.PSD से आवश्यक पैकेज आयात करना सुनिश्चित करें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## चरण 1: PSD छवि लोड करें
सबसे पहले, PSD छवि को लोड करें जिसमें JPEG थंबनेल है जिसके अभिविन्यास में सुधार की आवश्यकता है:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 प्रतिस्थापित करें`"Your Document Directory"` वास्तविक निर्देशिका पथ के साथ जहां आपकी PSD फ़ाइल स्थित है।
## चरण 2: छवि संसाधनों पर पुनरावृति करें
इसके बाद, JPEG थंबनेल संसाधन खोजने के लिए छवि संसाधनों के माध्यम से पुनरावृति करें:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // थंबनेल संसाधन ढूंढें. आमतौर पर वे जेपीईजी फ़ाइल स्वरूप में होते हैं।
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // थंबनेल डेटा समायोजित करें.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // यदि कोई थंबनेल संग्रहीत है, तो उसे स्वतः घुमाएँ।
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
यह चरण सुनिश्चित करता है कि छवि में किए गए परिवर्तन कायम हैं।

## निष्कर्ष
अंत में, जावा के लिए Aspose.PSD का उपयोग PSD फ़ाइलों के भीतर JPEG छवि अभिविन्यास को स्वचालित रूप से सही करने के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, डेवलपर्स अपने इमेज प्रोसेसिंग वर्कफ़्लो को बढ़ा सकते हैं, यह सुनिश्चित करते हुए कि छवियां विभिन्न प्लेटफार्मों और उपकरणों पर सही ढंग से प्रदर्शित हों।
## अक्सर पूछे जाने वाले प्रश्न
### जावा के लिए Aspose.PSD क्या है?
जावा के लिए Aspose.PSD एक शक्तिशाली लाइब्रेरी है जो जावा डेवलपर्स को PSD, JPEG और अन्य छवि प्रारूपों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है।
### मैं जावा के लिए Aspose.PSD कैसे डाउनलोड कर सकता हूँ?
 आप लाइब्रेरी को यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
### क्या जावा के लिए Aspose.PSD छवि हेरफेर का समर्थन करता है?
हां, यह आकार बदलने, क्रॉप करने और ओरिएंटेशन को समायोजित करने जैसे विभिन्न छवि हेरफेर कार्यों का समर्थन करता है।
### मैं जावा के लिए Aspose.PSD के लिए दस्तावेज़ कहां पा सकता हूं?
 व्यापक दस्तावेज उपलब्ध है[यहाँ](https://reference.aspose.com/psd/java/).
### क्या मैं जावा के लिए Aspose.PSD निःशुल्क आज़मा सकता हूँ?
 हाँ, आप नि:शुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).