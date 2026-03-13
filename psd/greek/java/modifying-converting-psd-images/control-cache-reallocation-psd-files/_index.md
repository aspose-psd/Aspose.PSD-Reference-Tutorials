---
date: 2026-03-13
description: Μάθετε πώς να δημιουργείτε έργα Java με εικόνες PSD, διαχειριζόμενοι
  την επανακατανομή της κρυφής μνήμης με το Aspose.PSD for Java. Βελτιστοποιήστε αποδοτικά
  τη μνήμη και τη χρήση του δίσκου.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Δημιουργία εικόνας PSD Java – Έλεγχος επανακατανομής κρυφής μνήμης
url: /el/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Έλεγχος Επανακατανομής Cache σε Αρχεία PSD

## Εισαγωγή
Αν χρειάζεστε να **create PSD image java** έργα αποδοτικά, ο έλεγχος της επανακατανομής του cache είναι απαραίτητος. Όταν εργάζεστε με εικόνες και αρχεία Photoshop προγραμματιστικά, η αποδοτικότητα είναι καθοριστικός παράγοντας. Το Aspose.PSD for Java προσφέρει ισχυρές δυνατότητες για τη διαχείριση και την επεξεργασία αρχείων PSD απρόσκοπτα. Ένα από τα θεμελιώδη στοιχεία της βελτιστοποίησης της απόδοσης είναι ο έλεγχος της επανακατανομής του cache. Η διαχείριση του cache βοηθά στη διατήρηση της ισορροπίας μεταξύ μνήμης και χρήσης δίσκου, εξασφαλίζοντας ότι η εφαρμογή σας λειτουργεί ομαλά, χωρίς απρόσμενα σφάλματα ή επιβραδύνσεις. 

## Γρήγορες Απαντήσεις
- **Τι κάνει η επανακατανομή του cache;** Ισορροπεί τη χρήση μνήμης και δίσκου κατά την επεξεργασία μεγάλων αρχείων PSD.  
- **Ποιος τύπος cache είναι ο καλύτερος για μεγάλες εικόνες;** `CacheOnDiskOnly` διατηρεί τη μνήμη ελεύθερη αποθηκεύοντας το cache στον δίσκο.  
- **Πόσο χώρο δίσκου μπορώ να διαθέσω;** Έως 1 GB (ή οποιοδήποτε μέγεθος ορίσετε με `setMaxDiskSpaceForCache`).  
- **Χρειάζεται άδεια για τη χρήση αυτών των λειτουργιών;** Μια άδεια αφαιρεί τους περιορισμούς της δοκιμαστικής έκδοσης· δείτε τη σελίδα αγοράς της Aspose.  
- **Μπορώ να παρακολουθήσω τη χρήση του cache σε χρόνο εκτέλεσης;** Ναι, χρησιμοποιήστε `Cache.getAllocatedDiskBytesCount()` και `Cache.getAllocatedMemoryBytesCount()`.

## Γιατί να Ελέγχετε την Επανακατανομή του Cache;
Η διαχείριση του cache είναι κρίσιμη όταν **create PSD image java** εφαρμογές που χειρίζονται αρχεία υψηλής ανάλυσης ή πολλαπλών στρωμάτων. Οι σωστές ρυθμίσεις του cache αποτρέπουν σφάλματα έλλειψης μνήμης, μειώνουν τις παύσεις του GC και παρέχουν προβλέψιμη απόδοση σε διακομιστές ή εφαρμογές επιφάνειας εργασίας.

