---
title: Drehen eines Bildes in Aspose.PSD für .NET
linktitle: Drehen eines Bildes
second_title: Aspose.PSD .NET API
description: Lernen Sie, Bilder mit Aspose.PSD mühelos in .NET zu drehen. Folgen Sie unserem Schritt-für-Schritt-Tutorial.
type: docs
weight: 15
url: /de/net/image-manipulation/rotate-image/
---
## Einführung

Wenn Sie in die Welt der Bildbearbeitung mit .NET eintauchen, ist Aspose.PSD Ihr bevorzugtes Tool für eine nahtlose und effiziente Bildverarbeitung. In diesem Tutorial konzentrieren wir uns auf eine grundlegende Aufgabe – das Drehen eines Bildes mit Aspose.PSD für .NET. Folgen Sie uns, während wir den Prozess in einfache, umsetzbare Schritte aufteilen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek herunter und installieren Sie sie von der[Aspose.PSD .NET-Dokumentation](https://reference.aspose.com/psd/net/).

- Ihr Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre Bilder gespeichert werden. Ersetzen Sie im Codeausschnitt „Ihr Dokumentverzeichnis“ durch den Pfad zu diesem Verzeichnis.

## Namespaces importieren

Stellen Sie sicher, dass Sie die erforderlichen Namespaces einschließen, um auf die Aspose.PSD-Funktionalität zuzugreifen. Fügen Sie am Anfang Ihres .NET-Projekts die folgenden Zeilen hinzu:

```csharp
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Laden Sie das Bild

```csharp
string sourceFile = dataDir + @"sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
using (Image image = Image.Load(sourceFile))
{
```

## Schritt 2: Bild drehen

```csharp
    // Drehen Sie das Bild um 270 Grad im Uhrzeigersinn
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Schritt 3: Speichern Sie das gedrehte Bild

```csharp
    // Speichern Sie das gedrehte Bild als JPEG-Datei
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Das ist es! Mit nur wenigen Codezeilen haben Sie ein Bild erfolgreich mit Aspose.PSD für .NET gedreht.

## Abschluss

In diesem Tutorial haben wir die Grundlagen der Bildrotation mit Aspose.PSD für .NET erkundet. Aspose.PSD bietet einen robusten Satz von Tools zur Bildbearbeitung und ist damit eine unverzichtbare Bibliothek für .NET-Entwickler. Experimentieren Sie mit verschiedenen Rotationen und erkunden Sie weitere Möglichkeiten zur Verbesserung Ihrer Bildverarbeitungs-Workflows.

## Häufig gestellte Fragen

### F1: Kann ich Bilder mit Aspose.PSD um einen benutzerdefinierten Winkel drehen?

 Ja, Aspose.PSD ermöglicht Ihnen, einen benutzerdefinierten Winkel für die Drehung anzugeben. Ersetzen Sie einfach die`RotateFlipType.Rotate270FlipNone` Linie mit dem gewünschten Drehwinkel.

### F2: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?

 Absolut. Aspose.PSD unterstützt eine Vielzahl von Bildformaten, darunter PSD, JPEG, PNG und mehr. Überprüfen Sie die[Dokumentation](https://reference.aspose.com/psd/net/) für die vollständige Liste.

### F3: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 Besuchen Sie die[Seite mit der temporären Lizenz](https://purchase.aspose.com/temporary-license/) auf der Aspose-Website, um eine temporäre Lizenz zu Evaluierungszwecken zu erhalten.

### F4: Wo finde ich Unterstützung für Aspose.PSD?

 Bei Fragen oder für Hilfe besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) und sich mit der Community zu verbinden.

### F5: Kann ich Aspose.PSD für die kommerzielle Nutzung kaufen?

 Sicherlich. Entdecken Sie die[Kaufseite](https://purchase.aspose.com/buy) um eine auf Ihre Bedürfnisse zugeschnittene Lizenz zu erwerben.