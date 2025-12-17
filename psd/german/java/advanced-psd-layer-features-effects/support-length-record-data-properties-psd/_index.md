---
date: 2025-12-17
description: Erfahren Sie, wie Sie PSD‑Vektorformen ändern können, indem Sie Längenaufzeichnungsdateneigenschaften
  mit Aspose.PSD für Java unterstützen. Schritt‑für‑Schritt‑Anleitung mit Codebeispielen.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Wie man PSD‑Vektorformen bearbeitet – Unterstützung von Length Record Data
  Properties in Java
url: /de/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unterstützung von Length Record Data Properties in PSD – Java

## Einführung
Wenn Sie **PSD-Vektorformen ändern** programmgesteuert benötigen, bietet Ihnen die Aspose.PSD for Java Bibliothek die vollständige Kontrolle über Photoshop-Dateien direkt aus Ihrem Java-Code. In diesem Tutorial führen wir Sie durch alles, was Sie wissen müssen, um Length Record Data Properties zu unterstützen – ein wesentlicher Schritt, wenn Sie Vektorformen‑Ebenen bearbeiten möchten. Am Ende können Sie ein PSD öffnen, seine Vektorformen‑Eigenschaften anpassen und die aktualisierte Datei speichern, ohne Ihre IDE zu verlassen. Lassen Sie uns loslegen!

## Schnelle Antworten
- **Was bedeutet “modify PSD vector shapes”?** Anpassen der Geometrie, Pfadoperationen oder anderer Eigenschaften von vektorbasierten Ebenen in einer PSD-Datei.  
- **Welche Bibliothek übernimmt das?** Aspose.PSD for Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Evaluierung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für ein einfaches Skript zur Formänderung.  
- **Was sind die wichtigsten Voraussetzungen?** Java JDK, Aspose.PSD for Java und eine Beispiel‑PSD-Datei.  

## Was bedeutet “modify PSD vector shapes”?
Das Ändern von PSD-Vektorformen beinhaltet das Ändern der zugrunde liegenden Vektor-Pfaddaten – wie Length Records und Pfadoperationen – sodass das visuelle Erscheinungsbild der Formen entsprechend aktualisiert wird. Dies ist besonders nützlich für automatisierte Grafik-Pipelines, Batch‑Verarbeitung oder benutzerdefinierte Design‑Tools.

## Warum Aspose.PSD for Java zum Ändern von PSD vector shapes verwenden?
- **Kein Photoshop erforderlich** – Arbeiten Sie direkt mit PSD-Dateien auf jedem Server.  
- **Umfangreiche API** – Zugriff auf Ebenen, Ressourcen und Vektordaten mit stark typisierten Klassen.  
- **Plattformübergreifend** – Ausführen unter Windows, Linux oder macOS mit jedem JDK.  
- **Leistungsorientiert** – effiziente Speicherverwaltung und schnelle Speicheroperationen.  

