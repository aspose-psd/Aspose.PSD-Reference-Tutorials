---
title: Render Level Adjustment Layer σε αρχεία PSD - Java
linktitle: Render Level Adjustment Layer σε αρχεία PSD - Java
second_title: Aspose.PSD Java API
description: Μάθετε πώς να βελτιώνετε εύκολα την αντίθεση και τη ζωντάνια της εικόνας χρησιμοποιώντας το Aspose.PSD για Java. Master Levels Adjustment Layers με αυτόν τον οδηγό βήμα προς βήμα.
type: docs
weight: 17
url: /el/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---
## Εισαγωγή

Έχετε ανοίξει ποτέ ένα αρχείο PSD μόνο για να βρείτε την εικόνα χωρίς αντίθεση ή ζωντάνια; Μη φοβάστε, πολεμιστές επεξεργασίας εικόνας! Το Aspose.PSD για Java έρχεται στη διάσωση με τις πανίσχυρες δυνατότητες χειρισμού Επίπεδων Προσαρμογής Επιπέδων. Αυτός ο οδηγός θα σας εξοπλίσει με τις γνώσεις για να ρυθμίσετε τις εικόνες σας χρησιμοποιώντας Levels in a breeze. 

## Προαπαιτούμενα

- Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκαταστήσει μια πρόσφατη έκδοση του JDK στο σύστημά σας. Μπορείτε να το κατεβάσετε από τον ιστότοπο της Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD για Java Library: Κάντε λήψη της βιβλιοθήκης Aspose.PSD για Java από τη σελίδα λήψης ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Θα χρειαστείτε μια έγκυρη άδεια χρήσης για να χρησιμοποιήσετε τις πλήρεις δυνατότητες, αλλά είναι διαθέσιμη μια δωρεάν δοκιμή για να ξεκινήσετε ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Εισαγωγή πακέτων

Πριν βουτήξουμε στον κώδικα, πρέπει να εισαγάγουμε τις απαραίτητες κλάσεις Aspose.PSD για αλληλεπίδραση με αρχεία PSD. Εδώ είναι τι θα χρειαστείτε:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 Ο`com.aspose.psd` Το πακέτο παρέχει πρόσβαση σε λειτουργίες χειρισμού PSD, ενώ`com.aspose.psd.imaging.PngOptions` μας επιτρέπει να ορίσουμε επιλογές κατά την αποθήκευση της εικόνας ως PNG.

Τώρα, ας ξεκινήσουμε την περιπέτεια προσαρμογής των επιπέδων:

## Βήμα 1: Ρύθμιση Διαδρομών Αρχείων:

- Ορίστε μεταβλητές για τον κατάλογο εγγράφων σας (`dataDir`), όνομα αρχείου προέλευσης PSD (`sourceFileName`), στόχευση ονόματος αρχείου PSD μετά από τροποποίηση (`psdPathAfterChange`), και την τελική διαδρομή εξαγωγής PNG (`pngExportPath`). Εξετάστε το ενδεχόμενο να χρησιμοποιήσετε περιγραφικά ονόματα για να βελτιώσετε την αναγνωσιμότητα του κώδικα.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Βήμα 2: Φόρτωση της εικόνας PSD:

-  Χρησιμοποιήστε το`Image.load` μέθοδος για να ανοίξετε το αρχείο προέλευσης PSD και να το αποθηκεύσετε σε α`PsdImage`αντικείμενο (`im`). Το Aspose.PSD εντοπίζει αυτόματα τη μορφή αρχείου.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Βήμα 3: Επανάληψη μέσω επιπέδων:

- Πρέπει να βρούμε το Επίπεδο Προσαρμογής Επιπέδων στο PSD σας. Το Aspose παρέχει έναν βολικό τρόπο επανάληψης σε όλα τα επίπεδα χρησιμοποιώντας έναν βρόχο.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (κωδικός για έλεγχο για Επίπεδα θα προστεθεί εδώ)
}
```

## Βήμα 4: Προσδιορισμός του επιπέδου των επιπέδων:

- Μέσα στον βρόχο, ελέγξτε εάν το τρέχον στρώμα (`im.getLayers()[i]` ) είναι ένα παράδειγμα του`LevelsLayer` τάξη χρησιμοποιώντας το`instanceof` χειριστής. 
-  Εάν είναι, ρίξτε το στρώμα στο a`LevelsLayer` αντικείμενο για περαιτέρω χειρισμό.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (κωδικός για την προσαρμογή των επιπέδων θα προστεθεί εδώ)
   }
}
```
## Βήμα 5: Βελτιστοποίηση των επιπέδων (Συνέχεια):

