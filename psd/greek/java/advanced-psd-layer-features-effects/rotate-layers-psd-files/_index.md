---
date: 2026-07-22
description: Μάθετε πώς να αποθηκεύσετε psd ως png, να διατηρήσετε τη διαφάνεια PNG
  και να περιστρέψετε τα επίπεδα PSD σε Java με Aspose.PSD. Οδηγός βήμα‑βήμα, εξηγήσεις
  χωρίς κώδικα και συμβουλές αντιμετώπισης προβλημάτων.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: Αποθήκευση psd ως png και περιστροφή επιπέδων σε Java χρησιμοποιώντας Aspose.PSD
og_description: Αποθήκευση psd ως png με Aspose.PSD για Java. Διατηρήστε τη διαφάνεια,
  περιστρέψτε τα επίπεδα και εξάγετε PNG με λίγες μόνο γραμμές κώδικα—ιδανικό για
  αυτοματοποιημένες ροές εργασίας.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: Αποθήκευση psd ως png και περιστροφή επιπέδων σε Java χρησιμοποιώντας Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: Αποθήκευση psd ως png και περιστροφή επιπέδων σε Java χρησιμοποιώντας Aspose.PSD
url: /el/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Σχετικά Μαθήματα

- [Αποθήκευση PSD ως PNG και Εφαρμογή Σκιάς Rendering Drop Shadow στο Aspose.PSD για Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Πώς να συμπιέσετε αρχεία PNG χρησιμοποιώντας το Aspose.PSD για Java](/psd/java/optimizing-png-files/compress-png-files/)
- [Πώς να Περιστρέψετε Εικόνα σε Java με το Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# αποθήκευση psd ως png και περιστροφή επιπέδων σε Java χρησιμοποιώντας το Aspose.PSD

## Εισαγωγή
Αν χρειάζεστε **αποθήκευση PSD ως PNG** ενώ περιστρέφετε επίσης τα επίπεδα, αυτός ο οδηγός είναι για εσάς. Είτε δημιουργείτε ένα εργαλείο παρτίδας επεξεργασίας, μια υπηρεσία web που χρειάζεται άμεση επεξεργασία εικόνας, είτε απλώς αυτοματοποιείτε μια ροή εργασίας σχεδίασης, η προγραμματιστική υλοποίηση εξοικονομεί χρόνο και αφαιρεί την εξάρτηση από το Adobe Photoshop. Σε αυτό το μάθημα θα δούμε **πώς να περιστρέψετε επίπεδα PSD** και να εξάγετε το αποτέλεσμα ως PNG χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD για Java. Ας μπει η δουλειά και ας κάνουμε τη ροή εργασίας σας πιο ομαλή!

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη μπορώ να χρησιμοποιήσω;** Aspose.PSD for Java  
- **Μπορώ να περιστρέψω και να αποθηκεύσω PSD ως PNG ταυτόχρονα;** Ναι – περιστρέψτε το PSD και στη συνέχεια αποθηκεύστε το ως PNG  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται πληρωμένη άδεια για παραγωγή  
- **Ποια έκδοση της Java υποστηρίζεται;** Java 8 και νεότερες  
- **Είναι η έξοδος PNG διαφανής;** Ναι, όταν ορίσετε `PngColorType.TruecolorWithAlpha`

## Τι είναι η «μετατροπή PSD σε PNG»;
Η μετατροπή ενός εγγράφου Photoshop (PSD) σε εικόνα PNG εξάγει το οπτικό περιεχόμενο—συμπεριλαμβανομένων των επιπέδων, μάσκων και καναλιών άλφα—σε μια ευρέως υποστηριζόμενη μορφή raster που διατηρεί τη διαφάνεια. Αυτό κάνει το PNG ιδανικό για γραφικά web, μικρογραφίες και επεξεργασία εικόνας σε επόμενα στάδια. Η προκύπτουσα PNG μπορεί να χρησιμοποιηθεί άμεσα σε ιστοσελίδες, κινητές εφαρμογές ή να υποβληθεί σε περαιτέρω επεξεργασία από άλλες βιβλιοθήκες εικόνας.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για Java για την αποθήκευση PSD ως PNG και την περιστροφή επιπέδων PSD;
Το Aspose.PSD σας επιτρέπει να **αποθηκεύσετε PSD ως PNG** και να περιστρέψετε επίπεδα χωρίς εγκατάσταση του Photoshop. Υποστηρίζει **50+ μορφές εισόδου και εξόδου**, επεξεργάζεται αρχεία PSD εκατοντάδων σελίδων χρησιμοποιώντας λιγότερο από 200 MB RAM, και λειτουργεί σε Windows, Linux και macOS. Το API απαιτεί μόνο λίγες κλήσεις μεθόδων, παρέχοντας αποτελέσματα υψηλής πιστότητας με ενσωματωμένη διαχείριση εφέ επιπέδων, μασκών και καναλιών άλφα.

## Προαπαιτούμενα
Πριν βουτήξουμε στον κώδικα, βεβαιωθείτε ότι έχετε τα εξής:

- **Java Development Kit (JDK)** – κατεβάστε από την [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse ή NetBeans είναι όλα εντάξει.  
- **Aspose.PSD for Java library** – αποκτήστε το τελευταίο JAR από τη [release page](https://releases.aspose.com/psd/java/).  
- **Basic Java knowledge** – εξοικείωση με κλάσεις, αντικείμενα και διαχείριση εξαιρέσεων.

## Οδηγός Βήμα‑Βήμα

### Βήμα 1: Ρύθμιση του Java Project σας
Δημιουργήστε ένα νέο Java project στο IDE σας και προσθέστε το JAR του Aspose.PSD στο build path του project.

### Βήμα 2: Εισαγωγή Απαιτούμενων Κλάσεων
`PsdImage` είναι η κεντρική κλάση που αντιπροσωπεύει ένα έγγραφο Photoshop στη μνήμη. `PngOptions` ελέγχει τις ρυθμίσεις PNG, και `RotateFlipType` ορίζει τις λειτουργίες περιστροφής και αναστροφής.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Αυτές οι εισαγωγές σας δίνουν πρόσβαση στη φόρτωση εικόνας, περιστροφή και επιλογές PNG.

### Βήμα 3: Ορισμός Διαδρομών Αρχείων
Καθορίστε πού βρίσκεται το αρχικό PSD και πού πρέπει να γραφτούν τα αρχεία εξόδου. Η χρήση απόλυτων διαδρομών κατά τη δοκιμή αποτρέπει σφάλματα «file not found».

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Συμβουλή:** Αποθηκεύστε τις διαδρομές σε ένα αρχείο ρυθμίσεων για ευκολότερη συντήρηση σε μεγαλύτερα έργα.

### Βήμα 4: Φόρτωση του Αρχείου PSD
`PsdImage` φορτώνει ολόκληρο το έγγραφο Photoshop, συμπεριλαμβανομένων όλων των επιπέδων, μασκών και εφέ, σε ένα αντικείμενο που μπορεί να τροποποιηθεί.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Τώρα το `im` αντιπροσωπεύει ολόκληρο το PSD, έτοιμο για μετασχηματισμούς.

### Βήμα 5: Περιστροφή της Εικόνας (Πώς να περιστρέψετε PSD)
`RotateFlipType` απαριθμεί όλες τις υποστηριζόμενες περιστροφές και αναστροφές. Σε αυτό το παράδειγμα περιστρέφουμε 270° και αναστρέφουμε και τους δύο άξονες, κάτι που ανταλλάσσει το πλάτος και το ύψος ενώ καθρεφτίζει την εικόνα.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Μπορείτε να πειραματιστείτε με άλλες τιμές όπως `Rotate90FlipNone` ή `Rotate180FlipX`.

### Βήμα 6: Αποθήκευση της Περιστραμμένης Εικόνας ως PNG (αποθήκευση PSD ως PNG)
Ρυθμίστε το `PngOptions` ώστε να διατηρεί τη διαφάνεια (`PngColorType.TruecolorWithAlpha`) και στη συνέχεια καλέστε `save`. Το PNG διατηρεί τη διαφάνεια των επιπέδων, εξασφαλίζοντας αδιάλειπτη λειτουργία σε web ή κινητές εφαρμογές.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Το προκύπτον PNG διατηρεί τα κανάλια άλφα, καθιστώντας το κατάλληλο για σύνθεση ή περαιτέρω επεξεργασία.

### Βήμα 7: Αποθήκευση του Τροποποιημένου PSD (προαιρετικό)
Αν χρειάζεστε επίσης ένα νέο PSD με την εφαρμοσμένη περιστροφή, μπορείτε να αποθηκεύσετε το τροποποιημένο `PsdImage` ξανά στο δίσκο.

```java
im.save(psdPath);
```

Τώρα έχετε τόσο μια προεπισκόπηση PNG όσο και ένα ενημερωμένο αρχείο PSD.

## Συνηθισμένα Προβλήματα και Λύσεις
- **File not found:** Επαληθεύστε ότι το `dataDir` τελειώνει με διαχωριστικό διαδρομής (`/` ή `\`).  
- **OutOfMemoryError on large PSDs:** Αυξήστε το μέγεθος heap της JVM (`-Xmx2g`).  
- **Transparency lost:** Βεβαιωθείτε ότι έχει οριστεί `PngColorType.TruecolorWithAlpha`; διαφορετικά το PNG θα αποθηκευτεί χωρίς άλφα.  
- **Flip PSD image not behaving as expected:** Ελέγξτε ξανά τη σταθερά `RotateFlipType` που επιλέξατε· μερικές σταθερές συνδυάζουν περιστροφή και αναστροφή σε ένα βήμα.

## Συχνές Ερωτήσεις

**Ε: Μπορώ να περιστρέψω ένα συγκεκριμένο επίπεδο σε αρχείο PSD;**  
Ναι, μπορείτε να καλέσετε `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` μετά από επανάληψη στα `im.getLayers()`.

**Ε: Υπάρχει κάποιος περιορισμός απόδοσης με το Aspose.PSD για Java;**  
Η βιβλιοθήκη διαχειρίζεται τα περισσότερα αρχεία αποδοτικά, αλλά εξαιρετικά μεγάλα PSD (>500 MB) μπορεί να απαιτούν επιπλέον μνήμη ή επιλογές streaming.

**Ε: Είναι το Aspose.PSD δωρεάν για χρήση;**  
Η Aspose προσφέρει δωρεάν δοκιμή, αλλά απαιτείται πληρωμένη άδεια για παραγωγή. Δείτε την [temporary license](https://purchase.aspose.com/temporary-license/) για δοκιμές.

**Ε: Πού μπορώ να βρω λεπτομερή τεκμηρίωση;**  
Πλήρης τεκμηρίωση είναι διαθέσιμη στο [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Ε: Τι κάνω αν αντιμετωπίσω προβλήματα κατά τη χρήση του Aspose.PSD;**  
Λάβετε βοήθεια μέσω του [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Ε: Η μετατροπή PSD σε PNG διατηρεί τα εφέ των επιπέδων;**  
Ναι, όταν αποθηκεύετε με `PngColorType.TruecolorWithAlpha`, τα περισσότερα οπτικά εφέ ραστεροποιούνται στο PNG.

**Ε: Μπορώ να επεξεργαστώ πολλαπλά αρχεία PSD σε παρτίδα;**  
Απολύτως. Τυλίξτε τον κώδικα σε βρόχο που επαναλαμβάνει έναν φάκελο με αρχεία PSD.

**Ε: Είναι δυνατόν να ορίσετε επίπεδο συμπίεσης PNG;**  
`PngOptions` παρέχει τη μέθοδο `setCompressionLevel(int)` για λεπτομερή ρύθμιση του μεγέθους εξόδου.

**Ε: Πρέπει να κλείσω το αντικείμενο εικόνας;**  
`PsdImage` υλοποιεί το `Closeable`; χρησιμοποιήστε try‑with‑resources ή καλέστε `im.close()` σε block `finally`.

**Ε: Θα έχει το περιστραμμένο PNG τις ίδιες διαστάσεις με το αρχικό;**  
Η περιστροφή κατά 90° ή 270° ανταλλάσσει το πλάτος και το ύψος, έτσι το PNG αντανακλά αυτόματα τη νέα προσανατολισμό.

## Συμπέρασμα
Αξιοποιώντας το Aspose.PSD για Java, μπορείτε να **αποθηκεύσετε PSD ως PNG**, **διατηρήσετε τη διαφάνεια PNG** και **περιστρέψετε επίπεδα PSD** με λίγες μόνο γραμμές κώδικα. Αυτή η προσέγγιση εξαλείφει την ανάγκη για Photoshop, επιταχύνει τις αυτοματοποιημένες ροές εργασίας και σας δίνει πλήρη έλεγχο πάνω στην έξοδο εικόνας. Δοκιμάστε το στα δικά σας έργα και δείτε πόσο χρόνο κερδίζετε!

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}