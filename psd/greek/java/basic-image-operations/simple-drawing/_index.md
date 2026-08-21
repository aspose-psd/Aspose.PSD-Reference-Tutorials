---
date: 2026-06-13
description: Μάθετε πώς να σχεδιάσετε ορθογώνιο σε αρχεία PSD χρησιμοποιώντας το Aspose.PSD
  for Java. Αυτός ο οδηγός παρουσιάζει κώδικα βήμα‑βήμα, προσθήκη επιπέδων, επεξεργασία
  εικόνας στο διακομιστή και σχεδίαση σχημάτων.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Εκτέλεση απλού σχεδίου
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Πώς να σχεδιάσετε ορθογώνιο σε PSD με το Aspose.PSD for Java
url: /el/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Σχεδιάσετε Ορθογώνιο σε PSD με Aspose.PSD για Java

## Εισαγωγή

Σε αυτό το σεμινάριο θα ανακαλύψετε **πώς να σχεδιάσετε ορθογώνιο** σχήματα μέσα σε αρχείο Photoshop PSD χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD για Java. Είτε δημιουργείτε μια διαδρομή επεξεργασίας περιουσιακών στοιχείων διακομιστή, αυτοματοποιείτε τη δημιουργία μικρογραφιών, είτε προσθέτετε δυναμικά γραφικά σε υπάρχοντα σχέδια, τα παρακάτω βήματα σας παρέχουν μια πλήρη, έτοιμη για παραγωγή λύση. Θα καλύψουμε τη δημιουργία νέου εγγράφου PSD, την προσθήκη στρώματος, τον καθαρισμό του φόντου και, τέλος, τη σχεδίαση τόσο κόκκινων όσο και μπλε ορθογωνίων—χωρίς ποτέ να ανοίξετε το Photoshop.

## Σύντομες Απαντήσεις
- **What is the primary class to create a PSD file?** `PsdImage`
- **Which method clears a layer’s background color?** `Graphics.clear(Color)`
- **How do you draw a red rectangle?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Do I need a license for development?** A free trial works for testing; a license is required for production.
- **Can I manipulate existing PSD files with the same API?** Yes, Aspose.PSD supports full PSD editing.

## Τι σημαίνει η σχεδίαση ενός κόκκινου ορθογωνίου σε αρχείο PSD;

Η σχεδίαση ενός κόκκινου ορθογωνίου σημαίνει τη χρήση του αντικειμένου `Graphics` για την απόδοση ενός ορθογώνιου σχήματος γεμάτου ή περιγραμμένου με το χρώμα κόκκινο σε συγκεκριμένο στρώμα μιας εικόνας PSD. Αυτή η λειτουργία είναι κοινή για την επισήμανση περιοχών, τη δημιουργία placeholders ή την προσθήκη απλών γραφικών προγραμματιστικά.

## Γιατί να χρησιμοποιήσετε Aspose.PSD για Java για την επεξεργασία αρχείων PSD;

Το Aspose.PSD για Java υποστηρίζει **50+ μορφές εισόδου και εξόδου**, μπορεί να επεξεργαστεί αρχεία PSD εκατοντάδων σελίδων χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, και λειτουργεί σε οποιαδήποτε πλατφόρμα που υποστηρίζει Java 8 ή νεότερη. Η μηχανή επεξεργασίας εικόνας διακομιστή εξαλείφει την ανάγκη για Photoshop, μειώνει τα κόστη αδειοδότησης και επιτρέπει αυτοματοποιημένες ροές εργασίας που διαχειρίζονται έως **10 GB** δεδομένων εικόνας ανά ώρα σε ένα μέτριο VM.

## Προαπαιτούμενα