-  Ρυθμίστε τα επίπεδα εξόδου χρησιμοποιώντας`setOutputShadowLevel` και`setOutputHighlightLevel` για να ελέγξετε το σκοτάδι και τη φωτεινότητα της εικόνας που προκύπτει. Αυτές οι τιμές καθορίζουν το εύρος των επιπέδων εισόδου που θα αντιστοιχιστούν στην περιοχή εξόδου.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Προσαρμογή επιπέδων εισόδου (0-255):
	   channel.setInputShadowLevel((short) 10); // Σκουρύνετε ελαφρώς τις σκιές
	   channel.setInputMidtoneLevel(2.0f);     // Αυξήστε τους μεσαίους τόνους
	   channel.setInputHighlightLevel((short) 230); // Μειώστε τις επισημάνσεις

	   // Προσαρμογή επιπέδων εξόδου (0-255):
	   channel.setOutputShadowLevel((short) 20); // Σκουραίνει περισσότερο τις σκιές
	   channel.setOutputHighlightLevel((short) 200); //Φωτίστε τις ανταύγειες
   }
}
```

## Βήμα 6: Αποθήκευση του τροποποιημένου PSD:

-  Χρησιμοποιήστε το`save` μέθοδος του`PsdImage` αντικείμενο για αποθήκευση της τροποποιημένης εικόνας στην καθορισμένη διαδρομή (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Βήμα 7: Εξαγωγή ως PNG (Προαιρετικό):

-  Εάν χρειάζεστε μια έκδοση PNG της προσαρμοσμένης εικόνας, δημιουργήστε ένα`PngOptions` αντικείμενο και ορίστε τον τύπο χρώματος σε`TruecolorWithAlpha` . Στη συνέχεια, χρησιμοποιήστε το`save` μέθοδος ξανά με τη διαδρομή εξαγωγής PNG και τις επιλογές.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Και ορίστε το! Προσαρμόσατε με επιτυχία το Επίπεδο Προσαρμογής Επιπέδων στο αρχείο PSD χρησιμοποιώντας το Aspose.PSD για Java. Κατανοώντας αυτά τα βήματα και πειραματιζόμενοι με διαφορετικές τιμές, μπορείτε να βελτιώσετε την αντίθεση και τη συνολική εμφάνιση των εικόνων σας.

## Σύναψη

Το Aspose.PSD για Java σάς δίνει τη δυνατότητα να αναλάβετε τον έλεγχο της διαδικασίας επεξεργασίας εικόνας. Κατακτώντας το Επίπεδο Προσαρμογής Επιπέδων, μπορείτε να δώσετε νέα πνοή στις φωτογραφίες και τα σχέδιά σας. Θυμηθείτε, η πρακτική κάνει τέλεια, γι' αυτό μη διστάσετε να πειραματιστείτε και να εξερευνήσετε όλες τις δυνατότητες αυτού του ισχυρού εργαλείου.
 
## Συχνές ερωτήσεις

### Μπορώ να προσαρμόσω ξεχωριστά μεμονωμένα κανάλια χρώματος (RGB); 
Ναι, μπορείτε να έχετε πρόσβαση σε κάθε κανάλι χρώματος χρησιμοποιώντας το`getChannel` μέθοδος του`LevelsLayer` αντικείμενο και να τροποποιήσει τα επίπεδά του ανεξάρτητα.

### Πώς μπορώ να χειριστώ πολλαπλά επίπεδα προσαρμογής επιπέδων σε ένα PSD;
Ο κώδικας επαναλαμβάνεται σε όλα τα επίπεδα, επομένως θα επεξεργαστεί αυτόματα τυχόν πρόσθετα επίπεδα Levels που βρίσκονται στην εικόνα.

### Υπάρχουν άλλοι τρόποι ρύθμισης της αντίθεσης της εικόνας εκτός από τα Επίπεδα;
Απολύτως! Το Aspose.PSD προσφέρει διάφορα εργαλεία προσαρμογής εικόνας όπως Curves, Brightness/Contrast και άλλα.

### Μπορώ να αυτοματοποιήσω αυτή τη διαδικασία για πολλές εικόνες; 
Ναι, μπορείτε να ενσωματώσετε αυτόν τον κώδικα σε ένα σενάριο επεξεργασίας βρόχου ή δέσμης για την αποτελεσματική επεξεργασία πολλών αρχείων PSD.

### Πού μπορώ να βρω περισσότερες πληροφορίες και υποστήριξη;
Η Aspose παρέχει εκτενή τεκμηρίωση ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) και ένα φόρουμ υποστήριξης ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) για τυχόν ερωτήσεις ή προβλήματα που μπορεί να αντιμετωπίσετε.