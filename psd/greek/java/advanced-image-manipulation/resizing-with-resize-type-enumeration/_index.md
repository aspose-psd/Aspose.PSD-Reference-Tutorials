---
date: 2026-06-03
description: Μάθετε πώς να αλλάζετε το μέγεθος εικόνας με το Aspose.PSD for Java.
  Αυτός ο οδηγός βήμα‑βήμα καλύπτει το Resize Type Enumeration, την υψηλής ποιότητας
  αλλαγή μεγέθους εικόνας και πώς να μετατρέψετε PSD σε JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Αλλαγή μεγέθους με το Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Πώς να αλλάξετε το μέγεθος εικόνας Java χρησιμοποιώντας το Resize Type Enumeration
url: /el/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Αλλάξετε το Μέγεθος Εικόνας σε Java Χρησιμοποιώντας την Απαρίθμηση Τύπου Resize

## Εισαγωγή

Αν ψάχνετε για **πώς να αλλάξετε το μέγεθος εικόνας** αρχεία αποδοτικά σε ένα έργο Java, το Aspose.PSD for Java παρέχει ένα καθαρό, υψηλής απόδοσης API. Σε αυτό το tutorial θα περάσουμε από τη φόρτωση ενός PSD, την εφαρμογή της **Resize Type Enumeration** για αλλαγή μεγέθους εικόνας υψηλής ποιότητας, και τελικά **μετατρέψτε PSD σε JPEG**. Είτε δημιουργείτε έναν επεξεργαστή επιφάνειας εργασίας είτε μια αυτοματοποιημένη διαδρομή διακομιστή, αυτά τα βήματα σας επιτρέπουν να ελέγχετε τις διαστάσεις, την ποιότητα και τη μορφή με λίγες μόνο γραμμές κώδικα.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται την αλλαγή μεγέθους εικόνας σε Java;** Aspose.PSD for Java.
- **Ποιος τύπος resize παρέχει την καλύτερη ποιότητα;** `ResizeType.LanczosResample`.
- **Μπορώ να μετατρέψω PSD σε JPEG μετά την αλλαγή μεγέθους;** Ναι – απλώς αποθηκεύστε με `JpegOptions`.
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται έγκυρη άδεια Aspose.PSD για χρήση σε παραγωγή.
- **Είναι αυτή η προσέγγιση κατάλληλη για μεγάλες παρτίδες;** Απόλυτα· το API επεξεργάζεται αρχεία εκατοντάδων σελίδων χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη.

## Τι είναι το "πώς να αλλάξετε το μέγεθος εικόνας" σε Java;

**Πώς να αλλάξετε το μέγεθος εικόνας** αναφέρεται στην προγραμματιστική αλλαγή των διαστάσεων εικονοστοιχείων μιας εικόνας διατηρώντας την οπτική πιστότητα. Η μέθοδος `Resize` του Aspose.PSD σε συνδυασμό με την απαρίθμηση `ResizeType` παρέχει ακριβή έλεγχο των αλγορίθμων κλιμάκωσης, επιτρέποντας στους προγραμματιστές να διατηρούν την ποιότητα σε ένα ευρύ φάσμα αρχείων προέλευσης και στόχων.

## Γιατί να χρησιμοποιήσετε την Απαρίθμηση Τύπου Resize;

`ResizeType` σας επιτρέπει να επιλέξετε τον αλγόριθμο επαναδειγματοληψίας που εξισορροπεί καλύτερα την ταχύτητα και την οπτική ποιότητα. Για τις περισσότερες περιπτώσεις, **LanczosResample** παρέχει καθαρά αποτελέσματα με μέτριο κόστος απόδοσης, επεξεργαζόμενος μια εικόνα 2000 × 1500 σε λιγότερο από 120 ms σε τυπική CPU εξυπηρετητή, διατηρώντας τις λεπτομέρειες των άκρων.

## Προαπαιτούμενα

