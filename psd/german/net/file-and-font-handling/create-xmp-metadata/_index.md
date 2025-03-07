---
title: Erstellen von XMP-Metadaten in Aspose.PSD für .NET
linktitle: Erstellen von XMP-Metadaten
second_title: Aspose.PSD .NET API
description: Entdecken Sie die Erstellung von XMP-Metadaten in Aspose.PSD für .NET. Verbessern Sie die Bildorganisation durch nahtlose Bearbeitung.
weight: 10
url: /de/net/file-and-font-handling/create-xmp-metadata/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen von XMP-Metadaten in Aspose.PSD für .NET

## Einführung

In der dynamischen Welt der .NET-Entwicklung ist die präzise Bildbearbeitung ein entscheidender Aspekt vieler Anwendungen. Dieses Tutorial untersucht die Erstellung von XMP-Metadaten in Aspose.PSD für .NET, einer leistungsstarken Bibliothek, die Bildverarbeitungsaufgaben vereinfacht. XMP (Extensible Metadata Platform) ermöglicht Ihnen das Einbetten von Metadaten in Bilddateien und erleichtert so die effiziente Organisation und Abfrage von mit Bildern verknüpften Informationen.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Laden Sie die Bibliothek herunter und installieren Sie sie von der[Aspose.PSD-Dokumentation](https://reference.aspose.com/psd/net/).

- Entwicklungsumgebung: Richten Sie mit Visual Studio oder Ihrer bevorzugten IDE eine .NET-Entwicklungsumgebung ein.

- Grundlegende .NET-Kenntnisse: Machen Sie sich mit den grundlegenden .NET-Konzepten vertraut, da dieses Tutorial grundlegende Kenntnisse der .NET-Entwicklung voraussetzt.

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

Lassen Sie uns nun den Prozess der Erstellung von XMP-Metadaten in eine Reihe umfassender Schritte aufteilen.

## Schritt 1: Bildgröße und Rechteck festlegen

```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//Geben Sie die Größe des Bildes an, indem Sie ein Rechteck definieren
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Schritt 2: Neues Image erstellen

```csharp
// Erstellen Sie das brandneue Image zu Beispielzwecken
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // Der Bildbearbeitungscode kommt hier hin...
}
```

## Schritt 3: XMP-Header und XMP-Trailer erstellen

```csharp
// Erstellen Sie eine Instanz des XMP-Headers
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Erstellen Sie eine Instanz von XMP-TrailerPi, XMPmeta-Klasse, um verschiedene Attribute festzulegen
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## Schritt 4: XMP-Attribute festlegen

```csharp
// Legen Sie beispielsweise XMP-Attribute fest:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Schritt 5: XMP-Paket-Wrapper erstellen

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
// Photoshop-Paket zu XMP-Metadaten hinzufügen
xmpData.AddPackage(photoshopPackage);
```

## Schritt 8: DublinCore-Paket erstellen und Attribute festlegen

```csharp
// Erstellen Sie eine Instanz des DublinCore-Pakets und legen Sie DublinCore-Attribute fest
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Schritt 9: DublinCore-Paket zu XMP-Metadaten hinzufügen

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

Herzlichen Glückwunsch! Sie haben erfolgreich XMP-Metadaten in Aspose.PSD für .NET erstellt. Diese leistungsstarke Funktion verbessert Ihre Bildverarbeitungsfunktionen und ermöglicht eine effiziente Organisation und Abfrage wichtiger Informationen.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD für .NET mit allen Bildformaten kompatibel?

A1: Aspose.PSD konzentriert sich hauptsächlich auf das PSD-Dateiformat (Adobe Photoshop), unterstützt aber verschiedene andere Formate.

### F2: Kann ich vorhandene XMP-Metadaten mit Aspose.PSD für .NET bearbeiten?

A2: Ja, Aspose.PSD ermöglicht Ihnen, vorhandene XMP-Metadaten zu lesen und zu ändern.

### F3: Gibt es bei der Verwendung von Aspose.PSD für .NET Einschränkungen hinsichtlich der Bildgröße?

A3: Aspose.PSD kann Bilder unterschiedlicher Größe verarbeiten, aber bei extrem großen Bildern sind möglicherweise zusätzliche Überlegungen erforderlich.

### F4: Wie häufig wird Aspose.PSD für .NET aktualisiert?

A4: Um die Kompatibilität mit den neuesten .NET Framework-Versionen und Industriestandards sicherzustellen, werden regelmäßig Updates veröffentlicht.

### F5: Gibt es ein Community-Forum für Aspose.PSD-Support?

 A: Ja, Sie finden Unterstützung und Diskussionen auf der[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
