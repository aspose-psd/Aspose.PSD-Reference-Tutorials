---
title: जावा में EXIF सेगमेंट में थंबनेल जोड़ें
linktitle: जावा में EXIF सेगमेंट में थंबनेल जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: Java के लिए Aspose.PSD का उपयोग करके थंबनेल के साथ छवि मेटाडेटा को बढ़ाने का तरीका जानें। सहज एकीकरण के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 10
url: /hi/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में EXIF सेगमेंट में थंबनेल जोड़ें

## परिचय
इस ट्यूटोरियल में, हम जावा के लिए Aspose.PSD का उपयोग करके EXIF सेगमेंट में थंबनेल जोड़कर छवि मेटाडेटा को बढ़ाने का तरीका जानेंगे। EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) मेटाडेटा डिजिटल फोटोग्राफी में महत्वपूर्ण भूमिका निभाता है, जो कैमरा सेटिंग, तिथि और स्थान जैसी मूल्यवान जानकारी प्रदान करता है। थंबनेल जोड़ने से छवियों का कुशलतापूर्वक पूर्वावलोकन करके उपयोगकर्ता अनुभव में वृद्धि होती है।
## आवश्यक शर्तें
ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:
- जावा प्रोग्रामिंग का बुनियादी ज्ञान.
- आपके सिस्टम पर जावा डेवलपमेंट किट (JDK) स्थापित है।
- जावा के लिए IDE (एकीकृत विकास वातावरण), जैसे कि IntelliJ IDEA या Eclipse.
- Aspose.PSD for Java लाइब्रेरी। आप इसे यहाँ से डाउनलोड कर सकते हैं[Aspose.PSD for Java डाउनलोड पृष्ठ](https://releases.aspose.com/psd/java/).
## पैकेज आयात करें
सबसे पहले, Aspose.PSD और Java से आवश्यक पैकेज आयात करें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
आइए Aspose.PSD का उपयोग करके जावा में EXIF सेगमेंट में थंबनेल जोड़ने की प्रक्रिया को विस्तृत चरणों में विभाजित करें:
## चरण 1: PSD छवि लोड करें
PSD छवि फ़ाइल को PsdImage ऑब्जेक्ट में लोड करें।
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```
## चरण 2: छवि संसाधनों पर पुनरावृति करें
उपयुक्त थंबनेल संसाधन ढूंढने के लिए छवि संसाधनों के माध्यम से पुनरावृति करें।
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // थंबनेल संसाधन को संसाधित करें
    }
}
```
## चरण 3: थंबनेल डेटा समायोजित करें
थम्बनेल डेटा तैयार करें और समायोजित करें.
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // JPEG गुणवत्ता सेट करें
```
## चरण 4: छवि सहेजें
संशोधित छवि को डिस्क पर वापस सहेजें.
```java
image.save(dataDir + "output.psd");
```
## निष्कर्ष
Aspose.PSD का उपयोग करके जावा में EXIF सेगमेंट में थंबनेल जोड़ना एक सीधी प्रक्रिया है जो छवि मेटाडेटा की उपयोगिता को बढ़ाती है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप अपनी छवियों को पूर्वावलोकन थंबनेल के साथ कुशलतापूर्वक समृद्ध कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न
### EXIF मेटाडेटा क्या है?
EXIF मेटाडेटा डिजिटल छवियों में अंतर्निहित जानकारी है जिसमें कैमरा सेटिंग्स, दिनांक और अन्य विवरण शामिल हैं।
### EXIF में थम्बनेल क्यों जोड़ें?
थंबनेल जोड़ने से संपूर्ण छवि को लोड किए बिना त्वरित छवि पूर्वावलोकन की अनुमति देकर उपयोगकर्ता अनुभव में सुधार होता है।
### मैं Java के लिए Aspose.PSD कहां से डाउनलोड कर सकता हूं?
 आप Java के लिए Aspose.PSD को यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
### मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 आप Aspose.PSD के लिए एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
### मैं Aspose.PSD के लिए समर्थन कैसे प्राप्त करूं?
 सहायता के लिए, यहां जाएं[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
