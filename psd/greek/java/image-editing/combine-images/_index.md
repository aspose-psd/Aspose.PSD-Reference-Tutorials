---
date: 2026-06-28
description: Μάθετε πώς να συνδυάσετε εικόνες java χρησιμοποιώντας το Aspose.PSD,
  να συγχωνεύσετε δύο εικόνες σε έναν καμβά PSD και να δημιουργήσετε ένα πολυεπίπεδο
  αρχείο σε λίγα λεπτά.
keywords:
- combine images java
- java graphics draw image
- merge images into psd
linktitle: Συνδυάστε Εικόνες
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  headline: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  type: TechArticle
- description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  name: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  steps:
  - name: Create PSD Options (prepare the file)
    text: '`PsdOptions` holds the configuration for the output PSD, such as compression
      level and color depth.'
  - name: Set the FileCreateSource (define where the PSD will be saved)
    text: '`FileCreateSource` tells Aspose where to write the generated file.'
  - name: Create Image Instance (initialize canvas size)
    text: The `Image` constructor creates a blank PSD canvas with the dimensions you
      specify.
  - name: Initialize Graphics and draw the first picture
    text: '`Graphics` provides drawing capabilities on the canvas. We clear the background
      to white and render the first source image on the left half.'
  - name: Draw the second picture (complete the combine)
    text: Now we place the second image on the right half of the same canvas, creating
      a second layer automatically.
  - name: Save the resulting PSD file
    text: Persist the combined canvas to disk. The resulting `combined.psd` contains
      two editable layers. Congratulations! You have successfully **combine images
      java** and generated a layered PSD file ready for further Photoshop editing.
  type: HowTo
- questions:
  - answer: Aspose.PSD natively reads and writes **15+ formats**, including PSD, PNG,
      JPEG, BMP, TIFF, GIF, and more, making it a versatile choice for image pipelines.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Each `drawImage` call creates a separate PSD layer, which you can
      later reposition, apply filters, or mask using Aspose.PSD’s extensive layer‑editing
      API.
    question: Can I perform additional edits after combining images?
  - answer: A valid license is required for production use. You can obtain one from
      the Aspose store; a free trial is available for evaluation.
    question: Do I need a commercial license for production?
  - answer: Simply repeat `graphics.drawImage(...)` with appropriate coordinates for
      each additional image. Each call adds a new layer.
    question: How do I add more than two pictures?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support, or consult the official documentation linked in the download page.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Συνδυάστε Εικόνες Java – Δημιουργήστε Αρχείο PSD Συγχωνεύοντας Εικόνες με Aspose.PSD
url: /el/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Συνδυασμός Εικόνων Java – Δημιουργία Αρχείου PSD Συγχωνεύοντας Εικόνες με το Aspose.PSD

## Εισαγωγή

Αν χρειάζεστε να **combine images java** συγχωνεύοντας πολλές εικόνες σε ένα ενιαίο αρχείο συμβατό με το Photoshop, το Aspose.PSD for Java κάνει τη διαδικασία απλή. Σε αυτό το tutorial θα δημιουργήσουμε έναν καμβά PSD 600 × 600 pixel, θα σχεδιάσουμε δύο πηγαίες εικόνες δίπλα-δίπλα και θα αποθηκεύσουμε το αποτέλεσμα ως αρχείο PSD με στρώσεις. Στο τέλος θα καταλάβετε γιατί αυτή η τεχνική είναι πολύτιμη για αυτοματοποιημένες γραφικές γραμμές παραγωγής και πώς να την επεκτείνετε σε οποιονδήποτε αριθμό εικόνων.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη είναι η καλύτερη για συγχώνευση εικόνων σε PSD;** Aspose.PSD for Java.
- **Πόσο διαρκεί ένας βασικός συνδυασμός;** Περίπου 10‑15 λεπτά για να γράψετε και να εκτελέσετε τον κώδικα.
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.
- **Μπορώ να προσθέσω περισσότερες από δύο εικόνες;** Απόλυτα – απλώς επαναλάβετε τις κλήσεις `drawImage` για κάθε επιπλέον στρώση.
- **Ποιες εκδόσεις της Java υποστηρίζονται;** Java 8 και νεότερες (έως Java 21).

