---
date: 2026-03-28
description: تعلم كيفية إنشاء طبقة فلتر صورة وإضافة طبقة تعديل لملفات PSD باستخدام
  Aspose.PSD للغة Java. اتبع هذا الدليل لتحرير وإضافة الفلاتر بسهولة.
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: كيفية إنشاء طبقة فلتر صورة في PSD باستخدام جافا
url: /ar/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدارة طبقة تعديل الفلتر الضوئي في PSD - Java

## مقدمة
إذا كنت مطور Java تبحث عن **إنشاء طبقة فلتر صورة** داخل ملفات PSD، فقد وصلت إلى المكان المناسب. في هذا البرنامج التعليمي سنستعرض كيفية استخدام Aspose.PSD for Java لتعديل طبقات تعديل الفلتر الضوئي الموجودة وإضافة طبقات جديدة. في النهاية، ستعرف بالضبط كيفية **إنشاء طبقة فلتر صورة**، تعديل خصائصها، وحتى **إضافة طبقة تعديل PSD** برمجيًا—مما يسرّع سير عمل التصميم الجرافيكي الخاص بك.

## إجابات سريعة
- **أي مكتبة تتعامل مع طبقات PSD في Java؟** Aspose.PSD for Java  
- **هل يمكنني تعديل طبقة فلتر صورة موجودة؟** نعم – قم بتحميل PSD، حدد `PhotoFilterLayer`، ثم عدّل خصائصها.  
- **كيف يمكنني إضافة طبقة فلتر جديدة؟** استخدم `addPhotoFilterLayer(Color)` على كائن `PsdImage`.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم الحصول على ترخيص تجاري؛ تتوفر نسخة تجريبية مجانية.  
- **ما نسخة Java المدعومة؟** JDK 8 أو أعلى (يوصى بـ JDK 11).  

## ما هي طبقة تعديل الفلتر الضوئي؟
طبقة تعديل الفلتر الضوئي هي تأثير غير مدمر يلون الصورة بالكامل بلون مختار، مشابه لتطبيق فلتر فوتوغرافي. توجد على طبقة خاصة بها، مما يتيح لك تعديل اللون والكثافة والسطوع دون تغيير البكسلات الأصلية.

## لماذا تستخدم Aspose.PSD لإنشاء طبقة فلتر صورة؟
- **تحكم كامل** في بنية PSD دون الحاجة إلى Adobe Photoshop.  
- **متعدد المنصات** API Java يعمل على Windows وLinux وmacOS.  
- **بدون COM interop** – Java نقي، مثالي للمعالجة على الخادم.  
- **يدعم إصدار PSD 1‑8**، مع الحفاظ على تأثيرات الطبقات والأقنعة.  

