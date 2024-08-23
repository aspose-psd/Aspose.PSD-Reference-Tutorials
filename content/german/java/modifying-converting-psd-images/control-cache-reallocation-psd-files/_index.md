---
title: Steuern der Cache-Neuzuweisung in PSD-Dateien
linktitle: Steuern der Cache-Neuzuweisung in PSD-Dateien
second_title: Aspose.PSD Java API
description: Verwalten Sie die Cache-Neuzuweisung in PSD-Dateien mit Aspose.PSD für Java. Erfahren Sie, wie Sie Speicher und Dateiverwaltung effizient optimieren – ideal für Entwickler.
type: docs
weight: 22
url: /de/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---
## Einführung
Beim programmgesteuerten Arbeiten mit Bildern und Photoshop-Dateien ist Effizienz ein Schlüsselfaktor. Aspose.PSD für Java bietet robuste Funktionen zum nahtlosen Verwalten und Bearbeiten von PSD-Dateien. Einer der grundlegenden Aspekte zur Leistungsoptimierung ist die Kontrolle der Cache-Neuzuweisung. Die Cache-Verwaltung hilft dabei, das Gleichgewicht zwischen Speicher- und Festplattennutzung aufrechtzuerhalten und sicherzustellen, dass Ihre Anwendung reibungslos und ohne unerwartete Abstürze oder Verlangsamungen ausgeführt wird. 
## Voraussetzungen
Bevor wir mit dem Codieren beginnen, müssen Sie einige Dinge sicherstellen, damit alles reibungslos läuft:
1. Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem Computer installiert ist. Sie können es hier herunterladen:[Website von Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD für Java: Sie müssen die Aspose.PSD-Bibliothek herunterladen. Die neueste Version finden Sie[Hier](https://releases.aspose.com/psd/java/).
3. IDE-Setup: Eine integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse erleichtert Ihnen die Verwaltung Ihres Codes.
4. Grundlegende Kenntnisse in Java: Wenn Sie mit der Java-Programmierung vertraut sind, verstehen Sie die Konzepte und Codeausschnitte besser.
5.  Aspose-Lizenz (optional): Wenn Sie Wasserzeichen entfernen und die volle Funktionalität nutzen möchten, sollten Sie eine Lizenz erwerben[Hier](https://purchase.aspose.com/buy) oder die kostenlose Testversion ausprobieren[Hier](https://releases.aspose.com/).
## Pakete importieren
Bevor wir mit dem Schreiben des Codes beginnen, stellen wir sicher, dass wir die erforderlichen Pakete importiert haben. Nachfolgend finden Sie eine kurze Liste dessen, was am Anfang Ihrer Java-Datei enthalten sein muss:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## Schritt 1: Einrichten Ihres Datenverzeichnisses
Als Erstes müssen Sie ein Verzeichnis einrichten, in dem Ihre Cache-Dateien gespeichert werden sollen. Dies ist für die effektive Verwaltung des Caches wichtig.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Definieren Sie das Verzeichnis für Ihren Dokumentcache.
- Cache.setCacheFolder(dataDir): Diese Methode legt den Cache-Ordner auf das angegebene Verzeichnis fest. Jeder von Aspose erstellte Cache wird jetzt hier statt im standardmäßigen temporären Verzeichnis gespeichert.
## Schritt 2: Cache auf Festplatte konfigurieren
Als Nächstes geben wir an, dass unser Cache nur auf der Festplatte gespeichert werden soll. Dies ist insbesondere dann nützlich, wenn Ihre Anwendung große Dateien verwendet und Sie sicherstellen möchten, dass Speicher frei bleibt.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Diese Option stellt sicher, dass der Cache nicht im Speicher gehalten wird, was für die Verarbeitung großer PSD-Dateien von Vorteil ist, da nicht zu viel RAM verbraucht wird.
## Schritt 3: Maximale Festplatten- und Speichercachegröße festlegen
Beschränken wir nun unsere Cache-Größen. Dies ist wichtig, da ein unbegrenzter Cache zu Leistungsproblemen führen kann.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 Gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 Gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): Hiermit wird ein Limit von 1 GB für den Cache auf der Festplatte festgelegt. Sie können diese Größe je nach Bedarf anpassen.
- Cache.setMaxMemoryForCache(1073741824): Dies begrenzt auf ähnliche Weise den Cache im Arbeitsspeicher und stellt sicher, dass Ihre Anwendung nicht zu viel Speicher verwendet.
## Schritt 4: Strategie zur Cache-Neuzuweisung verwalten
Die Verwaltung der Cache-Neuzuweisung ist für die Aufrechterhaltung der Leistung von entscheidender Bedeutung. So können Sie sie einrichten.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): Wenn der Wert auf „false“ gesetzt ist, kann Aspose die Cache-Neuzuweisung flexibler verwalten, was zu einer besseren Leistung führen kann.
## Schritt 5: Zugewiesene Cachegröße prüfen
In diesem Schritt geht es darum, zu überwachen, wie viele Bytes aktuell für den Cache im Speicher oder auf der Festplatte reserviert sind. Lassen Sie uns das implementieren:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Speichert die Anzahl der auf der Festplatte zugewiesenen Bytes.
- long l2: Speichert die Anzahl der im Speicher zugewiesenen Bytes. 
Sie können diese Werte jederzeit überprüfen, um sicherzustellen, dass Ihre Anwendung die Speicher- und Festplattennutzung wie erwartet verwaltet.
## Schritt 6: Erstellen eines PSD-Bildes
Nachdem wir nun unsere Cache-Konfigurationen eingerichtet haben, erstellen wir ein einfaches PSD-Bild.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions-Optionen: Mit diesem Objekt können Sie beim Erstellen eines Photoshop-Bildes Optionen angeben.
- Farbe[] Farbe: Ein Array, das die Farben enthält, die in der Bildpalette verwendet werden.
## Schritt 7: Pixeldaten im Bild speichern
Lassen Sie uns nun unser Bild mit Pixeldaten füllen und speichern.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Farbe[] Pixel: Dies ist ein Array von Farbobjekten. Hier füllen wir es mit weißen Pixeln.
- image.savePixels(image.getBounds(), pixels): Diese Methode speichert die Pixeldaten im Bild. Sie aktualisiert das Bild mit den von uns definierten Farben.
## Schritt 8: Überwachen des zugewiesenen Cache nach der Image-Erstellung
Nach dem Erstellen des Images empfiehlt es sich, noch einmal zu überprüfen, wie viele Bytes für den Cache reserviert sind.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: Erfasst die aktuelle Belegung der Festplatte nach der Image-Erstellung.
- long memoryBytes: Erfasst die aktuelle Zuordnung im Speicher. 
Mithilfe dieses Schritts können Sie ermitteln, wie viel Cache nach Ihren Vorgängen verbraucht wird.
## Schritt 9: Auf ordnungsgemäße Entsorgung achten
Schließlich muss unbedingt sichergestellt werden, dass alle Aspose.PSD-Objekte ordnungsgemäß entsorgt wurden, um Speicherlecks zu vermeiden.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 und l2: Mit diesen Variablen können Sie die endgültige Zuordnung überprüfen. Wenn sie nicht Null sind, bedeutet dies, dass einige Objekte nicht ordnungsgemäß entsorgt wurden.
## Abschluss
Die Steuerung der Cache-Neuzuweisung in Aspose.PSD für Java kann die Leistung Ihrer Anwendung erheblich verbessern. Indem Sie die oben beschriebenen Schritte befolgen, können Sie den Cache effektiv verwalten, den Speicherverbrauch minimieren und effizient schöne PSD-Dateien erstellen. Nutzen Sie diese Techniken und erleben Sie, wie Ihre Anwendungen mit optimaler Leistung gedeihen!
## Häufig gestellte Fragen
### Was ist Aspose.PSD?
Aspose.PSD ist eine Bibliothek für .NET- und Java-Entwickler zum programmgesteuerten Erstellen, Bearbeiten und Konvertieren von Photoshop-Dateien (PSD).
### Wie überprüfe ich die zugewiesene Cachegröße?
 Verwenden Sie Methoden wie`Cache.getAllocatedDiskBytesCount()` Und`Cache.getAllocatedMemoryBytesCount()` um die aktuelle Cache-Nutzung zu überwachen.
### Kann ich ein benutzerdefiniertes Verzeichnis für den Cache festlegen?
 Ja, Sie können ein anderes Verzeichnis angeben, indem Sie`Cache.setCacheFolder("Your Directory Path")`.
### Ist die Nutzung von Aspose.PSD kostenlos?
Aspose.PSD ist eine kostenpflichtige Bibliothek, aber Sie können mit einer kostenlosen Testversion beginnen, die auf deren[Webseite](https://releases.aspose.com/).
### Was passiert, wenn ich Gegenstände nicht entsorge?
Das Nichtentsorgen von Objekten kann zu Speicherlecks führen und dazu führen, dass Ihre Anwendung mehr Ressourcen als nötig verwendet.