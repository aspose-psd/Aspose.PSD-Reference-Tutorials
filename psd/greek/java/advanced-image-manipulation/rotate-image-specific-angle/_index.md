---
date: 2026-05-19
description: Μάθετε πώς να περιστρέψετε εικόνα σε συγκεκριμένη γωνία σε Java χρησιμοποιώντας
  το Aspose.PSD. Ο οδηγός καλύπτει rotate image java, rotate image specific angle,
  διαχείριση φόντου και άλλα.
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: Πώς να περιστρέψετε εικόνα σε συγκεκριμένη γωνία
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Πώς να περιστρέψετε εικόνα σε συγκεκριμένη γωνία με το Aspose.PSD για Java
url: /el/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Περιστρέψετε Εικόνα σε Συγκεκριμένη Γωνία με Aspose.PSD για Java

Αν χρειάζεστε **πώς να περιστρέψετε εικόνα** προγραμματιστικά σε μια εφαρμογή Java, το Aspose.PSD για Java προσφέρει ένα καθαρό, υψηλής απόδοσης API που αναλαμβάνει το βαρέως φορτίου κομμάτι. Είτε δημιουργείτε έναν επεξεργαστή φωτογραφιών, παράγετε μικρογραφίες, είτε προετοιμάζετε περιουσιακά στοιχεία για μια web υπηρεσία, η περιστροφή μιας εικόνας κατά ακριβή μοίρες είναι συχνή απαίτηση. Σε αυτό το tutorial θα περάσουμε από τη διαδικασία φόρτωσης ενός αρχείου PSD μέχρι την αποθήκευση του περιστραμμένου αποτελέσματος, επισημαίνοντας βέλτιστες πρακτικές όπως η προσωρινή αποθήκευση (caching) και η διαχείριση στο παρασκήνιο.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη είναι η καλύτερη για περιστροφή εικόνων σε Java;** Το Aspose.PSD για Java παρέχει τη πιο αξιόπιστη μηχανή περιστροφής.  
- **Μπορώ να περιστρέψω κατά οποιαδήποτε μοίρα;** Ναι, η μέθοδος `rotate` δέχεται μια γωνία τύπου `float`, θετική ή αρνητική.  
- **Χρειάζεται άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιοι τύποι εικόνας υποστηρίζονται;** PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF και 30+ επιπλέον μορφές.  
- **Πώς ορίζω χρώμα φόντου για κενό χώρο;** Περνάτε μια παρουσία `Color` στη μέθοδο `rotate`.

## Πώς να Περιστρέψετε Εικόνα σε Συγκεκριμένη Γωνία με Aspose.PSD για Java;

Φορτώστε το αρχείο προέλευσης, καλέστε `image.rotate(angle, true, backgroundColor)`, και στη συνέχεια αποθηκεύστε—τρεις σύντομες βήματα που διαχειρίζονται όλη τη βαριά μαθηματική λογική για εσάς. Το Aspose.PSD διατηρεί τα επίπεδα, τα προφίλ χρώματος και τα κανάλια άλφα ενώ επεκτείνει τον καμβά για να αποφύγει το κόψιμο, έτσι ώστε το αποτέλεσμα να φαίνεται ακριβώς όπως αναμένεται ακόμη και για κλασματικές γωνίες όπως 12,5°. Αυτή η προσέγγιση λειτουργεί για αρχεία από λίγα kilobytes μέχρι πολυ-εκατοντάδες σελίδες PSD χωρίς εξάντληση μνήμης.

## Τι είναι η Περιστροφή Εικόνας σε Java;

Η περιστροφή εικόνας είναι η γεωμετρική μετασχηματισμός που περιστρέφει έναν πίνακα pixel γύρω από ένα σημείο άξονα—συνήθως το κέντρο της εικόνας—κατά μια καθορισμένη γωνία. Σε απλή Java θα χειριζόσασταν ένα αντικείμενο `Graphics2D`, θα υπολογίζατε τριγωνομετρικές μετατοπίσεις και θα διαχειριζόσασταν το φόντο χειροκίνητα. Το Aspose.PSD αφαιρεί όλη αυτή τη πολυπλοκότητα, διαχειριζόμενο αυτόματα βάθος χρώματος, μάσκες επιπέδων και διαφορετικές μορφές αρχείων.

## Γιατί να Χρησιμοποιήσετε το Aspose.PSD για Περιστροφή Εικόνων;

