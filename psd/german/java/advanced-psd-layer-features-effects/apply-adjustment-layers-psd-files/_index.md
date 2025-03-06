---
title: Anwenden von Anpassungsebenen in PSD-Dateien mit Java
linktitle: Anwenden von Anpassungsebenen in PSD-Dateien mit Java
second_title: Aspose.PSD Java API
description: Erfahren Sie in dieser vollständigen Schritt-für-Schritt-Anleitung für Entwickler, wie Sie mit Aspose.PSD für Java Anpassungsebenen in PSD-Dateien anwenden.
weight: 15
url: /de/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Anwenden von Anpassungsebenen in PSD-Dateien mit Java

## Einführung
Sind Sie Java-Entwickler und möchten in PSD-Dateien gespeicherte Bilder verbessern? Dann sind Sie hier richtig! In diesem Artikel erfahren Sie, wie Sie mithilfe der Aspose.PSD-Bibliothek für Java Anpassungsebenen in PSD-Dateien anwenden. Egal, ob Sie an einem persönlichen Projekt oder einer professionellen Anwendung arbeiten: Wenn Sie wissen, wie Sie PSD-Dateien bearbeiten, können Sie die Leistungsfähigkeit Ihrer Software erheblich steigern. 

## Voraussetzungen
Bevor wir uns in den Code stürzen und mit der Anwendung dieser Anpassungsebenen beginnen, müssen Sie einige Voraussetzungen erfüllen:
1. Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem Computer installiert ist. Sie können es hier herunterladen:[Website von Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD-Bibliothek: Falls noch nicht geschehen, müssen Sie die Aspose.PSD-Bibliothek für Java herunterladen. Sie finden sie[Hier](https://releases.aspose.com/psd/java/).
3. Entwicklungsumgebung: Richten Sie eine integrierte Java-Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse ein, in der Sie Ihren Code schreiben und ausführen.
4. Grundlegende Kenntnisse in Java: Allgemeine Kenntnisse der Java-Programmierung helfen Ihnen dabei, problemlos mitzukommen.
5. PSD-Dateien: Halten Sie zu Testzwecken einige PSD-Dateien bereit. Sie können einige mit Adobe Photoshop erstellen oder Beispieldateien aus dem Internet herunterladen.
## Pakete importieren
Bevor wir mit dem Programmieren beginnen, klären wir, welche Pakete wir importieren müssen. Aspose.PSD ermöglicht uns, auf verschiedene Weise mit Photoshop-Dateien zu arbeiten. Besorgen wir uns also die erforderlichen Klassen, um PSD-Bilder und Anpassungsebenen zu verarbeiten.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
Nachdem wir nun unsere Pakete bereitgestellt haben, wollen wir die Beispiele Schritt für Schritt aufschlüsseln!
## Schritt 1: Laden Sie die PSD-Datei
Der erste Schritt auf unserem Weg ist das Laden der PSD-Datei. Mit dieser Datei werden wir arbeiten, um unsere Anpassungsebenen anzuwenden.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 In diesem Snippet definieren wir das Verzeichnis, in dem sich unsere PSD-Dateien befinden, und laden die spezifische Datei, die wir bearbeiten möchten. Stellen Sie sicher, dass Sie ersetzen`"Your Document Directory"` durch den tatsächlichen Pfad zu Ihren PSD-Dateien auf Ihrem Computer.
## Schritt 2: Über Ebenen iterieren
Nachdem wir nun die PSD-Datei geladen haben, möchten wir ihre Ebenen durchsuchen, um unsere Anpassungsebenen zu finden.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 In diesem Schritt durchlaufen wir jede Ebene in der PSD-Datei, um alle Ebenen zu identifizieren, die von der`AdjustmentLayer` Typ. Wenn wir einen finden, verschmelzen wir ihn mit der Basisebene, die normalerweise die erste Ebene ist (`im.getLayers()[0]`). Dieser Zusammenführungsprozess wendet die Anpassungen effektiv auf unser Bild an. 
## Schritt 3: Speichern Sie die geänderte PSD-Datei
Nach dem Ändern der Ebenen ist es wichtig, die vorgenommenen Änderungen zu speichern. Lassen Sie uns dies im nächsten Schritt tun.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 Hier geben wir den Exportpfad für unsere geänderte PSD-Datei an und rufen den`save()` Methode, um unsere Änderungen auf die Festplatte zu schreiben.
## Schritt 4: Ebene zur Tonwertkorrektur
Lassen Sie uns den Vorgang für einen anderen Typ von Anpassungsebene wiederholen: die Anpassungsebene „Tonwertkorrektur“. 
### Laden Sie die PSD-Datei mit der Ebenenanpassungsebene
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
Wie zuvor laden wir die PSD-Datei, die unsere Tonwertkorrekturebene enthält. 
### Durch Ebenen und Ebenen iterieren
Als Nächstes durchlaufen wir die Ebenen erneut, genau wie zuvor, aber jetzt arbeiten wir mit einer anderen PSD-Datei.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
Dieser Code funktioniert ähnlich wie die vorherige Iteration. Er sucht in der aktuellen PSD-Datei nach Anpassungsebenen, sodass wir alle verfügbaren Anpassungen anwenden können.
## Speichern Sie die Ebenenanpassungsebene im PSD-Format
Abschließend speichern wir diese neue Datei, nachdem wir die Anpassungen vorgenommen haben.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
Jetzt haben wir die Tonwertkorrekturebene erfolgreich verarbeitet!
## Abschluss
Herzlichen Glückwunsch! Sie haben gerade gelernt, wie Sie mit Java und der Aspose.PSD-Bibliothek Anpassungsebenen in PSD-Dateien anwenden. Egal, ob Sie Farben optimiert oder Ebenen angepasst haben, Sie verfügen jetzt über die grundlegenden Fähigkeiten, um PSD-Dateien programmgesteuert zu bearbeiten.
Die Verwendung von Aspose.PSD kann Arbeitsabläufe bei der Bildbearbeitung erheblich optimieren und ermöglicht Automatisierung und Anpassung auf eine Weise, die mit herkömmlichen Tools nicht möglich wäre. Zögern Sie nicht, die Bibliothek weiter zu erkunden und mit verschiedenen Ebenentypen zu experimentieren, um zu sehen, welche kreativen Möglichkeiten sich bieten.
## Häufig gestellte Fragen
### Was ist die Aspose.PSD-Bibliothek?
Aspose.PSD ist eine Bibliothek, die es Entwicklern ermöglicht, Photoshop-PSD-Dateien in Java-Anwendungen zu laden, zu bearbeiten und zu speichern.
### Kann ich Aspose.PSD kostenlos nutzen?
 Ja! Aspose bietet eine kostenlose Testversion an, mit der Sie die Bibliothek erkunden können. Sie können sich anmelden[Hier](https://releases.aspose.com/).
### Muss Photoshop installiert sein, um Aspose.PSD zu verwenden?
Nein, Sie benötigen kein Photoshop. Aspose.PSD arbeitet unabhängig und bearbeitet PSD-Dateien programmgesteuert.
### Wo finde ich Dokumentation für Aspose.PSD?
Sie können die Dokumentationsseite besuchen[Hier](https://reference.aspose.com/psd/java/) um Funktionen, Klassen und Methoden zu erkunden.
### Wie erhalte ich Support für Aspose-Produkte?
 Sie erreichen den Support über das[Aspose-Forum](https://forum.aspose.com/c/psd/34) wo Sie Fragen stellen und Lösungen finden können.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
