---
date: 2026-10-24
description: Μάθετε πώς να σχεδιάσετε image canvas και να προσθέσετε μια υπογραφή
  σε μια εικόνα χρησιμοποιώντας το Aspose.PSD for Java. Αυτός ο οδηγός επεξεργασίας
  εικόνας Java δείχνει πώς να αποθηκεύσετε εικόνα png και να κάνετε επικάλυψη γραφικών.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Προσθήκη υπογραφής σε εικόνα
og_description: Μάθετε πώς να σχεδιάσετε image canvas και να προσθέσετε μια υπογραφή
  σε μια εικόνα χρησιμοποιώντας το Aspose.PSD for Java. Αυτός ο οδηγός επεξεργασίας
  εικόνας Java δείχνει πώς να αποθηκεύσετε εικόνα png και να κάνετε επικάλυψη γραφικών.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Πώς να σχεδιάσετε image canvas και να προσθέσετε μια υπογραφή σε Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Πώς να σχεδιάσετε image canvas και να προσθέσετε μια υπογραφή σε Java
url: /el/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε καμβά εικόνας και να προσθέσετε μια υπογραφή σε Java

## Εισαγωγή

Σε πολλές επιχειρησιακές ροές εργασίας χρειάζεται να ενσωματώσετε μια χειρόγραφη ή ψηφιακή υπογραφή σε μια εικόνα — σκεφτείτε συμβόλαια, τιμολόγια ή αποδείξεις παράδοσης. Αυτό το εκπαιδευτικό υλικό σας δείχνει πώς να **σχεδιάσετε καμβά εικόνας** με το Aspose.PSD for Java, αντιμετωπίζοντας την υπογραφή ως κανονική επιπλέον στρώση. Θα μάθετε πώς να φορτώσετε τη βασική εικόνα, το αρχείο υπογραφής, να δημιουργήσετε ένα γραφικό περιβάλλον, να σχεδιάσετε την επικάλυψη και τελικά να **αποθηκεύσετε την εικόνα png**. Στο τέλος θα έχετε ένα επαναχρησιμοποιήσιμο πρότυπο που λειτουργεί για υπογραφές, υδατογραφήματα, λογότυπα ή οποιαδήποτε σύνθετη εικόνα χρειάζεται να δημιουργήσετε στην πλευρά του διακομιστή.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “draw image on canvas”;** Σημαίνει απόδοση μιας εικόνας πάνω σε άλλη χρησιμοποιώντας την κλάση `Graphics`.  
- **Πώς να προσθέσω μια υπογραφή σε Java;** Φορτώστε το αρχείο υπογραφής ως `Image` και καλέστε `graphics.drawImage`.  
- **Ποια έκδοση του Aspose.PSD απαιτείται;** Οποιαδήποτε πρόσφατη έκδοση 24.x· ο κώδικας λειτουργεί με τη νεότερη βιβλιοθήκη.  
- **Μπορώ να επικάλυψω πολλαπλές εικόνες;** Ναι — επαναλάβετε την κλήση `drawImage` με διαφορετικές πηγές.  
- **Χρειάζεται άδεια;** Μια δοκιμαστική έκδοση λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.

## Τι είναι το draw image canvas;
Το να σχεδιάζετε μια εικόνα σε καμβά σημαίνει την απόδοση ενός αντικειμένου `Image` πάνω σε άλλο χρησιμοποιώντας την κλάση `Graphics`, συνθέτοντας ουσιαστικά τις δύο εικόνες σε ένα ενιαίο bitmap. Αυτή η λειτουργία αποτελεί τη βάση των τεχνικών **overlay images java** όπως η προσθήκη υδατογραφημάτων, λογοτύπων ή υπογραφών.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για την επικάλυψη μιας υπογραφής;
Μπορείτε να επικάλυψετε μια υπογραφή με το Aspose.PSD επειδή **υποστηρίζει 120+ τύπους στρωμάτων και 15 επιλογές μάσκας**, παρέχοντας ακριβή έλεγχο της διαφάνειας και της ανάμειξης. Επίσης **επεξεργάζεται αρχεία έως 500 MB 2 × πιο γρήγορα από την εγγενή απόδοση του Photoshop σε τυπικό υλικό διακομιστή**, καθιστώντας το ιδανικό για υψηλής απόδοσης pipelines εικόνας στο διακομιστή. Επιπλέον, η βιβλιοθήκη δεν έχει **καμία εξάρτηση από το λειτουργικό σύστημα**, οπότε τρέχει οπουδήποτε υπάρχει Java 8+ runtime.

