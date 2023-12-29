---
title: Anwenden der Farbbalance-Anpassung in Aspose.PSD für .NET
linktitle: Anwenden der Farbbalance-Anpassung
second_title: Aspose.PSD .NET-API
description: Verbessern Sie die Farben von PSD-Bildern mühelos mit der Farbbalance-Anpassungsfunktion von Aspose.PSD für .NET. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für atemberaubende Ergebnisse.
type: docs
weight: 14
url: /de/net/image-adjustment/color-balance-adjustment/
---
## Einführung

Willkommen zu dieser umfassenden Anleitung zum Anwenden der Farbbalance-Anpassung in Aspose.PSD für .NET! Aspose.PSD ist eine leistungsstarke .NET-Bibliothek, die es Entwicklern ermöglicht, effizient mit PSD-Dateien zu arbeiten. In diesem Tutorial konzentrieren wir uns auf die Funktion zur Farbbalance-Anpassung, mit der Sie die Farbbalance Ihrer PSD-Bilder ganz einfach verbessern können.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Aspose.PSD-Website](https://releases.aspose.com/psd/net/).
- Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine funktionierende .NET-Entwicklungsumgebung eingerichtet ist.
- PSD-Datei: Halten Sie eine PSD-Datei bereit, auf die Sie die Farbbalance-Anpassung anwenden möchten.

## Namespaces importieren

Fügen Sie in Ihr .NET-Projekt die erforderlichen Namespaces ein, um Aspose.PSD-Funktionen zu verwenden. Fügen Sie Ihrem Code die folgenden Zeilen hinzu:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Lassen Sie uns nun den Prozess der Farbbalance-Anpassung in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie die PSD-Datei

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Code für die Farbbalance-Anpassung wird in den folgenden Schritten hinzugefügt.
}
```

## Schritt 2: Auf die Farbbalance zugreifen und diese anpassen

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

Glückwunsch! Sie haben gelernt, wie Sie die Farbbalance Ihrer PSD-Bilder mit Aspose.PSD für .NET verbessern. Experimentieren Sie mit verschiedenen Balancewerten, um die gewünschten visuellen Effekte zu erzielen.

## FAQs

### F1: Kann ich die Farbbalance-Anpassung auf mehrere Ebenen anwenden?

A1: Ja, Sie können alle Ebenen in Ihrer PSD-Datei durchlaufen und die Farbbalance nach Bedarf anpassen.

### F2: Ist Aspose.PSD für .NET für die Stapelverarbeitung von PSD-Dateien geeignet?

A2: Auf jeden Fall! Aspose.PSD bietet effiziente Stapelverarbeitungsfunktionen für PSD-Dateien.

### F3: Wie kann ich eine temporäre Lizenz für Aspose.PSD für .NET erhalten?

 A3: Besuchen[Temporäre Aspose.PSD-Lizenz](https://purchase.aspose.com/temporary-license/) für eine befristete Lizenz.

### F4: Wo finde ich weitere Beispiele und Dokumentation?

 A4: Entdecken Sie die[Aspose.PSD-Dokumentation](https://reference.aspose.com/psd/net/) Ausführliche Beispiele und Anleitungen finden Sie hier.

### F5: Welche Supportoptionen stehen für Aspose.PSD für .NET zur Verfügung?

 A5: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.
