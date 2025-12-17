---
date: 2025-12-17
description: Μάθετε πώς να τροποποιείτε τα διανυσματικά σχήματα PSD υποστηρίζοντας
  τις ιδιότητες δεδομένων εγγραφής μήκους χρησιμοποιώντας το Aspose.PSD για Java.
  Οδηγός βήμα‑βήμα με παραδείγματα κώδικα.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Πώς να τροποποιήσετε τα διανυσματικά σχήματα PSD – Υποστήριξη ιδιοτήτων δεδομένων
  εγγραφής μήκους σε Java
url: /el/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Υποστήριξη Ιδιοτήτων Δεδομένων Μήκους Εγγραφής σε PSD - Java

## Εισαγωγή
Αν χρειάζεστε να **modify PSD vector shapes** προγραμματιστικά, η βιβλιοθήκη Aspose.PSD for Java σας δίνει πλήρη έλεγχο στα αρχεία Photoshop απευθείας από τον κώδικα Java. Σε αυτό το tutorial θα καλύψουμε όλα όσα πρέπει να γνωρίζετε για την υποστήριξη ιδιοτήτων δεδομένων μήκους εγγραφής — ένα απαραίτητο βήμα όταν θέλετε να επεξεργαστείτε στρώματα διανυσματικών σχημάτων. Στο τέλος, θα μπορείτε να ανοίξετε ένα PSD, να τροποποιήσετε τις ιδιότητες των διανυσματικών σχημάτων του και να αποθηκεύσετε το ενημερωμένο αρχείο χωρίς να φύγετε ποτέ από το IDE σας. Ας ξεκινήσουμε!

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “modify PSD vector shapes”;** Προσαρμογή της γεωμετρίας, των λειτουργιών διαδρομής ή άλλων ιδιοτήτων των στρωμάτων βασισμένων σε διανύσματα μέσα σε ένα αρχείο PSD.  
- **Ποια βιβλιοθήκη το διαχειρίζεται;** Aspose.PSD for Java.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Πόσο χρόνο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για ένα βασικό script τροποποίησης σχήματος.  
- **Ποια είναι τα κύρια προαπαιτούμενα;** Java JDK, Aspose.PSD for Java και ένα δείγμα αρχείου PSD.

## Τι είναι το “modify PSD vector shapes”;
Η τροποποίηση PSD vector shapes περιλαμβάνει την αλλαγή των υποκείμενων δεδομένων διανυσματικής διαδρομής — όπως τα length records και οι λειτουργίες διαδρομής — ώστε η οπτική εμφάνιση των σχημάτων ενημερώνεται αναλόγως. Αυτό είναι ιδιαίτερα χρήσιμο για αυτοματοποιημένες γραφικές γραμμές παραγωγής, επεξεργασία παρτίδας ή προσαρμοσμένα εργαλεία σχεδίασης.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD for Java για την τροποποίηση PSD vector shapes;
- **No Photoshop required** – εργαστείτε απευθείας με αρχεία PSD σε οποιονδήποτε διακομιστή.  
- **Rich API** – πρόσβαση σε στρώματα, πόρους και διανυσματικά δεδομένα με κλάσεις ισχυρά τυποποιημένες.  
- **Cross‑platform** – εκτέλεση σε Windows, Linux ή macOS με οποιοδήποτε JDK.  
- **Performance‑focused** – αποδοτική διαχείριση μνήμης και γρήγορες λειτουργίες αποθήκευσης.

