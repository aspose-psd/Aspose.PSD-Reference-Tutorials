---
date: 2026-09-28
description: Μάθετε πώς να εξάγετε PSD ως PNG ενώ ορίζετε τη λειτουργία χρώματος του
  PSD σε 16‑bit grayscale χρησιμοποιώντας το Aspose.PSD for Java. Οδηγός βήμα‑βήμα
  με παραδείγματα κώδικα.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Εξαγωγή PSD ως PNG – 16-bit Grayscale – Java
og_description: Εξαγωγή PSD ως PNG με 16‑bit grayscale χρησιμοποιώντας το Aspose.PSD
  for Java. Ακολουθήστε αυτό το βήμα‑βήμα tutorial για να διατηρήσετε 65.536 αποχρώσεις
  του γκρι.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Εξαγωγή PSD ως PNG με 16‑bit grayscale σε Java – Οδηγός Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Πώς να εξάγετε PSD ως PNG με λειτουργία χρώματος 16‑bit grayscale σε Java
url: /el/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή PSD ως PNG με 16‑bit γκρι κλίμακα χρωματική λειτουργία σε Java

## Εισαγωγή
Exporting PSD as PNG while keeping a 16‑bit grayscale color mode gives you the depth of a professional photograph and the universal compatibility of PNG. In this guide you’ll learn how to **set the PSD color mode to 16‑bit grayscale** and then **export the PSD as PNG** using Aspose.PSD for Java. The tutorial covers everything from prerequisites to troubleshooting, so you can integrate the workflow into any Java‑based image pipeline.

## Γρήγορες απαντήσεις
- **Τι περιλαμβάνει η «εξαγωγή PSD ως PNG»;** Φορτώστε ένα PSD, προαιρετικά αλλάξτε τη χρωματική λειτουργία του και αποθηκεύστε το ως αρχείο PNG.  
- **Ποια κλάση Aspose διαχειρίζεται τη μετατροπή;** `PsdImage` φορτώνει το PSD και `PngOptions` ορίζει τις ρυθμίσεις εξόδου PNG.  
- **Χρειάζομαι άδεια για παραγωγή;** Ναι – μια δοκιμαστική έκδοση λειτουργεί για δοκιμές, αλλά απαιτείται πληρωμένη άδεια για εμπορική χρήση.  
- **Μπορεί το βάθος 16‑bit να διατηρηθεί στο PNG;** Απόλυτα, χρησιμοποιώντας το `PngColorType.GrayscaleWithAlpha`.  
- **Ποια IDE υποστηρίζονται;** Οποιοδήποτε Java IDE – IntelliJ IDEA, Eclipse, VS Code ή NetBeans.

## Τι είναι η εξαγωγή PSD ως PNG;
Η εξαγωγή PSD ως PNG είναι η διαδικασία μετατροπής ενός εγγράφου Adobe Photoshop (PSD) σε αρχείο Portable Network Graphics (PNG) διατηρώντας τα δεδομένα εικονοστοιχείων και το βάθος χρώματος της εικόνας. Αυτή η μετατροπή χρησιμοποιείται συχνά για την κοινή χρήση υψηλής ποιότητας γκρι κλίμακας πόρων στο web χωρίς απώλεια τόνου.

## Γιατί να εξάγετε PSD ως PNG με 16‑bit γκρι κλίμακα;
Η εξαγωγή σε PNG διατηρώντας 16‑bit γκρι κλίμακα διατηρεί 65 536 αποχρώσεις του γκρι, παρέχοντας πολύ μεγαλύτερη πλούσια τόνου σε σύγκριση με εικόνες 8‑bit. Η καθολική υποστήριξη του PNG εξασφαλίζει ότι τα αρχεία μπορούν να εμφανιστούν σε προγράμματα περιήγησης, κινητές εφαρμογές και επεξεργαστές επιφάνειας εργασίας χωρίς απώλειες, ενώ η χωρίς απώλειες συμπίεση του Aspose.PSD εγγυάται ότι δεν εισάγονται τεχνουργήματα.

## Προαπαιτούμενα
Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα παρακάτω:

1. **Java Development Kit (JDK)** – Εγκαταστήστε το τελευταίο JDK από [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – Κατεβάστε το JAR από τη [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **Ένα IDE** – IntelliJ IDEA, Eclipse ή Visual Studio Code λειτουργούν τέλεια.  
4. **Βασικές γνώσεις Java** – Θα πρέπει να αισθάνεστε άνετα με τη δημιουργία κλάσεων, τη διαχείριση εξαιρέσεων και την εργασία με διαδρομές αρχείων.  
5. **Ένα δείγμα αρχείου PSD** – Δημιουργήστε ένα στο Adobe Photoshop ή κατεβάστε ένα δωρεάν δείγμα online.

## Πώς να εξάγετε PSD ως PNG βήμα προς βήμα

## Πώς ορίζετε τη χρωματική λειτουργία PSD σε 16‑bit γκρι κλίμακα;
PsdImage είναι η κλάση Aspose.PSD που φορτώνει και αντιπροσωπεύει ένα αρχείο PSD στη μνήμη.  
ColorMode είναι μια απαρίθμηση που ορίζει τη χρωματική λειτουργία μιας εικόνας PSD.

Φορτώστε το PSD με `PsdImage`, αλλάξτε τη χρωματική λειτουργία χρησιμοποιώντας την ιδιότητα `ColorMode` και, στη συνέχεια, αποθηκεύστε το τροποποιημένο αρχείο. Αυτή η λειτουργία εκτελείται εξ ολοκλήρου στη μνήμη, εξαλείφοντας την ανάγκη για ενδιάμεσα αρχεία και εξασφαλίζοντας ότι η μετατροπή είναι γρήγορη και αποδοτική.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Αυτές οι εισαγωγές σας δίνουν πρόσβαση στις λειτουργίες που θα χρησιμοποιήσετε για τη διαχείριση αρχείων PSD, τον ορισμό της χρωματικής λειτουργίας και την εξαγωγή του αποτελέσματος ως PNG.

## Πώς ορίζετε τους φακέλους προέλευσης και εξόδου;
`File` είναι μια κλάση java.io που αντιπροσωπεύει μια διαδρομή αρχείου ή φακέλου στο σύστημα αρχείων.

Πρέπει να ενημερώσετε το πρόγραμμα πού θα διαβάσει το αρχικό PSD και πού θα γράψει το μετατρεπόμενο PNG. Η χρήση απόλυτων ή σχετικών διαδρομών λειτουργεί, αλλά διατηρήστε τις συνεπείς σε όλα τα περιβάλλοντα για να αποφύγετε σφάλματα επίλυσης διαδρομών.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Αντικαταστήστε τις συμβολοσειρές placeholder με τις πραγματικές διαδρομές στο μηχάνημά σας.

## Πώς να ενσωματώσετε τη λογική μετατροπής σε επαναχρησιμοποιήσιμη μέθοδο;
`convertPsdToPng` είναι μια προσαρμοσμένη μέθοδος που ενσωματώνει όλα τα βήματα που απαιτούνται για τη μετατροπή ενός αρχείου PSD σε PNG με προαιρετικές ρυθμίσεις.

Η δημιουργία μιας αφιερωμένης μεθόδου σας επιτρέπει να επαναχρησιμοποιήσετε τα ίδια βήματα μετατροπής για πολλά αρχεία ή διαφορετικές ρυθμίσεις. Περνάτε παραμέτρους όπως η διαδρομή προέλευσης, ο φάκελος προορισμού και το προαιρετικό επίπεδο συμπίεσης, καθιστώντας τη ροή εργασίας ευέλικτη και συντηρήσιμη.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Αυτή η μέθοδος σας επιτρέπει να **ορίσετε τη χρωματική λειτουργία PSD** και στη συνέχεια να **εξάγετε PSD ως PNG** σε μία ενιαία ροή.

## Πώς να φορτώσετε το PSD και να εφαρμόσετε τη λειτουργία 16‑bit γκρι κλίμακας;
PsdImage είναι η κλάση Aspose.PSD που φορτώνει ένα αρχείο PSD στη μνήμη.

ColorMode.GRAYSCALE_16 είναι μια τιμή απαρίθμησης που ορίζει την εικόνα σε 16‑bit γκρι κλίμακα.

`channelBitsCount` είναι μια ιδιότητα που καθορίζει τον αριθμό των bits ανά κανάλι.

Μέσα στη μέθοδο μετατροπής, δημιουργήστε τις πλήρεις διαδρομές αρχείων, δημιουργήστε ένα αντικείμενο `PsdImage` και αλλάξτε το `ColorMode` σε `ColorMode.GRAYSCALE_16`. Η ιδιότητα `channelBitsCount` πρέπει να οριστεί σε 16 για να διατηρηθεί το υψηλό βάθος bits, εξασφαλίζοντας ότι η εικόνα διατηρεί όλες τις τόνους πληροφορίες.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Το `postfix` σας βοηθά να παρακολουθείτε τις ρυθμίσεις που χρησιμοποιούνται για κάθε εξαγόμενο αρχείο.

## Πώς να σχεδιάσετε ένα λεπτό περίγραμμα στην εικόνα (προαιρετικό βήμα);
`Graphics` είναι μια κλάση που παρέχει δυνατότητες σχεδίασης σε έναν καμβά `PsdImage`.

Μπορείτε προαιρετικά να σχεδιάσετε ένα γκρι ορθογώνιο γύρω από την εικόνα για να κάνετε το αποτέλεσμα πιο ορατό κατά τη δοκιμή. Αυτό το βήμα δείχνει πώς να εργάζεστε με στρώματα και αντικείμενα γραφικών, και το ορθογώνιο υπολογίζεται δυναμικά ώστε να παραμένει κεντραρισμένο ανεξάρτητα από το μέγεθος της εικόνας.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Το ορθογώνιο υπολογίζεται δυναμικά ώστε να παραμένει κεντραρισμένο ανεξάρτητα από το μέγεθος της εικόνας.

## Πώς να αποθηκεύσετε το τροποποιημένο PSD με τη νέα χρωματική λειτουργία;
`PsdOptions` είναι μια κλάση που ελέγχει πώς αποθηκεύεται ένα αρχείο PSD, συμπεριλαμβανομένων των ρυθμίσεων χρωματικής λειτουργίας και βάθους bits.

Μετά το σχεδιασμό (ή την παράλειψη αυτού του βήματος), καλέστε `save` στο αντικείμενο `PsdImage`, περνώντας ένα αντικείμενο `PsdOptions` που διατηρεί τη ρύθμιση 16‑bit γκρι κλίμακας. Αυτό εξασφαλίζει ότι το αποθηκευμένο PSD διατηρεί τη ζητούμενη χρωματική λειτουργία χωρίς απώλεια δεδομένων.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Πώς να μετατρέψετε το PSD σε PNG διατηρώντας το βάθος 16‑bit;
`PngOptions` είναι μια κλάση που ορίζει τις ρυθμίσεις εξόδου PNG όπως ο τύπος χρώματος και το επίπεδο συμπίεσης.

`PngColorType.GrayscaleWithAlpha` είναι μια τιμή απαρίθμησης που αποθηκεύει δεδομένα 16‑bit γκρι κλίμακας με κανάλι άλφα.

Φορτώστε το νεοαποθηκευμένο PSD, διαμορφώστε το `PngOptions` με `PngColorType.GrayscaleWithAlpha` και καλέστε `save`. Αυτό διατηρεί τα δεδομένα 16‑bit γκρι κλίμακας μέσα στο αρχείο PNG, παρέχοντας μια χωρίς απώλειες, υψηλής ποιότητας εικόνα κατάλληλη για περαιτέρω επεξεργασία ή διανομή.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Τώρα έχετε εξαγάγει επιτυχώς **PSD ως PNG** διατηρώντας τα υψηλής ποιότητας δεδομένα 16‑bit γκρι κλίμακας.

## Κοινά προβλήματα και λύσεις
| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|------------------|----------|
| **“Unsupported color type” exception** | Προσπάθεια αποθήκευσης ενός PSD με μη υποστηριζόμενη διαμόρφωση καναλιών. | Βεβαιωθείτε ότι το `channelBitsCount` ταιριάζει με το πραγματικό βάθος bits (16) και το `channelsCount` είναι σωστό για γκρι κλίμακα (1). |
| **File not found** | Λανθασμένη διαδρομή φακέλου προέλευσης. | Ελέγξτε ξανά τη συμβολοσειρά `sourceDir` και βεβαιωθείτε ότι το αρχείο PSD υπάρχει σε αυτή τη θέση. |
| **Output PNG appears black** | Το PNG αποθηκεύτηκε χωρίς σωστή διαχείριση άλφα. | Χρησιμοποιήστε το `PngColorType.GrayscaleWithAlpha` όπως φαίνεται παραπάνω. |
| **Memory overflow on large PSDs** | Φόρτωση ολόκληρου του αρχείου στη μνήμη. | Ενεργοποιήστε τη λειτουργία streaming μέσω `PsdImage.load(inputStream, new LoadOptions())` για αποτελεσματική επεξεργασία μεγάλων αρχείων. |

## Συχνές ερωτήσεις

**Q: Τι είναι η λειτουργία χρώματος 16‑bit γκρι κλίμακας;**  
A: Παρέχει 65 536 αποχρώσεις του γκρι, προσφέροντας πολύ περισσότερη λεπτομέρεια τόνου σε σύγκριση με το τυπικό 8‑bit (256 αποχρώσεις).

**Q: Μπορώ να χρησιμοποιήσω το Aspose.PSD για εικόνες που δεν είναι γκρι κλίμακα;**  
A: Απόλυτα! Το Aspose.PSD υποστηρίζει RGB, CMYK, Lab, Indexed και πολλές άλλες χρωματικές λειτουργίες.

**Q: Υπάρχει δοκιμαστική έκδοση του Aspose.PSD;**  
A: Ναι, μπορείτε να δοκιμάσετε μια δωρεάν δοκιμαστική έκδοση του Aspose.PSD. Απλώς μεταβείτε στη [Aspose download page](https://releases.aspose.com/).

**Q: Πού μπορώ να βρω περισσότερα παραδείγματα Aspose.PSD;**  
A: Ελέγξτε την επίσημη [documentation](https://reference.aspose.com/psd/java/) για αναλυτικά tutorials, αναφορές API και δείγματα έργων.

**Q: Πώς μπορώ να αγοράσω άδεια για το Aspose.PSD;**  
A: Μπορείτε να αγοράσετε άδεια επισκεπτόμενοι τη [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Τελευταία ενημέρωση:** 2026-09-28  
**Δοκιμάστηκε με:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Μετατροπή PSD σε PNG με Καθορισμένο Βάθος Bit Χρησιμοποιώντας Aspose.PSD for Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Εξαγωγή PSD σε PNG με Εφέ Στρώματος χρησιμοποιώντας Aspose.PSD for Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Αποθήκευση PSD ως JPEG και Υποστήριξη RGB Χρώματος με Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}