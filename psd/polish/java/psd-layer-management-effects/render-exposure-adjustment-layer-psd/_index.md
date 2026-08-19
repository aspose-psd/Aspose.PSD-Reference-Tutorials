---
date: 2026-04-05
description: Dowiedz się, jak renderować warstwę korekty ekspozycji w plikach PSD
  przy użyciu Aspose.PSD dla Javy. Przewodnik krok po kroku z przykładami kodu, jak
  modyfikować i dodawać warstwy ekspozycji.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: Renderowanie warstwy dopasowania ekspozycji w plikach PSD – Java
second_title: Aspose.PSD Java API
title: Renderowanie warstwy korekcji ekspozycji w plikach PSD – Java
url: /pl/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderowanie warstwy korekcji ekspozycji w plikach PSD - Java

## Wprowadzenie

Czy pracujesz z plikami Photoshop PSD i potrzebujesz **renderować warstwę korekcji ekspozycji** programowo? Niezależnie od tego, czy modyfikujesz istniejące warstwy, czy dodajesz nowe, Aspose.PSD for Java zapewnia potężny i intuicyjny sposób radzenia sobie z tymi zadaniami. W tym przewodniku pokażemy, jak używać Aspose.PSD for Java do renderowania i modyfikacji warstw korekcji ekspozycji w plikach PSD. Po zakończeniu tego tutorialu będziesz wiedział, jak dostosować ustawienia ekspozycji w istniejących warstwach oraz dodać nowe warstwy korekcji ekspozycji do swoich plików PSD. Zanurzmy się!

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.PSD for Java
- **Czy mogę edytować istniejącą warstwę ekspozycji?** Yes, you can change exposure, offset, and gamma correction.
- **Jak dodać nową warstwę korekcji ekspozycji?** Use `addExposureAdjustmentLayer()` on a `PsdImage` instance.
- **Czy obsługiwany jest eksport PNG?** Absolutely – use `PngOptions` to save the result as a PNG.
- **Czy potrzebna jest licencja do produkcji?** A commercial license is required for production use; a free trial is available.

## Co to jest renderowanie warstwy korekcji ekspozycji?

Warstwa korekcji ekspozycji to niedestrukcyjna warstwa Photoshop, która zmienia jasność, offset i gamma podstawowego obrazu. Renderowanie jej oznacza zastosowanie tych ustawień, tak aby wynik wizualny odzwierciedlał korekty, które następnie można wyeksportować do formatów takich jak PNG.

## Dlaczego używać Aspose.PSD for Java do renderowania warstwy korekcji ekspozycji?

- **Pełna kontrola** – manipuluj właściwościami warstwy bez otwierania Photoshopa.
- **Przetwarzanie wsadowe** – automatyzuj korekty w wielu plikach.
- **Cross‑platform** – uruchamiaj na dowolnym systemie z JDK.
- **Zachowuje strukturę PSD** – utrzymuj warstwy edytowalne do przyszłych modyfikacji.

## Wymagania wstępne

