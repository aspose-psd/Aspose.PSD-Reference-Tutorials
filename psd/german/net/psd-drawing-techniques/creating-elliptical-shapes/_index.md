---
title: Erstellen elliptischer Formen mit Aspose.PSD für .NET
linktitle: Erstellen elliptischer Formen mit Aspose.PSD für .NET
second_title: Aspose.PSD .NET API
description: Erfahren Sie, wie Sie mit Aspose.PSD elliptische Formen in .NET zeichnen. Schritt-für-Schritt-Anleitung mit Codebeispielen. Erstellen Sie mühelos atemberaubende Grafiken.
weight: 13
url: /de/net/psd-drawing-techniques/creating-elliptical-shapes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen elliptischer Formen mit Aspose.PSD für .NET

## Einführung

Willkommen zu unserem umfassenden Leitfaden zum Erstellen elliptischer Formen mit Aspose.PSD für .NET. Aspose.PSD ist eine leistungsstarke .NET-Bibliothek, mit der Entwickler Photoshop-Dateien bearbeiten und konvertieren können, ohne Adobe Photoshop zu benötigen. In diesem Tutorial führen wir Sie durch den Prozess des Zeichnens elliptischer Formen mithilfe der Bibliothek.

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass die Aspose.PSD-Bibliothek in Ihrem .NET-Projekt installiert ist. Sie können sie von der[Aspose.PSD für .NET-Dokumentation](https://reference.aspose.com/psd/net/).

- .NET-Umgebung: Dieses Tutorial setzt voraus, dass Sie über praktische Kenntnisse des .NET-Frameworks verfügen.

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces in Ihr Projekt. Dadurch wird sichergestellt, dass Sie Zugriff auf die Klassen und Methoden haben, die zum Zeichnen elliptischer Formen erforderlich sind. Hier ist ein Beispiel:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Lassen Sie uns nun den Vorgang zum Erstellen elliptischer Formen in mehrere Schritte unterteilen:

## Schritt 1: Einrichten des Dokumentverzeichnisses

```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";
```

## Schritt 2: Erstellen Sie eine Instanz von BmpOptions

```csharp
// Erstellen Sie eine Instanz von BmpOptions und legen Sie deren verschiedene Eigenschaften fest
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Schritt 3: Erstellen Sie eine Image-Instanz

```csharp
// Erstellen Sie eine Instanz von Image
using (Image image = new PsdImage(100, 100))
{
    // Erstellen und initialisieren Sie eine Instanz der Graphics-Klasse und der Clear Graphics-Oberfläche
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Schritt 4: Zeichnen Sie eine gepunktete Ellipsenform

```csharp
    // Zeichnen Sie eine gepunktete Ellipsenform, indem Sie das Stiftobjekt mit roter Farbe und einem umgebenden Rechteck angeben
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Schritt 5: Zeichnen Sie eine durchgehende Ellipsenform

```csharp
    //Zeichnen Sie eine kontinuierliche Ellipsenform, indem Sie das Stiftobjekt mit einem festen Pinsel in blauer Farbe und einem umgebenden Rechteck angeben
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Bild in das BMP-Dateiformat exportieren.
    image.Save(outpath, saveOptions);
}
```

## Abschluss

Herzlichen Glückwunsch! Sie haben erfolgreich elliptische Formen mit Aspose.PSD für .NET erstellt. Dieses Tutorial behandelte die wesentlichen Schritte, vom Einrichten der Umgebung bis zum Zeichnen sowohl gepunkteter als auch durchgehender Ellipsenformen.

## Häufig gestellte Fragen

### F1: Wo finde ich die Dokumentation für Aspose.PSD für .NET?

 A1: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/psd/net/).

### F2: Wie lade ich Aspose.PSD für .NET herunter?

 A2: Sie können es von der Release-Seite herunterladen[Hier](https://releases.aspose.com/psd/net/).

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wie kann ich Support für Aspose.PSD für .NET erhalten?

 A4: Besuchen Sie das Support-Forum[Hier](https://forum.aspose.com/c/psd/34).

### F5: Benötige ich zum Testen eine vorübergehende Lizenz?

 A5: Ja, Sie können eine vorübergehende Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
