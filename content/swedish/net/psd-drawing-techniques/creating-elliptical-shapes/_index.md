---
title: Skapa elliptiska former med Aspose.PSD för .NET
linktitle: Skapa elliptiska former med Aspose.PSD för .NET
second_title: Aspose.PSD .NET API
description: Lär dig hur du ritar elliptiska former i .NET med Aspose.PSD. Steg-för-steg guide med kodexempel. Skapa fantastisk grafik utan ansträngning.
type: docs
weight: 13
url: /sv/net/psd-drawing-techniques/creating-elliptical-shapes/
---
## Introduktion

Välkommen till vår omfattande guide för att skapa elliptiska former med Aspose.PSD för .NET. Aspose.PSD är ett kraftfullt .NET-bibliotek som tillåter utvecklare att manipulera och konvertera Photoshop-filer utan att behöva Adobe Photoshop. I den här handledningen går vi igenom processen att rita elliptiska former med hjälp av biblioteket.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD för .NET-bibliotek: Se till att du har Aspose.PSD-biblioteket installerat i ditt .NET-projekt. Du kan ladda ner den från[Aspose.PSD för .NET-dokumentation](https://reference.aspose.com/psd/net/).

- .NET-miljö: Denna handledning förutsätter att du har praktiska kunskaper om .NET-ramverket.

## Importera namnområden

För att komma igång, importera de nödvändiga namnområdena till ditt projekt. Detta säkerställer att du har tillgång till de klasser och metoder som krävs för att rita elliptiska former. Här är ett exempel:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Låt oss nu dela upp processen att skapa elliptiska former i flera steg:

## Steg 1: Konfigurera dokumentkatalogen

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";
```

## Steg 2: Skapa en instans av BmpOptions

```csharp
// Skapa en instans av BmpOptions och ställ in dess olika egenskaper
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Steg 3: Skapa en instans av bild

```csharp
// Skapa en instans av bild
using (Image image = new PsdImage(100, 100))
{
    // Skapa och initiera en instans av Graphics class och Clear Graphics yta
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Steg 4: Rita en prickad ellipsform

```csharp
    // Rita en prickad ellipsform genom att ange att Pen-objektet har röd färg och en omgivande rektangel
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Steg 5: Rita en kontinuerlig ellipsform

```csharp
    // Rita en kontinuerlig ellipsform genom att ange att Pen-objektet har en solid pensel med blå färg och en omgivande rektangel
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Exportera bild till bmp-filformat.
    image.Save(outpath, saveOptions);
}
```

## Slutsats

Grattis! Du har framgångsrikt skapat elliptiska former med Aspose.PSD för .NET. Denna handledning täckte de väsentliga stegen, från att ställa in miljön till att rita både prickade och kontinuerliga ellipsformer.

## FAQ's

### F1: Var kan jag hitta dokumentationen för Aspose.PSD för .NET?

 S1: Dokumentationen finns tillgänglig[här](https://reference.aspose.com/psd/net/).

### F2: Hur laddar jag ner Aspose.PSD för .NET?

 S2: Du kan ladda ner den från releasesidan[här](https://releases.aspose.com/psd/net/).

### F3: Finns det en gratis provperiod?

 A3: Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/).

### F4: Hur kan jag få support för Aspose.PSD för .NET?

 S4: Besök supportforumet[här](https://forum.aspose.com/c/psd/34).

### F5: Behöver jag en tillfällig licens för att testa?

 A5: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).