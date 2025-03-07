---
title: Προσαρμόστε το γάμμα μιας εικόνας με το Aspose.PSD για Java
linktitle: Προσαρμόστε το γάμμα μιας εικόνας
second_title: Aspose.PSD Java API
description: Μάθετε να προσαρμόζετε το γάμμα εικόνων χωρίς κόπο χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για βέλτιστα αποτελέσματα.
weight: 23
url: /el/java/advanced-techniques/adjust-gamma/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσαρμόστε το γάμμα μιας εικόνας με το Aspose.PSD για Java

## Εισαγωγή

Στον τομέα της επεξεργασίας εικόνας, η προσαρμογή του γάμμα μιας εικόνας είναι ένα κρίσιμο βήμα για την ενίσχυση της οπτικής της ελκυστικότητας. Το Aspose.PSD για Java προσφέρει μια ισχυρή λύση για προγραμματιστές Java για τον αβίαστο χειρισμό του γάμμα εικόνων. Σε αυτό το σεμινάριο, θα εξερευνήσουμε πώς να προσαρμόζουμε το γάμμα χρησιμοποιώντας το Aspose.PSD, αναλύοντας κάθε βήμα για να διασφαλίσουμε μια απρόσκοπτη υλοποίηση.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε ρυθμίσει τις ακόλουθες προϋποθέσεις:

1. Περιβάλλον ανάπτυξης Java: Βεβαιωθείτε ότι έχετε εγκαταστήσει ένα περιβάλλον ανάπτυξης Java στο σύστημά σας.
2.  Aspose.PSD Library: Κατεβάστε και ενσωματώστε τη βιβλιοθήκη Aspose.PSD στο έργο σας Java. Μπορείτε να βρείτε τους απαραίτητους πόρους στο[απόδειξη με έγγραφα](https://reference.aspose.com/psd/java/).
3. Δείγμα εικόνας: Προετοιμάστε ένα δείγμα εικόνας PSD που θα χρησιμοποιήσετε για να εφαρμόσετε τη ρύθμιση γάμμα.

## Εισαγωγή πακέτων

Για να ξεκινήσετε τη διαδικασία, εισαγάγετε τα απαιτούμενα πακέτα στο έργο σας Java. Αυτό θέτει τη βάση για την απρόσκοπτη χρήση των λειτουργιών Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Βήμα 1: Φορτώστε την εικόνα

 Ξεκινήστε φορτώνοντας το δείγμα εικόνας PSD σε μια παρουσία του`RasterImage` τάξη. Αυτό είναι το θεμέλιο για τις επόμενες προσαρμογές γάμμα.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Φορτώστε μια υπάρχουσα εικόνα σε μια παρουσία της κλάσης RasterImage
Image image = Image.load(sourceFile);

// Μεταφορά αντικειμένου εικόνας στο RasterImage
RasterImage rasterImage = (RasterImage)image;

// Ελέγξτε εάν το RasterImage είναι αποθηκευμένο στην κρυφή μνήμη για καλύτερη απόδοση
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Βήμα 2: Προσαρμογή Gamma

 Τώρα, προσαρμόστε το γάμμα της φορτωμένης εικόνας χρησιμοποιώντας το`adjustGamma` μέθοδος. Ρυθμίστε τις τιμές γάμμα σύμφωνα με τις απαιτήσεις σας.

```java
// Ρυθμίστε το γάμμα
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Βήμα 3: Δημιουργήστε TiffOptions

 Δημιουργήστε ένα παράδειγμα του`TiffOptions` για την εικόνα που προκύπτει. Ορίστε διάφορες ιδιότητες, όπως bit ανά δείγμα και φωτομετρικές επιλογές, για να προσαρμόσετε την έξοδο στις προδιαγραφές σας.

```java
// Δημιουργήστε μια παρουσία του TiffOptions για την εικόνα που προκύπτει
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Βήμα 4: Αποθηκεύστε την εικόνα που προκύπτει

 Αποθηκεύστε τη χειραγωγημένη εικόνα σε μορφή TIFF χρησιμοποιώντας την προηγουμένως καθορισμένη`TiffOptions`.

```java
// Αποθηκεύστε την εικόνα που προκύπτει σε μορφή TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Σύναψη

Συγχαρητήρια! Προσαρμόσατε με επιτυχία το γάμμα μιας εικόνας χρησιμοποιώντας το Aspose.PSD για Java. Αυτή η διαδικασία δίνει τη δυνατότητα στους προγραμματιστές να βελτιώνουν την ποιότητα της εικόνας χωρίς κόπο, συμβάλλοντας σε μια οπτικά ελκυστική εμπειρία χρήστη.

## Συχνές ερωτήσεις

### Ε1: Πού μπορώ να βρω την τεκμηρίωση του Aspose.PSD;

 A1: Μπορείτε να αποκτήσετε πρόσβαση στην τεκμηρίωση στη διεύθυνση[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Ε2: Πώς μπορώ να κατεβάσω το Aspose.PSD για Java;

 A2: Κάντε λήψη της βιβλιοθήκης από[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Ε3: Πού μπορώ να αγοράσω το Aspose.PSD;

 Α3: Επίσκεψη[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) για να αγοράσετε το Aspose.PSD.

### Ε4: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

 A4: Ναι, μπορείτε να εξερευνήσετε μια δωρεάν δοκιμή στο[https://releases.aspose.com/](https://releases.aspose.com/).

### Ε5: Πού μπορώ να αναζητήσω υποστήριξη για το Aspose.PSD;

 A5: Για υποστήριξη, επισκεφτείτε το φόρουμ Aspose.PSD στη διεύθυνση[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
