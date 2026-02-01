---
date: 2026-02-01
description: Erfahren Sie, wie Sie PSD in PNG exportieren und mit Aspose.PSD für Java
  eine neue PSD‑Ebene erstellen. Dieses Schritt‑für‑Schritt‑Tutorial behandelt die
  Bildbearbeitung von PSD und die Konvertierung von PSD in PNG.
linktitle: Add a New Regular Layer to PSD
second_title: Aspose.PSD Java API
title: PSD nach PNG exportieren & eine neue reguläre Ebene mit Aspose.PSD für Java
  hinzufügen
url: /de/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD nach PNG exportieren & eine neue reguläre Ebene tutorial** erfahren Sie, wie Sie **export PSD to PNG** durchführen und gleichzeitig **creating a new regular layer** innerhalb derselben Datei erstellen können. Egal, Assets für eine Design‑Pipeline vorbereiten oder einfach mit **psd image manipulation** experimentieren möchten, Aspose.PSD für Java bietet Ihnen die vollständige programmatische Kontrolle. Wir führen – sodass Sie sofort mit der Manipulation von PSD‑Ebenen beginnen können.

## Wie man PSD nach PNG exportiert mit Aspose.PSD

Das Exportieren einer PSD nach PNG ist ein zweistufiger Prozess: Zuerst fügen Sie die benötigten Ebenen hinzu oder ändern sie, dann rufen Sie `save` mit einer `PngOptions`‑Instanz auf. Dieser Ansatz ermöglicht es Ihnen, **convert PSD to PNG** oder **export PSD as Ebene und warum eine neue PSD‑Ebene hinzufügen?

Eine **regular layer** ist eine grundlegende Rasterebene, die Pixeldaten, Transparenz und Positionsinformationenhalter einzufügen, ohne das vorhandene Artwork zu verändern. Dies ist besonders nützlich, wenn Sie **add layer to PSD** programmgesteuert für automatisierte Stapelverarbeitung benötigen.

## Schnelle Antworten
- **Can I export PSD to PNG with one call?** Ja, nach dem Hinzufügen der Ebenen können Sie `saverufen.
- **Do I need a license for development?** Eine temporäre Lizenz funktioniert für Tests; eine Voll‑Lizenz ist für die Produktion erforderlich.
- **Which Java version iseren Versionen.
- **Is layer positioning pixel‑based?** Ja, Sie setzen die linken, oberen, transparency?** Das PNG enthält das zusammengeführte Ergebnis aller sichtbaren Ebenen.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java Development Environment** – JDK 8+ und ein Build‑Tool (Maven/Gradle) installiert.
- **Aspose.PSD for Java** – Laden Sie das neueste JAR von der offiziellen Seite [here](https://releases.aspose.com/psd/java/) herunter.
- **A sample PSD file** – Wir verwenden `OneLayer.psd` in den Beispielen.

## Pakete importieren

Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu. Diese Klassen bieten die Kernfunktionalität für **psd image manipulation** und die Ebenenverwaltung.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Schritt 1: PSD‑Datei laden

Laden Sie zunächst die vorhandene PSD, die Sie ändern möchten. Dadurch erhalten Sie ein `PsdImage`‑Objekt, mit dem Sie arbeiten können.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Schritt 2: Pixeldaten und Rechtecke vorbereiten

Wir erstellen zwei Pixelpuffer (`int[]`) und definieren die rechteckigen Bereiche, in denen die neuen Ebenen gemalt werden. Dies ist die Grundlage für **creating a new PSD layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Schritt 3: Ebenendaten initialisieren

Füllen Sie die Pixelpuffer mit einem Standard‑ARGB‑Wert. Der Wert `-10000000` entspricht einem halbtransparenten dunklen Farbton.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Schritt 4: Reguläre Ebenen hinzufügen (PSD‑Ebenen manipulieren)

Jetzt **add regular layers** zum PSD‑Bild hinzu und setzen deren Begrenzungen. Dies zeigt, wie man **manipulate PSD layers** programmgesteuert und effektiv **add layer to PSD**.

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

## Schritt 5: PSD nach PNG exportieren und die aktualisierte PSD speichern

Nachdem die Ebenen platziert sind, speichern Sie das modifizierte Dokument. Zuerst exportieren wir das Ergebnis nach PNG (der **export psd to png**‑Schritt), dann speichern wir die PSD mit den neuen Ebenen.

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
| PNG erscheint leer | Ebenen sind unsichtbar oder vollständig transparent | Stellen Sie sicher, dass Sie nicht‑transparente Pixelwerte setzen oder `layer.setVisible(true)` aufrufen. |
| `ArrayIndexOutOfBoundsException` | Unstimmigkeit zwischen Rechteckgröße und Pixel‑Array‑Länge | Überprüfen Sie, dass `rect.width * rect.height == dataArray.length`. |
| LicenseException zur Laufzeit | Keine gültige Lizenz geladen | Laden Sie eine temporäre oder permanente Lizenz, bevor Sie API‑Methoden aufrufen. |

## Häufig gestellte Fragen

**Q: Ist Aspose.PSD mit Java 8 kompatibel?**  
A: Ja, Aspose.PSD unterstützt Java 8 und neuere Versionen.

**Q: Kann ich Transformationen (Drehen, Skalieren) auf die hinzugefügten Ebenen anwenden?**  
A: Absolut! Die `Layer`‑Klasse bietet Methoden wie `rotate`, `scale` und `translate` für die vollständige Transformationskontrolle.

**Q: Wo finde ich zusätzliche Aspose.PSD‑Dokumentation?**  
A: Detaillierte API‑Dokumentation ist [hier](https://reference.aspose.com/psd/java/) verfügbar.

**Q: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?**  
A: Besuchen Sie die Seite für temporäre Lizenzen [hier](https://purchase.aspose.com/temporary-license/).

**Q: Gibt es Community‑Foren für Aspose.PSD‑Support?**  
A: Ja, beteiligen Sie sich an den Diskussionen in den Aspose‑Foren [hier](https://forum.aspose.com/c/psd/34).

## Fazit

Sie haben nun gelernt, wie man **export PSD to PNG** durchführt, während man **adding new regular layers** mit Aspose.PSD für Java verwendet. Dieser Workflow demonstriert die Kernfunktionen der **psd image manipulation**: Laden einer Datei, Erstellen von Ebenen, Befüllen von Pixeldaten und Exportieren der endgültigen Komposition. Experimentieren Sie gern mit verschiedenen Rechteckgrößen, Pixel­farben oder Ebeneneffekten, um das Ergebnis an die Anforderungen Ihres Projekts anzupassen.

---

**Zuletzt aktualisiert:** 2026-02-01  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}