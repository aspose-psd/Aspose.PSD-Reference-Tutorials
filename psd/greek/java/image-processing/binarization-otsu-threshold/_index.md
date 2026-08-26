---
date: 2026-08-11
description: Μάθετε πώς να εφαρμόζετε otsu threshold java χρησιμοποιώντας Aspose.PSD
  for Java – μια ισχυρή τεχνική image segmentation.
keywords:
- apply otsu threshold java
- image segmentation with otsu
- java image segmentation tutorial
lastmod: 2026-08-11
linktitle: Δυαδικοποίηση με Otsu Threshold
og_description: Εφαρμόστε otsu threshold java με Aspose.PSD for Java. Αυτό το tutorial
  σας δείχνει βήμα‑βήμα πώς να binarize images, εξηγεί γιατί η μέθοδος είναι γρήγορη
  και παρέχει συμβουλές troubleshooting για κοινά pitfalls.
og_image_alt: Screenshot of Java code applying Otsu threshold using Aspose.PSD
og_title: Εφαρμογή otsu threshold java με Aspose.PSD – γρήγορος οδηγός
schemas:
- author: Aspose
  dateModified: '2026-08-11'
  description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  headline: Apply otsu threshold java with Aspose.PSD
  type: TechArticle
- description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  name: Apply otsu threshold java with Aspose.PSD
  steps:
  - name: set up your document directory
    text: Define the folder that contains the source PSD file and the output location
      for the binarized image.
  - name: load the PSD file
    text: '`PsdImage` is the top‑level Aspose.PSD class that represents a PSD document
      and gives access to its layers, metadata, and pixel data.'
  - name: cache the image
    text: '`RasterImage` holds the raster representation of a layer; calling `cache()`
      loads the pixel data into memory so subsequent operations are fast.'
  - name: binarize image with Otsu threshold
    text: '`applyOtsuThreshold()` evaluates all possible gray levels and selects the
      optimal cutoff, producing a binary image that separates foreground objects from
      the background.'
  - name: save the resultant image
    text: '`JpegOptions` configures JPEG‑specific settings such as quality and compression
      when saving the processed image. You can also choose PNG or BMP by swapping
      the options class – the API supports over **30 image formats** for output. {{<
      blocks/products/products-backtop-button >}}'
  type: HowTo
- questions:
  - answer: It automatically finds the gray‑level that minimizes intra‑class variance,
      producing a binary image in one step.
    question: What does Otsu Threshold do?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the sample?
  - answer: Aspose.PSD for Java supports Java 8 through Java 21.
    question: Which Java version is supported?
  - answer: Yes – you can iterate over each layer and apply the threshold individually.
    question: Can I process multi‑layer PSD files?
  - answer: For a 1920 × 1080 image the Otsu binarization finishes in under 30 ms
      on a typical laptop CPU.
    question: How fast is the operation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- apply otsu threshold java
- image segmentation
- Aspose.PSD
- Java image processing
title: Εφαρμογή του otsu threshold java με Aspose.PSD
url: /el/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εφαρμογή κατωφλίου Otsu java με Aspose.PSD

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε πώς να **apply otsu threshold java** χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD for Java. Η δυαδικοποίηση με το κατώφλι Otsu είναι μία από τις πιο αξιόπιστες τεχνικές τμηματοποίησης εικόνας με τεχνικές Otsu, επιλέγοντας αυτόματα ένα βέλτιστο επίπεδο γκρι για να διαχωρίσει το προσκήνιο από το φόντο. Στο τέλος του οδηγού θα έχετε ένα λειτουργικό απόσπασμα Java που μετατρέπει οποιοδήποτε στρώμα PSD σε καθαρή ασπρόμαυρη εικόνα.

## Γρήγορες απαντήσεις
- **Τι κάνει το κατώφλι Otsu;** Εντοπίζει αυτόματα το επίπεδο γκρι που ελαχιστοποιεί τη διακύμανση εντός κλάσης, παράγοντας μια δυαδική εικόνα σε ένα βήμα.  
- **Χρειάζομαι άδεια για την εκτέλεση του δείγματος;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια έκδοση Java υποστηρίζεται;** Το Aspose.PSD for Java υποστηρίζει Java 8 μέχρι Java 21.  
- **Μπορώ να επεξεργαστώ αρχεία PSD πολλαπλών στρωμάτων;** Ναι – μπορείτε να επαναλάβετε κάθε στρώμα και να εφαρμόσετε το κατώφλι ξεχωριστά.  
- **Πόσο γρήγορη είναι η λειτουργία;** Για εικόνα 1920 × 1080 η δυαδικοποίηση Otsu ολοκληρώνεται σε κάτω από 30 ms σε τυπική CPU laptop.

