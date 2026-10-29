---
date: 2026-10-29
description: Μάθετε πώς να αποθηκεύετε PSD με γραμματοσειρές και να εξαναγκάσετε την
  προσωρινή μνήμη γραμματοσειρών χρησιμοποιώντας το Aspose.PSD για Java, βελτιώνοντας
  την απόδοση των εικόνων και διαχειριζόμενοι αποτελεσματικά τις ελλιπείς γραμματοσειρές.
keywords:
- save psd with fonts
- java thread sleep
- update font cache
- refresh system fonts
- improve image performance
lastmod: 2026-10-29
linktitle: Εξαναγκασμός προσωρινής μνήμης γραμματοσειρών
og_description: Αποθήκευση PSD με γραμματοσειρές και εξαναγκασμός της προσωρινής μνήμης
  γραμματοσειρών σε Java. Μάθετε πώς το Aspose.PSD βελτιώνει την απόδοση των εικόνων,
  διαχειρίζεται τις ελλιπείς γραμματοσειρές και ενημερώνει γρήγορα τις γραμματοσειρές
  του συστήματος.
og_image_alt: Screenshot of Aspose.PSD Java code forcing font cache and saving PSD
  with fonts
og_title: Αποθήκευση PSD με γραμματοσειρές και εξαναγκασμός της προσωρινής μνήμης
  γραμματοσειρών χρησιμοποιώντας το Aspose.PSD για Java
schemas:
- author: Aspose
  dateModified: '2026-10-29'
  description: Learn how to save PSD with fonts and force the font cache using Aspose.PSD
    for Java, improving image performance and handling missing fonts efficiently.
  headline: Save PSD with fonts and force font cache – Aspose.PSD Java
  type: TechArticle
