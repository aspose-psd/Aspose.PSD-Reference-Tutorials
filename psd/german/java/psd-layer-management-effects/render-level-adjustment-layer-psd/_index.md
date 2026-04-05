---
date: 2026-04-05
description: Erfahren Sie, wie Sie PSD in PNG exportieren und mühelos den Bildkontrast
  mit Aspose.PSD für Java verbessern. Meistern Sie Ebenen‑Anpassungsebenen mit dieser
  Schritt‑für‑Schritt‑Anleitung.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: PSD nach PNG exportieren und Ebenen‑Anpassungsebene in Java rendern
second_title: Aspose.PSD Java API
title: PSD nach PNG exportieren und Ebenen‑Anpassungs‑Layer in Java rendern
url: /de/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD nach PNG exportieren und Ebenen‑Anpassungsebene in Java rendern

## Einführung

Haben Sie schon einmal eine PSD‑Datei geöffnet und bemerkt, dass die Farben flach wirken oder der Kontrast nicht stimmt? Sie können schnell **export PSD to PNG** durchführen, während Sie das Bild mit einer Levels Adjustment Layer feinabstimmen, indem Sie Aspose.PSD für Java verwenden. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer PSD, über das Anpassen ihrer Levels bis zum Speichern des Ergebnisses als PNG – sodass Sie die Lebendigkeit steigern und web‑fertige Assets in Minuten vorbereiten können.

## Schnelle Antworten
- **Was bedeutet „export PSD to PNG“?** Es konvertiert ein Photoshop‑Dokument in ein verlustfreies PNG‑Bild und bewahrt dabei die Transparenz.  
- **Kann ich die Levels vor dem Export anpassen?** Ja, Aspose.PSD ermöglicht es Ihnen, Eingabe‑ und Ausgabe‑Levels programmgesteuert zu ändern.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Ist Stapelverarbeitung möglich?** Absolut – Sie können den Code in einer Schleife platzieren, um mehrere PSD‑Dateien zu verarbeiten.  
- **Welche Java‑Version wird benötigt?** Java 8 oder neuer wird empfohlen.

## Was ist „export PSD to PNG“?
Das Exportieren einer PSD zu PNG bedeutet, die mehrschichtige Photoshop‑Datei zu nehmen und sie zu einem Portable Network Graphics‑Bild zu flachzulegen. PNG unterstützt verlustfreie Kompression und einen Alphakanal, wodurch es ideal für Web‑Grafiken und UI‑Assets ist.

## Warum Levels vor dem Export anpassen?
Das Anpassen der Levels ermöglicht es Ihnen, Schatten, Mitteltöne und Lichter zu steuern, wodurch der Gesamtkontrast und das Farbgleichgewicht verbessert werden. Dieser Schritt stellt sicher, dass das endgültige PNG ohne manuelle Nachbearbeitung in Photoshop professionell aussieht.

## Voraussetzungen

- **Java Development Kit (JDK)** – laden Sie die neueste Version von der Oracle‑Website herunter ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – erhalten Sie sie von der offiziellen Download‑Seite ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Eine kostenlose Testversion ist verfügbar ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Pakete importieren

Bevor Sie in den Code eintauchen, importieren Sie die Klassen, die uns Zugriff auf die PSD‑Manipulation und den PNG‑Export geben:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Dateipfade definieren (Wie man die PSD‑Verarbeitung automatisiert)

Legen Sie klare, beschreibende Variablen für die Quell‑PSD, die modifizierte PSD und den Zielort des PNG‑Exports fest.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Schritt 2: PSD‑Bild laden

Verwenden Sie `Image.load`, um die PSD‑Datei in ein `PsdImage`‑Objekt zu laden. Aspose.PSD erkennt das Format automatisch.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Schritt 3: Durch Ebenen iterieren (Wie man Levels anpasst)

Durchlaufen Sie jede Ebene, um die Levels Adjustment Layer zu finden.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Schritt 4: Die Levels‑Ebene identifizieren

