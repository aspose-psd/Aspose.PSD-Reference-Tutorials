---
date: 2026-06-13
description: Μάθετε πώς να αλλάζετε το μέγεθος εικόνας σε Java χρησιμοποιώντας μια
  βιβλιοθήκη Java για επεξεργασία εικόνας. Ακολουθήστε τον βήμα‑βήμα οδηγό μας με
  Aspose.PSD for Java για αποδοτική επεξεργασία εικόνας.
keywords:
- java image manipulation library
- how to resize image java
- change image dimensions java
linktitle: Εκτελέστε Απλή Αλλαγή Μεγέθους
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  headline: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  type: TechArticle
- description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  name: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  steps:
  - name: Set Your Document Directory
    text: Define the folder that contains the source PSD file. Replace the placeholder
      with your actual path.
  - name: Specify Source and Destination Paths
    text: Create full file names for the input PSD and the output JPEG.
  - name: Load the Image
    text: '`Image.load(path)` reads an image file from the given path and returns
      an `Image` instance. Load the PSD into an `Image` object.'
  - name: Resize the Image
    text: '`image.resize(width, height)` changes the image dimensions to the specified
      pixel size. Resize to the desired dimensions (e.g., 300 × 300 pixels).'
  - name: Save the Resized Image
    text: '`image.save(path, options)` writes the image to the specified file using
      the given format options. Export the resized bitmap as a JPEG file. > **Pro
      tip:** Experiment with different width/height values or maintain the aspect
      ratio by calculating one dimension from the other.'
  type: HowTo
