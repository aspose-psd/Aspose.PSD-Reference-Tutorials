---
date: 2025-12-04
description: Erfahren Sie, wie Sie PSD als PNG speichern und einen Rendering‑Schatten
  mit Aspose.PSD für Java anwenden. Dieser Leitfaden behandelt, wie man einen Schatten
  hinzufügt, PSD in PNG konvertiert und einen Drop‑Shadow in Java anwendet.
language: de
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: PSD als PNG speichern & Schlagschatten hinzufügen mit Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD als PNG speichern & Drop Shadow hinzufügen mit Aspose.PSD Java

## Einführung

Wenn Sie in Java mit Photoshop‑Dateien arbeiten, ist das **Speichern von PSD als PNG** bei gleichzeitiger Hinzufügung eines professionell aussehenden Drop‑Shadows ein häufiges Anliegen. Aspose.PSD macht diese Aufgabe unkompliziert, indem es Ihnen ermöglicht, **PSD in PNG zu konvertieren** und **Drop Shadow Java** mit nur wenigen Code‑Zeilen anzuwenden. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer PSD‑Datei bis zum Export des finalen PNG mit gerendertem Schatteneffekt.

## Schnellantworten
- **Was bedeutet „PSD als PNG speichern“?** Es konvertiert eine mehrschichtige Photoshop‑Datei in ein flaches PNG‑Bild und bewahrt die Transparenz.  
- **Kann ich beim Konvertieren einen Drop‑Shadow hinzufügen?** Ja – Aspose.PSD lässt Sie Ebeneneffekte vor dem Export ändern.  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher.  
- **Ist der Drop‑Shadow‑Effekt anpassbar?** Absolut – Sie können Farbe, Deckkraft, Abstand, Größe, Winkel und mehr anpassen.

## Voraussetzungen

Bevor wir starten, stellen Sie sicher, dass Sie Folgendes haben:

- **Java‑Entwicklungsumgebung** – JDK 8 oder neuer installiert.  
- **Aspose.PSD‑Bibliothek** – Laden Sie das neueste JAR von der offiziellen Seite [here](https://releases.aspose.com/psd/java/).  
- **Eine PSD‑Datei** – Eine Datei, die mindestens eine Ebene enthält, die Sie mit einem Schatten versehen möchten.  

## Wie speichere ich PSD als PNG mit einem Drop‑Shadow in Java?

Im Folgenden finden Sie eine Schritt‑für‑Schritt‑Anleitung. Jeder Schritt enthält eine kurze Erklärung sowie den genauen Code, den Sie kopieren können.

### Schritt 1: Importieren der erforderlichen Pakete

Wir beginnen mit dem Import der Klassen, die das Laden von Bildern, die Behandlung von Effekten und den PNG‑Export ermöglichen.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Schritt 2: Definieren des Dokumentverzeichnisses

Legen Sie den Ordner fest, in dem Ihre Quell‑PSD und das resultierende PNG gespeichert werden.

```java
String dataDir = "Your Document Directory";
```

### Schritt 3: Festlegen der PSD‑ und PNG‑Dateipfade

Geben Sie die vollständigen Pfade für das Eingabe‑PSD und das Ausgabe‑PNG an.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Schritt 4: Laden der PSD‑Datei mit aktivierten Effekten

Durch Aktivieren von **loadEffectsResource** werden Ebeneneffekte (wie Schatten) zur Manipulation bereitgestellt.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Schritt 5: Zugriff auf den Drop‑Shadow‑Effekt

Hier holen wir uns den ersten Effekt, der auf die zweite Ebene (Index 1) angewendet wurde. Dort lesen oder ändern wir die Schattenparameter.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Schritt 6: Validieren der Shadow‑Effekt‑Eigenschaften (optional, aber hilfreich)

Das Prüfen der vorhandenen Eigenschaften hilft Ihnen zu entscheiden, ob Änderungen nötig sind. Die nachfolgenden Assertions bestätigen die Standardwerte.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Pro‑Tipp:** Wenn Sie **wie man Schatten hinzufügt** mit benutzerdefinierten Einstellungen, ändern Sie die Eigenschaften von `shadowEffect` vor dem Speichern (z. B. `shadowEffect.setColor(Color.getRed());`).

### Schritt 7: Speichern des modifizierten Bildes als PNG

Abschließend exportieren wir das PSD (mit gerendertem Schatten) in eine PNG‑Datei. Die Option `TruecolorWithAlpha` bewahrt die Transparenz.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Und das war's – ein vollständiger **convert PSD to PNG**‑Workflow, der zudem **apply drop shadow java** in einem einzigen Durchlauf ausführt.

## Warum Aspose.PSD für diese Aufgabe verwenden?

- **Kein natives Photoshop erforderlich** – Funktioniert auf jeder Plattform, die Java unterstützt.  
- **Vollständige PSD‑Treue** – Alle Ebeneninformationen, Masken und Effekte bleiben erhalten.  
- **Feinkörnige Kontrolle** – Passen Sie jeden Parameter des Drop‑Shadows vor dem Export an.  
- **Hohe Leistung** – Optimiert für große Dateien und Batch‑Verarbeitung.

## Häufige Probleme & Fehlerbehebung

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| `NullPointerException` on `shadowEffect` | Die Ziel‑Ebene hat keine Effekte oder der Index ist falsch. | Überprüfen Sie den Ebenen‑Index (`im.getLayers()[i]`) und stellen Sie sicher, dass ein Effekt vorhanden ist. |
| Exportiertes PNG ist leer | PNG‑Optionen nicht korrekt gesetzt oder Bild nicht gespeichert. | Verwenden Sie `PngColorType.TruecolorWithAlpha` und prüfen Sie, ob der Pfad von `im.save()` beschreibbar ist. |
| Schattenfarbe ist nicht sichtbar | Schatten‑Deckkraft ist auf 0 gesetzt oder die Farbe entspricht dem Hintergrund. | Setzen Sie `shadowEffect.setOpacity(255);` und wählen Sie eine kontrastierende Farbe. |

## Häufig gestellte Fragen

**F: Kann ich Drop‑Shadows auf mehrere Ebenen gleichzeitig anwenden?**  
A: Ja. Durchlaufen Sie `im.getLayers()` und ändern Sie bei Bedarf das `DropShadowEffect` jeder Ebene.

**F: Was bewirkt der Parameter „Spread“?**  
A: Er steuert, wie stark der Schatten von vollständig undurchsichtig zu transparent übergeht. Ein höherer Spread erzeugt eine härtere Kante.

**F: Ist Aspose.PSD mit allen Photoshop‑Versionen kompatibel?**  
A: Es unterstützt ein breites Spektrum an PSD‑Versionen, von frühen Releases bis zu den neuesten Photoshop‑CC‑Dateien.

**F: Wie bekomme ich Hilfe, wenn ich Probleme habe?**  
A: Besuchen Sie das [Aspose.PSD‑Forum](https://forum.aspose.com/c/psd/34) für Community‑Support und offizielle Unterstützung.

**F: Kann ich Aspose.PSD vor dem Kauf testen?**  
A: Absolut. Laden Sie eine kostenlose Testversion von der [Aspose‑Website](https://releases.aspose.com/) herunter.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose