---
title: जावा के साथ PSD फ़ाइलों में Vmsk संसाधन का समर्थन करें
linktitle: जावा के साथ PSD फ़ाइलों में Vmsk संसाधन का समर्थन करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में Vmsk संसाधनों को आसानी से प्रबंधित करें। डेवलपर्स और डिज़ाइनरों दोनों के लिए एक व्यापक, चरण-दर-चरण ट्यूटोरियल आदर्श है।
type: docs
weight: 23
url: /hi/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---
## परिचय
जब PSD (फ़ोटोशॉप दस्तावेज़) फ़ाइलों के साथ काम करने की बात आती है, तो संसाधनों का प्रबंधन करना महत्वपूर्ण होता है, खासकर जब Vmsk (वेक्टर मास्क) संसाधन जैसी विशेष सुविधाओं को एकीकृत किया जाता है। Vmsk संसाधन जटिल वेक्टर आकृतियों को जोड़कर डिजाइनरों को सशक्त बना सकते हैं, जिससे वे आसानी से शानदार ग्राफ़िक्स बना सकते हैं। इस गाइड में, हम आपको Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में Vmsk संसाधनों का समर्थन करने का तरीका दिखाने के लिए एक व्यावहारिक दृष्टिकोण अपनाने जा रहे हैं। चाहे आप अपने एप्लिकेशन को बेहतर बनाने के इच्छुक डेवलपर हों या स्वचालन चाहने वाले डिज़ाइनर, यह ट्यूटोरियल आपको चरण दर चरण प्रक्रिया से गुजारेगा, जिससे इसका पालन करना और लागू करना आसान हो जाएगा।
## आवश्यक शर्तें
इससे पहले कि हम Vmsk संसाधनों को संभालने के रोचक विवरण में उतरें, आइए सुनिश्चित करें कि आपके पास निर्बाध अनुभव के लिए सब कुछ तैयार है।
### जिसकी आपको जरूरत है
-  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके मशीन पर JDK इंस्टॉल है। यदि नहीं, तो आप इसे यहाँ से डाउनलोड कर सकते हैं।[ओरेकल वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java लाइब्रेरी: यह PSD फ़ाइलों के प्रबंधन के लिए एक शक्तिशाली लाइब्रेरी है। आप इसे यहाँ से डाउनलोड कर सकते हैं[एस्पोज रिलीज पेज](https://releases.aspose.com/psd/java/) जो लोग खरीदने से पहले इसे आज़माना चाहते हैं, वे भी इससे शुरुआत कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).
- एक IDE: जावा के लिए कोई भी IDE (जैसे IntelliJ IDEA, Eclipse, आदि) इस परियोजना के लिए काम करेगा।
### अपना कार्यस्थल स्थापित करना
1. एक नया जावा प्रोजेक्ट बनाएँ: अपना पसंदीदा IDE शुरू करें और एक नया जावा प्रोजेक्ट बनाएँ। यह कोड के साथ काम करने के लिए आपका प्लेग्राउंड है।
2. Aspose लाइब्रेरी जोड़ें: Aspose लाइब्रेरी डाउनलोड करने के बाद, jar फ़ाइल को अपने प्रोजेक्ट की लाइब्रेरी में जोड़ें। यह कदम महत्वपूर्ण है क्योंकि यह हमें Aspose.PSD की सभी बेहतरीन सुविधाओं का उपयोग करने की अनुमति देता है।
इन पूर्व-आवश्यकताओं के साथ, आप Vmsk संसाधनों के साथ PSD फ़ाइलें बनाना, संशोधित करना और प्रबंधित करना शुरू करने के लिए तैयार हैं। चलिए सीधे प्रोग्रामिंग में उतरते हैं!
## पैकेज आयात करें
PSD फ़ाइलों पर काम करने से पहले, हमें आवश्यक पैकेज आयात करने की आवश्यकता है। यह हमारे कोड की रीढ़ है, जो हमें Aspose.PSD लाइब्रेरी द्वारा प्रदान की जाने वाली विभिन्न कक्षाओं और विधियों तक पहुँच प्रदान करता है।
```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```
अब जब हमने मंच तैयार कर लिया है, तो अब कार्रवाई का समय है! इस अनुभाग में, हम कोड को प्रबंधनीय चरणों में विभाजित करेंगे। ये चरण आपको PSD फ़ाइल पढ़ने, Vmsk संसाधन को संभालने और यहां तक कि उसे संपादित करने में मार्गदर्शन करेंगे।
## चरण 1: अपनी PSD फ़ाइल लोड करें
सबसे पहले आपको अपनी PSD फ़ाइल लोड करनी होगी। यहीं से जादू शुरू होता है।
```java
String dataDir = "Your Document Directory"; // इस पथ को अपडेट करें
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  हमने सेट किया`dataDir` अपने PSD फ़ाइल की निर्देशिका में. 
-  हम इसके लिए एक स्ट्रिंग बनाते हैं`sourceFileName`, निर्देशिका को PSD फ़ाइल के नाम के साथ संयोजित करना।
-  अंत में, हम PSD फ़ाइल को लोड करते हैं`PsdImage` वस्तु का उपयोग`Image.load()`.
## चरण 2: Vmsk संसाधन पुनः प्राप्त करें
अब जबकि हमारी PSD छवि लोड हो गई है, तो चलिए Vmsk संसाधन प्राप्त करते हैं।
```java
VmskResource resource = getVmskResource(im);
```

-  हम कहते हैं`getVmskResource()` विधि जो छवि से Vmsk संसाधन को खोजने और पुनर्प्राप्त करने का काम संभालती है।
## चरण 3: Vmsk संसाधन गुण सत्यापित करें
संशोधनों के साथ आगे बढ़ने से पहले, यह सत्यापित करना आवश्यक है कि हमारा Vmsk संसाधन अपेक्षित स्थिति में है।
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- यहाँ, हम Vmsk संसाधन के विभिन्न गुणों की जाँच कर रहे हैं। हम यह सुनिश्चित करना चाहते हैं कि यह अक्षम, उलटा या लिंक नहीं है, और इसमें सही संख्या में पथ हैं।
## चरण 4: प्रत्येक पथ तक पहुँचें और सत्यापित करें
आइए थोड़ा गहराई से देखें और Vmsk संसाधन के भीतर पथों का निरीक्षण करें।
```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- हम तीन विशिष्ट पथ रिकॉर्ड निकाल रहे हैं और उनके प्रकार और गुणों का सत्यापन कर रहे हैं ताकि यह सुनिश्चित किया जा सके कि वे हमारे मानदंडों को पूरा करते हैं।
## चरण 5: Vmsk संसाधन संपादित करें
अब हम संशोधन भाग में आ रहे हैं! आप आवश्यकतानुसार Vmsk संसाधन के गुणों में बदलाव कर सकते हैं।
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- इस ब्लॉक में, हम Vmsk संसाधन के विभिन्न गुणों को टॉगल कर रहे हैं। उन्हें true पर सेट करके, हम यह नियंत्रित कर सकते हैं कि PSD फ़ाइल में मास्क कैसे व्यवहार करता है।
## चरण 6: बेज़ियर गाँठ बिंदुओं को संशोधित करें
बेज़ियर नॉट्स वेक्टर पथों के लिए महत्वपूर्ण हैं। आइए यहाँ कुछ मान बदलें।
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  हम विशिष्ट तक पहुंच रहे हैं`BezierKnotRecord` पथों को चिह्नित करना तथा उनके बिंदुओं को परिवर्तित करके वेक्टर मास्क को संभावित रूप से पुनः आकार देना।
## चरण 7: संशोधित PSD फ़ाइल सहेजें
जब सभी संपादन पूरे हो जाएं, तो संशोधित PSD फ़ाइल को सहेजने का समय आ गया है। 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  हम निर्यात की गई PSD फ़ाइल के लिए पथ सेट करते हैं और फिर कॉल करते हैं`im.save()` इस नई फ़ाइल में परिवर्तन लिखने के लिए.
## चरण 8: संसाधनों को साफ करें
अंत में, हमें यह सुनिश्चित करना होगा कि हम संसाधनों को मुक्त करने के लिए छवि का उचित तरीके से निपटान करें।
```java
im.dispose();
```

- काम पूरा होने के बाद किसी भी संसाधन को नष्ट कर देना हमेशा एक अच्छा अभ्यास है। इससे आपके अनुप्रयोगों में मेमोरी लीक से बचने में मदद मिलती है।
## निष्कर्ष
बधाई हो! आपने अभी-अभी Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में Vmsk संसाधनों का समर्थन करने की विस्तृत प्रक्रिया को पूरा किया है। छवि लोड करने से लेकर, Vmsk संसाधन को पुनः प्राप्त करने और मान्य करने, इसके गुणों को संपादित करने और फिर अपने संशोधित PSD को सहेजने तक, आपने सभी आवश्यक कार्य पूरे कर लिए हैं। इन कौशलों के साथ, आप PSD फ़ाइलों में विभिन्न संसाधनों का कुशलतापूर्वक प्रबंधन और उपयोग कर सकते हैं, अपने ग्राफिक डिज़ाइन प्रोजेक्ट या ऑटोमेशन स्क्रिप्ट को बेहतर बना सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### Vmsk संसाधन क्या है?
Vmsk संसाधन PSD फ़ाइल में एक वेक्टर मास्क है जो जटिल वेक्टर आकृतियों और संपादन सुविधाओं की अनुमति देता है।
### क्या मैं Maven प्रोजेक्ट में Aspose.PSD का उपयोग कर सकता हूँ?
हां, आप रिपॉजिटरी से इसके निर्देशांक का उपयोग करके अपने मावेन प्रोजेक्ट में निर्भरता के रूप में Aspose.PSD को शामिल कर सकते हैं।
### मैं अपनी संशोधित PSD फ़ाइलों को किस प्रारूप में सहेज सकता हूँ?
आप उन्हें PSD फ़ाइलों के रूप में सहेज सकते हैं या उन्हें PNG, JPEG आदि जैसे अन्य प्रारूपों में निर्यात कर सकते हैं।
### क्या Aspose.PSD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?
 हां, आप इसकी सुविधाओं का परीक्षण करने के लिए Aspose.PSD का निःशुल्क परीक्षण प्राप्त कर सकते हैं।[निःशुल्क परीक्षण लिंक](https://releases.aspose.com/).
### मैं Aspose.PSD के लिए समर्थन कैसे प्राप्त कर सकता हूं?
 आप इसमें शामिल हो सकते हैं[एस्पोज फोरम](https://forum.aspose.com/c/psd/34)समर्थन और समस्या निवारण सहायता के लिए.