Überprüfen Sie jede Ebene mit `instanceof LevelsLayer`. Sobald sie gefunden ist, casten Sie sie, damit wir ihre Eigenschaften ändern können.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Schritt 5: Levels feinabstimmen (Wie man Levels anpasst)

Passen Sie sowohl Eingabe‑ als auch Ausgabe‑Levels für den ersten Kanal (in der Regel der zusammengesetzte Kanal) an. Diese Werte sind Beispiele; experimentieren Sie gern.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Schritt 6: Modifizierte PSD speichern (Wie man PSD automatisiert)

Speichern Sie die Änderungen in einer neuen PSD‑Datei.

```java
im.save(psdPathAfterChange);
```

### Schritt 7: Als PNG exportieren (Export PSD to PNG)

Falls Sie eine PNG‑Version benötigen, konfigurieren Sie `PngOptions` und speichern das Bild.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Häufige Anwendungsfälle

- **Web‑Asset‑Vorbereitung:** Konvertieren Sie vom Designer bereitgestellte PSD‑Mockups in PNGs, die für Browser bereit sind.  
- **Stapelverarbeitung:** Automatisieren Sie die Konvertierung von Dutzenden PSD‑Dateien in einer CI‑Pipeline.  
- **Dynamische Bildgenerierung:** Passen Sie Levels in Echtzeit basierend auf Benutzereingaben an, bevor Sie exportieren.

## Fehlerbehebung & Tipps

- **Null‑Pointer beim Zugriff auf Ebenen:** Stellen Sie sicher, dass die PSD tatsächlich eine Levels Adjustment Layer enthält; andernfalls fügen Sie eine Null‑Prüfung hinzu.  
- **Unerwartete Farben nach dem Export:** Vergewissern Sie sich, dass der PNG‑Farbtyp auf `TruecolorWithAlpha` gesetzt ist, um die Transparenz zu erhalten.  
- **Leistung bei vielen Dateien:** Verwenden Sie dieselbe `PsdImage`‑Instanz wieder, wenn Sie einen Stapel verarbeiten, um Speicherverbrauch zu reduzieren.

## Häufig gestellte Fragen

**Q: Kann ich einzelne Farbkanäle (RGB) separat anpassen?**  
A: Ja. Verwenden Sie `levelsLayer.getChannel(index)`, wobei `index` = 0 (Rot), 1 (Grün), 2 (Blau) ist, um jeden Kanal unabhängig zu justieren.

**Q: Wie gehe ich mit mehreren Levels Adjustment Layers in einer PSD um?**  
A: Die Schleife verarbeitet jede Ebene; jede gefundene `LevelsLayer` wird gemäß dem Code im `if`‑Block angepasst.

**Q: Gibt es neben Levels noch andere Möglichkeiten, den Kontrast zu verbessern?**  
A: Aspose.PSD bietet außerdem Anpassungen für Kurven, Helligkeit/Kontrast und Histogramm‑Equalisation.

**Q: Kann ich dies für einen Ordner mit PSD‑Dateien automatisieren?**  
A: Verpacken Sie den gesamten Workflow in eine Schleife wie `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` und verarbeiten jede Datei nacheinander.

**Q: Wo finde ich weitere Dokumentation und Support?**  
A: Besuchen Sie die offizielle Referenz ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) und das Community‑Forum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Fazit

Durch das Beherrschen des **export PSD to PNG**‑Workflows und das Erlernen, **wie man Levels programmatisch anpasst**, erhalten Sie die volle Kontrolle über die Bildqualität, ohne Ihre Java‑Umgebung zu verlassen. Egal, ob Sie Assets für das Web vorbereiten, eine Design‑Pipeline automatisieren oder einen Batch‑Prozessor erstellen, Aspose.PSD für Java macht die Aufgabe einfach und zuverlässig.

---

**Zuletzt aktualisiert:** 2026-04-05  
**Getestet mit:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}