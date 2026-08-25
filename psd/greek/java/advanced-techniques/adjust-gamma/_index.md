---
date: 2026-08-01
description: Μάθετε πώς να ρυθμίσετε το γάμμα στην επεξεργασία εικόνας Java με το
  Aspose.PSD, να μετατρέψετε PSD σε TIFF και να διορθώσετε εικόνες που έχουν ξεθωριάσει
  σε ένα σύντομο σεμινάριο.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Ρύθμιση γάμμα μιας εικόνας
og_description: Μάθετε πώς να ρυθμίσετε το γάμμα στην επεξεργασία εικόνας Java χρησιμοποιώντας
  το Aspose.PSD – μια γρήγορη βιβλιοθήκη διακομιστή που διορθώνει εικόνες που έχουν
  ξεθωριάσει και μετατρέπει PSD σε TIFF με λίγες μόνο γραμμές κώδικα.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: πώς να ρυθμίσετε το γάμμα – επεξεργασία Java με το Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Πώς να ρυθμίσετε το γάμμα στην επεξεργασία εικόνας Java με το Aspose.PSD
url: /el/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Ρυθμίσετε το Γάμμα στην Επεξεργασία Εικόνας Java με το Aspose.PSD

## Εισαγωγή

Αν εργάζεστε με **java image processing**, η εκμάθηση **πώς να ρυθμίσετε το γάμμα** είναι μια βασική τεχνική για τη βελτίωση της φωτεινότητας και της αντίθεσης χωρίς να χάνονται λεπτομέρειες. Σε αυτό το tutorial θα δούμε πώς να χρησιμοποιήσετε το **Aspose.PSD for Java** για να εφαρμόσετε διόρθωση γάμμα σε ένα αρχείο PSD, **να μετατρέψετε το PSD σε TIFF**, και να αποφύγετε μια **ξεθωριασμένη εικόνα**. Θα δείτε γιατί αυτή η προσέγγιση είναι γρήγορη, αξιόπιστη και ιδανική για **server‑side image processing** pipelines.

## Γρήγορες Απαντήσεις
- **Τι κάνει η διόρθωση γάμμα;** Αναπροσαρμόζει τις τιμές φωτεινότητας ώστε οι σκοτεινές περιοχές να γίνονται πιο φωτεινές ή οι φωτεινές περιοχές πιο σκοτεινές, διατηρώντας τη συνολική λεπτομέρεια.  
- **Ποια βιβλιοθήκη διαχειρίζεται την επεξεργασία;** Το Aspose.PSD for Java παρέχει τη μέθοδο `adjustGamma` για raster εικόνες.  
- **Μπορώ να μετατρέψω PSD σε TIFF στην ίδια ροή;** Ναι – μετά τη ρύθμιση γάμμα μπορείτε να αποθηκεύσετε την εικόνα απευθείας σε TIFF χρησιμοποιώντας `TiffOptions`.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγική χρήση.  
- **Ποια έκδοση Java υποστηρίζεται;** Το Aspose.PSD υποστηρίζει Java 8 και νεότερες.

## Τι είναι η Διόρθωση Γάμμα σε Java;

Η διόρθωση γάμμα αλλάζει τη μη γραμμική σχέση μεταξύ των κωδικοποιημένων τιμών pixel και της εμφανιζόμενης φωτεινότητας. Με την προσαρμογή της καμπύλης γάμμα μπορείτε **να διορθώσετε προβλήματα ξεθωριασμένης εικόνας** ή να ενισχύσετε λεπτομέρειες στις σκιές χωρίς υπερβολική έκθεση των φωτεινών περιοχών. Λειτουργεί εφαρμόζοντας μια συνάρτηση δύναμης σε κάθε pixel, φωτίζοντας τα σκοτεινά τόνους και συμπιέζοντας τα φωτεινά, προσφέροντας πιο φυσική οπτική εμφάνιση.

## Γιατί να Χρησιμοποιήσετε το Aspose.PSD για Διόρθωση Γάμμα;

Το Aspose.PSD είναι μια **java image processing library** που αφαιρεί τις πολυπλοκότητες της μορφής PSD. Υποστηρίζει επεξεργασία αρχείων έως 2 GB, διαχειρίζεται πάνω από 50 διαφορετικές μορφές εικόνας, και παρέχει μια απλή κλήση `adjustGamma`, καθιστώντας το ιδανικό για **java gamma correction** και **convert PSD to TIFF** workflows.

## Προαπαιτούμενα

