---
title: Ebene zur Ebenenanpassung in PSD hinzufügen
linktitle: Ebene zur Ebenenanpassung in PSD hinzufügen
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java effektiv eine Ebene zur Ebenenanpassung in Ihre PSD-Dateien einfügen. Verbessern Sie Ihre Bildbearbeitungsfähigkeiten.
weight: 16
url: /de/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ebene zur Ebenenanpassung in PSD hinzufügen

## Einführung
Wenn es um die Bildbearbeitung geht, kann die Verwaltung von Ebenen einen großen Unterschied in der Lebendigkeit und Klarheit Ihrer Fotos ausmachen. Ein praktisches Werkzeug im Photoshop-Arsenal ist die „Ebene zur Ebenenanpassung“, mit der Sie den Tonwertumfang und die Farbbalance Ihrer Bilder optimieren können. In dieser Anleitung zeigen wir Ihnen, wie Sie mit Aspose.PSD für Java eine Ebene zur Ebenenanpassung in einer PSD-Datei implementieren. Also schnappen Sie sich Ihre Java-IDE.
## Voraussetzungen
Bevor Sie in die Welt der Pegelanpassungen eintauchen, müssen Sie einige Dinge einrichten, um eine reibungslose Fahrt zu gewährleisten:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass das JDK auf Ihrem Rechner installiert ist. Wenn Sie es nicht haben, können Sie es von der[Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) oder verwenden Sie OpenJDK.
2.  Aspose.PSD für Java-Bibliothek: Um PSD-Dateien zu bearbeiten, müssen Sie die Aspose.PSD-Bibliothek herunterladen. Sie können die neueste Version hier herunterladen.[Downloadlink](https://releases.aspose.com/psd/java/) und stellen Sie sicher, dass Sie das JAR in die Bibliothek Ihres Projekts aufgenommen haben.
3. Grundkenntnisse in Java: Grundlegende Kenntnisse der Java-Programmierung sind hilfreich, da wir uns in diesem Tutorial eingehend mit Codeausschnitten befassen werden.
4. IDE-Setup: Sie können jede beliebige Java-IDE verwenden – beispielsweise IntelliJ IDEA, Eclipse oder NetBeans – um Ihren Code zu schreiben und auszuführen. Stellen Sie einfach sicher, dass Sie Ihr Java-Projekt eingerichtet und die Aspose.PSD-Bibliothek hinzugefügt haben.

## Pakete importieren
Bevor wir mit dem Schreiben unseres Codes beginnen, müssen wir die erforderlichen Pakete aus der Aspose.PSD-Bibliothek importieren. So können Sie das tun:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Durch das Importieren dieser Pakete haben wir Zugriff auf die Klassen, die zum Laden, Ändern und Speichern unserer PSD-Dateien erforderlich sind.

Lassen Sie uns den Vorgang nun in leicht verständliche Schritte unterteilen. Folgen Sie uns, während wir eine PSD-Datei laden, die Ebenen anpassen und dann Ihre Änderungen speichern. 
## Schritt 1: Richten Sie Ihre Dateipfade ein
Im ersten Schritt legen wir fest, wo sich unsere PSD-Datei befindet und wo wir die geänderte Ausgabe speichern möchten. Sie können den Verzeichnispfad Ihren Bedürfnissen entsprechend anpassen.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Ersetzen Sie hier`"Your Document Directory"`durch den tatsächlichen Pfad auf Ihrem System, in dem Ihre PSD-Datei gespeichert ist. Dies legt die Grundlage für alles, was wir als Nächstes tun werden.
## Schritt 2: Laden Sie die PSD-Datei
 Laden wir nun die PSD-Datei mit dem`PsdImage` Klasse. Dieser Schritt ist wichtig, da er uns den Zugriff und die Bearbeitung der Ebenen ermöglicht.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Wenn Sie anrufen`Image.load()` , wird die PSD-Datei gelesen und eine Instanz von erstellt`PsdImage` mit denen Sie arbeiten können.
## Schritt 3: Durch die Schichten iterieren
Da wir eine Ebene zur Ebenenanpassung anpassen möchten, müssen wir jede Ebene in unserer PSD-Datei durchlaufen. Dies hilft uns, die spezifische Ebene zu finden, die wir ändern möchten.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Weitere Manipulationen erfolgen hier...
    }
}
```
 In dieser Schleife`instanceof LevelsLayer` prüft, ob die aktuelle Ebene eine Ebene zur Tonwertkorrektur ist. Wenn ja, können wir mit der Anpassung ihrer Eigenschaften fortfahren.
## Schritt 4: Passen Sie die Pegelkanaleinstellungen an
Sobald wir die richtige Ebene identifiziert haben, können wir ihre Eingabe- und Ausgabepegel ändern. Hier geschieht die Magie! Passen Sie verschiedene Parameter an, um zu sehen, wie sie sich auf das Bild auswirken.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Die einzelnen Parameter bewirken Folgendes:
- Eingabe-Mitteltonpegel: Passt die Mitteltöne an.
- Eingabe-Schattenstufe: Optimiert die dunkleren Bereiche des Bildes.
- Eingabe-Hervorhebungsstufe: Ändert die hellen Bereiche des Bildes.
- Ausgabe-Schattenstufe: Legt fest, wie dunkle Schatten erscheinen.
- Ausgabe-Hervorhebungsstufe: Legt fest, wie helle Hervorhebungen angezeigt werden.
Experimentieren Sie ruhig mit unterschiedlichen Werten!
## Schritt 5: Speichern Sie die geänderte PSD-Datei
Nachdem wir unsere Anpassungen vorgenommen haben, ist es an der Zeit, die geänderte PSD-Datei zu speichern. Dieser Schritt ist entscheidend, um sicherzustellen, dass Ihre Änderungen angewendet und gespeichert werden.
```java
im.save(psdPathAfterChange);
```
 Sie finden Ihre angepasste PSD-Datei nun unter der angegebenen`psdPathAfterChange`. 
## Abschluss
Sie haben gerade gelernt, wie Sie mit Aspose.PSD für Java einer PSD-Datei eine Ebene zur Tonwertanpassung hinzufügen! Wenn Sie dieser Anleitung folgen, können Sie die Tonqualität Ihrer Bilder mühelos anpassen und so ein lebendigeres und optisch ansprechenderes Ergebnis erzielen. Denken Sie daran: Übung macht den Meister. Sie können also gerne die Anpassungen optimieren und verschiedene PSD-Dateien ausprobieren, um die Auswirkungen Ihrer Änderungen zu sehen.
## Häufig gestellte Fragen
### Was ist eine Ebene zur Pegelanpassung?
Mithilfe einer Ebene zur Tonwertanpassung können Sie den Tonwertumfang Ihrer Bilder korrigieren und Schatten, Mitteltöne und Glanzlichter ausgleichen.
### Kann ich Aspose.PSD ohne Kauf verwenden?
Ja! Aspose bietet eine kostenlose Testversion an, um die Bibliothek vor dem Kauf zu testen.
### Wo finde ich Dokumentation für Aspose.PSD?
 Die Dokumentation finden Sie[Hier](https://reference.aspose.com/psd/java/).
### Gibt es Community-Support für Aspose-Produkte?
 Auf jeden Fall! Sie können Fragen stellen und Unterstützung erhalten im[Aspose-Forum](https://forum.aspose.com/c/psd/34).
### Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?
 Sie können eine vorläufige Lizenz beantragen[Hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
