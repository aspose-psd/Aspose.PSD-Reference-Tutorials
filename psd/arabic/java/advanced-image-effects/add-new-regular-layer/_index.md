---
date: 2026-04-08
description: تعلم كيفية تصدير ملفات PSD إلى PNG وإنشاء طبقة PSD جديدة باستخدام Aspose.PSD
  للغة Java عبر ترخيص مؤقت من Aspose. يغطي هذا الدليل خطوة بخطوة معالجة صور PSD وتحديد
  موضع الطبقة.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: إضافة طبقة عادية جديدة إلى PSD
second_title: Aspose.PSD Java API
title: تصدير PSD إلى PNG وإضافة طبقة عادية جديدة باستخدام Aspose.PSD للغة Java – ترخيص
  مؤقت من Aspose
url: /ar/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير PSD إلى PNG وإضافة طبقة عادية جديدة باستخدام Aspose.PSD للـ Java

## المقدمة

في هذا **aspose psd tutorial** ستكتشف كيفية **export PSD to PNG** مع **إنشاء طبقة عادية جديدة** داخل نفس الملف، **باستخدام ترخيص Aspose مؤقت** للتطوير. سواء كنت بحاجة إلى إنشاء صور مصغرة جاهزة للويب، أو إعداد أصول لخط أنابيب التصميم، أو مجرد تجربة **psd image manipulation**، فإن Aspose.PSD للـ Java يمنحك تحكمًا برمجيًا كاملاً. سنستعرض كل خطوة — من تحميل الملف المصدر إلى حفظ كل من ملف PSD المحدث ونسخة PNG — حتى تتمكن من البدء في تعديل طبقات PSD فورًا.

## إجابات سريعة
- **هل يمكنني تصدير PSD إلى PNG باستدعاء واحد؟** نعم، بعد إضافة الطبقات يمكنك استدعاء `save` مع `PngOptions`.
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت يكفي للاختبار؛ الترخيص الكامل مطلوب للإنتاج.
- **ما نسخة Java المدعومة؟** Aspose.PSD يعمل مع Java 8 وما فوق.
- **هل تموضع الطبقة يعتمد على البكسل؟** نعم، تحدد إحداثيات اليسار، الأعلى، اليمين، الأسفل بالبكسل باستخدام طرق **set layer position**.
- **هل سيحتفظ PNG بشفافية الطبقة؟** سيحتوي PNG على النتيجة المدمجة لجميع الطبقات المرئية.

## لماذا تستخدم ترخيص Aspose مؤقت؟

**ترخيص Aspose مؤقت** يتيح لك تقييم مجموعة الميزات الكاملة لـ Aspose.PSD دون أي قيود وظيفية. يزيل علامة التقييم، يفتح جميع الـ APIs — بما في ذلك القدرة على **create new psd layer** — ويسمح لك باختبار الكود في بيئة شبيهة بالإنتاج قبل شراء ترخيص دائم.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود:

- **بيئة تطوير Java** – JDK 8+ وأداة بناء (Maven/Gradle) مثبتة.
- **Aspose.PSD للـ Java** – حمّل أحدث JAR من الموقع الرسمي [هنا](https://releases.aspose.com/psd/java/).
- **ملف PSD تجريبي** – سنستخدم `OneLayer.psd` في الأمثلة.

## استيراد الحزم

أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك. هذه الفئات توفر الوظائف الأساسية لـ **psd image manipulation** ومعالجة الطبقات.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## ما هو “set layer position” ولماذا هو مهم؟

عند إضافة طبقة جديدة، تحتاج إلى تحديد مكان ظهورها على القماش. طرق `setLeft`، `setTop`، `setRight` و `setBottom` **set layer position** بإحداثيات بكسل. يضمن التموقع الصحيح أن تتطابق رسوماتك تمامًا مع ما تتوقعه، وهو أمر حاسم لمهام مثل تركيب أصول واجهة المستخدم أو إعداد ملفات جاهزة للطباعة.

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف PSD

أولاً، حمّل ملف PSD الموجود الذي تريد تعديله. سيعطيك ذلك كائن `PsdImage` يمكنك العمل معه.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### الخطوة 2: إعداد بيانات البكسل والمستطيلات

سننشئ مخزنين بكسل (`int[]`) ونحدد المناطق المستطيلة التي ستُرسم فيها الطبقات الجديدة. هذا هو الأساس لـ **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### الخطوة 3: تهيئة بيانات الطبقة

املأ مخازن البكسل بقيمة ARGB افتراضية. القيمة `-10000000` تمثل ظلًا داكنًا شبه شفاف.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### الخطوة 4: إضافة طبقات عادية (Manipulate PSD Layers)

الآن **نضيف طبقات عادية** إلى صورة PSD و**نحدد موضع الطبقة** باستخدام خصائص اليسار، الأعلى، اليمين، والأسفل. يوضح هذا كيفية **manipulate PSD layers** برمجيًا.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### الخطوة 5: تصدير PSD إلى PNG وحفظ PSD المحدث

بعد وضع الطبقات، احفظ المستند المعدل. أولاً نصدر النتيجة إلى PNG (خطوة **export psd to png**)، ثم نحفظ ملف PSD مع الطبقات الجديدة.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **نصيحة احترافية:** إذا كنت تحتاج فقط إلى PNG، يمكنك تخطي استدعاء `save` الخاص بـ PSD واستدعاء `save` مباشرةً مع `PngOptions`.

## المشكلات الشائعة & استكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| PNG يظهر فارغًا | الطبقات غير مرئية أو شفافة تمامًا | تأكد من ضبط قيم بكسل غير شفافة أو استدعاء `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | عدم توافق حجم المستطيل مع طول مصفوفة البكسل | تحقق من أن `rect.width * rect.height == dataArray.length`. |
| LicenseException أثناء التشغيل | لم يتم تحميل ترخيص صالح | حمّل ترخيصًا مؤقتًا أو دائمًا قبل استدعاء أي من طرق الـ API. |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع Java 8؟**  
ج: نعم، Aspose.PSD يدعم Java 8 والإصدارات الأحدث.

**س: هل يمكنني تطبيق تحولات (دوران، تكبير) على الطبقات المضافة؟**  
ج: بالتأكيد! توفر فئة `Layer` طرقًا مثل `rotate`، `scale`، و `translate` للتحكم الكامل في التحولات.

**س: أين يمكنني العثور على وثائق Aspose.PSD الإضافية؟**  
ج: الوثائق التفصيلية للـ API متاحة [هنا](https://reference.aspose.com/psd/java/).

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: زر صفحة الترخيص المؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**س: هل توجد منتديات مجتمع لدعم Aspose.PSD؟**  
ج: نعم، انضم إلى المناقشات على منتديات Aspose [هنا](https://forum.aspose.com/c/psd/34).

## الخلاصة

لقد تعلمت الآن كيفية **export PSD to PNG** مع **إضافة طبقات عادية جديدة** باستخدام Aspose.PSD للـ Java، ورأيت كيف يتيح لك **ترخيص Aspose المؤقت** تجربة هذا سير العمل دون قيود. يعرض هذا الدرس قدرات **psd image manipulation** الأساسية: تحميل ملف، إنشاء طبقات، ملء بيانات البكسل، وتصدير التركيبة النهائية. لا تتردد في تجربة أحجام مستطيلات مختلفة، ألوان بكسل، أو تأثيرات طبقة لتخصيص النتيجة وفقًا لاحتياجات مشروعك.

---

**آخر تحديث:** 2026-04-08  
**تم الاختبار مع:** Aspose.PSD 24.11 للـ Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}