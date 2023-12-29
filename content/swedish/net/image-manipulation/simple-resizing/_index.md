---
title: Enkel storleksändring av bilder i Aspose.PSD för .NET
linktitle: Enkel storleksändring av bilder
second_title: Aspose.PSD .NET API
description: Master bildstorleksändring med Aspose.PSD för .NET. Effektiv, sömlös och kraftfull. Lyft dina .NET-projekt utan ansträngning.
type: docs
weight: 17
url: /sv/net/image-manipulation/simple-resizing/
---
## Introduktion

den dynamiska sfären av .NET-utveckling är det en vanlig nödvändighet att manipulera bilder. Aspose.PSD för .NET kommer till undsättning med sina kraftfulla funktioner, vilket ger en sömlös upplevelse för bildstorleksändring. I den här handledningen kommer vi att fördjupa oss i den enkla men avgörande processen att ändra storlek på bilder med Aspose.PSD för .NET. Spänn upp dig när vi ger oss ut på en resa för att förbättra dina färdigheter i bildbehandling.

## Förutsättningar

Innan vi dyker in i handledningen, låt oss se till att du har allt inställt för en smidig upplevelse:

## Importera namnområden

Se till att du har importerat de nödvändiga namnområdena för att komma åt funktionerna i Aspose.PSD för .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

Låt oss nu dela upp processen att ändra storlek på bilder i flera steg:

## Steg 1: Ställ in din dokumentkatalog

Börja med att ange sökvägen till din dokumentkatalog:

```csharp
string dataDir = "Your Document Directory";
```

## Steg 2: Ladda bilden

Ladda en befintlig bild i en instans av klassen RasterImage:

```csharp
string sourceFile = dataDir + @"sample.psd";
using (Image image = Image.Load(sourceFile))
{
    // Din kod här
}
```

## Steg 3: Ändra storlek på bilden

 Att ändra storlek på en bild är lika enkelt som att anropa`Resize` metod på bildobjektet:

```csharp
image.Resize(300, 300);
```

## Steg 4: Spara den ändrade storleken på bilden

Spara den ändrade storleken på bilden med önskat format och alternativ. I det här exemplet sparar vi det som en JPEG:

```csharp
string destName = dataDir + @"SimpleResizing_out.jpg";
image.Save(destName, new JpegOptions());
```

Och det är allt! Du har lyckats ändra storlek på en bild med Aspose.PSD för .NET.

## Slutsats

Att bemästra bildstorlek är en grundläggande färdighet i verktygslådan för alla .NET-utvecklare. Med Aspose.PSD för .NET blir processen inte bara effektiv utan också njutbar. Nu, beväpnad med denna kunskap, gå vidare och höj dina bildmanipuleringsmöjligheter i dina .NET-projekt.

## FAQ's

### F1: Kan jag ändra storlek på bilder till ett specifikt bildförhållande med Aspose.PSD för .NET?

S1: Ja, du kan bibehålla ett specifikt bildförhållande medan du ändrar storlek på bilder genom att justera antingen bredden eller höjden därefter.

### F2: Stöder Aspose.PSD för .NET andra bildformat än JPEG?

A2: Absolut! Aspose.PSD för .NET stöder en mängd olika bildformat, inklusive PNG, GIF, BMP och mer.

### F3: Finns en tillfällig licens tillgänglig för Aspose.PSD för .NET?

S3: Ja, du kan få en tillfällig licens för Aspose.PSD för .NET för att utvärdera dess kapacitet innan du gör ett köp.

### F4: Var kan jag hitta omfattande dokumentation för Aspose.PSD för .NET?

 S4: Utforska den detaljerade dokumentationen på[Aspose.PSD för .NET-dokumentation](https://reference.aspose.com/psd/net/).

### F5: Hur kan jag få support eller få kontakt med communityn för Aspose.PSD för .NET?

 A5: Besök[Aspose.PSD för .NET Forum](https://forum.aspose.com/c/psd/34) för samhällsstöd och diskussioner.