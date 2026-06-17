---
date: 2026-02-20
description: Μάθετε πώς να υποστηρίζετε τις ιδιότητες εγγραφής μήκους και να επεξεργάζεστε
  μαζικά αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Οδηγός βήμα‑βήμα με παραδείγματα
  κώδικα.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Υποστήριξη Ιδιοτήτων Μητρώου Μήκους – Τροποποίηση Διανυσματικών Σχημάτων PSD
  (Java)
url: /el/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Υποστήριξη Ιδιοτήτων Εγγραφής Μήκους – Τροποποίηση Διανυσματικών Σχημάτων PSD (Java)

## Εισαγωγή
Αν χρειάζεστε να **τροποποιήσετε διανυσματικά σχήματα PSD** προγραμματιστικά, η βιβλιοθήκη Aspose.PSD for Java σας παρέχει πλήρη έλεγχο των αρχείων Photoshop απευθείας από τον κώδικα Java. Σε αυτό το tutorial θα καλύψουμε όλα όσα πρέπει να γνωρίζετε για να **υποστηρίξετε τις ιδιότητες εγγραφής μήκους** — ένα απαραίτητο βήμα όταν θέλετε να επεξεργαστείτε επίπεδα διανυσματικών σχημάτων. Στο τέλος, θα μπορείτε να ανοίξετε ένα PSD, να προσαρμόσετε τις ιδιότητες των διανυσματικών σχημάτων του και να αποθηκεύσετε το ενημερωμένο αρχείο χωρίς να φύγετε από το IDE σας. Ας ξεκινήσουμε!

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “τροποποίηση διανυσματικών σχημάτων PSD”;** Η προσαρμογή της γεωμετρίας, των λειτουργιών διαδρομής ή άλλων ιδιοτήτων των επιπέδων βασισμένων σε διανύσματα μέσα σε ένα αρχείο PSD.  
- **Ποια βιβλιοθήκη το διαχειρίζεται;** Aspose.PSD for Java.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Πόσο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για ένα βασικό script τροποποίησης σχήματος.  
- **Ποια είναι τα κύρια προαπαιτούμενα;** Java JDK, Aspose.PSD for Java και ένα δείγμα αρχείου PSD.

## Τι σημαίνει “υποστήριξη ιδιοτήτων εγγραφής μήκους”;
Η υποστήριξη των ιδιοτήτων εγγραφής μήκους σημαίνει πρόσβαση και ενημέρωση των αντικειμένων `LengthRecord` που περιγράφουν κάθε διανυσματική διαδρομή μέσα σε ένα PSD. Η αλλαγή αυτών των εγγραφών σας επιτρέπει να ελέγχετε πώς τα σχήματα συνδυάζονται, τέμνονται ή αφαιρούνται το ένα από το άλλο.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD for Java για την υποστήριξη ιδιοτήτων εγγραφής μήκους;
- **Δεν απαιτείται Photoshop** – εργασία απευθείας με αρχεία PSD σε οποιονδήποτε διακομιστή.  
- **Πλούσιο API** – πρόσβαση σε επίπεδα, πόρους και διανυσματικά δεδομένα με ισχυρά τυποποιημένες κλάσεις.  
- **Διαπλατφορμικό** – εκτέλεση σε Windows, Linux ή macOS με οποιοδήποτε JDK.  
- **Επικεντρωμένο στην απόδοση** – αποδοτική διαχείριση μνήμης και γρήγορες λειτουργίες αποθήκευσης.  

