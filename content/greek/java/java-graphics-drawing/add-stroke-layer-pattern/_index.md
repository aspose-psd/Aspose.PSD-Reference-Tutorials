---
title: Πώς να προσθέσετε μοτίβο επιπέδου Stroke στην Java
linktitle: Πώς να προσθέσετε μοτίβο επιπέδου Stroke στην Java
second_title: Aspose.PSD Java API
description: Μάθετε πώς μπορείτε να προσθέσετε ένα μοτίβο επιπέδου stroke σε αρχεία PSD χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθήστε αυτόν τον οδηγό βήμα προς βήμα για να βελτιώσετε εύκολα τις εικόνες σας.
type: docs
weight: 11
url: /el/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Εισαγωγή
Η προσθήκη ενός μοτίβου στρώματος περιγράμματος σε μια εικόνα σε Java μπορεί να ακούγεται σαν μια τρομακτική εργασία, αλλά με το Aspose.PSD για Java, είναι πιο εύκολο από ό,τι νομίζετε. Είτε σχεδιάζετε γραφικά είτε εργάζεστε σε εφαρμογές επεξεργασίας φωτογραφιών, αυτός ο οδηγός θα σας καθοδηγήσει βήμα προς βήμα στη διαδικασία. Είστε έτοιμοι να ξεκινήσετε; Ας βουτήξουμε!
## Προαπαιτούμενα
Πριν ξεκινήσετε, θα χρειαστείτε μερικά πράγματα:
- Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκαταστήσει το JDK στο σύστημά σας.
-  Aspose.PSD για Java: Λήψη της βιβλιοθήκης από[εδώ](https://releases.aspose.com/psd/java/) και συμπεριλάβετέ το στο έργο σας.
- Ένα IDE: Χρησιμοποιήστε το αγαπημένο σας ολοκληρωμένο περιβάλλον ανάπτυξης (IDE) όπως το IntelliJ IDEA ή το Eclipse.
## Εισαγωγή πακέτων
Πρώτα πράγματα πρώτα, πρέπει να εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java. Αυτά τα πακέτα είναι απαραίτητα για την εργασία με το Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Βήμα 1: Φορτώστε το αρχείο PSD
Το πρώτο βήμα για την προσθήκη ενός μοτίβου στρώσης περιγράμματος είναι να φορτώσετε το αρχείο PSD που θέλετε να επεξεργαστείτε.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Με τη φόρτωση του αρχείου PSD, μπορείτε πλέον να έχετε πρόσβαση και να χειρίζεστε τα επίπεδα και τα εφέ του.
## Βήμα 2: Προετοιμάστε δεδομένα νέου μοτίβου
Στη συνέχεια, θα πρέπει να προετοιμάσετε τα νέα δεδομένα μοτίβου που θα εφαρμόσετε στο στρώμα stroke.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
Αυτά τα δεδομένα μοτίβου θα χρησιμοποιηθούν για τη δημιουργία του νέου εφέ διαδρομής.
## Βήμα 3: Πρόσβαση στο Stroke Effect
Για να τροποποιήσετε το εφέ stroke, πρέπει να αποκτήσετε πρόσβαση στο συγκεκριμένο επίπεδο και τις επιλογές ανάμειξής του.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Αυτό διασφαλίζει ότι εργάζεστε με το σωστό επίπεδο και εφέ.
## Βήμα 4: Τροποποιήστε το Stroke Effect
Τώρα, ας τροποποιήσουμε το εφέ διαδρομής με τα νέα δεδομένα μοτίβου.
### Ενημέρωση ιδιοτήτων εφέ Stroke
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Ενημερώστε τον πόρο του μοτίβου
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Αυτό το απόσπασμα κώδικα ενημερώνει τον πόρο του μοτίβου με τα νέα δεδομένα μοτίβου.
## Βήμα 5: Εφαρμόστε το νέο μοτίβο
Τέλος, εφαρμόστε το νέο μοτίβο στο εφέ stroke και αποθηκεύστε τις αλλαγές.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Αυτό διασφαλίζει ότι το νέο μοτίβο εφαρμόζεται σωστά και ότι το αρχείο αποθηκεύεται με τις αλλαγές.
## Βήμα 6: Επαληθεύστε τις Αλλαγές
Για να βεβαιωθείτε ότι όλα λειτουργούσαν σωστά, φορτώστε ξανά το αρχείο και επαληθεύστε τις αλλαγές.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
Αυτό το βήμα επαληθεύει ότι τα δεδομένα μοτίβου έχουν εφαρμοστεί σωστά στο εφέ διαδρομής.
## συμπέρασμα
Και εκεί το έχετε! Προσθέσατε επιτυχώς ένα μοτίβο επιπέδου stroke σε ένα αρχείο PSD χρησιμοποιώντας το Aspose.PSD για Java. Ακολουθώντας αυτά τα βήματα, μπορείτε να προσαρμόσετε και να βελτιώσετε τις εικόνες σας με ευκολία. Καλή κωδικοποίηση!
## Συχνές ερωτήσεις
### Τι είναι το Aspose.PSD για Java;
Το Aspose.PSD για Java είναι μια βιβλιοθήκη που επιτρέπει στους προγραμματιστές να δημιουργούν, να επεξεργάζονται και να μετατρέπουν αρχεία PSD (Photoshop Document) μέσω προγραμματισμού.
### Μπορώ να χρησιμοποιήσω το Aspose.PSD για Java σε ένα εμπορικό έργο;
 Ναι, μπορείτε να το χρησιμοποιήσετε σε εμπορικά έργα. Μπορείτε να αγοράσετε άδεια από[εδώ](https://purchase.aspose.com/buy).
### Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.PSD για Java;
 Ναι, μπορείτε να κάνετε λήψη μιας δωρεάν δοκιμαστικής έκδοσης από[εδώ](https://releases.aspose.com/).
### Πώς μπορώ να λάβω υποστήριξη για το Aspose.PSD για Java;
 Μπορείτε να λάβετε υποστήριξη από τα φόρουμ της κοινότητας Aspose[εδώ](https://forum.aspose.com/c/psd/34).
### Ποιες είναι οι απαιτήσεις συστήματος για το Aspose.PSD για Java;
Χρειάζεστε εγκατεστημένο το JDK και ένα IDE για ανάπτυξη. Η βιβλιοθήκη υποστηρίζει πολλαπλά λειτουργικά συστήματα, συμπεριλαμβανομένων των Windows, Linux και macOS.