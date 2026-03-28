---
date: 2026-03-28
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java Fotofilter‑Ebenen erstellen
  und Anpassungsebenen zu PSD‑Dateien hinzufügen. Folgen Sie dieser Anleitung, um
  Filter mühelos zu bearbeiten und hinzuzufügen.
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: Wie man mit Java eine Fotofilter‑Ebene in einer PSD erstellt
url: /de/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Verwalten Photo Filter Adjustment Layer in PSD - Java

## Einführung
Wenn Sie ein Java‑Entwickler sind und **Photo‑Filter‑Layer**‑Objekte in PSD‑Dateien erstellen möchten, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch die Verwendung von Aspose.PSD für Java, um vorhandene Photo Filter Adjustment Layers zu bearbeiten und neue hinzuzufügen. Am Ende wissen Sie genau, wie Sie **Photo‑Filter‑Layer** erstellen, dessen Eigenschaften anpassen und sogar **Adjustment Layer PSD**‑Dateien programmgesteuert **hinzufügen** – und beschleunigen damit Ihren Grafik‑Design‑Workflow.

## Schnellantworten
- **Welche Bibliothek verarbeitet PSD‑Layer in Java?** Aspose.PSD für Java  
- **Kann ich ein vorhandenes Photo Filter‑Layer bearbeiten?** Ja – PSD laden, das `PhotoFilterLayer` finden und dessen Eigenschaften ändern.  
- **Wie füge ich ein neues Filter‑Layer hinzu?** Verwenden Sie `addPhotoFilterLayer(Color)` auf einer `PsdImage`‑Instanz.  
- **Benötige ich eine Lizenz für die Produktion?** Eine kommerzielle Lizenz ist erforderlich; eine kostenlose Testversion ist verfügbar.  
- **Welche Java‑Version wird unterstützt?** JDK 8 oder höher (JDK 11 empfohlen).  

## Was ist ein Photo Filter Adjustment Layer?
Ein Photo Filter Adjustment Layer ist ein nicht‑destruktiver Effekt, der das gesamte Bild mit einer gewählten Farbe einfärbt, ähnlich wie das Auflegen eines fotografischen Filters. Er existiert als eigene Ebene, sodass Sie Farbe, Dichte und Leuchtkraft anpassen können, ohne die ursprünglichen Pixel zu verändern.

## Warum Aspose.PSD zum Erstellen von Photo Filter Layer verwenden?
- **Vollständige Kontrolle** über die PSD‑Struktur ohne Adobe Photoshop.  
- **Plattformübergreifende** Java‑API funktioniert unter Windows, Linux und macOS.  
- **Kein COM‑Interop** – reines Java, ideal für serverseitige Verarbeitung.  
- **Unterstützt PSD‑Version 1‑8**, wobei Ebeneneffekte und Masken erhalten bleiben.

