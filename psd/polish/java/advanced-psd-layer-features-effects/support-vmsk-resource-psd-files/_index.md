---
date: 2025-12-18
description: Dowiedz się, jak tworzyć maskę wektorową (zasób Vmsk) w plikach PSD przy
  użyciu Aspose.PSD for Java. Ten krok po kroku poradnik pokaże, jak dodać maskę wektorową,
  konwertować PSD na PNG i wiele więcej.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Tworzenie maski wektorowej (zasób Vmsk) w plikach PSD w Javie
url: /pl/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz maskę wektorową (zasób Vmsk) w plikach PSD przy użyciu Javy

## Wprowadzenie
Jeśli potrzebujesz **utworzyć maskę wektorową** (Vmsk) w plikach Photoshop (PSD), Aspose.PSD for Java zapewnia czysty, programowy sposób realizacji tego zadania. Niezależnie od tego, czy tworzysz narzędzie do automatyzacji projektowania, czy dodajesz obsługę własnych masek do istniejącego potoku graficznego, ten samouczek przeprowadzi Cię przez każdy krok — ładowanie PSD, odczyt zasobu Vmsk, modyfikację jego właściwości oraz zapis wyniku. Po zakończeniu będziesz swobodnie pracować z maskami wektorowymi, konwertować PSD na PNG i rozszerzać plik o dodatkowe dane wektorowe.

## Szybkie odpowiedzi
- **Czym jest zasób Vmsk?** To dane maski wektorowej przechowywane wewnątrz pliku PSD, definiujące złożone kształty wektorowe dla warstwy.  
- **Która biblioteka to obsługuje?** Aspose.PSD for Java zapewnia pełny dostęp odczytu/zapisu do zasobów Vmsk.  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa wersja próbna; licencja komercyjna jest wymagana do użytku produkcyjnego.  
- **Czy mogę przekonwertować edytowany PSD na PNG?** Tak — po zapisaniu możesz załadować PSD i wyeksportować go do PNG przy użyciu tego samego API.  
- **Czy dostępna jest obsługa Maven?** Oczywiście; Aspose.PSD można dodać jako zależność Maven (zobacz słowo kluczowe „aspose psd maven”).

## Czym jest maska wektorowa (zasób Vmsk)?
Maska wektorowa (Vmsk) to maska nieoparta na pikselach, wykorzystująca krzywe Béziera i rekordy ścieżek do definiowania przezroczystych i nieprzezroczystych obszarów na warstwie. Ponieważ jest wektorowa, skaluje się bez utraty jakości — idealna dla grafiki wysokiej rozdzielczości.

## Dlaczego tworzyć maskę wektorową przy użyciu Aspose.PSD?
- **Automatyzacja:** Programowo dodawaj lub modyfikuj maski bez otwierania Photoshopa.  
- **Spójność:** Zapewnij, że każdy generowany plik PSD stosuje te same zasady maski.  
- **Cross‑platform:** Działa na każdym systemie operacyjnym obsługującym Javę.  
- **Integracja:** Łącz z innymi API Aspose (np. konwersja PSD → PNG) w pełnych przepływach pracy.

## Prerequisites
Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:

### Czego potrzebujesz
- **Java Development Kit (JDK):** Upewnij się, że masz zainstalowany JDK na swoim komputerze. Jeśli nie, możesz go pobrać ze [strony Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- **Aspose.PSD for Java Library:** To potężna biblioteka do zarządzania plikami PSD. Pobierz ją ze [strony wydania Aspose](https://releases.aspose.com/psd/java/). Dla tych, którzy chcą wypróbować przed zakupem, dostępna jest także [darmowa wersja próbna](https://releases.aspose.com/).
- **IDE:** Dowolne środowisko IDE dla Javy (np. IntelliJ IDEA, Eclipse itp.) będzie odpowiednie dla tego projektu.

### Konfiguracja środowiska pracy
1. **Utwórz nowy projekt Java** – Otwórz wybrane IDE i rozpocznij nowy projekt.  
2. **Dodaj bibliotekę Aspose** – Po pobraniu pliku JAR Aspose, dodaj go do ścieżki kompilacji projektu, aby uzyskać dostęp do wszystkich klas związanych z PSD.

Po przygotowaniu środowiska przejdźmy do rzeczywistej implementacji.

## Jak utworzyć maskę wektorową w plikach PSD przy użyciu Javy
Poniżej znajduje się przewodnik krok po kroku. Bloki kodu pozostają niezmienione w stosunku do oryginalnego samouczka; dodaliśmy jedynie tekst wyjaśniający, aby każdy krok był jasny.

## Importowanie pakietów
Zanim zaczniemy pracować z plikami PSD, musimy zaimportować niezbędne klasy z biblioteki Aspose.PSD.

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

Teraz, gdy przygotowaliśmy scenę, przejdźmy przez każdą operację.

## Krok 1: Załaduj plik PSD
Pierwszą rzeczą, którą musisz zrobić, jest załadowanie pliku PSD. To tutaj zaczyna się cała magia.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Ustawiamy `dataDir` na katalog, w którym znajduje się Twój plik PSD.  
- Tworzymy ciąg znaków `sourceFileName`, łącząc katalog z nazwą pliku PSD.  
- Na koniec ładujemy plik PSD do obiektu `PsdImage` przy użyciu `Image.load()`.

## Krok 2: Pobierz zasób Vmsk
Teraz, gdy nasz obraz PSD jest załadowany, pobierzmy zasób Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Wywołujemy metodę `getVmskResource()`, która zajmuje się wyszukiwaniem i pobieraniem zasobu Vmsk z obrazu.

## Krok 3: Walidacja właściwości zasobu Vmsk
Zanim przystąpimy do modyfikacji, konieczne jest zweryfikowanie, że nasz zasób Vmsk znajduje się w oczekiwanym stanie.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Sprawdzamy różne właściwości zasobu Vmsk. Chcemy mieć pewność, że nie jest wyłączony, odwrócony ani niepowiązany oraz że posiada prawidłową liczbę ścieżek.

## Krok 4: Dostęp do każdej ścieżki i walidacja
Zagłębmy się nieco bardziej i sprawdźmy ścieżki wewnątrz zasobu Vmsk.

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

- Wyodrębniamy trzy konkretne rekordy ścieżek i walidujemy ich typy oraz właściwości, aby upewnić się, że spełniają nasze kryteria.

## Krok 5: Edycja zasobu Vmsk
Teraz przechodzimy do części modyfikacyjnej! Możesz dostosować właściwości zasobu Vmsk według potrzeb.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- W tym bloku przełączamy różne właściwości zasobu Vmsk. Ustawiając je na `true`, kontrolujemy zachowanie maski w pliku PSD.

## Krok 6: Modyfikacja punktów węzłów Béziera
Węzły Béziera są kluczowe dla ścieżek wektorowych. Zmienimy tutaj niektóre wartości.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Dostęp do konkretnych rekordów `BezierKnotRecord` i zmiana ich punktów może przekształcić maskę wektorową.

## Krok 7: Zapisz zmodyfikowany plik PSD
Po zakończeniu wszystkich edycji czas zapisać zmodyfikowany plik PSD.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Ustawiamy ścieżkę dla eksportowanego pliku PSD, a następnie wywołujemy `im.save()`, aby zapisać zmiany w nowym pliku.

## Krok 8: Czyszczenie zasobów
Na koniec musimy upewnić się, że prawidłowo zwalniamy zasoby obrazu.

```java
im.dispose();
```

- Zawsze warto zwolnić wszelkie zasoby po zakończeniu pracy. Pomaga to uniknąć wycieków pamięci w aplikacjach.

## Conclusion
Gratulacje! Właśnie przeszedłeś szczegółowy proces **tworzenia maski wektorowej** (Vmsk) w plikach PSD przy użyciu Aspose.PSD for Java. Od załadowania obrazu, przez pobranie i walidację zasobu Vmsk, edycję jego właściwości, po zapis zmodyfikowanego PSD — masz teraz solidne podstawy do automatyzacji przepływów pracy z maskami wektorowymi. Wykorzystaj te techniki, aby wzbogacić swoje pipeline’y projektowe, integrować się z innymi API Aspose (np. konwersja PSD do PNG) lub budować własne narzędzia graficzne.

## Najczęściej zadawane pytania
**Q: How do I add a new vector mask to an existing layer?**  
A: Create a `VmskResource`, populate it with the required path records (e.g., `BezierKnotRecord`), and attach it to the layer’s resources collection.  

**Q: Can I convert the edited PSD directly to PNG without opening Photoshop?**  
A: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")` specifying the PNG format.  

**Q: Is there a way to automate this in a CI/CD pipeline?**  
A: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle builds, Docker containers, or any CI system that supports Java.  

**Q: What versions of Aspose.PSD are compatible with Java 11+?**  
A: All recent releases (2024‑2025) support Java 8 and above, including Java 11, 17, and newer LTS versions.  

**Q: Do I need a license for development builds?**  
A: A free evaluation license works for development and testing. For production deployments, a commercial license is required.  

---

**Ostatnia aktualizacja:** 2025-12-18  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
