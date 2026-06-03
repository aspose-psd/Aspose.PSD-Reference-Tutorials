---
date: 2026-06-03
description: Μάθετε πώς να μετατρέψετε PSD σε PNG και να δημιουργήσετε vector mask
  Java χρησιμοποιώντας Aspose.PSD for Java, να προσθέσετε vector mask PSD και να διαχειριστείτε
  προγραμματιστικά τους πόρους Vmsk.
keywords:
- convert psd to png
- add vector mask psd
- psd vector mask tutorial
- aspose psd maven
linktitle: Μετατροπή PSD σε PNG και Δημιουργία Vector Mask Java – Πόρος Vmsk σε αρχεία
  PSD
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to convert PSD to PNG and create vector mask Java using Aspose.PSD
    for Java, add vector mask PSD, and manipulate Vmsk resources programmatically.
  headline: Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD
    Files
  type: TechArticle
- questions:
  - answer: Create a `VmskResource`, populate it with the required path records (e.g.,
      `BezierKnotRecord`), and attach it to the layer’s resources collection.
    question: How do I add a new vector mask to an existing layer?
  - answer: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")`
      specifying the PNG format.
    question: Can I convert the edited PSD directly to PNG without opening Photoshop?
  - answer: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle
      builds, Docker containers, or any CI system that supports Java.
    question: Is there a way to automate this in a CI/CD pipeline?
  - answer: All recent releases (2024‑2025) support Java 8 and above, including Java
      11, 17, and newer LTS versions.
    question: What versions of Aspose.PSD are compatible with Java 11+?
  - answer: A free evaluation license works for development and testing. For production
      deployments, a commercial license is required.
    question: Do I need a license for development builds?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Μετατροπή PSD σε PNG και Δημιουργία Vector Mask Java – Πόρος Vmsk σε αρχεία
  PSD
url: /el/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή PSD σε PNG και Δημιουργία Vector Mask Java – Πόρος Vmsk σε Αρχεία PSD

## Εισαγωγή
Αν χρειάζεστε **convert PSD to PNG** ενώ επίσης **create vector mask** (Vmsk) πόρους μέσα σε αρχεία Photoshop, το Aspose.PSD for Java σας παρέχει έναν καθαρό, προγραμματιστικό τρόπο για να κάνετε και τα δύο. Είτε δημιουργείτε ένα εργαλείο αυτοματοποίησης σχεδίασης, ένα CI pipeline που επικυρώνει πόρους, είτε επεκτείνετε μια ροή εργασίας γραφικών με προσαρμοσμένες μάσκες, αυτό το tutorial σας καθοδηγεί βήμα προς βήμα—φόρτωση ενός PSD, ανάγνωση του πόρου Vmsk, προσαρμογή των ιδιοτήτων του, εξαγωγή του αποτελέσματος σε PNG και αποθήκευση του τροποποιημένου αρχείου. Στο τέλος, θα είστε άνετοι με τη διαχείριση vector masks, τη μετατροπή PSD → PNG, και την επέκταση του αρχείου με πρόσθετα διανυσματικά δεδομένα—όλα με τεχνικές **convert PSD to PNG**.

## Γρήγορες Απαντήσεις
- **Τι είναι ένας πόρος Vmsk;** Είναι τα δεδομένα vector mask που αποθηκεύονται μέσα σε ένα αρχείο PSD, ορίζοντας σύνθετα διανυσματικά σχήματα για ένα στρώμα.  
- **Ποια βιβλιοθήκη το υποστηρίζει;** Aspose.PSD for Java παρέχει πλήρη πρόσβαση ανάγνωσης/εγγραφής στους πόρους Vmsk.  
- **Χρειάζομαι άδεια;** Διατίθεται δωρεάν δοκιμή· απαιτείται εμπορική άδεια για χρήση σε παραγωγή.  
- **Μπορώ να μετατρέψω το επεξεργασμένο PSD σε PNG;** Ναι—αφού αποθηκευτεί, μπορείτε να φορτώσετε το PSD και να το εξάγετε σε PNG με το ίδιο API.  
- **Υπάρχει υποστήριξη Maven;** Απόλυτα· το Aspose.PSD μπορεί να προστεθεί ως εξάρτηση Maven (δείτε τη λέξη-κλειδί “aspose psd maven”).

