---
title: Render-Level-Anpassungsebene in PSD-Dateien – Java
linktitle: Render-Level-Anpassungsebene in PSD-Dateien – Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java mühelos den Kontrast und die Lebendigkeit von Bildern verbessern. Meistern Sie Tonwertkorrektur-Anpassungsebenen mit dieser Schritt-für-Schritt-Anleitung.
type: docs
weight: 17
url: /de/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---
## Einführung

Haben Sie schon einmal eine PSD-Datei geöffnet und festgestellt, dass dem Bild Kontrast oder Lebendigkeit fehlt? Keine Angst, Bildbearbeitungskrieger! Aspose.PSD für Java kommt mit seinen leistungsstarken Manipulationsfunktionen für Ebenenanpassungsebenen zur Rettung. Diese Anleitung vermittelt Ihnen das Wissen, wie Sie Ihre Bilder im Handumdrehen mit Ebenen optimieren können. 

## Voraussetzungen

- Java Development Kit (JDK): Stellen Sie sicher, dass auf Ihrem System eine aktuelle Version des JDK installiert ist. Sie können es von der Oracle-Website herunterladen ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD für Java-Bibliothek: Laden Sie die Aspose.PSD für Java-Bibliothek von der Download-Seite herunter ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Sie benötigen eine gültige Lizenz, um alle Funktionen nutzen zu können. Für den Einstieg steht jedoch eine kostenlose Testversion zur Verfügung ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Pakete importieren

Bevor wir uns in den Code vertiefen, müssen wir die erforderlichen Aspose.PSD-Klassen importieren, um mit PSD-Dateien zu interagieren. Folgendes benötigen Sie:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 Der`com.aspose.psd` Paket bietet Zugriff auf PSD-Manipulationsfunktionen, während`com.aspose.psd.imaging.PngOptions` ermöglicht es uns, Optionen beim Speichern des Bildes als PNG festzulegen.

Lassen Sie uns nun unser Abenteuer der Tonwertanpassung beginnen:

## Schritt 1: Dateipfade einrichten:

- Definieren Sie Variablen für Ihr Dokumentverzeichnis (`dataDir`), Name der Quell-PSD-Datei (`sourceFileName`), Name der Ziel-PSD-Datei nach der Änderung (`psdPathAfterChange`) und dem endgültigen PNG-Exportpfad (`pngExportPath`). Erwägen Sie die Verwendung beschreibender Namen, um die Lesbarkeit des Codes zu verbessern.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Schritt 2: Laden des PSD-Bildes:

-  Verwenden Sie die`Image.load` Methode zum Öffnen der PSD-Quelldatei und Speichern in einem`PsdImage`Objekt (`im`). Aspose.PSD erkennt das Dateiformat automatisch.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Schritt 3: Durch Schichten iterieren:

- Wir müssen die Ebene zur Tonwertkorrektur in Ihrer PSD-Datei finden. Aspose bietet eine praktische Möglichkeit, alle Ebenen mithilfe einer Schleife zu durchlaufen.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (Code zur Überprüfung der Ebenenebene wird hier hinzugefügt)
}
```

## Schritt 4: Identifizieren der Ebenenebene:

- Überprüfen Sie innerhalb der Schleife, ob die aktuelle Ebene (`im.getLayers()[i]` ) ist ein Beispiel für`LevelsLayer` Klasse mit dem`instanceof` Operator. 
-  Wenn dies der Fall ist, wandeln Sie die Ebene in eine`LevelsLayer` Objekt zur weiteren Manipulation.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (Code zum Anpassen der Ebenen wird hier hinzugefügt)
   }
}
```
## Schritt 5: Feinabstimmung der Pegel (Fortsetzung):

-  Passen Sie die Ausgangspegel mit`setOutputShadowLevel` Und`setOutputHighlightLevel` um die Dunkelheit und Helligkeit des resultierenden Bildes zu steuern. Diese Werte bestimmen den Bereich der Eingangspegel, der dem Ausgangsbereich zugeordnet wird.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Eingangspegel anpassen (0-255):
	   channel.setInputShadowLevel((short) 10); // Schatten leicht abdunkeln
	   channel.setInputMidtoneLevel(2.0f);     // Mitteltöne verstärken
	   channel.setInputHighlightLevel((short) 230); // Reduzieren von Glanzlichtern

	   // Ausgabepegel anpassen (0-255):
	   channel.setOutputShadowLevel((short) 20); // Schatten weiter abdunkeln
	   channel.setOutputHighlightLevel((short) 200); //Highlights aufhellen
   }
}
```

## Schritt 6: Speichern der geänderten PSD:

-  Verwenden Sie die`save` Methode der`PsdImage` Objekt, um das geänderte Bild im angegebenen Pfad zu speichern (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Schritt 7: Als PNG exportieren (optional):

-  Wenn Sie eine PNG-Version des angepassten Bildes benötigen, erstellen Sie eine`PngOptions` Objekt und stellen Sie den Farbtyp auf`TruecolorWithAlpha` . Verwenden Sie dann die`save` Methode erneut mit dem PNG-Exportpfad und den Optionen.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Und da haben Sie es! Sie haben die Ebene zur Tonwertkorrektur in Ihrer PSD-Datei erfolgreich mit Aspose.PSD für Java angepasst. Wenn Sie diese Schritte verstehen und mit verschiedenen Werten experimentieren, können Sie den Kontrast und das Gesamterscheinungsbild Ihrer Bilder verbessern.

## Abschluss

Mit Aspose.PSD für Java übernehmen Sie die Kontrolle über Ihren Bildbearbeitungsprozess. Indem Sie die Ebene zur Tonwertkorrektur beherrschen, können Sie Ihren Fotos und Designs neues Leben einhauchen. Denken Sie daran: Übung macht den Meister. Zögern Sie also nicht, zu experimentieren und das volle Potenzial dieses leistungsstarken Tools zu erkunden.
 
## Häufig gestellte Fragen

### Kann ich einzelne Farbkanäle (RGB) separat einstellen? 
Ja, Sie können auf jeden Farbkanal zugreifen über die`getChannel` Methode der`LevelsLayer` Objekt und ändern dessen Ebenen unabhängig voneinander.

### Wie gehe ich mit mehreren Ebenen zur Tonwertanpassung in einer PSD um?
Der Code durchläuft alle Ebenen und verarbeitet daher automatisch alle zusätzlichen Ebenen, die im Bild gefunden werden.

### Gibt es außer den Tonwertstufen noch andere Möglichkeiten, den Bildkontrast anzupassen?
Auf jeden Fall! Aspose.PSD bietet verschiedene Bildanpassungstools wie Kurven, Helligkeit/Kontrast und mehr.

### Kann ich diesen Vorgang für mehrere Bilder automatisieren? 
Ja, Sie können diesen Code in eine Schleife oder ein Stapelverarbeitungsskript integrieren, um mehrere PSD-Dateien effizient zu verarbeiten.

### Wo finde ich weitere Informationen und Unterstützung?
Aspose bietet eine umfangreiche Dokumentation ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) und ein Support-Forum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) für alle Fragen oder Probleme, die auftreten können.