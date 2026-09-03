---
date: 2026-09-03
description: Erfahren Sie, wie Sie einen Gradient‑Strich in Java erstellen und Strich‑Verläufe
  in PSD‑Dateien mit Aspose.PSD für Java anpassen. Schritt‑für‑Schritt‑Anleitung für
  Entwickler.
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: Wie man Gradient Stroke Layer in Java erstellt
og_description: Erstellen Sie Gradient‑Strich in Java mit Aspose.PSD für Java in wenigen
  Minuten. Dieses Tutorial zeigt Ihnen, wie Sie Gradient‑Striche zu PSD‑Dateien hinzufügen
  und anpassen, inklusive code snippets und best practices.
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: Gradient‑Strich in Java erstellen – Aspose.PSD Tutorial‑Leitfaden
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: Gradient‑Strich in Java erstellen – Aspose.PSD Tutorial‑Leitfaden
url: /de/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man einen Farbverlauf‑Strich in Java mit Aspose.PSD erstellt

## Einleitung
Wenn Sie **Farbverlauf‑Strich‑Effekte in Java** erstellen möchten, ohne Photoshop zu öffnen, sind Sie hier genau richtig. In diesem Tutorial lernen Sie, wie Sie Aspose.PSD für Java – eine reine Java‑Bibliothek, die Ihnen vollständige programmgesteuerte Kontrolle über PSD‑Dateien gibt – verwenden. Wir gehen Schritt für Schritt durch das Laden einer PSD, den Zugriff auf den Strich‑Effekt einer Ebene, die Konfiguration einer Farbverlauf‑Füllung und schließlich das Speichern des Ergebnisses. Am Ende können Sie professionelle Farbverlauf‑Umrandungen zu Formen oder Text in nur wenigen Code‑Zeilen hinzufügen.

## Schnelle Antworten
- **Was ist das Hauptziel?** Einen Farbverlauf‑Strich‑Layer in einer PSD‑Datei mit Java erstellen.  
- **Welche Bibliothek stellt die API bereit?** Aspose.PSD für Java (unterstützt Java 8 +).  
- **Benötige ich eine Lizenz für die Produktion?** Ja – eine gültige oder temporäre Lizenz ist erforderlich.  
- **Wie lange dauert eine Grundimplementierung?** Ungefähr 10‑15 Minuten für einen einfachen Strich.  
- **Kann ich den Typ des Farbverlaufs anpassen?** Absolut – lineare, radiale und winkelbasierte Verläufe werden alle unterstützt.

## Was ist ein Farbverlauf‑Strich‑Layer?
Ein Farbverlauf‑Strich‑Layer ist eine Vektor‑Umrandung, deren Farbe sanft zwischen zwei oder mehr Farbtönen übergeht. Er kann auf Formen, Text oder jede Vektor‑Maske innerhalb einer PSD‑Datei angewendet werden und verleiht Designern einen dynamischen visuellen Effekt, ohne das Artwork zu rasterisieren.

## Warum Aspose.PSD für Java verwenden?
Aspose.PSD für Java bietet **vollständige PSD‑Unterstützung** für mehr als 100 Features – einschließlich Ebenen, Masken, Anpassungsebenen und Ebeneneffekte – und kann Dateien bis zu 2 GB verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Die Bibliothek läuft auf jedem Betriebssystem, das Java unterstützt, hat keine nativen Abhängigkeiten und wird monatlich aktualisiert, um mit den neuesten Photoshop‑Dateispezifikationen kompatibel zu bleiben.

