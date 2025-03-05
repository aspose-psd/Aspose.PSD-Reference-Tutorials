---
title: जावा में JPEG EXIF टैग पढ़ें और संशोधित करें
linktitle: जावा में JPEG EXIF टैग पढ़ें और संशोधित करें
second_title: Aspose.PSD जावा एपीआई
description: इस चरण-दर-चरण मार्गदर्शिका में जानें कि Aspose.PSD for Java का उपयोग करके JPEG EXIF टैग को कैसे पढ़ा और संशोधित किया जाए। उन डेवलपर्स के लिए बिल्कुल सही है जो आसानी से इमेज मेटाडेटा को संभालना चाहते हैं।
type: docs
weight: 18
url: /hi/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---
## परिचय
नमस्ते! क्या आपने कभी सोचा है कि आप Java का उपयोग करके JPEG EXIF टैग को कैसे पढ़ और संशोधित कर सकते हैं? यदि हाँ, तो आप सही जगह पर हैं! यह ट्यूटोरियल आपको Java के लिए Aspose.PSD का उपयोग करके चरण-दर-चरण प्रक्रिया के माध्यम से मार्गदर्शन करेगा। चाहे आप एक अनुभवी डेवलपर हों या नौसिखिया, इस गाइड के अंत तक, आप एक प्रो की तरह JPEG EXIF टैग को संभालने में सक्षम होंगे। तो, चलो शुरू करते हैं!
## आवश्यक शर्तें
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:
1.  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK इंस्टॉल है। आप इसे यहाँ से डाउनलोड कर सकते हैं[ओरेकल वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java लाइब्रेरी: आपको Aspose.PSD for Java लाइब्रेरी डाउनलोड करनी होगी। इसे यहाँ से प्राप्त करें[Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/).
3. एकीकृत विकास वातावरण (आईडीई): इंटेलीज आईडिया या एक्लिप्स जैसा आईडीई आपके कोडिंग अनुभव को आसान बना देगा।
4. बुनियादी जावा ज्ञान: इस ट्यूटोरियल का अनुसरण करने के लिए जावा की बुनियादी समझ आवश्यक है।
## पैकेज आयात करें
सबसे पहले, आइए आवश्यक पैकेज आयात करें। अपना Java IDE खोलें और एक नया Java प्रोजेक्ट बनाएँ। फिर, अपनी प्रोजेक्ट निर्भरताओं में Aspose.PSD for Java लाइब्रेरी शामिल करें।
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## चरण 1: PSD छवि लोड करें
इस चरण में, हम PSD छवि लोड करेंगे जिससे हम EXIF डेटा पढ़ना चाहते हैं। सुनिश्चित करें कि आपकी छवि सही निर्देशिका में है।
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## चरण 2: छवि संसाधनों पर पुनरावृति करें
एक बार छवि लोड हो जाने के बाद, अगला चरण थंबनेल संसाधन को खोजने के लिए उसके संसाधनों पर पुनरावृति करना है, जिसमें आमतौर पर EXIF डेटा होता है।
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // अगले चरण पर आगे बढ़ें
    }
}
```
## चरण 3: EXIF डेटा निकालें
अब जब हमारे पास थंबनेल संसाधन है, तो हम इससे EXIF डेटा निकाल सकते हैं। EXIF डेटा में कैमरा मालिक का नाम, एपर्चर मान, ओरिएंटेशन और बहुत कुछ जैसी मूल्यवान जानकारी शामिल होती है।
```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```
## चरण 4: EXIF डेटा संशोधित करें
EXIF डेटा पढ़ने के बाद, आप इसके कुछ फ़ील्ड को संशोधित करना चाह सकते हैं। यहाँ बताया गया है कि आप यह कैसे कर सकते हैं:
```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```
## चरण 5: परिवर्तन सहेजें
अंत में, EXIF डेटा को संशोधित करने के बाद, परिवर्तनों को एक नई PSD फ़ाइल में सहेजें।
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## निष्कर्ष
और अब यह आपके लिए है! इन चरणों का पालन करके, आप आसानी से Aspose.PSD for Java का उपयोग करके JPEG EXIF टैग को पढ़ और संशोधित कर सकते हैं। यह शक्तिशाली लाइब्रेरी इमेज मेटाडेटा को संभालना आसान बनाती है। तो, आगे बढ़ें और इसे अपने प्रोजेक्ट पर आज़माएँ। हैप्पी कोडिंग!
## अक्सर पूछे जाने वाले प्रश्न
### EXIF डेटा क्या है?
EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) डेटा में किसी छवि के बारे में मेटाडेटा होता है, जैसे कैमरा सेटिंग्स और ओरिएंटेशन।
### क्या मैं Java के लिए Aspose.PSD का निःशुल्क उपयोग कर सकता हूँ?
 आप यहां से निःशुल्क परीक्षण प्राप्त कर सकते हैं[Aspose रिलीज़ पेज](https://releases.aspose.com/).
### क्या Aspose.PSD for Java, Java के सभी संस्करणों के साथ संगत है?
Aspose.PSD for Java, Java SE 7 और इसके बाद के संस्करण का समर्थन करता है।
### मैं Java के लिए Aspose.PSD पर अधिक दस्तावेज़ कहां पा सकता हूं?
 इसकी जाँच पड़ताल करो[प्रलेखन](https://reference.aspose.com/psd/java/) अधिक जानकारी के लिए.
### मैं Java के लिए Aspose.PSD का समर्थन कैसे प्राप्त करूं?
 आप यहाँ से सहायता प्राप्त कर सकते हैं[Aspose PSD समर्थन मंच](https://forum.aspose.com/c/psd/34).