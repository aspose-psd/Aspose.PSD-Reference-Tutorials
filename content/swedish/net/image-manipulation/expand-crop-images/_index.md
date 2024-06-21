---
title: Expandera och beskära bilder i Aspose.PSD för .NET
linktitle: Expandera och beskära bilder
second_title: Aspose.PSD .NET API
description: Lär dig hur du dynamiskt expanderar och beskär bilder med Aspose.PSD för .NET. Följ vår steg-för-steg-guide för sömlös bildmanipulation.
type: docs
weight: 13
url: /sv/net/image-manipulation/expand-crop-images/
---
## Introduktion

Aspose.PSD för .NET är ett omfattande bildbibliotek som låter utvecklare arbeta med olika bildformat i sina .NET-applikationer. En av dess utmärkande egenskaper är förmågan att manipulera bilder med lätthet. I den här handledningen kommer vi att fokusera på att expandera och beskära bilder, vilket ger dig en praktisk guide för att utföra dessa uppgifter med Aspose.PSD.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD for .NET Library: Se till att du har Aspose.PSD for .NET-biblioteket installerat. Du kan ladda ner den från[Aspose.PSD för .NET-dokumentation](https://reference.aspose.com/psd/net/).

- Exempelbild: Förbered en exempelbildfil (t.ex. "example1.psd") som du ska använda för handledningen.

Låt oss nu komma igång med steg-för-steg-guiden.

## Importera namnområden

Börja med att importera de nödvändiga namnområdena för att utnyttja funktionerna som tillhandahålls av Aspose.PSD för .NET. Lägg till följande namnrymder i din kod:

```csharp
using Aspose.PSD.ImageOptions;
```

## Steg 1: Konfigurera projektet

 Se till att du har ett projekt inrättat med Aspose.PSD för .NET integrerat. Om inte, följ[dokumentation](https://reference.aspose.com/psd/net/) för vägledning.

## Steg 2: Ladda bilden

Ladda provbilden med följande kod:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Ladda bilden
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Ytterligare kod för bildbehandling kommer här
}
```

## Steg 3: Cachelagra bilddata

Cachelagra bilddata för att optimera prestanda:

```csharp
rasterImage.CacheData();
```

## Steg 4: Definiera destinationsrektangel

Skapa en instans av klassen Rectangle och definiera X, Y, bredd och höjd för rektangeln. Detta kommer att vara det område till vilket bilden kommer att expanderas eller beskäras.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Steg 5: Spara utdatabilden

Spara utdatabilden med de angivna alternativen och destinationsrektangeln:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig att utöka och beskära bilder med Aspose.PSD för .NET. Detta kraftfulla bibliotek öppnar upp en värld av möjligheter för bildmanipulation i dina .NET-applikationer.

## FAQ's

### F1: Kan Aspose.PSD hantera andra bildformat förutom PSD?

S1: Ja, Aspose.PSD stöder ett brett utbud av bildformat, inklusive JPEG, PNG, GIF och mer.

### F2: Var kan jag hitta support för Aspose.PSD?

 S2: Du kan hitta stöd och engagera dig i samhället på[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).

### F3 Finns det en gratis testversion tillgänglig för Aspose.PSD för .NET?

 S3: Ja, du kan utforska funktionerna med en gratis provperiod tillgänglig på[Aspose.PSD gratis provperiod](https://releases.aspose.com/).

### F4: Hur får jag en tillfällig licens för Aspose.PSD?

 A4: Du kan få en tillfällig licens från[Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag köpa Aspose.PSD för .NET?

 A5: Du kan köpa biblioteket på[Aspose.PSD köpsida](https://purchase.aspose.com/buy).