## Προαπαιτούμενα
Πριν περάσουμε στο τμήμα κώδικα, υπάρχουν μερικά πράγματα που πρέπει να διασφαλίσετε ώστε όλα να λειτουργούν ομαλά:
1. Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκατεστημένο το JDK στο μηχάνημά σας. Μπορείτε να το κατεβάσετε από [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Πρέπει να κατεβάσετε τη βιβλιοθήκη Aspose.PSD. Μπορείτε να βρείτε την τελευταία έκδοση [here](https://releases.aspose.com/psd/java/).
3. IDE Setup: Ένα Integrated Development Environment (IDE) όπως το IntelliJ IDEA ή το Eclipse θα κάνει τη διαχείριση του κώδικά σας πιο εύκολη.
4. Basic Understanding of Java: Η εξοικείωση με τον προγραμματισμό Java θα σας βοηθήσει να κατανοήσετε καλύτερα τις έννοιες και τα αποσπάσματα κώδικα.
5. Aspose License (Optional): Εάν θέλετε να αφαιρέσετε υδατογραφήματα και να αποκτήσετε πλήρη λειτουργικότητα, σκεφτείτε να αγοράσετε άδεια [here](https://purchase.aspose.com/buy) ή δοκιμάστε τη δωρεάν δοκιμή [here](https://releases.aspose.com/).

## Εισαγωγή Πακέτων
Πριν ξεκινήσουμε να γράφουμε τον κώδικα, ας βεβαιωθούμε ότι έχουμε εισάγει τα απαραίτητα πακέτα. Παρακάτω υπάρχει μια σύντομη λίστα με το τι πρέπει να συμπεριλάβετε στην αρχή του αρχείου Java:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## Πώς να Δημιουργήσετε PSD Image Java με Έλεγχο Cache
Παρακάτω υπάρχει ένας βήμα‑βήμα οδηγός που συνδέει τη διαμόρφωση του cache άμεσα με τη διαδικασία δημιουργίας μιας PSD εικόνας σε Java.

### Βήμα 1: Ρύθμιση του Καταλόγου Δεδομένων σας
Πρώτα απ' όλα, θα χρειαστεί να δημιουργήσετε έναν φάκελο όπου θα αποθηκεύονται τα αρχεία cache. Αυτό είναι απαραίτητο για αποτελεσματική διαχείριση του cache.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Ορίζει τον φάκελο για το cache του εγγράφου σας.  
- `Cache.setCacheFolder(dataDir)`: Αυτή η μέθοδος ορίζει το φάκελο cache στον καθορισμένο κατάλογο. Οποιοδήποτε cache δημιουργηθεί από το Aspose θα αποθηκεύεται εδώ αντί για τον προεπιλεγμένο προσωρινό φάκελο.

### Βήμα 2: Διαμόρφωση Cache στον Δίσκο
Στη συνέχεια, θα καθορίσουμε ότι το cache μας πρέπει να αποθηκεύεται μόνο στον δίσκο. Αυτό είναι ιδιαίτερα χρήσιμο εάν η εφαρμογή σας χρησιμοποιεί μεγάλα αρχεία και θέλετε η μνήμη να παραμένει ελεύθερη.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Αυτή η επιλογή εξασφαλίζει ότι το cache δεν θα κρατηθεί στη μνήμη, κάτι που είναι ωφέλιμο για την επεξεργασία μεγάλων αρχείων PSD χωρίς υπερβολική κατανάλωση RAM.

### Βήμα 3: Ορισμός Μέγιστου Μεγέθους Cache Δίσκου και Μνήμης
Τώρα, ας περιορίσουμε τα μεγέθη του cache. Αυτό είναι κρίσιμο επειδή ένα απεριόριστο cache μπορεί να προκαλέσει προβλήματα απόδοσης.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Ορίζει όριο 1 GB για το cache στον δίσκο. Μπορείτε να προσαρμόσετε αυτό το μέγεθος ανάλογα με τις ανάγκες σας.  
- `Cache.setMaxMemoryForCache(1073741824)`: Ομοίως, περιορίζει το cache στη μνήμη, διασφαλίζοντας ότι η εφαρμογή σας δεν θα χρησιμοποιήσει υπερβολική μνήμη.

### Βήμα 4: Διαχείριση Στρατηγικής Επανακατανομής Cache
Η διαχείριση του τρόπου επανακατανομής του cache είναι απαραίτητη για τη διατήρηση της απόδοσης. Δείτε πώς μπορείτε να το ρυθμίσετε.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Όταν οριστεί σε `false`, επιτρέπει στο Aspose να διαχειρίζεται την επανακατανομή του cache πιο ευέλικτα, κάτι που μπορεί να οδηγήσει σε καλύτερη απόδοση.

### Βήμα 5: Έλεγχος Κατανεμημένου Μεγέθους Cache
Αυτό το βήμα αφορά την παρακολούθηση του πόσα bytes είναι αυτή τη στιγμή κατανεμημένα για το cache στη μνήμη ή στον δίσκο. Ας το υλοποιήσουμε:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Αποθηκεύει τον αριθμό των bytes που έχουν κατανεμηθεί στον δίσκο.  
- `long l2`: Αποθηκεύει τον αριθμό των bytes που έχουν κατανεμηθεί στη μνήμη.  
Μπορείτε να ελέγχετε αυτές τις τιμές ανά πάσα στιγμή για να βεβαιωθείτε ότι η εφαρμογή σας διαχειρίζεται τη μνήμη και τη χρήση του δίσκου όπως αναμένεται.

### Βήμα 6: Δημιουργία PSD Εικόνας
Τώρα που έχουμε ρυθμίσει τις παραμέτρους του cache, ας δημιουργήσουμε μια απλή PSD εικόνα.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Αυτό το αντικείμενο σας επιτρέπει να ορίσετε επιλογές κατά τη δημιουργία μιας εικόνας Photoshop.  
- `Color[] color`: Ένας πίνακας που περιέχει τα χρώματα που θα χρησιμοποιηθούν στην παλέτα της εικόνας.

### Βήμα 7: Αποθήκευση Δεδομένων Pixel στην Εικόνα
Τώρα, ας γεμίσουμε την εικόνα μας με δεδομένα pixel και να την αποθηκεύσουμε.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Αυτός είναι ένας πίνακας αντικειμένων χρώματος. Εδώ, τον γεμίζουμε με λευκά pixel.  
- `image.savePixels(image.getBounds(), pixels)`: Αυτή η μέθοδος αποθηκεύει τα δεδομένα pixel στην εικόνα. Ενημερώνει την εικόνα με τα χρώματα που ορίσαμε.

### Βήμα 8: Παρακολούθηση Κατανεμημένου Cache μετά τη Δημιουργία Εικόνας
Μετά τη δημιουργία της εικόνας, είναι καλή πρακτική να ελέγξετε ξανά πόσα bytes είναι κατανεμημένα για το cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Καταγράφει την τρέχουσα κατανομή στον δίσκο μετά τη δημιουργία της εικόνας.  
- `long memoryBytes`: Καταγράφει την τρέχουσα κατανομή στη μνήμη.  
Αυτό το βήμα θα σας βοηθήσει να προσδιορίσετε πόσο cache καταναλώνεται μετά τις λειτουργίες σας.

### Βήμα 9: Έλεγχος Κατάλληλης Καταστροφής
Τέλος, είναι κρίσιμο να διασφαλίσετε ότι όλα τα αντικείμενα Aspose.PSD έχουν καταστραφεί σωστά ώστε να αποφευχθούν διαρροές μνήμης.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` και `l2`: Αυτές οι μεταβλητές θα σας βοηθήσουν να ελέγξετε την τελική κατανομή. Εάν δεν είναι μηδέν, υποδεικνύει ότι κάποια αντικείμενα δεν έχουν καταστραφεί σωστά.

## Συνηθισμένα Προβλήματα και Λύσεις
- **Cache folder not created** – Επαληθεύστε ότι η εφαρμογή έχει δικαιώματα εγγραφής για τη διαδρομή που περάσατε στο `Cache.setCacheFolder`.  
- **Out‑of‑memory errors** – Επαληθεύστε ξανά ότι το `Cache.setCacheType(CacheType.CacheOnDiskOnly)` έχει εφαρμοστεί πριν τη φόρτωση μεγάλων αρχείων PSD.  
- **Unexpected cache size** – Χρησιμοποιήστε τις μεθόδους `Cache.getAllocated*BytesCount()` μετά από κάθε σημαντική λειτουργία για να παρακολουθείτε την αύξηση.

## Συχνές Ερωτήσεις

**Q: What is Aspose.PSD?**  
A: Το Aspose.PSD είναι μια βιβλιοθήκη για προγραμματιστές .NET και Java που επιτρέπει τη δημιουργία, επεξεργασία και μετατροπή αρχείων Photoshop (PSD) προγραμματιστικά.

**Q: How do I check allocated cache size?**  
A: Χρησιμοποιήστε μεθόδους όπως `Cache.getAllocatedDiskBytesCount()` και `Cache.getAllocatedMemoryBytesCount()` για να παρακολουθείτε τη τρέχουσα χρήση του cache.

**Q: Can I set a custom directory for cache?**  
A: Ναι, μπορείτε να ορίσετε διαφορετικό φάκελο χρησιμοποιώντας `Cache.setCacheFolder("Your Directory Path")`.

**Q: Is Aspose.PSD free to use?**  
A: Το Aspose.PSD είναι εμπορική βιβλιοθήκη, αλλά μπορείτε να ξεκινήσετε με μια δωρεάν δοκιμή που διατίθεται στην [website](https://releases.aspose.com/).

**Q: What happens if I don’t dispose of objects?**  
A: Η μη καταστροφή των αντικειμένων μπορεί να οδηγήσει σε διαρροές μνήμης, προκαλώντας την εφαρμογή σας να χρησιμοποιεί περισσότερους πόρους από το απαραίτητο.

## Συμπέρασμα
Ο έλεγχος της επανακατανομής του cache ενώ **create PSD image java** εφαρμογές μπορεί να κάνει σημαντική διαφορά στην απόδοση. Ακολουθώντας τα παραπάνω βήματα, θα διαχειρίζεστε αποτελεσματικά το cache, θα ελαχιστοποιείτε την κατανάλωση μνήμης και θα παράγετε αρχεία PSD υψηλής ποιότητας με το Aspose.PSD for Java. Εφαρμόστε αυτές τις τεχνικές και τα έργα σας θα λειτουργούν πιο ομαλά και θα κλιμακώνονται καλύτερα.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}