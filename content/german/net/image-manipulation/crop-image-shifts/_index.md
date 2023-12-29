---
title: Zuschneiden von Bildern durch Verschiebungen in Aspose.PSD für .NET
linktitle: Bilder nach Schichten zuschneiden
second_title: Aspose.PSD .NET-API
description: Erfahren Sie, wie Sie mit Aspose.PSD für .NET Bilder mühelos zuschneiden. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für präzise Bildanpassungen.
type: docs
weight: 12
url: /de/net/image-manipulation/crop-image-shifts/
---
## Einführung

Im Bereich der .NET-Entwicklung sticht Aspose.PSD als leistungsstarkes Toolkit für Bildverarbeitungsaufgaben hervor. Eine seiner bemerkenswerten Funktionen ist die Möglichkeit, Bilder dank der Funktion „Zuschneiden nach Verschiebungen“ präzise zuzuschneiden. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess des nahtlosen Zuschneidens von Bildern mit Aspose.PSD für .NET.

## Voraussetzungen

Bevor Sie sich mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Bibliothek installiert haben. Wenn nicht, können Sie es hier herunterladen[Release-Seite](https://releases.aspose.com/psd/net/).

- .NET-Umgebung: Stellen Sie sicher, dass auf Ihrem Computer eine .NET-Entwicklungsumgebung eingerichtet ist.

- Beispielbild: Bereiten Sie ein Beispielbild im PSD-Format vor, mit dem Sie arbeiten möchten.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihr .NET-Projekt. Diese Namespaces bieten Zugriff auf die Aspose.PSD-Klassen und -Methoden, die zum Zuschneiden von Bildern erforderlich sind.

```csharp
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Definieren Sie Ihr Dokumentenverzeichnis

Legen Sie den Pfad zu Ihrem Dokumentverzeichnis fest, in dem sich die Quell- und Zieldateien befinden.

```csharp
string dataDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das Quellbild

Laden Sie das PSD-Bild, das Sie zuschneiden möchten. Stellen Sie sicher, dass Sie „sample.psd“ durch den Namen Ihrer Quelldatei ersetzen.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Schritt 3: Bilddaten zwischenspeichern, um eine bessere Leistung zu erzielen

Vor dem Zuschneiden empfiehlt es sich, die Bilddaten zwischenzuspeichern, um die Leistung zu verbessern.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Schritt 4: Definieren Sie Verschiebungswerte für das Zuschneiden

Geben Sie die Verschiebungswerte für die linke, rechte, obere und untere Seite des Bildes an. Passen Sie diese Werte entsprechend Ihren Zuschneideanforderungen an.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Schritt 5: Zuschneiden anwenden und Ergebnisse speichern

 Nutzen Sie die`Crop` Methode, um die angegebenen Verschiebungen anzuwenden und das zugeschnittene Bild in der Zieldatei zu speichern.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.PSD für .NET Bilder schichtweise zuschneiden. Diese leistungsstarke Funktionalität bietet Ihnen die Präzision und Kontrolle, die Sie für verschiedene Bildverarbeitungsaufgaben benötigen.

## FAQs

### F1: Kann ich Bilder in verschiedenen Formaten zuschneiden, nicht nur in PSD?

A1: Ja, Aspose.PSD unterstützt verschiedene Bildformate, sodass Sie Bilder in Formaten wie JPEG, PNG und mehr zuschneiden können.

### F2: Gibt es vor dem Kauf von Aspose.PSD für .NET eine Testversion?

 A2: Auf jeden Fall! Sie können das Toolkit mit einer kostenlosen Testversion erkunden[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD für .NET?

 A3: Zu Testzwecken können Sie eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).

### F4: Wo finde ich zusätzlichen Support und Diskussionen zu Aspose.PSD?

 A4: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für die Unterstützung und die spannenden Diskussionen.

### F5: Kann ich Aspose.PSD für .NET direkt von der Website kaufen?

 A5: Ja, Sie können die Bibliothek sicher bei kaufen[Kaufseite](https://purchase.aspose.com/buy).
