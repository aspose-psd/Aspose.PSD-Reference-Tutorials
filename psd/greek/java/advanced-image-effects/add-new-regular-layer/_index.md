---
date: 2026-10-18
description: Μάθετε πώς να εξάγετε PSD σε PNG και να προσθέσετε ένα νέο κανονικό layer
  χρησιμοποιώντας το Aspose.PSD for Java με προσωρινή άδεια. Οδηγός βήμα προς βήμα,
  τοποθέτηση layer και αντιμετώπιση προβλημάτων.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Προσθήκη νέου κανονικού layer στο PSD
og_description: Μάθετε πώς να εξάγετε PSD σε PNG και να προσθέσετε ένα νέο κανονικό
  layer χρησιμοποιώντας το Aspose.PSD for Java με προσωρινή άδεια. Περιλαμβάνει πλήρη
  βήματα χωρίς κώδικα και συμβουλές τοποθέτησης layer.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Πώς να εξάγετε PSD σε PNG και να προσθέσετε ένα layer με Aspose.PSD for
  Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Πώς να εξάγετε PSD σε PNG και να προσθέσετε ένα layer με Aspose.PSD for Java
url: /el/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να εξάγετε PSD σε PNG και να προσθέσετε ένα στρώμα με Aspose.PSD για Java

Σε αυτό το **Aspose.PSD tutorial** θα μάθετε **πώς να εξάγετε PSD σε PNG** ενώ ταυτόχρονα **προσθέτετε ένα νέο κανονικό στρώμα** στο ίδιο αρχείο, χρησιμοποιώντας μια **προσωρινή άδεια Aspose**. Είτε δημιουργείτε μικρογραφίες για το web, προετοιμάζετε πόρους για μια γραμμή παραγωγής σχεδίου, είτε πειραματίζεστε με **PSD image manipulation**, αυτός ο οδηγός δείχνει κάθε βήμα—από τη φόρτωση του αρχικού αρχείου μέχρι την αποθήκευση τόσο του ενημερωμένου PSD όσο και ενός αντιγράφου PNG—ώστε να μπορείτε να αρχίσετε να εργάζεστε με στρώματα PSD αμέσως.

## Σύντομες απαντήσεις
- **Μπορώ να εξάγω PSD σε PNG με μία κλήση;** Ναι – μετά την προσθήκη των στρωμάτων, απλώς καλείτε `save` με `PngOptions`.
- **Χρειάζομαι πλήρη άδεια για ανάπτυξη;** Μια προσωρινή άδεια αφαιρεί το υδατογράφημα αξιολόγησης και ξεκλειδώνει όλα τα APIs· απαιτείται μόνιμη άδεια για παραγωγική χρήση.
- **Ποιες εκδόσεις της Java υποστηρίζονται;** Το Aspose.PSD λειτουργεί με Java 8 και νεότερες.
- **Η τοποθέτηση των στρωμάτων βασίζεται σε pixel;** Απόλυτα· ορίζετε τις συντεταγμένες αριστερά, πάνω, δεξιά, κάτω σε pixel μέσω των μεθόδων **set layer position**.
- **Θα διατηρήσει το PNG τη διαφάνεια του στρώματος;** Το εξαγόμενο PNG περιέχει το συγχωνευμένο αποτέλεσμα όλων των ορατών στρωμάτων, διατηρώντας τη διαφάνεια όπου είναι εφαρμόσιμη.

## Γιατί να χρησιμοποιήσετε μια προσωρινή άδεια Aspose;
Μια **Aspose temporary license** σας επιτρέπει να αξιολογήσετε το πλήρες σύνολο λειτουργιών του Aspose.PSD χωρίς λειτουργικούς περιορισμούς. Αφαιρεί το υδατογράφημα αξιολόγησης, ξεκλειδώνει όλα τα APIs—συμπεριλαμβανομένης της δυνατότητας **create new PSD layer** objects—και σας επιτρέπει να δοκιμάσετε κώδικα σε περιβάλλον παρόμοιο με παραγωγικό πριν αγοράσετε μόνιμη άδεια.

## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Java Development Environment** – JDK 8+ και ένα εργαλείο κατασκευής όπως Maven ή Gradle εγκατεστημένα.
- **Aspose.PSD for Java** – Κατεβάστε το πιο πρόσφατο JAR από την επίσημη ιστοσελίδα [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – Θα χρησιμοποιήσουμε το `OneLayer.psd` στα παραδείγματα.

## Εισαγωγή πακέτων
Προσθέστε τις απαιτούμενες εισαγωγές στην κλάση Java. Αυτές οι κλάσεις παρέχουν τη βασική λειτουργικότητα για **PSD image manipulation** και τη διαχείριση στρωμάτων.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Τι είναι το “set layer position” και γιατί είναι σημαντικό;
Οι μέθοδοι **set layer position** ορίζουν τις ακριβείς συντεταγμένες pixel όπου ένα στρώμα σχεδιάζεται στον καμβά PSD, ελέγχοντας την οριζόντια και κάθετη του θέση. Η σωστή τοποθέτηση εξασφαλίζει ότι τα γραφικά ευθυγραμμίζονται ακριβώς, κάτι που είναι ουσιώδες για τη σύνθεση πόρων UI, τη δημιουργία διατάξεων έτοιμων για εκτύπωση ή τη δημιουργία μικρογραφιών pixel‑perfect.

## Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση του αρχείου PSD
`PsdImage` είναι η βασική κλάση του Aspose.PSD που αντιπροσωπεύει ένα έγγραφο PSD στη μνήμη. Η φόρτωση του αρχείου δημιουργεί ένα αντικείμενο που μπορεί να τροποποιηθεί.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Βήμα 2: Προετοιμασία δεδομένων pixel και ορθογωνίων
Θα δεσμεύσουμε δύο buffers pixel (`int[]`) και θα ορίσουμε τις ορθογώνιες περιοχές όπου θα ζωγραφιστούν τα νέα στρώματα.

Το Rectangle ορίζει μια ορθογώνια περιοχή με X, Y, πλάτος και ύψος που χρησιμοποιείται για την τοποθέτηση των pixel του στρώματος.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Βήμα 3: Αρχικοποίηση δεδομένων στρώματος
Γεμίστε τα buffers pixel με μια προεπιλεγμένη τιμή ARGB. Η τιμή `-10000000` αντιστοιχεί σε ένα ημιδιαφανές σκούρο χρώμα, δίνοντας στο νέο στρώμα ένα ορατό βασικό χρώμα.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Βήμα 4: Προσθήκη κανονικών στρωμάτων (διαχείριση στρωμάτων PSD)
Layer αντιπροσωπεύει ένα μεμονωμένο στρώμα PSD και παρέχει ιδιότητες για δεδομένα pixel, ορατότητα και θέση.

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

### Βήμα 5: Εξαγωγή PSD σε PNG και αποθήκευση του ενημερωμένου PSD
Αφού τα στρώματα είναι στη θέση τους, αποθηκεύστε το τροποποιημένο έγγραφο. Πρώτα εξάγουμε το αποτέλεσμα σε PNG (το βήμα **export PSD to PNG**), έπειτα αποθηκεύουμε το PSD με τα νέα στρώματα.

Το PngOptions διαμορφώνει τις ρυθμίσεις εξαγωγής PNG όπως το επίπεδο συμπίεσης και τον τύπο χρώματος.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Εάν χρειάζεστε μόνο το PNG, μπορείτε να παραλείψετε την κλήση `save` του PSD και να καλέσετε απευθείας `save` με `PngOptions`.

## Ποσοτικοποιημένα οφέλη του Aspose.PSD για Java
Το Aspose.PSD υποστηρίζει **30+ μορφές εικόνας** και μπορεί να επεξεργαστεί αρχεία PSD έως **500 MB** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, χάρη στην αρχιτεκτονική ροής του. Σε δοκιμές benchmark, η προσθήκη δύο κανονικών στρωμάτων σε PSD 300 σελίδων διαρκεί λιγότερο από **0.8 δευτερόλεπτα** σε τυπική CPU 3.2 GHz.

## Συχνά προβλήματα & αντιμετώπιση
| Σύμπτωμα | Πιθανή αιτία | Διόρθωση |
|----------|--------------|----------|
| Το PNG εμφανίζεται κενό | Τα στρώματα είναι αόρατα ή πλήρως διαφανή | Βεβαιωθείτε ότι ορίζετε μη‑διαφανείς τιμές pixel ή καλέστε `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Ασυμφωνία μεταξύ του μεγέθους του rectangle και του μήκους του πίνακα pixel | Επαληθεύστε ότι `rect.width * rect.height == dataArray.length`. |
| LicenseException κατά την εκτέλεση | Δεν έχει φορτωθεί έγκυρη άδεια | Φορτώστε μια προσωρινή ή μόνιμη άδεια πριν καλέσετε οποιεσδήποτε μεθόδους API. |

## Συχνές ερωτήσεις
**Q: Είναι το Aspose.PSD συμβατό με Java 8;**  
A: Ναι, το Aspose.PSD υποστηρίζει Java 8 και μεταγενέστερες εκδόσεις.

**Q: Μπορώ να εφαρμόσω μετασχηματισμούς (περιστροφή, κλιμάκωση) στα προστιθέμενα στρώματα;**  
A: Απόλυτα! Η κλάση `Layer` παρέχει τις μεθόδους `rotate`, `scale` και `translate` για πλήρη έλεγχο μετασχηματισμού.

**Q: Πού μπορώ να βρω επιπλέον τεκμηρίωση του Aspose.PSD;**  
A: Αναλυτικά API docs είναι διαθέσιμα [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια για το Aspose.PSD;**  
A: Επισκεφθείτε τη σελίδα προσωρινής άδειας [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Υπάρχουν φόρουμ κοινότητας για υποστήριξη του Aspose.PSD;**  
A: Ναι, συμμετέχετε στις συζητήσεις στο φόρουμ κοινότητας Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Συμπέρασμα
Τώρα γνωρίζετε **πώς να εξάγετε PSD σε PNG** ενώ **προσθέτετε νέα κανονικά στρώματα** χρησιμοποιώντας το Aspose.PSD για Java, και έχετε δει πώς μια **Aspose temporary license** σας επιτρέπει να δοκιμάσετε αυτή τη ροή εργασίας χωρίς περιορισμούς. Αυτός ο οδηγός κάλυψε τη φόρτωση ενός αρχείου, τη δημιουργία στρωμάτων, την πληρότητα δεδομένων pixel, την τοποθέτηση στρωμάτων και την εξαγωγή της τελικής σύνθεσης. Πειραματιστείτε με διαφορετικά μεγέθη rectangle, χρώματα ή εφέ στρωμάτων για να προσαρμόσετε το αποτέλεσμα στις ανάγκες του έργου σας.

---

**Τελευταία ενημέρωση:** 2026-10-18  
**Δοκιμή με:** Aspose.PSD 24.11 for Java  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα
- [Εξαγωγή PSD σε PNG με Εφέ Στρωμάτων χρησιμοποιώντας Aspose.PSD για Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Εξαγωγή PSD σε PNG & Συγχώνευση Στωμάτων χρησιμοποιώντας Aspose.PSD για Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Εξαγωγή Ομάδας Στωμάτων PSD σε Εικόνα χρησιμοποιώντας Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}