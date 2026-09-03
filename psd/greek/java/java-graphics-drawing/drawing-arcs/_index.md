---
date: 2026-09-03
description: Μάθετε πώς να java graphics σχεδιάζετε τόξο χρησιμοποιώντας το Aspose.PSD
  για Java. Οδηγός βήμα προς βήμα με αποσπάσματα κώδικα για τη δημιουργία τόξων σε
  αρχεία PSD.
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Σχεδίαση Τόξων σε Java
og_description: Μάθετε πώς να java graphics σχεδιάζετε τόξο με το Aspose.PSD για Java.
  Αυτό το σεμινάριο παρουσιάζει προαπαιτούμενα, βήματα κώδικα και συμβουλές για τη
  δημιουργία τόξων σε αρχεία PSD.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: Πώς να java graphics σχεδιάσετε τόξο σε Java – Οδηγός Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: Πώς να java graphics σχεδιάσετε τόξο σε Java
url: /el/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να σχεδιάσετε τόξο με Java graphics σε Java

## Εισαγωγή
Σε αυτό το tutorial θα ανακαλύψετε πώς να **java graphics draw arc** χρησιμοποιώντας τη βιβλιοθήκη Aspose.PSD for Java. Η προγραμματιστική σχεδίαση τόξων είναι μια κοινή απαίτηση για προσαρμοσμένα UI components, data visualisations και αναφορές πλούσιες σε γραφικά. Η Aspose.PSD for Java σας δίνει πλήρη έλεγχο πάνω στα αρχεία PSD (Photoshop Document), επιτρέποντάς σας να δημιουργείτε, να επεξεργάζεστε και να εξάγετε εικόνες χωρίς να είναι εγκατεστημένο το Photoshop.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη υποστηρίζει τη σχεδίαση τόξου σε Java;** Aspose.PSD for Java.
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Yes, a commercial license is required for non‑trial deployments.
- **Σε ποιες μορφές αρχείων μπορώ να εξάγω;** BMP, PNG, JPEG, TIFF, GIF and more.
- **Μπορώ να αλλάξω το πάχος και το χρώμα του τόξου;** Yes, via the `Pen` object passed to `drawArc`.
- **Είναι το API συμβατό με Java 8 και νεότερες εκδόσεις;** Fully compatible with Java 8‑21.

## Τι είναι το Java graphics draw arc;
`java graphics draw arc` αναφέρεται στη διαδικασία απόδοσης ενός καμπυλωτού τμήματος γραμμής—ένα τόξο—σε μια επιφάνεια γραφικών χρησιμοποιώντας τα drawing APIs της Java. Στο πλαίσιο της Aspose.PSD, η λειτουργία εκτελείται σε ένα αντικείμενο `Graphics` που αντιπροσωπεύει ένα layer μέσα σε ένα αρχείο PSD.

## Γιατί να χρησιμοποιήσετε την Aspose.PSD for Java για τη σχεδίαση τόξων;
Η Aspose.PSD υποστηρίζει **50+** μορφές εικόνας και εγγράφων, μπορεί να διαχειριστεί αρχεία PSD με **μέγεθος έως 2 GB**, και επεξεργάζεται έγγραφα με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη. Αυτή η ποσοτικοποιημένη απόδοση την καθιστά ιδανική για δημιουργία γραφικών στο διακομιστή όπου η ταχύτητα και η χρήση μνήμης έχουν σημασία.

