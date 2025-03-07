---
title: Προσθέστε ένα νέο κανονικό επίπεδο στο PSD με το Aspose.PSD για Java
linktitle: Προσθέστε ένα νέο κανονικό επίπεδο στο PSD
second_title: Aspose.PSD Java API
description: Μάθετε πώς μπορείτε να προσθέσετε ένα νέο κανονικό επίπεδο σε αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθήστε τον οδηγό βήμα προς βήμα για απρόσκοπτη χειραγώγηση PSD.
weight: 11
url: /el/java/advanced-image-effects/add-new-regular-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσθέστε ένα νέο κανονικό επίπεδο στο PSD με το Aspose.PSD για Java

## Εισαγωγή

Καλώς ήρθατε σε αυτό το ολοκληρωμένο σεμινάριο σχετικά με τη χρήση του Aspose.PSD για Java για την προσθήκη ενός νέου κανονικού επιπέδου σε ένα αρχείο PSD. Το Aspose.PSD είναι μια ισχυρή βιβλιοθήκη Java που επιτρέπει στους προγραμματιστές να χειρίζονται και να εργάζονται με αρχεία PSD αποτελεσματικά. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία προσθήκης ενός νέου κανονικού επιπέδου σε ένα αρχείο PSD, παρέχοντας λεπτομερή βήματα και παραδείγματα κώδικα.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Περιβάλλον ανάπτυξης Java: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα περιβάλλον ανάπτυξης Java στο σύστημά σας.
-  Aspose.PSD Library: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.PSD για Java. Μπορείτε να βρείτε τη βιβλιοθήκη[εδώ](https://releases.aspose.com/psd/java/).

## Εισαγωγή πακέτων

Για να ξεκινήσετε, εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java. Αυτά τα πακέτα είναι απαραίτητα για την εργασία με τις λειτουργίες Aspose.PSD. Συμπεριλάβετε τις ακόλουθες γραμμές στην αρχή του αρχείου σας Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Βήμα 1: Φόρτωση αρχείου PSD

Φορτώστε το αρχείο PSD που θέλετε να επεξεργαστείτε χρησιμοποιώντας τον ακόλουθο κώδικα:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Βήμα 2: Προετοιμάστε πίνακες δεδομένων και ορθογώνια

Προετοιμάστε δύο πίνακες int και δύο ορθογώνια αντικείμενα ως εξής:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Βήμα 3: Αρχικοποίηση δεδομένων επιπέδου

Αρχικοποιήστε πίνακες δεδομένων με προεπιλεγμένη τιμή:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Βήμα 4: Προσθέστε κανονικά επίπεδα

Προσθέστε δύο κανονικά επίπεδα στην εικόνα PSD:

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

## Βήμα 5: Αποθηκεύστε PSD και PNG

Αποθηκεύστε το τροποποιημένο PSD και ένα επιπλέον αρχείο PNG:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Συγχαρητήρια! Προσθέσατε με επιτυχία ένα νέο κανονικό επίπεδο σε ένα αρχείο PSD χρησιμοποιώντας το Aspose.PSD για Java.

## Σύναψη

Σε αυτό το σεμινάριο, καλύψαμε τη διαδικασία προσθήκης ενός νέου κανονικού επιπέδου σε ένα αρχείο PSD χρησιμοποιώντας το Aspose.PSD για Java. Αυτή η ισχυρή βιβλιοθήκη απλοποιεί τον χειρισμό του PSD, καθιστώντας το προσβάσιμο για προγραμματιστές Java. Πειραματιστείτε με διαφορετικές παραμέτρους και λειτουργίες για να εξερευνήσετε το πλήρες δυναμικό του Aspose.PSD.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.PSD συμβατό με Java 8;

A1: Ναι, το Aspose.PSD υποστηρίζει Java 8 και νεότερες εκδόσεις.

### Ε2: Μπορώ να εφαρμόσω μετασχηματισμούς στα επίπεδα που προστέθηκαν;

Α2: Απολύτως! Το Aspose.PSD παρέχει μια σειρά από επιλογές μετασχηματισμού για επίπεδα.

### Ε3: Πού μπορώ να βρω πρόσθετη τεκμηρίωση Aspose.PSD;

 A3: Μπορείτε να ανατρέξετε στην τεκμηρίωση[εδώ](https://reference.aspose.com/psd/java/).

### Ε4: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια για το Aspose.PSD;

 Α4: Επίσκεψη[αυτόν τον σύνδεσμο](https://purchase.aspose.com/temporary-license/) για προσωρινές επιλογές άδειας.

### Ε5: Υπάρχουν φόρουμ κοινότητας για υποστήριξη Aspose.PSD;

 A5: Ναι, μπορείτε να βρείτε υποστήριξη και συζητήσεις[εδώ](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
