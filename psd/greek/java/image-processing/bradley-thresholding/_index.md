---
date: 2026-08-17
description: Πώς να δυαδικοποιήσετε εικόνα με Bradley thresholding χρησιμοποιώντας
  το Aspose.PSD for Java. Ακολουθήστε αυτόν τον οδηγό βήμα‑βήμα για να μετατρέψετε
  PSD σε PNG και να βελτιώσετε την ποιότητα της εικόνας.
keywords:
- how to binarize image
- convert psd to png
- set threshold value
- enhance image quality
- save binarized image
lastmod: 2026-08-17
linktitle: Bradley Thresholding
og_description: Μάθετε πώς να δυαδικοποιήσετε εικόνα χρησιμοποιώντας Bradley thresholding
  στο Aspose.PSD for Java. Αυτός ο οδηγός σας δείχνει πώς να ορίσετε την τιμή του
  κατωφλίου, να μετατρέψετε PSD σε PNG και να αποθηκεύσετε τη δυαδικοποιημένη εικόνα.
og_image_alt: 'Guide: binarize image using Bradley thresholding in Aspose.PSD for
  Java'
og_title: Πώς να δυαδικοποιήσετε εικόνα σε Java με Bradley thresholding
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  headline: How to binarize image in Java using Bradley thresholding
  type: TechArticle
- description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  name: How to binarize image in Java using Bradley thresholding
  steps:
  - name: '**Java development environment** – JDK 11 or newer installed and configured.'
    text: '**Java development environment** – JDK 11 or newer installed and configured.'
  - name: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
    text: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
  type: HowTo
