---
title: Obsługa zasobów Vmsk w plikach PSD za pomocą języka Java
linktitle: Obsługa zasobów Vmsk w plikach PSD za pomocą języka Java
second_title: Aspose.PSD API Java
description: Bezproblemowo zarządzaj zasobami Vmsk w plikach PSD za pomocą Aspose.PSD dla Java. Kompleksowy samouczek krok po kroku, idealny zarówno dla programistów, jak i projektantów.
weight: 23
url: /pl/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obsługa zasobów Vmsk w plikach PSD za pomocą języka Java

## Wstęp
Jeśli chodzi o pracę z plikami PSD (dokument programu Photoshop), zarządzanie zasobami ma kluczowe znaczenie, szczególnie podczas integrowania specjalnych funkcji, takich jak zasób Vmsk (maska wektorowa). Zasoby Vmsk mogą pomóc projektantom poprzez dodanie złożonych kształtów wektorowych, umożliwiając im bezproblemowe tworzenie oszałamiającej grafiki. W tym przewodniku zastosujemy praktyczne podejście, aby pokazać, jak obsługiwać zasoby Vmsk w plikach PSD przy użyciu Aspose.PSD dla Java. Niezależnie od tego, czy jesteś programistą chcącym ulepszyć swoją aplikację, czy projektantem poszukującym automatyzacji, ten samouczek przeprowadzi Cię krok po kroku przez proces, ułatwiając jego śledzenie i wdrażanie.
## Warunki wstępne
Zanim zagłębimy się w soczyste szczegóły obsługi zasobów Vmsk, upewnijmy się, że masz wszystko gotowe, aby zapewnić płynne działanie.
### Czego potrzebujesz
-  Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK na swoim komputerze. Jeśli nie, możesz pobrać go ze strony[stronie internetowej Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Biblioteka Aspose.PSD dla Java: Jest to potężna biblioteka do zarządzania plikami PSD. Można go pobrać z[Strona wydania Aspose](https://releases.aspose.com/psd/java/) . Dla tych, którzy chcą wypróbować przed zakupem, możesz również zacząć od[bezpłatna wersja próbna](https://releases.aspose.com/).
- IDE: dowolne IDE dla Java (np. IntelliJ IDEA, Eclipse itp.) będzie działać w tym projekcie.
### Konfigurowanie obszaru roboczego
1. Utwórz nowy projekt Java: Uruchom preferowane IDE i utwórz nowy projekt Java. To jest Twoje miejsce do pracy z kodem.
2. Dodaj bibliotekę Aspose: Po pobraniu biblioteki Aspose dodaj plik jar do bibliotek swojego projektu. Ten krok jest kluczowy, ponieważ pozwala nam wykorzystać wszystkie te wspaniałe funkcje Aspose.PSD.
Po spełnieniu tych wymagań wstępnych możesz rozpocząć tworzenie, modyfikowanie i zarządzanie plikami PSD za pomocą zasobów Vmsk. Przejdźmy od razu do programowania!
## Importuj pakiety
Zanim będziemy mogli pracować nad plikami PSD, musimy zaimportować niezbędne pakiety. To jest szkielet naszego kodu, dający nam dostęp do różnych klas i metod, które oferuje biblioteka Aspose.PSD.
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
Skoro już przygotowaliśmy scenę, czas na działanie! W tej sekcji podzielimy kod na łatwe do wykonania kroki. Poniższe kroki poprowadzą Cię przez czytanie pliku PSD, obsługę zasobu Vmsk, a nawet jego edycję.
## Krok 1: Załaduj plik PSD
Pierwszą rzeczą, którą chcesz zrobić, to załadować plik PSD. Tutaj zaczyna się cała magia.
```java
String dataDir = "Your Document Directory"; // Zaktualizuj tę ścieżkę
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  Ustawiamy`dataDir` do katalogu z plikiem PSD. 
-  Tworzymy ciąg znaków dla`sourceFileName`, łącząc katalog z nazwą pliku PSD.
-  Na koniec ładujemy plik PSD do pliku`PsdImage` obiekt za pomocą`Image.load()`.
## Krok 2: Pobierz zasób Vmsk
Teraz, gdy mamy już załadowany obraz PSD, pobierzmy zasób Vmsk.
```java
VmskResource resource = getVmskResource(im);
```

-  Nazywamy`getVmskResource()` metoda obsługująca wyszukiwanie i pobieranie zasobu Vmsk z obrazu.
## Krok 3: Sprawdź właściwości zasobu Vmsk
Przed przystąpieniem do modyfikacji należy koniecznie sprawdzić, czy nasz zasób Vmsk jest w oczekiwanym stanie.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Tutaj sprawdzamy różne właściwości zasobu Vmsk. Chcemy mieć pewność, że nie jest ona wyłączona, odwrócona ani niepołączona i że ma odpowiednią liczbę ścieżek.
## Krok 4: Uzyskaj dostęp do każdej ścieżki i zatwierdź
Kopiemy trochę głębiej i sprawdźmy ścieżki w zasobie Vmsk.
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

- Wyodrębniamy trzy konkretne rekordy ścieżki i sprawdzamy ich typy i właściwości, aby upewnić się, że spełniają nasze kryteria.
## Krok 5: Edytuj zasób Vmsk
Teraz przechodzimy do części dotyczącej modyfikacji! W razie potrzeby możesz dostosować właściwości zasobu Vmsk.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- W tym bloku przełączamy różne właściwości zasobu Vmsk. Ustawiając je na true możemy kontrolować zachowanie maski w pliku PSD.
## Krok 6: Zmodyfikuj punkty węzła Beziera
Węzły Beziera są krytyczne dla ścieżek wektorowych. Zmieńmy tutaj niektóre wartości.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Mamy dostęp do konkretnych`BezierKnotRecord` ścieżki i zmieniając ich punkty, aby potencjalnie zmienić kształt maski wektorowej.
## Krok 7: Zapisz zmodyfikowany plik PSD
Po zakończeniu wszystkich edycji nadszedł czas na zapisanie zmodyfikowanego pliku PSD. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Ustawiamy ścieżkę do wyeksportowanego pliku PSD i następnie wywołujemy`im.save()` aby zapisać zmiany w tym nowym pliku.
## Krok 8: Oczyść zasoby
Na koniec musimy upewnić się, że prawidłowo pozbyliśmy się obrazu, aby zwolnić zasoby.
```java
im.dispose();
```

- Zawsze dobrą praktyką jest pozbycie się wszelkich zasobów po zakończeniu. Pomaga to uniknąć wycieków pamięci w aplikacjach.
## Wniosek
Gratulacje! Właśnie przeszedłeś przez szczegółowy proces obsługi zasobów Vmsk w plikach PSD przy użyciu Aspose.PSD dla Java. Od załadowania obrazu, pobrania i sprawdzenia zasobu Vmsk, edycji jego właściwości, a następnie zapisania zmodyfikowanego pliku PSD, omówiłeś już najważniejsze kwestie. Dzięki tym umiejętnościom możesz efektywnie zarządzać różnymi zasobami zawartymi w plikach PSD i wykorzystywać je, ulepszając swoje projekty graficzne lub skrypty automatyzacji.
## Często zadawane pytania
### Co to jest zasób Vmsk?
Zasób Vmsk to maska wektorowa w pliku PSD, która umożliwia tworzenie złożonych kształtów wektorowych i funkcje edycji.
### Czy mogę używać Aspose.PSD w projekcie Maven?
Tak, możesz dołączyć Aspose.PSD jako zależność do swojego projektu Maven, używając jego współrzędnych z repozytorium.
### W jakim formacie mogę zapisać zmodyfikowane pliki PSD?
Możesz zapisać je z powrotem jako pliki PSD lub wyeksportować do innych formatów, takich jak PNG, JPEG itp.
### Czy dostępna jest bezpłatna wersja próbna Aspose.PSD?
 Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.PSD, aby przetestować jego funkcje. Odwiedź[bezpłatny link próbny](https://releases.aspose.com/).
### Jak mogę uzyskać wsparcie dla Aspose.PSD?
 Możesz dołączyć do[forum dyskusyjne](https://forum.aspose.com/c/psd/34) celu uzyskania wsparcia i pomocy w rozwiązywaniu problemów.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
