---
title: Reduzieren Sie Ebenen in PSD-Dateien mit Aspose.PSD Java
linktitle: Reduzieren Sie Ebenen in PSD-Dateien mit Aspose.PSD Java
second_title: Aspose.PSD Java API
description: Reduzieren und fügen Sie Ebenen in PSD-Dateien mühelos mit Aspose.PSD für Java zusammen. Folgen Sie dieser Schritt-für-Schritt-Anleitung, um Ihre PSD-Dateiverwaltung zu vereinfachen.
type: docs
weight: 13
url: /de/java/psd-layer-management-effects/flatten-layers-psd-files/
---
## Einführung

Haben Sie schon einmal mit Photoshop-Dateien gearbeitet und sich eine einfachere Möglichkeit gewünscht, diese komplexen Ebenen zu verwalten? Nun, Sie haben Glück! Heute tauchen wir in die Welt von Aspose.PSD für Java ein, einem leistungsstarken Tool, mit dem Sie programmgesteuert mit PSD-Dateien arbeiten können. Eine der praktischen Funktionen, die wir untersuchen werden, ist das Reduzieren von Ebenen. Egal, ob Sie ein ganzes Bild reduzieren oder bestimmte Ebenen selektiv zusammenführen möchten, Aspose.PSD für Java bietet Ihnen alles. Dieses Tutorial führt Sie Schritt für Schritt durch den Prozess und stellt sicher, dass Sie bereit sind, Ihre PSD-Dateien selbstbewusst in Angriff zu nehmen.

## Voraussetzungen

Bevor wir uns in den Code stürzen, stellen wir sicher, dass Sie alles haben, was Sie brauchen:

