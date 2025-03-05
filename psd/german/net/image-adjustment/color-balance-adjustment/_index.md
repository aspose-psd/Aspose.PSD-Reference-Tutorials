---
title: Anwenden einer Farbbalance-Anpassung in Aspose.PSD für .NET
linktitle: Anwenden der Farbbalance-Anpassung
second_title: Aspose.PSD .NET API
description: Verbessern Sie PSD-Bildfarben mühelos mit der Funktion zur Farbbalance-Anpassung von Aspose.PSD für .NET. Folgen Sie unserer Schritt-für-Schritt-Anleitung für atemberaubende Ergebnisse.
type: docs
weight: 14
url: /de/net/image-adjustment/color-balance-adjustment/
---
## Einführung

Willkommen zu diesem umfassenden Leitfaden zur Anwendung der Farbbalance-Anpassung in Aspose.PSD für .NET! Aspose.PSD ist eine leistungsstarke .NET-Bibliothek, mit der Entwickler effizient mit PSD-Dateien arbeiten können. In diesem Tutorial konzentrieren wir uns auf die Funktion zur Farbbalance-Anpassung, mit der Sie die Farbbalance Ihrer PSD-Bilder mühelos verbessern können.

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek herunter und installieren Sie sie von der[Aspose.PSD-Website](https://releases.aspose.com/psd/net/).
- Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine funktionierende .NET-Entwicklungsumgebung eingerichtet ist.
- PSD-Datei: Halten Sie eine PSD-Datei bereit, auf die Sie die Farbbalance-Anpassung anwenden möchten.

## Namespaces importieren

Schließen Sie in Ihr .NET-Projekt die erforderlichen Namespaces ein, um Aspose.PSD-Funktionen zu verwenden. Fügen Sie Ihrem Code die folgenden Zeilen hinzu:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Lassen Sie uns nun den Vorgang zur Farbbalance-Anpassung in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie die PSD-Datei

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Code zur Farbbalance-Anpassung wird in den folgenden Schritten hinzugefügt.
}
```

## Schritt 2: Farbbalance aufrufen und anpassen

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Schritt 3: Speichern Sie das angepasste Bild

```csharp
im.Save(outputPath);
```

Jetzt haben Sie die Farbbalance-Anpassung mit Aspose.PSD für .NET erfolgreich auf Ihre PSD-Datei angewendet!

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie den Farbausgleich Ihrer PSD-Bilder mit Aspose.PSD für .NET verbessern können. Experimentieren Sie mit verschiedenen Ausgleichswerten, um die gewünschten visuellen Effekte zu erzielen.

## Häufig gestellte Fragen

### F1: Kann ich die Farbbalance-Anpassung auf mehrere Ebenen anwenden?

A1: Ja, Sie können alle Ebenen in Ihrer PSD-Datei durchlaufen und den Farbabgleich nach Bedarf anpassen.

### F2: Ist Aspose.PSD für .NET für die Stapelverarbeitung von PSD-Dateien geeignet?

A2: Auf jeden Fall! Aspose.PSD bietet effiziente Stapelverarbeitungsfunktionen für PSD-Dateien.

### F3: Wie kann ich eine temporäre Lizenz für Aspose.PSD für .NET erhalten?

 A3: Besuch[Aspose.PSD Temporäre Lizenz](https://purchase.aspose.com/temporary-license/) für eine vorübergehende Lizenz.

### F4: Wo finde ich weitere Beispiele und Dokumentation?

 A4: Erkunden Sie die[Aspose.PSD-Dokumentation](https://reference.aspose.com/psd/net/) für ausführliche Beispiele und Anleitungen.

### F5: Welche Supportoptionen sind für Aspose.PSD für .NET verfügbar?

 A5: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.
