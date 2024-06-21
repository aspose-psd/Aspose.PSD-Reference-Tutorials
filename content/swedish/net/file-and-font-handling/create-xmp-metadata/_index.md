---
title: Skapa XMP-metadata i Aspose.PSD för .NET
linktitle: Skapar XMP-metadata
second_title: Aspose.PSD .NET API
description: Utforska XMP-metadataskapande i Aspose.PSD för .NET. Förbättra bildorganisationen med sömlös manipulation.
type: docs
weight: 10
url: /sv/net/file-and-font-handling/create-xmp-metadata/
---
## Introduktion

den dynamiska världen av .NET-utveckling är manipulering av bilder med precision en avgörande aspekt av många applikationer. Denna handledning utforskar skapandet av XMP-metadata i Aspose.PSD för .NET, ett kraftfullt bibliotek som förenklar bildbehandlingsuppgifter. XMP (Extensible Metadata Platform) gör att du kan bädda in metadata i bildfiler, vilket underlättar effektiv organisation och hämtning av information som är kopplad till bilder.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD för .NET Library: Ladda ner och installera biblioteket från[Aspose.PSD-dokumentation](https://reference.aspose.com/psd/net/).

- Utvecklingsmiljö: Konfigurera en .NET-utvecklingsmiljö med Visual Studio eller din föredragna IDE.

- Grundläggande .NET-kunskap: Bekanta dig med grundläggande .NET-koncept, eftersom denna handledning förutsätter en grundläggande förståelse för .NET-utveckling.

## Importera namnområden

I ditt .NET-projekt, inkludera de nödvändiga namnområdena för att få tillgång till Aspose.PSD-funktionalitet:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

Låt oss nu dela upp processen för att skapa XMP-metadata i en serie omfattande steg.

## Steg 1: Ange bildstorlek och rektangel

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//Ange storleken på bilden genom att definiera en rektangel
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Steg 2: Skapa en ny bild

```csharp
// Skapa den helt nya bilden för exempeländamål
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // Bildmanipuleringskoden går här...
}
```

## Steg 3: Skapa XMP-Header och XMP-Trailer

```csharp
// Skapa en instans av XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Skapa en instans av XMP-TrailerPi, XMPmeta-klassen för att ställa in olika attribut
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## Steg 4: Ställ in XMP-attribut

```csharp
// Ställ in XMP-attribut, till exempel:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Steg 5: Skapa XMP Packet Wrapper

```csharp
// Skapa en instans av XmpPacketWrapper som innehåller all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Steg 6: Skapa Photoshop-paket och ställ in attribut

```csharp
// Skapa en instans av Photoshop-paketet och ställ in Photoshop-attribut
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## Steg 7: Lägg till Photoshop-paketet till XMP-metadata

```csharp
// Lägg till Photoshop-paket i XMP-metadata
xmpData.AddPackage(photoshopPackage);
```

## Steg 8: Skapa DublinCore-paket och ställ in attribut

```csharp
// Skapa en instans av DublinCore-paketet och ställ in dublinCore-attribut
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Steg 9: Lägg till DublinCore-paketet till XMP-metadata

```csharp
// Lägg till dublinCore Package i XMP-metadata
xmpData.AddPackage(dublinCorePackage);
```

## Steg 10: Uppdatera XMP-metadata och spara bild

```csharp
using (var ms = new MemoryStream())
{
    // Uppdatera XMP-metadata till bilden och spara bilden på disken eller i en minnesström
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## Steg 11: Ladda bild och läs metadata

```csharp
// Ladda bilden från minnesströmmen eller från disken för att läsa/hämta metadata
using (var img = (PsdImage)Image.Load(ms))
{
    // Hämta XMP-metadata
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // Använd paketdata...
    }
}
```

## Slutsats

Grattis! Du har framgångsrikt skapat XMP-metadata i Aspose.PSD för .NET. Denna kraftfulla förmåga förbättrar din bildbehandlingskapacitet, vilket möjliggör effektiv organisation och hämtning av viktig information.

## FAQ's

### F1: Är Aspose.PSD för .NET kompatibelt med alla bildformat?

S1: Aspose.PSD fokuserar främst på PSD (Adobe Photoshop) filformat men stöder olika andra format.

### F2: Kan jag manipulera befintlig XMP-metadata med Aspose.PSD för .NET?

S2: Ja, Aspose.PSD låter dig både läsa och ändra befintlig XMP-metadata.

### F3: Finns det några begränsningar för bildstorlek när du använder Aspose.PSD för .NET?

S3: Aspose.PSD kan hantera bilder av varierande storlek, men extremt stora bilder kan kräva ytterligare överväganden.

### F4: Hur ofta uppdateras Aspose.PSD för .NET?

S4: Uppdateringar släpps regelbundet för att säkerställa kompatibilitet med de senaste .NET framework-versionerna och industristandarderna.

### F5: Finns det ett communityforum för Aspose.PSD-support?

 A: Ja, du kan hitta stöd och diskussioner om[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).