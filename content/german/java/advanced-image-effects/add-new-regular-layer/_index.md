---
title: Fügen Sie mit Aspose.PSD für Java eine neue reguläre Ebene zu PSD hinzu
linktitle: Fügen Sie PSD eine neue reguläre Ebene hinzu
second_title: Aspose.PSD Java-API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java eine neue reguläre Ebene zu PSD-Dateien hinzufügen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose PSD-Manipulation.
type: docs
weight: 11
url: /de/java/advanced-image-effects/add-new-regular-layer/
---
## Einführung

Willkommen zu diesem umfassenden Tutorial zur Verwendung von Aspose.PSD für Java zum Hinzufügen einer neuen regulären Ebene zu einer PSD-Datei. Aspose.PSD ist eine leistungsstarke Java-Bibliothek, mit der Entwickler PSD-Dateien effizient bearbeiten und bearbeiten können. In diesem Tutorial führen wir Sie durch den Prozess des Hinzufügens einer neuen regulären Ebene zu einer PSD-Datei und stellen Ihnen detaillierte Schritte und Codebeispiele zur Verfügung.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem System eine Java-Entwicklungsumgebung eingerichtet ist.
-  Aspose.PSD-Bibliothek: Laden Sie die Aspose.PSD für Java-Bibliothek herunter und installieren Sie sie. Sie finden die Bibliothek[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Diese Pakete sind für die Arbeit mit Aspose.PSD-Funktionen unerlässlich. Fügen Sie die folgenden Zeilen am Anfang Ihrer Java-Datei ein:

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

## Schritt 2: Bereiten Sie Datenarrays und Rechtecke vor

Bereiten Sie zwei int-Arrays und zwei Rechteckobjekte wie folgt vor:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Schritt 3: Layer-Daten initialisieren

Datenarrays mit einem Standardwert initialisieren:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Schritt 4: Regelmäßige Ebenen hinzufügen

Fügen Sie dem PSD-Bild zwei reguläre Ebenen hinzu:

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

Speichern Sie die geänderte PSD und eine zusätzliche PNG-Datei:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Glückwunsch! Sie haben mit Aspose.PSD für Java erfolgreich eine neue reguläre Ebene zu einer PSD-Datei hinzugefügt.

## Abschluss

In diesem Tutorial haben wir den Prozess des Hinzufügens einer neuen regulären Ebene zu einer PSD-Datei mit Aspose.PSD für Java behandelt. Diese leistungsstarke Bibliothek vereinfacht die PSD-Manipulation und macht sie für Java-Entwickler zugänglich. Experimentieren Sie mit verschiedenen Parametern und Funktionen, um das volle Potenzial von Aspose.PSD auszuschöpfen.

## FAQs

### F1: Ist Aspose.PSD mit Java 8 kompatibel?

A1: Ja, Aspose.PSD unterstützt Java 8 und spätere Versionen.

### F2: Kann ich Transformationen auf die hinzugefügten Ebenen anwenden?

A2: Auf jeden Fall! Aspose.PSD bietet eine Reihe von Transformationsoptionen für Ebenen.

### F3: Wo finde ich zusätzliche Aspose.PSD-Dokumentation?

 A3: Sie können sich auf die Dokumentation beziehen.[Hier](https://reference.aspose.com/psd/java/).

### F4: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 A4: Besuchen[dieser Link](https://purchase.aspose.com/temporary-license/) für temporäre Lizenzoptionen.

### F5: Gibt es Community-Foren für Aspose.PSD-Unterstützung?

 A5: Ja, Sie können Unterstützung und Diskussionen finden.[Hier](https://forum.aspose.com/c/psd/34).