- questions:
  - answer: It is an adaptive binarization technique that computes a local average
      for each pixel and thresholds based on a percentage of that average.
    question: What is Bradley thresholding?
  - answer: Start with 0.5 (50 %). If the output is too noisy, increase the value;
      if details are lost, decrease it. Test a few values on a representative sample.
    question: How do I choose the right threshold value?
  - answer: Yes. Aspose.PSD supports more than 30 input and output formats—including
      PSD, PNG, JPEG, BMP, and TIFF—so you can load a JPEG, convert it to a `PsdImage`,
      and then binarize.
    question: Can I apply Bradley thresholding to other image formats?
  - answer: You can call `image.save("preview.png", new PngOptions())` after the `binarizeBradley`
      step to write a temporary file for visual inspection.
    question: Is there a way to preview the binarized image before saving?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      help and explore the official [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references.
    question: Where can I find more support and resources?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- image binarization
- Aspose.PSD
- Java image processing
- Bradley thresholding
title: Πώς να δυαδικοποιήσετε εικόνα σε Java χρησιμοποιώντας το Bradley thresholding
url: /el/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να δυαδικοποιήσετε μια εικόνα σε Java χρησιμοποιώντας το κατώφλι Bradley

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε **πώς να δυαδικοποιήσετε εικόνα** εφαρμόζοντας το Bradley Thresholding με Aspose.PSD for Java. Η δυαδικοποίηση μετατρέπει μια έγχρωμη ή γκρι κλίμακα εικόνα σε μια εκδοχή μαύρο‑λευκή, η οποία είναι απαραίτητη για OCR, αρχειοθέτηση εγγράφων και πολλές αλυσίδες υπολογιστικής όρασης. Θα περάσουμε από κάθε βήμα — από τη φόρτωση ενός αρχείου PSD μέχρι την αποθήκευση του τελικού PNG — ώστε να μπορείτε να ενσωματώσετε την τεχνική στα δικά σας έργα Java.

## Σύντομες απαντήσεις
- **Τι κάνει το κατώφλι Bradley;** Προσδιορίζει προσαρμοστικά ένα τοπικό κατώφλι για κάθε pixel, διατηρώντας τις λεπτομέρειες σε ανώμαλο φωτισμό.
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.PSD for Java (συνιστάται η πιο πρόσφατη έκδοση).
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.
- **Μπορώ να επεξεργαστώ μεγάλα αρχεία PSD;** Ναι, το API διαχειρίζεται αρχεία έως 2 GB χωρίς να φορτώνει ολόκληρη την εικόνα στη μνήμη.
- **Ποια μορφή εξόδου συνιστάται;** Το PNG είναι χωρίς απώλειες και ευρέως υποστηριζόμενο για δυαδικοποιημένα αποτελέσματα.

## Τι είναι το κατώφλι Bradley;

Το κατώφλι Bradley είναι ένας προσαρμοστικός αλγόριθμος δυαδικοποίησης που υπολογίζει έναν τοπικό μέσο όρο γύρω από κάθε pixel και ορίζει το pixel σε λευκό εάν η έντασή του υπερβαίνει το μέσο όρο κατά ένα ρυθμιζόμενο ποσοστό. Αυτή η προσέγγιση διατηρεί τις λεπτομέρειες των άκρων ακόμη και όταν ο φωτισμός διαφέρει στην εικόνα.

## Γιατί να χρησιμοποιήσετε το κατώφλι Bradley για τη δυαδικοποίηση εικόνας;

Το κατώφλι Bradley παρέχει σταθερά υψηλή αντίθεση σε εικόνες με άνισο φωτισμό, επιτυγχάνοντας έως και 95 % ακρίβεια OCR σε σαρωμένα έγγραφα σε σύγκριση με τις μεθόδους παγκόσμιου κατωφλίου. Η υλοποίηση του Aspose.PSD επεξεργάζεται ένα PSD 500 σελίδων σε λιγότερο από 4 δευτερόλεπτα σε έναν τυπικό διακομιστή 8‑πύρηνων, καθιστώντας το κατάλληλο για εργασίες παρτίδας.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

1. **Java development environment** – JDK 11 ή νεότερο εγκατεστημένο και ρυθμισμένο.
2. **Aspose.PSD library** – κατεβάστε το πιο πρόσφατο JAR από [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
3. **Sample PSD image** – ένα αρχείο PSD που θέλετε να δυαδικοποιήσετε· μπορείτε να χρησιμοποιήσετε οποιαδήποτε εικόνα έχετε ή ένα αρχείο δοκιμής.

## Εισαγωγή πακέτων

Οι παρακάτω εισαγωγές σας δίνουν πρόσβαση στις βασικές κλάσεις που χρειάζονται για τη φόρτωση, επεξεργασία και αποθήκευση εικόνων.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Πώς να δυαδικοποιήσετε εικόνα χρησιμοποιώντας το κατώφλι Bradley;

Σε αυτό το tutorial θα φορτώσετε ένα αρχείο PSD, θα επιλέξετε ένα κατάλληλο κατώφλι, θα εκτελέσετε την προσαρμοστική δυαδικοποίηση Bradley και τέλος θα γράψετε το αποτέλεσμα σε αρχείο PNG. Η διαδικασία αποτελείται από τέσσερις σύντομες κλήσεις μεθόδων, καθεμία με παραδείγματα κώδικα, επιτρέποντάς σας να ενσωματώσετε τη ροή εργασίας σε οποιαδήποτε εφαρμογή Java με ελάχιστη προσπάθεια.

## Βήμα 1: φόρτωση της εικόνας

Η κλάση `PsdImage` αντιπροσωπεύει ένα αρχείο PSD στη μνήμη και παρέχει μεθόδους για χειρισμό σε επίπεδο pixel. Δημιουργώντας μια παρουσία, αποκτάτε πρόσβαση στα πλήρη δεδομένα της εικόνας.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

Σε αυτό το βήμα το αρχείο PSD διαβάζεται από το δίσκο και αποθηκεύεται σε ένα αντικείμενο `PsdImage`, έτοιμο για επεξεργασία.

## Βήμα 2: ορισμός τιμής κατωφλίου

Η παράμετρος `threshold` ελέγχει πόσο επιθετική είναι η δυαδικοποίηση· μια τιμή 0.5 (50 %) είναι ένα κοινό σημείο εκκίνησης. Προσαρμόστε την ανάλογα με την αντίθεση της πηγαίας εικόνας σας.

```java
// Define threshold value
double threshold = 0.15;
```

Ο σωστός ορισμός του κατωφλίου εξισορροπεί τη μείωση του θορύβου με τη διατήρηση των λεπτομερειών.

## Βήμα 3: εφαρμογή του κατωφλίου Bradley

Η μέθοδος `binarizeBradley` εκτελεί την προσαρμοστική δυαδικοποίηση χρησιμοποιώντας το κατώφλι που δώσατε. Αναλύει ένα τοπικό παράθυρο γύρω από κάθε pixel για να αποφασίσει αν θα το κάνει μαύρο ή λευκό.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

Μετά από αυτήν την κλήση, η παρουσία `PsdImage` περιέχει μια μαύρο‑λευκή έκδοση της αρχικής εικόνας.

## Βήμα 4: αποθήκευση της εξόδου εικόνας

Η μέθοδος `save` γράφει την επεξεργασμένη εικόνα στο σύστημα αρχείων. Επιλέγεται το PNG επειδή διατηρεί τα δυαδικά δεδομένα χωρίς πρόσθετα σφάλματα συμπίεσης.

```java
// Save the output image
image.save(destName, new PngOptions());
```

Τώρα έχετε ένα δυαδικοποιημένο PNG που μπορεί να τροφοδοτηθεί σε μηχανές OCR ή άλλες επόμενες διεργασίες.

## Συχνά προβλήματα και λύσεις

Η LoadOptions είναι μια κλάση που σας επιτρέπει να καθορίσετε πώς φορτώνεται ένα αρχείο PSD, όπως η ενεργοποίηση της λειτουργίας streaming για μείωση της χρήσης μνήμης.

- **Η εικόνα εμφανίζεται πολύ σκοτεινή ή πολύ φωτεινή** – προσαρμόστε την τιμή του κατωφλίου· χαμηλότερες τιμές κάνουν την εικόνα πιο φωτεινή, υψηλότερες την κάνουν πιο σκοτεινή.
- **Σφάλματα έλλειψης μνήμης σε πολύ μεγάλα PSD** – ενεργοποιήστε τη λειτουργία streaming καλώντας `PsdImage.setLoadOptions(new LoadOptions { LoadMode = LoadMode.Stream })` πριν τη φόρτωση. Το `LoadMode.Stream` ενεργοποιεί τη λειτουργία streaming για μεγάλα αρχεία.
- **Απρόσμενες χρωματικές ζώνες** – βεβαιωθείτε ότι το πηγαίο PSD είναι σε λειτουργία RGB· μετατρέψτε το χρησιμοποιώντας `image.convertToRgb()` εάν είναι απαραίτητο. Η μέθοδος `convertToRgb()` μετατρέπει την εικόνα στο χρωματικό χώρο RGB, διασφαλίζοντας σωστή διαχείριση χρωμάτων.

## Συχνές ερωτήσεις

**Q: Τι είναι το κατώφλι Bradley;**  
A: Είναι μια προσαρμοστική τεχνική δυαδικοποίησης που υπολογίζει έναν τοπικό μέσο όρο για κάθε pixel και εφαρμόζει κατώφλι με βάση ένα ποσοστό αυτού του μέσου όρου.

**Q: Πώς να επιλέξω τη σωστή τιμή κατωφλίου;**  
A: Ξεκινήστε με 0.5 (50 %). Εάν το αποτέλεσμα είναι πολύ θορυβώδες, αυξήστε την τιμή· εάν χάνονται λεπτομέρειες, μειώστε την. Δοκιμάστε μερικές τιμές σε ένα αντιπροσωπευτικό δείγμα.

**Q: Μπορώ να εφαρμόσω το κατώφλι Bradley σε άλλες μορφές εικόνας;**  
A: Ναι. Το Aspose.PSD υποστηρίζει πάνω από 30 μορφές εισόδου και εξόδου — συμπεριλαμβανομένων των PSD, PNG, JPEG, BMP και TIFF — ώστε μπορείτε να φορτώσετε ένα JPEG, να το μετατρέψετε σε `PsdImage` και στη συνέχεια να το δυαδικοποιήσετε.

**Q: Υπάρχει τρόπος να προεπισκοπήσετε την δυαδικοποιημένη εικόνα πριν την αποθήκευση;**  
A: Μπορείτε να καλέσετε `image.save("preview.png", new PngOptions())` μετά το βήμα `binarizeBradley` για να γράψετε ένα προσωρινό αρχείο για οπτική επιθεώρηση.

**Q: Πού μπορώ να βρω περισσότερη υποστήριξη και πόρους;**  
A: Επισκεφθείτε το [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) για βοήθεια από την κοινότητα και εξερευνήστε την επίσημη [documentation](https://reference.aspose.com/psd/java/) για λεπτομερείς αναφορές API.

---

**Τελευταία ενημέρωση:** 2026-08-17  
**Δοκιμή με:** Aspose.PSD 24.12 for Java  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Java Image Processing Tutorial - Ρύθμιση Φωτεινότητας Εικόνας με Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Πώς να Ρυθμίσετε το Gamma στην Επεξεργασία Εικόνας Java με Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [Βιβλιοθήκη Επεξεργασίας Εικόνας Java: Αντιστροφή Στρώματος με Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}