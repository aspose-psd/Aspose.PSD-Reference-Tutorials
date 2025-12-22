---
date: 2025-12-21
description: Μάθετε πώς να εκτελείτε επεξεργασία εικόνας σε Java προσαρμόζοντας τη
  γάμμα της εικόνας με το Aspose.PSD. Οδηγός βήμα‑προς‑βήμα για τη μετατροπή PSD σε
  TIFF και την εφαρμογή διόρθωσης γάμμα.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Επεξεργασία Εικόνας Java – Ρύθμιση Gamma με το Aspose.PSD
url: /el/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Processing – Adjust Gamma with Aspose.PSD

## Introduction

Αν εργάζεστε με **java image processing**, η ρύθμιση του gamma μιας εικόνας είναι μια βασική τεχνική για τη βελτίωση της φωτεινότητας και της αντίθεσης χωρίς να χάνονται λεπτομέρειες. Σε αυτό το tutorial θα δούμε πώς να χρησιμοποιήσετε το **Aspose.PSD for Java** για να εφαρμόσετε διόρθωση gamma σε ένα αρχείο PSD και στη συνέχεια να εξάγετε το αποτέλεσμα ως εικόνα TIFF. Θα καταλάβετε γιατί αυτή η προσέγγιση είναι γρήγορη, αξιόπιστη και ιδανική για pipelines επεξεργασίας εικόνας στο διακομιστή.

## Quick Answers
- **What does gamma correction do?** It remaps luminance values to make dark areas brighter or bright areas darker while preserving overall detail.  
- **Which library handles the processing?** Aspose.PSD for Java provides a dedicated `adjustGamma` method for raster images.  
- **Can I convert PSD to TIFF in the same flow?** Yes – after gamma adjustment you can save the image directly to TIFF using `TiffOptions`.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production use.  
- **What Java version is supported?** Aspose.PSD supports Java 8 and later.

## What is java image processing?

Η Java image processing αναφέρεται στη διαχείριση, ανάλυση και μετασχηματισμό οπτικών δεδομένων χρησιμοποιώντας βιβλιοθήκες Java. Οι εργασίες περιλαμβάνουν αλλαγή μεγέθους, φιλτράρισμα, διόρθωση χρωμάτων και μετατροπή μορφών — όλα μπορούν να αυτοματοποιηθούν σε εφαρμογές desktop ή web.

## Why use Aspose.PSD for gamma correction?

Το Aspose.PSD προσφέρει ένα υψηλού επιπέδου API που αφαιρεί την πολυπλοκότητα της μορφής PSD, επιτρέποντάς σας να εστιάσετε στις πραγματικές ρυθμίσεις εικόνας. Διαχειρίζεται caching, προφίλ χρωμάτων και παρέχει μια απλή κλήση `adjustGamma`, καθιστώντας το ιδανικό για **image gamma correction** και **convert psd to tiff** workflows.

## Prerequisites

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε ρυθμίσει τα παρακάτω:

1. **Java Development Environment** – Βεβαιωθείτε ότι έχετε εγκατεστημένο ένα περιβάλλον ανάπτυξης Java στο σύστημά σας.  
2. **Aspose.PSD Library** – Κατεβάστε και ενσωματώστε τη βιβλιοθήκη Aspose.PSD στο Java project σας. Μπορείτε να βρείτε τους απαραίτητους πόρους στην [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Προετοιμάστε ένα δείγμα εικόνας PSD που θα χρησιμοποιήσετε για την εφαρμογή της ρύθμισης gamma.

## Import Packages

Για να ξεκινήσετε τη διαδικασία, εισάγετε τα απαιτούμενα πακέτα στο Java project σας. Αυτό θέτει το σκηνικό για την απρόσκοπτη χρήση των λειτουργιών του Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

Ξεκινήστε φορτώνοντας το δείγμα εικόνας PSD σε μια παρουσία της κλάσης `RasterImage`. Αυτό αποτελεί τη βάση για τις επόμενες ρυθμίσεις gamma.

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

## Step 2: Adjust Gamma

Τώρα, ρυθμίστε το gamma της φορτωμένης εικόνας χρησιμοποιώντας τη μέθοδο `adjustGamma`. Ρυθμίστε τις τιμές gamma σύμφωνα με τις απαιτήσεις σας.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Step 3: Create TiffOptions

Δημιουργήστε μια παρουσία του `TiffOptions` για την τελική εικόνα. Ορίστε διάφορες ιδιότητες, όπως bits per sample και photometric options, ώστε το αποτέλεσμα να ταιριάζει στις προδιαγραφές σας.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Step 4: Save the Resultant Image

Αποθηκεύστε την επεξεργασμένη εικόνα σε μορφή TIFF χρησιμοποιώντας το `TiffOptions` που ορίσατε προηγουμένως.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Image appears washed out** | Gamma value too high (e.g., > 2.5) | Lower the gamma factor to a value between 1.8 and 2.2. |
| **`rasterImage.isCached()` returns false** | Image not yet loaded into memory | Call `rasterImage.cacheData()` before adjusting gamma. |
| **TIFF file size is large** | Bits per sample set to 16‑bit | Use an 8‑bit sample (`{8,8,8}`) as shown in the example. |

## Frequently Asked Questions

**Q: Can I apply different gamma values to each colour channel?**  
A: Yes – the `adjustGamma` method accepts separate float values for red, green, and blue channels.

**Q: Is it possible to chain multiple image adjustments before saving?**  
A: Absolutely. You can perform resizing, cropping, or colour corrections sequentially on the same `RasterImage` instance.

**Q: Does Aspose.PSD support multi‑page PSD files?**  
A: Yes, each layer can be accessed and processed individually.

**Q: What format can I export to besides TIFF?**  
A: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective options classes.

## Conclusion

Συγχαρητήρια! Εκτελέσατε επιτυχώς **java image processing** ρυθμίζοντας το gamma ενός αρχείου PSD και εξάγοντας το ως εικόνα TIFF χρησιμοποιώντας το Aspose.PSD for Java. Αυτή η ροή εργασίας σας δίνει ακριβή έλεγχο της φωτεινότητας και της αντίθεσης της εικόνας, καθιστώντας την ιδανική για αυτοματοποιημένα γραφικά pipelines, web services ή desktop utilities.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
