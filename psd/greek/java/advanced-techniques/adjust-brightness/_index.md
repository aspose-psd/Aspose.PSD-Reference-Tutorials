---
date: 2026-09-28
description: Το tutorial επεξεργασίας εικόνας Java δείχνει πώς να ρυθμίσετε τη φωτεινότητα
  μιας εικόνας χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθήστε τον κώδικα step‑by‑step
  για να φορτώσετε, τροποποιήσετε και αποθηκεύσετε αρχεία PSD ή TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Ρύθμιση φωτεινότητας εικόνας
og_description: Το tutorial επεξεργασίας εικόνας Java δείχνει πώς να ρυθμίσετε τη
  φωτεινότητα μιας εικόνας χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθήστε τον
  κώδικα step‑by‑step για να φορτώσετε, τροποποιήσετε και αποθηκεύσετε αρχεία PSD
  ή TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Επεξεργασία εικόνας Java: ρύθμιση φωτεινότητας με Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Επεξεργασία εικόνας Java: ρύθμιση φωτεινότητας με Aspose.PSD'
url: /el/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ρύθμιση φωτεινότητας εικόνας με Aspose.PSD για Java

## Εισαγωγή

Σε αυτό το **java image processing** tutorial θα μάθετε πώς να ρυθμίζετε τη φωτεινότητα μιας εικόνας απευθείας από κώδικα Java. Η ρύθμιση της φωτεινότητας είναι μια συχνή εργασία για γραφίστες, φωτογράφους και όποιον δημιουργεί pipelines επεξεργασίας εικόνας. Σε αυτόν τον **java image manipulation** οδηγό θα περάσουμε από τη πλήρη ροή εργασίας — φόρτωση PSD/TIFF, εφαρμογή μετατόπισης φωτεινότητας και αποθήκευση του αποτελέσματος — χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD for Java.

## Γρήγορες απαντήσεις

- **Ποια βιβλιοθήκη διαχειρίζεται τη φωτεινότητα;** Aspose.PSD for Java.  
- **Ποια μέθοδος αλλάζει τη φωτεινότητα;** `RasterImage.adjustBrightness()`.  
- **Μπορώ να δουλέψω με αρχεία PSD και TIFF;** Ναι, το API υποστηρίζει και τις δύο μορφές και 10+ επιπλέον τύπους εικόνας.  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται εμπορική άδεια για μη‑αξονική χρήση.  
- **Πόσο χρόνο παίρνει η υλοποίηση;** Συνήθως λιγότερο από 10 λεπτά για μια βασική ρύθμιση.

## Τι είναι η επεξεργασία εικόνας με Java;

`Java image processing` αναφέρεται στο σύνολο των τεχνικών που σας επιτρέπουν να διαβάζετε, μετασχηματίζετε και γράφετε δεδομένα εικόνας προγραμματιστικά χρησιμοποιώντας Java. Η ρύθμιση της φωτεινότητας είναι μία από τις βασικές λειτουργίες που αλλάζει τη συνολική φωτεινότητα κάθε pixel, κάνοντας τις σκοτεινές περιοχές πιο φωτεινές ή τις φωτεινές πιο σκοτεινές.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για Java;

Aspose.PSD for Java παρέχει μια ολοκληρωμένη, καθαρά‑Java λύση που υποστηρίζει ένα ευρύ φάσμα μορφών raster και vector, εξαλείφει τις εγγενείς εξαρτήσεις και προσφέρει υψηλής απόδοσης caching για μεγάλα αρχεία. Το εκτενές του API επιτρέπει στους προγραμματιστές να εκτελούν σύνθετες διορθώσεις χρώματος και επεμβάσεις βασισμένες σε στρώματα με ελάχιστο κώδικα, καθιστώντας το ιδανικό τόσο για απλές ρυθμίσεις όσο και για προχωρημένα pipelines επεξεργασίας εικόνας.

