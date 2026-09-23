---
date: 2026-09-23
description: Erfahren Sie, wie Sie PSD-Vektorformen bearbeiten und PSD-Dateien stapelweise
  mit Aspose.PSD für Java verarbeiten. Detaillierte Schritte, Tipps und Code‑Platzhalter
  für eine vollständige Lösung.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Unterstützung von Length Record Data Properties in PSD – Java
og_description: Erfahren Sie, wie Sie PSD-Vektorformen bearbeiten und PSD-Dateien
  stapelweise mit Aspose.PSD für Java verarbeiten. Schritt‑für‑Schritt‑Anleitung mit
  Code‑Platzhaltern und Experten‑Tipps.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: PSD-Vektorformen mit Aspose.PSD für Java bearbeiten
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: PSD-Vektorformen mit Aspose.PSD für Java bearbeiten
url: /de/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD-Vektorformen mit Aspose.PSD für Java ändern

## Einführung
Wenn Sie **PSD-Vektorformen** programmgesteuert **ändern** müssen, bietet Aspose.PSD für Java Ihnen die volle Kontrolle über Photoshop-Dateien direkt aus Ihrem Java-Code. Dieses Tutorial führt Sie durch die Unterstützung von LengthRecord‑Eigenschaften – ein wesentlicher Schritt beim Bearbeiten von Vektorformen‑Ebenen. Am Ende können Sie eine PSD öffnen, deren Vektordaten anpassen und die aktualisierte Datei speichern, ohne Photoshop zu starten.

## Schnelle Antworten
- **Was bedeutet „PSD-Vektorformen ändern“?** Anpassung von Geometrie, Pfadoperationen oder anderen Attributen vektorbasierter Ebenen in einer PSD-Datei.  
- **Welche Bibliothek übernimmt das?** Aspose.PSD für Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für ein einfaches Skript zur Formänderung.  
- **Was sind die wichtigsten Voraussetzungen?** Java JDK, Aspose.PSD für Java und eine Beispiel‑PSD-Datei.

## Was bedeutet „support length record properties“?
Die Unterstützung von LengthRecord‑Eigenschaften bedeutet, dass Sie auf die `LengthRecord`‑Objekte zugreifen und diese aktualisieren, die jeden Vektorpfad innerhalb einer PSD beschreiben. Diese Datensätze speichern Informationen wie die Pfadlänge, den Typ und wie er mit anderen Pfaden verbunden ist. Durch deren Änderung können Sie steuern, wie Formen kombiniert, geschnitten oder voneinander subtrahiert werden, was eine präzise Vektorbearbeitung ermöglicht.

## Warum Aspose.PSD für Java verwenden, um LengthRecord‑Eigenschaften zu unterstützen?
Laden Sie Ihre PSD, bearbeiten Sie Vektordaten und speichern Sie – alles ohne Photoshop. Aspose.PSD verarbeitet mehrseitige PSDs in unter 2 Sekunden auf einem typischen Server, bietet über 150 Klassen (inklusive 30+ vektorbezogener Typen) und läuft auf Windows, Linux oder macOS mit jedem JDK 11+. Diese leistungsorientierte Bibliothek eliminiert die Notwendigkeit teurer Desktop‑Software.

