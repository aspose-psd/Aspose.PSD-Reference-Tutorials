---
title: Fügen Sie mit Java eine Kurvenanpassungsebene in PSD hinzu
linktitle: Fügen Sie mit Java eine Kurvenanpassungsebene in PSD hinzu
second_title: Aspose.PSD Java API
description: In diesem ausführlichen Tutorial erfahren Sie, wie Sie mit Aspose.PSD für Java einer PSD-Datei eine Ebene zur Kurvenanpassung hinzufügen. Verbessern Sie Ihre Bilder ganz einfach.
type: docs
weight: 11
url: /de/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---
## Einführung
Sind Sie beim Bearbeiten von Bildern im PSD-Format schon einmal ins Stocken geraten? Egal, ob Sie angehender Grafikdesigner oder erfahrener Profi sind, die Arbeit mit Photoshop-Dateien kann sich manchmal wie ein Labyrinth anfühlen. Glücklicherweise gibt es ein Tool, das diesen Vorgang vereinfacht – Aspose.PSD für Java. In diesem Tutorial erfahren Sie, wie Sie mit Aspose.PSD einer PSD-Datei eine Ebene zur Kurvenanpassung hinzufügen, um Ihre Bildbearbeitungsaufgaben einfacher und effizienter zu gestalten. Mit einer Schritt-für-Schritt-Anleitung können Sie Ihre Bilder wie ein Profi verbessern, ohne sich in den Komplexitäten zu verlieren, die traditionell mit der Bildbearbeitung verbunden sind.
## Voraussetzungen
Bevor wir uns in den Code vertiefen, stellen wir sicher, dass Sie alles bereit haben. Hier sind die Voraussetzungen, die Sie benötigen:
1. Java Development Kit (JDK): Sie müssen JDK auf Ihrem Computer installiert haben. Stellen Sie sicher, dass es die neueste Version ist, um optimale Kompatibilität zu gewährleisten.
2. Aspose.PSD für Java-Bibliothek: Um PSD-Dateien zu bearbeiten, müssen Sie die Aspose.PSD-Bibliothek herunterladen und in Ihr Projekt einbinden. Sie können sie herunterladen[Hier](https://releases.aspose.com/psd/java/).
3. Eine IDE: Verwenden Sie zum Schreiben Ihres Codes eine beliebige Java-IDE wie IntelliJ IDEA, Eclipse oder sogar einen einfachen Texteditor.
4. Grundlegende Kenntnisse in Java: Wenn Sie mit der Java-Programmierung vertraut sind, können Sie problemlos mitmachen.
Alles erledigt? Super! Kommen wir zum spaßigen Teil.
## Pakete importieren
Als Erstes müssen Sie die erforderlichen Pakete importieren. So geht's:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
```
Indem Sie diese Pakete importieren, teilen Sie Ihrer Java-Anwendung mit, welche Klassen sie zum Bearbeiten von PSD-Dateien und insbesondere zum Arbeiten mit Kurvenanpassungsebenen benötigt.
Nachdem wir nun alles eingerichtet haben, wollen wir den Code aufschlüsseln und Schritt für Schritt ansehen, wie eine Ebene zur Kurvenanpassung hinzugefügt wird.
## Schritt 1: Definieren Sie Ihr Datenverzeichnis
Der erste Schritt besteht darin, zu bestimmen, wo Ihre PSD-Dateien gespeichert werden. Legen Sie ein Verzeichnis fest, um alles organisiert zu halten.
```java
String dataDir = "Your Document Directory"; // Aktualisieren Sie diesen Pfad
```
 Denken Sie an`dataDir`als Ihr Arbeitsbereich; hier geschieht die ganze Magie! Ersetzen Sie unbedingt`Your Document Directory` durch den tatsächlichen Pfad, in dem sich Ihre PSD-Dateien befinden oder befinden werden.
## Schritt 2: Laden Sie Ihre PSD-Datei
Als nächstes müssen Sie die PSD-Datei laden, die Sie bearbeiten möchten. Dies geschieht mit dem folgenden Code:
```java
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
```
 In diesem Codeausschnitt`sourceFileName` verweist auf die ursprüngliche PSD-Datei, während`psdPathAfterChange` ist der Ort, an dem Sie Ihre geänderte Datei speichern. Vergessen Sie nicht, anzuhängen`.psd` später im Code.
## Schritt 3: Über Ebenen iterieren
Jetzt ist es an der Zeit, sich in die Ebenen Ihrer PSD-Datei zu vertiefen. Wir werden jede Ebene durchgehen und nach Ebenen zur Kurvenanpassung suchen.
```java
for (int j = 1; j < 2; j++) {
    String fileName = sourceFileName + ".psd";
    PsdImage im = (PsdImage) Image.load(fileName);
    
    for(int k = 0; k < im.getLayers().length; k++) {
        if (im.getLayers()[k] instanceof CurvesLayer) {
            // Hier wird die Kurvenebenenverarbeitung angezeigt
        }
    }
}
```
Hier ist eine Aufschlüsselung der Geschehnisse:
-  Wir laden zunächst die PSD-Datei in ein`PsdImage` Objekt mit dem Namen`im`.
-  Als nächstes durchlaufen wir alle Ebenen im Bild mit`im.getLayers().length` . Dadurch erhalten wir Zugriff auf jede Schicht und können prüfen, ob es sich um eine`CurvesLayer`.
## Schritt 4: Kurvenebene ändern
 Innerhalb der Schleife, die prüft, ob`CurvesLayer`fügen Sie Logik zum Ändern der Kurven hinzu. So gehen Sie dabei vor:
```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager) curvesLayer.getCurvesManager();
    for (int i = 10; i < 50; i++) {
        manager.setValueInPosition(0, (byte) i, (byte) (15 + (i * 2)));
    }
} else {
    CurvesContinuousManager manager = (CurvesContinuousManager) curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte) 0, (byte) 50, (byte) 100);
    manager.addCurvePoint((byte) 0, (byte) 150, (byte) 130);
}
```
In diesem Segment:
- Wir prüfen, ob die Kurvenebene einen diskreten oder einen kontinuierlichen Manager verwendet.
- Wenn es sich um einen diskreten Manager handelt, legen wir für jede Position neue Werte von 10 bis 49 fest.
- Umgekehrt fügen wir bei einem kontinuierlichen Manager Kurvenpunkte hinzu, um die Kurven nach Bedarf anzupassen.
## Schritt 5: Speichern Sie die geänderte PSD
Nachdem Sie Ihre Anpassungen vorgenommen haben, besteht der letzte Schritt darin, die geänderte PSD-Datei zu speichern.
```java
im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
```
 Diese Zeile speichert die angepasste PSD in dem Pfad, den Sie zuvor definiert haben. Bei jeder Änderung wird eine neue Datei mit einem anderen Suffix basierend auf dem Schleifenzähler erstellt.`j`.
## Abschluss
Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.PSD für Java einer PSD-Datei eine Ebene zur Kurvenanpassung hinzufügen. Mit nur wenigen Schritten können Sie Ihre Bilder verbessern und nach Ihren Wünschen bearbeiten. Die Flexibilität dieser Bibliothek macht sie zu einem unschätzbaren Werkzeug für jeden, der mit PSD-Dateien arbeitet. Experimentieren Sie jetzt mit verschiedenen Kurven und lassen Sie Ihrer Kreativität freien Lauf.
## Häufig gestellte Fragen
### Was ist Aspose.PSD?
Aspose.PSD ist eine Bibliothek zur Verarbeitung von Photoshop-PSD-Dateien in verschiedenen Programmiersprachen, einschließlich Java.
### Kann ich Aspose.PSD kostenlos nutzen?
 Ja, Aspose bietet eine kostenlose Testversion an, die Sie vor dem Kauf ausprobieren können. Überprüfen Sie die[kostenlose Testversion herunterladen](https://releases.aspose.com/) Link.
### Ist es notwendig, Photoshop installiert zu haben?
Nein, Sie müssen Photoshop nicht auf Ihrem Computer installiert haben, um mit Aspose.PSD zu arbeiten.
### Kann ich andere Ebenen als die Einstellungsebene für Kurven bearbeiten?
Auf jeden Fall! Aspose.PSD ermöglicht die Bearbeitung verschiedener Ebenentypen in PSD-Dateien.
### Wo finde ich weitere Dokumentation?
 Ausführliche Dokumentation finden Sie unter[Aspose.PSD für Java-Dokumente](https://reference.aspose.com/psd/java/).