---
date: 2025-12-02
description: Μάθετε πώς να σχεδιάζετε εικόνα σε καμβά και να προσθέτετε μια υπογραφή
  σε Java χρησιμοποιώντας το Aspose.PSD. Ακολουθήστε αυτό το βήμα‑βήμα tutorial επεξεργασίας
  εικόνας σε Java και αποθηκεύστε το αποτέλεσμα ως PNG.
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Σχεδίαση εικόνας σε καμβά – Προσθήκη υπογραφής με το Aspose.PSD για Java
url: /el/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Σχεδίαση Εικόνας σε Καμβά – Προσθήκη Υπογραφής με Aspose.PSD for Java

## Εισαγωγή

Η προσθήκη χειρόγραφης ή ψηφιακής υπογραφής σε μια εικόνα είναι συχνή απαίτηση για συμβόλαια, τιμολόγια ή οποιοδήποτε έγγραφο που χρειάζεται απόδειξη αυθεντικότητας. Με το **Aspose.PSD for Java** μπορείτε να **draw image on canvas** και να αντιμετωπίζετε την υπογραφή ως απλώς μια επιπλέον στρώση επικάλυψης. Σε αυτό το **java image processing tutorial** θα περάσουμε από όλη τη ροή εργασίας — από τη φόρτωση της βασικής εικόνας και του αρχείου υπογραφής, μέχρι την αρχικοποίηση γραφικών, τη σχεδίαση της επικάλυψης και, τέλος, το **save image png java**‑στυλ.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει το “draw image on canvas”;** Αναφέρεται στην απόδοση μιας εικόνας πάνω σε άλλη χρησιμοποιώντας την κλάση `Graphics`.  
- **Πώς να προσθέσω μια υπογραφή σε Java;** Φορτώστε το αρχείο υπογραφής ως `Image` και χρησιμοποιήστε `Graphics.drawImage`.  
- **Ποια έκδοση του Aspose.PSD απαιτείται;** Οποιαδήποτε πρόσφατη έκδοση 24.x· ο κώδικας λειτουργεί με την τελευταία βιβλιοθήκη.  
- **Μπορώ να επικάλυψω πολλαπλές εικόνες;** Ναι — επαναλάβετε την κλήση `drawImage` με διαφορετικές πηγές.  
- **Χρειάζεται άδεια;** Μια δοκιμαστική έκδοση λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.

## Τι είναι το “Draw Image on Canvas”;
Στην ορολογία του Aspose.PSD, η σχεδίαση μιας εικόνας σε καμβά σημαίνει την βαφή ενός αντικειμένου `Image` πάνω σε άλλο χρησιμοποιώντας ένα πλαίσιο `Graphics`. Αυτή η λειτουργία αποτελεί τη ραχοκοκαλιά των τεχνικών **overlay images java** όπως η προσθήκη υδατογραφήματος, λογότυπων ή υπογραφών.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για την επικάλυψη μιας υπογραφής;
- **Πλήρης υποστήριξη PSD** – λειτουργεί με στρώσεις, μάσκες και διαφάνεια.  
- **Χωρίς εξαρτήσεις από το λειτουργικό σύστημα** – καθαρά Java, ιδανικό για επεξεργασία στο διακομιστή.  
- **Απόδοση υψηλής ταχύτητας** – βελτιστοποιημένο για μεγάλα αρχεία και σύνθετες συνθέσεις.  

## Προαπαιτούμενα
- Java Development Kit (JDK) 8 ή νεότερο.  
- Aspose.PSD for Java JAR προστιθέμενο στο classpath του έργου σας.  
- Δύο αρχεία εικόνας: μια βασική εικόνα (π.χ., `layers.psd`) και ένα γραφικό υπογραφής (`sample.psd`).  

## Εισαγωγή Πακέτων

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Βήμα 1: Φόρτωση Πρωτεύουσας και Δευτερεύουσας Εικόνας

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Συμβουλή:** Κρατήστε και τις δύο εικόνες στην ίδια λειτουργία χρώματος (RGB) για να αποφύγετε απρόσμενες αλλαγές χρώματος κατά τη σχεδίαση.

## Βήμα 2: Αρχικοποίηση Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Το αντικείμενο `Graphics` λειτουργεί σαν πινέλο που σας επιτρέπει να **draw image on canvas**. Η αρχικοποίησή του με την πρωτεύουσα `Image` συνδέει όλες τις επόμενες εντολές σχεδίασης με αυτόν τον καμβά.