## Προαπαιτούμενα
1. **Java Development Kit (JDK)** – κατεβάστε από [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ή χρησιμοποιήστε τον προτιμώμενο διαχειριστή πακέτων.  
2. **Aspose.PSD for Java** – αποκτήστε το πιο πρόσφατο JAR από τη [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ή οποιονδήποτε επεξεργαστή συμβατό με Java.  
4. **A PSD file** – δημιουργήστε ένα στο Photoshop ή πάρτε ένα δείγμα PSD για πειραματισμό.  
5. **Basic Java knowledge** – εξοικείωση με κλάσεις, αντικείμενα και διαχείριση εξαιρέσεων.

## Εισαγωγή Πακέτων
Πρώτα, εισάγετε τις κλάσεις που θα χρειαστείτε για να εργαστείτε με αρχεία PSD και πόρους διανυσματικών σχημάτων.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Βήμα 1: Ρυθμίστε τους Καταλόγους Πηγής και Εξόδου
Ορίστε πού βρίσκεται το αρχικό PSD και πού θέλετε να αποθηκευτεί το τροποποιημένο αρχείο.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Βήμα 2: Φόρτωση του Αρχείου PSD
Χρησιμοποιήστε το `Image.load` για να ανοίξετε το αρχείο και μετατρέψτε το σε `PsdImage` για λειτουργίες ειδικές στο PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Βήμα 3: Εντοπισμός του Πόρου Vsms στο Στρώμα
Τα δεδομένα διανυσματικού σχήματος βρίσκονται μέσα σε ένα `VsmsResource`. Επανάληψη μέσω των πόρων του δεύτερου στρώματος για να το βρείτε.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Βήμα 4: Πρόσβαση στα Length Records
Κάθε `LengthRecord` αντιπροσωπεύει μια ξεχωριστή διανυσματική διαδρομή. Πάρτε εκείνα που σκοπεύετε να τροποποιήσετε.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Βήμα 5: Τροποποίηση Ιδιοτήτων Λειτουργίας Διαδρομής
Τώρα μπορείτε να **modify PSD vector shapes** αλλάζοντας τις `PathOperations` τους. Αυτό καθορίζει πώς αλληλεπιδρούν τα σχήματα (π.χ., εξαίρεση, τομή, αφαίρεση).

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

## Συνηθισμένα Πιθανά Σφάλματα & Συμβουλές
- **Null checks** – πάντα επαληθεύετε ότι το `resource` δεν είναι `null` πριν προσπελάσετε τις διαδρομές.  
- **Path index bounds** – βεβαιωθείτε ότι οι δείκτες που χρησιμοποιείτε (`[2]`, `[7]`, `[11]`) υπάρχουν στο συγκεκριμένο PSD που επεξεργάζεστε.  
- **License** – η εκτέλεση χωρίς έγκυρη άδεια θα ενσωματώσει υδατογράφημα στο αποθηκευμένο PSD.  

## Συμπέρασμα
Τώρα έχετε ένα πλήρες, ολοκληρωμένο παράδειγμα για το πώς να **modify PSD vector shapes** υποστηρίζοντας ιδιότητες δεδομένων μήκους εγγραφής με το Aspose.PSD for Java. Είτε αυτοματοποιείτε γραμμές παραγωγής περιουσιακών στοιχείων είτε δημιουργείτε ένα προσαρμοσμένο εργαλείο σχεδίασης, αυτά τα API σας δίνουν την ευελιξία να χειρίζεστε διανυσματικά στρώματα χωρίς χειροκίνητη εργασία στο Photoshop. Εξερευνήστε περαιτέρω πειραματιζόμενοι με άλλες `PathOperations` ή συνδυάζοντας πολλαπλές επεξεργασίες `LengthRecord` για σύνθετα σχήματα.

## Συχνές Ερωτήσεις
### Τι είναι το Aspose.PSD for Java;
Aspose.PSD for Java είναι μια βιβλιοθήκη που επιτρέπει στους προγραμματιστές να χειρίζονται και να εργάζονται με αρχεία Photoshop PSD προγραμματιστικά χρησιμοποιώντας τη Java.

### Μπορώ να χρησιμοποιήσω το Aspose.PSD σε δωρεάν έργο;
Ναι, μπορείτε να δοκιμάσετε τη βιβλιοθήκη δωρεάν χρησιμοποιώντας μια δοκιμαστική έκδοση που διατίθεται στην ιστοσελίδα της Aspose.

### Τι είδους τροποποιήσεις μπορώ να κάνω σε αρχεία PSD;
Μπορείτε να χειριστείτε στρώματα, σχήματα, κείμενα, λειτουργίες διαδρομής και πολλά άλλα μέσα στα αρχεία PSD.

### Είναι το Aspose.PSD συμβατό με άλλες γλώσσες προγραμματισμού;
Ναι, η Aspose προσφέρει διάφορες βιβλιοθήκες για διαφορετικές γλώσσες προγραμματισμού, συμπεριλαμβανομένων των .NET και Python.

### Πού μπορώ να βρω την τεκμηρίωση για το Aspose.PSD;
Μπορείτε να έχετε πρόσβαση στην πλήρη τεκμηρίωση [εδώ](https://reference.aspose.com/psd/java/).

## Συχνές Ερωτήσεις

**Ε: Πώς να διαχειριστώ ένα PSD που δεν περιέχει στρώματα διανυσματικών σχημάτων;**  
Α: Το `VsmsResource` θα λείπει, επομένως το `resource` θα παραμείνει `null`. Προσθέστε έναν έλεγχο και παραλείψτε το βήμα τροποποίησης ή ενημερώστε τον χρήστη.

**Ε: Μπορώ να αλλάξω άλλες ιδιότητες όπως χρώμα γεμίσματος ή πλάτος γραμμής;**  
Ν: Ναι, το `LengthRecord` παρέχει πρόσθετους setters για γέμισμα, γραμμή και διαφάνεια. Ανατρέξτε στην τεκμηρίωση του API για πλήρεις λεπτομέρειες.

**Ε: Είναι δυνατόν να επεξεργαστώ παρτίδα πολλαπλών αρχείων PSD;**  
Ν: Απόλυτα. Τυλίξτε τον κώδικα μέσα σε έναν βρόχο που διατρέχει έναν φάκελο με αρχεία PSD, προσαρμόζοντας τις διαδρομές εισόδου και εξόδου κάθε φορά.

**Ε: Πρέπει να κλείσω τις ροές (streams) χειροκίνητα όταν φορτώνω από διαδρομή αρχείου;**  
Α: Η μέθοδος `Image.load` διαχειρίζεται τις ροές αρχείων εσωτερικά, αλλά αν φορτώνετε από `InputStream`, θυμηθείτε να το κλείσετε μετά τη χρήση.

**Ε: Ποια έκδοση του Aspose.PSD απαιτείται για αυτά τα API;**  
Α: Οι κλάσεις `LengthRecord` και `PathOperations` είναι διαθέσιμες από το Aspose.PSD 20.10. Συνιστάται η χρήση της πιο πρόσφατης έκδοσης.

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}