1. **Java Development Kit (JDK)** – co najmniej JDK 8.
2. **Aspose.PSD for Java** – pobierz go z [tutaj](https://releases.aspose.com/psd/java/).
3. **Basic Java knowledge** – powinieneś być zaznajomiony ze standardową składnią Java.
4. **IDE or Text Editor** – IntelliJ IDEA, Eclipse, VS Code lub dowolny edytor, który preferujesz.

## Importowanie pakietów

Najpierw zaimportuj wymagane klasy Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Jak renderować warstwę korekcji ekspozycji – przewodnik krok po kroku

### Krok 1: Załaduj plik PSD

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

Zastąp `"Your Document Directory"` folderem zawierającym Twoje pliki PSD. Metoda `Image.load()` zwraca obiekt `PsdImage`, który zapewnia pełny dostęp do warstw dokumentu.

### Krok 2: Edytuj istniejącą warstwę korekcji ekspozycji

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

Pętla przechodzi przez wszystkie warstwy, znajduje każdą `ExposureLayer` i aktualizuje jej trzy kluczowe parametry. To jest sedno **renderowania warstwy korekcji ekspozycji** z własnymi wartościami.

### Krok 3: Zapisz zmodyfikowany plik PSD

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

Zmodyfikowany plik PSD zachowuje wszystkie oryginalne warstwy, ale korekcja ekspozycji odzwierciedla teraz nowe ustawienia.

### Krok 4: Wyeksportuj wynik jako PNG

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

Użycie `PngOptions` z `TruecolorWithAlpha` zapewnia, że wyeksportowany PNG zachowuje pełną głębię kolorów oraz ewentualną przezroczystość z PSD.

### Krok 5: Dodaj nową warstwę korekcji ekspozycji

Jeśli potrzebujesz **dodać nową warstwę korekcji ekspozycji** do istniejącego dokumentu, użyj poniższego kodu:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

Metoda `addExposureAdjustmentLayer` tworzy nową warstwę korekcji z określonymi wartościami ekspozycji, offsetu i gamma, po czym możesz ją renderować i eksportować tak jak wcześniej.

## Typowe problemy i wskazówki

- **Warstwa nie znaleziona** – Upewnij się, że PSD faktycznie zawiera `ExposureLayer`. Użyj `instanceof ExposureLayer` jak pokazano, aby uniknąć `ClassCastException`.
- **Błędy ścieżki pliku** – Używaj ścieżek bezwzględnych lub sprawdź, czy `dataDir` kończy się separatorem plików (`/` lub `\`).
- **Wyjątek licencyjny** – Uruchomienie bez ważnej licencji doda znak wodny do wyniku. Zarejestruj licencję wcześnie w kodzie (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## Najczęściej zadawane pytania

### Co to jest Aspose.PSD for Java?

Aspose.PSD for Java to biblioteka umożliwiająca programowe tworzenie, edytowanie i konwertowanie plików PSD przy użyciu Javy. Zapewnia kompleksową funkcjonalność pracy z dokumentami Photoshop.

### Czy mogę używać Aspose.PSD for Java do manipulacji innymi typami warstw?

Tak, Aspose.PSD for Java obsługuje różne typy warstw, w tym warstwy tekstowe, warstwy korekcji i warstwy obrazu, umożliwiając rozległą manipulację plikami PSD.

### Jak rozpocząć pracę z Aspose.PSD for Java?

Możesz rozpocząć od pobrania biblioteki ze [strony internetowej](https://releases.aspose.com/psd/java/) i zapoznania się z [dokumentacją](https://reference.aspose.com/psd/java/) w celu uzyskania szczegółowych przewodników i przykładów.

### Czy dostępna jest darmowa wersja próbna Aspose.PSD for Java?

Tak, dostępna jest darmowa wersja próbna. Możesz ją pobrać [tutaj](https://releases.aspose.com/).

### Jak mogę uzyskać wsparcie dla Aspose.PSD for Java?

Aby uzyskać wsparcie, możesz odwiedzić [forum wsparcia Aspose](https://forum.aspose.com/c/psd/34), gdzie możesz zadawać pytania i uzyskać pomoc od społeczności.

**Dodatkowe pytania**

**P: Czy mogę przetwarzać wsadowo wiele plików PSD?**  
A: Oczywiście. Umieść logikę ładowania, edycji i zapisywania w pętli, która iteruje po liście ścieżek plików.

**P: Czy biblioteka zachowuje hierarchię warstw, gdy dodaję nową warstwę ekspozycji?**  
A: Tak. Nowa warstwa jest dodawana na wierzchu istniejących warstw, zachowując pierwotną hierarchię.

**P: Do jakich formatów obrazów mogę eksportować oprócz PNG?**  
A: Aspose.PSD obsługuje JPEG, BMP, TIFF i kilka innych formatów za pomocą odpowiednich klas `*Options`.

---

**Ostatnia aktualizacja:** 2026-04-05  
**Testowano z:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}