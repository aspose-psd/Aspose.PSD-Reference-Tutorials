---
date: 2026-06-08
description: Μάθετε πώς να αποθηκεύσετε PSD ως PNG χρησιμοποιώντας το Aspose.PSD for
  Java και να διακόψετε τη μετατροπή όταν χρειάζεται. Διαχειριστείτε αποτελεσματικά
  τη ροή εργασίας εικόνας.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Υποστήριξη για Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Πώς να αποθηκεύσετε PSD ως PNG με Interrupt Monitor στο Aspose.PSD for Java
url: /el/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση PSD ως PNG με Interrupt Monitor στο Aspose.PSD για Java

## Εισαγωγή

Αν χρειάζεστε να **save PSD as PNG** ενώ διατηρείτε πλήρη έλεγχο πάνω σε μακροχρόνιες μετατροπές, το Interrupt Monitor του Aspose.PSD for Java σας παρέχει ακριβώς αυτό. Σε αυτό το tutorial θα περάσουμε από τη ρύθμιση του monitor, τη μετατροπή ενός αρχείου PSD σε PNG, και την ασφαλή διακοπή της λειτουργίας όταν απαιτείται. Θα δείτε επίσης πώς αυτό εντάσσεται σε μια τυπική ροή επεξεργασίας εικόνας και γιατί είναι απαραίτητο για αξιόπιστες εφαρμογές.

## Γρήγορες Απαντήσεις
- **Μπορώ να διακόψω μια μετατροπή PSD‑σε‑PNG;** Yes, use `InterruptMonitor` to stop the process on demand.  
- **Ποια μέθοδος αποθηκεύει ένα PSD ως PNG;** Call `save(outputPath, new PngOptions())`.  
- **Χρειάζομαι άδεια για παραγωγή;** A commercial license is required; a free trial is available.  
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 and later are fully supported.  
- **Είναι η βιβλιοθήκη thread‑safe;** Conversions can run in separate threads; the monitor handles interruptions safely.

## Απαιτούμενα

Πριν εμβαθύνετε στις λεπτομέρειες χρήσης του Interrupt Monitor, βεβαιωθείτε ότι έχετε τα παρακάτω:

