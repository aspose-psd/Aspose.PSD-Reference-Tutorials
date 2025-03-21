---
title: Αλλαγή μεγέθους εικόνων ανάλογα στο Aspose.PSD για .NET
linktitle: Αλλαγή μεγέθους εικόνων ανάλογα
second_title: Aspose.PSD .NET API
description: Εξερευνήστε απρόσκοπτη αλλαγή μεγέθους εικόνας με το Aspose.PSD για .NET. Κατεβάστε τη βιβλιοθήκη, ακολουθήστε το σεμινάριο μας και βελτιώστε τις δυνατότητες επεξεργασίας εικόνας σας.
weight: 14
url: /el/net/image-manipulation/resize-images-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αλλαγή μεγέθους εικόνων ανάλογα στο Aspose.PSD για .NET

Στον τομέα της επεξεργασίας εικόνας, το Aspose.PSD για .NET ξεχωρίζει ως ένα ισχυρό κιτ εργαλείων, που παρέχει στους προγραμματιστές τη δυνατότητα να αλλάζουν το μέγεθος των εικόνων αναλογικά με ευκολία. Σε αυτόν τον οδηγό βήμα προς βήμα, θα σας καθοδηγήσουμε στη διαδικασία αλλαγής μεγέθους εικόνων χρησιμοποιώντας το Aspose.PSD για .NET, διασφαλίζοντας ότι οι εικόνες σας διατηρούν άψογα τις αναλογίες τους.

## Εισαγωγή

Η αναλογική αλλαγή του μεγέθους των εικόνων είναι μια κοινή εργασία σε πολλές εφαρμογές και το Aspose.PSD για .NET απλοποιεί αυτή τη διαδικασία για τους προγραμματιστές. Είτε εργάζεστε σε μια εφαρμογή ιστού, σε λογισμικό επιτραπέζιου υπολογιστή ή σε εφαρμογή για κινητά, η κατανόηση του τρόπου αλλαγής μεγέθους των εικόνων διατηρώντας την αναλογία διαστάσεων είναι ζωτικής σημασίας για τη διατήρηση της οπτικής ελκυστικότητας και της συνέπειας.

## Προαπαιτούμενα

Πριν ξεκινήσετε τη μαγεία αλλαγής μεγέθους με το Aspose.PSD για .NET, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

1.  Aspose.PSD για .NET Library: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.PSD για .NET. Μπορείτε να το κατεβάσετε από το[Aspose.PSD για εκδόσεις .NET](https://releases.aspose.com/psd/net/) σελίδα.

2. Κατάλογος εγγράφων: Δημιουργήστε έναν κατάλογο για να αποθηκεύσετε τα έγγραφά σας και αντικαταστήστε τον "Κατάλογο εγγράφων σας" στον παρεχόμενο κώδικα με την πραγματική διαδρομή προς αυτόν τον κατάλογο.

Τώρα που έχετε ρυθμίσει τις προϋποθέσεις, ας μεταβούμε στον οδηγό βήμα προς βήμα.

## Εισαγωγή χώρων ονομάτων

```csharp
using Aspose.PSD.ImageOptions;
```

Εισαγάγετε τους απαραίτητους χώρους ονομάτων για πρόσβαση στις απαιτούμενες κλάσεις και μεθόδους.

## Βήμα 1: Φορτώστε την εικόνα

```csharp
// Η διαδρομή προς τον κατάλογο εγγράφων.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Φορτώστε μια υπάρχουσα εικόνα σε μια παρουσία της κλάσης RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Τα υπόλοιπα βήματα πηγαίνετε εδώ
}
```

 Φορτώστε την εικόνα προέλευσης χρησιμοποιώντας το`Image.Load` μέθοδος.

## Βήμα 2: Καθορίστε το πλάτος και το ύψος

```csharp
// Καθορισμός πλάτους και ύψους
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Προσδιορίστε το νέο πλάτος και ύψος για την αλλαγή μεγέθους εικόνας. Σε αυτό το παράδειγμα, το πλάτος και το ύψος μειώνονται στο μισό, αλλά μπορείτε να προσαρμόσετε αυτές τις τιμές με βάση τις απαιτήσεις σας.

## Βήμα 3: Αποθηκεύστε την εικόνα με αλλαγή μεγέθους

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Αποθηκεύστε την εικόνα με αλλαγή μεγέθους χρησιμοποιώντας το`Save` μέθοδος με καθορισμένες επιλογές. Σε αυτήν την περίπτωση, το αποθηκεύουμε ως αρχείο PNG.

## Σύναψη

Η αναλογική αλλαγή του μεγέθους των εικόνων στο Aspose.PSD για .NET είναι μια απλή διαδικασία που προσθέτει αξία στη ροή εργασιών επεξεργασίας εικόνας. Αυτός ο οδηγός σάς έχει εξοπλίσει με τις γνώσεις για την απρόσκοπτη ενσωμάτωση αυτής της λειτουργικότητας στις εφαρμογές σας.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να αλλάξω το μέγεθος των εικόνων σε συγκεκριμένες διαστάσεις;

A1: Ναι, μπορείτε να προσαρμόσετε το νέο πλάτος και ύψος σύμφωνα με τις απαιτήσεις σας στον κωδικό.

### Ε2: Είναι το Aspose.PSD για .NET κατάλληλο για μαζική αλλαγή μεγέθους εικόνας;

Α2: Απολύτως! Μπορείτε να ενσωματώσετε αυτά τα βήματα σε έναν βρόχο για ομαδική επεξεργασία πολλαπλών εικόνων.

### Ε3: Υπάρχουν άλλες δυνατότητες χειρισμού εικόνας στο Aspose.PSD για .NET;

A3: Ναι, το Aspose.PSD για .NET προσφέρει ένα ευρύ φάσμα δυνατοτήτων, όπως περικοπή, περιστροφή και εφαρμογή φίλτρων σε εικόνες.

### Ε4: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.PSD για .NET;

 A4: Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες του Aspose.PSD για .NET με μια δωρεάν δοκιμή. Επίσκεψη[εδώ](https://releases.aspose.com/) για να ξεκινήσετε.

### Ε5: Πού μπορώ να βρω υποστήριξη για το Aspose.PSD για .NET;

 A5: Επισκεφθείτε το[Aspose.PSD για φόρουμ .NET](https://forum.aspose.com/c/psd/34) για κοινοτική υποστήριξη και συζητήσεις.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
