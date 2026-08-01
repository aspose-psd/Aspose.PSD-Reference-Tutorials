---
date: 2026-08-01
description: Μάθετε πώς να εξάγετε PSD σε PNG και να διαχειριστείτε μη συμπιεσμένες
  ροές εικόνας με το Aspose.PSD για Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Διαχείριση αντικειμένου μη συμπιεσμένης ροής εικόνας σε PSD - Java
og_description: εξαγωγή psd σε png χρησιμοποιώντας το Aspose.PSD για Java. Μάθετε
  πώς να διαχειρίζεστε μη συμπιεσμένες ροές εικόνας, να δημιουργείτε αντικείμενα γραφικών
  και να αποθηκεύετε PNG υψηλής ποιότητας.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: εξαγωγή psd σε png – Οδηγός Java για μη συμπιεσμένες ροές PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Εξαγωγή PSD σε PNG – Δημιουργία αντικειμένου γραφικών PSD – Μη συμπιεσμένη
  ροή σε Java
url: /el/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή PSD σε PNG – Δημιουργία αντικειμένου γραφικών PSD – Ασυμπίεστη ροή σε Java

## Εισαγωγή
Σε αυτόν τον οδηγό βήμα‑βήμα θα **εξάγετε PSD σε PNG** ενώ εργάζεστε με μια ασυμπίεστη ροή εικόνας χρησιμοποιώντας το Aspose.PSD for Java. Είτε αυτοματοποιείτε μια γραμμή παραγωγής σχεδίου είτε δημιουργείτε έναν προσαρμοσμένο επεξεργαστή, η δυνατότητα απόδοσης ενός αρχείου Photoshop χωρίς απώλεια ποιότητας είναι ουσιώδης. Θα ξεκινήσουμε με τη απαιτούμενη ρύθμιση, θα περάσουμε από τη δημιουργία ενός αντικειμένου `Graphics` και θα ολοκληρώσουμε με μια εξαγωγή PNG χωρίς απώλειες. Στο τέλος, θα κατανοήσετε γιατί το Aspose.PSD διαχειρίζεται αποτελεσματικά τις ακατέργαστες ροές και πώς να το ενσωματώσετε σε οποιοδήποτε έργο Java.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “create PSD graphics object”;** Σημαίνει τη δημιουργία ενός πλαισίου `Graphics` που σας επιτρέπει να σχεδιάζετε ή να τροποποιείτε προγραμματιστικά μια εικόνα PSD.  
- **Ποια βιβλιοθήκη διαχειρίζεται τις ακατέργαστες ροές;** Το Aspose.PSD for Java παρέχει πλήρη υποστήριξη για ακατέργαστα (raw) δεδομένα εικόνας.  
- **Μπορώ να εξάγω PSD σε PNG μετά την επεξεργασία;** Ναι—αφού έχετε ένα αντικείμενο `Graphics`, μπορείτε να αποδώσετε το PSD και να το αποθηκεύσετε ως PNG με μία κλήση.  
- **Χρειάζεται άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.  
- **Η εξαγωγή είναι χωρίς απώλειες;** Η εξαγωγή σε PNG διατηρεί τα αρχικά δεδομένα pixel, προσφέροντας ποιότητα χωρίς απώλειες με μικρότερο μέγεθος αρχείου από το ακατέργαστο PSD.

## Τι είναι η εξαγωγή psd σε png;
Η εξαγωγή PSD σε PNG μετατρέπει ένα πολυεπίπεδο έγγραφο Photoshop σε μια μονοεπίπεδη, χωρίς απώλειες, εικόνα raster που μπορεί να εμφανιστεί από οποιονδήποτε φυλλομετρητή ή προβολέα εικόνων. Η διαδικασία διατηρεί τη διαφάνεια, το βάθος χρώματος και τα εφέ των επιπέδων, ενώ απορρίπτει τα μεταδεδομένα ειδικά για το Photoshop. Διατηρεί επίσης το αρχικό προφίλ χρώματος για ακριβή αναπαραγωγή χρωμάτων.

## Γιατί να χρησιμοποιήσω το Aspose.PSD for Java για επεξεργασία εικόνας;
Το Aspose.PSD υποστηρίζει **50+** μορφές εισόδου και εξόδου—συμπεριλαμβανομένων PSD, PNG, JPEG, BMP και TIFF—και μπορεί να επεξεργαστεί αρχεία με **200+ επίπεδα** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη. Η επιλογή συμπίεσης `Raw` αποθηκεύει τα δεδομένα pixel ακατέργαστα, εγγυώμενη τέλεια πιστότητα pixel για επόμενη επεξεργασία ή αρχειοθέτηση.

