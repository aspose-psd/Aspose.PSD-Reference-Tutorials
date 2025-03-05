---
title: Implementierung der Helligkeitsanpassung in Aspose.PSD für .NET
linktitle: Implementieren der Helligkeitsanpassung
second_title: Aspose.PSD .NET API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.PSD für .NET beim Anpassen der Bildhelligkeit. Folgen Sie unserer Schritt-für-Schritt-Anleitung für eine nahtlose Implementierung.
type: docs
weight: 10
url: /de/net/image-adjustment/brightness-adjustment/
---
## Einführung

Das Verbessern und Anpassen von Bildattributen ist eine häufige Anforderung in verschiedenen Anwendungen, und Aspose.PSD für .NET bietet eine leistungsstarke Lösung für die nahtlose Bearbeitung von PSD-Dateien. Eine solche Bearbeitung ist die Helligkeitsanpassung, mit der Sie die Helligkeit eines Bildes mühelos ändern können.

In diesem Tutorial führen wir Sie durch den Prozess der Implementierung der Helligkeitsanpassung mit Aspose.PSD für .NET. Befolgen Sie die nachstehenden Schritte, um ein umfassendes Verständnis dafür zu erlangen, wie Sie Helligkeitsanpassungen in Ihre PSD-Dateien integrieren.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Aspose.PSD für .NET-Bibliothek herunter und installieren Sie sie von der[Downloadlink](https://releases.aspose.com/psd/net/).

-  Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, in dem Sie Ihre PSD-Dateien speichern und aktualisieren können.`dataDir` Variable im bereitgestellten Code-Snippet mit dem Pfad zu Ihrem Dokumentverzeichnis.

## Namespaces importieren

Fügen Sie in Ihr .NET-Projekt die erforderlichen Namespaces ein, um auf die Aspose.PSD-Funktionalität zuzugreifen. Fügen Sie Ihrem Code die folgenden Namespaces hinzu:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Lassen Sie uns das Beispiel nun in mehrere Schritte aufteilen:

## Schritt 1: Laden Sie die PSD-Datei

```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Laden Sie die PSD-Datei mit Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Hier kommt Ihr Code für die weiteren Schritte hin
}
```

## Schritt 2: Rasterbild erhalten

```csharp
// Holen Sie sich das Rasterbild aus der geladenen PSD-Datei
RasterCachedImage rasterImage = image;
```

## Schritt 3: Helligkeit anpassen

```csharp
// Stellen Sie den Helligkeitswert ein. Die zulässigen Helligkeitswerte liegen im Bereich [-255, 255].
rasterImage.AdjustBrightness(-50);
```

## Schritt 4: Speichern Sie das geänderte Bild

```csharp
// Speichern Sie das geänderte Bild mit angepasster Helligkeit
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Nachdem wir das Beispiel nun in überschaubare Schritte unterteilt haben, können Sie die Helligkeitsanpassung mit Aspose.PSD nahtlos in Ihr .NET-Projekt integrieren.

## Abschluss

Aspose.PSD für .NET vereinfacht die Implementierung von Helligkeitsanpassungen in PSD-Dateien. Indem Sie der oben angegebenen Schritt-für-Schritt-Anleitung folgen, können Sie die visuelle Attraktivität Ihrer Bilder mühelos verbessern. Experimentieren Sie mit verschiedenen Helligkeitswerten, um die gewünschten Ergebnisse zu erzielen.

## Häufig gestellte Fragen

### F1: Wo finde ich die Dokumentation für Aspose.PSD für .NET?

 A1: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/psd/net/).

### F2: Wie kann ich die Aspose.PSD-Bibliothek für .NET herunterladen?

 A2: Sie können die Bibliothek herunterladen von der[Veröffentlichungsseite](https://releases.aspose.com/psd/net/).

### F3: Gibt es eine kostenlose Testversion für Aspose.PSD für .NET?

 A3: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wo erhalte ich Support für Aspose.PSD für .NET?

 A4: Für Support besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).

### F5: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD für .NET?

 A5: Sie können eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).