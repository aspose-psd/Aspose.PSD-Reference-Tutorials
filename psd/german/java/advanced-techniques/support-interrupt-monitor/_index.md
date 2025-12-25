---
date: 2025-12-25
description: Erfahren Sie, wie Sie PSD mit Aspose.PSD für Java unter Unterstützung
  des Interrupt‑Monitors in PNG konvertieren, einschließlich eines Java‑Thread‑Interrupt‑Beispiels
  und Tipps zum Speichern von PSD als PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Wie man PSD in PNG mit Unterstützung für Interrupt‑Monitor in Aspose.PSD für
  Java konvertiert
url: /de/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD zu PNG konvertieren mit Interrupt Monitor in Aspose.PSD für Java

## Einführung

Wenn Sie **PSD zu PNG konvertieren** müssen, während Sie die volle Kontrolle über langlaufende Bildkonvertierungen behalten, ist der Interrupt Monitor von Aspose.PSD für Java das Werkzeug, das Sie gesucht haben. In diesem Tutorial führen wir Sie durch ein praxisnahes **java thread interrupt example**, das Ihnen ermöglicht, eine Konvertierung mitten im Prozess zu stoppen, sodass Sie Ressourcen verwalten, Zeitlimits durchsetzen oder auf Benutzerabbrüche reagieren können.

## Schnelle Antworten
- **Was macht der Interrupt Monitor?** Er ermöglicht es, eine laufende Bildkonvertierung sicher zu stoppen.  
- **Kann ich damit PSD zu PNG konvertieren?** Ja – der Monitor funktioniert mit jeder Speicheroperation, einschließlich PNG.  
- **Ist ein separater Thread erforderlich?** In der Regel führen Sie die Konvertierung in einem separaten Thread aus, damit Sie ihn unterbrechen können.  
- **Welche Aspose.PSD-Version wird benötigt?** Jede aktuelle Version, die `com.aspose.psd.multithreading.InterruptMonitor` enthält.  
- **Benötige ich eine Lizenz für die Produktion?** Ja, für die Nutzung außerhalb der Testphase ist eine gültige Aspose.PSD-Lizenz erforderlich.

## Was bedeutet „PSD zu PNG konvertieren“ mit einem Interrupt Monitor?

Das Konvertieren eines großen Photoshop‑Dokuments (PSD/PSB) in ein PNG‑Bild kann CPU‑intensiv sein. Durch das Anbinden eines **Interrupt Monitor** an den Konvertierungs‑Worker erhalten Sie die Möglichkeit, den Vorgang programmgesteuert zu stoppen – ideal für Web‑Services, Batch‑Jobs oder UI‑Anwendungen, bei denen Benutzer Vorgänge abbrechen können.

## Warum den Interrupt Monitor verwenden?

- **Responsive UI:** Verhindern Sie, dass Ihre Anwendung einfriert, während eine große Datei verarbeitet wird.  
- **Resource Management:** Stoppen Sie Konvertierungen, die Zeit‑ oder Speicherbudgets überschreiten.  
- **Error Handling:** Bereinigen Sie bei einer Unterbrechung elegant teilweise erzeugte Ausgabedateien.

## Voraussetzungen

- Java-Entwicklungsumgebung (JDK 8 oder neuer).  
- Aspose.PSD für Java‑Bibliothek – laden Sie sie **[here](https://releases.aspose.com/psd/java/)** herunter.  
- Ein Ordner, der die PSD/PSB‑Dateien enthält, mit denen Sie arbeiten möchten.

## Pakete importieren

Beginnen Sie mit dem Import der erforderlichen Klassen. Dadurch erhalten Sie Zugriff auf Bildoptionen, den Interrupt Monitor und Thread‑Hilfsprogramme.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Dokumentverzeichnis festlegen

```java
String dataDir = "Your Document Directory";
```

Ersetzen Sie `"Your Document Directory"` durch den absoluten Pfad, in dem Ihre PSD‑Dateien liegen.

### Schritt 2: Bildoptionen und Ausgabepfad definieren

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Hier speichern wir **PSD als PNG** mit `PngOptions`. Passen Sie die Dateinamen bei Bedarf an.

### Schritt 3: Interrupt Monitor und SaveImageWorker initialisieren

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Die Instanz `InterruptMonitor` wird später verwendet, um die Konvertierung zu stoppen. `SaveImageWorker` verbindet den Monitor mit der Konvertierungsaufgabe.

### Schritt 4: Bildkonvertierung in einem separaten Thread starten

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Wir starten die Konvertierung in einem Hintergrund‑Thread, damit der Haupt‑Thread reaktionsfähig bleibt. Der Aufruf `Thread.sleep(3000)` simuliert ein Timeout‑Szenario.

### Schritt 5: Prozess unterbrechen (Java Thread Interrupt Beispiel)

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

Der Aufruf `monitor.interrupt()` löst die **how to interrupt monitor**‑Logik aus. Nach der Unterbrechung bereinigen wir ggf. teilweise geschriebene PNG‑Dateien.

## Häufige Probleme und Lösungen

| Problem | Grund | Lösung |
|---------|-------|--------|
| Konvertierung stoppt nie | Monitor nicht mit Worker verknüpft | Stellen Sie sicher, dass `SaveImageWorker` dieselbe `InterruptMonitor`‑Instanz erhält. |
| Ausgabedatei bleibt nach Unterbrechung erhalten | Aufräumcode wird nicht ausgeführt | Überprüfen Sie, dass der `finally`‑Block ausgeführt wird und der Dateipfad korrekt ist. |
| `OutOfMemoryError` on large PSB files | Keine Streaming‑Optionen verwendet | Verwenden Sie `PsdImage` mit `LoadOptions`, die ein speichereffizientes Laden ermöglichen. |

## Häufig gestellte Fragen

### Q1: Was ist ein Interrupt Monitor in Aspose.PSD für Java?

A1: Der Interrupt Monitor ermöglicht Entwicklern **die Verwaltung und Unterbrechung von Bildkonvertierungsprozessen**, wodurch Sie eine feinkörnige Kontrolle über langlaufende Aufgaben erhalten.

### Q2: Wie kann ich die Aspose.PSD‑Bibliothek für Java erhalten?

A2: Sie können die Aspose.PSD für Java‑Bibliothek **[here](https://releases.aspose.com/psd/java/)** herunterladen.

### Q3: Gibt es eine kostenlose Testversion von Aspose.PSD für Java?

A3: Ja, Sie können eine kostenlose Testversion von Aspose.PSD **[here](https://releases.aspose.com/)** ausprobieren.

### Q4: Wo finde ich Support für Aspose.PSD für Java?

A4: Besuchen Sie das Support‑Forum für Aspose.PSD für Java **[here](https://forum.aspose.com/c/psd/34)**.

### Q5: Wie kann ich eine Lizenz für Aspose.PSD für Java erwerben?

A5: Sie können eine Lizenz für Aspose.PSD für Java **[here](https://purchase.aspose.com/buy)** erwerben.

---

**Zuletzt aktualisiert:** 2025-12-25  
**Getestet mit:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}