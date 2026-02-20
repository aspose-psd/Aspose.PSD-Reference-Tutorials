---
date: 2026-02-20
description: تعلم كيفية دعم خصائص سجلات الطول ومعالجة ملفات PSD دفعيًا باستخدام Aspose.PSD
  للـ Java. دليل خطوة بخطوة مع أمثلة على الشيفرة.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: دعم خصائص سجل الطول – تعديل أشكال PSD المتجهة (جافا)
url: /ar/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم خصائص سجل الطول – تعديل أشكال PSD المتجهة (Java)

## المقدمة
إذا كنت بحاجة إلى **تعديل أشكال PSD المتجهة** برمجياً، فإن مكتبة Aspose.PSD for Java تمنحك التحكم الكامل في ملفات Photoshop مباشرة من كود Java الخاص بك. في هذا البرنامج التعليمي سنستعرض كل ما تحتاج معرفته **لدعم خصائص سجل الطول**—خطوة أساسية عندما تريد تعديل طبقات الأشكال المتجهة. في النهاية، ستكون قادرًا على فتح ملف PSD، تعديل خصائص الشكل المتجه، وحفظ الملف المحدث دون مغادرة بيئة التطوير المتكاملة. هيا نبدأ!

## إجابات سريعة
- **ماذا يعني “تعديل أشكال PSD المتجهة”؟** تعديل الهندسة، عمليات المسار، أو خصائص أخرى للطبقات القائمة على المتجهات داخل ملف PSD.  
- **أي مكتبة تتعامل مع ذلك؟** Aspose.PSD for Java.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتقييم؛ الترخيص التجاري مطلوب للإنتاج.  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لكتابة سكريبت تعديل شكل أساسي.  
- **ما هي المتطلبات الأساسية؟** Java JDK، Aspose.PSD for Java، وملف PSD تجريبي.

## ما معنى “دعم خصائص سجل الطول”؟
دعم خصائص سجل الطول يعني الوصول إلى كائنات `LengthRecord` التي تصف كل مسار متجه داخل PSD وتحديثها. تعديل هذه السجلات يتيح لك التحكم في كيفية دمج الأشكال، تقاطعها، أو طرحها من بعضها البعض.

## لماذا نستخدم Aspose.PSD for Java لدعم خصائص سجل الطول؟
- **لا حاجة لـ Photoshop** – العمل مباشرة مع ملفات PSD على أي خادم.  
- **API غني** – الوصول إلى الطبقات، الموارد، وبيانات المتجهات باستخدام فئات ذات نوعية قوية.  
- **متعدد المنصات** – يعمل على Windows، Linux، أو macOS مع أي JDK.  
- **مركز على الأداء** – إدارة ذاكرة فعّالة وعمليات حفظ سريعة.  

## المتطلبات المسبقة
1. **Java Development Kit (JDK)** – حمّله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) أو استخدم مدير الحزم المفضل لديك.  
2. **Aspose.PSD for Java** – احصل على أحدث ملف JAR من [صفحة إصدارات Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA، Eclipse، أو أي محرر يدعم Java.  
4. **ملف PSD** – أنشئه في Photoshop أو احصل على ملف PSD تجريبي لتجربة الكود.  
5. **معرفة أساسية بـ Java** – إلمام بالفئات، الكائنات، ومعالجة الاستثناءات.

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها للعمل مع ملفات PSD وموارد الأشكال المتجهة.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## الخطوة 1: إعداد مسارات المصدر والإخراج
حدد مكان وجود ملف PSD الأصلي وأين تريد حفظ الملف المعدل.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## الخطوة 2: تحميل ملف PSD
استخدم `Image.load` لفتح الملف وحوله إلى `PsdImage` للاستفادة من الميزات الخاصة بـ PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## الخطوة 3: تحديد مورد Vsms في الطبقة
بيانات الشكل المتجه توجد داخل `VsmsResource`. قم بالتكرار عبر موارد الطبقة الثانية للعثور عليه.

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
كل `LengthRecord` يمثل مسارًا متجهاً مميزًا. احصل على السجلات التي تنوي تعديلها.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## الخطوة 5: تعديل خصائص عمليات المسار
الآن يمكنك **تعديل أشكال PSD المتجهة** عن طريق تغيير `PathOperations`. هذا يحدد كيفية تفاعل الأشكال (مثل الاستبعاد، التقاطع، الطرح).

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

## كيفية معالجة ملفات PSD دفعيًا مع دعم خصائص سجل الطول
إذا كنت بحاجة لتطبيق نفس تعديلات الأشكال المتجهة على العديد من ملفات PSD، غلف الكود أعلاه داخل حلقة تتكرر عبر مجلد الملفات. حدّث `inPsdFilePath` و `outPsdFilePath` لكل تكرار، وستتمكن من **معالجة ملفات PSD دفعيًا** بفعالية.

## الأخطاء الشائعة والنصائح
- **التحقق من القيم الفارغة** – تأكد دائمًا أن `resource` ليس `null` قبل الوصول إلى المسارات.  
- **حدود فهارس المسار** – تأكد من وجود الفهارس التي تستخدمها (`[2]`، `[7]`، `[11]`) في ملف PSD المحدد.  
- **الترخيص** – تشغيل البرنامج بدون ترخيص صالح سيضيف علامة مائية إلى ملف PSD المحفوظ.  

## الخلاصة
أصبح لديك الآن مثال كامل من البداية إلى النهاية حول كيفية **تعديل أشكال PSD المتجهة** بدعم خصائص سجل الطول باستخدام Aspose.PSD for Java. سواء كنت تقوم بأتمتة خطوط إنتاج الأصول أو بناء أداة تصميم مخصصة، تمنحك هذه الـ APIs المرونة للتعامل مع طبقات المتجهات دون الحاجة إلى Photoshop يدويًا. استكشف المزيد بتجربة `PathOperations` أخرى أو دمج تعديلات `LengthRecord` متعددة لأشكال معقدة.

## الأسئلة المتكررة

**س: كيف أتعامل مع PSD لا يحتوي على طبقات شكل متجه؟**  
ج: سيكون `VsmsResource` غير موجود، وبالتالي سيبقى `resource` `null`. أضف فحصًا وتخطى خطوة التعديل أو أخطر المستخدم.

**س: هل يمكنني تغيير خصائص أخرى مثل لون التعبئة أو عرض الحد؟**  
ج: نعم، يوفر `LengthRecord` setters إضافية للملء، الحد، والشفافية. راجع وثائق الـ API للحصول على التفاصيل الكاملة.

**س: هل يمكن معالجة عدة ملفات PSD دفعيًا؟**  
ج: بالتأكيد. غلف الكود داخل حلقة تتكرر عبر مجلد ملفات PSD، مع تعديل مسارات الإدخال والإخراج في كل مرة.

**س: هل يجب إغلاق التيارات يدويًا عند التحميل من مسار ملف؟**  
ج: طريقة `Image.load` تتعامل مع التيارات داخليًا، لكن إذا قمت بالتحميل من `InputStream`، تذكر إغلاقه بعد الاستخدام.

**س: ما هو الإصدار المطلوب من Aspose.PSD لهذه الـ APIs؟**  
ج: فئات `LengthRecord` و `PathOperations` متوفرة منذ Aspose.PSD 20.10. يُنصح باستخدام أحدث نسخة.

---

**آخر تحديث:** 2026-02-20  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}