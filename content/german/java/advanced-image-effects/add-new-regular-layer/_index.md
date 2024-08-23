---
title: Fügen Sie PSD mit Aspose.PSD für Java eine neue reguläre Ebene hinzu
linktitle: Fügen Sie PSD eine neue normale Ebene hinzu
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java PSD-Dateien eine neue reguläre Ebene hinzufügen. Folgen Sie unserer Schritt-für-Schritt-Anleitung zur nahtlosen PSD-Bearbeitung.
type: docs
weight: 11
url: /de/java/advanced-image-effects/add-new-regular-layer/
---
## Einführung

Willkommen zu diesem umfassenden Tutorial zur Verwendung von Aspose.PSD für Java, um einer PSD-Datei eine neue reguläre Ebene hinzuzufügen. Aspose.PSD ist eine leistungsstarke Java-Bibliothek, mit der Entwickler PSD-Dateien effizient bearbeiten und damit arbeiten können. In diesem Tutorial führen wir Sie durch den Prozess des Hinzufügens einer neuen regulären Ebene zu einer PSD-Datei und liefern detaillierte Schritte und Codebeispiele.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem System eine Java-Entwicklungsumgebung eingerichtet ist.
-  Aspose.PSD-Bibliothek: Laden Sie die Aspose.PSD-Bibliothek für Java herunter und installieren Sie sie. Sie finden die Bibliothek[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Diese Pakete sind für die Arbeit mit Aspose.PSD-Funktionen unerlässlich. Fügen Sie am Anfang Ihrer Java-Datei die folgenden Zeilen ein:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Schritt 1: PSD-Datei laden

Laden Sie die PSD-Datei, die Sie bearbeiten möchten, mit dem folgenden Code:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Schritt 2: Datenarrays und Rechtecke vorbereiten

Bereiten Sie zwei int-Arrays und zwei Rectangle-Objekte wie folgt vor:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Schritt 3: Layer-Daten initialisieren

Initialisieren Sie Datenarrays mit einem Standardwert:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Schritt 4: Regelmäßige Ebenen hinzufügen

Fügen Sie dem PSD-Bild zwei normale Ebenen hinzu:

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

## Schritt 5: PSD und PNG speichern

Speichern Sie die geänderte PSD- und eine zusätzliche PNG-Datei:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Herzlichen Glückwunsch! Sie haben mit Aspose.PSD für Java erfolgreich eine neue reguläre Ebene zu einer PSD-Datei hinzugefügt.

## Abschluss

In diesem Tutorial haben wir den Vorgang des Hinzufügens einer neuen regulären Ebene zu einer PSD-Datei mithilfe von Aspose.PSD für Java behandelt. Diese leistungsstarke Bibliothek vereinfacht die PSD-Manipulation und macht sie für Java-Entwickler zugänglich. Experimentieren Sie mit verschiedenen Parametern und Funktionen, um das volle Potenzial von Aspose.PSD auszuschöpfen.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD mit Java 8 kompatibel?

A1: Ja, Aspose.PSD unterstützt Java 8 und spätere Versionen.

### F2: Kann ich Transformationen auf die hinzugefügten Ebenen anwenden?

A2: Auf jeden Fall! Aspose.PSD bietet eine Reihe von Transformationsoptionen für Ebenen.

### F3: Wo finde ich zusätzliche Aspose.PSD-Dokumentation?

 A3: Sie können die Dokumentation zu Rate ziehen[Hier](https://reference.aspose.com/psd/java/).

### F4: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 A4: Besuch[dieser Link](https://purchase.aspose.com/temporary-license/) für temporäre Lizenzoptionen.

### F5: Gibt es Community-Foren für Aspose.PSD-Support?

 A5: Ja, Sie finden Support und Diskussionen[Hier](https://forum.aspose.com/c/psd/34).