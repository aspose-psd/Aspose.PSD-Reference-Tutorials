---
date: 2025-12-25
description: تعلم درسًا في معالجة الصور بلغة جافا حول حفظ ملفات PSD كـ JPG باستخدام
  خيوط العمل. يوضح هذا الدليل كيفية حفظ الصور باستخدام الخيوط بكفاءة.
linktitle: Save Images using Worker Threads
second_title: Aspose.PSD Java API
title: دروس معالجة الصور في جافا – حفظ الصور باستخدام خيوط العامل
url: /ar/java/advanced-techniques/save-images-worker-threads/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل معالجة الصور بجافا – حفظ الصور باستخدام خيوط العامل

## المقدمة

مرحبًا بكم في هذا **دليل معالجة الصور بجافا** حيث سنوضح لكم كيفية حفظ ملفات PSD كـ JPG (أو صيغ أخرى) باستخدام **خيوط العامل** في Aspose.PSD for Java. يمكن لمعالجة الصور متعددة الخيوط أن تقلل بشكل كبير من وقت التنفيذ، خاصةً عندما تحتاج إلى تحويل دفعة كبيرة من الملفات. خلال الدقائق القليلة القادمة، ستتعلمون لماذا تعتبر الخيوط مهمة، وكيفية إعدادها بأمان، وستشاهدون مثالًا كاملاً وجاهزًا للتنفيذ.

## إجابات سريعة
- **ما الذي يغطيه هذا الدليل؟** حفظ الصور باستخدام خيوط العامل باستخدام Aspose.PSD for Java.  
- **لماذا نستخدم الخيوط؟** لمعالجة عدة صور بشكل متوازي وتحسين الإنتاجية.  
- **هل أحتاج إلى ترخيص؟** يلزم ترخيص مؤقت للإنتاج؛ النسخة التجريبية المجانية تكفي للاختبار.  
- **ما نسخة جافا المدعومة؟** Java 8 أو أعلى.  
- **هل يمكنني تحويل PSD إلى JPG؟** نعم – يوضح الدليل حفظًا بأي صيغة مدعومة.

## ما هو دليل معالجة الصور بجافا؟

يُعلمك *دليل معالجة الصور بجافا* كيفية تعديل، تحويل، وتصدير ملفات الصور برمجيًا باستخدام جافا. في هذا الدليل، يتركز التركيز على **حفظ الصور بكفاءة** عن طريق تفريغ أعمال الإدخال/الإخراج الثقيلة إلى خيوط الخلفية.

## لماذا نستخدم خيوط العامل لحفظ الصور؟

- **الأداء:** التنفيذ المتوازي يستخدم عدة نوى CPU، مما يقلل من إجمالي وقت المعالجة.  
- **الاستجابة:** يظل تطبيقك الرئيسي مستجيبًا أثناء حفظ الملفات الكبيرة.  
- **القابلية للتوسع:** يمكن توسيع النهج بسهولة للتعامل مع آلاف الملفات في مهمة دفعة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

