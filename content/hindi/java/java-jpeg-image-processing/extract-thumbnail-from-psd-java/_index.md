---
title: जावा में PSD से थंबनेल निकालें
linktitle: जावा में PSD से थंबनेल निकालें
second_title: Aspose.PSD जावा एपीआई
description: जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों से थंबनेल निकालना सीखें। यह चरण-दर-चरण मार्गदर्शिका सेटअप से लेकर निकाली गई छवियों को सहेजने तक सब कुछ कवर करती है।
type: docs
weight: 15
url: /hi/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## परिचय
इस ट्यूटोरियल में, हम जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों से थंबनेल निकालने का तरीका जानेंगे। थंबनेल त्वरित पूर्वावलोकन के लिए या PSD दस्तावेज़ों में एम्बेडेड छवियों के छोटे संस्करण बनाने के लिए उपयोगी हो सकते हैं। आइए Aspose.PSD का उपयोग करके इसे प्राप्त करने के लिए आवश्यक चरणों के बारे में जानें।
## आवश्यक शर्तें
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित सेटअप है:
- आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
-  जावा लाइब्रेरी के लिए Aspose.PSD। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
- जावा प्रोग्रामिंग का बुनियादी ज्ञान।
## पैकेज आयात करें
आरंभ करने के लिए, अपने जावा क्लास में आवश्यक Aspose.PSD पैकेज शामिल करें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## चरण 1: PSD फ़ाइल लोड करें
सबसे पहले, PSD फ़ाइल लोड करें जिसमें वह थंबनेल है जिसे आप निकालना चाहते हैं।
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 प्रतिस्थापित करें`"Your_Document_Directory/"` उस निर्देशिका पथ के साथ जहां आपकी PSD फ़ाइल स्थित है, और`"your_file.psd"` आपकी PSD फ़ाइल के नाम के साथ।
## चरण 2: छवि संसाधनों पर पुनरावृति करें
थंबनेल संसाधन ढूंढने के लिए छवि संसाधनों के माध्यम से पुनरावृति करें।
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // थंबनेल डेटा निकालें
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // निकाले गए थंबनेल डेटा के साथ एक नई छवि बनाएं
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // निकाले गए थंबनेल को एक अलग JPEG फ़ाइल के रूप में सहेजें
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // आउटपुट सफलता संदेश
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // थंबनेल मिल जाने और संसाधित हो जाने पर लूप से बाहर निकलें
    }
}
```
## चरण 3: निकाले गए थंबनेल को सहेजें
निकाले गए थंबनेल को एक अलग छवि फ़ाइल के रूप में सहेजें (इस मामले में, JPEG फ़ाइल के रूप में)।
## चरण 4: विभिन्न प्रकार के थंबनेल को संभालना
 यदि आपकी PSD फ़ाइल में कई प्रकार के थंबनेल हो सकते हैं, जैसे`Thumbnail4Resource`, आप उन मामलों को समान रूप से संभालने के लिए तर्क का विस्तार कर सकते हैं।

## निष्कर्ष
इस ट्यूटोरियल में, हमने पता लगाया कि जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों से थंबनेल कैसे निकालें। ऊपर बताए गए चरणों का पालन करके, आप अपने PSD दस्तावेज़ों में एम्बेडेड थंबनेल को कुशलतापूर्वक पुनर्प्राप्त और सहेज सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD क्या है?
Aspose.PSD एक जावा लाइब्रेरी है जो डेवलपर्स को PSD और अन्य छवि फ़ाइल स्वरूपों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है।
### मुझे Java के लिए Aspose.PSD पर अधिक दस्तावेज़ कहां मिल सकते हैं?
 आप इसका उल्लेख कर सकते हैं[प्रलेखन](https://reference.aspose.com/psd/java/) विस्तृत एपीआई संदर्भों और उदाहरणों के लिए।
### क्या मैं खरीदने से पहले Aspose.PSD को निःशुल्क आज़मा सकता हूँ?
 हाँ, आप डाउनलोड कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/) पुस्तकालय की क्षमताओं का मूल्यांकन करना।
### मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
 अस्थायी लाइसेंस प्राप्त किया जा सकता है[यहाँ](https://purchase.aspose.com/temporary-license/).
### क्या Aspose.PSD व्यावसायिक उपयोग के लिए उपयुक्त है?
हां, Aspose.PSD का उपयोग इसकी लाइसेंस शर्तों के तहत व्यक्तिगत और व्यावसायिक दोनों परियोजनाओं के लिए किया जा सकता है।