---
title: जावा में विशिष्ट EXIF टैग जानकारी पढ़ें
linktitle: जावा में विशिष्ट EXIF टैग जानकारी पढ़ें
second_title: Aspose.PSD जावा एपीआई
description: हमारे चरण-दर-चरण ट्यूटोरियल के साथ जावा के लिए Aspose.PSD का उपयोग करके PSD छवियों से विशिष्ट EXIF टैग पढ़ना सीखें। अपने छवि प्रसंस्करण कौशल को बढ़ाएं।
type: docs
weight: 19
url: /hi/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
---
## परिचय
क्या आप जावा के साथ PSD फ़ाइल हेरफेर की दुनिया में गोता लगाना चाह रहे हैं? यदि आप समझना चाहते हैं कि PSD छवियों से विशिष्ट EXIF टैग कैसे पढ़ें, तो आप सही जगह पर हैं। यह ट्यूटोरियल आपको जावा के लिए Aspose.PSD का उपयोग करके आपके वातावरण को स्थापित करने से लेकर विस्तृत EXIF डेटा निकालने तक की पूरी प्रक्रिया के बारे में बताएगा। आएँ शुरू करें!
## आवश्यक शर्तें
इससे पहले कि हम कोड के बारे में गहराई से जानें, आपको कुछ चीज़ें ध्यान में रखनी होंगी:
1.  जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपकी मशीन पर जेडीके स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[ओरेकल जेडीके वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  जावा के लिए Aspose.PSD: यहां से लाइब्रेरी डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/).
3. एकीकृत विकास पर्यावरण (आईडीई): IntelliJ IDEA, Eclipse, या NetBeans जैसी IDE कोडिंग को अधिक सुविधाजनक बनाएगी।
4. PSD फ़ाइल: EXIF डेटा के साथ एक PSD फ़ाइल। आप इस ट्यूटोरियल में दिए गए नमूने या EXIF टैग के साथ किसी अन्य PSD फ़ाइल का उपयोग कर सकते हैं।
## पैकेज आयात करें
सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक Aspose.PSD पैकेज आयात करने की आवश्यकता होगी। यहां बताया गया है कि इसे कैसे सेट अप करें।
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## चरण 1: PSD छवि लोड करें
आरंभ करने के लिए, आपको अपनी PSD फ़ाइल को एप्लिकेशन में लोड करना होगा। सुनिश्चित करें कि आपका फ़ाइल पथ सही ढंग से निर्दिष्ट है।
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 इस चरण में, हम इसका उपयोग करके PSD फ़ाइल लोड करते हैं`Image.load()` तरीका।`PsdImage` क्लास का उपयोग PSD छवि का प्रतिनिधित्व करने के लिए किया जाता है, और हम PSD-विशिष्ट कार्यात्मकताओं तक पहुंचने के लिए लोड की गई छवि को इस क्लास में डालते हैं।
## चरण 2: छवि संसाधनों पर पुनरावृति करें
अब, हमें थंबनेल संसाधन खोजने के लिए छवि संसाधनों पर पुनरावृति करने की आवश्यकता है, जिसमें आमतौर पर EXIF डेटा होता है।
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // आगे की प्रक्रिया यहीं की जाएगी
    }
}
```
 हम a का उपयोग करके छवि संसाधनों के माध्यम से लूप करते हैं`for` कुंडली। लक्ष्य उन संसाधनों की पहचान करना है जो इसके उदाहरण हैं`ThumbnailResource` या`Thumbnail4Resource`, क्योंकि ये वे प्रकार हैं जो EXIF डेटा रखते हैं।
## चरण 3: EXIF डेटा निकालें
एक बार जब हम थंबनेल संसाधन की पहचान कर लेते हैं, तो हम EXIF डेटा निकालते हैं और इसे कंसोल पर प्रिंट करते हैं।
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
 हम एक का उपयोग करते हैं`if` यह जाँचने के लिए कथन कि क्या संसाधन का एक उदाहरण है`ThumbnailResource` . यदि ऐसा है, तो हम इसे डालते हैं और इसे पुनः प्राप्त करते हैं`JpegOptions` तक पहुँचने के लिए`ExifData`अंत में, हम विभिन्न EXIF टैग जैसे व्हाइटबैलेंस, पिक्सेल डाइमेंशन, ISOSpeed, और FocalLength का प्रिंट आउट लेते हैं।

## निष्कर्ष
इन चरणों का पालन करके, आपने जावा के लिए Aspose.PSD का उपयोग करके PSD छवि से विशिष्ट EXIF टैग को पढ़ना सीख लिया है। इस प्रक्रिया में छवि को लोड करना, उसके संसाधनों पर पुनरावृत्ति करना, थंबनेल संसाधन की पहचान करना और EXIF डेटा निकालना शामिल है। इस ज्ञान के साथ, अब आप अधिक परिष्कृत छवि प्रसंस्करण कार्यों को सक्षम करते हुए, अपनी PSD फ़ाइलों में EXIF डेटा का पता लगा सकते हैं और उसमें हेरफेर कर सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### EXIF डेटा क्या है?
EXIF (एक्सचेंजेबल इमेज फाइल फॉर्मेट) डेटा छवि फ़ाइलों के भीतर एम्बेडेड मेटाडेटा है, जिसमें कैमरा सेटिंग्स, दिनांक और समय और छवि आयाम जैसी जानकारी होती है।
### क्या मैं Aspose.PSD का उपयोग करके EXIF डेटा संपादित कर सकता हूँ?
हां, Aspose.PSD आपको EXIF डेटा को पढ़ने और संशोधित करने की अनुमति देता है। आप टैग अपडेट कर सकते हैं और परिवर्तनों को वापस छवि फ़ाइल में सहेज सकते हैं।
### क्या जावा के लिए Aspose.PSD निःशुल्क है?
 Aspose.PSD एक निःशुल्क परीक्षण संस्करण प्रदान करता है जिसे आप डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/). पूर्ण सुविधाओं के लिए, आपको एक लाइसेंस खरीदना होगा।
### Aspose.PSD अन्य किन प्रारूपों का समर्थन करता है?
Aspose.PSD PSD, PSB और अन्य सहित विभिन्न Adobe Photoshop प्रारूपों का समर्थन करता है। यह इन प्रारूपों को पीएनजी, जेपीईजी, टीआईएफएफ इत्यादि जैसे अन्य प्रारूपों में परिवर्तित करने के विकल्प भी प्रदान करता है।
### मैं Aspose.PSD के लिए समर्थन कैसे प्राप्त करूं?
 आप Aspose.PSD के माध्यम से सहायता प्राप्त कर सकते हैं[मंच](https://forum.aspose.com/c/psd/34).