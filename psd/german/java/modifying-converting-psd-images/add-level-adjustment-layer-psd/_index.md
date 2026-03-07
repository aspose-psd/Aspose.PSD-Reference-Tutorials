---
date: 2026-03-07
description: Erfahren Sie, wie Sie die Pegel anpassen, indem Sie eine Ebenen‑Anpassungsebene
  in PSD‑Dateien mit Aspose.PSD für Java hinzufügen. Beherrschen Sie Tonwertanpassungen
  schnell.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Wie man die Tonwerte anpasst – Ebenen‑Anpassungsebene für Tonwertkorrektur
  in PSD hinzufügen
url: /de/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Level‑Anpassungsebene in PSD hinzufügen

## Introduction
Wenn Sie **wie man Levels anpasst** in Ihren Photoshop‑Dokumenten suchen, ist die Level Adjustment Layer das perfekte Werkzeug. Sie ermöglicht das feine Abstimmen von Schatten, Mitteltönen und Highlights, ohne die ursprünglichen Pixel dauerhaft zu verändern. In diesem Tutorial zeigen wir, wie man eine Level Adjustment Layer zu einer PSD‑Datei mit Aspose.PSD für Java hinzufügt, sodass Sie in nur wenigen Schritten eine professionelle Tonkontrolle erreichen können.

## Quick Answers
- **Was macht eine Level Adjustment Layer?** Sie modifiziert den Tonwertbereich eines Bildes nicht‑destruktiv.  
- **Welche Bibliothek wird verwendet?** Aspose.PSD für Java.  
- **Brauche ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für eine grundlegende Anpassung.  
- **Kann ich mehrere Kanäle anpassen?** Ja, Sie können Eingangs‑/Ausgangs‑Levels für jeden Farbkanal einzeln festlegen.

## What is a Level Adjustment Layer?
Eine Level Adjustment Layer ermöglicht es Ihnen, die tonale Balance eines Bildes zu korrigieren, indem Sie Eingabe‑Schatten, Mitteltöne und Highlights sowie Ausgangs‑Levels anpassen. Da sie auf einer eigenen Ebene liegt, können Sie ihre Sichtbarkeit umschalten oder sie löschen, ohne das darunterliegende Artwork zu beeinflussen.

## Why add a Level Adjustment Layer with Aspose.PSD?
- **Automatisierung:** Integrieren Sie Level‑Anpassungen in Batch‑Verarbeitungspipelines.  
- **Plattformübergreifend:** Funktioniert auf jedem Betriebssystem, das Java unterstützt.  
- **Präzision:** Greifen Sie programmgesteuert auf die Einstellungen jedes Kanals zu, um exakte Ergebnisse zu erzielen.  

