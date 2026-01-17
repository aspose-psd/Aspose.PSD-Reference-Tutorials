---
date: 2026-01-17
description: Leer hoe je een streeppatroon toevoegt in Java met Aspose.PSD voor Java.
  Volg deze stap‑voor‑stap gids om je PSD‑afbeeldingen snel te verbeteren.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Hoe een streeppatroon toe te voegen in Java met Aspose.PSD
url: /nl/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe Stroke Pattern Java Toevoegen met Aspose.PSD

## Introductie
Als je **add stroke pattern java** moet toevoegen aan een Photoshop‑bestand, maakt Aspose.PSD for Java het verrassend eenvoudig. Of je nu een grafisch‑ontwerptool bouwt, batch‑bewerkingen automatiseert, of gewoon experimenteert met laageffecten, deze tutorial leidt je door elke stap — van het laden van de PSD tot het verifiëren van het nieuwe patroon. Laten we beginnen en zien hoe snel je je afbeeldingen kunt verbeteren.

## Snelle Antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.PSD for Java  
- **Welke Java‑versie wordt ondersteund?** JDK 8 of later  
- **Heb ik een licentie nodig voor testen?** Een gratis proefversie werkt voor ontwikkeling; een licentie is vereist voor productie  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basis patroon‑stroke  
- **Kan ik het patroon hergebruiken op meerdere lagen?** Ja, wijs gewoon dezelfde `PattResource` toe aan andere lagen  

## Wat is add stroke pattern java?
Een stroke‑patroon toevoegen in Java betekent het toepassen van een aangepaste vulling (vaak een herhalende bitmap) op het stroke‑effect van een laag. Deze techniek stelt je in staat gestileerde contouren te maken — denk aan een gestippelde lijn, een baksteenstructuur of een aangepaste grafische rand — direct binnen een PSD‑bestand zonder Photoshop te openen.

## Waarom Aspose.PSD gebruiken voor add stroke pattern java?
- **Volledige PSD‑rouwheid** – Alle laageffecten, resources en mengmodi blijven behouden.  
- **Geen native Photoshop vereist** – Werkt op elk OS met een JDK.  
- **Programmatic control** – Automatiseer batchverwerking of integreer in server‑side services.  
- **Rijke API** – Toegang tot globale resources, patroonvullingen en mengmodi in één vloeiende interface.

## Voorvereisten
- **Java Development Kit (JDK)** – ervoor dat JDK 8 of nieuwer is geïnstalleerd.  
- **Aspose.PSD for Java** – Download de bibliotheek van [here](https://releases.aspose.com/psd/java/) en voeg de JAR toe aan de classpath van je project.  
- **IDE** – IntelliJ IDEA, Eclipse, of elke editor die je verkiest.

## Pakketten Importeren
Importeer eerst de klassen die je nodig hebt voor het verwerken van PSD‑bestanden, kleuren, rechthoeken en stroke‑effecten.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## Stap 1: Laad het PSD‑bestand
Laad de bron‑PSD zodat je kunt werken met de lagen en resources.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Stap 2: Bereid Nieuwe Patroongegevens Voor
Maak een eenvoudig 4 × 4‑pixelpatroon dat zal worden gebruikt voor de stroke.

```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```

## Stap 3: Toegang tot het Stroke‑Effect
Zoek het stroke‑effect op de doel‑laag (in dit voorbeeld de vierde laag).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Stap 4: Het Stroke‑Effect Wijzigen

### Stroke‑Effecteigenschappen Bijwerken
Pas de opacity en blend‑mode aan om de visuele impact van het nieuwe patroon te zien.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Het Patroon‑Resource Bijwerken
Vervang de bestaande globale patroon‑resource door degene die je zojuist hebt gemaakt.

```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```

## Stap 5: Het Nieuwe Patroon Toepassen
Koppel de bijgewerkte patroon‑resource aan het stroke‑effect en sla de PSD op.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Stap 6: Verifieer de Wijzigingen
Laad het bestand opnieuw en bevestig dat het nieuwe patroon, de opacity en de blend‑mode correct zijn toegepast.

```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```

## Veelvoorkomende Problemen en Oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| Patroon verschijnt niet | Verkeerde `PatternId`‑referentie | Zorg ervoor dat de `PatternId` ingesteld op `PattResource` overeenkomt met die gebruikt in `PatternFillSettings`. |
| Stroke verdwijnt na opslaan | Opacity ingesteld op 0 of effect verborgen | Controleer dat `setOpacity` tussen 0‑255 ligt en dat `isVisible()` `true` retourneert. |
| Onverwachte kleuren | Blend‑mode mismatch | Gebruik `BlendMode.Color` (of een andere modus) die overeenkomt met je ontwerpintentie. |

## Veelgestelde Vragen

### Wat is Aspose.PSD for Java?
Aspose.PSD for Java is een bibliotheek die ontwikkelaars in staat stelt PSD‑bestanden (Photoshop Document) programmatically te maken, bewerken en converteren.

### Kan ik Aspose.PSD for Java gebruiken in een commercieel project?
Ja, je kunt het gebruiken in commerciële projecten. Je kunt een licentie aanschaffen via [here](https://purchase.aspose.com/buy).

### Is er een gratis proefversie beschikbaar voor Aspose.PSD for Java?
Ja, je kunt een gratis proefversie downloaden via [here](https://releases.aspose.com/).

### Hoe kan ik ondersteuning krijgen voor Aspose.PSD for Java?
Je kunt ondersteuning krijgen via de Aspose community‑forums [here](https://forum.aspose.com/c/psd/34).

### Wat zijn de systeemvereisten voor Aspose.PSD for Java?
Je hebt een geïnstalleerde JDK en een IDE nodig voor ontwikkeling. De bibliotheek ondersteunt meerdere besturingssystemen, waaronder Windows, Linux en macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-01-17  
**Getest met:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose