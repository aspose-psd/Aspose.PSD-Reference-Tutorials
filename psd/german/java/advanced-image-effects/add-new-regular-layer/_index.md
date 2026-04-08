---
date: 2026-04-08
description: Erfahren Sie, wie Sie PSD in PNG exportieren und mit Aspose.PSD für Java
  unter Verwendung einer temporären Aspose‑Lizenz eine neue PSD‑Ebene erstellen. Dieses
  Schritt‑für‑Schritt‑Tutorial behandelt die PSD‑Bildbearbeitung und das Festlegen
  der Ebenenposition.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Neue reguläre Ebene zu PSD hinzufügen
second_title: Aspose.PSD Java API
title: PSD nach PNG exportieren & eine neue reguläre Ebene hinzufügen mit Aspose.PSD
  für Java – aspose temporäre Lizenz
url: /de/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD nach PNG & Einen neuen regulären Layer hinzufügen mit Aspose.PSD für Java

## Einführung

In diesem **aspose psd tutorial** erfahren Sie, wie Sie **PSD nach PNG exportieren** und gleichzeitig **einen neuen regulären Layer** in derselben Datei **unter Verwendung einer aspose temporären Lizenz** für die Entwicklung erstellen. Egal, ob Sie web‑fertige Thumbnails generieren, Assets für eine Design‑Pipeline vorbereiten oder einfach mit **psd image manipulation** experimentieren möchten – Aspose.PSD für Java gibt Ihnen die volle programmatische Kontrolle. Wir führen Sie durch jeden Schritt – vom Laden der Quelldatei bis zum Speichern sowohl der aktualisierten PSD als auch einer PNG‑Kopie – sodass Sie sofort mit der Manipulation von PSD‑Layern beginnen können.

## Schnelle Antworten
- **Kann ich PSD mit einem Aufruf nach PNG exportieren?** Ja, nach dem Hinzufügen von Layers können Sie `save` mit `PngOptions` aufrufen.
- **Benötige ich eine Lizenz für die Entwicklung?** Eine temporäre Lizenz funktioniert für Tests; für die Produktion ist eine Voll‑Lizenz erforderlich.
- **Welche Java-Version wird unterstützt?** Aspose.PSD funktioniert mit Java 8 und neuer.
- **Ist die Layer‑Positionierung pixelbasiert?** Ja, Sie setzen linke, obere, rechte und untere Koordinaten in Pixeln mittels der **set layer position**‑Methoden.
- **Behält das PNG die Transparenz der Layer bei?** Das PNG enthält das zusammengeführte Ergebnis aller sichtbaren Layer.

## Warum ein aspose Temporärlizenz verwenden?

