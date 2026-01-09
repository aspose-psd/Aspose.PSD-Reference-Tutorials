---
date: 2026-01-09
description: „Dowiedz się, jak konwertować pliki PSD na PNG przy użyciu progowania
  Bradley w Aspose.PSD dla Javy. Ten przewodnik pokazuje, jak wybrać optymalny próg
  i efektywnie binaryzować obraz PSD.”
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: Konwertuj PSD na PNG z progowaniem Bradley (Aspose.PSD Java)
url: /pl/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj PSD do PNG przy użyciu progowania Bradley (Aspose.PSD Java)

Witamy w tym kompleksowym przewodniku dotyczącym **convert PSD to PNG** przy użyciu progowania Bradley w Aspose.PSD dla Javy. W ciągu kilku minut zobaczysz, dlaczego ta technika jest idealna do tworzenia wysokiego kontrastu, binarnych plików PNG z dokumentów Photoshop oraz otrzymasz praktyczne, krok po kroku wyjaśnienie.

## Szybkie odpowiedzi
- **Can I convert PSD to PNG with Aspose.PSD?** Tak – załaduj plik PSD, zastosuj `binarizeBradley`, a następnie zapisz jako PNG.  
- **What does “choose optimal threshold” mean?** To wartość czułości (0‑1), która decyduje, jak ciemne/jaśne piksele są klasyfikowane.  
- **Do I need a license for production use?** Wymagana jest licencja komercyjna; darmowa wersja próbna działa w celach ewaluacyjnych.  
- **Which image formats are supported for saving?** PNG, JPEG, BMP i wiele innych za pośrednictwem klas `ImageOptions`.  
- **Is the code compatible with Java 8 and later?** Absolutnie – Aspose.PSD Java API obsługuje Java 8+.

## Czym jest progowanie Bradley?
Progowanie Bradley to adaptacyjny algorytm binaryzacji, który oblicza lokalną średnią dla każdego piksela i porównuje intensywność piksela z tą średnią pomnożoną przez zdefiniowany przez użytkownika próg. Wynikiem jest czysty obraz czarno‑biały, zachowujący ważne szczegóły.

## Dlaczego konwertować PSD do PNG przy użyciu progowania Bradley?
- **Zachowaj ostre krawędzie** – Idealny dla OCR, wykrywania kodów kreskowych lub dowolnego przepływu pracy, który wymaga wyraźnego rozdzielenia pierwszego planu od tła.  
- **Zmniejsz rozmiar pliku** – PNG jest bezstratny, ale po binaryzacji często jest mniejszy.  
- **Kompatybilność międzyplatformowa** – PNG działa wszędzie, podczas gdy PSD jest specyficzny dla Photoshopa.  

## Wymagania wstępne
Przed rozpoczęciem upewnij się, że masz:

1. **Java Development Environment** – JDK 8 lub nowszy zainstalowany.  
2. **Aspose.PSD Library** – Pobierz najnowszy JAR z [here](https://releases.aspose.com/psd/java/).  
3. **Sample PSD Image** – Dowolny plik PSD, który chcesz przekonwertować; możesz także użyć przykładu dostarczonego w przykładach Aspose.

## Importowanie pakietów
Begin by importing the necessary classes into your Java project:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Jak konwertować PSD do PNG przy użyciu progowania Bradley
Poniżej znajduje się pełny przepływ pracy podzielony na czytelne, numerowane kroki. Każdy krok zawiera krótkie wyjaśnienie oraz dokładny kod, który należy skopiować i wkleić.

### Krok 1: Załaduj obraz PSD
Najpierw wskaż plik źródłowy i załaduj go przy użyciu Aspose.PSD.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### Krok 2: Wybierz optymalny próg
Wartość progu (zakres 0 – 1) kontroluje intensywność binaryzacji. Typowym punktem wyjścia jest **0.15**, ale możesz go dostosować do swojego obrazu.

```java
// Define threshold value
double threshold = 0.15;
```

### Krok 3: Binaryzuj obraz PSD
Teraz zastosuj algorytm Bradley. Ten krok **binarize PSD image** na podstawie wybranego progu.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### Krok 4: Zapisz wynik jako PNG
Finally, write the processed image to disk in PNG format.

```java
// Save the output image
image.save(destName, new PngOptions());
```

Powtórz te kroki dla dowolnej liczby plików PSD, które musisz przetworzyć, dostosowując próg w razie potrzeby, aby uzyskać najlepszy efekt wizualny.

## Typowe problemy i wskazówki
- **Threshold too low/high:** Jeśli wynik wygląda zbyt zaszumiony lub wyblakły, dostosuj wartość `threshold` stopniowo (np. 0.10 – 0.20).  
- **Memory consumption:** Duże pliki PSD mogą wymagać dużo pamięci. Rozważ przetwarzanie ich pojedynczo lub zwiększenie rozmiaru sterty JVM (`-Xmx`).  
- **Preview before saving:** Użyj `image.save("preview.bmp", new BmpOptions());`, aby sprawdzić binaryzowany rezultat przed ostatecznym eksportem PNG.

## Najczęściej zadawane pytania

**Q: Jaka jest różnica między `binarizeBradley` a innymi metodami progowania?**  
A: `binarizeBradley` oblicza lokalną średnią dla każdego piksela, co czyni ją bardziej odporną na obrazy o nierównomiernym oświetleniu w porównaniu do progowania globalnego.

**Q: Czy mogę zastosować progowanie Bradley do plików JPEG lub BMP?**  
A: Tak. Załaduj dowolny obsługiwany format za pomocą `Image.load(...)`, a następnie wywołaj `binarizeBradley` przed zapisem.

**Q: Czy istnieje sposób na podgląd binaryzowanego obrazu przed zapisaniem?**  
A: Oczywiście. Użyj dowolnej z opcji zapisu obrazu Aspose.PSD (np. BMP), aby zapisać tymczasowy plik podglądowy.

**Q: Gdzie mogę znaleźć więcej wsparcia i zasobów?**  
A: Odwiedź [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) aby uzyskać pomoc społeczności oraz zapoznaj się z pełną [documentation](https://reference.aspose.com/psd/java/) w celu zaawansowanych scenariuszy.

## Podsumowanie
Nauczyłeś się teraz, jak **convert PSD to PNG** efektywnie, **wybierając optymalny próg** i **binaryzując obraz PSD** przy użyciu progowania Bradley. To podejście jest idealne dla przepływów pracy, które wymagają czystych, wysokiego kontrastu plików PNG z złożonych plików Photoshop.

---

**Ostatnia aktualizacja:** 2026-01-09  
**Testowano z:** Aspose.PSD Java 23.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}