Το Aspose.PSD υποστηρίζει **30+ μορφές εισόδου και εξόδου** και μπορεί να επεξεργαστεί **αρχεία PSD 500‑σελίδων σε λιγότερο από 5 δευτερόλεπτα** σε τυπική CPU server‑class. Η ενσωματωμένη προσωρινή αποθήκευση (`image.cacheData()`) μειώνει τη χρήση μνήμης έως και 60 % για μεγάλα περιουσιακά στοιχεία, και η μέθοδος `rotate` σας επιτρέπει να ορίσετε χρώμα φόντου, διατηρώντας διαφανείς γωνίες όταν χρειάζεται. Αυτά τα ποσοτικά οφέλη την καθιστούν την βιομηχανική επιλογή για υψηλής απόδοσης pipelines επεξεργασίας εικόνας.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

1. **Java Development Kit (JDK 8 ή νεότερο)** – οποιοδήποτε IDE ή περιβάλλον γραμμής εντολών αρκεί.  
2. **Aspose.PSD για Java** – κατεβάστε το τελευταίο JAR από τη [Aspose.PSD Java page](https://reference.aspose.com/psd/java/).  
3. **Ένα δείγμα αρχείου PSD** – π.χ., `sample.psd` τοποθετημένο σε φάκελο που μπορείτε να αναφέρετε από τον κώδικά σας.

## Εισαγωγή Πακέτων

Η κλάση `RasterImage` και τα συναφή βοηθητικά εργαλεία αποτελούν τον πυρήνα της ροής εργασίας περιστροφής.

Η κλάση `RasterImage` είναι το κύριο αντικείμενο του Aspose.PSD για χειρισμό εικόνων βασισμένων σε raster. Παρέχει μεθόδους για φόρτωση, μετασχηματισμό και αποθήκευση raster εικόνων διατηρώντας τα μεταδεδομένα.

## Οδηγός Βήμα‑Βήμα

### Βήμα 1: Ορίστε τον Κατάλογο Εγγράφου Σας

Ορίστε το φάκελο που περιέχει το αρχικό PSD και όπου θα γραφτεί το αποτέλεσμα. Η χρήση απόλυτης διαδρομής ή `System.getProperty("user.dir")` εξαλείφει τις εκπλήξεις σχετικών διαδρομών.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Βήμα 2: Καθορίστε Διαδρομές Πηγής και Προορισμού

Δώστε τα πλήρη ονόματα αρχείων για το εισερχόμενο PSD και τη ζητούμενη μορφή εξόδου (π.χ., PNG, JPEG, TIFF). Η αλλαγή της επέκτασης στο `destName` επιλέγει αυτόματα τον κατάλληλο κωδικοποιητή.

```java
String dataDir = "Your Document Directory";
```

### Βήμα 3: Φορτώστε την Εικόνα

Η μέθοδος `Image.load` ανιχνεύει τη μορφή του αρχείου και επιστρέφει μια συγκεκριμένη παρουσία `RasterImage` έτοιμη για raster λειτουργίες.

Η κλάση `Image` είναι ένα εργοστάσιο που διαβάζει ένα αρχείο από το δίσκο και δημιουργεί μια αναπαράσταση στη μνήμη κατάλληλη για περαιτέρω επεξεργασία. Υποστηρίζει αυτόματη ανίχνευση μορφής για όλες τις 30+ υποστηριζόμενες τύπους.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### Βήμα 4: Προσωρινή Αποθήκευση Δεδομένων Εικόνας (Προαιρετικό αλλά Συνιστάται)

Καλώντας `image.cacheData()` αποθηκεύει τα δεδομένα pixel στη μνήμη, επιταχύνοντας δραστικά τις επόμενες μετασχηματισμούς—ιδιαίτερα για μεγάλα αρχεία PSD που διαφορετικά θα προκαλούσαν επαναλαμβανόμενη πρόσβαση στο δίσκο.

Η μέθοδος `cacheData()` εξαναγκάζει την εικόνα να φορτωθεί πλήρως στη RAM, μειώνοντας το κόστος του lazy loading κατά τις εντατικές λειτουργίες.

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### Βήμα 5: Περιστρέψτε την Εικόνα

Κληθείτε τη `rotate` με τρία ορίσματα: τη γωνία περιστροφής (float), μια σημαία για επέκταση του καμβά, και το χρώμα φόντου για τις νέες εκτεθειμένες γωνίες.

Η μέθοδος `rotate` περιστρέφει την εικόνα γύρω από το κέντρο της, προαιρετικά επεκτείνοντας τον καμβά ώστε να χωρέσει τα περιστραμμένα όρια. Το φόντο `Color` γεμίζει οποιονδήποτε κενό χώρο, αποτρέποντας διαφανείς ή μαύρες γωνίες.

- **20f** – γωνία περιστροφής σε μοίρες (float). Αλλάξτε αυτή την τιμή για οποιαδήποτε γωνία, π.χ., `-45f` για δεξιόστροφη περιστροφή.  
- **true** – διατηρεί την αρχική αναλογία διαστάσεων ενώ επεκτείνει τον καμβά.  
- **Color.getRed()** – χρώμα φόντου που γεμίζει τις κενές γωνίες· αντικαταστήστε το με `Color.getWhite()` ή οποιοδήποτε προσαρμοσμένο χρώμα χρειάζεται.

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### Βήμα 6: Αποθηκεύστε το Αποτέλεσμα

Επιλέξτε έναν κωδικοποιητή (JPEG, PNG, κ.λπ.) και καλέστε `save`. Το `JpegOptions` σας επιτρέπει να ρυθμίσετε την ποιότητα, ενώ το `PngOptions` παρέχει απώλεια‑απώλειας έξοδο.

Η μέθοδος `save` γράφει την επεξεργασμένη εικόνα στο δίσκο χρησιμοποιώντας το καθορισμένο αντικείμενο επιλογών, διασφαλίζοντας ότι το επίπεδο συμπίεσης και το βάθος χρώματος διατηρούνται όπως απαιτείται.

```java
image.rotate(20f, true, Color.getRed());
```

## Συνηθισμένα Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Κενές γωνίες μετά την περιστροφή** | Δεν έχει δοθεί χρώμα φόντου | Περάστε ένα `Color` (π.χ., `Color.getWhite()`) στη `rotate`. |
| **Σφάλμα έλλειψης μνήμης σε μεγάλα PSD** | Η εικόνα δεν έχει προσωρινά αποθηκευτεί | Καλέστε `image.cacheData()` πριν την επεξεργασία. |
| **Λανθασμένη κατεύθυνση γωνίας** | Σύγχυση μεταξύ αρνητικής και θετικής γωνίας | Χρησιμοποιήστε αρνητικές τιμές για δεξιόστροφη περιστροφή (ή αντίστροφα ανάλογα με το σύστημα συντεταγμένων). |
| **Μη αποθηκευμένες αλλαγές** | Παράλειψη κλήσης `save` | Βεβαιωθείτε ότι εκτελείται `image.save(...)` μετά την περιστροφή. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να περιστρέψω εικόνες με διαφάνεια χρησιμοποιώντας Aspose.PSD για Java;**  
Α: Ναι. Η βιβλιοθήκη διατηρεί τα κανάλια άλφα· παραλείψτε ένα αδιαφανές χρώμα φόντου για να κρατήσετε τις γωνίες διαφανείς.

**Ε: Υπάρχουν περιορισμοί στους τύπους αρχείων εικόνας που υποστηρίζονται για περιστροφή;**  
Α: Όχι. Το Aspose.PSD υποστηρίζει PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF και 30+ επιπλέον μορφές.

**Ε: Μπορώ να περιστρέψω εικόνες με αρνητική γωνία;**  
Α: Απόλυτα. Περάστε μια αρνητική τιμή float στη `rotate` (π.χ., `-30f`) για δεξιόστροφη περιστροφή.

**Ε: Παρέχει το Aspose.PSD προεπισκόπηση εικόνας σε πραγματικό χρόνο κατά την περιστροφή;**  
Α: Το API είναι μόνο για διακομιστή. Για ζωντανές προεπισκοπήσεις, αποδώστε το περιστραμμένο bitmap σε ένα UI framework όπως Swing ή JavaFX και ανανεώστε την προβολή.

**Ε: Υπάρχει φόρουμ κοινότητας για το Aspose.PSD όπου μπορώ να ζητήσω βοήθεια;**  
Α: Ναι, επισκεφθείτε το [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) για να θέσετε ερωτήσεις και να μοιραστείτε εμπειρίες.

---

**Τελευταία Ενημέρωση:** 2026-05-19  
**Δοκιμασμένο Με:** Aspose.PSD για Java 24.11 (τελευταία έκδοση τη στιγμή της συγγραφής)  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## Σχετικά Tutorials

- [Υψηλής Ποιότητας Κλιμάκωση Εικόνας με Bicubic Resampler στο Aspose.PSD για Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Αλλαγή Μεγέθους Εικόνας Java - Χρήση της Καταμέτρησης Resize Type Enumeration στο Aspose.PSD για Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Θόλωση Εικόνας Java με Aspose.PSD – Προσθήκη Εφέ Θόλωσης](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}