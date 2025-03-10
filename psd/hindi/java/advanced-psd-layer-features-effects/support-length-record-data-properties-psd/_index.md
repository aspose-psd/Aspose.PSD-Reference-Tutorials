---
title: PSD में लंबाई रिकॉर्ड डेटा गुणों का समर्थन करें - जावा
linktitle: PSD में लंबाई रिकॉर्ड डेटा गुणों का समर्थन करें - जावा
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD का उपयोग करके जावा में लंबाई रिकॉर्ड डेटा गुणों के साथ PSD फ़ाइलों में हेरफेर करना सीखें। सभी विवरणों के लिए इस चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 14
url: /hi/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में लंबाई रिकॉर्ड डेटा गुणों का समर्थन करें - जावा

## परिचय
क्या आपने कभी फ़ोटोशॉप फ़ाइलों के साथ काम किया है और प्रोग्रामेटिक रूप से परतों या आकृतियों में हेरफेर करना चाहते हैं? यदि ऐसा है, तो आप Aspose.PSD for Java लाइब्रेरी की खूबसूरती पर ठोकर खा चुके हैं। यह शक्तिशाली उपकरण डेवलपर्स को जावा कोड के माध्यम से PSD फ़ाइलों के साथ सहजता से बातचीत करने और संशोधित करने की अनुमति देता है। आज के लेख में, हम इस लाइब्रेरी का उपयोग करके PSD फ़ाइल में लंबाई रिकॉर्ड डेटा गुणों का समर्थन करने के तरीके के बारे में जानेंगे। 
चाहे आप एक अनुभवी जावा डेवलपर हों या अभी शुरुआत कर रहे हों, यह गाइड आपको वह सब कुछ बताएगा जो आपको जानना चाहिए, चरण दर चरण। अंत में, आप PSD फ़ाइल खोल पाएंगे, इसके वेक्टर आकार गुणों को संशोधित कर पाएंगे, और अपने परिवर्तनों को सहेज पाएंगे - यह सब आपके जावा वातावरण की सुविधा को छोड़े बिना। चलो अपनी आस्तीन ऊपर चढ़ाएँ और कूद पड़ें!
## आवश्यक शर्तें
शुरू करने से पहले, आपको कुछ चीज़ें तैयार रखनी होंगी। यह सुनिश्चित करना कि आपके पास सब कुछ सही जगह पर है, प्रक्रिया को आसान बनाता है, और कोई भी आखिरी समय में भागदौड़ पसंद नहीं करता! आपको ये चीज़ें चाहिए होंगी:
1.  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके मशीन पर JDK इंस्टॉल है। आप इसे यहाँ से डाउनलोड कर सकते हैं[ओरेकल की वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) या पैकेज मैनेजर का उपयोग करें.
2.  Aspose.PSD for Java लाइब्रेरी: आपको अपने प्रोजेक्ट में Aspose.PSD for Java लाइब्रेरी को डाउनलोड करके शामिल करना होगा। इसे यहाँ से प्राप्त करें[Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/).
3. IDE: बेहतर कोड प्रबंधन के लिए IntelliJ IDEA, Eclipse या अपनी पसंद के किसी भी Java IDE जैसे एकीकृत विकास वातावरण (IDE) का उपयोग करें।
4. PSD फ़ाइल: इस ट्यूटोरियल के लिए, आपको काम करने के लिए एक PSD फ़ाइल की आवश्यकता होगी। आप Adobe Photoshop में एक फ़ाइल बना सकते हैं या एक नमूना PSD डाउनलोड कर सकते हैं।
5. बुनियादी जावा ज्ञान: जावा सिंटैक्स से परिचित होने से आपको आसानी से अनुसरण करने में मदद मिलेगी।
## पैकेज आयात करें
अब जब आपने सभी पूर्वापेक्षाएँ सेट कर ली हैं, तो अगला चरण आवश्यक पैकेज आयात करना है। यह चरण उन कक्षाओं और विधियों तक पहुँच प्राप्त करने के लिए महत्वपूर्ण है जिनका हम उपयोग करेंगे। नीचे आपके जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने का एक उदाहरण दिया गया है:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```
इन आयातों के साथ, आप PSD फ़ाइलों में हेरफेर करने के लिए पूरी तरह तैयार हैं!

## चरण 1: अपना स्रोत और आउटपुट निर्देशिका सेट करें
किसी भी फ़ाइल को लोड करने से पहले, आइए यह निर्धारित करें कि हमारी इनपुट PSD फ़ाइल कहाँ से आ रही है और हम संशोधित फ़ाइल को कहाँ सहेजना चाहते हैं। अपनी स्थानीय मशीन के अनुसार निर्देशिका पथ समायोजित करें।
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```
## चरण 2: PSD फ़ाइल लोड करें
 PSD फ़ाइल लोड करने का समय आ गया है! इसके लिए, हम इसका उपयोग करेंगे`Image.load` Aspose.PSD लाइब्रेरी से विधि। यह विधि हमें PSD फ़ाइल खोलने और इसकी परतों और संसाधनों तक पहुँचने की अनुमति देती है।