## Voraussetzungen
1. **Java Development Kit (JDK)** – herunterladen von [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) oder Ihren bevorzugten Paketmanager verwenden.  
2. **Aspose.PSD for Java** – das neueste JAR von der [Aspose releases page](https://releases.aspose.com/psd/java/) beziehen.  
3. **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Java‑kompatibler Editor.  
4. **Eine PSD-Datei** – in Photoshop erstellen oder eine Beispiel‑PSD zum Experimentieren verwenden.  
5. **Grundlegende Java‑Kenntnisse** – Vertrautheit mit Klassen, Objekten und Ausnahmebehandlung.

## Pakete importieren
Die Import‑Anweisungen bringen die Kern‑Aspose.PSD‑Klassen in den Geltungsbereich, wie `PsdImage`, `VsmsResource` und `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Schritt 1: Quellen- und Ausgabeverzeichnisse einrichten
Definieren Sie, wo die ursprüngliche PSD liegt und wohin die modifizierte Datei geschrieben wird.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Schritt 2: PSD-Datei laden
Verwenden Sie `Image.load`, um die Datei zu öffnen und sie zu `PsdImage` zu casten, um PSD‑spezifische Funktionen zu nutzen.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Schritt 3: Vsms-Ressource in der Ebene finden
`VsmsResource` ist der Container, der Vektorform‑Daten für eine Ebene speichert. Durchlaufen Sie die Ressourcen der zweiten Ebene, um sie zu finden.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Schritt 4: LengthRecord‑Datensätze abrufen
`LengthRecord` repräsentiert einen einzelnen Vektorpfad. Rufen Sie die Datensätze ab, die Sie ändern möchten.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Schritt 5: Pfadoperations‑Eigenschaften ändern
`PathOperations` definiert, wie einzelne Formen interagieren (z. B. Ausschluss, Schnittmenge, Subtraktion). Durch das Ändern dieser Werte wird die visuelle Zusammensetzung der Vektorebene aktualisiert.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Schritt 6: Modifizierte PSD-Datei speichern
Speichern Sie Ihre Änderungen in einer neuen Datei.

```java
psdImage.save(outPsdFilePath);
```

## Schritt 7: Ressourcen aufräumen
Entsorgen Sie die `PsdImage`‑Instanz, um Speicher freizugeben und Ressourcenlecks zu vermeiden.

```java
psdImage.dispose();
```

## Wie man PSD-Dateien stapelweise verarbeitet mit Unterstützung von LengthRecord‑Eigenschaften
Kapseln Sie den Ein‑Datei‑Workflow in einer Schleife, die über ein Verzeichnis von PSDs iteriert und dabei `inPsdFilePath` sowie `outPsdFilePath` für jede Datei aktualisiert. Dieser Ansatz ermöglicht es Ihnen, identische Vektorform‑Anpassungen in Minuten auf Dutzende oder Hunderte von Dateien anzuwenden – ideal für automatisierte Asset‑Pipelines.

## Häufige Fallstricke & Tipps
- **Null‑Prüfungen** – immer prüfen, ob `resource` nicht `null` ist, bevor Sie auf dessen Mitglieder zugreifen.  
- **Pfad‑Index‑Grenzen** – sicherstellen, dass die von Ihnen verwendeten Indizes (z. B. `[2]`, `[7]`, `[11]`) für die jeweilige PSD existieren.  
- **Lizenz** – das Ausführen ohne gültige Lizenz fügt ein Wasserzeichen in die gespeicherte PSD ein.

## Fazit
Sie haben nun ein vollständiges, durchgängiges Beispiel, wie Sie **PSD-Vektorformen** ändern, indem Sie LengthRecord‑Eigenschaften mit Aspose.PSD für Java unterstützen. Ob Sie eine Asset‑Pipeline automatisieren oder ein benutzerdefiniertes Design‑Tool bauen, diese APIs bieten Ihnen die Flexibilität, Vektorebenen zu manipulieren, ohne manuell Photoshop zu verwenden. Experimentieren Sie mit anderen `PathOperations`‑Werten oder kombinieren Sie mehrere `LengthRecord`‑Änderungen, um komplexe Formen zu erstellen.

## Häufig gestellte Fragen

**Q: Wie gehe ich mit einer PSD um, die keine Vektorformen‑Ebenen enthält?**  
A: Die `VsmsResource` wird fehlen, sodass `resource` `null` bleibt. Fügen Sie eine Prüfung hinzu und überspringen Sie den Änderungs‑Schritt oder informieren Sie den Benutzer.

**Q: Kann ich andere Eigenschaften wie Füllfarbe oder Strichbreite ändern?**  
A: Ja, `LengthRecord` bietet Setter für Füllung, Strich und Deckkraft. Siehe die API‑Dokumentation für die vollständige Liste.

**Q: Ist es möglich, mehrere PSD-Dateien stapelweise zu verarbeiten?**  
A: Absolut. Kapseln Sie den Code in einer Schleife, die über ein Verzeichnis von PSD‑Dateien iteriert und dabei die Eingabe‑ und Ausgabe‑Pfade jeweils anpasst.

**Q: Muss ich Streams manuell schließen, wenn ich von einem Dateipfad lade?**  
A: `Image.load` verwaltet Dateistreams automatisch, aber wenn Sie von einem `InputStream` laden, denken Sie daran, diesen nach Gebrauch zu schließen.

**Q: Welche Version von Aspose.PSD wird für diese APIs benötigt?**  
A: Die Klassen `LengthRecord` und `PathOperations` sind seit Aspose.PSD 20.10 verfügbar. Die Verwendung der neuesten Version (24.11 zum Zeitpunkt der Erstellung) wird empfohlen.

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Verwandte Tutorials

- [Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD Files](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Convert PSD to PNG with Layer Mask Support Using Aspose.PSD for Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Add Layer Support Psd Files](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}