---
date: 2026-07-03
description: Μάθετε πώς να περικόψετε εικόνα Java χρησιμοποιώντας το Aspose.PSD για
  Java. Αυτός ο οδηγός περικοπής εικόνας βήμα‑βήμα καλύπτει τη φόρτωση αρχείων PSD,
  τον ορισμό τιμών μετατόπισης και την αποθήκευση του αποτελέσματος.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Περικοπή εικόνας με μετατοπίσεις
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Περικοπή εικόνας Java με μετατοπίσεις με Aspose.PSD
url: /el/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Κόψιμο Εικόνας Java με Μετατοπίσεις με Aspose.PSD

## Εισαγωγή

Στην επεξεργασία εικόνας με Java, το **crop image java** είναι μια κοινή απαίτηση για την προετοιμασία γραφικών, μικρογραφιών ή στοιχείων UI. Το Aspose.PSD για Java καθιστά αυτήν την εργασία απλή, εκθέτοντας μια απλή μέθοδο `crop` που λειτουργεί σε οποιαδήποτε υποστηριζόμενη μορφή raster. Σε αυτό το tutorial θα μάθετε πώς να φορτώσετε ένα αρχείο PSD, να ορίσετε τιμές μετατόπισης αριστερά‑δεξιά‑πάνω‑κάτω, να εφαρμόσετε το κόψιμο και να αποθηκεύσετε το αποτέλεσμα—όλα χωρίς να γράψετε κώδικα προσαρμοσμένης διαχείρισης pixel.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται το κόψιμο;** Το Aspose.PSD για Java παρέχει μια ενσωματωμένη μέθοδο `crop`.  
- **Χρειάζομαι άδεια;** Μια προσωρινή άδεια λειτουργεί για αξιολόγηση· απαιτείται πλήρης άδεια για παραγωγή.  
- **Υποστηριζόμενες μορφές;** Πάνω από 30 μορφές raster, συμπεριλαμβανομένων PSD, JPEG, PNG, BMP και TIFF.  
- **Μέγιστο μέγεθος αρχείου;** Διαχειρίζεται αρχεία έως 2 GB χωρίς να φορτώνει ολόκληρη την εικόνα στη μνήμη.  
- **Πόσες γραμμές κώδικα;** Μόνο πέντε λογικά βήματα—φόρτωση, cache, ορισμός μετατοπίσεων, κόψιμο και αποθήκευση.

## Τι είναι το crop image java;
`crop image java` αναφέρεται στη λειτουργία περικοπής ενός bitmap σε εφαρμογή Java. Χρησιμοποιώντας το Aspose.PSD, η λειτουργία εκτελείται από τη μέθοδο `crop`, η οποία δέχεται τιμές μετατόπισης για κάθε πλευρά της εικόνας και επιστρέφει ένα νέο αντικείμενο εικόνας.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για κόψιμο εικόνας;
Το Aspose.PSD υποστηρίζει **30+** μορφές εικόνας και μπορεί να επεξεργαστεί αρχεία PSD με εκατοντάδες σελίδες, χρησιμοποιώντας λιγότερο από 150 MB RAM, χάρη στην αρχιτεκτονική lazy‑loading. Η βιβλιοθήκη επίσης εγγυάται αποτελέσματα pixel‑perfect, διατηρώντας στρώματα, μάσκες και προφίλ χρώματος—κάτι που πολλές γενικές βιβλιοθήκες εικόνας δεν μπορούν να εγγυηθούν.

## Προαπαιτούμενα

### Java Development Kit (JDK)

