---
title: Erstellen von XMP-Metadaten in Aspose.PSD für .NET
linktitle: Erstellen von XMP-Metadaten
second_title: Aspose.PSD .NET-API
description: Entdecken Sie die Erstellung von XMP-Metadaten in Aspose.PSD für .NET. Verbessern Sie die Bildorganisation durch nahtlose Bearbeitung.
type: docs
weight: 10
url: /de/net/file-and-font-handling/create-xmp-metadata/
---
## Einführung

In der dynamischen Welt der .NET-Entwicklung ist die präzise Bearbeitung von Bildern ein entscheidender Aspekt vieler Anwendungen. In diesem Tutorial wird die Erstellung von XMP-Metadaten in Aspose.PSD für .NET erläutert, einer leistungsstarken Bibliothek, die Bildverarbeitungsaufgaben vereinfacht. Mit XMP (Extensible Metadata Platform) können Sie Metadaten in Bilddateien einbetten und so die effiziente Organisation und den Abruf von mit Bildern verbundenen Informationen erleichtern.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Aspose.PSD-Dokumentation](https://reference.aspose.com/psd/net/).

- Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung mit Visual Studio oder Ihrer bevorzugten IDE ein.

- Grundlegende .NET-Kenntnisse: Machen Sie sich mit grundlegenden .NET-Konzepten vertraut, da dieses Tutorial ein grundlegendes Verständnis der .NET-Entwicklung voraussetzt.

## Namespaces importieren

Fügen Sie in Ihr .NET-Projekt die erforderlichen Namespaces ein, um auf die Aspose.PSD-Funktionalität zuzugreifen:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

Lassen Sie uns nun den Prozess der Erstellung von XMP-Metadaten in eine Reihe umfassender Schritte unterteilen.

## Schritt 1: Geben Sie Bildgröße und Rechteck an

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

// Geben Sie die Größe des Bildes an, indem Sie ein Rechteck definieren
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Schritt 2: Erstellen Sie ein neues Bild

```csharp
// Erstellen Sie das brandneue Bild zu Beispielzwecken
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // Bildmanipulationscode kommt hierher...
}
```

## Schritt 3: XMP-Header und XMP-Trailer erstellen

```csharp
// Erstellen Sie eine Instanz von XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Erstellen Sie eine Instanz der XMP-TrailerPi-Klasse XMPmeta, um verschiedene Attribute festzulegen
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## Schritt 4: XMP-Attribute festlegen

```csharp
// Legen Sie XMP-Attribute fest, zum Beispiel:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Schritt 5: Erstellen Sie einen XMP-Paket-Wrapper

```csharp
// Erstellen Sie eine Instanz von XmpPacketWrapper, die alle Metadaten enthält
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Schritt 6: Photoshop-Paket erstellen und Attribute festlegen

```csharp
// Erstellen Sie eine Instanz des Photoshop-Pakets und legen Sie Photoshop-Attribute fest
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## Schritt 7: Photoshop-Paket zu XMP-Metadaten hinzufügen

```csharp
// Fügen Sie das Photoshop-Paket zu den XMP-Metadaten hinzu
xmpData.AddPackage(photoshopPackage);
```

## Schritt 8: DublinCore-Paket erstellen und Attribute festlegen

```csharp
// Erstellen Sie eine Instanz des DublinCore-Pakets und legen Sie dublinCore-Attribute fest
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Schritt 9: DublinCore-Paket zu den XMP-Metadaten hinzufügen

```csharp
// Fügen Sie das DublinCore-Paket zu den XMP-Metadaten hinzu
xmpData.AddPackage(dublinCorePackage);
```

## Schritt 10: XMP-Metadaten aktualisieren und Bild speichern

```csharp
using (var ms = new MemoryStream())
{
    // Aktualisieren Sie die XMP-Metadaten im Bild und speichern Sie das Bild auf der Festplatte oder in einem Speicherstream
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## Schritt 11: Bild laden und Metadaten lesen

```csharp
// Laden Sie das Bild aus dem Speicherstream oder von der Festplatte, um die Metadaten zu lesen/abzurufen
using (var img = (PsdImage)Image.Load(ms))
{
    // Abrufen der XMP-Metadaten
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // Paketdaten verwenden...
    }
}
```

## Abschluss

Glückwunsch! Sie haben erfolgreich XMP-Metadaten in Aspose.PSD für .NET erstellt. Diese leistungsstarke Funktion erweitert Ihre Bildverarbeitungsfähigkeiten und ermöglicht eine effiziente Organisation und den Abruf wichtiger Informationen.

## FAQs

### F1: Ist Aspose.PSD für .NET mit allen Bildformaten kompatibel?

A1: Aspose.PSD konzentriert sich hauptsächlich auf das PSD-Dateiformat (Adobe Photoshop), unterstützt jedoch verschiedene andere Formate.

### F2: Kann ich vorhandene XMP-Metadaten mit Aspose.PSD für .NET bearbeiten?

A2: Ja, mit Aspose.PSD können Sie vorhandene XMP-Metadaten sowohl lesen als auch ändern.

### F3: Gibt es Einschränkungen hinsichtlich der Bildgröße bei der Verwendung von Aspose.PSD für .NET?

A3: Aspose.PSD kann Bilder unterschiedlicher Größe verarbeiten, aber extrem große Bilder erfordern möglicherweise zusätzliche Überlegungen.

### F4: Wie oft wird Aspose.PSD für .NET aktualisiert?

A4: Es werden regelmäßig Updates veröffentlicht, um die Kompatibilität mit den neuesten .NET Framework-Versionen und Industriestandards sicherzustellen.

### F5: Gibt es ein Community-Forum für Aspose.PSD-Unterstützung?

 A: Ja, Sie können Unterstützung und Diskussionen auf der finden[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).