## Τι είναι το combine images java;
*Combine images java* αναφέρεται στη προγραμματιστική συγχώνευση πολλαπλών ραστερ εικόνων σε ένα ενιαίο αρχείο εικόνας χρησιμοποιώντας Java APIs. Το Aspose.PSD παρέχει έναν υψηλού επιπέδου, καθαρό‑Java τρόπο για να το κάνετε αυτό χωρίς εξαρτήσεις από το Photoshop, επιτρέποντας την αυτοματοποίηση της σύνθεσης, τη διατήρηση των στρώσεων και την εξαγωγή ενός PSD συμβατού με το Photoshop που μπορεί να επεξεργαστεί αργότερα στο Photoshop ή σε άλλα εργαλεία που υποστηρίζουν PSD.

## Γιατί να συνδυάσετε εικόνες με το Aspose.PSD;
Το Aspose.PSD υποστηρίζει **15+ μορφές εικόνας** (συμπεριλαμβανομένων PSD, PNG, JPEG, BMP, TIFF, GIF και άλλων) και μπορεί να επεξεργαστεί **έγγραφα πολλαπλών εκατοντάδων σελίδων** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, χάρη στην αρχιτεκτονική ροής του. Η βιβλιοθήκη είναι **100 % managed Java**, επομένως εκτελείται σε οποιοδήποτε λειτουργικό σύστημα που υποστηρίζει το JDK, εξαλείφοντας τα προβλήματα με τις εγγενείς DLL.

## Προαπαιτούμενα

