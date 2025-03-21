---
title: Αλλαγή μεγέθους εικόνας ανάλογα με το Aspose.PSD για Java
linktitle: Αλλαγή μεγέθους εικόνας ανάλογα
second_title: Aspose.PSD Java API
description: Βελτιώστε τις εφαρμογές σας Java με το Aspose.PSD. Ακολουθήστε τον οδηγό μας για να αλλάξετε το μέγεθος των εικόνων αναλογικά χωρίς κόπο. Ενισχύστε τις δυνατότητες χειρισμού της εικόνας σας σήμερα.
weight: 17
url: /el/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αλλαγή μεγέθους εικόνας ανάλογα με το Aspose.PSD για Java

## Εισαγωγή

Καλώς ήρθατε στον αναλυτικό οδηγό μας για την αναλογική αλλαγή μεγέθους εικόνων χρησιμοποιώντας το Aspose.PSD για Java. Αν θέλετε να βελτιώσετε τις εφαρμογές σας Java με αποτελεσματικές δυνατότητες αλλαγής μεγέθους εικόνας, έχετε έρθει στο σωστό μέρος. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία χρησιμοποιώντας σαφή και συνοπτικά βήματα.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

1. Java Environment: Βεβαιωθείτε ότι έχετε εγκαταστήσει Java στο σύστημά σας.
2.  Aspose.PSD Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης Aspose.PSD. Μπορείτε να βρείτε τους απαραίτητους πόρους[εδώ](https://releases.aspose.com/psd/java/).

## Εισαγωγή πακέτων

Αφού ταξινομήσετε τις προϋποθέσεις σας, εισαγάγετε τα απαιτούμενα πακέτα στο έργο σας Java. Βεβαιωθείτε ότι η βιβλιοθήκη Aspose.PSD αναφέρεται σωστά στο έργο σας.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Βήμα 1: Φορτώστε την εικόνα

Ξεκινήστε φορτώνοντας την εικόνα που θέλετε να αλλάξετε το μέγεθος στην εφαρμογή Java.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Βήμα 2: Καθορίστε το πλάτος και το ύψος

Προσδιορίστε το νέο πλάτος και ύψος για την εικόνα που έχει αλλάξει μέγεθος. Σε αυτό το παράδειγμα, θα αλλάξουμε το μέγεθος της εικόνας στο ήμισυ των αρχικών της διαστάσεων.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Βήμα 3: Αποθηκεύστε την εικόνα με αλλαγή μεγέθους

Αποθηκεύστε το μέγεθος της εικόνας στην επιθυμητή θέση, καθορίζοντας τις επιλογές μορφής (PNG, σε αυτήν την περίπτωση).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Και ορίστε το! Αλλάξατε επιτυχώς το μέγεθος μιας εικόνας αναλογικά χρησιμοποιώντας το Aspose.PSD για Java.

## Σύναψη

Σε αυτό το σεμινάριο, καλύψαμε τα βασικά βήματα για την αναλογική αλλαγή μεγέθους εικόνων χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD για Java. Τώρα, μπορείτε να ενσωματώσετε αβίαστα αυτή τη λειτουργικότητα στις εφαρμογές σας Java για βελτιωμένο χειρισμό εικόνων.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.PSD συμβατό με όλες τις μορφές εικόνας;

 A1: Το Aspose.PSD υποστηρίζει διάφορες μορφές εικόνας, συμπεριλαμβανομένων των PSD, PNG, JPEG και άλλων. Ελέγξτε το[απόδειξη με έγγραφα](https://reference.aspose.com/psd/java/) για μια ολοκληρωμένη λίστα.

### Ε2: Μπορώ να χρησιμοποιήσω το Aspose.PSD για εμπορικά έργα;

 Α2: Ναι, μπορείς. Επισκεφθείτε το[σελίδα αγοράς](https://purchase.aspose.com/buy) για λεπτομέρειες αδειοδότησης.

### Ε3: Διατίθενται προσωρινές άδειες για δοκιμαστικούς σκοπούς;

 A3: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/) για αξιολόγηση.

### Ε4: Πού μπορώ να βρω υποστήριξη για το Aspose.PSD;

 A4: Επισκεφθείτε το[Φόρουμ Aspose.PSD](https://forum.aspose.com/c/psd/34) για κοινοτική υποστήριξη και βοήθεια.

### Ε5: Πώς μπορώ να έχω πρόσβαση στην τεκμηρίωση του Aspose.PSD;

 A5: Ανατρέξτε στη λεπτομερή τεκμηρίωση[εδώ](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
