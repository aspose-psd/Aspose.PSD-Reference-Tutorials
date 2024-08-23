---
title: Helligkeit und Kontrast in PSD-Ebenen verwalten – Java
linktitle: Helligkeit und Kontrast in PSD-Ebenen verwalten – Java
second_title: Aspose.PSD Java API
description: Lernen Sie, Helligkeit und Kontrast in PSD-Dateien mühelos mit Aspose.PSD für Java anzupassen. Ideal für Entwickler und Grafikdesigner.
type: docs
weight: 21
url: /de/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
---
## Einführung

Sind Sie Grafikdesigner oder Entwickler und arbeiten häufig mit PSD-Dateien (Photoshop Document)? Müssen Sie die Helligkeit und den Kontrast von Ebenen in diesen Dateien anpassen, wissen aber nicht, wie Sie diese Aufgabe mit Java automatisieren können? Dann haben Sie Glück! In diesem Tutorial erfahren Sie, wie Sie Helligkeit und Kontrast in PSD-Ebenen mithilfe der Aspose.PSD-Bibliothek für Java verwalten. Dies spart Ihnen nicht nur Zeit, sondern verbessert auch Ihren kreativen Workflow. Krempeln wir die Ärmel hoch und legen los!

## Voraussetzungen

Bevor wir uns auf diese spannende Reise der Bearbeitung von PSD-Dateien mit Java begeben, müssen Sie sicherstellen, dass Sie alles, was Sie brauchen, richtig eingerichtet haben. Folgendes benötigen Sie, um dieses Tutorial erfolgreich abzuschließen:

1.  Java Development Kit (JDK): Stellen Sie sicher, dass auf Ihrem Computer JDK 8 oder höher installiert ist. Sie können es hier herunterladen:[Website von Oracle](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. Aspose.PSD für Java-Bibliothek: Um mit PSD-Dateien arbeiten zu können, benötigen Sie die Aspose.PSD-Bibliothek. Sie können die neueste Version von der[Veröffentlichungsseite](https://releases.aspose.com/psd/java/).

3. IDE Ihrer Wahl: Zum Schreiben und Ausführen Ihres Java-Codes wird eine integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA, Eclipse oder NetBeans bevorzugt.

4. Grundkenntnisse in Java: Wenn Sie mit der Java-Programmierung vertraut sind, können Sie die Codefragmente besser verstehen, mit denen wir arbeiten werden.

Sobald Sie diese Voraussetzungen erfüllt haben, können wir fortfahren. Nehmen Sie jetzt Ihren bevorzugten Code-Editor zur Hand und legen Sie los!

## Pakete importieren

Der erste Schritt auf unserer Programmierreise besteht darin, die erforderlichen Pakete zu importieren. Bevor Sie die von Aspose.PSD bereitgestellten Funktionen nutzen können, müssen Sie sicherstellen, dass sich die Bibliothek in Ihrem Klassenpfad befindet. So können Sie das tun:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

Durch Ausführen dieser Schritte schaffen Sie die Voraussetzung für die effektive Arbeit mit PSD-Dateien!

Nachdem wir nun alles eingerichtet haben, können wir mit dem Kern des Tutorials beginnen: dem Anpassen von Helligkeit und Kontrast in PSD-Ebenen. Wir unterteilen diesen Vorgang in klare Schritte, damit Sie ihn problemlos nachvollziehen können.

## Schritt 1: Definieren Sie Ihr Dokumentverzeichnis

Definieren Sie zunächst das Verzeichnis, in dem sich Ihre PSD-Dateien befinden. Dieser Schritt hilft Ihnen dabei, Ihre Dateien effizient zu organisieren.

```java
String dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` durch den tatsächlichen Pfad zu Ihrem PSD-Dateiverzeichnis.

## Schritt 2: Quell- und Zieldateinamen angeben

Als Nächstes müssen Sie den Quelldateinamen Ihrer PSD und die Zieldatei angeben, in der die bearbeitete PSD gespeichert wird.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

 In diesem Beispiel gehen wir davon aus, dass Sie eine PSD-Datei mit dem Namen`BrightnessContrastModern.psd` in Ihrem Verzeichnis.

## Schritt 3: Laden Sie die PSD-Datei

Jetzt ist es an der Zeit, die PSD-Datei in Ihre Anwendung zu laden, damit Sie sie bearbeiten können.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

 Diese Codezeile erstellt eine Instanz von`PsdImage` stellt Ihre PSD-Datei dar. Damit können Sie nun auf alle Ebenen der PSD zugreifen.

## Schritt 4: Durch Schichten iterieren

Im nächsten Schritt durchlaufen Sie jede Ebene Ihrer PSD-Datei, um Helligkeits- und Kontrasteinstellungen zu finden und zu bearbeiten.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

 Der`for` Schleife durchläuft jede Ebene des PSD. Wir prüfen, ob eine Ebene eine Instanz von`BrightnessContrastLayer`Dies ist wichtig, um sicherzustellen, dass Sie nur versuchen, Helligkeit und Kontrast auf den richtigen Ebenen zu ändern.

## Schritt 5: Helligkeit und Kontrast anpassen

 Innerhalb der Schleife können Sie nun die Helligkeit und den Kontrast für jede`BrightnessContrastLayer`. 

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

 In diesem Beispiel setzen wir Helligkeit und Kontrast auf`50`. Sie können diese Werte Ihren Anforderungen entsprechend anpassen. Eine höhere Zahl erhöht die Helligkeit/den Kontrast, eine niedrigere Zahl verringert sie/ihn.

## Schritt 6: Änderungen speichern

Der letzte Schritt besteht darin, Ihre Änderungen an der PSD-Datei zu speichern. Sie möchten das geänderte Bild an das angegebene Ziel zurückschreiben.

```java
im.save(psdPathAfterChange);
```

Diese Codezeile speichert die bearbeitete PSD-Datei mit Ihren neuen Helligkeits- und Kontrasteinstellungen.

## Abschluss

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie Helligkeit und Kontrast in PSD-Ebenen mit Aspose.PSD für Java verwalten. Durch die Automatisierung dieser Anpassungen verbessern Sie nicht nur Ihren Arbeitsablauf, sondern steigern auch Ihre Produktivität. Wenn Sie diese Bilder das nächste Mal optimieren müssen, sind Sie mit Ihren neuen Java-Kenntnissen gut gerüstet, um die Aufgabe anzugehen. Also, was werden Sie als Nächstes erstellen?

## Häufig gestellte Fragen

### Was ist Aspose.PSD für Java?
Aspose.PSD für Java ist eine Bibliothek, die es Entwicklern ermöglicht, PSD-Dateien programmgesteuert zu bearbeiten und so Photoshop-bezogene Aufgaben zu automatisieren.

### Kann ich die Helligkeit und den Kontrast mehrerer Ebenen gleichzeitig anpassen?
 Ja, der in diesem Tutorial verwendete Ansatz durchläuft alle Ebenen im PSD, sodass Sie mehrere`BrightnessContrastLayer` Instanzen.

### Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?
 Sie können eine temporäre Lizenz erhalten, indem Sie die[Seite mit der temporären Lizenz](https://purchase.aspose.com/temporary-license/).

### Gibt es eine kostenlose Testversion für Aspose.PSD?
 Ja, Sie können eine kostenlose Testversion von Aspose.PSD herunterladen von der[Veröffentlichungsseite](https://releases.aspose.com/).

### Wo finde ich zusätzliche Unterstützung für Aspose.PSD?
 Sie können Unterstützung für Aspose.PSD auf deren[Support-Forum](https://forum.aspose.com/c/psd/34).