## Προαπαιτούμενα
1. **Java Development Kit (JDK)** – κατεβάστε από [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ή χρησιμοποιήστε τον προτιμώμενο διαχειριστή πακέτων σας.  
2. **Aspose.PSD for Java** – αποκτήστε το πιο πρόσφατο JAR από τη [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ή οποιονδήποτε επεξεργαστή συμβατό με Java.  
4. **Αρχείο PSD** – δημιουργήστε ένα στο Photoshop ή πάρτε ένα δείγμα PSD για πειραματισμό.  
5. **Βασικές γνώσεις Java** – εξοικείωση με κλάσεις, αντικείμενα και διαχείριση εξαιρέσεων.

## Εισαγωγή Πακέτων
Αρχικά, εισάγετε τις κλάσεις που θα χρειαστείτε για εργασία με αρχεία PSD και πόρους διανυσματικών σχημάτων.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Βήμα 1: Ρύθμιση των Καταλόγων Πηγής και Εξόδου
Ορίστε πού βρίσκεται το αρχικό PSD και πού θέλετε να αποθηκευτεί το τροποποιημένο αρχείο.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Βήμα 2: Φόρτωση του Αρχείου PSD
Χρησιμοποιήστε το `Image.load` για να ανοίξετε το αρχείο και κάντε cast σε `PsdImage` για λειτουργίες ειδικές του PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Βήμα 3: Εντοπισμός του Πόρου Vsms στο Επίπεδο
Τα δεδομένα διανυσματικού σχήματος βρίσκονται μέσα σε ένα `VsmsResource`. Κάντε επανάληψη στους πόρους του δεύτερου επιπέδου για να το βρείτε.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Βήμα 4: Πρόσβαση στις Εγγραφές Μήκους
Κάθε `LengthRecord` αντιπροσωπεύει μια ξεχωριστή διανυσματική διαδρομή. Πάρτε εκείνες που σκοπεύετε να τροποποιήσετε.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Βήμα 5: Τροποποίηση Ιδιοτήτων Λειτουργίας Διαδρομής
Τώρα μπορείτε να **τροποποιήσετε διανυσματικά σχήματα PSD** αλλάζοντας τις `PathOperations`. Αυτό καθορίζει πώς αλληλεπιδρούν τα σχήματα (π.χ., αποκλεισμός, τομή, αφαίρεση).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Βήμα 6: Αποθήκευση του Τροποποιημένου Αρχείου PSD
Αποθηκεύστε τις αλλαγές σας σε ένα νέο αρχείο.

```java
psdImage.save(outPsdFilePath);
```

## Βήμα 7: Καθαρισμός Πόρων
Αποδεσμεύστε το `PsdImage` για να ελευθερώσετε μνήμη.

```java
psdImage.dispose();
```

## Πώς να επεξεργαστείτε μαζικά αρχεία PSD με υποστήριξη ιδιοτήτων εγγραφής μήκους
Αν χρειάζεται να εφαρμόσετε τις ίδιες προσαρμογές διανυσματικών σχημάτων σε πολλά PSD, τυλίξτε τον παραπάνω κώδικα σε ένα βρόχο που διατρέχει έναν φάκελο αρχείων. Ενημερώστε τα `inPsdFilePath` και `outPsdFilePath` για κάθε επανάληψη και θα μπορείτε να **επεξεργάζεστε μαζικά αρχεία PSD** αποδοτικά.

## Συνηθισμένα Πιθανά Σφάλματα & Συμβουλές
- **Έλεγχοι null** – πάντα επαληθεύστε ότι το `resource` δεν είναι `null` πριν προσπελάσετε τις διαδρομές.  
- **Όρια δείκτη διαδρομής** – βεβαιωθείτε ότι οι δείκτες που χρησιμοποιείτε (`[2]`, `[7]`, `[11]`) υπάρχουν για το συγκεκριμένο PSD που επεξεργάζεστε.  
- **Άδεια** – η εκτέλεση χωρίς έγκυρη άδεια θα ενσωματώσει υδατογράφημα στο αποθηκευμένο PSD.  

## Συμπέρασμα
Τώρα έχετε ένα πλήρες, ολοκληρωμένο παράδειγμα για το πώς να **τροποποιήσετε διανυσματικά σχήματα PSD** υποστηρίζοντας τις ιδιότητες εγγραφής μήκους με το Aspose.PSD for Java. Είτε αυτοματοποιείτε pipelines περιουσιακών στοιχείων είτε δημιουργείτε ένα προσαρμοσμένο εργαλείο σχεδίασης, αυτά τα API σας δίνουν την ευελιξία να χειρίζεστε διανυσματικά επίπεδα χωρίς χειροκίνητη εργασία στο Photoshop. Εξερευνήστε περαιτέρω πειραματιζόμενοι με άλλες `PathOperations` ή συνδυάζοντας πολλαπλές επεμβάσεις `LengthRecord` για σύνθετα σχήματα.

## Συχνές Ερωτήσεις

**Q: Πώς να διαχειριστώ ένα PSD που δεν περιέχει επίπεδα διανυσματικών σχημάτων;**  
A: Το `VsmsResource` θα λείπει, έτσι το `resource` θα παραμείνει `null`. Προσθέστε έναν έλεγχο και παραλείψτε το βήμα τροποποίησης ή ενημερώστε τον χρήστη.

**Q: Μπορώ να αλλάξω άλλες ιδιότητες όπως το χρώμα γεμίσματος ή το πλάτος του περιγράμματος;**  
A: Ναι, το `LengthRecord` παρέχει πρόσθετους setters για γέμισμα, περίγραμμα και αδιαφάνεια. Ανατρέξτε στην τεκμηρίωση API για πλήρεις λεπτομέρειες.

**Q: Είναι δυνατόν να επεξεργαστείτε μαζικά πολλαπλά αρχεία PSD;**  
A: Απόλυτα. Τυλίξτε τον κώδικα μέσα σε έναν βρόχο που διατρέχει έναν φάκελο αρχείων PSD, προσαρμόζοντας τις διαδρομές εισόδου και εξόδου κάθε φορά.

**Q: Πρέπει να κλείσω τα streams χειροκίνητα όταν φορτώνω από διαδρομή αρχείου;**  
A: Η μέθοδος `Image.load` διαχειρίζεται τα streams αρχείων εσωτερικά, αλλά αν φορτώνετε από `InputStream`, θυμηθείτε να το κλείσετε μετά τη χρήση.

**Q: Ποια έκδοση του Aspose.PSD απαιτείται για αυτά τα API;**  
A: Οι κλάσεις `LengthRecord` και `PathOperations` είναι διαθέσιμες από το Aspose.PSD 20.10. Συνιστάται η χρήση της τελευταίας έκδοσης.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}