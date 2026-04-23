---
date: 2026-03-07
description: تعرّف على كيفية إضافة النص إلى ملفات PSD في وقت التشغيل باستخدام Java
  و Aspose.PSD. اتبع هذا الدليل خطوة بخطوة لإنشاء طبقة نصية في ملف PSD بسرعة.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: إضافة نص إلى ملفات PSD في وقت التشغيل باستخدام Java
url: /ar/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة نص إلى ملفات PSD في وقت التشغيل باستخدام Java

## المقدمة
إذا سبق لك تعديل مستند Photoshop يدويًا، فأنت تعرف مدى قوة الطبقات. ماذا لو كان بإمكانك **إضافة نص إلى PSD** تلقائيًا من تطبيق Java الخاص بك؟ باستخدام مكتبة Aspose.PSD for Java، يمكنك إنشاء طبقة نصية في ملف PSD أثناء وقت التشغيل، مما يفتح الباب للمعالجة الدفعية، وتوليد الرسومات الديناميكية، وتدفقات عمل العلامة التجارية المؤتمتة. في هذا الدرس سنستعرض العملية بالكامل، من إعداد المشروع إلى حفظ الملف المحدث.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java.  
- **هل يمكنني إضافة نص إلى PSD موجود؟** Yes – simply load the file, add a `TextLayer`, and save.  
- **هل أحتاج إلى ترخيص للإنتاج؟** A commercial license is required for non‑evaluation use.  
- **ما نسخة Java المدعومة؟** JDK 8 or higher (we recommend the latest LTS).  
- **هل هذا مناسب لخوادم الويب الخلفية؟** Absolutely – the API works in any Java‑based server environment.

## ما هو “إضافة نص إلى PSD”؟
إضافة نص إلى PSD تعني إنشاء طبقة نصية جديدة داخل مستند Photoshop برمجيًا. تتصرف الطبقة مثل أي طبقة نصية أخرى في Photoshop: يمكنك تحريكها، تعديل محتواها، وتطبيق الأنماط — كل ذلك دون فتح Photoshop.

## لماذا إنشاء طبقة نصية في PSD باستخدام Java؟
- **Automation** – توليد أصول تسويقية، علامات مائية، أو ملصقات منتجات بالجملة.  
- **Consistency** – ضمان نفس الخط، الحجم، والموضع عبر آلاف الملفات.  
- **Integration** – دمج مع خدمات Java الأخرى (التجارة الإلكترونية، التقارير، خطوط أنابيب CI) لتسليم الرسومات مباشرة.

