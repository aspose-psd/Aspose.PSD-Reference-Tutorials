---
title: Υποστήριξη Shadow Effect στο Aspose.PSD για Java
linktitle: Υποστήριξη εφέ σκιάς
second_title: Aspose.PSD Java API
description: Μάθετε πώς να προσθέτετε εντυπωσιακά εφέ σκιάς σε εικόνες χρησιμοποιώντας το Aspose.PSD για Java. Αναβαθμίστε το γραφικό σας σχέδιο με αυτό το βήμα προς βήμα σεμινάριο.
type: docs
weight: 13
url: /el/java/basic-image-operations/support-shadow-effect/
---
## Εισαγωγή

Η βελτίωση των εικόνων με εφέ σκιάς είναι μια κοινή πρακτική στη γραφιστική, προσθέτοντας βάθος και ρεαλισμό. Το Aspose.PSD για Java παρέχει ισχυρή υποστήριξη για εφέ σκιάς, επιτρέποντας στους προγραμματιστές να ενσωματώνουν αβίαστα αυτά τα εφέ στις εφαρμογές Java τους. Σε αυτό το σεμινάριο, θα εξερευνήσουμε πώς να υποστηρίξουμε εφέ σκιών χρησιμοποιώντας το Aspose.PSD, βήμα προς βήμα.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Βασικές γνώσεις προγραμματισμού Java.
-  Εγκαταστάθηκε το Aspose.PSD για Java. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/psd/java/).

## Εισαγωγή πακέτων

Βεβαιωθείτε ότι έχετε εισαγάγει τα απαραίτητα πακέτα για να αξιοποιήσετε τις λειτουργίες Aspose.PSD στην εφαρμογή Java. Χρησιμοποιήστε το ακόλουθο απόσπασμα κώδικα ως οδηγό:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Βήμα 1: Φορτώστε την εικόνα PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Βήμα 2: Ανάκτηση εφέ σκιάς

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Βήμα 3: Επαληθεύστε τις προεπιλεγμένες ρυθμίσεις

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## Βήμα 4: Προσαρμόστε το εφέ σκιάς

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Βήμα 5: Αποθηκεύστε την τροποποιημένη εικόνα

```java
im.save(psdPathAfterChange);
```

## συμπέρασμα

Με αυτά τα απλά βήματα, μπορείτε να υποστηρίξετε αβίαστα εφέ σκιών στο Aspose.PSD για Java, βελτιώνοντας την οπτική ελκυστικότητα των εικόνων σας.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.PSD για Java κατάλληλο για επαγγελματικά έργα γραφιστικής;

Α1: Απολύτως! Το Aspose.PSD για Java είναι μια ισχυρή βιβλιοθήκη σχεδιασμένη για επαγγελματικές εργασίες γραφιστικής.

### Ε2: Μπορώ να χρησιμοποιήσω το Aspose.PSD για Java σε εμπορικές εφαρμογές;

 A2: Ναι, το Aspose.PSD για Java είναι ένα εμπορικό προϊόν. Μπορείτε να το αγοράσετε[εδώ](https://purchase.aspose.com/buy).

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

 A3: Ναι, μπορείτε να εξερευνήσετε μια δωρεάν δοκιμαστική έκδοση[εδώ](https://releases.aspose.com/).

### Ε4: Πού μπορώ να βρω λεπτομερή τεκμηρίωση;

 A4: Ανατρέξτε στην πλήρη τεκμηρίωση[εδώ](https://reference.aspose.com/psd/java/).

### Ε5: Πώς μπορώ να λάβω υποστήριξη για το Aspose.PSD για Java;

 A5: Εγγραφείτε στο φόρουμ της κοινότητας[εδώ](https://forum.aspose.com/c/psd/34) για τυχόν απορίες υποστήριξης.