- Java Development Kit (JDK) 8 ή νεότερο εγκατεστημένο στο σύστημά σας.  
- Βιβλιοθήκη Aspose.PSD για Java. Μπορείτε να τη κατεβάσετε από την [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Εισαγωγή Πακέτων

Οι δηλώσεις `import` φέρνουν τις απαιτούμενες κλάσεις στο πεδίο ορατότητας ώστε να μπορείτε να εργαστείτε με εικόνες PSD, στρώματα, χρώματα και γραφικά.

Η κλάση `PsdImage` είναι το κορυφαίο αντικείμενο του Aspose.PSD που αντιπροσωπεύει ένα μοναδικό αρχείο PSD στη μνήμη.  
`Graphics` παρέχει primitives σχεδίασης όπως γραμμές, ορθογώνια και έλλειψη.  
`Color` και `Pen` σας επιτρέπουν να καθορίσετε χρώματα περιγράμματος και πάχος.  
Η κλάση `Layer` αντιπροσωπεύει ένα μεμονωμένο στρώμα εικόνας μέσα σε ένα έγγραφο PSD.  
Η κλάση `Rectangle` ορίζει τη θέση και το μέγεθος μιας ορθογώνιας περιοχής που χρησιμοποιείται για λειτουργίες σχεδίασης.  
Η κλάση `SolidBrush` γεμίζει σχήματα με ένα συμπαγές χρώμα.

## Ποιο είναι το πρώτο βήμα για τη δημιουργία ενός εγγράφου PSD;

Δημιουργείτε ένα αντικείμενο `PsdImage` παρέχοντας το πλάτος και το ύψος του καμβά σε εικονοστοιχεία, το οποίο δημιουργεί μια κενή δομή αρχείου PSD. Μετά τον ορισμό τυχόν αρχικών στρωμάτων ή φόντου, καλείτε τη μέθοδο `save` με διαδρομή αρχείου για να γράψετε το έγγραφο στο δίσκο. Αυτό προετοιμάζει την εικόνα για επόμενες λειτουργίες επεξεργασίας.

## Βήμα 1: Δημιουργία Νέου Εγγράφου

Πρώτα, δημιουργήστε ένα φρέσκο έγγραφο PSD με το επιθυμητό μέγεθος καμβά. Αυτό το έγγραφο θα φιλοξενήσει το στρώμα στο οποίο θα σχεδιάσουμε.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Πώς να προσθέσετε ένα νέο κενό στρώμα σε εικόνα PSD;

Πρώτα, δημιουργήστε μια νέα παρουσία `Layer` με το ίδιο πλάτος και ύψος με το γονικό `PsdImage`. Στη συνέχεια προσθέστε αυτό το στρώμα στη συλλογή `Layers` της εικόνας χρησιμοποιώντας τη μέθοδο `add`. Μόλις το στρώμα γίνει μέρος της εικόνας, ανακτήστε το αντικείμενο `Graphics` του για να εκτελέσετε λειτουργίες σχεδίασης· χωρίς αυτό το βήμα τα σχέδια δεν θα εμφανιστούν.

## Βήμα 2: Προσθήκη Στρώματος

Στη συνέχεια, προσθέστε ένα νέο κενό στρώμα που καλύπτει το πλήρες πλάτος και ύψος της εικόνας. Τα στρώματα είναι απαραίτητα για τον διαχωρισμό των λειτουργιών σχεδίασης.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Ποιος είναι ο σκοπός του καθαρισμού του χρώματος φόντου ενός στρώματος;

Η κλήση `Graphics.clear` με ένα συγκεκριμένο `Color` γεμίζει ολόκληρο το στρώμα με αυτό το χρώμα, επαναφέροντας ουσιαστικά όλα τα δεδομένα εικονοστοιχείων. Αυτό διασφαλίζει ότι οποιοδήποτε προηγούμενο περιεχόμενο αφαιρείται και ότι το στρώμα ξεκινά από ένα γνωστό φόντο, αποφεύγοντας απρόσμενη διαφάνεια ή ανάμειξη χρωμάτων όταν το PSD ανοιχτεί ή επεξεργαστεί αργότερα στο Photoshop.

## Βήμα 3: Σχεδίαση Σχημάτων

Θα χρησιμοποιήσουμε την κλάση `Graphics` για να επεξεργαστούμε τα δεδομένα εικονοστοιχείων του στρώματος. Παρακάτω υπάρχουν τρία παραδείγματα που δείχνουν τον καθαρισμό του φόντου και τη σχεδίαση ορθογωνίων με διαφορετικά χρώματα.

### Καθαρισμός Χρώματος Στρώματος (ορισμός φόντου σε κίτρινο)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Σχεδίαση Κόκκινου Ορθογωνίου (κύρια εστίαση)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Σχεδίαση Μπλε Ορθογωνίου (πρόσθετο παράδειγμα)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Πώς να αποθηκεύσετε το επεξεργασμένο αρχείο PSD στο δίσκο;

Χρησιμοποιήστε τη μέθοδο `save` στο αντικείμενο `PsdImage`, περνώντας τη πλήρη διαδρομή αρχείου και προαιρετικά καθορίζοντας τη μορφή εικόνας (PSD από προεπιλογή). Αυτό γράφει όλα τα στρώματα, μάσκες και εντολές σχεδίασης σε ένα ενιαίο αρχείο PSD που συμμορφώνεται με την προδιαγραφή του Photoshop, επιτρέποντας το άνοιγμα χωρίς προειδοποιήσεις.

## Βήμα 4: Αποθήκευση Αλλαγών

Τέλος, γράψτε την τροποποιημένη εικόνα PSD στο δίσκο. Το αρχείο θα περιέχει το νέο στρώμα και τα σχεδιασμένα σχήματα.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Συνηθισμένα Προβλήματα και Λύσεις

- **Το στρώμα δεν είναι ορατό μετά τη σχεδίαση:** Βεβαιωθείτε ότι το στρώμα προστέθηκε στην εικόνα **πριν** δημιουργήσετε το αντικείμενο `Graphics`. Η επιφάνεια σχεδίασης πρέπει να είναι συνδεδεμένη με ένα έγκυρο στρώμα.
- **Τα χρώματα εμφανίζονται λανθασμένα:** Επαληθεύστε ότι χρησιμοποιείτε `Color.getRed()` (ή `Color.getBlue()`) αντί να δημιουργείτε μια προσαρμοσμένη τιμή RGB που υπερβαίνει το εύρος 0‑255.
- **Το αρχείο δεν αποθηκεύεται:** Επιβεβαιώστε ότι η διαδρομή `outputDir` υπάρχει και ότι η εφαρμογή έχει δικαιώματα εγγραφής. Σε Linux, ίσως χρειαστεί να προσαρμόσετε την ιδιοκτησία του φακέλου ή να χρησιμοποιήσετε `Files.createDirectories`.
- **Μείωση απόδοσης σε μεγάλα αρχεία:** Χρησιμοποιήστε το `setLoadOptions` του `PsdImage` για να φορτώσετε μόνο τα απαιτούμενα κανάλια, μειώνοντας την κατανάλωση μνήμης για PSD μεγαλύτερα από 200 MB.

## Συχνές Ερωτήσεις

**Q1: Μπορώ να χρησιμοποιήσω Aspose.PSD για Java για την επεξεργασία υπαρχόντων αρχείων PSD;**  
A1: Ναι, το Aspose.PSD για Java παρέχει εκτεταμένη λειτουργικότητα για την επεξεργασία και τροποποίηση υπαρχόντων αρχείων PSD, συμπεριλαμβανομένης της αναδιάταξης στρωμάτων, ρυθμίσεων μάσκας και σχεδίασης διανυσματικών στοιχείων.

**Q2: Πού μπορώ να βρω υποστήριξη για Aspose.PSD για Java;**  
A2: Μπορείτε να επισκεφθείτε το [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) για βοήθεια από την κοινότητα και επίσημες απαντήσεις της Aspose.

**Q3: Υπάρχει δωρεάν δοκιμή διαθέσιμη για Aspose.PSD για Java;**  
A3: Ναι, μπορείτε να αποκτήσετε τη δωρεάν δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/). Η δοκιμή περιλαμβάνει όλες τις λειτουργίες αλλά προσθέτει υδατογράφημα στα αποθηκευμένα αρχεία.