## Τι είναι μια Vector Mask (Πόρος Vmsk);
Μια vector mask (Vmsk) είναι μια μάσκα μη‑pixel‑βασισμένη που χρησιμοποιεί καμπύλες Bézier και εγγραφές διαδρομής για να ορίσει διαφανείς και αδιαφανείς περιοχές σε ένα στρώμα. Επειδή είναι διανυσματική, κλιμακώνεται χωρίς απώλεια ποιότητας—ιδανική για γραφικά υψηλής ανάλυσης. Μπορεί να περιέχει πολλαπλές διαδρομές, η κάθε μία αποτελούμενη από κόμβους Bezier, και υποστηρίζει χαρακτηριστικά μάσκας όπως η αδιαφάνεια, το γέμισμα και η σύνδεση με μάσκες στρώματος.

## Γιατί να δημιουργήσετε μια Vector Mask με το Aspose.PSD;
Η δημιουργία vector masks προγραμματιστικά εξαλείφει την ανάγκη για χειροκίνητη επεξεργασία Photoshop, εξασφαλίζει συνέπεια σε μεγάλες παρτίδες αρχείων και επιτρέπει ενσωμάτωση σε αυτοματοποιημένες διαδικασίες κατασκευής ή ανάπτυξης. Με το Aspose.PSD μπορείτε να δημιουργήσετε ακριβή γεωμετρία μάσκας, να την εφαρμόσετε σε οποιοδήποτε στρώμα και να διατηρήσετε πλήρη δυνατότητα επεξεργασίας, κάτι που είναι ουσιώδες για τη δημιουργία δυναμικών γραφικών και τις ροές εργασίας responsive design.
- **Αυτοματοποίηση:** Προσθέστε ή τροποποιήστε μάσκες προγραμματιστικά χωρίς να ανοίξετε το Photoshop.  
- **Συνέπεια:** Διασφαλίστε ότι κάθε PSD που δημιουργείτε ακολουθεί τους ίδιους κανόνες μάσκας.  
- **Διαπλατφόρμα:** Λειτουργεί σε οποιοδήποτε λειτουργικό σύστημα που υποστηρίζει Java.  
- **Ενσωμάτωση:** Συνδυάστε με άλλα Aspose APIs (π.χ., convert PSD → PNG) για ολοκληρωμένες ροές εργασίας.  
- **Κλιμακωσιμότητα:** Οι vector masks παραμένουν καθαρές σε οποιοδήποτε μέγεθος, καθιστώντας τες ιδανικές για responsive designs.

## Γιατί αυτό είναι σημαντικό για προγραμματιστές Java
Η χρήση τεχνικών **create vector mask java** σας επιτρέπει να ενσωματώσετε σύνθετη λογική γραφικών απευθείας σε back‑end υπηρεσίες, CI pipelines ή επιτραπέζιες εφαρμογές. Δεν χρειάζεται πλέον ένας σχεδιαστής να προσθέτει μάσκες χειροκίνητα· ο κώδικάς σας μπορεί να τις δημιουργεί ή να τις προσαρμόζει άμεσα, εξοικονομώντας χρόνο και μειώνοντας τα ανθρώπινα σφάλματα.

## Προαπαιτούμενα
Πριν βουτήξουμε στον κώδικα, βεβαιωθείτε ότι έχετε τα εξής:

### Τι χρειάζεστε
- **Java Development Kit (JDK):** Εγκαταστήστε JDK 8 ή νεότερο. Μπορείτε να το κατεβάσετε από την [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library:** Αυτή η ισχυρή βιβλιοθήκη διαχειρίζεται αρχεία PSD. Κατεβάστε την από τη [Aspose release page](https://releases.aspose.com/psd/java/). Για γρήγορη εκκίνηση, πάρτε τη δωρεάν δοκιμή από την ίδια σελίδα ή το [free trial](https://releases.aspose.com/).  
- **IDE:** Οποιοδήποτε Java IDE (IntelliJ IDEA, Eclipse, NetBeans) θα λειτουργήσει.

### Ρύθμιση του Χώρου Εργασίας
1. **Create a New Java Project** – Ανοίξτε το προτιμώμενο IDE σας και ξεκινήστε ένα νέο έργο.  
2. **Add the Aspose Library** – Αφού κατεβάσετε το Aspose JAR, προσθέστε το στο build path του έργου σας ώστε να έχετε πρόσβαση σε όλες τις κλάσεις που σχετίζονται με PSD.  

Με το περιβάλλον έτοιμο, ας περάσουμε στην πραγματική υλοποίηση.

## Πώς να μετατρέψετε PSD σε PNG χρησιμοποιώντας το Aspose.PSD for Java;
Φορτώστε το πηγαίο PSD με `PsdImage.load()`, προαιρετικά επεξεργαστείτε τη vector mask του, και στη συνέχεια καλέστε `save()` καθορίζοντας `ExportFormat.Png`. Το Aspose.PSD διαχειρίζεται αυτόματα όλα τα προφίλ χρώματος, τα στρώματα και τα δεδομένα μάσκας, παράγοντας ένα pixel‑perfect PNG που ταιριάζει με την αρχική οπτική εμφάνιση. Αυτή η ροή δύο βημάτων λειτουργεί για οποιοδήποτε PSD, ανεξαρτήτως μεγέθους, και εκτελείται σε οποιαδήποτε πλατφόρμα συμβατή με Java.

## Εισαγωγή Πακέτων
Το πακέτο `com.aspose.psd` παρέχει βασικές κλάσεις για τη διαχείριση αρχείων PSD, συμπεριλαμβανομένης της φόρτωσης εικόνας, της διαχείρισης πόρων και των δυνατοτήτων εξαγωγής.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

## Βήμα 1: Φορτώστε το PSD Αρχείο Σας
Η φόρτωση του αρχείου σας παρέχει ένα αντικείμενο `PsdImage` που αντιπροσωπεύει ολόκληρο το έγγραφο στη μνήμη.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Ορίζουμε το `dataDir` στον φάκελο του αρχείου PSD.  
- Δημιουργούμε μια συμβολοσειρά για το `sourceFileName`, συνδυάζοντας τον φάκελο με το όνομα του αρχείου PSD.  
- Τέλος, φορτώνουμε το αρχείο PSD σε ένα αντικείμενο `PsdImage` χρησιμοποιώντας το `Image.load()`.

## Βήμα 2: Ανακτήστε τον Πόρο Vmsk
Η κλάση `VmskResource` περιλαμβάνει τα δεδομένα vector mask που αποθηκεύονται μέσα σε ένα στρώμα PSD. Η ανάκτησή της σας επιτρέπει να εξετάσετε ή να τροποποιήσετε τις διαδρομές της μάσκας.

```java
VmskResource resource = getVmskResource(im);
```

- Καλούμε τη μέθοδο `getVmskResource()` η οποία διαχειρίζεται την αναζήτηση και ανάκτηση του πόρου Vmsk από την εικόνα.

## Βήμα 3: Επικυρώστε τις Ιδιότητες του Πόρου Vmsk
Πριν κάνετε αλλαγές, επαληθεύστε ότι η μάσκα είναι ενεργοποιημένη, σωστά προσανατολισμένη και περιέχει τον αναμενόμενο αριθμό διαδρομών.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Εδώ ελέγχουμε διάφορες ιδιότητες του πόρου Vmsk. Θέλουμε να διασφαλίσουμε ότι δεν είναι απενεργοποιημένη, ανεστραμμένη ή μη συνδεδεμένη, και ότι έχει τον σωστό αριθμό διαδρομών.

## Βήμα 4: Πρόσβαση σε Κάθε Διαδρομή και Επικύρωση
Κάθε εγγραφή διαδρομής περιγράφει ένα τμήμα του διανυσματικού σχήματος. Η επιθεώρησή τους εξασφαλίζει ότι εργάζεστε με τη σωστή γεωμετρία.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Εξάγουμε τρία συγκεκριμένα records διαδρομής και επικυρώνουμε τους τύπους και τις ιδιότητές τους για να διασφαλίσουμε ότι πληρούν τα κριτήριά μας.

## Βήμα 5: Επεξεργασία του Πόρου Vmsk
Τώρα μπαίνουμε στο τμήμα τροποποίησης! Μπορείτε να εναλλάξετε τις σημαίες συμπεριφοράς της μάσκας ώστε να ταιριάζουν στη ροή εργασίας σας.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Σε αυτό το τμήμα, εναλλάσσουμε διάφορες ιδιότητες του πόρου Vmsk. Ορίζοντάς τες σε `true`, μπορούμε να ελέγξουμε πώς η μάσκα συμπεριφέρεται στο αρχείο PSD.

## Βήμα 6: Τροποποίηση των Σημείων Bezier Knot
Οι κόμβοι Bezier ορίζουν την καμπυλότητα κάθε διανυσματικού τμήματος. Η προσαρμογή τους αλλάζει το σχήμα της μάσκας χωρίς rasterization.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Πρόσβαση σε συγκεκριμένα paths `BezierKnotRecord` και αλλαγή των σημείων τους για πιθανή ανασχηματισμό της vector mask.

## Βήμα 7: Αποθήκευση του Τροποποιημένου Αρχείου PSD
Αφού ολοκληρωθούν όλες οι επεξεργασίες, αποθηκεύστε τις αλλαγές σε ένα νέο αρχείο PSD.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Ορίζουμε τη διαδρομή για το εξαγόμενο αρχείο PSD και στη συνέχεια καλούμε `im.save()` για να γράψουμε τις αλλαγές σε αυτό το νέο αρχείο.

## Βήμα 8: Εξαγωγή του PSD ως PNG
Τώρα που το PSD περιέχει την ενημερωμένη μάσκα, εξάγετέ το απευθείας σε PNG. Αυτό το βήμα επιδεικνύει τη ροή εργασίας **convert PSD to PNG**.

```java
im.dispose();
```

- Χρησιμοποιήστε `im.save("output.png", ExportFormat.Png)` για να δημιουργήσετε ένα PNG υψηλής ποιότητας που αντικατοπτρίζει τη τροποποιημένη vector mask.

## Καθαρισμός Πόρων
Τέλος, πρέπει να διασφαλίσουμε ότι απελευθερώνουμε σωστά την εικόνα για να ελευθερωθούν οι πόροι.

CODE_BLOCK_PLACEHOLDER_9_END

- Είναι πάντα καλή πρακτική να απελευθερώνετε οποιουσδήποτε πόρους μόλις τελειώσετε. Αυτό βοηθά στην αποφυγή διαρροών μνήμης στις εφαρμογές σας.

## Συχνά Προβλήματα και Λύσεις
| Πρόβλημα | Γιατί συμβαίνει | Πώς να το διορθώσετε |
|----------|------------------|----------------------|
| **`VmskResource` not found** | Το PSD δεν περιέχει στρώμα vector mask. | Επαληθεύστε ότι το πηγαίο PSD έχει vector mask ή προσθέστε το χειροκίνητα στο Photoshop πριν τρέξετε τον κώδικα. |
| **`ArrayIndexOutOfBoundsException` on path access** | Ο αναμενόμενος αριθμός εγγραφών διαδρομής διαφέρει. | Εξετάστε το `resource.getPaths().length` και προσαρμόστε τη χρήση των δεικτών αναλόγως. |
| **License exception** | Εκτέλεση χωρίς έγκυρη άδεια Aspose.PSD. | Εφαρμόστε δοκιμαστική ή αγορασμένη άδεια χρησιμοποιώντας `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | Η εικόνα δεν απελευθερώνεται σε μακροχρόνιες διεργασίες. | Πάντα καλέστε `im.dispose()` σε μπλοκ `finally` ή χρησιμοποιήστε try‑with‑resources αν υποστηρίζεται. |

## Συχνές Ερωτήσεις

**Q: Πώς μπορώ να προσθέσω μια νέα vector mask σε ένα υπάρχον στρώμα;**  
A: Δημιουργήστε ένα `VmskResource`, γεμίστε το με τις απαιτούμενες εγγραφές διαδρομής (π.χ., `BezierKnotRecord`), και συνδέστε το στη συλλογή πόρων του στρώματος.

**Q: Μπορώ να μετατρέψω το επεξεργασμένο PSD απευθείας σε PNG χωρίς να ανοίξω το Photoshop;**  
A: Ναι—αφού αποθηκεύσετε το PSD, φορτώστε το ξανά με `Image.load()` και καλέστε `im.save("output.png")` καθορίζοντας τη μορφή PNG.

**Q: Υπάρχει τρόπος να αυτοματοποιηθεί αυτό σε pipeline CI/CD;**  
A: Απόλυτα. Δεδομένου ότι η διαδικασία είναι καθαρά Java, μπορείτε να την ενσωματώσετε σε builds Maven/Gradle, Docker containers ή οποιοδήποτε σύστημα CI που υποστηρίζει Java.

**Q: Ποιες εκδόσεις του Aspose.PSD είναι συμβατές με Java 11+;**  
A: Όλες οι πρόσφατες κυκλοφορίες (2024‑2025) υποστηρίζουν Java 8 και άνω, συμπεριλαμβανομένων των Java 11, 17 και νεότερων εκδόσεων LTS.

**Q: Χρειάζομαι άδεια για builds ανάπτυξης;**  
A: Μια δωρεάν άδεια αξιολόγησης λειτουργεί για ανάπτυξη και δοκιμές. Για παραγωγικές εγκαταστάσεις, απαιτείται εμπορική άδεια.

**Last Updated:** 2026-06-03  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Εξαγωγή PSD σε PNG με Υποστήριξη Layer Mask σε Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Πώς να Μετατρέψετε PSD σε PNG και να Αλλάξετε το Μέγεθος Αναλογικά με Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Μετατροπή PSD σε PNG με Επικάλυψη Χρώματος – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}