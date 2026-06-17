---
date: 2026-02-20
description: Erfahren Sie, wie Sie Längenaufzeichnungseigenschaften unterstützen und
  PSD‑Dateien stapelweise mit Aspose.PSD für Java verarbeiten. Schritt‑für‑Schritt‑Anleitung
  mit Codebeispielen.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Unterstützung von Längenaufzeichnungs‑Eigenschaften – PSD‑Vektorformen bearbeiten
  (Java)
url: /de/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unterstützung von Length Record Properties – PSD-Vektorformen bearbeiten (Java)

## Einleitung
Wenn Sie **modify PSD vector shapes** programmgesteuert benötigen, bietet die Aspose.PSD for Java Bibliothek die volle Kontrolle über Photoshop‑Dateien direkt aus Ihrem Java‑Code. In diesem Tutorial führen wir Sie durch alles, was Sie wissen müssen, um **support length record properties** zu unterstützen – ein wesentlicher Schritt, wenn Sie Vektorformen‑Ebenen bearbeiten möchten. Am Ende können Sie eine PSD öffnen, ihre Vektorformen‑Eigenschaften anpassen und die aktualisierte Datei speichern, ohne Ihre IDE zu verlassen. Lassen Sie uns loslegen!

## Schnelle Antworten
- **Was bedeutet “modify PSD vector shapes”?** Anpassen der Geometrie, Pfadoperationen oder anderer Eigenschaften von vektor‑basierten Ebenen in einer PSD‑Datei.  
- **Welche Bibliothek übernimmt das?** Aspose.PSD for Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für ein einfaches Skript zur Form‑Modifikation.  
- **Was sind die wichtigsten Voraussetzungen?** Java JDK, Aspose.PSD for Java und eine Beispiel‑PSD‑Datei.

## Was bedeutet „support length record properties“?
„Support length record properties“ bedeutet, dass Sie auf die `LengthRecord`‑Objekte zugreifen und diese aktualisieren, die jeden Vektorpfad innerhalb einer PSD beschreiben. Durch das Ändern dieser Records können Sie steuern, wie Formen kombiniert, geschnitten oder voneinander subtrahiert werden.

## Warum Aspose.PSD for Java für die Unterstützung von Length Record Properties verwenden?
- **Kein Photoshop erforderlich** – arbeiten Sie direkt mit PSD‑Dateien auf jedem Server.  
- **Umfangreiche API** – greifen Sie auf Ebenen, Ressourcen und Vektordaten mit stark typisierten Klassen zu.  
- **Plattformübergreifend** – läuft unter Windows, Linux oder macOS mit jedem JDK.  
- **Leistungsorientiert** – effiziente Speicherverwaltung und schnelle Speicheroperationen.  

