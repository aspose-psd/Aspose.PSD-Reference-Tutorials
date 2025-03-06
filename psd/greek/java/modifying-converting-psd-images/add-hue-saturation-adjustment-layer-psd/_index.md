---
title: Προσθέστε το επίπεδο προσαρμογής κορεσμού απόχρωσης στο PSD
linktitle: Προσθέστε το επίπεδο προσαρμογής κορεσμού απόχρωσης στο PSD
second_title: Aspose.PSD Java API
description: Μάθετε πώς να προσθέτετε επίπεδα προσαρμογής κορεσμού απόχρωσης στο PSD χρησιμοποιώντας το Aspose.PSD για Java σε αυτό το περιεκτικό, βήμα προς βήμα σεμινάριο. Βελτιώστε τη ροή εργασιών σχεδίασης γραφικών.
weight: 14
url: /el/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσθέστε το επίπεδο προσαρμογής κορεσμού απόχρωσης στο PSD

## Εισαγωγή
Όσον αφορά το γραφικό σχέδιο, ο χειρισμός των χρωμάτων παίζει καθοριστικό ρόλο—συγκεκριμένα, η αλλαγή της απόχρωσης, του κορεσμού και της ελαφρότητας μπορούν να μεταμορφώσουν δραστικά τη διάθεση και την ποιότητα οποιασδήποτε εικόνας. Ένας αποτελεσματικός τρόπος για να επιτευχθεί αυτό είναι μέσω της χρήσης επιπέδων προσαρμογής στο Photoshop (αρχεία PSD). Αν θέλετε να βελτιώσετε τα αρχεία PSD σας μέσω προγραμματισμού χρησιμοποιώντας Java, η βιβλιοθήκη Aspose.PSD είναι εδώ για να σας βοηθήσει! Αυτό το σεμινάριο θα σας καθοδηγήσει στα βήματα για να προσθέσετε ένα επίπεδο προσαρμογής κορεσμού χρώματος στα αρχεία σας PSD, κάνοντας τις ροές εργασίας σας πιο παραγωγικές και αποτελεσματικές.
Σε αυτόν τον οδηγό, θα καλύψουμε τα πάντα, από την εισαγωγή των απαραίτητων πακέτων έως τις λεπτές λεπτομέρειες των παραδειγμάτων κώδικα.
## Προαπαιτούμενα
Προτού μεταβούμε στον κώδικα, βεβαιωθείτε ότι έχετε τα εξής:
1.  Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκαταστήσει το JDK 8 ή νεότερο στον υπολογιστή σας. Μπορείτε να το κατεβάσετε από το[Λήψεις κιτ ανάπτυξης Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD για Java Library: Θα χρειαστεί να έχετε τη βιβλιοθήκη Aspose.PSD, την οποία μπορείτε[κατεβάστε εδώ](https://releases.aspose.com/psd/java/). 
3. IDE: Ένα κατάλληλο ολοκληρωμένο περιβάλλον ανάπτυξης (IDE) όπως το IntelliJ IDEA ή το Eclipse για ανάπτυξη Java.
4. Βασικές γνώσεις Java: Η εξοικείωση με τον προγραμματισμό Java είναι ένα πλεονέκτημα, αλλά μην ανησυχείτε. θα σας καθοδηγήσουμε στον κώδικα βήμα προς βήμα.
Τώρα που έχουμε τακτοποιήσει τις προϋποθέσεις μας, ας περάσουμε στο διασκεδαστικό κομμάτι - την κωδικοποίηση!
## Εισαγωγή πακέτων
Για να ξεκινήσετε να εργάζεστε με τη βιβλιοθήκη Aspose.PSD, το πρώτο βήμα είναι να εισαγάγετε τις απαραίτητες κλάσεις. Δείτε πώς μπορείτε να το κάνετε στο αρχείο Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Βεβαιωθείτε ότι έχετε προσθέσει τις κατάλληλες βιβλιοθήκες στο έργο σας, ώστε αυτές οι εισαγωγές να λειτουργούν απρόσκοπτα.
## Βήμα 1: Ρυθμίστε τον Κατάλογο Εγγράφων σας
Κάθε έργο χρειάζεται ένα σημείο εκκίνησης και το δικό μας δεν αποτελεί εξαίρεση. Πρέπει να καθορίσετε έναν κατάλογο όπου αποθηκεύονται τα αρχεία PSD σας. Αυτό είναι ζωτικής σημασίας για τη σωστή φόρτωση και αποθήκευση εικόνων.
```java
String dataDir = "Your Document Directory"; // Ενημερώστε αυτήν τη διαδρομή στον πραγματικό σας κατάλογο
```
## Βήμα 2: Φορτώστε ένα υπάρχον αρχείο PSD
Για να χειριστούμε ένα υπάρχον αρχείο PSD, πρέπει πρώτα να το φορτώσουμε στο πρόγραμμά μας. Δείτε πώς μπορείτε να το κάνετε αυτό:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Σε αυτόν τον κώδικα, ενημερώστε`"HueSaturationAdjustmentLayer.psd"` στο όνομα του υπάρχοντος αρχείου PSD που θέλετε να επεξεργαστείτε.
## Βήμα 3: Επεξεργαστείτε το στρώμα απόχρωσης/κορεσμού
Στη συνέχεια, θα κάνουμε κύκλο στα επίπεδα της φορτωμένης εικόνας PSD μας για να βρούμε και να επεξεργαστούμε τυχόν υπάρχοντα επίπεδα Hue/Saturation. Αυτό το βήμα περιλαμβάνει την τροποποίηση των τιμών απόχρωσης, κορεσμού και φωτεινότητας.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
Σε αυτό το παράδειγμα:
- Προσαρμόζουμε την απόχρωση στο -25, τον κορεσμό στο -12 και την ελαφρότητα στο +67.
-  Ο`getRange(2)` Η μέθοδος μας επιτρέπει να προσαρμόσουμε συγκεκριμένες χρωματικές σειρές όπως επιθυμούμε.
## Βήμα 4: Αποθηκεύστε το τροποποιημένο αρχείο PSD
Αφού κάνετε τις ρυθμίσεις, το επόμενο βήμα είναι να αποθηκεύσετε το αρχείο. Αυτό είναι ένα ζωτικό μέρος της διαδικασίας μας, διασφαλίζοντας ότι οι αλλαγές που κάναμε δεν θα χαθούν.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Βήμα 5: Προσθέστε μια νέα απόχρωση/στρώμα κορεσμού
Στη συνέχεια, μπορεί να θέλετε να προσθέσετε ένα νέο επίπεδο προσαρμογής Hue/Saturation σε άλλο αρχείο PSD. Απλώς ακολουθήστε την ίδια προσέγγιση που χρησιμοποιήσατε νωρίτερα, αλλά με διαφορετικά αρχεία PSD.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Βήμα 6: Ορίστε τιμές νέας απόχρωσης/κορεσμού για το νέο επίπεδο
Τώρα που δημιουργήσατε αυτό το νέο επίπεδο, εφαρμόστε τις επιθυμητές ρυθμίσεις απόχρωσης, κορεσμού και φωτεινότητας όπως πριν.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Βήμα 7: Αποθηκεύστε το Ενημερωμένο αρχείο PSD
Τέλος, αποθηκεύστε το αρχείο PSD με το επίπεδο Hue/Saturation που προστέθηκε για να μπορείτε να δείτε τις αλλαγές σας.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Συγχαρητήρια! Έχετε χειριστεί με επιτυχία αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Τώρα, μπορείτε να πειραματιστείτε με διαφορετικές εικόνες και βαθύτερες αλλαγές, ζωντανεύοντας τα έργα γραφιστικής σας.
## Σύναψη
Η εργασία με γραφικά μέσω προγραμματισμού ανοίγει έναν κόσμο δυνατοτήτων. Η χρήση του Aspose.PSD για Java για την προσθήκη και τροποποίηση των επιπέδων προσαρμογής κορεσμού απόχρωσης παρέχει ευελιξία και αποτελεσματικότητα που μπορεί να βελτιστοποιήσει τη ροή εργασιών σχεδιασμού σας. Είτε βελτιώνετε φωτογραφίες για ένα έργο είτε δημιουργείτε εντυπωσιακό οπτικό περιεχόμενο, η γνώση αυτών των εργαλείων μπορεί να βελτιώσει σημαντικά την απόδοση σας.
 Μη διστάσετε να εξερευνήσετε περισσότερες λειτουργίες του Aspose.PSD κάνοντας κατάδυση[απόδειξη με έγγραφα](https://reference.aspose.com/psd/java/) ή σκεφτείτε να κολλήσετε α[προσωρινή άδεια](https://purchase.aspose.com/temporary-license/) για να δοκιμάσετε την πλήρη ισχύ της βιβλιοθήκης.
## Συχνές ερωτήσεις
### Τι είναι ένα στρώμα προσαρμογής κορεσμού απόχρωσης;
Ένα επίπεδο προσαρμογής κορεσμού απόχρωσης σάς επιτρέπει να τροποποιείτε τις ιδιότητες χρώματος μιας εικόνας χωρίς να τροποποιείτε μόνιμα τα αρχικά εικονοστοιχεία.
### Χρειάζομαι εγκατεστημένο το Photoshop για να χρησιμοποιήσω το Aspose.PSD;
Όχι, το Aspose.PSD είναι μια αυτόνομη βιβλιοθήκη που λειτουργεί ανεξάρτητα από το Photoshop.
### Μπορώ να χρησιμοποιήσω το Aspose.PSD για μαζική επεξεργασία;
Ναι, μπορείτε να αυτοματοποιήσετε και να επεξεργαστείτε ομαδικά πολλά αρχεία PSD με το Aspose.PSD.
### Είναι το Aspose.PSD δωρεάν;
Το Aspose.PSD προσφέρει δωρεάν δοκιμή, αλλά απαιτείται άδεια για μακροχρόνια χρήση. Μπορείτε να δείτε τις τιμές[εδώ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
