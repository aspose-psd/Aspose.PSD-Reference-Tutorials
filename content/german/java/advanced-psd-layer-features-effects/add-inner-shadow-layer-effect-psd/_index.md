---
title: Fügen Sie mit Java einen inneren Schattenebeneneffekt in PSD hinzu
linktitle: Fügen Sie mit Java einen inneren Schattenebeneneffekt in PSD hinzu
second_title: Aspose.PSD Java API
description: Erfahren Sie in diesem Schritt-für-Schritt-Tutorial, einschließlich Tipps und Best Practices, wie Sie mit Aspose.PSD für Java PSD-Dateien einen inneren Schatteneffekt hinzufügen.
type: docs
weight: 12
url: /de/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
---
## Einführung
Sind Sie bereit, in die Welt der Grafikdesign-Programmierung einzutauchen? Wenn Sie schon immer PSD-Dateien programmgesteuert bearbeiten wollten, sind Sie hier richtig! Heute werden wir untersuchen, wie man mit Aspose.PSD für Java einem PSD (Photoshop-Dokument) einen inneren Schattenebeneneffekt hinzufügt. Diese leistungsstarke Bibliothek ermöglicht Java-Entwicklern die effiziente Arbeit mit PSD-Dateien und ermöglicht eine Reihe von Bildbearbeitungen, von einfachen Bearbeitungen bis hin zu komplexen Effekten.
## Voraussetzungen
Bevor wir uns mit der Programmierung befassen, bereiten wir Sie zunächst vor. Folgendes müssen Sie bereitstellen:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist. Es ist für das Kompilieren und Ausführen von Java-Code unerlässlich. Wenn Sie es noch nicht haben, können Sie es von der[Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD-Bibliothek: Sie benötigen Zugriff auf die Aspose.PSD-Bibliothek. Sie können sie ganz einfach von der[Aspose-Veröffentlichungen](https://releases.aspose.com/psd/java/). Es ist ein robustes Tool zur Verarbeitung von PSD-Dateien. Besorgen Sie sich also unbedingt die neueste Version.
3. Eine integrierte Entwicklungsumgebung (IDE): Sie können zwar jeden beliebigen Texteditor verwenden, es empfiehlt sich jedoch die Verwendung einer IDE wie IntelliJ IDEA, Eclipse oder NetBeans. Diese bieten hilfreiche Funktionen wie Syntaxhervorhebung und Debugging-Tools.
4. Grundlegende Java-Kenntnisse: Wenn Sie mit den Java-Grundlagen wie Variablen, Klassen und Methoden vertraut sind, können Sie problemlos mit den Schritten weitermachen.
5. Beispiel-PSD-Datei: Um den Code zu testen, stellen Sie sicher, dass Sie eine Beispiel-PSD-Datei haben. Sie können eine in Adobe Photoshop erstellen oder ein kostenloses Beispiel online herunterladen.
## Pakete importieren
Sobald Sie alles eingerichtet und einsatzbereit haben, besteht der erste Schritt darin, die erforderlichen Pakete in Ihre Java-Klasse zu importieren. Dies ist für den Zugriff auf die Aspose.PSD-Funktionen von entscheidender Bedeutung. 
## Erforderliche Pakete importieren
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
In diesen Zeilen fügen wir die benötigten Klassen aus der Aspose-Bibliothek ein.
Nachdem wir nun unsere Pakete importiert und unsere Umgebung eingerichtet haben, können wir uns nun mit den Einzelheiten des Codes befassen. Ich werde ihn in überschaubare Schritte aufteilen.
## Schritt 1: Verzeichnisse definieren
In diesem Schritt geben wir an, wo sich unsere Quell-PSD-Datei befindet und wo wir die geänderte Version speichern möchten. 
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
 Ersetzen`"Your Source Directory"` Und`"Your Document Directory"` mit den tatsächlichen Pfaden auf Ihrem Computer. Hier teilen Sie Ihrem Programm mit, wo es nach der PSD-Datei suchen und wo es die neue Version speichern soll.
## Schritt 2: Laden Sie die PSD-Datei
 Als nächstes müssen wir die vorhandene PSD-Datei in ein`PsdImage` Objekt. Wir werden auch die Ladeoptionen so konfigurieren, dass Effekte einbezogen werden.
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
 Hier erstellen wir eine Instanz von`PsdLoadOptions` , richten Sie es so ein, dass Effektressourcen geladen werden, und laden Sie dann unsere Beispiel-PSD-Datei in ein Objekt namens`image`. Es ist, als würde man ein Buch vor dem Lesen öffnen!
## Schritt 3: Zugriff auf die Ebene für den Effekt
Greifen wir nun auf die letzte Ebene in unserer PSD-Datei zu (vorausgesetzt, dies ist die Ebene, auf die wir unseren Effekt anwenden möchten).
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
Diese Zeile greift auf die letzte Ebene unseres PSD-Bildes zu. In Photoshop sind Ebenen wie transparente Blätter, die übereinander gestapelt sind, und das oberste ist oft das, was Sie zuerst sehen.
## Schritt 4: Konfigurieren Sie den Inner Shadow-Effekt
Dieser Codeausschnitt wendet den inneren Schatteneffekt auf unsere Ebene an. 
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
Und hier geschieht die Magie! Dieser Code greift den Schatteneffekt aus den Fülloptionen der Ebene auf und passt seine Eigenschaften an:
- Farbe: Stellt den Schatten auf Grün ein.
- Opazität: Macht es halbtransparent.
- Abstand: Verschiebt den Schatten leicht vom Ebenenrand weg.
- Größe: Bestimmt, wie groß der Schatten ist.
- Winkel: Gibt die Richtung der Lichtquelle an.
- Ausbreitung und Rauschen: Eröffnen Sie kreative Optionen für das Aussehen des Schattens.
## Schritt 5: Speichern Sie die geänderte PSD
Sobald alle Einstellungen angewendet wurden, besteht der nächste Schritt darin, unsere geänderte PSD-Datei zu speichern.
```java
    image.save(destName, new PsdOptions(image));
```
Diese Zeile speichert unsere Änderungen. Die Ausgabedatei heißt`sample_out.psd`, und es enthält alle Effekte, die gerade angewendet wurden. Es ist, als ob Sie in Photoshop nach der Bearbeitung auf „Speichern“ klicken.
## Schritt 6: Ressourcen bereinigen
Schließlich stellen wir sicher, dass alle von uns verwendeten Ressourcen freigegeben werden.
```java
} finally {
    image.dispose();
}
```
 Dies ist eine gute Vorgehensweise, um Speicherlecks zu vermeiden. Durch die Entsorgung der`image` Objekt sorgen wir dafür, dass unsere Anwendung reibungslos und effizient läuft.
## Abschluss
Und da haben Sie es! In nur wenigen einfachen Schritten haben Sie gelernt, wie Sie mit Aspose.PSD für Java Ebenen in einer PSD-Datei einen inneren Schatteneffekt hinzufügen. Diese Bibliothek bietet fantastische Funktionen für alle, die Grafikdesignaufgaben automatisieren oder Bildbearbeitungsfunktionen in ihre Java-Anwendungen integrieren möchten. 

## Häufig gestellte Fragen
### Was ist Aspose.PSD?  
Aspose.PSD ist eine Java-Bibliothek für die Arbeit mit PSD-Dateien, die es Entwicklern ermöglicht, Ebeneneffekte, Masken und Bildeigenschaften programmgesteuert zu bearbeiten.
### Benötige ich Photoshop, um Aspose.PSD zu verwenden?  
Nein, Sie benötigen Photoshop nicht, um Aspose.PSD zu verwenden. Die Bibliothek funktioniert unabhängig zur Bearbeitung von PSD-Dateien.
### Kann ich mehrere Effekte auf dieselbe Ebene anwenden?  
Auf jeden Fall! Sie können mehrere Effekte anwenden, indem Sie auf jeden Effekttyp auf die gleiche Weise zugreifen, wie wir auf den inneren Schatteneffekt zugegriffen haben.
### Ist Aspose.PSD kostenlos?  
Aspose.PSD ist ein kommerzielles Produkt. Sie können jedoch eine kostenlose Testversion von Aspose nutzen.
### Wo finde ich weitere Dokumentation?  
 Eine umfassende Dokumentation zu Aspose.PSD finden Sie hier[Hier](https://reference.aspose.com/psd/java/).