---
date: 2026-05-19
description: Μάθετε πώς να μετατρέψετε PSD σε JPEG και να περιστρέψετε την εικόνα
  κατά 270 μοίρες χρησιμοποιώντας Aspose.PSD for Java. Αυτός ο οδηγός δείχνει πώς
  να περιστρέφετε αρχεία PSD, να αναστρέφετε εικόνες και να μετατρέπετε PSD σε JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Περιστροφή εικόνας 270 μοίρες
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Μετατροπή PSD σε JPEG & Περιστροφή 270° με Aspose.PSD for Java
url: /el/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή PSD σε JPEG & Περιστροφή Εικόνας 270 Μοιρών με Aspose.PSD για Java

## Εισαγωγή

Σε αυτό το **μαθήμα επεξεργασίας εικόνας Java**, θα μάθετε πώς να **μετατρέψετε PSD σε JPEG** ενώ περιστρέφετε την εικόνα 270 μοίρες χρησιμοποιώντας το Aspose.PSD για Java. Είτε δημιουργείτε μια αλυσίδα επεξεργασίας παρτίδας, έναν επεξεργαστή web‑βάσει, είτε ένα επιτραπέζιο εργαλείο, η βιβλιοθήκη σας επιτρέπει να χειρίζεστε τα στρώματα PSD χωρίς το Photoshop. Θα καλύψουμε επίσης προαιρετική αναστροφή και θα δείξουμε τη πλήρη ροή από τη φόρτωση ενός αρχείου PSD μέχρι την αποθήκευση ως JPEG.

## Σύντομες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται την περιστροφή;** Aspose.PSD for Java  
- **Ποια γωνία περιστροφής χρησιμοποιεί το παράδειγμα;** 270 μοίρες  
- **Μπορώ επίσης να αναστρέψω την εικόνα;** Ναι – χρησιμοποιήστε επιλογές `RotateFlipType` όπως `Rotate90FlipX`  
- **Πώς αποθηκεύεται το αποτέλεσμα;** Στο παράδειγμα αποθηκεύουμε ως JPEG χρησιμοποιώντας `JpegOptions`  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται έγκυρη άδεια Aspose.PSD για εμπορική χρήση  

