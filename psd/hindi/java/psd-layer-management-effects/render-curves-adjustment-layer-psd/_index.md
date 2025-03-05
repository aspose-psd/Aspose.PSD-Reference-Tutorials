---
title: PSD फ़ाइलों में कर्व्स एडजस्टमेंट लेयर रेंडर करें - जावा
linktitle: PSD फ़ाइलों में कर्व्स एडजस्टमेंट लेयर रेंडर करें - जावा
second_title: Aspose.PSD जावा एपीआई
description: इस विस्तृत चरण-दर-चरण मार्गदर्शिका के साथ Java के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में कर्व्स एडजस्टमेंट लेयर्स को प्रस्तुत और समायोजित करना सीखें।
type: docs
weight: 16
url: /hi/java/psd-layer-management-effects/render-curves-adjustment-layer-psd/
---
## परिचय

फ़ोटोशॉप की कर्व्स एडजस्टमेंट लेयर छवियों को बेहतर बनाने के लिए एक जादू की छड़ी की तरह है। कल्पना करें कि आप एक कलाकार हैं जो अपनी उत्कृष्ट कृति के रंगों और टोन को बदल रहे हैं - प्रत्येक कर्व एडजस्टमेंट आपको अविश्वसनीय सटीकता के साथ प्रकाश और रंग संतुलन को नियंत्रित करने देता है। यदि आप PSD फ़ाइलों के साथ काम कर रहे हैं और इन कर्व्स को प्रोग्रामेटिक रूप से हेरफेर करने की आवश्यकता है, तो Aspose.PSD for Java आपके लिए सबसे अच्छा टूल है। इस गाइड में, हम Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में कर्व्स एडजस्टमेंट लेयर्स को रेंडर और एडजस्ट करने का तरीका बताएंगे। चाहे आप इमेज टोन अपडेट कर रहे हों या अपने परिणाम निर्यात कर रहे हों, यह ट्यूटोरियल आपको शुरू करने के लिए आवश्यक सभी चीज़ों को कवर करेगा।

## आवश्यक शर्तें

इससे पहले कि हम कोडिंग की बारीकियों पर जाएं, आइए सुनिश्चित करें कि आपने पूरी तैयारी कर ली है। आपको ये चीज़ें चाहिए:

1. जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK स्थापित है। Java के लिए Aspose.PSD को Java 8 या उच्चतर की आवश्यकता होती है।
   
2.  Aspose.PSD for Java लाइब्रेरी: Aspose.PSD for Java लाइब्रेरी को यहाँ से डाउनलोड करें[Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/). 

3. IDE (एकीकृत विकास वातावरण): कोई भी जावा-संगत IDE काम करेगा, जैसे IntelliJ IDEA या Eclipse.

4. जावा प्रोग्रामिंग का बुनियादी ज्ञान: जावा सिंटैक्स और बुनियादी प्रोग्रामिंग अवधारणाओं को समझने से आपको ट्यूटोरियल का अनुसरण करने में मदद मिलेगी।

5. PSD फ़ाइल: कर्व्स एडजस्टमेंट लेयर वाली PSD फ़ाइल जिसे आप संपादित करना चाहते हैं। 

एक बार जब आप इन पूर्व-आवश्यकताओं को पूरा कर लेते हैं, तो आप अपनी PSD फ़ाइलों में हेरफेर शुरू करने के लिए तैयार हैं।

## पैकेज आयात करें

आरंभ करने के लिए, आपको Aspose.PSD से आवश्यक पैकेज आयात करने की आवश्यकता है। ये लाइब्रेरी PSD फ़ाइल संचालन को संभालेंगी, जिसमें कर्व्स लेयर को पढ़ना और संशोधित करना शामिल है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
import com.aspose.psd.imageoptions.PngOptions;
```

## चरण 1: PSD फ़ाइल लोड करें

 सबसे पहले, आपको अपनी PSD फ़ाइल को एप्लिकेशन में लोड करना होगा।`PsdImage` Aspose.PSD से क्लास आपको PSD फ़ाइलों को खोलने और उनमें हेरफेर करने की अनुमति देता है।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
PsdImage im = (PsdImage)Image.load(sourceFileName + ".psd");
```

 यहाँ, प्रतिस्थापित करें`"Your Document Directory/CurvesAdjustmentLayer"` अपनी PSD फ़ाइल के पथ के साथ। यह कोड स्निपेट PSD फ़ाइल को एक में लोड करता है`PsdImage` वस्तु।

## चरण 2: परतों के माध्यम से पुनरावृति करें