## Προαπαιτούμενα
1. **Java Development Environment** – Εγκαταστήστε τη Java από το [ιστότοπο της Oracle](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java Library** – Κατεβάστε το πιο πρόσφατο JAR από τη [σελίδα λήψης](https://releases.aspose.com/psd/java/). Ακολουθήστε τις παρεχόμενες οδηγίες για να προσθέσετε το JAR στο classpath του έργου σας.

## Πώς να Java graphics draw arc σε Java;
Φορτώστε ένα νέο `PsdImage`, αποκτήστε την επιφάνεια `Graphics` του, διαμορφώστε ένα `Pen` με το επιθυμητό χρώμα και πάχος, και καλέστε το `drawArc`. Αυτή η σύντομη ακολουθία δημιουργεί το τόξο και αποθηκεύει το αποτέλεσμα σε μια ενιαία αλυσίδα μεθόδων. Με την προσαρμογή του περιοριστικού ορθογωνίου και των παραμέτρων γωνίας μπορείτε να ελέγξετε το μέγεθος, τη θέση και το εύρος του τόξου ώστε να ταιριάζει στις απαιτήσεις του σχεδίου σας.

### Βήμα 1: ρυθμίστε το έργο Java σας
Δημιουργήστε ένα νέο έργο Java στο αγαπημένο σας IDE και προσθέστε το JAR της Aspose.PSD στο build path. Βεβαιωθείτε ότι το JAR αναφέρεται σωστά ώστε ο μεταγλωττιστής να μπορεί να εντοπίσει τις κλάσεις της βιβλιοθήκης.

### Βήμα 2: εισάγετε τα απαιτούμενα πακέτα
Για να ξεκινήσετε, εισάγετε τα απαραίτητα πακέτα από την Aspose.PSD for Java:
Η κλάση `Pen` ορίζει το χρώμα, το πλάτος και το στυλ της γραμμής που χρησιμοποιείται για τη σχεδίαση του τόξου.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
Αυτές οι εισαγωγές εκθέτουν τις κλάσεις `PsdImage`, `Graphics`, `Pen` και χρώματος που χρειάζονται για τη σχεδίαση τόξου.

### Βήμα 3: αρχικοποιήστε τα αντικείμενα εικόνας και γραφικών
Δημιουργήστε μια παρουσία του `PsdImage` και αποκτήστε ένα αντικείμενο `Graphics` για να σχεδιάσετε πάνω του:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
Αντικαταστήστε το `"Your Document Directory"` με το φάκελο όπου θέλετε να αποθηκευτούν τα αρχεία εξόδου.

### Βήμα 4: ορίστε τις παραμέτρους του τόξου
Ορίστε τη γεωμετρία και το στυλ του τόξου—το περιοριστικό ορθογώνιο, τη γωνία έναρξης, τη γωνία σάρωσης, το χρώμα και το πάχος:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
Ρυθμίστε τις τιμές ώστε να ταιριάζουν με το οπτικό σχέδιο που χρειάζεστε· για παράδειγμα, ένα τόξο με ακτίνα 200 px που ξεκινά στις 45° και σαρώνει 270°.

### Βήμα 5: σχεδιάστε το τόξο και αποθηκεύστε την εικόνα
Κλήστε το `drawArc` στο αντικείμενο `Graphics` και αποθηκεύστε το PSD (ή εξάγετε σε άλλη μορφή):
Η μέθοδος `drawArc` της κλάσης `Graphics` αποδίδει ένα τόξο που ορίζεται από ένα περιοριστικό ορθογώνιο, γωνία έναρξης και γωνία σάρωσης χρησιμοποιώντας το καθορισμένο `Pen`.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
Το απόσπασμα σχεδιάζει το τόξο στον καμβά και το αποθηκεύει ως αρχείο BMP. Αλλάξτε την επέκταση αρχείου στο `outputPath` για να εξάγετε σε PNG, JPEG ή TIFF.

## Συνηθισμένα προβλήματα και αντιμετώπιση
- **Incorrect angle units** – Η Aspose.PSD αναμένει γωνίες σε μοίρες, όχι σε ακτίνια. Η παροχή ακτινίων θα παράγει ανεπιθύμητα αποτελέσματα.
- **Pen thickness too large** – Πολύ παχιές πένες μπορεί να κάνουν το τόξο να υπερβεί τα όρια της εικόνας· μειώστε το πάχος ή μεγαλώστε τον καμβά.
- **File path issues** – Χρησιμοποιήστε απόλυτες διαδρομές ή βεβαιωθείτε ότι ο τρέχων φάκελος έχει δικαιώματα εγγραφής για να αποφύγετε το `IOException`.

## Συχνές ερωτήσεις

**Q: Μπορεί η Aspose.PSD for Java να χειριστεί άλλα σχήματα εκτός από τόξα;**  
A: Ναι, η βιβλιοθήκη μπορεί να σχεδιάσει ορθογώνια, έλλειπτες, γραμμές, πολύγωνα και προσαρμοσμένα μονοπάτια χρησιμοποιώντας το ίδιο `Graphics` API.

**Q: Πώς μπορώ να αλλάξω το χρώμα και το πάχος του τόξου;**  
A: Δημιουργήστε ένα `Pen` με το επιθυμητό `Color` και πλάτος, και στη συνέχεια περάστε αυτήν την παρουσία του `Pen` στο `drawArc`.

**Q: Είναι δυνατόν να εξάγετε το PSD σε μορφή διαφορετική από BMP;**  
A: Απόλυτα. Η Aspose.PSD υποστηρίζει PNG, JPEG, TIFF, GIF και πολλά άλλα – απλώς αλλάξτε την επέκταση αρχείου στη μέθοδο `save`.

**Q: Πού μπορώ να βρω περισσότερα παραδείγματα και υποστήριξη της κοινότητας;**  
A: Επισκεφθείτε το [φόρουμ Aspose.PSD](https://forum.aspose.com/c/psd/34) για tutorials, code samples, και βοήθεια από άλλους προγραμματιστές.

**Q: Η βιβλιοθήκη λειτουργεί με μεγάλα αρχεία PSD;**  
A: Ναι, μπορεί να επεξεργαστεί αρχεία έως 2 GB και να αποδώσει τόξα χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, χάρη στην αρχιτεκτονική ροής της.

---

**Τελευταία ενημέρωση:** 2026-09-03  
**Δοκιμή με:** Aspose.PSD for Java 24.11  
**Συγγραφέας:** Aspose

## Σχετικές οδηγίες

- [Σχεδίαση και αποθήκευση ορθογωνίου σε PSD χρησιμοποιώντας Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Αλλαγή μεγέθους εικόνας με Aspose.PSD for Java – Σχεδίαση σχημάτων & βασικές λειτουργίες εικόνας](/psd/java/basic-image-operations/)
- [Πώς να αλλάξετε το χρώμα γραμμής Java χρησιμοποιώντας Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}