- description: Learn how to save PSD with fonts and force the font cache using Aspose.PSD
    for Java, improving image performance and handling missing fonts efficiently.
  name: Save PSD with fonts and force font cache – Aspose.PSD Java
  steps:
  - name: Load the PSD image (how to load PSD image)
    text: '**Direct answer:** Load the original PSD with `Image.load("sample.psd")`
      to obtain an in‑memory representation that you can manipulate or inspect before
      any font updates. This initial load serves as a baseline for comparing the effect
      of the cache refresh. `Image.load` loads a PSD file into an Aspos'
  - name: Wait for font installation (java thread sleep – improve image performance)
    text: '**Direct answer:** Pause the execution for two minutes using `Thread.sleep(120_000)`
      so you can manually install the required font, then call `OpenTypeFontsCache.updateCache()`
      to force Aspose.PSD to refresh its internal font list before loading the PSD
      again. `Thread.sleep` pauses the current threa'
  - name: Load the updated PSD image and **save PSD with fonts**
    text: '`image.save` writes the current `Image` object to a file in the specified
      format. **Direct answer:** Reload the original PSD after the cache refresh;
      the newly installed font will now be recognized, and calling `image.save("HasFont.psd")`
      will embed the correct typefaces, confirming the cache update'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java supports JDK 8 and newer, covering the majority of
      modern Java applications.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Yes. A commercial license is required for production use. You can obtain
      one from the [purchase page](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Absolutely! Download a trial version from the [releases page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Join the discussion on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      for tips and troubleshooting.
    question: Where can I find community support?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a short‑term license.
    question: How can I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd
- aspose.psd
- java image processing
- font cache
title: Αποθήκευση PSD με γραμματοσειρές και εξαναγκασμός της προσωρινής μνήμης γραμματοσειρών
  – Aspose.PSD Java
url: /el/java/advanced-image-manipulation/force-font-cache/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση PSD με γραμματοσειρές και εξαναγκασμός προσωρινής μνήμης γραμματοσειρών – Aspose.PSD Java

## Εισαγωγή

Αν χρειάζεστε να **αποθηκεύσετε PSD με γραμματοσειρές** γρήγορα, εξασφαλίζοντας ταυτόχρονα ότι οι σωστές γραμματοσειρές είναι διαθέσιμες, βρίσκεστε στο σωστό μέρος. Η προσωρινή μνήμη γραμματοσειρών μπορεί να βελτιώσει δραστικά **την απόδοση της εικόνας**, ειδικά όταν επεξεργάζεστε επανειλημμένα μεγάλα έγγραφα Photoshop. Σε αυτό το μάθημα θα περάσουμε βήμα-βήμα τις ακριβείς ενέργειες για να εξαναγκάσετε την προσωρινή μνήμη γραμματοσειρών, **να φορτώσετε αρχεία PSD image**, και τελικά **να αποθηκεύσετε PSD με γραμματοσειρές** χρησιμοποιώντας το Aspose.PSD for Java.

## Γρήγορες απαντήσεις
- **Τι κάνει η εξαναγκασμένη προσωρινή μνήμη γραμματοσειρών;** Εξαναγκάζει το Aspose.PSD να ξανασκανάρει τις γραμματοσειρές του συστήματος ώστε οι νεοεγκατεστημένες γραμματοσειρές να αναγνωρίζονται άμεσα.  
- **Πόσο χρόνο πρέπει να περιμένω για την εγκατάσταση μιας γραμματοσειράς;** Ο κώδικας δείγματος κάνει παύση για **2 λεπτά**, που συνήθως είναι αρκετά για χειροκίνητη εγκατάσταση.  
- **Μπορώ να το χρησιμοποιήσω με οποιοδήποτε αρχείο PSD;** Ναι – εφόσον το αρχείο είναι προσβάσιμο και οι απαιτούμενες γραμματοσειρές είναι εγκατεστημένες στο σύστημα.  
- **Χρειάζομαι άδεια για την εκτέλεση αυτού του κώδικα;** Απαιτείται προσωρινή ή πλήρης άδεια για χρήση σε παραγωγή· μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση.  
- **Ποιες εκδόσεις Java υποστηρίζονται;** Το Aspose.PSD for Java λειτουργεί με JDK 8 και νεότερες.

## Τι είναι η «αποθήκευση PSD με γραμματοσειρές» και γιατί είναι σημαντική;

Η αποθήκευση ενός αρχείου PSD μετά την επεξεργασία των επιπέδων, του κειμένου ή των γραμματοσειρών είναι το τελικό βήμα που διατηρεί τις αλλαγές σας. Όταν η προσωρινή μνήμη γραμματοσειρών δεν είναι ενημερωμένη, το αποθηκευμένο αρχείο μπορεί να επιστρέψει σε προεπιλεγμένες γραμματοσειρές, προκαλώντας οπτικές ασυνέπειες. Εξαναγκάζοντας πρώτα τη μνήμη, εξασφαλίζετε ότι η λειτουργία **αποθήκευσης PSD με γραμματοσειρές** ενσωματώνει τις σωστές γραμματοσειρές.

## Γιατί να εξαναγκάσετε την προσωρινή μνήμη γραμματοσειρών με το Aspose.PSD;

Η εξαναγκασμένη προσωρινή μνήμη γραμματοσειρών σας προσφέρει τρία σαφή πλεονεκτήματα:

* **Performance boost** – Για αρχεία PSD μεγαλύτερα από 200 MB, η εξαναγκασμένη μνήμη μπορεί να μειώσει το χρόνο φόρτωσης έως και 30 %.  
* **Reliability** – Εγγυάται ότι τα αποθηκευμένα αρχεία PSD αποδίδουν ακριβώς όπως προορίζεται σε οποιονδήποτε υπολογιστή, εξαλείφοντας τα σφάλματα εναλλακτικών γραμματοσειρών.  
* **Simplicity** – Μία μόνο κλήση στο `OpenTypeFontsCache.updateCache()` διαχειρίζεται τη βαριά δουλειά χωρίς προσαρμοσμένα σενάρια λειτουργικού συστήματος.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

* Εγκατεστημένο Java Development Kit (JDK) 8 ή νεότερο.  
* Βιβλιοθήκη Aspose.PSD for Java (κατεβάστε από τον επίσημο [download link](https://releases.aspose.com/psd/java/)).  
* Ένα δείγμα αρχείου PSD (`sample.psd`) τοποθετημένο σε φάκελο που μπορείτε να αναφέρετε από τον κώδικά σας.  

Τώρα που όλα είναι έτοιμα, ας βουτήξουμε στην υλοποίηση.

## Εισαγωγή πακέτων

Πρώτα, εισάγετε τις κλάσεις που απαιτούνται για εργασία με εικόνες PSD και την προσωρινή μνήμη γραμματοσειρών. Τοποθετήστε αυτές τις δηλώσεις στην αρχή της κλάσης Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.OpenTypeFontsCache;

import com.aspose.psd.fileformats.psd.PsdImage;
import java.io.Console;
import java.util.concurrent.TimeUnit;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση της εικόνας PSD (πώς να φορτώσετε εικόνα PSD)

**Direct answer:** Φορτώστε το αρχικό PSD με `Image.load("sample.psd")` για να αποκτήσετε μια αναπαράσταση στη μνήμη που μπορείτε να επεξεργαστείτε ή να ελέγξετε πριν από τυχόν ενημερώσεις γραμματοσειρών. Αυτή η αρχική φόρτωση λειτουργεί ως βάση σύγκρισης για το αποτέλεσμα της ανανέωσης της μνήμης.

`Image.load` φορτώνει ένα αρχείο PSD σε ένα αντικείμενο `Image` του Aspose.PSD για επεξεργασία.

*Επεξήγηση:*  
- `Image.load` διαβάζει το αρχείο στη μνήμη.  
- `image.save` δημιουργεί ένα αντίγραφο με όνομα **NoFont.psd** που αντικατοπτρίζει την κατάσταση **πριν** να είναι διαθέσιμες νέες γραμματοσειρές.  
- Αυτό το βήμα είναι χρήσιμο για σύγκριση και διασφαλίζει ότι η επακόλουθη ενημέρωση της μνήμης αλλάζει πραγματικά το αποτέλεσμα.

### Βήμα 2: Αναμονή για εγκατάσταση γραμματοσειράς (java thread sleep – βελτίωση απόδοσης εικόνας)

**Direct answer:** Παύστε την εκτέλεση για δύο λεπτά χρησιμοποιώντας `Thread.sleep(120_000)` ώστε να μπορείτε να εγκαταστήσετε χειροκίνητα τη απαιτούμενη γραμματοσειρά, στη συνέχεια καλέστε `OpenTypeFontsCache.updateCache()` για να εξαναγκάσετε το Aspose.PSD να ανανεώσει τη λίστα εσωτερικών γραμματοσειρών του πριν φορτώσετε ξανά το PSD.

`Thread.sleep` παύει το τρέχον νήμα για καθορισμένη διάρκεια, επιτρέποντας χρόνο για εξωτερικές ενέργειες όπως η εγκατάσταση γραμματοσειρών.  

`OpenTypeFontsCache` είναι η βοηθητική κλάση του Aspose.PSD που ανανεώνει την προσωρινή μνήμη γραμματοσειρών OpenType του συστήματος.  

*Επεξήγηση:*  
- `Thread.sleep` (μια **java thread sleep**) παύει την εκτέλεση για **2 λεπτά** (2 × 60 × 1000 ms).  
- `OpenTypeFontsCache.updateCache()` εξαναγκάζει το Aspose.PSD να ξανασκανάρει τις OpenType γραμματοσειρές του συστήματος, καθιστώντας τις νεοεγκατεστημένες γραμματοσειρές άμεσα διαθέσιμες για απόδοση.  
- Αυτή η παύση βοηθά στη **βελτίωση της απόδοσης της εικόνας** διασφαλίζοντας ότι η μνήμη αντικατοπτρίζει τις πιο πρόσφατες γραμματοσειρές πριν από την επόμενη φόρτωση.

### Βήμα 3: Φόρτωση της ενημερωμένης εικόνας PSD και **αποθήκευση PSD με γραμματοσειρές**

`image.save` γράφει το τρέχον αντικείμενο `Image` σε ένα αρχείο στην καθορισμένη μορφή.

**Direct answer:** Φορτώστε ξανά το αρχικό PSD μετά την ανανέωση της μνήμης· η νεοεγκατεστημένη γραμματοσειρά θα αναγνωριστεί τώρα, και η κλήση `image.save("HasFont.psd")` θα ενσωματώσει τις σωστές γραμματοσειρές, επιβεβαιώνοντας ότι η ενημέρωση της μνήμης πέτυχε.

Η δεύτερη φόρτωση εντοπίζει τη νεοεγκατεστημένη γραμματοσειρά.  

*Επεξήγηση:*  
- Η δεύτερη φόρτωση εντοπίζει τη νεοεγκατεστημένη γραμματοσειρά.  
- Η αποθήκευση σε **HasFont.psd** παράγει ένα αρχείο που τώρα περιέχει τη σωστή απόδοση γραμματοσειράς, επιβεβαιώνοντας ότι η ενημέρωση της μνήμης λειτούργησε.

## Κοινά προβλήματα και λύσεις

| Πρόβλημα | Αιτία | Λύση |
|----------|-------|------|
| Το αποθηκευμένο PSD εξακολουθεί να εμφανίζει προεπιλεγμένη γραμματοσειρά | Η γραμματοσειρά δεν είναι εγκατεστημένη σε θέση που σαρώνεται από το λειτουργικό σύστημα | Εγκαταστήστε τη γραμματοσειρά στον φάκελο γραμματοσειρών του συστήματος (π.χ., `C:\Windows\Fonts` στα Windows) και εκτελέστε ξανά το `updateCache()`. |
| `Thread.sleep` προκαλεί `InterruptedException` | Η υπογραφή της μεθόδου δεν διαχειρίζεται ελεγχόμενες εξαιρέσεις | Προσθέστε `throws InterruptedException` στη μέθοδο `main` ή τυλίξτε την κλήση σε μπλοκ try‑catch. |
| `OpenTypeFontsCache.updateCache()` δεν κάνει τίποτα | Εκτέλεση σε headless server χωρίς διαμόρφωση γραμματοσειρών | Βεβαιωθείτε ότι ο διακομιστής έχει εγκατεστημένες τις απαιτούμενες γραμματοσειρές και ότι η διαδικασία Java έχει δικαίωμα ανάγνωσής τους. |
| **handle missing fonts** – Το PSD αποδίδει με εναλλακτική γραμματοσειρά | Τα αρχεία γραμματοσειρών είναι κατεστραμμένα ή μη προσβάσιμα | Επαληθεύστε την ακεραιότητα των αρχείων γραμματοσειρών και βεβαιωθείτε ότι η διαδικασία Java έχει πρόσβαση ανάγνωσης. |

## Συχνές ερωτήσεις

**Q: Είναι το Aspose.PSD συμβατό με όλες τις εκδόσεις Java;**  
A: Το Aspose.PSD for Java υποστηρίζει JDK 8 και νεότερες, καλύπτοντας την πλειονότητα των σύγχρονων εφαρμογών Java.

**Q: Μπορώ να χρησιμοποιήσω το Aspose.PSD για εμπορικά έργα;**  
A: Ναι. Απαιτείται εμπορική άδεια για χρήση σε παραγωγή. Μπορείτε να αποκτήσετε μία από τη [σελίδα αγοράς](https://purchase.aspose.com/buy).

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
A: Απολύτως! Κατεβάστε μια δοκιμαστική έκδοση από τη [σελίδα releases](https://releases.aspose.com/).

**Q: Πού μπορώ να βρω υποστήριξη από την κοινότητα;**  
A: Συμμετέχετε στη συζήτηση στο [φόρουμ Aspose.PSD](https://forum.aspose.com/c/psd/34) για συμβουλές και αντιμετώπιση προβλημάτων.

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για δοκιμές;**  
A: Επισκεφθείτε τη [σελίδα προσωρινής άδειας](https://purchase.aspose.com/temporary-license/) για να ζητήσετε μια βραχυπρόθεσμη άδεια.

## Συμπέρασμα

Τώρα έχετε μάθει πώς να **αποθηκεύετε PSD με γραμματοσειρές** μετά την εξαναγκασμένη προσωρινή μνήμη γραμματοσειρών, διασφαλίζοντας ότι τα αρχεία PSD σας αποδίδουν τις σωστές γραμματοσειρές κάθε φορά. Αυτή η τεχνική είναι ένα απλό αλλά ισχυρό μέρος της **βελτιστοποίησης επεξεργασίας εικόνας** και μπορεί να ενσωματωθεί σε μεγαλύτερες ροές εργασίας που απαιτούν αξιόπιστη, υψηλής απόδοσης επεξεργασία PSD.

---

**Last Updated:** 2026-10-29  
**Tested with:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  



```java
String dataDir = "Your Document Directory";

PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
image.save(dataDir + "NoFont.psd");
```

```java
System.out.println("You have 2 minutes to install the font");
Thread.sleep(2 * 60 * 1000);
OpenTypeFontsCache.updateCache();
```

```java
PsdImage image1 = (PsdImage)Image.load(dataDir + "sample.psd");
image1.save(dataDir + "HasFont.psd");
```

## Σχετικά μαθήματα

- [Αντικατάσταση Ελλειπουσών Γραμματοσειρών σε Αρχεία PSD με τη χρήση Aspose.PSD for Java](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Πώς να Αποθηκεύσετε PSD ως PNG και να Αντικαταστήσετε Ελλειπούσες Γραμματοσειρές σε Java με το Aspose](/psd/java/advanced-image-manipulation/replace-fonts/)
- [Δημιουργία Εικόνας PSD με Aspose.PSD for Java – Έλεγχος Επανακατανομής Μνήμης](/psd/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}