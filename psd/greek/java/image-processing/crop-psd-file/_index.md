---
date: 2026-08-17
description: Μάθετε πώς να κόψετε αρχείο PSD Java με το Aspose.PSD for Java – ένας
  γρήγορος, ακριβής τρόπος για να περικόψετε έγγραφα Photoshop στις εφαρμογές Java
  σας.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Κόψτε αρχείο PSD
og_description: Κόψτε αρχείο PSD Java χρησιμοποιώντας το Aspose.PSD for Java. Αυτός
  ο οδηγός σας δείχνει βήμα‑βήμα πώς να περικόψετε αρχεία Photoshop αποδοτικά, με
  εξηγήσεις χωρίς κώδικα και συμβουλές βέλτιστων πρακτικών.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Κόψτε αρχείο PSD Java με το Aspose.PSD – γρήγορη περικοπή εικόνας
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Κόψτε αρχείο PSD Java χρησιμοποιώντας το Aspose.PSD
url: /el/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Κόψιμο αρχείου psd java με χρήση Aspose.PSD

## Εισαγωγή

Αν χρειάζεται να περικόψετε έγγραφα Photoshop προγραμματιστικά, **crop psd file java** είναι μια κοινή εργασία για προγραμματιστές Java που εργάζονται με γραφικές γραμμές παραγωγής, γραμμές παραγωγής περιουσιακών στοιχείων ή αυτοματοποιημένες ροές σχεδίασης. Το Aspose.PSD for Java παρέχει μια ειδική API που σας επιτρέπει να ορίσετε ένα ορθογώνιο και να εξάγετε την περιοχή που χρειάζεστε με λίγες μόνο γραμμές κώδικα. Σε αυτό το μάθημα θα μάθετε γιατί η βιβλιοθήκη είναι σχεδιασμένη για υψηλής απόδοσης περικοπή, πώς να ρυθμίσετε το περιβάλλον σας και τα ακριβή βήματα για την παραγωγή αποτελεσμάτων τόσο σε PSD όσο και σε PNG.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται το κόψιμο PSD σε Java;** Aspose.PSD for Java.
- **Πόσες γραμμές κώδικα απαιτούνται για ένα βασικό κόψιμο;** Δύο κλήσεις API μετά τη φόρτωση της εικόνας.
- **Μπορώ να εξάγω την περικομμένη περιοχή ως PNG;** Ναι, χρησιμοποιώντας τις ενσωματωμένες επιλογές αποθήκευσης PNG.
- **Απαιτείται άδεια για χρήση σε παραγωγή;** Απαιτείται εμπορική άδεια μετά την περίοδο δοκιμής.
- **Ποιες εκδόσεις Java υποστηρίζονται;** Java 8 και νεότερες, συμπεριλαμβανομένων των Java 11, 17 και 21.

## Τι είναι το crop psd file java;

Το crop psd file java αναφέρεται στη διαδικασία προγραμματιστικής αφαίρεσης μιας ορθογώνιας περιοχής από ένα έγγραφο Photoshop (.psd) χρησιμοποιώντας κώδικα Java. Με το Aspose.PSD μπορείτε να εκτελέσετε αυτήν τη λειτουργία χωρίς να ανοίξετε το Photoshop, καθιστώντας το ιδανικό για pipelines εικόνας στο διακομιστή.

## Γιατί να χρησιμοποιήσετε Aspose.PSD για Java;

Το Aspose.PSD υποστηρίζει **30+ μορφές εισόδου και εξόδου** και μπορεί να επεξεργαστεί αρχεία PSD έως **500 MB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, χάρη στην αρχιτεκτονική ροής δεδομένων του. Η βιβλιοθήκη διατηρεί τα στρώματα, τις μάσκες και τα προφίλ χρώματος, παρέχοντας ένα περικομμένο αποτέλεσμα που ταιριάζει με την εγγενή έξοδο του Photoshop. Αυτή η ποσοτικοποιημένη απόδοση σας επιτρέπει να διαχειρίζεστε παρτίδες εργασιών σε κοινό υλικό με προβλέψιμη χρήση μνήμης.

## Προαπαιτούμενα

