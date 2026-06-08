---
date: 2026-06-08
description: Erfahren Sie, wie Sie PSD mit Aspose.PSD für Java als PNG speichern und
  die Konvertierung bei Bedarf unterbrechen. Verwalten Sie den Bild-Workflow effizient.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Unterstützung für Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Wie man PSD als PNG mit Interrupt Monitor in Aspose.PSD für Java speichert
url: /de/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD als PNG speichern mit Interrupt Monitor in Aspose.PSD für Java

## Einführung

Wenn Sie **PSD als PNG speichern** möchten, während Sie die vollständige Kontrolle über lang laufende Konvertierungen behalten, bietet Ihnen der Interrupt Monitor von Aspose.PSD für Java genau das. In diesem Tutorial führen wir Sie durch die Einrichtung des Monitors, die Konvertierung einer PSD‑Datei in PNG und das sichere Abbrechen des Vorgangs bei Bedarf. Außerdem sehen Sie, wie dies in einen typischen Bildverarbeitungs‑Workflow passt und warum es ein unverzichtbares Werkzeug für robuste Anwendungen ist.

## Schnelle Antworten
- **Kann ich eine PSD‑zu‑PNG-Konvertierung unterbrechen?** Ja, verwenden Sie `InterruptMonitor`, um den Vorgang bei Bedarf zu stoppen.  
- **Welche Methode speichert ein PSD als PNG?** Rufen Sie `save(outputPath, new PngOptions())` auf.  
- **Benötige ich eine Lizenz für die Produktion?** Eine kommerzielle Lizenz ist erforderlich; ein kostenloser Testzeitraum ist verfügbar.  
- **Welche Java-Version wird unterstützt?** Java 8 und höher werden vollständig unterstützt.  
- **Ist die Bibliothek thread‑sicher?** Konvertierungen können in separaten Threads laufen; der Monitor verarbeitet Unterbrechungen sicher.

## Voraussetzungen

