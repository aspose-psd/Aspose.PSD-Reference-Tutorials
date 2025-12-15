---
date: 2025-12-15
description: Μάθετε πώς να μετατρέπετε PSD σε PNG και να περιστρέφετε τα στρώματα
  PSD σε Java χρησιμοποιώντας το Aspose.PSD. Οδηγός βήμα‑προς‑βήμα με παραδείγματα
  κώδικα.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Μετατροπή PSD σε PNG και Περιστροφή Στρωμάτων σε Αρχεία PSD χρησιμοποιώντας
  Java
url: /el/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή PSD σε PNG και Περιστροφή Στρωμάτων σε Αρχεία PSD με Java

## Εισαγωγή
Αν χρειάζεστε **μετατροπή PSD σε PNG** ενώ ταυτόχρονα περιστρέφετε τα στρώματα, αυτός ο οδηγός είναι για εσάς. Είτε δημιουργείτε ένα εργαλείο μαζικής επεξεργασίας είτε ενσωματώνετε χειρισμό εικόνας σε μια web υπηρεσία, η προγραμματιστική προσέγγιση εξοικονομεί χρόνο και αφαιρεί την εξάρτηση από το Adobe Photoshop. Σε αυτό το tutorial θα σας δείξουμε **πώς να περιστρέψετε στρώματα PSD** και να εξάγετε το αποτέλεσμα ως PNG χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD για Java. Ας μπει κανείς στα χέρια και ας κάνουμε τη ροή εργασίας σχεδίασής σας πιο ομαλή!

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη μπορώ να χρησιμοποιήσω;** Aspose.PSD for Java  
- **Μπορώ να περιστρέψω και να μετατρέψω σε ένα βήμα;** Ναι – περιστρέψτε το PSD και αποθηκεύστε ως PNG  
- **Χρειάζεται άδεια;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται πληρωμένη άδεια για παραγωγή  
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 και μεταγενέστερες  
- **Το αρχείο PNG είναι διαφανές;** Ναι, όταν ορίζετε `PngColorType.TruecolorWithAlpha`

## Τι σημαίνει “μετατροπή PSD σε PNG”;
Η μετατροπή ενός εγγράφου Photoshop (PSD) σε εικόνα PNG σημαίνει εξαγωγή του οπτικού περιεχομένου—συμπεριλαμβανομένων όλων των στρωμάτων, μάσκων και διαφάνειας—σε μια ευρέως υποστηριζόμενη μορφή raster. Το PNG διατηρεί τα κανάλια άλφα, καθιστώντας το ιδανικό για γραφικά web, μικρογραφίες και περαιτέρω επεξεργασία εικόνας.

## Γιατί να χρησιμοποιήσετε Aspose.PSD for Java για μετατροπή PSD σε PNG και περιστροφή στρωμάτων PSD;
- **Δεν απαιτείται Photoshop** – λειτουργεί σε οποιονδήποτε διακομιστή ή περιβάλλον CI  
- **Πλήρης υποστήριξη στρωμάτων** – διατηρεί τη διαφάνεια και τα εφέ στρωμάτων ανέπαφα  
- **Απλό API** – περιστρέψτε, αναστρέψτε και αποθηκεύστε με λίγες κλήσεις μεθόδων  
- **Δια-πλατφόρμα** – τρέχει σε Windows, Linux και macOS  

## Προαπαιτούμενα
Πριν βουτήξουμε στον κώδικα, βεβαιωθείτε ότι έχετε τα εξής:

- **Java Development Kit (JDK)** – κατεβάστε το από την [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse ή NetBeans είναι όλα αποδεκτά.  
- **Aspose.PSD for Java library** – αποκτήστε το τελευταίο JAR από τη [release page](https://releases.aspose.com/psd/java/).  
- **Βασικές γνώσεις Java** – εξοικείωση με κλάσεις, αντικείμενα και διαχείριση εξαιρέσεων.

## Οδηγός Βήμα‑Βήμα

### Βήμα 1: Ρύθμιση του Java Project σας
Δημιουργήστε ένα νέο Java project στο IDE σας και προσθέστε το JAR του Aspose.PSD στο classpath του project.

### Βήμα 2: Εισαγωγή Απαιτούμενων Κλάσεων
Προσθέστε τις παρακάτω εισαγωγές στην αρχή του αρχείου πηγαίου κώδικα Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Αυτές οι κλάσεις σας δίνουν πρόσβαση στη φόρτωση εικόνας, περιστροφή και επιλογές PNG.

### Βήμα 3: Ορισμός Διαδρομών Αρχείων
Καθορίστε πού βρίσκεται το αρχικό PSD και πού πρέπει να γραφτούν τα αρχεία εξόδου.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Συμβουλή:** Χρησιμοποιήστε απόλυτη διαδρομή κατά τη δοκιμή για να αποφύγετε σφάλματα “file not found”.

### Βήμα 4: Φόρτωση του Αρχείου PSD
Φορτώστε το PSD σε ένα αντικείμενο που μπορεί να τροποποιηθεί.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Τώρα το `im` αντιπροσωπεύει ολόκληρο το έγγραφο Photoshop, συμπεριλαμβανομένων όλων των στρωμάτων.

### Βήμα 5: Περιστροφή της Εικόνας (Πώς να περιστρέψετε PSD)
Επιλέξτε τύπο περιστροφής από το `RotateFlipType`. Σε αυτό το παράδειγμα περιστρέφουμε 270° και αναστρέφουμε και τους δύο άξονες.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Μπορείτε να πειραματιστείτε με άλλες τιμές όπως `Rotate90FlipNone` ή `Rotate180FlipX`.

### Βήμα 6: Αποθήκευση της Περιστραμμένης Εικόνας ως PNG (μετατροπή PSD σε PNG)
Ρυθμίστε τις επιλογές PNG για να διατηρήσετε τη διαφάνεια, στη συνέχεια αποθηκεύστε.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Το παραγόμενο PNG διατηρεί τη διαφάνεια των στρωμάτων, καθιστώντας το έτοιμο για χρήση στο web.

### Βήμα 7: Αποθήκευση του Τροποποιημένου PSD (προαιρετικό)
Αν χρειάζεστε επίσης ένα νέο PSD με την εφαρμοσμένη περιστροφή, αποθηκεύστε το ξανά.

```java
im.save(psdPath);
```

Τώρα έχετε τόσο μια προεπισκόπηση PNG όσο και ένα ενημερωμένο αρχείο PSD.

## Συνηθισμένα Προβλήματα και Λύσεις
- **File not found:** Ελέγξτε ότι το `dataDir` λήγει με διαχωριστικό διαδρομής (`/` ή `\`).  
- **OutOfMemoryError σε μεγάλα PSD:** Αυξήστε το μέγεθος heap της JVM (`-Xmx2g`).  
- **Διαφάνεια χαμένη:** Βεβαιωθείτε ότι είναι ορισμένο `PngColorType.TruecolorWithAlpha`; διαφορετικά το PNG θα αποθηκευτεί χωρίς άλφα.

## Συχνές Ερωτήσεις
### Μπορώ να περιστρέψω ένα συγκεκριμένο στρώμα σε αρχείο PSD;
Ναι, μπορείτε να χρησιμοποιήσετε `Layer.rotateFlip()` σε μεμονωμένα στρώματα αφού κάνετε επανάληψη μέσω `im.getLayers()`.

### Υπάρχει περιορισμός απόδοσης με το Aspose.PSD for Java;
Η βιβλιοθήκη διαχειρίζεται τα περισσότερα αρχεία αποδοτικά, αλλά εξαιρετικά μεγάλα PSD (>500 MB) μπορεί να απαιτούν επιπλέον μνήμη.

### Είναι το Aspose.PSD δωρεάν;
Η Aspose προσφέρει δωρεάν δοκιμή, αλλά απαιτείται πληρωμένη άδεια για παραγωγή. Δείτε την [temporary license](https://purchase.aspose.com/temporary-license/) για δοκιμές.

### Πού μπορώ να βρω λεπτομερή τεκμηρίωση;
Μπορείτε να βρείτε εκτενή τεκμηρίωση στο [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

### Τι κάνω αν αντιμετωπίσω προβλήματα με το Aspose.PSD;
Ζητήστε βοήθεια μέσω του [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

## Επιπλέον Συχνές Ερωτήσεις

**Ε: Η μετατροπή PSD σε PNG διατηρεί τα εφέ στρωμάτων;**  
Α: Ναι, όταν αποθηκεύετε με `PngColorType.TruecolorWithAlpha`, τα περισσότερα οπτικά εφέ ραστεροποιούνται στο PNG.

**Ε: Μπορώ να επεξεργαστώ μαζικά πολλά αρχεία PSD;**  
Α: Απόλυτα. Τυλίξτε τον κώδικα σε βρόχο που διατρέχει έναν φάκελο με αρχεία PSD.

**Ε: Μπορώ να ορίσω επίπεδο συμπίεσης PNG;**  
Α: Η κλάση `PngOptions` παρέχει τη μέθοδο `setCompressionLevel(int)` για λεπτομερή ρύθμιση.

**Ε: Πρέπει να κλείσω το αντικείμενο εικόνας;**  
Α: Το `PsdImage` υλοποιεί το `Closeable`; καλέστε `im.close()` σε block `finally` ή χρησιμοποιήστε try‑with‑resources.

**Ε: Θα έχει το περιστραμμένο PNG τις ίδιες διαστάσεις με το αρχικό;**  
Α: Η περιστροφή κατά 90° ή 270° ανταλλάσσει το πλάτος και το ύψος. Το PNG θα αντανακλά τη νέα προσανατολισμό.

## Συμπέρασμα
Με τη χρήση του Aspose.PSD for Java, μπορείτε **να μετατρέψετε PSD σε PNG** και **να περιστρέψετε στρώματα PSD** με λίγες μόνο γραμμές κώδικα. Αυτή η προσέγγιση εξαλείφει την ανάγκη για Photoshop, επιταχύνει τις αυτοματοποιημένες ροές εργασίας και σας δίνει πλήρη έλεγχο πάνω στην έξοδο της εικόνας. Δοκιμάστε το στα δικά σας έργα και δείτε πόσο χρόνο εξοικονομείτε!

---

**Τελευταία ενημέρωση:** 2025-12-15  
**Δοκιμασμένο με:** Aspose.PSD for Java 24.11  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}