- **Περιβάλλον ανάπτυξης Java** – εγκατεστημένο και ρυθμισμένο JDK 8 ή νεότερο.
- **Aspose.PSD for Java** – κατεβάστε το τελευταίο JAR και την τεκμηρίωση [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **Δείγμα αρχείου PSD** – τοποθετήστε ένα αρχείο .psd μέσα στον φάκελο του έργου σας ώστε ο κώδικας να το εντοπίσει.

## Πώς να κόψετε ένα αρχείο PSD σε Java;

Φορτώστε το αρχείο προέλευσης, ορίστε το ορθογώνιο που θέλετε να διατηρήσετε, εφαρμόστε την περικοπή και, τέλος, αποθηκεύστε το αποτέλεσμα στις επιθυμητές μορφές. Η πλήρης ροή εργασίας απαιτεί μόνο πέντε απλά βήματα, το καθένα εικονογραφημένο με έναν χώρο κράτησης όπου θα εισάγετε τον δικό σας κώδικα.

### Βήμα 1: ορισμός καταλόγου εγγράφου

Αντικαταστήστε το “Your Document Directory” με την απόλυτη ή σχετική διαδρομή που περιέχει το PSD που θέλετε να επεξεργαστείτε.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Βήμα 2: φόρτωση αρχείου PSD

Η κλάση `RasterImage` είναι το σημείο εισόδου του Aspose.PSD για λειτουργίες βασισμένες σε raster σε ένα αρχείο PSD. Η φόρτωση του αρχείου δημιουργεί μια αναπαράσταση στη μνήμη που μπορείτε να επεξεργαστείτε.

```java
String dataDir = "Your Document Directory";
```

### Βήμα 3: ορισμός περιοχής κοπής

Η `Rectangle` ορίζει τις συντεταγμένες X και Y μαζί με το πλάτος και το ύψος της περιοχής που θα διατηρηθεί. Αυτή η κλάση είναι μέρος του τυπικού πακέτου Java AWT και χρησιμοποιείται από το Aspose.PSD για τον καθορισμό των ορίων της περικοπής.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Βήμα 4: αποθήκευση περικομμένου PSD

Αφού εφαρμόσετε την περικοπή, μπορείτε να αποθηκεύσετε το αποτέλεσμα ξανά σε μορφή PSD. Η βιβλιοθήκη γράφει μόνο τα περικομμένα pixel, διατηρώντας την αρχική λειτουργία χρώματος και το βάθος bit.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Βήμα 5: αποθήκευση περικομμένης εικόνας ως PNG

Αν χρειάζεστε μια έκδοση φιλική για το web, εξάγετε το περικομμένο raster σε PNG. Το Aspose.PSD παρέχει επιλογές αποθήκευσης PNG που σας επιτρέπουν να ελέγξετε το επίπεδο συμπίεσης και το interlacing.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Συχνά προβλήματα και λύσεις

- **Λανθασμένες συντεταγμένες ορθογωνίου** – Βεβαιωθείτε ότι οι τιμές X/Y ξεκινούν από 0 για την επάνω‑αριστερή γωνία· οι αρνητικές τιμές θα προκαλέσουν `ArgumentException`.
- **Αιχμές μνήμης σε μεγάλα αρχεία** – Χρησιμοποιήστε την επιλογή `loadOptions.setLoadOnlyVisibleLayers(true)` για μείωση της μνήμης όταν δεν χρειάζεστε κρυφά στρώματα.
- **Απώλεια χρωματικού προφίλ** – Διατηρήστε το αρχικό προφίλ ICC καλώντας `image.getColorProfile()` πριν το κόψιμο και επανατοποθετώντας το μετά την ενέργεια.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω Aspose.PSD για Java για να κόψω εικόνες σε άλλες μορφές;

Α1: Το Aspose.PSD στοχεύει κυρίως σε αρχεία PSD, αλλά υποστηρίζει επίσης BMP, GIF, JPEG, PNG, TIFF και αρκετές άλλες μορφές raster τόσο για είσοδο όσο και για έξοδο.

### Ε2: Είναι το Aspose.PSD για Java κατάλληλο για μεγάλης κλίμακας επεξεργασία εικόνων;

Α2: Ναι. Η αρχιτεκτονική streaming της βιβλιοθήκης επεξεργάζεται αρχεία PSD πολλαπλών εκατοντάδων σελίδων με κατανάλωση μνήμης κάτω από 100 MB, καθιστώντας το ιδανικό για εργασίες batch.

### Ε3: Υπάρχουν ζητήματα αδειοδότησης για τη χρήση του Aspose.PSD για Java;

Α3: Απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις. Λεπτομέρειες διατίθενται στη [σελίδα αγοράς Aspose.PSD for Java](https://purchase.aspose.com/buy).

### Ε4: Πώς μπορώ να λάβω υποστήριξη για ζητήματα σχετικά με Aspose.PSD for Java;

Α4: Επισκεφθείτε το [φόρουμ Aspose.PSD for Java](https://forum.aspose.com/c/psd/34) για να θέσετε ερωτήσεις, να μοιραστείτε αποσπάσματα κώδικα και να λάβετε βοήθεια από την κοινότητα και τους μηχανικούς του προϊόντος.

### Ε5: Μπορώ να δοκιμάσω το Aspose.PSD for Java πριν την αγορά;

Α5: Ναι, μπορείτε να κατεβάσετε μια πλήρως λειτουργική δωρεάν δοκιμή [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Σχετικά Μαθήματα

- [Κόψιμο εικόνας με ορθογώνιο στο Aspose.PSD για Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Κόψιμο εικόνας με μετατοπίσεις στο Aspose.PSD για Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Πώς να περιστρέψετε εικόνα σε Java με Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}