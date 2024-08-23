---
title: Εκτελέστε απλό σχέδιο με το Aspose.PSD για Java
linktitle: Εκτελέστε απλό σχέδιο
second_title: Aspose.PSD Java API
description: Μάθετε πώς να σχεδιάζετε σχήματα σε αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Αυτός ο οδηγός βήμα προς βήμα καλύπτει τη δημιουργία, την προσθήκη επιπέδων και τη σχεδίαση με παραδείγματα κώδικα.
type: docs
weight: 10
url: /el/java/basic-image-operations/simple-drawing/
---
## Εισαγωγή

Καλώς ήρθατε σε αυτόν τον οδηγό βήμα προς βήμα για την εκτέλεση απλών σχεδίων χρησιμοποιώντας το Aspose.PSD για Java! Σε αυτό το σεμινάριο, θα εξερευνήσουμε τα βασικά για τη δημιουργία ενός νέου εγγράφου PSD, την προσθήκη επιπέδων και τη σχεδίαση σχημάτων με διαφορετικά χρώματα. Το Aspose.PSD για Java είναι μια ισχυρή βιβλιοθήκη που σας δίνει τη δυνατότητα να χειρίζεστε αρχεία PSD μέσω προγραμματισμού, παρέχοντας εκτεταμένη λειτουργικότητα για εργασίες γραφικού σχεδιασμού.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Το Java Development Kit (JDK) είναι εγκατεστημένο στο μηχάνημά σας.
- Aspose.PSD για βιβλιοθήκη Java. Μπορείτε να το κατεβάσετε από το[Aspose.PSD για τεκμηρίωση Java](https://reference.aspose.com/psd/java/).

## Εισαγωγή πακέτων

Για να ξεκινήσετε, εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java. Συμπεριλάβετε τον ακόλουθο κώδικα στην αρχή του αρχείου σας Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Βήμα 1: Δημιουργήστε ένα νέο έγγραφο

Ας ξεκινήσουμε δημιουργώντας ένα νέο έγγραφο PSD με καθορισμένο πλάτος και ύψος:

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Βήμα 2: Προσθέστε ένα επίπεδο

Τώρα, ας προσθέσουμε ένα επίπεδο στο έγγραφο χρησιμοποιώντας τον κατασκευαστή χωρίς όρισμα:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Βήμα 3: Σχεδιάστε σχήματα

Σε αυτό το βήμα, θα χρησιμοποιήσουμε την κλάση Graphics για να σχεδιάσουμε σχήματα στο δημιουργημένο επίπεδο:

### Σχεδιάστε ένα ορθογώνιο με κίτρινο χρώμα

```java
//ExStart:DrawRectangle Yellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangle Yellow
```

### Σχεδιάστε ένα κόκκινο ορθογώνιο

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Σχεδιάστε ένα μπλε ορθογώνιο

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Βήμα 4: Αποθηκεύστε τις Αλλαγές

Τέλος, αποθηκεύστε ένα αντίγραφο του φορτωμένου αρχείου PSD συμπεριλαμβανομένων των αλλαγών:

```java
//ExStart: SaveChanges
image.save(outPsdFilePath);
//ExEnd: SaveChanges
```

## Σύναψη

Συγχαρητήρια! Πραγματοποιήσατε με επιτυχία ένα απλό σχέδιο χρησιμοποιώντας το Aspose.PSD για Java. Αυτό το σεμινάριο κάλυψε τη δημιουργία ενός νέου εγγράφου, την προσθήκη επιπέδων και τη σχεδίαση ορθογωνίων με διαφορετικά χρώματα. Μη διστάσετε να εξερευνήσετε πιο προηγμένες λειτουργίες που προσφέρει η βιβλιοθήκη για τις ανάγκες σας στο γραφικό σχεδιασμό.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.PSD για Java για να χειριστώ υπάρχοντα αρχεία PSD;

A1: Ναι, το Aspose.PSD για Java παρέχει εκτεταμένες λειτουργίες για την επεξεργασία και τον χειρισμό υπαρχόντων αρχείων PSD.

### Ε2: Πού μπορώ να βρω υποστήριξη για το Aspose.PSD για Java;

 A2: Μπορείτε να επισκεφθείτε το[Aspose.PSD για Java Forum](https://forum.aspose.com/c/psd/34) για τυχόν ερωτήματα που σχετίζονται με την υποστήριξη.

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.PSD για Java;

 A3: Ναι, μπορείτε να έχετε πρόσβαση στη δωρεάν δοκιμαστική έκδοση[εδώ](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να αγοράσω άδεια χρήσης για το Aspose.PSD για Java;

 A4: Μπορείτε να αγοράσετε μια άδεια από το[Σελίδα αγοράς Aspose.PSD](https://purchase.aspose.com/buy).

### Ε5: Διατίθενται προσωρινές άδειες χρήσης για το Aspose.PSD για Java;

 A5: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια από[εδώ](https://purchase.aspose.com/temporary-license/).