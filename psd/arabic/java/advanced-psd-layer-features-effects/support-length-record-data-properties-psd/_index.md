---
date: 2025-12-17
description: تعلم كيفية تعديل أشكال المتجهات في ملفات PSD بدعم خصائص بيانات سجل الطول
  باستخدام Aspose.PSD للغة Java. دليل خطوة بخطوة مع أمثلة على الشيفرة.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: كيفية تعديل أشكال المتجهات في PSD – دعم خصائص بيانات سجل الطول في Java
url: /ar/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم خصائص بيانات سجل الطول في PSD - Java

## مقدمة
إذا كنت بحاجة إلى **تعديل أشكال المتجهات في PSD** برمجيًا، فإن مكتبة Aspose.PSD for Java تمنحك التحكم الكامل في ملفات Photoshop مباشرة من كود Java الخاص بك. في هذا الدرس سنستعرض كل ما تحتاج معرفته لدعم خصائص بيانات سجل الطول — خطوة أساسية عندما تريد تعديل طبقات الأشكال المتجهية. في النهاية، ستكون قادرًا على فتح ملف PSD، تعديل خصائص الشكل المتجهي، وحفظ الملف المحدث دون مغادرة بيئة التطوير المتكاملة الخاصة بك. هيا نبدأ!

## إجابات سريعة
- **ما معنى “تعديل أشكال المتجهات في PSD”؟** تعديل الهندسة، عمليات المسار، أو خصائص أخرى للطبقات القائمة على المتجهات داخل ملف PSD.  
- **أي مكتبة تتعامل مع ذلك؟** Aspose.PSD for Java.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتقييم؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **كم من الوقت تستغرق العملية؟** حوالي 10‑15 دقيقة لسكريبت تعديل شكل أساسي.  
- **ما هي المتطلبات الأساسية؟** Java JDK، Aspose.PSD for Java، وعينة ملف PSD.

## ما هو “تعديل أشكال المتجهات في PSD”؟
يتضمن تعديل أشكال المتجهات في PSD تغيير بيانات مسار المتجه الأساسي — مثل سجلات الطول وعمليات المسار — بحيث يتم تحديث المظهر البصري للأشكال وفقًا لذلك. هذا مفيد بشكل خاص لخطوط إنتاج الرسومات الآلية، المعالجة الدفعية، أو أدوات التصميم المخصصة.

## لماذا نستخدم Aspose.PSD for Java لتعديل أشكال المتجهات في PSD؟
- **لا حاجة لبرنامج Photoshop** – العمل مباشرةً مع ملفات PSD على أي خادم.  
- **API غني** – الوصول إلى الطبقات والموارد وبيانات المتجهات باستخدام فئات ذات نوعية قوية.  
- **متعدد المنصات** – تشغيل على Windows أو Linux أو macOS مع أي JDK.  
- **مركز على الأداء** – معالجة ذاكرة فعّالة وعمليات حفظ سريعة.