1. **Aspose.PSD Library** – κατεβάστε την από [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Απαιτείται Java 8+· Συνιστάται Java 11 ή νεότερη για καλύτερη απόδοση.  
3. **Working Directory** – ένας φάκελος στον υπολογιστή σας που περιέχει τις πηγαίες εικόνες (`example1.png`, `example2.png`) και όπου θα γραφτεί το αρχείο εξόδου PSD (`combined.psd`).  
4. **License Purchase** – αποκτήστε εμπορική άδεια [here](https://purchase.aspose.com/buy) για χρήση σε παραγωγή.  
5. **Other Aspose Releases** – εξερευνήστε πρόσθετα προϊόντα και ενημερώσεις [here](https://releases.aspose.com/).

## Εισαγωγή Πακέτων

Οι δηλώσεις `import` φέρνουν τις απαραίτητες κλάσεις του Aspose.PSD στο πεδίο ορατότητας.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdOptions;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.PsdImageLayer;
import com.aspose.psd.imageoptions.FileCreateSource;
import com.aspose.psd.graphics.Graphics;
import com.aspose.psd.Color;
```

## Πώς να συνδυάσετε εικόνες java χρησιμοποιώντας το Aspose.PSD;

Φορτώστε έναν κενό καμβά, σχεδιάστε κάθε εικόνα πάνω στον καμβά και, στη συνέχεια, αποθηκεύστε το αποτέλεσμα ως αρχείο PSD – αυτό είναι ολόκληρη η ροή εργασίας σε τρία σύντομα βήματα. Το API δημιουργεί αυτόματα ξεχωριστή στρώση για κάθε κλήση `drawImage`, παρέχοντάς σας πλήρη δυνατότητα επεξεργασίας στο Photoshop αργότερα.

### Βήμα 1: Δημιουργία PSD Options (προετοιμασία αρχείου)

`PsdOptions` περιέχει τη διαμόρφωση για το αρχείο εξόδου PSD, όπως το επίπεδο συμπίεσης και το βάθος χρώματος.

```java
PsdOptions psdOptions = new PsdOptions();
```

### Βήμα 2: Ορισμός του FileCreateSource (καθορισμός του σημείου αποθήκευσης του PSD)

`FileCreateSource` ενημερώνει το Aspose πού να γράψει το παραγόμενο αρχείο.

```java
psdOptions.setSource(new FileCreateSource(dataDir + "combined.psd", false));
```

### Βήμα 3: Δημιουργία Αντικειμένου Image (αρχικοποίηση μεγέθους καμβά)

Ο κατασκευαστής `Image` δημιουργεί έναν κενό καμβά PSD με τις διαστάσεις που καθορίζετε.

```java
Image image = new Image(psdOptions, 600, 600);
```

### Βήμα 4: Αρχικοποίηση Graphics και σχεδίαση της πρώτης εικόνας

`Graphics` παρέχει δυνατότητες σχεδίασης στον καμβά. Καθαρίζουμε το φόντο σε λευκό και αποδίδουμε την πρώτη πηγή εικόνας στο αριστερό μισό.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(dataDir + "example1.png", new Rectangle(0, 0, 300, 600));
```

### Βήμα 5: Σχεδίαση της δεύτερης εικόνας (ολοκλήρωση του συνδυασμού)

Τώρα τοποθετούμε τη δεύτερη εικόνα στο δεξιό μισό του ίδιου καμβά, δημιουργώντας αυτόματα μια δεύτερη στρώση.

```java
graphics.drawImage(dataDir + "example2.png", new Rectangle(300, 0, 300, 600));
```

### Βήμα 6: Αποθήκευση του παραγόμενου αρχείου PSD

Αποθηκεύστε τον συνδυασμένο καμβά στο δίσκο. Το παραγόμενο `combined.psd` περιέχει δύο επεξεργάσιμες στρώσεις.

```java
image.save();
```

Συγχαρητήρια! Έχετε ολοκληρώσει με επιτυχία το **combine images java** και δημιουργήσατε ένα αρχείο PSD με στρώσεις, έτοιμο για περαιτέρω επεξεργασία στο Photoshop.

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| `File not found` κατά τη φόρτωση των πηγαίων εικόνων | Λανθασμένη διαδρομή `dataDir` | Επαληθεύστε ότι το `dataDir` δείχνει στον φάκελο που περιέχει τα `example1.png` και `example2.png`. |
| Το αρχείο PSD εξόδου είναι κενό | `graphics.clear` κλήθηκε μετά το σχεδιασμό | Κλήστε `graphics.clear(Color.getWhite())` **πριν** από οποιεσδήποτε λειτουργίες `drawImage`. |
| Εξαίρεση άδειας κατά την εκτέλεση | Λείπει ή έχει λήξει η άδεια Aspose.PSD | Εφαρμόστε μια έγκυρη άδεια χρησιμοποιώντας `License license = new License(); license.setLicense("Aspose.PSD.lic");` πριν από οποιαδήποτε κλήση API. |

## Συχνές Ερωτήσεις

**Q: Είναι το Aspose.PSD συμβατό με όλες τις μορφές εικόνας;**  
A: Το Aspose.PSD διαβάζει και γράφει εγγενώς **15+ μορφές**, συμπεριλαμβανομένων PSD, PNG, JPEG, BMP, TIFF, GIF και άλλων, καθιστώντας το μια ευέλικτη επιλογή για γραμμές επεξεργασίας εικόνας.

**Q: Μπορώ να πραγματοποιήσω πρόσθετες επεξεργασίες μετά το συνδυασμό των εικόνων;**  
A: Ναι. Κάθε κλήση `drawImage` δημιουργεί μια ξεχωριστή στρώση PSD, την οποία μπορείτε αργότερα να μετακινήσετε, να εφαρμόσετε φίλτρα ή μάσκα χρησιμοποιώντας το εκτενές API επεξεργασίας στρώσεων του Aspose.PSD.

**Q: Χρειάζομαι εμπορική άδεια για παραγωγή;**  
A: Απαιτείται έγκυρη άδεια για χρήση σε παραγωγή. Μπορείτε να αποκτήσετε μία από το κατάστημα Aspose· μια δωρεάν δοκιμή είναι διαθέσιμη για αξιολόγηση.

**Q: Πώς μπορώ να προσθέσω περισσότερες από δύο εικόνες;**  
A: Απλώς επαναλάβετε `graphics.drawImage(...)` με τις κατάλληλες συντεταγμένες για κάθε πρόσθετη εικόνα. Κάθε κλήση προσθέτει μια νέα στρώση.

**Q: Πού μπορώ να λάβω βοήθεια αν αντιμετωπίσω προβλήματα;**  
A: Επισκεφθείτε το [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) για υποστήριξη της κοινότητας ή συμβουλευτείτε την επίσημη τεκμηρίωση που συνδέεται στη σελίδα λήψης.

---

**Τελευταία Ενημέρωση:** 2026-06-28  
**Δοκιμάστηκε Με:** Aspose.PSD 24.11 for Java  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Δημιουργία Εικόνας με Ορισμό Διαδρομής στο Aspose.PSD για Java](/psd/java/image-editing/create-image-by-setting-path/)
- [Δημιουργία Εικόνας χρησιμοποιώντας Stream στο Aspose.PSD για Java](/psd/java/image-editing/create-image-using-stream/)
- [Αλλαγή Μεγέθους Εικόνας Java - Χρήση της Καταμέτρησης Resize Type στο Aspose.PSD για Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

```java
PsdOptions imageOptions = new PsdOptions();
```

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

```java
Image image = Image.create(imageOptions, 600, 600);
```

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

```java
image.save();
```