1. **Περιβάλλον Ανάπτυξης Java** – Εγκατεστημένο Java 8 ή νεότερο.  
2. **Βιβλιοθήκη Aspose.PSD** – Κατεβάστε και προσθέστε το JAR στο πρότζεκτ σας. Δείτε την επίσημη [documentation](https://reference.aspose.com/psd/java/).  
3. **Δείγμα Εικόνας** – Ένα αρχείο PSD που θέλετε να επεξεργαστείτε (π.χ., `sample.psd`).  

## Εισαγωγή Πακέτων

Πριν ξεκινήσετε, εισάγετε τα απαραίτητα namespaces που σας δίνουν πρόσβαση στη διαχείριση raster και στις επιλογές μορφής αρχείου.

## Βήμα 1: Φόρτωση της Εικόνας

Η κλάση `RasterImage` αντιπροσωπεύει τα rasterized pixel δεδομένα ενός στρώματος PSD στη μνήμη. Η φόρτωση της εικόνας μία φορά και η αποθήκευση στην cache μειώνει την κατανάλωση μνήμης για επόμενες ρυθμίσεις.

## Βήμα 2: Ρύθμιση Γάμμα

Φορτώστε το PSD με `new RasterImage("sample.psd")` και καλέστε `rasterImage.adjustGamma(2.0f)` — αυτή η εντολή εφαρμόζει γάμμα 2.0 σε όλα τα κανάλια χρώματος, φωτίζοντας τις σκιές ενώ διατηρεί τα φωτεινά αμετάβλητα. Μπορείτε να περάσετε ξεχωριστές τιμές για κόκκινο, πράσινο και μπλε αν απαιτούνται ρυθμίσεις ανά κανάλι.

## Βήμα 3: Δημιουργία TiffOptions

Το `TiffOptions` σας επιτρέπει να ελέγξετε τη συμπίεση, τα bits ανά δείγμα, και άλλες ρυθμίσεις ειδικές για TIFF. Ορίζοντας ένα 8‑bit δείγμα (`{8,8,8}`) διατηρεί το μέγεθος του αρχείου TIFF λογικό ενώ διασφαλίζει την πιστότητα του χρώματος.

## Βήμα 4: Αποθήκευση της Τελικής Εικόνας

Καλέστε `rasterImage.save("output.tif", tiffOptions)` για να γράψετε την επεξεργασμένη εικόνα στο δίσκο. Μετά την αποθήκευση, μπορείτε να τροφοδοτήσετε το TIFF σε downstream συστήματα όπως υπηρεσίες εκτύπωσης ή web APIs.

## Συνηθισμένες Περιπτώσεις Χρήσης

- **Αυτοματοποιημένα pipelines γραφικών** – Ρυθμίστε το γάμμα εν κινήσει πριν τη δημιουργία μικρογραφιών.  
- **Εργαλεία μαζικής μετατροπής** – Μετατρέψτε μεγάλες αρχειοθήκες PSD σε TIFF ενώ ομαλοποιείτε τη φωτεινότητα.  
- **Web services** – Εκθέστε ένα endpoint που λαμβάνει PSD, εφαρμόζει διόρθωση γάμμα, και επιστρέφει TIFF για χρήση από τον πελάτη.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί Συμβαίνει | Πώς να Διορθώσετε |
|----------|------------------|-------------------|
| **Η εικόνα φαίνεται ξεθωριασμένη** | Η τιμή γάμμα είναι πολύ υψηλή (π.χ., > 2.5) | Μειώστε τον παράγοντα γάμμα σε τιμή μεταξύ 1.8 και 2.2. |
| **`rasterImage.isCached()` επιστρέφει false** | Η εικόνα δεν έχει φορτωθεί ακόμη στη μνήμη | Καλέστε `rasterImage.cacheData()` πριν τη ρύθμιση γάμμα. |
| **Το αρχείο TIFF είναι μεγάλο** | Τα bits ανά δείγμα έχουν οριστεί σε 16‑bit | Χρησιμοποιήστε δείγμα 8‑bit (`{8,8,8}`) όπως φαίνεται στο παράδειγμα. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να εφαρμόσω διαφορετικές τιμές γάμμα σε κάθε κανάλι χρώματος;**  
Α: Ναι – η μέθοδος `adjustGamma` δέχεται ξεχωριστές τιμές float για τα κανάλια κόκκινο, πράσινο και μπλε.

**Ε: Είναι δυνατόν να αλυσίδω πολλαπλές ρυθμίσεις εικόνας πριν την αποθήκευση;**  
Α: Απόλυτα. Μπορείτε να εκτελέσετε αλλαγές μεγέθους, περικοπής ή χρωματικών διορθώσεων διαδοχικά στην ίδια παρουσία `RasterImage`.

**Ε: Υποστηρίζει το Aspose.PSD αρχεία PSD πολλαπλών σελίδων;**  
Α: Ναι, κάθε στρώμα μπορεί να προσπελαστεί και να επεξεργαστεί ξεχωριστά.

**Ε: Σε ποιες μορφές μπορώ να εξάγω εκτός από TIFF;**  
Α: Το Aspose.PSD υποστηρίζει PNG, JPEG, BMP και πολλές άλλες μορφές μέσω των αντίστοιχων κλάσεων επιλογών.

**Ε: Πώς να αποφύγω μια ξεθωριασμένη εικόνα μετά τη διόρθωση γάμμα;**  
Α: Ξεκινήστε με μέτριο γάμμα (περίπου 2.0) και προεπισκοπήστε το αποτέλεσμα· μειώστε το αν η εικόνα φαίνεται πολύ φωτεινή.

## Συμπέρασμα

Συγχαρητήρια! Μάθατε **πώς να ρυθμίσετε το γάμμα** σε μια **java image processing** ροή εργασίας, μετατρέψατε ένα PSD σε TIFF, και αποφύγατε κοινά προβλήματα όπως μια **ξεθωριασμένη εικόνα**. Αυτό το μοτίβο σας δίνει λεπτομερή έλεγχο πάνω στη φωτεινότητα και την αντίθεση, καθιστώντας το ιδανικό για αυτοματοποιημένα pipelines γραφικών, web services ή επιτραπέζιες εφαρμογές.

---

**Τελευταία Ενημέρωση:** 2026-08-01  
**Δοκιμή Με:** Aspose.PSD 24.11 for Java  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Tutorials

- [Java Image Processing Tutorial - Adjust Brightness of an Image with Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [How to Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Convert PSD to Image in Java – Apply Adjustment Layers with Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```