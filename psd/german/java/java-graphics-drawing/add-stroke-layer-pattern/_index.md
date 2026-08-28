---
date: 2026-08-28
description: Fügen Sie ein pattern zu einer layer in Java mit Aspose.PSD hinzu. Folgen
  Sie dieser Schritt‑für‑Schritt‑Anleitung, um einen stroke layer effect anzuwenden,
  pattern‑Ressourcen zu konfigurieren und Ihre PSD‑Dateien effizient zu speichern.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Wie man ein Stroke Layer Pattern in Java hinzufügt
og_description: Fügen Sie ein pattern zu einer layer in Java mit Aspose.PSD hinzu.
  Folgen Sie dieser kompakten Anleitung, um einen stroke layer effect anzuwenden,
  pattern‑Ressourcen zu konfigurieren und Ihre PSD‑Dateien effizient zu speichern.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Pattern zu einer layer in Java hinzufügen – Aspose.PSD Tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Wie man ein pattern zu einer layer in Java hinzufügt
url: /de/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Muster zu einer Ebene in Java hinzufügt

## Einführung
Ein Muster zu einer Ebene in Java hinzuzufügen ist ein häufiges Anliegen, wenn Sie Photoshop‑PSD‑Dateien mit benutzerdefinierten Kontureffekten anreichern müssen. Mit Aspose.PSD für Java wird diese Aufgabe unkompliziert, selbst wenn Sie neu in der Bibliothek sind. In diesem Tutorial lernen Sie, wie Sie ein PSD laden, eine Musterressource erstellen, diese an einen Kontureffekt anhängen und das Ergebnis speichern – alles mit klaren Schritt‑für‑Schritt‑Anleitungen.

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.PSD für Java.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für ein einfaches Muster.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** JDK 8 oder neuer.  
- **Kann ich das in einem Webservice verwenden?** Ja, die API ist plattformunabhängig und funktioniert in jeder Java‑Umgebung.

## Was bedeutet das Hinzufügen eines Musters zu einer Ebene?
Ein Muster zu einer Ebene hinzuzufügen bedeutet, ein gekacheltes Bitmap einer Kontur‑ oder Füllungseffekt zuzuweisen, sodass die Grafik über die Kontur der Form hinweg wiederholt wird. Diese Technik wird häufig für dekorative Rahmen, Texturen und Marken‑Overlays verwendet und ermöglicht es Designern, konsistente visuelle Themen zu erstellen, ohne jedes Element manuell zu zeichnen.

## Warum Aspose.PSD für diese Aufgabe verwenden?
Aspose.PSD unterstützt **über 30 Bildformate** und kann PSD‑Dateien bis zu **2 GB** manipulieren, ohne das gesamte Dokument in den Speicher zu laden, und liefert damit schnelle Leistung auf typischer Server‑Hardware. Die fluente API ermöglicht es, Ebeneneffekte programmgesteuert zu bearbeiten, wodurch Photoshop in automatisierten Pipelines überflüssig wird.

## Voraussetzungen
- Java Development Kit (JDK) 8 oder neuer installiert.
- Aspose.PSD für Java – laden Sie es von der **Aspose.PSD für Java Download‑Seite**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) herunter und fügen Sie die JAR-Datei dem Klassenpfad Ihres Projekts hinzu.
- Eine IDE wie IntelliJ IDEA oder Eclipse zum Bearbeiten und Ausführen des Beispielcodes.
- Eine Beispiel‑PSD‑Datei, die eine Formebene enthält, die Sie ändern möchten.

## Pakete importieren
Importieren Sie zunächst die Namespaces, die Zugriff auf PSD‑Objekte, Ressourcen und Effekte bieten.

```
// No actual code block is added to preserve original placeholders.
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
```

## Wie man ein Muster zu einer Ebene in Java hinzufügt?

Laden Sie das Ziel‑PSD, erstellen Sie eine Musterressource, hängen Sie diese an den Kontureffekt der gewünschten Ebene an und speichern Sie schließlich die Datei. Dieser End‑zu‑End‑Ablauf erfordert nur wenige Codezeilen und funktioniert mit jedem Standard‑PSD, das eine Vektor‑Formebene enthält.

### Schritt 1: PSD‑Datei laden
Das Laden des Dokuments gibt Ihnen Zugriff auf die Ebenenhierarchie und die Effekt‑Sammlung.  
`PsdLoadOptions` konfiguriert, wie das PSD gelesen wird, während `PsdImage` die geladene Datei im Speicher repräsentiert.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Durch das Laden der PSD‑Datei können Sie nun auf deren Ebenen und Effekte zugreifen und sie manipulieren.

### Schritt 2: neue Musterdaten vorbereiten
Erstellen Sie ein `PatternResource`, das das Bitmap enthält, das Sie als Konturmuster kacheln möchten.  
`PatternResource` ist eine globale PSD‑Ressource, die ein wiederholendes Bitmap‑Muster speichert. `Rectangle` definiert die Grenzen des Musters und `UUID` liefert einen eindeutigen Bezeichner.