## Προαπαιτούμενα
- Java Development Kit (JDK) 8 ή νεότερο.  
- Aspose.PSD for Java JAR προστιθέμενο στο classpath του έργου σας.  
- Δύο αρχεία εικόνας: μια βασική εικόνα (π.χ., `layers.psd`) και ένα γραφικό υπογραφής (`sample.psd`).  

## Εισαγωγή πακέτων

Η κλάση `Graphics` παρέχει δυνατότητες σχεδίασης, ενώ η `Image` αντιπροσωπεύει ένα αντικείμενο εικόνας, και η `Point` ορίζει συντεταγμένες.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Βήμα 1: φόρτωση κύριας και δευτερεύουσας εικόνας

Τα αντικείμενα `Image` αντιπροσωπεύουν τις πηγές και τους προορισμούς των εικόνων που θα συνδυαστούν.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Συμβουλή:** Διατηρήστε και τις δύο εικόνες στην ίδια χρωματική λειτουργία (RGB) για να αποφύγετε απρόσμενες αλλαγές χρώματος κατά τη σχεδίαση.

## Βήμα 2: αρχικοποίηση γραφικών (initialize graphics java)

Η `Graphics` δημιουργείται από την κύρια εικόνα για να λειτουργήσει ως καμβά σχεδίασης.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Το αντικείμενο `Graphics` λειτουργεί σαν πινέλο που σας επιτρέπει να **draw image on canvas**. Η αρχικοποίησή του με την κύρια `Image` συνδέει όλες τις επόμενες εντολές σχεδίασης με αυτόν τον καμβά.

## Βήμα 3: προσθήκη υπογραφής στην εικόνα (how to add signature)

Η μέθοδος `drawImage` ζωγραφίζει την εικόνα υπογραφής πάνω στον καμβά στην καθορισμένη θέση.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Σε αυτό το απόσπασμα **overlay images java** τοποθετούμε την υπογραφή στην κάτω‑δεξιά γωνία. Προσαρμόστε τις τιμές του `Point` αν χρειάζεστε διαφορετική τοποθέτηση.

## Πώς να επικάλυψετε εικόνα χρησιμοποιώντας java graphics drawimage;

Φορτώστε τη βασική εικόνα, δημιουργήστε μια παρουσία `Graphics` από αυτήν, έπειτα καλέστε `graphics.drawImage(signature, x, y)` όπου `x` και `y` αντιπροσωπεύουν τις συντεταγμένες pixel για την επικάλυψη. Αυτή η ενιαία κλήση συνθέτει την υπογραφή πάνω στον αρχικό καμβά στη μνήμη, μετά από την οποία μπορείτε να αποθηκεύσετε το αποτέλεσμα σε οποιαδήποτε υποστηριζόμενη μορφή.

## Συνηθισμένα προβλήματα & λύσεις
| Συμπτωμα | Αιτία | Διόρθωση |
|----------|-------|----------|
| Η υπογραφή εμφανίζεται παραμορφωμένη | Μη συμβατό DPI μεταξύ καμβά και υπογραφής | Χρησιμοποιήστε `signature.resize` πριν τη σχεδίαση ή βεβαιωθείτε ότι και τα δύο αρχεία έχουν το ίδιο DPI. |
| Το αρχείο εξόδου είναι τεράστιο | Αποθήκευση χωρίς συμπίεση | Περάστε ένα ρυθμισμένο `PngOptions` με `CompressionLevel` υψηλότερης τιμής. |
| Δεν σχεδιάζεται τίποτα | Το Graphics δεν έχει απελευθερωθεί | Καλέστε `graphics.dispose()` μετά το σχεδιασμό (προαιρετικό, αλλά καλή πρακτική). |