## Voraussetzungen
1. **Java Development Kit (JDK)** – herunterladen von [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) oder über Ihren bevorzugten Paket‑Manager.  
2. **Aspose.PSD for Java** – das neueste JAR von der [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Java‑kompatibler Editor.  
4. **Eine PSD‑Datei** – erstellen Sie eine in Photoshop oder holen Sie sich ein Beispiel‑PSD zum Experimentieren.  
5. **Grundkenntnisse in Java** – Vertrautheit mit Klassen, Objekten und Ausnahmebehandlung.

## Import Packages
Importieren Sie zunächst die Klassen, die Sie für die Arbeit mit PSD‑Dateien und Vektor‑Shape‑Ressourcen benötigen.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Schritt 1: Quell‑ und Ausgabeverzeichnisse festlegen
Definieren Sie, wo die ursprüngliche PSD liegt und wo die modifizierte Datei gespeichert werden soll.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Schritt 2: PSD‑Datei laden
Verwenden Sie `Image.load`, um die Datei zu öffnen, und casten Sie sie zu `PsdImage` für PSD‑spezifische Features.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Schritt 3: Vsms‑Ressource in der Ebene finden
Vektor‑Shape‑Daten befinden sich in einer `VsmsResource`. Durchlaufen Sie die Ressourcen der zweiten Ebene, um sie zu finden.

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
Jeder `LengthRecord` repräsentiert einen eigenen Vektorpfad. Holen Sie sich die Records, die Sie ändern möchten.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Schritt 5: Pfad‑Operations‑Eigenschaften ändern
Jetzt können Sie **modify PSD vector shapes**, indem Sie deren `PathOperations` ändern. Diese bestimmen, wie Formen interagieren (z. B. Ausschluss, Schnitt, Subtraktion).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Schritt 6: Modifizierte PSD‑Datei speichern
Speichern Sie Ihre Änderungen in einer neuen Datei.

```java
psdImage.save(outPsdFilePath);
```

## Schritt 7: Ressourcen aufräumen
Entsorgen Sie das `PsdImage`, um Speicher freizugeben.

```java
psdImage.dispose();
```

## Wie man PSD‑Dateien stapelweise mit Unterstützung von Length Record Properties verarbeitet
Wenn Sie dieselben Vektor‑Shape‑Anpassungen auf viele PSDs anwenden müssen, wickeln Sie den obigen Code in eine Schleife, die ein Verzeichnis von Dateien durchläuft. Aktualisieren Sie `inPsdFilePath` und `outPsdFilePath` für jede Iteration, und Sie können **batch process PSD files** effizient durchführen.

## Häufige Stolperfallen & Tipps
- **Null‑Prüfungen** – prüfen Sie immer, ob `resource` nicht `null` ist, bevor Sie Pfade zugreifen.  
- **Pfad‑Index‑Grenzen** – stellen Sie sicher, dass die von Ihnen verwendeten Indizes (`[2]`, `[7]`, `[11]`) für die jeweilige PSD existieren.  
- **Lizenz** – das Ausführen ohne gültige Lizenz fügt dem gespeicherten PSD ein Wasserzeichen hinzu.  

## Fazit
Sie haben nun ein vollständiges End‑zu‑End‑Beispiel, wie Sie **modify PSD vector shapes** durch Unterstützung von Length Record Properties mit Aspose.PSD for Java durchführen können. Ob Sie Asset‑Pipelines automatisieren oder ein benutzerdefiniertes Design‑Tool bauen – diese APIs geben Ihnen die Flexibilität, Vektor‑Ebenen zu manipulieren, ohne manuell Photoshop zu verwenden. Experimentieren Sie weiter mit anderen `PathOperations` oder kombinieren Sie mehrere `LengthRecord`‑Änderungen für komplexe Formen.

## Häufig gestellte Fragen

**Q: Wie gehe ich mit einer PSD um, die keine Vektor‑Shape‑Ebenen enthält?**  
A: Die `VsmsResource` wird fehlen, sodass `resource` `null` bleibt. Fügen Sie eine Prüfung hinzu und überspringen Sie den Modifikationsschritt oder informieren Sie den Benutzer.

**Q: Kann ich andere Eigenschaften wie Füllfarbe oder Strichstärke ändern?**  
A: Ja, `LengthRecord` bietet zusätzliche Setter für Füllung, Strich und Transparenz. Siehe die API‑Dokumentation für vollständige Details.

**Q: Ist es möglich, mehrere PSD‑Dateien stapelweise zu verarbeiten?**  
A: Absolut. Wickeln Sie den Code in eine Schleife, die ein Verzeichnis von PSD‑Dateien durchläuft und passen Sie bei jedem Durchlauf die Eingabe‑ und Ausgabepfade an.

**Q: Muss ich Streams manuell schließen, wenn ich aus einem Dateipfad lade?**  
A: Die Methode `Image.load` verwaltet Dateistreams intern, aber wenn Sie aus einem `InputStream` laden, denken Sie daran, diesen nach Gebrauch zu schließen.

**Q: Welche Version von Aspose.PSD wird für diese APIs benötigt?**  
A: Die Klassen `LengthRecord` und `PathOperations` sind seit Aspose.PSD 20.10 verfügbar. Die Verwendung der neuesten Version wird empfohlen.

---

**Zuletzt aktualisiert:** 2026-02-20  
**Getestet mit:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}