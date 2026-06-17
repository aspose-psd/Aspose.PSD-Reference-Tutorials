---
date: 2026-03-28
description: تعلم كيفية تعديل السطوع في ملفات PSD باستخدام Aspose.PSD للـ Java، بما
  في ذلك كيفية تغيير سطوع الطبقة وتباينها. مثالي للمطورين ومصممي الجرافيك.
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: ضبط السطوع PSD Java – إدارة السطوع والتباين
url: /ar/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط السطوع في PSD Java – إدارة السطوع والتباين

## مقدمة

هل أنت مصمم جرافيك أو مطور يعمل بشكل متكرر مع ملفات PSD (Photoshop Document)؟ هل تحتاج إلى **adjust brightness psd java** بسرعة وموثوقية دون مغادرة بيئة Java الخاصة بك؟ في هذا البرنامج التعليمي، سنوضح لك بالضبط كيفية تغيير سطوع وتباين طبقة PSD باستخدام مكتبة Aspose.PSD للغة Java. ستحصل على مقتطف كود قابل لإعادة الاستخدام يمكن دمجه في أي خط أنابيب لمعالجة الصور تلقائيًا. هيا نرفع أكمامنا ونبدأ!

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java  
- **هل يمكنني تغيير عدة طبقات في آن واحد؟** نعم – iterate through all `BrightnessContrastLayer` objects.  
- **ما إصدار Java المطلوب؟** JDK 8 or higher.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يتطلب الاستخدام غير التجريبي ترخيص تجاري.  
- **هل الكود متوافق مع مشاريع Maven/Gradle؟** بالتأكيد – just add the Aspose.PSD dependency.

## ما هو “adjust brightness psd java”؟

ضبط السطوع في ملف PSD عبر Java يعني تعديل قيم `BrightnessContrastLayer` برمجيًا، مما يتيح لك أتمتة التعديلات البصرية التي كانت تتطلب عملًا يدويًا في Photoshop.

## لماذا ضبط السطوع والتباين في طبقات PSD؟

- **تسريع المعالجة الدفعية** – مثالي لمكتبات التصميم الكبيرة.  
- **الحفاظ على بنية الطبقة** – يتم تعديل طبقات الضبط المستهدفة فقط، مع الحفاظ على الأقنعة والتأثيرات.  
- **التكامل مع خطوط أنابيب CI/CD** – إنشاء صور معاينة أو صور مصغرة تلقائيًا.

## المتطلبات المسبقة

قبل أن نبدأ هذه الرحلة المثيرة في تعديل ملفات PSD باستخدام Java، من الضروري التأكد من أن لديك كل ما تحتاجه مُعدًا بشكل صحيح. إليك ما ستحتاجه لإكمال هذا البرنامج التعليمي بنجاح:

