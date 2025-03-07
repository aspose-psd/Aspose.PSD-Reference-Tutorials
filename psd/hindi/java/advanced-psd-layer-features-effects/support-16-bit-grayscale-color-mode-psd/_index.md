---
title: PSD में 16-बिट ग्रेस्केल रंग मोड का समर्थन - जावा
linktitle: PSD में 16-बिट ग्रेस्केल रंग मोड का समर्थन - जावा
second_title: Aspose.PSD जावा एपीआई
description: इस विस्तृत चरण-दर-चरण ट्यूटोरियल के साथ जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में 16-बिट ग्रेस्केल रंग मोड को लागू करना सीखें।
weight: 11
url: /hi/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में 16-बिट ग्रेस्केल रंग मोड का समर्थन - जावा

## परिचय
जब आप ग्राफिक डिज़ाइन और इमेज मैनिपुलेशन की दुनिया में गोता लगा रहे हों, तो अलग-अलग रंग मोड के साथ काम करना समझना एक गुप्त हथियार होने जैसा है। विशेष रूप से, 16-बिट ग्रेस्केल एक गेम-चेंजर हो सकता है, जो आपकी छवियों को वह आश्चर्यजनक गहराई और विवरण देता है जो वास्तव में उन्हें पॉप बनाता है। तो, क्या आप जावा के लिए Aspose.PSD का उपयोग करके इस शक्तिशाली सुविधा का पता लगाने के लिए तैयार हैं? यदि आपके पास अपना कोडिंग गियर तैयार है, तो चलिए सीधे इसमें कूदते हैं।
## आवश्यक शर्तें
शुरू करने से पहले, आइए सुनिश्चित करें कि इस ट्यूटोरियल से सर्वश्रेष्ठ लाभ उठाने के लिए आपके पास सब कुछ सेट है। आपको ये चीज़ें चाहिए होंगी:
1. जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके पास JDK का नवीनतम संस्करण स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं[ओरेकल की साइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Library: यह वह है जिसका उपयोग हम PSD फ़ाइलों में हेरफेर करने के लिए करेंगे। आप इसे यहाँ से प्राप्त कर सकते हैं[Aspose डाउनलोड पृष्ठ](https://releases.aspose.com/psd/java/).
3. एक एकीकृत विकास वातावरण (IDE): जावा का समर्थन करने वाला कोई भी IDE काम करेगा। लोकप्रिय विकल्पों में IntelliJ IDEA, Eclipse, या यहाँ तक कि Visual Studio Code शामिल हैं।
4. जावा का बुनियादी ज्ञान: जावा प्रोग्रामिंग से परिचित होना निश्चित रूप से आपको सुचारू रूप से आगे बढ़ने में मदद करेगा।
5. सैंपल PSD फ़ाइल: सुनिश्चित करें कि आपके पास एक PSD फ़ाइल है जिसके साथ आप काम करना चाहते हैं। यदि आपके पास एक नहीं है, तो आप Adobe Photoshop जैसे सॉफ़्टवेयर का उपयोग करके एक सरल PSD बना सकते हैं, या ऑनलाइन सैंपल फ़ाइलों की तलाश कर सकते हैं।
तैयार हैं? बढ़िया! चलिए आवश्यक पैकेज आयात करते हैं और कोडिंग शुरू करते हैं।
## पैकेज आयात करें
काम शुरू करने के लिए, आइए उन प्रासंगिक पैकेजों को आयात करें जिनकी हमें Aspose.PSD for Java के साथ काम करने के लिए आवश्यकता होगी। अपनी Java फ़ाइल में निम्न पंक्तियाँ जोड़ें:
```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```
ये आयात आपको उन कार्यात्मकताओं तक पहुंच प्रदान करते हैं जिनका उपयोग आप PSD फाइलों में हेरफेर करने, ग्राफिक्स बनाने और विभिन्न प्रारूपों में छवियों को सहेजने के लिए करेंगे।
## चरण 1: अपनी निर्देशिकाएँ परिभाषित करें
सबसे पहली चीज़ जो आपको करनी है वह है अपनी सोर्स और आउटपुट निर्देशिकाएँ सेट करना। यहीं से आपकी PSD फ़ाइलें लोड की जाएँगी और सेव की जाएँगी। यहाँ बताया गया है कि आप यह कैसे कर सकते हैं:
```java
String sourceDir = "Your Source Directory"; // अपनी स्रोत निर्देशिका में बदलें
String outputDir = "Your Document Directory"; // अपनी आउटपुट निर्देशिका में परिवर्तन करें
```
सुनिश्चित करें कि "आपकी स्रोत निर्देशिका" और "आपकी दस्तावेज़ निर्देशिका" को आपके कंप्यूटर पर वास्तविक पथों से प्रतिस्थापित किया जाए जहां आपकी PSD फ़ाइलें स्थित हैं और जहां आप संसाधित फ़ाइलों को सहेजना चाहते हैं।
## चरण 2: छवि प्रसंस्करण को संभालने के लिए एक विधि बनाएं
अब हम PSD फ़ाइलों की प्रोसेसिंग को संभालने के लिए एक विधि तैयार करने जा रहे हैं। यह विधि PSD फ़ाइल और ग्रेस्केल प्रक्रिया की विशेषताओं की पहचान करने के लिए कई पैरामीटर लेगी।
```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```
यह विधि आपको फ़ाइल नाम, रंग मोड, बिट काउंट, चैनल काउंट, संपीड़न विधि और परत संख्या निर्दिष्ट करने की अनुमति देती है। हम इस विधि की कार्यक्षमता को चरण दर चरण विभाजित करेंगे!
## चरण 3: फ़ाइल पथ परिभाषित करें और PSD लोड करें
अपनी विधि के अंदर, आइए परिभाषित करें कि फ़ाइल पथ का निर्माण कैसे करें और वास्तव में PSD छवि को कैसे लोड करें:
```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// पूर्वनिर्धारित 16-बिट ग्रेस्केल PSD लोड करें
PsdImage image = (PsdImage)Image.load(filePath);
```
यहां, हम उस PSD फ़ाइल के लिए आवश्यक पथों का निर्माण करते हैं, जिसके साथ हम काम करेंगे, साथ ही संशोधित PSD और PNG फ़ाइलों को सहेजने की तैयारी भी करेंगे।
## चरण 4: परत या पूर्ण छवि को संसाधित करें
इसके बाद, आपको या तो चयनित परत या पूरी छवि पर रेखाचित्र बनाना होगा, और उसके चारों ओर एक ग्रे बॉर्डर जोड़ना होगा। यह दृश्यता बढ़ाने और छवि में थोड़ा आकर्षण जोड़ने का एक शानदार तरीका है।
```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // परत की परिधि के चारों ओर एक ग्रे आंतरिक बॉर्डर बनाएं
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```
इस भाग में, आप ड्राइंग संदर्भ बनाने के लिए Aspose से Graphics क्लास का उपयोग कर रहे हैं। आयत के आयामों की गणना आपकी छवि के आकार के आधार पर की जाती है, यह सुनिश्चित करते हुए कि यह केंद्र में पूरी तरह से आकर्षित हो।
## चरण 5: संशोधित PSD फ़ाइल सहेजें
एक बार जब आप ड्राइंग समाप्त कर लेते हैं, तो अपने संशोधनों को एक नई PSD फ़ाइल में सहेजने का समय आ जाता है। यह वह जगह है जहाँ आप पहले निर्दिष्ट किए गए विकल्प सेट करते हैं।
```java
    // विशिष्ट विशेषताओं के साथ PSD की एक प्रति सहेजें
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```
PSD के लिए विकल्प सेट करके, आप इस बात पर नियंत्रण बनाए रखते हैं कि आपकी छवि सहेजे जाने पर कैसा व्यवहार करेगी। यह सुनिश्चित करता है कि सभी सूक्ष्म विवरण संरक्षित हैं।
## चरण 6: PSD को PNG में बदलें
सबसे बड़ी बात तब होती है जब आप अपने नए सहेजे गए PSD को PNG प्रारूप में परिवर्तित करते हैं, जो विशेष रूप से अल्फा के साथ ग्रेस्केल के लिए डिज़ाइन किया गया है।
```java
finally {
    image.dispose();
}
// सहेजे गए PSD को लोड करें
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // सहेजे गए PSD को ग्रेस्केल PNG छवि में बदलें
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // यहाँ कोई अपवाद नहीं होना चाहिए
}
finally {
    image1.dispose();
}
```
रूपांतरण प्रक्रिया सरल है और यह सुनिश्चित करती है कि आपकी छवि विभिन्न अनुप्रयोगों में उपयोग के लिए या ऑनलाइन साझा करने के लिए तैयार है।
## निष्कर्ष
और अब आपके पास यह है - Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में 16-बिट ग्रेस्केल रंग मोड का समर्थन करने के तरीके पर एक संपूर्ण मार्गदर्शिका! आपने सीखा है कि अपने परिवेश को कैसे सेट अप करें, छवियों को कैसे प्रोसेस करें, और यहां तक कि उन्हें विभिन्न प्रारूपों में निर्यात करें। क्या यह आश्चर्यजनक नहीं है कि कोड की कुछ पंक्तियाँ इतने सुंदर परिणाम कैसे दे सकती हैं?
इस तरह की छवियों में हेरफेर करने की क्षमता के साथ, कौन जानता है कि आप किस रोमांच पर निकल सकते हैं? चाहे वह मौजूदा डिज़ाइन को बेहतर बनाना हो या बिल्कुल नई उत्कृष्ट कृतियाँ बनाना हो - आपकी कल्पना की कोई सीमा नहीं है!

## अक्सर पूछे जाने वाले प्रश्न
### 16-बिट ग्रेस्केल रंग मोड क्या है?
16-बिट ग्रेस्केल, मानक 8-बिट की तुलना में रंगों की अधिक व्यापक रेंज की अनुमति देता है, जिसके परिणामस्वरूप अधिक विस्तृत चित्र प्राप्त होते हैं।
### क्या मैं गैर-ग्रेस्केल छवियों के लिए Aspose.PSD का उपयोग कर सकता हूं?
बिल्कुल! Aspose.PSD विभिन्न रंग मोड का समर्थन करता है, इसलिए आप RGB, CMYK और अन्य के साथ भी काम कर सकते हैं।
### क्या Aspose.PSD का कोई परीक्षण संस्करण उपलब्ध है?
 हां, आप Aspose.PSD का निःशुल्क परीक्षण संस्करण आज़मा सकते हैं। बस यहाँ जाएँ[Aspose डाउनलोड पृष्ठ](https://releases.aspose.com/).
### मैं Aspose.PSD के उपयोग के और अधिक उदाहरण कहां पा सकता हूं?
 आप इसकी जांच कर सकते हैं[प्रलेखन](https://reference.aspose.com/psd/java/) अधिक गहन उदाहरणों और ट्यूटोरियल्स के लिए.
### मैं Aspose.PSD के लिए लाइसेंस कैसे खरीदूं?
 आप यहां जाकर लाइसेंस खरीद सकते हैं[Aspose खरीद पृष्ठ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