## Προαπαιτούμενα
Πριν βουτήξουμε στον κώδικα, βεβαιωθείτε ότι έχετε τα εξής:

- **Java Development Kit (JDK)** – Εγκατεστημένο JDK 8 ή νεότερο.  
- **Aspose.PSD for Java** – Κατεβάστε το τελευταίο JAR από τη σελίδα κυκλοφορίας: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). Μπορείτε επίσης να το αποκτήσετε μέσω [αυτού του συνδέσμου](https://releases.aspose.com/psd/java/) ή της [σελίδας κυκλοφορίας](https://releases.aspose.com/psd/java/). Για άλλα προϊόντα Aspose, κάντε κλικ [εδώ](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse ή οποιονδήποτε επεξεργαστή συμβατό με Java.  
- **Βασικές γνώσεις Java** – Εξοικείωση με κλάσεις, μεθόδους και διαχείριση εξαιρέσεων.

Με αυτά τα στοιχεία, είστε έτοιμοι να ξεκινήσετε τον κώδικα.

## Εισαγωγή Πακέτων
Η κλάση `Graphics` είναι η επιφάνεια σχεδίασης του Aspose.PSD που σας επιτρέπει να αποδίδετε ή να επεξεργάζεστε δεδομένα pixel άμεσα. Η κλάση `PsdImage` αντιπροσωπεύει ένα αρχείο PSD στη μνήμη, ενώ η `PsdOptions` ελέγχει πώς αποθηκεύεται η εικόνα.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Τώρα, ας αναλύσουμε τον κώδικα σε διαχειρίσιμα βήματα ώστε να μπορείτε να τον ακολουθήσετε εύκολα. Θα ρυθμίσουμε το περιβάλλον, θα φορτώσουμε ένα αρχείο PSD, θα το επεξεργαστούμε και τέλος θα αποθηκεύσουμε το αποτέλεσμα.

## Βήμα 1: Ορισμός του Καταλόγου Εγγράφων σας
Πριν από οποιαδήποτε λειτουργία αρχείου, πρέπει να ενημερώσετε το πρόγραμμα πού να ψάξει για τα αρχεία PSD. Αυτή η διαδρομή χρησιμοποιείται σε όλο το tutorial.

```java
String dataDir = "Your Document Directory";
```

Αντικαταστήστε το `"Your Document Directory"` με την απόλυτη διαδρομή που περιέχει το `layers.psd`. Η διατήρηση της διαδρομής ως παραμετρική καθιστά τον κώδικα επαναχρησιμοποιήσιμο σε διαφορετικά έργα.

## Βήμα 2: Δημιουργία Byte Array Output Stream
Το `ByteArrayOutputStream` είναι μια ροή Java που κρατά δεδομένα στη μνήμη ως πίνακα byte. Λειτουργεί ως ενδιάμεσος χώρος για την τροποποιημένη εικόνα, επιτρέποντάς σας να συλλάβετε τα ακατέργαστα byte πριν τα γράψετε στο δίσκο ή τα στείλετε μέσω δικτύου.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Η μεταβλητή `ms` θα περιέχει τα ακατέργαστα δεδομένα εικόνας μετά την ενέργεια `save`.

## Βήμα 3: Φόρτωση του Αρχείου PSD
Η κλάση `PsdImage` φορτώνει ένα αρχείο PSD στη μνήμη για επεξεργασία. Η φόρτωση του αρχείου μετατρέπει το PSD από το δίσκο σε ένα αντικείμενο `PsdImage` που μπορείτε να χειριστείτε. Σε αυτό το βήμα το Aspose.PSD διαβάζει την κεφαλίδα, τα επίπεδα και τους πόρους του αρχείου.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Αν η διαδρομή είναι λανθασμένη, το Aspose.PSD ρίχνει `FileNotFoundException`, το οποίο πρέπει να πιάσετε σε κώδικα παραγωγής.

## Βήμα 4: Ρύθμιση του PsdOptions για Αποθήκευση
Το `PsdOptions` καθορίζει τις παραμέτρους αποθήκευσης για αρχεία PSD. Ορίζοντας τη μέθοδο συμπίεσης σε `Raw` υποδεικνύει ότι τα δεδομένα pixel πρέπει να αποθηκευτούν χωρίς συμπίεση, διατηρώντας κάθε pixel ακριβώς όπως εμφανίζεται στη μνήμη.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Η επιλογή `CompressionMethod.Raw` αποθηκεύει τα δεδομένα pixel χωρίς καμία συμπίεση, κάτι που είναι ιδανικό όταν σκοπεύετε να κάνετε περαιτέρω επεξεργασίες αργότερα.

## Βήμα 5: Αποθήκευση της Εικόνας στο Output Stream
Τώρα αποθηκεύετε το PSD (με τυχόν τροποποιήσεις) στο προηγουμένως δημιουργημένο `ByteArrayOutputStream`. Η μέθοδος `save` σέβεται τις `PsdOptions` που διαμορφώσατε.

```java
psdImage.save(ms, saveOptions);
```

Σε αυτό το σημείο, το `ms` περιέχει την πλήρη δυαδική αναπαράσταση του ακατέργαστου PSD.

## Βήμα 6: Επαναφορά του Output Stream
Μετά τη γραφή, ο εσωτερικός δείκτης της ροής βρίσκεται στο τέλος. Η επαναφορά του (reset) επαναφέρει την ροή στην αρχή ώστε να μπορείτε να διαβάσετε από την αρχή.

```java
ms.reset();
```

Σκεφτείτε το ως μετακίνηση της κεφαλής ταινίας πίσω στην αρχή πριν από την αναπαραγωγή.

## Βήμα 7: Φόρτωση της Νεοδημιουργημένης Εικόνας
Τώρα μπορείτε να δημιουργήσετε μια νέα παρουσία `PsdImage` απευθείας από τον πίνακα byte. Αυτό το βήμα επαληθεύει ότι τα αποθηκευμένα δεδομένα μπορούν να ξαναφορτωθούν χωρίς διαφθορά.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Αν η εικόνα φορτωθεί επιτυχώς, ξέρετε ότι η ακατέργαστη ροή γράφτηκε σωστά.

## Βήμα 8: Δημιουργία Αντικειμένου Graphics
Η κλάση `Graphics` είναι ο καμβάς σχεδίασης του Aspose.PSD. Παρέχει μεθόδους για σχεδίαση σχημάτων, κειμένου και εφαρμογή φίλτρων απευθείας πάνω στο πλέγμα pixel ενός `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

Με αυτήν την παρουσία `Graphics` μπορείτε να ζωγραφίσετε νέο περιεχόμενο, να σβήσετε τμήματα ή να συνθέσετε επιπλέον επίπεδα.

## Πώς εξάγω PSD σε PNG χρησιμοποιώντας το Aspose.PSD for Java;
Φορτώστε το PSD με `new PsdImage(dataDir + "layers.psd")`, δημιουργήστε ένα αντικείμενο `Graphics`, εκτελέστε τις σχεδιαστικές ενέργειες που χρειάζεστε, έπειτα καλέστε `psdImage.save("output.png", new PngOptions())`. Αυτή η ακολουθία αποδίδει το επεξεργασμένο PSD και γράφει ένα PNG χωρίς απώλειες σε ένα βήμα, αξιοποιώντας τη μηχανή μετατροπής του Aspose.PSD.

## Επεξεργασία Επιπέδων PSD με το Αντικείμενο Graphics
Η ύπαρξη μιας παρουσίας `Graphics` σας δίνει έλεγχο σε επίπεδο pixel για κάθε επίπεδο. Μπορείτε να σχεδιάσετε γεωμετρικά σχήματα, να αποδώσετε κείμενο ή να εφαρμόσετε προσαρμοσμένα φίλτρα. Επειδή το πλαίσιο γραφικών λειτουργεί στην ραστεροποιημένη άποψη του επιπέδου, οι αλλαγές είναι άμεσα ορατές όταν αποθηκεύετε την εικόνα.

## Συνηθισμένα Προβλήματα και Λύσεις
- **NullPointerException κατά τη φόρτωση του αρχείου** – ελέγξτε ξανά τη διαδρομή `dataDir` και βεβαιωθείτε ότι το όνομα αρχείου ταιριάζει ακριβώς, συμπεριλαμβανομένης της ευαισθησίας σε πεζά‑κεφαλαία.  
- **Συμπιεσμένο αποτέλεσμα παρόλο που χρησιμοποιείται Raw** – βεβαιωθείτε ότι η κλήση `saveOptions.setCompressionMethod(CompressionMethod.Raw);` εκτελείται **πριν** την κλήση `save`.  
- **Το αντικείμενο Graphics εμφανίζεται κενό** – βεβαιωθείτε ότι σχεδιάζετε στο σωστό αντικείμενο `PsdImage` (αυτό που φορτώσατε, όχι σε μια νέα κενή εικόνα).  
- **OutOfMemoryError σε μεγάλα αρχεία** – χρησιμοποιήστε `PsdImage.load(dataDir, LoadOptions)` με `loadOptions.setLoadMode(LoadMode.Memory)` για ροή μεγάλων αρχείων χωρίς να φορτώνετε ολόκληρο το έγγραφο στη RAM.

## Συχνές Ερωτήσεις

### Τι είναι το Aspose.PSD;
Το Aspose.PSD είναι μια βιβλιοθήκη Java που επιτρέπει στους προγραμματιστές να δημιουργούν, να επεξεργάζονται και να μετατρέπουν αρχεία Photoshop PSD προγραμματιστικά χωρίς την ανάγκη του Adobe Photoshop. Υποστηρίζει ανάγνωση και εγγραφή αρχείων PSD, διαχείριση επιπέδων, μασκών, καναλιών και διαφόρων πόρων εικόνας, και παρέχει API για ραστερικές και διανυσματικές λειτουργίες, καθιστώντας το κατάλληλο για επεξεργασία εικόνας στο διακομιστή και αυτοματοποιημένες εργασίες.

### Πώς μπορώ να κατεβάσω το Aspose.PSD for Java;
Μπορείτε να το κατεβάσετε από τη σελίδα κυκλοφορίας: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Υπάρχει δωρεάν δοκιμή για το Aspose.PSD;
Ναι, μια πλήρως λειτουργική δοκιμή είναι διαθέσιμη στην ίδια σελίδα λήψης. Λειτουργεί για ανάπτυξη και αξιολόγηση.

### Μπορώ να λάβω υποστήριξη για το Aspose.PSD;
Απολύτως! Το φόρουμ υποστήριξης του Aspose παρέχει απαντήσεις από την ομάδα προϊόντος και την κοινότητα: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.PSD;
Μπορείτε να ζητήσετε προσωρινή άδεια απευθείας από το portal αδειοδότησης του Aspose, το οποίο παρέχει κλειδί περιορισμένου χρόνου έγκυρο για 30 ημέρες. Αυτό σας επιτρέπει να αξιολογήσετε τη πλήρη λειτουργικότητα του Aspose.PSD χωρίς αγορά εμπορικής άδειας. Μετά την περίοδο δοκιμής, πρέπει να αντικαταστήσετε το προσωρινό κλειδί με μόνιμη άδεια για να συνεχίσετε τη χρήση της βιβλιοθήκης σε παραγωγή. Επισκεφθείτε τη σελίδα προσωρινής άδειας για να δημιουργήσετε κλειδί περιορισμένου χρόνου: [temporary license page](https://purchase.aspose.com/temporary-license/).

## Συχνές Ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το αντικείμενο graphics για επεξεργασία μόνο ενός συγκεκριμένου επιπέδου;**  
Α: Ναι. Μετά τη φόρτωση του PSD, ανακτήστε το επιθυμητό επίπεδο μέσω `psdImage.getLayers().get_Item(index)` και περάστε αυτό το επίπεδο στον κατασκευαστή του `Graphics`.

**Ε: Η μέθοδος συμπίεσης Raw επηρεάζει το μέγεθος του αρχείου;**  
Α: Η Raw αποθηκεύει τα δεδομένα pixel χωρίς καμία συμπίεση, έτσι το τελικό αρχείο είναι μεγαλύτερο από ένα συμπιεσμένο PSD, αλλά εγγυάται 100 % πιστότητα pixel.

**Ε: Είναι δυνατόν να εξάγω το επεξεργασμένο PSD σε άλλη μορφή (π.χ., PNG);**  
Α: Απόλυτα. Μετά την επεξεργασία, καλέστε `psdImage.save("output.png", new PngOptions())`—αυτή είναι η τυπική μέθοδος για **εξαγωγή PSD σε PNG** με ποιότητα χωρίς απώλειες.

**Ε: Ποια έκδοση Java απαιτείται;**  
Α: Το Aspose.PSD for Java υποστηρίζει JDK 8 και νεότερες, συμπεριλαμβανομένων όλων των LTS εκδόσεων έως JDK 21.

**Ε: Πώς απελευθερώνω πόρους μετά την επεξεργασία;**  
Α: Καλείτε `psdImage.dispose()` και κλείνετε τυχόν ροές (π.χ., `ms.close()`) για να ελευθερώσετε τη φυσική μνήμη και να αποφύγετε διαρροές.

---

**Τελευταία ενημέρωση:** 2026-08-01  
**Δοκιμασμένο με:** Aspose.PSD for Java (τελευταία έκδοση)  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Tutorials

- [Save Images to Stream with Aspose.PSD for Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Export PSD Layer Group to Image using Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Create Image using Stream in Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}