- **Υποστηρίζει 10+ μορφές raster και vector** – PSD, TIFF, JPEG, PNG, BMP, GIF, και άλλα.  
- **Καθαρή υλοποίηση Pure‑Java** – χωρίς εγγενή DLLs ή εξωτερικές εξαρτήσεις, λειτουργεί σε οποιοδήποτε JVM.  
- **Caching υψηλής απόδοσης** – τα raster δεδομένα μπορούν να αποθηκευτούν στην κρυφή μνήμη, επιτρέποντας έως και 2× ταχύτερες επαναλαμβανόμενες επεμβάσεις σε μεγάλα αρχεία.  
- **Πλούσια επιφάνεια API** – πάνω από 150 μεθόδους για διόρθωση χρώματος, διαχείριση στρώσεων, μάσκες και σύνθεση.

## Απαιτούμενα

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω απαιτούμενα:

- Aspose.PSD for Java Library: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη από την [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 ή νεότερο εγκατεστημένο στον υπολογιστή σας.  
- Περιβάλλον ανάπτυξης (IDE) όπως IntelliJ IDEA, Eclipse ή VS Code.

## Εισαγωγή πακέτων

Για να ξεκινήσετε, εισάγετε τα απαραίτητα πακέτα στο έργο Java σας. Σε αυτό το παράδειγμα, θα χρησιμοποιήσουμε τα παρακάτω:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Τώρα, ας αναλύσουμε τη διαδικασία ρύθμισης της φωτεινότητας μιας εικόνας σε απλά βήματα:

## Πώς να ρυθμίσετε τη φωτεινότητα χρησιμοποιώντας το Aspose.PSD;

Φορτώστε την πηγή εικόνας, εφαρμόστε μια μετατόπιση φωτεινότητας, διαμορφώστε τις επιλογές αποθήκευσης και γράψτε το αποτέλεσμα στο δίσκο — όλα σε τέσσερα σύντομα βήματα. Οι παρακάτω ενότητες παρέχουν έναν σαφή, βήμα‑βήμα οδηγό που μπορείτε να αντιγράψετε στο δικό σας έργο. Αυτή η προσέγγιση εξασφαλίζει ότι κάθε λειτουργία εκτελείται αποδοτικά και ότι η τελική εικόνα διατηρεί την αρχική ποιότητα ενώ αντικατοπτρίζει την επιθυμητή αλλαγή φωτεινότητας.

### Βήμα 1: Φόρτωση της εικόνας

Η κλάση `RasterImage` αντιπροσωπεύει μια rasterized έκδοση ενός αρχείου PSD ή TIFF στη μνήμη. Παρέχει άμεση πρόσβαση σε pixel για λειτουργίες διόρθωσης χρώματος.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

### Βήμα 2: Ρύθμιση φωτεινότητας

`adjustBrightness(int value)` αλλάζει τη φωτεινότητα κάθε pixel κατά την καθορισμένη ακέραια τιμή. Οι θετικοί αριθμοί φωτίζουν την εικόνα· οι αρνητικοί την σκοτεινιάζουν. Η μέθοδος επεξεργάζεται την εικόνα εντός μνήμης, χωρίς να απαιτείται δημιουργία επιπλέον αντικειμένου.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Εδώ, χρησιμοποιούμε τη μέθοδο `adjustBrightness` για να τροποποιήσουμε τη φωτεινότητα της εικόνας. Σε αυτό το παράδειγμα, μειώνουμε τη φωτεινότητα κατά 50 μονάδες, αλλά μπορείτε να προσαρμόσετε αυτήν την τιμή σύμφωνα με τις απαιτήσεις σας.

### Βήμα 3: Ρύθμιση TiffOptions

`TiffOptions` καθορίζει τις παραμέτρους κωδικοποίησης για έξοδο TIFF, όπως bits per sample και photometric interpretation. Σας επιτρέπει να ελέγχετε πώς κωδικοποιείται το τελικό αρχείο.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Διαμορφώστε το `TiffOptions` για την αποθήκευση της ρυθμισμένης εικόνας. Προσαρμόστε τις ιδιότητες `bitsPerSample` και `photometric` ανάλογα με τις συγκεκριμένες ανάγκες σας.

### Βήμα 4: Αποθήκευση της τελικής εικόνας

Η κλήση του `save` γράφει τα επεξεργασμένα raster δεδομένα σε αρχείο χρησιμοποιώντας τις προηγουμένως ορισμένες επιλογές. Η λειτουργία είναι ατομική και εγγυάται ότι το αρχείο εξόδου είναι έγκυρη εικόνα TIFF.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Τέλος, αποθηκεύστε την τροποποιημένη εικόνα χρησιμοποιώντας το καθορισμένο `TiffOptions`.

## Κοινά προβλήματα και λύσεις

| Πρόβλημα | Αιτία | Λύση |
|----------|-------|------|
| **`ClassCastException` κατά την μετατροπή Image** | Το αρχείο δεν είναι raster εικόνα (π.χ., vector PSD). | Επαληθεύστε τη μορφή του αρχείου προέλευσης ή χρησιμοποιήστε `image instanceof RasterImage` πριν τη μετατροπή. |
| **Η αλλαγή φωτεινότητας δεν έχει αποτέλεσμα** | Η εικόνα δεν είχε αποθηκευτεί στην κρυφή μνήμη πριν τη ρύθμιση. | Καλέστε `rasterImage.cacheData()` όπως φαίνεται στο Βήμα 1. |
| **Το αποθηκευμένο αρχείο φαίνεται κατεστραμμένο** | Λανθασμένη διαμόρφωση `TiffOptions`. | Βεβαιωθείτε ότι το `bitsPerSample` ταιριάζει με το βάθος της πηγαίας εικόνας (συνήθως 8‑bit ανά κανάλι). |

## Συχνές ερωτήσεις

**Q: Μπορώ να ρυθμίσω τη φωτεινότητα σε άλλες μορφές εικόνας εκτός από PSD;**  
A: Ναι, το Aspose.PSD for Java υποστηρίζει JPEG, PNG, BMP, GIF και πολλές άλλες μορφές raster εκτός από PSD και TIFF.

**Q: Πώς μπορώ να διαχειριστώ σφάλματα κατά τη διαδικασία ρύθμισης της εικόνας;**  
A: Τυλίξτε τον κώδικα επεξεργασίας σε μπλοκ try‑catch και πιάστε `IOException` ή `ImageProcessingException` για να διαχειριστείτε σφάλματα πρόσβασης αρχείων και λειτουργιών raster.

**Q: Υπάρχει όριο στο εύρος ρύθμισης της φωτεινότητας;**  
A: Η μέθοδος δέχεται ακέραιες τιμές από –255 έως +255· οι τιμές εκτός αυτού του εύρους περιορίζονται στο πλησιέστερο όριο.

**Q: Μπορώ να χρησιμοποιήσω το Aspose.PSD for Java σε εμπορικά έργα;**  
A: Ναι, απαιτείται εμπορική άδεια για χρήση σε παραγωγή. Αγοράστε άδεια [εδώ](https://purchase.aspose.com/buy).

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
A: Ναι, μπορείτε να εξερευνήσετε τη βιβλιοθήκη με δωρεάν δοκιμή από [εδώ](https://releases.aspose.com/).

**Q: Η μέθοδος `adjustBrightness` επηρεάζει την ορατότητα των στρώσεων;**  
A: Η μέθοδος λειτουργεί στην rasterized σύνθετη εικόνα, έτσι οι κρυμμένες στρώσεις αγνοούνται κατά τη rasterization, διατηρώντας το επιθυμητό οπτικό αποτέλεσμα.

**Q: Μπορώ να συνδυάσω πολλαπλές ρυθμίσεις (π.χ., αντίθεση, κορεσμό) μαζί;**  
A: Απόλυτα. Μετά τη ρύθμιση της φωτεινότητας, μπορείτε να καλέσετε `adjustContrast`, `adjustSaturation` ή άλλες μεθόδους διόρθωσης χρώματος στο ίδιο αντικείμενο `RasterImage`.

---

**Τελευταία ενημέρωση:** 2026-09-28  
**Δοκιμάστηκε με:** Aspose.PSD for Java 24.12 (τελευταία έκδοση κατά τη στιγμή της συγγραφής)  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Βιβλιοθήκη επεξεργασίας εικόνας Java: Αντιστροφή στρώσης με Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Μετατροπή εικόνας σε κλίμακα του γκρι με Aspose.PSD for Java](/psd/java/advanced-techniques/grayscale-image/)
- [Πώς να περιστρέψετε εικόνα σε συγκεκριμένη γωνία με Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}