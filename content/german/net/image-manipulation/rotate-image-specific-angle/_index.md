---
title: Drehen eines Bildes in einem bestimmten Winkel in Aspose.PSD für .NET
linktitle: Drehen eines Bildes in einem bestimmten Winkel
second_title: Aspose.PSD .NET-API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.PSD für .NET. Drehen Sie Bilder mühelos in bestimmten Winkeln. Laden Sie die Bibliothek herunter und beginnen Sie mit der nahtlosen Bearbeitung von Bildern.
type: docs
weight: 16
url: /de/net/image-manipulation/rotate-image-specific-angle/
---
Wenn Sie in die Welt der Bildbearbeitung mit .NET eintauchen, bietet Aspose.PSD eine leistungsstarke Lösung. In diesem Tutorial führen wir Sie durch den Prozess der Drehung eines Bildes in einem bestimmten Winkel mit Aspose.PSD. Bevor wir uns mit den einzelnen Schritten befassen, bereiten wir mit einer Einführung die Bühne.

## Einführung

Aspose.PSD für .NET ist eine vielseitige Bibliothek, die Entwicklern die nahtlose Arbeit mit PSD- und Rasterbildformaten ermöglicht. Eines seiner Hauptmerkmale ist die Möglichkeit, Bilder in präzisen Winkeln zu drehen, was für Flexibilität bei der Bildbearbeitung sorgt. Dieses Tutorial führt Sie durch die Schritte zum Drehen eines Bildes in einem bestimmten Winkel mit Aspose.PSD für .NET.

## Voraussetzungen

Bevor wir uns auf diese Reise begeben, stellen Sie sicher, dass Sie über die folgenden Voraussetzungen verfügen:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Download-Seite](https://releases.aspose.com/psd/net/).
- Dokumentverzeichnis: Richten Sie ein Verzeichnis zum Speichern Ihrer Quell- und Ausgabedateien ein.

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces in Ihr .NET-Projekt:

```csharp
using Aspose.PSD.ImageOptions;
```

Lassen Sie uns nun das Beispiel in einer Schritt-für-Schritt-Anleitung in mehrere Schritte unterteilen.

## Schritt 1: Legen Sie Ihr Dokumentenverzeichnis fest

```csharp
string dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` mit dem Pfad zu dem Verzeichnis, in dem Sie Ihre Quell- und Ausgabedateien speichern.

## Schritt 2: Laden Sie das Bild

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Hier werden zusätzliche Schritte eingefügt
}
```

 Laden Sie das Bild, das Sie drehen möchten, in eine Instanz davon`RasterImage`.

## Schritt 3: Bilddaten zwischenspeichern

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Zwischenspeichern Sie die Bilddaten für eine bessere Leistung während der Rotation.

## Schritt 4: Drehen Sie das Bild

```csharp
image.Rotate(20f, true, Color.Red);
```

Drehen Sie das Bild um 20 Grad, behalten Sie dabei die proportionale Größe bei und verwenden Sie einen roten Hintergrund.

## Schritt 5: Speichern Sie das Ergebnis

```csharp
image.Save(destName, new JpegOptions());
```

Speichern Sie das gedrehte Bild mit den angegebenen Optionen (in diesem Fall als JPEG).

## Abschluss

 Glückwunsch! Sie haben ein Bild mit Aspose.PSD für .NET erfolgreich um einen bestimmten Winkel gedreht. Diese Bibliothek bietet einen robusten Satz an Werkzeugen zur Bildbearbeitung, und dieses Tutorial ist nur die Spitze des Eisbergs. Entdecke die[Dokumentation](https://reference.aspose.com/psd/net/) für weitere Funktionen und Optionen.

## FAQs

### F1: Kann ich Bilder um andere Winkel als 20 Grad drehen?

 A1: Ja, Sie können den Winkelparameter im anpassen`image.Rotate` Methode auf einen beliebigen Wert.

### F2: Unterstützt Aspose.PSD neben JPEG auch andere Bildformate?

A2: Auf jeden Fall! Aspose.PSD unterstützt eine Vielzahl von Formaten, darunter PNG, GIF, BMP und TIFF.

### F3: Müssen Bilddaten vor der Drehung zwischengespeichert werden?

A3: Das Zwischenspeichern von Daten ist zwar nicht zwingend erforderlich, kann jedoch die Leistung erheblich verbessern, insbesondere bei größeren Bildern.

### F4: Wo erhalte ich Unterstützung für Aspose.PSD-bezogene Abfragen?

 A4: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.

### F5: Kann ich Aspose.PSD vor dem Kauf testen?

 A5: Auf jeden Fall! Schnapp dir dein[Kostenlose Testphase](https://releases.aspose.com/) um die Möglichkeiten der Bibliothek zu erkunden.