## Voraussetzungen
### Notwendige Software
1. Java Development Kit (JDK): Stellen Sie sicher, dass eine kompatible JDK‑Version auf Ihrem Rechner installiert ist. Sie können es von [Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen.  
2. Aspose.PSD für Java: Um PSD‑Dateien zu manipulieren, benötigen Sie die Aspose.PSD‑Bibliothek. Sie können sie von der [Aspose‑Release‑Seite](https://releases.aspose.com/psd/java/) herunterladen. Vergessen Sie nicht, die [Aspose‑Dokumentation](https://reference.aspose.com/psd/java/) für weitere Details zu prüfen.  
3. IDE (Integrated Development Environment): Eine gute IDE wie IntelliJ IDEA oder Eclipse erleichtert das Programmieren.

### Grundlagen verstehen
Vertrautheit mit Java‑Programmierung und ein Grundverständnis darüber, wie PSD‑Dateien funktionieren, sind vorteilhaft. Wenn Sie neu im Umgang mit Bibliotheken in Java sind, sollten Sie sich mit dem Importieren und Nutzen von Frameworks vertraut machen.

## Pakete importieren
Um zu beginnen, müssen wir die erforderlichen Klassen aus der Aspose.PSD‑Bibliothek importieren. Hier ist eine einfache Import‑Anweisung, die Sie am Anfang Ihrer Java‑Datei benötigen:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Fügen Sie dies einfach oben in Ihre Java‑Datei ein, und Sie können sofort mit PSD‑Bildern arbeiten!

## Vorhandenes Photo Filter Layer bearbeiten
### Schritt 1: Datenverzeichnis einrichten
Zunächst müssen Sie das Verzeichnis festlegen, in dem Ihre PSD‑Dateien gespeichert sind. Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Pfad. So behalten Sie alles organisiert:
```java
String dataDir = "Your Document Directory";
```

### Schritt 2: PSD‑Datei laden
Laden wir nun die PSD‑Datei, die Sie bearbeiten möchten. Stellen Sie sicher, dass `PhotoFilterAdjustmentLayer.psd` in Ihrem angegebenen Verzeichnis existiert.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### Schritt 3: Bildobjekt initialisieren
Mit der integrierten Funktionalität von Aspose laden wir das Bild in unser Projekt:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Schritt 4: Durch die Ebenen iterieren
Als Nächstes untersuchen wir die Ebenen innerhalb der PSD‑Datei. Unser Ziel ist es, das `PhotoFilterLayer` zu finden:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### Schritt 5: Photo Filter Layer anpassen
Hier passiert die Magie! Sie können `Color` und `Density` ändern. Zum Beispiel können wir die Farbe auf ein kräftiges Rot setzen und die Dichte anpassen:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### Schritt 6: Bearbeitete PSD‑Datei speichern
Abschließend speichern wir die Änderungen, um eine neue PSD‑Datei mit Ihren Anpassungen zu erstellen:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
Sie haben soeben ein Photo Filter Adjustment Layer in einer PSD‑Datei bearbeitet.

## Neues Photo Filter Layer hinzufügen
### Schritt 1: Verzeichnispfad festlegen
Wie zuvor beginnen wir mit der Definition unseres Datenverzeichnisses:
```java
String dataDir = "Your Document Directory";
```

### Schritt 2: Quelldatei laden
Für dieses Beispiel laden wir eine andere PSD‑Datei, zu der wir **Adjustment Layer PSD** hinzufügen möchten:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### Schritt 3: Bildobjekt erneut initialisieren
Wir müssen eine neue `PsdImage`‑Instanz erstellen, also laden wir die Datei:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### Schritt 4: Photo Filter Layer hinzufügen
Jetzt können wir ein neues Photo Filter Layer mit einer benutzerdefinierten Farbe hinzufügen. So geht's:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### Schritt 5: Neue PSD‑Datei speichern
Erneut ist es Zeit, unsere Änderungen zu speichern. Hier ist die Zeile, die das erledigt:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
Sie haben erfolgreich ein neues Photo Filter Layer zu Ihrer PSD‑Datei hinzugefügt.

## Häufige Probleme und Lösungen
- **`ClassCastException` beim Laden des Bildes** – Stellen Sie sicher, dass die geladene Datei ein PSD ist; andere Formate benötigen andere Klassen.  
- **Farbwerte erscheinen falsch** – Verwenden Sie `Color.fromArgb(alpha, red, green, blue)`, wobei jeder Wert 0‑255 ist.  
- **Ebene nicht gefunden** – Prüfen Sie, ob das Quell‑PSD tatsächlich ein `PhotoFilterLayer` enthält. Nutzen Sie `im.getLayers().length` zum Debuggen.

## Häufig gestellte Fragen
### Was ist Aspose.PSD?
Aspose.PSD ist eine .NET‑ und Java‑Bibliothek zum Erstellen, Bearbeiten und Konvertieren von PSD‑Dateien.

### Kann ich Aspose.PSD kostenlos testen?
Ja, Aspose bietet eine kostenlose Testversion an. Weitere Informationen finden Sie [hier](https://releases.aspose.com/).

### Wo finde ich die Dokumentation?
Die vollständige Dokumentation finden Sie auf der [Aspose‑Referenzseite](https://reference.aspose.com/psd/java/).

### Wie kann ich Aspose.PSD erwerben?
Sie können die Software über [diesen Link](https://purchase.aspose.com/buy) kaufen.

### Gibt es Support für Aspose.PSD?
Absolut! Sie erhalten Unterstützung über das Aspose‑Support‑Forum [hier](https://forum.aspose.com/c/psd/34).

---

**Zuletzt aktualisiert:** 2026-03-28  
**Getestet mit:** Aspose.PSD für Java 24.11 (neueste Version 2026)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}