**Q4: Πώς μπορώ να αγοράσω άδεια για Aspose.PSD για Java;**  
A4: Μπορείτε να αγοράσετε άδεια από τη [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Οι επιλογές αδειοδότησης περιλαμβάνουν μόνιμη, συνδρομητική και εταιρική άδεια.

**Q5: Διατίθενται προσωρινές άδειες για Aspose.PSD για Java;**  
A5: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

## Πρόσθετες Συχνές Ερωτήσεις

**Q: Μπορώ να σχεδιάσω άλλα σχήματα εκτός από ορθογώνια;**  
A: Ναι, η κλάση `Graphics` υποστηρίζει επίσης σχεδίαση ελλείψεων, γραμμών και προσαρμοσμένων διαδρομών μέσω της μεθόδου `drawPath`.

**Q: Υποστηρίζει το Aspose.PSD διαφάνεια στα σχεδιασμένα σχήματα;**  
A: Απόλυτα· μπορείτε να χρησιμοποιήσετε `SolidBrush` με χρώμα ARGB για να συμπεριλάβετε διαφάνεια alpha, επιτρέποντας ημιδιαφανείς επικάλυψεις.

**Q: Είναι δυνατόν να επεξεργαστώ την αδιαφάνεια ενός στρώματος;**  
A: Ναι, κάθε αντικείμενο `Layer` διαθέτει μέθοδο `setOpacity` που δέχεται τιμή από 0 έως 255, παρέχοντας λεπτομερή έλεγχο της διαφάνειας του στρώματος.

**Q: Πώς να φορτώσω ένα υπάρχον αρχείο PSD αντί να δημιουργήσω νέο;**  
A: Χρησιμοποιήστε `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` πριν επεξεργαστείτε τα στρώματα. Η φορτωμένη εικόνα διατηρεί όλα τα αρχικά στρώματα και μάσκες.

## Συμπέρασμα

Τώρα έχετε κατακτήσει **πώς να σχεδιάσετε ορθογώνιο** σχήματα και να χειριστείτε στρώματα μέσα σε αρχείο PSD χρησιμοποιώντας Aspose.PSD για Java. Δημιουργώντας ένα έγγραφο, προσθέτοντας ένα στρώμα, καθαρίζοντας το φόντο του και σχεδιάζοντας με το API `Graphics`, μπορείτε να αυτοματοποιήσετε αμέτρητες εργασίες γραφιστικού σχεδιασμού στο διακομιστή. Πειραματιστείτε με διαφορετικά πένες, πινέλα και εφέ στρωμάτων για να επεκτείνετε αυτή τη βάση σε πλήρεις γραμμές παραγωγής εικόνων.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Σχετικά Σεμινάρια

- [Πώς να Σχεδιάσετε Σχήματα Java – Βασικές Λειτουργίες Εικόνας](/psd/java/basic-image-operations/)
- [Απλή Αλλαγή Μεγέθους με Aspose.PSD – Βιβλιοθήκη Επεξεργασίας Εικόνας Java](/psd/java/basic-image-operations/simple-resizing/)
- [Περικοπή Εικόνας με Ορθογώνιο στο Aspose.PSD για Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Τελευταία Ενημέρωση:** 2026-06-13  
**Δοκιμή Με:** Aspose.PSD for Java 24.12 (τελευταία έκδοση τη στιγμή της συγγραφής)  
**Συγγραφέας:** Aspose