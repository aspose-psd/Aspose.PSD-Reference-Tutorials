---
date: 2026-04-08
description: Μάθετε πώς να εξάγετε PSD σε PNG και να δημιουργήσετε ένα νέο στρώμα
  PSD με το Aspose.PSD για Java χρησιμοποιώντας προσωρινή άδεια Aspose. Αυτός ο οδηγός
  βήμα‑βήμα καλύπτει την επεξεργασία εικόνας PSD και τον ορισμό θέσης στρώματος.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Προσθήκη νέου κανονικού στρώματος στο PSD
second_title: Aspose.PSD Java API
title: Εξαγωγή PSD σε PNG & Προσθήκη νέου κανονικού στρώματος χρησιμοποιώντας το Aspose.PSD
  για Java – προσωρινή άδεια Aspose
url: /el/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή PSD σε PNG & Προσθήκη Νέας Κανονικής Στρώσης χρησιμοποιώντας το Aspose.PSD για Java

## Εισαγωγή

Σε αυτό το **aspose psd tutorial** θα ανακαλύψετε πώς να **export PSD to PNG** ενώ ταυτόχρονα **creating a new regular layer** μέσα στο ίδιο αρχείο, **using an aspose temporary license** για ανάπτυξη. Είτε χρειάζεστε να δημιουργήσετε μικρογραφίες έτοιμες για web, να προετοιμάσετε πόρους για μια γραμμή σχεδίασης, ή απλώς να πειραματιστείτε με **psd image manipulation**, το Aspose.PSD for Java σας δίνει πλήρη προγραμματιστικό έλεγχο. Θα περάσουμε βήμα‑βήμα από τη φόρτωση του αρχικού αρχείου μέχρι την αποθήκευση τόσο του ενημερωμένου PSD όσο και ενός αντιγράφου PNG — ώστε να μπορείτε να αρχίσετε να διαχειρίζεστε στρώσεις PSD αμέσως.

## Γρήγορες Απαντήσεις
- **Μπορώ να εξάγω PSD σε PNG με μία κλήση;** Ναι, μετά την προσθήκη των στρωμάτων μπορείτε να καλέσετε `save` με `PngOptions`.
- **Χρειάζεται άδεια για ανάπτυξη;** Μια προσωρινή άδεια λειτουργεί για δοκιμές· απαιτείται πλήρης άδεια για παραγωγή.
- **Ποια έκδοση Java υποστηρίζεται;** Το Aspose.PSD λειτουργεί με Java 8 και νεότερες.
- **Η τοποθέτηση στρώματος είναι pixel‑based;** Ναι, ορίζετε τις συντεταγμένες left, top, right, bottom σε pixel χρησιμοποιώντας τις μεθόδους **set layer position**.
- **Θα διατηρήσει το PNG τη διαφάνεια των στρωμάτων;** Το PNG θα περιέχει το συγχωνευμένο αποτέλεσμα όλων των ορατών στρωμάτων.

## Γιατί να χρησιμοποιήσετε μια aspose temporary license;