1. Java Development Kit (JDK): Stellen Sie sicher, dass JDK 8 oder höher auf Ihrem System installiert ist.
2.  Aspose.PSD für Java: Laden Sie die Aspose.PSD-Bibliothek herunter und fügen Sie sie Ihrem Projekt hinzu. Sie finden sie[Hier](https://releases.aspose.com/psd/java/).
3. Integrierte Entwicklungsumgebung (IDE): Eine IDE wie IntelliJ IDEA oder Eclipse macht Ihre Codierung reibungsloser.
4. Grundlegende Kenntnisse in Java: Dieses Tutorial ist zwar anfängerfreundlich, einige grundlegende Kenntnisse in Java werden Ihnen jedoch dabei helfen, ihm leichter zu folgen.
5. Beispiel-PSD-Datei: Halten Sie eine PSD-Datei zum Experimentieren bereit. Wir verwenden eine mit mehreren Ebenen, um den Reduziervorgang zu demonstrieren.

Nachdem wir nun das Wesentliche geklärt haben, kommen wir zum spaßigen Teil – der Arbeit mit dem Code!

## Pakete importieren

Zu Beginn müssen Sie die erforderlichen Pakete in Ihr Java-Projekt importieren. Mit diesen Paketen können Sie mit Aspose.PSD für Java mit PSD-Dateien arbeiten.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Diese Importe ermöglichen es uns, PSD-Dateien zu laden, Ebenen zu bearbeiten und die Änderungen zu speichern. Lassen Sie uns nun den Prozess der Ebenenreduzierung in überschaubare Schritte unterteilen.

## Schritt 1: Reduzieren des gesamten PSD-Bildes

Die erste Aufgabe besteht darin, das gesamte PSD-Bild zu reduzieren. Dies ist nützlich, wenn Sie alle Ebenen zu einer einzigen Ebene kombinieren möchten, damit das Bild einfacher zu verwalten und zu exportieren ist.

### 1.1 Laden Sie die PSD-Datei

 Zuerst laden wir die PSD-Datei in unser Programm. Diese Datei sollte in Ihrem Projektverzeichnis abgelegt werden, das wir als`Your Document Directory`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Dieser Codeausschnitt lädt die PSD-Datei mit dem Namen`ThreeRegularLayersSemiTransparent.psd` aus Ihrem angegebenen Verzeichnis.

### 1.2 Das Bild reduzieren

Als Nächstes reduzieren wir das gesamte Bild. Beim Reduzieren werden alle sichtbaren Ebenen zu einer einzigen Hintergrundebene kombiniert.

```java
im.flattenImage();
```

Mit diesem Einzeiler werden alle Ebenen Ihrer PSD-Datei zu einer zusammengeführt.

### 1.3 Speichern des abgeflachten Bildes

Abschließend speichern wir das reduzierte Bild in einer neuen Datei.

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

 Dadurch wird die abgeflachte PSD-Datei unter dem neuen Namen gespeichert`ThreeRegularLayersSemiTransparentFlattened.psd`. Herzlichen Glückwunsch! Sie haben gerade Ihr erstes PSD-Bild mit Aspose.PSD für Java reduziert.

## Schritt 2: Bestimmte Ebenen zusammenführen

Manchmal möchten Sie vielleicht nicht das gesamte Bild reduzieren, sondern nur bestimmte Ebenen zusammenführen. Sehen wir uns an, wie Sie das erreichen können.

### 2.1 Laden Sie die PSD-Datei erneut

Da wir einen anderen Vorgang durchführen, laden Sie zunächst die PSD-Datei erneut.

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

Dadurch wird dieselbe PSD-Datei geladen und ist bereit für ebenenspezifische Vorgänge.

### 2.2 Ebenen identifizieren und auswählen

Um bestimmte Ebenen zusammenzuführen, identifizieren und wählen Sie zunächst die Ebenen aus, die Sie zusammenführen möchten.

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

Hier wählen wir die erste, zweite und dritte Ebene der PSD-Datei aus. Diese Ebenen werden in einem Array gespeichert und Sie können über ihren Index darauf zugreifen.

### 2.3 Zusammenführen der Ebenen

Lassen Sie uns nun die ausgewählten Ebenen zusammenführen. Wir beginnen mit der Zusammenführung der unteren und mittleren Ebene und führen das Ergebnis dann mit der oberen Ebene zusammen.

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

Dieser Code führt die Ebenen sequenziell zusammen, sodass eine einzige kombinierte Ebene entsteht.

### 2.4 Ersetzen Sie die vorhandenen Ebenen durch die zusammengeführte Ebene

Nach dem Zusammenführen müssen Sie die vorhandenen Ebenen im Bild durch die neu zusammengeführte Ebene ersetzen.

```java
img.setLayers(new Layer[]{layer2});
```

Dieser Schritt stellt sicher, dass das Bild jetzt nur noch die zusammengefügte Ebene enthält.

### 2.5 Speichern der aktualisierten PSD-Datei

Speichern Sie abschließend die aktualisierte PSD-Datei mit den zusammengeführten Ebenen.

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Dadurch wird die PSD mit den zusammengeführten Ebenen unter einem neuen Namen gespeichert, sodass die Originaldatei erhalten bleibt.

## Abschluss

Das Arbeiten mit Ebenen in PSD-Dateien kann sich oft wie das Navigieren durch ein Labyrinth anfühlen, aber mit Aspose.PSD für Java ist es, als hätten Sie eine Karte in der Hand. Ob Sie ein ganzes Bild glätten oder ausgewählte Ebenen sorgfältig zusammenführen müssen, Aspose.PSD vereinfacht den Vorgang und macht aus einer möglicherweise entmutigenden Aufgabe eine unkomplizierte Operation. Wenn Sie diesem Tutorial folgen, sollten Sie nun mit der Ebenenmanipulation in PSD-Dateien mit Java vertraut sein. Warum also nicht mit Ihren eigenen Projekten ausprobieren und sehen, wie viel Zeit und Mühe Sie sparen?

## Häufig gestellte Fragen

### Kann ich die Abflachung der Ebenen in Aspose.PSD rückgängig machen?  
Nein, wenn Sie Ebenen mit Aspose.PSD reduzieren, ist die Aktion nicht mehr rückgängig zu machen. Es ist immer ratsam, eine Sicherungskopie der Originaldatei aufzubewahren.

### Ist es möglich, nur sichtbare Ebenen zu glätten?  
 Ja, Sie können anhand ihrer Sichtbarkeit steuern, welche Ebenen abgeflacht werden sollen. Stellen Sie sicher, dass nur die Ebenen sichtbar sind, die Sie abflachen möchten, bevor Sie die`flattenImage` Verfahren.

### Reduziert das Reduzieren von Ebenen die Dateigröße?  
Durch das Reduzieren von Ebenen kann die Dateigröße verringert werden, insbesondere wenn viele komplexe Ebenen vorhanden sind. Die genaue Reduzierung hängt jedoch vom Inhalt der Ebenen ab.

### Kann ich Ebenen mit unterschiedlichen Mischmodi zusammenführen?  
Ja, Sie können Ebenen mit unterschiedlichen Mischmodi mit Aspose.PSD zusammenführen und die resultierende Ebene behält das Erscheinungsbild der zusammengeführten Ebenen bei.

### Was passiert, wenn ich versuche, Ebenen zusammenzuführen, die nicht nebeneinander liegen?  
Mit Aspose.PSD können Sie beliebige Ebenen unabhängig von ihrer Reihenfolge im Ebenenstapel zusammenführen. Beim Zusammenführen werden die ausgewählten Ebenen wie angegeben kombiniert.