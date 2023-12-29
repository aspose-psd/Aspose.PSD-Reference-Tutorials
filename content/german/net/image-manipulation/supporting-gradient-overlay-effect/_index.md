---
title: Unterstützt den Verlaufsüberlagerungseffekt in Aspose.PSD für .NET
linktitle: Unterstützt den Verlaufsüberlagerungseffekt
second_title: Aspose.PSD .NET-API
description: Verbessern Sie Grafiken in .NET mit Aspose.PSD. Dieses Tutorial führt Sie durch die Unterstützung von Verlaufsüberlagerungseffekten.
type: docs
weight: 18
url: /de/net/image-manipulation/supporting-gradient-overlay-effect/
---
## Einführung

Willkommen zu diesem umfassenden Tutorial zur Unterstützung des Verlaufsüberlagerungseffekts in Aspose.PSD für .NET! Wenn Sie die Grafikfunktionen Ihrer .NET-Anwendung verbessern möchten, hilft Ihnen diese Schritt-für-Schritt-Anleitung weiter. Wir befassen uns mit den Feinheiten der Erstellung und Bearbeitung des Verlaufsüberlagerungseffekts in einer Ebene mithilfe von Aspose.PSD, einer leistungsstarken Bibliothek, die die Bildverarbeitung vereinfacht.

## Voraussetzungen

Bevor wir uns auf diese Reise begeben, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Ein grundlegendes Verständnis der C#- und .NET-Programmierung.
-  Aspose.PSD für .NET installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/psd/net/).
- Eine Entwicklungsumgebung, die mit Ihrer bevorzugten IDE eingerichtet ist.

## Namespaces importieren

Importieren wir zunächst die erforderlichen Namespaces in Ihren C#-Code:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
```

Nachdem wir uns nun mit den Grundlagen befasst haben, wollen wir jeden Schritt im Detail aufschlüsseln:

## Schritt 1: Laden Sie das PSD-Bild

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFilePath = Path.Combine(SourceDir, "psdnet256.psd");
string outputFilePath = Path.Combine(OutputDir, "psdnet256.psd_output.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Code für nachfolgende Schritte finden Sie hier...
}
```

## Schritt 2: Greifen Sie auf die Ebenenüberblendungsoptionen zu

```csharp
BlendingOptions layerBlendOptions = psdImage.Layers[1].BlendingOptions;
```

## Schritt 3: Finden oder erstellen Sie einen Verlaufsüberlagerungseffekt

```csharp
GradientOverlayEffect gradientOverlayEffect = null;

foreach (ILayerEffect effect in layerBlendOptions.Effects)
{
    gradientOverlayEffect = effect as GradientOverlayEffect;
    if (gradientOverlayEffect != null)
    {
        break;
    }
}

if (gradientOverlayEffect == null)
{
    gradientOverlayEffect = layerBlendOptions.AddGradientOverlay();
}
```

## Schritt 4: Konfigurieren Sie den Verlaufsüberlagerungseffekt

```csharp
gradientOverlayEffect.Opacity = 200;
gradientOverlayEffect.BlendMode = BlendMode.Hue;

GradientFillSettings settings = gradientOverlayEffect.Settings;

settings.ColorPoints = new IGradientColorPoint[]
{
    new GradientColorPoint(Color.GreenYellow, 0, 50),
    new GradientColorPoint(Color.BlueViolet, 4096, 50),
};

settings.Angle = 80;
settings.Scale = 150;
settings.GradientType = GradientType.Linear;

settings.TransparencyPoints[0].Opacity = 100;
settings.TransparencyPoints[1].Opacity = 100;
```

## Schritt 5: Speichern Sie das geänderte Bild

```csharp
psdImage.Save(outputFilePath);
```

Das ist es! Sie haben mit Aspose.PSD für .NET erfolgreich einen Verlaufsüberlagerungseffekt zu einer Ebene hinzugefügt.

## Abschluss

In diesem Tutorial haben wir den Prozess der Unterstützung des Verlaufsüberlagerungseffekts in Aspose.PSD für .NET untersucht. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie diese Funktion nahtlos in Ihre .NET-Anwendungen integrieren und so die visuelle Attraktivität Ihrer Bilder verbessern.

## FAQs

### F1: Ist Aspose.PSD mit allen Versionen von .NET kompatibel?

A1: Aspose.PSD für .NET ist mit .NET Framework und .NET Core kompatibel.

### F2: Kann ich mehrere Effekte auf eine einzelne Ebene anwenden?

A2: Ja, Sie können verschiedene Effekte, einschließlich Verlaufsüberlagerung, auf eine einzelne Ebene anwenden.

### F3: Wo finde ich weitere Beispiele und Dokumentation?

 A3: Besuchen Sie die[Dokumentation](https://reference.aspose.com/psd/net/) Ausführliche Beispiele und Richtlinien finden Sie hier.

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F5: Wie erhalte ich Unterstützung für Aspose.PSD?

 A5: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für die Unterstützung der Gemeinschaft.