- معرفة أساسية ببرمجة جافا.  
- مكتبة Aspose.PSD for Java مثبتة. يمكنك تنزيلها [هنا](https://releases.aspose.com/psd/java/).  
- بيئة تطوير مُعدة مع جافا (JDK 8 أو أحدث).  

## استيراد الحزم

في مشروع جافا الخاص بك، ابدأ باستيراد الحزم اللازمة للعمل مع Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ImageOptionsBase;
import com.aspose.psd.coreexceptions.OperationInterruptedException;
import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.multithreading.InterruptMonitor;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

### الخطوة 1: تهيئة `SaveImageWorker`

أنشئ فئة باسم `SaveImageWorker` وتهيئ المتغيرات المطلوبة. هذا العامل يضم جميع البيانات اللازمة لعملية حفظ واحدة.

```java
public class SaveImageWorker {
    // ... (Refer to provided code for variable declarations)
    
    public SaveImageWorker(String inputPath, String outputPath, ImageOptionsBase saveOptions, InterruptMonitor monitor) {
        // Constructor logic
    }
    
    // ... (Refer to provided code for additional methods)
}
```

### الخطوة 2: تعريف طريقة `ThreadProc`

نفّذ طريقة `ThreadProc` لتحويل صورة من صيغة إلى أخرى مع معالجة الانقطاعات بشكل سلس.

```java
public String ThreadProc() {
    Image image = Image.load(this.inputPath);

    InterruptMonitor.setThreadLocalInstance(this.monitor);

    try {
        image.save(this.outputPath, this.saveOptions);
    } catch (OperationInterruptedException e) {
        System.out.println("The save thread #" + Thread.currentThread().getId() + " finishes at " + getDateTime().toString());
        System.out.println(e);
    } catch (Exception e) {
        System.out.println(e);
    } finally {
        InterruptMonitor.setThreadLocalInstance(null);
    }

    return "Hello Aspose";
}
```

### الخطوة 3: استخدام `SaveImageWorker` في تطبيقك

في تطبيقك الرئيسي، أنشئ مثالًا من `SaveImageWorker` واستدعِ `ThreadProc` لتنفيذ عملية الحفظ على خيط خلفي.

```java
public class MainApplication {
    public static void main(String[] args) {
        // ... (Initialize inputPath, outputPath, saveOptions, and monitor)
        
        SaveImageWorker saveImageWorker = new SaveImageWorker(inputPath, outputPath, saveOptions, monitor);
        String result = saveImageWorker.ThreadProc();
        
        // ... (Handle the result as needed)
    }
}
```

## المشكلات الشائعة والحلول

| المشكلة | لماذا يحدث | كيفية الإصلاح |
|-------|----------------|------------|
| **توقف الخ `InterruptMonitor` لم يتم مسحه | تأكد من تشغيل `InterruptMonitor.setThreadLocalInstance(null)` داخل `finally`. |
| **صيغة غير مدعومة** | فئة فرعية خاطئة من `ImageOptionsBase` | استخدم `JpegOptions`، `PngOptions`، إلخ، لتطابق الإخراج المطلوب. |
| **نفاد الذاكرة** | تم تحميل PSD كبير على خيط الواجهة | قم بالتحميل والحفظ داخل خيط العامل؛ فكر في البث للملفات الضخمة. |

## الأسئلة المتكررة

### س1: هل Aspose.PSD for Java مناسب لمعالجة الصور متعددة الخيوط؟

نعم، يوفر Aspose.PSD for Java دعمًا مدمجًا للمعالجة متعددة الخيوط، مما يتيح لك تحسين الأداء في مهام معالجة الصور.

### س2: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.PSD for Java؟

يمكنك الرجوع إلى الوثائق [هنا](https://reference.aspose.com/psd/java/) للحصول على معلومات شاملة حول Aspose.PSD for Java.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD for Java؟

يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/) لاستكشاف جميع إمكانيات Aspose.PSD for Java.

### س4: ما هي خيارات الدعم المتاحة لـ Aspose.PSD for Java؟

لأي مساعدة أو استفسارات، زر [منتدى Aspose.PSD for Java](https://forum.aspose.com/c/psd/34) للتواصل مع المجتمع والخبراء.

### س5: أين يمكنني شراء Aspose.PSD for Java؟

لشراء Aspose.PSD for Java، زر [صفحة الشراء](https://purchase.aspose.com/buy).

### س6: هل يمكنني تحويل PSD إلى JPG باستخدام هذه الطريقة؟

بالطبع. استخدم `JpegOptions` كمعامل `saveOptions` عند استدعاء `image.save(...)`.

### س7: كم عدد الخيوط التي يجب إنشاؤها لتحقيق الأداء الأمثل؟

قاعدة جيدة هي مطابقة عدد الخيوط مع عدد نوى المعالج المتاحة (`Runtime.getRuntime().availableProcessors()`)، لكن يجب دائمًا اختبار ذلك مع حمل عملك.

## الخاتمة

لقد إتقنت الآن **دليل معالجة الصور بجافا** الذي يوضح كيفية **حفظ الصور باستخدام الخيوط** باستخدام Aspose.PSD for Java. من خلال تغليف منطق الحفظ في فئة عامل واستخدام `InterruptMonitor`، ستحصل على كل من السرعة والموثوقية. لا تتردد في توسيع هذا النمط لمعالجة المجلدات دفعةً، إضافة تقارير التقدم، أو دمجه في خط أنابيب معالجة صور أكبر.

---

**آخر تحديث:** 2025-12-25  
**تم الاختبار مع:** Aspose.PSD for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}