Βεβαιωθείτε ότι έχετε εγκατεστημένη την πιο πρόσφατη έκδοση του JDK στο σύστημά σας. Μπορείτε να το κατεβάσετε από [εδώ](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Library

Για να ξεκινήσετε, θα χρειαστεί να αποκτήσετε τη βιβλιοθήκη Aspose.PSD for Java. Μεταβείτε στη [σελίδα λήψης](https://releases.aspose.com/psd/java/) και κατεβάστε την πιο πρόσφατη έκδοση.

### Integrated Development Environment (IDE)

Επιλέξτε το αγαπημένο σας Java IDE, όπως Eclipse ή IntelliJ, για μια ομαλή εμπειρία προγραμματισμού.

## Πώς να κόψετε εικόνα java;

Φορτώστε το αρχείο προέλευσης, ορίστε τις μετατοπίσεις pixel για κάθε πλευρά και καλέστε τη μέθοδο `crop`—όλη αυτή η ροή εργασίας μπορεί να γραφτεί σε πέντε σύντομες γραμμές κώδικα. Η λειτουργία `crop` δημιουργεί μια νέα εικόνα που περιέχει μόνο την περιοχή που καθορίσατε, αφήνοντας το αρχικό αρχείο αμετάβλητο.

### Βήμα 1: Φόρτωση της Εικόνας

`Image` είναι η βασική κλάση για όλους τους τύπους εικόνας στο Aspose.PSD.  
`RasterImage` αντιπροσωπεύει μια raster εικόνα και παρέχει δυνατότητες κόψιμου.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Βήμα 2: Cache Δεδομένων Εικόνας

`cacheData()` φορτώνει τα δεδομένα της εικόνας στη μνήμη για ταχύτερη επεξεργασία.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Βήμα 3: Ορισμός Τιμών Μετατόπισης

Καθορίστε τις τιμές μετατόπισης για όλες τις τέσσερις πλευρές της εικόνας (αριστερά, πάνω, δεξιά, κάτω) σε pixel.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Βήμα 4: Εφαρμογή Κοπής

`crop(left, right, top, bottom)` περικόπτει την εικόνα με τις καθορισμένες μετατοπίσεις pixel σε κάθε πλευρά.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Βήμα 5: Αποθήκευση Αποτελεσμάτων

`JpegOptions` ορίζει τις ρυθμίσεις κωδικοποίησης JPEG όπως η ποιότητα και το προφίλ χρώματος.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Συγχαρητήρια! Έχετε κόψει επιτυχώς μια εικόνα χρησιμοποιώντας το Aspose.PSD για Java.

## Συχνά Προβλήματα και Λύσεις

- **Η εικόνα φαίνεται αμετάβλητη:** Επαληθεύστε ότι οι τιμές μετατόπισης είναι θετικές και δεν υπερβαίνουν τις αρχικές διαστάσεις.  
- **OutOfMemoryError σε μεγάλα αρχεία:** Ενεργοποιήστε το caching όπως φαίνεται στο Βήμα 2· αυτό αναγκάζει το Aspose.PSD να χρησιμοποιήσει ένα προσωρινό αρχείο αντί να κρατά ολόκληρη την εικόνα στη RAM.  
- **Μετατόπιση χρώματος μετά το κόψιμο:** Βεβαιωθείτε ότι διατηρείτε το προφίλ χρώματος καλώντας `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` εάν χρειάζεστε ακριβή πιστότητα χρώματος.

## Συχνές Ερωτήσεις

**Q: Είναι το Aspose.PSD συμβατό με όλες τις μορφές εικόνας;**  
A: Ναι, το Aspose.PSD υποστηρίζει πάνω από 30 μορφές raster, συμπεριλαμβανομένων PSD, JPEG, PNG, BMP, TIFF και GIF, εξασφαλίζοντας ευρεία συμβατότητα.

**Q: Μπορώ να εφαρμόσω πολλαπλές λειτουργίες κόψιμου στην ίδια εικόνα;**  
A: Απόλυτα. Μετά από κάθε κλήση `crop` λαμβάνετε ένα νέο αντικείμενο εικόνας, το οποίο μπορείτε να κόψετε ξανά όπως χρειάζεται.

**Q: Υπάρχει φόρουμ κοινότητας για υποστήριξη Aspose.PSD;**  
A: Ναι, μπορείτε να βρείτε υποστήριξη και να συμμετέχετε στην κοινότητα στο [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.PSD;**  
A: Επισκεφθείτε [εδώ](https://purchase.aspose.com/temporary-license/) για να αποκτήσετε μια προσωρινή άδεια.

**Q: Υπάρχουν δείγματα έργων που παρουσιάζουν τις λειτουργίες του Aspose.PSD;**  
A: Εξερευνήστε την τεκμηρίωση και τα παραδείγματα στο [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Τελευταία Ενημέρωση:** 2026-07-03  
**Δοκιμάστηκε Με:** Aspose.PSD 24.11 for Java  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Σχετικά Μαθήματα

- [Κόψιμο Εικόνας με Ορθογώνιο στο Aspose.PSD για Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - Επέκταση και Κόψιμο Εικόνων με Aspose.PSD για Java](/psd/java/image-editing/expand-and-crop-images/)
- [Resize Image Java - Χρήση της Καταμέτρησης Resize Type Enumeration στο Aspose.PSD για Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}