Eine **aspose temporäre Lizenz** ermöglicht Ihnen, den vollen Funktionsumfang von Aspose.PSD ohne funktionale Einschränkungen zu evaluieren. Sie entfernt das Evaluations‑Wasserzeichen, schaltet alle APIs frei – einschließlich der Möglichkeit, **neue psd layer**‑Objekte zu **erstellen** – und lässt Sie Ihren Code in einer produktionsähnlichen Umgebung testen, bevor Sie eine permanente Lizenz erwerben.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java-Entwicklungsumgebung** – JDK 8+ und ein Build‑Tool (Maven/Gradle) installiert.
- **Aspose.PSD für Java** – Laden Sie das neueste JAR von der offiziellen Seite [here](https://releases.aspose.com/psd/java/) herunter.
- **Eine Beispiel‑PSD‑Datei** – Wir verwenden `OneLayer.psd` in den Beispielen.

## Pakete importieren

Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu. Diese Klassen stellen die Kernfunktionalität für **psd image manipulation** und die Layer‑Verwaltung bereit.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Was ist „set layer position“ und warum ist es wichtig?

Wenn Sie einen neuen Layer hinzufügen, müssen Sie festlegen, wo er auf der Leinwand erscheint. Die Methoden `setLeft`, `setTop`, `setRight` und `setBottom` **setzen die Layer‑Position** in Pixelkoordinaten. Eine korrekte Positionierung sorgt dafür, dass Ihre Grafiken exakt dort liegen, wo Sie es erwarten – entscheidend für Aufgaben wie das Zusammenführen von UI‑Assets oder das Vorbereiten druckfertiger Dateien.

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: PSD‑Datei laden

Laden Sie zunächst die vorhandene PSD, die Sie ändern möchten. Dadurch erhalten Sie ein `PsdImage`‑Objekt, mit dem Sie arbeiten können.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Schritt 2: Pixeldaten und Rechtecke vorbereiten

Wir erstellen zwei Pixel‑Puffer (`int[]`) und definieren die rechteckigen Bereiche, in denen die neuen Layers gemalt werden. Dies ist die Grundlage für **die Erstellung eines neuen psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Schritt 3: Layer‑Daten initialisieren

Füllen Sie die Pixel‑Puffer mit einem Standard‑ARGB‑Wert. Der Wert `-10000000` entspricht einem halbtransparenten dunklen Farbton.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Schritt 4: Reguläre Layer hinzufügen (PSD‑Layer manipulieren)

Jetzt **fügen wir reguläre Layers** zum PSD‑Bild hinzu und **setzen die Layer‑Position** über die Eigenschaften left, top, right und bottom. Dies demonstriert, wie man **PSD‑Layer** programmgesteuert **manipuliert**.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Schritt 5: PSD nach PNG exportieren und die aktualisierte PSD speichern

Nachdem die Layers an ihrem Platz sind, speichern Sie das modifizierte Dokument. Zuerst exportieren wir das Ergebnis nach PNG (der **export psd to png**‑Schritt), dann persistieren wir die PSD mit den neuen Layers.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Wenn Sie nur das PNG benötigen, können Sie den PSD‑`save`‑Aufruf überspringen und direkt `save` mit `PngOptions` aufrufen.

## Häufige Probleme & Fehlerbehebung

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| PNG erscheint leer | Layer sind unsichtbar oder vollständig transparent | Stellen Sie sicher, dass Sie nicht‑transparente Pixelwerte setzen oder `layer.setVisible(true)` aufrufen. |
| `ArrayIndexOutOfBoundsException` | Unstimmigkeit zwischen Rechteckgröße und Pixel‑Array-Länge | Überprüfen Sie, dass `rect.width * rect.height == dataArray.length`. |
| LicenseException zur Laufzeit | Keine gültige Lizenz geladen | Laden Sie eine temporäre oder permanente Lizenz, bevor Sie API‑Methoden aufrufen. |

## Häufig gestellte Fragen

**F: Ist Aspose.PSD mit Java 8 kompatibel?**  
**A:** Ja, Aspose.PSD unterstützt Java 8 und spätere Versionen.

**F: Kann ich Transformationen (Drehen, Skalieren) auf die hinzugefügten Layer anwenden?**  
**A:** Absolut! Die `Layer`‑Klasse bietet Methoden wie `rotate`, `scale` und `translate` für vollständige Transformationskontrolle.

**F: Wo finde ich zusätzliche Aspose.PSD‑Dokumentation?**  
**A:** Detaillierte API‑Dokumentation ist verfügbar [hier](https://reference.aspose.com/psd/java/).

**F: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?**  
**A:** Besuchen Sie die Seite für temporäre Lizenzen [hier](https://purchase.aspose.com/temporary-license/).

**F: Gibt es Community‑Foren für Aspose.PSD‑Support?**  
**A:** Ja, treten Sie den Diskussionen in den Aspose‑Foren [hier](https://forum.aspose.com/c/psd/34) bei.

## Fazit

Sie haben nun gelernt, wie Sie **PSD nach PNG exportieren** und **neue reguläre Layers** mit Aspose.PSD für Java hinzufügen, und Sie haben gesehen, wie eine **aspose temporäre Lizenz** Ihnen ermöglicht, diesen Workflow ohne Einschränkungen auszuprobieren. Dieses Tutorial zeigt die Kernfähigkeiten der **psd image manipulation**: Laden einer Datei, Erstellen von Layers, Befüllen von Pixeldaten und Export der finalen Komposition. Experimentieren Sie gern mit unterschiedlichen Rechteckgrößen, Pixel­farben oder Layer‑Effekten, um das Ergebnis an die Bedürfnisse Ihres Projekts anzupassen.

---

**Zuletzt aktualisiert:** 2026-04-08  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}