PSD फ़ाइलों में कई परतें हो सकती हैं। कर्व्स एडजस्टमेंट लेयर को खोजने और उसमें बदलाव करने के लिए, आपको अपनी PSD फ़ाइल की परतों के माध्यम से पुनरावृति करनी होगी।

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof CurvesLayer) {
        CurvesLayer curvesLayer = (CurvesLayer)im.getLayers()[i];
        // अतिरिक्त कार्य यहां संभाले जाएंगे
    }
}
```

यह लूप प्रत्येक परत की जांच करता है ताकि यह निर्धारित किया जा सके कि क्या यह इसका उदाहरण है`CurvesLayer`यदि ऐसा है, तो आप वक्रों को समायोजित करने के लिए आगे बढ़ सकते हैं।

## चरण 3: कर्व्स लेयर को संशोधित करें

एक बार जब आप कर्व्स एडजस्टमेंट लेयर की पहचान कर लेते हैं, तो आप इसकी सेटिंग को संशोधित कर सकते हैं। इस बात पर निर्भर करते हुए कि लेयर डिस्क्रीट या कंटीन्यूअस मैनेजर का उपयोग करता है, दृष्टिकोण अलग-अलग होगा।

### असतत वक्र प्रबंधक को संशोधित करना

 यदि`CurvesLayer` का उपयोग करता है`CurvesDiscreteManager`, आप वक्र बिंदुओं को सीधे समायोजित कर सकते हैं।

```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();
    
    for (int k = 10; k < 50; k++) {
        manager.setValueInPosition(0, (byte)k, (byte)(15 + (k * 2)));
    }
}
```

इस स्निपेट में, हम वक्र मानों को अलग-अलग तरीके से समायोजित करते हैं। इसमें विभिन्न स्थितियों पर मान सेट करना शामिल है, जिससे वक्र के आकार को प्रभावी ढंग से संशोधित किया जा सके।

### सतत वक्र प्रबंधक को संशोधित करना

 परतों के लिए एक का उपयोग`CurvesContinuousManager`, आप वक्र बिंदु जोड़ेंगे.

```java
else {
    CurvesContinuousManager manager = (CurvesContinuousManager)curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte)0, (byte)50, (byte)100);
    manager.addCurvePoint((byte)0, (byte)150, (byte)130);
}
```

यह कोड दो वक्र बिंदुओं को जोड़ता है, तथा वक्र के आकार को निरंतर मानों के साथ समायोजित करता है। 

## चरण 4: PSD फ़ाइल सहेजें

अपने समायोजन करने के बाद, संशोधित PSD फ़ाइल को सेव करें। यह चरण सुनिश्चित करता है कि आपके सभी परिवर्तन संग्रहीत हैं।

```java
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
im.save(psdPathAfterChange + ".psd");
```

यहां, आप वह पथ निर्दिष्ट करते हैं जहां संशोधित PSD फ़ाइल सहेजी जाएगी। 

## चरण 5: PNG में निर्यात करें

 समायोजित PSD फ़ाइल को PNG के रूप में निर्यात करने के लिए, कॉन्फ़िगर करें`PngOptions` और फ़ाइल को सेव करें.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
String pngExportPath = dataDir + "CurvesAdjustmentLayerChanged";
im.save(pngExportPath + ".png", saveOptions);
```

यह स्निपेट अल्फा पारदर्शिता के साथ रंग प्रकार सहित PNG निर्यात विकल्प सेट करता है, और फ़ाइल को PNG के रूप में सहेजता है।

## निष्कर्ष

Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में कर्व्स एडजस्टमेंट लेयर्स में हेरफेर करना पहली बार में जटिल लग सकता है, लेकिन इन चरण-दर-चरण निर्देशों के साथ, आप इसे प्रबंधनीय और सहज पाएंगे। इस गाइड का पालन करके, आप आसानी से इमेज टोन को बदल सकते हैं और अपने परिणामों को विभिन्न प्रारूपों में निर्यात कर सकते हैं। चाहे आप किसी प्रोजेक्ट के लिए इमेज को बेहतर बना रहे हों या बैच प्रक्रियाओं को स्वचालित कर रहे हों, Aspose.PSD आपको आसानी से पेशेवर परिणाम प्राप्त करने के लिए आवश्यक उपकरण प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### कर्व्स समायोजन परत क्या है?
फ़ोटोशॉप में कर्व्स एडजस्टमेंट लेयर आपको RGB कर्व्स को संशोधित करके किसी छवि की चमक और कंट्रास्ट को समायोजित करने की अनुमति देता है। यह टोनल समायोजन पर सटीक नियंत्रण प्रदान करता है।

### क्या मैं अन्य छवि प्रारूपों के साथ Java के लिए Aspose.PSD का उपयोग कर सकता हूँ?
हां, Java के लिए Aspose.PSD मुख्य रूप से PSD फ़ाइलों के लिए है, लेकिन आप अपनी संपादित छवियों को PNG, TIFF और JPEG जैसे प्रारूपों में निर्यात कर सकते हैं।

### क्या मुझे Java के लिए Aspose.PSD का उपयोग करने के लिए फ़ोटोशॉप स्थापित करने की आवश्यकता है?
नहीं, Aspose.PSD for Java फ़ोटोशॉप से स्वतंत्र रूप से काम करता है, जिससे आप PSD फ़ाइलों को प्रोग्रामेटिक रूप से हेरफेर कर सकते हैं।

### मैं Java के लिए Aspose.PSD का निःशुल्क परीक्षण कैसे प्राप्त कर सकता हूँ?
 आप Java के लिए Aspose.PSD का निःशुल्क परीक्षण संस्करण यहाँ से डाउनलोड कर सकते हैं[Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/).

### मैं Java के लिए Aspose.PSD का समर्थन कहां पा सकता हूं?
 सहायता के लिए आप यहां जा सकते हैं[Aspose समर्थन मंच](https://forum.aspose.com/c/psd/34).