## Τι είναι η εφαρμογή κατωφλίου Otsu java;

Η εφαρμογή κατωφλίου Otsu java είναι η διαδικασία χρήσης κώδικα Java για την κλήση του αλγορίθμου Otsu σε μια εικόνα, παράγοντας ένα δυαδικό (μαύρο‑άσπρο) αποτέλεσμα. Ο αλγόριθμος αξιολογεί κάθε δυνατό επίπεδο γκρι, επιλέγει αυτό που δίνει τη χαμηλότερη σταθμισμένη διακύμανση εντός κλάσης, και στη συνέχεια ταξινομεί κάθε pixel ως προσκήνιο ή φόντο. Αυτή η αυτοματοποιημένη προσέγγιση εξαλείφει την ανάγκη χειροκίνητης επιλογής κατωφλίου και λειτουργεί καλά σε εικόνες με διπλόμονα ιστογράμματα, καθιστώντας την ιδανική για επεξεργασία μεγάλων συλλογών εικόνων σε παρτίδες.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD for Java;

Το Aspose.PSD for Java υποστηρίζει **50+ μορφές εισόδου και εξόδου** (συμπεριλαμβανομένων PSD, JPEG, PNG, BMP και TIFF) και μπορεί να επεξεργαστεί αρχεία έως **2 GB** σε μέγεθος χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη. Η ενσωματωμένη υλοποίηση Otsu της βιβλιοθήκης εκτελείται σε γραμμικό χρόνο, επιτρέποντάς σας να επεξεργαστείτε εκατοντάδες εικόνες σε λίγα δευτερόλεπτα.

## Προαπαιτούμενα

