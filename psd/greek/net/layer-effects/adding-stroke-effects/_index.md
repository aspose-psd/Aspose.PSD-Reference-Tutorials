---
title: Προσθήκη εφέ Stroke σε επίπεδα στο Aspose.PSD για .NET
linktitle: Προσθήκη εφέ Stroke στα επίπεδα
second_title: Aspose.PSD .NET API
description: Βελτιώστε την αισθητική της εικόνας με το Aspose.PSD για .NET. Μάθετε να προσθέτετε εφέ εγκεφαλικού επεισοδίου βήμα προς βήμα. Κατεβάστε, αγοράστε ή δοκιμάστε τη δωρεάν δοκιμή τώρα.
weight: 10
url: /el/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσθήκη εφέ Stroke σε επίπεδα στο Aspose.PSD για .NET

## Εισαγωγή

Καλώς ήρθατε σε αυτό το βήμα προς βήμα σεμινάριο για την προσθήκη εφέ stroke σε επίπεδα στο Aspose.PSD για .NET. Η βελτίωση της οπτικής ελκυστικότητας των εικόνων σας είναι παιχνιδάκι με το εφέ stroke και το Aspose.PSD το κάνει απρόσκοπτο για προγραμματιστές .NET. Σε αυτόν τον οδηγό, θα σας καθοδηγήσουμε στη διαδικασία, παρέχοντας σαφή βήματα και παραδείγματα που θα σας βοηθήσουν να κατακτήσετε αυτό το ισχυρό χαρακτηριστικό.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Aspose.PSD για .NET: Λήψη και εγκατάσταση της βιβλιοθήκης Aspose.PSD από το[δικτυακός τόπος](https://releases.aspose.com/psd/net/).

- Κατάλογος εγγράφων: Προετοιμάστε έναν κατάλογο που περιέχει το έγγραφο PSD στο οποίο θέλετε να εφαρμόσετε εφέ διαδρομής.

- Κατάλογος εξόδου: Έχετε έναν ξεχωριστό κατάλογο για την αποθήκευση των εικόνων εξόδου με εφέ περιγράμματος.

- Visual Studio: Βεβαιωθείτε ότι έχετε ρυθμίσει το Visual Studio ή οποιοδήποτε άλλο προτιμώμενο περιβάλλον ανάπτυξης .NET.

## Εισαγωγή χώρων ονομάτων

Στο έργο σας .NET, συμπεριλάβετε τους απαραίτητους χώρους ονομάτων για να αξιοποιήσετε τη λειτουργικότητα Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Βήμα 1: Φορτώστε το έγγραφο PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Ο κωδικός σας για τη φόρτωση του εγγράφου PSD βρίσκεται εδώ
}
```

## Βήμα 2: Προσθέστε εφέ Color Stroke

```csharp
// Προσθέτει Color fill, στη θέση Inside
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Βήμα 3: Εξωτερική θέση

```csharp
// Προσθέτει Color fill, στη θέση Outside
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Βήμα 4: Θέση στο κέντρο

```csharp
// Προσθέτει Color fill, στη θέση Κέντρο
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Επαναλάβετε παρόμοια βήματα για γεμίσματα κλίσης και μοτίβων, προσαρμόζοντας τις ρυθμίσεις ανάλογα.

## Σύναψη

Συγχαρητήρια! Μάθατε με επιτυχία πώς να προσθέτετε εφέ stroke σε επίπεδα χρησιμοποιώντας το Aspose.PSD για .NET. Πειραματιστείτε με διαφορετικές ρυθμίσεις για να επιτύχετε το επιθυμητό οπτικό αποτέλεσμα στις εικόνες σας.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να εφαρμόσω εφέ εγκεφαλικού επεισοδίου μόνο σε συγκεκριμένα επίπεδα;

A1: Ναι, μπορείτε να στοχεύσετε συγκεκριμένα επίπεδα προσαρμόζοντας τον δείκτη επιπέδων στον κώδικα.

### Ε2: Είναι το Aspose.PSD συμβατό με το πιο πρόσφατο πλαίσιο .NET;

Α2: Απολύτως! Το Aspose.PSD έχει σχεδιαστεί για να ενσωματώνεται απρόσκοπτα με τα πιο πρόσφατα πλαίσια .NET.

### Ε3: Πώς μπορώ να προσαρμόσω το χρώμα περιγράμματος;

 A3: Απλώς τροποποιήστε το`Color` ιδιότητα στον κώδικα για να επιτευχθεί το επιθυμητό χρώμα διαδρομής.

### Ε4: Το Aspose.PSD υποστηρίζει τη μαζική επεξεργασία για πολλά αρχεία PSD;

A4: Ναι, μπορείτε να κάνετε επαναφορά σε πολλά αρχεία PSD και να εφαρμόσετε το εφέ stroke χρησιμοποιώντας μια παρόμοια προσέγγιση.

### Ε5: Μπορώ να χρησιμοποιήσω τη δοκιμαστική έκδοση πριν αγοράσω το Aspose.PSD;

 Α5: Σίγουρα! Πιάσε το[δωρεάν δοκιμή](https://releases.aspose.com/) για να εξερευνήσετε τις δυνατότητες του Aspose.PSD πριν κάνετε μια αγορά.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
