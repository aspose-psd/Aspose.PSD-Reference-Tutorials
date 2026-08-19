---
date: 2026-04-03
description: Erfahren Sie, wie Sie PSD mit einem Kontureffekt und einer Farbfüllung
  als PNG speichern können, indem Sie Aspose.PSD für Java verwenden. Diese Schritt‑für‑Schritt‑Anleitung
  zeigt, wie Sie PSD schnell nach PNG exportieren.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: PSD als PNG mit Kontureffekt speichern – Java
second_title: Aspose.PSD Java API
title: PSD als PNG mit Kontureffekt speichern – Java
url: /de/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD als PNG mit Strich‑Effekt und Farbfüllung speichern – Java

## Einführung

In diesem Leitfaden lernen Sie, wie Sie **PSD als PNG** speichern, während Sie einen Strich‑Effekt mit einer Farbfüllung mithilfe von Aspose.PSD für Java anwenden. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, dieses Schritt‑für‑Schritt‑Tutorial macht es Ihnen leicht, die Aufgabe zu erledigen. Wir behandeln alles, von der Einrichtung Ihrer Umgebung bis zum Export des finalen Bildes, sodass Sie schnell **PSD nach PNG exportieren** können in Ihren eigenen Projekten.

## Schnelle Antworten
- **Was erreicht dieses Tutorial?** Es zeigt, wie man eine PSD‑Datei als PNG speichert, nachdem ein anpassbarer Strich‑Effekt angewendet wurde.  
- **Welche Bibliothek wird verwendet?** Aspose.PSD für Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert zum Testen; für die Produktion ist eine Lizenz erforderlich.  
- **Kann ich die Strichfarbe ändern?** Ja – Sie können jede Farbe über `ColorFillSettings` festlegen.  
- **Ist Batch‑Verarbeitung möglich?** Absolut – wickeln Sie den Code in eine Schleife, um mehrere PSD‑Dateien zu verarbeiten.

## Was bedeutet „PSD als PNG speichern“?
Das Speichern einer PSD als PNG bedeutet, Photoshop‑s native, mehrschichtige Datei in ein flaches, web‑freundliches Bildformat zu konvertieren, wobei die visuelle Treue erhalten bleibt. Das ist nützlich, wenn Sie PSD‑Inhalte auf Websites, mobilen Apps oder anderen Plattformen anzeigen müssen, die PSD‑Dateien nicht direkt unterstützen.

## Warum einen Strich‑Effekt mit Farbfüllung anwenden?
Ein Strich fügt um den Inhalt einer Ebene eine klare Kontur hinzu, sodass Grafiken vor komplexen Hintergründen hervorstechen. In Kombination mit einer benutzerdefinierten Füllfarbe können Sie Bilder branden, UI‑Elemente hervorheben oder auffällige Thumbnails erstellen, ohne Photoshop zu verlassen.

## Voraussetzungen

