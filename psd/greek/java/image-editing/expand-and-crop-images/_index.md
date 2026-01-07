---
date: 2026-01-07
description: Μάθετε πώς να περικόψετε εικόνα Java χρησιμοποιώντας το Aspose.PSD για
  Java. Οδηγός βήμα‑βήμα για το περικόψιμο εικόνας, την αλλαγή μεγέθους και τη μετατροπή
  από PSD σε JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Περικοπή Εικόνας Java: Επέκταση και Περικοπή Εικόνων με το Aspose.PSD για
  Java'
url: /el/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Expand and Crop Images with Aspose.PSD for Java

## Introduction

Σε αυτό το tutorial θα ανακαλύψετε πώς να **crop image java** με τη βιβλιοθήκη Aspose.PSD. Είτε χρειάζεστε να επεκτείνετε έναν καμβά, να κόψετε ανεπιθύμητες άκρες, είτε να μετατρέψετε ένα αρχείο PSD σε JPEG, τα παρακάτω βήματα θα σας καθοδηγήσουν μέσα από μια καθαρή, επαναλήψιμη διαδικασία. Θα καλύψουμε τις προαπαιτούμενες συνθήκες, τις δηλώσεις εισαγωγής και κάθε βήμα κώδικα με σαφείς εξηγήσεις ώστε να μπορείτε να εφαρμόσετε την τεχνική σε πραγματικά έργα.

## Quick Answers
- **What library handles crop image java?** Aspose.PSD for Java.
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.
- **Can I convert PSD to JPEG while cropping?** Yes, using `JpegOptions` together with a cropping rectangle.
- **Is Java 8 supported?** Aspose.PSD supports Java 8 and newer versions.
- **How long does the implementation take?** Typically under 10 minutes for a basic crop operation.

## What is “crop image java”?

Το κόψιμο μιας εικόνας σε Java σημαίνει την επιλογή μιας ορθογώνιας περιοχής της πηγαίας εικόνας και την απόρριψη του υπόλοιπου. Με το Aspose.PSD μπορείτε να ορίσετε αυτήν την περιοχή χρησιμοποιώντας ένα αντικείμενο `Rectangle`, έπειτα να αποθηκεύσετε το αποτέλεσμα σε διαφορετική μορφή όπως JPEG.

## Why use Aspose.PSD for Java image cropping?

- **Full PSD support** – εργασία απευθείας με αρχεία PSD με στρώσεις χωρίς ανάγκη μετατροπής.  
- **High‑performance raster handling** – αποδοτική χρήση μνήμης για μεγάλες εικόνες.  
- **Built‑in conversion** – εύκολη εξαγωγή σε JPEG, PNG, BMP κ.λπ., ενώ εφαρμόζετε κόψιμο ή επέκταση καμβά.  
- **Cross‑platform** – λειτουργεί σε οποιοδήποτε σύστημα εκτελεί Java.

## Prerequisites

Πριν προχωρήσουμε, βεβαιωθείτε ότι έχετε:

1. **Java Development Kit (JDK)** – εγκατεστημένο Java 8 ή νεότερο.  
2. **Aspose.PSD for Java** – κατεβάστε τη βιβλιοθήκη από την επίσημη ιστοσελίδα **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Προσθέστε το JAR του Aspose.PSD στο classpath του έργου σας ή στις εξαρτήσεις Maven/Gradle για να αποφύγετε το `ClassNotFoundException`.

## Import Packages

Προσθέστε τις απαιτούμενες εισαγωγές στο αρχείο πηγαίου κώδικα Java. Αυτές οι κλάσεις σας δίνουν πρόσβαση στη φόρτωση εικόνας, τη διαχείριση raster, τον ορισμό ορθογωνίου και τις επιλογές εξαγωγής JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step 1: Set Your Document Directory

Καθορίστε το φάκελο που περιέχει το πηγαίο αρχείο PSD. Αντικαταστήστε το placeholder με την πραγματική διαδρομή στο σύστημά σας.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Specify Source and Destination Paths

