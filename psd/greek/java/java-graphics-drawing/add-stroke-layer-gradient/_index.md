---
title: Πώς να προσθέσετε κλίση επιπέδου Stroke στην Java
linktitle: Πώς να προσθέσετε κλίση επιπέδου Stroke στην Java
second_title: Aspose.PSD Java API
description: Μάθετε πώς να προσθέτετε και να προσαρμόζετε διαβαθμίσεις στρώσης περιγράμματος σε αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java με αυτόν τον αναλυτικό, βήμα προς βήμα εκμάθηση.
weight: 10
url: /el/java/java-graphics-drawing/add-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να προσθέσετε κλίση επιπέδου Stroke στην Java

## Εισαγωγή
Αναρωτηθήκατε ποτέ πώς να προσθέσετε μια κλίση στρώσης περιγράμματος στις εικόνες σας χρησιμοποιώντας Java; Λοιπόν, είστε στο σωστό μέρος! Σήμερα, βουτάμε στον κόσμο του Aspose.PSD για Java, μιας ισχυρής βιβλιοθήκης που σας βοηθά να χειρίζεστε αρχεία PSD με ευκολία. Είτε είστε αρχάριος είτε έμπειρος προγραμματιστής, αυτός ο οδηγός βήμα προς βήμα θα σας καθοδηγήσει στη διαδικασία προσθήκης μιας διαβάθμισης επιπέδου stroke στα αρχεία PSD σας. Λάβετε, λοιπόν, και ετοιμαστείτε να βελτιώσετε τις δεξιότητές σας στην επεξεργασία γραφικών!
## Προαπαιτούμενα
Πριν ξεκινήσουμε, υπάρχουν μερικά πράγματα που πρέπει να έχετε στη θέση του. Βεβαιωθείτε ότι έχετε τα εξής:
1.  Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκαταστήσει το JDK στο σύστημά σας. Μπορείτε να το κατεβάσετε από[Ο ιστότοπος της Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD για Java Library: Μπορείτε να το κατεβάσετε από το[Σελίδα λήψης Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Ένα ολοκληρωμένο περιβάλλον ανάπτυξης (IDE): Οποιοδήποτε IDE όπως το IntelliJ IDEA, το Eclipse ή το NetBeans θα λειτουργήσει.
4.  Μια έγκυρη άδεια: Μπορείτε να αποκτήσετε ένα[προσωρινή άδεια](https://purchase.aspose.com/temporary-license/) αν δεν έχετε πλήρη.
## Εισαγωγή πακέτων
Πρώτα πρώτα, ας εισάγουμε τα απαραίτητα πακέτα. Αυτά θα μας επιτρέψουν να χρησιμοποιήσουμε τις κλάσεις και τις μεθόδους που απαιτούνται για τον χειρισμό του αρχείου PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
Τώρα, ας αναλύσουμε το παράδειγμα σε πολλά βήματα για καλύτερη κατανόηση.
## Βήμα 1: Φορτώστε το αρχείο PSD
 Αρχικά, πρέπει να φορτώσουμε το αρχείο PSD που θέλουμε να τροποποιήσουμε. Θα χρησιμοποιήσουμε το`PsdLoadOptions` για να καθορίσουμε ότι θέλουμε να φορτώσουμε τους πόρους εφέ.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Βήμα 2: Πρόσβαση στο Stroke Effect
Στη συνέχεια, πρέπει να αποκτήσουμε πρόσβαση στο εφέ stroke του επιπέδου που μας ενδιαφέρει. Εδώ, υποθέτουμε ότι είναι το τρίτο στρώμα (ευρετήριο 2) στο αρχείο PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Βήμα 3: Επαληθεύστε τις ιδιότητες εφέ Stroke
Πριν κάνετε οποιεσδήποτε αλλαγές, ας επαληθεύσουμε τις ιδιότητες του εφέ κτύπημα για να βεβαιωθούμε ότι τροποποιούμε τις σωστές ρυθμίσεις.
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
## Βήμα 4: Τροποποιήστε τις ρυθμίσεις πλήρωσης κλίσης
Τώρα, ήρθε η ώρα να τροποποιήσουμε τις ρυθμίσεις πλήρωσης κλίσης σύμφωνα με τις απαιτήσεις μας. Θα αλλάξουμε το χρώμα, την αδιαφάνεια, τη λειτουργία ανάμειξης και άλλες ιδιότητες.
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
## Βήμα 5: Προσθήκη και τροποποίηση σημείων χρώματος και διαφάνειας
Ας προσθέσουμε νέα σημεία χρώματος και διαφάνειας και ας τροποποιήσουμε τα υπάρχοντα για να επιτύχουμε το επιθυμητό εφέ διαβάθμισης.
```java
// Προσθέστε νέο σημείο χρώματος
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Αλλαγή θέσης προηγούμενου σημείου
fillSettings.getColorPoints()[1].setLocation(1899);
// Προσθήκη νέου σημείου διαφάνειας
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Αλλαγή θέσης προηγούμενου σημείου διαφάνειας
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Βήμα 6: Αποθηκεύστε το τροποποιημένο αρχείο PSD
Αφού κάνουμε όλες τις απαραίτητες τροποποιήσεις, πρέπει να αποθηκεύσουμε το αρχείο PSD.
```java
im.save(exportPath);
```
## Βήμα 7: Επαληθεύστε τις Τροποποιήσεις
Τέλος, ας φορτώσουμε το αποθηκευμένο αρχείο PSD και ας επαληθεύσουμε ότι οι αλλαγές μας έχουν εφαρμοστεί σωστά.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Ελέγξτε τα σημεία χρώματος
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Ελέγξτε τα σημεία διαφάνειας
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## Σύναψη
Και ορίστε το! Τώρα ξέρετε πώς να προσθέτετε και να χειρίζεστε τις διαβαθμίσεις του επιπέδου stroke σε αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Αυτό το σεμινάριο κάλυψε τη φόρτωση του αρχείου PSD, την πρόσβαση και την τροποποίηση των stroke εφέ και την αποθήκευση των αλλαγών. Με αυτές τις δεξιότητες, μπορείτε να δημιουργήσετε οπτικά ελκυστικές διαβαθμίσεις και να προσαρμόσετε τα αρχεία PSD για να ταιριάζουν στις ανάγκες σας.
## Συχνές ερωτήσεις
### Τι είναι το Aspose.PSD για Java;
Το Aspose.PSD για Java είναι μια βιβλιοθήκη που επιτρέπει στους προγραμματιστές να εργάζονται με αρχεία PSD σε εφαρμογές Java, παρέχοντας δυνατότητες δημιουργίας, χειρισμού και μετατροπής αρχείων PSD.
### Χρειάζομαι άδεια χρήσης για να χρησιμοποιήσω το Aspose.PSD για Java;
 Ναι, χρειάζεστε έγκυρη άδεια χρήσης για να χρησιμοποιήσετε το Aspose.PSD για Java. Μπορείτε να πάρετε ένα[προσωρινή άδεια](https://purchase.aspose.com/temporary-license/) για σκοπούς αξιολόγησης.
### Μπορώ να χρησιμοποιήσω το Aspose.PSD για Java για να δημιουργήσω αρχεία PSD από την αρχή;
Απολύτως! Το Aspose.PSD για Java παρέχει ολοκληρωμένα API για τη δημιουργία και τον χειρισμό αρχείων PSD μέσω προγραμματισμού.
### Είναι δυνατή η εφαρμογή άλλων εφέ χρησιμοποιώντας το Aspose.PSD για Java;
Ναι, μπορείτε να εφαρμόσετε διάφορα εφέ όπως σκιά, λάμψη και άλλα χρησιμοποιώντας το Aspose.PSD για Java.
### Πού μπορώ να βρω την τεκμηρίωση για το Aspose.PSD για Java;
 Μπορείτε να βρείτε την τεκμηρίωση[εδώ](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
