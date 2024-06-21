---
title: Προσαρμόστε την αντίθεση μιας εικόνας με το Aspose.PSD για Java
linktitle: Προσαρμόστε την αντίθεση μιας εικόνας
second_title: Aspose.PSD Java API
description: Εξερευνήστε τον κόσμο της ρύθμισης αντίθεσης εικόνας σε Java με το Aspose.PSD. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για απρόσκοπτη επεξεργασία εικόνας.
type: docs
weight: 22
url: /el/java/advanced-techniques/adjust-contrast/
---
## Εισαγωγή

Στον τομέα της επεξεργασίας εικόνας με Java, το Aspose.PSD ξεχωρίζει ως ένα ισχυρό εργαλείο. Μεταξύ των μυριάδων χαρακτηριστικών του, η προσαρμογή της αντίθεσης της εικόνας είναι μια κοινή απαίτηση. Αυτό το σεμινάριο θα σας καθοδηγήσει στη διαδικασία προσαρμογής της αντίθεσης εικόνας χρησιμοποιώντας το Aspose.PSD για Java. Είτε είστε έμπειρος προγραμματιστής είτε μόλις ξεκινάτε, αυτός ο οδηγός θα σας βοηθήσει να κατακτήσετε αυτή τη βασική πτυχή της χειραγώγησης εικόνας.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Βασική κατανόηση προγραμματισμού Java.
-  Εγκαταστάθηκε το Aspose.PSD για τη βιβλιοθήκη Java. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/psd/java/).

## Εισαγωγή πακέτων

Για να ξεκινήσετε, πρέπει να εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java. Προσθέστε τις ακόλουθες γραμμές στον κώδικά σας:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Βήμα 1: Φορτώστε την εικόνα

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Φορτώστε μια υπάρχουσα εικόνα σε μια παρουσία της κλάσης RasterImage
Image image = Image.load(sourceFile);
```

 Σε αυτό το βήμα, φορτώνουμε το δείγμα εικόνας ("sample.psd") χρησιμοποιώντας το`Image.load` μέθοδος.

## Βήμα 2: Μετάδοση σε RasterImage και Cache Data

```java
// Μεταφορά αντικειμένου εικόνας στο RasterImage
RasterImage rasterImage = (RasterImage)image;

// Ελέγξτε εάν το RasterImage είναι αποθηκευμένο στην κρυφή μνήμη και το Cache RasterImage για καλύτερη απόδοση
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Εδώ, ρίχνουμε το γενικό`Image` αντίρρηση σε α`RasterImage` για συγκεκριμένη επεξεργασία. Η προσωρινή αποθήκευση των δεδομένων εικόνας βελτιώνει την απόδοση.

## Βήμα 3: Προσαρμόστε την αντίθεση

```java
// Ρυθμίστε την αντίθεση
rasterImage.adjustContrast(50);
```

 ο`adjustContrast`μέθοδος χρησιμοποιείται για την τροποποίηση της αντίθεσης της εικόνας. Σε αυτό το παράδειγμα, η αντίθεση αυξάνεται κατά 50%.

## Βήμα 4: Δημιουργήστε TiffOptions και αποθηκεύστε

```java
// Δημιουργήστε μια παρουσία του TiffOptions για την εικόνα που προκύπτει
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Αποθηκεύστε την εικόνα που προκύπτει σε μορφή TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Εδώ, στήσαμε`TiffOptions` για την εικόνα εξόδου, προσδιορίζοντας τη μορφή και άλλες ιδιότητες. Στη συνέχεια, η τελική εικόνα αποθηκεύεται σε ένα αρχείο TIFF.

## συμπέρασμα

Συγχαρητήρια! Προσαρμόσατε με επιτυχία την αντίθεση μιας εικόνας χρησιμοποιώντας το Aspose.PSD για Java. Αυτό το σεμινάριο κάλυψε τα βασικά βήματα, από την εισαγωγή πακέτων έως την αποθήκευση της επεξεργασμένης εικόνας.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.PSD συμβατό με διαφορετικές μορφές εικόνας;

A1: Ναι, το Aspose.PSD υποστηρίζει διάφορες μορφές εικόνας, παρέχοντας ευελιξία στα έργα σας.

### Ε2: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια για το Aspose.PSD;

 A2: Μπορείτε να πάρετε μια προσωρινή άδεια.[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε3: Πού μπορώ να βρω την τεκμηρίωση του Aspose.PSD;

A3: Η τεκμηρίωση είναι διαθέσιμη.[εδώ](https://reference.aspose.com/psd/java/).

### Ε4: Ποιες επιλογές υποστήριξης είναι διαθέσιμες για το Aspose.PSD;

 A4: Για υποστήριξη, επισκεφθείτε το[Φόρουμ Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Ε5: Μπορώ να αγοράσω Aspose.PSD;

 A5: Ναι, μπορείτε να αγοράσετε Aspose.PSD[εδώ](https://purchase.aspose.com/buy).