Bevor Sie in die Feinheiten der Verwendung des Interrupt Monitors eintauchen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- **Java-Entwicklungsumgebung:** Richten Sie eine Java‑Entwicklungsumgebung auf Ihrem System ein.  
- **Aspose.PSD Bibliothek:** Beschaffen Sie die Aspose.PSD für Java Bibliothek. Sie können sie [hier](https://releases.aspose.com/psd/java/) herunterladen. Sie können auch die Hauptseite von Aspose [hier](https://releases.aspose.com/) besuchen.  
- **Dokumentenverzeichnis:** Haben Sie ein festgelegtes Verzeichnis für Ihre PSD‑Dokumente.

## Pakete importieren

Beginnen Sie damit, die erforderlichen Pakete in Ihr Java‑Projekt zu importieren. Dadurch haben Sie Zugriff auf die Aspose.PSD‑Funktionalitäten.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Jetzt zerlegen wir den Beispielcode in eine Schritt‑für‑Schritt‑Anleitung, um den Interrupt Monitor in Ihr Aspose.PSD‑Projekt für Java zu integrieren.

## Wie speichert man PSD als PNG mit dem Interrupt Monitor?

`PsdImage` stellt ein in den Speicher geladenes PSD‑Dokument dar.  
`SaveImageWorker` führt die Bildkonvertierung in einem separaten Thread aus.  

Laden Sie Ihre PSD‑Datei mit `new PsdImage("source.psd")`, hängen Sie einen `InterruptMonitor` an den `SaveImageWorker` und rufen Sie `save("output.png", new PngOptions())` auf. Der Monitor überwacht Anfragen zum Abbruch und beendet die Konvertierung sauber, wobei er die Kontrolle innerhalb von Millisekunden an Ihre Anwendung zurückgibt.

### Schritt 1: Dokumentenverzeichnis festlegen

```java
String dataDir = "Your Document Directory";
```

Stellen Sie sicher, dass Sie „Your Document Directory“ durch den tatsächlichen Pfad ersetzen, in dem Ihre PSD‑Dokumente gespeichert sind.

### Schritt 2: Bildoptionen und Ausgabepfad festlegen

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Geben Sie die Bildoptionen, die Quell‑PSD‑Datei und den gewünschten Ausgabepfad für das konvertierte Bild an.

### Schritt 3: Interrupt Monitor und SaveImageWorker initialisieren

Die Klasse `InterruptMonitor` überwacht eine laufende Konvertierung und kann sie unterbrechen, wenn `requestInterrupt()` aufgerufen wird.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Erstellen Sie Instanzen von `InterruptMonitor` und `SaveImageWorker` und verknüpfen Sie den Monitor mit dem Bildkonvertierungs‑Worker.

### Schritt 4: Bildkonvertierungs‑Thread starten

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Starten Sie einen neuen Thread für den Bildkonvertierungsprozess und führen Sie eine Timeout‑Periode ein, um eine Unterbrechung zu antizipieren.

### Schritt 5: Prozess unterbrechen

Der Aufruf von `monitor.requestInterrupt()` signalisiert dem Monitor, die laufende Konvertierung abzubrechen.

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Unterbrechen Sie den Bildkonvertierungsprozess mit dem `InterruptMonitor` und warten Sie, bis die Unterbrechung abgeschlossen ist. Löschen Sie schließlich die Ausgabedatei, um aufzuräumen.

## Warum den Interrupt Monitor für PSD‑zu‑PNG‑Konvertierung verwenden?

Aspose.PSD unterstützt **über 30 Ausgabeformate**, darunter PNG, JPEG, BMP und TIFF, und kann Dateien bis zu **500 MB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Durch das Hinzufügen eines Interrupt Monitors reduzieren Sie CPU‑Verschwendung und verbessern die Reaktionsfähigkeit in Batch‑Verarbeitungspipelines, insbesondere wenn eine Konvertierung die erwarteten Zeitlimits überschreitet.

## Häufige Probleme und Lösungen

- **Konvertierung hängt unendlich:** Stellen Sie sicher, dass der Monitor **vor** dem Aufruf von `save` angehängt ist.  
- **Ausgabedatei ist nach Unterbrechung beschädigt:** Der Monitor bricht sauber ab; prüfen Sie jedoch immer, ob die Datei existiert, bevor Sie sie verwenden.  
- **Bedenken bezüglich Thread‑Sicherheit:** Führen Sie jede Konvertierung in einem eigenen Thread aus; der Monitor wirkt nur auf den zugehörigen Worker.

## Häufig gestellte Fragen

**Q1: Was ist ein Interrupt Monitor in Aspose.PSD für Java?**  
A: Der Interrupt Monitor ermöglicht Entwicklern, lang laufende Bildkonvertierungen zu pausieren oder abzubrechen und bietet Echtzeit‑Kontrolle über die Ressourcennutzung.

**Q2: Wie kann ich die Aspose.PSD‑Bibliothek für Java erhalten?**  
A: Sie können die Aspose.PSD für Java Bibliothek [hier](https://releases.aspose.com/psd/java/) herunterladen.

**Q3: Gibt es eine kostenlose Testversion von Aspose.PSD für Java?**  
A: Ja, Sie können eine kostenlose Testversion von Aspose.PSD [hier](https://releases.aspose.com/) erkunden.

**Q4: Wo finde ich Support für Aspose.PSD für Java?**  
A: Besuchen Sie das Aspose.PSD für Java Support‑Forum [hier](https://forum.aspose.com/c/psd/34).

**Q5: Wie kann ich eine Lizenz für Aspose.PSD für Java erwerben?**  
A: Sie können eine Lizenz für Aspose.PSD für Java [hier](https://purchase.aspose.com/buy) kaufen.

**Q6: Kann ich mehrere PSD‑Dateien parallel zu PNG konvertieren?**  
A: Ja, starten Sie für jede Datei einen separaten Thread und hängen Sie einen individuellen `InterruptMonitor` an jeden Konvertierungs‑Worker.

**Q7: Handhabt die Bibliothek Farbprofile während der PSD‑zu‑PNG‑Konvertierung?**  
A: Absolut; Aspose.PSD bewahrt eingebettete ICC‑Profile und wendet sie automatisch auf das Ausgabepng an.

---

**Letzte Aktualisierung:** 2026-06-08  
**Getestet mit:** Aspose.PSD 23.12 für Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [PSD als PNG speichern und Rendering‑Drop‑Shadow in Aspose.PSD für Java anwenden](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [PSD nach PNG exportieren & eine neue reguläre Ebene mit Aspose.PSD für Java hinzufügen](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Unterstützung für Interrupt Monitor in PSD‑Dateien – Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}