## Voraussetzungen
1. **Java Development Kit (JDK)** – Installieren Sie das neueste JDK von der [Oracle-Website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD für Java** – Laden Sie die Bibliothek von der [Aspose.PSD‑Download‑Seite](https://releases.aspose.com/psd/java/) herunter.  
3. **IDE** – IntelliJ IDEA, Eclipse oder NetBeans.  
4. **Lizenz** – Besorgen Sie sich eine [temporäre Lizenz](https://purchase.aspose.com/temporary-license/), falls Sie keine vollständige kommerzielle Lizenz besitzen.

## Pakete importieren
Die `import`‑Anweisungen bringen die notwendigen Klassen in den Gültigkeitsbereich.  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

Nun teilen wir den Prozess in klare Schritte auf.

## Schritt 1: PSD‑Datei laden
Das Laden der Quelldatei ist der erste Schritt; Sie müssen Effekt‑Ressourcen aktivieren, damit Strich‑Informationen zum Bearbeiten verfügbar sind. **PsdLoadOptions** konfiguriert, wie eine PSD‑Datei geladen wird, und ermöglicht das Ein‑ oder Ausschalten bestimmter Ressourcen.  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## Schritt 2: Auf den Strich‑Effekt zugreifen
**StrokeEffect** repräsentiert die Umrandungs‑Gestaltung, die auf eine Ebene angewendet wird, einschließlich Breite, Farbe und Farbverlauf‑Füllung.  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## Schritt 3: Strich‑Effekteigenschaften prüfen
Bevor Sie etwas ändern, sollten Sie die bestehenden Eigenschaften auslesen. Das hilft, die aktuelle Konfiguration zu verstehen und ein unbeabsichtigtes Überschreiben wichtiger Einstellungen zu vermeiden. **GradientFillSettings** enthält die Konfiguration der Farbverlauf‑Füllung für einen Strich‑Effekt.  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## Schritt 4: Farbverlauf‑Füllungseinstellungen ändern
`GradientFill` definiert, wie Farben über den Strich hinweg übergehen. Sie können den Typ (linear, radial), den Winkel und den Mischmodus ändern und anschließend neue Farb‑ und Transparenz‑Punkte zuweisen.  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## Schritt 5: Farb‑ und Transparenz‑Punkte hinzufügen und ändern
Ein Farbverlauf besteht aus einer Reihe von Farb‑Stop‑ und Opazitäts‑Stop‑Punkten. **GradientColorPoint** definiert einen Farb‑Stop im Verlauf, indem er Farbe und Position festlegt. **GradientTransparencyPoint** definiert einen Opazitäts‑Stop, ebenfalls mit Opazität und Position. Das Hinzufügen oder Anpassen dieser Punkte ermöglicht es, den visuellen Fluss des Strichs zu gestalten.  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## Schritt 6: Modifizierte PSD‑Datei speichern
Nach allen Anpassungen schreiben Sie das aktualisierte Dokument zurück auf die Festplatte. Aspose.PSD bewahrt automatisch alle anderen Ebenen und Ressourcen.  

```text
```java
im.save(exportPath);
```
```

## Schritt 7: Änderungen überprüfen
Laden Sie die gespeicherte Datei erneut und prüfen Sie, ob die Farbverlauf‑Eigenschaften des Strichs den gesetzten Werten entsprechen. Dieser Verifizierungsschritt ist für automatisierte Pipelines essenziell. **Assert** liefert einfache Test‑Assertions, um Bedingungen zur Laufzeit zu prüfen.  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## Häufige Stolperfallen und Tipps zur Fehlersuche
- **Lizenz‑Fehler** – Wenn Sie eine Lizenz‑Ausnahme sehen, prüfen Sie, ob die temporäre Lizenzdatei vor irgendeinem API‑Aufruf korrekt geladen wurde.  
- **Farbverlauf nicht sichtbar** – Stellen Sie sicher, dass das Flag `strokeEnabled` der Ziel‑Ebene auf `true` gesetzt ist; andernfalls wird der Effekt beim Rendern ignoriert.  
- **Performance bei großen Dateien** – Für PSD‑Dateien größer als 500 MB sollten Sie `PsdImage.load(..., LoadOptions)` mit `loadResources = false` verwenden und nur die Ressourcen aktivieren, die Sie benötigen.

## Häufig gestellte Fragen

**F: Was ist Aspose.PSD für Java?**  
A: Aspose.PSD für Java ist eine reine Java‑Bibliothek, die Entwicklern ermöglicht, Photoshop‑PSD‑Dateien zu erstellen, zu bearbeiten, zu konvertieren und zu rendern, ohne Adobe Photoshop zu benötigen.

**F: Benötige ich eine Lizenz, um Aspose.PSD für Java zu verwenden?**  
A: Ja, für den Produktionseinsatz ist eine gültige Lizenz erforderlich. Sie können eine [temporäre Lizenz](https://purchase.aspose.com/temporary-license/) für Evaluierungszwecke erhalten.

**F: Kann ich mit dieser Bibliothek PSD‑Dateien von Grund auf neu erstellen?**  
A: Absolut. Aspose.PSD stellt APIs bereit, um ein neues PSD‑Dokument zu bauen, Ebenen hinzuzufügen, Effekte anzuwenden und die Datei vollständig programmgesteuert zu speichern.

**F: Ist es möglich, neben Farbverlauf‑Strichen andere Effekte anzuwenden?**  
A: Ja, Sie können Schatten, Leuchten, Abschrägungen und viele andere Ebeneneffekte über dieselbe effektbasierte API hinzufügen.

**F: Wo finde ich die vollständige Referenzdokumentation?**  
A: Die offizielle Dokumentation ist verfügbar in der [Aspose.PSD Java API‑Referenz](https://reference.aspose.com/psd/java/).

## Fazit
Sie haben nun eine vollständige End‑zu‑End‑Lösung, wie Sie **Farbverlauf‑Strich‑Effekte in Java** in PSD‑Dateien mit Aspose.PSD erstellen können. Durch das Laden einer PSD, den Zugriff auf den Strich‑Effekt, die Konfiguration einer Farbverlauf‑Füllung und das Speichern der Datei können Sie anspruchsvolle Grafik‑Workflows automatisieren, die sonst manuelle Arbeit in Photoshop erfordern würden. Experimentieren Sie mit verschiedenen Farbverlauf‑Typen, Mischmodi und Opazitäts‑Stops, um das exakt gewünschte Aussehen für Ihre Anwendung zu erzielen.

---

**Zuletzt aktualisiert:** 2026-09-03  
**Getestet mit:** Aspose.PSD für Java 24.11  
**Autor:** Aspose

## Verwandte Tutorials

- [Gradient‑Füllung‑PSD mit Java und Aspose.PSD erstellen – Gradient‑Füllungs‑Layer hinzufügen](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Wie man radiale Farbverlauf‑Effekte in Aspose.PSD für Java erstellt](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Wie man die Strichfarbe in Java mit Aspose.PSD ändert](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}