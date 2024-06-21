---
title: Ändra storlek på bilder proportionellt i Aspose.PSD för .NET
linktitle: Ändra storlek på bilder proportionellt
second_title: Aspose.PSD .NET API
description: Utforska sömlös bildstorleksändring med Aspose.PSD för .NET. Ladda ner biblioteket, följ vår handledning och förbättra dina bildbehandlingsmöjligheter.
type: docs
weight: 14
url: /sv/net/image-manipulation/resize-images-proportionally/
---
När det gäller bildmanipulation framstår Aspose.PSD för .NET som en kraftfull verktygslåda, som ger utvecklare möjlighet att ändra storlek på bilder proportionellt med lätthet. I den här steg-för-steg-guiden går vi igenom processen att ändra storlek på bilder med Aspose.PSD för .NET, vilket säkerställer att dina bilder bibehåller sina proportioner felfritt.

## Introduktion

Att ändra storlek på bilder proportionellt är en vanlig uppgift i många applikationer, och Aspose.PSD för .NET förenklar denna process för utvecklare. Oavsett om du arbetar med en webbapplikation, datorprogramvara eller mobilapp är det avgörande att förstå hur man ändrar storlek på bilder samtidigt som deras bildförhållande bevaras för att bibehålla visuell tilltalande och konsekvens.

## Förutsättningar

Innan du dyker in i storleksändringsmagin med Aspose.PSD för .NET, se till att du har följande förutsättningar på plats:

1.  Aspose.PSD for .NET Library: Se till att du har Aspose.PSD for .NET-biblioteket installerat. Du kan ladda ner den från[Aspose.PSD för .NET-utgåvor](https://releases.aspose.com/psd/net/) sida.

2. Dokumentkatalog: Skapa en katalog för att lagra dina dokument och ersätt "Din dokumentkatalog" i den medföljande koden med den faktiska sökvägen till denna katalog.

Nu när du har ställt in förutsättningarna, låt oss hoppa in i steg-för-steg-guiden.

## Importera namnområden

```csharp
using Aspose.PSD.ImageOptions;
```

Importera nödvändiga namnområden för att komma åt de klasser och metoder som krävs.

## Steg 1: Ladda bilden

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Ladda en befintlig bild i en instans av RasterImage-klassen
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Resten av stegen går här
}
```

 Ladda källbilden med hjälp av`Image.Load` metod.

## Steg 2: Ange bredd och höjd

```csharp
// Ange bredd och höjd
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Bestäm den nya bredden och höjden för den ändrade storleken på bilden. I det här exemplet halveras bredden och höjden, men du kan justera dessa värden baserat på dina krav.

## Steg 3: Spara den ändrade storleken på bilden

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Spara den ändrade storleken på bilden med hjälp av`Save` metod med specificerade alternativ. I det här fallet sparar vi den som en PNG-fil.

## Slutsats

Ändra storlek på bilder proportionellt i Aspose.PSD för .NET är en enkel process som tillför värde till ditt arbetsflöde för bildbehandling. Den här guiden har utrustat dig med kunskapen för att sömlöst integrera denna funktionalitet i dina applikationer.

## FAQ's

### F1: Kan jag ändra storlek på bilder till specifika mått?

A1: Ja, du kan anpassa den nya bredden och höjden enligt dina krav i koden.

### F2: Är Aspose.PSD för .NET lämplig för batch-bildstorleksändring?

A2: Absolut! Du kan infoga dessa steg i en loop för batchbearbetning av flera bilder.

### F3: Finns det andra bildmanipuleringsfunktioner i Aspose.PSD för .NET?

S3: Ja, Aspose.PSD för .NET erbjuder ett brett utbud av funktioner, inklusive beskärning, rotering och applicering av filter på bilder.

### F4: Finns det en gratis testversion tillgänglig för Aspose.PSD för .NET?

 S4: Ja, du kan utforska funktionerna hos Aspose.PSD för .NET med en gratis provperiod. Besök[här](https://releases.aspose.com/) för att starta.

### F5: Var kan jag hitta support för Aspose.PSD för .NET?

 A5: Besök[Aspose.PSD för .NET-forum](https://forum.aspose.com/c/psd/34) för samhällsstöd och diskussioner.