---
date: 2026-03-28
description: تعلم كيفية إنشاء طبقة PSD جديدة وإدارة تاريخ ووقت إنشائها باستخدام Aspose.PSD
  للغة Java. يغطي هذا الدليل خطوة بخطوة تحميل الطبقات، قراءتها، التحقق منها، وإضافتها.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: إنشاء طبقة PSD جديدة وإدارة تاريخ ووقت الإنشاء في جافا
url: /ar/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء طبقة PSD جديدة وإدارة تاريخ ووقت الإنشاء في Java

## مقدمة
عند العمل مع ملفات Photoshop (PSD) برمجيًا، القدرة على **create new PSD layer** وتتبع الطوابع الزمنية لإنشائها تُعدّ تغييرًا جذريًا. سواء كنت تبني نظام تحكم إصدارات لأصول التصميم، أو تُؤتمت تعديلات دفعية، أو تحتاج فقط إلى سجل تدقيق للمشاريع التعاونية، فإن معرفة كيفية قراءة وتعيين تاريخ إنشاء الطبقة يتيح لك الحفاظ على أصالة كل تعديل. في هذا الدرس سنستعرض العملية بالكامل باستخدام Aspose.PSD for Java — من تحميل ملف PSD، جلب تاريخ إنشاء الطبقة، التحقق منه، وحتى إضافة طبقة تعديل جديدة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع ملفات PSD في Java؟** Aspose.PSD for Java  
- **هل يمكنني قراءة تاريخ إنشاء الطبقة؟** نعم، باستخدام `layer.getLayerCreationDateTime()`  
- **هل من الممكن إضافة طبقة تعديل جديدة؟** بالتأكيد – `im.addLevelsAdjustmentLayer()` ينشئ واحدة  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** الترخيص التجاري مطلوب للنشر غير التجريبي  
- **ما إصدار Java المدعوم؟** JDK 8 أو أحدث  

## ما هو “create new PSD layer”؟
إنشاء طبقة PSD جديدة يعني إدراج كائن طبقة جديد برمجيًا — مثل طبقة تعديل أو نص أو بكسل — داخل مستند PSD موجود. تتيح لك هذه العملية توسيع أو تعديل الصورة دون الحاجة إلى فتح Photoshop يدويًا.

## لماذا إدارة تاريخ ووقت إنشاء الطبقة؟
- **تدقيق التعديلات** – معرفة بالضبط متى تمت إضافة الطبقة.  
- **مزامنة الأصول** عبر الفرق عن طريق مقارنة الطوابع الزمنية.  
- **أتمتة سير العمل** الذي يعتمد على قواعد زمنية (مثال: إخفاء الطبقات الأقدم من شهر).  

## المتطلبات المسبقة
قبل الغوص في التفاصيل، تأكد من توفر ما يلي:

1. **Java Development Kit (JDK)** – الإصدار 8 أو أحدث.  
2. **IDE** – IntelliJ IDEA، Eclipse، NetBeans، أو أي محرر تفضله.  
3. **Aspose.PSD for Java** – يمكنك [تحميله هنا](https://releases.aspose.com/psd/java/) للتثبيت.  
4. **معرفة أساسية بـ Java** – إذا كنت جديدًا على Java، لا تقلق؛ الكود مشروح بالكامل.

هل لديك كل شيء؟ رائع! لننتقل إلى الجزء الممتع من البرمجة.

## استيراد الحزم
أولاً، استورد فئات Aspose.PSD وأدوات Java التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى معالجة الصور، تعديل الطبقات، وتنسيق التواريخ.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## الخطوة 1: إعداد دليل المستند الخاص بك
حدد المجلد الذي يحتوي على ملف PSD الذي تريد العمل معه. استبدل العنصر النائب بالمسار المطلق على جهازك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل ملف PSD
أنشئ كائن `PsdImage` بتحميل الملف المستهدف. هذا الكائن هو نقطة الدخول لجميع عمليات الطبقة.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## الخطوة 3: الوصول إلى الطبقة وتاريخ إنشائها
احصل على الطبقة الأولى (الفهرس 0) واسترجع طابعها الزمني للإنشاء. هذا هو التاريخ الذي ستقارن أو تسجله لاحقًا.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## الخطوة 4: تنسيق تاريخ الإنشاء
حوّل كائن `Date` الخام إلى سلسلة قابلة للقراءة للإنسان. عدّل النمط إذا كنت تفضّل تنسيقًا مختلفًا.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## الخطوة 5: التحقق من صحة تاريخ الإنشاء
للتوضيح، نقارن التاريخ المسترجع بقيمة متوقعة. في المشاريع الحقيقية قد تقارن ضد سجل قاعدة بيانات أو ملف إعدادات.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## الخطوة 6: إنشاء طبقة جديدة
الآن نقوم فعليًا بإنشاء كائنات **create new PSD layer**. هنا نضيف طبقة تعديل Levels، التي تسمح لك بضبط النطاقات اللونية دون تغيير البكسلات الأصلية.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **نصيحة احترافية:** المتغير `now` يلتقط اللحظة التي تضيف فيها الطبقة، ويمكنك لاحقًا تخزينه كبيانات تعريف إذا كنت بحاجة إلى طابع زمني مخصص.

## المشكلات الشائعة والحلول
| المشكلة | سبب حدوثها | الحل |
|-------|----------------|-----|
| `NullPointerException` on `layer.getLayerCreationDateTime()` | ملف PSD لا يحتوي على طبقات أو أن فهرس الطبقة خارج النطاق. | تحقق من أن `im.getLayers().length > 0` قبل الوصول. |
| عدم تطابق التاريخ في التحقق | منشئ `Date` يحلل السلاسل وفقًا للغة المحلية. | استخدم `SimpleDateFormat.parse("2018/07/17 08:57:24")` للحصول على تحليل موثوق. |
| الطبقة الجديدة غير مرئية في Photoshop | قد تكون طبقة التعديل مخفية بشكل افتراضي. | استدعِ `createdLayer.setVisible(true);` بعد الإنشاء. |

## الخاتمة
أنت الآن تعرف كيف تنشئ كائنات **create new PSD layer**، تقرأ طوابع إنشائها، تتحقق من صحتها، وتضيف طبقات تعديل — كل ذلك باستخدام Aspose.PSD for Java. هذه القدرة تفتح الباب أمام أتمتة متقدمة، سجلات تدقيق، وسير عمل تعاوني في أي خط أنابيب معالجة صور مبني على Java.

إذا استمتعت بهذا الدرس، استكشف ميزات Aspose.PSD الأخرى مثل دمج الطبقات، تطبيق الفلاتر، أو التصدير إلى صيغ مختلفة. الاحتمالات لا حصر لها!

## الأسئلة الشائعة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة قوية للعمل مع ملفات Photoshop (PSD) برمجيًا.

### هل يمكنني استخدام Aspose.PSD مجانًا؟
نعم! يمكنك البدء بتجربة مجانية متاحة [هنا](https://releases.aspose.com/).

### هل أحتاج إلى شراء ترخيص للاستخدام طويل الأمد؟
نعم، يمكنك الحصول على ترخيص [هنا](https://purchase.aspose.com/buy) عندما تكون جاهزًا.

### أين يمكنني العثور على مزيد من المعلومات حول Aspose.PSD؟
يمكنك الاطلاع على [الوثائق](https://reference.aspose.com/psd/java/) للحصول على أدلة مفصلة ومراجع API.

### كيف يمكنني طلب الدعم إذا واجهت مشكلات مع Aspose.PSD؟
لا تتردد في زيارة [منتدى الدعم](https://forum.aspose.com/c/psd/34) للحصول على مساعدة المجتمع.

---

**آخر تحديث:** 2026-03-28  
**تم الاختبار مع:** Aspose.PSD for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}