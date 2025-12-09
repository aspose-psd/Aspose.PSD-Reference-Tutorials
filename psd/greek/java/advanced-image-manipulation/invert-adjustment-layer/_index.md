---
date: 2025-12-02
description: Μάθετε πώς να χρησιμοποιείτε τη βιβλιοθήκη επεξεργασίας εικόνας Java
  Aspose.PSD για να εφαρμόζετε πολλαπλά στρώματα προσαρμογής, συμπεριλαμβανομένου
  του στρώματος προσαρμογής Αντιστροφής, για αδιάλειπτη διαχείριση αρχείων PSD.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Βιβλιοθήκη Java Επεξεργασίας Εικόνας: Αντιστροφή Στρώματος με Aspose.PSD'
url: /el/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Invert Adjustment Layer in Aspose.PSD for Java

## Introduction

Αν ψάχνετε για μια ισχυρή **image processing java library**, η Aspose.PSD for Java είναι μία από τις πιο ευέλικτες επιλογές στην αγορά. Σε αυτό το tutorial θα δούμε πώς να προσθέσουμε ένα **Invert Adjustment Layer** σε αρχείο PSD, μια τεχνική που μπορείτε να συνδυάσετε με άλλα adjustment layers για να πετύχετε σύνθετα οπτικά εφέ. Είτε δημιουργείτε ένα εργαλείο batch‑processing είτε έναν επεξεργαστή μίας εικόνας, αυτός ο οδηγός σας παρέχει μια σαφή, βήμα‑βήμα διαδρομή για να ολοκληρώσετε τη δουλειά γρήγορα.

## Quick Answers
- **What does the Invert Adjustment Layer do?** It reverses all color values in the selected area, creating a negative‑image effect.  
- **Which library provides this feature?** Aspose.PSD, a leading image processing java library.  
- **Can I stack it with other adjustments?** Yes – you can **apply multiple adjustment layers** such as Brightness/Contrast, Hue/Saturation, and more.  
- **Do I need a license for development?** A free trial is available; a license is required for production use.  
- **How long does the implementation take?** Typically under 10 minutes for a basic use‑case.

## What is the Invert Adjustment Layer?

Το Invert Adjustment Layer είναι μια μη καταστροφική επεξεργασία που αντιστρέφει τις τιμές RGB κάθε pixel που επηρεάζει. Επειδή βρίσκεται πάνω από τη στοίβα των layers, μπορείτε να εναλλάσσετε την ορατότητά του ή να το μετακινήσετε χωρίς να αλλάξετε μόνιμα τα αρχικά δεδομένα της εικόνας.

## Why Use Aspose.PSD as Your Image Processing Java Library?

- **Full PSD support** – read, edit, and write Photoshop files without Photoshop installed.  
- **Cross‑platform** – works on any Java runtime (Java 6+).  
- **Rich adjustment features** – includes built‑in methods for many common edits, making it easy to **apply multiple adjustment layers** in a single workflow.  
- **Performance‑optimized** – handles large files efficiently, which is essential for batch processing.

## Prerequisites

Before you start, make sure you have the following:

1. **Aspose.PSD Library** – download it from the official site [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 6.0 or later installed and configured.  

Now, let’s dive into the code.

## Import Packages

Begin by importing the necessary classes. These imports give you access to the core image‑handling APIs and the PSD‑specific functionality.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Step 1: Set Up Document Directory

Define the folder that contains your source PSD file and where the output will be saved.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load PSD File

Load the source file into a `PsdImage` object. This object represents the entire PSD document in memory.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Step 3: Add Invert Adjustment Layer

Call the built‑in method to insert an Invert Adjustment Layer on top of the current layer stack. You can later add more layers (e.g., Brightness, Hue) to **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Step 4: Save the Output

Persist the modified PSD to disk. The saved file now contains the Invert Adjustment Layer and can be opened in Photoshop or any PSD‑compatible viewer.

```java
im.save(outputPath);
```

### What just happened?

- The PSD was loaded into memory.  
- An Invert Adjustment Layer was added as the topmost layer.  
- The image was saved, preserving the non‑destructive edit.

You’ve now successfully used Aspose.PSD, an **image processing java library**, to manipulate a PSD file.

## Common Issues & Tips

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | Incorrect file path or missing file | Verify `dataDir` and file name; use absolute paths for testing |
| **Layer order not as expected** | Adding layers after existing ones changes stacking | Use `im.addInvertAdjustmentLayer()` before adding other adjustments, or reorder layers via `im.getLayers()` |
| **Performance slowdown on large PSDs** | Loading very large files into memory | Consider processing pages in chunks or increasing JVM heap size (`-Xmx2g`) |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with all Java versions?**  
A: Aspose.PSD supports Java 6.0 and later versions.

**Q: Can I apply multiple adjustment layers in a single operation?**  
A: Yes, you can stack several adjustment layers—such as Invert, Brightness, and Hue/Saturation—to achieve complex effects.

**Q: Where can I find additional documentation for Aspose.PSD?**  
A: Refer to the documentation [here](https://reference.aspose.com/psd/java/) for comprehensive guides and API references.

**Q: Is there a free trial available for Aspose.PSD?**  
A: Yes, you can explore the free trial [here](https://releases.aspose.com/).

**Q: How can I obtain a temporary license for Aspose.PSD?**  
A: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}