- **Java Development Environment:** Ρυθμίστε ένα περιβάλλον ανάπτυξης Java στο σύστημά σας.  
- **Aspose.PSD Library:** Αποκτήστε τη βιβλιοθήκη Aspose.PSD for Java. Μπορείτε να τη κατεβάσετε [here](https://releases.aspose.com/psd/java/). Μπορείτε επίσης να επισκεφθείτε την κύρια ιστοσελίδα Aspose [here](https://releases.aspose.com/).  
- **Document Directory:** Διατηρήστε έναν καθορισμένο φάκελο για τα έγγραφα PSD σας.

## Εισαγωγή Πακέτων

Ξεκινήστε εισάγοντας τα απαραίτητα πακέτα στο έργο Java σας. Αυτό εξασφαλίζει ότι έχετε πρόσβαση στις λειτουργίες του Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Τώρα, ας αναλύσουμε το παράδειγμα κώδικα βήμα‑βήμα για την ενσωμάτωση του Interrupt Monitor στο έργο Aspose.PSD for Java.

## Πώς να αποθηκεύσετε PSD ως PNG χρησιμοποιώντας το Interrupt Monitor;

`PsdImage` αντιπροσωπεύει ένα έγγραφο PSD που έχει φορτωθεί στη μνήμη.  
`SaveImageWorker` εκτελεί τη μετατροπή της εικόνας σε ξεχωριστό νήμα.  

Φορτώστε το αρχείο PSD με `new PsdImage("source.psd")`, συνδέστε ένα `InterruptMonitor` στο `SaveImageWorker` και καλέστε `save("output.png", new PngOptions())`. Το monitor παρακολουθεί για αίτημα ακύρωσης και διακόπτει την μετατροπή καθαρά, επιστρέφοντας τον έλεγχο στην εφαρμογή σας μέσα σε χιλιοστά του δευτερολέπτου.

### Βήμα 1: Ορίστε τον Φάκελο Εγγράφων σας

```java
String dataDir = "Your Document Directory";
```

Βεβαιωθείτε ότι αντικαθιστάτε το “Your Document Directory” με την πραγματική διαδρομή όπου αποθηκεύονται τα έγγραφα PSD σας.

### Βήμα 2: Ορίστε τις Επιλογές Εικόνας και τη Διαδρομή Εξόδου

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Καθορίστε τις επιλογές εικόνας, το αρχείο PSD προέλευσης και τη ζητούμενη διαδρομή εξόδου για τη μετατρεπόμενη εικόνα.

### Βήμα 3: Αρχικοποιήστε το Interrupt Monitor και το SaveImageWorker

Η κλάση `InterruptMonitor` παρακολουθεί μια εκτελούμενη μετατροπή και μπορεί να τη διακόψει όταν κληθεί η `requestInterrupt()`.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Δημιουργήστε στιγμιότυπα του `InterruptMonitor` και του `SaveImageWorker`, συνδέοντας το monitor με το νήμα μετατροπής εικόνας.

### Βήμα 4: Εκκινήστε το Νήμα Μετατροπής Εικόνας

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Ξεκινήστε ένα νέο νήμα για τη διαδικασία μετατροπής εικόνας και εισάγετε μια περίοδο timeout για να προβλέψετε πιθανή διακοπή.

### Βήμα 5: Διακόψτε τη Διαδικασία

Καλώντας `monitor.requestInterrupt()` στέλνετε σήμα στο monitor να διακόψει την τρέχουσα μετατροπή.

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Διακόψτε τη διαδικασία μετατροπής εικόνας χρησιμοποιώντας το `InterruptMonitor` και περιμένετε να ολοκληρωθεί η διακοπή. Τέλος, καθαρίστε διαγράφοντας το αρχείο εξόδου.

## Γιατί να χρησιμοποιήσετε το Interrupt Monitor για μετατροπή PSD‑σε‑PNG;

Το Aspose.PSD υποστηρίζει **30+ μορφές εξόδου**, όπως PNG, JPEG, BMP και TIFF, και μπορεί να επεξεργαστεί αρχεία έως **500 MB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη. Προσθέτοντας ένα interrupt monitor μειώνετε την άσκοπη χρήση CPU και βελτιώνετε την ανταπόκριση σε pipelines επεξεργασίας παρτίδων, ειδικά όταν μια μετατροπή υπερβαίνει τα αναμενόμενα χρονικά όρια.

## Κοινά Προβλήματα και Λύσεις

- **Η μετατροπή κρέμεται επ' άπειρο:** Ensure the monitor is attached **before** calling `save`.  
- **Το αρχείο εξόδου είναι κατεστραμμένο μετά τη διακοπή:** The monitor aborts cleanly; however, always check if the file exists before using it.  
- **Ανησυχίες σχετικά με το thread‑safety:** Run each conversion in its own thread; the monitor only affects its associated worker.

## Συχνές Ερωτήσεις

**Q1: Τι είναι το Interrupt Monitor στο Aspose.PSD for Java;**  
A: Το Interrupt Monitor επιτρέπει στους προγραμματιστές να παύσουν ή να ακυρώσουν μακροχρόνιες μετατροπές εικόνας, παρέχοντας έλεγχο σε πραγματικό χρόνο της χρήσης πόρων.

**Q2: Πώς μπορώ να αποκτήσω τη βιβλιοθήκη Aspose.PSD για Java;**  
A: Μπορείτε να κατεβάσετε τη βιβλιοθήκη Aspose.PSD for Java [here](https://releases.aspose.com/psd/java/).

**Q3: Υπάρχει δωρεάν δοκιμαστική έκδοση για το Aspose.PSD for Java;**  
A: Ναι, μπορείτε να εξερευνήσετε μια δωρεάν δοκιμαστική έκδοση του Aspose.PSD [here](https://releases.aspose.com/).

**Q4: Πού μπορώ να βρω υποστήριξη για το Aspose.PSD for Java;**  
A: Επισκεφθείτε το φόρουμ υποστήριξης του Aspose.PSD for Java [here](https://forum.aspose.com/c/psd/34).

**Q5: Πώς μπορώ να αγοράσω άδεια για το Aspose.PSD for Java;**  
A: Μπορείτε να αγοράσετε άδεια για το Aspose.PSD for Java [here](https://purchase.aspose.com/buy).

**Q6: Μπορώ να μετατρέψω πολλαπλά αρχεία PSD σε PNG παράλληλα;**  
A: Ναι, δημιουργήστε ξεχωριστό νήμα για κάθε αρχείο και συνδέστε ένα ατομικό `InterruptMonitor` σε κάθε εργαζόμενο μετατροπής.

**Q7: Η βιβλιοθήκη διαχειρίζεται προφίλ χρωμάτων κατά τη μετατροπή PSD‑σε‑PNG;**  
A: Απόλυτα· το Aspose.PSD διατηρεί τα ενσωματωμένα ICC προφίλ και τα εφαρμόζει αυτόματα στο εξαγόμενο PNG.

---

**Τελευταία ενημέρωση:** 2026-06-08  
**Δοκιμή με:** Aspose.PSD 23.12 for Java  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Αποθήκευση PSD ως PNG και Εφαρμογή Rendering Drop Shadow στο Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Εξαγωγή PSD σε PNG & Προσθήκη Νέας Κανονικής Στρώσης χρησιμοποιώντας Aspose.PSD for Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Υποστήριξη Interrupt Monitor σε Αρχεία PSD - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}