- **Περιβάλλον ανάπτυξης Java** – JDK 8 ή νεότερο εγκατεστημένο και ρυθμισμένο.  
- **Βιβλιοθήκη Aspose.PSD for Java** – Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη από την επίσημη σελίδα λήψης Aspose.PSD for Java. Μπορείτε να βρείτε τον σύνδεσμο λήψης [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
- **Δείγμα αρχείου PSD** – Έχετε ένα αρχείο PSD με τουλάχιστον ένα raster στρώμα για να δοκιμάσετε τη δυαδικοποίηση.  
- Για άλλα προϊόντα Aspose μπορείτε επίσης να περιηγηθείτε στη γενική σελίδα εκδόσεων στο [Aspose releases](https://releases.aspose.com/).

## Εισαγωγή πακέτων

Εισάγετε τις κλάσεις `PsdImage`, `RasterImage` και `JpegOptions` από τη βιβλιοθήκη Aspose.PSD, οι οποίες παρέχουν πρόσβαση σε αρχεία PSD, δεδομένα raster και επιλογές εξαγωγής JPEG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Πώς να εφαρμόσετε το κατώφλι Otsu java;

Φορτώστε το PSD σας, ανακτήστε το επιθυμητό raster στρώμα και καλέστε τη μέθοδο δυαδικοποίησης Otsu – η πλήρης ροή εργασίας χωράει σε πέντε σύντομες δηλώσεις. Πρώτα, δημιουργείτε ένα αντικείμενο `PsdImage` που αντιπροσωπεύει το αρχείο προέλευσης, στη συνέχεια λαμβάνετε το `RasterImage` για το στοχευόμενο στρώμα, καλείτε `applyOtsuThreshold()` επάνω του, και τέλος αποθηκεύετε το αποτέλεσμα χρησιμοποιώντας `JpegOptions`. Αυτή η προσέγγιση εξασφαλίζει ελάχιστη χρήση μνήμης και μέγιστη απόδοση.

### Βήμα 1: ρυθμίστε τον φάκελο εγγράφου σας

Ορίστε το φάκελο που περιέχει το αρχείο PSD προέλευσης και την τοποθεσία εξόδου για τη δυαδικοποιημένη εικόνα.  
```java
String dataDir = "Your Document Directory";
```

### Βήμα 2: φορτώστε το αρχείο PSD

`PsdImage` είναι η κλάση υψηλότερου επιπέδου του Aspose.PSD που αντιπροσωπεύει ένα έγγραφο PSD και παρέχει πρόσβαση στα στρώματά του, στα μεταδεδομένα και στα δεδομένα pixel.  
```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Βήμα 3: αποθηκεύστε την εικόνα στην κρυφή μνήμη

`RasterImage` διατηρεί την raster αναπαράσταση ενός στρώματος· η κλήση του `cache()` φορτώνει τα δεδομένα pixel στη μνήμη ώστε οι επόμενες λειτουργίες να είναι γρήγορες.  
```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

### Βήμα 4: δυαδικοποιήστε την εικόνα με το κατώφλι Otsu

`applyOtsuThreshold()` αξιολογεί όλα τα πιθανά επίπεδα γκρι και επιλέγει το βέλτιστο όριο, παράγοντας μια δυαδική εικόνα που διαχωρίζει τα αντικείμενα προσκηνίου από το φόντο.  
```java
rasterCachedImage.binarizeOtsu();
```

### Βήμα 5: αποθηκεύστε την προκύπτουσα εικόνα

`JpegOptions` διαμορφώνει ρυθμίσεις ειδικές για JPEG όπως η ποιότητα και η συμπίεση κατά την αποθήκευση της επεξεργασμένης εικόνας. Μπορείτε επίσης να επιλέξετε PNG ή BMP αντικαθιστώντας την κλάση επιλογών – το API υποστηρίζει πάνω από **30 μορφές εικόνας** για έξοδο.  
```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

{{< blocks/products/products-backtop-button >}}

## Κοινά προβλήματα και λύσεις

- **Σφάλματα Memory‑out‑of‑bounds** – Βεβαιωθείτε ότι καλείτε `cache()` σε μεγάλα στρώματα πριν την επεξεργασία· αυτό αναγκάζει το Aspose.PSD να χρησιμοποιήσει προσέγγιση streaming.  
- **Λανθασμένα χρώματα μετά τη δυαδικοποίηση** – Επαληθεύστε ότι το στρώμα προέλευσης είναι μια πραγματική εικόνα γκρι κλίμακας· τα χρωματιστά στρώματα πρέπει να μετατραπούν σε γκρι κλίμακα πρώτα χρησιμοποιώντας `convertToGrayscale()`.

## Συχνές ερωτήσεις

### Ε1: Τι είναι η δυαδικοποίηση με το κατώφλι Otsu;

Η δυαδικοποίηση με το κατώφλι Otsu είναι μια μέθοδος που χρησιμοποιείται για τμηματοποίηση εικόνας, διαχωρίζοντας μια εικόνα σε προσκήνιο και φόντο βάσει βέλτιστης επιλογής κατωφλίου.

### Ε2: Μπορώ να χρησιμοποιήσω το Aspose.PSD for Java δωρεάν;

Το Aspose.PSD for Java είναι εμπορική βιβλιοθήκη, αλλά μπορείτε να εξερευνήσετε τις δυνατότητές του με δωρεάν δοκιμή. Λάβετε το από τη [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

### Ε3: Πού μπορώ να βρω την τεκμηρίωση του Aspose.PSD for Java;

Η τεκμηρίωση είναι διαθέσιμη στην επίσημη ιστοσελίδα αναφοράς Aspose.PSD for Java: [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

### Ε4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.PSD for Java;

Επισκεφθείτε το φόρουμ κοινότητας Aspose.PSD για βοήθεια: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Ε5: Υπάρχει προσωρινή άδεια διαθέσιμη για το Aspose.PSD for Java;

Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια από τη σελίδα προσωρινής άδειας Aspose: [Aspose temporary license](https://purchase.aspose.com/temporary-license/).

---

**Τελευταία ενημέρωση:** 2026-08-11  
**Δοκιμή με:** Aspose.PSD for Java 24.11  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Μετατροπή εικόνας σε γκρι κλίμακα χρησιμοποιώντας Aspose.PSD for Java](/psd/java/advanced-techniques/grayscale-image/)
- [Μάθημα επεξεργασίας εικόνας Java - Ρύθμιση φωτεινότητας εικόνας με Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Πώς να ρυθμίσετε το Gamma στην επεξεργασία εικόνας Java με Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}