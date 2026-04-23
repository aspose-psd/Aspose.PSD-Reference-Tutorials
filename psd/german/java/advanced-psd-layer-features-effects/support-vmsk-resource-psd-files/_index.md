---
date: 2026-02-22
description: Lernen Sie, wie Sie mit Aspose.PSD für Java Vektormasken in Java erstellen,
  Vektormasken‑PSDs hinzufügen und Vmsk‑Ressourcen programmgesteuert manipulieren.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Vektor‑Maske in Java erstellen – Vmsk‑Ressource in PSD‑Dateien
url: /de/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vektor-Maske in Java erstellen – Vmsk-Ressource in PSD-Dateien

## Einführung
Wenn Sie **Vektor-Masken** (Vmsk) Ressourcen innerhalb von Photoshop (PSD)-Dateien erstellen müssen, bietet Aspose.PSD für Java einen sauberen, programmatischen Weg, dies zu tun. Egal, ob Sie ein Design‑Automatisierungstool bauen oder benutzerdefinierte Maskenunterstützung zu einer bestehenden Grafik‑Pipeline hinzufügen – dieses Tutorial führt Sie durch jeden Schritt: Laden einer PSD, Lesen der Vmsk‑Ressource, Anpassen ihrer Eigenschaften und Speichern des Ergebnisses. Am Ende können Sie Vektor‑Masken handhaben, PSD in PNG konvertieren und die Datei mit zusätzlichen Vektordaten erweitern – alles mit **create vector mask java** Techniken.

## Schnellantworten
- **Was ist eine Vmsk‑Ressource?** Sie ist die Vektor‑Maskendaten, die in einer PSD‑Datei gespeichert sind und komplexe Vektorformen für eine Ebene definieren.  
- **Welche Bibliothek unterstützt das?** Aspose.PSD für Java bietet vollen Lese‑/Schreibzugriff auf Vmsk‑Ressourcen.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion ist verfügbar; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich die bearbeitete PSD in PNG konvertieren?** Ja – nach dem Speichern können Sie die PSD laden und mit derselben API nach PNG exportieren.  
- **Ist Maven‑Unterstützung verfügbar?** Absolut; Aspose.PSD kann als Maven‑Abhängigkeit hinzugefügt werden (siehe Stichwort „aspose psd maven“).

## Was ist eine Vektor‑Maske (Vmsk‑Ressource)?
Eine Vektor‑Maske (Vmsk) ist eine nicht‑pixelbasierte Maske, die Bézier‑Kurven und Pfad‑Records verwendet, um transparente und undurchsichtige Bereiche einer Ebene zu definieren. Da sie vektor‑basiert ist, skaliert sie ohne Qualitätsverlust – perfekt für hochauflösende Grafiken.

## Warum eine Vektor‑Maske mit Aspose.PSD erstellen?
- **Automatisierung:** Programmatisch Masken hinzufügen oder ändern, ohne Photoshop zu öffnen.  
- **Konsistenz:** Sicherstellen, dass jede generierte PSD denselben Maskenregeln folgt.  
- **Plattform‑übergreifend:** Funktioniert auf jedem OS, das Java unterstützt.  
- **Integration:** Kombination mit anderen Aspose‑APIs (z. B. PSD → PNG) für End‑zu‑End‑Workflows.  
- **Skalierbarkeit:** Vektor‑Masken bleiben bei jeder Größe scharf und eignen sich ideal für responsive Designs.

## Warum das für Java‑Entwickler wichtig ist
Mit **create vector mask java** Techniken können Sie anspruchsvolle Grafik‑Logik direkt in Backend‑Services, CI‑Pipelines oder Desktop‑Utilities einbetten. Sie benötigen keinen Designer mehr, der Masken manuell hinzufügt; Ihr Code kann sie on‑the‑fly erzeugen oder anpassen, Zeit sparen und menschliche Fehler reduzieren.

## Voraussetzungen
Bevor wir in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