## Βήμα 3: Προσθήκη Υπογραφής στην Εικόνα (how to add signature)

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

Σε αυτό το απόσπασμα **overlay images java** τοποθετούμε την υπογραφή στην κάτω‑δεξιά γωνία. Προσαρμόστε τις τιμές του `Point` εάν χρειάζεστε διαφορετική θέση.

## Κοινά Προβλήματα & Λύσεις
| Σύμπτωμα | Αιτία | Διόρθωση |
|---------|-------|----------|
| Η υπογραφή εμφανίζεται παραμορφωμένη | Μη συμβατό DPI μεταξύ καμβά και υπογραφής | Χρησιμοποιήστε `signature.resize` πριν τη σχεδίαση ή βεβαιωθείτε ότι και τα δύο αρχεία έχουν το ίδιο DPI. |
| Το αρχείο εξόδου είναι τεράστιο | Αποθήκευση χωρίς συμπίεση | Περάστε ένα ρυθμισμένο `PngOptions` με `CompressionLevel` ορισμένο σε υψηλότερη τιμή. |
| Δεν σχεδιάζεται τίποτα | Το Graphics δεν έχει διαγραφεί | Καλέστε `graphics.dispose()` μετά τη σχεδίαση (προαιρετικό, αλλά καλή πρακτική). |

## Συμπέρασμα

Ακολουθώντας αυτά τα βήματα έχετε μάθει **πώς να draw image on canvas** και να προσθέτετε απρόσκοπτα μια **υπογραφή** χρησιμοποιώντας το Aspose.PSD for Java. Αυτή η τεχνική μπορεί να επεκταθεί σε υδατογραφήματα, λογότυπα ή οποιαδήποτε γραφικά επικάλυψη, προσφέροντας στις εφαρμογές Java σας ισχυρές δυνατότητες **java image processing**.

## Συχνές Ερωτήσεις

### Q1: Μπορώ να προσθέσω πολλαπλές υπογραφές σε μια εικόνα;

A1: Ναι, μπορείτε να προσθέσετε πολλαπλές υπογραφές επαναλαμβάνοντας τα βήματα με διαφορετικές εικόνες υπογραφής.

### Q2: Υποστηρίζει το Aspose.PSD άλλες μορφές εικόνας;

A2:, το Aspose.PSD υποστηρίζει ένα ευρύ φάσμα μορφών εικόνας, εξασφαλίζοντας ευελιξία στην επεξεργασία εικόνας.

### Q3: Απαιτείται άδεια για τη χρήση του Aspose.PSD for Java;

A3: Ναι, χρειάζεστε έγκυρη άδεια για τη χρήση του Aspose.PSD. Επισκεφθείτε [Purchase Aspose.PSD](https://purchase.aspose.com/buy) για λεπτομέρειες αδειοδότησης.

### Q4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.PSD;

A4: Επισκεφθείτε το [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) για υποστήριξη κοινότητας και συζητήσεις.

### Q5: Μπορώ να δοκιμάσω το Aspose.PSD for Java πριν το αγοράσω;

A5: Ναι, μπορείτε να αποκτήσετε [free trial](https://releases.aspose.com/) για να εξερευνήσετε τις δυνατότητες πριν κάνετε την αγορά.

## Πρόσθετες Συχνές Ερωτήσεις

**Ε: Πώς αλλάζω τη διαφάνεια της υπογραφής;**  
Α: Χρησιμοποιήστε `graphics.setOpacity(float opacity)` πριν καλέσετε `drawImage`. Οι τιμές κυμαίνονται από 0.0 (διαφανές) έως 1.0 (αδιαφανές).

**Ε: Είναι δυνατόν να περιστρέψω την υπογραφή;**  
Α: Ναι — εφαρμόστε έναν πίνακα μετασχηματισμού μέσω `graphics.rotateTransform(angle)` πριν τη σχεδίαση.

**Ε: Μπορώ να σχεδιάσω την υπογραφή σε JPEG αντί για PNG;**  
Α: Απόλυτα. Αντικαταστήστε το `PngOptions` με `JpegOptions` και καθορίστε το επιθυμητό επίπεδο ποιότητας.

---

**Τελευταία Ενημέρωση:** 2025-12-02  
**Δοκιμάστηκε Με:** Aspose.PSD for Java 24.11  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}