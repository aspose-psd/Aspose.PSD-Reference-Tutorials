---
title: Hinzufügen einer Strichebene mit Volltonfarbe in Aspose.PSD für .NET
linktitle: Strichebene mit Volltonfarbe hinzufügen
second_title: Aspose.PSD .NET API
description: Verbessern Sie Ihre .NET-Bildbearbeitungsfähigkeiten mit Aspose.PSD. Erfahren Sie Schritt für Schritt, wie Sie Strichebenen mit Volltonfarben hinzufügen.
type: docs
weight: 11
url: /de/net/layer-effects/adding-stroke-layer-solid-color/
---
## Einführung

Im Bereich der .NET-Entwicklung ist die Erstellung optisch ansprechender Bilder eine häufige Anforderung. Aspose.PSD für .NET bietet einen leistungsstarken Satz von Tools zur nahtlosen Bearbeitung und Verbesserung von Bildern. Eine der wesentlichen Funktionen ist das Hinzufügen einer Strichebene mit einer Volltonfarbe, die Ihren Bildern Lebendigkeit und Tiefe verleiht. In diesem Tutorial führen wir Sie Schritt für Schritt durch den Prozess mit Aspose.PSD für .NET.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- Grundkenntnisse der .NET-Entwicklung.
- Visual Studio ist auf Ihrem Computer installiert.
- Aspose.PSD für .NET-Bibliothek. Sie können es herunterladen von der[Webseite](https://releases.aspose.com/psd/net/).

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces, um die Funktionalität von Aspose.PSD für .NET zu nutzen:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Schritt 1: Laden Sie die PSD-Datei

Laden Sie zunächst die PSD-Datei, die Sie mit einer Strichebene verbessern möchten. Stellen Sie sicher, dass Sie den richtigen Dateipfad haben:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Code für weitere Schritte wird hier hinzugefügt
}
```

## Schritt 2: Auf die Eigenschaften des Stricheffekts zugreifen

Rufen Sie die Eigenschaften des Stricheffekts aus der PSD-Datei ab:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## Schritt 3: Stricheinstellungen anpassen

Ändern Sie die Stricheinstellungen nach Ihren Wünschen. In diesem Beispiel ändern wir die Farbe in Gelb, stellen die Deckkraft auf 127 ein und verwenden den Farbmischmodus:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## Schritt 4: Speichern Sie das bearbeitete Bild

Speichern Sie das Bild, nachdem Sie die Änderungen an der Strichebene angewendet haben:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## Schritt 5: Überprüfen der Änderungen

Stellen Sie sicher, dass die Änderungen korrekt angewendet wurden, indem Sie das bearbeitete Bild laden und überprüfen:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Code zur Überprüfung der Änderungen wird hier hinzugefügt
}
```

Wiederholen Sie diese Schritte für weitere Anpassungen oder experimentieren Sie mit verschiedenen Stricheffekten, um die gewünschte visuelle Wirkung zu erzielen.

## Abschluss

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.PSD für .NET eine Strichebene mit einer Volltonfarbe hinzufügen. Diese leistungsstarke Funktion eröffnet Ihnen eine Welt voller Möglichkeiten zur Verbesserung Ihrer Bilder in der .NET-Umgebung.

## FAQs

### F1: Ist Aspose.PSD für .NET mit den neuesten Versionen des .NET-Frameworks kompatibel?

A1: Ja, Aspose.PSD für .NET wird regelmäßig aktualisiert, um die Kompatibilität mit den neuesten Versionen des .NET-Frameworks sicherzustellen.

### F2: Kann ich Aspose.PSD für .NET für kommerzielle Projekte verwenden?

A2: Auf jeden Fall! Aspose.PSD für .NET ist ein kommerzielles Produkt und Sie können es in Ihren Projekten verwenden, indem Sie eine Lizenz erwerben.

### F3: Wo finde ich weitere Beispiele und Dokumentation für Aspose.PSD für .NET?

 A3: Erkunden Sie die[Dokumentation](https://reference.aspose.com/psd/net/) für umfassende Beispiele und Anleitungen.

### F4: Gibt es eine kostenlose Testversion für Aspose.PSD für .NET?

 A4: Ja, Sie können eine kostenlose Testversion erhalten von der[Veröffentlichungsseite](https://releases.aspose.com/).

### F5: Wie erhalte ich Support für Aspose.PSD für .NET?

 A5: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) um Hilfe zu suchen und Kontakt mit der Community aufzunehmen.