1. **Java Development Kit (JDK)** – تأكد من أن لديك JDK 8 أو أعلى مثبتًا على جهازك. يمكنك تنزيله من [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. **Aspose.PSD for Java Library** – للعمل مع ملفات PSD، ستحتاج إلى مكتبة Aspose.PSD. يمكنك تنزيل أحدث نسخة من [release page](https://releases.aspose.com/psd/java/).

3. **IDE of Your Choice** – يُفضَّل استخدام بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse أو NetBeans لكتابة وتشغيل كود Java الخاص بك.

4. **Basic Knowledge of Java** – الإلمام ببرمجة Java سيساعدك على فهم مقتطفات الكود التي سنعمل عليها.

بمجرد أن تكون هذه المتطلبات جاهزة، نحن مستعدون للمضي قدمًا. الآن، افتح محرر الكود المفضل لديك ولنبدأ البرمجة!

## استيراد الحزم

الخطوة الأولى في رحلتنا البرمجية هي استيراد الحزم اللازمة. قبل أن تتمكن من استخدام الوظائف التي توفرها Aspose.PSD، يجب التأكد من أن المكتبة موجودة في مسار الفئة (classpath). إليك كيفية القيام بذلك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

من خلال إكمال هذه الخطوات، أنت تُعد المشهد للعمل مع ملفات PSD بفعالية!

الآن بعد أن تم إعداد كل شيء، حان الوقت للدخول في صلب البرنامج التعليمي: ضبط السطوع والتباين في طبقات PSD. سنقسم هذه العملية إلى خطوات واضحة لضمان قدرتك على المتابعة بسهولة.

## الخطوة 1: تعريف دليل المستند الخاص بك

ابدأ بتعريف الدليل الذي توجد فيه ملفات PSD الخاصة بك. تساعدك هذه الخطوة على تنظيم ملفاتك بكفاءة.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار الفعلي إلى دليل ملفات PSD الخاص بك.

## الخطوة 2: تحديد أسماء ملفات المصدر والوجهة

بعد ذلك، تحتاج إلى تحديد اسم ملف المصدر لملف PSD وملف الوجهة حيث سيتم حفظ ملف PSD المعدل.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

في هذا المثال، نفترض أن لديك ملف PSD باسم `BrightnessContrastModern.psd` في الدليل الخاص بك.

## الخطوة 3: تحميل ملف PSD

حان الوقت الآن لتحميل ملف PSD إلى تطبيقك حتى تتمكن من التلاعب به.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

هذا السطر من الكود ينشئ نسخة من `PsdImage` تمثل ملف PSD الخاص بك. الآن يمكنك الوصول إلى جميع طبقات PSD.

## الخطوة 4: التكرار عبر الطبقات

الخطوة التالية تتضمن التكرار عبر كل طبقة من ملف PSD للعثور على إعدادات السطوع والتباين وتعديلها.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

حلقة `for` تمر عبر كل طبقة من PSD. نحن نتحقق مما إذا كانت الطبقة نسخة من `BrightnessContrastLayer`. هذا ضروري لضمان أنك تحاول تعديل سطوع طبقة PSD فقط على الطبقات الصحيحة.

## الخطوة 5: ضبط السطوع والتباين

داخل الحلقة، يمكنك الآن ضبط السطوع والتباين لكل `BrightnessContrastLayer`.

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

في هذا المثال، قمنا بتعيين السطوع والتباين إلى `50`. يمكنك تعديل هذه القيم وفقًا لمتطلباتك. الرقم الأعلى يزيد السطوع/التباين، بينما الرقم الأقل يقلل منهما.

## الخطوة 6: حفظ التغييرات

الخطوة الأخيرة هي حفظ التغييرات التي أجريتها على ملف PSD. ستحتاج إلى كتابة الصورة المعدلة مرة أخرى إلى الوجهة المحددة.

```java
im.save(psdPathAfterChange);
```

هذا السطر من الكود يحفظ ملف PSD المعدل بإعدادات السطوع والتباين الجديدة.

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثها | الحل |
|-------|----------------|-----|
| **No `BrightnessContrastLayer` found** | قد يستخدم ملف PSD نوع تعديل مختلف (مثل Levels). | تحقق من نوع الطبقة أو حوّل التعديل إلى `BrightnessContrastLayer`. |
| **Saved file looks corrupted** | الترخيص مفقود أو يتم استخدام نسخة قديمة من Aspose.PSD. | قم بتطبيق ترخيص صالح وتأكد من أنك تستخدم أحدث إصدار من المكتبة. |
| **Values out of range** | يجب أن تكون قيم السطوع/التباين بين -100 و 100. | قيد القيم قبل استدعاء `setBrightness`/`setContrast`. |

## الأسئلة المتكررة

**س: ما هو Aspose.PSD للغة Java؟**  
ج: Aspose.PSD للغة Java هي مكتبة تسمح للمطورين بالتعامل مع ملفات PSD برمجيًا، مما يتيح أتمتة المهام المتعلقة بـ Photoshop.

**س: هل يمكنني ضبط سطوع وتباين عدة طبقات في آن واحد؟**  
ج: نعم، النهج المستخدم في هذا البرنامج التعليمي يتكرر عبر جميع طبقات PSD، مما يتيح لك ضبط عدة نسخ من `BrightnessContrastLayer`.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: يمكنك الحصول على ترخيص مؤقت بزيارة [temporary license page](https://purchase.aspose.com/temporary-license/).

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.PSD من [release page](https://releases.aspose.com/).

**س: أين يمكنني العثور على دعم إضافي لـ Aspose.PSD؟**  
ج: يمكنك الحصول على الدعم لـ Aspose.PSD عبر [support forum](https://forum.aspose.com/c/psd/34).

---

**آخر تحديث:** 2026-03-28  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}