## المتطلبات المسبقة
### البرامج الأساسية
1. Java Development Kit (JDK): تأكد من أن لديك نسخة متوافقة من JDK مثبتة على جهازك. يمكنك تنزيلها من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: للتعامل مع ملفات PSD، ستحتاج إلى مكتبة Aspose.PSD. يمكنك تنزيلها من [صفحة إصدارات Aspose](https://releases.aspose.com/psd/java/). لا تنسَ الاطلاع على [توثيق Aspose](https://reference.aspose.com/psd/java/) لمزيد من التفاصيل.
3. IDE (بيئة التطوير المتكاملة): بيئة تطوير جيدة مثل IntelliJ IDEA أو Eclipse ستجعل تجربة البرمجة أكثر سلاسة.

### فهم الأساسيات
الإلمام ببرمجة Java وفهم أساسي لكيفية عمل ملفات PSD سيكون مفيدًا. إذا كنت جديدًا على استخدام المكتبات في Java، فمن الجيد أن تعتاد على استيراد واستخدام الأطر.

## استيراد الحزم
لبدء العمل، نحتاج إلى استيراد الفئات الضرورية من مكتبة Aspose.PSD. إليك بيان استيراد بسيط ستحتاجه في بداية ملف Java الخاص بك:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Simply paste this at the top of your Java file, and you’re set to begin working with PSD images!

## تعديل طبقة الفلتر الضوئي الموجودة
### الخطوة 1: إعداد دليل البيانات
أولاً، تحتاج إلى تحديد الدليل الذي تُخزن فيه ملفات PSD الخاصة بك. استبدل `"Your Document Directory"` بالمسار الفعلي. هكذا تنظم كل شيء:
```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحميل ملف PSD الخاص بك
الآن، لنحمّل ملف PSD الذي تريد تعديله. تأكد من وجود `PhotoFilterAdjustmentLayer.psd` في الدليل المحدد.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### الخطوة 3: تهيئة كائن الصورة
باستخدام وظائف Aspose المدمجة، نقوم بتحميل الصورة إلى مشروعنا:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### الخطوة 4: التجوال عبر الطبقات
بعد ذلك، سنفحص الطبقات داخل ملف PSD. هدفنا هو العثور على `PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### الخطوة 5: تخصيص طبقة الفلتر الضوئي
هنا يحدث السحر! يمكنك تعديل `Color` و `Density`. على سبيل المثال، يمكننا ضبط اللون إلى أحمر زاهي وتعديل الكثافة:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### الخطوة 6: حفظ ملف PSD المعدل
أخيرًا، احفظ التغييرات لإنشاء ملف PSD جديد مع التعديلات الخاصة بك:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
لقد قمت للتو بتعديل طبقة تعديل الفلتر الضوئي في ملف PSD.

## إضافة طبقة فلتر صورة جديدة
### الخطوة 1: إعداد مسار الدليل
كما في السابق، نبدأ بتحديد دليل البيانات الخاص بنا:
```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحميل الملف المصدر
في هذا المثال، لنحمّل ملف PSD مختلف حيث نريد **إضافة طبقة تعديل PSD**:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### الخطوة 3: تهيئة كائن الصورة مرة أخرى
يجب إنشاء مثيل جديد من `PsdImage`، لذا نقوم بتحميل الملف:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### الخطوة 4: إضافة طبقة فلتر صورة
الآن، يمكننا إضافة طبقة فلتر صورة جديدة بلون مخصص. إليك الطريقة:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### الخطوة 5: حفظ ملف PSD الجديد
مرة أخرى، حان وقت حفظ التغييرات. إليك السطر للقيام بذلك:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
لقد أضفت بنجاح طبقة فلتر صورة جديدة إلى ملف PSD الخاص بك.

## المشكلات الشائعة والحلول
- **`ClassCastException` عند تحميل الصورة** – تأكد من أن الملف الذي تحمّله هو PSD؛ الصيغ الأخرى تتطلب فئات مختلفة.  
- **قيمة اللون تظهر غير صحيحة** – استخدم `Color.fromArgb(alpha, red, green, blue)` حيث كل مكوّن يتراوح بين 0‑255.  
- **الطبقة غير موجودة** – تحقق من أن ملف PSD المصدر يحتوي فعليًا على `PhotoFilterLayer`. استخدم `im.getLayers().length` للتصحيح.  

## الأسئلة المتكررة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة .NET وJava لإنشاء وتعديل وتحويل ملفات PSD.

### هل يمكنني تجربة Aspose.PSD مجانًا؟
نعم، تقدم Aspose نسخة تجريبية مجانية. تحقق منها [هنا](https://releases.aspose.com/).

### أين يمكنني العثور على الوثائق؟
يمكنك العثور على الوثائق الكاملة في [صفحة مرجع Aspose](https://reference.aspose.com/psd/java/).

### كيف يمكنني شراء Aspose.PSD؟
يمكنك شراء البرنامج من [هذا الرابط](https://purchase.aspose.com/buy).

### هل هناك دعم متاح لـ Aspose.PSD؟
بالطبع! يمكنك الحصول على الدعم عبر منتدى دعم Aspose [هنا](https://forum.aspose.com/c/psd/34).

---

**آخر تحديث:** 2026-03-28  
**تم الاختبار مع:** Aspose.PSD for Java 24.11 (latest as of 2026)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}