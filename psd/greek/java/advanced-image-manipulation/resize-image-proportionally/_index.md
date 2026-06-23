---
date: 2026-06-23
description: Μάθετε πώς να μετατρέψετε το PSD σε PNG και να αλλάξετε το μέγεθος των
  εικόνων αναλογικά σε Java χρησιμοποιώντας το Aspose.PSD. Αυτό το step‑by‑step tutorial
  καλύπτει την προσωρινή αποθήκευση εικόνων, την αλλαγή μεγέθους και την αποθήκευση
  ως PNG.
keywords:
- convert psd to png
- save psd as png
- how to cache image
- resize image without distortion
- proportional image scaling
linktitle: Μετατροπή PSD σε PNG & Αναλογική αλλαγή μεγέθους
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  headline: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for
    Java
  type: TechArticle
- description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  name: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – Java 8 or later installed.'
    text: '**Java Development Kit (JDK)** – Java 8 or later installed.'
  - name: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
  - name: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
    text: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
  type: HowTo
- questions:
  - answer: Aspose.PSD supports PSD, PNG, JPEG, BMP, GIF, and many more. See the full
      list in the [documentation](https://reference.aspose.com/psd/java/). For the
      full API reference, see the guide **here**.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Purchase a commercial license on the [Aspose store](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Absolutely – request a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Are temporary licenses available for testing?
  - answer: The [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) is a great place
      to ask questions and share solutions.
    question: Where can I find community support?
  - answer: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).
    question: How do I access the full API reference?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Πώς να μετατρέψετε το PSD σε PNG και να αλλάξετε το μέγεθος αναλογικά με το
  Aspose.PSD για Java
url: /el/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Μετατρέψετε PSD σε PNG και να Αλλάξετε το Μέγεθος Αναλογικά με το Aspose.PSD για Java

## Εισαγωγή

Αν χρειάζεστε **convert PSD to PNG** ενώ διατηρείτε την αρχική αναλογία διαστάσεων, βρίσκεστε στο σωστό μέρος. Σε αυτό το **Aspose.PSD Java** tutorial θα περάσουμε από ένα πλήρες **java image processing tutorial** που δείχνει **how to resize image** αρχεία αναλογικά, αποθηκεύει την εικόνα στην κρυφή μνήμη για βέλτιστη απόδοση, και τέλος αποθηκεύει το αποτέλεσμα ως PNG. Στο τέλος θα μπορείτε να ενσωματώσετε αυτή τη ροή εργασίας σε οποιοδήποτε Java‑based image‑processing pipeline.

## Γρήγορες Απαντήσεις
- **Μπορεί το Aspose.PSD να μετατρέψει PSD σε PNG;** Yes – simply load the PSD and save it with `PngOptions`.
- **Υποστηρίζει η βιβλιοθήκη αναλογική αλλαγή μεγέθους;** Absolutely; use `resizeWidthProportionally` and `resizeHeightProportionally`.
- **Χρειάζεται να αποθηκεύσω την εικόνα στην κρυφή μνήμη πρώτα;** Caching (`image.cacheData()`) improves performance for large PSD files.
- **Ποια έκδοση Java απαιτείται;** Java 8 or newer is fully supported.
- **Απαιτείται άδεια για παραγωγή;** Yes, a commercial license removes evaluation watermarks.

## Τι είναι το “convert PSD to PNG” και γιατί είναι σημαντικό;

**convert PSD to PNG** σημαίνει τη μετατροπή ενός πολυεπίπεδου εγγράφου Photoshop σε ένα μονοεπίπεδο, lossless PNG αρχείο που διατηρεί τη διαφάνεια και την οπτική πιστότητα. Αυτή η μετατροπή σας επιτρέπει να μοιράζεστε σχέδια χωρίς να απαιτείται Photoshop, δημιουργεί web‑ready assets και μικρογραφίες, και αφαιρεί βαριά PSD αρχεία από τους browsers των πελατών ενώ διατηρεί την ποιότητα που απαιτείται για UI components και branding.

## Γιατί να αλλάζετε το μέγεθος της εικόνας αναλογικά σε Java;

Η αλλαγή μεγέθους μιας εικόνας **without distortion** διατηρεί την αρχική αναλογία πλάτους‑ύψους, ώστε τα γραφικά να διατηρούν την προοριζόμενη εμφάνιση σε οποιοδήποτε μέγεθος οθόνης. Οι μέθοδοι αναλογικής κλιμάκωσης του Aspose.PSD υπολογίζουν αυτόματα τη χαμένη διάσταση, εξαλείφοντας τους χειροκίνητους υπολογισμούς και τον κίνδυνο παραμορφωμένων ή συμπιεσμένων οπτικών στοιχείων.

## Γιατί αυτό είναι σημαντικό για τους προγραμματιστές

Για τους προγραμματιστές, η αναλογική αλλαγή μεγέθους και η μετατροπή PSD‑to‑PNG μειώνουν την κατανάλωση μνήμης και βελτιώνουν τους χρόνους φόρτωσης, εξασφαλίζοντας ότι οι εφαρμογές διαχειρίζονται μεγάλα γραφικά αποδοτικά. Με την πρώιμη κλιμάκωση των εικόνων, διατηρείτε τη σταθερότητα του UI rendering σε όλες τις συσκευές και εξαλείφετε την ανάγκη για Photoshop σε διακομιστές κατασκευής, κάτι που απλοποιεί την ανάπτυξη και μειώνει τα λειτουργικά κόστη.

- **Reduced PSD file size** – Με τη μείωση μεγέθους μεγάλων PSD πριν τη μετατροπή, μειώνετε τη χρήση μνήμης και επιταχύνετε την επεξεργασία downstream.  
- **Consistent UI rendering** – Η αναλογική αλλαγή μεγέθους εγγυάται ότι τα εικονίδια και τα γραφικά διατηρούν την οπτική τους ισορροπία σε όλες τις συσκευές.  
- **No Photoshop dependency** – Μπορείτε να εκτελείτε αυτές τις λειτουργίες σε διακομιστή ή CI pipeline χωρίς εγκατάσταση Photoshop.

## Προαπαιτούμενα

1. **Java Development Kit (JDK)** – Java 8 ή νεότερη έκδοση εγκατεστημένη.  
2. **Aspose.PSD for Java** – κατεβάστε το πιο πρόσφατο JAR από την επίσημη ιστοσελίδα [here](https://releases.aspose.com/psd/java/).  
3. Ένα δείγμα αρχείου PSD (`sample.psd`) τοποθετημένο σε έναν φάκελο που μπορείτε να αναφέρετε από το έργο σας.

## Εισαγωγή Πακέτων

Η κλάση `PsdImage` είναι το βασικό αντικείμενο του Aspose.PSD που αντιπροσωπεύει ένα αρχείο PSD στη μνήμη. Εισάγετε τα απαραίτητα namespaces για να εργαστείτε με φόρτωση, caching, αλλαγή μεγέθους και εξαγωγή PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Βήμα 1: Φόρτωση της Εικόνας PSD

**Direct answer:** Φορτώστε το αρχείο πηγής με `new PsdImage("sample.psd")`; στη συνέχεια καλέστε `image.cacheData()` για προφόρτωση των δεδομένων εικόνας, κάτι που αποτρέπει επαναλαμβανόμενες αναγνώσεις δίσκου σε μεταγενέστερες λειτουργίες.

`cacheData()` φορτώνει ολόκληρο το PSD στη μνήμη, επιτρέποντας ταχύτερη επόμενη επεξεργασία. Η μέθοδος `cacheData()` διαβάζει ολόκληρο το έγγραφο στη μνήμη, επιτρέποντας ταχύτερη επόμενη επεξεργασία για μεγάλα αρχεία. Πρώτα, φορτώστε το αρχικό αρχείο PSD. Αν το αρχείο είναι μεγάλο, η caching των δεδομένων εικόνας μειώνει την κατανάλωση μνήμης όταν εκτελείτε επόμενες λειτουργίες.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Βήμα 2: Αναλογική Αλλαγή Μεγέθους Εικόνας (Java)

**Direct answer:** Καλέστε `image.resizeWidthProportionally(targetWidth)` (ή `resizeHeightProportionally`) για να μειώσετε την εικόνα ενώ διατηρείται αυτόματα η αρχική αναλογία διαστάσεων.

`resizeWidthProportionally(int targetWidth)` κλιμακώνει το πλάτος της εικόνας και υπολογίζει αυτόματα το αντίστοιχο ύψος για να διατηρήσει την αρχική αναλογία διαστάσεων. Τώρα αποφασίστε τις νέες διαστάσεις. Σε αυτό το παράδειγμα μειώνουμε την εικόνα στο **half** του αρχικού μεγέθους διατηρώντας την αναλογία. Μπορείτε να προσαρμόσετε το target width ή height όπως χρειάζεται.

Η μέθοδος `resizeWidthProportionally` υπολογίζει το αντίστοιχο ύψος βάσει της αρχικής αναλογίας, έτσι η εικόνα αλλάζει μέγεθος **without distortion**. Χρησιμοποιήστε οποιαδήποτε μέθοδο—το Aspose.PSD διαχειρίζεται τη συμπληρωματική διάσταση για εσάς.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro tip:** Χρησιμοποιήστε είτε `resizeWidthProportionally` *or* `resizeHeightProportionally`—η βιβλιοθήκη υπολογίζει αυτόματα τη δεύτερη διάσταση για να διατηρήσει την εικόνα αναλογική.

## Βήμα 3: Αποθήκευση της Αλλαγμένης Εικόνας ως PNG

**Direct answer:** Δημιουργήστε μια παρουσία `PngOptions`, αναθέστε την στην εικόνα, και καλέστε `image.save("output.png", pngOptions)` για να γράψετε το αλλαγμένο αρχείο σε μορφή PNG.

`PngOptions` καθορίζει ρυθμίσεις για την εξαγωγή PNG όπως επίπεδο συμπίεσης και βάθος χρώματος. Τέλος, εξάγετε την αλλαγμένη εικόνα σε μορφή PNG. Αυτό το βήμα ολοκληρώνει τη ροή εργασίας **convert PSD to PNG**.

Όταν εκτελεστεί ο κώδικας, θα βρείτε ένα αρχείο PNG που είναι στο μισό του μεγέθους του αρχικού PSD, με την ίδια οπτική ποιότητα και χωρίς παραμόρφωση.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Όταν εκτελεστεί ο κώδικας, θα βρείτε ένα αρχείο PNG που είναι στο μισό του μεγέθους του αρχικού PSD, με την ίδια οπτική ποιότητα και χωρίς παραμόρφωση.

## Συνηθισμένα Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **OutOfMemoryError** | Μεγάλο PSD χωρίς caching | Καλέστε `image.cacheData()` πριν την αλλαγή μεγέθους |
| **Blank PNG output** | Λανθασμένη διαδρομή αρχείου | Επαληθεύστε το `dataDir` και τα δικαιώματα εγγραφής |
| **Aspect ratio looks off** | Χρήση τόσο του πλάτους όσο και του ύψους χειροκίνητα | Χρησιμοποιήστε τις αναλογικές μεθόδους που παρέχει το Aspose.PSD |

## Συμβουλές για Μείωση του Μεγέθους Αρχείου PSD

- **Crop unnecessary layers** before loading the file.  
- **Resize proportionally** as shown above to shrink dimensions early.  
- **Save as PNG with appropriate bit depth** to avoid excess data.

## Συχνές Ερωτήσεις

**Q: Είναι το Aspose.PSD συμβατό με όλες τις μορφές εικόνας;**  
A: Το Aspose.PSD υποστηρίζει PSD, PNG, JPEG, BMP, GIF, και πολλά άλλα. Δείτε τη πλήρη λίστα στην [documentation](https://reference.aspose.com/psd/java/). Για την πλήρη αναφορά API, δείτε τον οδηγό **here**.

**Q: Μπορώ να χρησιμοποιήσω το Aspose.PSD για εμπορικά έργα;**  
A: Ναι. Αγοράστε εμπορική άδεια στο [Aspose store](https://purchase.aspose.com/buy).

**Q: Υπάρχουν προσωρινές άδειες διαθέσιμες για δοκιμή;**  
A: Απόλυτα – ζητήστε μια προσωρινή άδεια [here](https://purchase.aspose.com/temporary-license/) για σκοπούς αξιολόγησης.

**Q: Πού μπορώ να βρω υποστήριξη κοινότητας;**  
A: Το [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) είναι ένας εξαιρετικός χώρος για ερωτήσεις και λύσεις.

**Q: Πώς μπορώ να έχω πρόσβαση στην πλήρη αναφορά API;**  
A: Λεπτομερή τεκμηρίωση API είναι διαθέσιμη [here](https://reference.aspose.com/psd/java/).

## Συμπέρασμα

Τώρα γνωρίζετε πώς να **convert PSD to PNG**, **resize image proportionally**, και να διαχειρίζεστε την caching αποδοτικά χρησιμοποιώντας το Aspose.PSD για Java. Ενσωματώστε αυτά τα βήματα στις δικές σας εφαρμογές για γρήγορη, υψηλής ποιότητας επεξεργασία εικόνας χωρίς εξάρτηση από εγκατεστημένο Photoshop. Αυτή η προσέγγιση **aspose psd java** είναι αξιόπιστο μέρος οποιουδήποτε **java image processing tutorial** και σας βοηθά να διατηρείτε τα μεγέθη αρχείων PSD υπό έλεγχο διατηρώντας την οπτική πιστότητα.

---

**Last Updated:** 2026-06-23  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Απλή Αλλαγή Μεγέθους με Aspose.PSD – Βιβλιοθήκη Java Image Manipulation](/psd/java/basic-image-operations/simple-resizing/)
- [Αλλαγή Μεγέθους Εικόνας Java - Χρήση της Εν enumeration Resize Type στο Aspose.PSD για Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Κλιμάκωση Εικόνας Υψηλής Ποιότητας με Bicubic Resampler στο Aspose.PSD για Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}