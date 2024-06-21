---
title: Εξαγωγή μικρογραφίας από το PSD σε Java
linktitle: Εξαγωγή μικρογραφίας από το PSD σε Java
second_title: Aspose.PSD Java API
description: Μάθετε πώς να εξάγετε μικρογραφίες από αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Αυτός ο οδηγός βήμα προς βήμα καλύπτει τα πάντα, από τη ρύθμιση έως την αποθήκευση εξαγόμενων εικόνων.
type: docs
weight: 15
url: /el/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Εισαγωγή
Σε αυτό το σεμινάριο, θα εξερευνήσουμε πώς να εξαγάγετε μικρογραφίες από αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Οι μικρογραφίες μπορούν να είναι χρήσιμες για γρήγορες προεπισκοπήσεις ή για τη δημιουργία μικρότερων εκδόσεων εικόνων που είναι ενσωματωμένες σε έγγραφα PSD. Ας βουτήξουμε στα βήματα που απαιτούνται για να το πετύχουμε αυτό χρησιμοποιώντας το Aspose.PSD.
## Προαπαιτούμενα
Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε ρυθμίσει τις ακόλουθες ρυθμίσεις:
- Το Java Development Kit (JDK) είναι εγκατεστημένο στο σύστημά σας.
-  Aspose.PSD για βιβλιοθήκη Java. Μπορείτε να το κατεβάσετε από[εδώ](https://releases.aspose.com/psd/java/).
- Βασικές γνώσεις προγραμματισμού Java.
## Εισαγωγή πακέτων
Για να ξεκινήσετε, συμπεριλάβετε το απαραίτητο πακέτο Aspose.PSD στην τάξη Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Βήμα 1: Φορτώστε το αρχείο PSD
Αρχικά, φορτώστε το αρχείο PSD που περιέχει τη μικρογραφία που θέλετε να εξαγάγετε.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Αντικαθιστώ`"Your_Document_Directory/"` με τη διαδρομή καταλόγου όπου βρίσκεται το αρχείο PSD και`"your_file.psd"` με το όνομα του αρχείου PSD σας.
## Βήμα 2: Επαναλάβετε τους πόρους εικόνας
Επαναλάβετε τους πόρους της εικόνας για να βρείτε τον πόρο της μικρογραφίας.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Εξαγωγή δεδομένων μικρογραφιών
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Δημιουργήστε μια νέα εικόνα με τα εξαγόμενα δεδομένα μικρογραφιών
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Αποθηκεύστε τη μικρογραφία που εξάγεται ως ξεχωριστό αρχείο JPEG
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Έξοδος μηνύματος επιτυχίας
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Βγείτε από τον βρόχο μόλις βρεθεί και υποβληθεί σε επεξεργασία η μικρογραφία
    }
}
```
## Βήμα 3: Αποθηκεύστε την εξαγόμενη μικρογραφία
Αποθηκεύστε τη μικρογραφία που εξάγεται ως ξεχωριστό αρχείο εικόνας (σε αυτήν την περίπτωση, ως αρχείο JPEG).
## Βήμα 4: Χειρισμός διαφορετικών τύπων μικρογραφιών
 Εάν το αρχείο PSD μπορεί να περιέχει πολλούς τύπους μικρογραφιών, όπως π.χ`Thumbnail4Resource`, μπορείτε να επεκτείνετε τη λογική για να χειριστείτε αυτές τις περιπτώσεις με παρόμοιο τρόπο.

## συμπέρασμα
Σε αυτό το σεμινάριο, εξερευνήσαμε τον τρόπο εξαγωγής μικρογραφιών από αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθώντας τα βήματα που περιγράφονται παραπάνω, μπορείτε να ανακτήσετε και να αποθηκεύσετε αποτελεσματικά μικρογραφίες που είναι ενσωματωμένες στα έγγραφά σας PSD.

## Συχνές ερωτήσεις
### Τι είναι το Aspose.PSD;
Το Aspose.PSD είναι μια βιβλιοθήκη Java που επιτρέπει στους προγραμματιστές να εργάζονται με PSD και άλλες μορφές αρχείων εικόνας μέσω προγραμματισμού.
### Πού μπορώ να βρω περισσότερη τεκμηρίωση για το Aspose.PSD για Java;
 Μπορείτε να ανατρέξετε στο[τεκμηρίωση](https://reference.aspose.com/psd/java/) για λεπτομερείς αναφορές και παραδείγματα API.
### Μπορώ να δοκιμάσω το Aspose.PSD δωρεάν πριν το αγοράσω;
 Ναι, μπορείτε να κατεβάσετε ένα[δωρεάν δοκιμή](https://releases.aspose.com/) να αξιολογήσει τις δυνατότητες της βιβλιοθήκης.
### Πώς μπορώ να λάβω προσωρινές άδειες για το Aspose.PSD;
 Οι προσωρινές άδειες μπορούν να ληφθούν από[εδώ](https://purchase.aspose.com/temporary-license/).
### Είναι το Aspose.PSD κατάλληλο για εμπορική χρήση;
Ναι, το Aspose.PSD μπορεί να χρησιμοποιηθεί τόσο για προσωπικά όσο και για εμπορικά έργα υπό τους όρους αδειοδότησης του.