1. **Java Development Kit (JDK) 8+** – stellen Sie sicher, dass `java` in Ihrem PATH ist.  
2. **Aspose.PSD für Java** – herunterladen von der [Website](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Editor Ihrer Wahl.  
4. **Beispiel‑PSD** – eine Datei, die bereits einen Strich‑Effekt enthält (oder fügen Sie einen in Photoshop hinzu).  
5. **Grundlegende Java‑Kenntnisse** – Sie werden ein paar Codezeilen schreiben, aber nichts Fortgeschrittenes.

Sobald Sie diese bereit haben, können wir mit dem Codieren beginnen.

## Pakete importieren

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Diese Importe bringen alle Klassen mit, die zum Laden einer PSD, zum Ändern ihres Strichs und zum Speichern sowohl von PSD‑ als auch PNG‑Ausgaben benötigt werden.

## Wie man PSD als PNG mit Strich‑Effekt speichert

### Schritt 1: PSD‑Datei laden

Zuerst geben Sie den Ordner an, der Ihre Quell‑PSD enthält.

```java
String dataDir = "Your Document Directory";
```

Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Pfad auf Ihrem Rechner.

Laden Sie nun die Datei, wobei vorhandene Effekt‑Ressourcen erhalten bleiben:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Schritt 2: Strichfarbe festlegen (und optional Breite anpassen)

Die Schleife unten durchläuft jede Ebene, greift auf den ersten `StrokeEffect` zu und ändert dessen Füllfarbe. Sie können auch `setWidth` oder `setPosition` am `StrokeEffect`‑Objekt anpassen, wenn Sie die **Strichbreite anpassen** möchten.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Pro‑Tipp:** `Color.getDeepPink()` ist nur ein Beispiel. Verwenden Sie `new Color(r, g, b)` für benutzerdefinierte RGB‑Werte.

### Schritt 3: Modifizierte PSD speichern (optional)

Wenn Sie eine PSD‑Version mit dem aktualisierten Strich behalten möchten, speichern Sie sie wie folgt:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Schritt 4: Bild als PNG exportieren (der Kernschritt „PSD als PNG speichern“)

Konvertieren Sie schließlich die bearbeitete PSD in eine PNG‑Datei, die für die Web‑Nutzung bereit ist:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Das PNG behält den zuvor gesetzten tief‑rosa Strich bei, und die Option `TruecolorWithAlpha` sorgt dafür, dass die Transparenz erhalten bleibt.

## Häufige Probleme & Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| **`ArrayIndexOutOfBoundsException`** | Die Ebene hat keine Effekte oder der erste Effekt ist kein `StrokeEffect`. | Stellen Sie sicher, dass die Ebene tatsächlich einen Strich enthält oder iterieren Sie über `getEffects()`, um den richtigen Typ zu finden. |
| **Farbe ändert sich nicht** | Möglicherweise bearbeiten Sie eine Kopie der Einstellungen statt des Originals. | Stellen Sie sicher, dass Sie direkt zu `ColorFillSettings` casten, indem Sie `effect.getFillSettings()` verwenden. |
| **PNG erscheint leer** | Die PSD wurde geladen, ohne die Ebene zu rasterisieren. | Rufen Sie `im.save(..., new PngOptions())` nach allen Änderungen auf; vermeiden Sie das Speichern des ursprünglichen `im` vor den Änderungen. |

## Häufig gestellte Fragen

**F: Kann ich mehrere Effekte auf einer einzelnen Ebene mit Aspose.PSD für Java anwenden?**  
A: Ja – Sie können auf die Mischoptionen der Ebene zugreifen und beliebig viele Effekte hinzufügen, einschließlich Schatten, Leuchten und Striche.

**F: Ist es möglich, den Vorgang für einen Stapel von PSD‑Dateien zu automatisieren?**  
A: Absolut. Wickeln Sie das Laden, Anwenden der Effekte und Speichern in eine `for‑each`‑Schleife, die über die Dateien in einem Verzeichnis iteriert.

**F: Wie kann ich Änderungen an einer PSD‑Datei rückgängig machen?**  
A: Laden Sie die Originaldatei erneut, bevor Sie Änderungen speichern; Aspose.PSD bietet keinen Undo‑Stack.

**F: Kann ich die Strichbreite und Position anpassen?**  
A: Ja. Verwenden Sie `effect.setWidth(float)` und `effect.setPosition(StrokeEffect.Position)`, um Dicke und Platzierung (innen, außen oder zentriert) zu steuern.

**F: Ist die Aspose.PSD für Java‑Bibliothek kostenlos nutzbar?**  
A: Eine kostenlose Testversion ist für die Evaluierung verfügbar. Der volle Funktionsumfang erfordert eine gekaufte Lizenz. Siehe die [Kaufoptionen](https://purchase.aspose.com/buy) für Details.

---

**Zuletzt aktualisiert:** 2026-04-03  
**Getestet mit:** Aspose.PSD 24.12 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}