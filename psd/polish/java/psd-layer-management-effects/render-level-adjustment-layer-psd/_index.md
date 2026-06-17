---
date: 2026-04-05
description: Dowiedz się, jak wyeksportować plik PSD do PNG i bez wysiłku poprawić
  kontrast obrazu przy użyciu Aspose.PSD dla Javy. Opanuj warstwy dopasowania poziomów
  dzięki temu przewodnikowi krok po kroku.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Eksportuj PSD do PNG i renderuj warstwę dopasowania poziomu w Javie
second_title: Aspose.PSD Java API
title: Eksportuj PSD do PNG i renderuj warstwę dopasowania poziomu w Javie
url: /pl/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj PSD do PNG i renderuj warstwę dopasowania poziomów w Javie

## Wprowadzenie

Czy kiedykolwiek otworzyłeś plik PSD i zauważyłeś, że kolory wyglądają na płaskie lub kontrast jest nieodpowiedni? Możesz szybko **export PSD to PNG**, jednocześnie precyzyjnie dostosowując obraz za pomocą warstwy dopasowania poziomów przy użyciu Aspose.PSD for Java. W tym samouczku przeprowadzimy Cię przez cały proces — od wczytania PSD, regulacji poziomów, po zapisanie wyniku jako PNG — abyś mógł zwiększyć żywotność kolorów i przygotować zasoby gotowe do sieci w kilka minut.

## Szybkie odpowiedzi
- **Co oznacza „export PSD to PNG”?** Konwertuje dokument Photoshop na bezstratny obraz PNG, zachowując przezroczystość.  
- **Czy mogę dostosować poziomy przed eksportem?** Tak, Aspose.PSD pozwala programowo modyfikować poziomy wejściowe i wyjściowe.  
- **Czy potrzebuję licencji?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy przetwarzanie wsadowe jest możliwe?** Oczywiście — możesz umieścić kod w pętli, aby obsłużyć wiele plików PSD.  
- **Która wersja Javy jest wymagana?** Zalecana jest Java 8 lub nowsza.

## Co to jest „export PSD to PNG”?
Eksportowanie PSD do PNG oznacza wzięcie warstwowego pliku Photoshop i spłaszczenie go do obrazu Portable Network Graphics. PNG obsługuje bezstratną kompresję oraz kanał alfa, co czyni go idealnym do grafiki internetowej i zasobów interfejsu użytkownika.

## Dlaczego dostosować poziomy przed eksportem?
Dostosowanie poziomów pozwala kontrolować cienie, półtony i podświetlenia, poprawiając ogólny kontrast i balans kolorów. Ten krok zapewnia, że końcowy PNG wygląda dopracowanie, bez konieczności ręcznej edycji w Photoshopie.

## Wymagania wstępne

- **Java Development Kit (JDK)** – pobierz najnowszą wersję ze strony Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – pobierz ją z oficjalnej strony pobierania ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Dostępna jest wersja próbna ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Importowanie pakietów

Zanim przejdziesz do kodu, zaimportuj klasy, które zapewniają dostęp do manipulacji PSD i eksportu PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Przewodnik krok po kroku

### Krok 1: Zdefiniuj ścieżki plików (Jak zautomatyzować przetwarzanie PSD)

Ustaw jasne, opisowe zmienne dla źródłowego PSD, zmodyfikowanego PSD oraz docelowej lokalizacji eksportu PNG.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Krok 2: Wczytaj obraz PSD

Użyj `Image.load`, aby wczytać plik PSD do obiektu `PsdImage`. Aspose.PSD automatycznie wykrywa format.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Krok 3: Iteruj przez warstwy (Jak dostosować poziomy)

Przejdź pętlą po każdej warstwie, aby znaleźć warstwę dopasowania poziomów.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Krok 4: Zidentyfikuj warstwę poziomów

Sprawdź każdą warstwę przy użyciu `instanceof LevelsLayer`. Gdy zostanie znaleziona, rzutuj ją, aby móc modyfikować jej właściwości.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Krok 5: Precyzyjnie dopasuj poziomy (Jak dostosować poziomy)

Dostosuj zarówno poziomy wejściowe, jak i wyjściowe dla pierwszego kanału (zwykle kanał złożony). Te wartości są przykładami; możesz swobodnie eksperymentować.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Krok 6: Zapisz zmodyfikowany PSD (Jak zautomatyzować PSD)

Zapisz zmiany do nowego pliku PSD.

```java
im.save(psdPathAfterChange);
```

### Krok 7: Eksportuj jako PNG (Export PSD to PNG)

Jeśli potrzebujesz wersji PNG, skonfiguruj `PngOptions` i zapisz obraz.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Typowe przypadki użycia

- **Przygotowanie zasobów webowych:** Konwertuj udostępnione przez projektanta mockupy PSD na PNG gotowe do przeglądarek.  
- **Przetwarzanie wsadowe:** Zautomatyzuj konwersję dziesiątek plików PSD w potoku CI.  
- **Dynamiczne generowanie obrazów:** Dostosuj poziomy w locie na podstawie danych wejściowych użytkownika przed eksportem.  

## Rozwiązywanie problemów i wskazówki

- **Null pointer przy dostępie do warstw:** Upewnij się, że PSD rzeczywiście zawiera warstwę Levels Adjustment Layer; w przeciwnym razie dodaj sprawdzenie null.  
- **Nieoczekiwane kolory po eksporcie:** Sprawdź, czy typ koloru PNG jest ustawiony na `TruecolorWithAlpha`, aby zachować przezroczystość.  
- **Wydajność przy wielu plikach:** Ponownie używaj tego samego obiektu `PsdImage` podczas przetwarzania wsadu, aby zmniejszyć zużycie pamięci.  

## Najczęściej zadawane pytania

**Q: Czy mogę dostosować poszczególne kanały kolorów (RGB) osobno?**  
A: Tak. Użyj `levelsLayer.getChannel(index)`, gdzie `index` = 0 (Red), 1 (Green), 2 (Blue), aby regulować każdy kanał niezależnie.

**Q: Jak obsłużyć wiele warstw Levels Adjustment Layers w jednym PSD?**  
A: Pętla przetwarza każdą warstwę; każda znaleziona `LevelsLayer` zostanie dostosowana zgodnie z kodem wewnątrz bloku `if`.

**Q: Czy istnieją inne sposoby poprawy kontrastu poza Levels?**  
A: Aspose.PSD oferuje również korekty Curves, Brightness/Contrast oraz Histogram Equalization.

**Q: Czy mogę zautomatyzować to dla folderu plików PSD?**  
A: Umieść cały przepływ pracy w pętli `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` i przetwarzaj każdy plik kolejno.

**Q: Gdzie mogę znaleźć więcej dokumentacji i wsparcia?**  
A: Odwiedź oficjalną dokumentację ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) oraz forum społeczności ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).  

## Podsumowanie

Opanowując przepływ pracy **export PSD to PNG** i ucząc się **jak dostosować poziomy** programowo, zyskujesz pełną kontrolę nad jakością obrazu bez opuszczania środowiska Java. Niezależnie od tego, czy przygotowujesz zasoby na potrzeby sieci, automatyzujesz pipeline projektowy, czy tworzysz przetwarzanie wsadowe, Aspose.PSD for Java sprawia, że zadanie jest proste i niezawodne.

---

**Ostatnia aktualizacja:** 2026-04-05  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}