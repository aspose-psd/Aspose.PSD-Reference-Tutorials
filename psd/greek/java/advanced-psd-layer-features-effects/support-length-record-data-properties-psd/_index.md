---
date: 2026-09-23
description: Μάθετε πώς να τροποποιείτε διανυσματικά σχήματα PSD και να επεξεργάζεστε
  μαζικά αρχεία PSD χρησιμοποιώντας Aspose.PSD for Java. Λεπτομερή βήματα, συμβουλές
  και code placeholders για μια ολοκληρωμένη λύση.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Υποστήριξη ιδιοτήτων δεδομένων εγγραφής μήκους στο PSD - Java
og_description: Μάθετε πώς να τροποποιείτε διανυσματικά σχήματα PSD και να επεξεργάζεστε
  μαζικά αρχεία PSD χρησιμοποιώντας Aspose.PSD for Java. Οδηγός βήμα‑βήμα με code
  placeholders και επαγγελματικές συμβουλές.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Τροποποίηση διανυσματικών σχημάτων PSD με Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Τροποποίηση διανυσματικών σχημάτων PSD με Aspose.PSD for Java
url: /el/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Τροποποίηση διανυσματικών σχημάτων PSD με Aspose.PSD για Java

## Εισαγωγή
Αν χρειάζεστε να **τροποποιήσετε διανυσματικά σχήματα PSD** προγραμματιστικά, το Aspose.PSD για Java σας παρέχει πλήρη έλεγχο στα αρχεία Photoshop απευθείας από τον κώδικα Java. Αυτό το tutorial σας καθοδηγεί στη στήριξη των ιδιοτήτων εγγραφής μήκους — ένα απαραίτητο βήμα κατά την επεξεργασία των επιπέδων διανυσματικών σχημάτων. Στο τέλος θα μπορείτε να ανοίξετε ένα PSD, να προσαρμόσετε τα δεδομένα του διανυσματικού σχήματος και να αποθηκεύσετε το ενημερωμένο αρχείο χωρίς ποτέ να εκκινήσετε το Photoshop.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “modify PSD vector shapes”;** Προσαρμογή γεωμετρίας, λειτουργιών διαδρομής ή άλλων χαρακτηριστικών των επιπέδων βασισμένων σε διανύσματα μέσα σε αρχείο PSD.  
- **Ποια βιβλιοθήκη το διαχειρίζεται;** Aspose.PSD for Java.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Πόσο χρόνο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για ένα βασικό script τροποποίησης σχήματος.  
- **Ποια είναι τα κύρια προαπαιτούμενα;** Java JDK, Aspose.PSD for Java και ένα δείγμα αρχείου PSD.

## Τι είναι η υποστήριξη ιδιοτήτων εγγραφής μήκους;
Η υποστήριξη ιδιοτήτων εγγραφής μήκους σημαίνει την πρόσβαση και την ενημέρωση των αντικειμένων `LengthRecord` που περιγράφουν κάθε διανυσματική διαδρομή μέσα σε ένα PSD. Αυτές οι εγγραφές αποθηκεύουν πληροφορίες όπως το μήκος της διαδρομής, ο τύπος της και πώς συνδέεται με άλλες διαδρομές. Η αλλαγή τους σας επιτρέπει να ελέγχετε πώς τα σχήματα συνδυάζονται, τέμνονται ή αφαιρούνται το ένα από το άλλο, επιτρέποντας ακριβή επεξεργασία διανυσμάτων.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD για Java για την υποστήριξη ιδιοτήτων εγγραφής μήκους;
Φορτώστε το PSD, επεξεργαστείτε τα διανυσματικά δεδομένα και αποθηκεύστε — όλα χωρίς Photoshop. Το Aspose.PSD επεξεργάζεται PSD με εκατοντάδες σελίδες σε λιγότερο από 2 δευτερόλεπτα σε έναν τυπικό διακομιστή, προσφέρει πάνω από 150 κλάσεις (συμπεριλαμβανομένων 30+ τύπων σχετικών με διανύσματα) και λειτουργεί σε Windows, Linux ή macOS με οποιοδήποτε JDK 11+. Αυτή η βιβλιοθήκη προσανατολισμένη στην απόδοση εξαλείφει την ανάγκη για ακριβό λογισμικό επιφάνειας εργασίας.