### Was Sie benötigen
- Java Development Kit (JDK): Stellen Sie sicher, dass das JDK auf Ihrem Rechner installiert ist. Falls nicht, können Sie es von der [Oracle-Website](https://www.oracle.com/java/technologies/javase-downloads.html) herunterladen.
- Aspose.PSD für Java Bibliothek: Eine leistungsstarke Bibliothek zur Verwaltung von PSD‑Dateien. Sie können sie von der [Aspose-Release‑Seite](https://releases.aspose.com/psd/java/) herunterladen. Für diejenigen, die es zuerst testen möchten, steht auch die [kostenlose Testversion](https://releases.aspose.com/) bereit.
- Eine IDE: Jede Java‑IDE (wie IntelliJ IDEA, Eclipse usw.) funktioniert für dieses Projekt.

### Einrichtung Ihrer Arbeitsumgebung
1. **Neues Java‑Projekt erstellen** – Öffnen Sie Ihre bevorzugte IDE und starten Sie ein frisches Projekt.  
2. **Aspose‑Bibliothek hinzufügen** – Nachdem Sie das Aspose‑JAR heruntergeladen haben, fügen Sie es dem Build‑Path Ihres Projekts hinzu, damit Sie auf alle PSD‑bezogenen Klassen zugreifen können.

Mit der vorbereiteten Umgebung können wir zur eigentlichen Implementierung übergehen.

## Wie man Vektor‑Masken in PSD‑Dateien mit Java erstellt
Im Folgenden finden Sie eine Schritt‑für‑Schritt‑Anleitung. Die Code‑Blöcke bleiben unverändert; wir haben nur erläuternden Text hinzugefügt, um jeden Schritt klar zu machen.

### Pakete importieren
Bevor wir mit PSD‑Dateien arbeiten können, müssen wir die notwendigen Klassen aus der Aspose.PSD‑Bibliothek importieren.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Jetzt, wo wir das Fundament gelegt haben, gehen wir jede Operation durch.

### Schritt 1: Laden Ihrer PSD‑Datei
Der erste Schritt besteht darin, Ihre PSD‑Datei zu laden. Hier beginnt die Magie.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Wir setzen `dataDir` auf das Verzeichnis Ihrer PSD‑Datei.  
- Wir erstellen einen String für `sourceFileName`, indem wir das Verzeichnis mit dem Namen der PSD‑Datei kombinieren.  
- Schließlich laden wir die PSD‑Datei in ein `PsdImage`‑Objekt mittels `Image.load()`.

### Schritt 2: Vmsk‑Ressource abrufen
Jetzt, wo unser PSD‑Bild geladen ist, holen wir die Vmsk‑Ressource.

```java
VmskResource resource = getVmskResource(im);
```

- Wir rufen die Methode `getVmskResource()` auf, die das Suchen und Abrufen der Vmsk‑Ressource aus dem Bild übernimmt.

### Schritt 3: Vmsk‑Ressourceneigenschaften validieren
Bevor wir Änderungen vornehmen, ist es wichtig zu prüfen, ob unsere Vmsk‑Ressource im erwarteten Zustand ist.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Hier prüfen wir verschiedene Eigenschaften der Vmsk‑Ressource. Wir wollen sicherstellen, dass sie nicht deaktiviert, invertiert oder nicht verknüpft ist und die richtige Anzahl von Pfaden enthält.

### Schritt 4: Jeden Pfad zugreifen und validieren
Lassen Sie uns etwas tiefer gehen und die Pfade innerhalb der Vmsk‑Ressource untersuchen.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Wir extrahieren drei spezifische Pfad‑Records und validieren deren Typen und Eigenschaften, um sicherzustellen, dass sie unseren Kriterien entsprechen.

### Schritt 5: Vmsk‑Ressource bearbeiten
Jetzt kommen wir zum Modifikations‑Teil! Sie können die Eigenschaften der Vmsk‑Ressource nach Bedarf anpassen.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- In diesem Block schalten wir verschiedene Eigenschaften der Vmsk‑Ressource um. Durch das Setzen auf `true` können wir steuern, wie die Maske in der PSD‑Datei wirkt.

### Schritt 6: Bézier‑Knotenpunkte ändern
Bézier‑Knoten sind entscheidend für Vektor‑Pfade. Ändern wir hier einige Werte.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Wir greifen auf bestimmte `BezierKnotRecord`‑Pfade zu und ändern deren Punkte, um die Vektor‑Maske eventuell neu zu formen.

### Schritt 7: Modifizierte PSD‑Datei speichern
Nachdem alle Änderungen abgeschlossen sind, speichern wir die modifizierte PSD‑Datei.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Wir setzen den Pfad für die exportierte PSD‑Datei und rufen dann `im.save()` auf, um die Änderungen in dieser neuen Datei zu schreiben.

### Schritt 8: Ressourcen aufräumen
Abschließend müssen wir sicherstellen, dass das Bild ordnungsgemäß freigegeben wird, um Ressourcen zu schonen.

```java
im.dispose();
```

- Es ist stets eine gute Praxis, Ressourcen zu disposen, sobald Sie fertig sind. Das hilft, Speicherlecks in Ihren Anwendungen zu vermeiden.

## Häufige Probleme und Lösungen
| Problem | Warum es passiert | Wie man es behebt |
|-------|----------------|------------|
| **`VmskResource` nicht gefunden** | Die PSD enthält keine Ebene mit einer Vektor‑Maske. | Stellen Sie sicher, dass die Quell‑PSD eine Vektor‑Maske hat oder fügen Sie manuell in Photoshop eine Maske hinzu, bevor Sie den Code ausführen. |
| **`ArrayIndexOutOfBoundsException` beim Pfad‑Zugriff** | Die erwartete Anzahl von Pfad‑Records weicht ab. | Prüfen Sie `resource.getPaths().length` und passen Sie die Index‑Verwendung entsprechend an. |
| **Lizenz‑Ausnahme** | Ausführung ohne gültige Aspose.PSD‑Lizenz. | Laden Sie eine Test‑ oder Kauf‑Lizenz mit `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Speicherleck** | Bild wird in langlaufenden Prozessen nicht disposiert. | Rufen Sie immer `im.dispose()` in einem `finally`‑Block auf oder verwenden Sie try‑with‑resources, falls unterstützt. |

## Häufig gestellte Fragen

**F: Wie füge ich einer bestehenden Ebene eine neue Vektor‑Maske hinzu?**  
A: Erstellen Sie ein `VmskResource`, füllen Sie es mit den erforderlichen Pfad‑Records (z. B. `BezierKnotRecord`) und hängen Sie es an die Ressourcen‑Sammlung der Ebene an.

**F: Kann ich die bearbeitete PSD direkt in PNG konvertieren, ohne Photoshop zu öffnen?**  
A: Ja – nach dem Speichern laden Sie die PSD erneut mit `Image.load()` und rufen `im.save("output.png")` auf, wobei Sie das PNG‑Format angeben.

**F: Gibt es eine Möglichkeit, dies in einer CI/CD‑Pipeline zu automatisieren?**  
A: Absolut. Da der Prozess reines Java ist, können Sie ihn in Maven/Gradle‑Builds, Docker‑Containern oder jedem CI‑System, das Java unterstützt, einbetten.

**F: Welche Aspose.PSD‑Versionen sind mit Java 11+ kompatibel?**  
A: Alle aktuellen Releases (2024‑2025) unterstützen Java 8 und höher, einschließlich Java 11, 17 und neueren LTS‑Versionen.

**F: Benötige ich eine Lizenz für Entwicklungs‑Builds?**  
A: Eine kostenlose Evaluations‑Lizenz funktioniert für Entwicklung und Tests. Für Produktions‑Deployments ist eine kommerzielle Lizenz erforderlich.

---

**Zuletzt aktualisiert:** 2026-02-22  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}