## المتطلبات المسبقة
قبل كتابة الكود، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – تثبيت JDK 8 أو أحدث. يمكنك [download it here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – احصل على أحدث JAR من [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE (optional but helpful)** – IntelliJ IDEA، Eclipse، أو أي محرر تفضله.  
4. **Basic Java knowledge** – يجب أن تكون مرتاحًا مع الفئات، الكائنات، وملفات الإدخال/الإخراج.  
5. **A sample PSD** – سنستخدم في هذا الدليل `OneLayer.psd` موجودًا في مجلد من اختيارك.

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها للعمل مع ملفات PSD وطبقات النص.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

تمنحك هذه الاستيرادات الوصول إلى الوظائف الأساسية لمكتبة Aspose.PSD.

## دليل خطوة بخطوة

### الخطوة 1: إعداد دليل المستندات الخاص بك
حدد المجلد الذي يحتوي على ملف PSD المصدر ومكان حفظ الناتج.

```java
String dataDir = "Your Document Directory"; 
```

استبدل `"Your Document Directory"` بالمسار المطلق أو النسبي إلى ملفاتك.

### الخطوة 2: تحميل ملف PSD المصدر الخاص بك
قم بتحميل ملف PSD الموجود إلى الذاكرة باستخدام `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

إذا كان المسار صحيحًا، فإن `img` الآن يمثل مستند Photoshop المحمل.

### الخطوة 3: تحويل إلى `PsdImage`
نظرًا لأننا نتعامل مع ميزات خاصة بـ Photoshop، نقوم بتحويل الكائن العام `Image` إلى `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

يتيح هذا التحويل الوصول إلى طرق مثل `addTextLayer()`.

### الخطوة 4: تعريف المستطيل لطبقة النص
حدد مكان ظهور النص الجديد. يحدد المستطيل الموضع (x, y) والحجم (العرض, الارتفاع).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

يمكنك تعديل الحسابات لتناسب احتياجات تخطيطك.

### الخطوة 5: إضافة طبقة النص
إنشاء طبقة النص الفعلية داخل المستطيل المحدد.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

استبدل `"Added text"` بأي سلسلة تريد ظهورها في PSD. هذا هو المكان الذي **ننشئ فيه طبقة نصية في PSD** برمجيًا.

### الخطوة 6: حفظ ملف PSD المحدث
اكتب المستند المعدل إلى ملف جديد حتى لا تكتب فوق الأصلي.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

بعد التنفيذ، ستجد `ImageWithTextLayer.psd` في المجلد المستهدف، الآن يحتوي على طبقة النص الجديدة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **`NullPointerException` on `im.addTextLayer`** | لم يتم تحميل PSD بشكل صحيح (مسار خاطئ). | تحقق من أن `sourceFileName` يشير إلى PSD موجود. |
| **Text not visible** | المستطيل موضوع خارج اللوحة أو الطبقة مخفية. | قم بضبط إحداثيات المستطيل أو تحقق من رؤية الطبقة باستخدام `layer.setVisible(true)`. |
| **LicenseException** | استخدام المكتبة بدون ترخيص صالح في بيئة الإنتاج. | احصل على ترخيص تجاري وقم بتعيينه عبر `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## الأسئلة المتكررة

**س: هل يمكنني إضافة طبقات نصية متعددة؟**  
ج: نعم – ببساطة كرر الخطوتين 4 و5 لكل قطعة نص تريد إدراجها.

**س: كيف أقوم بتنسيق النص (الخط، الحجم، اللون)؟**  
ج: تُظهر فئة `TextLayer` طريقة `getTextData()` حيث يمكنك تعديل `Font`، `FontSize`، `Color`، وغيرها من خصائص التنسيق. راجع وثائق Aspose.PSD API للحصول على التفاصيل الكاملة.

**س: ماذا لو كان PSD الخاص بي يحتوي بالفعل على العديد من الطبقات؟**  
ج: تعمل Aspose.PSD مع هياكل طبقات معقدة. يمكنك استهداف مجموعات محددة أو إدراج طبقة النص الجديدة في فهرس مرغوب باستخدام إصدارات `addTextLayer` المتعددة.

**س: هل هذه الطريقة مناسبة لتطبيقات الويب؟**  
ج: بالتأكيد. طالما أن الخادم الخاص بك يعمل بـ Java، يمكنك إنشاء أو تعديل ملفات PSD مباشرةً وتقديمها للعملاء.

**س: أين يمكنني الحصول على المساعدة إذا واجهت مشاكل؟**  
ج: قم بزيارة [Aspose support forums](https://forum.aspose.com/c/psd/34) حيث يمكن للمجتمع ومهندسي Aspose مساعدتك.

## الخلاصة
لقد رأيت الآن مدى سهولة **إضافة نص إلى PSD** في وقت التشغيل باستخدام Java و Aspose.PSD. تمكنك هذه التقنية من أتمتة إنشاء الرسومات، تخصيص الأصول، ودمج تحرير على مستوى Photoshop في أي حل مبني على Java. استكشف باقي واجهة Aspose.PSD API لإضافة أشكال، طبقات نقطية، أو حتى تطبيق فلاتر لمزيد من الأتمتة المتقدمة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-03-07  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose