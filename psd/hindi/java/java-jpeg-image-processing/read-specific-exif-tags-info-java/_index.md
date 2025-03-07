---
title: जावा में विशिष्ट EXIF टैग जानकारी पढ़ें
linktitle: जावा में विशिष्ट EXIF टैग जानकारी पढ़ें
second_title: Aspose.PSD जावा एपीआई
description: हमारे चरण-दर-चरण ट्यूटोरियल के साथ Aspose.PSD for Java का उपयोग करके PSD छवियों से विशिष्ट EXIF टैग पढ़ना सीखें। अपनी छवि प्रसंस्करण कौशल को बढ़ाएँ।
weight: 19
url: /hi/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में विशिष्ट EXIF टैग जानकारी पढ़ें

## परिचय
क्या आप जावा के साथ PSD फ़ाइल हेरफेर की दुनिया में गोता लगाना चाहते हैं? यदि आप PSD छवियों से विशिष्ट EXIF टैग को पढ़ना सीखना चाहते हैं, तो आप सही जगह पर हैं। यह ट्यूटोरियल आपको जावा के लिए Aspose.PSD का उपयोग करके पूरी प्रक्रिया से गुजारेगा, आपके वातावरण को सेट करने से लेकर विस्तृत EXIF डेटा निकालने तक। चलिए शुरू करते हैं!
## आवश्यक शर्तें
इससे पहले कि हम कोड में उतरें, कुछ चीजें हैं जिन्हें आपको ध्यान में रखना होगा:
1.  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपकी मशीन पर JDK इंस्टॉल है। आप इसे यहाँ से डाउनलोड कर सकते हैं[Oracle JDK वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java: लाइब्रेरी को यहाँ से डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/).
3. एकीकृत विकास वातावरण (आईडीई): इंटेलीज आईडीईए, एक्लिप्स या नेटबीन्स जैसे आईडीई कोडिंग को अधिक सुविधाजनक बना देंगे।
4. PSD फ़ाइल: EXIF डेटा वाली PSD फ़ाइल। आप इस ट्यूटोरियल में दिए गए नमूने या EXIF टैग वाली किसी अन्य PSD फ़ाइल का उपयोग कर सकते हैं।
## पैकेज आयात करें
सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक Aspose.PSD पैकेज आयात करने होंगे। इसे सेट अप करने का तरीका यहां बताया गया है।
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## चरण 1: PSD छवि लोड करें
आरंभ करने के लिए, आपको अपनी PSD फ़ाइल को एप्लिकेशन में लोड करना होगा। सुनिश्चित करें कि आपकी फ़ाइल पथ सही ढंग से निर्दिष्ट है।
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 इस चरण में, हम PSD फ़ाइल को लोड करते हैं`Image.load()` विधि.`PsdImage` क्लास का उपयोग PSD छवि को दर्शाने के लिए किया जाता है, और हम PSD-विशिष्ट कार्यात्मकताओं तक पहुंचने के लिए लोड की गई छवि को इस क्लास में डालते हैं।
## चरण 2: छवि संसाधनों पर पुनरावृति करें
अब, हमें थंबनेल संसाधन को खोजने के लिए छवि संसाधनों पर पुनरावृति करने की आवश्यकता है, जिसमें आमतौर पर EXIF डेटा होता है।
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // आगे की प्रक्रिया यहां की जाएगी
    }
}
```
 हम छवि संसाधनों के माध्यम से लूप का उपयोग करते हैं`for` लूप। लक्ष्य उन संसाधनों की पहचान करना है जो इसके उदाहरण हैं`ThumbnailResource` या`Thumbnail4Resource`, क्योंकि ये वे प्रकार हैं जो EXIF डेटा रखते हैं।
## चरण 3: EXIF डेटा निकालें
एक बार जब हम थंबनेल संसाधन की पहचान कर लेते हैं, तो हम EXIF डेटा निकालते हैं और उसे कंसोल पर प्रिंट करते हैं।
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```
 हम एक का उपयोग करते हैं`if` यह जाँचने के लिए कथन कि क्या संसाधन इसका उदाहरण है`ThumbnailResource` यदि ऐसा है, तो हम इसे डालते हैं और इसे पुनः प्राप्त करते हैं`JpegOptions` तक पहुंचने के लिए`ExifData`अंत में, हम विभिन्न EXIF टैग जैसे कि व्हाइटबैलेंस, पिक्सेल आयाम, ISOSpeed और फोकललेंथ को प्रिंट करते हैं।

## निष्कर्ष
इन चरणों का पालन करके, आपने सीखा है कि Aspose.PSD for Java का उपयोग करके PSD छवि से विशिष्ट EXIF टैग कैसे पढ़ें। इस प्रक्रिया में छवि को लोड करना, उसके संसाधनों पर पुनरावृत्ति करना, थंबनेल संसाधन की पहचान करना और EXIF डेटा निकालना शामिल है। इस ज्ञान के साथ, अब आप अपनी PSD फ़ाइलों में EXIF डेटा का पता लगा सकते हैं और उसमें हेरफेर कर सकते हैं, जिससे अधिक परिष्कृत छवि प्रसंस्करण कार्य सक्षम हो सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### EXIF डेटा क्या है?
EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) डेटा, इमेज फाइलों में सन्निहित मेटाडेटा है, जिसमें कैमरा सेटिंग्स, दिनांक और समय, तथा इमेज आयाम जैसी जानकारी शामिल होती है।
### क्या मैं Aspose.PSD का उपयोग करके EXIF डेटा संपादित कर सकता हूँ?
हां, Aspose.PSD आपको EXIF डेटा पढ़ने और संशोधित करने की अनुमति देता है। आप टैग अपडेट कर सकते हैं और परिवर्तनों को वापस इमेज फ़ाइल में सहेज सकते हैं।
### क्या Java के लिए Aspose.PSD निःशुल्क है?
 Aspose.PSD एक निःशुल्क परीक्षण संस्करण प्रदान करता है जिसे आप डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/)पूर्ण सुविधाओं के लिए, आपको लाइसेंस खरीदना होगा।
### Aspose.PSD अन्य कौन से प्रारूपों का समर्थन करता है?
Aspose.PSD विभिन्न Adobe Photoshop प्रारूपों का समर्थन करता है, जिसमें PSD, PSB, और बहुत कुछ शामिल है। यह इन प्रारूपों को PNG, JPEG, TIFF, आदि जैसे अन्य प्रारूपों में बदलने के विकल्प भी प्रदान करता है।
### मैं Aspose.PSD के लिए समर्थन कैसे प्राप्त करूं?
 आप Aspose.PSD के माध्यम से सहायता प्राप्त कर सकते हैं[मंच](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
