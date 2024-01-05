---
title: Implementieren der Helligkeitsanpassung in Aspose.PSD für .NET
linktitle: Implementierung der Helligkeitsanpassung
second_title: Aspose.PSD .NET-API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.PSD für .NET bei der Anpassung der Bildhelligkeit. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine reibungslose Implementierung.
type: docs
weight: 10
url: /de/net/image-adjustment/brightness-adjustment/
---
## Einführung

Das Verbessern und Anpassen von Bildattributen ist eine häufige Anforderung in verschiedenen Anwendungen, und Aspose.PSD für .NET bietet eine leistungsstarke Lösung für die nahtlose Bearbeitung von PSD-Dateien. Eine dieser Manipulationen ist die Helligkeitsanpassung, mit der Sie die Helligkeit eines Bildes mühelos ändern können.

In diesem Tutorial führen wir den Prozess der Implementierung der Helligkeitsanpassung mit Aspose.PSD für .NET durch. Befolgen Sie die folgenden Schritte, um umfassend zu verstehen, wie Sie Helligkeitsanpassungen in Ihre PSD-Dateien integrieren.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Aspose.PSD für .NET-Bibliothek von herunter und installieren Sie sie[Download-Link](https://releases.aspose.com/psd/net/).

-  Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, um Ihre PSD-Dateien zu speichern und zu aktualisieren`dataDir` Variable im bereitgestellten Code-Snippet mit dem Pfad zu Ihrem Dokumentverzeichnis.

## Namespaces importieren

Fügen Sie in Ihr .NET-Projekt die erforderlichen Namespaces ein, um auf die Aspose.PSD-Funktionalität zuzugreifen. Fügen Sie Ihrem Code die folgenden Namespaces hinzu:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Lassen Sie uns das Beispiel nun in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie die PSD-Datei

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Laden Sie die PSD-Datei mit Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Ihr Code für weitere Schritte finden Sie hier
}
```

## Schritt 2: Rasterbild erhalten

```csharp
// Rufen Sie das Rasterbild aus der geladenen PSD-Datei ab
RasterCachedImage rasterImage = image;
```

## Schritt 3: Helligkeit anpassen

```csharp
// Stellen Sie den Helligkeitswert ein. Die akzeptierten Helligkeitswerte liegen im Bereich [-255, 255].
rasterImage.AdjustBrightness(-50);
```

## Schritt 4: Speichern Sie das geänderte Bild

```csharp
// Speichern Sie das geänderte Bild mit angepasster Helligkeit
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Nachdem wir das Beispiel nun in überschaubare Schritte unterteilt haben, können Sie die Helligkeitsanpassung mithilfe von Aspose.PSD nahtlos in Ihr .NET-Projekt integrieren.

## Abschluss

Aspose.PSD für .NET vereinfacht die Implementierung von Helligkeitsanpassungen in PSD-Dateien. Indem Sie die oben bereitgestellte Schritt-für-Schritt-Anleitung befolgen, können Sie die visuelle Attraktivität Ihrer Bilder mühelos verbessern. Experimentieren Sie mit verschiedenen Helligkeitswerten, um die gewünschten Ergebnisse zu erzielen.

## FAQs

### F1: Wo finde ich die Dokumentation für Aspose.PSD für .NET?

 A1: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/psd/net/).

### F2: Wie kann ich die Aspose.PSD für .NET-Bibliothek herunterladen?

 A2: Sie können die Bibliothek von herunterladen[Release-Seite](https://releases.aspose.com/psd/net/).

### F3: Gibt es eine kostenlose Testversion für Aspose.PSD für .NET?

 A3: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wo erhalte ich Unterstützung für Aspose.PSD für .NET?

 A4: Für Unterstützung besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).

### F5: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD für .NET?

 A5: Sie können eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).