## Voraussetzungen
1. **Java Development Kit (JDK)** – herunterladen von [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) oder Ihren bevorzugten Paketmanager verwenden.  
2. **Aspose.PSD for Java** – das neueste JAR von der [Aspose releases page](https://releases.aspose.com/psd/java/) beziehen.  
3. **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Java‑kompatibler Editor.  
4. **Eine PSD-Datei** – erstellen Sie eine in Photoshop oder holen Sie sich ein Beispiel‑PSD zum Experimentieren.  
5. **Grundlegende Java-Kenntnisse** – Vertrautheit mit Klassen, Objekten und Ausnahmebehandlung.  

## Pakete importieren
Zuerst importieren Sie die Klassen, die Sie benötigen, um mit PSD-Dateien und Vektorformen‑Ressourcen zu arbeiten.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Schritt 1: Quell- und Ausgabeverzeichnisse einrichten
Definieren Sie, wo die ursprüngliche PSD-Datei liegt und wo die modifizierte Datei gespeichert werden soll.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Schritt 2: PSD-Datei laden
Verwenden Sie `Image.load`, um die Datei zu öffnen und casten Sie sie zu `PsdImage` für PSD‑spezifische Funktionen.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Schritt 3: Vsms‑Ressource in der Ebene finden
Vektorformen‑Daten befinden sich in einer `VsmsResource`. Durchlaufen Sie die Ressourcen der zweiten Ebene, um sie zu finden.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Schritt 4: Length Records zugreifen
Jeder `LengthRecord` repräsentiert einen eigenen Vektorpfad. Holen Sie sich die, die Sie ändern möchten.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Schritt 5: Path Operation‑Eigenschaften ändern
Jetzt können Sie **PSD-Vektorformen ändern** indem Sie deren `PathOperations` ändern. Dies bestimmt, wie Formen interagieren (z. B. Ausschluss, Schnittmenge, Subtraktion).

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

## Schritt 7: Ressourcen bereinigen
Entsorgen Sie das `PsdImage`, um Speicher freizugeben.

```java
psdImage.dispose();
```

## Häufige Fallstricke & Tipps
- **Null‑Prüfungen** – immer prüfen, dass `resource` nicht `null` ist, bevor Pfade zugegriffen werden.  
- **Pfad‑Index‑Grenzen** – sicherstellen, dass die von Ihnen verwendeten Indizes (`[2]`, `[7]`, `[11]`) für die jeweilige zu bearbeitende PSD existieren.  
- **Lizenz** – das Ausführen ohne gültige Lizenz fügt dem gespeicherten PSD ein Wasserzeichen hinzu.  

## Fazit
Sie haben nun ein vollständiges End‑zu‑Ende‑Beispiel, wie Sie **PSD-Vektorformen ändern** können, indem Sie Length Record Data Properties mit Aspose.PSD for Java unterstützen. Egal, ob Sie Asset‑Pipelines automatisieren oder ein benutzerdefiniertes Design‑Tool erstellen, diese APIs bieten Ihnen die Flexibilität, Vektorebenen zu manipulieren, ohne manuell Photoshop zu verwenden. Erkunden Sie weiter, indem Sie mit anderen `PathOperations` experimentieren oder mehrere `LengthRecord`‑Änderungen für komplexe Formen kombinieren.

## FAQ

### Was ist Aspose.PSD for Java?
Aspose.PSD for Java ist eine Bibliothek, die Entwicklern ermöglicht, Photoshop‑PSD‑Dateien programmgesteuert mit Java zu manipulieren und zu bearbeiten.

### Kann ich Aspose.PSD in einem kostenlosen Projekt verwenden?
Ja, Sie können die Bibliothek kostenlos mit einer Testversion ausprobieren, die auf der Aspose-Website verfügbar ist.

### Welche Arten von Änderungen kann ich an PSD-Dateien vornehmen?
Sie können Ebenen, Formen, Texte, Pfadoperationen und vieles mehr innerhalb von PSD-Dateien manipulieren.

### Ist Aspose.PSD mit anderen Programmiersprachen kompatibel?
Ja, Aspose bietet verschiedene Bibliotheken für unterschiedliche Programmiersprachen, einschließlich .NET und Python.

### Wo finde ich die Dokumentation für Aspose.PSD?
Sie können die vollständige Dokumentation [hier](https://reference.aspose.com/psd/java/) aufrufen.

## Häufig gestellte Fragen

**Q: Wie gehe ich mit einer PSD um, die keine Vektorformen‑Ebenen enthält?**  
A: Die `VsmsResource` wird fehlen, sodass `resource` `null` bleibt. Fügen Sie eine Prüfung hinzu und überspringen Sie den Modifikationsschritt oder informieren Sie den Benutzer.

**Q: Kann ich andere Eigenschaften wie Füllfarbe oder Strichbreite ändern?**  
A: Ja, `LengthRecord` bietet zusätzliche Setter für Füllung, Strich und Deckkraft. Siehe die API‑Dokumentation für vollständige Details.

**Q: Ist es möglich, mehrere PSD-Dateien stapelweise zu verarbeiten?**  
A: Absolut. Verpacken Sie den Code in einer Schleife, die ein Verzeichnis von PSD-Dateien durchläuft und dabei die Eingabe‑ und Ausgabepfade jedes Mal anpasst.

**Q: Muss ich Streams beim Laden von einem Dateipfad manuell schließen?**  
A: Die Methode `Image.load` verwaltet Dateistreams intern, aber wenn Sie von einem `InputStream` laden, sollten Sie diesen nach der Verwendung schließen.

**Q: Welche Version von Aspose.PSD wird für diese APIs benötigt?**  
A: Die Klassen `LengthRecord` und `PathOperations` sind seit Aspose.PSD 20.10 verfügbar. Es wird empfohlen, die neueste Version zu verwenden.

---

**Zuletzt aktualisiert:** 2025-12-17  
**Getestet mit:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}