## Τι σημαίνει «περιστροφή εικόνας 270 μοίρες»;
Η περιστροφή μιας εικόνας 270 μοίρες σημαίνει την στροφή της εικόνας τρία τέταρτα ενός πλήρους κύκλου δεξιόστροφα (ή 90 μοίρες αριστερόστροφα). Αυτή η προσανατολισμός συχνά επαναφέρει την αρχική διάταξη πορτραίτου μετά από προηγούμενες μετατροπές και χρησιμοποιείται συνήθως όταν οι εικόνες λήφθηκαν σε λειτουργία τοπίου αλλά πρέπει να εμφανιστούν σε πορτραίτο. Το αποτέλεσμα είναι μια σωστά προσανατολισμένη εικόνα χωρίς απώλεια ποιότητας.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για αυτήν την εργασία;
Το Aspose.PSD υποστηρίζει **πάνω από 50 μορφές εισόδου και εξόδου** — συμπεριλαμβανομένων των PSD, JPEG, PNG, BMP, GIF και TIFF — και μπορεί να επεξεργαστεί αρχεία έως **2 GB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη. Το API λειτουργεί σε οποιοδήποτε περιβάλλον Java (JDK 8+), δεν απαιτεί εγκατάσταση του Photoshop και παρέχει μια ενιαία κλήση `rotateFlip` που διαχειρίζεται τόσο την περιστροφή όσο και την αναστροφή σε ένα βήμα.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- Βιβλιοθήκη **Aspose.PSD for Java** εγκατεστημένη. Μπορείτε να την κατεβάσετε και να δείτε την πλήρη αναφορά API [εδώ](https://reference.aspose.com/psd/java/).  
- Περιβάλλον ανάπτυξης Java (JDK 8 ή νεότερο).  
- Ένα δείγμα αρχείου PSD που θέλετε να περιστρέψετε. Ενημερώστε τη μεταβλητή `sourceFile` στον κώδικα με τη σωστή διαδρομή προς το αρχείο σας.

## Εισαγωγή Πακέτων

Οι κλάσεις `Image`, `RotateFlipType` και `JpegOptions` απαιτούνται για τη φόρτωση, τη μετασχηματισμό και την αποθήκευση του αρχείου.  
`Image` είναι η βασική κλάση που αντιπροσωπεύει ένα έγγραφο PSD στη μνήμη.  
`RotateFlipType` απαριθμεί τις υποστηριζόμενες λειτουργίες περιστροφής και αναστροφής.  
`JpegOptions` διαμορφώνει τις ρυθμίσεις εξόδου JPEG όπως η ποιότητα.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Πώς να μετατρέψετε PSD σε JPEG μετά την περιστροφή;

Φορτώστε το αρχικό PSD, εφαρμόστε μια περιστροφή 270 μοίρες και αποθηκεύστε το αμέσως ως JPEG. Αυτή η τρι-βήμα ροή εκτελείται σε λιγότερο από ένα δευτερόλεπτο για τυπικές εικόνες 10 MP σε σύγχρονο CPU, καθιστώντας την ιδανική για εργασίες παρτίδας υψηλής απόδοσης. Επεξεργαζόμενοι μόνο τα απαραίτητα δεδομένα εικόνας, η κατανάλωση μνήμης παραμένει χαμηλή και το παραγόμενο JPEG διατηρεί την οπτική πιστότητα ενώ μειώνει το μέγεθος του αρχείου.

### Βήμα 1: Φόρτωση του αρχείου PSD

`Image` είναι η βασική κλάση του Aspose.PSD που αντιπροσωπεύει ένα ενιαίο έγγραφο PSD στη μνήμη. Η δημιουργία της διαβάζει μόνο τις πληροφορίες κεφαλίδας, διατηρώντας τη χρήση μνήμης χαμηλή.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Βήμα 2: Περιστροφή της εικόνας 270 μοίρες

`rotateFlip` εκτελεί την καθορισμένη περιστροφή και προαιρετική αναστροφή στην εικόνα. `RotateFlipType.Rotate270FlipNone` περιστρέφει τον καμβά 270 μοίρες δεξιόστροφα αφήνοντας τον προσανατολισμό της εικόνας αμετάβλητο.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Συμβουλή:** Εάν χρειάζεστε επίσης να αναστρέψετε την εικόνα οριζόντια ή κάθετα, επιλέξτε διαφορετικό `RotateFlipType` όπως `Rotate90FlipX` ή `Rotate180FlipY`.

### Βήμα 3: Μετατροπή PSD σε JPEG και αποθήκευση

`JpegOptions` ορίζει παραμέτρους ειδικές για JPEG όπως η ποιότητα συμπίεσης. Η μέθοδος `save` γράφει την μετασχηματισμένη εικόνα στο δίσκο στην επιθυμητή μορφή.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Το αρχείο `RotatedImage_out.jpg` τώρα περιέχει το αρχικό περιεχόμενο PSD περιστραμμένο 270 μοίρες και αποθηκευμένο ως JPEG.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Λύση |
|----------|------|
| **Η εικόνα εμφανίζεται ανάποδα** | Επιβεβαιώστε ότι χρησιμοποιήσατε `Rotate270FlipNone`. Για περιστροφή 90 μοίρες δεξιόστροφα χρησιμοποιήστε `Rotate90FlipNone`. |
| **Το αρχείο εξόδου είναι κατεστραμμένο** | Βεβαιωθείτε ότι ο φάκελος προορισμού υπάρχει και έχετε δικαιώματα εγγραφής. |
| **Πρόβλημα άδειας** | Εγκαταστήστε προσωρινή ή μόνιμη άδεια Aspose.PSD πριν φορτώσετε την εικόνα σε παραγωγή. |

## Συχνές Ερωτήσεις

**Ε: Είναι το Aspose.PSD συμβατό με διαφορετικές μορφές εικόνας;**  
Α: Ναι, το Aspose.PSD υποστηρίζει PSD, JPEG, PNG, BMP, GIF, TIFF και πολλές άλλες μορφές raster.

**Ε: Μπορώ να εφαρμόσω προσαρμοσμένες περιστροφές, όχι μόνο προεπιλεγμένες αναστροφές;**  
Α: Απόλυτα! Ενώ το `RotateFlipType` παρέχει κοινές γωνίες, μπορείτε να αλυσίδετε πολλαπλές κλήσεις ή να χρησιμοποιήσετε πίνακες μετασχηματισμού για αυθαίρετες γωνίες.

**Ε: Πώς να μετατρέψω το περιστραμμένο PSD σε άλλη μορφή, όπως PNG;**  
Α: Αντικαταστήστε το `JpegOptions` με `PngOptions` (ή την αντίστοιχη κλάση επιλογών) στη μέθοδο `save`.

**Ε: Πού μπορώ να βρω πρόσθετη υποστήριξη ή βοήθεια;**  
Α: Για βοήθεια από την κοινότητα, επισκεφθείτε το [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Ε: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
Α: Ναι, μπορείτε να εξερευνήσετε το Aspose.PSD με μια [δωρεάν δοκιμή](https://releases.aspose.com/).

**Ε: Πώς να αποκτήσω προσωρινή άδεια;**  
Α: Εάν χρειάζεστε προσωρινή άδεια, μπορείτε να την αποκτήσετε [εδώ](https://purchase.aspose.com/temporary-license/).

**Τελευταία ενημέρωση:** 2026-05-19  
**Δοκιμή με:** Aspose.PSD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Μετατροπή PSD σε μορφές Raster Image με Aspose.PSD για Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Μετατροπή PSD σε PNG και Περιστροφή Στρωμάτων σε αρχεία PSD χρησιμοποιώντας Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Πώς να Περιστρέψετε Εικόνα σε Java με Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}