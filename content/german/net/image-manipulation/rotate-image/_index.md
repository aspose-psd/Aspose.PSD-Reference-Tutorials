---
title: Drehen eines Bildes in Aspose.PSD für .NET
linktitle: Ein Bild drehen
second_title: Aspose.PSD .NET-API
description: Erfahren Sie, wie Sie mit Aspose.PSD Bilder mühelos in .NET drehen. Folgen Sie unserer Schritt-für-Schritt-Anleitung.
type: docs
weight: 15
url: /de/net/image-manipulation/rotate-image/
---
## Einführung

Wenn Sie in die Welt der Bildbearbeitung mit .NET eintauchen, ist Aspose.PSD Ihr Werkzeug der Wahl für eine nahtlose und effiziente Bildverarbeitung. In diesem Tutorial konzentrieren wir uns auf eine grundlegende Aufgabe – das Drehen eines Bildes mit Aspose.PSD für .NET. Folgen Sie uns, während wir den Prozess in einfache, umsetzbare Schritte unterteilen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Aspose.PSD .NET-Dokumentation](https://reference.aspose.com/psd/net/).

- Ihr Dokumentenverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre Bilder gespeichert werden. Ersetzen Sie „Ihr Dokumentverzeichnis“ im Codeausschnitt durch den Pfad zu diesem Verzeichnis.

## Namespaces importieren

Stellen Sie sicher, dass Sie die erforderlichen Namespaces für den Zugriff auf die Aspose.PSD-Funktionalität angeben. Fügen Sie am Anfang Ihres .NET-Projekts die folgenden Zeilen hinzu:

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

## Schritt 2: Drehen Sie das Bild

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

Das ist es! Mit nur wenigen Codezeilen haben Sie ein Bild mit Aspose.PSD für .NET erfolgreich gedreht.

## Abschluss

In diesem Tutorial haben wir die Grundlagen des Drehens von Bildern mit Aspose.PSD für .NET erkundet. Aspose.PSD bietet einen robusten Satz an Tools zur Bildbearbeitung und ist damit eine unverzichtbare Bibliothek für .NET-Entwickler. Experimentieren Sie mit verschiedenen Rotationen und entdecken Sie weitere Möglichkeiten, um Ihre Bildverarbeitungs-Workflows zu verbessern.

## FAQs

### F1: Kann ich Bilder mit Aspose.PSD um einen benutzerdefinierten Winkel drehen?

 Ja, mit Aspose.PSD können Sie einen benutzerdefinierten Winkel für die Drehung angeben. Ersetzen Sie einfach die`RotateFlipType.Rotate270FlipNone` Linie mit Ihrem gewünschten Drehwinkel.

### F2: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?

 Absolut. Aspose.PSD unterstützt eine Vielzahl von Bildformaten, darunter PSD, JPEG, PNG und mehr. Überprüf den[Dokumentation](https://reference.aspose.com/psd/net/) für die vollständige Liste.

### F3: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 Besuche den[temporäre Lizenzseite](https://purchase.aspose.com/temporary-license/) auf der Aspose-Website, um eine temporäre Lizenz zu Evaluierungszwecken zu erhalten.

### F4: Wo finde ich Unterstützung für Aspose.PSD?

 Bei Fragen oder Hilfe besuchen Sie bitte die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) und mit der Community in Kontakt treten.

### F5: Kann ich Aspose.PSD für die kommerzielle Nutzung erwerben?

 Sicherlich. Entdecke die[Kaufseite](https://purchase.aspose.com/buy) um eine auf Ihre Bedürfnisse zugeschnittene Lizenz zu erwerben.