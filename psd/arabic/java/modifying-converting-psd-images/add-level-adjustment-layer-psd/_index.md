---
date: 2026-03-07
description: تعلم كيفية تعديل المستويات بإضافة طبقة تعديل المستوى في ملفات PSD باستخدام
  Aspose.PSD للغة Java. إتقان تعديل النغمات بسرعة.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: كيفية تعديل المستويات – إضافة طبقة تعديل المستويات في PSD
url: /ar/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة طبقة تعديل المستويات في PSD

## المقدمة
إذا كنت تبحث عن **كيفية تعديل المستويات** في مستندات Photoshop الخاصة بك، فإن طبقة تعديل المستويات هي الأداة المثالية. تتيح لك ضبط الظلال، والنصوص المتوسطة، والإضاءات بدقة دون تعديل البكسلات الأصلية بشكل دائم. في هذا الدرس سنستعرض إضافة طبقة تعديل المستويات إلى ملف PSD باستخدام Aspose.PSD for Java، حتى تتمكن من تحقيق تحكم نغمي احترافي في بضع خطوات فقط.

## إجابات سريعة
- **ماذا تفعل طبقة تعديل المستويات؟** تقوم بتعديل النطاق النغمي للصورة بشكل غير مدمر.  
- **ما المكتبة المستخدمة؟** Aspose.PSD for Java.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ الترخيص مطلوب للإنتاج.  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لتعديل أساسي.  
- **هل يمكن تعديل قنوات متعددة؟** نعم، يمكنك ضبط مستويات الإدخال/الإخراج لكل قناة لون على حدة.

## ما هي طبقة تعديل المستويات؟
تتيح لك طبقة تعديل المستويات تصحيح التوازن النغمي للصورة عن طريق ضبط ظلال الإدخال، والنصوص المتوسطة، والإضاءات بالإضافة إلى مستويات الإخراج. وبما أنها موجودة كطبقة مستقلة، يمكنك تشغيل/إيقاف رؤيتها أو حذفها دون التأثير على العمل الأساسي.

## لماذا إضافة طبقة تعديل المستويات باستخدام Aspose.PSD؟
- **الأتمتة:** دمج تعديل المستويات في خطوط معالجة الدفعات.  
- **متعدد المنصات:** يعمل على أي نظام تشغيل يدعم Java.  
- **الدقة:** الوصول إلى إعدادات كل قناة برمجياً للحصول على نتائج دقيقة.  

## المتطلبات المسبقة
1. مجموعة تطوير Java (JDK). إذا لم تكن لديك، قم بتنزيلها من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) أو استخدم OpenJDK.  
2. مكتبة Aspose.PSD for Java – احصل على أحدث ملف JAR من هذا [رابط التحميل](https://releases.aspose.com/psd/java/).  
3. معرفة أساسية ببرمجة Java.  
4. بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse أو NetBeans مع إضافة ملف JAR الخاص بـ Aspose.PSD إلى مسار الفئات (classpath) للمشروع.

## استيراد الحزم
قبل أن نبدأ بكتابة الكود، نحتاج إلى استيراد الحزم الضرورية من مكتبة Aspose.PSD. إليك الطريقة:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
تتيح لنا هذه الاستيرادات الوصول إلى الفئات الخاصة بتحميل ملفات PSD، والعمل مع طبقات تعديل المستويات، وتعديل إعدادات القنوات الفردية.

## كيفية تعديل المستويات في ملف PSD
فيما يلي دليل خطوة بخطوة يوضح لك بالضبط **كيفية تعديل المستويات** برمجياً.

### الخطوة 1: إعداد مسارات الملفات الخاصة بك
حدد موقع ملف PSD الأصلي ومكان حفظ الملف المعدل.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
استبدل `"Your Document Directory"` بالمجلد الفعلي على جهازك.

### الخطوة 2: تحميل ملف PSD
أنشئ كائن `PsdImage` من الملف المصدر.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
الآن لديك وصول كامل إلى جميع الطبقات داخل ملف PSD.

### الخطوة 3: التجول عبر الطبقات
ابحث عن طبقة تعديل المستويات التي تريد تعديلها.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
تحقق `instanceof LevelsLayer` يضمن أننا نتعامل فقط مع طبقات تعديل المستويات.

### الخطوة 4: تعديل إعدادات قناة المستوى
قم بضبط قيم الإدخال والإخراج للقناة المحددة.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **مستوى النص المتوسط (Input Midtone Level):** يغيّر نطاق النص المتوسط.  
- **مستوى الظل (Input Shadow Level):** يغمق أو يفتح الظلال.  
- **مستوى الإضاءة (Input Highlight Level):** يتحكم في الأجزاء الأكثر سطوعًا.  
- **مستويات الظل/الإضاءة للإخراج (Output Shadow/Highlight Levels):** تحدد النطاق النهائي للإخراج.  

لا تتردد في تجربة قيم مختلفة لمعرفة تأثيرها على الصورة.

### الخطوة 5: حفظ ملف PSD المعدل
احفظ تغييراتك في ملف جديد.
```java
im.save(psdPathAfterChange);
```
ستجد ملف PSD المحدث في الموقع الذي حددته في `psdPathAfterChange`.

## المشكلات الشائعة والحلول
- **الملف غير موجود:** تأكد من أن `dataDir` يشير إلى المجلد الصحيح وأن ملف PSD المصدر موجود.  
- **ClassCastException:** تأكد من أن الملف الذي تم تحميله هو PSD فعليًا؛ الصيغ الأخرى تتطلب فئات مختلفة.  
- **أخطاء الترخيص:** استخدم ترخيص Aspose.PSD صالح لإصدارات الإنتاج؛ النسخة التجريبية تعمل للتطوير.

## الخلاصة
أنت الآن تعرف **كيفية تعديل المستويات** عن طريق إضافة وتكوين طبقة تعديل المستويات في ملف PSD باستخدام Aspose.PSD for Java. تمنحك هذه التقنية تحكمًا دقيقًا في التوازن النغمي مع الحفاظ على سير العمل آليًا بالكامل. استمر في تجربة قيم القنوات المختلفة واستكشف المعالجة الدفعية لتطبيق نفس التعديلات على صور متعددة.

## الأسئلة المتكررة

**س: ما هي طبقة تعديل المستويات؟**  
ج: إنها طبقة غير مدمرة تتيح لك تعديل النطاق النغمي (الظلال، النصوص المتوسطة، الإضاءات) للصورة.

**س: هل يمكنني استخدام Aspose.PSD دون شراء ترخيص؟**  
ج: نعم، يمكنك تقييم المكتبة باستخدام النسخة التجريبية المجانية، لكن الترخيص مطلوب للنشر التجاري.

**س: أين يمكنني العثور على وثائق Aspose.PSD؟**  
ج: يمكنك العثور على الوثائق [هنا](https://reference.aspose.com/psd/java/).

**س: هل هناك دعم مجتمع لمنتجات Aspose؟**  
ج: بالتأكيد! يمكنك طرح الأسئلة والحصول على المساعدة في [منتدى Aspose](https://forum.aspose.com/c/psd/34).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: يمكنك التقدم بطلب للحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

---

**آخر تحديث:** 2026-03-07  
**تم الاختبار مع:** Aspose.PSD latest version (Java)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}