```
// Placeholder for original code.
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
```

Diese Musterdaten werden verwendet, um den neuen Kontureffekt zu erstellen.

### Schritt 3: Zugriff auf den Kontureffekt
Identifizieren Sie die Formebene, die bereits eine Kontur hat, und rufen Sie ihr `StrokeEffect`‑Objekt ab.  
`StrokeEffect` stellt den Kontureffekt dar, der auf eine Formebene angewendet wird.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Damit wird sichergestellt, dass Sie mit der richtigen Ebene und dem richtigen Effekt arbeiten.

### Schritt 4: Kontureffekt ändern
Aktualisieren Sie nun die Eigenschaften der Kontur, um auf die neue Musterressource zu verweisen.

#### Kontureffekt‑Eigenschaften aktualisieren
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Musterressource aktualisieren
`PattResource` ist eine globale PSD‑Ebenenressource, die Musterdaten speichert.

```
// Placeholder for original code.
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
```

Diese Code‑Snippets ersetzen das vorhandene Muster durch das von Ihnen bereitgestellte.

### Schritt 5: Neues Muster anwenden
`PatternFillSettings` enthält die Füllungseinstellungen für einen musterbasierten Kontureffekt. Übernehmen Sie die Änderungen an der Ebene und schreiben Sie das aktualisierte PSD zurück auf die Festplatte.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Damit wird sichergestellt, dass das neue Muster korrekt angewendet wird und die Datei mit den Änderungen gespeichert wird.

### Schritt 6: Änderungen überprüfen
Laden Sie die Datei erneut und prüfen Sie die Kontur, um zu bestätigen, dass das Muster wie erwartet erscheint.

```
// Placeholder for original code.
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
```

Dieser Schritt verifiziert, dass die Musterdaten korrekt auf den Kontureffekt angewendet wurden.

## Häufige Probleme und Fehlerbehebung
- **Muster nicht sichtbar:** Stellen Sie sicher, dass die DPI des Musterbildes mit der Auflösung des PSD übereinstimmt und dass das `Enabled`‑Flag der Kontur auf `true` gesetzt ist.  
- **Große PSD‑Dateien verursachen OutOfMemoryError:** Verwenden Sie `PsdImage.load(..., LoadOptions)` mit `LoadOptions.setLoadAllLayers(false)`, um Ebenen bei Bedarf zu laden.  
- **Falsche Ebene ausgewählt:** Überprüfen Sie den Ebenen‑Index oder -Namen, bevor Sie auf deren Effekte zugreifen; Sie können `psdImage.getLayers()` enumerieren, um verfügbare Ebenen aufzulisten.

## Häufig gestellte Fragen

**F: Was ist Aspose.PSD für Java?**  
Aspose.PSD für Java ist eine Bibliothek, die Entwicklern ermöglicht, PSD‑ (Photoshop‑Dokument‑) Dateien programmgesteuert zu erstellen, zu bearbeiten und zu konvertieren.

**F: Kann ich Aspose.PSD für Java in einem kommerziellen Projekt verwenden?**  
Ja, Sie können es in kommerziellen Projekten einsetzen. Sie können eine Lizenz über die **Aspose‑Kaufseite**([Aspose purchase page](https://purchase.aspose.com/buy)) erwerben.

**F: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?**  
Ja, Sie können eine kostenlose Testversion von der **Aspose‑Release‑Seite**([Aspose releases page](https://releases.aspose.com/)) herunterladen.

**F: Wie kann ich Support für Aspose.PSD für Java erhalten?**  
Sie können Support über die Aspose‑Community‑Foren **hier**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)) erhalten.

**F: Was sind die Systemanforderungen für Aspose.PSD für Java?**  
Sie benötigen ein installiertes JDK und eine IDE für die Entwicklung. Die Bibliothek unterstützt Windows, Linux und macOS.

## Fazit
Sie haben nun gelernt, wie man mit Aspose.PSD ein Muster zu einer Ebene in Java hinzufügt. Durch Befolgen der obigen Schritte können Sie PSD‑Dateien programmgesteuert mit benutzerdefinierten Konturmustern verbessern, Branding‑Workflows automatisieren und die Grafikverarbeitung in jede Java‑basierte Anwendung integrieren. Erkunden Sie weitere Aspose.PSD‑Funktionen wie Ebenen‑Zusammenführung, Farb‑Anpassungen und den Export nach PNG oder JPEG, um Ihr Bildverarbeitungs‑Toolkit weiter zu erweitern.

---

**Zuletzt aktualisiert:** 2026-08-28  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose

## Verwandte Tutorials

- [Render Pattern Fill Layer PSD-Dateien](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Pattern Overlay PSD: Effekte mit Aspose.PSD für Java hinzufügen](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Wie man die Konturfarbe in Java mit Aspose.PSD ändert](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}