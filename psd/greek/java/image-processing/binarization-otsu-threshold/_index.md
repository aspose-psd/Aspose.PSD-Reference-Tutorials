---
date: 2026-01-09
description: Μάθετε πώς να εκτελείτε τμηματοποίηση εικόνας με τη μέθοδο Otsu χρησιμοποιώντας
  το Aspose.PSD για Java. Αυτό το σεμινάριο καλύπτει την επεξεργασία εικόνας σε Java,
  πώς να δυαδικοποιείτε και να εφαρμόζετε το όριο Otsu.
linktitle: Binarization with Otsu Threshold
second_title: Aspose.PSD Java API
title: Τμηματοποίηση Εικόνας Otsu – Δυαδικοποίηση με Κατώφλι Otsu στο Aspose.PSD για
  Java
url: /el/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δυαδικοποίηση με Κατώφλι Otsu στο Aspose.PSD για Java

## Εισαγωγή

Καλώς ήρθατε! Σε αυτόν τον οδηγό βήμα‑βήμα θα μάθετε **image segmentation otsu** χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD για Java. Είτε δημιουργείτε ένα εργαλείο επεξεργασίας φωτογραφιών, μια αυτοματοποιημένη γραμμή ανάλυσης εγγράφων, ή οποιοδήποτε έργο **java image processing**, η κατανόηση του πώς να δυαδικοποιείτε εικόνες με το κατώφλι Otsu θα σας προσφέρει έναν αξιόπιστο τρόπο για τη δημιουργία μιας καθαρής **binary image conversion**. Ας περάσουμε από όλη τη διαδικασία—από τη ρύθμιση του περιβάλλοντος μέχρι την αποθήκευση του τελικού JPEG—ώστε να μπορείτε να εφαρμόζετε το Otsu στις δικές σας εφαρμογές.

## Γρήγορες Απαντήσεις
- **What does Otsu threshold do?** Τι κάνει το κατώφλι Otsu; Αυτό αυτόματα βρίσκει το βέλτιστο όριο επιπέδου γκρι που διαχωρίζει τα pixel του προσκηνίου και του φόντου.  
- **Which library supports it in Java?** Ποια βιβλιοθήκη το υποστηρίζει σε Java; Το Aspose.PSD για Java παρέχει ενσωματωμένη μέθοδο `binarizeOtsu()`.  
- **Do I need a license to try it?** Χρειάζομαι άδεια για να το δοκιμάσω; Διατίθεται δωρεάν δοκιμή· απαιτείται άδεια για παραγωγική χρήση.  
- **What output format can I use?** Ποια μορφή εξόδου μπορώ να χρησιμοποιήσω; Το παράδειγμα αποθηκεύει JPEG, αλλά λειτουργεί οποιαδήποτε μορφή υποστηρίζεται από `RasterCachedImage.save()`.  
- **How long does the implementation take?** Πόσο χρόνο παίρνει η υλοποίηση; Με το έτοιμο API, μπορείτε να έχετε μια λειτουργική λύση σε λιγότερο από 10 λεπτά.

## Τι είναι το Image Segmentation Otsu;

**Image segmentation otsu** είναι μια στατιστική τεχνική που καθορίζει μια βέλτιστη τιμή κατωφλίου για τη μετατροπή μιας εικόνας σε κλίμακα του γκρι σε δυαδική εικόνα. Η μέθοδος αξιολογεί τη διασπορά εντός κλάσης του προσκηνίου και του φόντου και επιλέγει το κατώφλι που ελαχιστοποιεί αυτή τη διασπορά, οδηγώντας σε σαφή διαχωρισμό των αντικειμένων από το φόντο.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για Java;

- **High‑performance caching** – λειτουργεί αποδοτικά με μεγάλα αρχεία PSD.  
- **One‑line binarization** – το `binarizeOtsu()` αναλαμβάνει τη βαριά δουλειά.  
- **Cross‑format support** – φορτώνει PSD, επεξεργάζεται και αποθηκεύει ως JPEG, PNG κ.λπ.  
- **Enterprise‑ready licensing** – κατάλληλο για εμπορικές εφαρμογές.

## Προαπαιτούμενα

Πριν βυθιστούμε στον κώδικα, βεβαιωθείτε ότι έχετε τα εξής:

- **Java Development Environment** – Εγκατεστημένο JDK 8 ή νεότερο.  
- **Aspose.PSD for Java Library** – Κατεβάστε το από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/psd/java/).  
- **Sample PSD File** – Ένα PSD που θέλετε να δυαδικοποιήσετε (π.χ., `sample.psd`).  

## Εισαγωγή Πακέτων

Ξεκινήστε εισάγοντας τις απαραίτητες κλάσεις:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Βήμα 1: Ρύθμιση του Καταλόγου Εγγράφων σας

Ορίστε το φάκελο που περιέχει το πηγαίο PSD και όπου θα γραφτεί το αποτέλεσμα:

```java
String dataDir = "Your Document Directory";
```

## Βήμα 2: Φόρτωση του Αρχείου PSD

Φορτώστε το PSD σε αντικείμενο `Image` ώστε να μπορείτε να το επεξεργαστείτε:

```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Βήμα 3: Cache της Εικόνας

Αν η εικόνα δεν είναι ήδη cached, κάντε cache για να βελτιώσετε την ταχύτητα επεξεργασίας:

```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

## Βήμα 4: Δυαδικοποίηση της Εικόνας με Κατώφλι Otsu

Εφαρμόστε τον αλγόριθμο Otsu—αυτό είναι το κεντρικό μέρος του **how to apply otsu** για μια **binary image conversion**:

```java
rasterCachedImage.binarizeOtsu();
```

## Βήμα 5: Αποθήκευση της Παραγόμενης Εικόνας

Τέλος, γράψτε τη δυαδικοποιημένη εικόνα στο δίσκο χρησιμοποιώντας `JpegOptions` (μπορείτε επίσης να χρησιμοποιήσετε PNG ή BMP):

```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

## Κοινά Προβλήματα και Λύσεις

| Issue | Reason | Fix |
|-------|--------|-----|
| **`ClassCastException`** | Προσπάθεια μετατροπής μιας μη‑raster εικόνας | Βεβαιωθείτε ότι το PSD περιέχει raster στρώματα ή χρησιμοποιήστε `image.convertToRasterImage()` πριν από τη μετατροπή. |
|ωρίτερα και σκεφτείτε την αύξηση του μεγέθους heap της JVM (`-Xmx`). |
| **Incorrect output colors** | Η εικόνα δεν είχε cache σωστά | Επαληθεύστε ότι `isCached()` επέστρεψε `true` πριν καλέσετε `binarizeOtsu()`. |

## Συχνές Ερωτήσεις

### Q1: Τι είναι η Δυαδικοποίηση με Κατώφλι Otsu;

Η Δυαδικοποίηση με Κατώφλι Otsu είναι μια μέθοδος που χρησιμοποιείται για την κατατμηση εικόνας, χωρίζοντας μια εικόνα σε προσκήνιο και φόντο βάσει βέλτιστης οριοθέτησης.

### Q2: Μπορώ να χρησιμοποιήσω το Aspose.PSD για Java δωρεάν;

Το Aspose.PSD για Java είναι εμπορική βιβλιοθήκη, αλλά μπορείτε να εξερευνήσετε τις δυνατότητές της με δωρεάν δοκιμή. Λάβετε το [εδώ](https://releases.aspose.com/).

### Q3: Πού μπορώ να βρω την τεκμηρίωση του Aspose.PSD για Java;

Η τεκμηρίωση είναι διαθέσιμη [εδώ](https://reference.aspose.com/psd/java/).

### Q4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.PSD για Java;

Επισκεφθείτε το φόρουμ Aspose.PSD [εδώ](https://forum.aspose.com/c/psd/34) για υποστήριξη από την κοινότητα.

### Q5: Υπάρχει προσωρινή άδεια διαθέσιμη για το Aspose.PSD για Java;

Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

**Additional Q&A**

**Q: Πώς εντάσσεται αυτή η μέθοδος σε ένα μεγαλύτερο workflow επεξεργασίας εικόνας java;**  
A: Μετά τη δυαδικοποίηση, μπορείτε να τροφοδοτήσετε τη δυαδική εικόνα σε μονάδες ανίχνευσης περιγράμματος, προεπεξεργασίας OCR ή ανάλυσης σχήματος.

**Q: Μπορώ να ρυθμίσω τις παραμέτρους του αλγορίθμου Otsu;**  
A: Η μέθοδος `binarizeOtsu()` χρησιμοποιεί την τυπική υλοποίηση Otsu· για προσαρμοσμένα κατώφλια, χρησιμοποιήστε `binarize(int threshold)` αντί αυτού.

## Συμπέρασμα

Τώρα έχετε δει πώς να εκτελέσετε **image segmentation otsu** χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθώντας αυτά τα βήματα—ρύθμιση του περιβάλλοντος, φόρτωση και caching του PSD, εφαρμογή του `binarizeOtsu()` και αποθήκευση του αποτελέσματος—μπορείτε να ενσωματώσετε αξιόπιστη μετατροπή σε δυαδική εικόνα σε οποιοδήποτε έργο **java image processing**. Πειραματιστείτε με διαφορετικά αρχεία προέλευσης, συνδυάστε το αποτέλεσμα με OCR ή δημιουργήστε έναν επεξεργαστή δέσμης για αυτόματη διαχείριση πολλαπλών PSD.

---

**Τελευταία ενημέρωση:** 2026-01-09  
**Δοκιμάστηκε με:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}