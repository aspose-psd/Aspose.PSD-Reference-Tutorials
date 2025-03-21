---
title: Περικοπή εικόνας κατά Rectangle στο Aspose.PSD για Java
linktitle: Περικοπή εικόνας κατά ορθογώνιο
second_title: Aspose.PSD Java API
description: Εξερευνήστε τις δυνατότητες απρόσκοπτης περικοπής εικόνας στην Java με το Aspose.PSD. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για να περικόψετε εικόνες χωρίς κόπο χρησιμοποιώντας το Aspose.PSD για Java.
weight: 15
url: /el/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Περικοπή εικόνας κατά Rectangle στο Aspose.PSD για Java

## Εισαγωγή

Στον κόσμο της ανάπτυξης Java, ο χειρισμός εικόνων είναι μια κοινή εργασία και το Aspose.PSD για Java παρέχει μια ισχυρή λύση για την επεξεργασία εικόνας. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία περικοπής μιας εικόνας από ένα ορθογώνιο χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθήστε τα παρακάτω βήματα για να το πετύχετε εύκολα.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Το Java Development Kit (JDK) είναι εγκατεστημένο στο μηχάνημά σας.
- Aspose.PSD για βιβλιοθήκη Java. Μπορείτε να το κατεβάσετε από το[δικτυακός τόπος](https://releases.aspose.com/psd/java/).

## Εισαγωγή πακέτων

Φροντίστε να συμπεριλάβετε τα απαραίτητα πακέτα στο έργο σας Java για να αξιοποιήσετε τις δυνατότητες του Aspose.PSD για Java. Προσθέστε τις ακόλουθες δηλώσεις εισαγωγής στην αρχή του αρχείου Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Τώρα, ας αναλύσουμε τη διαδικασία σε πολλά βήματα για να σας καθοδηγήσουμε στην περικοπή μιας εικόνας από ένα ορθογώνιο χρησιμοποιώντας το Aspose.PSD για Java.

## Βήμα 1: Ρυθμίστε τον Κατάλογο Εγγράφων σας

```java
String dataDir = "Your Document Directory";
```

 Αντικαθιστώ`"Your Document Directory"` με την πραγματική διαδρομή όπου βρίσκεται το αρχείο PSD σας.

## Βήμα 2: Καθορίστε τα αρχεία προέλευσης και προορισμού

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Καθορίστε τις διαδρομές για το αρχείο PSD προέλευσης και το αρχείο JPEG προορισμού.

## Βήμα 3: Φόρτωση και προσωρινή αποθήκευση της εικόνας

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Φορτώστε την εικόνα PSD σε ένα`RasterImage` παράδειγμα και κρυφή αποθήκευση των δεδομένων του.

## Βήμα 4: Δημιουργήστε και ορίστε το ορθογώνιο περικοπής

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Δημιουργήστε ένα παράδειγμα του`Rectangle` τάξη με το επιθυμητό μέγεθος για καλλιέργεια.

## Βήμα 5: Περικοπή και αποθήκευση της εικόνας

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Εκτελέστε τη λειτουργία περικοπής χρησιμοποιώντας το καθορισμένο ορθογώνιο και αποθηκεύστε τα αποτελέσματα ως αρχείο JPEG.

Επαναλάβετε αυτά τα βήματα όπως χρειάζεται, προσαρμόζοντας τις παραμέτρους σύμφωνα με τις συγκεκριμένες απαιτήσεις σας.

## Σύναψη

Σε αυτό το σεμινάριο, ακολουθήσαμε τη διαδικασία περικοπής μιας εικόνας από ένα ορθογώνιο χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθώντας αυτά τα βήματα, μπορείτε εύκολα να ενσωματώσετε ισχυρές δυνατότητες χειρισμού εικόνας στις εφαρμογές σας Java.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.PSD για Java με άλλα πλαίσια Java;

A1: Ναι, το Aspose.PSD για Java μπορεί να ενσωματωθεί με διάφορα πλαίσια Java, παρέχοντας ευελιξία στα αναπτυξιακά σας έργα.

### Ε2: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.PSD για Java;

 A2: Ναι, μπορείτε να έχετε πρόσβαση στη δωρεάν δοκιμαστική έκδοση[εδώ](https://releases.aspose.com/).

### Ε3: Πού μπορώ να βρω πρόσθετη υποστήριξη ή βοήθεια;

 A3: Επισκεφθείτε το[Φόρουμ Aspose.PSD](https://forum.aspose.com/c/psd/34) για κοινοτική υποστήριξη και συζητήσεις.

### Ε4: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια χρήσης για το Aspose.PSD για Java;

 A4: Μπορείτε να αποκτήσετε μια προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Ποιες είναι οι υποστηριζόμενες μορφές εικόνας για περικοπή στο Aspose.PSD για Java;

A5: Το Aspose.PSD για Java υποστηρίζει διάφορες μορφές εικόνας, όπως PSD, PNG, JPEG και άλλα.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
