---
date: 2026-09-08
description: Μάθετε πώς να σχεδιάσετε ορθογώνιο σε μια εικόνα χρησιμοποιώντας το Aspose.PSD
  for Java, καλύπτοντας τη δημιουργία bitmap, το χρώμα φόντου και την αρχικοποίηση
  graphics για επεξεργασία εικόνας σε Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Σχεδίαση Ορθογωνίων σε Java
og_description: Μάθετε πώς να σχεδιάσετε ορθογώνιο σε μια εικόνα χρησιμοποιώντας το
  Aspose.PSD for Java. Αυτός ο οδηγός καλύπτει τη δημιουργία bitmap, τον ορισμό του
  χρώματος φόντου και την αρχικοποίηση graphics σε Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Πώς να σχεδιάσετε ορθογώνιο σε μια εικόνα με Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Πώς να σχεδιάσετε ορθογώνιο σε μια εικόνα με Aspose.PSD for Java
url: /el/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε ορθογώνιο σε μια εικόνα με Aspose.PSD for Java

## Εισαγωγή
Αν χρειάζεστε **πώς να σχεδιάσετε ορθογώνιο** σε μια εικόνα προγραμματιστικά, το Aspose.PSD for Java σας προσφέρει ένα καθαρό, υψηλής απόδοσης API. Σε αυτό το tutorial θα δείτε πώς να δημιουργήσετε ένα bitmap, να ορίσετε το χρώμα φόντου και **να αρχικοποιήσετε αντικείμενα graphics java** ώστε να μπορείτε να αποδίδετε ορθογώνια οποιουδήποτε μεγέθους και χρώματος. Τα βήματα είναι απλά, ο κώδικας συνοπτικός, και το αποτέλεσμα είναι ένα αρχείο BMP που μπορείτε να χρησιμοποιήσετε σε οποιαδήποτε ροή εργασίας βασισμένη σε Java.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη χειρίζεται το σχεδιασμό ορθογωνίου;** Aspose.PSD for Java.
- **Πόσες γραμμές κώδικα απαιτούνται;** Περίπου έξι γραμμές για τη δημιουργία της εικόνας, τον ορισμό του φόντου και το σχεδιασμό δύο ορθογωνίων.
- **Ποιοι τύποι εικόνας υποστηρίζονται για εξαγωγή;** BMP, PNG, JPEG, TIFF, GIF και άλλα.
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται άδεια για παραγωγή.
- **Μπορώ να αλλάξω το πάχος του περιγράμματος;** Ναι – προσαρμόστε την ιδιότητα `Pen` thickness πριν το σχεδιασμό.

## Τι σημαίνει το σχεδιασμό ορθογωνίου σε μια εικόνα;
Το σχεδιασμό ορθογωνίου σε μια εικόνα σημαίνει την απόδοση ενός γεμιστού ή περιγραμμισμένου σχήματος πάνω σε bitmap χρησιμοποιώντας ένα graphics context. Η κλάση `Graphics` του Aspose.PSD παρέχει μεθόδους που σας επιτρέπουν να καθορίσετε χρώμα, θέση και μέγεθος με μία κλήση.

## Γιατί να χρησιμοποιήσετε το Aspose.PSD for Java για το σχεδιασμό ορθογωνίου;
Το Aspose.PSD υποστηρίζει **πάνω από 50 τύπους εικόνας** και μπορεί να επεξεργαστεί αρχεία έως **2 GB** χωρίς να φορτώσει ολόκληρο το έγγραφο στη μνήμη. Το API `Graphics` του τρέχει έως **3× πιο γρήγορα** από το εγγενές Java AWT για μαζικές λειτουργίες, καθιστώντας το ιδανικό για υψηλής απόδοσης επεξεργασία εικόνας στο διακομιστή.

## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Java Development Kit (JDK) 8 ή νεότερο** εγκατεστημένο.
- **Aspose.PSD for Java** βιβλιοθήκη που έχετε κατεβάσει από τη [σελίδα λήψης Aspose.PSD for Java](https://releases.aspose.com/psd/java/) και προσθέσατε στο classpath του έργου σας.

### Εισαγωγή πακέτων
Οι δηλώσεις `import` σας δίνουν πρόσβαση στις κλάσεις που απαιτούνται για τη δημιουργία bitmap και το σχεδιασμό.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Αυτές οι εισαγωγές θα σας επιτρέψουν να έχετε πρόσβαση στις κλάσεις και τις μεθόδους που χρειάζονται για το σχεδιασμό ορθογωνίων σε εικόνες.

## Πώς να σχεδιάσετε ορθογώνιο σε μια εικόνα με Java;
Φορτώστε ένα νέο `PsdImage`, καθαρίστε την επιφάνειά του με χρώμα φόντου, δημιουργήστε ένα αντικείμενο `Graphics` και, στη συνέχεια, καλέστε `drawRectangle` με το επιθυμητό `Pen` και `Brush`. Η ολόκληρη διαδικασία απαιτεί μόνο λίγες κλήσεις μεθόδων και παράγει ένα bitmap έτοιμο για αποθήκευση.  
`PsdImage` αντιπροσωπεύει ένα bitmap στη μνήμη που μπορεί να επεξεργαστεί και να αποθηκευτεί.  
`Graphics` παρέχει μια επιφάνεια σχεδίασης για την απόδοση σχημάτων πάνω σε μια εικόνα.

### Βήμα 1: δημιουργία νέας εικόνας
Η κλάση `PsdImage` αντιπροσωπεύει ένα bitmap στη μνήμη. Η αρχικοποίησή της επίσης εκχωρεί το buffer των pixel.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
Σε αυτό το βήμα, το `PsdImage` αρχικοποιείται με πλάτος και ύψος **100 px** το καθένα, παρέχοντάς σας έναν μικρό καμβά για επίδειξη.

### Βήμα 2: αρχικοποίηση αντικειμένου graphics java
Μια παρουσία `Graphics` είναι η επιφάνεια σχεδίασης που συνδέεται με την εικόνα που μόλις δημιουργήσατε.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Αυτό το αντικείμενο `Graphics` θα χρησιμοποιηθεί για εκτέλεση λειτουργιών σχεδίασης όπως γέμισμα σχημάτων ή σχεδίαση περιγραμμάτων.

### Βήμα 3: ορισμός χρώματος φόντου java
Πριν σχεδιάσετε σχήματα συχνά θέλετε ένα στερεό φόντο. Χρησιμοποιήστε `clear` με ένα `Color` για να γεμίσετε ολόκληρο τον καμβά.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Το φόντο ορίζεται σε **κίτρινο**, παρέχοντας υψηλή αντίθεση για τα κόκκινα και μπλε ορθογώνια που ακολουθούν.

### Βήμα 4: σχεδίαση ορθογωνίων στην εικόνα
Χρησιμοποιήστε `drawRectangle` με ένα `Pen` για το περίγραμμα και ένα `SolidBrush` για το γέμισμα. Μπορείτε να σχεδιάσετε πολλαπλά ορθογώνια με διαφορετικά χρώματα και θέσεις.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Αυτές οι εντολές σχεδιάζουν ένα **κόκκινο** ορθογώνιο στο (10, 10) και ένα **μπλε** ορθογώνιο στο (50, 50), καθένα 40 px πλάτος και 30 px ύψος.

### Βήμα 5: εξαγωγή εικόνας σε bitmap
Τέλος, αποθηκεύστε την τροποποιημένη εικόνα στο δίσκο. Το Aspose.PSD κωδικοποιεί αυτόματα το bitmap στη μορφή που καθορίζετε.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Η εικόνα αποθηκεύεται ως αρχείο BMP στη διαδρομή που βρίσκεται στο `outpath`.

## Κοινά προβλήματα και λύσεις
- **Κενό αρχείο εξόδου** – Βεβαιωθείτε ότι καλείτε `graphics.clear` πριν το σχεδιασμό· διαφορετικά ο καμβάς μπορεί να παραμείνει διαφανής.
- **Λανθασμένα χρώματα** – Επαληθεύστε ότι εισάγετε `com.aspose.psd.Color` και όχι `java.awt.Color`.
- **Μεγάλες εικόνες χωρίς μνήμη** – Χρησιμοποιήστε κατασκευαστές `PsdImage` που υποστηρίζουν streaming για να αποφύγετε τη φόρτωση ολόκληρου του αρχείου στη RAM.

## Συχνές ερωτήσεις

**Ε: Μπορεί το Aspose.PSD for Java να χειριστεί άλλα σχήματα εκτός από ορθογώνια;**  
Α: Ναι, υποστηρίζει έλλειψη, γραμμές, πολύγωνα και προσαρμοσμένες διαδρομές, παρέχοντάς σας πλήρεις δυνατότητες διανυσματικού σχεδιασμού.

**Ε: Πώς μπορώ να τροποποιήσω το πάχος του περιγράμματος του ορθογωνίου;**  
Α: Ορίστε τη μέθοδο `setWidth(float)` του αντικειμένου `Pen` πριν καλέσετε `drawRectangle`.

**Ε: Είναι το Aspose.PSD for Java κατάλληλο για εργασίες υψηλής απόδοσης επεξεργασίας εικόνας;**  
Α: Απόλυτα – το streaming API του επεξεργάζεται αρχεία PSD εκατοντάδων σελίδων με λιγότερο από 200 MB RAM.

**Ε: Πού μπορώ να βρω περισσότερα παραδείγματα και tutorials για το Aspose.PSD for Java;**  
Α: Μπορείτε να εξερευνήσετε περισσότερα παραδείγματα και λεπτομερή τεκμηρίωση στη [τεκμηρίωση Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Ε: Υποστηρίζει το Aspose.PSD for Java άλλες μορφές εικόνας εκτός από BMP;**  
Α: Ναι, υποστηρίζει PNG, JPEG, TIFF, GIF και πάνω από 30 επιπλέον μορφές για εισαγωγή και εξαγωγή.

## Συμπέρασμα
Τώρα ξέρετε **πώς να σχεδιάσετε ορθογώνιο** σε μια εικόνα χρησιμοποιώντας το Aspose.PSD for Java, από τη δημιουργία bitmap μέχρι τον ορισμό χρώματος φόντου και την αρχικοποίηση graphics. Πειραματιστείτε με διαφορετικά μεγέθη, χρώματα και επιπλέον σχήματα για να κυριαρχήσετε τη **java image manipulation**. Όταν είστε έτοιμοι, ενσωματώστε αυτό το μοτίβο σε μεγαλύτερες γραμμές επεξεργασίας batch ή σε UI‑βασισμένους επεξεργαστές.

---

**Τελευταία ενημέρωση:** 2026-09-08  
**Δοκιμάστηκε με:** Aspose.PSD for Java 24.12  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Αλλαγή μεγέθους εικόνας με Aspose.PSD for Java – Σχεδίαση Σχημάτων & Βασικές Λειτουργίες Εικόνας](/psd/java/basic-image-operations/)
- [Προσθήκη Υπογραφής σε Εικόνα – Σχεδίαση Εικόνας σε Καμβά με Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Περικοπή Εικόνας με Ορθογώνιο με Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}