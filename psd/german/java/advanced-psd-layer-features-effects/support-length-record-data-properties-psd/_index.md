---
title: Unterstützte Längendatensatz-Dateneigenschaften in PSD – Java
linktitle: Unterstützte Längendatensatz-Dateneigenschaften in PSD – Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie PSD-Dateien mit Längendatensatz-Dateneigenschaften in Java mithilfe von Aspose.PSD bearbeiten. Folgen Sie dieser Schritt-für-Schritt-Anleitung für alle Einzelheiten.
type: docs
weight: 14
url: /de/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
---
## Einführung
Haben Sie schon einmal mit Photoshop-Dateien gearbeitet und wollten Ebenen oder Formen programmgesteuert bearbeiten? Wenn ja, sind Sie auf die Schönheit der Aspose.PSD-Bibliothek für Java gestoßen. Dieses leistungsstarke Tool ermöglicht Entwicklern die nahtlose Interaktion mit PSD-Dateien und deren Änderung über Java-Code. Im heutigen Artikel werden wir uns damit befassen, wie man mit dieser Bibliothek Dateneigenschaften für Längendatensätze in einer PSD-Datei unterstützt. 
Egal, ob Sie ein erfahrener Java-Entwickler sind oder gerade erst anfangen, dieser Leitfaden führt Sie Schritt für Schritt durch alles, was Sie wissen müssen. Am Ende können Sie eine PSD-Datei öffnen, ihre Vektorformeigenschaften ändern und Ihre Änderungen speichern – und das alles, ohne Ihre komfortable Java-Umgebung verlassen zu müssen. Krempeln Sie die Ärmel hoch und legen Sie los!
## Voraussetzungen
Bevor wir beginnen, müssen Sie ein paar Dinge bereitlegen. Wenn Sie alles bereit haben, läuft der Prozess reibungsloser, und niemand mag Hektik in letzter Minute! Folgendes brauchen Sie:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass das JDK auf Ihrem Computer installiert ist. Sie können es hier herunterladen:[Website von Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) oder verwenden Sie einen Paketmanager.
2.  Aspose.PSD für Java-Bibliothek: Sie müssen die Aspose.PSD für Java-Bibliothek herunterladen und in Ihr Projekt einbinden. Sie erhalten sie von der[Aspose-Veröffentlichungsseite](https://releases.aspose.com/psd/java/).
3. IDE: Verwenden Sie für eine bessere Codeverwaltung eine integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA, Eclipse oder eine beliebige Java-IDE Ihrer Wahl.
4. Eine PSD-Datei: Für dieses Tutorial benötigen Sie eine PSD-Datei zum Arbeiten. Sie können eine in Adobe Photoshop erstellen oder eine Beispiel-PSD herunterladen.
5. Grundlegende Java-Kenntnisse: Wenn Sie mit der Java-Syntax vertraut sind, können Sie den Anweisungen problemlos folgen.
## Pakete importieren
Nachdem Sie nun alle Voraussetzungen eingerichtet haben, besteht der nächste Schritt darin, die erforderlichen Pakete zu importieren. Dieser Schritt ist entscheidend, um Zugriff auf die Klassen und Methoden zu erhalten, die wir verwenden werden. Nachfolgend finden Sie ein Beispiel für den Import der erforderlichen Pakete in Ihr Java-Projekt:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```
Mit diesen Importen sind Sie bereit, mit der Bearbeitung von PSD-Dateien loszulegen!

## Schritt 1: Richten Sie Ihre Quell- und Ausgabeverzeichnisse ein
Bevor wir irgendwelche Dateien laden, legen wir fest, woher unsere PSD-Eingabedatei kommt und wo wir die geänderte Datei speichern möchten. Passen Sie die Verzeichnispfade entsprechend Ihrem lokalen Computer an.
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```
## Schritt 2: Laden Sie die PSD-Datei
 Zeit, die PSD-Datei zu laden! Dafür verwenden wir die`Image.load` Methode aus der Aspose.PSD-Bibliothek. Mit dieser Methode können wir die PSD-Datei öffnen und auf ihre Ebenen und Ressourcen zugreifen.
```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```
Es ist, als würden Sie ein Buch öffnen – Sie können durch die Seiten (Ebenen und Ressourcen) blättern.
## Schritt 3: Suchen Sie die Vsms-Ressource in der Ebene
Als nächstes müssen wir die spezifische VsmsResource in unserer PSD-Datei finden. Diese Ressourcen enthalten die Daten für Vektorformebenen. Hier geschieht die Magie! In diesem Snippet durchlaufen wir die Ressourcen der Ebene, um diese Ressource zu finden.
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```
Wie bei einer Schatzsuche durchsuchen Sie die Ebenen, um die wertvollen Vektordaten zu finden!
## Schritt 4: Zugriff auf Längendatensätze
Sobald wir die VsmsResource haben, können wir die LengthRecord-Objekte extrahieren. Jeder LengthRecord stellt einen Pfad innerhalb der Vektorformen dar. Hier greifen wir auf drei LengthRecords zu, um ihre Eigenschaften zu bearbeiten.
```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```
Es ist, als würden Sie auswählen, welche Teile eines Gemäldes Sie retuschieren möchten!
## Schritt 5: Pfadoperationseigenschaften ändern
Jetzt kommt der spaßige Teil – das Ändern der Pfadeigenschaften! Hier ermöglicht die Methode setPathOperations das Ändern der Art und Weise, wie die Formen miteinander interagieren. Wir können Operationen festlegen, wie beispielsweise das Ausschließen überlappender Bereiche oder das Subtrahieren der vorderen Form von der hinteren.
```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```
Stellen Sie es sich so vor, als würden Sie die Schichten eines Kuchens anordnen – jede Schicht reagiert anders, je nachdem, wie Sie sie schneiden!
## Schritt 6: Speichern Sie die geänderte PSD-Datei
Nachdem Sie die erforderlichen Änderungen vorgenommen haben, besteht der nächste Schritt darin, Ihre geänderte PSD-Datei zu speichern. Hier zahlt sich all Ihre harte Arbeit aus. 
```java
psdImage.save(outPsdFilePath);
```
Ihr Meisterwerk ist jetzt ordentlich verpackt, damit die ganze Welt es sehen kann!
## Schritt 7: Ressourcen bereinigen
Abschließend müssen Sie unbedingt die verwendeten Objekte entsorgen, um Speicher und Ressourcen freizugeben.
```java
psdImage.dispose();
```
Stellen Sie es sich wie das Aufräumen Ihres Arbeitsplatzes nach einem Kunstprojekt vor – stellen Sie sicher, dass alles ordentlich und sauber ist!
## Abschluss
Da haben Sie es! Sie haben gerade ein umfassendes Tutorial zur Unterstützung von Längendatensatz-Dateneigenschaften in PSD-Dateien mit Aspose.PSD für Java abgeschlossen. Vom Laden der Datei über das Ändern von Formeigenschaften bis hin zum Speichern des Endprodukts – jeder Schritt enthüllt die Leistungsfähigkeit dieser Bibliothek. Egal, ob Sie an kreativen Projekten arbeiten oder grafische Assets automatisieren, Aspose.PSD eröffnet eine ganz neue Welt der Möglichkeiten. Bereit, loszulegen? Tauchen Sie ein in Ihre PSD-Dateien und entfesseln Sie Ihre Kreativität!
## Häufig gestellte Fragen
### Was ist Aspose.PSD für Java?
Aspose.PSD für Java ist eine Bibliothek, die es Entwicklern ermöglicht, Photoshop-PSD-Dateien programmgesteuert mit Java zu bearbeiten und zu bearbeiten.
### Kann ich Aspose.PSD in einem kostenlosen Projekt verwenden?
Ja, Sie können die Bibliothek mit einer auf der Aspose-Website verfügbaren Testversion kostenlos ausprobieren.
### Welche Arten von Änderungen kann ich an PSD-Dateien vornehmen?
Sie können Ebenen, Formen, Texte, Pfadoperationen und vieles mehr in PSD-Dateien bearbeiten.
### Ist Aspose.PSD mit anderen Programmiersprachen kompatibel?
Ja, Aspose bietet verschiedene Bibliotheken für unterschiedliche Programmiersprachen, darunter .NET und Python.
### Wo finde ich die Dokumentation für Aspose.PSD?
 Sie können auf die vollständige Dokumentation zugreifen[Hier](https://reference.aspose.com/psd/java/).