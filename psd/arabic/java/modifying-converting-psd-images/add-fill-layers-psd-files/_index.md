---
date: 2026-03-04
description: تعلم كيفية تعديل طبقات PSD برمجياً عن طريق إضافة طبقات تعبئة باستخدام
  Aspose.PSD للغة Java. اتبع هذا الدليل خطوة بخطوة لتعزيز تصاميمك بسرعة.
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: تعديل طبقات PSD برمجياً – إضافة طبقات تعبئة (Java)
url: /ar/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعديل طبقات PSD برمجياً – إضافة طبقات تعبئة (Java)

إذا كنت تبحث عن **تعديل طبقات PSD برمجياً**، فإن إضافة طبقات تعبئة هي واحدة من أسرع الطرق لإثراء مستندات Photoshop دون الحاجة إلى فتح البرنامج نفسه. في هذا الدرس سنستعرض الخطوات الدقيقة التي تحتاجها لإنشاء ملف PSD جديد، وإدراج طبقات تعبئة باللون، التدرج، والنقش، ثم حفظ النتيجة—كل ذلك باستخدام Aspose.PSD for Java.

## إجابات سريعة
- **ماذا يمكنني تحقيقه؟** إضافة طبقات تعبئة باللون، التدرج، والنقش إلى ملف PSD برمجياً.  
- **ما المكتبة المطلوبة؟** Aspose.PSD for Java (أحدث إصدار).  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **كم من الوقت تستغرق العملية؟** حوالي 10‑15 دقيقة لمثال أساسي.  
- **ما نسخة Java المدعومة؟** JDK 11 أو أحدث.

## ما هو “تعديل طبقات PSD برمجياً”؟
تعديل طبقات PSD برمجياً يعني استخدام الكود لإنشاء، تعديل، أو حذف طبقات داخل مستند Photoshop، مما يمنحك تحكمًا كاملاً في سير عمل التصميم دون الحاجة إلى التفاعل اليدوي مع الواجهة.

## لماذا نضيف طبقات تعبئة باستخدام Aspose.PSD؟
- **الأتمتة** – إنشاء العشرات من ملفات PSD في مهمة دفعة.  
- **الاتساق** – تطبيق نفس اللون أو التدرج أو النمط عبر ملفات متعددة.  
- **السرعة** – تخطي الخطوات اليدوية المستهلكة للوقت في Photoshop.  
- **متعدد المنصات** – يعمل على أي نظام تشغيل يدعم Java.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من وجود ما يلي:

1. **مجموعة تطوير جافا (JDK)** – تثبيت JDK 11 أو أحدث. يمكنك تحميله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – احصل على أحدث مكتبة من صفحة التحميل الرسمية [هنا](https://releases.aspose.com/psd/java/).  
3. **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA، Eclipse، أو أي محرر تفضله.  
4. **معرفة أساسية بـ Java** – الإلمام بالصفوف والطرق سيساعد، لكن الدرس يشرح كل شيء خطوة بخطوة.

## استيراد الحزم
لبدء العمل مع ملفات PSD تحتاج إلى استيراد الفئات ذات الصلة من Aspose.PSD:

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

تمنحك هذه الاستيرادات إمكانية الوصول إلى كائن `PsdImage` (المستند نفسه) وأنواع `FillLayer` المختلفة التي سنستخدمها.

## كيفية تعديل طبقات PSD برمجياً – دليل خطوة بخطوة

### الخطوة 1: إعداد دليل الإخراج
حدد أين سيتم حفظ ملف PSD الناتج لتتمكن من العثور عليه لاحقًا.

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

استبدل `"Your Document Directory"` بمسار مطلق أو نسبي على جهازك.

### الخطوة 2: إنشاء مستند Photoshop جديد
أنشئ لوحة فارغة ستستضيف طبقات التعبئة.

```java
PsdImage psdImage = new PsdImage(100, 100);
```

المعلمات `100, 100` تمثل العرض والارتفاع بالبكسل. عدلها لتتناسب مع متطلبات التصميم الخاصة بك.

### الخطوة 3: إضافة طبقة تعبئة لونية
أنشئ طبقة تعبئة بلون صلب ومنحها اسمًا وصفيًا.

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

يمكنك لاحقًا تغيير اللون الفعلي عبر إعدادات تعبئة الطبقة (غير موضح هنا لتقليل الإطالة).

### الخطوة 4: إضافة طبقة تعبئة متدرجة
تضيف التعبئات المتدرجة عمقًا واهتمامًا بصريًا.

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

لا تتردد في تجربة التدرجات الخطية أو الدائرية عبر إعدادات الطبقة.

### الخطوة 5: إضافة طبقة تعبئة بنقش
تتيح لك التعبئات بالنقش تكرار الصور أو القوام عبر الطبقة.

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

ضبط الشفافية إلى 50 % يجعل النقش يندمج بشكل جميل مع الطبقات الموجودة تحته.

### الخطوة 6: حفظ ملف PSD
احفظ التغييرات على القرص.

```java
psdImage.save(outPsdFilePath);
```

افتح الملف المحفوظ في Photoshop أو أي عارض PSD لرؤية الطبقات الثلاث الجديدة.

### الخطوة 7: تنظيف الموارد
دائمًا قم بتحرير كائن `PsdImage` لتحرير الذاكرة الأصلية.

```java
psdImage.dispose();
```

## مشكلات شائعة ونصائح
- **مسار الإخراج غير صالح** – تأكد من وجود الدليل وأن لديك صلاحيات الكتابة.  
- **استخدام الذاكرة** – بالنسبة للكانفاس كبير جداً، استدعِ `psdImage.dispose()` بمجرد الانتهاء من الصورة.  
- **ترتيب الطبقات** – تُضاف الطبقات إلى أعلى المكدس افتراضياً؛ استخدم `psdImage.insertLayer(layer, index)` إذا كنت بحاجة إلى ترتيب محدد.

## أسئلة متكررة

**س: ما أنواع طبقات التعبئة التي يمكنني إضافتها باستخدام Aspose.PSD for Java؟**  
ج: يمكنك إضافة طبقات تعبئة باللون، التدرج، والنقش.

**س: هل يدعم Aspose.PSD صيغ صور أخرى؟**  
ج: نعم، يعمل مع BMP، JPEG، PNG، والعديد من الصيغ الأخرى.

**س: هل يمكنني استخدام Aspose.PSD مجانًا؟**  
ج: يمكنك تجربة نسخة تجريبية مجانية من Aspose.PSD for Java [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على مزيد من الوثائق حول Aspose.PSD؟**  
ج: يمكنك الوصول إلى الوثائق الكاملة [هنا](https://reference.aspose.com/psd/java/).

**س: هل هناك مجتمع دعم لـ Aspose.PSD؟**  
ج: نعم، يمكنك الحصول على المساعدة من المجتمع في منتدى Aspose [هنا](https://forum.aspose.com/c/psd/34).

## الخاتمة
لقد تعلمت الآن كيفية **تعديل طبقات PSD برمجياً** بإضافة طبقات تعبئة مختلفة باستخدام Aspose.PSD for Java. هذه الطريقة توفر لك الوقت، وتضمن الاتساق عبر المشاريع، وتفتح الباب أمام سيناريوهات معالجة دفعات قوية. جرب ألوانًا، تدرجات، ونقوش مختلفة لترى إلى أي مدى يمكنك دفع إنشاء التصميم الآلي.

---

**آخر تحديث:** 2026-03-04  
**تم الاختبار مع:** Aspose.PSD for Java (أحدث إصدار)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}