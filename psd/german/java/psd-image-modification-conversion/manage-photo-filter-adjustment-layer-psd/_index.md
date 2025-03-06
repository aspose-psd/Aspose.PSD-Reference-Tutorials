---
title: Verwalten der Anpassungsebene für Fotofilter in PSD – Java
linktitle: Verwalten der Anpassungsebene für Fotofilter in PSD – Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie Fotofilter-Anpassungsebenen in PSD-Dateien mit Aspose.PSD für Java verwalten. Folgen Sie dieser Anleitung zum mühelosen Bearbeiten und Hinzufügen von Filtern.
weight: 24
url: /de/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Verwalten der Anpassungsebene für Fotofilter in PSD – Java

## Einführung
Sind Sie Entwickler und möchten Ihre Grafikbearbeitungsfähigkeiten mit Java verbessern? Dann sind Sie hier richtig! Heute tauchen wir ein in die Verwaltung von Fotofilter-Anpassungsebenen mit Aspose.PSD für Java. Mit dieser leistungsstarken Bibliothek können Sie PSD-Dateien nahtlos bearbeiten und so einen effizienten Workflow im Grafikdesign ermöglichen. Egal, ob Sie Effekte hinzufügen oder vorhandene Ebenen bearbeiten möchten, wir bieten Ihnen eine Schritt-für-Schritt-Anleitung, die den Vorgang vereinfacht.
## Voraussetzungen
Bevor wir uns auf diese Reise begeben, stellen wir sicher, dass Sie alles, was Sie brauchen, einsatzbereit haben:
### Wichtige Software
1.  Java Development Kit (JDK): Stellen Sie sicher, dass auf Ihrem Computer eine kompatible Version von JDK installiert ist. Sie können es hier herunterladen:[Website von Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD für Java: Um PSD-Dateien zu bearbeiten, benötigen Sie die Aspose.PSD-Bibliothek. Sie können sie von der[Aspose-Veröffentlichungsseite](https://releases.aspose.com/psd/java/) Vergessen Sie nicht, sich die[Aspose-Dokumentation](https://reference.aspose.com/psd/java/) für weitere Details.
3. IDE (Integrated Development Environment): Eine gute IDE wie IntelliJ IDEA oder Eclipse erleichtert Ihnen das Codieren.
### Die Grundlagen verstehen
Kenntnisse in der Java-Programmierung und ein grundlegendes Verständnis der Funktionsweise von PSD-Dateien sind von Vorteil. Wenn Sie noch keine Erfahrung mit der Verwendung von Bibliotheken in Java haben, ist es eine gute Idee, sich mit dem Importieren und Verwenden von Frameworks vertraut zu machen.
## Pakete importieren
Um zu beginnen, müssen wir die erforderlichen Klassen aus der Aspose.PSD-Bibliothek importieren. Hier ist eine einfache Importanweisung, die Sie am Anfang Ihrer Java-Datei benötigen:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Fügen Sie dies einfach oben in Ihre Java-Datei ein und schon können Sie mit der Arbeit mit PSD-Bildern beginnen!
## Vorhandene Fotofilterebene bearbeiten
### Schritt 1: Einrichten des Datenverzeichnisses
 Zunächst müssen Sie das Verzeichnis definieren, in dem Ihre PSD-Dateien gespeichert sind. Ersetzen Sie`"Your Document Directory"` mit dem tatsächlichen Pfad. So organisieren Sie alles:
```java
String dataDir = "Your Document Directory";
```
### Schritt 2: Laden Sie Ihre PSD-Datei
 Laden wir nun die PSD-Datei hoch, die Sie bearbeiten möchten. Stellen Sie sicher, dass`PhotoFilterAdjustmentLayer.psd`existiert in Ihrem angegebenen Verzeichnis.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```
### Schritt 3: Initialisieren Sie das Bildobjekt
Mithilfe der integrierten Funktionalität von Aspose laden wir das Bild in unser Projekt:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
### Schritt 4: Durch die Schichten iterieren
 Als nächstes untersuchen wir die Ebenen in der PSD-Datei. Unser Ziel ist es, die`PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Änderungen an der Ebene vornehmen
    }
}
```
### Schritt 5: Passen Sie die Fotofilterebene an
 Hier geschieht die Magie! Sie können die`Color` Und`Density`. Wir können beispielsweise die Farbe auf ein leuchtendes Rot einstellen und die Dichte anpassen:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```
### Schritt 6: Speichern Sie die bearbeitete PSD-Datei
Speichern Sie abschließend die Änderungen, um eine neue PSD-Datei mit Ihren Anpassungen zu erstellen:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
Sie haben gerade eine Anpassungsebene für einen Fotofilter in einer PSD-Datei bearbeitet.
## Hinzufügen einer neuen Fotofilterebene
### Schritt 1: Verzeichnispfad einrichten
Wie zuvor beginnen wir mit der Definition unseres Datenverzeichnisses:
```java
String dataDir = "Your Document Directory";
```
### Schritt 2: Laden Sie die Quelldatei
Für dieses Beispiel laden wir eine andere PSD-Datei, in die wir einen neuen Fotofilter einfügen möchten:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```
### Schritt 3: Das Bildobjekt erneut initialisieren
 Wir müssen eine neue`PsdImage` Instanz, also laden wir die Datei:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
### Schritt 4: Fügen Sie eine Fotofilterebene hinzu
Jetzt können wir eine neue Fotofilterebene mit einer benutzerdefinierten Farbe hinzufügen. So geht's:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```
### Schritt 5: Speichern Sie die neue PSD-Datei
Es ist wieder Zeit, unsere Änderungen zu speichern. Hier ist die Zeile, die genau das tut:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
Sie haben Ihrer PSD-Datei erfolgreich eine neue Fotofilterebene hinzugefügt.
## Abschluss
Die Verwaltung von Fotofilter-Anpassungsebenen in PSD-Dateien mit Aspose.PSD für Java ist nicht nur unkompliziert, sondern eröffnet auch eine Welt voller Möglichkeiten zur Grafikbearbeitung. Indem Sie diese Schritt-für-Schritt-Anleitungen befolgen, können Sie Ihre PSD-Dateien mit lebendigen Filtern verbessern und atemberaubende Grafiken erstellen. Testen Sie diese Funktionen in Ihren Anwendungen. Sie werden sie für Ihre Projekte sicherlich effizient finden!
## Häufig gestellte Fragen
### Was ist Aspose.PSD?
Aspose.PSD ist eine .NET- und Java-Bibliothek zum Erstellen, Bearbeiten und Konvertieren von PSD-Dateien.
### Kann ich Aspose.PSD kostenlos testen?
 Ja, Aspose bietet eine kostenlose Testversion an. Probieren Sie es aus[Hier](https://releases.aspose.com/).
### Wo finde ich die Dokumentation?
 Die vollständige Dokumentation finden Sie auf[Aspose's Referenzseite](https://reference.aspose.com/psd/java/).
### Wie kann ich Aspose.PSD kaufen?
 Sie können die Software kaufen bei[dieser Link](https://purchase.aspose.com/buy).
### Gibt es Support für Aspose.PSD?
 Auf jeden Fall! Sie können Unterstützung über das Aspose-Supportforum erhalten[Hier](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