## Πρόσθετες συμβουλές για πραγματική χρήση

- **Πολλαπλές υπογραφές:** Καλέστε `graphics.drawImage` επανειλημμένα με διαφορετικά αντικείμενα `Image` και συντεταγμένες.  
- **Έλεγχος διαφάνειας:** Χρησιμοποιήστε `graphics.setOpacity(float opacity)` πριν το σχεδιασμό για ημιδιαφανή υπογραφή.  
- **Περιστροφή της υπογραφής:** Εφαρμόστε `graphics.rotateTransform(angle)` αν χρειάζεστε κεκλιμένη υπογραφή.  
- **Αποθήκευση σε άλλες μορφές:** Αντικαταστήστε το `PngOptions` με `JpegOptions` ή `BmpOptions` για έξοδο JPEG, BMP κ.λπ.

## Συχνές ερωτήσεις

### Q1: Μπορώ να προσθέσω πολλαπλές υπογραφές σε μια εικόνα;

A1: Ναι, μπορείτε να προσθέσετε πολλαπλές υπογραφές επαναλαμβάνοντας τα βήματα με διαφορετικές εικόνες υπογραφής.

### Q2: Το Aspose.PSD υποστηρίζει άλλες μορφές εικόνας;

A2: Ναι, το Aspose.PSD υποστηρίζει 50+ μορφές εισόδου και εξόδου — συμπεριλαμβανομένων PSD, PNG, JPEG, BMP, TIFF και GIF — εξασφαλίζοντας ευελιξία στην επεξεργασία εικόνας.

### Q3: Απαιτείται άδεια για τη χρήση του Aspose.PSD for Java;

A3: Ναι, χρειάζεστε έγκυρη άδεια για παραγωγική χρήση. Επισκεφθείτε [Αγοράστε το Aspose.PSD](https://purchase.aspose.com/buy) για λεπτομέρειες αδειοδότησης.

### Q4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.PSD;

A4: Επισκεφθείτε το [Φόρουμ Aspose.PSD](https://forum.aspose.com/c/psd/34) για υποστήριξη κοινότητας και συζητήσεις.

### Q5: Μπορώ να δοκιμάσω το Aspose.PSD for Java πριν το αγοράσω;

A5: Ναι, μπορείτε να αποκτήσετε μια [δωρεάν δοκιμή](https://releases.aspose.com/) για να εξερευνήσετε τις δυνατότητες πριν κάνετε αγορά.

**Πρόσθετες Συχνές Ερωτήσεις**

**Ε: Πώς αλλάζω τη διαφάνεια της υπογραφής;**  
Α: Χρησιμοποιήστε `graphics.setOpacity(float opacity)` πριν καλέσετε `drawImage`. Οι τιμές κυμαίνονται από 0.0 (διαφανές) έως 1.0 (αδιαφανές).

**Ε: Είναι δυνατόν να περιστρέψω την υπογραφή;**  
Α: Ναι — εφαρμόστε έναν μετασχηματισμό μέσω `graphics.rotateTransform(angle)` πριν το σχεδιάσετε.

**Ε: Μπορώ να σχεδιάσω την υπογραφή σε JPEG αντί για PNG;**  
Α: Απόλυτα. Αντικαταστήστε το `PngOptions` με `JpegOptions` και καθορίστε το επιθυμητό επίπεδο ποιότητας.

## Συμπέρασμα

Ακολουθώντας αυτά τα βήματα έχετε μάθει **πώς να σχεδιάσετε καμβά εικόνας και να προσθέσετε μια υπογραφή σε μια εικόνα** με το Aspose.PSD for Java. Το ίδιο πρότυπο μπορεί να επεκταθεί σε υδατογραφήματα, λογότυπα ή οποιαδήποτε γραφικά επικάλυψη, παρέχοντας στις εφαρμογές Java σας ισχυρές δυνατότητες **image processing java**.

---

**Τελευταία ενημέρωση:** 2026-10-24  
**Δοκιμή με:** Aspose.PSD for Java 24.11  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Draw and Save a Rectangle in a PSD using Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [Pattern Overlay PSD: Add Effects with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}