1. **Περιβάλλον Ανάπτυξης Java** – JDK 8 ή νεότερο εγκατεστημένο και ρυθμισμένο.  
2. **Βιβλιοθήκη Aspose.PSD** – Κατεβάστε το πιο πρόσφατο JAR από την [website](https://releases.aspose.com/psd/java/).  
3. **Δείγμα αρχείου PSD** – Χρησιμοποιήστε το αρχείο [sample.psd](Your Document Directory/sample.psd) που περιλαμβάνεται στο SDK για πρακτική δοκιμή.

## Εισαγωγή Πακέτων

`Image` είναι η βασική κλάση για όλους τους τύπους εικόνας στο Aspose.PSD. Προσθέστε τις απαιτούμενες εισαγωγές στο αρχείο πηγαίου κώδικα Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Βήμα 1: Φόρτωση της Εικόνας

### Anchor Ορισμού
Η κλάση `RasterImage` είναι το κεντρικό αντικείμενο του Aspose.PSD που αντιπροσωπεύει μια raster‑βάση εικόνα που φορτώνεται από αρχείο PSD.

Φορτώστε το PSD σας σε μια παρουσία `RasterImage` ώστε να μπορείτε να χειριστείτε τα εικονοστοιχεία του:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Βήμα 2: Αλλαγή Μεγέθους της Εικόνας

`image.resize(width, height, resizeType)` αλλάζει το μέγεθος της εικόνας στις καθορισμένες διαστάσεις χρησιμοποιώντας τον επιλεγμένο αλγόριθμο.

Τώρα αλλάξτε το μέγεθος της φορτωμένης εικόνας χρησιμοποιώντας την **Resize Type Enumeration**. Σε αυτό το παράδειγμα χρησιμοποιούμε τη μέθοδο Lanczos Resample, η οποία είναι ιδανική όταν **πώς να αλλάξετε το μέγεθος εικόνας** με υψηλή ποιότητα:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Βήμα 3: Αποθήκευση της Αλλαγμένης Εικόνας

`image.save(path, options)` γράφει την εικόνα στο δίσκο στη μορφή που ορίζεται από τις παρεχόμενες επιλογές.

Μετά την αλλαγή μεγέθους, αποθηκεύστε την εικόνα με τις καθορισμένες διαστάσεις και τον επιλεγμένο τύπο αλλαγής μεγέθους. Εδώ, επίσης, δείχνουμε **μετατροπή psd σε jpeg** αποθηκεύοντας το αποτέλεσμα ως αρχείο JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Γιατί να χρησιμοποιήσετε την Απαρίθμηση Τύπου Resize;

`ResizeType` σας παρέχει λεπτομερή έλεγχο του αλγορίθμου επαναδειγματοληψίας, επιτρέποντάς σας να εξισορροπήσετε την ταχύτητα και την ποιότητα. Για τις περισσότερες εφαρμογές, το `LanczosResample` προσφέρει εξαιρετική ισορροπία, παρέχοντας καθαρά αποτελέσματα χωρίς μεγάλο κόστος απόδοσης, και λειτουργεί καλά με ποικίλο περιεχόμενο εικόνας.

## Συχνά Προβλήματα και Λύσεις

- **Η εικόνα φαίνεται θολή μετά την αλλαγή μεγέθους** – Δοκιμάστε διαφορετικό `ResizeType` όπως `Bicubic` ή `NearestNeighbour` για να δείτε ποιο προσφέρει το καλύτερο οπτικό αποτέλεσμα για τη συγκεκριμένη εικόνα σας.  
- **OutOfMemoryError σε μεγάλα αρχεία PSD** – Επεξεργαστείτε την εικόνα σε μικρότερα τμήματα ή αυξήστε το μέγεθος της μνήμης heap της JVM (`-Xmx` flag). Το Aspose.PSD μπορεί να διαχειριστεί αρχεία έως **2 GB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη.

## Συχνές Ερωτήσεις

### Q1: Είναι το Aspose.PSD for Java κατάλληλο τόσο για μικρά όσο και για μεγάλης κλίμακας έργα;
A1: Απόλυτα! Το Aspose.PSD for Java έχει σχεδιαστεί για να εξυπηρετεί έργα όλων των μεγεθών, παρέχοντας κλιμακωσιμότητα και αποδοτικότητα.

### Q2: Μπορώ να χρησιμοποιήσω διαφορετικό τύπο αλλαγής μεγέθους εκτός από το Lanczos Resample;
A2: Ναι, το Aspose.PSD for Java προσφέρει διάφορους τύπους αλλαγής μεγέθους, όπως **NearestNeighbour**, **Bicubic**, κ.ά. Ανατρέξτε στην τεκμηρίωση API για την πλήρη λίστα.

### Q3: Πού μπορώ να βρω πρόσθετη υποστήριξη για το Aspose.PSD for Java;
A3: Για οποιεσδήποτε ερωτήσεις ή βοήθεια, επισκεφθείτε το [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q4: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.PSD for Java;
A4: Ναι, μπορείτε να αποκτήσετε δωρεάν έκδοση δοκιμής [εδώ](https://releases.aspose.com/).

### Q5: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.PSD for Java;
A5: Για να αποκτήσετε προσωρινή άδεια, επισκεφθείτε [this link](https://purchase.aspose.com/temporary-license/).

## Συχνές Ερωτήσεις

**Ε: Πώς μπορώ να μετατρέψω προγραμματιστικά ένα αρχείο PSD σε JPEG χωρίς αλλαγή μεγέθους;**  
Α: Φορτώστε το PSD με `Image.load`, στη συνέχεια καλέστε `image.save("output.jpg", new JpegOptions());`.

**Ε: Είναι δυνατόν να διατηρήσω το αρχικό DPI κατά την αλλαγή μεγέθους;**  
Α: Ναι, μπορείτε να ορίσετε την ιδιότητα `Resolution` στο αντικείμενο `Image` πριν την αποθήκευση.

**Ε: Μπορώ να αλυσίδω πολλαπλές λειτουργίες αλλαγής μεγέθους;**  
Α: Αν και μπορείτε να καλέσετε `resize` πολλές φορές, είναι πιο αποδοτικό να υπολογίσετε τις τελικές διαστάσεις και να αλλάξετε το μέγεθος μία φορά.

---

**Τελευταία Ενημέρωση:** 2026-06-03  
**Δοκιμή με:** Aspose.PSD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Απλή Αλλαγή Μεγέθους με Aspose.PSD – Βιβλιοθήκη Επεξεργασίας Εικόνας Java](/psd/java/basic-image-operations/simple-resizing/)
- [Κλιμάκωση Εικόνας Υψηλής Ποιότητας με Bicubic Resampler στο Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Πώς να Μετατρέψετε PSD σε PNG και να Αλλάξετε το Μέγεθος Αναλογικά με Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}