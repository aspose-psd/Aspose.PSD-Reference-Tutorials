---
date: 2026-03-15
description: Dowiedz się, jak kompresować pliki PNG przy użyciu Aspose.PSD dla Javy
  – krok po kroku przewodnik, jak kompresować PNG, optymalizować rozmiar PNG i efektywnie
  konwertować PSD na PNG.
linktitle: Compress PNG Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak kompresować pliki PNG przy użyciu Aspose.PSD dla Javy
url: /pl/java/optimizing-png-files/compress-png-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak kompresować pliki PNG przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

Kiedy w programowaniu musisz obsługiwać obrazy, nauka **jak kompresować PNG** w sposób efektywny może znacząco przyspieszyć ładowanie stron i zmniejszyć zużycie przepustowości. Aspose.PSD dla Javy to potężna biblioteka, która umożliwia pracę z plikami Photoshop (PSD) i ich eksport do różnych formatów, w tym PNG. Niezależnie od tego, czy potrzebujesz **optymalizacji rozmiaru PNG**, konwersji PSD do PNG dla galerii internetowej, czy precyzyjnego dostosowania **poziomów kompresji PNG**, ten samouczek przeprowadzi Cię przez kompletny, gotowy do produkcji przykład.

## Szybkie odpowiedzi
- **Co oznacza „jak kompresować PNG”?** Odnosi się do zmniejszenia rozmiaru pliku obrazu PNG przy zachowaniu jakości wizualnej, zazwyczaj poprzez dostosowanie parametrów kompresji.  
- **Która biblioteka jest najlepsza do kompresji PNG w Javie?** Aspose.PSD dla Javy oferuje wbudowane opcje PNG i obsługuje pełny zakres poziomów kompresji (0‑9).  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę automatyzować wiele poziomów kompresji?** Tak — poprzez pętlę po właściwości `setCompressionLevel` możesz generować PNG o każdym poziomie.  
- **Czy to rozwiązanie nadaje się do dużych plików PSD?** Zdecydowanie; Aspose.PSD strumieniuje dane efektywnie, co jest bezpieczne dla zasobów wysokiej rozdzielczości.

## Co to jest kompresja PNG?

PNG wykorzystuje kompresję bezstratną, co oznacza, że jakość obrazu pozostaje niezmieniona, a rozmiar pliku zostaje zmniejszony. Poprzez regulację **poziomu kompresji PNG** (0 = brak kompresji, 9 = maksymalna kompresja) kontrolujesz, jak intensywnie dane są pakowane. Wyższe poziomy wymagają nieco więcej czasu, ale dają mniejsze pliki — idealne do optymalizacji sieciowej.

## Dlaczego używać Aspose.PSD dla Javy do kompresji PNG?

- **Pełne wsparcie PSD** – Otwieraj, edytuj i eksportuj warstwy PSD bez utraty informacji.  
- **Szczegółowa kontrola** – Ustaw dokładny poziom kompresji PNG, typ koloru i głębię bitową.  
- **Cross‑platform** – Działa w każdym środowisku kompatybilnym z Javą, od aplikacji desktopowych po usługi w chmurze.  
- **Wydajność** – Zoptymalizowany kod natywny zapewnia szybkie przetwarzanie nawet dużych obrazów.  

## Prerequisites

Zanim przejdziesz do kodu, upewnij się, że masz następujące elementy:

1. **Java JDK** – Pobierz najnowszy JDK ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – Pobierz najnowszy plik JAR z oficjalnej strony pobierania [tutaj](https://releases.aspose.com/psd/java/).  
3. **IDE lub edytor kodu** – IntelliJ IDEA, Eclipse lub VS Code będą w pełni wystarczające.  
4. **Podstawowa znajomość Javy** – Znajomość obsługi wyjątków i operacji I/O przyspieszy proces nauki.  
5. **Przykładowy plik PSD** – Umieść plik PSD (np. `sample.psd`) w folderze, który będziesz odnosić jako katalog dokumentów.

Posiadanie tych elementów pozwoli Ci skupić się na krokach **java image optimization**, zamiast na problemach konfiguracyjnych.

## Importowanie pakietów

Poniższe importy dają dostęp do podstawowych klas Aspose.PSD oraz opcji PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Te klasy umożliwiają załadowanie PSD, skonfigurowanie ustawień PNG i zapis wyniku.

## Krok 1: Skonfiguruj swój projekt

Utwórz nowy projekt Java (np. `PsdImageCompressor`) i dodaj plik JAR Aspose.PSD do ścieżki budowania. Dzięki temu kompilator będzie mógł znaleźć odwołania do klas wymienionych powyżej.

## Krok 2: Zdefiniuj katalog dokumentów

Powiedz programowi, gdzie znajduje się źródłowy plik PSD i gdzie zapisać skompresowane PNG:

```java
String dataDir = "Your Document Directory"; // Replace with actual path
```

Zastąp `"Your Document Directory"` absolutną lub względną ścieżką, w której znajduje się `sample.psd`. Utrzymanie ścieżki jako konfigurowalnej ułatwia **konwersję PSD do PNG** w różnych środowiskach.

## Krok 3: Załaduj obraz PSD

Załaduj plik PSD do pamięci. Ten krok jest analogiczny do otwarcia książki przed rozpoczęciem czytania:

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Jeśli plik nie zostanie znaleziony, Aspose.PSD zgłosi informacyjny wyjątek — sprawdź dokładnie nazwę pliku i ścieżkę.

## Krok 4: Pętla po poziomach kompresji

Aby przetestować każdy możliwy **poziom kompresji png**, używamy prostej pętli `for`. Automatycznie tworzy ona dziewięć dodatkowych plików PNG, każdy z innym ustawieniem kompresji:

```java
for (int i = 0; i <= 9; i++) {
    // Create a new instance of PngOptions
    PngOptions options = new PngOptions();
    options.setCompressionLevel(i); // Set the compression level
```

Pętla działa od 0 (brak kompresji) do 9 (maksymalna kompresja), dając wyraźny obraz kompromisu między rozmiarem pliku a czasem przetwarzania.

## Krok 5: Zapisz skompresowane pliki PNG

Wewnątrz pętli zapisz każdy PNG używając nazwy pliku odzwierciedlającej poziom kompresji. To ułatwia porównanie:

```java
    psdImage.save(dataDir + i + "_out.png", options);
}
```

Po zakończeniu pętli w Twoim katalogu znajdziesz pliki o nazwach `0_out.png`, `1_out.png`, … `9_out.png`.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **FileNotFoundException** | Nieprawidłowa ścieżka `dataDir` lub brak pliku `sample.psd`. | Zweryfikuj ciąg ścieżki i upewnij się, że plik PSD istnieje. |
| **OutOfMemoryError** on large PSDs | Ładowanie ogromnego PSD bez wystarczającej pamięci sterty. | Zwiększ pamięć JVM (`-Xmx2g`) lub przetwarzaj obraz w partiach. |
| **Compressed PNG looks unchanged** | Użyto niskiego poziomu kompresji (0‑2). | Podnieś poziom do 5‑9, aby uzyskać zauważalne zmniejszenie rozmiaru. |
| **LicenseException** | Uruchomiono bez ważnej licencji Aspose.PSD. | Zastosuj licencję próbną lub zakup pełną licencję. |

## Najczęściej zadawane pytania

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java to biblioteka, która pozwala programistom programowo manipulować plikami Photoshop, w tym odczytywać, edytować i eksportować je do formatów takich jak PNG, JPEG i TIFF.

**Q: Can I compress other image formats besides PNG?**  
A: Ten samouczek koncentruje się na PNG, ale Aspose.PSD obsługuje PSD, TIFF, JPEG, BMP i inne. Możesz zmienić klasę opcji wyjściowych, aby skierować wynik do innego formatu.

**Q: Do I need a license to use Aspose.PSD?**  
A: Choć możesz ocenić bibliotekę w wersji próbnej, pełna licencja jest wymagana w środowiskach produkcyjnych. Licencję możesz uzyskać [tutaj](https://purchase.aspose.com/buy).

**Q: What if I encounter an error while running the code?**  
A: Sprawdź ponownie ścieżki plików, upewnij się, że wszystkie instrukcje importu są obecne i zweryfikuj, czy używasz kompatybilnej wersji pliku JAR Aspose.PSD.

**Q: Where can I find more documentation on Aspose.PSD for Java?**  
A: Szczegółowe referencje API i dodatkowe przykłady dostępne są pod adresem [Aspose.PSD reference](https://reference.aspose.com/psd/java/).

---

**Ostatnia aktualizacja:** 2026-03-15  
**Testowane z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}