---
title: PSD में ह्यू संतृप्ति समायोजन परत जोड़ें
linktitle: PSD में ह्यू संतृप्ति समायोजन परत जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: इस विस्तृत, चरण-दर-चरण ट्यूटोरियल में Aspose.PSD for Java का उपयोग करके PSD में ह्यू सैचुरेशन एडजस्टमेंट लेयर्स जोड़ने का तरीका जानें। अपने ग्राफ़िक डिज़ाइन वर्कफ़्लो को बेहतर बनाएँ।
type: docs
weight: 14
url: /hi/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## परिचय
जब ग्राफिक डिज़ाइन की बात आती है, तो रंग हेरफेर एक महत्वपूर्ण भूमिका निभाता है - विशेष रूप से, रंग, संतृप्ति और हल्कापन में बदलाव किसी भी छवि के मूड और गुणवत्ता को काफी हद तक बदल सकता है। इसे प्राप्त करने का एक प्रभावी तरीका फ़ोटोशॉप (PSD फ़ाइलों) में समायोजन परतों का उपयोग करना है। यदि आप जावा का उपयोग करके प्रोग्रामेटिक रूप से अपनी PSD फ़ाइलों को बेहतर बनाना चाहते हैं, तो Aspose.PSD लाइब्रेरी आपकी मदद के लिए यहाँ है! यह ट्यूटोरियल आपको अपनी PSD फ़ाइलों में ह्यू संतृप्ति समायोजन परत जोड़ने के चरणों के माध्यम से ले जाएगा, जिससे आपके वर्कफ़्लो अधिक उत्पादक और कुशल बनेंगे।
इस गाइड में, हम आवश्यक पैकेजों को आयात करने से लेकर कोड उदाहरणों के विस्तृत विवरण तक सब कुछ कवर करेंगे।
## आवश्यक शर्तें
इससे पहले कि हम कोड में प्रवेश करें, सुनिश्चित करें कि आपके पास निम्नलिखित मौजूद हैं:
1.  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके मशीन पर JDK 8 या उससे ऊपर का संस्करण इंस्टॉल है। आप इसे यहाँ से डाउनलोड कर सकते हैं[जावा SE डेवलपमेंट किट डाउनलोड](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java लाइब्रेरी: आपके पास Aspose.PSD लाइब्रेरी होनी चाहिए, जिसे आप[यहाँ से डाउनलोड करें](https://releases.aspose.com/psd/java/). 
3. IDE: जावा विकास के लिए IntelliJ IDEA या Eclipse जैसा उपयुक्त एकीकृत विकास वातावरण (IDE)।
4. बुनियादी जावा ज्ञान: जावा प्रोग्रामिंग से परिचित होना एक लाभ है, लेकिन चिंता न करें; हम आपको चरण दर चरण कोड समझाएंगे।
अब जब हमने अपनी पूर्व-आवश्यकताओं को सुलझा लिया है, तो चलिए मज़ेदार भाग की ओर बढ़ते हैं - कोडिंग!
## पैकेज आयात करें
Aspose.PSD लाइब्रेरी के साथ काम करना शुरू करने के लिए, पहला कदम आवश्यक क्लासेस को आयात करना है। यहाँ बताया गया है कि आप इसे अपनी जावा फ़ाइल में कैसे कर सकते हैं:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
सुनिश्चित करें कि आपने अपनी परियोजना में उपयुक्त लाइब्रेरीज़ जोड़ी हैं ताकि ये आयात निर्बाध रूप से काम करें।
## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें
हर प्रोजेक्ट को एक शुरुआती बिंदु की आवश्यकता होती है, और हमारा भी कोई अपवाद नहीं है। आपको एक निर्देशिका निर्दिष्ट करने की आवश्यकता है जहाँ आपकी PSD फ़ाइलें संग्रहीत हैं। छवियों को ठीक से लोड करने और सहेजने के लिए यह महत्वपूर्ण है।
```java
String dataDir = "Your Document Directory"; // इस पथ को अपनी वास्तविक निर्देशिका में अपडेट करें
```
## चरण 2: मौजूदा PSD फ़ाइल लोड करें
किसी मौजूदा PSD फ़ाइल में बदलाव करने के लिए, हमें सबसे पहले उसे अपने प्रोग्राम में लोड करना होगा। आप ऐसा कैसे कर सकते हैं:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 इस कोड में, अद्यतन करें`"HueSaturationAdjustmentLayer.psd"` अपनी मौजूदा PSD फ़ाइल के नाम पर क्लिक करें जिसे आप संपादित करना चाहते हैं।
## चरण 3: ह्यू/संतृप्ति परत को संपादित करें
इसके बाद, हम अपनी लोड की गई PSD छवि की परतों के माध्यम से लूप करेंगे ताकि किसी भी मौजूदा ह्यू/संतृप्ति परतों को ढूंढा और संपादित किया जा सके। इस चरण में ह्यू, संतृप्ति और लाइटनेस मानों को संशोधित करना शामिल है।
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
इस उदाहरण में:
- हम रंग को -25, संतृप्ति को -12, तथा चमक को +67 पर समायोजित कर रहे हैं।
- `getRange(2)` यह विधि हमें इच्छानुसार विशिष्ट रंग श्रेणियों में परिवर्तन करने की अनुमति देती है।
## चरण 4: संशोधित PSD फ़ाइल सहेजें
समायोजन करने के बाद, अगला चरण फ़ाइल को सहेजना है। यह हमारी प्रक्रिया का एक महत्वपूर्ण हिस्सा है, यह सुनिश्चित करना कि हमारे द्वारा किए गए परिवर्तन नष्ट न हों।
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## चरण 5: एक नई ह्यू/संतृप्ति परत जोड़ें
इसके बाद, आप किसी दूसरी PSD फ़ाइल में एक नई ह्यू/सैचुरेशन एडजस्टमेंट लेयर जोड़ना चाह सकते हैं। बस उसी तरीके को अपनाएँ जो आपने पहले इस्तेमाल किया था, लेकिन अलग PSD फ़ाइलों के साथ।
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## चरण 6: नई परत के लिए नया ह्यू/संतृप्ति मान सेट करें
अब जब आपने यह नई परत बना ली है, तो पहले की तरह ही वांछित रंग, संतृप्ति और चमक सेटिंग्स लागू करें।
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## चरण 7: अपडेट की गई PSD फ़ाइल को सेव करें
अंत में, PSD फ़ाइल को जोड़े गए Hue/Saturation परत के साथ सेव करें ताकि आप अपने परिवर्तन देख सकें।
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
बधाई हो! आपने Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में सफलतापूर्वक हेरफेर किया है। अब, आप अलग-अलग छवियों और गहन परिवर्तनों के साथ प्रयोग कर सकते हैं, जिससे आपके ग्राफ़िक डिज़ाइन प्रोजेक्ट जीवंत हो उठेंगे।
## निष्कर्ष
प्रोग्रामेटिक रूप से ग्राफ़िक्स के साथ काम करने से संभावनाओं की एक दुनिया खुल जाती है। ह्यू सैचुरेशन एडजस्टमेंट लेयर्स को जोड़ने और संशोधित करने के लिए जावा के लिए Aspose.PSD का उपयोग करने से लचीलापन और दक्षता मिलती है जो आपके डिज़ाइन वर्कफ़्लो को सुव्यवस्थित कर सकती है। चाहे आप किसी प्रोजेक्ट के लिए फ़ोटो को बेहतर बना रहे हों या शानदार विज़ुअल कंटेंट बना रहे हों, इन टूल में महारत हासिल करने से आपका आउटपुट काफी बेहतर हो सकता है।
 Aspose.PSD की अधिक कार्यक्षमताओं का पता लगाने के लिए स्वतंत्र महसूस करें[प्रलेखन](https://reference.aspose.com/psd/java/) या एक छीनने पर विचार करें[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) पुस्तकालय की पूरी शक्ति का परीक्षण करने के लिए।
## अक्सर पूछे जाने वाले प्रश्न
### ह्यू संतृप्ति समायोजन परत क्या है?
ह्यू संतृप्ति समायोजन परत आपको मूल पिक्सेल को स्थायी रूप से परिवर्तित किए बिना किसी छवि के रंग गुणों को संशोधित करने की अनुमति देती है।
### क्या मुझे Aspose.PSD का उपयोग करने के लिए फ़ोटोशॉप स्थापित करने की आवश्यकता है?
नहीं, Aspose.PSD एक स्टैंडअलोन लाइब्रेरी है जो फ़ोटोशॉप से स्वतंत्र रूप से काम करती है।
### क्या मैं बैच प्रोसेसिंग के लिए Aspose.PSD का उपयोग कर सकता हूँ?
हां, आप Aspose.PSD के साथ कई PSD फ़ाइलों को स्वचालित और बैच प्रक्रिया कर सकते हैं।
### क्या Aspose.PSD निःशुल्क है?
Aspose.PSD निःशुल्क परीक्षण प्रदान करता है, लेकिन दीर्घकालिक उपयोग के लिए लाइसेंस की आवश्यकता होती है। आप मूल्य निर्धारण देख सकते हैं[यहाँ](https://purchase.aspose.com/buy).