## المتطلبات المسبقة
1. **Java Development Kit (JDK)** – قم بتنزيله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) أو استخدم مدير الحزم المفضل لديك.  
2. **Aspose.PSD for Java** – احصل على أحدث ملف JAR من [صفحة إصدارات Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر متوافق مع Java.  
4. **ملف PSD** – أنشئ واحدًا في Photoshop أو احصل على عينة PSD للتجربة.  
5. **معرفة أساسية بـ Java** – الإلمام بالفئات، الكائنات، ومعالجة الاستثناءات.

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها للعمل مع ملفات PSD وموارد الأشكال المتجهية.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## الخطوة 1: إعداد مجلدات المصدر والإخراج
حدد موقع ملف PSD الأصلي ومكان حفظ الملف المعدل.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## الخطوة 2: تحميل ملف PSD
استخدم `Image.load` لفتح الملف وحوله إلى `PsdImage` للوصول إلى ميزات PSD الخاصة.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## الخطوة 3: تحديد مورد Vsms في الطبقة
بيانات الشكل المتجهي موجودة داخل `VsmsResource`. قم بالتكرار عبر موارد الطبقة الثانية للعثور عليه.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## الخطوة 4: الوصول إلى سجلات الطول
كل `LengthRecord` يمثل مسارًا متجهيًا مميزًا. احصل على السجلات التي تنوي تعديلها.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## الخطوة 5: تعديل خصائص عمليات المسار
الآن يمكنك **تعديل أشكال المتجهات في PSD** عن طريق تغيير `PathOperations` الخاصة بها. هذا يحدد كيفية تفاعل الأشكال (مثل الاستبعاد، التقاطع، الطرح).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## الخطوة 6: حفظ ملف PSD المعدل
احفظ تغييراتك في ملف جديد.

```java
psdImage.save(outPsdFilePath);
```

## الخطوة 7: تنظيف الموارد
قم بتحرير `PsdImage` لتفريغ الذاكرة.

```java
psdImage.dispose();
```

## الأخطاء الشائعة والنصائح
- **فحص القيم الفارغة** – تأكد دائمًا أن `resource` ليست `null` قبل الوصول إلى المسارات.  
- **حدود فهارس المسار** – تأكد من أن الفهارس التي تستخدمها (`[2]`, `[7]`, `[11]`) موجودة في ملف PSD المحدد الذي تقوم بتحريره.  
- **الترخيص** – تشغيل البرنامج بدون ترخيص صالح سيضيف علامة مائية إلى ملف PSD المحفوظ.

## الخلاصة
أصبح لديك الآن مثال كامل من البداية إلى النهاية حول كيفية **تعديل أشكال المتجهات في PSD** بدعم خصائص بيانات سجل الطول باستخدام Aspose.PSD for Java. سواء كنت تقوم بأتمتة خطوط إنتاج الأصول أو بناء أداة تصميم مخصصة، فإن هذه الـ APIs تمنحك المرونة لتعديل الطبقات المتجهية دون الحاجة إلى عمل يدوي في Photoshop. استكشف المزيد بتجربة `PathOperations` أخرى أو دمج تعديلات `LengthRecord` متعددة للحصول على أشكال معقدة.

## الأسئلة المتكررة
### ما هو Aspose.PSD for Java؟
Aspose.PSD for Java هي مكتبة تتيح للمطورين تعديل والعمل مع ملفات Photoshop PSD برمجيًا باستخدام Java.

### هل يمكنني استخدام Aspose.PSD في مشروع مجاني؟
نعم، يمكنك تجربة المكتبة مجانًا باستخدام النسخة التجريبية المتوفرة على موقع Aspose.

### ما أنواع التعديلات التي يمكنني إجراؤها على ملفات PSD؟
يمكنك تعديل الطبقات، الأشكال، النصوص، عمليات المسار، وأكثر من ذلك داخل ملفات PSD.

### هل Aspose.PSD متوافق مع لغات برمجة أخرى؟
نعم، تقدم Aspose مكتبات مختلفة للغات برمجة متعددة، بما في ذلك .NET وPython.

### أين يمكنني العثور على وثائق Aspose.PSD؟
يمكنك الوصول إلى الوثائق الكاملة [هنا](https://reference.aspose.com/psd/java/).

## أسئلة شائعة
**س: كيف أتعامل مع PSD لا يحتوي على طبقات أشكال متجهية؟**  
ج: سيكون `VsmsResource` غير موجود، وبالتالي سيبقى `resource` `null`. أضف فحصًا وتجاوز خطوة التعديل أو أخطر المستخدم.

**س: هل يمكنني تغيير خصائص أخرى مثل لون التعبئة أو عرض الحد؟**  
ج: نعم، يوفر `LengthRecord` إعدادات إضافية للتعبئة، الحد، والشفافية. راجع وثائق الـ API للحصول على التفاصيل الكاملة.

**س: هل يمكن معالجة عدة ملفات PSD دفعيًا؟**  
ج: بالتأكيد. ضع الكود داخل حلقة تتكرر عبر دليل يحتوي على ملفات PSD، مع تعديل مسارات الإدخال والإخراج في كل مرة.

**س: هل يجب إغلاق التدفقات يدويًا عند التحميل من مسار ملف؟**  
ج: طريقة `Image.load` تتعامل مع تدفقات الملفات داخليًا، لكن إذا قمت بالتحميل من `InputStream`، تذكر إغلاقه بعد الاستخدام.

**س: ما هو إصدار Aspose.PSD المطلوب لهذه الـ APIs؟**  
ج: تتوفر فئات `LengthRecord` و `PathOperations` منذ Aspose.PSD 20.10. يُنصح باستخدام أحدث إصدار.

---

**آخر تحديث:** 2025-12-17  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}