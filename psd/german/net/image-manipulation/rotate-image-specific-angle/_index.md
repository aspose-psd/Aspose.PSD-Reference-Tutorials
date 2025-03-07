---
title: Drehen eines Bildes in einem bestimmten Winkel in Aspose.PSD für .NET
linktitle: Drehen eines Bildes um einen bestimmten Winkel
second_title: Aspose.PSD .NET API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.PSD für .NET. Drehen Sie Bilder mühelos in bestimmte Winkel. Laden Sie die Bibliothek herunter und beginnen Sie nahtlos mit der Bildbearbeitung.
weight: 16
url: /de/net/image-manipulation/rotate-image-specific-angle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Drehen eines Bildes in einem bestimmten Winkel in Aspose.PSD für .NET

Wenn Sie in die Welt der Bildbearbeitung mit .NET eintauchen, bietet Aspose.PSD eine leistungsstarke Lösung. In diesem Tutorial führen wir Sie durch den Prozess der Drehung eines Bilds in einem bestimmten Winkel mit Aspose.PSD. Bevor wir in die einzelnen Schritte eintauchen, wollen wir die Bühne mit einer Einführung bereiten.

## Einführung

Aspose.PSD für .NET ist eine vielseitige Bibliothek, die Entwicklern die nahtlose Arbeit mit PSD- und Rasterbildformaten ermöglicht. Eines ihrer wichtigsten Features ist die Möglichkeit, Bilder in präzisen Winkeln zu drehen, was Flexibilität bei der Bildbearbeitung bietet. Dieses Tutorial führt Sie durch die Schritte zum Drehen eines Bilds in einem bestimmten Winkel mit Aspose.PSD für .NET.

## Voraussetzungen

Bevor wir uns auf diese Reise begeben, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek herunter und installieren Sie sie von der[Download-Seite](https://releases.aspose.com/psd/net/).
- Dokumentverzeichnis: Richten Sie ein Verzeichnis zum Speichern Ihrer Quell- und Ausgabedateien ein.

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces in Ihr .NET-Projekt:

```csharp
using Aspose.PSD.ImageOptions;
```

Lassen Sie uns das Beispiel nun im Format einer Schritt-für-Schritt-Anleitung in mehrere Schritte aufteilen.

## Schritt 1: Legen Sie Ihr Dokumentverzeichnis fest

```csharp
string dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` durch den Pfad zum Verzeichnis, in dem Sie Ihre Quell- und Ausgabedateien speichern.

## Schritt 2: Laden Sie das Bild

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Weitere Schritte werden hier eingefügt
}
```

 Laden Sie das Bild, das Sie drehen möchten, in eine Instanz von`RasterImage`.

## Schritt 3: Bilddaten zwischenspeichern

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Zwischenspeichern Sie die Bilddaten für eine bessere Leistung während der Rotation.

## Schritt 4: Bild drehen

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

 Herzlichen Glückwunsch! Sie haben ein Bild erfolgreich in einem bestimmten Winkel gedreht, indem Sie Aspose.PSD für .NET verwendet haben. Diese Bibliothek bietet einen robusten Satz von Werkzeugen zur Bildbearbeitung, und dieses Tutorial ist nur die Spitze des Eisbergs. Entdecken Sie die[Dokumentation](https://reference.aspose.com/psd/net/) für weitere Funktionen und Optionen.

## Häufig gestellte Fragen

### F1: Kann ich Bilder um andere Winkel als 20 Grad drehen?

 A1: Ja, Sie können den Winkelparameter im`image.Rotate` -Methode auf jeden gewünschten Wert.

### F2: Unterstützt Aspose.PSD andere Bildformate außer JPEG?

A2: Auf jeden Fall! Aspose.PSD unterstützt eine Vielzahl von Formaten, darunter PNG, GIF, BMP und TIFF.

### F3: Ist es notwendig, Bilddaten vor der Rotation zwischenzuspeichern?

A3: Obwohl es nicht zwingend erforderlich ist, kann das Zwischenspeichern von Daten die Leistung erheblich steigern, insbesondere bei größeren Bildern.

### F4: Wo erhalte ich Unterstützung bei Fragen zu Aspose.PSD?

 A4: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.

### F5: Kann ich Aspose.PSD vor dem Kauf ausprobieren?

 A5: Natürlich! Schnapp dir deine[Kostenlose Testversion](https://releases.aspose.com/)um die Möglichkeiten der Bibliothek zu erkunden.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