Μια **aspose temporary license** σας επιτρέπει να αξιολογήσετε το πλήρες σύνολο λειτουργιών του Aspose.PSD χωρίς περιορισμούς λειτουργικότητας. Αφαιρεί το υδατογράφημα αξιολόγησης, ξεκλειδώνει όλα τα API — συμπεριλαμβανομένης της δυνατότητας **create new psd layer** — και σας επιτρέπει να δοκιμάσετε τον κώδικά σας σε περιβάλλον παρόμοιο με την παραγωγή πριν αγοράσετε μόνιμη άδεια.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Java Development Environment** – JDK 8+ και ένα εργαλείο κατασκευής (Maven/Gradle) εγκατεστημένο.
- **Aspose.PSD for Java** – Κατεβάστε το τελευταίο JAR από την επίσημη ιστοσελίδα [here](https://releases.aspose.com/psd/java/).
- **Ένα δείγμα αρχείου PSD** – Θα χρησιμοποιήσουμε το `OneLayer.psd` στα παραδείγματα.

## Εισαγωγή Πακέτων

Προσθέστε τις απαιτούμενες εισαγωγές στην κλάση Java. Αυτές οι κλάσεις παρέχουν τη βασική λειτουργικότητα για **psd image manipulation** και διαχείριση στρωμάτων.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Τι είναι το “set layer position” και γιατί είναι σημαντικό;

Όταν προσθέτετε ένα νέο στρώμα, πρέπει να ορίσετε πού θα εμφανιστεί στον καμβά. Οι μέθοδοι `setLeft`, `setTop`, `setRight` και `setBottom` **set layer position** σε συντεταγμένες pixel. Η σωστή τοποθέτηση εξασφαλίζει ότι τα γραφικά σας ευθυγραμμίζονται ακριβώς όπως το επιθυμείτε, κάτι κρίσιμο για εργασίες όπως η σύνθεση UI πόρων ή η προετοιμασία αρχείων έτοιμων για εκτύπωση.

## Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση του Αρχείου PSD

Πρώτα, φορτώστε το υπάρχον PSD που θέλετε να τροποποιήσετε. Αυτό σας δίνει ένα αντικείμενο `PsdImage` με το οποίο μπορείτε να εργαστείτε.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Βήμα 2: Προετοιμασία Δεδομένων Pixel και Ορθογωνίων

Θα δημιουργήσουμε δύο buffers pixel (`int[]`) και θα ορίσουμε τις περιοχές ορθογωνίων όπου θα ζωγραφιστούν τα νέα στρώματα. Αυτό αποτελεί τη βάση για **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Βήμα 3: Αρχικοποίηση Δεδομένων Στρώματος

Γεμίστε τα buffers pixel με μια προεπιλεγμένη τιμή ARGB. Η τιμή `-10000000` αντιστοιχεί σε ένα ημιδιαφανές σκούρο χρώμα.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Βήμα 4: Προσθήκη Κανονικών Στωμάτων (Manipulate PSD Layers)

Τώρα **add regular layers** στην εικόνα PSD και **set layer position** χρησιμοποιώντας τις ιδιότητες left, top, right και bottom. Αυτό δείχνει πώς να **manipulate PSD layers** προγραμματιστικά.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Βήμα 5: Εξαγωγή PSD σε PNG και Αποθήκευση του Ενημερωμένου PSD

Αφού τα στρώματα είναι στη θέση τους, αποθηκεύστε το τροποποιημένο έγγραφο. Πρώτα εξάγουμε το αποτέλεσμα σε PNG (το βήμα **export psd to png**), μετά αποθηκεύουμε το PSD με τα νέα στρώματα.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Αν χρειάζεστε μόνο το PNG, μπορείτε να παραλείψετε την κλήση `save` του PSD και να καλέσετε απευθείας `save` με `PngOptions`.

## Συχνά Προβλήματα & Επίλυση

| Συμπτωμα | Πιθανή Αιτία | Διόρθωση |
|----------|--------------|----------|
| Το PNG εμφανίζεται κενό | Τα στρώματα είναι αόρατα ή πλήρως διαφανή | Βεβαιωθείτε ότι ορίζετε τιμές pixel μη‑διαφανείς ή καλέστε `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Αναντιστοιχία μεταξύ του μεγέθους του ορθογωνίου και του μήκους του πίνακα pixel | Επαληθεύστε ότι `rect.width * rect.height == dataArray.length`. |
| LicenseException κατά την εκτέλεση | Δεν φορτώθηκε έγκυρη άδεια | Φορτώστε μια προσωρινή ή μόνιμη άδεια πριν καλέσετε οποιεσδήποτε μεθόδους API. |

## Συχνές Ερωτήσεις

**Ε: Είναι το Aspose.PSD συμβατό με Java 8;**  
Α: Ναι, το Aspose.PSD υποστηρίζει Java 8 και μεταγενέστερες εκδόσεις.

**Ε: Μπορώ να εφαρμόσω μετασχηματισμούς (περιστροφή, κλιμάκωση) στα προστιθέμενα στρώματα;**  
Α: Απολύτως! Η κλάση `Layer` παρέχει μεθόδους όπως `rotate`, `scale` και `translate` για πλήρη έλεγχο μετασχηματισμού.

**Ε: Πού μπορώ να βρω πρόσθετη τεκμηρίωση του Aspose.PSD;**  
Α: Λεπτομερή API docs είναι διαθέσιμα [here](https://reference.aspose.com/psd/java/).

**Ε: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.PSD;**  
Α: Επισκεφθείτε τη σελίδα προσωρινής άδειας [here](https://purchase.aspose.com/temporary-license/).

**Ε: Υπάρχουν φόρουμ κοινότητας για υποστήριξη του Aspose.PSD;**  
Α: Ναι, συμμετέχετε στις συζητήσεις στα φόρουμ Aspose [here](https://forum.aspose.com/c/psd/34).

## Συμπέρασμα

Τώρα έχετε μάθει πώς να **export PSD to PNG** ενώ **adding new regular layers** χρησιμοποιώντας το Aspose.PSD for Java, και έχετε δει πώς μια **aspose temporary license** σας επιτρέπει να δοκιμάσετε αυτή τη ροή εργασίας χωρίς περιορισμούς. Αυτό το tutorial παρουσιάζει βασικές δυνατότητες **psd image manipulation**: φόρτωση αρχείου, δημιουργία στρωμάτων, γεμίσματος pixel δεδομένων, και εξαγωγή της τελικής σύνθεσης. Μη διστάσετε να πειραματιστείτε με διαφορετικά μεγέθη ορθογωνίων, χρώματα pixel ή εφέ στρωμάτων για να προσαρμόσετε το αποτέλεσμα στις ανάγκες του έργου σας.

---

**Τελευταία ενημέρωση:** 2026-04-08  
**Δοκιμάστηκε με:** Aspose.PSD 24.11 for Java  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}