- questions:
  - answer: Absolutely. The `resize(width, height)` method lets you define any pixel
      size you need.
    question: Can I resize images to specific dimensions using Aspose.PSD for Java?
  - answer: Yes. Besides PSD, the library supports JPEG, PNG, BMP, TIFF, and many
      more.
    question: Is Aspose.PSD for Java compatible with different image formats?
  - answer: Refer to the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for a full API reference.
    question: Where can I find additional documentation for Aspose.PSD for Java?
  - answer: Certainly! Download the [free trial version](https://releases.aspose.com/)
      to explore all features.
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to ask
      questions and share experiences with the community.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Απλή Αλλαγή Μεγέθους με Aspose.PSD – Βιβλιοθήκη Java για Επεξεργασία Εικόνας
url: /el/java/basic-image-operations/simple-resizing/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Απλή Αλλαγή Μεγέθους με το Aspose.PSD – Βιβλιοθήκη Επεξεργασίας Εικόνας Java

## Εισαγωγή

Αν είστε προγραμματιστής Java που αναζητά μια αξιόπιστη **java image manipulation library**, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε βήμα-βήμα το **how to resize image java** χρησιμοποιώντας το Aspose.PSD for Java – μια ισχυρή βιβλιοθήκη που κάνει την επεξεργασία εικόνας γρήγορη και απλή. Στο τέλος αυτού του οδηγού θα έχετε ένα σαφές, έτοιμο για παραγωγή παράδειγμα που μπορείτε να ενσωματώσετε σε οποιαδήποτε εφαρμογή Java.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη χρησιμοποιείται;** Aspose.PSD for Java, a leading java image manipulation library.  
- **Μπορώ να αλλάξω το μέγεθος οποιουδήποτε PSD;** Yes – the library supports PSD, JPEG, PNG, and more.  
- **Πώς να καθορίσετε το μέγεθος;** Call `image.resize(width, height)` with the desired pixel dimensions.  
- **Χρειάζομαι άδεια;** A free trial works for development; a license is required for production.  
- **Ποια έκδοση Java απαιτείται;** Java 8 or higher.

## Τι είναι μια Java Image Manipulation Library;

Μια **java image manipulation library** είναι ένα σύνολο Java API που σας επιτρέπει να επεξεργάζεστε προγραμματιστικά γραφικά raster—αλλαγή μεγέθους, περικοπή, μετατροπή μορφής και διαχείριση επιπέδων—χωρίς εξωτερικά εργαλεία. Το Aspose.PSD παρέχει αυτές τις δυνατότητες για PSD και πολλές άλλες μορφές, εκθέτοντας ένα καθαρό αντικειμενοστραφές API για προγραμματιστές.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για Απλή Αλλαγή Μεγέθους;

Το Aspose.PSD προσφέρει **performance‑optimized** αλγόριθμους που μπορούν να επεξεργαστούν αρχεία με 500+ επίπεδα σε κάτω από ένα δευτερόλεπτο σε τυπικό διακομιστή, και λειτουργεί εξ ολοκλήρου σε Java—χωρίς native DLLs ή εξωτερικά binaries. Η βιβλιοθήκη υποστηρίζει **30+ image formats** (συμπεριλαμβανομένων PSD, JPEG, PNG, TIFF, BMP, GIF) και μπορεί να διαχειριστεί αρχεία μεγαλύτερα από 200 MB χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, καθιστώντας την ιδανική για υψηλής απόδοσης pipelines στο server‑side.

## Προαπαιτούμενα

1. **Java Development Kit (JDK)** – κατεβάστε την πιο πρόσφατη έκδοση από το [Java website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – αποκτήστε τη βιβλιοθήκη από τη [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  

Η ύπαρξη αυτών εξασφαλίζει μια ομαλή ρύθμιση για το παράδειγμα αλλαγής μεγέθους.

## Εισαγωγή Πακέτων

Η κλάση `Image` και οι σχετικές επιλογές εξαγωγής απαιτούνται για τη φόρτωση και αποθήκευση αρχείων.

`Image` είναι η κύρια κλάση που αντιπροσωπεύει μια εικόνα που μπορεί να φορτωθεί, να επεξεργαστεί και να αποθηκευτεί.

`JpegOptions` καθορίζει τις ρυθμίσεις για την αποθήκευση μιας εικόνας σε μορφή JPEG.

Αυτές οι εισαγωγές σας δίνουν πρόσβαση στην βασική κλάση `Image` και στις επιλογές εξαγωγής JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Οδηγός Βήμα‑Βήμα

### Βήμα 1: Ορίστε τον Κατάλογο Εγγράφου σας

Ορίστε το φάκελο που περιέχει το αρχείο PSD προέλευσης. Αντικαταστήστε το placeholder με την πραγματική διαδρομή σας.

```java
String dataDir = "Your Document Directory";
```

### Βήμα 2: Καθορίστε τις Διαδρομές Πηγής και Προορισμού

Δημιουργήστε πλήρη ονόματα αρχείων για το εισερχόμενο PSD και το εξαγόμενο JPEG.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "SimpleResizing_out.jpg";
```

### Βήμα 3: Φορτώστε την Εικόνα

`Image.load(path)` διαβάζει ένα αρχείο εικόνας από τη δεδομένη διαδρομή και επιστρέφει ένα αντικείμενο `Image`.

Φορτώστε το PSD σε ένα αντικείμενο `Image`.

```java
Image image = Image.load(sourceFile);
```

### Βήμα 4: Αλλάξτε το Μέγεθος της Εικόνας

`image.resize(width, height)` αλλάζει τις διαστάσεις της εικόνας στο καθορισμένο μέγεθος σε εικονοστοιχεία.

Αλλάξτε το μέγεθος στις επιθυμητές διαστάσεις (π.χ., 300 × 300 pixel).

```java
image.resize(300, 300);
```

### Βήμα 5: Αποθηκεύστε την Αλλαγμένη Εικόνα

`image.save(path, options)` γράφει την εικόνα στο καθορισμένο αρχείο χρησιμοποιώντας τις δοσμένες επιλογές μορφής.

Εξάγετε το αλλαγμένο bitmap ως αρχείο JPEG.

```java
image.save(destName, new JpegOptions());
```

> **Pro tip:** Δοκιμάστε διαφορετικές τιμές πλάτους/ύψους ή διατηρήστε την αναλογία διαστάσεων υπολογίζοντας τη μία διάσταση από την άλλη.

## Πώς να Αλλάξετε τις Διαστάσεις Εικόνας Java;

Χρησιμοποιήστε τη μέθοδο `resize(width, height)` στο αντικείμενο `Image`, περνώντας τις ακριβείς τιμές εικονοστοιχείων που χρειάζεστε. Για παράδειγμα, `image.resize(800, 600)` θα παραγάγει έξοδο 800 × 600 pixel διατηρώντας το βάθος χρώματος και τα μεταδεδομένα. Αν θέλετε να διατηρήσετε την αρχική αναλογία διαστάσεων, υπολογίστε τη δεύτερη διάσταση βάσει της αρχικής αναλογίας πλάτους προς ύψος πριν καλέσετε το `resize`.

## Συνηθισμένα Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **`OutOfMemoryError`** | Πολύ μεγάλα αρχεία PSD μπορούν να υπερβούν τη μνήμη heap της JVM. | Αυξήστε το μέγεθος heap της JVM (`-Xmx2g`) ή επεξεργαστείτε τις εικόνες σε τμήματα. |
| **Unsupported format** | Προσπάθεια φόρτωσης αρχείου που δεν είναι PSD χωρίς τις κατάλληλες επιλογές. | Χρησιμοποιήστε την κατάλληλη υπερφόρτωση `Image.load` ή μετατρέψτε πρώτα το αρχείο. |
| **Distorted output** | Λανθασμένη αναλογία διαστάσεων. | Υπολογίστε το ύψος βάσει της αρχικής αναλογίας ή χρησιμοποιήστε `image.resizeProportionally`. |

## Συχνές Ερωτήσεις

**Q: Μπορώ να αλλάξω το μέγεθος των εικόνων σε συγκεκριμένες διαστάσεις χρησιμοποιώντας το Aspose.PSD for Java;**  
A: Απόλυτα. Η μέθοδος `resize(width, height)` σας επιτρέπει να ορίσετε οποιοδήποτε μέγεθος σε εικονοστοιχεία χρειάζεστε.

**Q: Είναι το Aspose.PSD for Java συμβατό με διαφορετικές μορφές εικόνας;**  
A: Ναι. Εκτός από PSD, η βιβλιοθήκη υποστηρίζει JPEG, PNG, BMP, TIFF και πολλές άλλες.

**Q: Πού μπορώ να βρω πρόσθετη τεκμηρίωση για το Aspose.PSD for Java;**  
A: Ανατρέξτε στην [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) για πλήρη αναφορά API.

**Q: Μπορώ να δοκιμάσω το Aspose.PSD for Java πριν την αγορά;**  
A: Φυσικά! Κατεβάστε τη [free trial version](https://releases.aspose.com/) για να εξερευνήσετε όλες τις δυνατότητες.

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.PSD for Java;**  
A: Επισκεφθείτε το [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) για να θέσετε ερωτήσεις και να μοιραστείτε εμπειρίες με την κοινότητα.

## Συμπέρασμα

Σε αυτό το tutorial δείξαμε πώς μια **java image manipulation library** όπως το Aspose.PSD κάνει τις εργασίες **how to resize image java** εύκολες. Ακολουθώντας τα σύντομα βήματα παραπάνω, μπορείτε να ενσωματώσετε την αλλαγή μεγέθους εικόνας σε οποιαδήποτε εφαρμογή Java, εξασφαλίζοντας γρήγορα, αξιόπιστα αποτελέσματα χωρίς εξωτερικά εργαλεία.

---

**Τελευταία Ενημέρωση:** 2026-06-13  
**Δοκιμή Με:** Aspose.PSD for Java 24.12 (latest)  
**Συγγραφέας:** Aspose

## Σχετικά Tutorials

- [Αλλαγή Μεγέθους Εικόνας Java - Χρήση της Εκατονομίας Resize Type στο Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Κλιμάκωση Εικόνας Υψηλής Ποιότητας με Bicubic Resampler στο Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Πώς να Μετατρέψετε PSD σε PNG και να Αλλάξετε το Μέγεθος Αναλογικά με το Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}