```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```
यह एक किताब खोलने जैसा है - आप इसके पृष्ठों (परतों और संसाधनों) को ब्राउज़ कर सकेंगे।
## चरण 3: परत में Vsms संसाधन का पता लगाएँ
इसके बाद, हमें अपनी PSD फ़ाइल में विशिष्ट VsmsResource ढूँढ़ना होगा। ये संसाधन वेक्टर आकार परतों के लिए डेटा रखते हैं। यहीं पर जादू होता है! इस स्निपेट में, हम इस संसाधन को खोजने के लिए परत के संसाधनों के माध्यम से लूप करते हैं।
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```
एक खजाने की खोज की तरह, आप बहुमूल्य वेक्टर डेटा को खोजने के लिए परतों के माध्यम से खोज कर रहे हैं!
## चरण 4: लंबाई रिकॉर्ड तक पहुंचें
एक बार जब हमारे पास VsmsResource हो जाता है, तो हम LengthRecord ऑब्जेक्ट्स को निकाल सकते हैं। प्रत्येक LengthRecord वेक्टर आकृतियों के भीतर एक पथ का प्रतिनिधित्व करता है। यहाँ, हम उनके गुणों में हेरफेर करने के लिए तीन LengthRecords तक पहुँचते हैं।
```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```
यह किसी पेंटिंग के किस भाग को संशोधित करना है, इसका चयन करने जैसा है!
## चरण 5: पथ संचालन गुण संशोधित करें
अब आता है मज़ेदार हिस्सा—पथ गुणों को संशोधित करना! यहाँ, setPathOperations विधि यह बदलने की अनुमति देती है कि आकृतियाँ एक दूसरे के साथ कैसे इंटरैक्ट करती हैं। हम ओवरलैपिंग क्षेत्रों को बाहर करने या पीछे से सामने की आकृति को घटाने जैसे ऑपरेशन सेट कर सकते हैं।
```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```
इसे एक केक की परतों को समायोजित करने के रूप में कल्पना करें - प्रत्येक परत आपके द्वारा इसे कैसे काटा जाता है, इसके आधार पर अलग-अलग तरीके से परस्पर क्रिया करती है!
## चरण 6: संशोधित PSD फ़ाइल सहेजें
आवश्यक परिवर्तन करने के बाद, अगला चरण आपकी संशोधित PSD फ़ाइल को सहेजना है। यहीं पर आपकी सारी मेहनत रंग लाती है। 
```java
psdImage.save(outPsdFilePath);
```
आपकी उत्कृष्ट कृति अब दुनिया के देखने के लिए बड़े करीने से पैक की गई है!
## चरण 7: संसाधनों को साफ़ करें
अंत में, मेमोरी और संसाधनों को मुक्त करने के लिए आपके द्वारा उपयोग किए गए ऑब्जेक्ट्स को हटाना महत्वपूर्ण है।
```java
psdImage.dispose();
```
इसे किसी कला परियोजना के बाद अपने कार्यस्थल की सफाई करने के रूप में सोचें - यह सुनिश्चित करना कि सब कुछ साफ-सुथरा हो!
## निष्कर्ष
बस, अब यह हो गया! आपने अभी-अभी Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में लंबाई रिकॉर्ड डेटा गुणों का समर्थन करने पर एक व्यापक ट्यूटोरियल पूरा किया है। फ़ाइल लोड करने से लेकर आकार गुणों को संशोधित करने और अंतिम उत्पाद को सहेजने तक - प्रत्येक चरण इस लाइब्रेरी की शक्ति को उजागर करता है। चाहे आप रचनात्मक परियोजनाओं पर काम कर रहे हों या ग्राफ़िक संपत्तियों को स्वचालित कर रहे हों, Aspose.PSD संभावनाओं की एक पूरी नई दुनिया खोलता है। आरंभ करने के लिए तैयार हैं? अपनी PSD फ़ाइलों में गोता लगाएँ और अपनी रचनात्मकता को उजागर करें!
## अक्सर पूछे जाने वाले प्रश्न
### Java के लिए Aspose.PSD क्या है?
Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को जावा का उपयोग करके प्रोग्रामेटिक रूप से फ़ोटोशॉप PSD फ़ाइलों में हेरफेर करने और उनके साथ काम करने की अनुमति देती है।
### क्या मैं एक निःशुल्क प्रोजेक्ट में Aspose.PSD का उपयोग कर सकता हूँ?
हां, आप Aspose वेबसाइट पर उपलब्ध परीक्षण संस्करण का उपयोग करके लाइब्रेरी को मुफ्त में आज़मा सकते हैं।
### मैं PSD फ़ाइलों में किस प्रकार के संशोधन कर सकता हूँ?
आप PSD फ़ाइलों के भीतर परतों, आकृतियों, पाठों, पथ संचालनों और बहुत कुछ में हेरफेर कर सकते हैं।
### क्या Aspose.PSD अन्य प्रोग्रामिंग भाषाओं के साथ संगत है?
हां, Aspose .NET और पायथन सहित विभिन्न प्रोग्रामिंग भाषाओं के लिए विभिन्न लाइब्रेरी प्रदान करता है।
### मैं Aspose.PSD के लिए दस्तावेज़ कहां पा सकता हूं?
 आप सम्पूर्ण दस्तावेज़ तक पहुँच सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
