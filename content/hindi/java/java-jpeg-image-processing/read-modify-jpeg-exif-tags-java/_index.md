---
title: जावा में JPEG EXIF टैग पढ़ें और संशोधित करें
linktitle: जावा में JPEG EXIF टैग पढ़ें और संशोधित करें
second_title: Aspose.PSD जावा एपीआई
description: इस चरण-दर-चरण मार्गदर्शिका में जावा के लिए Aspose.PSD का उपयोग करके JPEG EXIF टैग को पढ़ने और संशोधित करने का तरीका जानें। उन डेवलपर्स के लिए बिल्कुल सही जो छवि मेटाडेटा को सहजता से संभालना चाहते हैं।
type: docs
weight: 18
url: /hi/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---
## परिचय
सुनो! क्या आपने कभी सोचा है कि आप जावा का उपयोग करके JPEG EXIF टैग को कैसे पढ़ और संशोधित कर सकते हैं? यदि हां, तो आप सही जगह पर हैं! यह ट्यूटोरियल जावा के लिए Aspose.PSD का उपयोग करके चरण-दर-चरण प्रक्रिया में आपका मार्गदर्शन करेगा। चाहे आप एक अनुभवी डेवलपर हों या नौसिखिया, इस गाइड के अंत तक, आप एक पेशेवर की तरह JPEG EXIF टैग को संभालने में सक्षम होंगे। तो, आइए गोता लगाएँ!
## आवश्यक शर्तें
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:
1.  जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[ओरेकल वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  जावा लाइब्रेरी के लिए Aspose.PSD: आपको जावा लाइब्रेरी के लिए Aspose.PSD डाउनलोड करना होगा। से प्राप्त करें[Aspose ने पृष्ठ जारी किया](https://releases.aspose.com/psd/java/).
3. इंटीग्रेटेड डेवलपमेंट एनवायरनमेंट (आईडीई): IntelliJ IDEA या Eclipse जैसा IDE आपके कोडिंग अनुभव को आसान बना देगा।
4. बुनियादी जावा ज्ञान: इस ट्यूटोरियल का अनुसरण करने के लिए जावा की बुनियादी समझ आवश्यक है।
## पैकेज आयात करें
सबसे पहले चीज़ें, आइए आवश्यक पैकेज आयात करें। अपना जावा आईडीई खोलें और एक नया जावा प्रोजेक्ट बनाएं। फिर, अपने प्रोजेक्ट निर्भरता में जावा लाइब्रेरी के लिए Aspose.PSD को शामिल करें।
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## चरण 1: PSD छवि लोड करें
इस चरण में, हम PSD छवि लोड करेंगे जिससे हम EXIF डेटा पढ़ना चाहते हैं। सुनिश्चित करें कि आपकी छवि सही निर्देशिका में है.
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
एक बार छवि लोड हो जाने के बाद, अगला कदम थंबनेल संसाधन खोजने के लिए इसके संसाधनों पर पुनरावृति करना है, जिसमें आमतौर पर EXIF डेटा होता है।
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // अगले चरण पर आगे बढ़ें
    }
}
```
## चरण 3: EXIF डेटा निकालें
अब हमारे पास थंबनेल संसाधन है, हम इससे EXIF डेटा निकाल सकते हैं। EXIF डेटा में कैमरा मालिक का नाम, एपर्चर मान, ओरिएंटेशन और बहुत कुछ जैसी मूल्यवान जानकारी शामिल होती है।
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
## चरण 4: EXIF डेटा को संशोधित करें
EXIF डेटा पढ़ने के बाद, आप इसके कुछ फ़ील्ड को संशोधित करना चाह सकते हैं। यहां बताया गया है कि आप यह कैसे कर सकते हैं:
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
आखिर तुमने इसे हासिल कर ही लिया है! इन चरणों का पालन करके, आप Java के लिए Aspose.PSD का उपयोग करके JPEG EXIF टैग को आसानी से पढ़ और संशोधित कर सकते हैं। यह शक्तिशाली लाइब्रेरी छवि मेटाडेटा को संभालना आसान बनाती है। तो, आगे बढ़ें और इसे अपने प्रोजेक्ट पर आज़माएँ। हैप्पी कोडिंग!
## अक्सर पूछे जाने वाले प्रश्न
### EXIF डेटा क्या है?
EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) डेटा में एक छवि के बारे में मेटाडेटा होता है, जैसे कैमरा सेटिंग्स और ओरिएंटेशन।
### क्या मैं जावा के लिए Aspose.PSD का निःशुल्क उपयोग कर सकता हूँ?
 आप नि:शुल्क परीक्षण प्राप्त कर सकते हैं[Aspose ने पृष्ठ जारी किया](https://releases.aspose.com/).
### क्या जावा के लिए Aspose.PSD जावा के सभी संस्करणों के साथ संगत है?
जावा के लिए Aspose.PSD जावा SE 7 और इसके बाद के संस्करण का समर्थन करता है।
### मुझे Java के लिए Aspose.PSD पर अधिक दस्तावेज़ कहां मिल सकते हैं?
 इसकी जाँच पड़ताल करो[प्रलेखन](https://reference.aspose.com/psd/java/) अधिक जानकारी के लिए।
### मैं जावा के लिए Aspose.PSD के लिए समर्थन कैसे प्राप्त करूं?
 से आपको सहयोग मिल सकता है[Aspose PSD समर्थन मंच](https://forum.aspose.com/c/psd/34).