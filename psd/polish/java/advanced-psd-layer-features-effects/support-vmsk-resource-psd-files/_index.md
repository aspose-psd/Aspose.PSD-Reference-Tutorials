---
date: 2026-02-22
description: Dowiedz się, jak tworzyć maski wektorowe w Javie przy użyciu Aspose.PSD
  for Java, dodawać maski wektorowe do plików PSD oraz programowo manipulować zasobami
  Vmsk.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Tworzenie wektorowej maski w Javie – zasób Vmsk w plikach PSD
url: /pl/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie maski wektorowej w Javie – zasób Vmsk w plikach PSD

## Introduction
Jeśli potrzebujesz **create vector mask** (Vmsk) zasobów wewnątrz plików Photoshop (PSD), Aspose.PSD for Java zapewnia czysty, programowy sposób ich tworzenia. Niezależnie od tego, czy budujesz narzędzie do automatyzacji projektowania, czy dodajesz obsługę niestandardowych masek do istniejącego potoku graficznego, ten samouczek przeprowadzi Cię przez każdy krok — ładowanie PSD, odczyt zasobu Vmsk, dostosowywanie jego właściwości i zapisywanie wyniku. Po zakończeniu będziesz pewnie obsługiwać maski wektorowe, konwertować PSD na PNG oraz rozszerzać plik o dodatkowe dane wektorowe — wszystko przy użyciu technik **create vector mask java**.

## Quick Answers
- **Co to jest zasób Vmsk?** To dane maski wektorowej przechowywane w pliku PSD, definiujące złożone kształty wektorowe dla warstwy.  
- **Która biblioteka to obsługuje?** Aspose.PSD for Java zapewnia pełny dostęp odczyt/zapis do zasobów Vmsk.  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa wersja próbna; licencja komercyjna jest wymagana do użytku produkcyjnego.  
- **Czy mogę przekonwertować edytowany PSD na PNG?** Tak — po zapisaniu możesz wczytać PSD i wyeksportować do PNG przy użyciu tego samego API.  
- **Czy dostępna jest obsługa Maven?** Oczywiście; Aspose.PSD można dodać jako zależność Maven (zobacz słowo kluczowe „aspose psd maven”).

## What is a Vector Mask (Vmsk Resource)?
Maska wektorowa (Vmsk) to maska nieoparta na pikselach, która wykorzystuje krzywe Béziera i rekordy ścieżek do definiowania przezroczystych i nieprzezroczystych obszarów na warstwie. Ponieważ jest oparta na wektorach, skaluje się bez utraty jakości — idealna dla grafiki wysokiej rozdzielczości.

## Why Create a Vector Mask with Aspose.PSD?
- **Automatyzacja:** Programowo dodawaj lub modyfikuj maski bez otwierania Photoshopa.  
- **Spójność:** Zapewnij, że każdy generowany PSD stosuje te same zasady maski.  
- **Cross‑platform:** Działa na każdym systemie operacyjnym obsługującym Javę.  
- **Integracja:** Łącz z innymi API Aspose (np. konwersja PSD → PNG) w pełnych przepływach pracy.  
- **Skalowalność:** Maski wektorowe pozostają ostre przy dowolnym rozmiarze, co czyni je idealnymi dla responsywnych projektów.

## Why This Matters for Java Developers
Używanie technik **create vector mask java** pozwala osadzić zaawansowaną logikę graficzną bezpośrednio w usługach back‑end, pipeline’ach CI lub narzędziach desktopowych. Nie potrzebujesz już projektanta do ręcznego dodawania masek; Twój kod może generować lub modyfikować je w locie, oszczędzając czas i redukując błędy ludzkie.

## Prerequisites
Before we dive into the code, make sure you have the following:

### What You Need
- Java Development Kit (JDK): Upewnij się, że masz zainstalowany JDK na swoim komputerze. Jeśli nie, możesz go pobrać ze [strony Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: To potężna biblioteka do zarządzania plikami PSD. Możesz ją pobrać ze [strony wydania Aspose](https://releases.aspose.com/psd/java/). Dla osób, które chcą wypróbować przed zakupem, dostępna jest również [darmowa wersja próbna](https://releases.aspose.com/).
- An IDE: Dowolne środowisko IDE dla Javy (np. IntelliJ IDEA, Eclipse itp.) będzie odpowiednie dla tego projektu.

### Setting Up Your Workspace
1. **Utwórz nowy projekt Java** – Otwórz wybrane IDE i rozpocznij nowy projekt.  
2. **Dodaj bibliotekę Aspose** – Po pobraniu pliku JAR Aspose, dodaj go do ścieżki kompilacji projektu, aby mieć dostęp do wszystkich klas związanych z PSD.

Po przygotowaniu środowiska, przejdźmy do rzeczywistej implementacji.

## How to create vector mask in PSD files with Java
Poniżej znajduje się przewodnik krok po kroku. Bloki kodu pozostają niezmienione w stosunku do oryginalnego samouczka; dodaliśmy jedynie tekst wyjaśniający, aby każdy krok był całkowicie jasny.

### Import Packages
Zanim będziemy mogli pracować z plikami PSD, musimy zaimportować niezbędne klasy z biblioteki Aspose.PSD.

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

Teraz, gdy przygotowaliśmy scenę, przejdźmy przez każde działanie.

### Step 1: Load Your PSD File
Pierwszą rzeczą, którą należy zrobić, jest wczytanie pliku PSD. To tutaj zaczyna się cała magia.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Ustawiamy `dataDir` na katalog zawierający plik PSD.  
- Tworzymy ciąg znaków `sourceFileName`, łącząc katalog z nazwą pliku PSD.  
- Na koniec wczytujemy plik PSD do obiektu `PsdImage` przy użyciu `Image.load()`.

### Step 2: Retrieve the Vmsk Resource
Teraz, gdy nasz obraz PSD jest wczytany, pobierzmy zasób Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Wywołujemy metodę `getVmskResource()`, która obsługuje wyszukiwanie i pobieranie zasobu Vmsk z obrazu.

### Step 3: Validate Vmsk Resource Properties
Przed przystąpieniem do modyfikacji konieczne jest zweryfikowanie, że nasz zasób Vmsk znajduje się w oczekiwanym stanie.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Tutaj sprawdzamy różne właściwości zasobu Vmsk. Chcemy upewnić się, że nie jest wyłączony, odwrócony ani niepowiązany oraz że posiada właściwą liczbę ścieżek.

### Step 4: Access Each Path and Validate
Zanurzmy się nieco głębiej i sprawdźmy ścieżki w zasobie Vmsk.

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

- Wyodrębniamy trzy konkretne rekordy ścieżek i weryfikujemy ich typy oraz właściwości, aby upewnić się, że spełniają nasze kryteria.

### Step 5: Edit the Vmsk Resource
Teraz przechodzimy do części modyfikacji! Możesz dostosować właściwości zasobu Vmsk w razie potrzeby.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- W tym bloku przełączamy różne właściwości zasobu Vmsk. Ustawiając je na `true`, możemy kontrolować zachowanie maski w pliku PSD.

### Step 6: Modify the Bezier Knot Points
Węzły Béziera są kluczowe dla ścieżek wektorowych. Zmienimy tutaj niektóre wartości.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Dostęp do konkretnych rekordów `BezierKnotRecord` i zmiana ich punktów, aby potencjalnie przekształcić maskę wektorową.

### Step 7: Save the Modified PSD File
Po zakończeniu wszystkich edycji, czas zapisać zmodyfikowany plik PSD.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Ustawiamy ścieżkę dla eksportowanego pliku PSD, a następnie wywołujemy `im.save()`, aby zapisać zmiany w nowym pliku.

### Step 8: Clean Up Resources
Na koniec musimy upewnić się, że prawidłowo zwalniamy obraz, aby zwolnić zasoby.

```java
im.dispose();
```

- Zawsze warto zwalniać wszelkie zasoby po zakończeniu ich użycia. Pomaga to uniknąć wycieków pamięci w aplikacjach.

## Common Issues and Solutions
| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **`VmskResource` nie znaleziono** | Plik PSD nie zawiera warstwy z maską wektorową. | Sprawdź, czy źródłowy PSD ma maskę wektorową lub dodaj ją ręcznie w Photoshopie przed uruchomieniem kodu. |
| **`ArrayIndexOutOfBoundsException` przy dostępie do ścieżki** | Oczekiwana liczba rekordów ścieżek różni się. | Sprawdź `resource.getPaths().length` i odpowiednio dostosuj użycie indeksów. |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji Aspose.PSD. | Zastosuj wersję próbną lub zakupioną licencję używając `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Wycieki pamięci** | Obraz nie jest zwalniany w długotrwałych procesach. | Zawsze wywołuj `im.dispose()` w bloku `finally` lub używaj try‑with‑resources, jeśli jest obsługiwane. |

## Frequently Asked Questions

**Q: Jak dodać nową maskę wektorową do istniejącej warstwy?**  
A: Utwórz `VmskResource`, wypełnij go wymaganymi rekordami ścieżek (np. `BezierKnotRecord`) i dołącz do kolekcji zasobów warstwy.

**Q: Czy mogę bezpośrednio przekonwertować edytowany PSD na PNG bez otwierania Photoshopa?**  
A: Tak — po zapisaniu PSD, wczytaj go ponownie przy użyciu `Image.load()` i wywołaj `im.save("output.png")`, określając format PNG.

**Q: Czy istnieje sposób na automatyzację tego w pipeline CI/CD?**  
A: Oczywiście. Ponieważ proces jest czystą Javą, możesz go osadzić w buildach Maven/Gradle, kontenerach Docker lub dowolnym systemie CI obsługującym Javę.

**Q: Jakie wersje Aspose.PSD są kompatybilne z Java 11+?**  
A: Wszystkie najnowsze wydania (2024‑2025) wspierają Java 8 i wyższe, w tym Java 11, 17 oraz nowsze wersje LTS.

**Q: Czy potrzebna jest licencja do buildów deweloperskich?**  
A: Darmowa licencja ewaluacyjna działa w środowisku deweloperskim i testowym. Do wdrożeń produkcyjnych wymagana jest licencja komercyjna.

---

**Ostatnia aktualizacja:** 2026-02-22  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}