## Προαπαιτούμενα
1. **Java Development Kit (JDK)** – κατεβάστε από [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ή χρησιμοποιήστε τον προτιμώμενο διαχειριστή πακέτων σας.  
2. **Aspose.PSD for Java** – αποκτήστε το πιο πρόσφατο JAR από τη [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ή οποιονδήποτε επεξεργαστή συμβατό με Java.  
4. **Αρχείο PSD** – δημιουργήστε ένα στο Photoshop ή πάρτε ένα δείγμα PSD για πειραματισμό.  
5. **Βασικές γνώσεις Java** – εξοικείωση με κλάσεις, αντικείμενα και διαχείριση εξαιρέσεων.

## Εισαγωγή πακέτων
Οι δηλώσεις εισαγωγής φέρνουν τις βασικές κλάσεις του Aspose.PSD στο πεδίο εφαρμογής, όπως `PsdImage`, `VsmsResource` και `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Βήμα 1: Ρυθμίστε τους καταλόγους πηγής και εξόδου
Ορίστε πού βρίσκεται το αρχικό PSD και πού θα γραφτεί το τροποποιημένο αρχείο.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Βήμα 2: Φορτώστε το αρχείο PSD
Χρησιμοποιήστε `Image.load` για να ανοίξετε το αρχείο και να το μετατρέψετε σε `PsdImage` για λειτουργίες ειδικές στο PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Βήμα 3: Εντοπίστε τον πόρο Vsms στο επίπεδο
`VsmsResource` είναι ο κοντέινερ που αποθηκεύει τα δεδομένα διανυσματικών σχημάτων για ένα επίπεδο. Επανάληψη μέσω των πόρων του δεύτερου επιπέδου για να το βρείτε.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Βήμα 4: Πρόσβαση σε εγγραφές μήκους
`LengthRecord` αντιπροσωπεύει μια ξεχωριστή διανυσματική διαδρομή. Ανακτήστε τις εγγραφές που σκοπεύετε να τροποποιήσετε.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Βήμα 5: Τροποποίηση ιδιοτήτων λειτουργίας διαδρομής
`PathOperations` ορίζει πώς αλληλεπιδρούν τα μεμονωμένα σχήματα (π.χ., εξαίρεση, τομή, αφαίρεση). Η αλλαγή αυτών των τιμών ενημερώνει τη οπτική σύνθεση του διανυσματικού επιπέδου.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Βήμα 6: Αποθήκευση του τροποποιημένου αρχείου PSD
Αποθηκεύστε τις αλλαγές σας σε ένα νέο αρχείο.

```java
psdImage.save(outPsdFilePath);
```

## Βήμα 7: Καθαρισμός πόρων
Αποδεσμεύστε το αντικείμενο `PsdImage` για να ελευθερώσετε μνήμη και να αποφύγετε διαρροές πόρων.

```java
psdImage.dispose();
```

## Πώς να επεξεργαστείτε μαζικά αρχεία PSD με υποστήριξη ιδιοτήτων εγγραφής μήκους
Τυλίξτε τη ροή εργασίας ενός αρχείου σε έναν βρόχο που διατρέχει έναν φάκελο με PSD, ενημερώνοντας τα `inPsdFilePath` και `outPsdFilePath` για κάθε αρχείο. Αυτή η προσέγγιση σας επιτρέπει να εφαρμόσετε τα ίδια προσαρμογές διανυσματικών σχημάτων σε δεκάδες ή εκατοντάδες αρχεία σε λίγα λεπτά, ιδανική για αυτοματοποιημένες γραμμές παραγωγής πόρων.

## Κοινά προβλήματα & συμβουλές
- **Έλεγχοι null** – πάντα βεβαιωθείτε ότι το `resource` δεν είναι `null` πριν προσπελάσετε τα μέλη του.  
- **Όρια δείκτη διαδρομής** – βεβαιωθείτε ότι οι δείκτες που χρησιμοποιείτε (π.χ., `[2]`, `[7]`, `[11]`) υπάρχουν για το συγκεκριμένο PSD που επεξεργάζεστε.  
- **Άδεια** – η εκτέλεση χωρίς έγκυρη άδεια ενσωματώνει υδατογράφημα στο αποθηκευμένο PSD.  

## Συμπέρασμα
Τώρα έχετε ένα πλήρες, ολοκληρωμένο παράδειγμα για το πώς να **τροποποιήσετε διανυσματικά σχήματα PSD** υποστηρίζοντας τις ιδιότητες εγγραφής μήκους με το Aspose.PSD για Java. Είτε αυτοματοποιείτε μια γραμμή παραγωγής πόρων είτε δημιουργείτε ένα προσαρμοσμένο εργαλείο σχεδίασης, αυτά τα API σας δίνουν την ευελιξία να χειρίζεστε διανυσματικά επίπεδα χωρίς χειροκίνητη εργασία στο Photoshop. Πειραματιστείτε με άλλες τιμές `PathOperations` ή συνδυάστε πολλαπλές επεξεργασίες `LengthRecord` για να δημιουργήσετε σύνθετα σχήματα.

## Συχνές ερωτήσεις

**Ε: Πώς να χειριστώ ένα PSD που δεν περιέχει επίπεδα διανυσματικών σχημάτων;**  
Α: Το `VsmsResource` θα λείπει, έτσι το `resource` παραμένει `null`. Προσθέστε έναν έλεγχο και παραλείψτε το βήμα τροποποίησης ή ενημερώστε τον χρήστη.

**Ε: Μπορώ να αλλάξω άλλες ιδιότητες όπως το χρώμα γεμίσματος ή το πλάτος γραμμής;**  
Α: Ναι, το `LengthRecord` παρέχει setters για γεμίσμα, γραμμή και αδιαφάνεια. Δείτε την τεκμηρίωση API για την πλήρη λίστα.

**Ε: Είναι δυνατόν να επεξεργαστώ μαζικά πολλά αρχεία PSD;**  
Α: Απόλυτα. Τυλίξτε τον κώδικα μέσα σε έναν βρόχο που διατρέχει έναν φάκελο με αρχεία PSD, προσαρμόζοντας τις διαδρομές εισόδου και εξόδου κάθε φορά.

**Ε: Πρέπει να κλείσω τα streams χειροκίνητα όταν φορτώνω από διαδρομή αρχείου;**  
Α: Το `Image.load` διαχειρίζεται τα streams αρχείων αυτόματα, αλλά αν φορτώνετε από `InputStream`, θυμηθείτε να το κλείσετε μετά τη χρήση.

**Ε: Ποια έκδοση του Aspose.PSD απαιτείται για αυτά τα API;**  
Α: Οι κλάσεις `LengthRecord` και `PathOperations` είναι διαθέσιμες από το Aspose.PSD 20.10. Συνιστάται η χρήση της τελευταίας έκδοσης (24.11 τη στιγμή της συγγραφής).

---

**Τελευταία ενημέρωση:** 2026-09-23  
**Δοκιμή με:** Aspose.PSD for Java 24.11  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Μετατροπή PSD σε PNG και δημιουργία διανυσματικής μάσκας Java – Πόρος Vmsk σε αρχεία PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Μετατροπή PSD σε PNG με υποστήριξη μάσκας επιπέδου χρησιμοποιώντας Aspose.PSD για Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Προσθήκη υποστήριξης επιπέδου σε αρχεία PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}