Ορίστε πού θα διαβάσετε το PSD και πού θα γράψετε το κομμένο JPEG.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Step 3: Load and Cache the Image

Φορτώστε το PSD σε ένα αντικείμενο `RasterImage`. Η προσωρινή αποθήκευση (caching) βελτιώνει την απόδοση για επόμενες λειτουργίες όπως το κόψιμο.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Step 4: Create Rectangle for Cropping

Δημιουργήστε ένα `Rectangle` που περιγράφει την περιοχή που θέλετε να διατηρήσετε. Οι συντεταγμένες μπορούν να είναι αρνητικές για **επέκταση** του καμβά πριν το κόψιμο, κάτι χρήσιμο για προσθήκη περιθωρίου γύρω από την αρχική εικόνα.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Why use negative coordinates?**  
> Negative X/Y values shift the crop area left/up, effectively adding empty space (expanding) around the original content before the final crop.

> **Γιατί να χρησιμοποιήσετε αρνητικές συντεταγμένες;**  
> Οι αρνητικές τιμές X/Y μετατοπίζουν την περιοχή κοπής προς τα αριστερά/πάνω, προσθέτοντας ουσιαστικά κενό χώρο (επέκταση) γύρω από το αρχικό περιεχόμενο πριν το τελικό κόψιμο.

## Step 5: Save the Cropped Image

Τέλος, αποθηκεύστε την προκύπτουσα εικόνα χρησιμοποιώντας `JpegOptions`. Αυτό το βήμα επίσης δείχνει **convert psd jpeg** ενώ εφαρμόζεται το ορθογώνιο κοπής.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Result:** `jpeg_out.jpg` now contains a 300 × 300 pixel image that has been expanded by 200 px on each side and then cropped to the defined rectangle.

> **Αποτέλεσμα:** Το `jpeg_out.jpg` περιέχει τώρα μια εικόνα 300 × 300 pixel που έχει επεκταθεί κατά 200 px σε κάθε πλευρά και στη συνέχεια έχει κοπεί σύμφωνα με το ορισμένο ορθογώνιο.

Congratulations! You've successfully performed **java image cropping**, expanded the canvas, and converted a PSD file to JPEG—all in a few concise lines of code.

## Common Use Cases

- **Preparing assets for web** – κόψιμο και αλλαγή μεγέθους screenshots ή σχεδίων πριν τη μεταφόρτωση.  
- **Generating thumbnails** – εξαγωγή συγκεκριμένης περιοχής από μεγάλο PSD για προεπισκοπήσεις.  
- **Automated batch processing** – επανάληψη σε φάκελο PSD αρχείων, εφαρμόζοντας το ίδιο ορθογώνιο κοπής σε καθένα.

## Troubleshooting & Tips

| Issue | Suggested Fix |
|-------|----------------|
| `OutOfMemoryError` when loading large PSDs | Call `rasterImage.cacheData()` early and consider increasing the JVM heap size (`-Xmx`). |
| Cropped area is off‑center | Verify the rectangle’s X/Y offsets; remember negative values expand the canvas. |
| Output JPEG looks blurry | Adjust `JpegOptions` quality setting (e.g., `new JpegOptions { Quality = 90 }`). |

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with different Java versions?

A1: Yes, Aspose.PSD supports various Java versions, ensuring compatibility with a wide range of development environments.

### Q2: Can I use Aspose.PSD for commercial projects?

A2: Absolutely, Aspose.PSD provides commercial licenses for developers, allowing its use in both personal and commercial projects.

### Q3: Are there any limitations on the image file formats supported?

A3: Aspose.PSD supports a variety of image file formats, including PSD, JPEG, PNG, and more. Refer to the [documentation](https://reference.aspose.com/psd/java/) for a complete list.

### Q4: How can I get support for Aspose.PSD-related queries?

A4: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to seek assistance from the community or the Aspose support team.

### Q5: Is there a free trial available?

A5: Yes, you can explore Aspose.PSD with a free trial. Download it [here](https://releases.aspose.com/).

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}