## Prerequisites
1. Java Development Kit (JDK). Wenn Sie es nicht haben, laden Sie es von der [Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunter oder verwenden Sie OpenJDK.  
2. Aspose.PSD für Java‑Bibliothek – holen Sie sich das neueste JAR über diesen [Download‑Link](https://releases.aspose.com/psd/java/).  
3. Grundlegende Kenntnisse in Java‑Programmierung.  
4. Eine IDE wie IntelliJ IDEA, Eclipse oder NetBeans mit dem Aspose.PSD‑JAR, das dem Klassenpfad des Projekts hinzugefügt wurde.

## Import Packages
Bevor wir mit dem Schreiben unseres Codes beginnen, müssen wir die erforderlichen Pakete aus der Aspose.PSD‑Bibliothek importieren. So geht's:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Diese Importe geben uns Zugriff auf Klassen zum Laden von PSD‑Dateien, zur Arbeit mit Level Adjustment Layers und zur Manipulation einzelner Kanaleinstellungen.

## How to Adjust Levels in a PSD File
Im Folgenden finden Sie eine Schritt‑für‑Schritt‑Anleitung, die Ihnen genau zeigt, **wie man Levels programmgesteuert anpasst**.

### Step 1: Set Up Your File Paths
Definieren Sie, wo die Quell‑PSD liegt und wo die bearbeitete Datei gespeichert werden soll.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Ordner auf Ihrem Rechner.

### Step 2: Load the PSD File
Erstellen Sie eine `PsdImage`‑Instanz aus der Quelldatei.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Jetzt haben Sie vollen Zugriff auf alle Ebenen innerhalb der PSD.

### Step 3: Iterate Through the Layers
Durchsuchen Sie die Ebenen, um die Level Adjustment Layer zu finden, die Sie ändern möchten.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Die Prüfung `instanceof LevelsLayer` stellt sicher, dass wir nur mit Level Adjustment Layers arbeiten.

### Step 4: Adjust the Level Channel Settings
Passen Sie die Eingabe‑ und Ausgabe‑Werte für den ausgewählten Kanal an.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Input Midtone Level:** Verschiebt den Mitteltönerbereich.  
- **Input Shadow Level:** Verdunkelt oder hellt Schatten auf.  
- **Input Highlight Level:** Steuert die hellsten Bereiche.  
- **Output Shadow/Highlight Levels:** Definieren den endgültigen Ausgabe‑Bereich.

Probieren Sie verschiedene Werte aus, um zu sehen, wie sie das Bild beeinflussen.

### Step 5: Save the Modified PSD File
Speichern Sie Ihre Änderungen in einer neuen Datei.
```java
im.save(psdPathAfterChange);
```
Die aktualisierte PSD finden Sie an dem von Ihnen in `psdPathAfterChange` angegebenen Ort.

## Common Issues and Solutions
- **Datei nicht gefunden:** Stellen Sie sicher, dass `dataDir` auf den richtigen Ordner zeigt und die Quell‑PSD existiert.  
- **ClassCastException:** Vergewissern Sie sich, dass die geladene Datei tatsächlich eine PSD ist; andere Formate erfordern andere Klassen.  
- **Lizenzfehler:** Verwenden Sie eine gültige Aspose.PSD‑Lizenz für Produktions‑Builds; die Testversion funktioniert für die Entwicklung.

## Conclusion
Sie wissen jetzt **wie man Levels** anpasst, indem Sie eine Level Adjustment Layer in einer PSD‑Datei mit Aspose.PSD für Java hinzufügen und konfigurieren. Diese Technik gibt Ihnen präzise Kontrolle über die tonale Balance, während Ihr Workflow vollständig automatisiert bleibt. Experimentieren Sie weiter mit verschiedenen Kanalwerten und erkunden Sie die Batch‑Verarbeitung, um dieselben Anpassungen auf mehrere Bilder anzuwenden.

## Frequently Asked Questions

**Q: Was ist eine Level Adjustment Layer?**  
A: Es ist eine nicht‑destruktive Ebene, die es Ihnen ermöglicht, den Tonwertbereich (Schatten, Mitteltöne, Highlights) eines Bildes zu ändern.

**Q: Kann ich Aspose.PSD ohne Lizenzkauf nutzen?**  
A: Ja, Sie können die Bibliothek mit einer kostenlosen Testversion evaluieren, aber für den kommerziellen Einsatz ist eine Lizenz erforderlich.

**Q: Wo finde ich die Dokumentation für Aspose.PSD?**  
A: Die Dokumentation finden Sie [hier](https://reference.aspose.com/psd/java/).

**Q: Gibt es Community‑Support für Aspose‑Produkte?**  
A: Auf jeden Fall! Sie können Fragen stellen und Hilfe im [Aspose‑Forum](https://forum.aspose.com/c/psd/34) erhalten.

**Q: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?**  
A: Sie können hier eine temporäre Lizenz beantragen [hier](https://purchase.aspose.com/temporary-license/).

---

**Zuletzt aktualisiert:** 2026-03-07  
**Getestet mit:** Aspose.PSD neueste Version (Java)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}